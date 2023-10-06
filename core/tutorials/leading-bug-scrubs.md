<!--
# Leading Bug Scrubs
-->

# バグスクラブを実施する

<!--
Ensuring tickets move towards a resolution is one of the most important aspects of maintaining the WordPress project. Bug Scrubs serve as one of the ways to make this happen.
-->

チケットを解決に向けて確実に進めることは、WordPress プロジェクトを維持するうえで最も重要なことの一つです。バグスクラブはこれを実現するための方法のひとつです。

<!--
Bug Scrubs can have a general focus, focus on a specific component, or focus on a specific report (such as ancient tickets).
-->

バグスクラブには、一般的なもの、特定のコンポーネントに焦点を当てたもの、特定のレポート (古いチケットなど) に焦点を当てたものなどがあります。

<!--
Want to learn more? Here is a list of “Potentially Asked Questions”.
-->

もっと詳しく知りたいですか ? こちらが「よくある質問」のリストです。

<!--
### Who can run a Bug Scrub?
-->

### バグスクラブを実施できるのは誰ですか ?

<!--
You! Leading a Bug Scrub is something any interested community member can do.
-->

あなたです ! バグスクラブをリードすることは、興味のあるコミュニティメンバーであれば誰でも行うことができます。

<!--
### What is a Bug Scrub?
-->

### バグスクラブとは何ですか ?

<!--
Bug Scrubs are set and announced meetings where the goal is to go through a list of tickets and move them towards a resolution. They are also something where anyone is welcome to run them!
-->

バグスクラブとは、チケットのリストに目を通し、解決に向けて進めることを目的として設定・告知されたミーティングです。また、誰でも開催できるミーティングでもあります !

<!--
### Where do I get a list of tickets for my Bug Scrub?
-->

### バグスクラブのチケットリストはどこで入手できますか ?

