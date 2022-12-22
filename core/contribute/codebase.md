<!--
# The WordPress Codebase
-->

# WordPress のコードベース

<!--
WordPress is managed by a centralized version control system called [Subversion](http://subversion.tigris.org/). A mirror of this repository is also available via [Git](http://git-scm.com/), a distributed VCS.
-->

WordPress は、[Subversion](http://subversion.tigris.org/) という集中型バージョン管理システムで管理されています。このリポジトリのミラーは、分散型 VCS である [Git](http://git-scm.com/) を介して利用することもできます。

<!--
The WordPress codebase can be accessed in a number of ways: using Subversion, using Git, through Trac (the bug tracker), and via direct download:
-->

WordPress のコードベースには、Subversion、Git、Trac (バグトラッカー)、直接のダウンロードなど、さまざまな方法でアクセスできます。

<!--
*   **Subversion:** The repository is located at [https://develop.svn.wordpress.org/](https://develop.svn.wordpress.org/). The main development branch – called trunk– is [https://develop.svn.wordpress.org/trunk](https://develop.svn.wordpress.org/trunk).
*   **Git:** The repository is located at git://develop.git.wordpress.org/. There is also a [mirror of the WordPress repository on Github](https://github.com/wordpress/wordpress), though issues and pull requests on Github are not currently accepted.
*   **Trac:** The repository can be viewed through the browser at [https://core.trac.wordpress.org/browser/](https://core.trac.wordpress.org/browser/). A log of changesets can be viewed at [https://core.trac.wordpress.org/log/](https://core.trac.wordpress.org/log/).
*   **Download:** The latest stable version of WordPress can be downloaded at [https://wordpress.org/latest.zip](https://wordpress.org/latest.zip). The latest nightly build (2300 GMT) can be found at [https://wordpress.org/nightly-builds/wordpress-latest.zip](https://wordpress.org/nightly-builds/wordpress-latest.zip).
-->

*   **Subversion:** リポジトリは [https://develop.svn.wordpress.org/](https://develop.svn.wordpress.org/) にあります。メインの開発ブランチ (trunk と呼ばれます) は [https://develop.svn.wordpress.org/trunk](https://develop.svn.wordpress.org/trunk) にあります。
*   **Git:** リポジトリは git://develop.git.wordpress.org/ にあります。また、[Github 上の WordPress リポジトリのミラー](https://github.com/wordpress/wordpress)もありますが、GitHub 上の issue およびプルリクエストは現在受け付けていません。
*   **Trac:** リポジトリは [https://core.trac.wordpress.org/browser/](https://core.trac.wordpress.org/browser/) でブラウザから見ることができます。変更点のログは [https://core.trac.wordpress.org/log/](https://core.trac.wordpress.org/log/) で見ることができます。
*   **ダウンロード:** WordPress の最新安定版は、[https://wordpress.org/latest.zip](https://wordpress.org/latest.zip) でダウンロードできます。最新のナイトリービルド (2300 GMT) は、[https://wordpress.org/nightly-builds/wordpress-latest.zip](https://wordpress.org/nightly-builds/wordpress-latest.zip) で確認できます。

<!--
## How Code In WordPress Is Organized
-->

## WordPress コードの構成

<!--
If you are using the “develop” repository, as mentioned above, the core codebase is in the `src` directory. A downloaded package serves a “built” version of this directory, thus placing these files in the root. The codebase consists of around 1000 files and directories.
-->

「develop」リポジトリを使用している場合、コアのコードベースは前述の通り `src` ディレクトリにあります。ダウンロードされるパッケージはこのディレクトリの「ビルド」バージョンを提供し、そのためこれらのファイルはルートに配置されます。コードベースは、約1000のファイルやディレクトリから構成されています。

<!--
Initial bootstrap files, such as `index.php`, `wp-load.php`, `wp-blog-header.php`, and `wp-settings.php`, appear in this `src` directory. Special handlers such as the XML-RPC, trackback, and comment submission endpoints, are also in the root.
-->

`index.php`、`wp-load.php`、`wp-blog-header.php`、`wp-settings.php` などの初期起動のためのファイルは、この `src` ディレクトリに配置されます。XML-RPC、トラックバック、コメント投稿のエンドポイントなどの特別なハンドラもルートにあります。

<!--
The remaining files are divided into three distinct directories: **wp-admin**, **wp-includes**, and, to some extent, **wp-content**.
-->

残りのファイルは、3つの異なるディレクトリに分けられています。**wp-admin**、**wp-includes**、そして **wp-content** です。

### wp-content

<!--
The **wp-content** directory consists of user-defined and site-specific files, including themes, plugins, and uploads. The repository only contains a **wp-content** directory for the bundled plugins (e.g. Hello Dolly) and themes (e.g. Twenty Fifteen).
-->

**wp-content** ディレクトリは、テーマ、プラグイン、アップロードなど、ユーザー定義のファイルやサイト固有のファイルで構成されています。リポジトリには、バンドルされているプラグイン (例: Hello Dolly) とテーマ (例: Twenty Fifteen) 用の **wp-content** ディレクトリしかありません。

### wp-includes

<!--
The **wp-includes** directory consists of the primary core and third-party libraries for WordPress. Many of these files are loaded as the application is bootstrapped.
-->

**wp-includes** ディレクトリは、WordPress の主要なコアとサードパーティライブラリで構成されています。これらのファイルの多くは、アプリケーションを起動する際に読み込まれます。

<!--
The files in **wp-includes** go by a (mostly) standard set of prefixes and suffixes:
-->

**wp-includes** に含まれるファイルは、(ほぼ) 標準的な接頭辞と接尾辞のセットで扱われます。

<!--
*   `class-*.php` – PHP classes. Some of these are external libraries.
*   `ms-*.php` – Code specific to WordPress multisite functionality.
*   `default-*.php` – Code that implements or defines default functionality, namely constants, widgets, and filters.
*   `*deprecated.php` – Functions which are deprecated.
*   `*-template.php` – Template functions for the relevant API.
-->

*   `class-*.php` – PHP クラス。一部、外部ライブラリもあります。
*   `ms-*.php` – WordPressのマルチサイト機能に特化したコードです。
*   `default-*.php` – デフォルトの機能を実装または定義するコード。すなわち定数、ウィジェット、およびフィルターです。
*   `*deprecated.php` – 非推奨となった機能です。
*   `*-template.php` – 関連する API のテンプレート機能です。

<!--
The files in **wp-admin/includes** follow similar naming conventions.
-->

**wp-admin/includes** にあるファイルも、同様の命名規則に従っています。

### wp-admin

<!--
The **wp-admin** directory contains the code powering the administration area of WordPress. The primary bootstrap is `wp-admin/admin.php`. Other special files include `admin-header.php` and `admin-footer.php`, the AJAX handler `admin-ajax.php`, and the generic POST handler `admin-post.php`. Most of the files in the **wp-admin** directory are pages in the WordPress admin interface.
-->

**wp-admin** ディレクトリには、WordPress の管理エリアを動作させるためのコードが含まれています。主なブートストラップは `wp-admin/admin.php` です。その他の特別なファイルとしては、`admin-header.php` と `admin-footer.php` 、AJAX ハンドラである `admin-ajax.php`、一般的な POST ハンドラである `admin-post.php` があります。**wp-admin** ディレクトリにあるファイルのほとんどは、WordPress の管理画面のページのためのものです。

<!--
The **wp-admin/includes** directory consists of the primary core and third-party libraries available and used in the administration area. Some of these are loaded as the admin is bootstrapped; see `wp-admin/includes/admin.php` for the primary list of files included.
-->

**wp-admin/includes** ディレクトリは、管理エリアで使用される主要なコアおよびサードパーティライブラリで構成されています。これらの一部は、管理画面を起動するときに読み込まれます。含まれるファイルの主要なリストは `wp-admin/includes/admin.php` を参照してください。

<!--
### JavaScript and CSS
-->

### JavaScript と CSS

<!--
The **wp-admin** and **wp-includes** directories also have **js** and **css** directories, for scripts and styles, respectively. Third-party scripts are packaged in a compressed and minified state, which are available at [https://wordpress.org/download/source/](https://wordpress.org/download/source/). Both minified and development versions are included for core scripts and styles, with the minified versions receiving the suffixes `.min.js` and `.min.css`.
-->

**wp-admin** と **wp-includes** ディレクトリには、それぞれスクリプトとスタイルのための **js** と **css** ディレクトリもあります。サードパーティのスクリプトは圧縮・軽量化された状態でパッケージ化されており、[https://wordpress.org/download/source/](https://wordpress.org/download/source/) で入手できます。コアのスクリプトとスタイルには、圧縮・軽量化されたバージョンと開発バージョンの両方が含まれており、圧縮・軽量化されたバージョンには `.min.js` と `.min.css` という接尾辞が付きます。

<!--
The **wp-includes** directory has a number of third-party libraries in folders. The **wp-includes/js** directory, in particular, has **jquery** and **tinymce** directories, with the former holding jQuery, jQuery UI, and various plugins, and the latter holding TinyMCE and various TinyMCE core and WordPress-specific extensions.
-->

**wp-includes** ディレクトリでは、多くのサードパーティライブラリがフォルダーに格納されています。特に **wp-includes/js** ディレクトリには **jquery** と **tinymce** ディレクトリがあり、前者には jQuery、jQuery UI、各種プラグイン、後者には TinyMCE、TinyMCE コアと WordPress 固有の拡張機能が格納されています。

<!--
The `wp-includes/script-loader.php` file registers all bundled scripts and styles. Each script and style is given a date-specific version number (yyyymmdd), which is bumped by a committer when the stylesheet changes. The version number is added to the URL, forcing the browser cache to clear and the new CSS or JavaScript to be loaded.
-->

`wp-includes/script-loader.php` ファイルは、バンドルされているすべてのスクリプトとスタイルを登録します。各スクリプトとスタイルには日付にもとづくバージョン番号 (yyyymmdd) が与えられ、スタイルシートが変更されたときにコミッターによってバージョンアップされます。バージョン番号は URL に追加され、ブラウザのキャッシュをクリアして新しい CSS や JavaScript を強制的に読み込むようにします。

<!--
## Searching and Browsing Code History
-->

## コード履歴の検索と閲覧

<!--
To search the codebase, developers rely on either a project search tool in their code editor or IDE, or command-line utilities such as **ack** or **grep**. Browsing the codebase on Trac is manageable, but one particular feature is noteworthy: Trac includes an excellent user interface for the Subversion **blame** command.
-->

コードベースを検索するために、開発者はコードエディターや IDE のプロジェクト検索ツール、または **ack** や **grep** のようなコマンドラインユーティリティを使用します。Trac 上でのコードベースのブラウジングは管理しやすいですが、注目すべき1つの特別な機能があります。Trac は Subversion の **blame** コマンドのための優れたユーザーインタフェースを備えています。

<!--
To **blame** a line of code means to determine who last edited that line and when. To access this in Trac when browsing a file, click the **Annotate** link in the top right corner. Most consider the UI far more efficient than individual svn blame commands.
-->

コードの行を **blame** することは、誰がいつその行を最後に編集したかを決定することを意味します。Trac でファイルを閲覧しているときに、右上にある **Annotate** リンクをクリックすると、これにアクセスできます。多くの人は、この UI について個別の svn blame コマンドよりもずっと効率的だと考えています。

<!--
Core committers do not make changes to WordPress lightly, and commits should never occur without as complete understanding of the existing code as possible. If the code causes a bug, was that always the case? When was it introduced? Why? Is the code in question a fix for a different bug? These questions are very important.
-->

コアコミッターは軽率に WordPress に変更を加えることはありませんし、既存のコードを完全に理解せずにコミットを行うべきではありません。もしそのコードがバグを引き起こすのであれば、それは常にそうだったのでしょうか ? いつ引き起こされたのでしょうか ? なぜでしょう ? 問題となっているコードは別のバグを修正するのでしょうか ? これらの質問は非常に重要です。

<!--
Note: To learn more about code history, read the section on [Researching Code History With Subversion Annotate](https://make.wordpress.org/core/handbook/svn/code-history/).
-->

備考: コードの履歴についてもっと知りたい方は、[コードの履歴を調べる](https://make.wordpress.org/core/handbook/svn/code-history/)のセクションを参考にしてください。

<!--
## Installation
-->

## インストール

<!--
When a WordPress install is initially run, if a `wp-config.php` file cannot be located, the `wp-load.php` file will suggest you visit `wp-admin/setup-config.php` to create the configuration file.
-->

WordPressのインストールを最初に実行したとき、`wp-config.php` ファイルが見つからない場合、`wp-load.php` ファイルは `wp-admin/setup-config.php` にアクセスして設定ファイルを作成するよう提案します。

<!--
Once this is done, you’ll be taken to `wp-admin/install.php`. At this point, the database tables are created. The database schema is stored in `wp-admin/includes/schema.php`, and the installation libraries are primarily located in `wp-admin/includes/upgrade.php` *(where else are they located? we should be specific here)*.
-->

これが完了すると、`wp-admin/install.php` に移動します。この時点で、データベースのテーブルが作成されます。データベーススキーマは `wp-admin/includes/schema.php` に、インストールされるライブラリは主に `wp-admin/includes/upgrade.php` に格納されます。(他のものはどこにあるのか、ここで具体的に説明する必要があります)

<!--
## Database Upgrades
-->

## データベースのアップグレード

<!--
Database upgrade instructions are included in `wp-admin/includes/upgrade.php`. Whenever a database change is needed with a new version of WordPress – whether that means altering the database structure, or updating some database content – an upgrade routine can be triggered. Indeed, you can safely update from WordPress 0.70 to the latest version and the database will keep up with the more than a decade of changes.
-->

データベースのアップグレード方法は `wp-admin/includes/upgrade.php` に記載されています。データベース構造の変更でもデータベースの一部のコンテンツの更新でも、WordPress の新しいバージョンでデータベースの変更が必要なときは、いつでもアップグレードルーチンを起動できます。実際に、WordPress 0.70から最新バージョンに安全に更新でき、データベースは10年以上の変化にも対応します。

<!--
Knowing *when* to upgrade is handled by a number in `wp-includes/version.php`, the WordPress database version. This number corresponds to a revision number of the codebase, generally the revision that last introduced a database upgrade routine. When the number in the code differs from the number stored in the database, the routines in `wp-admin/includes/upgrade.php` are run.
-->

「いつ」アップグレードされるかは、`wp-includes/version.php` にある WordPress データベースのバージョン番号によって判断されます。この番号はコードベースのリビジョン番号に対応し、一般的には最後にデータベースのアップグレードルーチンを実行したリビジョンとなります。コード内の番号がデータベースに保存されている番号と異なる場合、 `wp-admin/includes/upgrade.php` にあるルーチンが実行されます。

<!--
The function `wp_upgrade()` calls `upgrade_all()` (among other functions), which will run the appropriate routines in sequence. In order to trigger a new routine, a “schema bump” – changing the right numbers, including the WordPress database version in `version.php` – needs to occur.
-->

`wp_upgrade()` 関数 は `upgrade_all()` を (他の関数と一緒に) 呼び出し、適切なルーチンを順番に実行します。新しいルーチンを起動するためには、「スキーマのバージョンアップ (`version.php` にある、WordPress データベースのバージョンを含む正しい数値に変更する)」が必要となります。

<!--
Changes to the database structure are handled by a function called `dbDelta()`, which takes the table definitions, compares them to the existing schema, and makes any changes that are required – for example, adding new tables, altering fields, adding indexes. For `dbDelta()` to run over the core table definitions, the DB version in `version.php` simply needs to be bumped.
-->

データベース構造の変更は `dbDelta()` という関数によって行われます。この関数はテーブルの定義を受け取り、それを既存のスキーマと比較し、必要な変更を行います。たとえば、新しいテーブルを追加したり、フィールドを変更したり、インデックスを追加したりする場合です。コアテーブルの定義に対して `dbDelta()` を実行するには、`version.php` のデータベースバージョンを上げるだけです。

<!--
## File Updates
-->

## ファイルの更新

<!--
Core developers generally distinguish between database “upgrades” and version “updates.” Updating WordPress to the newest codebase (via the user interface) triggers a complex series of actions.
-->

コア開発者は一般的に、データベースの「アップグレード」とバージョンの「更新」を区別しています。(ユーザーインタフェースを介して) WordPress を最新のコードベースに更新することは、一連の複雑なアクションを引き起こします。

<!--
Prior to any update, WordPress has already polled **api.wordpress.org** to determine whether it needs to update, and if so, where to find the new version. Once the update is triggered, WordPress will download the ZIP archive and unzip it into a temporary directory in **wp-content/upgrade**. A single file, `wp-admin/includes/update-core.php`, will be copied out of the temporary directory and over the existing `wp-admin/includes/update-core.php`, at which point it will be executed. Thus, the newly downloaded code handles the main process of copying over the new files. This allows us to provide instructions specific to the new version, such as which files are old and can be removed.
-->

更新に先立ち、WordPress は **api.wordpress.org** に問い合わせ、更新が必要かどうか、必要な場合は新しいバージョンをどこで入手できるかを判断しています。更新が開始されると、WordPress は ZIP アーカイブをダウンロードし、**wp-content/upgrade** にある一時ディレクトリに解凍されます。一つのファイルである `wp-admin/includes/update-core.php` が一時ディレクトリからコピーされ、既存の `wp-admin/includes/update-core.php` を上書きし、その時点でそれが実行されます。このように、新しくダウンロードされたコードは、新しいファイルをコピーする主要な処理を行います。これにより、どのファイルが古くて削除できるのかといった、新しいバージョンに特有の指示を出すことができます。

<!--
## Exploring The Code
-->

## コードを調べる

<!--
These tools may be useful in exploring the WordPress codebase:
-->

これらのツールは、WordPress のコードベースを調べるときに役立つかもしれません。

*   [The Official WordPress Code Reference](https://developer.wordpress.org/reference/)
*   [QueryPosts.com](http://queryposts.com/)
*   [Westi’s PHPXref](http://phpxref.ftwr.co.uk/wordpress/nav.html?index.html)
*   [The Git mirror, mirrored to GitHub](https://github.com/WordPress/WordPress/)
