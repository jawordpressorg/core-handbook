<!--
# WordPress Release Team and Focus Leads
-->

# WordPress リリースチームとフォーカスリード

<!--
**Each new WordPress software release is a substantial undertaking that can only succeed through the dedication and support of hundreds of contributors.** 
-->

**新しい WordPress ソフトウェアのリリースは、何百人もの貢献者の協力とサポートによってのみ成功できる重要な作業です。**

<!--
The work can span many months and involves all areas of the global project. Each release is managed by a changing group of active contributors who take ownership of its various aspects. This group is known as the ‘Release Team’ for the particular software version. It coordinates across all the teams to connect ideas and solutions and make the release as effective as possible.
-->

その作業は何ヵ月にも及ぶこともあり、グローバルプロジェクトのあらゆる分野に関わります。各リリースは、さまざまな側面のオーナーシップを持つ活動的な貢献者のグループによって管理されます。このグループは、特定のソフトウェアバージョンの「リリースチーム」として知られています。リリースチームは、アイデアや解決策を結び付け、リリースを可能な限り効果的なものにするために、すべてのチームを横断して調整します。

<!--
Members of each Release Team come from a variety of backgrounds and skillsets. They should have a thorough understanding of the WordPress software and the community, but also of open source web development. In addition, they have good communication and project management skills.
-->

各リリースチームのメンバーは、さまざまな経歴やスキルを持っています。彼らは WordPress ソフトウェアとコミュニティだけでなく、オープンソースの Web 開発についても十分に理解している必要があります。さらに、コミュニケーションスキルとプロジェクト管理スキルも持っています。

<!--
This page explains the various roles involved with a given release and the type of tasks involved. 
-->

このページでは、リリースに関わるさまざまな役割と、それに関わるタスクの種類について説明します。

<!--
## Release Team
-->

## リリースチーム

<!--
The main focus of the release team is to lead the release from its beginning through to launch. This requires members to act as connectors and facilitators, resolving bottlenecks and issues.
-->

リリースチームの主な役割は、リリースの開始から立ち上げまでをリードすることです。そのため、メンバーはコネクターやファシリテーターとして、ボトルネックや問題を解決する必要があります。

<!--
A new release affects all the moving parts of the software. Any newly introduced, or amended feature could potentially:
-->

新しいリリースは、ソフトウェアのすべての部品に影響を与えます。新しく導入された、または修正された機能は、潜在的に以下の可能性があります:

<!--
*   affect existing plugins
*   have an impact on the accessibility of both front-end and back-end of the platform
*   and so much more.
-->

*   既存のプラグインに影響を与える
*   プラットフォームのフロントエンドとバックエンドの両方のアクセシビリティに影響を与える
*   など沢山あります。

<!--
It is therefore vital to have representatives from all fields of expertise in the Release Team. Each will take responsibility for a particular aspect and act as an advocate during the process.
-->

そのため、リリースチームにはあらゆる専門分野の代表者を置くことが重要です。それぞれが特定の側面に責任を持ち、プロセス中の支持者として行動します。

<!--
In addition, it is crucial that all changes are thoroughly documented. This also helps all stakeholders to be involved.
-->

さらに、すべての変更を完全にドキュメント化することが重要です。これは、すべての関係者が参加することにも役立ちます。

<!--
During the course of a development cycle, the Release Team is joined by hundreds of contributors. These contributors collectively work on a range of tasks, guided and mentored by both Release Team members, and other experienced contributors. 
-->

開発サイクルの過程で、リリースチームには何百人もの貢献者が参加します。これらの貢献者は、リリースチームのメンバーや他の経験豊富な貢献者の指導を受けながら、さまざまなタスクに取り組みます。

<!--
Historically, not all releases have included representatives from every area of the platform. Minor releases may not need the involvement of all teams. Some of the most commonly seen release team roles are listed below.
-->

これまで、すべてのリリースにプラットフォームのあらゆる分野の代表者が含まれていたわけではありません。マイナーリリースでは、すべてのチームの関与は必要ないかもしれません。よく見られるリリースチームの役割を以下に示します。

<!--
## Release team roles
-->

## リリースチームの役割

<!--
To cover all situations, ideally each lead role in a release should have at least two people.
-->

あらゆる状況をカバーするために、理想的には、リリースの各リードには少なくとも2人が必要です。

<!--
### Shared Responsibilities
-->

### 共有の責任

<!--
These are tasks and responsibilities that may be documented for specific roles below but can be taken on by anyone throughout the release cycle.
-->

これらは、以下の特定の役割のためにドキュメント化されたタスクと責任ですが、リリースサイクル全体を通して誰でも引き受けることができます。

<!--
*   Communicating publicly as much as possible (on tickets, in component chats, Make/Core posts, etc.).
*   Identifying blockers to progress and asking for help from buddies, team leads, and/or the Release Lead.
*   Being mindful of deadlines.
*   Identifying changes that require documentation, HelpHub articles, or communication to the community at large (through dev notes, marketing, etc.).
*   Leading bug scrubs focused on your team’s tickets and tasks.
*   Facilitating and participating in inter-team discussions.
*   Always be testing!
-->

