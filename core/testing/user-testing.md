<!--
# User Testing
-->

# ユーザーテスト

<!--
When you conduct user testing, you are measuring to see if the feature or patch accomplishes its intended purpose.
-->

ユーザーテストを実施する場合、機能やパッチが意図した目的を達成しているかどうかを確認します。

<!--
The types of user testing that WordPress needs help with are:
-->

WordPress がサポートを必要としているユーザーテストの種類は以下の通りです:

<!--
1.  Manually testing new features yourself
2.  Testing those same features with other users
-->

1.  新しい機能を手動でテストする
2.  他のユーザーと同じ機能をテストする

<!--
## Before You Test
-->

## テストの前に

<!--
1.  Setup a test site either [locally](https://make.wordpress.org/core/handbook/tutorials/installing-a-local-server/) or with your web hosting provider
2.  Install the [WordPress Beta Tester](https://wordpress.org/plugins/wordpress-beta-tester/) plugin
3.  Find a [feature](https://make.wordpress.org/core/features/) or [patch](https://core.trac.wordpress.org/tickets/needs-testing) to test
4.  Make sure you know the intended purpose of the feature
5.  Install the feature or patch you want to test onto your test site
6.  Make sure to reset the test site between every test
-->

1.  [ローカル](https://make.wordpress.org/core/handbook/tutorials/installing-a-local-server/)または Web ホスティングプロバイダでテストサイトをセットアップする
2.  [WordPress Beta Tester](https://wordpress.org/plugins/wordpress-beta-tester/) プラグインをインストールする
3.  テストする[機能](https://make.wordpress.org/core/features/)または[パッチ](https://core.trac.wordpress.org/tickets/needs-testing)を見つける
4.  機能の意図された目的を確認する
5.  テストしたい機能やパッチをテストサイトにインストールする
6.  テストのたびにテストサイトをリセットする

<!--
## Do a Walk-through
-->

## ウォークスルーを実行する

<!--
With the end goal in mind, do a walk-through of the feature and take notes as you go, or record your session and take notes when you play it back. If you are testing a feature early in the design process, more open-ended suggestions and potential points of confusion are appropriate to note. If you are testing a feature later in the development process, then your main focus should be to look for blockers in the design decisions that have already been made.
-->

最終目標を念頭に置いて、機能のウォークスルーを行い、その都度メモを取るか、セッションを録音して再生時にメモを取ります。設計プロセスの初期段階で機能をテストする場合は、より自由な提案や潜在的に混乱するポイントをメモすることが適切です。開発プロセスの後半で機能をテストする場合、主な焦点は、すでに行われた設計上の決定の阻害要因を探すことです。

<!--
One of the fastest and easiest ways to write up a task list for usability testing is to find out the feature’s end goal and then do a walk-through yourself. Take notes as you go through each step, or record the walk-through and then write down the steps when you play back the video. This will also help you set an expectation for how long the test may take others.
-->

ユーザビリティテスト用のタスクリストを作成する最も速くて簡単な方法の一つは、機能の最終目標を見つけ、自分でウォークスルーを行うことです。各ステップを進めるときにメモを取るか、ウォークスルーを録画し、ビデオを再生するときにステップを書きとめます。これは、他の人がテストにかかる時間を予想することにも役立ちます。

<!--
If you use any assistive technologies, such as JAWS or any other screen reading software, testing using those would be a great addition to user testing.
-->

JAWS やその他のスクリーンリーダーソフトウェアなどの支援技術を使用している場合、それらを使用したテストをユーザーテストに加えることもよいでしょう。

<!--
## Write a Task List
-->

## タスクリストを書く

<!--
Start with a specific scenario. These are imaginary situations that help people get into the right mindset for completing a task. Feel free to have fun with it! Choose a scenario that mimics the real world as much as possible, so that people can engage with the tasks as if they are real. Here is an example:
-->

具体的なシナリオから始めます。これらは、ユーザーがタスクを完了するための正しい考え方を身に着けることに役立つ想像上の状況です。気軽に楽しんでください ! 現実であるかのようにタスクに取り組めるように、できるだけ現実の世界を模倣したシナリオを選びます。以下に例を示します:

<!--
> You’re setting up a website for a new department. You need to set some people up so they can add content, and others will need to be able to submit content that must be reviewed before it can be published.
-->

> あなたは新しい部門の Web サイトを立ち上げてようとしています。一部のユーザーがコンテンツを追加できるように設定する必要があり、他のユーザーは公開前にレビューが必要なコンテンツを送信できるようにする必要があります。

<!--
Tasks should be realistic and clearly written without describing the steps in too much detail. Use language you think would be used by users, and avoid giving clues like specific words used on the site. You’ll also want to avoid asking people what they “think,” because you want to focus on what they actually do and not what they think they might do.
-->

タスクは、手順をあまり詳細に説明せずに、現実的で明確に記述する必要があります。ユーザーが使いそうな言葉を使用し、サイトで使用されている特定の単語などのヒントを与えることは避けてください。また、ユーザーが行おうとしていることではなく、実際に何をしているかに焦点を当てたいため、ユーザーに「どう思う」かを尋ねることも避けたほうがよいでしょう。

<!--
*   Goal: Look up a user role.
*   Poor task: You want to see the role for your co-worker. Go to the website, sign in, and tell me where you would click to find user roles.
*   Better task: Look up the rights for your co-worker, Sally, to make sure she is able to publish new content.
-->

*   目標: ユーザーの役割を調べます。
*   良くないタスク: 同僚の役割を確認したいと考えています。Web サイトにアクセスしてサインインし、ユーザーの役割を見つけるためにクリックしようとしている場所を教えてください。
*   より良いタスク: 同僚のサリーの権限を調べて、彼女が新しいコンテンツを公開できることを確認します。

<!--
## Test with Other Users
-->

## 他のユーザーとテストする

<!--
Choose a location where you are likely to find your target audience. WordPress meetup groups are a great resource. Another potential source of volunteer testers is your local WordCamp, where people can sign up to help test during breaks—ask your local WordCamp organizers if they have space for a breakout area for user testing. Some people also find testers at coffee shops.
-->

対象ユーザーが見つかりそうな場所を選びましょう。WordPress の Meetup グループはすばらしいリソースです。ボランティアテスターのもう一つの潜在的なソースは、休憩中にテストを手伝うためにサインアップできるローカルの WordCamp です。ユーザーテスト用のブレークアウトエリアのスペースがあるかどうか、ローカルの WordCamp 主催者に問い合わせてください。コーヒーショップでテスターを見つける人もいます。

<!--
It is common to compensate users for their time, though many WordPress contributors will volunteer their time if you ask up front. At meetup groups, buying food like snacks or pizza for the group can be a good incentive for adding some time to the meetup for testing. When testing, don’t underestimate the power of chocolate, or offering to cover the cost of a cup of coffee in exchange for a few minutes of their time. Giving a small gift card is reasonable for a short test. Longer tests should be paid. If you don’t have a budget for testing, consider asking your local WordPress group if they might be able to work with you to raise money for user research.
-->

多くの WordPress 貢献者は、前もってお願いすればボランティアで時間を提供してくれますが、ユーザーには時間に対する報酬を支払うことが一般的です。Meetup グループでは、グループのためにスナックやピザなどの食べ物を提供することが、Meetup にテストのための時間を追加する良いインセンティブになるかもしれません。テストをするときは、チョコレートの力を過小評価してはいけないし、数分の時間と引き換えにコーヒー一杯の費用を負担すると申し出ることもできます。短時間のテストであれば、少額のギフトカードを贈ることが良いでしょう。より長いテストには料金が支払われるべきです。テストのための予算がない場合は、ローカルの WordPress グループに、ユーザー調査のための資金を集めるために協力してもらえないか問い合わせることを検討してください。

<!--
When conducting a test, encourage users to think out loud and either record their onscreen interactions with a tool such as QuickTime or take notes during the test. Try not to be leading or answer questions. Just pay close attention to what they do onscreen as they think aloud and find their way through the tasks. Your goal should be to take out as much bias as possible and pay attention to what you can observe someone doing.
-->

テストを実施するときは、考えていることを口に出してもらい、QuickTime などのツールで画面上の操作を録画するか、テスト中にメモを取るようにしましょう。誘導したり、質問に答えたりしないようにしてください。ユーザーが声に出して考え、タスクを解決する方法を見つけるときに、画面上で何をするかに細心の注意を払ってください。あなたの目標は、バイアスをできるだけ排除し、相手の行動を注意深く観察することです。

<!--
## Reporting Results
-->

## 結果を報告する

<!--
Whether you are reporting results from a walkthrough or from a test with another user, the most valuable results you can report are bugs that block you from completing the goal or trends about pain points and satisfaction rates. A short “Top 5” list of bugs and pain points should be at the top of any report followed by notes, personal suggestions (labeled personal as they may have bias), and details of the test.
-->

ウォークスルーの結果を報告する場合でも、他のユーザーとのテストの結果を報告する場合でも、報告できる最も価値のある結果は、目標の達成を妨げるバグや、問題点や満足度に関する傾向です。バグと問題点の短い「トップ5」リストがレポートの先頭にあり、その後にメモ、個人的な提案 (バイアスがあるかもしれないため個人的なラベルが付けらます)、およびテストの詳細が続きます。

<!--
If you recorded a video, it’s helpful to include a link to it in your report or a highlight reel if you have tested with several people.
-->

ビデオを録画した場合は、そのリンクや、複数人でテストした場合はビデオクリップのハイライトをレポートに含めると便利です。
