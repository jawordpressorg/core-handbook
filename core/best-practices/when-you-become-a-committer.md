<!--
# When you become a committer
-->

# コミッターになったら

<!--
Welcome to being a committer! Here are some things you should know:
-->

コミッターになることを歓迎します ! 知っておくべきことは次のとおりです:

<!--
*   Make sure you have a strong password: it should be long, random, and stored in the password manager of your choice.
    *   Bad: X\*7z7XL{kZvky7E(
    *   Good: aLy%t;67zvy3VdFwVPKA@VGV?i7oq.63Lj.2aKZ@Tw3\].Eu4kVUJJVGyXH7oRL\*a
*   Make sure you have two-factor auth enabled for GitHub, Slack, and the email account associated with your w.org account. It’s also a very good idea to enable it for any service you use, since hackers will often leverage access to a low priority account to gain access to a high priority account.
*   Join the [#core-committers](https://make.wordpress.org/core/tag/core-committers/) channel on Slack.  This channel is for onboarding and questions from committers about the act of committing, tips and tricks for SVN, etc. You’re welcome and encouraged to ask here whenever you have a question about committing (e.g., SVN syntax, backports, etc). Anything that is relevant to non-committers (e.g., whether or not a patch is ready for commit, project philosophy, proposals, etc) should still take place in [#core](https://make.wordpress.org/core/tag/core/) to avoid excluding other contributors.
*   Please add `svnusername@git.wordpress.org` (e.g.`pento@git.wordpress.org`) to your GitHub account: https://github.com/settings/emails . This will allow the new GitHub mirror (https://github.com/WordPress/wordpress-develop) to correctly attribute your commits. GitHub will try to send a verification email, but it won’t be delivered. There’s no need to verify this email address for commit attribution purposes.
*   Read through [this guide on commit messages](https://make.wordpress.org/core/handbook/best-practices/commit-messages/) for a primer on what’s considered best practices.
*   Please ask a relevant committer to peer-review your first few prospective patches and commit messages before you commit them. This serves as a safety check to make sure you know what to look out for before you actually commit. It also gives you a chance to ask any questions you have about process, standards, norms, etc.
*   It can also be a good idea to ask for peer-review from another committer whenever you have any doubts about a patch, especially if you’re committing outside an area that you normally work on.
*   When attending contributor day of WordCamps, you are strongly encouraged to commit someone else’s code, ideally, an attendee that is there working on a patch. It’s also good to encourage innactive committers to dip their toes back in at these events.
-->

*   強力なパスワードを設定すること: パスワードは長く、ランダムで、好みのパスワード・マネージャーに保存すること。
    *   悪い: `X\*7z7XL{kZvky7E(`
    *   良い: `aLy%t;67zvy3VdFwVPKA@VGV?i7oq.63Lj.2aKZ@Tw3\].Eu4kVUJJVGyXH7oRL\*a`
*   GitHub、Slack、そして w.org アカウントに関連するメールアカウントで、二要素認証が有効になっていることを確認してください。また、ハッカーは優先度の低いアカウントへのアクセスを利用して優先度の高いアカウントにアクセスすることが多いため、使用するサービスに対してこれを有効にすることも非常に良い考えです。
*   Slack の [#core-committers](https://make.wordpress.org/core/tag/core-committers/) チャンネルに参加してください。このチャンネルは、コミットのオンボーディングと、コミットすること、SVN のコツやヒントなどに関するコミッターからの質問のためのものです。コミットに関する質問 (例: SVN の構文、バックポートなど) があればいつでも歓迎しますし、ここで質問することを推奨します。非コミッターに関連すること (たとえば、パッチがコミット可能かどうか、プロジェクトの理念、提案など) は、他の貢献者の邪魔をしないように、[#core](https://make.wordpress.org/core/tag/core/) で行われるべきです。
*   あなたの GitHub アカウントに `svnusername@git.wordpress.org` (例: `pento@git.wordpress.org`) を追加してください: https://github.com/settings/emails。こうすることで、新しい GitHub ミラー (https://github.com/WordPress/wordpress-develop)であなたのコミットの属性が正しく表示されます。GitHub は認証メールを送ろうとしますが、届きません。コミット属性のためにこのメールアドレスを確認する必要はありません。
*   ベストプラクティスと考えられるものについての入門として、[コミットメッセージに関するこのガイド](https://ja.wordpress.org/team/handbook/core/best-practices/commit-messages/)を読んでください。
*   最初のいくつかのパッチやコミットメッセージをコミットする前に、関連するコミッターに査読を依頼してください。これは実際にコミットする前に、何に注意すべきかを確認するための安全なチェックとして機能します。また、プロセスや標準、規範などに関して質問があれば質問する機会にもなります。
*   また、パッチについて疑問があるときは、特に普段取り組んでいる分野以外のパッチをコミットする場合は、別のコミッターに査読を依頼することも良いでしょう。
*   WordCamp のコントリビューターデイに参加するときは、他の人のコードをコミットすることを強くおすすめします。またこのようなイベントで、活動休止中のコミッターに再びコミットに参加することをすすめることも良いでしょう。

<!--
## Tasks to add a committer
-->

## コミッターを追加するタスク

<!--
*   Ensure the committer has completed the above steps.
*   On a WordPress.org Sandbox, add them to the following lists:
    *   `/home/svn/etc/develop.svn.wordpress.org` in Deploy SVN
    *   `$committers` in `.config/capes.php`
    *   `wpTracContributorLabels` in the [Trac SVN](https://meta.svn.wordpress.org/sites/trunk/trac.wordpress.org) file `templates/core/site-specific.html`
*   Additionally, add them to the following groups:
    *   The Core Committers user group in WordPress Slack
    *   The [WordPress Core Team](https://github.com/orgs/WordPress/teams/wordpress-core) on GitHub
    *   The Committer group on [Core Trac](https://core.trac.wordpress.org/admin)
*   If the committer will be working on security issues, refer to the Security Team handbook for onboarding tasks.
-->

*   コミッターが上記のステップを完了したことを確認する。
*   WordPress.org サンドボックス上で、以下のリストに追加する:
    *   デプロイ SVN の `/home/svn/etc/develop.svn.wordpress.org`
    *   `.config/capes.php` の `$committers`
    *   [Trac SVN](https://meta.svn.wordpress.org/sites/trunk/trac.wordpress.org) の `templates/core/site-specific.html` ファイルの中の `wpTracContributorLabels`
*   さらに、以下のグループに追加する:
    *   WordPress Slack の コアコミッターのユーザーグループ
    *   GitHub の [WordPress Core Team](https://github.com/orgs/WordPress/teams/wordpress-core)
    *   [Core Trac](https://core.trac.wordpress.org/admin) のコミッターグループ
*   コミッターがセキュリティ問題に取り組む場合は、セキュリティチームのハンドブックを参照して、オンボーディングタスクに取り組んでください。
