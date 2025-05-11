<!--
# Contributor Attribution (&#8220;Props&#8221;)
-->

# 貢献者の帰属 (&#8220;Props&#8221;)

<!--
One of the greatest things about open source is that contributions come in many shapes and sizes. Anyone can contribute regardless of skill set, experience, time zone, or background. There are countless ways for someone to get involved with open source projects.
-->

オープンソースの最大の利点の一つは、貢献の形態や規模が多様であることです。スキルセット、経験、タイムゾーン、バックグラウンドを問わず、誰でも貢献できます。オープンソースプロジェクトに参加する方法は無数にあります。

<!--
WordPress is no different. Contributors submitting code modifications are only a small subset of the larger community. Recognizing all types of contributions in all locations is essential to establishing a healthy contributor base. Contributors who feel recognized and valued are more likely to continue contributing.
-->

WordPress も例外ではありません。コード変更を提出する貢献者は、コミュニティ全体から見ればごく一部に過ぎません。あらゆる場所でのあらゆる種類の貢献を認めることは、健全な貢献者基盤を確立するために不可欠です。認められ、評価されていると感じている貢献者は、貢献を継続する可能性が高くなります。

<!--
**The responsibility for this falls on the shoulders of the project’s maintainers.** When work is done, and changes are made, the project tracks them by giving “props” to all contributors involved.
-->

**この責任はプロジェクトのメンテナーにかかっています。** 作業が完了し、変更が加えられると、プロジェクトは関与したすべての貢献者に「props」を与えることで、その進捗状況を追跡します。

<!--
## What are “props”?
-->

## “props” とは何ですか ?

