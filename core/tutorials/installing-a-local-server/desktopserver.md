<!--
# Installing DesktopServer
-->

# DesktopServer のインストール

<!--
## Overview
-->

## 概要

<!--
[DesktopServer](http://serverpress.com/products/desktopserver/) is a local server package that runs on Mac and Windows. The installation, configuration, and site creation steps are almost identical for both platforms.
-->

[DesktopServer](http://serverpress.com/products/desktopserver/) は、Mac と Windows 上で動作するローカルサーバーのパッケージです。インストール、設定、サイト作成の手順は、どちらのプラットフォームでもほぼ同じです。

<!--
This article will walk you through the steps to install DesktopServer on your computer.
-->

この記事では、DesktopServer をコンピューターにインストールするための手順を説明します。

<!--
## Installing DesktopServer
-->

## DesktopServer のインストール

<!--
### 1\. Downloading DesktopServer
-->

### 1\. DesktopServer のダウンロード

<!--
Download the installer file for the [latest free version of DesktopServer](http://serverpress.com/downloads/) (currently 3.9.4), and save the file to your computer. Scroll down the page to download the free version for your operating system.
-->

[DesktopServer の最新の無償版](http://serverpress.com/downloads/) (現在3.9.4) のインストーラファイルをダウンロードし、コンピューターに保存します。ページを下にスクロールして、お使いのオペレーティングシステムに対応した無償版をダウンロードしてください。

<!--
![Download DesktopServer Screen](https://make.wordpress.org/core/files/2013/07/desktopserver-download.png)
-->

![DesktopServer のダウンロード画面](https://make.wordpress.org/core/files/2013/07/desktopserver-download.png)

<!--
The download is about 100mb, so it will take a few minutes.
-->

ダウンロードは約100MB ですので、数分かかるでしょう。

<!--
### 2\. Installing DesktopServer
-->

### 2\. DesktopServer のインストール

<!--
Once the download is complete, extract the contents of the zip file to a folder on your computer.
-->

ダウンロードが完了したら、ZIP ファイルの中身をパソコンのフォルダーに解凍してください。

<!--
You should use the DesktopServer installer for new installations, as it performs checks for conflicts on your computer. The installer file’s icon is a blue box with a green arrow. **Open the installer file** to begin the installation.
-->

DesktopServer のインストーラは、コンピューターのコンフリクトのチェックを行うため、新規インストールには DesktopServer のインストーラを使用する必要があります。インストーラファイルのアイコンは、青い枠に緑の矢印です。**インストーラファイルを開く**と、インストールが開始されます。

<!--
The first screen that appears will ask you whether you want to install, upgrade, or uninstall DesktopServer. **Choose New DesktopServer Limited Installation**, then **click Continue**.
-->

最初に表示される画面では、DesktopServer のインストール、アップグレード、またはアンインストールを行うかどうかを尋ねられます。**DesktopServer の新しい限定インストール**を選択し、**続行**をクリックしてください。

<!--
![DesktopServer Choose New Installation Screen](https://make.wordpress.org/core/files/2013/07/desktopserver-install-1.png)
-->

![DesktopServer 新規インストールを選択する画面](https://make.wordpress.org/core/files/2013/07/desktopserver-install-1.png)

<!--
You will be presented with the License Agreement screen next. Read the agreement, then **click Accept**.
-->

次に「使用許諾契約書」の画面が表示されます。契約内容をご確認の上、**許可する**をクリックしてください。

<!--
![DesktopServer License Agreement Screen](https://make.wordpress.org/core/files/2013/07/desktopserver-install-2.png)
-->

![DesktopServer 使用許諾契約画面](https://make.wordpress.org/core/files/2013/07/desktopserver-install-2.png)

<!--
The next screen shows DesktopServer extracting the files into the correct location on your computer:
-->

次の画面では、DesktopServer がファイルをコンピューターの適切な場所に展開する様子が表示されます:

*   **Mac:** Macintosh HD/Applications/XAMPP/
*   **Windows:** C:/xampplite/

<!--
![DesktopServer Unpacking Files Screen](https://make.wordpress.org/core/files/2013/07/desktopserver-install-3.png)
-->

![DesktopServer ファイル解凍画面](https://make.wordpress.org/core/files/2013/07/desktopserver-install-3.png)

<!--
Once all of the files have been extracted, the Installation Complete screen will appear. **Click Finish** to complete the installation.
-->

すべてのファイルの解凍が完了すると、「インストール完了」画面が表示されます。**終了をクリック**すると、インストールが完了します。

<!--
![DesktopServer Installation Complete Screen](https://make.wordpress.org/core/files/2013/07/desktopserver-install-4.png)
-->

![DesktopServer インストールの完了画面](https://make.wordpress.org/core/files/2013/07/desktopserver-install-4.png)

<!--
A small window will appear, with the install location and how to start DesktopServer. **Click OK** to close the window, then **click Finish** on the main screen to close the installer.
-->

小さなウィンドウが表示され、インストール先と DesktopServer の起動方法が表示されます。**OK をクリック**してウィンドウを閉じ、メイン画面の **終了をクリック**してインストーラを終了します。

<!--
![DesktopServer Close Installer Screen](https://make.wordpress.org/core/files/2013/07/desktopserver-install-5.png)
-->

![DesktopServer インストーラを終了する画面](https://make.wordpress.org/core/files/2013/07/desktopserver-install-5.png)

<!--
### 3\. Configuring DesktopServer
-->

### 3\. DesktopServer の設定

<!--
DesktopServer includes the latest stable release of WordPress when you install the program (currently 3.6.1). The program also allows you to add other versions of WordPress in the Blueprints folder, including beta releases, as well as create a custom package for installing WordPress via Subversion (SVN). Any new packages you create will automatically show up in the Blueprint dropdown when you create a new local site. The following shows the location of the Blueprints folder:
-->

DesktopServer には、プログラムのインストール時に WordPress の最新の安定版リリースが含まれます (現在は3.6.1)。またこのプログラムでは、ベータ版リリースを含む他のバージョンの WordPress を Blueprints フォルダーに追加したり、Subversion (SVN) 経由で WordPress をインストールするためのカスタムパッケージを作成できます。作成した新しいパッケージは、新しいローカルサイトを作成する際に、Blueprint のドロップダウンに自動的に表示されます。以下は、Blueprints フォルダーの場所を示しています:

*   **Mac:** Macintosh HD/Applications/XAMPP/blueprints/
*   **Windows:** C:/xampplite/blueprints/

<!--
To add the latest alpha release, **download the zip file of the [latest nightly build](https://wordpress.org/nightly-builds/wordpress-latest.zip)**, and place it in the Blueprints folder. Make sure the zip file has the appropriate beta release name (e.g. **wordpress-3.8-alpha.zip**).
-->

最新のアルファリリースを追加するには、**[最新のナイトリービルド](https://wordpress.org/nightly-builds/wordpress-latest.zip)の ZIP ファイルをダウンロード**し、Blueprints フォルダーに配置します。ZIP ファイルには適切なベータ版リリース名 (例: **wordpress-3.8-alpha.zip**) が含まれていることを確認してください。

<!--
![DesktopServer Blueprints Folder File Structure](https://make.wordpress.org/core/files/2013/07/desktopserver-blueprints-file-structure-1.png)
-->

![DesktopServer Blueprints フォルダーのファイル構成](https://make.wordpress.org/core/files/2013/07/desktopserver-blueprints-file-structure-1.png)

<!--
To create a blank package for installing WordPress via SVN, **create a new subfolder** called **Blank (WordPress SVN)** in the Blueprints folder. **Copy the `index.html` file** from the **Blank (non-WordPress)** subfolder, then add a copy of the `wp-config-sample.php` file from the latest WordPress release. This file is needed during site creation so DesktopServer can create a `wp-config.php` file with the database credentials for that local site.
-->

SVN 経由で WordPress をインストールするためのブランクパッケージを作成するには、Blueprints フォルダー内に **Blank (WordPress SVN)** という**新しいサブフォルダーを作成**します。**Blank (non-WordPress)** サブフォルダーから `index.html` ファイルをコピーし、最新の WordPress リリースから `wp-config-sample.php` ファイルをコピーして追加してください。このファイルは、DesktopServer がローカルサイトのデータベース認証情報を含む `wp-config.php` ファイルを作成するために、サイト作成時に必要です。

<!--
![DesktopServer Blank (WordPress SVN) File Structure](https://make.wordpress.org/core/files/2013/07/desktopserver-blueprints-file-structure-2.png)
-->

![DesktopServer Blank (WordPress SVN) ファイル構造](https://make.wordpress.org/core/files/2013/07/desktopserver-blueprints-file-structure-2.png)

<!--
### 4\. Starting DesktopServer
-->

### 4\. DesktopServer の実行

<!--
Once you’ve completed the installation and configuration process, **navigate to the install directory** and open the program.
-->

インストールと設定が完了したら、**インストール先ディレクトリに移動**して、プログラムを開きます。

<!--
Tip: Create a program shortcut (or alias) on your desktop or dock to make it easier to start DesktopServer each time.
-->

ヒント: デスクトップまたはドックにプログラムのショートカット (またはエイリアス) を作成すると、DesktopServer を毎回簡単に起動できます。

<!--
DesktopServer needs to run with Administrator Privileges on both Mac and Windows. On the start-up screen, **select Yes**, then **click Next** to restart DesktopServer and grant those privileges.
-->

DesktopServer は、Mac と Windows の両方において Administrator 権限で実行する必要があります。スタートアップ画面で、**はいを選択**し、**次へをクリック**をクリックすると、DesktopServer が再起動し、これらの権限が付与されます。

<!--
![DesktopServer Grant Administrator Privileges Screen](https://make.wordpress.org/core/files/2013/07/desktopserver-start-1.png)
-->

![DesktopServer 管理者権限を付与する画面](https://make.wordpress.org/core/files/2013/07/desktopserver-start-1.png)

<!--
Next you will need to start Apache and MySQL services. On the next screen, **select Yes**, then **click Next**.
-->

次に、Apache と MySQL のサービスを開始する必要があります。次の画面で、**はいを選択**し、**次へをクリック**します。

<!--
![DesktopServer Start Apache and MySQL Services Screen](https://make.wordpress.org/core/files/2013/07/desktopserver-start-2.png)
-->

![DesktopServer Apache と MySQL サービスを起動する画面](https://make.wordpress.org/core/files/2013/07/desktopserver-start-2.png)

<!--
The final startup screen will appear, indicating that both services have been started. **Click Next** to create your first local site.
-->

最終的な起動画面が表示され、両方のサービスが開始されたことが示されます。**次へをクリック**すると、最初のローカルサイトが作成されます。

<!--
![DesktopServer Services Started Screen](https://make.wordpress.org/core/files/2013/07/desktopserver-start-3.png)
-->

![DesktopServer サービスが開始された画面](https://make.wordpress.org/core/files/2013/07/desktopserver-start-3.png)

<!--
### 5\. Creating A New Local Site
-->

### 5\. 新しいローカルサイトの作成

<!--
Now it’s time for you to create your first local site to use for testing WordPress. **Select Create a New Development Website**, then **click Next**.
-->

さて、WordPress のテストに使用する最初のローカルサイトを作成するときが来ました。**新しい開発用 Web サイトを作成するを選択**し、**次へをクリック**します。

<!--
![DesktopServer Create A New Development Website Screen](https://make.wordpress.org/core/files/2013/07/desktopserver-create-new-site-1.png)
-->

![DesktopServer 新しい開発用ウェブサイトを作成する画面](https://make.wordpress.org/core/files/2013/07/desktopserver-create-new-site-1.png)

<!--
The next screen asks for the information about the site you want to create.
-->

次の画面では、作成するサイトの情報を尋ねられます。

<!--
*   **Site Name:** Enter your desired site name (e.g. **wordpress-trunk**) in the first box.
*   **Blueprint:** To install the WordPress alpha release, you will **choose WordPress-3.8-alpha.zip** (or the latest beta release) for your blueprint.
*   **Site Root:** DesktopServer will automatically display the default location where WordPress will be installed. If you would like to change the location to another folder (such as **/htdocs/**), **click Browse**, select the desired folder, then **click Okay**.
-->

*   **サイト名:** 最初のボックスに希望のサイト名 (例: **wordpress-trunk**) を入力してください。
*   **ブループリント:** WordPress のアルファリリースをインストールするには、Blueprint に **WordPress-3.8-alpha.zip** (または最新のベータリリース) を選択します。
*   **サイトルート:** DesktopServer は、WordPress がインストールされるデフォルトのロケーションを自動的に表示します。他のフォルダー (**/htdocs/** など) に場所を変更したい場合は、**参照** をクリックして希望のフォルダーを選択し、**OK をクリック**します。

<!--
Once you have completed all 3 fields, **click Create**.
-->

3つの項目をすべて入力したら、**作成をクリック**します。

<!--
![DesktopServer Create A New Development Website With 3.6 Beta4 Selected Screen](https://make.wordpress.org/core/files/2013/07/desktopserver-create-new-site-2.png)
-->

![DesktopServer 3.6Beta4で新規開発サイトを作成する画面](https://make.wordpress.org/core/files/2013/07/desktopserver-create-new-site-2.png)

<!--
Next, DesktopServer will create the source folder, virtual host, and server name entries; create a database and pre-configure the `wp-config.php` file with the database information; and restart the Apache and MySQL services. Once those are done, **click Next** to continue.
-->

次に、DesktopServer は、ソースフォルダー、バーチャルホスト、およびサーバー名のエントリーを作成し、データベースを作成して `wp-config.php` ファイルにデータベース情報を事前に設定し、Apache と MySQL サービスを再起動します。これらの作業が完了したら、**次へをクリック**して続行します。

<!--
![DesktopServer Create Local Site Process Screen](https://make.wordpress.org/core/files/2013/07/desktopserver-create-new-site-3.png)
-->

![DesktopServer ローカルサイトの作成プロセス画面](https://make.wordpress.org/core/files/2013/07/desktopserver-create-new-site-3.png)

<!--
You will be able to access your WordPress install at the URL listed on the next screen. Clicking the URL will bring up the WordPress install screen, where you will enter your site title, desired username, choice of a password (twice), and your e-mail address. **Click Install WordPress** to complete the installation.
-->

次の画面に記載されている URL から、WordPress のインストールにアクセスできます。URL をクリックすると、WordPress のインストール画面が表示されるので、サイトのタイトル、希望するユーザー名、パスワードの選択 (2回)、メールアドレスを入力してください。**WordPress のインストールをクリック**し、インストールを完了させてください。

<!--
![DesktopServer Access New Site Screen](https://make.wordpress.org/core/files/2013/07/desktopserver-access-new-site.png)
-->

![DesktopServer 新しいサイトにアクセスする画面](https://make.wordpress.org/core/files/2013/07/desktopserver-access-new-site.png)

<!--
**Note:** After you have finished installing the latest WordPress beta release, you will need to do the following 2 things:
-->

**注意:** WordPress の最新ベータ版のインストールが完了した後に、以下の2つの作業を行う必要があります:

<!--
*   It is important that you to set `WP_DEBUG` to **true** in your `wp-config.php` file to display errors, warnings, etc. during testing:

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

*   You will need to install and activate the [WordPress Beta Tester plugin](https://wordpress.org/extend/plugins/wordpress-beta-tester/) to upgrade the install from the latest beta release to the latest bleeding-edge version of WordPress trunk. Once installed, **follow the directions** for [configuring the plugin](https://make.wordpress.org/core/handbook/installing-wordpress-locally/installing-from-a-zip-file/#4-install-the-beta-tester-plugin) to update to the bleeding edge nightlies.
-->

*   テスト中にエラーや警告を表示するために、`wp-config.php` ファイルで `WP_DEBUG` を **true** に設定することが重要です:

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

*   [WordPress Beta Tester プラグイン](https://wordpress.org/extend/plugins/wordpress-beta-tester/)をインストールして有効化し、最新のベータ版から WordPress trunk の最新ブリーディングエッジバージョンにインストールをアップグレードすることが必要です。インストールしたら、[プラグインの設定](https://ja.wordpress.org/team/handbook/core/installing-wordpress-locally/from-zip/#4-install-the-beta-tester-plugin)の**指示に従って**、ブリーディングエッジのナイトリーに更新してください。

<!--
### 6\. Shutting Down DesktopServer
-->

### 6\. DesktopServer のシャットダウン

<!--
To shut down DesktopServer, double-click the shortcut on your screen. On the first screen, **select Stop or restart web and database services**, then **click Next**.
-->

DesktopServer をシャットダウンするには、画面上のショートカットをダブルクリックします。最初の画面で、**Web サービスとデータベースサービスを停止または再起動する** を選択し、**次へをクリック**します。

<!--
![DesktopServer Stop Services Screen](https://make.wordpress.org/core/files/2013/07/desktopserver-shutdown-1.png)
-->

![DesktopServer サービスを停止する画面](https://make.wordpress.org/core/files/2013/07/desktopserver-shutdown-1.png)

<!--
You will be asked to confirm whether you want to restart or stop the services. **Select Stop web and database services**, then **click Next**.
-->

サービスを再起動するか停止するかを確認する画面が表示されます。**Web サービスとデータベースサービスの停止を選択**し、**次へをクリック**します。

<!--
![DesktopServer Confirm Stop Services Screen](https://make.wordpress.org/core/files/2013/07/desktopserver-shutdown-2.png)
-->

![DesktopServer サービスを停止する確認画面](https://make.wordpress.org/core/files/2013/07/desktopserver-shutdown-2.png)

<!--
DesktopServer will then shut down the Apache and MySQL services. Once this task is completed, **click Close** to exit the program.
-->

DesktopServer は、Apache と MySQL のサービスをシャットダウンします。このタスクが完了したら、**閉じるをクリック**して、プログラムを終了します。

<!--
![DesktopServer Close Program Screen](https://make.wordpress.org/core/files/2013/07/desktopserver-shutdown-3.png)
-->

![DesktopServer プログラムを閉じる画面](https://make.wordpress.org/core/files/2013/07/desktopserver-shutdown-3.png)

<!--
## Next Steps
-->

## 次のステップ

<!--
*   [Installing WordPress Via SVN](https://make.wordpress.org/core/handbook/tutorials/installing-wordpress-locally/from-svn/)
-->

*   [SVN によるインストール](https://ja.wordpress.org/team/handbook/core/installing-wordpress-locally/from-svn/)
