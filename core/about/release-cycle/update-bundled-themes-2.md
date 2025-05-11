<!--
# Updating Bundled Theme Versions
-->

# バンドルテーマのバージョン更新

<!--
## The Process
-->

## プロセス

<!--
Every release, if there have been any changes in a bundled theme, we ship a new version to the WordPress.org theme directory. What follows are detailed steps to update the themes.
-->

リリースごとに、バンドルされているテーマに変更があった場合、WordPress.org のテーマディレクトリに新しいバージョンを配布します。以下は、テーマを更新するための詳細な手順です。

<!--
1.  Read each theme’s changelog in Trac, and create a changelog file with the highlights (used in Trac tickets, both core and theme review). The changelog should start at the last version of the theme released.
<<<<<<< HEAD:core/about/release-cycle/update-bundled-themes-2.md
    *   [Twenty Twenty-Four log](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentytwentyfour/)
    *   [Twenty Twenty-Three log](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentytwentythree/)
    *   [Twenty Twenty-Two log](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentytwentytwo/)
    *   [Twenty Twenty-One log](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentytwentyone/)
    *   [Twenty Twenty log](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentytwenty/)
    *   [Twenty Nineteen log](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentynineteen/)
    *   [Twenty Seventeen log](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentyseventeen/)
    *   [Twenty Sixteen log](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentysixteen/)
    *   [Twenty Fifteen log](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentyfifteen/)
    *   [Twenty Fourteen log](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentyfourteen/)
    *   [Twenty Thirteen log](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentythirteen/)
    *   [Twenty Twelve log](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentytwelve/)
    *   [Twenty Eleven log](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentyeleven/)
    *   [Twenty Ten log](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentyten/)
