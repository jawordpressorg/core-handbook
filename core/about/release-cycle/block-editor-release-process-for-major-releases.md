<!--
# Block Editor Release Process for Major Releases
-->

# ブロックエディター メジャーリリース時のリリースプロセス

<!--
This guide will clarify how to handle the block editor portion of a major WordPress release. This is a living document, and feedback is welcomed as the hope is this can be continually improved as more people get experience managing this side of a release cycle. 
-->

このガイドでは、WordPress のメジャーリリースにおけるブロックエディターの扱い方を明らかにします。これは随時更新されるドキュメントであり、リリースサイクルのこの側面を管理する経験をより多くの人が得ることで、継続的に改善できることが期待されるため、フィードバックは歓迎されます。

<!--
## Release Team Roles Involved
-->

## リリースプロセスでの役割

<!--
### Editor tech leads
-->

### エディターテックリード

<!--
Coordinate merging of new features from Gutenberg plugin into core. This involves making sure all relevant feature work is merged and stable in the plugin before updating the npm packages and then updating the package versions in core. It also involves making sure any relevant PHP changes are manually added to the core codebase.
-->

Gutenberg プラグインからコアへの新機能のマージを調整します。これは、npm パッケージを更新する前に、関連するすべての機能がプラグインにマージされ、安定していることを確認し、コアのパッケージバージョンを更新することを含みます。また、関連する PHP の変更が手動でコアのコードベースに追加されるようにすることも含まれます。

<!--
### Editor triage leads
-->

### エディタートリアージリード

<!--
Set up and manage the release project board on GitHub and triage incoming bug reports for issues that need fixing during the release cycle. Run regular triage sessions in WordPress Slack, both synchronously and async. Ping Editor tech leads and feature developers as needed about any urgent bugs.
-->

GitHub のリリースプロジェクトボードを設定・管理し、リリースサイクル中に修正が必要な問題のトリアージを行います。同期と非同期の両方で、WordPress Slack で定期的にトリアージセッションを行います。緊急のバグについては、必要に応じてエディターテックリードや機能開発者に通知します。

<!--
### Documentation leads
-->

### ドキュメントリード

<!--
Wrangle dev notes for any new features or changes that impact the developer/extender community.
-->

開発者コミュニティに影響を与える新機能や変更について、開発ノートをまとめます。

<!--
## Quick Reference Timeline
-->

## タイムラインのクリックリファレンス

<!--
This is a list of the major time-critical tasks, sorted by when they should be done:
-->

これは、時間が重要である主要なタスクを、いつまでに終わらせるべきかによって分類したリストです:

<!--
**2 month before Beta 1**
-->

### ベータ1の2ヵ月前

<!--
*   Set up the release project board on GitHub.
*   Audit experimental APIs in Gutenberg
*   Create an overview issue of PHP changes that need to be manually added in core.
-->

*   GitHub にリリースプロジェクトボードを設置する。
*   実験的 API を精査する。
*   コアに手動で追加する必要がある PHP の変更について、概要の issue を作成する。

<!--
**1 month before Beta 1**
-->

### ベータ1の1ヵ月前

<!--
*   Update Trunk with the latest Gutenberg packages and PHP changes.
*   Create tracking issue for dev notes (dev notes should be published by RC1 and need plenty of time to wrangle).
-->

*   最新の Gutenberg パッケージと PHP の変更で Trunk をアップデートする。
*   開発ノートのためのイシュートラッカーを作成する (開発ノートは RC1 までに公開されるはずであり、そのために十分な時間が必要です)。

<!--
**Between Beta 1 and last RC**
-->

### ベータ1から最後の RC までの間

<!--
*   Triage recent bug reports and unlabelled issues for critical regressions.
-->

*   最近のバグレポートやラベルのない問題をトリアージし、重大なリグレッションを発見する。

<!--
**The week before each Beta/RC release**
-->

### 各ベータ/RCリリースの前の週

