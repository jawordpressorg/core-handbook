<!--
# Installing from a Zip File
-->

# Zip ファイルからのインストール

<!--
## Overview
-->

## 概要

<!--
This article will walk you through installing the latest WordPress development version from a zip file.
-->

この記事では、最新の WordPress 開発バージョンを ZIP ファイルからインストールする方法を説明します。

<!--
### What You Will Need Before Starting
-->

### 始める前に必要なこと

<!--
Create a new database in your local web server using phpMyAdmin. \[[MAMP](https://make.wordpress.org/core/handbook/installing-a-local-server/installing-mamp/#5-creating-a-mysql-database-with-mamp)\] \[[WampServer](https://make.wordpress.org/core/handbook/installing-a-local-server/installing-wampserver/#5-creating-a-mysql-database-with-wampserver)\] \[[XAMPP](https://make.wordpress.org/core/handbook/installing-a-local-server/installing-xampp/#6-creating-a-mysql-database-with-xampp)\]
-->

phpMyAdmin を使用して、ローカルの Web サーバーに新しいデータベースを作成します。\[[MAMP](https://make.wordpress.org/core/handbook/installing-a-local-server/installing-mamp/#5-creating-a-mysql-database-with-mamp)\] \[[WampServer](https://make.wordpress.org/core/handbook/installing-a-local-server/installing-wampserver/#5-creating-a-mysql-database-with-wampserver)\] \[[XAMPP](https://make.wordpress.org/core/handbook/installing-a-local-server/installing-xampp/#6-creating-a-mysql-database-with-xampp)\]

<!--
**Note:** If you are using DesktopServer as your local server, you’ll need to follow those [instructions for creating a new local development site](https://make.wordpress.org/core/handbook/tutorials/installing-a-local-server/desktopserver/#5-creating-a-new-local-site) instead of the instructions listed below.
-->

**備考**: DesktopServer をローカルサーバーとして使用している場合は、以下の手順ではなく、この[新しいローカル開発サイトの作成手順](https://make.wordpress.org/core/handbook/tutorials/installing-a-local-server/desktopserver/#5-creating-a-new-local-site) に従う必要があります。


<!--
## Installing WordPress Trunk from a Zip File
-->

## WordPress Trunk を Zip ファイルからインストールする

<!--
### 1\. Download/Extract WordPress
-->

### 1\. WordPress のダウンロードと解凍

<!--
Download the [latest nightly build](https://wordpress.org/nightly-builds/wordpress-latest.zip) of the WordPress development version and save it to your computer.
-->

WordPress 開発バージョンの[最新ナイトリービルド](https://wordpress.org/nightly-builds/wordpress-latest.zip)をダウンロードし、コンピューターに保存してください。

<!--
Next you will need to open the zip file, and extract the contents into the root of your local web server’s public folder:
-->

次に、ZIP ファイルを開き、コンテンツをローカルの Web サーバーの公開フォルダーのルートに解凍する必要があります。

*   **MAMP**: Applications/MAMP/htdocs/
*   **WampServer**: wamp/www/
*   **XAMPP**: xampp/htdocs/

<!--
A new folder will appear in your local web server’s public folder named **wordpress**. Rename this folder **wordpress-trunk**.
-->

ローカルの Web サーバーの公開フォルダーに、**wordpress** という名前の新しいフォルダーが表示されます。このフォルダーの名前を **wordpress-trunk** に変更します。

<!--
### 2\. Creating wp-config.php
-->

### 2\. wp-config.php の作成

<!--
There are two ways you can create the `wp-config.php` file:
-->

`wp-config.php` ファイルを作成する方法は2つあります。

<!--
*   **Manual:** Open `wp-config-sample.php` in your plain text editor and enter the `DB_NAME`, `DB_USER`, `DB_PASSWORD`, and `DB_HOST` information for your local web server, then **Save the file** as `wp-config.php` in the root of the folder WordPress will be installed in (e.g. **wordpress-trunk**).
*   **Automated:** Allow WordPress to create the file during the installation process. If there is no `wp-config.php` file present, you will be asked to create one at the beginning of the install process.
-->

*   **手動:** プレーンテキストエディターで `wp-config-sample.php` を開き、ローカルの Web サーバーの `DB_NAME`、`DB_USER`、`DB_PASSWORD`、`DB_HOST` 情報を入力し、WordPress をインストールするフォルダーのルートに `wp-config.php` として**ファイルを保存**します (例: **wordpress-trunk**)。
*   **自動:** インストール中に WordPress がファイルを作成することを許可します。もし `wp-config.php` ファイルが存在しない場合、インストール処理の最初にファイルを作成するよう求められます。

<!--
Both are acceptable – use the method that you prefer.
-->

どちらでもかまいませんので、好きな方法を選んでください。

<!--
### 3\. Run the Install Script
-->

### 3\. インストールスクリプトの実行

<!--
In your web browser, navigate to [http://localhost/wordpress-trunk/](http://localhost/wordpress-trunk/) to run the installation process.
-->

Web ブラウザで [http://localhost/wordpress-trunk/](http://localhost/wordpress-trunk/) に移動し、インストールを実行します。

<!--
**If you created your `wp-config.php` file manually**, you will be presented with the standard WordPress installation screen. You will do the famous “5 minute install” – enter your site title, desired username, choice of a password (twice), and your e-mail address, then **click Install WordPress** to complete the installation. **Click Log In** on the Success screen, enter your username and password, and configure the settings for your preferences.
-->

**`wp-config.php` ファイルを手動で作成した場合**、WordPress の標準的なインストール画面が表示され、有名な「5分インストール」を行います。サイトのタイトル、希望のユーザー名、パスワード (2回)、メールアドレスを入力し、**WordPress をインストール**をクリックすると、インストールが完了します。インストールが成功した画面で**ログイン**をクリックし、ユーザー名とパスワードを入力し、設定を行います。

<!--
**If you prefer to let WordPress create the file**, you will be presented with a screen asking if you want to create the file now. **Click Create a Configuration File** to continue. Enter your database credentials for your local web server on the third screen, as well as the database table prefix you want to use (default is `wp_`). After you complete all the fields, **click Submit**. WordPress will check that it can connect to your database with the information you provided. If successful, **click Run the install** to proceed.
-->

**WordPress にファイルを作成させる場合は**、今すぐファイルを作成するかどうかを尋ねる画面が表示されます。**設定ファイルの作成**をクリックして、次に進みます。3番目の画面で、ローカルの Web サーバーのデータベース認証情報と、使用するデータベーステーブルの接頭辞を入力します (デフォルトは `wp_`)。すべての項目を入力したら、**送信**をクリックします。WordPress は、提供された情報を使って、データベースに接続できるかどうかを確認します。成功したら、**インストール実行**をクリックして次に進みます。

<!--
You will then do the “5 minute install”, complete all the fields, and **click Install WordPress** to complete the installation. **Click Log In** on the Success screen, enter your username and password, and configure your settings.
-->

その後、「5分インストール」を行い、すべての項目を入力し、**WordPress をインストール**をクリックするとインストールが完了します。インストールが成功した画面で**ログイン**をクリックし、ユーザー名とパスワードを入力し、設定を行います。

<!--
### 4\. Edit wp-config.php
-->

### 4\. wp-config.php の編集

<!--
Your local install will be used for beta testing and reporting bugs, so it is important for you to see error messages and notices. Open `wordpress-trunk/wp-config.php` in your plain text editor, and set `WP_DEBUG` to **true**:
-->

ローカルインストールはベータテストやバグレポートに使用されるため、エラーメッセージや通知を見ることができるのは重要です。プレーンテキストエディターで `wordpress-trunk/wp-config.php` を開き、`WP_DEBUG` を **true** に設定します。

```php
/**
 * For developers: WordPress debugging mode.
 *
 * Change this to true to enable the display of notices during development.
 * It is strongly recommended that plugin and theme developers use WP_DEBUG
 * in their development environments.
 */
define('WP_DEBUG', true);
```

<!--
### 5\. Updating Your Local Install
-->

### 5\. ローカルインストールのアップデート

<!--
WordPress 3.7 [introduced automatic updates](https://codex.wordpress.org/Configuring_Automatic_Background_Updates) for minor stable WordPress releases (3.7.x). This feature, by default, will also automatically update your development install daily.
-->

WordPress 3.7では、WordPress のマイナーな安定版リリース (3.7.x) に対して [自動更新を導入](https://codex.wordpress.org/Configuring_Automatic_Background_Updates) しています。この機能はデフォルトで、開発用インストールも毎日自動的に更新されます。

<!--
You will need to visit your local install once daily to make the cron task run that triggers the automatic update.
-->

自動更新のトリガーとなる cron タスクを実行させるために、毎日一度、ローカルインストールにアクセスする必要があります。

<!--
You can check what version you’re using either on the **Dashboard**, or by checking the footer of any admin page (*You are using a development version (3.8-alpha). Cool! Please stay updated.*).
-->

使用中のバージョンは、**ダッシュボード** または管理画面のフッターで確認できます (「お使いの WordPress は開発版 (3.8-alpha) です。すばらしい ! どうぞ最新版を使い続けてください。」)。

<!--
## Next Steps
-->

## 次のステップ

<!--
*   [Beta Testing](https://make.wordpress.org/core/handbook/testing/beta/)
-->

*   [ベータテスト](https://make.wordpress.org/core/handbook/testing/beta/)
