<!--
# GitHub Pull Requests for Code Review
-->

# コードレビューのための GitHub プルリクエスト

<!--
WordPress development uses SVN, but many contributors prefer to work in Git though GitHub. Many contributors create pull requests using their own forks of the official [WordPress Develop mirror](https://github.com/wordpress/wordpress-develop) so that they can use features like continuous integration and inline code commenting.
-->

WordPress の開発では SVN を使用していますが、多くの貢献者は GitHub を使用して Git で作業することを好んでいます。多くの貢献者は、継続的インテグレーションやインラインコードコメントなどの機能を使用できるように、公式の [WordPress 開発用ミラー](https://github.com/wordpress/wordpress-develop)をフォークしてプルリクエストを作成しています。

<!--
An experimental feature has been added to Trac that will let you link GitHub pull requests opened against the official [WordPress Develop Git mirror](https://github.com/wordpress/wordpress-develop) to tickets. This makes GitHub contributions more visible directly in their related Trac tickets and makes collaborating across the two repositories easier.
-->

Trac に実験的な機能が追加され、公式の [WordPress 開発用 Git ミラー](https://github.com/wordpress/wordpress-develop)に対して開かれた GitHub のプルリクエストをチケットにリンクできるようになりました。これにより、GitHub での貢献が、関連する Trac チケットにおいてより直接的に表示されるようになり、2つのリポジトリ間でのコラボレーションが容易になります。

<!--
**Note:** Pull requests on GitHub will **not** be merged. Code changes are still required to be made to the SVN repository by trusted long term contributors granted commit access.
-->

**備考**: GitHub 上のプルリクエストはマージ**されません。** コードの変更は、コミット権限が付与された信頼できる長期的な貢献者によって、SVN リポジトリに行われる必要があります。

<!--
## In GitHub
-->

## GitHub

<!--
*   Fork the official [WordPress Develop mirror](https://github.com/wordpress/wordpress-develop) on GitHub.
*   Create a branch on your fork, work on your changes, commit, and push.
*   Open a PR to [wordpress-develop](https://github.com/wordpress/wordpress-develop) with the full URL for the Trac ticket in the PR body. For example:

    > See https://core.trac.wordpress.org/ticket/49295

*   To make collaboration easier, make sure to check the “Allow edits and access to secrets by maintainers”. This will allow WordPress Core committers to push directly to the branch on your fork with larger suggested changes.
-->

*   GitHub で、公式の [WordPress 開発用ミラー](https://github.com/wordpress/wordpress-develop)をフォークします。
*   フォークにブランチを作成し、変更を加え、コミットし、プッシュします。
*   プルリクエストを [wordpress-develop](https://github.com/wordpress/wordpress-develop) に対して作成し、プルリクエスト本文に Trac チケットの完全な URL を記述してください。例: `See https://core.trac.wordpress.org/ticket/49295`

*   コラボレーションを容易にするために、「Allow edits and access to secrets by maintainers」に必ずチェックを入れてください。これにより、WordPress コアのコミッターがあなたのフォーク上のブランチに、より大きな変更案を直接プッシュできます。

![](https://make.wordpress.org/core/files/2020/02/example-github-pr-1024x602.png)

<!--
## In Trac
-->

## Trac

<!--
*   The PR will be displayed below the attachments area on tickets with the following information:
    *   How many lines were modified
    *   Status of the PR checks (Draft/Closed, Travis CI, merge conflicts, etc.)
    *   A button to view the PR
    *   A button to view the raw diff
*   A bot comment will be added to the ticket’s timeline of events indicating when the ticket was mentioned and where.
*   Every time the PR receives a comment, a PR bot will post the comment onto the Trac ticket.
-->

*   プルリクエストは、チケットの添付ファイル欄の下に、以下の内容で表示されます。
    *   変更された行の数
    *   プルリクエストのチェック状況 (Draft/Closed、Travis CI、コンフリクトの発生など)
    *   プルリクエストを見るためのボタン
    *   差分を見るためのボタン
*   チケットのイベントのタイムラインに、そのチケットがいつどこで言及されたかを示すボットコメントが追加されます。
*   プルリクエストがコメントを受け取るたびに、プルリクエストのボットがそのコメントを Trac チケットに投稿します。

<!--
![A screenshot of a WordPress Core Trac ticket with the new linked Pull Requests between the ticket attachments and comments.](https://make.wordpress.org/core/files/2020/02/Screen-Shot-2020-02-20-at-20.42.53.png)
-->

![A screenshot of a WordPress Core Trac ticket with the new linked Pull Requests between the ticket attachments and comments.](https://make.wordpress.org/core/files/2020/02/Screen-Shot-2020-02-20-at-20.42.53.png)

<!--
Pull requests show between Attachments and Change History.
-->

プルリクエストは、添付ファイルと変更履歴の間に表示されます。

<!--
## Important Notes
-->

## 重要事項

<!--
**When the PR bot syncs comments over to Trac, it will not trigger an email notification to the subscribers of the Trac ticket.** For this reason, it is recommended to provide some type of ticket update in Trac itself. Most likely there will be a need to update the keywords anyway (add has-patch or needs-testing, etc.).
-->

**プルリクエストのボットがコメントを Trac に同期するとき、Trac チケットを購読している人にはメールは送信されません。** この理由から、Trac 自身で何らかのチケットの更新することが推奨されます。ほとんどの場合、キーワードを更新する必要があるでしょう (has-patch や needs-testing を追加するなど)。

<!--
**Inline comments made during a code review on the PR will not be posted to the Trac ticket.** These comments are contextual to specific lines at a specific state (commit) of a PR and would seem out of place as the branch’s code is iterated.
-->

**プルリクエストのコードレビュー中に作成されたインラインコメントは、Trac チケットには投稿されません。** これらのコメントは、プルリクエストの特定の状態 (コミット) における特定の行に関連するもので、ブランチのコードが更新されるにつれて不自然な印象を与えるでしょう。

<!--
**Pull requests on GitHub are not monitored.** No one will be checking for new pull requests regularly. Pull requests **must** be attached to a Trac ticket to be considered for inclusion in WordPress Core.
-->

**GitHub 上のプルリクエストは監視されません。** 新しいプルリクエストを定期的にチェックする人はいないでしょう。WordPress コアに含めることを検討するために、プルリクエストは Trac チケットに添付されなければなりません。

<!--
**Clean up after yourself occasionally.** Right now, PRs are not automatically closed when the associated Trac ticket is resolved. If you open a PR, do your best to close PRs that have been merged into Core whenever you are able to.
-->

**時々、自分自身の作業を整理してください。** 今のところ、プルリクエストは関連する Trac チケットが解決されたときに自動的にクローズされるわけではありません。もしあなたがプルリクエストを開いたら、コアにマージされたプルリクエストを可能な限り閉じるようにしましょう。

<!--
And finally, **this is an experiment.** There will likely be some small bugs and things that can be improved since this is the first iteration. Please open up tickets in [Meta Trac](https://meta.trac.wordpress.org/) for any issues that you find. All feedback is welcome!
-->

そして最後に、**これは実験です**。これは最初のバージョンですので、おそらく小さなバグや改善点があるでしょう。何か問題を見つけた場合は、[Meta トラック](https://meta.trac.wordpress.org/)でチケットを作成してください。すべてのフィードバックを歓迎します !