<!--
*   Go through all merged Pull Requests labeled [Backport to WP Beta/RC](https://github.com/WordPress/gutenberg/issues?q=label%3A%22Backport+to+WP+Beta%2FRC%22+is%3Aclosed) and check that they are OK to include.
*   Review any open Pull Requests with the same label.
*   Start package update/core patch process (described below).
-->

*   [Backport to WP Beta/RC](https://github.com/WordPress/gutenberg/issues?q=label%3A%22Backport+to+WP+Beta%2FRC%22+is%3Aclosed) とラベル付け、マージされたすべてのプルリクエストに目を通し、それらを含めても問題がないことを確認する。
*   同じラベルのプルリクエストをレビューする。
*   パッケージアップデートとコアパッチプロセスを開始する。

<!--
## Planning before the first Major Release Beta
-->

## 最初のメジャーリリースベータ版の前の計画

<!--
**Planning the editor releases and communicating the deadlines**
-->

### エディターのリリースを計画し、締め切りを伝える

<!--
At the start of each release cycle, a planning post is published ([example from 5.6](https://make.wordpress.org/core/2020/08/13/wordpress-5-6-release-planning/)) that shows key milestones leading up to a major WordPress release. With Gutenberg releases happening biweekly, you can then determine which Gutenberg release is scheduled closest to Beta 1 and, if necessary, rearrange the plugin release date so it aligns better with the Beta 1 date. Ideally, the Gutenberg RC should be cut 4-5 days before Beta 1 to give plenty of time for any bugs to be identified and fixed, as well as publishing the npm packages and updating their versions in core.
-->

各リリースサイクルの開始時には、WordPress のメジャーリリースに至るまでの主要なマイルストーンを示す計画に関する投稿が公開されます ([5.6の例](https://make.wordpress.org/core/2020/08/13/wordpress-5-6-release-planning/))。Gutenberg のリリースは隔週で行われるため、どの Gutenberg のリリースがベータ1に最も近い日程で予定されているかを判断し、必要であればプラグインのリリース日をベータ1の日程に合わせて再調整できます。理想的には、Gutenberg RC はベータ1の4～5日前にリリースし、バグを特定して修正し、npm パッケージを公開し、コアでバージョンを更新するための十分な時間を確保する必要があります。

<!--
As part of this planning, be sure to include a communication plan with deadlines that features need to be merged by in order to be included in a major release. The best place to share these deadlines is on Make Core and in [#core-editor](https://make.wordpress.org/core/tag/core-editor/) slack channel as a pinned post. You may also want to give a heads up for specific deadlines as they get closer in the core editor meetings.
-->

この計画の一環として、メジャーリリースに含めるために必要な機能のマージ期限を記載したコミュニケーションプランを必ず含めてください。これらの期限を共有するために最適な場所は、Make Core と [#core-editor](https://make.wordpress.org/core/tag/core-editor/) の Slack チャンネルで、ピン留めされた投稿として共有することです。また、特定の期限が近付いたら、コアエディターミーティングの中で注意を喚起することもよいでしょう。

<!--
**Project Board Management**
-->

### プロジェクトボードの管理

<!--
**How to set up a project board**
-->

#### プロジェクトボードの設定方法

<!--
To help coordinate tasks for release, it’s become a best practice to create a “Must Haves” board” for the major release in Gutenberg’s GitHub repo. [Here’s an example from 5.5](https://github.com/WordPress/gutenberg/projects/45). This board  should contain issues and PRs along with meta tasks like audits, discussion points, etc.
-->

リリースのタスクを調整するために、Gutenberg の GitHub リポジトリにメジャーリリースの「Must Haves」ボードを作成することがベストプラクティスとなっています。[これは5.5の例です](https://github.com/WordPress/gutenberg/projects/45)。このボードには、精査やディスカッションポイントなどのメタタスクに加え、issue やプルリクエストが含まれるはずです。

<!--
Generally speaking, the following columns are recommended:
-->

一般的には、以下のカラムが推奨されます:

<!--
*   To do: Contained issues/cards with all the tasks for which there is no progress yet. Try to keep items ordered by priority.
*   In Progress: Contained tasks that must be done and had someone working on them.
*   Needs reviews: Tasks that needed a review.
*   Research/Discussions in progress: An area to record issues that may be a must for a release but where there was no conclusion. Some possible reasons for not having a conclusion are:
    *   The problem was critical but was impossible to replicate, so it’s a matter of waiting for more information to understand the specific conditions where the problem happens.
    *   It is not clear yet if the issue is a regression or not, or it is not clear if the issue is a bug or desired behavior.
    *   The issue required a very complex testing setup or trying to replicate it takes a lot of time. In that case, it’s recommended that you write a comment upon finding the issue saying what needed to be done to test it. This helps make it easier for others to jump in to help with testing. If needed, you may need to add the “needs-testing” label as well. From there, make sure to include it in the issue part of the board so you don’t lose track. As soon as things are tested, you can move the issue to the “To do” column if it should be fixed or archive/close the issue if it does not need a fix. 
*   Approved: Tasks that were ready to merge (reviewed and approved). This is helpful to see at a glance any issues that might be approved but that the PR author hasn’t merged yet and can enable you to keep PRs moving. 
*   Done: Tasks that were finished, merged, etc. and didn’t require any additional work.
*   Notes, Useful Links, Etc: this is a helpful column to add relevant information like:
    *   The version of Gutenberg that the last WordPress release included and the version of Gutenberg that we were going to include in the next major release. 
    *   Link to the WordPress release cycle page.
    *   Link to the WordPress Planning Roundup post that included the most relevant editor features.
    *   During the release, you’ll find many people will ask questions. If a question was repeated multiple times, that was a signal to include the information people were asking in this column.
-->

*   To do: まだ進行していないすべてのタスクの issue やカードを含め、優先度順に並べる。
*   In Progress: 必ず完了させなければならないタスクで、誰かが取り組んでいるもの。
*   Needs reviews: レビューが必要なタスク。
*   Research/Discussions in progress: リリースのために必要かもしれないが、結論が出ていない問題を記録するエリア。結論が出ない理由として考えられることは、以下のようなものです:
    *   問題はクリティカルであるが、再現が不可能であるため、問題が発生する具体的な状況を理解するためにより多くの情報を待つ必要がある。
    *   その問題がリグレッションなのかそうでないのか、あるいはバグなのか望ましい動作なのかがまだ明確ではない。
    *   その問題が非常に複雑なテスト手順を必要とするか、その問題を再現しようとすると多くの時間がかかる。そのような場合は、問題を発見したときに、それをテストするために何が必要だったかをコメントとして書くことをおすすめします。こうすることで、他の人がテストしやすくなります。必要であれば、「needs-testing」のラベルを追加することもよいでしょう。それから、見失わないようにボードの issue の部分にそれを含めるようにしてください。テストが終わり次第、修正すべき問題であれば「To Do」欄に移動し、修正の必要がなければアーカイブするかクローズしてください。
*   Approved: マージする準備ができた (レビューされ、承認された) タスク。これは、承認されたかもしれないが、プルリクエスト作成者がまだマージしていない issue を一目で確認することに役立ち、プルリクエストを継続的に進めることができます。
*   Done: 作業が完了し、マージなどが行われ、追加作業が必要ないもの。
*   メモ、便利なリンクなど: 以下のような関連情報を追加することに役立つ列です:
    *   前回の WordPress リリースに含まれた Gutenberg のバージョンと、次のメジャーリリースに含まれる予定の Gutenberg のバージョン。
    *   WordPress リリースサイクルページへのリンク。
    *   最も関連性の高いエディター機能を含む、WordPress Planning Roundup 投稿へのリンク。
    *   リリースの間、多くの人が質問するでしょう。質問が何度も繰り返された場合、人々が求めている情報をこのカラムにを含めるという合図です。

<!--
After creating the board, it’s recommended that you [configure GitHub automation](https://docs.github.com/en/free-pro-team@latest/github/managing-your-work-on-github/configuring-automation-for-project-boards) to move tasks to “Done” when the relevant PRs are merged or issues are closed and to move PRs to needs review when they are pending approval. This will lessen the amount of meta work that needs to be done.
-->

ボードを作成したら、関連するプルリクエストがマージされたときや issue がクローズされたときにタスクを「Done」に移動し、プルリクエストが承認待ちのときに「needs review」に移動するように、[GitHub の自動化を設定すること](https://docs.github.com/en/free-pro-team@latest/github/managing-your-work-on-github/configuring-automation-for-project-boards)をおすすめします。これにより、実行する必要があるメタ作業の量を減らすことができます。

<!--
**How to keep the project board useful for others**
-->

#### プロジェクトボードを他の人のために役立てるには

<!--
Since the project board will be a place that meetings reference and people bookmark, it’s important to take steps to keep it current and useful for others. The following actions are recommended and can be divided up:
-->

プロジェクトボードは、ミーティングで参照され人々がブックマークする場所となるため、情報を最新の状態に保ち、他の人にとって役立つようにすることが重要です。以下のアクションが推奨され、分割できます:

<!--
*   Sort items in “To do” column by priority. Keep the highest priority items at the top so more people will see them and perhaps jump in to help or at least be aware of current challenges. 
*   When an issue gets a PR associated, or a card got an issue, archive the issue or card and add the PR or issue to the board. 
*   Regularly move items to the most relevant columns as the status of a task changes. This is particularly important to do if automation doesn’t automatically catch them. For example, this can happen with meta tasks without any associated PRs. 
-->

*   「To do」欄の項目を優先順位で並べ替えます。優先順位の高い項目を一番上に置くことで、より多くの人がそれらを目にして、手助けに参加したり、少なくとも現在の問題に気付いたりできます。
*   issue にプルリクエストが関連付けられたり、カードに issue が追加された場合は、issue またはカードをアーカイブし、プルリクエストまたは issue をボードに追加します。
*   タスクのステータスが変化したら、定期的に最も関連性の高い列に項目を移動します。これは特に、自動化がそれを自動的に行わない場合に行うことが重要です。たとえば、関連するプルリクエストがないメタタスクで起こりえます。

<!--
**Where to share the project board**
-->

#### プロジェクトボードを共有する場所

<!--
To help others discover the project board, it’s recommended that you share the link to it regularly in both the core editor meetings and in the general slack channel as helpful. This will get people in the habit of checking the project board and for them to share it in turn. 
-->

他の人にプロジェクトボードを発見してもらうために、コアエディターのミーティングや一般的な Slack チャンネルで、定期的にプロジェクトボードへのリンクを共有することをおすすめします。これにより、人々はプロジェクトボードをチェックし、共有する習慣が身に付きます。

<!--
**Assigning Tasks From the Board**
-->

#### ボードからのタスクを割り当てる

<!--
For items in the “To Do” column, it’s recommended that you find someone assigned in time before the release milestones. The easiest way to do this is to ask in the [#core-editor](https://make.wordpress.org/core/tag/core-editor/) channel for volunteers to pick tasks from that column. If no one volunteers, you will need to do some research to find the people familiar with the items needing help (checking previous Gutenberg PRs can be helpful here) and asking them if they can take on that work or help another person do so. 
-->

「To Do」欄の項目については、リリースのマイルストーンまでに割り当てられる人を見つけることをおすすめします。最も簡単な方法は、[#core-editor](https://make.wordpress.org/core/tag/core-editor/) チャンネルで、その欄のタスクを選んでくれるボランティアを募集することです。ボランティアとして参加できる人がいない場合は、助けが必要な項目に詳しい人を見つけて (ここでは、過去の Gutenberg プルリクエストを確認することも役に立ちます)、その人に引き受けてもらえるか、または他の人に手伝ってもらえるかをたずねる必要があるでしょう。

<!--
## Knowing which features to include in the release
-->

## どの機能をリリースに含めるべきかを考える

<!--
**Review [release roadmap post](https://make.wordpress.org/core/2023/05/18/roadmap-to-6-3/) and recent** [**“What’s New”**](https://make.wordpress.org/core/tag/gutenberg-new/) **release posts to determine important features**
-->

**[リリースロードマップの投稿](https://make.wordpress.org/core/2023/05/18/roadmap-to-6-3/)と最近の** [**「What's New」**](https://make.wordpress.org/core/tag/gutenberg-new/) **リリース投稿をレビューし、重要な機能を決定します**。

<!--
The release roadmap post lists the features considered top priority for each release. Special attention should be given to these to make sure they land in core in a timely and stable manner.
-->

リリースロードマップの投稿には、各リリースで最優先とされる機能がリストアップされています。タイムリーで安定した方法でコアに取り込まれるよう、これらに特別な注意を払う必要があります。

<!--
To get a sense of all the features currently being worked on, as well as smaller enhancements and bug fixes, it’s good to review plugin release posts too.
-->

小さな機能強化やバグ修正だけでなく、現在取り組んでいるすべての機能を把握するためには、プラグインのリリース投稿も確認するとよいでしょう。

<!--
For experimental features in particular, it helps to ping the developers working on them and discuss whether they are ready to be included in core or not.
-->

特に実験的な機能については、それらに取り組んでいる開発者に連絡し、コアに含める準備ができているかどうかを話し合うことが役立ちます。

<!--
**Deciding on additional features to include**
-->

### 追加する機能を決定する

<!--
Outside of the main features of a release, there are often in progress additional features that are still helpful to include to help complement the release as a whole. This might include features that were missed in the last major release as well as simply more minor features or updates to include. Whether you can include these depends on various factors including but not limited to:
-->

リリースの主な機能以外に、リリース全体を補完するために含めると便利な追加機能が進行中であることがよくあります。これには、前回のメジャーリリースで見落とされた機能だけでなく、単純にマイナーな機能やアップデートが含まれるかもしれません。これらを含めることができるかどうかは、以下のようなさまざまな要因によりますが、これらに限定されるものではありません:

<!--
*   What features might be important to finish. 
*   The complexity/risk of each feature. 
*   How complementary they are to the main features for the release.
*   Whether there are individuals working on the feature. 
-->

*   どのような機能を完成させることが重要か。
*   各機能の複雑とリスク。
*   リリースの主な機能をどのように補完するか。
*   その機能に取り組んでいる人がいるかどうか。

<!--
For any feature you do decide to add, remember to add it to the release “Must Haves” Project Board in GitHub. As you can, do your best to help move these features along whether through helping with PRs, unblocking the original authors, etc. 
-->

あなたが追加すると決めた機能については、GitHub のリリースの「Must Haves」プロジェクトボードに追加することを忘れないでください。プルリクエストを手伝ったり、元の作成者のブロックを解除したりするなど、これらの機能を前進させるために最善を尽くしてください。

<!--
If there’s an additional feature you want to include that you don’t have anyone actively working on, please ask for volunteers in the [#core-editor](https://make.wordpress.org/core/tag/core-editor/) meetings during the Open Floor time. If you know of any developer who may be a good person to work on a given feature, it’s often best to ping them directly and ask if they are able to do so. Even if they can’t, they may be able to point you to someone who can!
-->

もしあなたが追加したい機能で、積極的に取り組んでいる人がいないものがあれば、[#core-editor](https://make.wordpress.org/core/tag/core-editor/) ミーティングのオープンフロアの時間にボランティアを募集してください。もしあなたが、ある機能に取り組むことに適した開発者を知っているなら、その開発者に連絡し、それが可能かどうかたずねることが良いでしょう。彼らができないとしても、できる人を紹介してくれるかもしれません !

<!--
**How to handle removing features**
-->

### 機能を削除するときの対処法

<!--
As with any release, there are going to be tough calls that have to be made. What follows are the best steps you can take to communicate effectively and, if needed, make the call to not include a feature in a release:
-->

どのようなリリースでもそうですが、厳しい決断を迫られることがあります。以下は、効果的なコミュニケーションを行い、必要であればリリースにその機能を含めないという決断を下すための最善のステップです:

<!--
*   Communicate as early as you can with the people working on the feature that it is at risk of not being included and clearly state what needs to be done by when in order to change that. 
*   Give updates to the release squad as things do or do not progress alongside updates in [#core-editor](https://make.wordpress.org/core/tag/core-editor/) meetings. 
*   If the decision is made to remove a feature, please write a post on Make Core announcing the final decision. [Here’s an example from a past release](https://make.wordpress.org/core/2020/02/07/navigation-block-exclusion-from-wp-5-4/). 
-->

*   その機能に取り組んでいる人々に、その機能が含まれないリスクがあることをできるだけ早く伝え、それを変更するにはいつまでに何をする必要があるかを明確に示す。
*   [#core-editor](https://make.wordpress.org/core/tag/core-editor/) ミーティングでのアップデートと並行して、進捗があった場合やなかった場合のアップデートをリリースチームに伝える。
*   機能の削除が決定された場合、Make Core に最終決定を知らせる記事を書いてください。[これは過去のリリースの例です](https://make.wordpress.org/core/2020/02/07/navigation-block-exclusion-from-wp-5-4/)。

<!--
The key in all of this is clear, timely communication so all involved (contributors, release squad members, etc) can prepare appropriately. 
-->

これらすべてにおいて重要なことは、すべての関係者 (貢献者、リリースチームのメンバーなど) が適切な準備ができるように、明確でタイムリーなコミュニケーションをとることです。

<!--
## Experimental API Management
-->

## 実験的 API の管理

<!--
Since the [private-apis](https://github.com/WordPress/gutenberg/tree/trunk/packages/private-apis) system was created in early 2023, the system for managing experimental APIs changed, and everything that is not stable or not meant to be available as a public API is kept private.
-->

2023年初頭に [private-apis](https://github.com/WordPress/gutenberg/tree/trunk/packages/private-apis) システムが作成されて以来、実験的 API を管理するシステムが変更され、安定していないものや公開 API として利用する予定のないものはすべて非公開となりました。

<!--
However, there are still many older experimental APIs in Gutenberg, which can be recognised by their `__experimental` prefix. These can be functions, properties or variables and they can be found throughout the codebase. Every release it’s customary to do an audit of these and check if any are ready for stabilisation. It’s important that stabilisation be done before the first beta 1 release (ideally at least two weeks beforehand) as renames during the beta phase are not possible.
-->

しかし、Gutenberg にはまだ多くの古い実験的 API が残っており、接頭辞が `__experimental` であることで見分けることができます。これらは関数、プロパティ、変数であり、コードベースのいたるところにあります。リリースのたびに、これらの API を監査し、安定化の準備ができているかどうかをチェックすることが通例です。ベータ段階では名前の変更ができないため、最初のベータ1リリースの前 (理想的には少なくとも2週間前) に安定化を行うことが重要です。

<!--
**How to run the audit**
-->

### 精査する方法

<!--
Generally speaking, the process is as follows:
-->

一般的には、以下のような流れになります:

<!--
*   Use the script below to audit experimental APIs
*   [Use git blame](https://docs.github.com/en/free-pro-team@latest/github/managing-files-in-a-repository/tracking-changes-in-a-file) to identify who was involved with each API
*   Create an overview issue in GitHub tracking each experimental API pinging those involved to decide whether an API needs to be stabilized ([example from 6.2](https://github.com/WordPress/gutenberg/issues/47196)).
-->

*   以下のスクリプトを使って実験的 API を精査する
*   [git blame を使って](https://docs.github.com/en/free-pro-team@latest/github/managing-files-in-a-repository/tracking-changes-in-a-file)各 API に誰が関わったかを特定する
*   各実験的 API を追跡するために、GitHub で概要の issue を作成し、API を安定化させる必要があるかどうかを決定するために関係者に通知する ([6.2 の例](https://github.com/WordPress/gutenberg/issues/47196))。

<!--
**Task Breakdown**
-->

### タスクの内訳

<!--
To get started, here’s a script to use to begin auditing the experimental APIs:
-->

まず、実験的 API の精査を開始するために使用するスクリプトを次に示します:

[https://raw.githubusercontent.com/WordPress/gutenberg/trunk/bin/list-experimental-api-matches.sh](https://raw.githubusercontent.com/WordPress/gutenberg/trunk/bin/list-experimental-api-matches.sh)

<!--
With the information from the report and any information manually collected, it can help to then group related experimental APIs to get a sense of what’s in place currently. From there, use git blame to know who was involved in each API in order to ping them. You can then create a new overview issue in GitHub that lists out a checkbox for each API where one can see at a glance the status of whether a decision has been made around the API being stabilized or not. 
-->

レポートからの情報と手動で収集した情報があれば、関連する実験的な API をグループ化して、現在何があるのかを把握することに役立ちます。そこから git blame を使って、それぞれの API に誰が関与していたかを知ることで、彼らに通知を送ることができます。そして GitHub に新しい概要の issue を作成し、各 API のチェックボックスをリストアップすれば、API の安定化に関する決定がなされたかどうかのステータスが一目でわかるようになります。

<!--
## Communication Management
-->

## コミュニケーション管理

<!--
**Planning and Writing Dev Notes**
-->

### 開発ノートの計画と執筆

<!--
*For more context on Dev Note best practices, check out* [*this handbook page*](https://make.wordpress.org/core/handbook/tutorials/writing-developer-notes/)*.*
-->

*Dev Note のベストプラクティスに関するより詳しい情報は、[このハンドブックのページ](https://make.wordpress.org/core/handbook/tutorials/writing-developer-notes/)をチェックしてください。*

<!--
In order to know what needs a Dev Note, you can check all PRs [labeled with  “Needs Dev Note”.](https://github.com/WordPress/gutenberg/issues?q=label%3A%22Needs+Dev+Note%22.) You might find that there are more PRs than you can feasible write individual posts for without overwhelming the community with information. The best thing to do if you find too many PRs with that label is to group related changes and propose a dev note for each group.
-->

Dev Note が必要なものを知るために、[「Needs Dev Note」とラベルづけされた](https://github.com/WordPress/gutenberg/issues?q=label%3A%22Needs+Dev+Note%22.)プルリクエストをすべてチェックできます。個々の投稿を書くことでコミュニティを情報で圧倒してしまうほど、多くのプルリクエストがあることに気付くかもしれません。このようなラベルのプルリクエストが多すぎる場合、最善の方法は、関連する変更をグループ化しグループごとに開発ノートを提案することです。

<!--
Once you have a sense of the different dev notes that are needed, create a GitHub issue ([previous example](https://github.com/WordPress/gutenberg/issues/20185)) detailing the plan: what posts need to be done, what sections for each post, and which PRs are included in each. When doing so, make sure to ping the people that had PRs needing dev notes to contribute to this effort. Your job ideally should be to wrangle the updates from each PR author and plan out the timeline for sharing each dev note so that you don’t share too many in a short period of time. To help with this, it’s recommended to share target dates in order to help space out and plan appropriately. 
-->

必要な開発ノートの種類がわかったら、GitHub の issue ([以前の例](https://github.com/WordPress/gutenberg/issues/20185)) に計画を詳しく書きましょう。どのような投稿が必要で、それぞれの投稿にはどのようなセクションがあり、それぞれの投稿にどのプルリクエストが含まれるのかなどです。その際、開発ノートが必要なプルリクエストを持っている人たちに、作業に取り組むよう通知してください。あなたの理想的な仕事は、それぞれのプルリクエストの作成者からのアップデートを取りまとめ、各開発ノートを共有するタイムラインを計画し、短期間に共有しすぎないようにすることです。これを解決するには、適切な間隔と計画を立てるために、目標日を共有することをおすすめします。

<!--
Keep in mind that dev notes are extremely collaborative efforts requiring help from many different people! This might mean that some people you need information from didn’t see the ping the first time or don’t have the availability to take writing one note. It’s okay and expected that follow-up will be needed, likely in the form of additional pings or even DMs in Slack to get updates. When each section is done for each dev note, you can then check the checkbox to show progress made and to help others see what’s left. 
-->

開発ノートは共同作業であり、多くの異なる人々の助けが必要であることに注意してください ! これは、あなたが情報を必要としている人の中には、最初の通知を見逃したり、ノートを書く時間がなかったりする人がいることを意味するかもしれません。おそらく、追加の通知や Slack のダイレクトメールなどの形で、最新情報を入手するためのフォローアップが必要になることでしょう。各開発ノートの各セクションが書き終わったら、チェックボックスにチェックを入れて進捗を表示し、他の人が残りの内容を確認できるようにします。

<!--
As you compile each dev note, particularly if you are combining multiple PRs into one dev note, make sure you share the posts with those involved for review so everyone is on the same page. Once there’s consensus there, make sure to then share the dev notes with those involved in the major release squad to get a final review. Finally, make sure not to share too many dev notes in a short period of time.  
-->

各開発ノートをまとめる際、特に複数のプルリクエストを1つの開発ノートにまとめる場合は、関係者と投稿を共有し、全員が同じページで確認できるようにしましょう。そこで合意が得られたら、その開発ノートをメジャーリリースチーム関係者と共有して、最終的なレビューを受けるようにしてください。最後に、短期間にあまり多くの開発ノートを共有しないように注意してください。

<!--
## General Triage Management
-->

## 一般的なトリアージ管理

<!--
**Regular Triage**
-->

### 通常のトリアージ

<!--
Because months pass between core releases, it’s important to regularly check in on GitHub to triage issues (ideally weekly) particularly [new ones that are unlabeled](https://github.com/WordPress/gutenberg/issues?q=is%3Aissue+is%3Aopen+no%3Alabel+sort%3Acreated-desc). The key is to not miss anything that might be critical. 
-->

コアリリースの間に数ヵ月が経過するため、GitHub で定期的に (理想的には毎週) 問題をトリアージすることが重要です。特に、[ラベルのない新しい issue](https://github.com/WordPress/gutenberg/issues?q=is%3Aissue+is%3Aopen+no%3Alabel+sort%3Acreated-desc) が重要です。ポイントは、重大かもしれないものを見逃さないことです。

<!--
**High Level Triage**
-->

### ハイレベルなトリアージ

<!--
Outside of reviewing unlabeled issues, it’s important to take time to review all reported issues since a major release occurred to spot any key critical issues to resolve. This is a great task to divide up among others. The easiest way to do this is to divide the work into month-long increments ([example link for all bugs reported in October 2019](https://github.com/WordPress/gutenberg/issues?page=2&q=is%3Aissue+is%3Aopen+label%3A%22%5BType%5D+Bug%22+created%3A2019-10-01..2019-10-31+sort%3Acreated-asc&utf8=%E2%9C%93)).
-->

ラベルのない issue をレビューすること以外では、解決すべき重要な問題を見つけるために、メジャーリリース以降に報告されたすべての issue を時間をかけてレビューすることが重要です。これは、他の人と分担することが最適です。これを行う最も簡単な方法は、作業を月単位に分割することです ([2019年10月に報告されたすべてのバグのリンクの例](https://github.com/WordPress/gutenberg/issues?page=2&q=is%3Aissue+is%3Aopen+label%3A%22%5BType%5D+Bug%22+created%3A2019-10-01..2019-10-31+sort%3Acreated-asc&utf8=%E2%9C%93))。

<!--
**Important Note For Determining How Critical A Bug Is**
-->

### バグがどの程度重大かを判断するための重要な注意事項

<!--
When reviewing bug reports and trying to determine how critical they are, it becomes even more important to know the version that introduced the particular bug. For example, you might find a bug that was introduced in many core WordPress versions ago but that doesn’t have many comments. This is a good sign that the bug is not truly critical to fix. Because after the first Beta, you can only include bug fixes for issues that regressed during the alpha phase, it’s essential to know if the bug you are reviewing affects the latest stable release of WordPress. This might require having multiple testing environments with different setups in order to determine the impact (current version of WordPress, beta version of core Release, and the latest version of Gutenberg). It might also mean following up with those who reported issues to get more information about their particular setup like if they are using Gutenberg and, if so, what version. 
-->

バグレポートを確認し、それがどの程度重大なものかを判断しようとする場合、特定のバグが導入されたバージョンを知ることがさらに重要になります。たとえば、WordPress の多くのコアバージョンで導入されたものの、コメントがあまりないバグを見つけるかもしれません。これは、そのバグが本当に修正すべき重要なものではないという良い兆候です。最初のベータ版の後は、アルファフェーズでリグレッションを起こした問題のバグ修正のみを含めることができるため、レビューしているバグが WordPress の最新の安定リリースに影響するかどうかを知ることが重要です。影響を判断するために、異なるセットアップで複数のテスト環境を用意する必要があるかもしれません (WordPress の現行バージョン、コアリリースのベータ版、Gutenberg の最新バージョン)。また、Gutenberg を使用しているかどうか、使用している場合はどのバージョンかなど、特定のセットアップに関する詳細な情報を得るために、問題を報告した人をフォローアップする必要があるかもしれません。また、問題を報告した人をフォローアップして、Gutenberg を使用しているかどうか、使用している場合はどのバージョンかなど、特定の設定に関する詳細な情報を得る必要があるかもしれません。

<!--
## Managing the first WordPress Beta release
-->

## 最初の WordPress ベータリリースの管理

<!--
**Important Context**
-->

### 重要な背景

<!--
The first beta is a very significant deadline since no additional features or enhancements can be included after this milestone. Exceptions for enhancements to new features can be made: these must be discussed with the release team, and if approved a Trac ticket should be created for each feature with the type “task (blessed)”. All enhancements to these tasks must be finished before RC1.
-->

最初のベータ版マイルストーン以降は追加機能や拡張機能を含めることができないため、最初のベータ版は非常に重要な期限となります。新機能の拡張には例外を設けることができます。これらについてはリリースチームと話し合う必要があり、承認された場合は、機能ごとに「task (blessed)」タイプの Trac チケットを作成する必要があります。これらのタスクに対するすべての機能拡張は、RC1よりも前に完了する必要があります。

<!--
**To make the process easier, start updating trunk as early as possible before Beta 1**
-->

### プロセスを簡単にするために、ベータ1の前にできるだけ早く trunk の更新を開始してください

<!--
As the volume of changes for each release is quite high, it helps to start adding new features to core trunk as early as possible in the cycle. This means both updating the `@wordpress` npm packages used by core, and manually syncing any PHP changes from the `lib` and `phpunit` folders in Gutenberg.
-->

各リリースの変更の量は非常に多いため、サイクルのできるだけ早い段階でコア trunk に新機能の追加を開始することが役立ちます。これは、コアによって使用される `@wordpress` npm パッケージを更新することと、Gutenberg の `lib` フォルダーと `phpunit` フォルダーから PHP の変更を手動で同期することの両方を意味します。

<!--
**Make sure any experimental features are behind feature flags in Gutenberg so they don’t accidentally get included in core**
-->

### 実験的な機能が誤ってコアに含まれないように、Gutenberg の機能フラグによって管理されていることを確認してください

<!--
In order to safely update the npm packages in core, experimental Gutenberg features that aren’t slated for inclusion in core must be safely behind feature flags. `IS_GUTENBERG_PLUGIN` flag is commonly used for this purpose, or a specific feature filter may be used, such as in [this example](https://github.com/WordPress/gutenberg/pull/52579) for the interactivity API.
-->

コアの npm パッケージを安全に更新するには、コアに含める予定のない実験的な Gutenberg 機能を機能フラグから隠す必要があります。この目的のために `IS_GUTENBERG_PLUGIN` フラグが一般的に使用されます。またはインタラクティビティ API の[この例](https://github.com/WordPress/gutenberg/pull/52579)のように、特定の機能フィルターが使用される場合もあります。

<!--
**List PHP changes to be manually synced**
-->

### 手動で同期する PHP の変更をリストアップする

<!--
Create an overview issue of all the changes from the `lib` and `phpunit` folders that need to be manually synced. Using git blame, find the authors of those changes and ping them to create core PRs for them.
-->

手動で同期する必要がある `lib` フォルダーと `phpunit` フォルダーから、すべての変更に関する概要の issue を作成します。 git blame を使用して、それらの変更の作成者を見つけて通知し、それらの変更のコアプルリクエストを作成します。

<!--
The PHP files in `block-library` package don’t need to be manually synced, as they are auto-generated in core based on the npm package.
-->

`block-library` パッケージ内の PHP ファイルは、npm パッケージにもとづいてコアで自動生成されるため、手動で同期する必要はありません。

<!--
## Managing Weekly Beta and RC releases
-->

## ウィークリーベータ版と RC リリースの管理

<!--
After the first beta, there are weekly beta releases leading up to the Release Candidate. At this point, there are three main tasks to take care of: triage new issues, cherry-pick PRs for inclusion in the release, and update package and core paths. The following section is broken down into these three areas. 
-->

最初のベータ版の後、リリース候補に至るまで毎週ベータ版がリリースされます。この時点では、新しい issue のトリアージ、リリースに含めるプルリクエストのチェリーピック、パッケージとコアパスの更新という3つの主なタスクがあります。次のセクションでは、これら3つの領域に分けて説明します。

<!--
**Triage New Issues**
-->

### 新しい issue のトリアージ

<!--
Throughout the week, it is best to check all new issues reported since the last release to make sure no regressions have been found. If issues have been created for regressions, add those issues to the “Must Haves” project board immediately. 
-->

その週を通して、前回のリリース以降に報告されたすべての新しい issue をチェックし、リグレッションが見つかっていないことを確認することがベストです。リグレッションのために issue が作成された場合、それらの issue をすぐに「Must Haves」プロジェクトボードに追加してください。

<!--
When PR’s are submitted for issues on the “Must Haves” project board, add the “Backport to WP Beta/RC” label to the issue so you can keep track of what to include in the next beta release. 
-->

「Must Haves」プロジェクトボードにある issue に対してプルリクエストが提出されたら、その issue に「Backport to WP Beta/RC」というラベルを追加して、次のベータリリースに何を含めるべきかを追跡できるようにしてください。

<!--
Outside of triaging these issues for inclusion in the “Must Haves” project board, it’s important to make sure that any issues added are assigned to someone to resolve, particularly with beta releases occuring on a weekly schedule.. 
-->

「Must Haves」プロジェクトボードに含めるためにこれらの issue をトリアージする以外には、特にベータ版のリリースが毎週のスケジュールで行われるため、追加された issue が誰かに割り当てられ、解決されるようにすることが重要です。

### リリース用プルリクエストのチェリーピックについて

<!--
Once tasks on the “Must Haves” board are completed they need to be backported into the core to be available on the next beta or RC version. This is the process to do it:
-->

「Must Haves」ボード上のタスクが完了したら、次のベータ版または RC 版で利用できるようにコアにバックポートする必要があります。これはそのためのプロセスです:

<!--
*   If a wp/x.x (should have the correct WP release number) hasn’t been created yet, create it and push it to the remote repo.
*   Review all PRs with the label [“Backport to WP Beta/RC”](https://github.com/WordPress/gutenberg/pulls?q=label%3A%22Backport+to+WP+Core%22+sort%3Acreated-desc+). Verify if everything is expected, and that the PRs are not “risky” to go into a core release.
*   Create a branch based on wp/trunk and named in accordance with the release being prepared e.g: wp/trunk-5-4-0-rc-1.
*   Cherry-pick each PR into the newly created branch.

    *   There is [a convenient cherry-picking automation](https://developer.wordpress.org/block-editor/contributors/code/release/auto-cherry-picking/) available via `npm run cherry-pick`. It finds all merged Pull Requests with the “Backport to WP Beta/RC” label, cherry-picks them, and asks whether to automatically comment on the relevant PRs and push the branch to Github. You can also pass another label as the first argument.

    *   You can also do it manually. The hash of the commit can be extracted from the GitHub pull request page. In order to avoid merge conflicts, it is important to make sure the commits are cherry-picked in the same order they were made in trunk. This will likely not be the same order that appears in the label view, so double-check the merge date and if necessary refer to the [commit history](https://github.com/WordPress/gutenberg/commits/master). You can combine multiple commits in a single command, like so: `git cherry-pick c82094d8389b1756f05d4079ba98e4ee25961502 && git cherry-pick 548e600f14924d7fcfdb5250f45f718d3759d022 && git cherry-pick b72b41e27f008540410c45023b655c8ee20b67ae`
*   Merge conflicts may still happen. If they do, you will have to resolve them, and if you are unsure how, message the PR author for assistance. Take notes about what steps were taken to resolve the conflict.
*   After solving a conflict execute the cherry-pick command (or the cherry-pick automation) with the remaining commits to merge.
*   Push the branch to GitHub.
*   Create a pull request on GitHub from the branch you created into the wp-trunk branch. The PR description should include a table that lists all the PRs that were cherry-picked, the authors (pinging the authors with a mention so the authors are aware that the PR will be part of the next WordPress release) and specify the changes that were made to solve the conflicts (in case there was a conflict). A sample PR can be checked at  [https://github.com/WordPress/gutenberg/pull/21083](https://href.li/?https://github.com/WordPress/gutenberg/pull/21083).
*   Verify that continuous integration executed with success for the PR.
*   If there were merge conflicts to solve, you might want to ping the authors of the conflicting commits to double-check they were solved correctly. Otherwise, if all tests pass on CI, it’s fine to go ahead and merge the PR to the release branch.
*   After merging, run the package publish task from the release branch:
    *   On [this page](https://github.com/WordPress/gutenberg/actions/workflows/publish-npm-packages.yml), click on the “Run workflow” button, choose the release branch, release type should be “wp” and the release version should be added underneath.
    *   Once the workflow appears in the list below, click through to authorise it. If you don’t have `gutenberg-core` access, ask someone who does to approve it for you.
    *   This workflow will publish the npm packages with a dist tag corresponding to the release, which can then be used to select the correct package versions in core.
    -->

*   wp/x.x (正しい WP リリース番号のはずです) がまだ作成されていない場合は、作成してリモートリポジトリにプッシュしてください。
*   [Backport to WP Beta/RC](https://github.com/WordPress/gutenberg/pulls?q=label%3A%22Backport+to+WP+Core%22+sort%3Acreated-desc+) というラベルがついたプルリクエストをすべてレビューしてください。すべてが期待通りかどうか、プルリクエストがコアリリースに入ることが「リスク」ではないかどうかを確認します。
*   wp/trunk をベースにブランチを作成し、準備中のリリースに従って名前をつけます (例: wp/trunk-5-4-0-rc-1)。
*   各プルリクエストを新しく作成したブランチにチェリーピックします。

    *   [便利なチェリーピッキングの自動化](https://developer.wordpress.org/block-editor/contributors/code/release/auto-cherry-picking/)が `npm run cherry-pick` によって利用できます。これは、「Backport to WP Beta/RC」ラベルのついたすべてのマージされたプルリクエストを見つけ、それらをチェリーピックし、関連するプルリクエストに自動的にコメントし、ブランチを Github にプッシュするかどうかを尋ねます。第一引数に別のラベルを渡すこともできます。

    *   手動で行うこともできます。コミットのハッシュは GitHub のプルリクエストページから抽出できます。マージのコンフリクトを避けるためには、trunk で行われたのと同じ順番でコミットをチェリーピックすることが重要です。これは、ラベルビューに表示される順番と同じではない可能性が高いので、マージされた日付を再確認し、必要に応じて[コミット履歴](https://github.com/WordPress/gutenberg/commits/master)を参照しましょう。複数のコミットを、このようにひとつのコマンドにまとめることもできます: `git cherry-pick c82094d8389b1756f05d4079ba98e4ee25961502 && git cherry-pick 548e600f14924d7fcfdb5250f45f718d3759d022 && git cherry-pick b72b41e27f008540410c45023b655c8ee20b67ae`
*   マージがコンフリクトする可能性があります。もしコンフリクトが起きたら、それを解決しなければなりません。解決方法がわからない場合は、プルリクエストの作者にメッセージを送って助けを求めてください。コンフリクトを解決するためにどのような手順が取られたかをメモしておいてください。
*   コンフリクトを解決したら、残りのコミットでチェリーピックコマンド (またはチェリーピックの自動化) を実行し、マージします。
*   ブランチを GitHub にプッシュします。
*   作成したブランチから wp-trunk ブランチへのプルリクエストを GitHub に作成します。プルリクエストの説明には、チェリーピックされたプルリクエストの一覧、作者 (プルリクエストが次の WordPress リリースの一部であることを作者に知らせるために、作者にメンションを付けて ping を送信します)、(コンフリクトがあった場合は) コンフリクトを解決するために行われた変更を記載します。プルリクエストのサンプルは [https://github.com/WordPress/gutenberg/pull/21083](https://href.li/?https://github.com/WordPress/gutenberg/pull/21083) で確認できます。
*   プルリクエストの継続的インテグレーションが成功したことを確認します。
*   解決すべきマージコンフリクトがある場合は、競合しているコミットの作成者に連絡し、それらが正しく解決されたことを再確認することをおすすめします。それ以外の場合、すべてのテストが CI で合格した場合は、プルリクエストをリリースブランチにマージしても問題ありません。
*   マージ後、リリースブランチからパッケージ公開タスクを実行します:
    *   [このページ](https://github.com/WordPress/gutenberg/actions/workflows/publish-npm-packages.yml)で、「Run workflow」ボタンをクリックし、リリースブランチを選択します。リリースタイプは「wp」で、その下にリリースバージョンが追加されます。
     * ワークフローが下のリストに表示されたら、クリックして承認します。`gutenberg-core` へのアクセス権を持っていない場合は、アクセス権を持っている人に承認を依頼してください。
     * このワークフローは、リリースに対応する dist タグを持つ npm パッケージを公開します。これは、コアで正しいパッケージバージョンを選択するために使用できます。

<!--
**Package update and core patch**
-->

### パッケージの更新とコアパッチ

<!--
*   After merging the cherry picking PR switch to the `wp/trunk` branch and run `git pull`.
*   Run the relevant Github action to update the `@wordpress` npm packages for a WordPress release as documented at [https://github.com/WordPress/gutenberg/blob/trunk/docs/contributors/code/release.md#wordpress-releases](https://github.com/WordPress/gutenberg/blob/trunk/docs/contributors/code/release.md#wordpress-releases)
*   Update the packages using the automated script by running `npm run sync-gutenberg-packages -- --dist-tag=wp-<VERSION>` in the wordpress-develop folder. Remember to use the same dist-tag as the newly released `@wordpress` packages, e.g. `wp-6.2` for the 6.2 major version.
*   Then run `npm run postsync-gutenberg-packages` in the wordpress-develop folder. It includes any new Gutenberg blocks in core and runs the required builds.
*   Verify the issues that were supposed to be resolved are in fact resolved on the WordPress trunk.
*   Create a [Trac](https://core.trac.wordpress.org/) ticket for the package updates in Core.
*   Submit a PR against wordpress-develop to make sure the continuous integration tests pass, and add the Trac ticket number to the description. This ensures the PR gets linked to the ticket, and the patch will then be created automatically. For example, here’s the PR from WordPress 6.0 release cycle: [#2564](https://github.com/WordPress/wordpress-develop/pull/2564)
*   Ask for reviews. During the beta stage a review is recommended but not mandatory; during the RC process a double signoff by two different committers is required. If you are a committer and are confident with the changes you can be one of the approvers and add the “dev-feedback” keyword.
*   When approved, commit the patch or coordinate with a committer to make sure it is committed in case you are not a committer.
*   If a branch for the WordPress release already exists, backporting the commit from trunk to the release branch is required.
-->

*   チェリーピックを行ったプルリクエストをマージしたら、`wp/trunk` ブランチに移動して `git pull` を実行します。
*   [https://github.com/WordPress/gutenberg/blob/trunk/docs/contributors/code/release.md#wordpress-releases](https://github.com/WordPress/gutenberg/blob/trunk/docs/contributors/code/release.md#wordpress-releases) に記載されているように、関連する Github アクションを実行して、WordPress リリース用の `@wordpress` npm パッケージを更新します。
*   wordpress-develop フォルダーで、自動化スクリプトである `npm run sync-gutenberg-packages -- --dist-tag=wp-<VERSION>` を実行し、パッケージを更新します。新しくリリースされた `@wordpress` パッケージと同じ dist-tag を使用することを忘れないでください。
*   次に、wordpress-develop フォルダーで `npm run postsync-gutenberg-packages` を実行します。新しい Gutenberg ブロックがコアに含まれ、必要なビルドが実行されます。
*   解決されるはずの問題が WordPress trunk 上で実際に解決されていることを確認します。
*   コアのパッケージ更新を更新するために [Trac](https://core.trac.wordpress.org/) チケットを作成します。
*   Wordpress-develop に対してプルリクエストを提出し、継続的インテグレーションのテストがパスしたことを確認し、説明に Trac のチケット番号を追加します。これにより、プルリクエストがチケットにリンクされ、パッチが自動的に作成されます。たとえば、WordPress 6.0 のリリースサイクルのプルリクエストは次の通りです: [#2564](https://github.com/WordPress/wordpress-develop/pull/2564)
*   レビューを依頼します。ベータ段階ではレビューが推奨されますが、必須ではありません。RC プロセスでは、2人のコミッターによるダブルチェック必要です。もしあなたがコミッターで、その変更に自信があるのであれば、承認者の一人として「dev-feedback」キーワードを追加してください。
*   承認されたら、パッチをコミットするか、コミッターでない場合はコミッターと調整してコミットされるようにしてください。
*   WordPress リリースのブランチがすでに存在する場合は、trunk からリリースブランチへのコミットのバックポートが必要です。
