<!--
# New User Quick Start Guide
-->

# 新規ユーザー向けのクイックスタートガイド

<!--
## Who should use this guide?
-->

## 誰がこのガイドを使うべきですか ?

<!--
If you are a developer who wants to contribute to WordPress core for the first time, this guide is designed to help you navigate and use [Trac](https://make.wordpress.org/core/handbook/contribute/trac/). This is meant as a high level overview to get you started quickly. This page should guide you through some overall knowledge you will need before contributing, the basic steps of working on a ticket and finally the layout of a Trac ticket. We highly encourage you to consult the [core handbook](https://make.wordpress.org/core/handbook/contribute/trac/) and [tutorials](https://make.wordpress.org/core/handbook/tutorials/working-with-patches/) to learn how to use Trac more thoroughly.
-->

あなたが初めて WordPress コアに貢献したい開発者なら、このガイドは [Trac](https://make.wordpress.org/core/handbook/contribute/trac/) をナビゲートして使用するためのものです。これは、あなたがすぐに始められるように、ハイレベルな概要として意図されています。このページは、貢献する前に必要ないくつかの全体的な知識、チケットの作業の基本的なステップ、そして最後に Trac チケットのレイアウトを案内するものです。Trac の使い方をより深く学ぶために、[コアハンドブック](https://make.wordpress.org/core/handbook/contribute/trac/)と[チュートリアル](https://make.wordpress.org/core/handbook/tutorials/working-with-patches/)を参照することを強くおすすめします。

<!--
We are going to assume you already have a [WordPress.org account](https://login.wordpress.org/register), have thoroughly read [https://core.trac.wordpress.org/](https://core.trac.wordpress.org/), and already have access to the [make.wordpress.org Slack](https://chat.wordpress.org/) workspace, which is where you can ask for guidance and assistance.
-->

ここでは、すでに [WordPress.org アカウント](https://login.wordpress.org/register) を持っており、[https://core.trac.wordpress.org/](https://core.trac.wordpress.org/) を熟読され、ガイダンスやサポートを求めることができる [make.wordpress.org の Slack](https://chat.wordpress.org/) ワークスペースにすでにアクセスされていると想定しています。

<!--
## What You Should Know Before Getting Started
-->

## 始める前に知っておくべきこと

<!--
### Trac Functionalities
-->

### Trac の機能

<!--
Trac is an open source, web-based project management and bug tracking system. It is used by many parts of the WordPress project, including Core, Meta and Theme Review. Trac is based on working in tickets. Contributors leverage the tool to find tickets in need of work, monitor progress on open tickets, contribute patches for WordPress core.
-->

Trac はオープンソースであり、Web ベースのプロジェクト管理およびバグ追跡システムです。コア、メタ、テーマレビューを含む WordPress プロジェクトの多くの部分で使用されています。Trac はチケットで作業することを基本としています。貢献者は、作業が必要なチケットの発見、オープンチケットの状況の監視、WordPress コアへのパッチの貢献などにこのツールを活用します。

<!--
### How Core Contributors Communicate With Trac
-->

### コアコントリビューターが Trac でどのようにコミュニケーションをとっているか

<!--
Trac is the official record of work for WordPress core. The tickets written here become part of the living historical document of open source contributions. Because of this, the tone and language used in tickets and comments should be formal and to the point.
-->

Trac は WordPress コアで行われた作業の公式な記録です。ここに書かれたチケットは、オープンソースへの貢献に関する生きた歴史的な文書の一部となります。このため、チケットやコメントで使用されるトーンや言語は、フォーマルで要点を押さえたものであるべきです。

<!--
Because this is the official record, be sure to search thoroughly to see if there is an existing ticket for the bug or feature you want to log. If something already exists, please add your notes to that existing ticket. If what you have to add is related to an existing item or for something with a finished milestone, reference that ticket using the format #{ticket\_id} to automatically create a link between tickets: “This was previously discussed in [#99999](https://core.trac.wordpress.org/ticket/99999).” If you need to refer to a particular changeset (a set of code changes logged in Trac), you can link to it using the format \[{changeset\_id}\]: “The original bug was fixed in \[999999\].” Note, finished milestone tickets should never be reopened.
-->

これは公式な記録であるため、記録したいバグや機能のチケットが存在しないかどうか、十分に検索してください。すでにある場合は、その既存のチケットにあなたのメモを追加してください。もし、あなたが追加しなければならないことが、既存のアイテムに関連していたり、マイルストーンが終了しているものであれば、チケット間のリンクを自動的に作成するために、#{ticket_id} というフォーマットを使ってそのチケットを参照してください:「これは以前 [#99999](https://core.trac.wordpress.org/ticket/99999) で議論されました。」特定のチェンジセット (Trac に記録されたコード変更のセット) を参照する必要がある場合、[{changeset_id}}] というフォーマットでリンクできます:「元のバグが修正されたのは[999999]です。」なお、終了したマイルストーンチケットは決して再オープンしてはいけません。

<!--
Please remember contributors are volunteers and this process takes time. Patience is always appreciated.
-->

貢献者はボランティアであり、このプロセスには時間がかかることを覚えておいてください。

<!--
## Working On Open Trac Tickets
-->

## オープンな Trac チケットでの作業

<!--
1.  Find a ticket ready for work by using [https://make.wordpress.org/core/reports/](https://make.wordpress.org/core/reports/)
2.  Check the attachments and see of there is a current patch being suggested.
3.  If no patch exists, time to replicate the scenario and [add a new patch](https://make.wordpress.org/core/handbook/tutorials/working-with-patches/).
4.  If there is a patch, it likely needs to be reviewed and tested, the comments will reveal the current status of things. Download the patch and test in your development environment. If works as expected, please provide appropriate feedback.
5.  If you make changes to the patch, please provide a link to the Diff (https://make.wordpress.org/themes/handbook/review/working-with-trac/#comparing-ticket-updates) as well as comment.
6.  Always leave a comment on the ticket describing what you changed and why you changed it. A patch upload itself does not trigger a notification. Please use \[attachment:{filename}\] in a comment to link to that patch.
7.  Make sure to adjust the keywords as necessary: [https://make.wordpress.org/core/handbook/contribute/trac/keywords/](https://make.wordpress.org/core/handbook/contribute/trac/keywords/)
-->

1.  [https://make.wordpress.org/core/reports/](https://make.wordpress.org/core/reports/) を使って、取り組むことが可能なチケットを探します。
2.  添付ファイルを確認し、現在提案されているパッチがあるかどうかを確認します。
3.  パッチが存在しない場合は、シナリオを再現し、[新しいパッチを追加する](https://make.wordpress.org/core/handbook/tutorials/working-with-patches/)必要があります。
4.  パッチがある場合は、レビューとテストが必要で、コメントから現在の状況がわかります。パッチをダウンロードし、あなたの開発環境でテストしてください。期待通りに動作する場合は、適切なフィードバックを提供してください。
5.  パッチに変更を加えた場合は、コメントと合わせて Diff (https://make.wordpress.org/themes/handbook/review/working-with-trac/#comparing-ticket-updates) へのリンクも提供してください。
6.  チケットには、何を変更したか、なぜ変更したかを記述したコメントを必ず残してください。パッチのアップロードそのものは、通知のきっかけとはなりません。パッチへリンクするときは、コメントで [attachment:{filename}] を使用してください。
7.  必要に応じてキーワードを調整するようにしてください: [https://make.wordpress.org/core/handbook/contribute/trac/keywords/](https://make.wordpress.org/core/handbook/contribute/trac/keywords/)

<!--
If a ticket does not already exist for an issue, please open a new ticket: [https://make.wordpress.org/core/handbook/tutorials/trac/opening-a-ticket/](https://make.wordpress.org/core/handbook/tutorials/trac/opening-a-ticket/)
-->

もし、その課題に対するチケットがまだ存在しない場合は、新しいチケットを開いてください: [https://make.wordpress.org/core/handbook/tutorials/trac/opening-a-ticket/](https://make.wordpress.org/core/handbook/tutorials/trac/opening-a-ticket/)

<!--
## Ticket Overview
-->

## チケットの概要

<!--
[![Trac Ticket Overview](https://make.wordpress.org/core/files/2018/03/trac-ticket-overview-1024x1024.jpg)](https://make.wordpress.org/core/files/2018/03/trac-ticket-overview.jpg)
-->

[![Trac チケットの概要](https://make.wordpress.org/core/files/2018/03/trac-ticket-overview-1024x1024.jpg)](https://make.wordpress.org/core/files/2018/03/trac-ticket-overview.jpg)

<!--
Trac Ticket Overview
-->

Trac チケットの概要

<!--
1.  Ticket ID Number – When commenting please use the format #{ticket\_id} to automatically create a link between tickets.
2.  Type –
    1.  Defect (bug): There’s something wrong and it needs to be fixed.
    2.  Enhancements: An existing feature could use this improvement, like an additional hook or other modification.
    3.  Feature requests: This is a new item not currently represented in WordPress core or another Trac ticket.
    4.  Tasks (blessed): This option won’t appear when filing a new ticket. This status is only given to a ticket if a feature team has accepted it for development (hence, “blessed”).
3.  Milestone – This is set to “Awaiting Review” by default. Once accepted for development, this will be set to the specific version number slated for release. Only [trusted core contributors](https://make.wordpress.org/core/handbook/about/organization/#contributing-developers) can set a milestone.
4.  Severity – normal, major, minor, trivial, critical, or blocker., Only trusted core contributors have the ability to modify the severity.
5.  Component – Which specific part of the project are we working on? For a more detailed definition of each component, please read: [https://make.wordpress.org/core/components/](https://make.wordpress.org/core/components/)
6.  Focuses – Optional when creating a ticket. This indicates if a ticket is relevant to an area that encompasses multiple WordPress components. Options are: ui, accessibility, javascript, docs, rtl, admin, template, multisite, rest-api, performance, coding-standards
7.  Priority – How quickly this issue should be addressed. Options are: normal, low, high, lowest or highest omg bbq. Unless you have discussed a different status with a trusted core contributor, ‘normal’ should be used.
8.  Version (for bugs) – The earliest known version of WordPress affected by this bug. You should not change this.
9.  Keywords – These are like tags, used to track the current status of the ticket and required next steps. This will change as work progresses. For more definition of the available choices, refer to: [https://make.wordpress.org/core/handbook/contribute/trac/keywords/](https://make.wordpress.org/core/handbook/contribute/trac/keywords/)
10.  Description – The heart of the ticket. Please be as thorough and specific as possible. If this is a bug, include steps to reproduce the issue and what you expected to happen.
11.  Attachments – Add additional info, like screenshots, new patches or diff files for patches.
12.  Change History – This is where the conversation happens! This is open by default and you should read it all the way through before you begin work to see what has been tried and what others are actively doing.
-->

1.  チケット ID 番号 - コメントの際は、チケット間のリンクを自動的に作成するため、#{ticket_id} のフォーマットを使用してください。
2.  タイプ -
    1.  Defect (bug): 何か問題があり、修正する必要があります。
    2.  Enhancements: フックの追加やその他の修正のような、既存の機能の改善です。
    3.  Feature requests: WordPress コアや他の Trac チケットにない新しいアイテムです。
    4.  Tasks (blessed): このオプションは、新しいチケットを提出するときには表示されません。このステータスは、機能チームがそのチケットを開発対象として受け入れた場合にのみ与えられます (「blessed」というのはそのためです)。
3.  マイルストーン - デフォルトで「Awaiting Review」に設定されています。開発が承認されると、これはリリース予定の特定のバージョン番号に設定されます。マイルストーンを設定できるのは、[信頼されたコア貢献者](https://make.wordpress.org/core/handbook/about/organization/#contributing-developers)のみです。
4.  重要度 - normal、major、minor、trivial、critical、または blocker。信頼できるコア貢献者のみが重要度を変更できます。
5.  コンポーネント - プロジェクトのどの部分に取り組んでいるのか ? 各コンポーネントの詳細な定義については、[https://make.wordpress.org/core/components/](https://make.wordpress.org/core/components/)をお読みください。
6.  フォーカス - チケットを作成する際にオプションで設定します。これは、チケットが WordPress コンポーネントの複数の領域に関連しているかどうかを示します。選択肢は ui、accessibility、javascript、docs、rtl、admin、template、multisite、rest-api、performance、coding-standards です。
7.  優先度 - この問題をどの程度早く対処すべきか。選択肢は normal、low、high、lowest、highest omg bbq です。信頼されたコア貢献者と別のステータスについて話し合ったことがない限り、「normal」を使用する必要があります。
8.  バージョン (バグの場合) - このバグの影響を受ける WordPress の最も古い既知のバージョンです。これを変更するべきではありません。
9.  キーワード - これはタグのようなもので、チケットの現在のステータスと必要な次のステップを追跡するために使用されます。これは、作業の進行に応じて変更されます。利用可能な選択肢に関する詳細な定義については、以下を参照してください: [https://make.wordpress.org/core/handbook/contribute/trac/keywords/](https://make.wordpress.org/core/handbook/contribute/trac/keywords/)
10.  説明文 - チケットの中心となる部分です。できるだけ詳しく、具体的に書いてください。バグの場合は、問題を再現するための手順と、期待することを記載してください。
11.  添付ファイル - スクリーンショット、新しいパッチ、パッチの差分ファイルなど、追加情報を追加します。
12.  変更履歴 - ここで会話が行われます ! デフォルトで開かれているため、作業を始める前に最後まで読んで、何が試されたのか、他の人は何を積極的に行っているのかを確認する必要があります。

<!--
## Resources
-->

## リソース

<!--
Printable high resolution of the above infographic are available in [JPG](https://make.wordpress.org/core/files/2018/03/trac-ticket-overview-print.jpg) and [PDF](https://make.wordpress.org/core/files/2018/03/trac-ticket-overview-print.pdf) formats.
-->

上記インフォグラフィックの印刷用高解像度画像は、[JPG](https://make.wordpress.org/core/files/2018/03/trac-ticket-overview-print.jpg) と [PDF](https://make.wordpress.org/core/files/2018/03/trac-ticket-overview-print.pdf) のフォーマットで提供されています。
