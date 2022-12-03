<!--
# JavaScript Docs
-->

# JavaScript ドキュメント

<!--
This initiative follows the [inline docs initiative](https://make.wordpress.org/docs/handbook/core/inline-docs/) with a specific focus on JavaScript. The goal is to get all JavaScript files in WordPress well documented and make this documentation easily accessible. JavaScript development within WordPress core is speeding up fast and becoming more and more prominent given the current core editor and REST API focuses. To help these developments progress as smoothly as possible, we need to make sure the existing code is documented well.
-->

この取り組みは、[インラインドキュメントの取り組み](https://make.wordpress.org/docs/handbook/core/inline-docs/)に続いて、特に JavaScript に重点を置いています。目標は、WordPress のすべての JavaScript ファイルをきちんとドキュメント化し、この文書に簡単にアクセスできるようにすることです。WordPress コアにおける JavaScript の開発は急速にスピードアップしており、現在のコアエディターと REST API に焦点を当てるとますます顕著になってきています。これらの開発をできるだけスムーズに進めるために、既存のコードをしっかりとドキュメント化する必要があります。

<!--
If you’re not familiar with what inline documentation is, read our page [on inline documentation standards](https://make.wordpress.org/core/handbook/best-practices/inline-documentation-standards/).
-->

インラインドキュメントとは何かをよく知らない人は、私たちのページである[インラインドキュメントの規格について](https://make.wordpress.org/core/handbook/best-practices/inline-documentation-standards/)を読んでみてください。


<!--
## Which JS files should be documented?
-->

## どの JS ファイルをドキュメント化するべきか ?

<!--
There are three pages tracking JS files for documentation:
-->

ドキュメント用の JS ファイルを追跡している3つのページがあります。

<!--
*   [Unclaimed JS docs files](https://make.wordpress.org/core/2018/01/31/js-docs-initiative-add-inline-docs-for-javascript/): Nobody is working on documenting these files yet. You can claim a file by commenting on the post.
*   [In progress JS docs file tickets](https://make.wordpress.org/core/handbook/docs/inline/js/in-progress-tickets/): These files have patches with documentation or someone is working on creating a documentation patch.
*   [Closed JS docs file tickets](https://make.wordpress.org/core/handbook/docs/inline/js/closed-tickets/): These files have been documented already.
-->

*   [Unclaimed JS docs files](https://make.wordpress.org/core/2018/01/31/js-docs-initiative-add-inline-docs-for-javascript/): これらのファイルをドキュメント化する作業はまだ誰も行っていません。投稿にコメントすることで、ファイルを担当できます。
*   [進行中の JS ドキュメントファイルのチケット](https://make.wordpress.org/core/handbook/docs/inline/js/in-progress-tickets/): これらのファイルには、ドキュメントを含むパッチがあるか、誰かがドキュメントのパッチを作成する作業しています。
*   [クローズされた JS ドキュメントファイルのチケット](https://make.wordpress.org/core/handbook/docs/inline/js/closed-tickets/): これらのファイルは、すでに文書化されています。

<!--
## How to get involved
-->

## 参加方法について

<!--
Inline documentation is considered to be “technical” documentation, so some familiarity with the WordPress codebase will be necessary – you have to understand the code to write about it.
-->

インラインドキュメントは「技術的」なドキュメントとみなされるため、WordPress のコードベースについてある程度の知識が必要となり、コードを理解する必要があります。

<!--
1\. Familiarize yourself with the [JavaScript documentation standard](https://make.wordpress.org/core/handbook/best-practices/inline-documentation-standards/javascript/), as well as the [formatting guidelines](https://make.wordpress.org/core/handbook/best-practices/inline-documentation-standards/php/#formatting-guidelines) and [documenting tips](https://make.wordpress.org/core/handbook/best-practices/inline-documentation-standards/javascript/#documenting-tips).
-->

1\. [JavaScript ドキュメントスタンダート](https://make.wordpress.org/core/handbook/best-practices/inline-documentation-standards/javascript/)をはじめ、[書式ガイドライン](https://make.wordpress.org/core/handbook/best-practices/inline-documentation-standards/php/#formatting-guidelines)や[ドキュメント作成のヒント](https://make.wordpress.org/core/handbook/best-practices/inline-documentation-standards/javascript/#documenting-tips)をよく理解してください。

<!--
2\. Set up a local copy of the developer version of the WordPress codebase using [Varying Vagrant Vagrants](https://make.wordpress.org/core/handbook/tutorials/installing-a-local-server/installing-vvv/) (VVV). WordPress is versioning using SVN, but you can also use Git (the VVV link for how to do that).
-->

2\. [Varying Vagrant Vagrants](https://make.wordpress.org/core/handbook/tutorials/installing-a-local-server/installing-vvv/) (VVV) を使って、WordPress コードベース開発版のローカルコピーをセットアップします。WordPress は バージョン管理に SVN を使用していますが、Git を使うこともできます (その方法は VVV のリンク先にあります)。

<!--
3\. Read [Opening a Ticket](https://make.wordpress.org/core/handbook/working-with-trac/opening-a-ticket/) to learn how to create a Trac ticket.
-->

3\. Trac チケットの作り方は[チケットを開く](https://make.wordpress.org/core/handbook/working-with-trac/opening-a-ticket/)を読んでください。

<!--
4\. Creating patches:
-->

4\. パッチの作成:

<!--
*   [Claim a file to start documenting](https://make.wordpress.org/core/2018/01/31/js-docs-initiative-add-inline-docs-for-javascript/).
*   Always update your local copy of WordPress trunk before editing the file and creating patches. Use `svn up` or `git pull`, as appropriate.
*   Generate the patch from the root directory of your WordPress SVN or Git checkout.
*   It is best to name your patch file with the Trac ticket number you created, such as **12345.patch** or **12345.diff**. Either file extension is acceptable.
-->

*   [ドキュメント化を開始するファイルを担当する](https://make.wordpress.org/core/2018/01/31/js-docs-initiative-add-inline-docs-for-javascript/)。
*   ファイルを編集したりパッチを作成したりする前に、必ず WordPress trunk のローカルコピーを更新してください。必要に応じて `svn up` や `git pull` を使ってください。
*   WordPress の SVN または Git チェックアウトのルートディレクトリからパッチを生成してください。
*   パッチファイルの名前は **12345.patch** や **12345.diff** のように、作成した Trac チケット番号と同じ名前にするのがよいでしょう。拡張子はどちらでもかまいません。

<!--
5\. How to submit a patch:
-->

5\. パッチの提出方法:

<!--
*   Create a [new ticket](https://core.trac.wordpress.org/newticket) on Core Trac for the file:
    *   Suggested *Title* formats could be “JSDoc correction for path/to/file.js” or “Improve documentation for path/to/file.js”.
    *   The *Type* should be **defect (bug)**.
    *   Assign the ticket to the *Component* the file is associated with.
    *   Leave the *Version* blank.
    *   Add the **docs** and the **JavaScript** *Focus* by clicking on it.
    *   Here’s a shortcut link to create a new ticket in the `Media` component with the `docs` and `javascript` focuses and the title `JSDocs correction for`, all that is left to add is the filename in the title: [New JSDocs Ticket](https://core.trac.wordpress.org/newticket?component=Media&focuses=docs%20javascript&summary=JSDocs%20correction%20for%20)
*   Upload your patch to the Trac ticket you created, and add the keyword **has-patch**.
*   Make sure to leave a comment describing your newly-uploaded patch. Simply uploading patches doesn’t trigger a notification for anyone watching the ticket.
*   Note: Documentation changes should not mix with code changes (even whitespacing) unless the ticket specifically calls for both.
-->

*   Core Trac で、ファイルに対する [新しいチケット](https://core.trac.wordpress.org/newticket) を作成します。
    *   提案される *Title* の形式は、"JSDoc correction for path/to/file.js" または "Improve documentation for path/to/file.js" のようになります。
    *   The *Type* should be **defect (bug)**.
    *   「タイプ」は、**defect (bug)** でなければなりません。
    *   ファイルが関連付けられている「コンポーネント」にチケットを割り当てます。
    *   「バージョン」は空欄にしてください。
    *   **docs** と **JavaScript** をクリックして「フォーカス」を追加します。
    *   これは、`Media` コンポーネントに `docs` と `javascript` をフォーカスし、`JSDocs correction for` というタイトルをつけて新しいチケットを作成するショートカットリンクです。あとは、タイトルにファイル名を追加するだけです。 [新しい JS ドキュメントチケット](https://core.trac.wordpress.org/newticket?component=Media&focuses=docs%20javascript&summary=JSDocs%20correction%20for%20)
*   作成した Trac チケットにパッチをアップロードし、キーワード **has-patch** を追加してください。
*   アップロードしたパッチについて、必ずコメントを残してください。パッチをアップロードしただけでは、このチケットを見ている人には通知されません。
*   備考: ドキュメントの変更は、チケットが特に両方を要求していない限り、(たとえホワイトスペースであっても) コードの変更と一緒にしてはいけません。

<!--
6\. You can also contribute to [inline docs-related Trac tickets](https://core.trac.wordpress.org/query?status=!closed&focuses=~docs) that need iteration.
-->

6\. また、必要に応じて引き続き[インラインドキュメントに関連した Trac チケット](https://core.trac.wordpress.org/query?status=!closed&focuses=~docs) にも貢献できます。

<!--
*   If a ticket is marked **needs-patch** or **needs-refresh**, it’s possible the existing patch(es) might just need a touch-up or be refreshed against the latest trunk. Every little bit helps!
-->

*   チケットに **needs-patch** や **needs-refresh** と書かれている場合、既存のパッチに手を加えたり、最新のトランクに対して更新する必要があるかもしれません。どんな小さなことでも役に立つのです !

<!--
## Points of contact
-->

## 問い合わせ先

<!--
For any questions, pop by the [#docs](https://wordpress.slack.com/messages/docs/) channel in [Slack](https://make.wordpress.org/chat/). For JavaScript specific questions, you can also join the [#core-js](https://wordpress.slack.com/messages/core-js/) channel.
-->

質問は、[Slack](https://make.wordpress.org/chat/) の [#docs](https://wordpress.slack.com/messages/docs/) チャンネルで受け付けています。JavaScript に関する質問の場合は、[#core-js](https://wordpress.slack.com/messages/core-js/) チャンネルに参加することもできます。

<!--
## Resources
-->

## リソース

<!--
*   [JS Documentation Standard](https://make.wordpress.org/core/handbook/best-practices/inline-documentation-standards/javascript/)
-->

*   [JS ドキュメントスタンダード](https://make.wordpress.org/core/handbook/best-practices/inline-documentation-standards/javascript/)
