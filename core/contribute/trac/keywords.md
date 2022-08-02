<!--
# Trac Workflow Keywords
-->

# Trac ワークフローキーワード

<!--
There are a number of **keywords** with a defined meaning. These are commonly used to manage the workflows of specific tickets, as well as releases, and to generate reports. Keywords should not be thought of as generic “tags,” which are not necessary.
-->

定義された意味を持ついくつかの**キーワード**があります。これらは一般的に、特定のチケットやリリースのワークフローを管理したり、レポートを生成するために使用されます。

<!--
## Status-based Keywords
-->

## ステータスにもとづいたキーワード

**changes-requested**

<!--
Feedback has been provided, and the attached patch needs to be updated.
-->

フィードバックがあったため、添付されたパッチを更新する必要があります。

**close**

<!--
The ticket is a candidate for closure with a disposition other than fixed (i.e. **wontfix**, **worksforme**, **invalid**, or **duplicate**). Often seen with **reporter-feedback** or **2nd-opinion**; otherwise, the ticket would have been closed in lieu of adding the **close** keyword.
-->

このチケットは、修正以外の処理によってクローズされる候補です (例: **wontfix**、**worksforme**、**invalid**、または **duplicate**)。しばしば **reporter-feedback** や **2nd-opinion** と一緒に付与される事があります。そうでなければ、チケットは **close** キーワードを追加する代わりにクローズされているはずです。

**early**

<!--
This keyword should only be applied by committers. The keyword signals that the ticket is a priority, and should be handled early in the next release cycle.
-->

このキーワードはコミッターのみが付与できます。このキーワードは、そのチケットが優先され、次のリリースサイクルの早い段階で取り組むべきものであることを示します。

**good-first-bug**

<!--
This keyword signals that the ticket would be a good starting point for new contributors to get used to the process before tackling more complicated tickets.
-->

このキーワードは、新しい貢献者がより複雑なチケットに取り組む前に、プロセスに慣れるための良い出発点であることを示します。

**has-patch**

<!--
A proposed solution to the ticket has been attached, and it is ready for review.
-->

チケットに解決案が添付され、レビューの準備ができています。

**has-screenshots**