*   可能な限り公の場でコミュニケーションをとる (チケット、コンポーネントチャット、Make/Core 投稿、GitHub での issue や PR のスレッドなどで)。
*   進捗を妨げるものを特定し、仲間、チームリード、リリースリードに助けを求める。
*   期限を守る。
*   ドキュメント、HelpHub の記事、または  (開発ノート、マーケティング、P2 投稿などを通じた) コミュニティ全体へのコミュニケーション を必要とする変更を特定し、そのような変更についてドキュメントチームとコミュニケーションをとる。
*   自分のチームのチケットやタスクに焦点を当てたバグスクラブを実施する。
*   チーム間のディスカッションを促進し参加する。
*   常にテストすること !

<!--
### Release lead
-->

### リリースリード

<!--
**Responsibilities**
-->

**責任**

<!--
*   Set the overall goals and main focus for the release
*   Make final decisions on merging [feature plugins](https://make.wordpress.org/core/handbook/about/release-cycle/features-as-plugins/)
*   Give final review to and publish news blog post announcing the release. Older ones can be [found on this page](https://wordpress.org/news/category/releases/)
-->

* リリースの全体的な目標と主な焦点を設定する
* [機能プラグイン](https://ja.wordpress.org/team/handbook/core/about/release-cycle/features-as-plugins/)のマージに関する最終決定を行う
* リリースを発表するニュースブログ記事を最終レビューし、公開する。過去の記事は[このページ](https://wordpress.org/news/category/releases/)でご覧いただけます

<!--
### Release Coordination
-->

### リリース調整

<!--
**Responsibilities**
-->

**責任**

<!--
*   Run various release processes in Slack (beta, release candidate, release).
*   Write [blog posts for various milestones](https://make.wordpress.org/core/tag/releases/).
*   Keep an eye on the deadlines in the handbook and contact the different teams involved (ping plugin, theme, ping polyglots, etc.). Remind people of said deadlines when needed.
*   Take notes on the procedures outlined in the handbook to propose changes if needed.
*   Facilitate inter-team discussions if needed.
*   Maintain a birds-eye view of the moving parts for any red flags, blockers, or additional help needed for teams.
*   Coordinate with the WordPress Executive Director to ensure a jazz musician is selected to name the release. This involves reaching out to the WordPress Executive Director to start the process in the week before the final Release Candidate. The WordPress Executive Director will then work with Matt Mullenweg to finalize. This is only done for major releases and should be done in the week before the last planned Release Candidate. Past jazzers are documented on the [WordPress versions](https://wordpress.org/documentation/article/wordpress-versions/) page.
-->

*   Slack でさまざまなリリースプロセス (ベータ版、リリース候補版、リリース) を実行する。
*   さまざまなマイルストーンに関するブログ記事](https://make.wordpress.org/core/tag/releases/)を作成する。
*   ハンドブックに記載されている期限を常に把握し、関係するさまざまなチーム (プラグイン、テーマ、多言語対応チームなど) に連絡を取る。必要に応じて、期限を知らせる。
*   ハンドブックに記載されている手順をメモし、必要に応じて変更を提案する。
*   必要に応じて、チーム間の議論を促進する。
*   進行中のプロジェクトを俯瞰的に把握し、危険信号、阻害要因、チームに必要な追加サポートなどを把握する。
*   WordPress エグゼクティブディレクターと調整し、リリースの名称にジャズミュージシャンが選ばれるようにする。これには、最終リリース候補版の1週間前に WordPress エグゼクティブディレクターに連絡を取り、プロセスを開始することが含まれます。その後、WordPress エグゼクティブディレクターは Matt Mullenweg と協力して最終決定を行います。これはメジャーリリースのみで行われ、最終リリース候補版の1週間前に行う必要があります。過去のジャズバージョンについては、[WordPress バージョン](https://wordpress.org/documentation/article/wordpress-versions/) ページをご覧ください。

<!--
### Core Triage Lead
-->

### コアトリアージリード

<!--
**Responsibilities**
-->

**責任**

<!--
*   [Run Bug Scrubs](https://make.wordpress.org/core/handbook/tutorials/leading-bug-scrubs/)
*   Run various release processes in Slack with the Release Coordinator (beta, release candidate, release). These are detailed in the process [detailed in this document](https://make.wordpress.org/core/handbook/about/release-cycle/releasing-major-versions).
*   Attempt to triage core tickets(in trac) in the release’s milestone
*   Prioritize tickets to ensure that the most time-sensitive and urgent issues are given the necessary exposure within the group to garner a fast resolution
*   Communicate with component maintainers to gauge where more resources/attention is needed
-->

* [バグスクラブを実行する](https://ja.wordpress.org/team/handbook/core/tutorials/leading-bug-scrubs/)
* リリースコーディネーターと Slack さまざまなリリースプロセス (ベータ版、リリース候補版、リリース版) を実行する。これらのプロセスの詳細は、[このドキュメントで詳しく説明されています](https://ja.wordpress.org/team/handbook/core/about/release-cycle/releasing-major-versions/)。
*   リリースのマイルストーンで (trac 内の) コアチケットのトリアージを試みる
*   チケットの優先順位付けを行い、すぐに取り掛かる必要がある緊急性の高い問題に対してグループ内で注意喚起を行い、迅速な解決を図る
*   コンポーネントメンテナーとのコミュニケーションを図り、より多くのリソースや注意が必要な箇所を把握する

<!--
### Core Tech Lead
-->

### コアテックリード

<!--
**Responsibilities**
-->

**責任**

<!--
*   Review core patches and changesets for feasibility, code quality, technical design, and [coding standards](https://developer.wordpress.org/coding-standards/wordpress-coding-standards/) compliance. Ensure they follow the overall software architecture.
*   Provide a “second opinion” and technical guidance where requested or needed.
*   Ensure the release cycle stages are followed by all contributors. For example — no enhancements during the beta, unless an exception was proposed and approved by project leadership
*   Ensure the beta, RC and final release processes run as smoothly as possible on the technical side, and all release steps are completed
*   This role is also responsible for escalating cases and helping to make decisions when new features, enhancements, and (large) bug-fixes are not ready in time. For example — if a new feature is not 100% complete before beta, and/or the code is still “alpha” quality and needs more work. In such cases, the core tech lead would facilitate reviews and gather more information to decide whether to proceed with the feature or add it in the next release. These cases are usually escalated to project leadership.
-->

*   パッチやチェンジセットの実現可能性、コードの品質、技術設計、[コーディング規約](https://ja.wordpress.org/team/handbook/coding-standards/wordpress-coding-standards/)への準拠をレビューする。全体的なソフトウェアアーキテクチャーに従っていることを確認する。
*   要求または必要に応じて「セカンドオピニオン」と技術的なガイダンスを提供する。
*   すべての貢献者がリリースサイクルのフェーズに従っていることを確認する。たとえば、例外が提案され、プロジェクトリーダーによって承認されない限り、ベータ版の間は機能強化を行いません
*   ベータ、RC、最終リリースの各プロセスが、技術面で可能な限りスムーズに実行され、すべてのリリース手順が完了していることを確認する
*   この役割は、新機能や機能強化、(大規模な) バグ修正が間に合わない場合、ケースをエスカレーションし、意思決定を支援する責任もあります。たとえば、新機能がベータ版までに100%完成していない場合や、コードがまだ「アルファ」品質でさらに作業が必要な場合などです。コアテックリードはレビューを促し、より多くの情報を収集して、その機能を継続するか、次のリリースで追加するかを決定します。これらのケースは通常、プロジェクトリーダーにエスカレーションされます。

<!--
### Design Lead
-->

### デザインリード

<!--
**Responsibilities**
-->

**責任**

<!--
*   This role is split into two main areas – Product, and release.
    *   The “product” area comprises the work going into the actual UI/UX of WordPress.
    *   The “release” area includes coordinating release-specific materials (like the About page).
*   Provide guidance and decision-making on core and block editor tickets that need any design input.
*   Coordinate design and copy for various release assets.
    *   Guiding the creation of the highlight grid and microsite for each WordPress release. This includes the unique about page that ships with each major release, and shows up in wp-admin. Examples of previous highlight grids for reference:
        *   [6.5 microsite](https://wordpress.org/download/releases/6-5/)
        *   [6.4 microsite](https://wordpress.org/download/releases/6-4/)
        *   [6.3 microsite](https://wordpress.org/download/releases/6-3/)
    *   Work on, and provide design support for creating social media assets for each release.
    *   Decide and design the artwork for the jazz musician associated with each major release
-->

*   この役割は、製品とリリースという2つの主要な領域に分かれています。
    *   「製品」領域は、WordPress の実際の UI/UX に関わる作業です。
    *   「リリース」領域には、リリース固有の資料 (アバウトページなど) の調整が含まれます。
*   デザインに関するインプットが必要なコアエディターおよびブロックエディターのチケットについて、ガイダンスと意思決定を提供します。
*   さまざまなリリースアセットのデザインとコピーを調整します。
    *   各 WordPress リリースのハイライトグリッドとマイクロサイトの作成をガイドします。これには、各メジャーリリースに同梱され、wp-admin に表示される独自の アバウトページも含まれます。参考までに、過去のハイライトグリッドの例を以下に示します。
        *   [6.5 マイクロサイト](https://wordpress.org/download/releases/6-5/)
        *   [6.4 マイクロサイト](https://wordpress.org/download/releases/6-4/)
        *   [6.3 マイクロサイト](https://wordpress.org/download/releases/6-3/)
    *   各リリースのソーシャルメディアアセット作成に携わり、デザインサポートを提供します。
    *   各メジャーリリースに関連するジャズミュージシャンのアートワークを決定し、デザインします。

<!--
### Documentation Wrangling
-->

### ドキュメントの調整

<!--
**Responsibilities**
-->

**責任**

<!--
*   [Write and publish the Field Guide](https://make.wordpress.org/core/handbook/tutorials/publishing-the-field-guide/) on RC1 release date ([Example from the WP 6.6 release](https://make.wordpress.org/core/2024/06/25/wordpress-6-6-field-guide/)) 
*   Manage [writing and publishing of dev notes](https://make.wordpress.org/core/handbook/tutorials/writing-developer-notes/)
    *   Keep track of changes within the release that require dev notes. This includes Gutenberg PRs for all releases of the plugin between two core releases
    *   Coordinate with the participants of those tickets/PRs with the best understanding of the changes (the committer, component maintainers, contributors who own a ticket/PR) to draft dev notes
    *   Ensure all dev notes are written with enough time to proofread, reviewed, and published before the Field Guide (which publishes at the same time as Release Candidate 1)
    *   Proofread and review dev notes before publication.
    *   If a ticket participant is not available to write a dev note, finding someone to write one, or writing one yourself
*   Ensure any documentation pages required for new features are created before the release. Check out the [Documentation process during a major version release](https://make.wordpress.org/docs/handbook/workflows/documentation-process-during-a-major-version-release/) to prepare for release day.
-->

*   RC1リリース日に[フィールドガイドの作成と公開](https://ja.wordpress.org/team/handbook/core/tutorials/publishing-the-field-guide/)を行う ([WP 6.6リリースの例](https://make.wordpress.org/core/2024/06/25/wordpress-6-6-field-guide/))
*   [開発ノートの作成と公開](https://ja.wordpress.org/team/handbook/core/tutorials/writing-developer-notes/)を管理する
    *   開発ノートが必要となるリリース内の変更を追跡する。これには、2つのコアリリース間のプラグインのすべてのリリースに対する Gutenberg PR が含まれます。
    *   変更内容を最もよく理解しているチケットや PR の参加者 (コミッター、コンポーネントメンテナー、チケット/PR の所有者である貢献者) と調整し、開発ノートの草稿を作成します。
    *   (リリース候補1と同時に公開される) フィールドガイドの前に、すべての開発ノートが十分な時間をかけて校正、レビュー、公開されるように作成します。
    *   公開前に開発ノートの校正とレビューを行います。
    *   チケットに関わった人が開発ノートを作成できない場合は、作成してくれる人を探すか、自分で作成します。
*   新機能に必要なドキュメントページは、リリース前に作成します。[メジャーバージョンリリース中のドキュメント作成プロセス](https://make.wordpress.org/docs/handbook/workflows/documentation-process-during-a-major-version-release/)を確認し、リリース当日の準備を進めてください。

<!--
### MarComms (Marketing and Communications) Lead
-->

### MarComms (マーケティングおよびコミュニケーション) リード

<!--
**Responsibilities**
-->

**責任**

<!--
*   Collaborate with release leads and contributors to draft Marketing and Communications (MarComms) deliverables, including:
    *   Beta & Release Candidate announcement posts
    *   General release announcement post
    *   About page and microsite content
*   Ensure the content for these deliverables is written and ready for proofreading and review with enough time, follows the [WordPress.org Brand Writing Style Guide](https://make.wordpress.org/marketing/handbook/resources/style-guide-and-brand-book/), and accurately reflects the release features and benefits.
*   Collaborate with release design contributors on creative and visual assets such as the highlight grid, featurettes, and/or other social media visuals for release marketing and communication purposes.
*   Help develop or collaborate with marketing contributors on a social media posting plan to promote the release milestones and key features.
*   For a comprehensive guide to this role’s tasks, visit the [Marketing Communications Release Cycle Guide](https://make.wordpress.org/marketing/handbook/resources/marketing-communications-release-cycle-guide/).
-->

*   リリースリーダーおよび貢献者と協力し、マーケティングおよびコミュニケーション (MarComms) 成果物 (以下を含む) のドラフトを作成します。
    *   ベータ版およびリリース候補版のアナウンス投稿
    *   リリース全般のアナウンス投稿
    *   アバウトページおよびマイクロサイトのコンテンツ
*   これらの成果物のコンテンツが、十分な時間を確保して校正およびレビューの準備が整っていること、[WordPress.org ブランドライティングスタイルガイド](https://make.wordpress.org/marketing/handbook/resources/style-guide-and-brand-book/)に準拠し、リリースの機能とメリットを正確に反映していることを確認します。
*   リリースマーケティングおよびコミュニケーションを目的として、ハイライトグリッド、特集記事、その他のソーシャルメディアビジュアルなどのクリエイティブおよびビジュアルアセットについて、リリースデザイン貢献者と協力します。
*   リリースのマイルストーンと主要機能を宣伝するためのソーシャルメディア投稿計画の策定を支援し、マーケティング貢献者と協力します。
*   この役割のタスクに関する包括的なガイドについては、[マーケティング・コミュニケーション・リリースサイクルガイド](https://make.wordpress.org/marketing/handbook/resources/marketing-communications-release-cycle-guide/)をご覧ください。

<!--
### Editor Tech Lead 
-->

### エディターテックリード

<!--
**Responsibilities**
-->

**責任**

<!--
*   Loosely help define what Gutenberg features can/should get included in the release
*   Triage and review patches and PRs, test RCs, and coordinates meetings for the block editor
*   Ensure all Gutenberg features and bug fixes land on time before each Core beta/RC
*   Gather a list of important Gutenberg bugs and regressions that need to be fixed on each release. Ensure the contributors know about these and their importance ([Project board example](https://github.com/orgs/WordPress/projects/179))
*   Help with Gutenberg ⇔ Core sync/updates through Trac tickets ([More details here](https://make.wordpress.org/core/handbook/about/release-cycle/block-editor-release-process-for-major-releases/))
*   Make sure the Gutenberg props get collected properly
*   Communication with the rest of the release squad about:
    *   Documenting the updates from Gutenberg included in the release and on each Core beta/RC
    *   Highlighting the important features and updates for the marketing team and for the About page.
    *   Co-ordination with other leads
*   Make sure Gutenberg updates get shipped in Core releases on time, with as few bugs as possible, and get communicated properly. 
*   Communication with all contributors to get features and enhancements ready in time, help them out if needed.
-->

*   どの Gutenberg の機能がリリースに含まれるのか、含まれるべきなのかを大まかに定義する
*   パッチやプルリクエストのトリアージとレビューを行い、RC のテスト、ブロックエディターのミーティングを調整する
*   すべての Gutenberg に関する機能とバグ修正が、各コアベータ版、RC の前に予定通りに行われるようにする
*   各リリースで修正が必要な Gutenberg の重要なバグやリグレッションのリストを集める。貢献者がこれらのバグと重要性を理解できるようにする ([プロジェクトボードの例](https://github.com/orgs/WordPress/projects/179))
*   Trac チケットを通して、Gutenberg とコアの同期・更新を手伝う ([詳細はこちら](https://ja.wordpress.org/team/handbook/core/about/release-cycle/block-editor-release-process-for-major-releases/))
*   Gutenberg の props が適切に収集されていることを確認する
*   リリースチームの残りのメンバーと次の点についてコミュニケーションをとる:
    *   リリースおよび各 コアベータ版/RC に含まれる Gutenberg の更新内容を文書化する
    *   マーケティングチームと アバウトページ向けに重要な機能と更新内容をハイライトする
    *   他のリーダーと連携する
*   Gutenberg の更新が可能な限りバグが少なく、適切に伝達され、予定どおりにコアリリースに出荷されることを確認する
*   機能と拡張機能を期限内に準備するために、すべての貢献者とコミュニケーションを取り、必要に応じてサポートする

<!--
### Editor Triage Lead
-->

### エディタートリアージリード

<!--
**Responsibilities**
-->

**責任**

<!--
*   This role is similar to the Core triage lead role, but focuses mainly on the development of the block editor, and integrating it in core releases.
*   Run Bug Scrubs focused on Editor items. This is done in the [#core-editor](https://make.wordpress.org/core/tag/core-editor/) channel on Slack.
*   Review incoming tickets to the [Gutenberg GitHub repo](https://github.com/WordPress/gutenberg/issues) to ensure items are labeled appropriately for further review, including adding anything necessary to the appropriate release specific project board.
*   Communicate with the Core Editor Tech leads to help gauge where more resources/attention is needed.
*   Help prioritize any key issues throughout the release cycle to ensure time sensitive and urgent problems are resolved promptly.
-->

*   この役割はコアトリアージリードの役割に似ていますが、主にブロックエディターの開発と、それをコアリリースに統合することに重点を置いています。
*   エディターに関する項目にフォーカスしたバグスクラブを実行する。
*   [Gutenberg GitHub リポジトリ](https://github.com/WordPress/gutenberg/issues)に送られてくるチケットをレビューし、適切なリリース固有のプロジェクトボードに必要なものを追加するなど、さらなるレビューのために項目が適切にラベル付けされていることを確認する。
*   コアエディターのテックリードとコミュニケーションをとり、より多くのリソースや注意が必要な箇所を把握する。
*   リリースサイクルを通して重要な問題に優先順位をつけ、緊急性の高い問題が迅速に解決されるようにする。

<!--
This work is done in collaboration and coordination with the Core Tech leads so please refer to [Block Editor Release Process for Major Releases](https://make.wordpress.org/core/handbook/about/release-cycle/block-editor-release-process-for-major-releases/) for a more detailed and practical look.
-->

この作業はコアテックリードとの協力と調整によって行われるため、より詳細で実践的な内容については[ブロックエディター メジャーリリース時のリリースプロセス](https://ja.wordpress.org/team/handbook/core/about/release-cycle/block-editor-release-process-for-major-releases/)を参照してください。

<!--
### Accessibility Lead
-->

### アクセシビリティリード

<!--
**Responsibilities**
-->

**責任**

<!--
*   Set up priorities for the release and define a general scope for the accessibility focus
*   Triage all other tickets that are not in the main priority for the release and make choices based on priority/severity
*   Organize/run accessibility bug scrubs (1 accessibility focused scrub per week)
*   Contribute to tickets from various components to give accessibility feedback on both Trac and Gutenberg GitHub repository
*   Write accessibility-related documentation and publish it on Make/Core ([dev notes](https://make.wordpress.org/core/handbook/tutorials/writing-developer-notes/)) or [HelpHub](https://wordpress.org/documentation/) as necessary
*   Coordinate with the design and media teams to keep the release scope on its way.
*   Open tickets/issues on Trac/GitHub to handle potential accessibility regressions on all the components during the entirety of the release process
*   Communicate about the release scope and progress updates on Make/Accessibility and during core dev chats
*   Ensure patches are solid, reviewed, and committed in time
*   Contribute to ticket patches with code, tests, screenshots, code, and design reviews, etc
*   Provide accessibility-related reviews and contributions to ensure accessibility standards are met
-->

*   リリースの優先順位を設定し、アクセシビリティに関する一般的な範囲を定義する
*   リリースの主な優先順位にない他のすべてのチケットをトリアージし、優先度や重要度にもとづいて選択する
*   アクセシビリティのバグスクラブを計画し実行する (アクセシビリティに焦点を当てたスクラブを週に1回行う)
*   さまざまなコンポーネントのチケットに貢献し、Trac と Gutenberg GitHub リポジトリの両方でアクセシビリティフィードバックを行う
*   アクセシビリティ関連のドキュメントを作成し、必要に応じて Make/Core ([開発者ノート](https://ja.wordpress.org/team/handbook/core/tutorials/writing-developer-notes/))または [HelpHub](https://wordpress.org/documentation/) で公開する
*   リリースの範囲を計画通りに進めるために、デザインチームやメディアチームと調整する
*   リリースプロセス全体を通じて、すべてのコンポーネントのアクセシビリティに関する潜在的なリグレッションに対処するために、Trac/GitHub 上でチケット/issue を開く
*   Make/Accessibility やコア開発者チャットで、リリースの範囲や進捗状況を伝える
*   パッチが確実で、レビューされ、期限内にコミットされるようにする
*   コード、テスト、スクリーンショット、デザインレビューなどでチケットパッチに貢献する
*   アクセシビリティに関連したレビューと貢献を行い、アクセシビリティ標準が満たされていることを確認する

<!--
### Performance Lead
-->

### パフォーマンスリード

<!--
**Responsibilities**
-->

**責任**

<!--
*   Set up priorities for the release and define a general scope for the [performance focus](https://core.trac.wordpress.org/query?status=accepted&status=assigned&status=new&status=reopened&status=reviewing&focuses=~performance) by estimating both horizontal impact (“how many sites does this apply to?”) and vertical impact (“how much does this improve performance for sites where it applies?”)
*   Regularly triage tickets in the milestone that fall outside of the main priorities, following up with the reporter and other contributors involved
*   Assess feasibility of committing a fix for specific tickets in the current release cycle, based on priority, severity, effort and time needed, contributor availability, time left in the cycle
*   Join or lead regular performance bug scrubs and other [performance related meetings](https://make.wordpress.org/performance/#block-3)
*   Benchmark performance of relevant pull requests / patches from various components (in both [Trac](https://core.trac.wordpress.org/) and [Gutenberg](https://github.com/WordPress/gutenberg/issues)), both proactively and on demand, focusing primarily on tickets that are one of the following:
    *   A new feature or API planned for the release
    *   A performance enhancement or fix that is intended to improve performance
    *   Another change that suggests to have a measurable performance impact (whether positive or negative)
*   Work with team members to ensure [performance measurement best practices](https://make.wordpress.org/performance/handbook/measuring-performance/) are followed and clearly communicated
*   Monitor the [WordPress core performance dashboard](https://www.codevitals.run/project/wordpress) regularly to identify potential performance regressions and report them back to the relevant ticket for which the underlying change was committed
*   Coordinate with other release leads, primarily the Core Tech and Editor Tech Leads to support their priorities with performance guidance
*   Communicate about the release scope and progress updates in the release leads Slack channel and during core dev chats
*   Work with the Documentation Lead to ensure timely publishing of performance related dev note posts prior to or early in the beta phase
*   Support team members contributing to tickets in the performance focus, e.g. through triaging, coordinating team members to help with feedback, code review, and benchmarking, as well as guidance on communication and documentation related tasks such as enhancing WordPress core documentation or writing dev notes
*   Coordinate the contributions to tickets, pull requests/patches, tests, performance benchmarks, code reviews, etc.
*   Run benchmarks to assess the performance of the release compared to the previous stable release, once the Beta or RC is available
*   Draft and publish a Make Core post highlighting the release’s performance improvements and sharing key metrics from the benchmarks
-->

*   リリースの優先順位を設定し、[パフォーマンスフォーカス](https://core.trac.wordpress.org/query?status=accepted&status=assigned&status=new&status=reopened&status=reviewing&focuses=~performance)の一般的な範囲を定義する。水平的な影響 (「どれだけのサイトに適用されるか ?」) と垂直的な影響 (「適用されるサイトのパフォーマンスをどれだけ向上させるか ?」) の両方を判断する
*   主な優先事項から外れたマイルストーンのチケットを定期的にトリアージし、報告者と関係する他の貢献者にフォローアップする
*   優先度、重要度、必要な労力と時間、貢献者の可用性、サイクルの残り時間にもとづいて、現在のリリースサイクルで特定のチケットの修正をコミットすることの実現可能性を評価する
*   定期的なパフォーマンスバグスクラブやその他の[パフォーマンス関連ミーティング](https://make.wordpress.org/performance/#block-3)に参加またはリードする
*   以下に挙げる項目を主な対象として、[Trac](https://core.trac.wordpress.org/) や [Gutenberg](https://github.com/WordPress/gutenberg/issues) 内の、さまざまコンポーネントの関連するプルリクエストやパッチのパフォーマンスを、事前に、そして必要に応じてベンチマークする:
    *   リリース予定の新機能または API
    *   パフォーマンスの向上を目的とした機能強化や修正
    *   測定可能なパフォーマンスへの影響 (ポジティブかネガティブかにかかわらず) を示唆する別の変更
*   チームメンバーと協力して、[パフォーマンス測定のベストプラクティス](https://make.wordpress.org/performance/handbook/measuring-performance/)が守られ、明確に伝達されるようにする
*   [WordPress コアパフォーマンスダッシュボード](https://www.codevitals.run/project/wordpress)を定期的に監視し、潜在的なパフォーマンス低下を特定し、根本的な変更がコミットされた関連チケットに報告する
*   他のリリースリード、主にコアテックリードとエディターテックリードと調整し、パフォーマンスガイダンスで優先事項をサポートする
*   リリースリードの Slack チャンネルやコア開発者チャットで、リリースの範囲や進捗状況を伝える
*   ドキュメンテーションリードと協力して、ベータフェーズの前または初期に、パフォーマンス関連の開発者ノートの投稿をタイムリーに公開する
*   パフォーマンス関連のチケットに貢献しているチームメンバーをサポートする。たとえば、トリアージ、フィードバック、コードレビュー、ベンチマーキングを支援するチームメンバーの調整や、コミュニケーションやドキュメント関連タスク (WordPress のコアドキュメントの強化や開発者ノートの執筆) のガイダンスなど
*   チケット、プルリクエスト/パッチ、テスト、パフォーマンスベンチマーク、コードレビューなどへの貢献を調整する
*   ベータ版または RC 版が利用可能になったら、ベンチマークを実行し、リリースのパフォーマンスを以前の安定版リリースと比較して評価する
*   リリースのパフォーマンス改善点を強調し、ベンチマークから得られた主要な指標を共有する Make Core 投稿の下書きを作成して公開する

<!--
### Default Theme
-->

### デフォルトテーマ

<!--
A new default theme will be bundled together with the last release of the year. This task needs a number of roles.
-->

新しいデフォルトテーマは、今年の最後のリリースにバンドルされます。この作業には多くの役割が必要です。

<!--
#### Default Theme Design
-->

#### デフォルトテーマデザイン

<!--
**Responsibilities**
-->

**責任**

<!--
*   Create drafts for the default theme design, iterate on those drafts, and polish the design selected as the final candidate
*   Introduce the design on the Make Core/Make Themes blogs
*   Update the design as needed throughout the process
*   Participate in meetings (and occasionally lead them) in [#core-themes](https://make.wordpress.org/core/tag/core-themes/)
*   Contribute code to the theme, mostly front-end heavy stuff
*   Document the theme features and behavior, both to guide development (in issues and PRs) and for the support pages on WordPress.org
*   Review issues and PRs, primarily design-related ones
-->

*   デフォルトのテーマデザインのドラフトを作成し、それらのドラフトを繰り返し、最終候補として選択されたデザインに磨きをかける
*   Make Core/Make Themes ブログでデザインを紹介する
*   プロセスを通して、必要に応じてデザインを更新する
*   [#core-themes](https://make.wordpress.org/core/tag/core-themes/) でのミーティングに参加する (時にはリードする)。
*   主にフロントエンドで重要な点に関して、コードでテーマに貢献する
*   テーマの機能と動作をドキュメント化し、(issue やプルリクエストの) 開発ガイドと WordPress.org のサポートページに掲載する
*   主にデザイン関連の issue やプルリクエストをレビューする

<!--
#### Default Theme Development
-->

#### デフォルトテーマ開発

<!--
**Responsibilities**
-->

**責任**

<!--
*   Leading implementation for major designs crafted by Default Theme Design Lead
*   Providing technical guidance and review for others assisting with implementing designs from Default Theme Design Lead
*   Create issues and PR’s as I found bugs within the theme
*   Organize issues and PR’s with labels
*   Run the weekly new default theme meeting in [#core-themes](https://make.wordpress.org/core/tag/core-themes/)
*   Close duplicate issues and issues which were not within the scope of our timeline or were decided against by the [#core-themes](https://make.wordpress.org/core/tag/core-themes/) team
*   Review issues and PRs, marking them for \`commit\` them as needed
*   Approve and review default theme tickets (other than a new default theme being built for the same release) in the milestone and punt tickets when necessary
*   Manage the development of the new default theme and help everyone involved stay focused on tasks and the short timeline
*   Package the theme for upload to the theme directory for each phase of the release
-->

*   デフォルトテーマのデザインリードによって作成された主要なデザインの実装をリードする
*   デフォルトテーマのデザインリードからのデザインの実装を支援する他のユーザーに、技術的なガイダンスとレビューを提供する
*   テーマ内のバグを見つけたときは issue やプルリクエストを作成する
*   issue や プルリクエストをラベルで整理する
*   [#core-themes](https://make.wordpress.org/core/tag/core-themes/) で毎週新しいデフォルトテーマのミーティングを行う
*   重複する issue や、タイムラインの範囲外であったり、[#core-themes](https://make.wordpress.org/core/tag/core-themes/) チームによって却下された issue をクローズする
*   issue やプルリクエストをレビューし、必要に応じて「コミット」マークをつける
*   (同じリリースでビルドされる新しいデフォルトテーマ以外の) デフォルトテーマのチケットをマイルストーンで承認し、レビューし、必要に応じてチケットを延期する
*   新しいデフォルトテーマの開発を管理し、関係者全員がタスクと短いスケジュールに集中できるようにする
*   リリースの各フェーズでテーマディレクトリにアップロードするテーマをパッケージ化する

<!--
#### Default Theme Wrangler
-->

#### デフォルトテーマの調整

<!--
**Responsibilities**
-->

**責任**

<!--
*   Guarantee that all default themes fully support any new features added in the current release (as deemed appropriate).
*   Triage tickets in the Bundled Theme component in Trac
*   Manage tickets and decide what is ready, what is not, and what should not be included
*   Mark tickets for \`commit\` when they are tested and confirmed to be ready
*   Communicate with the new default theme designers and developers to use a common approach when adding support for new features
-->

*   すべてのデフォルトテーマが、現在のリリースで追加された新機能を完全にサポートしていることを保証する (適切と判断された場合)。
*   Trac の バンドルテーマコンポーネントでチケットをトリアージする
*   チケットを管理し、何が準備できていて、何が準備できていなくて、何が含まれるべきでないかを決定する
*   チケットがテストされ、準備ができたと確認されたときに、チケットに「コミット」マークを付ける
*   新しいデフォルトテーマのデザイナーや開発者とコミュニケーションを取り、新しい機能のサポートを追加する際に共通のアプローチを使用する

<!--
### Support
-->

### サポート

<!--
**Responsibilities**
-->

**責任**

<!--
*   Have a presence in the WordPress.org support forums during phases 2-4 of the release cycle keeping an eye on the [Alpha/Beta/RC forum](https://wordpress.org/support/forum/alphabeta/)
*   Bring any potential problems reported there to the attention of the appropriate release team member
*   Help respond to [posts with no replies](https://wordpress.org/support/view/no-replies/)
*   If you speak a language other than English, check out the [list of non-English support forums](https://make.wordpress.org/support/handbook/contributing-to-the-wordpress-forums/support-forums-in-your-language/) and provide support
*   If there are common questions appearing in the forums, bring it to the attention of the release team so that new user documentation pages can be created.
-->

*   リリースサイクルのフェーズ2～4の間は、WordPress.org のサポートフォーラムに参加し、[アルファ/ベータ/RC フォーラム](https://wordpress.org/support/forum/alphabeta/)に注目する
*   そこで報告された潜在的な問題を、適切なリリースチームメンバーに知らせる
*   [返信のない投稿](https://wordpress.org/support/view/no-replies/)への返信を手伝う
*   英語以外の言語を話す場合は、[英語以外のサポートフォーラムのリスト](https://make.wordpress.org/support/handbook/contributing-to-the-wordpress-forums/support-forums-in-your-language/)をチェックして、サポートを提供する
*   フォーラムによくある質問がある場合は、新しいユーザードキュメントページを作成できるように、リリースチームに知らせる

<!--
### Test
-->

### テスト

<!--
**Responsibilities**
-->

**責任**

<!--
*   Coordinating and leading efforts to increase testing of beta releases, release candidate releases, final release, and where feasible everyday trunk/nightly builds in an effort to provide real-world testing feedback to the rest of the release team.
*   Amplify testing efforts and opportunities, including helping onboard folks who are interested in helping or [doing round up posts for feature specific testing](https://make.wordpress.org/test/2021/11/30/help-test-wordpress-5-9-features/). 
*   Attend test meetings as much as possible to communicate priorities for testing to the community.
*   Work with teams to ensure any necessary testing for new features or big changes (example: [Gallery Block refactor](https://make.wordpress.org/core/2021/08/20/gallery-block-refactor-dev-note/)).
*   As possible, improve documentation for testing related items to help more folks get involved.
-->

*   ベータリリース、リリース候補、最終リリース、そして可能であれば毎日の trunk/ナイトリービルドのテストを増やすための取り組みを調整し、リードする。
*   テストへの取り組みや機会を拡大する。手伝いたいと考えている人たちのオンボーディングを手伝ったり、[特定の機能のテストのためのラウンドアップ投稿を行う](https://make.wordpress.org/test/2021/11/30/help-test-wordpress-5-9-features/)。
*   できる限りテストミーティングに参加して、テストの優先順位をコミュニティに伝える。
*   チームと協力して、新機能や大きな変更に必要なテストを確実に行う (例: [ギャラリーブロックのリファクタリング](https://make.wordpress.org/core/2021/08/20/gallery-block-refactor-dev-note/))。
*   できるだけ多くの人が参加できるように、テストに関するドキュメントを改善する。

<!--
The section above outlines the roles for the Release Team rather than the work of the individual core teams and their work towards a release launch. To learn more about how the Make Teams contribute to the current release cycle, [visit the development blog.](https://make.wordpress.org/core/)
-->

上記のセクションでは、各コアチームの作業やリリース開始に向けた作業ではなく、リリースチームの役割について説明しています。Make チームが現在のリリースサイクルにどのように貢献しているかについては、[開発ブログをご覧ください](https://make.wordpress.org/core/)。

<!--
## Further resources
-->

## その他のリソース

<!--
> [How the Release Cycle Works](https://make.wordpress.org/core/handbook/about/release-cycle/)

> [Releasing Major Versions](https://make.wordpress.org/core/handbook/about/release-cycle/releasing-major-versions/)
-->

*   [リリースサイクルの仕組み](https://ja.wordpress.org/team/handbook/core/about/release-cycle/)
*   [メジャーバージョンのリリース](https://ja.wordpress.org/team/handbook/core/about/release-cycle/releasing-major-versions/)
