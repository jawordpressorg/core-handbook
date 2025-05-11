<!--
# Getting Started at a Contributor Day
-->

# コントリビューターデイの開催

<!--
*This guide is intended to help you get started at a contributor day. It includes a schematic outline of what the group does and how to quickly get started. If you need any help, talk to the contributor day organizer, or ask your question in the [#core](https://make.wordpress.org/core/tag/core/) channel in [Slack](https://chat.wordpress.org/).*
-->

**このガイドは、コントリビューターデイを開催するためのものです。このガイドには、グループが何をするのか、どのようにすればすぐに始められるのかの概要が含まれています。サポートが必要な場合は、コントリビューターデイのオーガナイザーに相談するか、[Slack](https://chat.wordpress.org/) の [#core](https://make.wordpress.org/core/tag/core/) チャンネルで質問してください。**

<!--
*This is a work in progress so don’t be afraid to amend the document or leave comments, particularly if you’re at a contributor day and find that we’ve missed something.*
-->

**これは進行中の作業であるため、特にあなたがコントリビューターデイに参加していて、何かを見落としていることに気づいた場合は、遠慮なくドキュメントを修正したり、コメントを残してください。**

<!--
**Regular Meeting Time:** Wednesdays at 21:00 UTC
**New Contributor Meetings:** 2nd and 4th Wednesdays at 19:00 UTC**
Where:** [#core](https://make.wordpress.org/core/tag/core/) channel on [Slack](https://chat.wordpress.org/)
-->

-   **レギュラーミーティングの時間:** 水曜日 21:00 UTC
-   **新しい貢献者のミーティング:** 第2、第4水曜日 19:00 UTC
-   **場所:** [Slack](https://chat.wordpress.org/) の [#core](https://make.wordpress.org/core/tag/core/) チャンネル

<!--
## Group responsibilities
-->

## グループの責任

<!--
The responsibilities of the core group are:
-->

コアグループの責任は次のとおりです:

<!--
*   To maintain the code and develop it for the future
*   Develop new features for WordPress
*   Maintain and improve design and UX
*   Design, develop, and maintain default themes
*   Maintain the utilities used to develop core
*   Maintain the bundled packages of default plugins
*   Maintain the bundled libraries available in core
*   Maintaining the bug tracker
-->

*   コードのメンテナンスと、将来に向けての開発
*   WordPress の新機能の開発
*   デザインと UX の維持と改善
*   デフォルトのテーマの設計、開発、保守
*   コアの開発に使用されるユーティリティのメンテナンス
*   デフォルトのプラグインのバンドルパッケージのメンテナンス
*   コアで利用可能なバンドルライブラリのメンテナンス
*   バグトラッカーのメンテナンス

<!--
## Common Tasks
-->

## 共通のタスク

<!--
As a member of the core group, some common tasks that you’ll carry out are:
-->

コアグループのメンバーとして実行する一般的なタスクは次のとおりです:

<!--
*   Testing patches and fixing bugs
*   Handling stability and security issues
*   Code new features
*   Work on the user interface
*   User testing for new features
*   Writing unit tests to keep WordPress stable
*   Bug gardening
*   Review patches for [Coding Standards](https://make.wordpress.org/core/handbook/coding-standards/)
*   Review patches for accessibility and privacy concerns
-->

*   パッチのテストとバグの修正
*   安定性とセキュリティに関する問題の処理
*   新しい機能のコードを書く
*   ユーザーインターフェイスに取り組む
*   新機能のユーザーテスト
*   WordPress の安定性を維持するためのユニットテストの作成
*   バグガーデニング
*   [コーディング規約](https://ja.wordpress.org/team/handbook/core/coding-standards/)のパッチを確認する
*   アクセシビリティとプライバシーの問題についてパッチをレビューする

<!--
## Prior Knowledge
-->

## 予備知識

<!--
Prior knowledge that you’ll find helpful for working on core is:
-->

コアの作業に役立つ予備知識は次のとおりです:

<!--
*   Grasp of whatever coding language you want to help out with, e.g. CSS, PHP, Javascript or React
*   Familiarity with WordPress is beneficial but you don’t need a deep understanding of core to get started
-->

*   CSS、PHP、JavaScript、React など、手伝いたいコーディング言語を理解していること
*   WordPress に精通していると役に立ちますが、始めるためにコアについて深く理解する必要はありません

<!--
## Tools
-->

## ツール

<!--
*   A version control system: either [SVN](http://sourceforge.net/projects/win32svn/) or [Git](http://git-scm.com/)
*   a [local development environment](https://make.wordpress.org/core/handbook/contribute/#local-development-overview)
*   for unit testing, [PHPUnit](http://phpunit.de/)
*   [Grunt](http://gruntjs.com/) for compiling assets, building release packages, and JavaScript and PHP testing
*   [QUnit](http://qunitjs.com/) for Javascript testing
*   [WPCS](https://github.com/WordPress/WordPress-Coding-Standards) rules for [PHP\_CodeSniffer](https://github.com/squizlabs/PHP_CodeSniffer)
-->

*   バージョン管理システム: [SVN](http://sourceforge.net/projects/win32svn/) または [Git](http://git-scm.com/)
*   [ローカル開発環境](https://ja.wordpress.org/team/handbook/core/contribute/#local-development-overview)
*   ユニットテストの場合、[PHPUnit](http://phpunit.de/)
*   アセットのコンパイル、リリースパッケージのビルド、JavaScript と PHP のテストのための [Grunt](http://gruntjs.com/)
*  Javascript テストのための [QUnit](http://qunitjs.com/)
*   [PHP\_CodeSniffer](https://github.com/squizlabs/PHP_CodeSniffer) の [WPCS](https://github.com/WordPress/WordPress-Coding-Standards) ルール

<!--
## Essential Reading
-->

## 必読書

<!--
*   Sections of the [Core Contributor Handbook](https://make.wordpress.org/core/handbook/) relevant to what you’re working on
*   If you’re writing code, the [WordPress Coding Standards](https://make.wordpress.org/core/handbook/coding-standards/)
-->

*   [コアコントリビューターハンドブック](https://ja.wordpress.org/team/handbook/core/)の、取り組んでいる内容に関連するセクション
*   コードを書いている場合は、[WordPress コーディング規約](https://ja.wordpress.org/team/handbook/core/coding-standards/)

<!--
## First Steps
-->

## 最初のステップ

<!--
The first step is to get set up with a local environment:
-->

最初のステップは、ローカル環境をセットアップすることです。

<!--
1\. Install SVN: [Installing a VCS](https://make.wordpress.org/core/handbook/tutorials/installing-a-vcs/)  
2\. Install a local server: [Mac](https://make.wordpress.org/core/handbook/tutorials/installing-a-local-server/mamp/) | [Windows](https://make.wordpress.org/core/handbook/installing-a-local-server/installing-xampp/) | [Windows](https://make.wordpress.org/core/handbook/tutorials/installing-a-local-server/wampserver/) (alternative)  
3\. [Check out the WordPress codebase using SVN](https://make.wordpress.org/core/handbook/tutorials/installing-wordpress-locally/from-svn/)
-->

1. SVN のインストール: [バージョン管理システムのインストール](https://ja.wordpress.org/team/handbook/core/tutorials/installing-a-vcs/)
2. ローカルサーバーのインストール: [Mac](https://ja.wordpress.org/team/handbook/core/tutorials/installing-a-local-server/mamp/) | [Windows](https://ja.wordpress.org/team/handbook/core/installing-a-local-server/installing-xampp/) | [Windows](https://ja.wordpress.org/team/handbook/core/installing-a-local-server/wampserver/) (代替)
3. [SVN を使用して WordPress コードベースを確認する](https://ja.wordpress.org/team/handbook/core/tutorials/installing-wordpress-locally/from-svn/)

<!--
After that:
-->

その後に:

<!--
*   If you find an issue with WordPress you can [Open a ticket on Trac](https://make.wordpress.org/core/handbook/working-with-trac/opening-a-ticket/)
*   [Fix a bug](https://make.wordpress.org/core/handbook/fixing-bugs/)
*   [Create and apply a patch](https://make.wordpress.org/core/handbook/tutorials/working-with-patches/)
-->

*   WordPress で問題が見つかった場合は、[Trac でチケットを開く](https://ja.wordpress.org/team/handbook/core/working-with-trac/opening-a-ticket/)ことができます。
*   [バグの修正](https://ja.wordpress.org/team/handbook/core/fixing-bugs/)
*   [パッチを作成して適用する](https://ja.wordpress.org/team/handbook/core/tutorials/working-with-patches/)


<!--
There are other ways that you can help out:
-->

他にも、次のような方法で手助けできます:

<!--
*   [Bug gardening](https://make.wordpress.org/core/handbook/bug-gardening/)
*   If a beta or release candidate is available try out some [Alpha or Beta testing](https://make.wordpress.org/core/handbook/testing/beta/)
*   [Writing unit tests](https://make.wordpress.org/core/handbook/automated-testing/)
*   If you want to help out with a UI\-centric feature, check out the [features as plugins information](https://make.wordpress.org/core/features-as-plugins/)
*   If you want to focus on a specific Component, check out the [WordPress Core Components](https://make.wordpress.org/core/components/) listing.
-->

*   [バグガーデニング](https://ja.wordpress.org/team/handbook/core/bug-gardening/)
*   ベータ版またはリリース候補が利用可能な場合は、[アルファ版またはベータ版のテスト](https://ja.wordpress.org/team/handbook/core/testing/beta/)を試してみてください
*   [ユニットテストを書く](https://ja.wordpress.org/team/handbook/core/automated-testing/)
*   UI 中心の機能を手助けしたい場合は、[プラグインとしての機能に関する情報](https://make.wordpress.org/core/features-as-plugins/)を確認してください
*   特定のコンポーネントにフォーカスしたい場合は、[WordPress コアコンポーネント](https://make.wordpress.org/core/components/)のリストを確認してください。

<!--
## Tasks
-->

## タスク

<!--
Some easy tasks for a first time contributor to get started at a contributor day are:
-->

初めての貢献者が、コントリビューターデイで簡単に始められるタスクがいくつかあります:

<!--
*   Check the [good first bug tag](https://core.trac.wordpress.org/query?status=!closed&keywords=~good-first-bug) for easy wins
*   Update the [Inline Docs](https://developer.wordpress.org/coding-standards/inline-documentation-standards/)
*   Work on the user interface, check out the [UI focus](https://core.trac.wordpress.org/focus/ui)
*   Provide [Developer feedback](https://core.trac.wordpress.org/tickets/dev-feedback)
*   Provide [Design feedback](https://core.trac.wordpress.org/tickets/ux-feedback)
*   Provide [Copy feedback](https://core.trac.wordpress.org/query?status=accepted&status=assigned&status=new&status=reopened&status=reviewing&keywords=~needs-copy-review&col=id&col=summary&col=status&col=owner&col=type&col=priority&col=milestone&order=priority)
*   Provide [Privacy feedback](https://core.trac.wordpress.org/query?status=accepted&status=assigned&status=new&status=reopened&status=reviewing&keywords=~needs-privacy-review&col=id&col=summary&col=status&col=owner&col=type&col=priority&col=milestone&order=priority)
*   [Refresh an existing patch](https://core.trac.wordpress.org/query?status=accepted&status=assigned&status=new&status=reopened&status=reviewing&keywords=~needs-refresh&col=id&col=summary&col=status&col=owner&col=type&col=priority&col=milestone&order=priority) that doesn’t apply or needs an update.
*   Try your hand at [bug gardening](https://make.wordpress.org/core/handbook/bug-gardening/) (Helen has a [good post to help you get started](http://helen.wordpress.com/2013/08/09/scared-of-wordpress-core-trac-but-want-to-give-it-a-shot-try-trac-gardening/))
-->

*   [good first bug タグ](https://core.trac.wordpress.org/query?status=!closed&keywords=~good-first-bug)をチェックする
*   [インラインドキュメント](https://ja.wordpress.org/team/handbook/coding-standards/inline-documentation-standards/)を更新する
*   ユーザーインターフェイスに取り組み、[UI フォーカス](https://core.trac.wordpress.org/focus/ui)を確認する
*   [開発者フィードバック](https://core.trac.wordpress.org/tickets/dev-feedback)を提供する
*   [デザインに関するフィードバック](https://core.trac.wordpress.org/tickets/ux-feedback)を提供する
*   [コピーに関するフィードバック](https://core.trac.wordpress.org/query?status=accepted&status=assigned&status=new&status=reopened&status=reviewing&keywords=~needs-copy-review&col=id&col=summary&col=status&col=owner&col=type&col=priority&col=milestone&order=priority)を提供する
*   [プライバシーに関するフィードバック](https://core.trac.wordpress.org/query?status=accepted&status=assigned&status=new&status=reopened&status=reviewing&keywords=~needs-privacy-review&col=id&col=summary&col=status&col=owner&col=type&col=priority&col=milestone&order=priority)を提供する
*   適用されていない、またはアップデートが必要な[既存のパッチを更新する](https://core.trac.wordpress.org/query?status=accepted&status=assigned&status=new&status=reopened&status=reviewing&keywords=~needs-refresh&col=id&col=summary&col=status&col=owner&col=type&col=priority&col=milestone&order=priority)
*   [バグガーデニング](https://ja.wordpress.org/team/handbook/core/bug-gardening/)に挑戦してみる (Helen が、[始めるときに役立つ良い記事](http://helen.wordpress.com/2013/08/09/scared-of-wordpress-core-trac-but-want-to-give-it-a-shot-try-trac-gardening/)を投稿しています)

<!--
## **Gutenberg Contributions**
-->

## Gutenberg への貢献

<!--
### **Prerequisites**
-->

### 前提条件

<!--
*   A local dev environment running WordPress (we suggest [VVV](https://varyingvagrantvagrants.org/docs/en-US/installation/software-requirements/))
*   Latest [npm](https://nodejs.org/en/download/package-manager/) version.
-->

* WordPress が動作するローカル開発環境 ([VVV](https://varyingvagrantvagrants.org/docs/en-US/installation/software-requirements/) を推奨します)
* 最新の [npm](https://nodejs.org/en/download/package-manager/) バージョン。

<!--
If you are unsure if you are on the latest npm version, run the following command:
-->

npm のバージョンが最新かどうかわからない場合は、以下のコマンドを実行してください:

```bash
 npm install npm@latest -g
```

*    Docker – https://docs.docker.com/install/

<!--
A handy guide to setting up your local environment can be found in [**Contributing.md**](https://github.com/WordPress/gutenberg/blob/trunk/CONTRIBUTING.md) in the Gutenberg github repository. There you will find commands to help get your local environment up and running.  
-->

Gutenberg の GitHub リポジトリにある [**Contributing.md**](https://github.com/WordPress/gutenberg/blob/trunk/CONTRIBUTING.md) に、ローカル環境を構築するための便利なガイドがあります。そこには、ローカル環境の起動と実行に役立つコマンドが記載されています。

<!--
Largely, the setup process can be finished end to end by running the following command from the Gutenberg directory (Powershell works well if you are on Windows.):
-->

通常セットアッププロセスは、Gutenberg ディレクトリで次のコマンドを実行することで完了できます (Windows を使用している場合は、Powershell が有効です)。

```bash
./bin/setup-local-env.sh
```

<!--
The script will go step by step through the process of validating prerequisites are met. If there is something missing, the script will report what needs to be done to complete the setup. Re running the script a few times after making the suggested changes will complete setup.
-->

スクリプトは、前提条件が満たされていることを確認するプロセスを段階的に実行します。何かが不足している場合、スクリプトはセットアップを完了するために何をする必要があるかを報告します。提案された変更を行った後、スクリプトを数回再実行するとセットアップが完了します。

<!--
Once you have the development version of Gutenberg running on your local environment you will need to run the following from within the Gutenberg directory:
-->

ローカル環境で Gutenberg の開発版を起動したら、Gutenberg ディレクトリから以下を実行してください:

```bash
npm run dev
```

<!--
This will monitor/update changes you make.
-->

これは、あなたが行った変更を監視／更新します。

<!--
***In order to avoid huge downloads at WordCamp Contributor Days it is recommended that the environment is configured before the event.***
-->

**WordCamp コントリビューターデイでの膨大なダウンロードを避けるため、イベントの前に環境を設定することを推奨します。**

<!--
### **Good First Gutenberg Issues**
-->

### Gutenberg の Good First Issues

<!--
If you are looking for some unassigned first issues to get familiar with contribution to Gutenberg, [look here](https://github.com/WordPress/gutenberg/issues?utf8=%E2%9C%93&q=is%3Aopen+is%3Aissue+label%3A%22Good+First+Issue%22+-label%3A%22%5BStatus%5D+In+Progress%22+no%3Aassignee)
-->

Gutenberg への貢献に慣れるために、割り当てられていない最初の issue を探している場合は、[こちらをご覧ください](https://github.com/WordPress/gutenberg/issues?utf8=%E2%9C%93&q=is%3Aopen+is%3Aissue+label%3A%22Good+First+Issue%22+label%3A%22%5BStatus%5D+In+Progress%22+no%3Aassignee)。

<!--
### **Gutenberg First issue steps**
-->

### Gutenberg 最初の issue の手順

<!--
1.  Fork the Gutenberg repository to your own account.
2.  Clone your fork locally to your ‘plugins’ directory using \`git clone\`
3.  Create a new branch in your fork with the the issue number somewhere in the branch name (example: ***\`fix-admin\-align-center-12306\`*** would be a good branch name for issue: ***“Latest Posts block “align center” has no effect in admin [#12306](https://core.trac.wordpress.org/ticket/12306)”)***
4.  Make an initial commit 
5.  Publish your branch using:
-->

1.  Gutenberg リポジトリを自分のアカウントにフォークする。
2.  `git clone` を使用して、自分の「plugins」ディレクトリにフォークしたリポジトリをクローンする。
3.  フォークの中に新しいブランチを作成し、ブランチ名のどこかに issue 番号を入れる
(例: ***`fix-admin-align-center-12306`*** は、issue のブランチ名としてよいでしょう: ***“Latest Posts block “align center” has no effect in admin [#12306](https://core.trac.wordpress.org/ticket/12306)”)***
4.  最初のコミットを行う
5.  以下を使用してブランチを公開する:

```bash
git push -u origin <branch name>
```

<!--
Now you are ready to make your changes locally to fix the issue. When finished, commit your changes and push them to your branch.
-->

これで、ローカルで問題を修正する準備ができました。完了したら、変更をコミットしてブランチにプッシュします。

<!--
If you are ready to submit your changes for review to merge into Gutenberg, simply create a pull request via github.com by navigating to your branch. Create pull request and fill out the information requested in the form.
-->

変更を Gutenberg にマージするためにレビューに出す準備ができたら、github.com から自分のブランチに移動してプルリクエストを作成します。プルリクエストを作成し、フォームに必要事項を入力してください。
