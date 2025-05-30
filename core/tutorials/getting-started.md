<!--
# Getting Started
-->

# はじめに

<!--
This page gives you a clear guide on what you need to do in order to get started with contributing to WordPress core. Below you will find a list of items that need to be taken care of, with links leading to more specific tutorials on the individual steps.
-->

このページでは、WordPress コアへの貢献をはじめるために何が必要かを分かりやすく説明します。以下に、注意が必要な項目のリストと、個々のステップに関するより具体的なチュートリアルへのリンクがあります。

<!--
Everything described here is recommended to efficiently contribute to WordPress core. Where possible, different choices are highlighted to leave enough flexibility to account for your typical workflows. If you are planning to join a contributor day in the WordPress core team, following these steps in advance will ensure you maximize your outcome of that day since often-times several of them can be time-consuming during contributor days, particularly due to slow internet connections.
-->

ここで説明する内容はすべて、WordPress コアに効率的に貢献するために推奨されます。可能な場合は、一般的なワークフローに対応できる十分な柔軟性を残すために、さまざまな選択肢が強調表示されます。WordPress コアチームのコントリビューターデイに参加する予定がある場合は、事前に次の手順に従うことで、その日の成果を最大限に高めることができます。これは、コントリビューターデイの間は特にインターネット接続が遅いために、そのうちのいくつかは時間がかかることがよくあるためです。

<!--
## Joining communication channels
-->

## コミュニケーションチャンネルに参加する

<!--
Communication in WordPress commonly happens either asynchronously on Trac, which is the issue tracker used by the project, or in live chat on Slack, which is a popular instant messaging service used by many organizations. Here is how you get access to these two tools:
-->

WordPress でのコミュニケーションは、プロジェクトで使用されている課題追跡ツールである Trac 上で非同期に行われるか、多くの組織で使用されている一般的なインスタントメッセージングサービスである Slack 上のライブチャットで行われることが一般的です。この2つのツールへアクセスする方法は次のとおりです:

