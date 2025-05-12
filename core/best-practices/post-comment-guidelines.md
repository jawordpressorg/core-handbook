<!--
# Post &amp; Comment Guidelines
-->

# 投稿とコメントのガイドライン

<!--
These guidelines were [initially proposed on make/core](https://make.wordpress.org/core/2015/09/30/proposal-makecore-post-guidelines/). If you have questions or feedback, please join Slack and ask in [#core](https://wordpress.slack.com/messages/C02RQBWTW).
-->

このガイドラインは、[最初に make/core で提案されました。](https://make.wordpress.org/core/2015/09/30/proposal-makecore-post-guidelines/)質問やフィードバックがある場合は、Slack に参加して [#core](https://wordpress.slack.com/messages/C02RQBWTW) で質問してください。

<!--
## Introduction
-->

## はじめに

<!--
The Make WordPress Core Blog (make/core) is the official blog of the WordPress core team. It is read by thousands of people, many of whom may not know the intricacies of core, or understand the process of core development.
-->

Make WordPress Core ブログ (make/core) は、WordPress コアチームの公式ブログです。何千人もの人に読まれていますが、その多くはコアの複雑なしくみを知らなかったり、コアの開発プロセスを理解していないかもしれません。

<!--
Most make/core posts must serve one of two goals:
-->

ほとんどの make/core の投稿は、2つの目的のうちどちらかを果たす必要があります。

<!--
1.  Generate feedback (including testing) from the developer community
2.  Ensure developers know about changes and can plan accordingly
-->

1.  開発者コミュニティからのフィードバック (テストを含む) を受ける
2.  開発者が変更点を把握し、それに応じた計画を立てられるようにする

<!--
In order to ensure the best experience possible for the developer community, the guidelines on this page are written with unexperienced readers in mind.
-->

このガイドラインは、開発者コミュニティ内のできるだけ大勢のメンバーに有益なものとなるように、未経験者を想定して書かれています。

<!--
## Posting
-->

## 投稿

<!--
### Getting Access to Post
-->

### 投稿へのアクセス権限の取得

<!--
Access to posting and editing on make/core is managed in the [#core room in Slack](https://wordpress.slack.com/archives/C02RQBWTW). It is best to have someone who already has access to ask on your behalf, but if you feel you should have access to create a post, please don’t hesitate to ask for yourself. The same process is used for changing roles.
-->

make/core への投稿と編集権限は、[Slack の #core ルーム](https://wordpress.slack.com/archives/C02RQBWTW) で管理されています。既にアクセス権限を持っている方に代理でアクセス権限を申請してもらうのが最善ですが、投稿作成権限が必要と思われる場合は、ご自身でアクセス権限を申請してください。権限の変更も同様の手順で行えます。

<!--
### When to Write a Post
-->

### 記事を書くタイミング

<!--
Posting on make/core should be a common occurrence for committers, component maintainers, and other core contributors. There are many kinds of posts that should be written on a schedule:
-->

make/core に投稿することは、コミッター、コンポーネントメンテナー、その他のコア貢献者にとって、頻繁に行われるべきです。スケジュールに沿って書かれるべき投稿の種類はたくさんあります。

<!--
*   **API changes.** There are a few examples of API changes that should be announced on make/core, including: new filters/actions, changed order of hooks, substantial enhancements to queries (the *Boone Gorges Rule*), changing the purpose of a parameter in a hook, new general helper functions, or any other significant changes in a release. These posts should be published on make/core within the first week of the beta period to ensure developers are aware of any upcoming changes.Grouping related changes into one post to accepted, so long as the post does not become too long. For example, a single post called “Customizer changes in WordPress 4.2” is fine, rather than individual changes about each commit. If in doubt, use the weekly devchat to discuss your proposed post(s).
*   **Meeting announcements.** Regular devchat meetings do not need to be announced, but an agenda post is helpful to developers who do not regularly follow the release. Other meetings should receive an initial post on make/core announcing the meeting, but do not need weekly announcements.
*   **Meeting notes.** Do you hold regular or one-off meetings? Post notes from your meeting on make/core to ensure those that couldn’t attend have an easy way to provide feedback. Devchats almost always receive an accompanying summary post for those who can’t attend. Component chats and feature plugin chats should also have summary posts after meetings.
*   **Feature Plugin-related posts.** Introducing your feature plugin idea to the world is best done at a weekly devchat or one of the semi-regular feature plugin chats. Once proposed, a post on make/core can make sense, depending on the stage of the idea. Merge proposals should also make their way to make/core, when asked for from a release lead.
-->

*   **API の変更。** make/core で告知すべき API 変更の例としては、新しいフィルターやアクション、フックの順番の変更、クエリーの大幅な強化 (**ブーン・ゴルジュのルール**)、フックのパラメータの目的の変更、新しい汎用ヘルパー関数、その他リリースにおける重大な変更などがあります。これらの投稿は、開発者が今後の変更点を確実に把握できるように、ベータ期間の最初の1週間以内に make/core で公開されるべきです。関連する変更点をひとつの投稿にまとめることは、投稿が長くなり過ぎない限り、認められます。たとえば、「WordPress 4.2におけるカスタマイザーの変更点」という投稿は、各コミットについての個別の変更点ではなく、1つの投稿でかまいません。もし疑問があれば、提案した投稿について話し合うために、毎週の開発チャットを使用してください。
*   **ミーティングのお知らせ。** 定期的な 開発チャットのミーティングは告知する必要はありませんが、要約の投稿は定期的にリリースを追いかけていない開発者にとって役に立ちます。その他のミーティングでは、make/core にミーティングの告知をする必要がありますが、毎週告知をする必要はありません。
*   **ミーティングのメモ。** 定期的または一度限りのミーティングを開催していますか ? ミーティングのメモを make/core に投稿し、参加できなかった人が簡単にフィードバックできるようにしましょう。開発チャットでは、参加できなかった人のために、ほとんどの場合は要約記事を添付しています。コンポーネントチャットやプラグインチャットも、ミーティング後に要約記事を投稿してください。
*   **機能プラグインに関する記事。** あなたの機能プラグインのアイデアを世界に紹介するには、毎週の開発チャットか、不定期に開催される機能プラグインチャットのいずれかが最適です。一度提案されたら、アイデアの段階によっては、make/core に投稿することも良いでしょう。リリースリードから依頼された場合、マージの提案も make/core に投稿されるべきです。

<!--
Keep in mind that feedback on make/core will almost always be greater than that in Trac tickets. Announcing changes and posting early and often is helpful to the entire community.
-->

make/core でのフィードバックは、Trac チケットでのフィードバックよりも常に大きいこと覚えておいてください。変更のアナウンスや投稿を早い段階で頻繁に行うことは、コミュニティ全体にとって有益なことです。

<!--
### Peer Review
-->

### 査読

<!--
Whether it’s your first time posting or your millionth, it is strongly encouraged to ask a committer to proofread a post before publishing it. Peer review (like code review) helps make sure your words are clear and working as intended, but also helps identify any phrases that might not translate well. Some posts (like weekly agendas) do not necessarily need peer review, but if it’s your first few times posting on make/core, it doesn’t hurt to ask.
-->

初めての投稿でも100万回目の投稿でも、投稿を公開する前にコミッターに校正を依頼することが強く推奨されます。査読 (コードレビューのようなもの) は、あなたの言葉が明確で意図したとおりに書かれているか確認することに役立ち、また、うまく翻訳されないかもしれないフレーズを特定することに役立ちます。いくつかの投稿 (毎週の要約など) は必ずしも査読を必要としませんが、もしあなたが make/core に投稿するのが初めてなら、お願いしても損はないでしょう。

<!--
Feature plugin merge proposals should *always* be read by the release lead (or designee) before posting. Release devnotes should be read by the release lead (or designee) before publishing.
-->

機能プラグインのマージの提案は、投稿する前に「必ず」リリースリーダー (または指名された人) に読んでもらうべきです。リリース開発者ノートは、公開する前にリリースリーダー (または指名された人) に読んでもらうべきです。

<!--
See the Giving Proper Credit (Props) section below for information on how to make sure the proofreaders/peer reviewers are recognized.
-->

校正者や査読者の貢献を認知する方法については、以下の「適切なクレジット (props) を与える」のセクションを参照してください。

<!--
### Style and Substance
-->

### スタイルと内容

<!--
The make/core blog is the official voice of the core team. As a result, you should keep your personal thoughts out of the body of the post, leaving them for the comments. Furthermore, **first person pronouns should be avoided**.
-->

make/core ブログはコアチームの公式な声明です。そのため、個人的な感想は記事の本文に書かず、コメントに残してください。さらに、**一人称の代名詞は避けるべきです**。

<!--
Similarly, **the word “we” should be avoided** in posts, unless its made very clear which group is speaking. An example of this is listing attendees of a meeting and, in the summary post, noting that “we, those present at the meeting” made a decision or agreed on a plan of action.
-->

同様に、どのグループが発言しているかが明確でない限り、投稿では **「私たち」という言葉は避けるべきです。** たとえば、ミーティングの参加者をリストアップし、要約の投稿で「ミーティングに参加した私たち」が決定を下したり、行動計画に合意したことを記すことです。

<!--
If you’re proposing a roadmap or making a request for comments, make sure to **highlight the draft/proposal status** in both the title and opening paragraph. This helps to avoid confusion about the status of your proposal.
-->

ロードマップを提案したり、コメントを求めたりする場合は、タイトルと冒頭の段落の両方で、**ドラフトや提案のステータスを強調してください。** これにより、提案のステータスに関する混乱を避けることができます。

<!--
Many people reading make/core don’t speak English as a first language. Keep that in mind when deciding how to phrase your post. For make/core, it’s always better to write simple instead of smart. In general, the tone should be similar to WordPress: Friendly.
-->

make/core を読んでいる人の多くは、英語を第一言語としていません。そのことを念頭に置いて、投稿のフレーズを決めてください。make/core では、スマートではなく、シンプルに書くことが常に好まれます。一般的には、WordPress と同じようなトーンであるべきです (親しみやすい)。

<!--
*Check out the [Text-based Communication in Open Source](https://wordpress.org/contributor-training/lesson/text-based-communication-in-open-source/) and [Best Practices for Global Collaboration](https://wordpress.org/contributor-training/lesson/best-practices-for-global-collaboration/) pages on the [WordPress Contributor Training](https://wordpress.org/contributor-training/) site for more tips and best practices.*
-->

[オープンソースにおけるテキストベースのコミュニケーション](https://wordpress.org/contributor-training/lesson/text-based-communication-in-open-source/)や[グローバルなコラボレーションのためのベストプラクティス](https://wordpress.org/contributor-training/lesson/best-practices-for-global-collaboration/)については、[WordPress 貢献者トレーニング](https://wordpress.org/contributor-training/)サイトのページを参照してください。

<!--
### Giving Proper Credit (Props)
-->

### 適切なクレジット (Props) を与える

<!--
When a post is finally published, it goes out under one person’s name. However, posts are often the combined efforts of several contributors who deserve to be recognized. Noting who helped bring a post to a publishable state can also provide important context to readers and helps them understand who they would be addressing in discussion.
-->

最終的に投稿が公開されるとき、それは一人の名前で発信されます。しかし、投稿は多くの場合、複数の投稿者の努力によるものであり、それらは評価されるべきです。また、投稿を公開可能な状態にするために誰が協力したかを示すことは、読者に重要な文脈を提供し、議論する際に誰を相手にするのかを理解するために役立ちます。

<!--
At the bottom of your post, include a footnote like so:
-->

投稿の一番下に、以下のような脚注を入れてください。

<!--
*Props @desrosj and @jeffpaul for providing historical background, @chanthaboune and @andreamiddleton for proofreading.*
-->

「歴史的背景を提供してくれた @desrosj と @jeffpaul、校正してくれた @chanthaboune と @andreamiddleton に感謝します。」

<!--
### Tagging and Other Specifics
-->

### タグ付けとその他の仕様

<!--
For each of the following types of post, there are some things to keep in mind:
-->

以下の投稿の種類ごとに、いくつかの注意点があります。

<!--
*   **Component-related posts.** Almost all posts relate to a component. Please tag component-related posts with the component name. If your post covers multiple components, use multiple tags!
*   **API changes.** All API changes should be tagged with the related release number, the component name, and “dev-notes” to indicate that it is a note for developers.
*   **Release announcements.** All posts related to a specific release – including agendas, meeting summaries, API changes, week in core, etc – should be tagged with the related release.
*   **Feature plugins and other projects.** Each of these type of post should be consistently tagged with a project name. For example, if you’re working on a redesign of the admin called “MP6,” tag all related posts with MP6.
*   **Meeting announcements.** When posting about a meeting ahead of time (aka, not summary notes), use the [time shortcode](https://make.wordpress.org/meta/2013/04/03/time-shortcode-for-make-p2s/) so that readers know exactly when the meeting will take place in their local time.
-->

*   **コンポーネントに関連した投稿。** ほとんどすべての投稿は、コンポーネントに関連しています。コンポーネントに関連する投稿には、コンポーネント名をタグ付けしてください。複数のコンポーネントを扱う場合は、複数のタグを使用してください。
*   **API の変更。** すべての API の変更には、関連するリリース番号、コンポーネント名、そして開発者向けの注意事項であることを示す「dev-notes」のタグを付ける必要があります。
*   **リリースに関するお知らせ。** 特定のリリースに関連するすべての投稿 (要約、ミーティングの概要、API の変更、今週のコアなど) には、関連するリリースをタグ付けする必要があります。
*   **機能プラグインやその他プロジェクト。** これらのタイプの投稿には、それぞれプロジェクト名で一貫したタグを付ける必要があります。たとえば、「MP6」という管理画面の再設計に取り組んでいるのであれば、関連するすべての投稿に「MP6」のタグを付けましょう。
*   **ミーティングのお知らせ。** ミーティングについて事前に投稿する場合 (別名、要約メモではない)、読者が自分のローカルタイムで会議が行われる時間を正確に知ることができるように、[time ショートコード](https://make.wordpress.org/meta/2013/04/03/time-shortcode-for-make-p2s/)を使用します。

<!--
### Proposals
-->

### 提案

<!--
When writing up an idea aimed at generating feedback and assessing a potential change from the core contributor community it is important that it is clear that what is being written is a proposal and not a final decision. To help achieve that, proposals must include the word “Proposal” at the start of the title and include text in the body explaining that a final decision has not yet been made.
-->

コア貢献者コミュニティからフィードバックを得て、変更の可能性を評価することを目的としてアイデアを書き上げる場合、書かれていることが提案であり最終決定ではないことを明確にすることが重要です。これを達成するために、提案はタイトルの最初に「提案」という単語を含み、最終決定がまだなされていないことを説明する文章を本文に含めなければなりません。

<!--
### Comments on Posts
-->

### 投稿へのコメント

<!--
Comments on posts will automatically close after 180 days (about 6 months). If you need to keep comments open, you can use the tag `#keep-comments-open` but this should only be used with a specific timeframe in mind rather than allowing comments to stay open forever.
-->

投稿へのコメントは180日 (約6ヵ月) 後に自動的に閉じられます。コメントを開いたままにしておく必要がある場合は、`#keep-comments-open` タグを使用できますが、これはコメントを永久に開いたままにするのではなく、特定の期間を念頭に置いて使用する必要があります。

<!--
## Comments
-->

## コメント

<!--
Discussion and criticism of ideas are important to the long-term success of WordPress. In support of this, all make/core posts have open comments. As a result, **commenters should be respectful and professional**, understanding that many other commenters and readers do not speak English as a first language. At times, it may make sense to over-communicate and be extra polite to ensure no misunderstandings occur.
-->

アイデアに関する議論や批判は、WordPress の長期的な成功のために重要です。これを支持するため、すべての make/core の投稿はコメントがオープンな状態になっています。そのため、他のコメント投稿者や読者の多くが英語を母国語としていないことを理解した上で、**コメント投稿者は敬意とプロ意識を持って**投稿する必要があります。時には、誤解が生じないように、過剰なコミュニケーションや丁寧な対応をすることも意味があるかもしれません。

<!--
If a comment is disrespectful and/or unprofessional, it may be edited at the discretion of the core team.
-->

失礼なコメントやプロフェッショナルでないコメントは、コアチームの判断で編集されることがあります。

<!--
Editing of a comment will be done with the approval of at least two blog administrators. When a comment is edited, only the offending section will be edited with the intent of retaining as much of the expressed opinion. The administrators who edit the offending comment will add an editor’s note stating the reason for editing and the names of the administrators who took action. Additionally, the administrator doing the editing should retain a screenshot of the unedited comment, which can be uploaded to the Media Library on make/core, if necessary.
-->

コメントの編集は、少なくとも2名のブログ管理者の承認を得て行うものとします。コメントを編集する場合、表現された意見をできるだけ残すことを意図して、問題のある部分のみを編集します。編集した管理者は、編集の理由と編集した管理者の名前を記した編集者ノートを付けます。さらに編集した管理者は、編集前のコメントのスクリーンショットを残し、必要に応じて make/core のメディアライブラリにアップロードしてください。

<!--
Comments will only be deleted when the offending comment is clearly spam that was not properly moderated.
-->

コメントは、明らかに適切なモデレーションが行われていないスパムと判断された場合のみ削除されます。

[#core](https://make.wordpress.org/core/tag/core/)
