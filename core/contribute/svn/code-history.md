<!--
# Researching Code History
-->

# コードの履歴を調べる

<!--
## Using Subversion Annotate
-->

## Subversion Annotate の使用

<!--
When you need to investigate code, you’ll often have questions about why the code is written the way it is, what it looked like before, who wrote it, and if you can find any more details about it. Subversion annotate (also called **svn blame** or **svn praise**), combined with Core Trac, can help you answer these questions.
-->

コードを調査する必要があるとき、なぜそのコードがそのように書かれているのか、以前はどうだったのか、誰が書いたのか、それについてもっと詳しく知ることができるのか、という疑問を持つことがよくあります。Subversion の annotate (**svn blame** や **svn praise** とも呼ばれます) と Core Trac を組み合わせると、これらの質問に答えることができます。

<!--
To get started, open the [Trac browser](https://core.trac.wordpress.org/browser/trunk), and navigate to the file you want to investigate. Click the Blame link at the top right of the page. You’ll see a new column appear on the left-hand side with the changeset that is associated with each line of the file.
-->

まず [Trac ブラウザ](https://core.trac.wordpress.org/browser/trunk)を開き、調べたいファイルに移動してください。ページの右上にある「Blame」リンクをクリックします。左側に、そのファイルの各行に関連するチェンジセットが書かれた新しい列が表示されるのが分かると思います。

<!--
## Anatomy Of A Changeset
-->

## チェンジセットの構造

<!--
When you click on the changeset, a new dialog appears with the following information:
-->

チェンジセットをクリックすると、新しいダイアログが表示され、以下の情報が表示されます。

<!--
*   Changeset number (also called revision number) – Click the number in the title for a link to the changeset.
*   Timestamp – When the change was committed to WordPress core.
*   Author – Who committed the code.
*   Message – Why the change was made. Often, this includes any associated trac tickets (e.g. [#12345](https://core.trac.wordpress.org/ticket/12345)), associated unit test tickets (e.g. #UT12345), and the user who wrote the accepted patch (e.g. props username).
*   Changed files – A list of added and removed files, and an inline diff of modified files.
-->

*   チェンジセット番号 (リビジョン番号とも呼ばれます) – タイトルの数字をクリックすると、そのチェンジセットへのリンクが表示されます。
*   タイムスタンプ – WordPress コアに、その変更がいつコミットされたか。
*   作成者 – 誰がコードをコミットしたのか。
*   メッセージ – なぜその変更が行われたのか。多くの場合、これには関連する trac チケット (例: [#12345](https://core.trac.wordpress.org/ticket/12345)) や関連するユニットテストチケット (例: #UT12345)、受け入れられたパッチを書いたユーザー (例: props ユーザー名) が含まれます。
*   変更されたファイル – 追加・削除されたファイルのリストと、変更されたファイルのインラインでの差分表示です。

<!--
## Associating Code With A WordPress Release
-->

## WordPress のリリースとコードの関連付け

<!--
To find out when a piece of code was released, look at the associated revision number and find the next highest revision number on the [WordPress tags browser](https://core.trac.wordpress.org/browser?order=name#tags). For example, if you want to know when revision 14377 shipped, you can see that 3.0 was tagged as 15274 and 2.9.2 was tagged as 13165. Revision 14377 was too late to ship with 2.9.2, so it must have shipped with 3.0. You can also verify this by looking at the associated ticket. Revision 14377 is associated with [#12637](https://core.trac.wordpress.org/ticket/12637), which has a milestone of 3.0.
-->

コードの一部がいつリリースされたかを知るためには、関連するリビジョン番号を参照して、[WordPress タグブラウザ](https://core.trac.wordpress.org/browser?order=name#tags)で次に高いリビジョン番号を探します。たとえば、リビジョン14377がいつリリースされたかを知りたい場合、3.0のタグは15274で、2.9.2のタグは13165であることを確認できます。リビジョン14377は2.9.2と一緒にリリースされるには遅すぎたので、3.0でリリースされたのでしょう。このことは、関連するチケットを見ることでも確認できます。リビジョン14377は、マイルストーン3.0の [#12637](https://core.trac.wordpress.org/ticket/12637) と関連しています。

<!--
## Using The Command Line
-->

## コマンドラインの使用

<!--
If you prefer using the command line, you can use the **svn blame** (or **svn annotate**, **svn ann**, or **svn praise**) command. The syntax is: `svn blame [filename]`. Since the output can be verbose, you probably want to pipe it to less. For example: `svn blame wp-includes/formatting.php | less`.
-->

コマンドラインを使いたい場合は、**svn blame** (または **svn annotate**、**svn ann**、**svn praise**) コマンドを使用できます。構文は以下の通りです。`svn blame [filename]`。出力は長くなることがあるので、less にパイプしたいことでしょう。たとえば、`svn blame wp-includes/formatting.php | less` のようになります。

<!--
Once you see a specific revision you want to investigate, use **svn diff** to find exactly what changed. The syntax is `svn diff -r [revision number - 1]:[revision number]`. For example, to view changes made in revision 2000, type `svn diff -r 1999:2000`.
-->

調査したい特定のリビジョンが見つかったら、**svn diff** を使って何が変更されたかを正確に調べます。構文は `svn diff -r [リビジョン番号 - 1]:[リビジョン番号]` です。たとえば、リビジョン2000での変更を見るには、`svn diff -r 1999:2000` と入力してください。

<!--
To view the full commit message, including the committer and timestamp, use **svn log**. The syntax is `svn log -r [revision number]`. For example, to view the commit message for revision 14377, type `svn log -r 14377`.
-->

コミッターとタイムスタンプを含む完全なコミットメッセージを表示するには、**svn log** を使用します。構文は `svn log -r [リビジョン番号]` です。たとえば、リビジョン14377のコミットメッセージを表示するには、`svn log -r 14377` と入力してください。