<!--
There are many [pre-generated reports](https://make.wordpress.org/core/reports/) that you can use, such as:
-->

次のような、[事前に生成されたレポート](https://make.wordpress.org/core/reports/)が多数あります:

<!--
*   specific component reports such as for [Bootstrap/Load](https://core.trac.wordpress.org/component/Bootstrap/Load)
*   focus oriented ones such as for [JavaScript](https://core.trac.wordpress.org/focus/javascript)
*   [all tickets requesting dev feedback](https://core.trac.wordpress.org/tickets/dev-feedback)
-->

*   [Bootstrap/Load](https://core.trac.wordpress.org/component/Bootstrap/Load)などの特定のコンポーネントに関するレポート
*   [JavaScript](https://core.trac.wordpress.org/focus/javascript) などのフォーカス指向のもの
*   [開発者のフィードバックをリクエストするすべてのチケット](https://core.trac.wordpress.org/tickets/dev-feedback)

<!--
You can also create a custom query. For example, here’s one for [defects discussed during the last cycle that don’t have a resolution yet](https://core.trac.wordpress.org/query?status=accepted&status=assigned&status=new&status=reopened&status=reviewing&changetime=04%2F12%2F16..08%2F16%2F16&type=defect+(bug)&col=id&col=summary&col=status&col=owner&col=type&col=priority&col=milestone&order=priority).
-->

カスタムクエリーも作成できます。たとえば、これは[前回のサイクルで議論されたまだ解決していない不具合](https://core.trac.wordpress.org/query?status=accepted&status=assigned&status=new&status=reopened&status=reviewing&changetime=04%2F12%2F16..08%2F16%2F16&type=defect+(bug)&col=id&col=summary&col=status&col=owner&col=type&col=priority&col=milestone&order=priority)に関するものです。

<!--
### What does it mean to move tickets towards a resolution?
-->

### 解決に向けてチケットを動かすとはどういう意味ですか ?

<!--
There are a number of possible resolutions to a ticket. Moving a ticket towards a resolution might involve:
-->

チケットにはさまざまな解決方法があります。チケットを解決に向けて進めるためには、以下のようなことが考えられます:

<!--
*   Pinging a specific person for feedback/information
*   Reviewing a patch and providing feedback on it
*   Adding a new keyword to a ticket
-->

*   特定の人にフィードバック/情報を送る
*   パッチをレビューし、それに対するフィードバックを提供する
*   チケットに新しいキーワードを追加する

<!--
Almost always, it should include a summary of the discussion.
-->

ほとんどの場合、チケットには議論の要約を含めるべきです。

<!--
### How many tickets should be reviewed in a Bug Scrub?
-->

### バグスクラブではどれだけのチケットをレビューする必要がありますか ?

<!--
There is no magic number for Bug Scrubs. It is entirely up to the organizers.
-->

バグスクラブにマジックナンバーはありません。それは主催者次第です。

<!--
Bug Scrubs work best when they have a specific end goal. This may be a number of tickets or this may be a time period. Generally, 1 hour is a good amount of time and no more than 5 minutes is enough for each ticket.
-->

バグスクラブは、特定の最終目標があるときですに最も効果的に機能します。これはチケットの数かもしれないし、時間かもしれません。一般的には、1時間は十分な時間であり、1枚のチケットにかかる時間は5分以内で十分です。

<!--
### How do I run a Bug Scrub?
-->

### バグスクラブはどのように行うのですか ?

<!--
Let’s walk through the steps:
-->

手順を見ていきましょう:

<!--
1.  At the start of the scrub, you should:
    *   Announce it by opening the Bug Scrub `<bug-scrub>` tag and welcoming people
    *   Then link to the list of tickets you will be going through. This list should either be a pre-existing report on Trac or a query that you generate.
2.  Then post the first ticket for discussion. Make sure to mention it via number or a link so that slack auto posts a link so someone can see this ticket was discussed.
3.  Then take a moment to review the ticket and discuss what it needs to move forward. You may call for volunteers for specific tasks.
    *   Tip: Sometimes cutting off discussion and moving it back to the ticket with some summary of thoughts makes the most sense. That’s a decision you need to make, though anyone should feel free to suggest it.
4.  Finally, make sure one person is responsible for updating the ticket with whatever decision is made.
5.  Repeat steps 2-4 for the next ticket on the list.
6.  When done, make sure to close `</bug-scrub>` and thank everyone who helped.
-->

1.  スクラブをはじめるときには、以下のことを行ってください:
    *   バグスクラブ `<bug-scrub>` タグを開いて告知し、参加者を歓迎します。
    *   その後、取り組むチケットリストにリンクします。このリストは Trac にある既存のレポートか、あなたが作成したクエリーであるべきです。
2.  次に、議論のための最初のチケットを投稿してください。Slack がリンクを自動的に投稿して、このチケットが議論されたことを誰かが確認できるようにするために、必ず番号またはリンクで言及でメンションしてください。
3.  その後、少し時間をとってチケットを確認し、次に進むために何が必要かについて話し合います。特定のタスクについてボランティアを募集してもよいでしょう。
    *   ヒント: 場合によっては議論を打ち切り、考えをまとめてチケットに戻すことが最も合理的です。それはあなたが決める必要がありますが、誰でも自由に提案できます。
4.  最後に、どのような決定が下されたとしても、チケットの更新を誰か一人が責任をもって行うようにしましょう。
5.  リストの次のチケットに対して、手順2-4を繰り返します。
6.  完了したら、必ず `</bug-scrub>` で閉じ、手伝ってくれた人全員に感謝します。

<!--
### What do I need to organize a Bug Scrub?
-->

### バグスクラブを実施するには何が必要ですか ?

<!--
You’ll need:
-->

必要なもの:

<!--
*   An internet connection
*   An account on both WordPress.org and [wordpress.slack.com](https://wordpress.slack.com/) ( which you can get through [https://make.wordpress.org/chat/](https://make.wordpress.org/chat/) with your WordPress.org account)
*   A willingness to devote some time to help WordPress 
-->

*   インターネット接続
*   WordPress.org と [wordpress.slack.com](https://wordpress.slack.com/) の両方のアカウント (WordPress.org のアカウントで [https://make.wordpress.org/chat/](https://make.wordpress.org/chat/) から取得できます)
*   WordPress を支援するために時間を割く意欲があること

<!--
You don’t need to be:
-->

次のようなものは必要ありません:

<!--
*   A core committer or someone that would be called a “core dev” (whatever that means) to lead a Bug Scrub.
*   A developer at all. Designers, project managers, QA engineers, and product managers can be great Bug Scrub leaders.
-->

*   コアコミッターや「コア開発者」と呼ばれる人。
*   開発者である必要はありません。デザイナー、プロジェクトマネージャー、QA エンジニア、プロダクトマネージャーは優れたバグスクラブリーダーになることができます。

<!--
People that are successful at running Bug Scrubs are people that can communicate well and are familiar with [the trac workflow](https://make.wordpress.org/core/handbook/contribute/trac/) and [how WordPress uses keywords on trac](https://make.wordpress.org/core/handbook/contribute/trac/keywords/).
-->

バグスクラブの運営で成功する人は、コミュニケーションがうまく、[trac のワークフロー](https://ja.wordpress.org/team/handbook/core/contribute/trac/)や [WordPress が trac 上でどのようにキーワードを使うか](https://ja.wordpress.org/team/handbook/core/contribute/trac/keywords/) について精通している人です。

<!--
Running a Bug Scrub involves [Bug Gardening](https://make.wordpress.org/core/handbook/testing/bug-gardening/), so a tester mindset and understanding users helps as well.
-->

バグスクラブの運営には[バグガーデニング](https://ja.wordpress.org/team/handbook/core/testing/bug-gardening/)が含まれるため、テスターとしての考え方やユーザーの理解も役立ちます。

<!--
### I want to lead one, what do I need to do?
-->

### バグスクラブをリードしたいのですが、何をする必要がありますか ?

<!--
Awesome! Thank you!
-->

すばらしい ! ありがとう !

<!--
You can schedule a bug scrub by pinging a the Core Triage lead for the current release, by volunteering in during the Core Dev chat open floor time, or by commenting on the Core Dev chat agenda/summary posts with your interest.
-->

現在のリリースのコアトリアージリードに通知するか、コア開発者チャットのオープンフロアにボランティアとして参加するか、コア開発者チャットの要約の投稿にコメントすることで、バグスクラブをスケジュールできます。

<!--
Have the report or list of tickets that you want to go through in mind, and someone will make sure your scrub is scheduled in the most appropriate Slack room.
-->

取り組みたいチケットのレポートやリストがあれば、あなたのスクラブが最も適切な Slack ルームでスケジュールされていることを誰かが確認してくれるでしょう。

<!--
Most scrubs will happen in the [#core](https://make.wordpress.org/core/tag/core/) room, though some components have their own rooms where it makes sense to hold the scrub.
-->

ほとんどのスクラブは [#core](https://make.wordpress.org/core/tag/core/) ルームで行われますが、一部のコンポーネントにはスクラブを保持することが適切な独自のルームがあります。

<!--
If you are new to leading bug scrubs, you can be paired up with an experience scrubber to help guide you through the process!
-->

もしあなたがバグスクラブに慣れていない場合は、経験豊富なスクラブ担当者とペアを組み、そのプロセスを指導してもらうことができます !

<!--
### What should I do if a ticket won’t realistically get completed in its “milestoned” release?
-->

### チケットが「マイルストーン」リリース内に現実的に完了しない場合はどうすればよいですか ?

<!--
If a ticket will not likely be completed in a timely manner for a given release, you will want to “punt” it from the milestone. The best approach is to change the milestone to `Future Release` and not the next major or minor release as this typically ends up with a large amount of open tickets rolling over from release to release. “Punting” them to `Future Release` allows component maintainers and people particularly passionate about the issue to purposefully, intentionally milestone it for a release.
-->

チケットが特定リリースでタイムリーに完了しない可能性が高い場合は、マイルストーンから「punt (次のリリースに持ち越す)」したくなるでしょう。最良の方法は、マイルストーンを次のメジャーリリースやマイナーリリースではなく `Future Release` に変更することです。これにより、通常、大量のオープンチケットがリリース間で引き継がれていくことになります。それらを `Future Release` に「Punting」することで、コンポーネントのメンテナーやこの問題に特に熱心な人々が、リリースに向けて意図的にマイルストーンを設定できます。

<!--
### What if no one else shows up?
-->

### 他に誰も来なかったらどうしますか ?

<!--
This sometimes happens and is fine. It just means you end up publicly sharing your thoughts on how to move a ticket forward. Sometimes people will start to chime in once they see someone being active.
-->

これは時々起こりますが、問題はありません。それは、チケットをどのように進めるかについて自分の考えを公の場で共有することになることを意味します。誰かが活発に活動していることを知ると、誰かが参加し始めることもあります。

<!--
An active bug tracker is one sign of a healthy project. Help ensure the health of WordPress by running a Bug Scrub.
-->

バグトラッカーが活発であることは、プロジェクトが健全であることの一つの証です。バグスクラブを実行することで、WordPress の健全性を確保してください。

<!--
*This page is a modified version of the [Bug Scrubs for 4.7](https://make.wordpress.org/core/2016/08/25/bug-scrubs-for-4-7/) post on [Making WordPress Core](https://make.wordpress.org/core/). Props to @jorbin for writing that post.*
-->

**このページは [Making WordPress Core](https://make.wordpress.org/core/) の [Bug Scrubs for 4.7](https://make.wordpress.org/core/2016/08/25/bug-scrubs-for-4-7/) の投稿を修正したものです。この記事を書いてくれた @jorbin に感謝します。**
