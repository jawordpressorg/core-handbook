<!--
# Installing via SVN
-->

# SVN によるインストール

<!--
## Overview
-->

## 概要

<!--
This article will walk you through installing the latest WordPress development version via Subversion (SVN).
-->

この記事では、Subversion (SVN) を使って最新の WordPress 開発版をインストールする方法を説明します。

<!--
### What You Will Need Before Starting
-->

### 始める前に必要なこと

<!--
*   Create a new database in your local web server using phpMyAdmin. \[[MAMP](https://make.wordpress.org/core/handbook/tutorials/installing-a-local-server/mamp/)\] \[[WampServer](https://make.wordpress.org/core/handbook/tutorials/installing-a-local-server/wampserver/)\] \[[XAMPP](https://make.wordpress.org/core/handbook/tutorials/installing-a-local-server/xampp/)\]
    *   **Note:** If you are using DesktopServer as your local server, you’ll need to choose the **Blank (WordPress SVN)** option from the Blueprint dropdown when creating a new local development site. That will create your database and `wp-config.php` file. Once you’ve created the site, delete the `index.html` and `wp-config-sample.php` files in the development site’s folder (**wordpress-svn.dev**) before you check out a copy of WordPress trunk.
*   Subversion installed on your computer:
    *   Installing SVN on Windows
    *   [Installing SVN on MAC](https://make.wordpress.org/core/handbook/tutorials/installing-a-vcs/#installing-subversion-on-a%c2%a0mac)
    *   [Installing TortoiseSVN](https://make.wordpress.org/core/handbook/tutorials/installing-a-vcs/#installing-tortoisesvn) (Windows)
*   A command line client installed on your computer:
    *   Windows: [Cygwin](http://cygwin.com/)
    *   MAC: [Terminal](http://en.wikipedia.org/wiki/Terminal_(OS_X)) or [Bash](http://www.gnu.org/software/bash/)
-->

*   phpMyAdmin を使用して、ローカルの Web サーバーに新しいデータベースを作成します。\[[MAMP](https://ja.wordpress.org/team/handbook/core/tutorials/installing-a-local-server/mamp/)\] \[[WampServer](https://ja.wordpress.org/team/handbook/core/tutorials/installing-a-local-server/wampserver/)\] \[[XAMPP](https://ja.wordpress.org/team/handbook/core/tutorials/installing-a-local-server/installing-xampp/)\]
    *   **備考**: ローカルサーバーとして DesktopServer を使用している場合、新しいローカル開発サイトを作成する際に、Blueprint ドロップダウンから **Blank (WordPress SVN)** オプションを選択する必要があります。これにより、データベースと `wp-config.php` ファイルが作成されます。サイトを作成したら、WordPress trunk のコピーをチェックアウトする前に、開発サイトのフォルダー (**wordpress-svn.dev**) にある `index.html` と `wp-config-sample.php` ファイルを削除してください。
*   コンピューターに Subversion がインストールされていること:
    *   Windows に SVN をインストールする
    *   [MACに SVN をインストールする](https://ja.wordpress.org/team/handbook/core/tutorials/installing-a-vcs/#installing-subversion-on-a%c2%a0mac)
    *   [TortoiseSVN のインストール](https://ja.wordpress.org/team/handbook/core/tutorials/installing-a-vcs/#installing-tortoisesvn) (Windows)
*   コンピューターにコマンドラインクライアントがインストールされていること:
    *   Windows: [Cygwin](http://cygwin.com/)
    *   MAC: [Terminal](http://en.wikipedia.org/wiki/Terminal_(OS_X)) or [Bash](http://www.gnu.org/software/bash/)

<!--
## Installing WordPress Using Subversion
-->

## Subversion を使用して WordPress をインストールする

<!--
The 3.7 release cycle brought a [restructuring of the SVN repository](https://make.wordpress.org/core/2013/08/06/a-new-frontier-for-core-development/), to bring the code, unit tests, and tools together in one place for core contributors to work with.
-->

3.7リリースサイクルでは、[SVN リポジトリの再構築](https://make.wordpress.org/core/2013/08/06/a-new-frontier-for-core-development/)を行い、コード、ユニットテスト、ツールを1つの場所にまとめ、コア貢献者が作業しやすいようにしました。

<!--
You can still check out just the source code from [https://core.svn.wordpress.org/trunk/](https://core.svn.wordpress.org/trunk/) to install and test with; however, if you plan on contributing to core, it is recommended that you check out the source code, unit tests, and tools from the new repository to test, fix bugs, and create patches and unit tests with.
-->

[https://core.svn.wordpress.org/trunk/](https://core.svn.wordpress.org/trunk/) からソースコードだけをチェックアウトして、インストールしたりテストしたりすることはできます。しかし、もしコアに貢献するつもりなら、新しいリポジトリからソースコード、ユニットテスト、ツールをチェックアウトして、テスト、バグ修正、パッチやユニットテストの作成に利用することをおすすめします。


<!--
The steps outlined below are for installing WordPress via SVN using the new development repository.
-->

以下の手順は、新しい開発リポジトリを使用して SVN 経由で WordPress をインストールするためのものです。

<!--
### 1\. Check Out WordPress Trunk
-->

### 1\. WordPress Trunk をチェックアウトする

<!--
#### 1.1 Using TortoiseSVN
-->

#### 1.1 TortoiseSVN の使用

<!--
Create a folder in your local web server’s public folder (**/htdocs** or **/www**) called **wordpress-svn**. Open that folder, right-click and **select SVN Checkout**.
-->

ローカル Web サーバーの公開フォルダー (**/htdocs** または **/www**) に、**wordpress-svn** というフォルダーを作成します。そのフォルダーを開き、右クリックして、**SVN チェックアウト**を選択します。

<!--
![TortoiseSVN Checkout Context Menu Screen](https://make.wordpress.org/core/files/2013/09/tortoisesvn-checkout-1.png)
-->

![TortoiseSVN チェックアウトコンテキストメニュー画面](https://make.wordpress.org/core/files/2013/09/tortoisesvn-checkout-1.png)

<!--
You will be presented with the checkout window. Enter the URL of the wordpress.org SVN repo in URL repository field.
-->

チェックアウトウィンドウが表示されます。URL リポジトリ 欄に wordpress.org SVN リポジトリの URL を入力します。

![TortoiseSVN Checkout Window Screen](https://make.wordpress.org/core/files/2013/09/tortoisesvn-checkout-2.png)

<!--
The files will begin downloading to that folder.
-->

そのフォルダーへのファイルのダウンロードが始まります。

![TortoiseSVN Checkout File Download Screen](https://make.wordpress.org/core/files/2013/09/tortoisesvn-checkout-3.png)

<!--
The green checkmark you see over the icons for the files and folders indicates that is now a versioned file. If you don’t see that icon, refresh the folder content list.
-->

ファイルやフォルダーのアイコンの上に表示されている緑色のチェックマークは、現在バージョン管理されているファイルであることを示します。このアイコンが表示されない場合は、フォルダーの内容一覧を更新してください。

<!--
#### 1.2 Using Command Line
-->

#### 1.2 コマンドラインの使用

<!--
You can also use the command line to download the latest version of WordPress trunk. **Note:** Do not type the `$` characters from the examples below – it represents the command prompt.
-->

また、コマンドラインを使用して、WordPress trunk の最新バージョンをダウンロードできます。**備考:** 以下の例の `$` 文字はコマンドプロンプトを表しますので、入力しないでください。

<!--
Tip: you can use the **cd** command to change directories, and the **pwd** command to find out what your current directory is.
-->

ヒント: ディレクトリを変更するには **cd** コマンドを、カレントディレクトリを調べるには **pwd** コマンドを使用します。

<!--
Create a directory in your local web server’s public folder called **wordpress-svn** using your command line client:
-->

コマンドラインクライアントを使用して、ローカルの Web サーバーの公開フォルダーに **wordpress-svn** という名前のディレクトリを作成します。

```bash
$ mkdir ~/wordpress-svn
```

<!--
Now switch to the directory you just created:
-->

ここで、先ほど作成したディレクトリに切り替えます。

```bash
$ cd ~/wordpress-svn
```

<!--
Next you will check out a copy of WordPress trunk from SVN:
-->

次に、WordPress の trunk のコピーを SVN からチェックアウトします。

```bash
$ svn co https://develop.svn.wordpress.org/trunk/ .
```

<!--
The trailing slash on the URL, and the period at the end of the command, are both important – they make sure that downloaded files from the repository end up in the current directory. If you leave off that dot, you’ll end up creating a new installation directory called “trunk”, which is not what you want.
-->

URL の末尾のスラッシュと、コマンドの末尾のピリオドは、どちらも重要です。これらは、リポジトリからダウンロードしたファイルがカレントディレクトリにあることを確認するためです。もしこのドットを削除してしまうと、"trunk" という名前の新しいインストールディレクトリが作成されてしまいますが、これは望んだものではありません。

<!--
The following message may appear asking you to accept WordPress’ security certificate:
-->

WordPress のセキュリティ証明書を受け入れるかどうか、以下のメッセージが表示される場合があります。

```bash
Error validating server certificate for 'https://plugins.svn.wordpress.org:443':
 - The certificate is not issued by a trusted authority. Use the
   fingerprint to validate the certificate manually!
Certificate information:
 - Hostname: *.svn.wordpress.org
 - Valid: from Thu, 21 Jun 2012 16:07:30 GMT until Wed, 15 Jul 2015 19:04:26 GMT
 - Issuer: 07969287, http://certificates.godaddy.com/repository, GoDaddy.com, Inc., Scottsdale, Arizona, US
 - Fingerprint: bf:08:a3:de:ab:e4:76:fd:d0:5d:10:d1:c8:de:19:12:5f:bf:71:25
(R)eject, accept (t)emporarily or accept (p)ermanently?
```

<!--
Type **p** to accept it permanently.
-->

永続的に許可する場合は、**p** と入力してください。

<!--
### 2\. Creating wp-config.php
-->

### 2\. wp-config.php の作成

<!--
There are two ways you can create the `wp-config.php` file:
-->

`wp-config.php` ファイルを作成する方法は2つあります。

<!--
*   **Manual:** Open `wp-config-sample.php` in your plain text editor and enter the `DB_NAME`, `DB_USER`, `DB_PASSWORD`, and `DB_HOST` information for your local web server, then save it as `wp-config.php` in the root directory of your local SVN repository (e.g. **wordpress-svn**).
*   **Automated:** Allow WordPress to create the file during the installation process. If there is no `wp-config.php` file present, you will be asked to create one at the beginning of the install process.
-->

*   **手動:** プレーンテキストエディターで `wp-config-sample.php` を開き、ローカル Web サーバーの `DB_NAME`、`DB_USER`、`DB_PASSWORD`、`DB_HOST` 情報を入力し、ローカル SVN リポジトリ (例: **wordpress-svn**) のルートディレクトリに `wp-config.php` として保存してください。
*   **自動:** インストール中に WordPress がファイルを作成することを許可します。もし `wp-config.php` ファイルが存在しない場合、インストール処理の最初にファイルを作成するよう求められます。

<!--
Both are acceptable – use the method that you prefer.
-->

どちらでもかまいませんので、お好みの方法をお使いください。

<!--
Remember that you will need to **create a MySQL database** to install WordPress in.
-->

WordPress をインストールするために、**MySQL データベースを作成**する必要があることを忘れないでください。

<!--
### 3\. Run the Install Script
-->

### 3\. インストールスクリプトの実行

<!-- In your web browser, navigate to [http://localhost/wordpress-svn/src/](http://localhost/wordpress-svn/src/) to run the installation process. -->

Web ブラウザーで[http://localhost/wordpress-svn/src/](http://localhost/wordpress-svn/src/) に移動し、インストール作業を実行します。

<!--
**For those using Windows 11**: If you have not previously installed npm and grunt you will get an error with suggested npm commands. Download and install nodejs from here: [https://nodejs.org/download/release/latest-v14.x/](https://nodejs.org/download/release/latest-v14.x/). Before attempting to run the suggested npm commands, open a command window and navigate to your wordpress-svn directory. Issue the following command: `npm install -g grunt-cli` – This installs the grunt client. Then add grunt to your wordpress instance using:  
`npm install grunt --save-dev`  
`npm run dev` should now complete the process of unpacking the WordPress install.
-->

**Windows 11をお使いの方へ**: npm と grunt をインストールしていない場合、npm コマンドのエラーが表示されます。ここから nodejs をダウンロードし、インストールしてください: [https://nodejs.org/download/release/latest-v14.x/](https://nodejs.org/download/release/latest-v14.x/)。npm コマンドを実行する前に、コマンドウィンドウを開き、wordpress-svn ディレクトリに移動し、以下のコマンドを実行します。`npm install -g grunt-cli` - これは、grunt クライアントをインストールします。そして、次のコマンドを実行して、wordpress インスタンスに grunt を追加します。
`npm install grunt --save-dev`
`npm run dev` で、WordPress インストールの解凍が完了するはずです。

<!--
Upon browser refresh you should get the response as described below. These directions are described in more detail at [https://gruntjs.com/getting-started](https://gruntjs.com/getting-started).
-->

ブラウザーを更新すると、以下のような応答が得られるはずです。これらの方法は、[https://gruntjs.com/getting-started](https://gruntjs.com/getting-started) でより詳細に説明されています。

<!--
**If you created your `wp-config.php` file manually**, you will be presented with the standard WordPress installation screen. You will do the famous “5 minute install” – enter your site title, desired username, choice of a password (twice), and your e-mail address, then **click Install WordPress** to complete the installation. **Click Log In** on the Success screen, enter your username and password, and configure the settings for your preferences.
-->

**`wp-config.php` ファイルを手動で作成した場合**、WordPress の標準的なインストール画面が表示され、有名な「5分インストール」を行います。サイトのタイトル、希望のユーザー名、パスワード (2回)、メールアドレスを入力し、**WordPress をインストール**をクリックすると、インストールが完了します。インストールが成功した画面で**ログイン**をクリックし、ユーザー名とパスワードを入力し、設定を行います。**成功の画面でログイン**をクリックし、ユーザー名とパスワードを入力し、お好みの設定を行います。


<!--
**If you prefer to let WordPress create the file**, you will be presented with a screen asking if you want to create the file now. **Click Create a Configuration File** to continue. Enter your database credentials for your local web server on the third screen, as well as the database table prefix you want to use (default is `wp_`). After you complete all the fields, **click Submit**. WordPress will check that it can connect to your database with the information you provided. If successful, **click Run the install** to proceed.
-->

**WordPress にファイルを作成させる場合は**、今すぐファイルを作成するかどうかを尋ねる画面が表示されます。**設定ファイルの作成**をクリックして、次に進みます。3番目の画面で、ローカルの Web サーバーのデータベース認証情報と、使用するデータベーステーブルの接頭辞を入力します (デフォルトは `wp_`)。すべての項目を入力したら、**送信**をクリックします。WordPress は、提供された情報を使って、データベースに接続できるかどうかを確認します。成功したら、**インストール実行**をクリックして次に進みます。

<!--
You will then do the “5 minute install”, complete all the fields, and **click Install WordPress** to complete the installation. **Click Log In** on the Success screen, enter your username and password, and configure your settings.
-->

その後、「5分インストール」を行い、すべての項目を入力し、**WordPress をインストール**をクリックするとインストールが完了します。インストールが成功した画面で**ログイン**をクリックし、ユーザー名とパスワードを入力し、設定を行います。

<!--
**Note:** Under the new configuration, WordPress will create the `wp-config.php` file in the root directory of your local repository, not in the `/src/` directory.
-->

**備考:** 新しい設定では、WordPress は `wp-config.php` ファイルを `/src/` ディレクトリではなく、あなたのローカルリポジトリのルートディレクトリに作成します。

<!--
### 4\. Edit wp-config.php
-->

### 4\. wp-config.php の編集

<!--
Your local install will be used for beta testing, fixing bugs, creating/testing patches, and running unit tests, so it is important for you to see error messages and notices. Open `wordpress-svn/wp-config.php` in your plain text editor, and set `WP_DEBUG` to **true**:
-->

ローカルインストールはベータテストやバグ修正、パッチの作成やテストに使用されるため、エラーメッセージや通知を見ることができるのは重要です。プレーンテキストエディターで `wordpress-svn/wp-config.php` を開き、`WP_DEBUG` を **true** に設定します。

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
### 5\. Updating Your Subversion Install
-->

### 5\. Subversion インストールのアップデート

<!--
You will need to run the latest version of WordPress trunk on your local SVN install while testing, fixing bugs, and contributing patches.
-->

テスト、バグ修正、パッチでの貢献を行っている間は、ローカルの SVN インストールで最新バージョンの WordPress trunk を実行する必要があります。

<!--
WordPress 3.7 [introduces automatic updates](https://make.wordpress.org/core/2013/09/24/automatic-core-updates/) for minor stable WordPress releases (3.7.x). This feature, by default, does not work for Subversion installs.
-->

WordPress 3.7では、WordPress のマイナーな安定版リリース (3.7.x) に対して[自動更新を導入](https://codex.wordpress.org/Configuring_Automatic_Background_Updates)しています。この機能は、デフォルトでは、Subversion インストールでは機能しません。

<!--
You will need to manually update your local SVN install. The instructions below are for updating to the latest version of WordPress trunk using either TortoiseSVN or the command line.
-->

ローカルの SVN インストールを手動で更新する必要があります。以下の手順は、TortoiseSVN またはコマンドラインを使用して WordPress trunk の最新版に更新するものです。

<!--
#### 5.1 Using TortoiseSVN
-->

#### 5.1 TortoiseSVN の使用

<!--
To update your local WordPress SVN install using TortoiseSVN, right-click in the root folder (e.g. **wordpress-svn**) and **select SVN Update**.
-->

TortoiseSVN を使用してローカルの WordPress SVN インストールを更新するには、ルートフォルダー (例: **wordpress-svn**) を右クリックし、**SVN Update** を選択してください。

<!--
![TortoiseSVN Update Local Subversion Screen](https://make.wordpress.org/core/files/2013/09/tortoisesvn-update-1.png)
-->

![TortoiseSVN によるローカル Subversion を更新する画面](https://make.wordpress.org/core/files/2013/09/tortoisesvn-update-1.png)

<!--
The changed files will begin downloading. Most files will show the action as **Updated**, but you may see some with an action of **Added** (indicating a new file), or **Deleted** (indicating a file has been removed).
-->

変更されたファイルのダウンロードが開始されます。ほとんどのファイルは **Updated** と表示されますが、**Added** (新しいファイル)、**Deleted** (ファイルが削除された) と表示される場合もあります。

<!--
Once the update is complete, you will see a message at the bottom of the window with the revision number that the update included changed files for.
-->

アップデートが完了すると、ウィンドウの下部に、アップデートによって変更されたファイルが含まれるリビジョン番号のメッセージが表示されます。

<!--
#### 5.2 Using Command Line
-->

#### 5.2 コマンドラインの使用

<!--
To update your local WordPress SVN install using the command line, **open your command line client** and change the directory to your WordPress SVN install:
-->

コマンドラインを使用してローカルの WordPress SVN インストールを更新するには、**コマンドラインクライアントを開き**、WordPress SVN インストールにディレクトリを変更します。

```bash
$ cd ~/wordpress-svn
```

<!--
You will then use the SVN update command to download any changed files from the WordPress Subversion repository:
-->

SVN update コマンドを使用して、WordPress Subversion リポジトリから変更されたファイルをダウンロードします。

```bash
$ svn up
```

<!--
## Next Steps
-->

## 次のステップ

<!--
*   [Beta Testing](https://make.wordpress.org/core/handbook/testing/beta/)
*   [Submitting a Patch](https://make.wordpress.org/core/handbook/tutorials/trac/submitting-a-patch/)
-->

*   [ベータテスト](https://ja.wordpress.org/team/handbook/core/testing/beta/)
*   [パッチの提出](https://ja.wordpress.org/team/handbook/core/tutorials/trac/submitting-a-patch/)

<!--
### Learn More
-->

### より詳しく

*   [Creating a WordPress site using SVN](http://ottopress.com/2011/creating-a-wordpress-site-using-svn/)
*   [WordPress Workflow Tips: Using Subversion Externals for Plugins, Themes and Core](http://kovshenin.com/2012/wordpress-workflow-tips-using-subversion-externals-for-plugins-themes-and-core/)
*   [Installing WordPress With Clean Subversion Repositories](https://codex.wordpress.org/Installing_WordPress_With_Clean_Subversion_Repositories)
*   [Installing/Updating WordPress with Subversion](https://codex.wordpress.org/Installing/Updating_WordPress_with_Subversion)