<!--
“Props” is short for “proper respect” and is used in WordPress to signify thanks for a contribution. This practice began in [\[1102\]](https://core.trac.wordpress.org/changeset/1102) when the first contributor was given props for a contribution to WordPress. Since then, props have been used as a way to recognize and track contributions throughout the project’s history. Contributions to Core take on many forms, from things that directly impact the code (such as writing and reviewing patches) to things like design, testing, and well-written bug reports.
-->

「Props」は「proper respect (適切な敬意)」の略で、WordPress では貢献への感謝を表すために使用されます。この慣習は [\[1102\]](https://core.trac.wordpress.org/changeset/1102) において、WordPress への最初の貢献者に Props が贈られたことに始まります。それ以来、props はプロジェクトの歴史を通して貢献を認識し、追跡する方法として使用されてきました。コアへの貢献は、コードに直接影響を与えるもの (パッチの作成とレビューなど) から、設計、テスト、よく書かれたバグレポートなど、さまざまな形をとります。

<!--
## Who gives props?
-->

## 誰が props をくれますか ?

<!--
The props (or credits) within a release are collected using a script on WordPress.org that parses commit logs to extract all props given to contributors by committers and maintainers using the specific formats detailed below. The commit log files are carefully scoped to represent all activity for the specific date or commit ranges representing the current release cycle. The results are embedded in the About Page, Release Announcement Post, and committed to the [w.org Credits API](https://api.wordpress.org/core/credits/1.1/), which is used to list contributors on the Credits page in the WordPress admin area.
-->

リリース内の props (またはクレジット) は、WordPress.org 上のスクリプトを使用して収集されます。このスクリプトはコミットログを解析し、コミッターとメンテナーが貢献者に付与したすべての props を、以下に詳述する特定の形式で抽出します。コミットログファイルは、現在のリリースサイクルを表す特定の日付またはコミット範囲のすべてのアクティビティを表すように、慎重にスコープ設定されています。結果はアバウトページとリリースアナウンス投稿に埋め込まれ、WordPress ダッシュボードのクレジットページに貢献者リストを表示するために使用される [w.org クレジット API](https://api.wordpress.org/core/credits/1.1/) にコミットされます。

<!--
Additional non-code contributions are gathered by the Release Squad, and focus leads to be added to the Credits API as necessary. For example, any props given in Slack for helping to test release packages, facilitating meetings, writing developer notes, etc., are currently *not* automatically compiled.
-->

コード以外の貢献はリリースチームによって収集され、必要に応じてフォーカスリードがクレジット API に追加します。たとえば、リリースパッケージのテスト、ミーティングの進行、開発者メモの作成などに対する Slack での貢献は、現在自動的にコンパイル **されません**。

<!--
The Credits API currently only contains contributor lists for WordPress >= 3.2.
-->

クレジット API には現在、WordPress 3.2以上の貢献者リストのみが含まれています。

<!--
## When should props be given?
-->

## Props はいつ与えるべきですか ?

<!--
Err on the side of giving props liberally. Props can provide major encouragement for contributors and ensure people receive recognition for their contributions.
-->

惜しみなく与えましょう。Props は貢献者にとって大きな励みとなり、貢献が認められることにつながります。

<!--
Props should be given to all those who contributed to the final commit, whether through patches, refreshed patches, code suggested otherwise, design, writing, user testing, or other significant investments of time and effort.
-->

パッチ、更新されたパッチ、別の提案のコード、デザイン、執筆、ユーザーテスト、その他の多大な時間と労力の投資など、最終コミットに貢献したすべての人に props が与えられるべきです。

<!--
In the case of bug reports, props should also be given to the reporter of the bug. Check any tickets that were closed as duplicates in case they contain contributions that warrant props, too.
-->

バグレポートの場合は、バグレポートの報告者にも props を付与する必要があります。重複としてクローズされたチケットにも props に値する貢献が含まれているかどうかを確認してください。

<!--
## How are props given?
-->

## Props はどのように与えられますか ?

<!--
Because contributions happen in multiple locations using many different tools, there are some nuances to how props should be formatted. Below is how props are given in SVN and Git repositories.
-->

貢献は複数の場所でさまざまなツールを用いて行われるため、props のフォーマットには微妙な違いがあります。以下は、SVN リポジトリと Git リポジトリにおける props の記述方法です。

<!--
### wordpress-develop commits in SVN
-->

### SVN における wordpress-develop のコミット

<!--
When Core Committers deem a change ready and record a transaction in the canonical subversion repository, aka committing code. 
-->

コアコミッターが変更の準備が整ったと判断し、正規の Subversion リポジトリにトランザクションを記録する (つまり、コードをコミットする) とき。

`Props desrosj, jorbin, jeffpaul.`

<!--
The full [commit message guide covers this](https://make.wordpress.org/core/handbook/best-practices/commit-messages/) in-depth, but the standard rules are:
-->

完全な[コミットメッセージガイド](https://ja.wordpress.org/team/handbook/core/best-practices/commit-messages/)ではこの点について詳細に説明していますが、標準的なルールは次のとおりです:

<!--
*   Props must be preceded by a blank line.
*   Usernames must not start with an @ (at) sign.
*   Separate usernames by comma + space. Think: /^props (\\s\*(\[^,\]+),?)+$/
*   Copy/paste usernames to avoid typos. (Sorry, rmccue; or is that rmmcue?)
*   If the user has a space in their displayed name, use the slug from their w.org profile URL. For example, Frank Klein on Trac should get props as frank-klein.
*   The props line should only include the word props, wordpress.org usernames, spaces, and punctuation.
*   The `props` line must end with a period.
-->

*   先頭には空白行が必要です。
*   ユーザー名は `@` (アット) 記号で始めることはできません。
*   ユーザー名はカンマとスペースで区切ってください。正規表現: `/^props (\s*([^,]+),?)+$/`
*   タイプミスを避けるため、ユーザー名はコピー & ペーストしてください。
*   ユーザーの表示名にスペースがある場合は、w.org プロフィールの URL のスラッグを使用してください。たとえば、Trac の Frank Klein は frank-klein として props を取得する必要があります。
*   props 行には、props、wordpress.org ユーザー名、スペース、句読点のみを含めてください。
*   `props` 行はピリオドで終わらせます。

<!--
### GitHub repositories/merge commits
-->

### GitHub リポジトリ/マージコミット

<!--
When merging code through a pull request on GitHub, maintainers are required to copy and paste the list of contributors provided by the Props Bot GitHub Action into the bottom of the merge commit message.
-->

GitHub のプルリクエストを通じてコードをマージする場合、メンテナーは Props Bot GitHub Action によって提供された貢献者のリストをコピーして、マージ コミットメッセージの下部に貼り付ける必要があります。

<!--
Always review the list of GitHub accounts included to ensure all who have contributed meaningfully to the PR or any linked issues are credited.
-->

含まれる GitHub アカウントのリストを常に確認し、PR またはリンクされた問題に有意義な貢献をしたすべての人がクレジットされていることを確認してください。

<!--
Some technical notes:
-->

いくつかの技術的な注意事項:

<!--
*   The list of `Co-authored-by` trailers must be preceded by a blank line.
*   `Co-authored-by` trailers should be the last thing in a commit message.
*   The unlinked contributors must come before the `Co-authored-by` trailers.
*   Unlinked contributors should be entered in one line preceded by `Unlinked contributors:`, each one separated by a comma and a space (`,` ), and a period after the last one. Example: `Unlinked contributors: nacin, wapuu.`
*   Usernames must not start with an `@` (at) sign.
*   When manually adding someone, please only use their WordPress.org username in the following format: `Co-authored-by: dotorgusername <[dotorgusername@git.wordpress.org](mailto:dotorgusername@git.wordpress.org)>`. The only exception to this rule is for bot accounts, such as `dependabot` or `github-actions`. It’s important to include them so future contributors know they were involved in the changes.
*   If there are contributors already noted with `Co-authored-by` in the suggested commit message, verify they are also included in the list provided by Props Bot before removing. These will be in **GitHub format and should be converted to the above w.org format**. Deleting the GitHub formatted ones will ensure an accurate contributor count for each commit, but it’s not required. Non w.org emails will be ignored by the props parsing scripts.
*   If a contributor’s w.org username is unknown, add their GitHub username to the “Unlinked contributors” list.
*   If there are `Signed-off-by` trailers in the suggested commit message, leave them in place above `Co-authored-by` trailers. These serve a different purpose and are ignored in the context of collecting props.
-->

*   `Co-authored-by` のリストの前には空白行が必要です。
*   `Co-authored-by` はコミット メッセージの最後に置く必要があります。
*   リンクされていない貢献者は、`Co-authored-by` の前に来なければなりません。
リンクされていない貢献者は、`Unlinked contributors:` を先頭に付けて1行に入力し、各貢献者をカンマとスペース (`,`) で区切り、最後の貢献者の後にピリオドを付けます。例: `Unlinked contributors: nacin, wapuu.`
*   ユーザー名は `@` (アット) 記号で始まってはいけません。
*   手動で追加する場合は、次の形式で WordPress.org のユーザー名のみを使用してください: `Co-authored-by: dotorgusername <[dotorgusername@git.wordpress.org](mailto:dotorgusername@git.wordpress.org)>`。このルールの唯一の例外は、`dependabot` や `github-actions` などのボットアカウントです。将来の貢献者が変更に関与したことがわかるように、これらのアカウントも含めることが重要です。
*   提案されたコミットメッセージにすでに `Co-authored-by` で貢献者が記載されている場合は、削除する前に、Props Bot が提供するリストにも含まれていることを確認してください。これらの貢献者は**GitHub 形式であるため、上記の w.org 形式に変換する必要があります**。GitHub 形式の貢献者を削除すると、各コミットの貢献者数が正確に把握できますが、必須ではありません。w.org 以外のメールアドレスは、props 解析スクリプトによって無視されます。
*   貢献者の w.org ユーザー名が不明な場合は、GitHub ユーザー名を「Unlinked contributors」リストに追加してください。
*   提案されたコミットメッセージに `Signed-off-by` が含まれている場合は、`Co-authored-by` の上に残してください。これらは別の目的で使用され、props 収集のコンテキストでは無視されます。

#### Props Bot

<!--
A GitHub Action, [WordPress Props](https://github.com/WordPress/props-bot-action), has been created and should be utilized in GitHub repos across the WordPress project to help identify, capture, and include contributors within the props in merge commits. If you need help setting up that as an action within your repo, please [open a ticket with the Meta team](https://meta.trac.wordpress.org/newticket).
-->

WordPress プロジェクト全体の GitHub リポジトリで活用することで、マージコミットに props 内の貢献者を特定、取得、追加できる GitHub Actions である [WordPress Props](https://github.com/WordPress/props-bot-action) が作成されました。リポジトリ内でのアクションとしての設定についてサポートが必要な場合は、[Meta チームにチケットを作成](https://meta.trac.wordpress.org/newticket)してください。

<!--
## General Rules and best practices
-->

## 一般的なルールとベストプラクティス

<!--
*   Always manually review any generated list to ensure that no contributions go unrecognized.
*   When someone does not contribute in a meaningful way, it’s sometimes appropriate to remove them from a props list. Use your best judgment to decide whether someone was trying to be helpful. If they only commented, “Why is this still broken?” or “When will this be fixed?” they have not really positively impacted the eventual solution. On the other hand, while a comment like “I’m seeing this on my site using updating to x.y” may seem unhelpful at first, it’s providing important detailed information that could be used to substantiate a report and under which conditions.
*   If you’re ever unsure, please ask in the \[#core-committers channel in Slack\](https://wordpress.slack.com/archives/C18723MQ8).
-->

*   生成されたリストは常に手動で確認し、貢献が認識されないことがないようにします。
*   誰かが有意義な貢献をしていない場合、そのユーザーを props リストから削除することが適切な場合もあります。そのユーザーが本当に助けようとしていたのかどうかは、ご自身の判断で判断してください。「なぜまだ壊れているのですか ?」や「いつ修正されるのですか ?」といったコメントだけでは、最終的な解決にはあまり良い影響を与えていません。一方、「xy にアップデートしたら、自分のサイトでこの問題が発生しました」といったコメントは、一見役に立たないように思えるかもしれませんが、報告の裏付けとなる重要な詳細情報や、どのような状況で発生したかを示す情報を提供してくれます。
*   不明な点がある場合は、[Slack の #core-committers チャンネル](https://wordpress.slack.com/archives/C18723MQ8)で質問してください。

<!--
### `wordpress-develop` specific notes
-->

### `wordpress-develop` 特有のメモ

<!--
*   Prop yourself when the commit is the product of huge efforts involving multiple people, such as a major feature, API, or particularly nasty bug.
*   If committing your own code, props are assumed, so omit yourself here as well.
*   If you forget to prop someone, check to see if they already have props in the current release. It will not matter in the long run, as they will be included in the release credits anyway. If they are not already propped, then you can flag it to the [Release Coordinator](https://make.wordpress.org/core/handbook/about/release-cycle/wordpress-release-team-and-focus-leads/#release-co-ordinator) so they can ensure that person is added on release day. It is also recommended to reach out to the contributor in Slack or in a comment on the ticket as a courtesy, apologize for missing their name in the commit message, and let them know their contribution will be recognized. Note how. Also, use the [core props tool](https://make.wordpress.org/core/wp-admin/admin.php?page=props-edit-core) to ensure people are properly credited on their profiles.
*   When listing props while committing, avoid including anything that is not part of a w.org username. There’s no need to say `Props jorbin for testing.` or `Props nacin for the initial implementation.`. This can create false positives when using a script to extract contributor usernames ([implementation is not a w.org contributor](https://profiles.wordpress.org/implementation/)). 
*   It is normal for committers to adjust style or rearrange logic before a commit or to account for a simple edge case. In these instances, omit yourself. Your name on the commit implies that you have reviewed and tested it, which is just as important as the contents of the commit.
-->

*   コミットが複数の人が関わる多大な努力の成果である場合 (主要な機能、API、特にやっかいなバグなど) は、自分自身に props を付与しましょう。
*   自分のコードをコミットする場合は、props が付与されているものとみなされるため、ここでも自分自身に props を付与する必要はありません。
*   誰かに props を付与することを忘れた場合は、現在のリリースですでにその人に props が付与されているかどうかを確認してください。いずれにせよリリースのクレジットには含まれるため、長期的には問題ありません。まだ props が付与されていない場合は、[リリースコーディネーター](https://ja.wordpress.org/team/handbook/core/about/release-cycle/wordpress-release-team-and-focus-leads/#release-co-ordinator)に報告して、リリース日にその人が追加されるようにしてもらうことができます。また、Slack やチケットへのコメントで貢献者に連絡を取り、コミットメッセージに名前が記載されていないことをお詫びし、貢献が認められていることを伝えることもおすすめします。その方法に注意してください。また、[コア props ツール](https://make.wordpress.org/core/wp-admin/admin.php?page=props-edit-core)を使用して、各自のプロフィールに適切にクレジットが付与されていることを確認してください。
*   コミット時に props をリストする際は、w.org ユーザー名に含まれないものは含めないようにしてください。`Props jorbin for testing.` や `Props nacin for the initial implementation.` などと書く必要はありません。スクリプトを使用して貢献者のユーザー名を抽出する際に、誤検知が発生する可能性があります ([implementation 実装は w.org 貢献者ではありません](https://profiles.wordpress.org/implementation/))。
*   コミッターがコミット前にスタイルを調整したり、ロジックを変更したり、単純なエッジケースに対応したりすることはよくあります。このような場合は、自分自身を省略してください。コミットにあなたの名前が記載されているということは、あなたがコミットをレビューし、テストしたことを意味します。これはコミットの内容と同じくらい重要です。

<!--
### GitHub specific notes
-->

### GitHub 特有のメモ

<!--
*   Always include yourself in the props list, even if it’s noted that you will be the author of the merge commit. The w.org style credit is required attribute your contribution to your w.org profile.
*   **Do not use personal emails or GitHub-specific emails** ([`ID+USERNAME@users.noreply.github.com`](mailto:ID+USERNAME@users.noreply.github.com) or `USERNAME@users.noreply.github.com`).
*   There’s currently no automated way to add a contributor who is not included in the list prepared by Props Bot. To find someone’s w.org profile, visit `[https://profiles.wordpress.org/github:GHUSERNAME](https://profiles.wordpress.org/github:GHUSERNAME)`, replacing `GHUSERNAME` with the contributor’s GitHub username. This will redirect you to the person’s w.org profile if they have connected their account. Add their GitHub username (without an `@`) to the `Unlinked contributors:` list when there’s no connection.
-->

*   マージコミットの作成者であることが明記されている場合でも、必ず props リストに自分自身を含めてください。w.org スタイルのクレジット表記で、貢献を w.org プロフィールに明記してください。
*   **個人用メールアドレスや GitHub 固有のメールアドレスは使用しないでください** ([`ID+USERNAME@users.noreply.github.com`](mailto:ID+USERNAME@users.noreply.github.com) または `USERNAME@users.noreply.github.com`)。
*   現在、Props Bot によって作成されたリストに含まれていない貢献者を自動的に追加する方法はありません。誰かの w.org プロフィールを見つけるには、`[https://profiles.wordpress.org/github:GHUSERNAME](https://profiles.wordpress.org/github:GHUSERNAME)` にアクセスし、`GHUSERNAME` を貢献者の GitHub ユーザー名に置き換えてください。相手がアカウントを接続している場合は、w.org プロフィールにリダイレクトされます。接続されていない場合は、(`@` なしの) GitHub ユーザー名を `Unlinked contributors:` リストに追加してください。

<!--
### Major Release Credits
-->

### メジャーリリースのクレジット

<!--
The .org props script will attempt to detect spelling mistakes and match unlinked GitHub accounts as best as possible. But there will always be some manual review that needs to take place. The contributor running the props script can easily perform most of this. Here are some tips for reviewing and improving the accuracy of the contributor list for a release.
-->

.org props スクリプトは、スペルミスを検出し、リンクされていない GitHub アカウントを可能な限り一致させようとします。ただし、必ず何らかの手動レビューが必要になります。props スクリプトを実行する貢献者は、そのほとんどを簡単に実行できます。リリースの貢献者リストを確認し、正確性を向上させるためのヒントをいくつか紹介します。

<!--
*   [https://profiles.wordpress.org/github:username](https://profiles.wordpress.org/github:noisysocks) will redirect to a contributor’s w.org profile when a valid connection exists.
*   [https://profiles.wordpress.org/$slack\_user\_id](https://profiles.wordpress.org/%24slack_id) will redirect to a contributor’s w.org profile. The Slack ID comes from the details view for a user in Slack (Click on avatar > View full profile > More \[…\] > Copy ID).
*   For unlinked GitHub accounts, perform a reasonable amount of detective work trying to confirm a contributor’s identity.
    *   Use any details listed on the user’s GitHub profile page (listed name, email, etc.) or website/social profile.
    *   Look for review commits and append `.patch` to the commit URL. Sometimes, there are different names and emails listed there.
*   That information can then be used to search profiles on WordPress.org to find a potential match. An example search query for search engines is `site:profiles.wordpress.org desrosj.`
-->

*   [https://profiles.wordpress.org/github:username](https://profiles.wordpress.org/github:noisysocks) は、有効な接続が存在する場合、貢献者の w.org プロフィールにリダイレクトします。
*   [https://profiles.wordpress.org/$slack_user_id](https://profiles.wordpress.org/%24slack_id) は、貢献者の w.org プロフィールにリダイレクトします。Slack ID は、Slack のユーザー詳細ビューから取得されます (アバターをクリック > プロフィールを表示 > その他 \[…\] > ID をコピー)。
*   リンクされていない GitHub アカウントの場合は、貢献者の情報を確認するために、ある程度の調査作業を実行してください。
    * ユーザーの GitHub プロフィールページ (名前、メールアドレスなど) または Web サイト/ソーシャル プロフィールに記載されている詳細情報を使用します。
    * レビューコミットを探し、コミット URL に `.patch` を追加します。場合によっては、異なる名前とメールアドレスがリストされていることがあります。
*   この情報は、WordPress.org のプロフィールを検索する際に使用され、一致する可能性のあるユーザーを見つけることができます。検索エンジンでの検索クエリーの例は、`site:profiles.wordpress.org desrosj.` です。

<!--
Once a match has been identified, refer the GitHub account owner through Slack or a PR they participated in to the [handbook page about linking GitHub and WordPress.org accounts](https://make.wordpress.org/core/handbook/tutorials/linking-your-github-and-w-org-profiles/). This will be helpful in the future to avoid the same research effort in future releases.
-->

一致が見つかったら、Slack または参加した PR を通じて、GitHub アカウントの所有者に [GitHub アカウントと WordPress.org アカウントのリンクに関するハンドブックのページ](https://ja.wordpress.org/team/handbook/core/tutorials/linking-your-github-and-w-org-profiles/)を参照するよう伝えてください。これは、将来のリリースで同じ調査作業を繰り返さなくて済むため、非常に役立ちます。

<!--
## Props and About Pages
-->

## Props とアバウトページ

<!--
## Props and Release Announcements
-->

## Props とリリースアナウンス

<!--
All associated props for each release should always be listed towards the bottom of the matching announcement post. There are two ways to do this.
-->

各リリースに関連するすべての props は、対応するアナウンス投稿の下部に必ず記載してください。これには2つの方法があります。

<!--
In major release posts, props should be listed using the `[wpcredits x.y]` shortcode. For example, the following is how the shortcode would be used for WordPress 6.5: `[wpcredits 6.5]`. 
-->

メジャーリリースの投稿では、props は `[wpcredits x.y]` ショートコードを使用して記載する必要があります。たとえば、WordPress 6.5の場合は `[wpcredits 6.5]` というショートコードを使用します。

<!--
The Credits API does support listing credits for each minor version. Instead, contributors for minor versions that did not also contribute to the corresponding major version are just added to the API under the major version. Because of this, an HTML list should be used instead of the shortcode. Someone with access to a wordpress.org sandbox will be able to generate this list using a script. Each contributor’s name as configured on their w.org profile, should be used and linked to their profile page.
-->

クレジット API は、マイナーバージョンごとにクレジットの一覧表示をサポートしています。ただし、対応するメジャーバージョンには貢献していないマイナーバージョンの貢献者は、メジャーバージョンの下の API に追加されます。そのため、ショートコードではなく HTML リストを使用する必要があります。wordpress.org のサンドボックスにアクセスできるユーザーは、スクリプトを使用してこのリストを生成できます。各貢献者の名前は、w.org のプロフィールで設定されているものを使用し、プロフィールページにリンクする必要があります。

* * *

<!--
Additional resources:
-->

追加リソース:

*   [https://make.wordpress.org/core/handbook/best-practices/commit-messages/#props](https://make.wordpress.org/core/handbook/best-practices/commit-messages/#props)
*   [https://make.wordpress.org/core/handbook/about/release-cycle/preparing-the-about-page/#props](https://make.wordpress.org/core/handbook/about/release-cycle/preparing-the-about-page/#props)
*   [https://helen.wordpress.com/2019/01/22/what-are-commit-props/](https://helen.wordpress.com/2019/01/22/what-are-commit-props/)
