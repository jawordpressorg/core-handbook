<!--
# Working with Patches
-->

# パッチに取り組む

<!--
This section of the handbook contains tutorials that will help you learn how to create, apply, and revert patches.
-->

ハンドブックのこのセクションには、パッチの作成、適用、およびそれらを元に戻す方法を学ぶために役立つチュートリアルが含まれています。

<!--
Patches are the only way that a contributor, like you, can submit code to the WordPress project.
-->

パッチは、あなたのような貢献者が WordPress プロジェクトにコードを提出する唯一の方法です。

<!--
Whether you are fixing a bug or contributing to a new feature, a patch is required so the core developers and committers can consider your code for inclusion in the repository.
-->

バグを修正する場合でも、新機能に貢献する場合でも、コア開発者やコミッターがあなたのコードをリポジトリに含めるかどうか検討するために、パッチが必要です。

<!--
For beta testing the latest development version of WordPress, you will need to be able to apply patches that other contributors have created to determine if the patch fixes the issue.
-->

WordPress の最新開発版をベータテストする場合、他の貢献者が作成したパッチを適用して、そのパッチが問題を修正しているかどうかを判断する必要があります。

<!--
## SVN Client or Command Line Interface?
-->

## SVN クライアントかコマンドラインインターフェースか ?

<!--
Many developers prefer to work with Subversion (SVN) using the [command line interface](https://make.wordpress.org/core/glossary/#command-line-interface) (CLI), while others prefer to use a [GUI](http://en.wikipedia.org/wiki/GUI) application. Both are acceptable, and will allow you to create, apply, and revert patches.
-->

多くの開発者は、[コマンドラインインターフェイス](https://make.wordpress.org/core/glossary/#command-line-interface) (CLI) を使って Subversion (SVN) を操作することを好みますが、[GUI](http://en.wikipedia.org/wiki/GUI) アプリケーションを使うことを好む人もいます。どちらも問題なく、パッチの作成、適用、およびそれらを元に戻すことができます。

<!--
For command line users, there are programs such as [Cygwin](http://cygwin.com/) (Windows), [Terminal](http://en.wikipedia.org/wiki/Terminal_(OS_X)) (Mac), and [Bash](http://www.gnu.org/software/bash/) (Mac).
-->

コマンドラインユーザーのために、[Cygwin](http://cygwin.com/) (Windows)、[Terminal](http://en.wikipedia.org/wiki/Terminal_(OS_X)) (Mac)、[Bash](http://www.gnu.org/software/bash/) (Mac) などのプログラムがあります。

<!--
If you prefer to use a GUI application, the recommended SVN clients are [TortoiseSVN](http://tortoisesvn.net/) (Windows, free/open-source), and [Cornerstone](http://www.zennaware.com/cornerstone/) (Mac, purchase).
-->

GUI アプリケーションを使用する場合、推奨される SVN クライアントは [TortoiseSVN](http://tortoisesvn.net/) (Windows、フリー/オープンソース)、[Cornerstone](http://www.zennaware.com/cornerstone/) (Mac、有料) です。

<!--
## Creating and Applying Patches with Grunt
-->

## Grunt を使ったパッチの作成と適用

<!--
If you like to automatically submit the created patch to an existing ticket, there is an easy-to-use [Grunt](https://gruntjs.com/getting-started) command available that can take care of both creating the patch and uploading it. In order to use the command, you need to have [Node.js](https://nodejs.org/) and [Grunt-CLI](https://gruntjs.com/getting-started#installing-the-cli) globally installed, and you need to ensure that the WordPress development dependencies are installed locally, which you can do by running `npm install`.
-->

作成したパッチを既存のチケットに自動的に提出したい場合は、パッチの作成とアップロードの両方を行うことができる使いやすい [Grunt](https://gruntjs.com/getting-started) コマンドがあります。このコマンドを使うには、[Node.js](https://nodejs.org/) と [Grunt-CLI](https://gruntjs.com/getting-started#installing-the-cli) がグローバルにインストールされている必要があります。また、WordPress の開発依存パッケージがローカルにインストールされている必要があります。これは、`npm install` を実行することでインストールできます。

<!--
### Apply a patch from the command line
-->

### コマンドラインからパッチを適用する

<!--
1.  Have a diff or a patch file in your working Directory, then run `grunt patch`. If multiple files are found, you’ll be asked which one to apply.
2.  Enter a ticket number, e.g.
-->

1.  作業ディレクトリに diff かパッチファイルを用意して、`grunt patch` を実行します。複数のファイルが見つかった場合、どれを適用するか尋ねられます。
2.  チケット番号を入力します。

> `grunt patch:15705`

<!--
3.  Enter a ticket url, e.g.
-->

3.  チケットの URL を入力します。

> `grunt patch:https://core.trac.wordpress.org/ticket/15705`

<!--
4.  Enter a patch url, e.g.
-->

4.  パッチの URL を入力します。

> `grunt patch:https://core.trac.wordpress.org/attachment/ticket/11817/13711.diff`

<!--
5.  Enter a github url that points to a changeset such as a Pull Request, e.g.
-->

5.  プルリクエストなどのチェンジセットを指す GitHub の URL を入力します。

> `grunt patch:https://github.com/muhammadfaizanhaidar/develop.wordpress/pull/23`

<!--
### Upload a patch from the command line
-->

### コマンドラインからパッチをアップロードする

<!--
After you’ve made changes to your local WordPress develop repository, you can upload a patch file directly to a Trac ticket. e.g. given the ticket number is 2907,
-->

ローカルの WordPress 開発リポジトリに変更を加えた後、パッチファイルを Trac チケットに直接アップロードできます。たとえばチケット番号が2907であるとすると、

```
grunt upload_patch:2907
```

<!--
You can also store your WordPress.org credentials in environment variables. Please exercise caution when using this option, as it may cause your credentials to be leaked!
-->

WordPress.org の認証情報を環境変数に保存することもできますが、認証情報が漏洩する可能性があるため、このオプションを使用する場合は注意してください !

```
export WPORG_USERNAME=matt
export WPORG_PASSWORD=MyPasswordIsVerySecure12345
grunt uploadPatch:40000
```

<!--
## Creating and Applying Patches with TortoiseSVN
-->

## TortoiseSVN を使ったパッチの作成と適用

<!--
Before starting, you need:
-->

開始する前に、次のものが必要です:

<!--
*   [TortoiseSVN installed on your computer](https://make.wordpress.org/core/handbook/tutorials/installing-a-vcs/)
*   A plain text editor, such as [Notepad++](http://notepad-plus-plus.org/), installed on your computer
-->

*   [コンピューターにインストールされた TortoiseSVN](https://make.wordpress.org/core/handbook/tutorials/installing-a-vcs/)
*   コンピューターにインストールされた [Notepad++](http://notepad-plus-plus.org/) のようなプレーンテキストエディター

<!--
### Creating a Patch with TortoiseSVN
-->

### TortoiseSVN でパッチを作成する

<!--
#### 1\. Editing/Saving a File
-->

#### 1\. ファイルの編集と保存

<!--
Open the folder, and find the file you need to change. Open it in your favorite plain-text editor. **Note:** Do not use a rich-text editor such as Word or OpenOffice to edit the files.
-->

フォルダーを開き、変更したいファイルを見つけてください。好きなプレーンテキストエディターで開いてください。**注意:** ファイルの編集には、Word や OpenOffice のようなリッチテキストエディターは使用しないでください。

<!--
Make the changes necessary, then save the file.
-->

必要な変更を加えて、ファイルを保存します。

<!--
You will notice that the green checkmark has changed to a red exclamation point. That means the file has been changed, and is no longer in sync with the repo version.
-->

緑色のチェックマークが赤色の感嘆符に変わっていることが分かります。これはファイルが変更され、リポジトリのバージョンと同期していないことを意味します。

<!--
![TortoiseSVN Changed File Indicator](https://make.wordpress.org/core/files/2013/02/tortoisesvn-changed-file.png)
-->

![TortoiseSVN 変更ファイルインジケーター](https://make.wordpress.org/core/files/2013/02/tortoisesvn-changed-file.png)

<!--
#### 2\. Creating/Naming a Patch
-->

#### 2\. パッチの作成と命名

<!--
Next you will create the patch file. Right-click in the root directory of your SVN checkout folder, and select **SVN Create Patch**.
-->

次にパッチファイルを作成します。SVN チェックアウトフォルダーのルートディレクトリで右クリックし、**SVN Create Patch** を選択します。

<!--
It is important to create patches from the root directory (the folder containing all of the WordPress files). To do that, either right-click on white space in the folder or move one level up from that folder and right-click on it.
-->

ルートディレクトリ (WordPress のすべてのファイルが含まれているフォルダー) からパッチを作成することが重要です。そのためには、フォルダー内の空白を右クリックするか、そのフォルダーから1つ上の階層に移動して右クリックします。

<!--
![TortoiseSVN Create Patch Context Menu](https://make.wordpress.org/core/files/2013/02/tortoisesvn-create-patch-1.png)
-->

![TortoiseSVN パッチを作成するコンテキストメニュー](https://make.wordpress.org/core/files/2013/02/tortoisesvn-create-patch-1.png)

<!--
A pop-up window will show you the list of changed files. Make sure the file(s) you want to include in the patch are checked, then **click OK**.
-->

ポップアップウィンドウに変更されたファイルのリストが表示されます。パッチに含めたいファイルにチェックが入っていることを確認し、**OK** をクリックします。

<!--
![Check the box for all file(s) that should be included in the patch](https://make.wordpress.org/core/files/2013/02/tortoisesvn-create-patch-2.png)
-->

![パッチに含めたいすべてのファイルにチェックを入れる](https://make.wordpress.org/core/files/2013/02/tortoisesvn-create-patch-2.png)

<!--
You will be prompted to save the file. Create a folder called **patches**, then type in the filename you want to save it as. Use the format **ticket#.diff**.
-->

ファイルを保存するプロンプトが表示されます。**patches** というフォルダーを作成し、保存するファイル名を入力します。形式は **ticket#.diff** にしてください。

<!--
The TortoiseUDiff editor will open and show you the patch file you just created.
-->

TortoiseUDiff エディターが開き、作成したパッチファイルが表示されます。

<!--
![TortoiseUDiff Editor](https://make.wordpress.org/core/files/2013/02/tortoisesvn-22121-patch.png)
-->

![TortoiseUDiff エディター](https://make.wordpress.org/core/files/2013/02/tortoisesvn-22121-patch.png)

<!--
### Applying a Patch with TortoiseSVN
-->

### TortoiseSVN でパッチを適用する

<!--
Got a patch you want to test with your local environment? Follow these steps to test your patch.
-->

ローカル環境でパッチをテストしたいですか ? 以下の手順に従ってパッチをテストしてください。

<!--
#### 1\. Downloading a Patch
-->

#### 1\. パッチのダウンロード

<!--
Part of the troubleshooting/testing process involves downloading and applying patches to your local WordPress trunk install from a Trac ticket that you are involved in.
-->

トラブルシューティングやテストプロセスの一環として、あなたが関わっている Trac チケットからパッチをダウンロードして、ローカルの WordPress trunk インストールに適用することが含まれます。

<!--
To download a patch, **click on the Download icon** next to the patch filename in the **Attachments** section of the ticket (just below the **Description** section), and save it to a folder called **patches**.
-->

パッチをダウンロードするには、チケットの **Attachments** セクション (**Description** セクションのすぐ下) にあるパッチファイル名の横にある **Download アイコンをクリック**し、**patches** というフォルダーに保存してください。

<!--
![Download A Patch From Trac Ticket Screen](https://make.wordpress.org/core/files/2013/04/tortoisesvn-apply-patch-download-file.png)
-->

![Trac チケットからパッチをダウンロードする画面](https://make.wordpress.org/core/files/2013/04/tortoisesvn-apply-patch-download-file.png)

<!--
#### 2\. Applying a Patch with TortoiseSVN
-->

#### 2\. TortoiseSVN でパッチを適用する

<!--
To apply the patch you just downloaded, **right-click in the folder** for your working copy of WordPress, which will bring up a context menu. Click on **SVN Apply Patch**.
-->

ダウンロードしたパッチを適用するために、WordPress の作業コピーの**フォルダー内で右クリック**するとコンテキストメニューが表示されます。**SVN Apply Patch** をクリックしてください。

<!--
![TortoiseSVN Apply Patch Context Menu Screen](https://make.wordpress.org/core/files/2013/03/tortoisesvn-apply-patch-context-menu.png)
-->

![TortoiseSVN パッチを適用するコンテキストメニュー画面](https://make.wordpress.org/core/files/2013/03/tortoisesvn-apply-patch-context-menu.png)

<!--
This will bring up a file open dialog window, allowing you to select the patch file to apply. By default, only **.patch** or **.diff** files are shown, but you can change the file type to **All files** if you don’t see the patch file you are looking for.
-->

ファイルを開くダイアログウィンドウが表示され、適用するパッチファイルを選択できます。デフォルトでは、**.patch** または **.diff** ファイルだけが表示されますが、探しているパッチファイルが見つからない場合は、ファイルタイプを **すべてのファイル** に変更できます。

<!--
![TortoiseSVN Select Local File Screen](https://make.wordpress.org/core/files/2013/03/tortoisesvn-apply-patch-select-local-file.png)
-->

![TortoiseSVN ローカルファイルの選択画面](https://make.wordpress.org/core/files/2013/03/tortoisesvn-apply-patch-select-local-file.png)

<!--
Applying a patch file to your working copy of WordPress should be done at the same folder level as was used to create the patch. If you are in the correct working copy, but picked the wrong folder level, TortoiseSVN will display a notice, suggesting the correct level, and allows you to select that.
-->

WordPress の作業コピーにパッチファイルを適用する場合は、パッチを作成したときと同じフォルダーの階層で行ってください。正しい作業コピーであるにもかかわらず、間違ったフォルダー階層を選択した場合、TortoiseSVN は正しい階層を提案するメッセージを表示し、それを選択できるようにします。

<!--
![TortoiseSVN Wrong Directory Screen](https://make.wordpress.org/core/files/2013/03/tortoisesvn-apply-patch-wrong-directory.png)
-->

![TortoiseSVN 誤ったディレクトリを示す画面](https://make.wordpress.org/core/files/2013/03/tortoisesvn-apply-patch-wrong-directory.png)

<!--
Once you have selected the patch file and correct working copy location, TortoiseMerge will run to merge the changes from the patch file with your working copy. A small window lists the files which have been changed. **Double-click each filename**, review the changes, and save the patched file to your working copy.
-->

パッチファイルと正しい作業コピーの場所を選択すると、TortoiseMerge が実行され、パッチファイルの変更が作業コピーにマージされます。小さなウィンドウに、変更されたファイルが一覧表示されます。**各ファイル名をダブルクリック**し、変更内容を確認し、パッチを適用したファイルを作業コピーに保存してください。

<!--
![TortoiseSVN File Patched Screen](https://make.wordpress.org/core/files/2013/03/tortoisesvn-apply-patch-files-patched.png)
-->

![TortoiseSVN パッチが適用されたファイルを示す画面](https://make.wordpress.org/core/files/2013/03/tortoisesvn-apply-patch-files-patched.png)

<!--
## Creating and Applying Patches with the Command Line
-->

## コマンドラインを使ったパッチの作成と適用

<!--
This article will walk you through creating, applying, and reverting a patch using the command line. Before starting, you’ll need the following:
-->

この記事では、コマンドラインを使ってパッチを作成、適用、およびそれらを元に戻す手順を説明します。はじめる前に、次のものが必要です:

<!--
*   A plain text editor, such as [Notepad++](http://notepad-plus-plus.org/) (Windows) or [TextMate](http://macromates.com/) (Mac), installed on your computer
*   A copy of WordPress trunk, [checked out via SVN](https://make.wordpress.org/core/handbook/tutorials/installing-wordpress-locally/from-svn/)
*   A command line client installed on your computer:
    *   Windows: [Cygwin](http://cygwin.com/)
    *   MAC: [Terminal](http://en.wikipedia.org/wiki/Terminal_(OS_X)) or [Bash](http://www.gnu.org/software/bash/)
    -->

*   [Notepad++](http://notepad-plus-plus.org/) (Windows) や [TextMate](http://macromates.com/) (Mac) などのプレーンテキストエディターがコンピューターにインストールされていること
*   [SVN 経由でチェックアウトした](https://make.wordpress.org/core/handbook/tutorials/installing-wordpress-locally/from-svn/) WordPress trunk のコピー
*   コンピューターにインストールされたコマンドラインクライアント:
    *   Windows: [Cygwin](http://cygwin.com/)
    *   MAC: [Terminal](http://en.wikipedia.org/wiki/Terminal_(OS_X)) または [Bash](http://www.gnu.org/software/bash/)

<!--
### Creating a Patch with the Command Line
-->

### コマンドラインでパッチを作成する

<!--
During beta testing, you may run across a bug that you are able to fix. Before you submit the Trac ticket, however, you should create a patch with the proposed fix so you can attach it to the ticket.
-->

ベータテスト中に、あなたが修正できるバグに遭遇するかもしれません。しかし、Trac チケットを提出する前に、修正案をパッチとして作成し、チケットに添付する必要があります。

<!--
Open the folder where you have WordPress installed via SVN, and find the file you need to change. Open the file in your favorite plain-text editor. Make the changes necessary to fix the bug, then save the file. Do not create patches for minified JS files or RTL CSS files. These are generated automatically from source files. Read more about [this build process](https://make.wordpress.org/core/2013/08/06/a-new-frontier-for-core-development/).
-->

SVN 経由で WordPress がインストールされているフォルダーを開き、変更したいファイルを見つけてください。好きなプレーンテキストエディターでファイルを開いてください。バグを修正するために必要な変更を加えて、ファイルを保存します。圧縮された JS ファイルや RTL CSS ファイルのパッチは作成しないでください。これらはソースファイルから自動的に生成されます。詳細については、[このビルドプロセス](https://make.wordpress.org/core/2013/08/06/a-new-frontier-for-core-development/)を参照してください。

<!--
Next you will create the patch file, which records the differences between your version of the files and those from WordPress trunk. Patches should be created from the root directory of your WordPress SVN install.
-->

次に、パッチファイルを作成します。このパッチファイルは、WordPress trunk のファイルとの差分を記録します。パッチは WordPress SVN インストールのルートディレクトリから作成します。

<!--
To do so, ensure that you are in the root directory created by your SVN checkout (**wordpress-svn**), then run the following command, where `00000` is replaced with the ticket number from Trac:
-->

パッチを作成するには、SVN チェックアウトで作成したルートディレクトリ (**wordpress-svn**) にいることを確認し、次のコマンドを実行します。ここで、`00000` は Trac からのチケット番号に置き換えられます:

```bash
svn diff > 00000.diff
```

<!--
If you also like to automatically submit the created patch to an existing ticket, there is an easy-to-use [Grunt](https://make.wordpress.org/core/handbook/tutorials/working-with-patches/#creating-and-applying-patches-with-grunt) command available that can take care of both creating the patch and uploading it. In order to use the command, you need to have [Node.js](https://nodejs.org/) and Grunt-CLI globally installed, and you need to ensure that the WordPress development dependencies are installed locally, which you can do by running `npm install`.
-->

作成したパッチを既存のチケットに自動的に提出したい場合は、パッチの作成とアップロードの両方を行うことができる使いやすい [Grunt](https://make.wordpress.org/core/handbook/tutorials/working-with-patches/#creating-and-applying-patches-with-grunt) コマンドがあります。このコマンドを使うには、[Node.js](https://nodejs.org/) と Grunt-CLI がグローバルにインストールされている必要があります。また、WordPress の開発依存パッケージがローカルにインストールされている必要があります。これは、`npm install` を実行することでインストールできます。

<!--
The actual command to create and upload a patch works as follows:
-->

パッチを作成してアップロードする実際のコマンドは次のように機能します:

```bash
grunt upload_patch:00000
```

<!--
Make sure to replace `00000` with the ticket number from Trac. During execution of the command, you may be asked for your wordpress.org user name and password.
-->

`00000` は Trac のチケット番号に置き換えてください。コマンドの実行中に、wordpress.org のユーザー名とパスワードの入力を求められる場合があります。

<!--
### Applying a Patch with the Command Line
-->

### コマンドラインでパッチを適用する

<!--
Part of the troubleshooting/testing process involves downloading and applying patches to your local WordPress trunk install from a Trac ticket that you are involved in.
-->

トラブルシューティングやテストプロセスの一環として、あなたが関わっている Trac チケットからパッチをダウンロードして、ローカルの WordPress trunk インストールに適用することが含まれます。

<!--
To download a patch, click on the handy download icon next to the patch’s name in trac:
-->

パッチをダウンロードするには、Trac のパッチ名の横にある便利なダウンロードアイコンをクリックしてください:

<!--
[![Download a Patch from Trac Ticket Screen](https://make.wordpress.org/core/files/2013/07/smpxJogJyp-300x102.png)](https://make.wordpress.org/core/files/2013/07/smpxJogJyp.png)
-->

![Trac チケットからパッチをダウンロードする画面](https://make.wordpress.org/core/files/2013/07/smpxJogJyp.png)

<!--
On a Mac, this will save it to your default downloads folder, from where you can move it to your chosen **wordpress-svn** directory. On a Windows machine, this will prompt you to save it in your chosen location, which should be the aforementioned directory.
-->

Mac では、デフォルトのダウンロードフォルダーに保存され、そこから選択した **wordpress-svn** ディレクトリに移動できます。Windows マシンの場合は、選択した場所 (前述のディレクトリ) に保存するように求められます。

<!--
You can also download a patch via command line. Make sure that you are in the **wordpress-svn** directory, then download the patch into the **patches** folder.
-->

コマンドラインでパッチをダウンロードすることもできます。**wordpress-svn** ディレクトリにいることを確認し、**patches** フォルダーにパッチをダウンロードしてください。

```bash
curl -O https://core.trac.wordpress.org/raw-attachment/ticket/00000/00000.diff
```

<!--
Note: If you download the patch this way, make sure that it is coming from the **raw-attachment** directory on the Trac server. You can get this URL by clicking on the patch in Trac, then grabbing the URL linked to by **Original Format** at the bottom of the page.
-->

注意: この方法でパッチをダウンロードする場合、Trac サーバーの **raw-attachment** ディレクトリからダウンロードされていることを確認してください。この URL は、Trac でパッチをクリックし、ページ下部の **Original Format** でリンクされている URL を取得することで取得できます。

<!--
You will need to apply the patch from the **wordpress-svn** directory, where you have downloaded the patch file. Use the following command to apply the patch:
-->

パッチファイルをダウンロードした **wordpress-svn** ディレクトリからパッチを適用する必要があります。パッチを適用するには、以下のコマンドを使用します:

```
patch -p 0 < 00000.diff
```

<!--
Now, the **wordpress-svn** code has been patched with the file you downloaded, giving you the version of the code that the developer who submitted that patch was working with.
-->

これで、ダウンロードしたパッチファイルが **wordpress-svn** のコードに適用され、そのパッチを提出した開発者が作業していたバージョンのコードになります。

<!--
Note: If the patch fails to apply cleanly, you will need to leave a note on the Trac ticket that the patch needs to be refreshed, and add the **needs-refresh** keyword to the ticket.
-->

注意: もしパッチがきれいに適用できない場合は、Trac チケットにパッチの更新が必要であるというメモを残し、**needs-refresh** キーワードをチケットに追加する必要があります。

<!--
To make this process a little easier for you, there is another [Grunt](https://make.wordpress.org/core/handbook/tutorials/working-with-patches/#creating-and-applying-patches-with-grunt) command available that takes care of both downloading a patch from an existing ticket and applying it. As mentioned before, in order to use it, you need to have both [Node.js](https://nodejs.org/) and Grunt-CLI globally installed, and you also need to have the local dependencies set up, which you can do by using the command `npm install`.
-->

このプロセスを少し簡単にするために、既存のチケットからパッチをダウンロードし、それを適用するもう一つの [Grunt](https://make.wordpress.org/core/handbook/tutorials/working-with-patches/#creating-and-applying-patches-with-grunt) コマンドがあります。前述したように、このコマンドを使うには、[Node.js](https://nodejs.org/) と Grunt-CLI の両方がグローバルにインストールされている必要があります。また、ローカルでの依存関係も設定する必要がありますが、これは `npm install` を実行することでインストールできます。

<!--
You can then use the following command:
-->

その後、以下のコマンドを使用できます:

```bash
grunt patch:00000
```

<!--
Make sure to replace `00000` with the ticket number from Trac. The command will automatically download the patch file from the ticket if there is only a single patch available. Otherwise, you can select which patch to download from a list, using the arrow keys on your keyboard.
-->

必ず `00000` を Trac のチケット番号に置き換えてください。利用可能なパッチが一つしかない場合、コマンドは自動的にチケットからパッチファイルをダウンロードします。そうでなければ、キーボードの矢印キーを使って、ダウンロードするパッチをリストから選択できます。

<!--
### Reverting a Patch with the Command Line
-->

### コマンドラインでパッチを元に戻す

<!--
When you have finished testing, it is best to revert your SVN install back to the latest version of trunk, removing all applied patches and any changes you have made. You will use the following command to revert all patches/changes:
-->

テストが終了したら、インストールした SVN を最新バージョンの trunk に戻し、適用したパッチや変更点をすべて削除することをおすすめします。すべてのパッチや変更を戻すには、以下のコマンドを使います:

```bash
svn revert -R *
```

<!--
## Download a GitHub pull request
-->

## GitHub プルリクエストのダウンロード

<!--
With [hub](https://hub.github.com/) is very easy to download a pull request from a WordPress fork on a Git repo (like on GitHub). For the purpose of this section you need to install this tool on your system.
-->

[hub](https://hub.github.com/) を使用すると、(GitHub などの) Git リポジトリ上の WordPress フォークからプルリクエストをダウンロードすることがとても簡単になります。このセクションでは、このツールをシステムにインストールする必要があります。

<!--
Now you have a super version of Git that include the Hub version so inside the \``public_html` on VVV or your WP trunk folder you can execute this command (as example):
-->

これで、hub のバージョンを含むスーパーバージョンの Git が手に入ったので、VVV または WP の trunk フォルダーの `public_html` 内で次のコマンドを実行できます (例):

`git checkout https://github.com/WordPress/wordpress-develop/pull/195`

<!--
This command will create automatically for you a new branch with the content of this pull request, with the ability to update that branch with the code over there.
-->

このコマンドは、そこにあるコードでそのブランチを更新する機能を備えており、このプルリクエストの内容を含む新しいブランチを自動的に作成します。

<!--
Otherwise you can download the patch or diff version of a pull request appending to the pull request url `.patch` or `.diff` like:
-->

それ以外の場合は、次のようにプルリクエストの URL に `.patch` や `.diff` を追加することで、プルリクエストのパッチ版や diff 版をダウンロードできます:

git checkout https://github.com/WordPress/wordpress-develop/pull/195`

*   [https://patch-diff.githubusercontent.com/raw/WordPress/wordpress-develop/pull/195.diff](https://patch-diff.githubusercontent.com/raw/WordPress/wordpress-develop/pull/195.diff)
*   [https://patch-diff.githubusercontent.com/raw/WordPress/wordpress-develop/pull/195.patch](https://patch-diff.githubusercontent.com/raw/WordPress/wordpress-develop/pull/195.patch)

<!--
## Next Steps
-->

## 次のステップ

<!--
*   [Submitting a Patch](https://make.wordpress.org/core/handbook/tutorials/trac/submitting-a-patch/)
-->

*   [パッチの提出](https://make.wordpress.org/core/handbook/tutorials/trac/submitting-a-patch/)
