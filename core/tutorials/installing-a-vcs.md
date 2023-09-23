<!--
# Installing a Version Control System
-->

# バージョンコントロールシステムのインストール

<!--
When using an IDE (Integrated Developer Environment) application or a stand-alone GUI client application, chances are that a separate installation of Subversion or Git will not be needed. Most of these applications include a local copy of the version control system.
-->

IDE (統合開発環境) アプリケーションやスタンドアローンの GUI クライアントアプリケーションを使用している場合、Subversion や Git を個別にインストールする必要はないでしょう。これらのアプリケーションの多くは、バージョン管理システムのローカルコピーを含んでいます。

<!--
## Installing Subversion on a Mac
-->

## Mac に Subversion をインストールする

<!--
Prior to OS 10.8 (Mountain Lion), Macs came with Subversion pre-installed. Subversion has since been moved to the [Xcode developer package](https://developer.apple.com/xcode/).
-->

OS 10.8 (Mountain Lion) 以前の Mac には、Subversion がプリインストールされていました。Subversion はその後、[Xcode 開発者パッケージ](https://developer.apple.com/xcode/)に移されました。

<!--
This article will walk you through the steps to install Subversion on your Mac.
-->

この記事では、Mac に Subversion をインストールするための手順を説明します。

<!--
### 1\. Download The Package
-->

### 1\. パッケージのダウンロード

<!--
You can install [Xcode](https://developer.apple.com/xcode/) to set up Subversion on your Mac; however, the download package is around 1.5 GB.
-->

[Xcode](https://developer.apple.com/xcode/) をインストールして、Mac に Subversion をセットアップできます。しかし、ダウンロードパッケージは約1.5GB あります。

<!--
Instead, you can download Apple’s Command Line Tools from Apple’s Mac Developer website. You will need an Apple ID to download the files.
-->

代わりに、Apple の Mac 開発者 Web サイトから、Apple のコマンドラインツールをダウンロードできます。ファイルをダウンロードするには、Apple ID が必要です。

<!--
Log in to [Apple’s Developer tools](https://developer.apple.com/downloads/index.action). Search for Command Line Tools, and download the correct package for your operating system.
-->

[Apple の開発者ツール](https://developer.apple.com/downloads/index.action)にログインしてください。コマンドラインツールを検索し、あなたのオペレーティングシステムに適したパッケージをダウンロードします。

<!--
### 2\. Install
-->

### 2\. インストール

<!--
Install the package.
-->

パッケージをインストールします。

<!--
### 3\. Verify the installation
-->

### 3\. インストールの確認

<!--
You can verify the installation by typing:
-->

以下のように入力すると、インストールが確認できます。

```bash
$  svn --version
```

<!--
You should see something like this:
-->

このように表示されるはずです。

<!--
```bash
svn, version 1.7.10 (r1485443)
   compiled Aug 13 2013, 15:31:22</p>
<p>Copyright (C) 2013 The Apache Software Foundation.
This software consists of contributions made by many people; see the NOTICE
file for more information.
Subversion is open source software, see http://subversion.apache.org/</p>
<p>The following repository access (RA) modules are available:</p>
<p>* ra_neon : Module for accessing a repository via WebDAV protocol using Neon.
  - handles 'http' scheme
  - handles 'https' scheme
* ra_svn : Module for accessing a repository using the svn network protocol.
  - handles 'svn' scheme
* ra_local : Module for accessing a repository on local disk.
  - handles 'file' scheme
* ra_serf : Module for accessing a repository via WebDAV protocol using serf.
  - handles 'http' scheme
  - handles 'https' scheme
```
-->

<!--
```bash
svn, version 1.7.10 (r1485443)
   compiled Aug 13 2013, 15:31:22</p>
<p>Copyright (C) 2013 The Apache Software Foundation.
This software consists of contributions made by many people; see the NOTICE
file for more information.
Subversion is open source software, see http://subversion.apache.org/</p>
<p>The following repository access (RA) modules are available:</p>
<p>* ra_neon : Module for accessing a repository via WebDAV protocol using Neon.
  - handles 'http' scheme
  - handles 'https' scheme
* ra_svn : Module for accessing a repository using the svn network protocol.
  - handles 'svn' scheme
* ra_local : Module for accessing a repository on local disk.
  - handles 'file' scheme
* ra_serf : Module for accessing a repository via WebDAV protocol using serf.
  - handles 'http' scheme
  - handles 'https' scheme
```
-->

```bash
svn, version 1.7.10 (r1485443)
   compiled Aug 13 2013, 15:31:22
Copyright (C) 2013 The Apache Software Foundation.
This software consists of contributions made by many people; see the NOTICE
file for more information.
Subversion is open source software, see http://subversion.apache.org/
The following repository access (RA) modules are available:
* ra_neon : Module for accessing a repository via WebDAV protocol using Neon.
  - handles 'http' scheme
  - handles 'https' scheme
* ra_svn : Module for accessing a repository using the svn network protocol.
  - handles 'svn' scheme
* ra_local : Module for accessing a repository on local disk.
  - handles 'file' scheme
* ra_serf : Module for accessing a repository via WebDAV protocol using serf.
  - handles 'http' scheme
  - handles 'https' scheme
```

<!--
Subversion is now installed and ready to use.
-->

これで、Subversion がインストールされ、使用できるようになりました。

<!--
## Installing TortoiseSVN
-->

## TortoiseSVN のインストール

<!--
[TortoiseSVN](http://tortoisesvn.net/) is an Apache Subversion (SVN) client, implemented as a Windows shell extension. It’s intuitive and easy to use, and doesn’t require the Subversion command line client to run.
-->

[TortoiseSVN](http://tortoisesvn.net/) は Apache Subversion (SVN) のクライアントで、Windows のシェル拡張として実装されています。直感的で使いやすく、実行するために Subversion のコマンドラインクライアントを必要としません。

<!--
This section will walk you through the steps to install TortoiseSVN on your computer.
-->

このセクションでは、コンピューターに TortoiseSVN をインストールするための手順を説明します。

<!--
### 1\. Downloading TortoiseSVN
-->

### 1\. TortoiseSVN のダウンロード

<!--
Download the [latest version of TortoiseSVN](http://tortoisesvn.net/downloads.html), and save the installer file to your computer.
-->

[TortoiseSVN の最新バージョン](http://tortoisesvn.net/downloads.html)をダウンロードし、インストーラファイルをコンピューターに保存します。

<!--
![Download TortoiseSVN](https://make.wordpress.org/core/files/2013/02/tortoisesvn-download.png)
-->

![TortoiseSVN のダウンロード](https://make.wordpress.org/core/files/2013/02/tortoisesvn-download.png)

<!--
### 2\. Installing TortoiseSVN
-->

### 2\. TortoiseSVN のインストール

<!--
Next, you need to open the folder where you saved the file, and double-click the installer file. A security warning window will open, asking if you want to run this file. **Click Run** to start the installation process.
-->

次に、ファイルを保存したフォルダーを開き、インストーラファイルをダブルクリックします。セキュリティ警告ウィンドウが開き、このファイルを実行するかどうか尋ねられます。**実行をクリック**すると、インストールが始まります。

<!--
![TortoiseSVN Open File Warning Screen](https://make.wordpress.org/core/files/2013/02/tortoisesvn-installing-run-file1.png)
-->

![TortoiseSVN ファイルを開くときの警告画面](https://make.wordpress.org/core/files/2013/02/tortoisesvn-installing-run-file1.png)

<!--
You will now see the welcome screen, which will confirm the version of TortoiseSVN that you are going to install. **Click Next** to continue.
-->

ウェルカム画面が表示され、インストールする TortoiseSVN のバージョンを確認されます。**次へをクリック**し、次に進みます。

<!--
![TortoiseSVN Installation Welcome Screen](https://make.wordpress.org/core/files/2013/02/tortoisesvn-installing-1.png)
-->

![TortoiseSVN のインストール画面](https://make.wordpress.org/core/files/2013/02/tortoisesvn-installing-1.png)

<!--
The next screen you are presented with is the End-User License Agreement (EULA). Read the agreement, check the radio button next to **I accept the terms in the License Agreement**, then **click Next** to continue the installation.
-->

次に表示される画面は、エンドユーザー使用許諾契約 (EULA) です。契約書を読み、**使用許諾契約の条項に同意する** のラジオボタンをチェックし、**次へをクリック**してインストールを続行します。

<!--
![TortoiseSVN End-User License Agreement Screen](https://make.wordpress.org/core/files/2013/02/tortoisesvn-installing-21.png)
-->

![TortoiseSVN のエンドユーザー使用許諾契約画面](https://make.wordpress.org/core/files/2013/02/tortoisesvn-installing-21.png)

<!--
The Custom Setup screen will appear next. This screen will allow you to choose which components you would like to install. Unless you are dangerously low on disk space, you shouldn’t need to change anything. **Click Next** to continue.
-->

次に、カスタムセットアップ画面が表示されます。この画面では、インストールするコンポーネントを選択できます。ディスク容量がとても少ない場合を除き、何も変更する必要はないはずです。**次へをクリック**してください。

<!--
![TortoiseSVN Custom Setup Screen](https://make.wordpress.org/core/files/2013/02/tortoisesvn-installing-3.png)
-->

![TortoiseSVN のカスタムセットアップ画面](https://make.wordpress.org/core/files/2013/02/tortoisesvn-installing-3.png)

<!--
Once the Confirm Installation screen appears, you are ready to start the installation process. **Click Install** to begin the process.
-->

インストールを確認する画面が表示されたら、インストールを開始する準備が整いました。**インストールをクリック**すると、処理が開始されます。

<!--
![TortoiseSVN Confirm Installation Screen](https://make.wordpress.org/core/files/2013/02/tortoisesvn-installing-4.png)
-->

![TortoiseSVN のインストール確認画面](https://make.wordpress.org/core/files/2013/02/tortoisesvn-installing-4.png)

<!--
The Installation Status screen will appear, which shows you the status of the installation process. Once the progress bar is completely green, **click Next**.
-->

インストール状況を示す画面が表示され、インストール作業の状況がわかります。プログレスバーが完全に緑色になったら、**次へをクリック**します。

<!--
![TortoiseSVN Installation Status Screen](https://make.wordpress.org/core/files/2013/02/tortoisesvn-installing-5.png)
-->

![TortoiseSVN のインストール状況を示す画面](https://make.wordpress.org/core/files/2013/02/tortoisesvn-installing-5.png)

<!--
The Installation Complete screen will now appear. Congratulations, you have now installed TortoiseSVN. **Click Finish** to complete the installation.
-->

これで、インストール完了の画面が表示されます。おめでとうございます。これで TortoiseSVN のインストールが完了しました。**終了をクリック**して、インストールを完了します。

<!--
![TortoiseSVN Installation Complete Screen](https://make.wordpress.org/core/files/2013/02/tortoisesvn-installing-7.png)
-->

![TortoiseSVN のインストール完了画面](https://make.wordpress.org/core/files/2013/02/tortoisesvn-installing-7.png)

<!--
### 3\. Configuring TortoiseSVN
-->

### 3\. TortoiseSVN の設定

<!--
TortoiseSVN adds a few items to your context menu during installation, including a way to access the settings panel. To review and change any of the default settings, right-click inside any folder, go to **TortoiseSVN**, then select **Settings** in the submenu.
-->

TortoiseSVN はインストール中に、設定パネルにアクセスする方法を含む、いくつかの項目をコンテキストメニューに追加します。デフォルトの設定を確認・変更するには、任意のフォルダー内で右クリックし、**TortoiseSVN** に移動し、サブメニューから **設定** を選択してください。

<!--
![TortoiseSVN Settings Menu Screen](https://make.wordpress.org/core/files/2013/02/tortoisesvn-settings-context-menu.png)
-->

![TortoiseSVN の設定メニュー画面](https://make.wordpress.org/core/files/2013/02/tortoisesvn-settings-context-menu.png)

<!--
The first screen you see is for the **General Settings**. You can change your language, configure system sounds, and check for updates.
-->

最初に表示されるのは、**一般設定**の画面です。言語の変更、システムサウンドの設定、アップデートの確認ができます。

<!--
![TortoiseSVN General Settings Screen](https://make.wordpress.org/core/files/2013/02/tortoisesvn-settings-1.png)
-->

![TortoiseSVN の一般設定画面](https://make.wordpress.org/core/files/2013/02/tortoisesvn-settings-1.png)

<!--
Select **Context Menu** under **General** in the settings tree on the left side of the window. You can now choose which items will appear on the first-level context menu. The items you will be using often when contributing patches to WordPress will be **Checkout**, **Update**, **Show log**, **Repo-browser**, **Create Patch**, and **Apply Patch**.
-->

ウィンドウの左側にある設定ツリーの**一般**の下にある**コンテキストメニュー**を選択します。これで、最初のレベルのコンテキストメニューに表示される項目を選択できるようになりました。WordPress にパッチを提供する際によく使う項目は、**チェックアウト**、**更新**、**ログの表示**、**レポブラウザ**、**パッチの作成**、**パッチの適用**です。

<!--
![TortoiseSVN Context Menu Settings Screen](https://make.wordpress.org/core/files/2013/02/tortoisesvn-settings-2.png)
-->

![TortoiseSVN のコンテキストメニュー設定画面](https://make.wordpress.org/core/files/2013/02/tortoisesvn-settings-2.png)

<!--
More information about the settings can be found in the [Settings section of the TortoiseSVN documention](http://tortoisesvn.net/docs/release/TortoiseSVN_en/tsvn-dug-settings.html).
-->

設定についての詳細は、[TortoiseSVN ドキュメントの設定セクション](http://tortoisesvn.net/docs/release/TortoiseSVN_en/tsvn-dug-settings.html)に記載されています。

<!--
## Next Steps
-->

## 次のステップ

<!--
*   [Install WordPress locally with Subversion](https://make.wordpress.org/core/handbook/tutorials/installing-wordpress-locally/from-svn/)
*   [Working with Patches](https://make.wordpress.org/core/handbook/tutorials/working-with-patches/)
-->

*   [Subversion で WordPress をローカルにインストールする](https://make.wordpress.org/core/handbook/tutorials/installing-wordpress-locally/from-svn/)
*   [パッチに取り組む](https://make.wordpress.org/core/handbook/tutorials/working-with-patches/)
