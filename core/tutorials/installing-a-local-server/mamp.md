<!--
# Installing MAMP
-->

# MAMP のインストール

<!--
## Overview
-->

## 概要

<!--
[MAMP](http://www.mamp.info/en/index.html) is a local server package which runs on a Mac, similar to packages for Windows and Linux, and is easy to set up and configure.
-->

[MAMP](http://www.mamp.info/en/index.html) は、Windows や Linux 用のパッケージと同様に Mac 上で動作するローカルサーバーパッケージで、セットアップや設定を簡単に行うことができます。

<!--
This article will walk you through the steps to install MAMP on your computer.
-->

この記事では、コンピューターに MAMP をインストールする手順を説明します。

<!--
## Installing MAMP
-->

## MAMP のインストール

<!--
### 1\. Downloading MAMP
-->

### 1\. MAMP のダウンロード

<!--
Download the installer package for the [latest free version of MAMP](http://www.mamp.info/en/) by **clicking on the gray elephant icon on the left**, and save the file to your computer. There is also a MAMP Pro version available which has more advanced options, but most users will find the free version works fine for their needs.
-->

[MAMP の 最新無料版](http://www.mamp.info/en/)のインストーラパッケージを、**左の灰色の象のアイコンをクリックして**ダウンロードし、ファイルをコンピューターに保存してください。より高度な機能を持つ MAMP Pro 版もありますが、ほとんどのユーザーは、無料版で問題なく使用できます。

<!--
![Download MAMP Screen](https://make.wordpress.org/core/files/2013/06/download-mamp.png)
-->

![MAMP のダウンロード画面](https://make.wordpress.org/core/files/2013/06/download-mamp.png)

<!--
The installer package is around 140mb, so it will take a few minutes for the download to complete.
-->

インストーラパッケージは約140mb あるため、ダウンロードが完了するまで数分かかると思います。

<!--
### 2\. Installing MAMP
-->

### 2\. MAMP のインストール

<!--
Once the download is complete, **double-click the zip file** and extract the contents to your desktop. You will see an installer file called **MAMP\_2.1.4.pkg** (your version may be different) – **double-click that file** to run the installer. There are 7 steps in the MAMP install process:
-->

ダウンロードが完了したら、**zip ファイルをダブルクリック**して、デスクトップに解凍してください。インストーラファイルの名前は **MAMP_2.1.4.pkg** (あなたのバージョンとは異なるかもしれません) です。**そのファイルをダブルクリック**してインストーラを実行してください。MAMP のインストールは7つのステップで行われます。

<!--
*   **Introduction – Welcome to the MAMP Installer Screen**: MAMP will guide you through the steps necessary to install the application. **Click Continue** to go to the next step.
*   **Read Me – Important Information Screen**: The installer will install both the MAMP and MAMP PRO applications. Do not remove or rename the MAMP folder. **Click Continue** for the next step.
*   **License – Software License Agreement Screen**: Select the language you wish to use with MAMP. Read the license agreement, **click Agree** in the small dropdown to accept the agreement, then **click Continue**.
*   **Destination Select**: MAMP must be installed in the Applications folder to work properly. **Click Continue** for the next step.
*   **Installation Type – Standard Install on “Macintosh HD” Screen**: This screen tells you how much disk space MAMP will use on your hard drive. **Click Install** to perform a standard installation of MAMP for all users of your computer. You can **click the Customize** button, which will allow you to opt out of installing MAMP PRO. **Click Install** to continue. The installer will prompt you to authenticate with your admin username and password. Enter the information requested, then **click Install Software**.
*   **Installation – Installing MAMP Screen**: The installation process takes several minutes. The screen will show you what part of the process is occurring, along with the estimated time remaining until installation is complete.
*   **Summary – Success Screen**: MAMP has been installed successfully. **Click Close**.
-->

* **はじめに - MAMP インストーラ画面へようこそ**: MAMP がアプリケーションのインストールに必要なステップを案内します。**Continue をクリックして** で次のステップに進みます。
* **Read Me - 重要なお知らせ画面**: インストーラは MAMP と MAMP PRO の両方のアプリケーションをインストールします。MAMP フォルダーを削除したり、名前を変更したりしないでください。**Continue をクリックして** 次のステップに進みます。
* **ライセンス - ソフトウェア使用許諾画面**: MAMP で使用したい言語を選択します。使用許諾を読み、小さなドロップダウンで **Agree をクリック** して同意し、**Continue をクリック**します。
* **インストール先の選択**: MAMP が正常に動作するためには、アプリケーションフォルダーにインストールされる必要があります。次のステップで **Continue をクリック**してください。
* **インストールの種類 - 「Macintosh HD」画面での標準インストール**: この画面では、MAMP がハードディスクで使用するディスク容量を表示します。**インストールをクリック**すると、お使いのコンピューターのすべてのユーザーに対して MAMP の標準インストールが実行されます。**カスタマイズボタンをクリック**すると、MAMP PRO のインストールをオプトアウトできます。**インストールをクリック**して続行します。インストーラは、管理者ユーザー名とパスワードで認証するよう促します。要求された情報を入力し、**ソフトウェアのインストールをクリック**します。
* **インストール - MAMP のインストール画面**: インストールには数分かかります。この画面では、インストールが完了するまでの残り時間とともに、プロセスのどの部分が実行されているかが表示されます。
* **概要 - インストールに成功した画面**: MAMP は正常にインストールされました。**Close をクリックします**。

<!--
### 3\. Starting MAMP
-->

### 3\. MAMP の実行

<!--
The MAMP Welcome page should automatically open in your browser after installation, which indicates that MAMP has been installed correctly. This page contains links to your PHP configuration (phpinfo), phpMyAdmin, as well as the standard MAMP configurations.
-->

インストール後、自動的に MAMP のウェルカムページがブラウザで開くはずですが、これは MAMP が正しくインストールされたことを示しています。このページには、PHP の設定 (phpinfo)、phpMyAdmin、および MAMP の標準的な設定へのリンクが含まれています。

<!--
If you don’t see the Welcome page, go to [http://localhost:8888/MAMP/](http://localhost:8888/MAMP/) in your browser.
-->

ウェルカムページが表示されない場合は、ブラウザで [http://localhost:8888/MAMP/](http://localhost:8888/MAMP/) にアクセスしてください。

<!--
The Welcome page also shows you the MySQL connection information you will need when you install WordPress:
-->

ウェルカムページには、WordPress をインストールする際に必要な MySQL の接続情報も表示されています。

<!--
![MySQL Connection Information on Welcome Page Screen](https://make.wordpress.org/core/files/2013/02/mamp6.png)
-->

![ウェルカムページ画面の MySQL 接続情報](https://make.wordpress.org/core/files/2013/02/mamp6.png)

<!--
The MAMP control panel also opens, which shows that your local MAMP server is working. You should see green indicators next to **Apache Server** and **MySQL Server**:
-->

MAMP のコントロールパネルも開き、ローカルの MAMP サーバーが動作していることがわかります。**Apache Server** と **MySQL Server** の横に緑色のインジケータが表示されているはずです。

<!--
![MAMP Control Panel Screen](https://make.wordpress.org/core/files/2013/06/mamp-control-panel.png)
-->

![MAMP コントロールパネル画面](https://make.wordpress.org/core/files/2013/06/mamp-control-panel.png)

<!--
From the control panel, you can stop your local servers by clicking **Stop Servers**, or start them by clicking **Start Servers**. You can also **open the Welcome page**, and access **Preferences**.
-->

コントロールパネルから、**Stop Servers** をクリックしてローカルサーバーを停止したり、**Start Servers** をクリックして起動したりできます。また、**ウェルカムページを開いたり**、**環境設定**にアクセスできます。

<!--
Note: When starting and stopping services or changing the configuration, MAMP may ask you for your admin username and password, which is required to make system changes in OS X.
-->

注意: サービスの起動、停止や設定の変更するときは、MAMP は OS X でシステム変更する際に必要な管理者ユーザー名とパスワードの入力を求めることがあります。

<!--
![MAMP Change Authentication Screen](https://make.wordpress.org/core/files/2013/06/mamp-change-authentication.png)
-->

![MAMP の認証変更画面](https://make.wordpress.org/core/files/2013/06/mamp-change-authentication.png)

<!--
### 4\. Configuring MAMP
-->

### 4\. MAMP の設定

<!--
During installation, MAMP sets the default ports for both Apache (port 8888) and MySQL (port 8889). Normally, web servers use port 80 for Apache, and port 3306 for MySQL. This allows access to web pages without having to append a port number to the domain in the URL.
-->

インストール時に、MAMP は Apache (ポート8888) と MySQL (ポート8889) の両方のデフォルトポートを設定します。通常、Web サーバーは Apache にポート80、MySQL にポート3306を使用します。これにより、URL のドメインにポート番号を付加することなく、Web ページにアクセスできます。

<!--
In MAMP, you have to append the port number to **localhost** in order to access web pages, i.e. [http://localhost:8888/wordpress-trunk/](http://localhost:8888/wordpress-trunk/).
-->

MAMP では、Web ページにアクセスするために **localhost** にポート番号を付加する必要があります。たとえば、[http://localhost:8888/wordpress-trunk/](http://localhost:8888/wordpress-trunk/) です。

<!--
You can change the ports to the normal Apache/MySQL ports by **clicking Preferences** in the control panel, then **clicking Ports**. You must have administrator privileges for your computer to do this.
-->

コントロールパネルの**環境設定をクリック**し、**ポートをクリック**すると、通常の Apache/MySQL のポートに変更できます。この操作を行うには、お使いのコンピューターの管理者権限が必要です。

<!--
![MAMP Change Default Ports Screen](https://make.wordpress.org/core/files/2013/06/mamp-change-ports.png)
-->

![MAMP のデフォルトポート変更画面](https://make.wordpress.org/core/files/2013/06/mamp-change-ports.png)

<!--
Changing those ports would allow you to access your local WordPress install without the port number, i.e. [http://localhost/wordpress-trunk/](http://localhost/wordpress-trunk/).
-->

これらのポートを変更すると、ポート番号なしでローカルの WordPress インストールにアクセスできます、つまり、[http://localhost/wordpress-trunk/](http://localhost/wordpress-trunk/) です。

<!--
**Caution:** There are other applications that use port 80, such as Skype. If you find you are unable to start Apache or access your local web pages, then you’ll need to find the conflicting application, and try to resolve the port conflict.
-->

**注意:** Skype など、ポート80を使用する他のアプリケーションもあります。Apache を起動できないまたはローカルの Web ページにアクセスできない場合、競合するアプリケーションを見つけ、ポートの競合を解決する必要があります。

<!--
For Skype, go to **Tools > Options**, click on **Advanced**, and then **Connections**. Uncheck the box next to **Use port 80 and 443 as alternatives for incoming connections**. Click **Save Options**, then restart Skype.
-->

Skype の場合は、**ツール > オプション**に移動して、**詳細**をクリックし、**接続**をクリックします。**追加の受信接続にポート80と443を使用**の隣のボックスのチェックをはずします。**オプションの保存**をクリックし、Skype を再起動します。

<!--
### 5\. Creating a MySQL Database With MAMP
-->

### 5\. MAMP で MySQL データベースを作成する

<!--
In MAMP, you need to **open phpMyAdmin** to create a MySQL database. If you have installed MAMP with the default ports, **open the Welcome page** in your browser ([http://localhost:8888/MAMP/](http://localhost:8888/MAMP/)), then **click the phpMyAdmin link** at the top of the screen.
-->

MAMP では、MySQL データベースを作成するために **phpMyAdmin** を開く必要があります。MAMP をデフォルトのポートでインストールした場合、ブラウザで**ウェルカムページを開き** ([http://localhost:8888/MAMP/](http://localhost:8888/MAMP/))、画面上部にある **phpMyAdmin のリンクをクリック**します。

<!--
The main phpMyAdmin screen will appear. To create a database, click **Databases** in the top navbar.
-->

phpMyAdmin のメイン画面が表示されます。データベースを作成するには、一番上のナビバーにある**データベース**をクリックします。

<!--
![MAMP Navbar On phpMyAdmin Main Screen](https://make.wordpress.org/core/files/2013/06/database-create-phpmyadmin-navbar.png)
-->

![phpMyAdmin のメイン画面にある MAMP ナビバー](https://make.wordpress.org/core/files/2013/06/database-create-phpmyadmin-navbar.png)

<!--
On the screen that appears, you need to enter the database name (for example, **root\_wordpress-trunk**) in the left field, choose your database connection collation from the dropdown box (**utf8\_unicode\_ci**), then **click Create**.
-->

表示された画面で、左側のフィールドにデータベース名 (例: **root\_wordpress-trunk**) を入力し、ドロップダウンボックスからデータベース接続照合順序 (**utf8\_unicode\_ci**) を選択し、**Create をクリック**してください。

<!--
![MAMP Create Database In phpMyAdmin Screen](https://make.wordpress.org/core/files/2013/06/database-create-name-collation.png)
-->

![MAMP phpMyAdmin でデータベースを作成する画面](https://make.wordpress.org/core/files/2013/06/database-create-name-collation.png)

<!--
You will see a success message once the database has been created, and your new database will appear in the list on the left.
-->

データベースが作成されると、成功のメッセージが表示され、左のリストに新しいデータベースが表示されます。

<!--
![MAMP Database Creation Success Message Screen](https://make.wordpress.org/core/files/2013/06/database-create-success-message.png)
-->

![MAMP データベース作成の成功メッセージ画面](https://make.wordpress.org/core/files/2013/06/database-create-success-message.png)

<!--
The default phpMyAdmin user, **root**, is automatically assigned to the database upon creation, and has a password of **root**. The database connection info you will need to use when installing WordPress locally is:
-->

データベースを作成すると、デフォルトの phpMyAdmin ユーザーである **root** が自動的に割り当てられ、パスワードは **root** になります。WordPress をローカルにインストールする際に必要なデータベース接続情報は以下の通りです。

<!--
```php
/** The name of the database for WordPress */
define('DB_NAME', 'root_databasename');</p>
<p>/** MySQL database username */
define('DB_USER', 'root');</p>
<p>/** MySQL database password */
define('DB_PASSWORD', 'root');</p>
<p>/** MySQL hostname */
define('DB_HOST', 'localhost');
```
-->

<!--
```php
/** The name of the database for WordPress */
define('DB_NAME', 'root_databasename');</p>
<p>/** MySQL database username */
define('DB_USER', 'root');</p>
<p>/** MySQL database password */
define('DB_PASSWORD', 'root');</p>
<p>/** MySQL hostname */
define('DB_HOST', 'localhost');
```
-->

```php
/** The name of the database for WordPress */
define('DB_NAME', 'root_databasename');
/** MySQL database username */
define('DB_USER', 'root');
/** MySQL database password */
define('DB_PASSWORD', 'root');
/** MySQL hostname */
define('DB_HOST', 'localhost');
```

<!--
### 6\. Shutting Down MAMP
-->

### 6\. MAMP のシャットダウン

<!--
To shut down MAMP, you will need to **click Stop Servers** to shut down the Apache and MySQL services. The indicators will turn red once all services have been shut down. You will then **click Quit** to close the program.
-->

MAMP をシャットダウンするには、**Stop Servers をクリック**して、Apache と MySQL のサービスをシャットダウンする必要があります。すべてのサービスが停止すると、インジケータが赤くなります。その後、**Quit をクリック**してプログラムを終了します。

<!--
![MAMP Shutdown Screen](https://make.wordpress.org/core/files/2013/06/mamp-shutdown.png)
-->

![MAMP のシャットダウン画面](https://make.wordpress.org/core/files/2013/06/mamp-shutdown.png)

<!--
## Next Steps
-->

## 次のステップ

<!--
*   [Installing WordPress From A Zip File](https://make.wordpress.org/core/handbook/tutorials/installing-wordpress-locally/from-zip/)
*   [Installing WordPress Via SVN](https://make.wordpress.org/core/handbook/tutorials/installing-wordpress-locally/from-svn/)
-->

*   [Zip ファイルからのインストール](https://make.wordpress.org/core/handbook/tutorials/installing-wordpress-locally/from-zip/)
*   [SVN によるインストール](https://make.wordpress.org/core/handbook/tutorials/installing-wordpress-locally/from-svn/)
