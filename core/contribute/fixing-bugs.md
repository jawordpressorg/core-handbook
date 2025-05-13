<!--
# Fixing Bugs
-->

# バグの修正

<!--
A great way to contribute to the development of WordPress is to help patch bugs. Having a good working knowledge of PHP, JavaScript, or CSS is recommended.
-->

WordPress の開発に貢献するには、バグのパッチを作成することが重要です。PHP、JavaScript、CSS の知識があることが推奨されます。

<!--
First, if you have found a bug in WordPress, please make sure you [report it](https://make.wordpress.org/core/handbook/testing/reporting-bugs/). Please [search Trac](https://core.trac.wordpress.org/search) first to see if the bug has already been reported before creating a new ticket.
-->

まず、WordPress のバグを発見した場合は、必ず[報告](https://ja.wordpress.org/team/handbook/core/testing/reporting-bugs/)してください。新しいチケットを作成する前に、まずは [Trac を検索](https://core.trac.wordpress.org/search)して、そのバグがすでに報告されていないかどうかを確認してください。

<!--
Once you’ve either found an existing Trac ticket or created a new ticket for the bug, you can get to work.
-->

既存の Trac チケットを見つけるか、バグのために新しいチケットを作成したら、作業に取り掛かることができます。

<!--
If you want to help, but don’t know which bugs to fix, review the [Finding Bugs to Fix](#finding-bugs-to-fix) section below.
-->

貢献したいけれど、どのバグを直せばいいのかわからないという方は、以下の[修正すべきバグの発見](https://ja.wordpress.org/team/handbook/core/contribute/fixing-bugs/#finding-bugs-to-fix)セクションをご覧ください。

<!--
## Overview
-->

## 概要

<!--
WordPress uses Subversion for source control. You will want to *check out* a working copy of WordPress using a Subversion client (such as Tortoise SVN on Windows, using the command line on Mac and Linux). For more, read the [Subversion](https://make.wordpress.org/core/handbook/svn/) article.
-->

WordPress はソース管理に Subversion を使用しています。Subversion クライアント (Windows では Tortoise SVN、Mac や Linux ではコマンドライン) を使用して、WordPress の作業コピーを「チェックアウト」したいでしょう。詳しくは、[Subversion](https://ja.wordpress.org/team/handbook/core/svn/) の記事を読んでください。

<!--
One of the many benefits to using a version control system is that you can create a simple text file, called a [patch](https://make.wordpress.org/core/glossary/#patch), that shows exactly what you’ve changed – the lines of code you added, modified, and removed. A patch is also called a *diff*, for differences.
-->

バージョン管理システムを使うことの多くの利点の一つは、[パッチ](https://make.wordpress.org/core/glossary/#patch)と呼ばれる簡単なテキストファイルを作成し、あなたが何を変更したかを正確に示すことができることです。パッチは *diff* とも呼ばれ、追加したコードや変更したコード、削除したコードの行を示します。パッチは、差分の意味で *diff* とも呼ばれます。

<!--
If you are not familiar with how WordPress is written and organized, read the article on [the WordPress Codebase](https://make.wordpress.org/core/handbook/contribute/codebase/).
-->

WordPress がどのように書かれていてどのように構成されているかよく分からない場合は、[WordPress のコードベース](https://ja.wordpress.org/team/handbook/core/contribute/codebase/)の記事を読んでみてください。

<!--
Once you’ve figured out how to fix the bug by modifying WordPress core files, you should create a *patch*. Review the [Creating a Patch](https://make.wordpress.org/core/handbook/submitting-a-patch/ "Creating a Patch") documentation.
-->

WordPress のコアファイルを変更することでバグを修正する方法がわかったら、「パッチ」を作成します。[パッチの作成](https://ja.wordpress.org/team/handbook/core/submitting-a-patch/)のドキュメントを確認してください。

<!--
Once you’ve created a patch, upload it to the Trac ticket using the *Attach file* button, and add *has-patch* to the workflow keywords. Please don’t overwrite any existing, previous patches.
-->

パッチを作成したら、*Attach file* ボタンを使って Trac チケットにアップロードし、ワークフローのキーワードに *has-patch* を追加してください。既存のパッチは上書きしないでください。

<!--
## Finding Bugs to Fix
-->

## 修正すべきバグの発見

<!--
If you want to fix bugs in the core parts of WordPress, but don’t know what to fix, here are some suggestions on finding one:
-->

WordPress コアのバグを直したいけれど、何を直せばいいかわからないという方のために、探し方のヒントを紹介します。

<!--
*   Try starting with tickets that have been [tagged with the ‘good-first-bug’ keyword](https://core.trac.wordpress.org/tickets/good-first-bugs). They’re great for getting familiar with the process before attempting to solve more complicated problems.
*   Look through the [ticket report for the latest release](https://core.trac.wordpress.org/report/6), in particular the **Needs Patch** group.
*   Look through the [ticket report for “early” tickets](https://core.trac.wordpress.org/report/14). These tickets have been marked by contributing developers as needing attention early in the WordPress release cycle. Generally, this means a trusted core contributor has shown interest in it, “blessing” the ticket to a certain extent.
*   Look through the [Awaiting Review report](https://core.trac.wordpress.org/report/40). These tickets have not yet been slated for the next release of WordPress, but if a developer takes an interest in it, that can change.
*   There are individual reports of tickets for a number of specialized areas: you may be interested in writing unit tests (see [Automated Testing](https://make.wordpress.org/core/handbook/automated-testing/)), working on or providing feedback for [user interfaces and user experiences](https://core.trac.wordpress.org/report/35), [tickets of interest to the mobile development team](https://core.trac.wordpress.org/report/42), and [tickets requiring more documentation in the Codex](https://core.trac.wordpress.org/report/36).
*   If you are interested in tickets from a particular component, you can use the [Query](https://core.trac.wordpress.org/query) feature of Trac. For example, [all open XML-RPC tickets](https://core.trac.wordpress.org/query?status=!closed&component=XML-RPC), all [open Multisite](https://core.trac.wordpress.org/query?status=!closed&component=Multisite&group=milestone) tickets grouped by milestones, and all [open Accessibility tickets](https://core.trac.wordpress.org/query?status=!closed&component=Accessibility).
*   The WordPress development team has daily discussions on bug triage, and weekly project meetings. For dates and times, see the sidebar on [Make WordPress Core](https://make.wordpress.org/core/).
*   Consider joining the [wp-trac](http://lists.automattic.com/mailman/listinfo/wp-trac) mailing list to follow the discussions in every Trac ticket. Also follow along on [Make WordPress Core](https://make.wordpress.org/core/), and potentially [other Make WordPress blogs](http://make.wordpress.org).
-->

*   [good-first-bug キーワード](https://core.trac.wordpress.org/tickets/good-first-bugs)でタグ付けされたチケットから始めてみてください。これらは、より複雑な問題を解決しようとする前に、プロセスに慣れるために最適です。
*   [最新リリースのチケットレポート](https://core.trac.wordpress.org/report/6)、特に **Needs Patch** グループに目を通してみてください。
*   [初期のチケットレポート](https://core.trac.wordpress.org/report/14)に目を通してみてください。これらのチケットは、WordPress のリリースサイクルの初期に注意が必要であるとして、貢献する開発者によってマークされたものです。一般的に、これは信頼できるコア貢献者がそのチケットに関心を示し、ある程度まで精査されていることを意味します。
*   [レビュー報告待ち](https://core.trac.wordpress.org/report/40)に目を通してみてください。これらのチケットはまだ WordPress の次のリリースには予定されていませんが、開発者が興味を持てば変わるかもしれません。
*   専門的分野に関するチケットの個別レポートもいくつかあります。ユニットテスト ([自動テスト](https://ja.wordpress.org/team/handbook/core/automated-testing/)を参照) を書くことや、[ユーザーインターフェースやユーザー体験](https://core.trac.wordpress.org/report/35)、[モバイル開発チームが注目するチケット](https://core.trac.wordpress.org/report/42)、[Codex に多くのドキュメントを必要とするチケット](https://core.trac.wordpress.org/report/36)の作業やフィードバックに興味を持つかもしれません。
*   もし、特定のコンポーネントに関するチケットに興味があるなら、Trac の [クエリー](https://core.trac.wordpress.org/query)機能を使用できます。たとえば、[すべてのオープンな XML-RPC のチケット](https://core.trac.wordpress.org/query?status=!closed&component=XML-RPC)、マイルストーンでグループ化されたすべての [オープンなマルチサイト](https://core.trac.wordpress.org/query?status=!closed&component=Multisite&group=milestone)チケット、すべての[オープンなアクセシビリティチケット](https://core.trac.wordpress.org/query?status=!closed&component=Accessibility)などです。
*   WordPress 開発チームでは、毎日バグトリアージに関して議論し、毎週プロジェクトミーティングを行っています。日時については、[Make WordPress Core](https://make.wordpress.org/core/) のサイドバーをご覧ください。
*   [wp-trac](http://lists.automattic.com/mailman/listinfo/wp-trac) メーリングリストに参加すると、すべての Trac チケットでの議論をフォローできます。[Make WordPress Core](https://make.wordpress.org/core/) や[他の Make WordPress ブログ](http://make.wordpress.org)もフォローしてみてください。
