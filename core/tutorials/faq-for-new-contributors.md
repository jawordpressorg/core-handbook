<!--
# FAQ for New Contributors
-->

# 新しい貢献者向けの FAQ

<!--
This Frequently Asked Questions list comes from questions that new Core contributors ask in *New Contributors Meetings*.
-->

このよくある質問リストは、「新しい貢献者ミーティング」において、新規のコア貢献者から寄せられた質問から作成されています。

<!--
Look for the list to grow over time as more questions get asked and answered.
-->

このリストは、より多くの質問が寄せられ、回答されるにつれて、時間の経過とともに増えていきます。

<!--
## How do I get started?
-->

## どうすれば始められますか ?

<!--
There’s a lot of documentation out there. You’ll want to get a sense of what it covers and where the various parts and pieces live, start by going through it with an eye toward figuring out where things are, how they’re structured and what the topics are that particularly appeal to you.
-->

ここにはたくさんのドキュメントがあります。このドキュメントが何をカバーしているのか、さまざまな部分や部分がどこにあるのかを把握する必要があります。まず、どこに何があるのか、どのように構成されているのか、特に興味を引くトピックは何なのかを把握することを目的として、このドキュメントを読み進めることからはじめてください。

<!--
You’ll probably forget the details, but you’ll know you can find things again with a search. Go ahead and bookmark those pages for further reference.
-->

おそらく詳細は忘れてしまうかもしれませんが、検索すればまた見つけることができるでしょう。さらに、参照できるようにするためにそれらのページをブックマークしておきましょう。

<!--
You’ll also want to set up Slack and join a few channels.
-->

また、Slack を立ち上げ、いくつかのチャンネルに参加できます。

