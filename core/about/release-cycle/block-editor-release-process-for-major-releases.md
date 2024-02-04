<!--
# Block Editor Release Process for Major Releases
-->

# ブロックエディター メジャーリリース時のリリースプロセス

<!--
This guide will clarify how to handle the Editor (Gutenberg) portion of a major WordPress release. This is a living document. You are encouraged to leave feedback and provide updates.
-->

このガイドでは、WordPress のメジャーリリースにおけるエディター (Gutenberg) の扱い方を明らかにします。これは随時更新されるドキュメントです。フィードバックやアップデートをお寄せください。

<!--
## Release team roles
-->

## リリースプロセスでの役割

<!--
It takes a team to manage the Editor release process for each major version of WordPress. You can learn more about the roles and responsibilities of each key role below. 
-->

WordPress の各メジャーバージョンのエディターリリースプロセスを管理するには、チームが必要です。主要な役割とその責任については、以下をご覧ください。

<!--
*   [Editor Tech Leads](https://make.wordpress.org/core/handbook/about/release-cycle/wordpress-release-team-and-focus-leads/#editor-tech-lead)
*   [Editor Triage Leads](https://make.wordpress.org/core/handbook/about/release-cycle/wordpress-release-team-and-focus-leads/#editor-triage-lead)
*   [Documentation Leads](https://make.wordpress.org/core/handbook/about/release-cycle/wordpress-release-team-and-focus-leads/#documentation-wrangling)
-->

*   [エディターテックリード](https://ja.wordpress.org/team/handbook/core/about/release-cycle/wordpress-release-team-and-focus-leads/#editor-tech-lead)
*   [エディタートリアージリード](https://ja.wordpress.org/team/handbook/core/about/release-cycle/wordpress-release-team-and-focus-leads/#editor-triage-lead)
*   [ドキュメントリード](https://ja.wordpress.org/team/handbook/core/about/release-cycle/wordpress-release-team-and-focus-leads/#documentation-wrangling)

<!--
## Quick reference timeline
-->

## タイムラインのクリックリファレンス

<!--
Here’s a list of the significant time-critical tasks, sorted by when they should be completed. More details about each task are available later in this document.
-->

これは時間が重要なタスクで、いつ完了する必要があるかを順に並べたリストです。各タスクの詳細については、このドキュメントの後半で説明します。

<!--
**Two months before Beta 1**
-->

### ベータ1の2ヵ月前

<!--
*   Set up the release project board on GitHub
*   Audit experimental APIs in Gutenberg
*   Create an overview issue of PHP changes that need to be manually added in Core
-->

*   GitHub にリリースプロジェクトボードを設置する
*   実験的 API を精査する
*   コアに手動で追加する必要がある PHP の変更について、概要の issue を作成する

<!--
**One month before Beta 1**
-->

### ベータ1の1ヵ月前

<!--
*   Update trunk with the latest Gutenberg packages and PHP changes
*   Create a tracking issue for dev notes, which should be published by RC1 and require plenty of time to wrangle
-->

*   最新の Gutenberg パッケージと PHP の変更で Trunk をアップデートする
*   開発者ノートのためのイシュートラッカーを作成します。開発者ノートは RC1までに公開されるはずであり、そのために十分な時間が必要です

<!--
**Between Beta 1 and the last RC**
-->

### ベータ1から最後の RC までの間

<!--
*   Triage recent bug reports and unlabelled issues for critical regressions
*   Fix all critical regressions and as many bug fixes related to the release as possible
-->

*   最近のバグレポートやラベルのない issue をトリアージし、重大なリグレッションを発見する
*   重要なリグレッションをすべて修正し、リリースに関連するバグを可能な限り修正する

<!--
**The week before each Beta/RC release**
-->

### 各ベータ/RC リリースの前の週

<!--
*   Go through all merged PRs labeled [`Backport to WP Beta/RC`](https://github.com/WordPress/gutenberg/issues?q=label%3A%22Backport+to+WP+Beta%2FRC%22+is%3Aclosed) and check that they are ok to include in the release
*   Review any open PRs with the same label
*   Start package update/core patch process
-->

*   [Backport to WP Beta/RC](https://github.com/WordPress/gutenberg/issues?q=label%3A%22Backport+to+WP+Beta%2FRC%22+is%3Aclosed) とラベル付け、マージされたすべてのプルリクエストに目を通し、それらを含めても問題がないことを確認する
*   同じラベルのプルリクエストをレビューする
*   パッケージアップデートとコアパッチプロセスを開始する

<!--
## Planning before the first Major Release Beta
-->

## 最初のメジャーリリースベータ版の前の計画

<!--
At the start of each release cycle, a planning roundup post should be published ([example from 6.3](https://make.wordpress.org/core/2023/05/18/wordpress-6-3-planning-roundup/)) that details key milestones leading up to the major WordPress release. This post includes deadlines for all Beta and RC releases and the names of all release team members. 
-->

各リリースサイクルの開始時には、WordPress のメジャーリリースに至るまでの主要なマイルストーンを示す計画に関する投稿が公開されます ([6.3の例](https://make.wordpress.org/core/2023/05/18/wordpress-6-3-planning-roundup/))。この投稿には、すべてのベータ版と RC 版のリリースの期限と、すべてのリリースチームメンバーの名前が含まれます。

<!--
### Scheduling the last editor release and communicating deadlines
-->

### 最後のエディターのリリースを計画し、締め切りを伝える

<!--
Gutenberg releases happen biweekly, so you can determine which Gutenberg release is scheduled closest to Beta 1 and, if necessary, rearrange the plugin release date to align better with Beta 1. 
-->

Gutenberg のリリースは隔週で行われるため、どの Gutenberg のリリースがベータ1に最も近い時期に予定されているかを判断し、必要に応じてプラグインのリリース日をベータ1に合わせて再調整できます。

<!--
Ideally, this last Gutenberg RC should be released 4-5 days before Beta 1. This schedule will give plenty of time for any bugs to be identified and fixed while allowing the team to publish npm packages and update their versions in Core. 
-->

理想的には、この最後 の Gutenberg RC はベータ1の4～5日前にリリースされるべきです。このスケジュールであれば、チームが npm パッケージを公開し、コアでバージョンを更新できるようにしながら、バグを特定して修正するために十分な時間が与えられます。

<!--
If a contributor wants to include a new Editor feature in the major release, it must be included in this last Gutenberg RC. Therefore, once you have identified the final Gutenberg release, share it in the [#core-editor](https://wordpress.slack.com/archives/C02QB2JS7) Slack channel and during the weekly Editor Weekly Chat meeting to allow contributors to prepare appropriately.
-->

貢献者がエディターの新機能をメジャーリリースに含めたい場合、この最後の Gutenberg RC に含める必要があります。そのため、最終的な Gutenberg のリリースが決まったら、[#core-editor](https://wordpress.slack.com/archives/C02QB2JS7) Slack チャンネルや、毎週のエディターチャットミーティングで共有し、貢献者が適切に準備できるようにしましょう。

<!--
### The Roadmap post
-->

### ロードマップに関する投稿

<!--
A Roadmap post identifies the features, enhancements, and bug fixes slated for the current major release ([example from 6.3](https://make.wordpress.org/core/2023/05/18/roadmap-to-6-3/)). The creation of this resource is a collaborative effort between release leads and contributors.
-->

ロードマップの投稿は、現在のメジャーリリース ([6.3の例](https://make.wordpress.org/core/2023/05/18/roadmap-to-6-3/)) で予定されている機能、拡張、バグ修正を特定します。このリソースの作成は、リリースリードと貢献者による共同作業です。

<!--
You should become familiar with this post if you are an Editor Tech or Triage lead. It’s an excellent resource for knowing what should be included in the release. It’s also invaluable for determining which reported issues are related to the release and which need to be added to the project board. More on that below. 
-->

エディターテックやトリアージリードであれば、この投稿をよく理解しておく必要があります。これは、リリースに何を含めるべきかを知るための優れたリソースです。また、報告されたどの問題がリリースに関連していて、どれをプロジェクトボードに追加する必要があるのかを判断するうえでも非常に役立ちます。詳細については以下をご覧ください。

<!--
## Managing the project board
-->

## プロジェクトボードの管理

<!--
Creating a “project board” for the major release in Gutenberg’s [GitHub repository](https://github.com/WordPress/gutenberg/projects?query=is%3Aopen) has become a best practice. [This board](https://github.com/WordPress/gutenberg/projects/45) helps coordinate tasks and should contain all issues and PRs related to the release.
-->

Gutenberg の [GitHub リポジトリ](https://github.com/WordPress/gutenberg/projects?query=is%3Aopen)にメジャーリリース用の「プロジェクトボード」を作成することがベストプラクティスとなっています。[このボード](https://github.com/WordPress/gutenberg/projects/45)はタスクの調整に役立ち、リリースに関連するすべての issue とプルリクエストを含む必要があります。

<!--
### Setting up the project board
-->

### プロジェクトボードの設定方法

<!--
Beginning with WordPress 6.3, a template has been created to help you set up the project board. 
-->

WordPress 6.3から、プロジェクトボードの設定に役立つテンプレートが作成されました。

<!--
*   Navigate to the template: [WordPress (X.X) Editor Tasks](https://github.com/orgs/WordPress/projects/126)
*   Click on the “Use this template” button to create a new board
*   Update the title of the board using the format “WordPress X.X Editor Tasks”
*   Update the “Punted to 6.X.1” and “Punted to 6.Y” column titles
*   Navigate to the [Gutenberg Projects](https://github.com/WordPress/gutenberg/projects?query=is%3Aopen) page and click the “Link Project” to link the newly created project to the Gutenberg repository. 
-->

*   テンプレートに移動します: [WordPress (X.X) Editor Tasks](https://github.com/orgs/WordPress/projects/126)
*   新しいボードを作成するために「Use this template」ボタンをクリックします
*   ボードのタイトルを「WordPress X.X Editor Tasks」の形式で更新します
*   「Punted to 6.X.1」と「Punted to 6.Y」のカラムタイトルを更新します
*   [Gutenberg Projects](https://github.com/WordPress/gutenberg/projects?query=is%3Aopen) ページに移動し、「Link Project」をクリックして新しく作成したプロジェクトを Gutenberg リポジトリにリンクします。

<!--
The template will contain the following columns:
-->

テンプレートには以下のカラムが含まれます:

<!--
*   Triage – All new issues enter the board in this column. Release leads then decide if the issues belong in the “Todo”, “In discussion / Needs decision” or other columns as needed. Issues can also be removed from the board completely if there is a general consensus among leads.
*   In Discussion / Needs Decision –  Contains issues or PRs that the team needs more time to consider for the release. Some possible reasons for not having a conclusion are:
    *   The problem was critical but was impossible to replicate, so it’s a matter of waiting for more information to understand the specific conditions where the problem happens.
    *   It still needs to be clarified if the issue is a regression or not, or it is not clear if the issue is a bug or desired behavior.
    *   The issue requires a complex testing setup, and replicating it takes time. In this case, you should write a comment upon finding the issue, saying what must be done to test it. This helps make it easier for others to help with testing. If needed, you may need to add the “needs-testing” label as well. Once the issue is tested and confirmed, move it to the “Todo” column. 
*   Todo – Contains issues that the team has determined should be fixed by the release but do not have a PR associated with them.
*   In Progress – Contains issues that the team has determined should be fixed by the release and have a PR associated with them.
*   Needs Review – Contains PRs associated with issues in the “In Progress” columns that are not yet merged and need review.
*   Needs Core Commit – Contains PRs that need an additional Core commit, which the Editor Tech Leads determine. 
*   Done – Contains issues and PRs that are complete.
*   Punted to 6.X.1 – Contains issues and PRs that the team has determined should be punted to the next minor release.
*   Punted to 6.Y – Contains issues and PRs that the team has determined should be punted to the next major release.
-->

* Triage - すべての新しい issue は、このカラムのボードに追加されます。リリースリードは、必要に応じてその issue が「Todo」、「In discussion / Needs decision」、または他のカラムに属するかどうかを決定します。リードの間で一般的な合意が得られた場合は、issue をボードから完全に削除することもできます。
* In Discussion / Needs Decision - リリースに向けてチームが検討するためにさらに時間が必要な issue やプルリクエストが含まれます。結論が出ない理由としては、次のようなことが考えられます。
    *   問題は重大であるが、再現できなかったため、問題が発生する具体的な条件を理解するために、より多くの情報を待つ必要がある。
    *   その問題がリグレッションなのかそうでないのか、あるいはバグなのか期待された動作なのかを明確にする必要がある
    *   その問題は複雑なテスト設定を必要とし、その再現には時間がかかる。この場合、issue を見付けた時点で、それをテストするために何をしなければならないかをコメントとして書くべきです。こうすることで、他の人がテストを手伝いやすくなります。必要であれば、「needs-testing」ラベルも追加する必要があるかもしれません。issue をテストし問題を確認できたら、「Todo」列に移動してください。
*   Todo - チームがリリースまでに修正する必要があると判断したものの、プルリクエストが関連付けられていない issue が含まれます。
*   In Progress - チームがリリースまでに修正する必要があると判断し、プルリクエストが関連付けられている issue が含まれます。
*   Needs Review - 「In Progress」カラムの issue に関連するプルリクエストで、まだマージされておらず、レビューが必要なものが含まれます。
*   Needs Core Commit - エディターテックリードが、追加のコアコミットが必要であると決定したプルリクエストが含まれます。
*   Done - 完了した issue とプルリクエストが含まれます。
*   Punted to 6.X.1 - チームが次のマイナーリリースに持ち越すべきと判断した issue とプルリクエストが含まれます。
*   Punted to 6.Y - チームが次のメジャーリリースに持ち越すべきと判断した issue やプルリクエストが含まれます。

<!--
After you have created the project board, make sure to review the project board from the prior release and migrate over all punted issues and PRs. Remove each from the old project board once you have moved everything over.
-->

プロジェクトボードを作成したら、前のリリースのプロジェクトボードを確認し、前のリリースから持ち越された issue やプルリクエストをすべて移行してください。すべてを移行したら、古いプロジェクトボードからそれぞれ削除してください。

[![](https://make.wordpress.org/core/files/2023/08/project-board-1024x541.png)](https://make.wordpress.org/core/files/2023/08/project-board.png)

<!--
An example of the WordPress 6.4 Editor Tasks project board.
-->

これは、WordPress 6.4 Editor Tasks プロジェクトボードの例です。

<!--
Note that “punting” is a sports metaphor from [American football](https://en.wikipedia.org/wiki/Punt_(gridiron_football)). If you punt something, you decide not to include it in the current release, and it’s “punted” to the next minor or major release.
-->

「punting」は[アメリカンフットボール](https://en.wikipedia.org/wiki/Punt_(gridiron_football))に由来するスポーツの比喩であることに注意してください。何かを punt した場合、現在のリリースにそれを含めないことを決定し、次のマイナーまたはメジャーリリースに「punt」されます。

<!--
### Keeping the project board updated
-->

### プロジェクト・ボードを常に最新の状態に保つ

<!--
Since the project board will be a place that meetings reference and people bookmark, it’s important to take steps to keep it current and useful for others. The following actions are recommended and can be divided up:
-->

プロジェクトボードは、ミーティングで参照され人々がブックマークする場所となるため、情報を最新の状態に保ち、他の人にとって役立つようにすることが重要です。以下のアクションが推奨されます。分割することもできます:

<!--
*   The release leads, and members of the Gutenberg Triage Team should regularly review new [Gutenberg issues](https://github.com/WordPress/gutenberg/issues) and add those relevant to the current release to the project in the “Triage” column.
*   Sort items in “Todo” column by priority. Keep the highest priority items at the top so more people will see them. Issues with the `Regression` label should always be at the top. 
*   When an issue gets a PR associated, move the issue to the “In Progress” column and add the PR to the “In Review” column.
*   PRs associated with issues on the board also need to be added to the project board. 
*   Ensure all issues and PRs are properly labeled.
-->

*   リリースリードや Gutenberg トリアージチームのメンバーは、定期的に新しい [Gutenberg の issue](https://github.com/WordPress/gutenberg/issues) を確認し、現在のリリースに関連するものを「トリアージ」カラムのプロジェクトに追加してください。
*   「Todo」カラムの項目を優先度順にソートしてください。より多くの人に見てもらえるよう、優先度の高い項目を一番上に置いてください。`Regression` ラベルの付いた issue は常に一番上に来るようにします。
*   issue にプルリクエストが関連付けられたら、その issue を「In Progress」カラムに移動し、プルリクエストを「In Review」カラムに追加してください。
*   ボード上の issue に関連付けられているプルリクエストもプロジェクトボードに追加する必要があります。
*   すべての issue とプルリクエストに適切なラベルが付けられていることを確認してください。

<!--
Share the link to the project board regularly in the Editor Weekly Chat meetings and the [#core-editor](https://wordpress.slack.com/archives/C02QB2JS7) Slack channel as helpful. This will get people in the habit of checking the project board and for them to share it in turn. You can also encourage contributors with permission to add issues they think are important to the “Triage” column. The Editor Triage leads will handle it from there. 
-->

エディターウィークリーチャットミーティングや [#core-editor](https://wordpress.slack.com/archives/C02QB2JS7) Slack チャンネルで、プロジェクトボードへのリンクを定期的に共有します。これにより、人々はプロジェクトボードをチェックし、共有する習慣が身に付きます。また、許可を得て貢献者に、重要だと思う issue を「トリアージ」カラムに追加するよう促すこともできます。そこから先はエディタートリアージリードが対応します。

<!--
### Running asynchronous triage sessions
-->

### 非同期トリアージセッションの開催

<!--
During the Beta release cycle, the weekly triage sessions in the [#core-editor](https://wordpress.slack.com/archives/C02QB2JS7) Slack channel are suspended. They are replaced with asynchronous triage sessions to specifically handle the project board, especially the “Triage” and “In Discussion / Needs Decision” column. These meetings allow the Editor Tech and Triage leads to efficiently “vote” on how issues and PR should be prioritized and managed.
-->

ベータ版のリリースサイクル中、[#core-editor](https://wordpress.slack.com/archives/C02QB2JS7) Slack チャンネルでの毎週のトリアージセッションは中断されます。その代わりに、プロジェクトボード、特に「Triage」と「In Discussion / Needs Decision」カラムを特別に扱う非同期のトリアージセッションが行われます。これらのミーティングにより、エディターテックとトリアージリードは、issue とプルリクエストをどのように優先順位付けし、管理すべきかについて効率的に「投票」できます。

<!--
Often a release team consists of members across various time zones, so an asynchronous meeting allows everyone to participate when convenient. 
-->

多くの場合、リリースチームはさまざまなタイムゾーンにまたがるメンバーで構成されるため、非同期ミーティングであれば全員が都合の良いときに参加できます。

<!--
You create an initial announcement for the meeting in the [#core-editor](https://wordpress.slack.com/archives/C02QB2JS7) Slack channel and add each PR and issue in a thread. The leads then vote using emojis and can add additional comments in the thread. 
-->

最初のミーティングのお知らせを [#core-editor](https://wordpress.slack.com/archives/C02QB2JS7) Slack チャンネルに作成し、各プルリクエストと issue をスレッドに追加します。リードは絵文字を使って投票し、スレッドにコメントを追加できます。

<!--
These meetings are held publicly so all other contributors can see the decisions being made. Below is an example of a meeting for 6.3, but feel free to modify it as needed.
-->

これらのミーティングは、他のすべての貢献者が決定された内容を見ることができるように、公開で行われます。以下は6.3のミーティングの例ですが、必要に応じて自由に変更してください。

[![](https://make.wordpress.org/core/files/2023/08/async-triage-slack-1024x517.png)](https://make.wordpress.org/core/files/2023/08/async-triage-slack.png)

<!--
An example asynchronous triage session held during the WordPress 6.3 release cycle.
-->

WordPress 6.3のリリースサイクル中に開催された非同期トリアージセッションの例。

<!--
### Assigning tasks from the board
-->

### ボードからのタスクを割り当てる

<!--
For items in the “Todo” column, it’s recommended that you find someone assigned in time before the release milestones. The easiest way to do this is to ask in the [#core-editor](https://wordpress.slack.com/archives/C02QB2JS7) channel for volunteers to pick tasks from that column. If no one volunteers, you will need to research to find contributors familiar with the items needing help (checking previous Gutenberg PRs can be helpful here) and ask them if they can take on that work or help another person do so. 
-->

「To Do」欄の項目については、リリースのマイルストーンまでに割り当てられる人を見つけることをおすすめします。最も簡単な方法は、[#core-editor](https://wordpress.slack.com/archives/C02QB2JS7) チャンネルで、その欄のタスクを選んでくれるボランティアを募集することです。ボランティアとして参加できる人がいない場合は、助けが必要な項目に詳しい人を見つけて (ここでは、過去の Gutenberg プルリクエストを確認することも役に立ちます)、その人に引き受けてもらえるか、または他の人に手伝ってもらえるかをたずねる必要があるでしょう。

<!--
If issues seem critical to the release but nobody is picking them up, alert the Editor Tech Leads as soon as possible. 
-->

リリースにとって重要だと思われる issue があるにもかかわらず、誰もその issue を取り上げてない場合は、できるだけ早くエディターテックリードに知らせてください。

<!--
## Knowing which features to include in the release
-->

## どの機能をリリースに含めるべきかを考える

<!--
**Review [the release roadmap post](https://make.wordpress.org/core/2023/05/18/roadmap-to-6-3/) and recent Gutenberg [“What’s New”](https://make.wordpress.org/core/tag/gutenberg-new/) release posts to determine essential features.**
-->

**[リリースロードマップの投稿](https://make.wordpress.org/core/2023/05/18/roadmap-to-6-3/)と最近の[「What's New」](https://make.wordpress.org/core/tag/gutenberg-new/)リリース投稿をレビューし、重要な機能を決定します**。

<!--
The release roadmap post lists the features considered a top priority for each release. Special attention should be given to these to ensure they land in Core in a timely and stable manner.
-->

リリースロードマップの投稿には、各リリースで最優先とされる機能がリストアップされています。タイムリーで安定した方法でコアに取り込まれるよう、これらに特別な注意を払う必要があります。

<!--
It’s good to review Gutenberg release posts too. They will give you a sense of all the features currently being worked on, as well as smaller enhancements and bug fixes.
-->

Gutenberg のリリース投稿を確認することも良いでしょう。現在取り組んでいるすべての機能や、小さな機能強化、バグ修正などを知ることができます。

<!--
For experimental features in particular, it helps to ping the developers working on them and discuss whether they are ready to be included in Core.
-->

特に実験的な機能については、それらに取り組んでいる開発者に連絡し、コアに含める準備ができているかどうかを話し合うことが役立ちます。

<!--
### Deciding on additional features to include
-->

### 追加する機能を決定する

<!--
Outside of the main features of a release, there are often in progress additional features that are still helpful to include to help complement the release as a whole. This might include features that were missed in the last major release as well as simply more minor updates to include. Whether you can include these depends on various factors, including but not limited to the following:
-->

リリースの主な機能以外に、リリース全体を補完するために含めると便利な追加機能が進行中であることがよくあります。これには、前回のメジャーリリースで見落とされた機能だけでなく、単純にマイナーな機能やアップデートが含まれるかもしれません。これらを含めることができるかどうかは、以下のようなさまざまな要因によりますが、これらに限定されるものではありません:

<!--
*   What features might be important to finish? 
*   What is the complexity/risk of each feature? 
*   How complementary they are to the main features of the release.
*   Are there contributors actively working on the feature? 
-->

*   どのような機能を完成させることが重要か ?
*   各機能の複雑さとリスクは何か ?
*   リリースの主な機能をどのように補完するか。
*   その機能に積極的に取り組んでいる貢献者はいますか ?

<!--
For any feature you do decide to add, remember to add it to the release project board in GitHub. Do your best to help move these features along, whether through helping with PRs, unblocking the original authors, etc. 
-->

追加すると決めた機能については、必ず GitHub のリリースプロジェクトボードに追加してください。プルリクエストを手伝ったり、元の作成者のブロックを解除したりするなど、これらの機能を前進させるために最善を尽くしてください。

<!--
If there’s an additional feature you want to include that you don’t have anyone actively working on, please ask for volunteers in the [#core-editor](https://wordpress.slack.com/archives/C02QB2JS7) meetings. If you know of any developer who may be a good person to work on a given feature, it’s often best to ping them directly and ask if they can do so. Even if they can’t, they may be able to point you to someone who can.
-->

もしあなたが追加したい機能で、積極的に取り組んでいる人がいないものがあれば、[#core-editor](https://make.wordpress.org/core/tag/core-editor/) ミーティングでボランティアを募集してください。もしあなたが、ある機能に取り組むことに適した開発者を知っているなら、その開発者に連絡し、それが可能かどうかたずねることが良いでしょう。彼らができないとしても、できる人を紹介してくれるかもしれません。

<!--
### How to handle removing features
-->

### 機能を削除するときの対処法

<!--
As with any release, there will be tough calls that must be made. What follows are the best steps you can take to communicate effectively and, if needed, make the call to not include a feature in a release:
-->

どのようなリリースでもそうですが、厳しい決断を迫られることがあります。以下は、効果的なコミュニケーションを行い、必要であればリリースにその機能を含めないという決断を下すための最善のステップです:

<!--
*   Communicate as early as you can with the people working on the feature that it is at risk of not being included and clearly state what needs to be done by when in order to change that. 
*   Give updates to the release squad as things do or do not progress alongside updates in [#core-editor](https://wordpress.slack.com/archives/C02QB2JS7) meetings. 
*   If you decide to remove a feature, please write a post on Make Core announcing the final decision. [Here’s an example from a past release](https://make.wordpress.org/core/2020/02/07/navigation-block-exclusion-from-wp-5-4/). 
-->

*   その機能に取り組んでいる人々に、その機能が含まれないリスクがあることをできるだけ早く伝え、それを変更するにはいつまでに何をする必要があるかを明確に示す。
*   [#core-editor](https://make.wordpress.org/core/tag/core-editor/) ミーティングでのアップデートと並行して、進捗があった場合やなかった場合のアップデートをリリースチームに伝える。
*   機能の削除が決定された場合、Make Core に最終決定を知らせる記事を書いてください。[これは過去のリリースの例です](https://make.wordpress.org/core/2020/02/07/navigation-block-exclusion-from-wp-5-4/)。

<!--
The key is clear, timely communication so all involved (contributors, release squad members, etc) can prepare appropriately.
-->

これらすべてにおいて重要なことは、すべての関係者 (貢献者、リリースチームのメンバーなど) が適切な準備ができるように、明確でタイムリーなコミュニケーションをとることです。

<!--
## Experimental API management
-->

## 実験的 API の管理

<!--
Since the [private-apis](https://github.com/WordPress/gutenberg/tree/trunk/packages/private-apis) system was created in early 2023, the system for managing experimental APIs has changed. Everything that is unstable or not meant to be available as a public API is kept private.
-->

2023年初頭に [private-apis](https://github.com/WordPress/gutenberg/tree/trunk/packages/private-apis) システムが作成されて以来、実験的 API を管理するシステムが変更され、安定していないものや公開 API として利用する予定のないものはすべて非公開となりました。

<!--
However, there are still many older experimental APIs in Gutenberg that can be recognized by the `__experimental` prefix. These can be functions, properties, or variables found throughout the codebase. For every release, it’s customary to audit these and check if any are ready for stabilization. Stabilization must be done before the Beta 1 release (ideally at least two weeks beforehand), as renames during the Beta phase are not possible.
-->

しかし、Gutenberg にはまだ多くの古い実験的 API が残っており、接頭辞が `__experimental` であることで見分けることができます。これらは関数、プロパティ、変数であり、コードベースのいたるところにあります。リリースのたびに、これらの API を監査し、安定化の準備ができているかどうかをチェックすることが通例です。ベータフェーズでは名前の変更ができないため、最初のベータ1リリースの前 (理想的には少なくとも2週間前) に安定化を行うことが重要です。

<!--
### How to run the audit
-->

### 精査する方法

<!--
Generally speaking, the process is as follows:
-->

一般的には、以下のような流れになります:

<!--
*   Use the script below for auditing experimental APIs
*   [Use git blame](https://docs.github.com/en/free-pro-team@latest/github/managing-files-in-a-repository/tracking-changes-in-a-file) to identify who was involved with each API
*   Create an overview issue in GitHub tracking each experimental API pinging those involved to decide whether an API needs to be stabilized ([example from 6.2](https://github.com/WordPress/gutenberg/issues/47196)).
-->

*   以下のスクリプトを使って実験的 API を精査する
*   [git blame を使って](https://docs.github.com/en/free-pro-team@latest/github/managing-files-in-a-repository/tracking-changes-in-a-file)各 API に誰が関わったかを特定する
*   各実験的 API を追跡するために、GitHub で概要の issue を作成し、API を安定化させる必要があるかどうかを決定するために関係者に通知する ([6.2の例](https://github.com/WordPress/gutenberg/issues/47196))。

<!--
To get started, here’s a script to use to begin auditing the experimental APIs:
-->

まず、実験的 API の精査を開始するために使用するスクリプトを次に示します:

[https://raw.githubusercontent.com/WordPress/gutenberg/trunk/bin/list-experimental-api-matches.sh](https://raw.githubusercontent.com/WordPress/gutenberg/trunk/bin/list-experimental-api-matches.sh)

<!--
It can help to group related experimental APIs from the report and any information manually collected to get a sense of what’s currently in place. From there, use git blame to know which contributors were involved in each API to ping them and inquire if the API can be stabilized. You can then create a new overview issue in GitHub that lists out a checkbox for each API where you can easily see whether a decision has been made around stabilizing the API.
-->

レポートや手動で収集した情報から、関連する実験的な API をグループ化し、現在何があるのかを把握できます。そこから git blame を使って、それぞれの API にどの貢献者が関わっているかを把握し、API を安定できるかどうかを確認します。そして GitHub に新しい概要の issue を作成し、各 API のチェックボックスをリストアップすれば、API の安定化に関する決定が行われたかどうかを簡単に確認できます。

<!--
## Planning and writing dev notes
-->

### 開発者ノートの計画と執筆

<!--
*Check out* [*this handbook page*](https://make.wordpress.org/core/handbook/tutorials/writing-developer-notes/) *for more context on dev note best practices.*
-->

**開発者ノートのベストプラクティスに関するより詳しい情報は、[このハンドブックのページ](https://ja.wordpress.org/team/handbook/core/tutorials/writing-developer-notes/)をチェックしてください。**

<!--
You can check all PRs labeled with [`Needs Dev Note`](https://github.com/WordPress/gutenberg/issues?q=label%3A%22Needs+Dev+Note%22.) to know what needs a dev note. You might find that there are more PRs than you can feasibly write individual posts for without overwhelming the community with information. In this case, group PRs with the same label and propose a dev note for each group.
-->

開発者ノートが必要なものを知るために、[`Needs Dev Note`](https://github.com/WordPress/gutenberg/issues?q=label%3A%22Needs+Dev+Note%22.) というラベルのついたすべてのプルリクエストをチェックできます。個々の投稿を書くことでコミュニティを情報で圧倒してしまうほど、多くのプルリクエストがあることに気付くかもしれません。このような場合、プルリクエストを同じラベルでグループ化し、グループごとに開発者ノートを提案します。

<!--
Once you have a sense of the needed dev notes, create a GitHub issue ([previous example](https://github.com/WordPress/gutenberg/issues/20185)) detailing the plan: 
-->

必要な開発者ノートの種類がわかったら、GitHub の issue ([以前の例](https://github.com/WordPress/gutenberg/issues/20185)) に計画を詳細に記述します:

<!--
*   What posts need to be done 
*   What are the essential sections of each post
*   What PRs should be included in each 
-->

*   どのような記事が必要か
*   各投稿の重要なセクションは何か
*   それぞれの記事にどのようなプルリクエストを入れるべきか

<!--
When doing so, ping the people with PRs needing dev notes to contribute to this effort. Ideally, your job should be to wrangle the updates from each PR author and plan the timeline for sharing each dev note so that you don’t share too many in a short time. Sharing target dates is recommended to help space out and plan appropriately. 
-->

その際、開発者ノートが必要なプルリクエストを持っている人たちに、作業に取り組むよう通知してください。あなたの理想的な仕事は、それぞれのプルリクエストの作成者からのアップデートを取りまとめ、各開発者ノートを共有するタイムラインを計画し、短期間にあまりにも多くの開発者ノートを共有しないようにすることです。適切な間隔と計画を立てるために、目標日を共有することをおすすめします。

<!--
Keep in mind that dev notes are extremely collaborative efforts requiring help from many people. This might mean that some people you need information from didn’t see the ping the first time or are unavailable to write a note. It’s okay and expected that follow-up will be required, likely in the form of additional pings or even DMs in Slack to get updates. When each section is done for each dev note, you can check the checkbox to show progress and help others see what’s left. 
-->

開発者ノートは共同作業であり、多くの異なる人々の助けが必要であることに注意してください。これは、あなたが情報を必要としている人の中には、最初の通知を見逃したり、ノートを書く時間がなかったりする人がいることを意味するかもしれません。追加の通知や Slack のダイレクトメールなどの形で、最新情報を入手するためのフォローアップが必要になるかもしれません。各開発者ノートの各セクションを書き終わったら、チェックボックスにチェックを入れて進捗を表示し、他の人が残りの内容を確認できるようにします。

<!--
As you compile each dev note, particularly if you combine multiple PRs into one dev note, ensure you share the posts with those involved for review so everyone is on the same page. Once there’s consensus, share the dev notes with those involved in the major release squad for a final review. 
-->

各開発者ノートをまとめる際、特に複数のプルリクエストを1つの開発者ノートにまとめる場合は、レビューのために関係者と投稿を共有して、全員が同じ認識を持つようにしてください。。そこで合意が得られたら、その開発者ノートをメジャーリリースチームの関係者と共有して、最終的なレビューを受けるようにしてください。

<!--
## General triage management
-->

## 一般的なトリアージ管理

<!--
### Routine triage
-->

### 定期的なトリアージ

<!--
Because months pass between Core releases, it’s important to regularly check in on GitHub to triage issues (ideally weekly), particularly new ones that are unlabeled. The key is not to miss anything that might be critical. 
-->

コアリリースの間に数ヵ月が経過するため、GitHub で定期的に (理想的には毎週)、特にラベルのない新しい issue をトリアージすることが重要です。ポイントは、重大かもしれないものを見逃さないことです。

<!--
### Release-specific triage
-->

### リリース固有のトリアージ

<!--
Outside of reviewing unlabeled issues, it’s important to review all reported issues since a major release occurred to spot any critical issues that need to be resolved. While this is primarily the job of the Editor Triage Leads, this is a great task to divide up among other contributors. 
-->

ラベルのない issue をレビューすること以外では、解決すべき重要な issue を見つけるために、メジャーリリース以降に報告されたすべての issue を時間をかけてレビューすることが重要です。これは主にエディタートリアージリードの仕事ですが、他の貢献者に分担させることもできるすばらしいタスクです。

<!--
### Determining how critical a bug is
-->

### バグがどの程度重大かを判断する

<!--
When reviewing bug reports and trying to determine how critical they are, it becomes even more important to know the version that introduced the particular bug. For example, you might find a bug introduced many WordPress versions ago, but it doesn’t have many recent comments. This is a good sign that the bug is not critical to fix. 
-->

バグレポートを確認し、それがどの程度重大なものかを判断しようとする場合、特定のバグが導入されたバージョンを知ることがさらに重要になります。たとえば、WordPress の多くのコアバージョンで導入されたものの、コメントがあまりないバグを見つけるかもしれません。これは、そのバグが本当に修正すべき重要なものではないという良い兆候です。

<!--
After the first Beta, you can only include bug fixes for issues that regressed during the Alpha phase. It’s essential to know if the bug you are reviewing affects the latest stable release of WordPress. This might require multiple testing environments with different setups to determine the impact, for example, the current version of WordPress, the Beta version, and the latest version of Gutenberg. It might also mean following up with those who reported issues to get more information about their particular setup, like if they are using Gutenberg and, if so, what version.
-->

最初のベータ版の後は、アルファフェーズでリグレッションを起こした問題のバグ修正のみを含めることができるため、レビューしているバグが WordPress の最新の安定リリースに影響するかどうかを知ることが重要です。影響を判断するために、異なるセットアップで複数のテスト環境を用意する必要があるかもしれません。たとえば、WordPress の現行バージョン、ベータバージョン、Gutenberg の最新バージョンです。また、問題を報告した人をフォローアップして、Gutenberg を使用しているかどうか、使用している場合はどのバージョンかなど、特定の設定に関する詳細な情報を得る必要があるかもしれません。

<!--
## Managing the first WordPress Beta release
-->

## 最初の WordPress ベータリリースの管理

<!--
**Beta 1 is a very significant deadline.** 
-->

### 最初のベータ版は非常に重要な期限です

<!--
No additional features or enhancements can be included after this milestone. Exceptions for enhancements to new features can be made, but these must be discussed with the release team. If approved, a Trac ticket should be created for each feature with the type “task (blessed)”. All enhancements to these tasks must be finished before RC1.
-->

最初のベータ版マイルストーン以降は追加機能や拡張機能を含めることができません。新機能の拡張には例外を設けることができます。これらについてはリリースチームと話し合う必要があり、承認された場合は、機能ごとに「task (blessed)」タイプの Trac チケットを作成する必要があります。これらのタスクに対するすべての機能強化は、RC1よりも前に完了する必要があります。

<!--
**To make the Beta 1 release process easier, start updating trunk as early as possible.**
-->

### ベータ1のリリースプロセスを容易にするため、できるだけ早く trunk の更新を開始してください

<!--
As the volume of changes for each release is quite high, it helps to start adding new features to Core trunk as early as possible in the cycle. This means both updating the `@wordpress` npm packages used by Core and manually syncing any PHP changes from the `lib` and `phpunit` folders in Gutenberg.
-->

各リリースの変更の量は非常に多いため、サイクルのできるだけ早い段階でコア trunk に新機能の追加を開始することが役立ちます。これは、コアによって使用される `@wordpress` npm パッケージを更新することと、Gutenberg の `lib` フォルダーと `phpunit` フォルダーから PHP の変更を手動で同期することの両方を意味します。

<!--
**Make sure any experimental features are behind feature flags in Gutenberg, so they don’t accidentally get included in Core.**
-->

### 実験的な機能が誤ってコアに含まれないように、Gutenberg の機能フラグによって管理されていることを確認してください

<!--
In order to safely update the npm packages in Core, experimental Gutenberg features that aren’t slated for inclusion in Core must be safely behind feature flags. `IS_GUTENBERG_PLUGIN` flag is commonly used for this purpose, or a specific feature filter may be used, such as in [this example](https://github.com/WordPress/gutenberg/pull/52579) for the interactivity API.
-->

コアの npm パッケージを安全に更新するには、コアに含める予定のない実験的な Gutenberg 機能を機能フラグから隠す必要があります。この目的のために `IS_GUTENBERG_PLUGIN` フラグが一般的に使用されます。またはインタラクティビティ API の[この例](https://github.com/WordPress/gutenberg/pull/52579)のように、特定の機能フィルターが使用される場合もあります。

<!--
**List PHP changes to be manually synced.**
-->

### 手動で同期する PHP の変更をリストアップする

<!--
Create an overview issue of all the changes from the `lib` and `phpunit` folders that need to be manually synced. Using git blame, find the authors of those changes and ping them to create Core PRs for each change.
-->

手動で同期する必要がある `lib` フォルダーと `phpunit` フォルダーから、すべての変更に関する概要の issue を作成します。`git blame` を使用して、それらの変更の作成者を見つけて通知し、それらの変更のコアプルリクエストを作成します。

<!--
The PHP files in `block-library` package don’t need to be manually synced, as they are auto-generated in Core based on the npm package.
-->

`block-library` パッケージ内の PHP ファイルは、npm パッケージにもとづいてコアで自動生成されるため、手動で同期する必要はありません。

<!--
## Managing weekly Beta and RC releases
-->

## ウィークリーベータ版と RC リリースの管理

<!--
After the first Beta, there are weekly Beta releases leading up to the Release Candidate (RC). At this point, there are three main tasks to take care of: triage new issues, cherry-pick PRs for inclusion in the release, and update both package and Core paths.
-->

最初のベータ版の後、リリース候補 (RC) に至るまで毎週ベータ版がリリースされます。この時点では、新しい issue のトリアージ、リリースに含めるプルリクエストのチェリーピック、パッケージとコアパスの更新という3つの主なタスクがあります。

<!--
### Triaging new issues
-->

### 新しい issue のトリアージ

<!--
Throughout the week, you should closely monitor all new Gutenberg issues since the last release to ensure no regressions have been found. If you identify regressions, immediately add those issues to the “WordPress X.X Editor Tasks” project board in the “Triage” column for further investigation. 
-->

その週を通して、前回のリリース以降に提出された新しい Gutenberg の issue をすべて注意深く監視し、リグレッションが見つかっていないことを確認してください。もしリグレッションを発見した場合は、すぐに「WordPress X.X Editor Tasks」プロジェクトボードの「Triage」欄にその issue を追加し、さらに調査を進めてください。

<!--
When PRs are submitted for issues on the project board, add the `Backport to WP Beta/RC` label to the PR so you can track what needs to be included in the next Beta release. 
-->

プロジェクトボードにある issue に対してプルリクエストが提出されたら、その issue に `Backport to WP Beta/RC` というラベルを追加して、次のベータリリースに何を含めるべきかを追跡できるようにしてください。

<!--
Outside of looking for issues that need to be added to the project board, it’s important to ensure all issues on the board are assigned to someone to resolve, especially with Beta releases occurring on a weekly schedule.
-->

プロジェクトボードに追加する必要のある issue を探すこと以外に、特に毎週のスケジュールで行われるベータリリースの場合、ボード上のすべての issue が、解決されるために誰かに割り当てられていることを確認することが重要です。

<!--
### Cherry-picking PRs for release
-->

### リリース用プルリクエストのチェリーピックについて

<!--
Once PRs on the project board are completed, they must be backported into the Core to be available on the next Beta or RC version. Follow this process:
-->

プロジェクトボード上のプルリクエストが完了したら、次のベータ版または RC 版で利用できるように、コアにバックポートする必要があります。次の手順に従ってください:

<!--
*   If a `wp/x.x` (use the correct WordPress release number) has yet to be created, create it and push it to the remote repository.
*   Review all PRs labeled [`Backport to WP Beta/RC`](https://github.com/WordPress/gutenberg/pulls?q=label%3A%22Backport+to+WP+Core%22+sort%3Acreated-desc+). Verify that everything looks good and that the PRs are not “too risky” to go into a Core release. Refer to the Editor Tech Leads and Core Tech Leads for guidance.
*   Remove the label from any PRs that were closed without merging. Otherwise, they’ll mess with the automated cherry-pick script.
*   Create a branch based on the format of `wp/x.x`
*   Cherry-pick each PR into the newly created branch.
    *   There is [cherry-picking automation](https://developer.wordpress.org/block-editor/contributors/code/release/auto-cherry-picking/) available via `npm run other:cherry-pick`. It finds all merged PRs with the `Backport to WP Beta/RC` label, cherry-picks them, and asks whether to automatically comment on the relevant PRs and push the branch to GitHub. You can also pass another label as the first argument.
    *   You can also do it manually. The hash of the commit is extracted from the GitHub pull request page. To avoid merge conflicts, cherry-pick the commits in the same order they were made in trunk. The order will likely not be the same as the PRs appear in the label view, so double-check the merge date and refer to the [commit history](https://github.com/WordPress/gutenberg/commits/master). You can combine multiple commits in a single command, like so: `git cherry-pick c82094d8389b1756f05d4079ba98e4ee25961502 && git cherry-pick 548e600f14924d7fcfdb5250f45f718d3759d022 && git cherry-pick b72b41e27f008540410c45023b655c8ee20b67ae`
*   Merge conflicts may still happen. If they do, you will have to resolve them. If you need help with this, message the PR author for assistance.
*   Sometimes a conflict happens because the cherry-picked commit depends on another commit that wasn’t included in the release branch. This may be an accidental omission, so it’s good to double-check by pinging the authors of the PRs.
*   After manually solving a conflict, return to the original PR and remove the `Backport to WP Beta/RC` label.
*   Create a pull request on GitHub from the branch you created into the `wp/x.x` branch.
*   Verify that continuous integration is executed with success for the PR.
*   If there were merge conflicts to solve, you should ping the authors of the conflicting commits to double-check they were solved correctly. Otherwise, if all tests pass on CI, merging the PR to the release branch is fine.
*   After merging, run the package publish task from the release branch:
    *   On [this page](https://github.com/WordPress/gutenberg/actions/workflows/publish-npm-packages.yml), click the “Run workflow” button and choose the release branch. The release type should be `wp`, and the release version should be added underneath.
    *   Once the workflow appears in the list below, click through to authorize it. If you don’t have `gutenberg-core` access, ask someone who does to approve it for you.
    *   This workflow will publish the npm packages with a dist tag corresponding to the release, which can then be used to select the correct package versions in Core.
-->

*   `wp/x.x` (正しい WP リリース番号を使用してください) がまだ作成されていない場合は、作成してリモートリポジトリにプッシュしてください。
*   [Backport to WP Beta/RC](https://github.com/WordPress/gutenberg/pulls?q=label%3A%22Backport+to+WP+Core%22+sort%3Acreated-desc+) というラベルがついたプルリクエストをすべてレビューしてください。すべてが期待通りかどうか、プルリクエストがコアリリースに入ることが「リスク」ではないかどうかを確認します。ガイダンスについては、エディターテックリードとコアテックリードに確認してください。
*   マージされずにクローズされたプルリクエストからラベルを削除します。そうしないと、自動チェリーピックスクリプトを混乱させることになります。
*   `wp/x.x` の形式にもとづいてブランチを作成します。
*   各プルリクエストを新しく作成したブランチにチェリーピックします。
    *   [チェリーピックの自動化](https://developer.wordpress.org/block-editor/contributors/code/release/auto-cherry-picking/)が `npm run cherry-pick` によって利用できます。これは、`Backport to WP Beta/RC` ラベルのついたすべてのマージされたプルリクエストを見つけ、それらをチェリーピックし、関連するプルリクエストに自動的にコメントし、ブランチを GitHub にプッシュするかどうかを尋ねます。第一引数に別のラベルを渡すこともできます。
    *   手動で行うこともできます。コミットのハッシュは GitHub のプルリクエストページから抽出できます。マージのコンフリクトを避けるためには、trunk で行われたのと同じ順番でコミットをチェリーピックすることが重要です。これは、ラベルビューに表示される順番と同じではない可能性が高いので、マージされた日付を再確認し、必要に応じて[コミット履歴](https://github.com/WordPress/gutenberg/commits/master)を参照します。複数のコミットを、このようにひとつのコマンドにまとめることもできます: `git cherry-pick c82094d8389b1756f05d4079ba98e4ee25961502 && git cherry-pick 548e600f14924d7fcfdb5250f45f718d3759d022 && git cherry-pick b72b41e27f008540410c45023b655c8ee20b67ae`
*   マージはコンフリクトする場合があります。もしコンフリクトが起きたら、それを解決しなければなりません。もしサポートが必要であれば、プルリクエストの作者にメッセージを送ってください。
*   チェリーピックされたコミットが、リリースブランチに含まれていない別のコミットに依存しているためにコンフリクトが起こることがあります。これは意図されたものではないかもしれないため、プルリクエストの作者に連絡して再確認することをおすすめします。
*   手動でコンフリクトを解決した後、元のプルリクエストに戻り、`Backport to WP Beta/RC` ラベルを削除してください。
*   GitHub で、作成したブランチから `wp/x.x` ブランチにプルリクエストを作成します。
*   プルリクエストの継続的インテグレーションが成功したことを確認します。
*   解決すべきマージコンフリクトがある場合は、競合しているコミットの作成者に連絡し、それらが正しく解決されたことを再確認することをおすすめします。それ以外の場合、すべてのテストが CI で合格した場合は、プルリクエストをリリースブランチにマージしても問題ありません。
*   マージ後、リリースブランチからパッケージ公開タスクを実行します:
    *    [このページ](https://github.com/WordPress/gutenberg/actions/workflows/publish-npm-packages.yml)で、「Run workflow」ボタンをクリックし、リリースブランチを選択します。リリースタイプは `wp` で、その下にリリースバージョンが追加されます。
    *   ワークフローが下のリストに表示されたら、クリックして承認します。`gutenberg-core` へのアクセス権を持っていない場合は、アクセス権を持っている人に承認を依頼してください。
    *   このワークフローは、リリースに対応する dist タグを持つ npm パッケージを公開します。これは、コアで正しいパッケージバージョンを選択するために使用できます。

<!--
### Package updates and Core patches
-->

### パッケージの更新とコアパッチ

<!--
*   Once the npm packages are published, they can be updated in the `wp-develop` repo using the automated script: `npm run sync-gutenberg-packages -- --dist-tag=wp-<VERSION>`. Remember to use the same dist-tag as the newly released `@wordpress` packages, e.g. `wp-6.2` for the 6.2 major version.
*   Then run `npm run postsync-gutenberg-packages` in the `wordpress-develop` folder. It includes any new Gutenberg blocks in Core and runs the required builds.
*   If any new front-end scripts have been added to dynamic blocks, these need to be referenced manually in the [webpack block config](https://github.com/WordPress/wordpress-develop/blob/trunk/tools/webpack/blocks.js#L67).
*   After running both sync and postsync tasks, verify that the correct files have been updated for any blocks with changes to their PHP or block.json files and that files have been generated for any brand new blocks.
*   In your local WordPress development environment, check that the issues that were supposed to be resolved are in fact resolved.
*   Create a [Trac](https://core.trac.wordpress.org/) ticket for the package updates in Core.
*   Submit a PR against `wordpress-develop` to ensure the continuous integration tests pass, and add the Trac ticket number to the description. This ensures the PR gets linked to the ticket, and the patch will then be created automatically ([previous example](https://github.com/WordPress/wordpress-develop/pull/2564)).
*   Ask for reviews. During the Beta stage, a review is recommended but not mandatory. A double signoff by two different committers is required during the RC process. If you are a committer and are confident with the changes, you can be one of the approvers and add the “dev-feedback” keyword.
*   When approved, commit the patch or coordinate with a committer to ensure it’s committed if you are not a committer.
*   If a branch for the WordPress release already exists, backporting the commit from trunk to the release branch is required.
-->

*   npm パッケージが公開されると、自動化スクリプトを使用して `wp-develop` リポジトリで更新できます: `npm run sync-gutenberg-packages -- --dist-tag=wp-<VERSION>`。新しくリリースされた `@wordpress` パッケージと同じ dist-tag を使用することを忘れないでください。たとえば、`wp-6.2` はメジャーバージョン6.2です。
*   次に、`wordpress-develop` フォルダーで `npm run postsync-gutenberg-packages` を実行します。新しい Gutenberg ブロックがコアに含まれ、必要なビルドが実行されます。
*   動的ブロックに新しいフロントエンドスクリプトが追加された場合は、[webpack block config](https://github.com/WordPress/wordpress-develop/blob/trunk/tools/webpack/blocks.js#L67) の参照に手動で追加する必要があります。
*   sync タスクと postsync タスクの両方を実行した後、PHP ファイルや block.json ファイルに変更があったブロックについて正しいファイルが更新されたこと、および新規ブロックについてファイルが生成されたことを確認します。
*   ローカルの WordPress 開発環境で、解決されるはずの問題が実際に解決されていることを確認します。
*   コアのパッケージを更新するために [Trac](https://core.trac.wordpress.org/) チケットを作成します。
*   `wordpress-develop` に対してプルリクエストを提出し、継続的インテグレーションのテストがパスしたことを確認し、説明に Trac のチケット番号を追加します。これにより、プルリクエストがチケットにリンクされ、パッチが自動的に作成されます ([以前の例](https://github.com/WordPress/wordpress-develop/pull/2564))。
*   レビューを依頼します。ベータ版のフェーズでは、レビューは推奨されますが必須ではありません。RC プロセスでは、2人のコミッターによるダブルチェックが必要です。もしあなたがコミッターで、その変更に自信があるなら、承認者の一人として「dev-feedback」キーワードを追加してください。
*   承認されたら、パッチをコミットするか、コミッターでない場合はコミッターと調整してコミットされるようにしてください。
*   WordPress リリースのブランチがすでに存在する場合は、trunk からリリースブランチへのコミットのバックポートが必要です。

[#core-editor](https://make.wordpress.org/core/tag/core-editor/)
