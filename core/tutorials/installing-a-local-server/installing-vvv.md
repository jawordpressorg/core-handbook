<!--
# Installing VVV
-->

# VVV のインストール

<!--
## Overview
-->

## 概要

<!--
Varying Vagrant Vagrants is an open source [Vagrant](https://www.vagrantup.com) configuration focused on [WordPress](https://wordpress.org) development. VVV is [MIT Licensed](https://github.com/varying-vagrant-vagrants/vvv/blob/master/LICENSE).
-->

Varying Vagrant Vagrants は、[WordPress](https://wordpress.org) の開発にフォーカスしたオープンソースの [Vagrant](https://www.vagrantup.com) 設定です。VVV は [MIT ライセンス](https://github.com/varying-vagrant-vagrants/vvv/blob/master/LICENSE)です。

<!--
VVV is ideal for developing themes and plugins as well as for [contributing to WordPress core](https://make.wordpress.org/core/).
-->

VVV は、テーマやプラグインの開発だけでなく、[WordPress コアへの貢献](https://make.wordpress.org/core/)にも最適です。

<!--
This article will walk you through the steps to install VVV on your Mac, PC, or Linux computer.
-->

この記事では、Mac、PC、または Linux コンピューターに VVV をインストールする手順を説明します。

<!--
**For the official VVV instructions, [visit the official VVV documentation here](https://varyingvagrantvagrants.org/docs/en-US/installation/).**
-->

**VVV の公式な説明については、[VVV 公式ドキュメントをご覧ください](https://varyingvagrantvagrants.org/docs/en-US/installation/)。**

<!--
## Running a Contributor Day
-->

## コントリビューターデイの開催

<!--
If you’re running a contributor day for a WordCamp, you should use the contributor day set up script. Setting up a local environment over conference Wifi can cause problems for all, so the script generates a pre-built version.
-->

WordCamp でコントリビューターデイを開催する場合、コントリビューターデイのセットアップスクリプトを使用する必要があります。会議室の無線 LAN 上でローカル環境をセットアップすると、すべての人に問題が発生する可能性があるため、スクリプトは事前にビルドされたバージョンを生成します。

<!--
This pre-built version comes with instructions and a full environment needed for contributor day. These then get copied on to USB drives and handed out at the beginning on contributor day. The entire process can be performed offline using only the contents of the USB drive.
-->

このビルド済みバージョンは、説明書とコントリビューターデイに必要な完全な環境が付属しています。これを USB メモリにコピーして、コントリビューターデイ当日の最初に配布します。USB メモリの内容物だけで、すべてのプロセスをオフラインで実行できます。

<!--
[Click here for information about the VVV contributor day USB drive generator](https://github.com/Varying-Vagrant-Vagrants/CD-USB-Generator)
-->

[VVV コントリビューターデイ USB ドライブジェネレータに関する情報はこちら](https://github.com/Varying-Vagrant-Vagrants/CD-USB-Generator)

<!--
## Installing VVV
-->

## VVV のインストール

<!--
VVV requires recent versions of both [Vagrant](https://www.vagrantup.com/) and [VirtualBox](https://www.virtualbox.org/) (or similar) to be installed.
-->

VVV は、[Vagrant](https://www.vagrantup.com/) と [VirtualBox](https://www.virtualbox.org/) の両方 (または類似のもの) の最新版がインストールされていることが必要です。

<!--
Vagrant is a “tool for building and distributing development environments”. It works with [virtualization](https://en.wikipedia.org/wiki/X86_virtualization) software such as VirtualBox to provide a virtual machine sandboxed from your local environment.
-->

Vagrant は、「開発環境を構築・配布するためのツール」です。VirtualBox などの[仮想化](https://en.wikipedia.org/wiki/X86_virtualization)ソフトウェアと連携し、ローカル環境でサンドボックス化された仮想マシンを提供します。

<!--
### 1\. Downloading VirtualBox
-->

### 1\. VirtualBox のダウンロード

<!--
Navigate to the [Downloads](https://www.virtualbox.org/wiki/Downloads) page on the VirtualBox site. Just like with Vagrant, there are several different download packages available depending on your operating system. Choose the one that’s right for you.
-->

VirtualBox サイトの[ダウンロード](https://www.virtualbox.org/wiki/Downloads)ページに移動します。Vagrant と同様、OS によってダウンロードできるパッケージが異なります。自分に合ったものを選んでください。

<!--
Depending on your operating system, the installer package will vary in size, so it may take a few minutes to download. Once the download is completed, run the installer.
-->

OS によってインストーラパッケージのサイズが異なるので、ダウンロードに数分かかる場合があります。ダウンロードが完了したら、インストーラを実行します。

<!--
### 2\. Downloading Vagrant
-->

### 2\. Vagrant のダウンロード

<!--
Navigate to the [Downloads](https://www.vagrantup.com/downloads.html) page on the Vagrant site. There are a variety of download packages available depending on your operating system, whether that is Mac OS X or Windows. If you’re running Linux, packages are available for 32- and 64-bit Debian and CentOS distributions. Choose the one that’s right for you to download
-->

Vagrant サイトの [ダウンロード](https://www.vagrantup.com/downloads.html) ページに移動します。Mac OS X や Windows など、お使いの OS に応じてさまざまなダウンロードパッケージが用意されています。Linux であれば、32bit と64bit の Debian と CentOS のディストリビューションが用意されています。自分に合ったものを選んでダウンロードしてください。

<!--
Depending on your operating system, the installer package will vary in size, so it may take a few minutes to download. Once the download is completed, run the installer.
-->

OS によってインストーラパッケージのサイズが異なるので、ダウンロードに数分かかる場合があります。ダウンロードが完了したら、インストーラを実行します。

<!--
### 3\. Grabbing VVV
-->

### 3\. VVV のインストール

<!--
The official [official instructions for installing VVV are here](https://varyingvagrantvagrants.org/docs/en-US/installation/).
-->

公式の [VVV のインストール方法はこちら](https://varyingvagrantvagrants.org/docs/en-US/installation/)をご覧ください。

<!--
### 4\. Start up VVV
-->

### 4\. VVV のスタート

<!--
*   In a command prompt, change to the directory VVV is installed to. You can sometimes drag and drop the folder on to the terminal as a fast way to type the path of the directory. **If you are on Windows this must be a ran with elevated administrator privileges**.
*   Start the VVV environment with `vagrant up --provision`
*   Be patient as the magic happens. This could take a while on the first run as your local machine downloads the required files.
*   Watch as the script ends, as an administrator or `su` ***password may be required*** to properly modify the hosts file on your local machine.
*   Do not use `sudo` with the `vagrant` command.
-->

* コマンドプロンプトで、VVV がインストールされているディレクトリに移動します。このディレクトリのパスは、ターミナルにフォルダーをドラッグ & ドロップすることで、すばやく入力できる場合があります。**Windows の場合、管理者権限で実行する必要があります。**
* VVV 環境を `vagrant up --provision` で起動します。
* 魔法が起こるまで、しばらくお待ちください。初回実行時は、ローカルマシンが必要なファイルをダウンロードするため、しばらく時間がかかる可能性があります。
* ローカルマシンの hosts ファイルを正しく変更するために、管理者または `su` ***パスワードが必要な場合があります***ので、スクリプトが終了まで確認してください。
* `vagrant` コマンドで `sudo` を使用しないでください。

<!--
Once the provisioning script has run its course, visit the VVV dashboard at  [http://vvv.test](http://vvv.test) in your browser. You should see a listing of all the sites VVV created, as well as links to other administration-related tools:
-->

プロビジョニングスクリプトの実行が完了したら、ブラウザで [http://vvv.test](http://vvv.test) にある VVV ダッシュボードにアクセスします。VVV が作成したすべてのサイトのリストと、他の管理に関連したツールへのリンクが表示されるはずです。

<!--
*   [http://one.wordpress.test/](http://one.wordpress.test/) A standard WP install, useful for building plugins, testing things, etc.
*   [http://two.wordpress.test/](http://two.wordpress.test/) A second standard WP install, useful for building plugins, testing things, etc.
-->

* [http://one.wordpress.test/](http://one.wordpress.test/) 標準的な WP インストールで、プラグインの構築やテストなどに便利です。
* [http://two.wordpress.test/](http://two.wordpress.test/) 2番目の標準的な WP インストールで、プラグインの構築やテストなどに便利です。

<!--
### 5\. Enabling Trunk and The Meta Environment
-->

### 5\. Trunk とメタ環境を有効化する

<!--
There are also 2 environments that are disabled by default:
-->

また、デフォルトで無効になっている環境が2つあります。

<!--
*   [http://trunk.wordpress.test/](http://trunk.wordpress.test/) An svn-based WordPress Core trunk dev setup, useful for contributor days, Trac tickets, patches, general core contributing, etc.
*   [http://wpmeta.test](http://wpmeta.test) A collection of sites for contributing to WordPress.org and WordCamps
-->

*   [http://trunk.wordpress.test/](http://trunk.wordpress.test/) svn ベースの WordPress コア trunk 開発セットアップで、コントリビューターデイ、Trac チケット、パッチ、一般的なコア貢献などに便利です。
*   [http://wpmeta.test](http://wpmeta.test) WordPress.org や WordCamp に貢献するためのサイト集です。

<!--
To enable these, open `vvv-custom.yml`, find `skip_provisioning: true` for the desired site, and change `true` to `false`. Save the file and reprovision to apply changes using `vagrant reload --provision`. This will take some time to run.
-->

これらを有効にするには、`vvv-custom.yml` を開き、目的のサイトの `skip_provisioning: true` を見つけて、`true` を `false` に変更します。ファイルを保存して、`vagrant reload --provision` を使って、変更を適用するために再ビジョニングします。これは実行に時間がかかります。

<!--
You can also setup additional sites, [to learn how to do that click here](https://varyingvagrantvagrants.org/docs/en-US/adding-a-new-site/).
-->

また、追加のサイトを設定できます。[その方法はこちらをご覧ください](https://varyingvagrantvagrants.org/docs/en-US/adding-a-new-site/)。

<!--
### 6\. Create a GitHub Repo (optional)
-->

### 6\. GitHub リポジトリの作成 (オプション)

<!--
Pull requests on GitHub provide a convenient way to receive feedback and also to share the patch for your contributions. You can add “`.diff`” to any pull request URL and GitHub will return a diff file which you can then attach to a Trac ticket. You can also just add a link to the pull request in a Trac ticket comment. There is currently no Git repo clone for `develop.git.wordpress.org` located on GitHub, so you have to set this up yourself:
-->

GitHub でのプルリクエストはフィードバックを受けたり、パッチを共有したりするのに便利な方法です。プルリクエストの URL に「`.diff`」を追加すると、GitHub が diff ファイルを返してくれるので、それを Trac チケットに添付できます。Trac のチケットのコメントにプルリクエストへのリンクも追加できます。現在、`develop.git.wordpress.org` の Git リポジトリのクローンは GitHub に存在しないので、自分でセットアップする必要があります。

<!--
1.  Have VVV set up (above).
2.  Swap out your SVN repo with a Git one in VVV via: `vagrant ssh -c /srv/www/wordpress-trunk/bin/develop_git`
3.  [Create](https://github.com/new) an empty “wordpress-develop” on GitHub (you can name this however you like).
4.  Run these commands to set this new repo as your origin remote: `cd ...vvv/www/wordpress-trunk/public_html && git remote set-url origin https://github.com/YOURNAME/wordpress-develop.git && git remote add upstream git://develop.git.wordpress.org/`
5.  Check out the master branch: `git checkout master`
6.  Create a feature branch based on the Trac ticket (e.g. 12345) you want to work on: `git checkout -b trac-12345`
7.  Add commits for your fixes and `git push` (see also [Caching your GitHub password in Git](https://help.github.com/articles/caching-your-github-password-in-git/) to prevent having to re-enter your GitHub password each time).
8.  Go to GitHub and open a pull request to your `master` branch.
9.  With the newly-created pull request in hand, copy the URL and paste it into a new comment on WordPress Trac and solicit for feedback. Ideally you should also attach a diff of your patch, and again you can do this just by adding “`.diff`” to any pull request URL, for example: [https://github.com/xwp/wordpress-develop/pull/61.diff](https://github.com/xwp/wordpress-develop/pull/61.diff)
-->

1.  VVV をセットアップする (上記参照)。
2.  VVV で、`vagrant ssh -c /srv/www/wordpress-trunk/bin/develop_git` によって SVN リポジトリと Git リポジトリを入れ替えます。
3.  GitHub 上に空の「wordpress-develop」を[作成](https://github.com/new)します (この名前は好きなものをつけてください)。
4.  次のコマンドを実行して、この新しいリポジトリをオリジンリモートとして設定します。`cd ...vvv/www/wordpress-trunk/public_html && git remote set-url origin https://github.com/YOURNAME/wordpress-develop.git && git remote add upstream git://develop.git.wordpress.org/`.
5.  master ブランチをチェックアウトします。`git checkout master`
6.  作業したい Trac チケット (例: 12345) にもとづいて、feature ブランチを作成します。`git checkout -b trac-12345`
7.  修正のコミットを追加して、`git push` します (GitHub のパスワードを再入力することを防ぐために、[Git で GitHub パスワードをキャッシュする](https://help.github.com/articles/caching-your-github-password-in-git/) も参照してください)。
8.  GitHub にアクセスし、`master` ブランチへのプルリクエストをオープンします。
9.  作成したプルリクエストの URL をコピーして WordPress Trac の新しいコメントに貼り付けて、フィードバックを求めます。パッチの diff を添付するのが理想的ですが、これはプルリクエストの URL に「`.diff`」を追加するだけです。例: [https://github.com/xwp/wordpress-develop/pull/61.diff](https://github.com/xwp/wordpress-develop/pull/61.diff)
