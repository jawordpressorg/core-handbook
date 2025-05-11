<!--
# Backporting Commits
-->

# コミットのバックポート

<!--
When porting a commit from `trunk` back to versioned branches, it’s best done by different committer than the one who made the `trunk` commit, as an extra layer of review. During the RC phase, at least two committers must sign off on any commit.
-->

`trunk` からバージョンブランチにコミットを戻す場合、追加のレビューとして `trunk` にコミットを行ったコミッターとは別のコミッターが行うことがベストです。RC フェーズでは、どのようなコミットに対しても少なくとも2人のコミッターが承認しなければなりません。

<!--
Do not commit to multiple branches in the same commit. This will, at a minimum, break the Git mirrors.
-->

同じコミットで複数のブランチにコミットしないでください。少なくとも Git ミラーが壊れてしまうでしょう。

<!--
A basic SVN flow to backport a commit could look like this:
-->

コミットをバックポートする基本的な SVN のフローは次のようになります:

1.  `$ svn switch '^/branches/5.9'`
2.  `$ svn merge -c 12345 '^/trunk'` where `12345` is the changeset ID.
3.  `$ svn ci`

<!--
If the fix in `trunk` required multiple separate commits, you can backport them all in a single command like this:
-->

`trunk` での修正が複数の別々のコミットを必要とする場合、以下のように1つのコマンドですべてをバックポートできます:

`svn merge -c 10001,10002 '^/trunk'`

<!--
For merges you should generally use a pristine `branches/5.9` checkout that has no code changes other than what’s being merged and a test site for testing the merged commit on (which you should always do).
-->

マージの際には、一般的に、マージ対象以外のコード変更がない元の `branches/5.9` チェックアウトと、マージされたコミットをテストするためのテストサイトを使うべきです (これは常に行うべきです)。

<!--
Also, although you’ll probably never need it, if you’re merging multiple commits one after each other, don’t forget to run `svn up` between them. If what you need to merge has multiple commits, also feel free to squash them down for the branch commit to make it easier for everyone reading.
-->

また、おそらく必要になることはないと思いますが、複数のコミットを次々とマージする場合は、その間に `svn up` を実行することを忘れないでください。マージするコミットが複数ある場合は、ブランチのコミットでそれらをまとめておくと、誰でも読みやすくなります。

<!--
Sometimes multiple changes to the same code are made in `trunk` before they are ported to a branch.  In this case, you will get conflicts, so be sure to port the older changesets as well.  Committers asking for a backport should indicate this situation on the ticket.
-->

ブランチにバックポートする前に `trunk` で同じコードに対して複数の変更が行われることがあります。この場合コンフリクトが発生するため、古いチェンジセットもバックポートするようにしてください。バックポートを依頼するコミッターは、チケットにこの状況を書いてください。

<!--
To add the merge info afterwards you can run `svn merge --record-only -c 12345 '^/trunk'`.
-->

The branch commit message will largely be copied from the `trunk` commit(s) with a few updates. Please see the commit message documentation, especially the sections on [Merges and Reviewed By.](https://make.wordpress.org/core/handbook/best-practices/commit-messages/#reviewed-by-and-merges)

<!--
The branch commit message will largely be copied from the `trunk` commit(s) with a few updates. Please see the commit message documentation, especially the sections on [Merges and Reviewed By.](https://make.wordpress.org/core/handbook/best-practices/commit-messages/#reviewed-by-and-merges)
-->

ブランチコミットメッセージの大部分は `trunk` コミットからコピーされ、いくつかの更新が加えられます。コミットメッセージのドキュメント、特に[マージとレビューする人](https://ja.wordpress.org/team/handbook/core/best-practices/commit-messages/#reviewed-by-and-merges)のセクションを参照してください。

<!--
Make sure to run the above commands from the branch root, and not from a sub directory. The reason for this is that the `svn:mergeinfo` is a SVN property on `/branches/5.9` which the SVN client sets, it’s not a server side thing.

At the bottom of https://core.trac.wordpress.org/browser/branches/5.9 you see two links, ‘merged’ and ‘eligible’. The second one shouldn’t list commits which are already merged.
-->

\[info\]上記のコマンドは、サブディレクトリからではなく、必ずブランチのルートから実行してください。なぜなら、`svn:mergeinfo` は `/branches/5.9` の SVN プロパティで、SVN クライアントが設定するものであり、サーバーサイドのものではないからです。

https://core.trac.wordpress.org/browser/branches/5.9 の一番下に、「'merged」と「eligible」という2つのリンクがあります。2番目のリンクは、すでにマージされたコミットでは表示されないはずです。\[/info\]

<!--
## Backport Process
-->

## バックポートプロセス

<!--
The standard process for any commit not to trunk is “double signoff”. Essentially, another committer must review and comment with their agreement before the code is backported. In practice, this process looks as follows:
-->

trunk にコミットしない場合の標準的なプロセスは「ダブルサインオフ」です。基本的に、コードをバックポートする前に、別のコミッターがレビューし、同意を示すコメントを付ける必要があります。実際には、このプロセスは以下のようになります。

<!--
1.  Make a commit to trunk.
2.  Reopen the ticket and add the `dev-feedback` keyword. You should also remove the `commit` keyword if that had previously been applied. A comment along the lines of “Reopening [#15705](https://core.trac.wordpress.org/ticket/15705) to request backporting [\[27195\]](https://core.trac.wordpress.org/changeset/27195) to 2.4 branch”.
3.  A second committer should add a comment approving the backport and add the `dev-reviewed` keyword.
4.  Follow the technical steps above.
-->

1. trunk にコミットします。
2. チケットを再オープンし、`dev-feedback` キーワードを追加します。以前に `commit` キーワードが適用されていた場合は、削除する必要があります。「[#15705](https://core.trac.wordpress.org/ticket/15705) を再オープンし、[\[27195\]](https://core.trac.wordpress.org/changeset/27195) を2.4ブランチにバックポートすることをリクエストします」といった内容のコメントを追加します。
3. 2人目のコミッターが、バックポートを承認するコメントと `dev-reviewed` キーワードを追加します。
4. 上記の技術的な手順に従います。

<!--
### Security Backports
-->

### セキュリティバックポート

<!--
Security fixes are backported to many versions, and are not committed until the day of a release. Because of this, the process can be streamlined a bit.
-->

セキュリティの修正は多くのバージョンにバックポートされ、リリース当日までコミットされません。このため、プロセスを少し合理化できます。

<!--
You should still make individual commits to `trunk` and the current branch, but on the older branches you can make a single commit with all of the fixes for that branch. Do not commit to multiple branches at once, though.
-->

`trunk` と現在のブランチには個別にコミットすべきですが、古いブランチではそのブランチのすべての修正を1つのコミットにまとめることができます。しかし、一度に複数のブランチにコミットしてはいけません。

<!--
When committing the bulk patch to each branch, you still need to record the merge metadata with:
-->

一括パッチを各ブランチにコミットする際には、マージメタデータを記録する必要があります:

```
svn merge --record-only -c 12345,12347,12349 '^/trunk'
```
