<!--
# Submitting a Patch
-->

# パッチの提出

<!--
## Overview
-->

## 概要

<!--
Once you’ve edited the file and tested it, you need to create a patch and upload it to the corresponding Trac ticket so other people can see and test the changes. You can create a *patch* a number of ways.
-->

ファイルを編集してテストしたら、パッチを作成して対応する Trac チケットにアップロードし、他の人が変更点を見たりテストしたりできるようにする必要があります。「パッチ」はさまざまな方法で作成できます。

<!--
When using an IDE or a Subversion client a patch can be created directly by the application. The patch should be created from the root directory (the folder that contains the `/src` directory, the `wp-config-sample.php` file, etc.).
-->

IDE や Subversion クライアントを使用している場合、パッチはアプリケーションから直接作成できます。パッチはルートディレクトリ (`/src` ディレクトリ、`wp-config-sample.php` ファイルなどを含むフォルダー) から作成する必要があります。

### Windows

<<<<<<< HEAD
**If you are on Windows,** consider using [Tortoise SVN](http://tortoisesvn.net/). You can [read our tutorial on creating a patch with Tortoise SVN](https://make.wordpress.org/core/handbook/tutorials/working-with-patches/#creating-a-patch-with-tortoisesvn).
=======
<!--
**If you are on Windows,** consider using [Tortoise SVN](http://tortoisesvn.net/). You can [read our tutorial on creating a patch with Tortoise SVN](https://make.wordpress.org/core/handbook/tutorials/working-with-patches/#creating-a-patch-with-tortoisesvn).
-->
>>>>>>> main

**Windows の場合、** [Tortoise SVN](http://tortoisesvn.net/) の使用を検討してください。[Tortoise SVN でパッチを作成するためのチュートリアルを読む](https://ja.wordpress.org/team/handbook/core/tutorials/working-with-patches/#creating-a-patch-with-tortoisesvn)ことができます。

<!--
### Mac/Linux Command Line
-->

### Mac/Linux コマンドライン

<!--
From [Mark Jaquith’s Tutorial](http://markjaquith.wordpress.com/2005/11/02/my-wordpress-toolbox/)
-->

[Mark Jaquith のチュートリアル](http://markjaquith.wordpress.com/2005/11/02/my-wordpress-toolbox/)より

<!--
Make a patch, for filename.php:
-->

filename.php のパッチを作成する:

`$ svn diff filename.php > filename.diff`

<!--
Make a patch for all files modified in the checkout:
-->

チェックアウトで変更されたすべてのファイルのパッチを作成する:

`$ svn diff > big_patch.diff`

<!--
Apply a patch from someone else:
-->

誰かからもらったパッチを適用する:

`$ patch -p0 < patch.diff`

<!--
There are some GUI options for the Mac, as well — you just need it to create patch files (Versions cannot, for example).
-->

Mac 用の GUI オプションもあります。パッチファイルを作成するのに必要なだけです (たとえば、Versions ではできません)。

<!--
Also: [creating SVN patches using Git](http://scribu.net/wordpress/svn-patches-from-git.html), from Cristi Burca.
-->

もしくは、Cristi Burca の [Git を使用して SVN パッチを作成する](http://scribu.net/wordpress/svn-patches-from-git.html)もあります。

<!--
## Adding your GitHub fork to your WP trunk copy
-->

## GitHub のフォークを WP trunk のコピーに追加する

<!--
First of all you need your own WordPress fork somewhere, usually on GitHub (also because there is the [mirror](http://github.com/wordpress/wordpress-develop)). After creating a fork, a branch (is important to not work on the master/trunk branch to avoid conflicts) you need to add this new remote to your git instance.
-->

まず最初に、どこかに自分の WordPress フォークが必要です。通常は GitHub にあります ([ミラー](http://github.com/wordpress/wordpress-develop)があるためです)。フォークとブランチを作成したら (競合を避けるために master/trunk ブランチでは作業しないことが重要です)、この新しいリモートをあなたの git インスタンスに追加する必要があります。

`git remote add fork git@github.com:WordPress/wordpress-develop.git`

<!--
Change in this command with the repo url or the git url as you prefer
-->

必要に応じて、リポジトリの URL または git の URL を使用してこのコマンドを変更します。

<!--
Now it is time to a command to align your local git instance `git fetch --all`
-->

次に、ローカルの git インスタンスと連携させるコマンド `git fetch --all` を実行します。

<!--
Now you are able to switch to a master from your fork with this command as example `git checkout fork/44722` or create a new branch like `git checkout -b 44722`, this command require to switch to the fork instead of the official version and you can achieve it with `git checkout fork master`.
-->

`git checkout fork/44722` のようなコマンドでフォークからマスターに切り替えたり、`git checkout -b 44722` のように新しいブランチを作成できます。このコマンドは、正式版ではなくフォーク版に切り替えることを要求しており、`git checkout fork master` で実現可能です。

<!--
Now you can use as usual git and create all the code changes that you need, commit and so on. If you open now the [GitHub mirror](https://github.com/wordpress/wordpress-develop) (and you associated your WP profile to GitHub) you get a on the GH page a button to create a new pull request because it detected this change.
-->

これで、いつものように git を使って、必要なコードの変更をすべて作成し、コミットできます。[GitHub ミラー](https://github.com/wordpress/wordpress-develop)を開くと (WP プロフィールを GitHub に関連付けると)、GH ページに新しいプルリクエストを作成するボタンが表示され、この変更が検出されます。

<!--
The next step is to add a name to the pull request that need to include the ticket number as explained [here](https://make.wordpress.org/core/handbook/contribute/git/github-pull-requests-for-code-review/). For other information about GitHub integration check this documentation page.
-->

次のステップでは、[こちら](https://ja.wordpress.org/team/handbook/core/contribute/git/github-pull-requests-for-code-review/)で説明したように、プルリクエストにチケット番号を含めた名前を付けます。GitHub との統合に関するその他の情報は、このドキュメントページをご覧ください。