<!--
Start going to the [scheduled meetings](https://make.wordpress.org/meetings/) just to get an idea of how things get done:
-->

[予定されているミーティング](https://make.wordpress.org/meetings/)に参加し、物事がどのように行われるかを把握しましょう:

<!--
*   what each group talks about,
*   what gets a lot of attention across groups and, therefore,
*   what the priorities are.
-->

*   各グループが何について話しているか、
*   グループ全体で何が注目されているか、したがって、
*   優先順位は何か。

<!--
You also will want to go through the posts on [Make WordPress Core](https://make.wordpress.org/core/) to read meeting summaries from a while back, for context and to see how things get priority. Along with your other reading, you’ll start to get an idea of what the focus areas are and where you’d like to focus your time.
-->

また、[Make WordPress Core](https://make.wordpress.org/core/) の投稿を見て、以前のミーティングの要約を読み、文脈を理解し、物事の優先順位を確認できます。他の読む作業と合わせて、重要な分野が何なのか、どこに時間を集中したいのかが見えてくるでしょう。

<!--
## Are there specific people who can help me get started?
-->

## 手助けしてくれる人はいますか ?

<!--
There are. [@desrosj](https://profiles.wordpress.org/desrosj/), [@flixos90](https://profiles.wordpress.org/flixos90/), [@adamsilverstein](https://profiles.wordpress.org/adamsilverstein/), [@welcher](https://profiles.wordpress.org/welcher/), [@audrasjb](https://profiles.wordpress.org/audrasjb/), [@costdev](https://profiles.wordpress.org/costdev/), [@mike](https://profiles.wordpress.org/mike/), [@oglekler](https://profiles.wordpress.org/oglekler/), and [@SergeyBiryukov](https://profiles.wordpress.org/SergeyBiryukov/) run the New Core Contributors Bimonthly Chats on Slack; plan to start going to a few. The schedule is on [Make/Meetings](https://make.wordpress.org/meetings/), and they’ll welcome your questions.
-->

はい。[desrosj](https://profiles.wordpress.org/desrosj/)、[@flixos90](https://profiles.wordpress.org/flixos90/)、[@adamsilverstein](https://profiles.wordpress.org/adamsilverstein/)、[@welcher](https://profiles.wordpress.org/welcher/)、[@audrasjb](https://profiles.wordpress.org/audrasjb/)、[@costdev](https://profiles.wordpress.org/costdev/)、[@mike](https://profiles.wordpress.org/mike/)、[@goglekler](https://profiles.wordpress.org/oglekler/)、[@SergeyBiryukov](https://profiles.wordpress.org/SergeyBiryukov/) は、Slack 上で隔月の新しいコア貢献者チャットを運営しています。スケジュールは [Make/Meetings](https://make.wordpress.org/meetings/) にあります。彼らはあなたの質問を歓迎します。

<!--
You can also ping them on Slack. If you have questions after a meeting, or you have a question you’d rather not ask publicly, you’re more than welcome to ping them throughout the week.
-->

Slack で連絡することもできます。ミーティング後に質問がある場合や、公にはしたくない質問がある場合は、1週間を通して遠慮なく質問してください。

<!--
## Given that most tickets already have a patch submitted, where should I start on Trac?
-->

## ほとんどのチケットはすでにパッチが提出されていることを考えると、Trac のどこから始めるべきですか ?

<!--
It’s true that some tickets already have patches.
-->

いくつかにチケットには、すでにパッチが提出されていることは事実です。

<!--
But patched rarely means finished. Generally, patches need review and feedback from other contributors. And from [component](https://make.wordpress.org/core/components/) maintainers.
-->

しかし、パッチが提出されたからといって、それが完了を意味することはほとんどありません。一般的に、パッチは他の貢献者からのレビューとフィードバックを必要とします。そして、[コンポーネント](https://make.wordpress.org/core/components/)メンテナーからもです。

<!--
Sometimes a first patch takes significant edits. Sometimes you might see multiple patches at the same time, iterating on a solution or exploring a variety of approaches.
-->

場合によっては、最初のパッチに大幅な編集が必要になることもあります。時には、解決策が繰り返されたり、さまざまなアプローチが検討されたりするため、同時に複数のパッチを目にするかもしれません。

<!--
That’s why you see tickets that already have a patch, and why we don’t just automatically commit them. They still need testing, plus all those reviews and feedback we just mentioned. In fact, testing an existing patch and giving feedback is an excellent way for you to get involved, and a critical step in the process that moves them forward.
-->

すでにパッチが提出されているチケットを見かけるのはこのためであり、私たちがそれらを自動的にコミットしない理由です。それらはまだテストが必要であり、さらに先ほど述べたすべてのレビューとフィードバックが必要なのです。実際、既存のパッチをテストしてフィードバックを与えることは、参加するためのすばらしい方法であり、パッチを前進させるプロセスの重要なステップなのです。

<!--
So once you’ve done your thing, whether patching or testing or reviewing, how do you get more eyes on a ticket?
-->

さて、パッチやテスト、レビューなどのやるべきことを終えたら、チケットにより多くの注目を集めるにはどうしたらいいでしょうか ?

<!--
The ticket comments are your best friend. When you leave a comment, the ticket automatically pings everyone on the ticket: its owner, people who are watching the ticket and, best of all, one or more relevant component maintainers. And they have every interest in the world in getting that ticket committed and merged – it’s what we do as contributors to WordPress.
-->

チケットのコメントはあなたの強い味方です。コメントを残すと、自動的にチケットに関するすべての人 (チケットの所有者、チケットを見ている人たち、そして何よりも、関連するコンポーネントメンテナーの一人または複数に) に通知が送られます。彼らはそのチケットをコミットしてマージすることにあらゆる関心を持っています。それが、私たちが WordPress のコントリビューターとして行っていることなのです。

<!--
You can also bring it up in [#core](https://wordpress.slack.com/archives/C02RQBWTW) on Slack any time outside of any ongoing meeting (or in the open floor section of the weekly dev meeting).
-->

また、Slack の [#core](https://wordpress.slack.com/archives/C02RQBWTW) で、進行中のミーティング以外でも (あるいは毎週の開発ミーティングのオープンフロアのセクションでも)、いつでもそのチケットを話題にできます。
<!--
## Are there specific priorities or components that need more help than others? Where can I help the most?
-->

## 他のものよりも支援が必要な特定の優先事項やコンポーネントはありますか ? どこを一番助けることができますか ?

<!--
Start with the list of [good first bugs](https://core.trac.wordpress.org/tickets/good-first-bugs) in core or [good first issues](https://github.com/WordPress/gutenberg/contribute) in Gutenberg.
-->

コアの [good first bugs](https://core.trac.wordpress.org/tickets/good-first-bugs)、または Gutenberg の [good first issues](https://github.com/WordPress/gutenberg/contribute) のリストから始めましょう。

<!--
These are well-contained tasks designed to help you get familiar with WordPress core code, processes and contributing. And they likely won’t send you down a rabbit hole.
-->

これらは、WordPress のコアコード、プロセス、貢献についてよく理解できるように設計された、よくまとまったタスクです。これらのタスクは、あなたを迷わせることはないでしょう。

<!--
If nothing catches your eye on that list, start looking at the [tickets marked as needs-patch, needs-testing, needs-design, or needs-design-feedback](https://core.trac.wordpress.org/query?status=!closed&keywords=~good-first-bug&keywords=~needs-patch&keywords=~needs-testing&keywords=~needs-design&keywords=~needs-design-feedback&group=milestone&order=priority) in the current milestone. They have a higher priority and need the most attention.
-->

もしこのリストに目を引くものがなければ、現在のマイルストーンにある [needs-patch, needs-testing, needs-design, needs-design-feedback とマークされたチケット](https://core.trac.wordpress.org/query?status=!closed&keywords=~good-first-bug&keywords=~needs-patch&keywords=~needs-testing&keywords=~needs-design&keywords=~needs-design-feedback&group=milestone&order=priority)を見てください。これらのチケットは優先度が高く、最も注意を払う必要があります。

<!--
You can run a query for tickets with no patch: [https://core.trac.wordpress.org/tickets/no-patch](https://core.trac.wordpress.org/tickets/no-patch)
-->

パッチのないチケットのクエリーも実行できます: [https://core.trac.wordpress.org/tickets/no-patch](https://core.trac.wordpress.org/tickets/no-patch)

<!--
## How can I get involved with Bug Gardening? Can I pick any ticket that seems interesting?
-->

## バグガーデニングに参加するにはどうすればよいですか ? 興味があるチケットを選んでいいですか ?

<!--
Bug Gardening is a great way to contribute. And, yes. Feel free to pick any ticket that seems interesting.
-->

バグガーデニングは貢献するためのすばらしい方法です。そして、興味のあるチケットを自由に選んでください。

<!--
Do start by reading the [handbook entry on Bug Gardening](https://make.wordpress.org/core/handbook/testing/bug-gardening/).
-->

[バグガーデニングに関するハンドブック](https://make.wordpress.org/core/handbook/testing/bug-gardening/)を読むことから始めてください。

<!--
There’s a Triage Team that’s looking for contributors. Its mission is to go through every open ticket in Trac to review and triage each one, aiming to lower the absolute number of tickets in the short term and keep that number low going forward.
-->

貢献者を探しているトリアージチームがあります。このチームのミッションは、Trac にあるすべてのオープンなチケットをレビューし、トリアージすることです。このチームは、Trac にあるすべてのオープンなチケットを調べて、それぞれをレビューしてトリアージし、短期的にチケットの絶対数を減らし、今後もその数を低く抑えることを目的としています。

<!--
Some recommended reading on that:
-->

それに関するおすすめの記事をいくつか紹介します:

*   [Introducing the WordPress Triage Team](https://make.wordpress.org/core/2019/03/01/introducing-the-wordpress-triage-team/)
*   [Triage Team Meeting Summary – March 11, 2019](https://make.wordpress.org/core/2019/03/13/triage-team-meeting-summary-march-11-2019/)
*   [WordPress Triage Team: A 3 Month Reflection](https://jonathandesrosiers.com/2019/06/wordpress-triage-team-3-month-reflection/)

<!--
## While I browsed Trac, I replied to some tickets. Where can I find them again?
-->

## Trac を閲覧しているときに、いくつかのチケットに返信しました。どこでまた見つけることができますか ?

<!--
Bookmark this: [https://core.trac.wordpress.org/my-comments](https://core.trac.wordpress.org/my-comments)
-->

これをブックマークしてください: [https://core.trac.wordpress.org/my-comments](https://core.trac.wordpress.org/my-comments)

<!--
## How do core maintainers choose what goes into a next release?
-->

## コアメンテナーは、次のリリースに何を入れるかをどのように選んでいるのですか ?

<!--
Generally, the release leads and component maintainers have some tasks they would like to prioritize for the release. For reference, [see the proposed scope for 5.4](https://make.wordpress.org/core/2020/01/14/wordpress-5-4-planning-roundup/).
-->

一般的に、リリースリードとコンポーネントメンテナーには、リリースに向けて優先したいタスクがいくつかあります。参考までに、[5.4で提案されたスコープを参照してください](https://make.wordpress.org/core/2020/01/14/wordpress-5-4-planning-roundup/)。

<!--
Plus, from Trac, we merge a lot of small bug fixes and enhancements across every component.
-->

さらに Trac から、すべてのコンポーネントにわたる多くの小さなバグ修正と拡張機能をマージします。

<!--
Also, in the earliest weeks, there’s an [open call for tickets](https://make.wordpress.org/core/2019/12/04/wordpress-5-4-open-call-for-tickets/) so teams can get a better idea of what’s important to the community. Then, component maintainers and committers go over the results and add tickets that make sense, based on the overall priorities of the release.
-->

また、最初の数週間は[チケットの公募](https://make.wordpress.org/core/2019/12/04/wordpress-5-4-open-call-for-tickets/)があるため、チームはコミュニティにとって何が重要かをよりよく知ることができます。そして、コンポーネントメンテナーとコミッターがその結果を検討し、リリースの全体的な優先順位にもとづいて、意味のあるチケットを追加します。

<!--
## What do all those keywords on the tickets mean? What are they for?
-->

## チケットにあるこれらのキーワードは何を意味し、何のためにあるのですか ?

<!--
See [Trac workflow keywords glossary](https://make.wordpress.org/core/handbook/contribute/trac/keywords/).
-->

[Trac ワークフローキーワード 用語集](https://make.wordpress.org/core/handbook/contribute/trac/keywords/)を参照してください。

<!--
## How do I make patches with Git?
-->

## Git でパッチを作成するにはどうすればよいですか ?

<!--
See these articles for more information on creating patches with Git:
-->

Git を使ったパッチの作成については、以下の記事を参照してください:

<!--
*   [The Code Repository (Git)](https://make.wordpress.org/core/handbook/contribute/git/)
*   [Contributing To WordPress (Using Git)](http://scribu.net/wordpress/contributing-to-wordpress-using-github.html)
*   [Contributing to WordPress using Git and GitHub PRs](https://make.wordpress.org/core/handbook/contribute/git/github-pull-requests-for-code-review/)
-->

*   [コードリポジトリ (Git)](https://make.wordpress.org/core/handbook/contribute/git/)
*   [Contributing To WordPress (Using Git)](http://scribu.net/wordpress/contributing-to-wordpress-using-github.html)
*   [Git と GitHub プルリクエストを使用して WordPress に貢献する](https://make.wordpress.org/core/handbook/contribute/git/github-pull-requests-for-code-review/)

<!--
Find out more on the [Contributing with Code Handbook page](https://make.wordpress.org/core/handbook/contribute/).
-->

詳しくは、[コードによる貢献に関するハンドブックページ](https://make.wordpress.org/core/handbook/contribute/)を参照してください。

<!--
## How should I name my patches?
-->

## パッチにはどのような名前を付ければよいですか ?

<!--
If there are other patches on the ticket, add a numeric increment to your version, separated with a dot. Otherwise, name your patch after the ticket number.
-->

チケットに他のパッチがある場合は、あなたのバージョンをドットで区切って、数字のインクリメントを追加します。そうでない場合は、チケット番号の後にパッチの名前を付けます。

<!--
For example, if your patch is the first for ticket 12345, name your file 12345.diff. If there are 2 other patches, name your file 12345.2.diff.
-->

たとえば、あなたのパッチがチケット12345の最初のものであれば、ファイル名を 12345.diff とします。他に2つのパッチがある場合は、12345.2.diff とします。

<!--
If you want, you can include a very shortened purpose to your filename.
-->

必要であれば、目的を非常に短くしたものをファイル名に含めることができます。

<!--
## Where can I learn more about working with Trac?
-->

## Trac での作業について、詳しくはどこで確認できますか ?

<!--
See the related [Core Handbook Page](https://make.wordpress.org/core/handbook/tutorials/trac/new-user-quick-start/).
-->

関連する[コアハンドブックページ](https://make.wordpress.org/core/handbook/tutorials/trac/new-user-quick-start/)を参照してください。

<!--
Also, check the [bug scrub schedule](https://make.wordpress.org/core/2020/01/20/bug-scrub-schedule-for-5-4/) and go to some scrubs. You’ll learn a lot by doing!
-->

また、[バグスクラブのスケジュール](https://make.wordpress.org/core/2020/01/20/bug-scrub-schedule-for-5-4/)をチェックして、いくつかのスクラブに参加してみてください。そうすることで多くのことを学べるでしょう !
