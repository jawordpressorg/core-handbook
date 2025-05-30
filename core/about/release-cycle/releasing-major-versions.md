<!--
# Releasing Major Versions
-->

# メジャーバージョンのリリース

<!--
Some things may be out of date, or unclear. If you have questions, reach out to a [prior release lead](https://make.wordpress.org/core/tag/release-lead/).
-->

\[alert\]古い情報や不明な点があるかもしれません。ご質問がある場合は、[先行リリースリード](https://make.wordpress.org/core/tag/release-lead/)までご連絡ください。\[/alert\]

<!--
Congratulations! You’re a release lead for WordPress! The next few months of your life will be a whirlwind of excitement, frustration, and fun. Leading a WordPress release isn’t *easy*, but you’ll have a great time anyway.
-->

おめでとうございます ! あなたは WordPress のリリースリードです ! これからの数ヵ月は、興奮と挫折、楽しさが渦巻く人生になるでしょう。WordPress のリリースをリードすることは**簡単**ではありませんが、とにかくすばらしい時間を過ごすことになるでしょう。

<!--
There have been many before you, and there will be many after you. While this page might help guide you to the finish line, each release lead brings their own touch to the release. When in doubt, talk with a [previous release lead](https://make.wordpress.org/core/tag/release-lead/) and ask for direction.
-->

あなたの前にも沢山の人がいて、あなたの後にも沢山の人がいるでしょう。このページがあなたをゴールまで導いてくれるかもしれませんが、リリースリードはそれぞれ、リリースに独自のタッチをもたらします。迷ったときは、[以前のリリースリード](https://make.wordpress.org/core/tag/release-lead/)に相談し、指示を仰いでください。

<!--
#
-->

## はじめに

<!--
It’s worth reading through the [Releasing Minor Versions](https://make.wordpress.org/core/handbook/about/release-cycle/releasing-minor-versions/) handbook page, since many of its points apply to major version releases, too. That’s especially true as you get closer to the release date.
-->

[マイナーバージョンのリリース](https://ja.wordpress.org/team/handbook/core/about/release-cycle/releasing-minor-versions/)のハンドブックページは一読する価値があります。そのポイントの多くはメジャーバージョンのリリースにも当てはまるからです。リリース日が近付くにつれ、特にそう言えるでしょう。

<!--
Once you’ve been appointed lead for a given release, here are some things you should think about or do right away:
-->

あるリリースのリードに任命されたら、すぐに考えるべきこと、やるべきことをいくつか挙げてみます:

<!--
*   **Talk to leads, committers, and component maintainers.** On day one, you might have no idea what your release will contain. Spend some time with each of the various WordPress leads, committers, and component maintainers to see what they have in mind. These discussions can happen over days, weeks, or even months depending on when your release is scheduled.
*   **Set a schedule.** A good cadence for major releases is every four months —often April, August, and December—though that’s not set in stone. One of the best ways to set your schedule: pick a release date and work backward from that date. Check out the scheduling section below for some tips!
*   **Pick release deputies.** You don’t have to have a release deputy, but it’s *strongly encouraged*. Some release leads have two or more deputies, which is perfectly fine! The trick here is to pick deputies who can augment your talents and assist throughout the cycle. Don’t enjoy writing meeting notes or running meetings? Pick a deputy who does! Not a fan of triage? There’s a community member out there who would love to help. If you’re unsure who might be interested in being a deputy, [post on make/core with a call for volunteers](https://make.wordpress.org/core/tag/deputy/). (Be sure to tag your post!)
*   **Post a call for ideas.** WordPress is built by a large community of volunteers, only some of which are committers and component maintainers. Early on in the release cycle, [post on make/core asking for ideas for the release](https://make.wordpress.org/core/tag/wishlist/). From that post, you will get individual tickets and bigger feature ideas. Sorting through them all will take some time, but will give you a great list of things to investigate for your release.
-->

* **リード、コミッター、コンポーネントメンテナーと話す。** 初日には、リリースに何が含まれるのか見当もつかないかもしれません。さまざまな WordPress のリード、コミッター、コンポーネントメンテナーと時間をかけて、彼らが何を考えているのかを確認しましょう。このような話し合いは、リリースのスケジュールにもよりますが、数日、数週間、あるいは数ヵ月に渡って行われることもあります。
* **スケジュールを設定する。** メジャーリリースの良いサイクルは4ヵ月ごとです。多くの場合、4月、8月、12月です。とはいえ、明確に決まっているわけではありません。スケジュールを設定する最良の方法のひとつは、リリース日を決め、その日から逆算することです。いくつかのヒントについては、以下のスケジューリングセクションをチェックしてください !
* **リリースのサブリードを選ぶ。** リリースのサブリードを立てる必要はありませんが、立てることを*強くおすすめします*。いくつかのリリースのリードは2人以上のサブリードを持っていますが、それはまったく問題ありません ! ここでのコツは、あなたの才能を補強し、サイクル全体を通してアシストしてくれるサブリードを選ぶことです。ミーティングノートを書いたり、ミーティングを運営したりするのが苦手ですか ? そのようなことができるサブリードを選びましょう ! トリアージが苦手ですか ? 手伝ってくれるコミュニティメンバーがいるはずです。誰がサブリードになることに興味があるかわからない場合は、[make/core にボランティア募集の投稿](https://make.wordpress.org/core/tag/deputy/)をしてください。(投稿には必ずタグをつけてください !)
* **アイデアを募集する。** WordPress はボランティアによる大きなコミュニティによって構築されていますが、そのうち一部のみがコミッターやコンポーネントメンテナーです。リリースサイクルの早い段階で、[make/core にリリースのアイデアを募集する投稿](https://make.wordpress.org/core/tag/wishlist/)をしてください。その投稿から、個別のチケットや大きな機能のアイデアが得られます。それらをすべて整理するのは時間がかかりますが、リリースのために調査すべきことのすばらしいリストを得ることができます。

<!--
### On Scheduling
-->

### スケジュールについて

<!--
As the WordPress project grows increasingly global, it gets harder to find perfect release dates. Here are a few best practices to keep in mind as you settle on the likely timeline:
-->

WordPress プロジェクトがグローバルになるにつれ、完璧なリリース日を見つけることが難しくなっています。ここでは、可能性の高いスケジュールを決定する際に注意すべきベストプラクティスをいくつか紹介します:

<!--
*   Try to be firm on the release date itself, but be prepared to add betas if necessary, or adjust RC dates.
*   Check for major holidays (including religious holidays, banking holidays, national holidays, etc.)
*   Check for large events that the community attends (WCUS, WCEU, etc.)
-->

* リリース日自体についてはしっかりと決める。ただし、必要に応じてベータ版を追加したり、RC 版の日付を調整したりできるように準備しておくこと。
* 主要な祝日 (宗教上の祝日、銀行休業日、国民の祝日などを含む) をチェックする。
* コミュニティが参加する大きなイベント (WCUS、WCEU など) をチェックする。

<!--
### On Roles & Responsibilities
-->

### 役割と責任について

<!--
There are a [number of roles and responsibilities](https://make.wordpress.org/core/handbook/about/release-cycle/wordpress-release-team-and-focus-leads/) over the course of a release. In practice, if there’s not a release coordinator for a cycle, a release lead and their deputies act as project managers (and technical project managers) for the entire release cycle. Otherwise, a release coordinator takes on ensuring the various pieces are properly covered by the cohesive release squad.
-->

リリースの間には[いくつもの役割と責任](https://ja.wordpress.org/team/handbook/core/about/release-cycle/wordpress-release-team-and-focus-leads/)があります。実際には、そのサイクルのリリースコーディネーターがいない場合、リリースリードとそのサブリードがリリースサイクル全体のプロジェクトマネージャー (およびテクニカルプロジェクトマネージャー) として活動します。そうでない場合は、リリースコーディネーターが、結束力のあるリリースチームによってさまざまな部分が適切にカバーされるようにします。

<!--
**Important note:** Much of the tasks listed in this handbook page are done by those who act as “mission control” or MC. These are a very specific set of folks with a particular ability to perform larger meta\-tasks for the project. If you’re not sure how to do something or don’t have access, it’s likely a task for those folks to handle. 
-->

**重要な注意事項:** このハンドブックのページに記載されているタスクの多くは、「ミッションコントロール」または MC として行動する人々によって行われます。これらは、プロジェクトのためのより大きなメタタスクを実行する、特定の能力を持った人々のための非常に特別なセットです。もしやり方がわからなかったり、アクセスできなかったりした場合は、そのような人たちが処理するタスクである可能性が高いでしょう。

<!--
Prior to considering the responsibilities of release leads and deputies, it’s important to understand a few qualities of effective release leads:
-->

リリースリードとサブリードの責任を考える前に、有効なリリースリードの資質をいくつか理解しておくことが重要です:

<!--
*   **An understanding of how WordPress – both the software and the community – works.** WordPress, the software, is vast. No single contributor understands the entire codebase. However, release leads and deputies should have a good understanding of how WordPress works and how the core community functions. Knowing who to ask about various tickets is an important skill for leading a release!
*   **Knowledge of how open source works.** Open source projects run quite a bit differently than most software projects. To be a release lead or deputy, it’s expected that you have the ability to work well as a part of an open source, global, distributed project.
*   **The ability to communicate well with the community.** Communication is incredibly important across every part of the WordPress community, so good communication is valued and expected. The core community communicates in English, on this site, and in Slack, even though many contributors speak English as a second language. As a result of the varying backgrounds in this global community, release leads and deputies should take care when communicating in official and unofficial channels. See also: [Post & Comment Guidelines](https://make.wordpress.org/core/handbook/best-practices/post-comment-guidelines/).
-->

* **WordPress のしくみ (ソフトウェアとコミュニティの両方) を理解していること。** WordPress というソフトウェアは巨大なものです。一人の貢献者がコードベース全体を理解しているわけではありません。しかし、リリースリードとサブリードは、WordPress がどのように動作し、どのようにコアコミュニティが機能するかをよく理解している必要があります。さまざまなチケットについて誰に尋ねるべきかを知ることは、リリースをリードするための重要なスキルです !
* **オープンソースがどのように機能するかについての知識。** オープンソースプロジェクトは、ほとんどのソフトウェアプロジェクトとはかなり異なっています。リリースリードやサブリードになるためには、オープンソースでグローバルな分散型プロジェクトの一員として働く能力があることが期待されます。
* **コミュニティとの良好なコミュニケーション能力。** コミュニケーションは WordPress コミュニティのあらゆる部分で非常に重要であるため、良好なコミュニケーションが評価され、期待されます。中心的なコミュニティは、多くの貢献者が第二言語として英語を話しているにもかかわらず、このサイトや Slack では英語でコミュニケーションをとっています。このグローバルコミュニティにはさまざまなバックグラウンドがあるため、リリースリードやサブリードは公式・非公式チャンネルでコミュニケーションをとる際には注意が必要です。こちらもご覧ください: [投稿とコメントのガイドライン](https://ja.wordpress.org/team/handbook/core/best-practices/post-comment-guidelines/)。

<!--
There are also a few responsibilities that release leads and deputies have over the course of a release cycle:
-->

またリリースサイクルの中で、リリースリードとサブリードが持つ責任もいくつかあります:

<!--
*   **Posting agendas, running weekly developer chats, and posting chat summaries.** The overall WordPress developer community should be kept informed throughout the release cycle. Not every community member can attend the weekly developer chats, so posting [agendas](https://make.wordpress.org/core/tag/agenda/) and [chat summaries](https://make.wordpress.org/core/tag/summary/) is a necessity.
*   **Triaging tickets and monitoring ticket reports.** There are many moving pieces to a release. Release leads and deputies should keep a watchful eye on incoming trunk tickets and monitor relevant [ticket reports](https://make.wordpress.org/core/reports/). This includes triaging new ticket reports (especially in unowned components) to check for blocking issues.
*   **Keeping the release on schedule.** [Deadlines are not arbitrary.](https://make.wordpress.org/core/handbook/about/philosophies/#deadlines-are-not-arbitrary) WordPress releases should strive to stay on schedule and the release lead and deputies are responsible for this schedule. (See “On Scheduling,” above.) There are many aspects to maintaining the release schedule, many of which are listed as responsibilities here.
*   **Running bug scrubs.** Weekly bug scrubs are a useful activity that encourages contributions from all kinds of contributors. They can be successfully run by release leads, deputies, and other contributors. Component maintainers can also run bug scrubs.
*   **Reviewing and responding to feature ideas.** WordPress contributors and users will post feature ideas throughout the release cycle, especially on [wishlist](https://make.wordpress.org/core/tag/wishlists/) posts. While it is not the responsibility of the release lead (or deputy) to develop each feature, they should review each feature idea and see if it warrants inclusion in their release. Many of these ideas will come from [feature projects](https://make.wordpress.org/core/features/), but some may be tickets that need attention.
*   **Tracking down contributors for help.** It is not the responsibility of the release lead to make every technical decision or even the majority of them. The release lead should know how and when to track down and solicit contributors for assistance. The core team is large with varied availability and the release lead should have a good understanding of which contributors are the best to provide feedback and support for a variety of tickets.
*   **Regularly chatting with contributors.** Keeping in close contact with regular contributors helps ensure that a given WordPress release is stable and ready for the public. Chatting with contributors on a regular basis ensures that the release lead knows both the availability of contributors and any potential blocking issues, among other things.
*   **Coordinating marketing efforts.** There are a number of marketing efforts that need to be managed and the release lead or deputy should have an awareness of them. The [About page](https://docs.google.com/document/d/13itxtCD2jkKIMUj8anKLNMKoIWXE3dtJ6FyfkF-XN4E/edit#heading=h.1voz9urseun7) in WordPress core, the /news/ post, and the video are all part of this effort (more below on these specific efforts). [As learned on 4.7](https://core.trac.wordpress.org/ticket/39560), we should avoid having videos set to autoplay simultaneously. Note that these efforts should be conducted in conjunction with the [marketing team](https://make.wordpress.org/marketing/) and the relevant component maintainers. [Reference this release cycle marketing and communications guide](https://make.wordpress.org/marketing/handbook/resources/marketing-communicationsrelease-cycle-guide/) for an in-depth handbook on release communications.
*   **Communicating any changes to the release or to features.** As releases proceed, there are times when big decisions need to be made and communicated appropriately by the release squad. This requires both coming together to find a way forward, sometimes involving project leadership, and doing the work to appropriately communicate any changes. Here are two examples in case the release squad you are a part of runs into similar situations: [Announcing a revised release schedule for WordPress 5.9](https://make.wordpress.org/core/2021/11/22/wordpress-5-9-revised-release-schedule/) and [Webfonts API changes for WordPress 6.0](https://make.wordpress.org/core/2022/04/22/status-of-webfonts-api-for-wordpress-6-0-inclusion/). 
-->

*   **議題の投稿、毎週の開発者チャットの運営、チャットの要約の投稿。** リリースサイクル全体を通して、情報は WordPress 開発者コミュニティ全体に提供されるべきです。すべてのコミュニティメンバーが毎週の開発者チャットに参加できるわけではないので、[議題](https://make.wordpress.org/core/tag/agenda/)と[要約](https://make.wordpress.org/core/tag/summary/)を投稿する必要があります。
*   **チケットのトリアージとチケットレポートのモニタリング。** リリースには多くの重要な要素があります。リリースリードとサブリードは、新しく提出される trunk チケットを注意深く見守り、関連する[チケットレポート](https://make.wordpress.org/core/reports/)を監視する必要があります。これには、(特に未所有のコンポーネントの) 新しいチケットレポートをトリアージして、ブロックする問題がないかチェックすることも含まれます。
*   **リリースを予定通りに進める。** [期限を守ること。](https://ja.wordpress.org/about/philosophy/#deadlines-are-not-arbitrary)WordPress のリリースは、スケジュール通りに進むように努力すべきであり、リリースリードとサブリードがこのスケジュールに責任を持ちます (上記の「スケジュールについて」を参照してください)。リリースのスケジュールを維持するには多くの側面があり、その多くはここで責任として挙げられています。
*   **バグスクラブの開催。** バグスクラブを毎週開催することは、あらゆる種類の貢献者からの貢献を促す有用な活動です。この活動は、リリースリード、サブリード、その他の貢献者によってうまく運営できます。コンポーネントメンテナーもバグスクラブを行うことができます。
*   **機能に関するアイデアを検討し、対応する。** WordPress の貢献者やユーザーは、リリースサイクル中、特に[ウィッシュリスト](https://make.wordpress.org/core/tag/wishlists/)の投稿に機能のアイデアを投稿します。各機能を開発することはリリースリード (またはそのサブリード) の責任ではありませんが、各機能のアイデアをレビューし、リリースに含める価値があるかどうかを確認する必要があります。これらのアイデアの多くは、[機能に関するプロジェクト](https://make.wordpress.org/core/features/)から出てくるものですが、中には注意が必要なチケットもあるでしょう。
*   **助けてくれる貢献者を見つける。** すべての技術的な決定、あるいはその大部分を行うことは、リリースリードの責任ではありません。リリースリードは、いつどのように貢献者を探し出し、支援を求めるべきかを知っておくべきです。コアチームは大規模で、リソースの状況もさまざまであるため、リリースリードはさまざまなチケットに対してフィードバックやサポートを提供するために、どの貢献者が最適であるかをよく理解している必要があります。
*   **貢献者と定期的にチャットする。** 定期的に貢献者と連絡を取り合うことは、WordPress のリリースが安定し、公開の準備が整っていることを保証するために役立ちます。定期的に貢献者とチャットすることで、リリースリードは貢献者の稼働状況やブロックの可能性のある問題などを把握できます。
*   **マーケティング活動の調整。** 管理するべきマーケティング活動がいくつかあり、リリースリードやサブリードはそれらを認識している必要があります。WordPress コアの[アバウトページ](https://docs.google.com/document/d/13itxtCD2jkKIMUj8anKLNMKoIWXE3dtJ6FyfkF-XN4E/edit#heading=h.1voz9urseun7)、/news/ の投稿、ビデオはすべてこの取り組みの一部です (これらの具体的な取り組みについては後述します)。[4.7で学んだように](https://core.trac.wordpress.org/ticket/39560)、動画を同時に自動再生するように設定することは避けるべきです。これらの活動は、[マーケティングチーム](https://make.wordpress.org/marketing/)と関連するコンポーネントのメンテナーと連携して行うべきであることに注意してください。リリースコミュニケーションに関する詳細なハンドブックについては、この[リリースサイクルのマーケティングとコミュニケーションガイド](https://make.wordpress.org/marketing/handbook/resources/marketing-communicationsrelease-cycle-guide/)を参照してください。
*   **リリースや機能に対するあらゆる変更を伝える。** リリースが進むにつれて、大きな決断が必要になり、リリースチームによって適切に伝えられなければならないときがあります。そのためには、時にはプロジェクトのリーダーを巻き込みながら、一緒になって進むべき道を見つけることと、変更点を適切に伝えるために作業することの両方が必要です。あなたが所属するリリースチームが同じような状況に陥ったときのために、2つの例を挙げます。[WordPress 5.9のリリーススケジュール変更のアナウンス](https://make.wordpress.org/core/2021/11/22/wordpress-5-9-revised-release-schedule/)と [WordPress 6.0におけるウェブフォント API の変更点](https://make.wordpress.org/core/2022/04/22/status-of-webfonts-api-for-wordpress-6-0-inclusion/)です。

<!--
#### Expectations
-->

#### 期待されること

<!--
Focus leads should be available for at least 5-6 hours a week to perform their tasks, with more time as milestones like Betas, Release Candidates, and General release approach. On the days of those milestones, you might need to dedicate 4-6 hours to WordPress in one day.
-->

フォーカスリードは、タスクを実行するために少なくとも週に5～6時間は確保する必要がありますが、ベータ、リリース候補、正式リリースなどのマイルストーンが近付くにつれ、より多くの時間が必要になります。これらのマイルストーンの日には、1日に4～6時間を WordPress に費やす必要があるかもしれません。

<!--
There are no limitations to where you come from. We are a global community, open 24/7 so you will schedule scrubs, if needed, according to your availability and potentially find a deputy to cover other time zones.
-->

出身地の制限はありません。私たちは24時間365日休みのないグローバルコミュニティですので、必要であればあなたの都合に合わせてスクラブのスケジュールを組み、他のタイムゾーンをカバーするサブリードを見つけられるかもしれません。

<!--
### Helpful Hints
-->

### 役に立つヒント

<!--
*   **Create a public slack channel for communication and perform weekly updates starting just before beta 1.** This helps both the release squad work out in the open for the benefit of future contributors and allows folks to follow along as they see fit. The [#meta](https://make.wordpress.org/core/tag/meta/) team can help facilitate this. 
*   **Ensure redundancy in the release squad and during release parties.** With the size of the project, it goes a long way to have multiple folks in key roles and to ensure that, during release parties, there are multiple folks who can accomplish tasks. For example, having multiple MCs helps ensure someone is available in case the pre-arranged MC has a late arising conflict and cannot participate. 
*   **Examine what folks have done for the last release.** Because this is an open source project, much of what you need to do can be learned by looking at those who came before you. Search slack for release parties, ask questions of prior release leads, look on Make for how prior decisions were handled, etc. 
*   **Recognize each part of the cycle has different restrictions and focuses.** As the release cycle goes on, the focus shifts and it’s important to shift with it. For example, RC requires double sign-off for Core commits so it’s important to plan any important work with that variable in mind. 
*   **Create release party scripts and get alignment well before release days.** It’s normal for there to be plenty of coordination ahead of time, including creating scripts for release parties, checking with folks to ensure they can take on specific steps, etc. Handle the necessary and known stressors so that when unexpected stressors come up you have more capacity to respond. 
*   **Share early and often, especially if you have concerns**. While something might feel obvious to you, it can easily be overlooked by the group if not expressed. 
-->

*   **コミュニケーションのために slack チャンネルを公開し、ベータ1の直前から毎週アップデートを行う。** これによって、将来の貢献者のためにリリースチームがオープンに活動できるようになり、また人々がフォローできます。[#meta](https://make.wordpress.org/core/tag/meta/) チームはこれを促進する手助けができます。
*   **リリースチームとリリースパーティ中には冗長性を確保する。** プロジェクトの規模に伴い、重要な役割に複数の人を配置し、リリースパーティ中にタスクを達成できる人が複数いるようにすることは、とても大切です。たとえば、複数の MC がいることで、事前に予定されていた MC が遅刻などにより参加できなくなった場合に、誰かが確実に対応できます。
*   **前回のリリースで人々が何をしたかを調べる。** これはオープンソースのプロジェクトですので、あなたがすべきことの多くは、先人たちから学ぶことができます。Slack でリリースパーティについて調べたり、前のリリースリードに質問したり、Make で前の決定がどのように行われたかを調べたりしてください。
*   **サイクルの各パートには、それぞれ異なる制限とフォーカスがあることを認識する。** リリースサイクルが進むにつれてフォーカスは移り変わるので、それに合わせてシフトすることが重要です。たとえば、RC では コアコミットに対し二重チェックが必要ですので、その変数を念頭に置いて重要な作業を計画することが大切です。
*   **リリースパーティのスクリプトを作成し、リリース日のかなり前に調整する。** リリースパーティのスクリプトを作成したり、特定のステップを確実にこなせるよう関係者に確認したりなど、前もって十分に調整しておくことは当然です。必要かつ既知のストレス要因に対処しておくことで、予期せぬストレス要因が出てきたときに対応できます。
*   **特に懸念事項がある場合は、早めに頻繁に共有すること。** 自分にとっては当たり前のことでも、それを表現しなければ、グループ内では簡単に見過ごされてしまいます。

<!--
## Pre Merge Window
-->

## マージウィンドウの前に

<!--
*   Feature projects should prepare for merge consideration at the beginning of a release cycle. 
*   Merge proposals should be created and reviewed during this time.
*   Check to see if a new bundled theme will be included in this release.
-->

*   機能に関するプロジェクトは、リリースサイクルの最初に統合の検討を準備するべきです。
*   統合の提案はこの時期に作成し、レビューされるべきです。
*   新しいバンドルテーマがこのリリースに含まれるかどうかを確認してください。

<!--
## Merge Window
-->

## マージウィンドウ

<!--
*   Decide which feature projects (if any) should be merged.
*   If a release video is required, kick off the work on that.
-->

* (もしあれば) どの機能プロジェクトを統合するかを決めます。
* リリースビデオが必要なら、その作業を開始します。

<!--
## Pre Beta 1
-->

## ベータ1の前に

<!--
*   A week before Beta 1, **publish a Release Party Schedule post** that includes the planned timing of the Beta, RC, Dry Run, and Final releases along with who’s responsible for various roles for each release (e.g. Emcee, Committer, Security, Mission Control, Marketing & Communications). [Here is an example from the 6.7 release cycle](https://make.wordpress.org/core/2024/09/24/wordpress-6-7-release-party-schedule/).
*   **[Compile and start to publish Dev notes](https://make.wordpress.org/core/handbook/tutorials/writing-developer-notes/)**. Start compiling and publishing posts that inform developers of breaking changes and major developer-focused updates of the release on [make/core using #dev-notes](https://make.wordpress.org/core/tag/dev-notes/).
*   **About Page**. Start compiling noteworthy features in the release and identifying a designer who can contribute illustrations. Words should be complete by RC1, images can update through RC2. Some [in-depth information on the About Page process](https://docs.google.com/document/d/13itxtCD2jkKIMUj8anKLNMKoIWXE3dtJ6FyfkF-XN4E/edit#heading=h.1voz9urseun7) is also available as well as the [marketing communications handbook](https://make.wordpress.org/marketing/handbook/resources/marketing-communicationsrelease-cycle-guide/).
*   **HelpHub Version Page**. Begin compiling noteworthy updates for designers, developers, and users. *The* [*5.2 version page*](https://wordpress.org/support/wordpress-version/version-5-2/) *can be used as an example, or reach out to the [Docs Team](https://make.wordpress.org/docs/) for help.*
*   Identify if any of the browsers listed on the [Browser support page](https://make.wordpress.org/core/handbook/best-practices/browser-support/) had dropped below the percentage required to support them in core and if any need updating plan for that now as that will be one of the final checks and updates in the [Pre Final Release phase below](https://make.wordpress.org/core/handbook/about/release-cycle/releasing-major-versions/#pre-final-release).
-->

*   ベータ1の1週間前に、**リリースパーティスケジュールの投稿** を公開します。この投稿には、ベータ、RC、ドライラン、最終リリースの予定時期と、各リリースにおける各役割の責任者 (司会者、コミッター、セキュリティ、ミッション コントロール、マーケティングとコミュニケーションなど) が記載されます。[6.7 リリースサイクルの例はこちら](https://make.wordpress.org/core/2024/09/24/wordpress-6-7-release-party-schedule/)。
*   **[開発者ノートを編集して公開を開始する](https://ja.wordpress.org/team/handbook/core/tutorials/writing-developer-notes/)**。[make/core で #dev-notes を使って](https://make.wordpress.org/core/tag/dev-notes/)、リリースの重要な変更点や開発者向けの主要な更新を開発者に知らせる記事の編集と公開を開始します。
*   **アバウトページ**。リリースの注目すべき機能をまとめ始め、イラストを提供できるデザイナーを特定します。文章は RC1までに完成させ、画像は RC2まで更新できるようにします。[マーケティングコミュニケーションハンドブック](https://make.wordpress.org/marketing/handbook/resources/marketing-communicationsrelease-cycle-guide/)と同様に、[アバウトページのプロセスに関する詳細情報](https://docs.google.com/document/d/13itxtCD2jkKIMUj8anKLNMKoIWXE3dtJ6FyfkF-XN4E/edit#heading=h.1voz9urseun7)もあります。
*   **HelpHub バージョンページ**。デザイナー、開発者、ユーザーのために、注目すべきアップデートをまとめ始めます。*[5.2 バージョンページ](https://wordpress.org/support/wordpress-version/version-5-2/)を例として使用できますし、[ドキュメントチーム](https://make.wordpress.org/docs/)に助けを求めることもできます。*
*   [ブラウザーサポートページ](https://ja.wordpress.org/team/handbook/core/best-practices/browser-support/)にリストアップされているブラウザーのどれかが、コアでそれらをサポートするために必要なパーセンテージを下回ったかどうかを確認し、更新が必要なものがあれば、[以下の最終的なリリースの前](https://ja.wordpress.org/team/handbook/core/about/release-cycle/releasing-major-versions/#pre-final-release)における最終チェックと更新の1つになるので、そのための計画を立てます。

## ベータ1

<!--
The [process for a Beta release](https://make.wordpress.org/core/handbook/about/release-cycle/releasing-beta-versions/) is well-documented on a separate handbook page.
-->

[ベータ版リリースのプロセス](https://ja.wordpress.org/team/handbook/core/about/release-cycle/releasing-beta-versions/)は、別のハンドブックのページで詳しく説明されています。

<!--
## Pre Release Candidate
-->

## リリース候補の前に

<!--
*   There should be no open tickets on the release milestone.
*   The process for [publishing the Field Guide is documented on a separate handbook page](https://make.wordpress.org/core/handbook/tutorials/publishing-the-field-guide/).
*   All Plugin Authors (in the wp.org repo) should be emailed, letting them know to test their plugins for compatibility with the release. The email should link them to the Field Guide. [Contact the Plugin Team Rep to coordinate](https://make.wordpress.org/updates/team-reps/) or publish the draft release email on the [Plugin Review Team’s make site](https://make.wordpress.org/pluginrepo) ([sample from 5.3 here](https://make.wordpress.org/pluginrepo/2019/10/18/5-3-release-email/)).
*   Test the Classic Editor plugin to make sure it still works well.
*   Remind the Akismet team about the release schedule, to ensure they get any pending plugin updates released before our final release.
    *   Akismet is automatically checked for updates, and updated if required, on every WordPress commit
    *   The plugin is updated in trunk , the current stable branch and the current development branch (if it differs from trunk).
*   The Hosting community should be notified of an updated release date for the major version. Post a Slack message in the [#hosting](https://wordpress.slack.com/messages/hosting/) Slack channel as a reminder.
*   An announcement should be made about the [string freeze](https://make.wordpress.org/polyglots/handbook/glossary/#hard-freeze) on the Polyglots P2 ([example from 5.9](https://make.wordpress.org/polyglots/2021/12/16/wordpress-5-9-ready-to-be-translated/)).
*   Committers should be given a proactive reminder that the [Release Candidate com](https://make.wordpress.org/core/2022/05/04/wordpress-6-0-release-candidate-phase/)[mit policy](https://make.wordpress.org/core/2018/10/05/wordpress-5-0-commit-management/) is coming up when RC 1 is released, specifically that in the RC Phase all commits have to get double sign-off from committers. This begins *after* RC1 is released so, in the reminder, alert folks that the RC phase is coming up but has not yet begun.
*   Run the private security unit test suite.
-->

*   リリースのマイルストーン時点で、オープンチケットが残っていてはなりません。
*   フィールドガイドの公開プロセスは、[別のハンドブックページ](https://ja.wordpress.org/team/handbook/core/tutorials/publishing-the-field-guide/)にドキュメント化されています。
*   (wp.org のリポジトリにある) すべてのプラグイン作者に、リリースとの互換性をテストするように知らせるメールを送るべきです。そのメールはフィールドガイドにリンクされるべきです。[プラグインチームに連絡して調整する](https://make.wordpress.org/updates/team-reps/)か、[プラグインレビューチームが作るサイト](https://make.wordpress.org/pluginrepo)でリリースメールの下書きを公開します ([5.3のサンプルはこちら](https://make.wordpress.org/pluginrepo/2019/10/18/5-3-release-email/))。
*   Classic Editor プラグインがまだうまく動作するかテストしてください。
*   Akismet チームにリリースのスケジュールを伝え、最終リリースの前に保留中のプラグインのアップデートがリリースされるようにします。
    *   Akismet は WordPress のコミットごとに自動的に更新がチェックされ、必要であれば更新されます。
    *   プラグインは trunk、現在の安定版ブランチ、(trunk と異なる場合は) 現在の開発版ブランチで更新されます。
*   ホスティングコミュニティには、メジャーバージョンの更新リリース日を通知する必要があります。リマインダーとして、[#hosting](https://wordpress.slack.com/messages/hosting/) Slack チャンネルにメッセージを投稿してください。
*   [翻訳文字列のフリーズ](https://make.wordpress.org/polyglots/handbook/glossary/#hard-freeze)について、Polyglots P2 でアナウンスしてください ([5.9の例](https://make.wordpress.org/polyglots/2021/12/16/wordpress-5-9-ready-to-be-translated/))。
*   コミッターには、RC1がリリースされるときに[リリース候補コミットポリシー](https://make.wordpress.org/core/2022/05/04/wordpress-6-0-release-candidate-phase/)が適用されること、特に RC フェーズでは、すべてのコミットがコミッターから二重チェックを得なければならないことを積極的に知らせるべきです。これは RC1がリリースされた*後*に始まるので、リマインダーでは、RC フェーズが近付いているが、まだ始まっていないことをみんなに知らせてください。
*   プライベートセキュリティのユニットテスト・スイートを実行してください。

<!--
## Release Candidate
-->

## リリース候補

<!--
A Release Candidate version is released as the last stage of the release cycle before the major version is released. The Release Candidate means that  the release squad feels confident that what is in trunk is good enough for the major release, and should be thoroughly tested by the community.
-->

リリース候補バージョンは、メジャーバージョンがリリースされる前のリリースサイクルの最終フェーズとしてリリースされます。リリース候補版は、trunk にあるものがメジャーリリースに十分であるとリリースチームが自信を持っていることを意味し、コミュニティによって徹底的にテストされるべきです。

<!--
*   A [hard string freeze](https://make.wordpress.org/polyglots/handbook/glossary/#hard-freeze) takes effect at the Release Candidate stage, meaning text strings in the application can no longer be changed, including the About Page text.
*   Multiple Release Candidate versions should be released (e.g. RC1, RC2) as bugs reported against it are fixed.
*   Alert committers that all changes to src/ at the Release Candidate stage must be reviewed by two committers. When choosing a second committer to review your patch, look for a veteran committer with extensive experience in that area of the codebase, so that the patch can receive a meaningful critique. Committers can commit to tests/ at any time.
*   The [process for an RC release](https://make.wordpress.org/core/handbook/about/release-cycle/releasing-beta-versions/) is well-documented on a separate handbook page.
*   Following the first release candidate a branch for the release can be created so that early work on trunk can begin for the next release.
*   The Documentation Lead should prepare drafts and become familiar with the docs to publish on release day, see [documentation process during a major version release](https://make.wordpress.org/docs/handbook/workflows/documentation-process-during-a-major-version-release/). For questions, reach out to the [#docs](https://wordpress.slack.com/archives/C02RP4WU5) team.
*   An announcement should be made on Make Core about the release candidate phase ([example from 6.0](https://make.wordpress.org/core/2022/05/04/wordpress-6-0-release-candidate-phase/)) and the various above protocols in order to better amplify this specific part of the release cycle and prepare the community.
*   At this point, two Make Core posts should be published to begin gathering nominations for folks interested and able to (1) participate in the Minor Release Squad that follows this major release cycle and to (2) participate in the Major Release Square that’s up next.
-->

*   [翻訳文字列のハードフリーズ](https://make.wordpress.org/polyglots/handbook/glossary/#hard-freeze)がリリース候補のフェーズで有効になります。これは、アプリケーションの文字列が、アバウトページのテキストを含めて、もはや変更できないことを意味します。
*   報告されたバグが修正されるにつれて、複数のリリース候補版 (たとえば RC1、RC2) がリリースされるべきです。
*   リリース候補フェーズでの src/ に対するすべての変更は、2人のコミッターによってレビューされなければならないことをコミッターに警告してください。あなたのパッチをレビューする2人目のコミッターを選ぶときは、そのパッチを意味のあるレビューを受けられるように、コードベースのその領域で豊富な経験を持つベテランのコミッターを探しましょう。コミッターはいつでも tests/ にコミットできます。
*   [RC リリースのプロセス](https://ja.wordpress.org/team/handbook/core/about/release-cycle/releasing-beta-versions/)については、別のハンドブックのページに詳しく書かれています。
*   最初のリリース候補に続いてリリース用のブランチを作成し、次のリリースに向けて trunk の初期作業を開始できるようにします。
*   ドキュメンテーションリードは、リリース日に公開するドキュメントのドラフトを作成し、内容を把握しておく必要があります。[メジャーバージョンリリース時のドキュメント作成プロセス](https://make.wordpress.org/docs/handbook/workflows/documentation-process-during-a-major-version-release/)をご覧ください。ご質問は、[#docs](https://wordpress.slack.com/archives/C02RP4WU5) チームまでお問い合わせください。
*   リリースサイクルの特定の部分をより明確にし、コミュニティを準備するために、リリース候補のフェーズ ([6.0の例](https://make.wordpress.org/core/2022/05/04/wordpress-6-0-release-candidate-phase/)) と上記のさまざまなプロトコルについて Make Core でアナウンスする必要があります。
*   この時点で、2つの Make Core 投稿を公開して、興味があり、(1) このメジャーリリースサイクルに続くマイナーリリースチームに参加できる人、および (2) 次のメジャーリリースチームに参加できる人たちの候補を集め始める必要があります。

### translate.WordPress.org

<!--
It’s time to ask the [Polyglots team](https://make.wordpress.org/polyglots/) to help translate the upcoming WordPress version. *In the list below, the example release is A.B.*
-->

[Polyglots チーム](https://make.wordpress.org/polyglots/)に、WordPress の次のバージョンの翻訳に協力してもらいましょう。**以下のリストでは、リリース例を A.B.** としています。

<!--
*   Create a A.B.x sub-project to the main WordPress project.
*   Copy the translation sets from the Development project.
*   Do the same for each Development sub-project.
*   Update [/home/rosetta/public\_html/wp-content/mu-plugins/rosetta/rosetta.php](https://dotorg.trac.wordpress.org/browser/wordpress/rosetta/website/wp-content/mu-plugins/rosetta/rosetta.php) to add mappings from GlotPress project to WordPress branch and the project name in Rosetta.
*   Update [/home/wporg/public\_html/translate/bin/update-all-core-packs.sh](https://dotorg.trac.wordpress.org/browser/wordpress/website/translate/bin/update-all-core-packs.sh) to use the A.B.x sub-project for A.B language packs.
*   Migrate existing translations for Gutenberg plugin to the WordPress project.
*   Notify the [Polyglots team](https://make.wordpress.org/polyglots/) of the strings.
-->

*   メインの WordPress プロジェクトに A.B.x サブプロジェクトを作成します。
*   開発プロジェクトから翻訳セットをコピーします。
*   各開発サブプロジェクトに同じことを行います。
*   [/home/rosetta/public_html/wp-content/mu-plugins/rosetta/rosetta.php](https://dotorg.trac.wordpress.org/browser/wordpress/rosetta/website/wp-content/mu-plugins/rosetta/rosetta.php) を更新して、GlotPress プロジェクトから WordPress ブランチへのマッピングと、Rosetta のプロジェクト名を追加します。
*   A.B 言語パックのための A.B.x サブプロジェクトを使用するために、[/home/wporg/public_html/translate/bin/update-all-core-packs.sh](https://dotorg.trac.wordpress.org/browser/wordpress/website/translate/bin/update-all-core-packs.sh) を更新します。
*   Gutenberg プラグインの既存の翻訳を WordPress プロジェクトに移行します。
*   [Polyglots チーム](https://make.wordpress.org/polyglots/)に文字列を通知します。

<!--
## Branching Before Release
-->

## リリース前のブランチ

<!--
At this point, once the milestone is mostly clear, a branch for the release can be created, so that early work on trunk could start. The following files need to have version numbers updated when branching:
-->

この時点で、マイルストーンがほぼ明確になれば、リリース用のブランチを作成し、トランクの初期作業を開始できます。ブランチを作成する際には、以下のファイルのバージョン番号を更新する必要があります:

<!--
*   `src/wp-includes/version.php`
*   Both NPM files: `package.json` and `package-lock.json`. **Note:** the `package-lock.json` file must not be edited manually. Change the version specified in `package.json` and run `npm install` to update the lock file.
*   The `composer.json` file.
-->

*   `src/wp-includes/version.php`
*   両方の NPM ファイル: `package.json` と `package-lock.json`。**注意:** `package-lock.json` ファイルは手動で編集しないでください。`package.json` で指定されているバージョンを変更し、`npm install` を実行してロックファイルを更新してください。
*   `composer.json` ファイル。

<!--
When branching before a release, there are two important things that need setting after branching has taken place. Ideally these should be done before any development work on trunk begins.
-->

リリース前にブランチを行う場合、ブランチが行われた後に設定しなければならない重要なことが2つあります。理想的には、これらは trunk での開発作業が始まる前に行うべきです。

<!--
*   API: Set `WP_CORE_DEV_BRANCH` in [/home/wporg/public\_html/.config/versions.php](https://dotorg.trac.wordpress.org/browser/wordpress/website/.config/versions.php) to the branch, for example, 4.9. This is used in the core update check to keep Beta Tester plugin users on the branch development path (instead of pushing them into the super-alpha 5.0).
*   Translate: Update `DEV_BRANCH` in [/home/wporg/public\_html/translate/bin/update-originals-wp.sh](https://dotorg.trac.wordpress.org/browser/wordpress/website/translate/bin/update-originals-wp.sh) to cause GlotPress to know that the “WordPress Development” project should import strings (“originals”) from the branch rather than trunk. This is required to prevent any string changes in trunk affecting the translation files generated. This is often also set following releases for a few weeks while translation efforts continue on the latest stable version of WordPress, and trunk may have many iterations on string changes.
*   Translate: Update [/home/wporg/public\_html/translate/bin/update-all-core-packs.sh](https://dotorg.trac.wordpress.org/browser/wordpress/website/translate/bin/update-all-core-packs.sh) to use the branch for beta/RC packages.
*   Translate: Update [/home/rosetta/public\_html/wp-content/mu-plugins/rosetta/rosetta.php](https://dotorg.trac.wordpress.org/browser/wordpress/rosetta/website/wp-content/mu-plugins/rosetta/rosetta.php) to use the branch for the `wp/dev` project.
-->

<!--
After branching is performed, there are a few additional tasks that need to take place:
-->

ブランチが実行された後、実行する必要がある追加タスクがいくつかあります:

<!--
*   In `trunk`, update the `SECURITY.md` file to include the newly created branch in the list of versions receiving security updates.
*   The `test-old-branches.yml`, `upgrade-testing.yml`, and `upgrade-develop-testing.yml` workflow files need to be updated. As an example, here is a [PR that would update the workflow file after 5.8 is branched](https://github.com/WordPress/wordpress-develop/pull/1199). The needed changes should only be applied to `trunk`. This workflow only runs within the primary branch, so the numbered branches do not need to be updated.
    *   **Note:** Because WP CLI is used in the `upgrade-testing.yml` and `upgrade-develop-testing.yml` workflows, any versions that have not been released yet will be unavailable. Before a version’s final release, use an RC version (`6.7-RC1`, for example), or wait until final release.
*   The `npm run grunt replace:workflow-references-local-to-remote` command should be used to change any local workflow references to remote ones pinned to `trunk` in the new branch. This makes the testing infrastructure more maintainable, ensuring that old branches receive maintenance changes without the need to backport to ever branch (see [#62416](https://core.trac.wordpress.org/ticket/62416)/\[[\[59673\]](https://core.trac.wordpress.org/changeset/59673)).
*   The `.version-support-mysql.json` and `.version-support-php.json` files in `trunk` should be updated to include keys for the new alpha version. Reuse the same set of values as the previous version to start. Any version support policy changes should be made separately.
*   The `.env` and `docker-compose.yml` files in the new branch should be updated. This ensures the local Docker environment continues working and helps avoid test failures in the future when the PHP version associated with the `latest` Docker container is changed.
    *   In the `.env` file, change the `LOCAL_PHP` and `LOCAL_DB_VERSION` values from `latest` to the highest version of PHP/MySQL supported by that release.
    *   In the `docker-compose.yml` file, change the `${LOCAL_PHP-latest}` and `${LOCAL_DB_VERSION-latest}` values to reflect the highest version of PHP/MySQL supported by that release (anything after the `-` is considered the default value).
*   Ensure that new tickets are created in Trac for each of the tickets that encapsulate ongoing improvements throughout each release cycle. These can usually be found by [running a query for ticket summaries that end in the branch version number](https://core.trac.wordpress.org/query?summary=%246.8&order=priority).
    *   Update/Audit NPM Dependencies
    *   GitHub Actions updates and improvements
    *   PHP 8.x: various compatibility fixes
    *   Tests: Reduce usage of assertEquals
    *   Coding Standards fixes
    *   Test tool and unit test improvements
    *   Docblock improvements
    *   Update bundled root certificates
-->

*   `trunk` で、`SECURITY.md` ファイルを更新し、新しく作成したブランチをセキュリティアップデートを受け取るバージョンのリストに追加します。
*   `test-old-branches.yml`、`upgrade-testing.yml`、`upgrade-develop-testing.yml` ワークフローファイルを更新する必要があります。例として、[5.8がブランチされた後にワークフローファイルを更新するプルリクエスト](https://github.com/WordPress/wordpress-develop/pull/1199) を示します。必要な変更は `trunk` にのみ適用する必要があります。このワークフローはプライマリブランチ内でのみ実行されるため、番号付きブランチは更新する必要はありません。
    *   **注意:** `upgrade-testing.yml` および `upgrade-develop-testing.yml` ワークフローでは WP CLI が使用されているため、まだリリースされていないバージョンは利用できません。バージョンの最終リリース前は、RC バージョン (例: 6.7-RC1) を使用するか、最終リリースまでお待ちください。
*   `npm run grunt replace:workflow-references-local-to-remote` コマンドを使用して、ローカルワークフロー参照を、新しいブランチの `trunk` に固定されたリモートワークフロー参照に変更してください。これにより、テストインフラストラクチャの保守性が向上し、古いブランチにメンテナンス変更を適用する際に、ブランチへのバックポートが不要になります ([#62416](https://core.trac.wordpress.org/ticket/62416)/\[[\[59673\]](https://core.trac.wordpress.org/changeset/59673) を参照)。
*   `trunk` 内の `.version-support-mysql.json` ファイルと `.version-support-php.json` ファイルを更新し、新しいアルファ版のキーを含める必要があります。最初は以前のバージョンと同じ値セットを再利用してください。バージョンサポートポリシーの変更は別途行う必要があります。
*   新しいブランチ内の `.env` ファイルと `docker-compose.yml` ファイルを更新する必要があります。これにより、ローカル Docker 環境が引き続き動作し、将来的に `latest` Docker コンテナに関連付けられた PHP バージョンが変更された場合でもテストが失敗するのを防ぐことができます。
    *   `.env` ファイルで、`LOCAL_PHP` と `LOCAL_DB_VERSION` の値を `latest` から、そのリリースでサポートされている PHP/MySQL の最新バージョンに変更します。
    *   `docker-compose.yml` ファイルで、`${LOCAL_PHP-latest}` と `${LOCAL_DB_VERSION-latest}` の値を、そのリリースでサポートされている PHP/MySQL の最新バージョンに変更します (`-` の後の部分はデフォルト値とみなされます)。
*   各リリースサイクルを通じて、継続的な改善をまとめたチケットごとに、Trac に新しいチケットが作成されていることを確認します。これらのチケットは通常、[ブランチのバージョン番号で終わるチケットの概要を検索するクエリを実行する](https://core.trac.wordpress.org/query?summary=%246.8&order=priority)ことによって見つかります。
    *   Update/Audit NPM Dependencies
    *   GitHub Actions updates and improvements
    *   PHP 8.x: various compatibility fixes
    *   Tests: Reduce usage of assertEquals
    *   Coding Standards fixes
    *   Test tool and unit test improvements
    *   Docblock improvements
    *   Update bundled root certificates

<!--
## Pre Final Release
-->

## 最終的なリリースの前に

<!--
This is your pre-release checklist. Do not skip it. To help with coordination, it’s recommended to [duplicate this sheet](https://docs.google.com/spreadsheets/d/1SQov6AK7ZM8O5TbSVlxNEul3HDHzqjANeRW61WTSyG4/edit#gid=546938884) and begin assigning tasks amongst the release squad, along with wider contributors who tend to step in during this part of the release cycle.
-->

これはリリース前のチェックリストです。スキップしないでください。[このシートを複製して](https://docs.google.com/spreadsheets/d/1SQov6AK7ZM8O5TbSVlxNEul3HDHzqjANeRW61WTSyG4/edit#gid=546938884)、調整に役立てることをおすすめします。また、リリースサイクルのこの部分に関係するより広い貢献者たちとともに、リリースチームの間でタスクを割り当て始めることをおすすめします。

<!--
*   Publish a post summarizing the release process for those looking to help and/or follow along ([example from 5.1](https://make.wordpress.org/core/2019/02/21/wordpress-5-1-release-day/)), including a list of general release roles and the contributors assigned to each role.
*   Get the name of the release’s Jazz Musician (reach out to Matt or the current project director).
*   Gather the list of Noteworthy Contributors for the Credits page. [Utilize this template spreadsheet (showing sample data from 5.4) to help capture those users](https://docs.google.com/spreadsheets/d/1sejDx2WcH2XW_i_0PK6qtYzu7Vsh1jrasR1otPmTf1s/edit#gid=246976924). Ensure all Noteworthy Contributors have a photo in Gravatar.
    *   This should include props from Trac, Github, and any non-code props to add manually.
    *   There are sections: All Leads, Noteworthy Contributors (including Core Devs), All Contributors. *Leads and Noteworthy Contributors are compiled manually — ask each focus lead to review your list.*
    *   Ensure that Design leads in the release check for any missing designers as they may have been missed on code props.
*   The Credits API should be updated.
    *   Everyone in the first Noteworthy Contributors section (named `core-developers`, though not limited to developers) should get a Core Team badge.
*   Make sure the tagline is synced in about.php, freedoms.php, and credits.php.
*   Make sure the About page images use CDN URLs and any filler images are properly replaced with the final version.
*   Run the private security unit test suite.
*   The announcement post should be drafted. **DO NOT PUBLISH.**
    *   This is based on the copy from the About Page, but will also include video (if applicable) and props at the end.
    *   To display the list of props in the release post, use this shortcode: `[wpcredits X.Y]`, where X.Y is the release version. It fetches the data from the Credits API, so there is no need to generate a separate list of props for the release post as this will display automatically once the Credits API is updated for the release.
    *   Make sure the post includes a thank you note for support volunteers and translators after core props (see previous major release announcements for an example like [5.6](https://wordpress.org/news/2020/12/simone/)).
    *   Categorize post as “release” *only*, ***not*** as “release” *and* “development”.
    *   Update the tweet if desired, including the hashtag [#WordPress](https://make.wordpress.org/core/tag/wordpress/).
    *   Set a featured image which is used for the link preview when sharing the post. Ensure that previews on Twitter, Facebook, etc. do not crop of significant portions of the image. If need be, you can clear the cache on Facebook using [https://developers.facebook.com/tools/debug/](https://developers.facebook.com/tools/debug/) and on Twitter using [https://cards-dev.twitter.com/validator](https://cards-dev.twitter.com/validator).
    *   Adjust the excerpt.
        *   Append `&embed=true` to the preview URL to ensure the embed looks good.
*   Update the [Browser support page](https://make.wordpress.org/core/handbook/best-practices/browser-support/) if we end support for any browsers.
-->

*   リリースのプロセスをまとめた投稿を、手伝いたい、あるいはフォローしたい人のために公開します ([5.1の例](https://make.wordpress.org/core/2019/02/21/wordpress-5-1-release-day/))。これには、一般的なリリースロールのリストと、各ロールに割り当てられた貢献者が含まれます。
*   リリースのジャズミュージシャンの名前を入手する (Matt か現在のプロジェクトディレクターに連絡を取ります)。
*   クレジットページのために、注目すべき貢献者のリストを集めてください。[これらのユーザーを管理するために、このスプレッドシートのテンプレート (5.4のサンプルデータです) を利用します](https://docs.google.com/spreadsheets/d/1sejDx2WcH2XW_i_0PK6qtYzu7Vsh1jrasR1otPmTf1s/edit#gid=246976924)。すべての注目すべき貢献者が Gravatar で写真を持っていることを確認してください。
    *   これには、Trac や GitHub からの props、そして手動で追加するコード以外の props も含まれるはずです。
    *   セクションがあります: すべてのリード、注目すべき貢献者 (コア開発者を含む)、すべての貢献者。*リードと注目すべき貢献者は手動で編集されます。各フォーカスリードにリストを確認してもらいましょう。*
    *   リリースのデザインリードは、コード props で見逃しているデザイナーがいないか確認してください。
*   クレジット API を更新する必要があります。
    *   最初の注目すべき貢献者セクション (開発者に限らないが、`core-developers` という名前) にいる人全員に Core Team バッジをつけるべきです。
*   about.php、freedoms.php、credits.php でタグラインが同期していることを確認してください。
*   アバウトページの画像が CDN の URL を使っていることと、フィラー画像が最終バージョンに適切に置き換えられていることを確認してください。
*   プライベートなセキュリティ・ユニットテストスイートを実行します。
*   アナウンス投稿は下書きのままであるべきです。**公開しないでください。**
    *   これはアバウトページのコピーにもとづきますが、最後にビデオ (該当する場合) と props も含まれます。
    *   リリース投稿に props のリストを表示するには、次のショートコードを使用してください: `［wpcredits X.Y］`。X.Y はリリースのバージョンです。これはクレジット API からデータを取得するので、リリース投稿のために props のリストを別に生成する必要はありません。
    *   コア props の後に、サポートボランティアと翻訳者への感謝の言葉を投稿に含めるようにしてください ([5.6](https://wordpress.org/news/2020/12/simone/)のような、以前のメジャーリリースのアナウンスの例を参照してください)。
    *   投稿を「release」**および**「development」として**ではなく**、「release」**のみに**分類してください。
    *   ハッシュタグ [#WordPress](https://make.wordpress.org/core/tag/wordpress/) を含むツイートを更新します。
    *   投稿を共有する際にリンクのプレビューに使用されるアイキャッチ画像を設定します。Twitter や Facebook などのプレビューで、画像の大部分が切り取られないようにします。必要であれば、Facebook では [https://developers.facebook.com/tools/debug/](https://developers.facebook.com/tools/debug/)、Twitter では [https://cards-dev.twitter.com/validator](https://cards-dev.twitter.com/validator) を使ってキャッシュをクリアできます。
    *   抜粋文を調整します。
        *   プレビュー URL に `&embed=true` を追加して、埋め込みがうまくいくようにします。
*   いずれかのブラウザーのサポートを終了した場合は、[ブラウザーサポートページ](https://ja.wordpress.org/team/handbook/core/best-practices/browser-support/)を更新します。

<!--
### Dry Run
-->

### ドライラン

<!--
24 hours before the release is scheduled, perform a dry run and walk through these steps:
-->

リリースが予定されている24時間前にドライランを実行し、以下のステップを進めてください:

<!--
*   Triage any bugs reported against trunk, most easily found at the top of [report 40](https://core.trac.wordpress.org/report/40).
*   Update `src/wp-admin/includes/update-core.php`
    *   Check for old files and see if they are in `$_old_files`:
        *   `svn diff --summarize [https://core.svn.wordpress.org/tags/6.1.1](https://core.svn.wordpress.org/tags/4.4) [https://core.svn.wordpress.org/trunk](https://core.svn.wordpress.org/trunk) | grep '^D'`
        *   If the current major has already been branched from `trunk` use `svn diff --summarize [https://core.svn.wordpress.org/tags/6.1.1](https://core.svn.wordpress.org/tags/4.4) [https://core.svn.wordpress.org/branches/6.2](https://core.svn.wordpress.org/trunk) | grep '^D'`
        *   **Note**: Any deleted files from the Requests library should not be noted in `$_old_files`. Instead, they should be added to the `$_old_requests_files` global.
    *   Check for added files with names that are in `$_old_files`. Comment any out in `$_old_files` with the version where it was added back. Do not delete the lines, for the sake of history.
        *   `svn diff --summarize [https://core.svn.wordpress.org/tags/4.4](https://core.svn.wordpress.org/tags/4.4) [https://core.svn.wordpress.org/trunk](https://core.svn.wordpress.org/trunk) | grep '^A'`
        *   If the current major has already been branched from `trunk` use `svn diff --summarize [https://core.svn.wordpress.org/tags/6.1.1](https://core.svn.wordpress.org/tags/4.4) [https://core.svn.wordpress.org/branches/6.2](https://core.svn.wordpress.org/trunk) | grep '^A'`
    *   Check that `$_new_bundled_files` is up to date. This needs to be updated with every new default theme.
    *   **Note:** files removed from default themes should not be listed in `$_old_files`. Those are updated separately from Core updates, so including them is not necessary.
    *   **Note:** When verifying that files are either deleted or added, also consider that many files are “built” and may not appear in the source repo.
*   Run `npm run grunt prerelease`, to ensure all tests pass, and CSS and JS files conform to standards. (this takes a while). *Note: the `imagemin` subtask produces indeterminate results and should be ignored if there are no appreciable file size savings.*
*   Walk through and simulate all Release Day tasks, noting which contributors are responsible for each task.
-->

*   trunk に対して報告されたバグをトリアージします。[report 40](https://core.trac.wordpress.org/report/40)の先頭で簡単に見つけることができます。
*   `src/wp-admin/includes/update-core.php` を更新します。
    *   古いファイルをチェックし、それらが `$_old_files` にあるかどうかを確認します:
        *   `svn diff --summarize [https://core.svn.wordpress.org/tags/4.4](https://core.svn.wordpress.org/tags/4.4) [https://core.svn.wordpress.org/trunk](https://core.svn.wordpress.org/trunk) | grep '^D'`
        *   現在のメジャーがすでに `trunk` からブランチされている場合は、`svn diff --summarize [https://core.svn.wordpress.org/tags/6.1.1](https://core.svn.wordpress.org/tags/4.4) [https://core.svn.wordpress.org/branches/6.2](https://core.svn.wordpress.org/trunk) | grep '^D'` を使ってください。
        *   **注意**: Requests ライブラリから削除されたファイルは `$_old_files` には記録されません。代わりに `$_old_requests_files` グローバルに追加する必要があります。
    *   `$_old_files` 名前のあるファイルが追加されていないかチェックします。追加されたファイルが `$_old_files` にある場合は、追加されたバージョンと一緒にコメントアウトします。履歴のために、その行は削除しないでください。
        *   `svn diff --summarize [https://core.svn.wordpress.org/tags/4.4](https://core.svn.wordpress.org/tags/4.4) [https://core.svn.wordpress.org/trunk](https://core.svn.wordpress.org/trunk) | grep '^A'`
        *   現在のメジャーがすでに `trunk` からブランチされている場合は、`svn diff --summarize [https://core.svn.wordpress.org/tags/6.1.1](https://core.svn.wordpress.org/tags/4.4) [https://core.svn.wordpress.org/branches/6.2](https://core.svn.wordpress.org/trunk) | grep '^A'` を使ってください。
    *   `$_new_bundled_files` が最新かどうかをチェックします。これは新しいデフォルトテーマごとに更新する必要があります。
    *   **注意:** デフォルトテーマから削除されたファイルは `$_old_files` にリストされるべきではありません。これらはコアのアップデートとは別に更新されるので、含める必要はありません。
    *   **注意:** ファイルが削除または追加されたことを確認する際は、多くのファイルが「ビルド」され、ソースリポジトリに表示されない可能性があることも考慮してください。
*   `npm run grunt prerelease` を実行して、すべてのテストが成功し、CSS および JS ファイルが標準に準拠していることを確認してください。(これには少し時間がかかります) **注意: `imagemin` サブタスクは不確定な結果を生成するため、ファイルサイズの大幅な削減が見られない場合は無視してください。**
*   リリース日のすべてのタスクを順に確認し、シミュレーションし、各タスクの担当者をメモしてください。

<!--
### Notify Everyone
-->

### 全員に通知する

<!--
*   Notify hosts that a release is coming.
*   Notify the [polyglots team](https://make.wordpress.org/polyglots/) of string changes.
*   Notify the [systems team](https://make.wordpress.org/systems/) so they can have someone available during release. If you aren’t sure how best to do this, ask your release squad if anyone is a part of this team.
-->

*   リリースが近付いていることをホストに通知します。
*   文字列の変更を [polyglots チーム](https://make.wordpress.org/polyglots/)に通知します。
*   [システムチーム](https://make.wordpress.org/systems/)に通知して、リリース中に誰かが対応できるようにします。どのようにするのがベストかわからない場合は、リリースチームにこのチームに誰がいるのかを尋ねてください。

<!--
## Release Day
-->

## リリース日

<!--
You’ve made it to release day!
-->

リリース日に間に合いました !

<!--
### Core
-->

### コア

<!--
1.  Ensure the top of [report 40](https://core.trac.wordpress.org/report/40) is triaged, preferably clear.
2.  Alert committers about the release and to pause committing:
    1.  Example: @committers Please refrain from committing until we get 5.8 released.
3.  If applicable, make the final commit to `about.php`, e.g. to include a release video or update final illustrations.
4.  Verify `package.json` is updated.
5.  Verify `src/wp-admin/includes/update-core.php`.
6.  *If there is a new default theme*, verify:
    1.  `WP_DEFAULT_THEME` in `src/wp-includes/default-constants.php`
    2.  `WP_Theme::$default_themes` in `src/wp-includes/class-wp-theme.php`
    3.  **Very important:** `WP_CORE_NEW_BUNDLED_VERSION` in `/home/wporg/public_html/.config/versions.php`
7.  Run unit tests.
8.  Run `npm run grunt prerelease`. This will also run the unit tests. Check for result of GitHub Actions (e.g., [https://github.com/WordPress/wordpress-develop/actions?query=branch%3A5.8](https://github.com/WordPress/wordpress-develop/actions?query=branch%3A5.8)).
9.  Update version in `src/wp-includes/version.php` to remove the RC identifier and changeset – eg. `5.3-src`.
10.  Tag the release. From branch:
    `svn copy https://develop.svn.wordpress.org/branches/4.7 https://develop.svn.wordpress.org/tags/4.7 -m "Tag 4.7"`
    If this command line fails, then attempt the same tag via a GUI interface such as TortoiseSVN.
11.  Create release packages via the form at mc.wordpress.org.
12.  Share in Slack: “Just a reminder: Do not tweet or share on any social media any of the links for the release. Sometimes things go wrong and packages need to be rebuilt. The release is not official until the post is published on the official news blog.”
-->

1.  [report 40](https://core.trac.wordpress.org/report/40)の先頭がトリアージされおり、クリアであることを確認します。
2.  コミッターに、リリースについて通知し、コミットを一時停止するよう警告します:
    1.  例: @committers 5.8がリリースされるまでコミットを控えてください。
3.  該当する場合、`about.php` に最終コミットをします。たとえば、リリースビデオを入れたり、最終イラストを更新したりします。
4.  `package.json` が更新されていることを確認してください。
5.  `src/wp-admin/includes/update-core.php` を確認します。
6.  **新しいデフォルトテーマ**がある場合は、以下を確認します:
    1.  `src/wp-includes/default-constants.php` の `WP_DEFAULT_THEME` を確認します。
    2.  `src/wp-includes/class-wp-theme.php` にある `WP_Theme::$default_themes` を確認します。
    3.  **非常に重要:** `/home/wporg/public_html/.config/versions.php` の中の `WP_CORE_NEW_BUNDLED_VERSION`
7.  ユニットテストを実行します。
8.  `npm run grunt prerelease` を実行します。これでユニットテストも実行されます。GitHub Actions の結果を確認します (例: [https://github.com/WordPress/wordpress-develop/actions?query=branch%3A5.8](https://github.com/WordPress/wordpress-develop/actions?query=branch%3A5.8))。
9.  `src/wp-includes/version.php` のバージョンを更新し、RC 識別子とチェンジセットを削除します – 例: `5.3-src`。
10.  リリースにタグを付けます。ブランチから:
    `svn copy https://develop.svn.wordpress.org/branches/4.7 https://develop.svn.wordpress.org/tags/4.7 -m "Tag 4.7"`
    このコマンドラインで失敗した場合は、TortoiseSVN などの GUI インターフェースで同じタグ付けを試みてください。
11.  mc.wordpress.org のフォームからリリースパッケージを作成します。
12.  Slack で共有する:「念のため: リリースのリンクをツイートしたり、ソーシャルメディアで共有したりしないでください。時には物事がうまくいかず、パッケージの再構築が必要になることがあります。公式ニュースブログに投稿が掲載されるまでは、リリースは正式なものではありません。」

### WordPress.org

<!--
1.  Check packages are showing up at [https://wordpress.org/download/releases/](https://wordpress.org/download/release-archive/).
2.  Download and unzip/untar packages. Verify they are the same. Check MD5 sums.
3.  Test the packages:
    1.  There are two ways to help test the package:
        1.  Use WP-CLI to test: `wp core update https://wordpress.org/wordpress-5.8.zip`
        2.  Directly download the Beta/RC version (e.g., [https://wordpress.org/wordpress-5.8.zip](https://wordpress.org/wordpress-5.8.zip))
    2.  In particular, testing the following types of installs and updates would be much appreciated:
        1.  Does a new WordPress install work correctly? This includes running through the manual install process, as well as WP-CLI or one-click installers.
        2.  Test upgrading from 4.0.33, 4.9.18, 5.7.2, and 5.8 RC 4 as well as any other versions possible.
        3.  Remove `wp-config.php` file and test fresh install.
        4.  Test single site and multisite/network (both subdirectory and subdomain) installs.
        5.  Does it upgrade correctly? Are the [files listed in `$_old_files`](https://core.trac.wordpress.org/browser/branches/5.8/src/wp-admin/includes/update-core.php#L21) removed when you upgrade?
        6.  Does Multisite upgrade properly?
    3.  Finally the following user flows, on desktop and mobile, would be great to validate work as expected:
        1.  Publish a post, including a variety of different blocks.
        2.  Comment on the post.
        3.  Install a new plugin/theme, or upgrade an existing one.
        4.  Change the site language.
        5.  If you’re a plugin developer, or if there are complex plugins you depend upon, test that they’re working correctly.
4.  Privately take a final screenshot of [the downloads counter](https://wordpress.org/download/counter/). *Note: This is done privately to prevent a flood of screenshots during the release party.*
5.  Bump versions in `.config/versions.php`. (Do this on a WordPress.org sandbox so you can test update notifications before deploying.)
    
    *   Switch `WP_CORE_DEV_BRANCH` back to `trunk` if it was set to the branch during RC.Bump `WP_CORE_STABLE_BRANCH` if this is a major release.
    
    *   Bump `WP_CORE_LATEST_RELEASE`.
    *   Bump `WP_CORE_NEW_BUNDLED_VERSION` if there is a new default theme. **Important.**
    *   Update `wporg_get_secure_versions()` with the previous secure stable release, used by [an API endpoint used by Google Webmasters Tools](https://api.wordpress.org/core/stable-check/1.0/).
    *   Update `wporg_get_version_equivalents()` if required, used by the plugin directory.
    *   Automatic updates will commence once these changes are deployed – See the final step #8.
6.  Update the [relevant credits file](https://meta.trac.wordpress.org/browser/sites/trunk/api.wordpress.org/public_html/core/credits), and deploy the changes.
7.  Build language packs for the release by bumping versions in `translate/bin/update-all-core-packs.sh`.
8.  Deploy WordPress.org, `deploy-dotorg.sh wporg` from a sandbox.
-->

1.  [https://wordpress.org/download/releases/](https://wordpress.org/download/release-archive/) にパッケージが表示されていることを確認します。
2.  パッケージをダウンロードし、解凍します。同じパッケージであることを確認し、MD5サムをチェックします。
3.  パッケージをテストします:
    1.  パッケージのテストには2つの方法があります:
        1.  WP-CLI を使ってテストする: `wp core update https://wordpress.org/wordpress-5.8.zip`
        2.  ベータ版/RC 版を直接ダウンロードする (例: [https://wordpress.org/wordpress-5.8.zip](https://wordpress.org/wordpress-5.8.zip))
    2.  特に、以下のタイプのインストールとアップデートをテストすると良いでしょう:
        1.  WordPress の新規インストールは正しく動作しますか ? これには、WP-CLI やワンクリックインストーラだけでなく、手動インストールプロセスの実行も含まれます。
        2.  4.0.33、4.9.18、5.7.2、5.8 RC4、およびその他のバージョンからのアップグレードをテストしてください。
        3.  `wp-config.php` ファイルを削除し、新規インストールをテストします。
        4.  シングルサイトとマルチサイト/ネットワーク (サブディレクトリとサブドメインの両方) のインストールをテストします。
        5.  正しくアップグレードされていますか ? アップグレード時に、[`$_old_files` にリストされているファイル](https://core.trac.wordpress.org/browser/branches/5.8/src/wp-admin/includes/update-core.php#L21)は削除されていますか ?
        6.  マルチサイトは正しくアップグレードされますか ?
    3.  最後に、デスクトップとモバイルの以下のユーザーフローが期待通りに動作することを検証すると良いでしょう:
        1.  さまざまなブロックを含む投稿を公開する。
        2.  投稿にコメントする。
        3.  新しいプラグイン/テーマをインストールするか、既存のものをアップグレードする。
        4.  サイトの言語を変更する。
        5.  あなたがプラグイン開発者である場合、またはあなたが依存している複雑なプラグインがある場合、それらが正しく動作していることをテストします。
4.  [ダウンロードカウンター](https://wordpress.org/download/counter/)の最後のスクリーンショットを非公開で撮影します。**注意: リリースパーティー中にスクリーンショットが大量に投稿されるのを防ぐため、非公開で撮影します。**
5.  `.config/versions.php` のバージョンを上げます。(デプロイする前に更新通知をテストできるように、WordPress.org のサンドボックス上で行ってください)。

    * RC 中にブランチに設定されていた場合は、`WP_CORE_DEV_BRANCH` を `trunk` に戻します。メジャーリリースの場合は、`WP_CORE_STABLE_BRANCH` を更新します。

    * `WP_CORE_LATEST_RELEASE` を更新します。
    * 新しいデフォルトテーマがある場合は `WP_CORE_NEW_BUNDLED_VERSION` を更新します。**これは重要です。**
    * `wporg_get_secure_versions()` を、[Google ウェブマスターツールで使用される API エンドポイント](https://api.wordpress.org/core/stable-check/1.0/)で使用される以前のセキュアな安定版リリースで更新します。
    * プラグインディレクトリで使用される `wporg_get_version_equivalents()` を必要に応じて更新してください。
    * これらの変更がデプロイされると、自動アップデートが開始されます - 最後のステップ #8 を参照してください。
6.  [関連するクレジットファイル](https://meta.trac.wordpress.org/browser/sites/trunk/api.wordpress.org/public_html/core/credits)を更新し、変更をデプロイします。
7.  リリース用の言語パック、`translate/bin/update-all-core-packs.sh` でバージョンを上げてビルドします。
8.  サンドボックスから `deploy-dotorg.sh wporg` を実行して、WordPress.org をデプロイします。

<!--
### Tell the World
-->

### 世界に伝える

<!--
1.  (Publish the release video on WordPress.TV. **DO NOT Publicize**. Un-check the publicize button so the release video does not go out on Twitter/Facebook.)
2.  Publish announcement on wordpress.org/news.
    1.  Update the slug to include only the name of the release jazzer, not the release number.
3.  Open an Amplication request with the Marketing team’s GitHub to send announcement out to social networks.
4.  Publish the [HelpHub release page](https://wordpress.org/support/wordpress-version/version-5-2/).
5.  Update [WordPress Versions](https://wordpress.org/documentation/article/wordpress-versions/) page.
    1.  Add:  
        `{{ ReleaseTableMajor | version = 4.4  | date = December 8, 2015 | musician = Clifford Brown | blog = https://wordpress.org/news/2015/12/clifford/  | db = 35700 }}`
    2.  Remove the version from the “Planned Versions” section.
6.  Update [PHP Compatibility and WordPress Versions](https://make.wordpress.org/core/handbook/contribute/php-compatibility-and-wordpress-versions/) table.
7.  Update [PHPUnit Compatibility and WordPress Versions](https://make.wordpress.org/core/handbook/references/phpunit-compatibility-and-wordpress-versions/) table.
-->

1.  (リリースビデオを WordPress.TV に投稿します。**ただし、公開しないでください。** Twitter や Facebook に公開しないよう、公開ボタンのチェックを外してください)
2.  wordpress.org/news でお知らせを公開します。
    1.  リリース番号ではなく、リリースジャズミュージシャンの名前のみを含めスラッグを更新します。
3.  マーケティング チームの GitHub で Amplication リクエストを開き、ソーシャル ネットワークにアナウンスを送信します。
4.  [HelpHub リリースページ](https://wordpress.org/support/wordpress-version/version-5-2/)を公開します。
5.  [WordPress バージョン](https://codex.wordpress.org/WordPress_Versions)ページを更新します。
    1.  以下を追加します:
        `{{ ReleaseTableMajor | version = 4.4  | date = December 8, 2015 | musician = Clifford Brown | blog = https://wordpress.org/news/2015/12/clifford/  | db = 35700 }}`
    2.  「予定されているバージョン」セクションからバージョンを削除します。
6.  [PHP の互換性と WordPress のバージョン](https://ja.wordpress.org/team/handbook/core/contribute/php-compatibility-and-wordpress-versions/)テーブルを更新します。
7.  [PHPUnit の互換性と WordPress のバージョン](https://ja.wordpress.org/team/handbook/core/references/phpunit-compatibility-and-wordpress-versions/)を更新します。

<!--
*   Stare at [download counter](https://wordpress.org/download/counter/) and rejoice.
-->

*  [ダウンロードカウンター](https://wordpress.org/download/counter/)を見つめて楽しみましょう。

<!--
## Post Release
-->

## リリース後

<!--
*   Bump the branch version to `X.Y.1-alpha-$REVNUM-src` and trunk to `X.Y+1-alpha-$REVNUM-src` along with the corresponding `package.json`,  `package-lock.json`, and `composer.json` changes. Assuming the next release lead has commit privileges, they should be given the honors of the trunk bump. Example commit from the 6.3 release: [https://core.trac.wordpress.org/changeset/55611](https://core.trac.wordpress.org/changeset/55611).

*   Force nightly builds. (Note: Checksums aren’t available for the nightly. WP-CLI grabs the checksums for both the installed version and the version you’re upgrading to, so it can remove old files.)

*   In Trac, rename the `trunk` version to `X.Y` and create a new one for trunk. Complete the `X.Y` milestone and create new milestones for the new cycle and `X.Y.1`. This must be done by a Trac admin.

*   In Trac, if there is an unreleased minor milestone for the previous major, update the milestone to the new `X.Y` (for tickets already resolved and included in the `X.Y` branch) or `X.Y.1` (for tickets that still need investigation or discussion). A Trac admin should then remove the unreleased minor milestone.
    
    *   *   Update various parts of the documentation:
            *   The current release sidebar on [make.wordpress.org/core](https://make.wordpress.org/core/).Update [make.wordpress.org/core/reports](https://make.wordpress.org/core/reports/) to modify the ‘Next Major Release’ version.  
                ***Note**: Edit using the Gutenberg Code editor, otherwise Dashicons will be stripped.*Update [wordpress.org/about/roadmap](https://wordpress.org/about/roadmap/) and [wordpress.org/about/history](https://wordpress.org/about/history/), removing the new release from the list of upcoming releases, adding the jazzer, and adding the release date. Follow [this process to update content on wordpress.org](https://make.wordpress.org/meta/handbook/about/projects/wordpress-org/updating-content-on-wordpress-org/).
    
    *   *   *   Update [wordpress.org/documentation/article/history](https://wordpress.org/documentation/article/history/).
            *   The dev cycle docs (ex. https://make.wordpress.org/core/x-x/).
            *   Update the sticky thread at the top of [https://wordpress.org/support/forum/how-to-and-troubleshooting/](https://wordpress.org/support/forum/how-to-and-troubleshooting/).
            *   Run `wp devhub parse --url=developer.wordpress.org` on a wordpress.org sandbox. That will update [the DevHub code reference](https://developer.wordpress.org/reference/) docs to parse the latest stable Core release.
    

*   Don’t forget the polyglots team! Share the code version of the release post on the [#polyglots](https://make.wordpress.org/core/tag/polyglots/) channel so they can translate it easily. Open the release post in the editor, then go to Settings > Copy all content. Paste it as a snippet in the [#polyglots](https://make.wordpress.org/core/tag/polyglots/) channel on Slack.

*   Identify folks who helped with significant testing during the release process and submit them for additions to the Credits API if they were not already credited in the release. This can be done via a Meta Trac ticket.

*   During the week following the release:
    
    *   *   Publish a retrospective post if desired.
    
    *   *   Check in with the [Support Team](https://make.wordpress.org/support/) for any notable issues.
    
    *   *   Check in with the [Community Team](https://make.wordpress.org/community/) for any community feedback.
    
    *   *   Kick off the next cycle with the next lead.
    
-->

*   ブランチのバージョンを `X.Y.1-alpha-$REVNUM-src` に、trunk のバージョンを `X.Y+1-alpha-$REVNUM-src` に更新し、対応する `package.json` と `package-lock.json`、`composer.json` の変更も一緒に更新します。次のリリースのリードがコミット権限を持っている場合は、trunk を更新する栄誉が与えられるべきです。6.3リリースのコミット例: [https://core.trac.wordpress.org/changeset/55611](https://core.trac.wordpress.org/changeset/55611)。
*   ナイトリービルドを強制します。(注意: ナイトリービルドではチェックサムは利用できません。WP-CLI は、インストールされているバージョンとアップグレード先のバージョンの両方のチェックサムを取得するので、古いファイルを削除できます)。
*   Trac で `trunk` バージョンの名前を `X.Y` に変更し、trunk 用の新しいバージョンを作成します。`X.Y` のマイルストーンを完成させ、新しいサイクルと `X.Y.1` の新しいマイルストーンを作成します。これは Trac の管理者が行う必要があります。
*   Trac では、前のメジャーに対して未リリースのマイナーマイルストーンがある場合、マイルストーンを新しい `X.Y` (すでに解決され `X.Y` ブランチに含まれるチケットの場合) または `X.Y.1` (まだ調査や議論が必要なチケットの場合) に更新します。Trac 管理者は未リリースのマイナーマイルストーンを削除してください。
*   ドキュメントのさまざまな部分を更新してください:
    *   [make.wordpress.org/core](https://make.wordpress.org/core/) のサイドバーにある現在のリリース。
    *   [make.wordpress.org/core/reports](https://make.wordpress.org/core/reports/) を更新して「次のメジャーリリース」のバージョンを変更します。
        **注意: Gutenberg コードエディターを使用して編集します。そうしないと、ダッシュアイコンが削除されます。**
    *   [wordpress.org/about/roadmap](https://wordpress.org/about/roadmap/) と [wordpress.org/about/history](https://wordpress.org/about/history/) を更新し、今後のリリースリストから新しいリリースを削除し、ジャズミュージシャンを追加し、リリース日を追加します。[wordpress.org のコンテンツを更新するには、このプロセスに従ってください](https://make.wordpress.org/meta/handbook/about/projects/wordpress-org/updating-content-on-wordpress-org/)。
    *   [wordpress.org/support/article/history](https://wordpress.org/support/article/history/) を更新します。
    *   [wordpress.org/support/article/wordpress-versions](https://wordpress.org/support/article/wordpress-versions/) を更新します。
    *   [https://wordpress.org/support/](https://wordpress.org/support/) のトップページにある「Getting Started」の最新リリースを更新します。
    *   [https://wordpress.org/support/forum/how-to-and-troubleshooting/](https://wordpress.org/support/forum/how-to-and-troubleshooting/) のトップにある固定スレッドを更新します。
    *   wordpress.org のサンドボックスで `wp devhub parse --url=developer.wordpress.org` を実行します。これで [DevHub コードリファレンス](https://developer.wordpress.org/reference/)のドキュメントが最新の安定版コアリリースを解析するように更新されます。
*   Polyglots チームを忘れないでください ! リリース投稿のコードバージョンを [#polyglots](https://make.wordpress.org/core/tag/polyglots/) チャンネルで共有し、彼らが簡単に翻訳できるようにしましょう。リリース投稿をエディターで開き、設定 > すべてのコンテンツをコピーに進みます。Slack の [#polyglots](https://make.wordpress.org/core/tag/polyglots/) チャンネルにスニペットとして貼り付けます。
*   リリースの過程で重要なテストを手伝ってくれた人たちを特定し、まだクレジットされていない場合はクレジット API に追加するために登録してください。これは Meta Trac チケットで行うことができます。
*   リリースの翌週に:
    *   必要であれば、ふりかえりの記事を掲載します。
    *   [サポートチーム](https://make.wordpress.org/support/)に、目立った問題がないか確認します。
    *   [コミュニティチーム](https://make.wordpress.org/community/)に、コミュニティからのフィードバックを確認します。
    *   次のリードで次のサイクルを開始します。

<!--
**Congratulations! You did it!**
-->

**おめでとうございます ! やり遂げました !**

[#core](https://make.wordpress.org/core/tag/core/)
