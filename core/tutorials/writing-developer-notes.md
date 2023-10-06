<!--
# Writing developer notes
-->

# 開発者ノートを書く

<!--
A Developer note (or “dev note” for short) is a blog post on the [Making WordPress Core](https://make.wordpress.org/core/) blog that details a technical change in an upcoming release and what developers need to know about that change.
-->

開発者ノート (略して「dev note」) とは、[Making WordPress Core](https://make.wordpress.org/core/) ブログにおいて、次のリリースにおける技術的な変更と、その変更について開発者が知っておくべきことを詳細に説明するブログ記事のことです。

<!--
Dev notes are an important part of the WordPress Core release cycle. They keep the developer community informed by calling out changes that could impact how they build on WordPress, and supplements inline documentation by explaining the problems, solutions, best practices, and edge cases related to the change.
-->

開発者ノートは、WordPress コアのリリースサイクルにおいて重要です。WordPress の構築方法に影響を与える可能性のある変更について開発者コミュニティに情報を提供し、問題点、解決策、ベストプラクティス、エッジケースを説明することでインラインドキュメントを補完します。

<!--
The best dev notes are clear, concise, and complete.
-->

最高の開発者ノートとは、明確で、簡潔で、完全なものです。

<!--
## How do you know what needs a dev note?
-->

## 開発者ノートが必要なものは、どのように判断しますか ?

<!--
For each release, tickets that may need developer notes are given the `needs-dev-note` keyword on Trac. When a note has been published for a ticket, that keyword is replaced with the `has-dev-note` keyword and a link to the note is included in a comment.
-->

各リリースにおいて、開発者ノートが必要なチケットは Trac 上で `needs-dev-note` キーワードが与えられます。チケットにノートが投稿されると、そのキーワードは `has-dev-note` キーワードに置き換えられ、コメントにノートへのリンクが含まれます。

<!--
**It’s important to remember that not all tickets in a milestone marked `needs-dev-note` on Trac end up being committed and included in that release.**
-->

**重要なのは、Trac で `needs-dev-note` とマークされたマイルストーンのすべてのチケットがコミットされ、そのリリースに含まれるわけではないということです。**

<!--
For that reason, care should be taken to only write notes for tickets and changes once it becomes clear that the changes will be included in the release. Usually, that means tickets with the `closed` status (and sometimes `reopened`) are where the focus should be.
-->

そのため、チケットや変更点のノートを書くのは、その変更点がリリースに含まれることが明らかになってから行うべきです。通常、これは `closed` ステータス (ときには `reopened` ステータス) のチケットに焦点を当てるべきことを意味します。

<!--
## Who should write dev notes?
-->

## 誰が開発者ノートを書きますか ?

<!--
The hierarchy for who should author a dev note is as follows:
-->

開発者ノートを作成する人の優先順位は、以下の通りです。

<!--
*   Someone with deep, working knowledge of the changes. This is usually the committer that made the change, a component maintainer that helped craft/test the changes, or any other contributor that helped push that change forward.
*   Someone with a good technical foundation that did not work on the change, but can review the code changes in detail to convey the right message.
*   Someone that is less technical, but is comfortable interviewing or asking someone in the above groups questions about the changes in order to have the information needed to write the note.
-->

*   その変更について、深く実用的な知識を持っている人。これは通常、それ変更したコミッター、その変更の作成とテストを手伝ったコンポーネントのメンテナー、またはその変更を前進させることを手伝ったその他の貢献者です。
*   その変更に関わっていないが、技術的な基礎があり、正しいメッセージを伝えるためにコードの変更を詳細にレビューできる人。
*   技術的なことはあまり詳しくないが、ノートを書くうえで必要な情報を得るために、変更点について上記のグループの誰かにインタビューしたり質問したりできる人。

<!--
## What should a dev note include?
-->

## 開発者ノートには何を書くべきですか ?

<!--
Each note will be unique, but every dev note should clearly define a problem that is being solved, how that problem was solved, and what developers need to know about the related changes. It usually contains a mix of the following:
-->

それぞれのノートはユニークなものですが、すべての開発者ノートは、解決されようとしている問題、その問題がどのように解決されたか、開発者が関連する変更について知っておくべきことなどを明確に定義する必要があります。通常、以下のような内容が混在しています。

<!--
*   Clear identification of a problem
*   Description of why this is problematic
*   Are developers currently solving the problem in a less than ideal way?
*   Are there established patterns in the wild within plugins and themes addressing this problem already?
*   Documents current practices or usage, and how the current state of the code base may contribute to the issue.
*   Describes what the ideal behavior would be and why,
*   Explains the changes made to achieve the desired behavior/outcome
*   Provides examples for how to correctly use the function/feature/API after these changes (establish a best practice)
*   Identifies backwards compatibility considerations, explains how they were addressed in Core, and how they should be addressed within plugins and themes.
*   Details possible edge cases that have been identified
*   Links to additional reading materials about the change as necessary, such as Trac or GitHub tickets, changesets, past dev notes, past posts on Make blogs, etc.
-->

*   問題を明確にする。
*   なぜ問題なのかを説明する。
*   開発者は現在、理想的とは言えない方法で問題を解決しているのかどうか。
*   この問題に対処するために、プラグインやテーマにおいてすでに確立されたパターンがあるのかどうか。
*   現在のプラクティスまたは使用方法、およびコードベースの現在の状態が、どのように問題の原因となりうるかをドキュメント化する。
*   理想的な行動とは何か、またその理由を記述する。
*   望ましい行動や結果を達成するために行った変更を説明する。
*   変更後の機能や特徴、API を正しく使用するための例を提供する (ベストプラクティスの確立)。
*   後方互換性に関する考慮事項を特定し、それらがコアでどのように対処されたか、またプラグインやテーマでどのように対処されるべきかを説明する。
*   判明しているエッジケースについての詳細。
*   Trac や GitHub のチケット、チェンジセット、過去の開発者ノート、Make ブログの過去の投稿など、必要に応じて変更に関する追加資料へのリンクを貼る。

<!--
Sometimes, there are a large handful of changes that deserve to be called out, but are not detailed enough to warrant individual dev notes. **It is more than fine to group multiple changes together in a single dev note.**
-->

ときには、言及する価値はあるが、個々の開発者ノートを書くほど詳細ではない大きな変更点があります。**複数の変更を一つの開発者ノートにまとめることは、むしろ良いことです。**

<!--
It is common for component maintainers to publish a single dev note for their component to detail several different changes. It’s also common for a more generic “Miscellaneous developer focused changes in X.X” dev note to be published collecting any other remaining smaller changes that should receive a call out.
-->

コンポーネントのメンテナーが、そのコンポーネントについて、いくつかの異なる変更点を詳述した一つの開発者ノートを公開することはよくあることです。また、より一般的な「X.X での開発者向けのさまざまな変更点」という開発者ノートとして、言及すべき残りの小さな変更点をまとめて発表することもよくあります。

<!--
**After researching the ticket but before writing the dev note, ask “Is this a change that needs to be documented at length? Is a one sentence call out sufficient? Or does the change not have anything technical that actually needs to be called out”**
-->

**チケットを調査してから開発者ノートを書く前に、「これは長々とドキュメント化する必要がある変更なのか、一文を記載するだけで十分なのか、その変更に関連する技術的なものはないか」などを考慮すべきです。**

<!--
The goal is to find a balance between post length, related changes and topics, and the number of dev notes published during a release. More dev notes are better than less. However, it is important to keep in mind that readers should not get tired of the notes and stop reading them.
-->

目標は、記事の長さ、関連する変更とトピック、そしてリリース中に公開される開発者ノートの数のバランスを見つけることです。開発者ノートの数は、少ないより多いほうがよいでしょう。しかし、読者がノートに飽きて読むのをやめてしまわないように注意することが重要です。

<!--
## Should dev notes be reviewed?
-->

## 開発者ノートはレビューされるべきですか ?

<!--
Every post on a [Making WordPress](https://make.wordpress.org/) blog should be peer reviewed by at least one other person. **For dev notes, each one must have *at least* two reviewers**: 
-->

[Making WordPress](https://make.wordpress.org/) ブログのすべての記事は、少なくとも他の人によって査読されるべきです。**開発者ノートの場合、「少なくとも」2人のレビュアーが必要です**。 

<!--
*   One technical review to verify the accuracy of the post and ensure no important details were missed.
*   One copy review to help spot grammatical, spelling, and other errors.
-->

*   投稿の正確さを確認し、重要な点を見落としていないことを確認するための1回の技術的レビュー。
*   文法やスペルなどの誤りを発見するための1回のコピーレビュー。

<!--
After receiving at least two reviews, reach out to the Documentation lead for the release. They will have a high level overview of all dev notes planned or in progress and can help recommend a publish window. It’s important to spread out dev notes to prevent “dev note fatigue”. For example, 3 or more dev notes should not be published on the same day.
-->

少なくとも2件のレビューを受けたら、そのリリースのドキュメンテーションリードに連絡を取ってください。彼らは、計画中または進行中のすべての開発者ノートの概要を把握し、公開のタイミングを調整できます。「開発者ノート疲れ」を防ぐために、開発者ノートを分散させることが重要です。たとえば、3つ以上の開発者ノートを同じ日に公開するべきではありません。

<!--
## When should a dev note be published?
-->

## 開発者ノートをいつ公開すべきですか ?

<!--
A dev note can be published any time during the release cycle. If a change to the code base is committed today, the dev note could be published tomorrow. However, it’s usually best to wait a while after the changes are committed to allow several days for testing.
-->

開発者ノートは、リリースサイクル中いつでも公開できます。コードベースへの変更が今日コミットされれば、開発者ノートは明日公開されるかもしれません。しかし、通常は変更をコミットした後、テストのために数日待つことがベストでしょう。

<!--
A handful of WordPress contributors run `trunk` on their websites in order to test every change after it’s made. On occasion, an issue does come up requiring adjustments to be made. Waiting to publish the dev note ensures that only one note is required for a change, avoiding the potential for confusion and making more work for developers.
-->

WordPress の貢献者の中には、自分のサイトで `trunk` を運用し、変更箇所をすべてテストしている人も少なくありません。ときには、調整が必要な問題が発生することもあります。開発者ノートの公開を待つことで、1つの変更に対して1つのノートしか必要ないことが保証され、混乱の可能性や開発者の仕事を増やすことを避けることができます。

<!--
**However, all dev notes for a changes in a specific release should be published before the first release candidate for that release.**
-->

**ただし、特定のリリースでの変更に関するすべての開発者ノートは、そのリリースの最初のリリース候補の前に公開されるべきです。**

<!--
To help organize documentation about the upcoming release, a Field Guide collated and published for every major version of WordPress at the same time as [Release Candidate 1](https://make.wordpress.org/core/handbook/about/release-cycle/releasing-major-versions/#release-candidate). Field Guides are a collection of all relevant dev notes and tickets for an upcoming release.
-->

次期リリースに関するドキュメントを整理するために、[リリース候補版1](https://ja.wordpress.org/team/handbook/core/about/release-cycle/releasing-major-versions/#release-candidate) と同時に、WordPress のメジャーバージョンごとにフィールドガイドが作成・投稿されます。

<!--
All field guides for previous releases can be found here: [make.wordpress.org/core/tag/field-guide](https://make.wordpress.org/core/tag/field-guide).
-->

過去のリリースにおけるすべてのフィールドガイドは、こちらで確認できます。[make.wordpress.org/core/tag/field-guide](https://make.wordpress.org/core/tag/field-guide)

<!--
## Other Tips
-->

## その他のヒント

<!--
Here are some additional resources and tips to help write developer notes
-->

以下は、開発者用ノートを書くために役に立つ追加のリソースとヒントです。

<!--
### Tone and style
-->

### トーンとスタイル

<!--
When writing or reviewing any post on the [Making WordPress Core blog,](https://make.wordpress.org/core/) it’s important to remember the [Post & Comment Guidelines](https://make.wordpress.org/core/handbook/best-practices/post-comment-guidelines/). The Style and Substance section is particularly important. The guidelines on that page help ensure clear communication with a consistent tone and voice throughout all official WordPress channels.
-->

[Making WordPress Core ブログ](https://make.wordpress.org/core/) で記事を書いたりレビューしたりするときには、[投稿とコメントのガイドライン](https://ja.wordpress.org/team/handbook/core/best-practices/post-comment-guidelines/)を覚えておくことが重要です。特に、スタイルと内容のセクションは重要です。このページのガイドラインは、WordPress のすべての公式チャンネルにおいて、一貫したトーンと表現によって明確なコミュニケーションを確保するために役立ちます。

<!--
### Tagging and categorizing
-->

### タグ付けとカテゴライズ

<!--
After writing a developer note, it is also important to make sure it is tagged correctly. The tags that every dev note should have are `dev-notes`, and a specific version tag (`5.5`, for example). Additional tags can be added as necessary, and usually include specific component tags.
-->

開発者ノートを書いた後は、それが正しくタグ付けされていることを確認することも重要です。すべての開発者ノートには `dev-notes` というタグと、特定のバージョンタグ (たとえば `5.5`) が必要です。必要に応じてタグを追加でき、通常、特定のコンポーネントに関するタグを含みます。

<!--
Properly tagging notes is important to make them easier to find and revisit later.
-->

ノートに適切なタグを付けることは、後で見つけやすく、再度確認しやすくするために重要です。

<!--
[dev notes for a particular release](https://make.wordpress.org/core/tag/dev-notes+5.5/), all the [dev notes written on the blog](https://make.wordpress.org/core/tag/dev-notes), or the [dev notes for a particular component](https://make.wordpress.org/core/tag/dev-notes+rest-api/).
-->

[特定のリリースの開発者ノート](https://make.wordpress.org/core/tag/dev-notes+5.5/)、[ブログに書かれたすべての開発者ノート](https://make.wordpress.org/core/tag/dev-notes)、あるいは[特定のコンポーネントの開発者ノート](https://make.wordpress.org/core/tag/dev-notes+rest-api/)があります。

## Attribution

<!--
When the dev note is published, a “props” line at the very bottom should always be included. For example: “*Props* [](https://wordpress.slack.com/team/U02SVSW3U)*@janedoe for technical review,* [](https://wordpress.slack.com/team/U02RR5UTA)*@johndoe for proofreading.*“
-->

開発者ノートを公開するときには、必ず一番下に「props」の行を入れるようにしてください。たとえば、「**Props [@janedoe](https://wordpress.slack.com/team/U02SVSW3U) による技術的なレビュー, [@johndoe](https://wordpress.slack.com/team/U02RR5UTA) による校正**」などです。

<!--
This ensures everyone that contributed to the post receives proper recognition, helps the reader know the voices behind the post, and who they are addressing if there are comments or questions.
-->

こうすることで、その投稿に貢献したすべての人が正しく評価され、読者は投稿の関係者を知ることができ、コメントや質問がある場合は誰に向けて発信しているのかが分かります。
