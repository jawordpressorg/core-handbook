<!--
# Bug Gardening
-->

# バグガーデニング

<!--
Not only is it important to [beta test](https://make.wordpress.org/core/handbook/testing/beta/) point release and bleeding edge WordPress nightly builds, but it’s also important to test and confirm reported bugs, and test patches submitted for possible inclusion to WordPress before they ever make it into the nightly builds. This job is mostly handled by volunteers (such as yourself) that serve as **bug gardeners**.
-->

[ベータテスト](https://make.wordpress.org/core/handbook/testing/beta/)ポイントリリースや最先端の WordPress ナイトリービルドだけでなく、報告されたバグのテストや確認、WordPress に組み込まれる可能性のあるパッチをナイトリービルドに組み込まれる前にテストすることも重要です。この仕事は、**バグを修正する人**として働く (あなたのような) ボランティアによって主に処理されます。

<!--
The [bug tracker](https://make.wordpress.org/core/handbook/trac/) contains numerous, wildly different [workflows](https://make.wordpress.org/core/handbook/trac/keywords/) through which all types of reported bugs, enhancements, new features, and various tasks are handled by reporters, gardeners, developers, and committers. It can be incredibly confusing trying to grasp the big picture all at once, but you don’t have to.
-->

[バグトラッカー](https://make.wordpress.org/core/handbook/trac/)には、報告者、修正する人、開発者、コミッターによって処理される、報告されたあらゆる種類のバグ、機能強化、新機能、およびさまざまなタスクなどの多種多様な[ワークフロー](https://make.wordpress.org/core/handbook/trac/keywords/)が含まれています。全体像を一度に把握しようとすると非常に混乱するかもしれませんが、その必要はありません。

<!--
If you are new to the bug tracker and want to help out, here’s how you can get started with your first simple workflow. Once you have spent some time in this workflow, the rest of the tracker will become much more familiar, and you can feel confident in exploring other areas of Trac that also need help.
-->

バグトラッカーを初めて使用する場合、手伝いたい場合は、ここで最初の簡単なワークフローを始めることができます。一度このワークフローに時間を費やせば、トラッカーの他の部分がよりよく理解できるようになり、同様にサポートが必要な Trac の他の領域でも自信を持って探索できます。

<!--
Keep an eye on [upcoming WordPress meetings](https://make.wordpress.org/meetings/) to join a bug scrub.
-->

バグスクラブに参加するには、[今後の WordPress ミーティング](https://make.wordpress.org/meetings/)に注目してください。

<!--
## The Bugfix Review Workflow
-->

## バグ修正レビューのワークフロー

<!--
In this workflow, we are only going to work on tickets categorized as **bugs/defects**, and also just the ones with patches attached that supposedly fix those bugs. Additionally, this workflow only involves tickets in the **Awaiting Review** or the **Future Release** milestones, meaning that these are mostly reported bugs and patches that have not been reviewed or thoroughly tested yet. The [Patches to Defects That Need Review](https://core.trac.wordpress.org/report/46) report in Trac handles these filters for you already, so go ahead and open that now.
-->

このワークフローでは、**bugs/defects** に分類されるチケットと、それらのバグを修正すると思われるパッチが添付されたチケットのみを扱います。さらに、このワークフローは **Awaiting Review** または **Future Release** マイルストーンにあるチケットのみを対象としています。つまり、これらのチケットはほとんどが、まだレビューや徹底的なテストが行われていない、報告されたバグやパッチです。Trac の [Patches to Defects That Need Review](https://core.trac.wordpress.org/report/46) レポートはこれらのフィルターをすでに処理しているため、今すぐ開いてください。

<!--
There are over 600 unique tickets in the report (at the time of this writing), so the first step is to choose one of those to start with. If you are just starting out as a bug gardener, we recommend avoiding any tickets more than 12 months old. Older tickets usually involve some controversial changes, or involve complex problems with complex solutions, requiring a heavier review process, which is usually why they have been stuck in the review process for more than a year.
-->

このレポートには、(この記事の執筆時点で) 600を超える固有のチケットがあるため、最初のステップは、そのうちの1つを選択して開始することです。もしあなたがバグ修正を始めたばかりなら、12ヵ月以上前のチケットは避けることをおすすめします。古いチケットは通常、議論を呼ぶような変更を含んでいたり、複雑な解決策を伴う複雑な問題が含まれており、より厳しいレビュープロセスを必要とします。そのため、通常レビュープロセスが1年以上滞っています。

<!--
You should try to work on tickets related to parts of WordPress that you are familiar with. The report is grouped by component, which makes the task of finding your first ticket to work on much easier.
-->

自分がよく知っている WordPress の部分に関連するチケットに取り組むようにしてください。レポートはコンポーネントごとにグループ化されているので、最初に作業するチケットを見つけることがとても簡単になります。

<!--
Last, you should skip over any tickets with the **reporter-feedback** or **dev-feedback** keywords – you won’t be able to do anything with those tickets without more information from the reporter or a core developer.
-->

最後に、**reporter-feedback** または **dev-feedback** というキーワードのチケットはスキップしてください。報告者またはコア開発者からの詳しい情報がなければ、これらのチケットに対して何も行うことはできません。

<!--
Once you have found a ticket you want to work on, continue reading the rest of the instructions here for how you should address the ticket you have picked out.
-->

取り組みたいチケットを見つけたら、選んだチケットにどのように対処すべきか、ここでの残りの手順を読み進めてください。

<!--
### 1\. Ensure The Ticket Is A Bug
-->

### 1\. チケットがバグであることを確認する

<!--
The first step required for any of the tickets in this report is to ensure that the ticket is in fact a bug, and not a feature request or enhancement.
-->

このレポートのチケットに必要な最初のステップは、そのチケットが機能リクエストや機能強化ではなく、実際にバグであることを確認することです。

<!--
Since new tickets are assigned to the **Awaiting Review** milestone by default, this report will include completely fresh issues, assuming the reporter attached a patch and added the **has-patch** keyword properly upon submission. Some of these tickets have not been through an initial review to ensure it was submitted with the proper issue type, component, and keywords. The documentation on the [ticket properties](https://make.wordpress.org/core/handbook/trac/#ticket-properties) should help clarify exactly which values the ticket type and component should be set as, and what keywords the ticket should have.
-->

新しいチケットはデフォルトで **Awaiting Review** マイルストーンに割り当てられるため、報告者がパッチを添付し、**has-patch** キーワードを適切に追加して提出したと仮定すると、このレポートには完全に新しい問題が含まれます。これらのチケットの中には、適切な issue タイプ、コンポーネント、キーワードで提出されたことを確認するための初期レビューが行われていないものがあります。[チケットプロパティ](https://make.wordpress.org/core/handbook/trac/#ticket-properties)のドキュメントは、チケットの種類とコンポーネントがどのような値に設定されるべきか、そしてチケットがどのようなキーワードを持つべきかを明確にするために役立つはずです。

<!--
Considering what is involved for new tickets to be included in this report, the reporters submitting tickets listed here usually have a fairly good feel for the ticket properties and how they should be set. However, this is one of those exceptions to the rule – you will need to be much more critical of this in other workflows.
-->

新しいチケットがこのレポートに含まれるために必要なことを考慮すると、通常、ここにリストされたチケットを提出している報告者は、チケットのプロパティとその設定方法について十分に理解しています。ただし、これはルールの例外の1つであり、他のワークフローではこの点にもっと注意を払う必要があります。

<!--
The most common problem you need to watch for in this workflow are tickets that have been submitted as a **defect**, but in reality, the issue (and patch) is actually an **enhancement** or a **feature request**. If the ticket describes new functionality, or even a change to existing functionality that is working perfectly fine (but perhaps not in the most ideal way), then the ticket type needs to be set as an enhancement (in the case of a change/addition to an existing component), or as a feature request (in the case of entirely new features). If this happens, fix the ticket type, and move on to the next ticket.
-->

このワークフローで注意しなければならない最も一般的な問題は、**不具合**として提出されたチケットですが、実際にはその問題 (およびパッチ) は**機能強化**または**機能リクエスト**であるものです。チケットに新しい機能、あるいは完全に問題なく動作している (ただし、おそらく最も理想的な方法ではない) 既存の機能への変更が記述されている場合、チケットの種類は機能強化 (既存のコンポーネントの変更/追加の場合)、または機能リクエスト (まったく新しい機能の場合) として設定する必要があります。この場合、チケットの種類を修正し、次のチケットに進んでください。

<!--
If the ticket is actually a bug, you need to confirm that the reported bug is, in fact, one that can be reproduced.
-->

チケットが実際にバグである場合、報告されたバグが実際に再現可能なものであることを確認する必要があります。

<!--
### 2\. Confirm The Bug
-->

### 2\. バグを確認する

<!--
You should always test for the bug using a [SVN trunk](https://make.wordpress.org/core/handbook/svn/) checkout of WordPress. In the rare cases of critical bugs and regressions, then you should also test for the bug in the latest stable release of WordPress too.
-->

常に、WordPress の [SVN trunk](https://make.wordpress.org/core/handbook/svn/) チェックアウトを使用してバグをテストする必要があります。まれに重大なバグやリグレッションが発生する場合は、WordPress の最新の安定版リリースでもバグをテストしてください。

<!--
Remember that it’s possible the bug only exhibits itself under specific versions of PHP, MySQL, browsers, and/or certain WordPress settings (i.e. multisite, roles/capabilities, different plugins/themes).
-->

バグが特定のバージョンの PHP、MySQL、ブラウザ、特定の WordPress 設定 (マルチサイト、ユーザーの種類と権限、異なるプラグイン/テーマなど) でのみ発生する可能性があることも覚えておいてください。

<!--
*   If the reporter wasn’t clear and you can’t reproduce it, ask for clarification from the reporter, and add the **reporter-feedback** keyword to the ticket.
*   If the reporter was very clear, and you still can’t reproduce the bug under their claimed conditions, leave a note that you tested it and couldn’t reproduce the bug.
*   If you are the second tester (besides the reporter) that can’t reproduce the bug, there’s a chance that something else could be wrong with the reporter’s installation/configuration. If this happens, add the **dev-feedback** keyword to the ticket, and move to the next ticket.
-->

*   報告者の説明が明確でなく、再現できない場合は、報告者に説明を求め、チケットに **reporter-feedback** キーワードを追加してください。
*   もし報告者の説明が非常に明確で、あなたが彼らの説明する条件下でまだバグを再現できない場合、テストしてバグを再現できなかったというメモを残してください。
*   もしあなたがバグを再現できない (報告者を除く) 二人目のテスターである場合は、報告者のインストール/設定に何か他の問題がある可能性があります。この場合、チケットに **dev-feedback** キーワードを追加し、次のチケットに進んでください。

<!--
### 3\. Confirm The Patch
-->

### 3\. パッチを確認する

<!--
If you were able to reproduce the bug, then it is time to confirm the patch. Don’t worry too much about how the patch was written, unless you are a more experienced developer and can immediately spot problems with the way the patch was written.
-->

バグを再現できた場合は、パッチを確認します。あなたが経験豊富な開発者で、パッチの書き方に問題があることをすぐに見つけられるのでない限り、パッチがどのように書かれたかについてはあまり気にしないでください。

<!--
[Download and apply the suggested patch](https://make.wordpress.org/core/handbook/tutorials/working-with-patches/#creating-and-applying-patches-with-grunt) to the same installation you were able to confirm the bug on. Sometimes a ticket will have multiple patches attached, and, if so, usually only the latest suggested patch needs testing; however, you might need to test the other patches too, if they haven’t been tested.
-->

あなたがバグを確認できた同じインストール環境に、[提案されたパッチをダウンロードして適用](https://make.wordpress.org/core/handbook/tutorials/working-with-patches/#creating-and-applying-patches-with-grunt)します。チケットに複数のパッチが添付されていることがありますが、その場合、通常は最新の提案されたパッチだけをテストする必要があります。ただし、他のパッチがテストされていない場合は、それらもテストする必要がある場合があります。

<!--
If any of the following conditions apply, remove the **has-patch** keyword, and add the **needs-patch** keyword:
-->

次の条件のいずれかに当てはまる場合、**has-patch** キーワードを削除し、**needs-patch** キーワードを追加してください:

<!--
*   The patch does not apply cleanly, or does not follow the [coding standards](https://make.wordpress.org/core/handbook/coding-standards/). Add the **needs-refresh** keyword for this case.
*   The patch does not fix the bug. This seems obvious, but some patches might not have been written for the development version of WordPress, yet still apply cleanly where things have changed. The patch might only fix the bug under a specific version of PHP and MySQL, or won’t fix the bug in multisite.
*   The patch introduces new errors or warning messages. Remember to test with debug turned on.
*   New [unit tests](https://make.wordpress.org/core/handbook/automated-testing/) fail with the patch applied.
*   The patch does not use appropriate [data validation and output sanitization](https://codex.wordpress.org/Data_Validation), or doesn’t make checks against user roles and capabilities when it should.
*   The patch is not adequate for any other reason not covered here. We strive for legible, efficient, and secure code in WordPress, so don’t be afraid to point out areas of a patch that should be improved, even if it does actually fix the bug.
-->

*   パッチが適切に適用されないか、[コーディング規約](https://make.wordpress.org/core/handbook/coding-standards/)に従っていない。この場合、**needs-refresh** キーワードを追加してください。
*   パッチがバグを修正しない。これは当然のことのように思えますが、WordPress の開発バージョン用に書かれたものではないパッチでも、変更された箇所にはきちんと適用されることがあります。パッチは特定のバージョンの PHP と MySQL でのみバグを修正するかもしれませんし、マルチサイトではバグを修正しないかもしれません。
*   パッチによって新しいエラーや警告メッセージが発生する。デバッグを有効にしてテストすることを忘れないでください。
*   パッチが適用されると、新しい[単体テスト](https://make.wordpress.org/core/handbook/automated-testing/)が失敗する。
*   パッチが適切な[データ検証と出力のサニタイズ](https://codex.wordpress.org/Data_Validation)を使っていないか、ユーザーの種類と権限をチェックすべきときにチェックをしていない。
*   パッチが、ここで説明されていないその他の理由により適切ではない。私たちは、WordPress において読みやすく、効率的で安全なコードを目指しています。そのため、たとえ実際にバグが修正されていたとしても、パッチの改善すべき点を指摘することを恐れないでください。

<!--
Make sure you explain why the patch cannot be accepted in the ticket notes, in addition to removing the **has-patch** keyword and adding **needs-patch**. If, however, the patch looks good on all fronts, then you should explain what aspects of the patch you tested in the ticket notes, and triage the ticket next.
-->

また、**has-patch** キーワードを削除し、**needs-patch** を追加するだけでなく、パッチが受け入れられない理由をチケットのノートで必ず説明してください。ただし、パッチがすべての面で良いものである場合は、パッチのどのような点をテストしたかをチケットのメモで説明し、次にそのチケットをトリアージしてください。

<!--
### 4\. Triage The Ticket
-->

### 4\. チケットのトリアージ

<!--
With both the bug and patch confirmed, the priority of the ticket often still needs to be adjusted in this workflow. We also need to decide whether the patch should be applied in the next [point release](https://make.wordpress.org/core/glossary/#point-release) (x.x.x), the next [major release](https://make.wordpress.org/core/glossary/#major-release) (x.x), or if it should still be delayed farther into the future.
-->

バグとパッチの両方が確認された場合でも、多くの場合、このワークフローではチケットの優先度を調整する必要があります。また、そのパッチを次の[ポイントリリース](https://make.wordpress.org/core/glossary/#point-release) (x.x.x) で適用するのか、次の[メジャーリリース](https://make.wordpress.org/core/glossary/#major-release) (x.x) で適用するのか、それともさらに将来に延期するのかを決定する必要があります。

<!--
**Note:** New Trac users do not have the ability to adjust the priority of a ticket or move it to a different milestone by default, so until you feel comfortable with this workflow and Trac in general, this step will require you to simply add a note to the ticket explaining that the priority or milestone should be adjusted. One of the other bug gardeners will see the update, and adjust the ticket accordingly if it looks correct. When you feel comfortable making these adjustments yourself, you can request access on the [Make WordPress Core](https://make.wordpress.org/core/) blog.
-->

**注意:** 新しい Trac ユーザーには、デフォルトではチケットの優先度を調整したり、チケットを別のマイルストーンに移動したりする機能がありません。そのため、このワークフローと Trac 全体に慣れるまでは、このステップでは優先度やマイルストーンを調整する必要があることを説明するメモをチケットに追加するだけです。バグを修正する他の人が更新を確認し、それが正しいと思われる場合は、それに応じてチケットを調整します。これらの調整を自分で行うことに慣れたら、[Make WordPress Core](https://make.wordpress.org/core/) ブログでアクセスをリクエストできます。

<!--
Tickets related to [regressions](https://make.wordpress.org/core/glossary/#regression) and critical bugs should be immediately set to the highest priority, and assigned to the next point release milestone. Regressions are broken features that were working perfectly fine in the latest release or the WordPress release before that, and we take these seriously. The same goes for critical bugs which may not be a regression, but still involves an aspect of a major feature being broken for a majority of users. This mostly refers to bugs with high exposure, such as breaking the public-facing side of WordPress, or major breaks in the administration panel. This should be very rare, and should be used sparingly.
-->

[リグレッション](https://make.wordpress.org/core/glossary/#regression)や重大なバグに関連するチケットは、すぐに最優先事項に設定し、次のポイントリリースのマイルストーンに割り当ててください。リグレッションとは、最新リリースやその前の WordPress リリースではまったく問題なく動作していた機能が壊れていることであり、私たちはこれらを真剣に受け止めています。リグレッションとまではいかなくても、多数のユーザーにとっての主要な機能が壊れているような重大なバグも同様です。これは主に、WordPress の公開側を壊してしまったり、管理パネルが大きく壊れてしまったりするような、露出度の高いバグを指します。これは非常にまれであり、慎重に扱われるべきです。

<!--
Tickets involving patches that fix simple typos, add [inline documentation](https://make.wordpress.org/core/glossary/#inline-docs), or fix minor style/appearance issues, should be set to a lower priority.
-->

単純なタイプミスの修正、[インラインドキュメント](https://make.wordpress.org/core/glossary/#inline-docs)の追加、小さなスタイル/外観の問題の修正などのパッチを含むチケットは、優先順位を低く設定してください。

<!--
All remaining tickets in this workflow should be triaged to the next major release milestone. This does not normally apply to all tickets in general, just confirmed defects with quality patches, which is all this workflow deals with. If the WordPress development cycle is in the middle of release candidates for the next major release, critical bug fixes should still be assigned to the **Next Release** milestone; however, everything else should be moved to the **Future Release** milestone, and should also be tagged with the keyword **x.x-early** (where x.x is the next major release after the one with a release candidate out). For example, during the 3.6 release candidate phase, confirmed fixes for non-critical bugs should be tagged with the **3.7-early** keyword.
-->

このワークフローの残りのチケットはすべて、次のメジャーリリースのマイルストーンにトリアージされるべきです。これは通常、すべてのチケットに適用されるわけではなく、ワークフローでは品質パッチを伴う確認済みの不具合のみに適用されます。WordPress の開発サイクルが次のメジャーリリースのリリース候補の途中である場合、重要なバグ修正は引き続き **Next Release** マイルストーンに割り当てる必要があります。ただし、それ以外のものはすべて **Future Release** マイルストーンに移し、**x.x-early** というキーワードもつける必要があります (x.x は、リリース候補が出ているリリースの次のメジャーリリースです)。たとえば、3.6のリリース候補の段階では、重大ではないバグに対する確認済みの修正には、**3.7-early** というキーワードをつける必要があります。

<!--
## Learn More
-->

## より詳しく

*   [Get Involved With Trac Bug Gardening](http://helen.wordpress.com/2013/08/09/scared-of-wordpress-core-trac-but-want-to-give-it-a-shot-try-trac-gardening/)
