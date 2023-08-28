<!--
# Core APIs
-->

# コア API

<!--
The [WordPress Core Application Programming Interface (API)](https://codex.wordpress.org/WordPress_APIs "WordPress Core Application Programming Interface (API)") is comprised of several individual APIs, each one covering the functions involved in, and use of, a given set of functionality. Together, these form the project interface which allows plugins and themes to interact with, alter, and extend WordPress core functionality.
-->

[WordPress Core Application Programming Interface (API)](https://codex.wordpress.org/WordPress_APIs "#WordPress Core Application Programming Interface (API)") は、いくつかの個別の API で構成されており、それぞれの API は、特定の機能セットに関連する機能とその使用方法をカバーしています。これらの API は、プラグインやテーマが WordPress のコア機能と相互作用し、変更し、拡張することを可能にするプロジェクトインターフェイスを形成しています。

<!--
## Why You Should Use The Core APIs
-->

## なぜコア API を使うべきか

<!--
Using the core APIs when developing for WordPress is strongly encouraged because:
-->

WordPress おいて開発する場合は、次の理由からコア API を使用することを強く推奨されます:

<!--
*   Core APIs make building things for WordPress easier by providing hooks, actions, filters, helper functions.
*   WordPress does the “heavy lifting” for you (database calls, input validation, security, form building) so you don’t have to.
*   Using core APIs ensures your code will be both backward-compatible and future-proof.
*   The APIs allow seamless integration into wp-admin for plugin/theme options pages, inline help documentation, etc.
-->

*   コア API は、フック、アクション、フィルター、ヘルパー関数を提供しているため、WordPress 向けの開発を容易にします。
*   WordPress があなたのために「面倒な作業」(データベース呼び出し、入力の検証、セキュリティ、フォーム構築) を行うため、あなたがそれを行う必要がありません。
*   コア API を使用することで、コードの後方互換性と将来性の両方が保証されます。
*   API により、プラグイン/テーマのオプションページ、インラインヘルプドキュメントなどを wp-admin にシームレスに統合できます。

<!--
## WordPress Core APIs
-->

## WordPress コア API

<!--
The following is an overview of the individual APIs that make up the WordPress Core API. More information on each API can be found on their respective Codex pages.
-->

以下は WordPress コア API を構成する個々の API の概要です。各 API の詳細については、それぞれの Codex ページを参照してください。

### Dashboard Widgets API

<!--
The [Dashboard Widgets API](https://developer.wordpress.org/apis/handbook/dashboard-widgets/ "Dashboard Widgets API"), added in WordPress 2.7, makes it very simple for plugin or theme authors to add new widgets to the admin dashboard. Widgets created using the API will automatically appear on the admin dashboard, will contain all the standard custom features including drag/drop, minimize, and configure, and appear in the screen options so users can hide them, if desired.
-->

WordPress 2.7で追加された [Dashboard Widgets API](https://developer.wordpress.org/apis/handbook/dashboard-widgets/ "Dashboard Widgets API") を使用すると、プラグインまたはテーマの作者は新しいウィジェットを非常に簡単に追加できます。API を使用して作成されたウィジェットは自動的に管理ダッシュボードに表示され、ドラッグ & ドロップ、最小化、設定を含むすべての標準的なカスタム機能が含まれ、画面オプションに表示されるため、ユーザーは必要に応じて非表示にできます。

### Database API

<!--
The [Database API](https://developer.wordpress.org/apis/handbook/database/ "Database API"), added in WordPress 0.71, provides the correct method for accessing data as named values which are stored in the database layer.
-->

WordPress 0.71で追加された [Database API](https://developer.wordpress.org/apis/handbook/database/ "Database API") は、データベース層に保存されている名前付きの値としてのデータにアクセスするための正しい方法を提供します。

### File Header API

<!--
The [File Header API](https://codex.wordpress.org/File_Header_API "File Header API"), added in WordPress 1.5 and extended in WordPress 2.9 and 3.0, consists of functions and hooks regarding the use of file headers in themes and plugins, and provides the ability to pull meta\-information (Name, Version, Author, URI, Description, etc.) from those files.
-->

WordPress 1.5で追加され、WordPress2.9と3.0で拡張された [File Header API](https://codex.wordpress.org/File_Header_API "File Header API") は、テーマとプラグインのファイルヘッダーの使用に関する関数とフックで構成され、それらのファイルからメタ情報 (名前、バージョン、作者、URI、説明など) を取得する機能を提供します。

### Filesystem API

<!--
The [Filesystem API](https://codex.wordpress.org/Filesystem_API "Filesystem API"), added in WordPress 2.6, was originally created for WordPress’ own automatic updates feature. The API abstracts out the functionality needed for reading and writing local files to the filesystem to be done securely, on a variety of host types, using the **WP\_Filesystem\_Base** class, and several sub-classes which implement different ways of connecting to the local filesystem, depending on individual host support.
-->

WordPress 2.6で追加された [Filesystem API](https://codex.wordpress.org/Filesystem_API "Filesystem API") は、もともと WordPress 独自の自動更新機能のために作られたものです。この API は、**WP_Filesystem_Base** クラスと、個々のホストのサポートに応じてローカルファイルシステムへ接続するさまざまな手段を実装しているいくつかのサブクラスを使って、さまざまな種類のホスト上でローカルファイルをファイルシステムへ安全に読み書きするために必要な機能を抽象化しています。

### HTTP API

<!--
The [HTTP API](https://developer.wordpress.org/plugins/http-api/ "HTTP API"), added in WordPress 2.7 and extended further in WordPress 2.8, standardizes the HTTP requests for WordPress. The API handles cookies, gzip encoding and decoding, chunk decoding (if HTTP 1.1), and various other HTTP protocol implementations. The API standardizes requests, tests each method prior to sending, and, based on your server configuration, uses the appropriate method to make the request.
-->

WordPress 2.7で追加され、WordPress2.8でさらに拡張された [HTTP API](https://developer.wordpress.org/plugins/http-api/ "HTTP API") は、WordPress の HTTP リクエストを標準化します。この API は Cookie、gzip エンコードとデコード、チャンクデコード (HTTP 1.1 の場合)、その他さまざまな HTTP プロトコルの実装を扱います。API はリクエストを標準化し、送信前に各メソッドをテストし、サーバーの設定にもとづいて適切なメソッドを使用してリクエストを行います。

### Metadata API

<!--
The [Metadata API](https://codex.wordpress.org/Metadata_API "Metadata API"), added in WordPress 2.9, is a simple and standardized way for retrieving and manipulating metadata of various WordPress object types. Metadata for an object is a represented by a simple key-value pair. Objects may contain multiple metadata entries that share the same key, and differ only in their value.
-->

WordPress 2.9で追加された [Metadata API](https://codex.wordpress.org/Metadata_API "Metadata API") は、WordPress のさまざまなオブジェクトタイプのメタデータを取得・操作するためのシンプルで標準化された方法です。オブジェクトのメタデータは単純なキーと値のペアで表されます。オブジェクトには、同じキーを共有し、値のみが異なる複数のメタデータエントリが含まれる場合があります。

### Options API

<!--
The [Options API](https://codex.wordpress.org/Options_API "Options API"), added in WordPress 1.0 and extended in versions 1.2 and 1.5, is a simple and standardized way of storing data in the database. The API makes it easy to create, access, update, and delete those options. All the data is being stored in the `wp_options` table under a given custom name.
-->

WordPress 1.0で追加され、バージョン1.2と1.5で拡張された [Options API](https://codex.wordpress.org/Options_API "Options API") は、データベースにデータを保存するためのシンプルで標準化された方法です。この API を使えば、オプションの作成、アクセス、更新、削除を簡単に行うことができます。すべてのデータは `wp_options` テーブルに任意のカスタム名で保存されます。

### Plugin API

<!--
The [Plugin API](https://codex.wordpress.org/Plugin_API "Plugin API"), added in WordPress 1.5, allows for creating actions and filters in hooking functions and methods. The functions or methods will then be run when the action or filter is called. Hooks are provided by WordPress to allow your plugin to *hook into* the rest of WordPress; that is, to call functions in your plugin at specific times, and set your plugin in motion.
-->

WordPress 1.5で追加された [Plugin API](https://codex.wordpress.org/Plugin_API "Plugin API") では、関数やメソッドをフックすることでアクションやフィルターを作成できます。関数やメソッドは、アクションやフィルターが呼び出されたときに実行されます。フックは WordPress が提供するもので、プラグインが WordPress の他の部分に*フック*できるようにするものです。つまり、特定の時間にプラグイン内の関数を呼び出し、プラグインを動作させます。

### Quicktags API

<!--
The [Quicktags API](https://codex.wordpress.org/Quicktags_API "Quicktags API"), added in WordPress 3.3, allows you to include additional buttons in the Text (HTML) mode of the WordPress editor.
-->

WordPress 3.3で追加された [Quicktags API](https://codex.wordpress.org/Quicktags_API "Quicktags API") を使用すると、WordPress エディターのテキスト (HTML) モードにボタンを追加できます。

### Rewrite API

<!--
The [Rewrite API](https://codex.wordpress.org/Rewrite_API "Rewrite API"), added in WordPress 2.1, is used to manage the rewrite rules that allow you to use the **Pretty Permalinks** feature. It has several methods that generate the rewrite rules from values in the database. It is used internally when updating the rewrite rules, and also to find the URL of a specific post, page, category archive, etc. It also allows theme and plugin developers to specify new, custom rewrite rules.
-->

WordPress 2.1で追加された [Rewrite API](https://codex.wordpress.org/Rewrite_API "Rewrite API") は、**Pretty パーマリンク**機能を使用するためのリライトルールを管理するために使用されます。データベースの値からリライトルールを生成するメソッドがいくつかあります。リライトルールを更新する際に内部的に使用されるほか、特定の投稿、ページ、カテゴリーアーカイブなどの URL を検索するためにも使用されます。また、テーマやプラグインの開発者は新しいカスタムリライトルールを指定できます。

### Settings API

<!--
The [Settings API](https://codex.wordpress.org/Settings_API "Settings API"), added in WordPress 2.7, allows admin pages containing settings forms to be created and managed semi-automatically. It lets plugin and theme developers define settings pages, sections within those pages, and fields within the sections. New settings pages can be registered, and new settings sections or fields can be added to existing settings pages.
-->

WordPress 2.7で追加された [Settings API](https://codex.wordpress.org/Settings_API "Settings API") を使用すると、設定フォームを含む管理ページを半自動的に作成・管理できます。これにより、プラグインやテーマの開発者は設定ページ、ページ内のセクション、セクション内のフィールドを定義できます。新しい設定ページを登録したり、既存の設定ページに新しい設定セクションやフィールドを追加したりできます。

### Shortcode API

<!--
The [Shortcode API](https://codex.wordpress.org/Shortcode_API "Shortcode API"), added in WordPress 2.5, is a set of functions that create a simple hook used to pull in content. Using the API, plugin developers can create special kinds of content (e.g. forms, content generators, galleries, etc.) that users can add to posts or pages by inserting the corresponding **\[shortcode\]** into the content.
-->

WordPress 2.5で追加された [Shortcode API](https://codex.wordpress.org/Shortcode_API "Shortcode API") は、コンテンツを取り込むためのシンプルなフックを作成する関数のセットです。プラグイン開発者は、対応する **\[ショートコード\]** をコンテンツに挿入することでユーザーが投稿やページに追加できる特別な種類のコンテンツ (フォーム、コンテンツジェネレータ、ギャラリーなど) を作成できます。

### Theme Modification API

<!--
The [Theme Modification API](https://codex.wordpress.org/Theme_Modification_API "Theme Modification API"), added in WordPress 2.1, consists of the functions and hooks related to the use of theme modification values. These functions can be used by theme authors to save and retrieve modifications to their themes as options.
-->

WordPress 2.1で追加された [Theme Modification API](https://codex.wordpress.org/Theme_Modification_API "Theme Modification API") は、テーマの変更値の利用に関する関数とフックで構成されています。これらの関数は、テーマ作者がテーマの変更値をオプションとして保存したり取得したりするために使用できます。

### Theme Customization API

<!--
The [Theme Customization API](https://codex.wordpress.org/Theme_Customization_API "Theme Customization API"), added in WordPress 3.4, allows theme developers to add custom options specific to their theme to the Theme Customization admin screen (aka Theme Customizer).
-->

WordPress 3.4で追加された [Theme Customization API](https://codex.wordpress.org/Theme_Customization_API "Theme Customization API") を使用すると、テーマ開発者はテーマカスタマイズ管理画面 (別名: テーマカスタマイザー) にテーマ固有のカスタムオプションを追加できます。

### Transients API

<!--
The [Transients API](https://developer.wordpress.org/apis/handbook/transients/ "Transients API"), added in WordPress 2.8, offers a simple and standardized way of storing cached data in the database temporarily by giving it a custom name and a timeframe, after which it will expire and be deleted. The Transients API is very similar to the Options API, but with the added feature of an expiration time, which simplifies the process of using the `wp_options` database table to temporarily store cached information.
-->

WordPress 2.8で追加された [Transients API](https://developer.wordpress.org/apis/handbook/transients/ "Transients API") は、キャッシュされたデータにカスタム名と期間を指定してデータベースに一時的に保存し、その後有効期限が切れて削除されるシンプルかつ標準化された方法を提供します。Transients API は Options API とよく似ていますが、有効期限という機能が追加されており、`wp_options` データベーステーブルを使用してキャッシュ情報を一時的に保存するプロセスを簡素化します。

### Widgets API

<!--
The [Widgets API](https://codex.wordpress.org/Widgets_API "Widgets API"), added in WordPress 2.8, allows developers to build custom widgets for use in sidebars and other widgetized areas of a theme. The API simplifies the widget creation process, and makes all widgets multiple instance capable.
-->

WordPress 2.8で追加された [Widgets API](https://codex.wordpress.org/Widgets_API "Widgets API") を使用すると、開発者はテーマのサイドバーやその他のウィジェット化されたエリアで使用するカスタムウィジェットを構築できます。この API は、ウィジェットの作成プロセスを簡素化し、すべてのウィジェットをマルチインスタンスに対応させます。

### XML-RPC WordPress API

<!--
The [XML-RPC WordPress API](https://codex.wordpress.org/XML-RPC_WordPress_API "XML-RPC WordPress API"), added in WordPress 1.5, allows other systems to connect to and communicate with WordPress, even remotely, including publishing clients (desktop and mobile), and other software that perform batch tasks like creating multiple posts from a file, etc.
-->

WordPress 1.5で追加された [XML-RPC WordPress API](https://codex.wordpress.org/XML-RPC_WordPress_API "XML-RPC WordPress API") を使用すると、他のシステムがリモートであっても WordPress に接続して通信できます。これには、投稿クライアント (デスクトップおよびモバイル) や、ファイルから複数の投稿を作成するなどのバッチタスクを実行するその他のソフトウェアが含まれます。

## WordPress.org API

<!--
There are also APIs available for the [WordPress.org site](https://codex.wordpress.org/WordPress.org_API "WordPress.org API"):
-->

[WordPress.org サイト](https://codex.wordpress.org/WordPress.org_API "WordPress.org API")で利用できる API も用意されています:

<!--
*   **Secret Key**: Secret key and salt generator for `wp-config.php`.
*   **Stats API**: Stats about the systems websites are running WordPress on.
*   **Version Check API**: WordPress version checker.
*   **Translations API**: Provides information on available translations for plugins and themes.
*   **Credits API**: Details about the various individuals who contribute to the WordPress code base, which are used in the **Credits screen** in `/wp-admin/`.
*   **Popular Import Plugin API**: List of popular import plugins in the WordPress Plugin Directory, which is used by the **Tools > Import screen** in `/wp-admin/`.
*   **Plugins API**: Provides information on plugins hosted on WordPress.org, and allows WordPress to check the repository for updates to those plugins.
*   **Themes API**: Provides information on themes hosted on WordPress.org, and allows WordPress to check the repository for updates to those themes.
*   **Editor API**: Used by the theme and plugin editor to get a reference to documentation generated with phpDocumentor..
*   **Events API**: Upcoming WordCamps and meetup events, filterable by location.
*   **Browse Happy API**: Latest browser release matrix.
*   **Serve Happy API**: WordPress PHP version compatibility matrix.
-->

*   **Secret Key**: `wp-config.php` の秘密鍵とソルト。
*   **Stats API**: WordPress が稼働している Web サイトのシステムに関する統計。
*   **Version Check API**: WordPress のバージョンチェッカー。
*   **Translations API**: プラグインとテーマで利用可能な翻訳に関する情報を提供します。
*   **Credits API**: WordPress のコードベースに貢献しているさまざまな個人に関する情報で、`/wp-admin/` の**クレジット画面**で使用されます。
*   **Popular Import Plugin API**: WordPress プラグインディレクトリにある人気のインポートプラグインのリスト。これは、`/wp-admin/` の**ツール > インポート画面**で使用されます。
*   **Plugins API**: WordPress.org でホストされているプラグインに関する情報を提供し、WordPress がそれらのプラグインの更新のためにリポジトリを確認できるようにします。
*   **Themes API**: WordPress.org でホストされているテーマに関する情報を提供し、WordPress がそれらのテーマの更新のためにリポジトリを確認できるようにします。
*   **Editor API**: テーマとプラグインのエディターが、phpDocumentor で生成されたドキュメントへの参照を取得するために使用されます。
*   **Events API**: 場所によってフィルター可能な、今後の WordCamp および Meetup イベント
*   **Browse Happy API**: 最新のブラウザリリースマトリックス。
*   **Serve Happy API**: WordPress での PHP バージョン互換マトリックス。

<!--
## Other Resources
-->

## その他のリソース

<!--
*   The WordPress Settings API (WordCamp Sofia 2012) \[[Read](http://kovshenin.com/2012/the-wordpress-settings-api/ "Read the blog post")\] \[[Watch](http://wordpress.tv/2012/10/31/konstantin-kovshenin-settings-api/ "Watch the video on WordPress.tv")\]
-->

*   The WordPress Settings API (WordCamp Sofia 2012) \[[ブログ投稿を読む](http://kovshenin.com/2012/the-wordpress-settings-api/ "ブログ投稿を読む")\] \[[ビデオを見る](http://wordpress.tv/2012/10/31/konstantin-kovshenin-settings-api/ "WordPress.tv でビデオを見る")\]