<!--
1.  [Sign up for a wordpress.org account](https://login.wordpress.org/register) and complete the instructions. You may optionally sign up at [gravatar.com](https://gravatar.com/) with the same email address if you’d like to have a profile picture (recommended). This account can be used for all contributing activities.
2.  In order to join the international WordPress Slack team and thus be able to participate in core team meetings and other discussions, you need to receive an invite. Visit the [WordPress + Slack page](https://make.wordpress.org/chat/) while being logged in with your wordpress.org account, and click the link to receive the invite per email.
3.  Via the email, log in to the [Slack team](https://wordpress.slack.com). For email address, use `{username}@chat.wordpress.org` where `{username}` is your user name you picked for wordpress.org. If possible, pick the same username for Slack.
-->

1.  [wordpress.org アカウントにサインアップ](https://login.wordpress.org/register)し、手順を完了します。プロフィール画像を用意したい場合は、同じメールアドレスで [gravatar.com](https://gravatar.com/) にサインアップできます (推奨)。このアカウントは、すべての貢献活動に使用できます。
2.  国際的な WordPress Slack チームに参加し、コアチームのミーティングやその他のディスカッションに参加するには、招待を受ける必要があります。wordpress.org アカウントでログインした状態で [WordPress + Slack ページ](https://make.wordpress.org/chat/)にアクセスし、リンクをクリックして招待メールを受け取ります。
3.  そのメールから [Slack チーム](https://wordpress.slack.com)にログインします。メールアドレスには、`{username}@chat.wordpress.org` を使用します。`{username}` は wordpress.org 用に選択したユーザー名です。可能であれば、Slack と同じユーザー名を選択してください。

<!--
## Setting up your development environment
-->

## 開発環境のセットアップ

<!--
In order to contribute to WordPress core, you need a local development environment and a checkout of WordPress trunk, which is the development version of WordPress. Be aware that this is *not* the same as the latest downloadable WordPress release.
-->

WordPress コアに貢献するには、ローカルの開発環境と WordPress 開発バージョンである trunk のチェックアウトが必要です。これはダウンロード可能な WordPress の最新リリースとは**異なる**ことに注意してください。

<!--
### Setting up a local server
-->

### ローカルサーバーのセットアップ

<!--
Check out [options to download and install a local development environment](https://make.wordpress.org/core/handbook/contribute/#local-development-overview) on your machine.
-->

お使いのマシンに[ローカル開発環境をダウンロードしてインストールするためのオプション](https://ja.wordpress.org/team/handbook/core/contribute/#local-development-overview)を確認してください。

<!--
### Setting up a version control system
-->

### バージョン管理システムのセットアップ

<!--
Install a version control system to use for WordPress core. Here you have two options:
-->

<!--
*   WordPress core by default uses Subversion (or SVN) for version control, which works relatively similar to Git, but is a little older. While most people prefer working with Git, the SVN commands you typically use when developing for WordPress core are trivial and almost the same as their Git counterparts. If you are using a [local environment like VVV](https://make.wordpress.org/core/handbook/contribute/#local-development-overview) your environment may already have SVN pre-installed. If you are using another environment or prefer to also use SVN directly on your computer, there is a [handbook tutorial guiding you through the process](https://make.wordpress.org/core/handbook/tutorials/installing-a-vcs/).
*   Alternatively, you can install Git from the [Git project website](https://git-scm.com/). On many environments, for example VVV, you will already find it pre-installed. If you prefer using a visual UI in addition, feel free to use a client app such as [Sourcetree](https://www.atlassian.com/software/sourcetree), or [GitHub Desktop](https://desktop.github.com/) (which works particularly well when used together with GitHub).
-->

*   WordPress コアはデフォルトでバージョン管理に Subversion (または SVN) を使用しています。これは Git と比較的似たしくみですが、少し古いものです。多くの人は Git での作業を好みますが、WordPress コアの開発時に一般的に使用する SVN コマンドは簡単で、Git のコマンドとほぼ同じです。[VVV のようなローカル環境](https://ja.wordpress.org/team/handbook/core/contribute/#local-development-overview) を使用している場合は、すでに SVN が環境にプリインストールされている可能性があります。別の環境を使用している場合、またはコンピューター上で直接 SVN を使用したい場合は、[手順を説明したハンドブックチュートリアル](https://ja.wordpress.org/team/handbook/core/tutorials/installing-a-vcs/) があります。
*   あるいは、[Git プロジェクトのWeb サイト](https://git-scm.com/)から Git をインストールできます。VVV などの多くの環境では、すでにプリインストールされています。さらにビジュアルな UI を使いたい場合は、[Sourcetree](https://www.atlassian.com/software/sourcetree) や [GitHub Desktop](https://desktop.github.com/) (GitHub と一緒に使うと特に効果的です) のようなクライアントアプリを自由に使ってください。

<!--
### Setting up the WordPress development repository
-->

### WordPress 開発リポジトリのセットアップ

<!--
Set up the development version of WordPress in your development environment. How you proceed depends on whether you decided to use SVN or Git for version control in the second step:
-->

開発環境に WordPress の開発バージョンをセットアップします。手順は、2番目のステップでバージョン管理に SVN と Git のどちらを使用するかによって異なります。

<!--
*   If you are [cloning from GitHub](https://github.com/WordPress/wordpress-develop) and using the built-in [Docker](https://www.docker.com/) environment, you can run `npm run env:start` and `npm run env:install` from your WordPress Develop repository checkout to start a local server on `localhost`.
*   If you are using SVN and VVV, everything is already setup after the initial booting process. You can access your development version of WordPress under [http://src.wordpress-develop.test](http://src.wordpress-develop.test) with your VVV running. If you’re using SVN on another environment than VVV, please [follow the instructions on how to install WordPress from SVN](https://make.wordpress.org/core/handbook/tutorials/installing-wordpress-locally/from-svn/).
*   If you’re using Git and VVV, please [follow the optional instructions on how to change the included WordPress development repository to use Git instead of the default SVN](https://make.wordpress.org/core/handbook/tutorials/installing-a-local-server/installing-vvv/#5-create-github-repo-optional). If you’re using Git on another environment than VVV, create a GitHub fork of the [WordPress/wordpress-develop](https://github.com/WordPress/wordpress-develop) repository. Afterwards, you can proceed with the above instructions, just skip the first three points and instead of using develop.git.wordpress.org as upstream repository, use the GitHub version.
-->

*   [GitHub からクローン](https://github.com/WordPress/wordpress-develop)し、組込みの [Docker](https://www.docker.com/) 環境を使用している場合は、WordPress Develop リポジトリのチェックアウトから `npm run env:start` と `npm run env:install` を実行して、`localhost` でローカル サーバーを起動できます。
*   SVN および VVV を使用している場合は、最初の起動プロセスの後にすべてがすでにセットアップされています。VVV を実行している状態で、[http://src.wordpress-develop.test](http://src.wordpress-develop.test) にある WordPress の開発バージョンにアクセスできます。VVV とは別の環境で SVN を使用している場合は、[SVN から WordPress をインストールする方法の手順に従ってください](https://ja.wordpress.org/team/handbook/core/tutorials/installing-wordpress-locally/from-svn/)。
*   Git と VVV を使用している場合は、[デフォルトの SVN の代わりに Git を使用するために同梱の WordPress 開発リポジトリを変更する方法に関するオプションの手順に従ってください](https://ja.wordpress.org/team/handbook/core/tutorials/installing-a-local-server/installing-vvv/#6-create-a-github-repo-optional)。VVV 以外の環境で Git を使用している場合は、[WordPress/wordpress-develop](https://github.com/WordPress/wordpress-develop) リポジトリの GitHub フォークを作成します。その後は上記の手順で進めますが、最初の3つのポイントをスキップして、develop.git.wordpress.org をアップストリームリポジトリとして使用する代わりに、GitHub バージョンを使用します。

<!--
And with that, you’re ready to get started with contributing!
-->

これで、貢献する準備が整いました !

<!--
## What is next?
-->

## 次に何をしますか ?

<!-- If you plan to attend a contributor day, the above prerequisites will give you a jumpstart so that you can immediately focus on learning how to actually contribute. If you are not visiting this page because you are going to attend a contributor day or if you are already interested in diving in deeper, the best way to proceed is to [learn more about why contributing to core is important and which processes are involved](https://make.wordpress.org/core/handbook/contribute/). In case you immediately prefer working with tickets instead, [this introduction to Trac will help you get familiar](https://make.wordpress.org/core/handbook/tutorials/trac/new-user-quick-start/). -->

コントリビューターデイに参加する予定がある場合は、上記の前提条件を満たしておけば、すぐに実際に貢献する方法を学ぶことに集中できます。コントリビューターデイに参加するためにこのページを訪れていない場合、あるいはすでに深く掘り下げることに興味がある場合は、[コアへの貢献が重要である理由と、どのプロセスが関係しているかについて詳しく学ぶ](https://ja.wordpress.org/team/handbook/core/contribute/)ことが最善の方法です。もし、すぐにチケットで作業することを望むのであれば、[Trac に慣れるためのこの Trac の概要が役に立ちます](https://ja.wordpress.org/team/handbook/core/tutorials/trac/new-user-quick-start/)。