2.  Create a new core Trac ticket (like [#54783](https://core.trac.wordpress.org/ticket/54783)) to bump the POT and versions for each theme.
3.  Locally, check out the current version of the theme from the WordPress.org theme directory, e.g., the largest number in each of these directories:
    *   [Twenty Twenty-Four](https://themes.svn.wordpress.org/twentytwentyfour/)
    *   [Twenty Twenty-Three](https://themes.svn.wordpress.org/twentytwentythree/)
=======
    *   [Twenty Twenty-Two](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentytwentyone/)
    *   [Twenty Twenty-One](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentytwentyone/)
    *   [Twenty Twenty](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentytwenty/)
    *   [Twenty Nineteen](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentynineteen/)
    *   [Twenty Seventeen](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentyseventeen/)
    *   [Twenty Sixteen](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentysixteen/)
    *   [Twenty Fifteen](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentyfifteen/)
    *   [Twenty Fourteen](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentyfourteen/)
    *   [Twenty Thirteen](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentythirteen/)
    *   [Twenty Twelve](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentytwelve/)
    *   [Twenty Eleven](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentyeleven/)
    *   [Twenty Ten](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentyten/)
2.  Create a new core Trac ticket (like [#54783](https://core.trac.wordpress.org/ticket/54783)) to bump the POT and versions for each theme.
3.  Locally, check out the current version of the theme from the WordPress.org theme directory, e.g., the largest number in each of these directories:
>>>>>>> main:core/about/release-cycle/update-bundled-themes.md
    *   [Twenty Twenty-Two](https://themes.svn.wordpress.org/twentytwentytwo/)
    *   [Twenty Twenty-One](https://themes.svn.wordpress.org/twentytwentyone/)
    *   [Twenty Twenty](https://themes.svn.wordpress.org/twentytwenty/)
    *   [Twenty Nineteen](https://themes.svn.wordpress.org/twentynineteen/)
    *   [Twenty Seventeen](https://themes.svn.wordpress.org/twentyseventeen/)
    *   [Twenty Sixteen](https://themes.svn.wordpress.org/twentysixteen/)
    *   [Twenty Fifteen](https://themes.svn.wordpress.org/twentyfifteen/)
    *   [Twenty Fourteen](https://themes.svn.wordpress.org/twentyfourteen/)
    *   [Twenty Thirteen](https://themes.svn.wordpress.org/twentythirteen/)
    *   [Twenty Twelve](https://themes.svn.wordpress.org/twentytwelve/)
    *   [Twenty Eleven](https://themes.svn.wordpress.org/twentyeleven/)
    *   [Twenty Ten](https://themes.svn.wordpress.org/twentyten/)
4.  Compare with a diff tool to the theme versions in core trunk, is there anything to test or note specifically? Any big unexpected changes?
5.  Test! Load the themes on all recent versions of WordPress (five back is a good place to start). Run the [Theme Check plugin](https://wordpress.org/plugins/theme-check/), and check for any errors or things we didn’t catch in the core cycle.
6.  Bump the theme versions by 0.1 in core, in each stylesheet.
7.  For themes with a `package.json` and/or `composer.json` file, the `version` should be bumped by 0.1. The `package-lock.json` must also be updated by running `npm install`.
8.  Update “Tested up to” in each readme.
9.  If you’re updating Twenty Ten or Twenty Eleven, wait for the POT update for each theme to be committed, then proceed to make the ZIP packages (a committer is needed to trigger the POT files update). This can be done like this example `php makepot.php wp-theme ../../src/wp-content/themes/twentyeleven twentyeleven.pot`. Run that from the `tools/i18n` directory. For all other default themes, translations are managed by WordPress.org GlotPress, outside of the theme. So this step isn’t necessary for Twenty Twelve and later.
10.  Run the theme build script when one is present (currently Twenty Nineteen, Twenty Twenty, and Twenty Twenty-One). Some themes copy the version into generated files (RTL stylesheets, etc.).
11.  Prepare the new version of each theme.
    *   `svn export` from core repository to a temporary location on your local hard drive.
    *   Do another quick diff with the previous version for a final sanity check.
    *   Zip it: `zip -r [name].zip name` **(Be sure the file name is the same as the theme directory path, otherwise the theme repository will consider the theme new on upload.)**
12.  All contributors with WordPress Core commit access are able to upload new versions of the default themes to WordPress.org through the [theme uploader](https://wordpress.org/themes/getting-started/). **Note**: theme updates will go live *automatically* if manual intervention is not taken beforehand by the theme or meta team. If this is not desired, contact them first to prevent the go-live process. If needed: note in the ticket, “Do not approve yet, please. We’d like to coordinate with the core release*.”*
13.  Ping the release lead to coordinate with the main release process. The updates should be approved automatically. [@Otto42](https://profiles.wordpress.org/Otto42/) can help if anything goes wrong, and the release should know when everything is uploaded and live.
-->

1.  Trac で各テーマの変更履歴を読み、ハイライトを含む変更履歴ファイルを作成します (Trac チケット、コアとテーマレビューの両方で使用します)。変更履歴はテーマがリリースされた最後のバージョンから始めてください。
    *   [Twenty Twenty-Two](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentytwentyone/)
    *   [Twenty Twenty-One](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentytwentyone/)
    *   [Twenty Twenty](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentytwenty/)
    *   [Twenty Nineteen](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentynineteen/)
    *   [Twenty Seventeen](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentyseventeen/)
    *   [Twenty Sixteen](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentysixteen/)
    *   [Twenty Fifteen](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentyfifteen/)
    *   [Twenty Fourteen](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentyfourteen/)
    *   [Twenty Thirteen](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentythirteen/)
    *   [Twenty Twelve](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentytwelve/)
    *   [Twenty Eleven](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentyeleven/)
    *   [Twenty Ten](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentyten/)
2.  各テーマの POT とバージョンを更新するために、新しいコア Trac チケット (例: [#54783](https://core.trac.wordpress.org/ticket/54783)) を作成します。
3.  ローカルで、WordPress.org のテーマディレクトリからテーマの現在のバージョンをチェックします。たとえば、これらの各ディレクトリの中で最も大きい番号のものをチェックします:
    *   [Twenty Twenty-Two](https://themes.svn.wordpress.org/twentytwentytwo/)
    *   [Twenty Twenty-One](https://themes.svn.wordpress.org/twentytwentyone/)
    *   [Twenty Twenty](https://themes.svn.wordpress.org/twentytwenty/)
    *   [Twenty Nineteen](https://themes.svn.wordpress.org/twentynineteen/)
    *   [Twenty Seventeen](https://themes.svn.wordpress.org/twentyseventeen/)
    *   [Twenty Sixteen](https://themes.svn.wordpress.org/twentysixteen/)
    *   [Twenty Fifteen](https://themes.svn.wordpress.org/twentyfifteen/)
    *   [Twenty Fourteen](https://themes.svn.wordpress.org/twentyfourteen/)
    *   [Twenty Thirteen](https://themes.svn.wordpress.org/twentythirteen/)
    *   [Twenty Twelve](https://themes.svn.wordpress.org/twentytwelve/)
    *   [Twenty Eleven](https://themes.svn.wordpress.org/twentyeleven/)
    *   [Twenty Ten](https://themes.svn.wordpress.org/twentyten/)
4.  コア trunk のテーマバージョンと差分ツールで比較してみて、特にテストすべき点や注意すべき点はありませんか ? 予期せぬ大きな変更はありませんか ?
5.  テストしましょう ! WordPress のすべての最新バージョンでテーマを読み込みます (5つ前のバージョンから始めるのが良いでしょう)。[Theme Check プラグイン](https://wordpress.org/plugins/theme-check/)を実行し、エラーやコアサイクルで見つけられなかったものをチェックします。
6.  コアのそれぞれのスタイルシートで、テーマのバージョンを0.1上げます。
7.  コアのそれぞれの `package.json` と `package-lock.json` ファイルで、テーマのバージョンを0.1ずつ上げます。
8.  それぞれの readme の「Tested up to」を更新します。
9.  Twenty Ten または Twenty Eleven を更新する場合は、各テーマの POT の更新がコミットされるのを待ってから、ZIP パッケージの作成に進んでください (POT ファイルのアップデートをトリガーするにはコミッターが必要です)。これは次の例のように行うことができます: `php makepot.php wp-theme ../../src/wp-content/themes/twentyeleven twentyeleven.pot`。これを `tools/i18n` ディレクトリから実行します。他のすべてのデフォルトテーマでは、翻訳は WordPress.org の GlotPress によって管理されています。そのため、Twenty Twelve 以降ではこのステップは必要ありません。
10.  テーマにビルドスクリプトがある場合は、それを実行します (今のところ Twenty Nineteen、Twenty Twenty、Twenty Twenty-One)。テーマによっては、生成されたファイル (RTL スタイルシートなど) にバージョンをコピーします。
11.  それぞれのテーマの新しいバージョンを準備します。
    *   コアリポジトリからローカルハードディスクの一時的な場所に `svn export` します。
    *   最終確認のために、前のバージョンとの簡単な差分をもう一度チェックします。
    *   Zip で圧縮します: `zip -r [name].zip name` **(ファイル名がテーマディレクトリのパスと同じであることを確認してください。そうでないと、テーマリポジトリはアップロード時に新しいテーマとみなします)**
12.  WordPress Core のコミットアクセス権を持つすべての貢献者は、[theme uploader](https://wordpress.org/themes/getting-started/) を通じて WordPress.org にデフォルトテーマの新バージョンをアップロードできます。**注意**: テーマのアップデートは、テーマチームまたはメタチームによる手動での介入が事前に行われない場合、*自動的に*開始されます。これを望ましくない場合は、稼働開始プロセスを止めるために、まずは彼らに連絡してください。必要であれば、チケットに「コアリリースと調整したいので、まだ承認しないでください」と記載しておきましょう。
13.  リリースリードに連絡し、メインのリリースプロセスを調整します。アップデートは自動的に承認されるはずです。[@Otto42](https://profiles.wordpress.org/Otto42/) は何か問題が発生したときに助けてくれるでしょう。リリースはすべてがアップロードされ、有効になったときにわかるはずです。

<!--
## Tips
-->

## ヒント

<!--
*   If a major version of WordPress is also being released with a new bundled theme, the oldest theme being bundled needs to be removed from the build script. **To keep packages sizes down, only the 3 most recent default themes should be included in WordPress packages.**
*   If a theme has any code changes, that means it should get a version number bump and changelog update. Not updating the version number means a new version of the theme can’t be uploaded to the theme directory.
*   Sometimes when looking at the diff of changes after a theme is uploaded, you may notice image or font files showing up as changed when they haven’t been changed. This is a [Trac oddity](https://wordpress.slack.com/archives/core-themes/p1471287983000406).
*   All default themes are marked as special cases on WordPress.org Themes Trac. Themes marked as special still show the theme check errors, but they upload anyway.
-->

*   WordPress のメジャーバージョンが新しいバンドルテーマとともにリリースされる場合、バンドルされている最も古いテーマをビルドスクリプトから削除する必要があります。**パッケージのサイズを小さくするために、WordPress のパッケージには最新のデフォルトテーマ3つだけを含めるべきです。**
*   テーマにコード変更があった場合、バージョン番号と変更履歴を更新する必要があります。バージョン番号を更新しないということは、新しいバージョンのテーマをテーマディレクトリにアップロードできないということです。
*   テーマがアップロードされた後に変更点の diff を見ると、画像ファイルやフォントファイルが変更されていないのに変更されたように表示されることがあります。これは [Trac の変わった振る舞い](https://wordpress.slack.com/archives/core-themes/p1471287983000406)です。
*   WordPress.org の Themes Trac では、デフォルトのテーマはすべて特殊なケースとしてマークされています。特殊とマークされたテーマはまだテーマチェックエラーを表示しますが、いずれにせよアップロードされます。
