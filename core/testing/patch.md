<!--
# Testing a Patch
-->

# パッチをテストする

<!--
Alert: This page is under construction and may contain inaccurate information. Want to help fix it? Ping the [#docs](https://make.wordpress.org/core/tag/docs/) channel in WordPress Slack.
-->

\[alert\]このページは作成中のため、不正確な情報が含まれている可能性があります。修正を手伝ってみませんか ? WordPress Slack の [#docs](https://make.wordpress.org/core/tag/docs/) チャンネルでお知らせください。\[/alert\]

<!--
Testing patches is an important part of ensuring the quality of WordPress releases.
-->

パッチのテストは、WordPress のリリースの品質を保証する重要なパートです。

<!--
## Setting up without VVV
-->

## VVV を使用しない設定

<!--
If you use VVV, skip to the section below.
-->

VVV を使用している場合は、以下のセクションはスキップしてください。

<!--
Grunt is a command runner that allows you to test patches that have been uploaded to Trac. To use Grunt, follow these steps:
-->

Grunt は、Trac にアップロードされたパッチをテストするためのコマンドランナーです。Grunt を使うには以下のステップに従ってください:

<!--
1.  Install `nodejs` and `npm` to your development environment.
2.  Clone the *develop* WordPress repository located at https://develop.svn.wordpress.org/
3.  Run `npm install` to get all the dependencies.
4.  Run `npm run grunt build` to get the fully-built version
5.  Setup your server to use `/build` as the root (varies depending on how your development environment is setup).
6.  In order for changes to `/src` to be reflected in `/build`, run `npm run grunt watch` while you are working.
7.  **Alternatively**, you can [use /src as your document root](https://make.wordpress.org/core/2018/12/24/build-tools-weve-enabled-running-wordpress-from-src-again/), which may be much more convenient for PHP\-focused development. You’ll need to run `npm run grunt build -- --dev` once, but after that you don’t need `npm run grunt watch` at all, unless you’re changing JavaScript/CSS. If you are, then use `npm run grunt watch -- --dev` instead of `npm run grunt watch`.
-->

1.  開発環境に `nodejs` と `npm` をインストールします。
2.  https://develop.svn.wordpress.org/ にある *develop* WordPress リポジトリをクローンします。
3.  `npm install` を実行して、すべての依存関係を取得します。
4.  `npm run grunt build` を実行して、完全にビルドされたバージョンを取得します。
5.  サーバーのルートとして `/build` を使うように設定します (開発環境の設定によって異なります)。
6.  `src` への変更を `/build` に反映させるために、作業中に `npm run grunt watch` を実行する。
7.  **別の方法として**、[/src をドキュメントルートとして使う](https://make.wordpress.org/core/2018/12/24/build-tools-weve-enabled-running-wordpress-from-src-again/)こともできます。これは、PHP を中心とした開発には便利です。`npm run grunt build -- --dev` を一度実行する必要がありますが、その後は JavaScript/CSS を変更しない限り、`npm run grunt watch` はまったく必要ありません。その場合は、`npm run grunt watch` の代わりに `npm run grunt watch -- --dev` を使用してください。

<!--
## Setting up with VVV
-->

## VVV を使用した設定

<!--
VVV includes support for [WP Core Development](https://github.com/Varying-Vagrant-Vagrants/custom-site-template-develop/), and you can find the settings on the [config.yml](https://github.com/Varying-Vagrant-Vagrants/VVV/blob/develop/config/default-config.yml) file.
-->

VVV は [WP コア開発](https://github.com/Varying-Vagrant-Vagrants/custom-site-template-develop/)をサポートしており、[config.yml](https://github.com/Varying-Vagrant-Vagrants/VVV/blob/develop/config/default-config.yml) ファイルに設定があります。

<!--
If you use VVV, a site can be added that contains a full [WP Core development build](https://github.com/Varying-Vagrant-Vagrants/custom-site-template-develop/). If you open `config/config.yml` there is a site pre-pepared for this, but disabled out of the box. Look for `wordpress-trunk` and change `skip_provisioning` from `true` to `false`, it should look like this:
-->

VVV を使用する場合、完全な [WP コア開発ビルド](https://github.com/Varying-Vagrant-Vagrants/custom-site-template-develop/)を含むサイトを追加できます。`config/config.yml` を開くと、このためのサイトがあらかじめ用意されていますが、そのままでは無効になっています。`wordpress-trunk` を探し、`skip_provisioning` を `true` から `false` に変更すると、以下のようになります:

```yaml
  wordpress-trunk:
    skip_provisioning: true
    description: "An git based WP Core trunk dev setup, useful for contributor days, Trac tickets, patches"
    repo: https://github.com/Varying-Vagrant-Vagrants/custom-site-template-develop.git
    hosts:
      - trunk.wordpress.test
    custom:
      vcs: git # using 'svn' will force this vcs
```

<!--
Once saved, reprovision with `vagrant up --provision`. VVV will download and prepare a developer environment for working on core and testing. This new site will be located in the `www/wordpress-trunk/public_html` folder.
-->

保存したら、`vagrant up --provision` で再プロビジョニングします。VVV は、コアでの作業とテストのための開発環境をダウンロードして準備します。この新しいサイトは `www/wordpress-trunk/public_html` フォルダーに配置されます。

<!--
Inside the site there will be 2 folders, `src` and `build`. Changes made in the `src` folder are processed by a tool called `grunt` and put in the `build` folder. This happens automatically by running the command `npm run grunt watch` in the `www/wordpress-trunk/public_html` folder. For example:
-->

サイト内には `src` と `build` の2つのフォルダーがあります。`src` フォルダーで行われた変更は `grunt` というツールで処理され、`build` フォルダーに格納されます。これは `www/wordpress-trunk/public_html` フォルダーで `npm run grunt watch` コマンドを実行することで自動的に行わます。例:

```bash
vagrant ssh
cd /srv/www/wordpress-trunk/public_html
npm run grunt watch
```

<!--
## Testing with Grunt
-->

## Grunt を使用したテスト

<!--
Now that [Grunt](https://make.wordpress.org/core/handbook/tutorials/working-with-patches/#creating-and-applying-patches-with-grunt) is setup, type in `npm run grunt patch:####`, replacing `####` with either a ticket number from Trac or a patch URL. This will download the patch and apply the changes to your development environment.
-->

[Grunt](https://ja.wordpress.org/team/handbook/core/tutorials/working-with-patches/#creating-and-applying-patches-with-grunt) のセットアップが完了したら、`npm run grunt patch:####` と入力し、`###` を Trac のチケット番号かパッチの URL に置き換えてください。これでパッチがダウンロードされ、開発環境に変更が適用されます。

<!--
Note: If you receive a `Cannot find module 'grunt-cli/bin/grunt'` error, run the following and then try again:
-->

注: `Cannot find module 'grunt-cli/bin/grunt'` エラーが表示された場合は、以下を実行してから再度試してください:

`rm -rf node_modules && npm install`

<!--
Ready to test your environment? Use `npm run grunt test` to automatically run automated tests. Note that this step requires PHPUnit to be installed.
-->

環境をテストする準備はできましたか ? `npm run grunt test` を使って自動テストを実行します。このステップでは、PHPUnit がインストールされている必要があることに注意してください。

<!--
If you’re a committer, be sure to run `npm run grunt precommit` before committing code, *especially* code that touches anything on the front-end (CSS/JS).
-->

もしあなたがコミッターなら、コードをコミットする前に必ず `npm run grunt precommit` を実行してください。

コミッターの場合は、コード、**特に**フロントエンド (CSS/JS) に関わるコードをコミットする前に、必ず `npm run grunt precommit` を実行してください。

<!--
## Testing without Grunt
-->

## Grunt を使用しないテスト

<!--
See [https://make.wordpress.org/core/handbook/tutorials/working-with-patches/#applying-a-patch-with-the-command-line](https://make.wordpress.org/core/handbook/tutorials/working-with-patches/#applying-a-patch-with-the-command-line)
-->

[https://ja.wordpress.org/team/handbook/core/tutorials/working-with-patches/#applying-a-patch-with-the-command-line](https://ja.wordpress.org/team/handbook/core/tutorials/working-with-patches/#applying-a-patch-with-the-command-line) を参照してください