<!--
Serves as a partner to *needs-screenshots*. Once a ticket has at least one screenshot, tag it with has-screenshots. If more screenshots are needed, leave needs-screenshots on the ticket until all screenshots are provided. [#has-screenshots](https://core.trac.wordpress.org/query?status=accepted&status=assigned&status=closed&status=new&status=reopened&status=reviewing&keywords=~has-screenshots&col=id&col=summary&col=status&col=owner&col=type&col=priority&col=milestone&col=changetime&order=priority) is used to create visual changelogs and the [Today in the Nightly](https://make.wordpress.org/core/tag/today-in-the-nightly/) posts. Do not clear this tag from closed tickets. has-screenshot and needs-screenshots are part of the post-commit diligence lifecycle and are expected to exist on closed tickets. need-screenshots exists temporarily until all screenshots are provided and has-screenshots exists permanently.
-->

*needs-screenshots* と一緒に機能します。チケットに少なくとも1枚のスクリーンショットがあれば、has-screenshots とタグ付けします。さらにスクリーンショットが必要な場合は、すべてのスクリーンショットが提供されるまで、チケットに needs-screenshots を残してください。[#has-screenshots](https://core.trac.wordpress.org/query?status=accepted&status=assigned&status=closed&status=new&status=reopened&status=reviewing&keywords=~has-screenshots&col=id&col=summary&col=status&col=owner&col=type&col=priority&col=milestone&col=changetime&order=priority) は視覚的な変更履歴と [今日の最新情報](https://make.wordpress.org/core/tag/today-in-the-nightly/) の投稿を作成するために使用されます。クローズされたチケットからこのタグを消さないでください。has-screenshot と needs-screenshots はコミット後のライフサイクルの一部であり、クローズドチケットに存在することが期待されます。need-screenshots はすべてのスクリーンショットが提供されるまで一時的に存在し、has-screenshots は永続的に存在します。

**has-unit-tests**

<!--
The ticket has been reviewed, found to be desirable to solve, and the latest patch contains unit tests. Like *needs-unit-tests*, this keyword indicates the proposed changes constitute a high risk of causing other issues.
-->

チケットはレビューされ、解決することが望ましいと判断され、最新のパッチはユニットテストを含んでいます。このキーワードは *needs-unit-tests* と同様に、提案された変更が他の問題を引き起こす危険性が高いことを示します。

**needs-codex**

<!--
Documentation in the Codex needs updating or expanding. Remove the keyword from the ticket once the Codex is updated.
-->

Codex のドキュメントを更新または追加する必要があります。Codex が更新されたら、チケットからキーワードを削除してください。

**needs-docs**

<!--
Inline documentation for the code is needed. These are either place holder tickets for individual files, or tickets with patches for new functions which need documenting before they are committed.
-->

コードのためのインラインドキュメントが必要です。これらは、個々のファイルに対するプレースホルダーチケットか、コミットする前に文書化が必要な新機能のパッチを持つチケットのどちらかです。

**needs-patch**

<!--
The ticket has been reviewed, found to be desirable to solve, and marked as especially needing a patch, or the submitted patch doesn’t work and needs to be redone.
-->

このチケットはレビューされ、解決することが望ましいと判断され、特にパッチが必要であるとマークされています。または、提出されたパッチが動作せず、やり直しが必要な場合です。

**needs-refresh**

<!--
A submitted patch no longer applies cleanly to the WordPress core files, usually because nearby code has been modified since the patch was submitted. The patch needs to be merged and re-submitted.
-->

パッチが提出された後、近くのコードが変更されたため、提出されたパッチが WordPress のコアファイルにきれいに適用されなくなった場合です。パッチをマージして再提出する必要があります。

**needs-screenshots**

<!--
Patches and commits that change UI need screenshots. Document visual iterations. Upload screenshots directly to the ticket or post to [make/flow](https://make.wordpress.org/flow/) for more involved visual documentation such as visual records or visual surveys. Cross-link any make/flow posts with the ticket. Remove the needs-screenshots keyword from the ticket once screenshots for both a desktop and a phone, at the least, are provided. Full context screenshots taken on physical devices are preferred. New patches require new screenshots. Once a ticket has at least one of the needed screenshots, tag it with has-screenshots. [#needs-screenshots](https://core.trac.wordpress.org/query?status=accepted&status=assigned&status=closed&status=new&status=reopened&status=reviewing&keywords=~needs-screenshots&col=id&col=summary&col=status&col=owner&col=type&col=priority&col=milestone&order=priority)
-->

UIを変更するパッチやコミットにはスクリーンショットが必要です。視覚的なイテレーションを文書化します。スクリーンショットをチケットに直接アップロードするか、音声や映像記録のようなより複雑なドキュメントの場合は [make/flow](https://make.wordpress.org/flow/) に投稿してください。make/flow の投稿は、すべてチケットと相互にリンクしてください。少なくともデスクトップとモバイルの両方のスクリーンショットが提供されたら、チケットから needs-screenshots キーワードを削除してください。物理的なデバイスで撮影されたフルコンテキストを持つスクリーンショットが望ましいです。新しいパッチでは、新しいスクリーンショットが必要です。チケットに必要なスクリーンショットが少なくとも1枚あれば、has-screenshots というタグを付けてください。[#needs-screenshots](https://core.trac.wordpress.org/query?status=accepted&status=assigned&status=closed&status=new&status=reopened&status=reviewing&keywords=~needs-screenshots&col=id&col=summary&col=status&col=owner&col=type&col=priority&col=milestone&order=priority)

**needs-unit-tests**

<!--
The ticket has been reviewed, found to be desirable to solve, and we would like some unit tests written to test the functionality and any patch that may exist before committing a change, as the risk of causing other issues is high.
-->

このチケットはレビューされ、解決することが望ましいと判断されました。そして、他の問題を引き起こすリスクが高いため、機能および存在する可能性のあるパッチをテストするために、変更をコミットする前にいくつかのユニットテストを書くことが推奨されています。

<!--
## Action-based Keywords
-->

## アクションにもとづいたキーワード

**2nd-opinion**

<!--
Another person is needed to express an opinion about the problem or the solution.
-->

問題や解決策について別の意見が必要です。

**commit**

<!--
The patch has been reviewed and tested by a trusted member of the development community; therefore, the patch should be considered a commit candidate, and is ready to be added to the WordPress core files.
-->

このパッチは、開発コミュニティの信頼できるメンバーによってレビューおよびテストされています。したがって、このパッチはコミット候補とみなされ、WordPress のコアファイルに追加する準備ができています。

**dev-feedback**

<!--
A response is wanted from a [core developer](https://make.wordpress.org/core/handbook/about/organization/#the-wordpress-core-team) or trusted members of the development community.
-->

[コア開発者](https://make.wordpress.org/core/handbook/about/organization/#the-wordpress-core-team)または開発コミュニティの信頼できるメンバーからの回答が求められています。

**dev-reviewed**

<!--
After a branch has been created for a release, each change (except for build and test suite changes) needs to be reviewed by two permanent committers. The first reviewer should set the keywords “commit dev-feedback”, and the second reviewer should set the keywords “commit dev-reviewed”. If a permanent committer created the patch, only one additional review is necessary.
-->

リリースのためにブランチが作成された後、各変更は (ビルドとテストスイートの変更を除いて) 2人のレギュラーコミッターによってレビューされる必要があります。最初のレビュアーは「commit dev-feedback」というキーワードを設定し、2番目のレビュアーは「commit dev-reviewed」というキーワードを設定しなければなりません。レギュラーコミッターがパッチを作成した場合、追加で必要なレビューは1回だけです。

**fixed-major**

<!--
Only used late in the development cycle (after a branch has been created for a release) to indicate that an issue has been “fixed” in the next “major” version (trunk) and needs to be merged back to the branch for the upcoming release by a permanent committer.  (There is also “fixed-minor” which indicates that an issue needs to be merged back into trunk from a minor release branch; more info about these keywords in this post: [The keywords “fixed-major” and “fixed-minor”](https://make.wordpress.org/core/2011/04/06/the-keywords-fixed-major-and-fixed/).)
-->

開発サイクルの後半 (リリース用のブランチが作成された後) で、次の「メジャー」バージョン (trunk) で問題が「修正」され、レギュラーコミッターによって次のリリース用のブランチにマージされる必要があることを示します (マイナーリリースブランチから trunk にマージする必要があることを示す「fixed-minor」というキーワードもあります。これらのキーワードの詳細については、こちらの記事をご覧ください。[「fixed-major」と「fixed-minor」キーワード](https://make.wordpress.org/core/2011/04/06/the-keywords-fixed-major-and-fixed/))。

**has-copy-review**

<!--
Input has been given from a copywriter reviewing the suggested verbiage changes.
-->

コピーライターが文言の変更案を検討し、意見を述べました。

**has-dev-note**

<!--
A [dev note](https://make.wordpress.org/core/tag/dev-notes/) has been published on the make core blog outlining this change. This change provides significant new functionality, a large refactor, or includes a breaking change.
-->

この変更の概要を説明する [dev note](https://make.wordpress.org/core/tag/dev-notes/) が make core ブログに掲載されました。この変更は、重要な新機能を提供したり、大規模なリファクタリングを行ったり、破壊的な変更を含んでいます。

**has-privacy-review**

<!--
Input has been given from the [core privacy team](https://make.wordpress.org/core/components/privacy/) reviewing the privacy implications of the suggested changes.
-->

提案された変更に対して、プライバシーへの影響を検討する[コアプライバシーチーム](https://make.wordpress.org/core/components/privacy/)から意見が出されました。

**i18n\-change**

<!--
Only used late in the development cycle (after string freeze) to track potential string changes, as translators need to be notified.
-->

開発サイクルの後半 (翻訳文字列のフリーズ後) にのみ使用し、翻訳者に通知するために、翻訳文字列の変更の可能性を追跡します。

**needs-copy-review**

<!--
Input is needed from a copywriter with regards to the suggested verbiage changes.
-->

コピーライターの意見が必要となる文言の変更案です。

**needs-design**

<!--
A designer should create a prototype of how the suggested changes should look/behave before writing code.
-->

デザイナーはコードを書く前に、提案された変更がどのように見えるかまたは動作するかを確認するためのプロトタイプを作成する必要があります。

**needs-design-feedback**

<!--
A designer should review and give feedback on the proposed changes.
-->

デザイナーは、変更案を確認し、フィードバックする必要があります。

**needs-dev-note**

<!--
This change is one that warrants a [dev note](https://make.wordpress.org/core/tag/dev-notes/) on the make core blog. If a change is significant new functionality, a large refactor, or includes a breaking change, it always requires a dev note.
-->

この変更は、make core ブログに [dev note](https://make.wordpress.org/core/tag/dev-notes/) を掲載する価値のあるものです。もしその変更が重要な新機能や大規模なリファクタリング、あるいは破壊的な変更を含んでいるならば、常に dev note を必要とします。

**needs-privacy-review**

<!--
Input is needed from the [core privacy team](https://make.wordpress.org/core/components/privacy/) with regards to the privacy implications of the suggested changes.
-->

提案された変更のプライバシーへの影響に関して、[コアプライバシーチーム](https://make.wordpress.org/core/components/privacy/)からの意見が必要です。

**needs-testing**

<!--
One or more people are needed to test the solution. When testing a patch, please comment with the patch filename that was tested, how the patch was tested, and which version of WordPress was used (including the SVN revision number, if it is not an officially released version).
-->

解決策をテストするために、一人または複数の人が必要です。パッチをテストするときには、テストしたパッチのファイル名、パッチのテスト方法、使用した WordPress のバージョン (正式リリース版でない場合は SVN リビジョン番号も含む) をコメントで知らせてください。


**reporter-feedback**

<!--
A response is needed from the reporter. Further investigation is unlikely without a response to the questions from someone experiencing the problem.
-->

報告者からの回答が必要です。問題を調査している人からの質問への回答がなければ、さらなる調査は望めません。
