<!--
# Commit Messages
-->

# コミットメッセージ

<!--
Commit messages are a critical aspect of how WordPress is developed. They are an integral part of the project’s history, along with the changesets themselves. We write commit messages for multiple audiences: contemporaries (fellow core developers, plugin developers, anybody following along with core development), future contributors, and computers. Good commit messages serve each of these audiences well. They describe the *what* and the *why* of the changeset; the *how* is described by the diff itself.
-->

コミットメッセージは、WordPress がどのように開発されてきたかを示す重要な要素です。チェンジセットそのものとともに、プロジェクトの歴史の重要な一部です。私たちは、同世代の人々 (コア開発者達、プラグイン開発者、コア開発に関わる人々)、将来の貢献者、そしてコンピューターという対象者の読者に向けてコミットメッセージを書きます。優れたコミットメッセージは、これらの対象者のそれぞれに有益です。コミットメッセージは、チェンジセットの「内容」と「理由」を記述します。「どのように」は diff 自体によって記述されます。

<!--
Even if you are not a committer, you can make use of these guidelines while contributing to WordPress, as well as in your own projects. By describing your patch in a way that is sensitive to the concerns outlined here – or even drafting a commit message yourself – you make it easier for the committer process your contribution quickly.
-->

たとえあなたがコミッターでなくても、WordPress への貢献や自分のプロジェクトでこれらのガイドラインを活用できます。ここで概説されている懸念事項に配慮した方法でパッチを記述することで、あるいは自分自身でコミットメッセージを作成することで、コミッターがあなたの貢献を迅速に処理しやすくなります。

<!--
Remember: Do not commit to multiple branches in the same commit. This will, at a minimum, break the Git mirrors.
-->

注意: 同じコミットで複数のブランチにコミットしないでください。これは、少なくとも Git ミラーを壊すことになります。

<!--
## Format
-->

## フォーマット

<!--
The full format for a commit message is as follows:
-->

コミットメッセージの完全な形式は次のとおりです:

> Component: Brief summary.
>
> Longer description with more details, such as a \`new\_hook\` being introduced with the context of a \`$post\` and a \`$screen\`.
>
> More paragraphs can be added as needed.
> 
> Follow-up to [\[27195\]](https://core.trac.wordpress.org/changeset/27195), [\[41062\]](https://core.trac.wordpress.org/changeset/41062).
> 
> Reviewed by a-fellow-committer, maybe-multiple.  
> Merges [\[26851\]](https://core.trac.wordpress.org/changeset/26851) to the to the x.x branch.
> 
> Props person, another.  
> Fixes [#30000](https://core.trac.wordpress.org/ticket/30000). See [#20202](https://core.trac.wordpress.org/ticket/20202), #105.

<!--
### Global Guidelines
-->

### グローバルガイドライン

<!--
*   Each line should begin with a capital letter and end with a full stop/period.
*   Code, such as the name of a function or a hook, should appear inside backticks, to ensure proper formatting in Trac and Slack.
*   Outside of the brief summary, there are no character limits. Don’t manually wrap lines.
*   Pay attention to places that should have a blank line before them and areas that should not.
*   Ticket numbers preceded by a number sign [#20202](https://core.trac.wordpress.org/ticket/20202) and revision numbers inside square brackets [\[30000\]](https://core.trac.wordpress.org/changeset/30000) will auto-link in Trac, Slack, and here on make/core.
*   Outside of the `props` section, avoid using the word `props` in order to not confuse the tools that generate contributor statistics. If talking about properties, use the full word. Otherwise, consult a [thesaurus](https://www.thesaurus.com/browse/prop).
-->

*   各行は大文字で始まり、ピリオドで終わらせます。
*   Trac と Slack で適切な書式設定が適用されるようにするために、関数名やフック名などのコードはバッククオートの内側に表示します。
*   概要以外は文字数制限はありません。手動で行を折り返さないでください。
*   空白行を入れるべき箇所と入れるべきではない箇所に注意してください。
*   チケット番号の前には番号記号 [#20202](https://core.trac.wordpress.org/ticket/20202) が付き、角括弧内のリビジョン番号 [\[30000\]](https://core.trac.wordpress.org/changeset/30000) は、Trac、Slack、そして make/core で自動リンクされます。
*   貢献者の統計を生成するツールが混同しないように、`props` セクションの外では `props` という単語の使用を避けてください。プロパティについて話す場合は、完全な単語を使用してください。それ以外の場合は、[類義語辞典](https://www.thesaurus.com/browse/prop) を参照してください。

<!--
### Brief summary
-->

### 簡単な要約

<!--
The first line of a commit message is a brief summary of the changeset. The brief summary is used for email subject lines, Trac changelogs, and features prominently in most VCS log formats, such as `git log --format=oneline`. The high visibility of the summary makes it critical to craft something that is as descriptive as possible within space limits.
-->

コミットメッセージの最初の行は、チェンジセットの簡単な要約です。これはメールの件名や Trac の変更履歴、および `git log --format=oneline` などのほとんどの VCS のログ形式で目立つ機能で使用されます。要約は目につきやすいため、スペースの制限内でできるだけ説明的な内容を作成することが重要です。

<!--
#### Guidelines
-->

#### ガイドライン

<!--
*   Must be one line; no line breaks.
*   Aim for around 50 characters or less, stopping at 70. This is important because log-viewing tools nearly all expect the first line of commit messages to fit within these limits. This difficult restriction may force you to think critically about the essence of your commit; if you can’t describe the change in a short sentence, the commit may not be atomic enough.
*   You may prefix the summary with the component or focus of the change. Such a prefix may make it easier for contributors to scan the changelog for commits of interest. See [\[33901\]](https://core.trac.wordpress.org/changeset/33901), [\[33883\]](https://core.trac.wordpress.org/changeset/33883), [\[33848\]](https://core.trac.wordpress.org/changeset/33848) for some examples. Note that the prefix counts toward the 50/70 character count.
*   Use the imperative mood when possible: “Relax term ID comparisons…” instead of “Relaxes term ID comparisons…”
-->

*   1行であり、改行を入れてはいけません。
*   およそ50文字以内、長くても70文字までにします。ログ閲覧ツールはほぼすべて、コミットメッセージの最初の行がこの制限内に収まることを期待しているので、これは重要です。この厳しい制限は、コミットの本質について批判的に考えさせることになるかもしれません。短い文章で変更を説明できない場合、コミットが必要以上に大きなものであるかもしれません。
*   接頭辞としてコンポーネント名付きの要約、または変更の要点を付けられます。このような接頭辞をつけることで、貢献者が興味のあるコミットを変更履歴から探しやすくなるかもしれません。例として、[\[33901\]](https://core.trac.wordpress.org/changeset/33901)、[\[33883\]](https://core.trac.wordpress.org/changeset/33883)、[\[33848\]](https://core.trac.wordpress.org/changeset/33848) を参照してください。接頭辞も50/70文字にカウントされることに注意してください。
*   可能であれば、「Relaxes term ID comparisons…」の代わりに「Relax term ID comparisons…」という命令形を使用します。

<!--
### Description
-->

### 説明

<!--
The longer description of a commit should include more details about the commit and its repercussions for developers. These may include new hooks, “gotchas”, other solutions that were considered, or backstory. Consider your audiences when deciding what should go into the description: developers following along with the commit mailing list, volunteers collating information for each release’s dev notes and WordPress Core Weekly, and future code archaeologists trying to figure out who did what and **why**.
-->

コミットに関するより長い説明には、そのコミットの詳細と開発者への影響を含めるべきです。これには、新しいフック、「gotchas (見落としやすい点)」、検討された他の解決策、背景などが含まれるかもしれません。説明に何を書くかを決める際には、読み手を意識してください。読み手はたとえば、コミットメーリングリストをフォローしている開発者、各リリースの開発者ノートや WordPress Core Weekly のために情報をまとめているボランティア、そして、誰が、何を、**なぜ**、行ったのかを解明しようとしている未来のコード開発者などです。

<!--
#### Guidelines
-->

#### ガイドライン

<!--
*   Must be separated from the summary by a blank line.
*   Can be multiple paragraphs if necessary, separated by blank lines. It is not unreasonable for a commit message to be more verbose than the final changeset itself.
*   Unlike the Summary, lines should not be manually wrapped – log viewers can take care of wrapping the description themselves if they need to.
*   At times it is best to use lists instead of paragraphs, this is at the discretion of the committer.
*   The words `props`, `backport`, `backports` should be avoided.
-->

*   要約と空白行で区切ってください。
*   必要に応じて、空白行で区切って複数の段落にできます。コミットメッセージが最終的なチェンジセット自体よりも冗長になることは不合理ではありません。
*   要約とは異なり、行を手動で折り返す必要はありません。必要に応じて、ログビューアが説明を自分で折り返すことができます。
*   段落の代わりにリストを使用することが良い場合がありますが、これはコミッターの裁量によって決まります。
*   `props`、`backport`、`backports` という単語は避けてください。

<!--
### Follow-up to
-->

### Follow-up to (フォローアップ)

<!--
When the commit is directly related to some previous work such as adding tests for a specific changeset or fast follow fixes, “Follow-up to” must be used with a link to those changesets. If you are backporting a commit, please follow the “Reviewed By and Merges” section instead.
-->

特定のチェンジセットのテストの追加や修正の迅速なフォローなど、コミットが以前の作業に直接関連している場合は、それらのチェンジセットへのリンクとともに「フォローアップ」を使用する必要があります。コミットをバックポートする場合は、代わりに「レビューした人とマージ」セクションに従ってください。

<!--
#### Guidelines
-->

#### ガイドライン

<!--
*   Must be preceded by a blank line.
*   Must wrap changesets in square brackets.
-->

*   先頭には空白行が必要です。
*   チェンジセットは角括弧で囲んでください。

<!--
### Reviewed By and Merges
-->

### Reviewed By and Merges (レビューした人とマージ)

<!--
When [backporting code](https://make.wordpress.org/core/handbook/best-practices/backporting-commits/), use the `Reviewed By and Merges` section to indicate the code that is being merged and who reviewed it. Please specify the branch this is being merged into to help people seeing the commit in chat or email. It’s a best practice for the review to be noted in trac with the `[dev-reviewed](https://make.wordpress.org/core/handbook/contribute/trac/keywords/#action-based-keywords)` keyword.
-->

[コードをバックポートする](https://make.wordpress.org/core/handbook/best-practices/backporting-commits/)場合、マージされるコードとレビューした人を示すために `Reviewed By and Merges` セクションを使用します。チャットやメールでコミットを確認できるように、マージ先のブランチを指定してください。レビューのために、`[dev-reviewed](https://make.wordpress.org/core/handbook/contribute/trac/keywords/#action-based-keywords)` キーワードを使用して Trac に記録することをおすすめします。

<!--
#### Guidelines
-->

#### ガイドライン

<!--
*   This set of two lines must be preceded by a blank line.
*   There should be a hard return between the Reviewed By and Merges lines but there must not be a blank line between them.
*   Multiple core committers may be mentioned as reviewers. When this happens, please separate them with a comma.
*   While the task of moving the code is called backporting, the words `backport`, `backports`, and `backporting` should not be used anywhere in the commit message.
*   Unlike the Summary, lines should not be manually wrapped – log viewers can take care of wrapping the description themselves, if they need to.
-->

*   この2行セットの前には空白行が必要です。
*   「Reviewed By」の行と「Merges」の行の間には改行が必要ですが、間に空白行があってはなりません。
*   複数のコアコミッターがレビュアーとして言及される場合がありますが、その場合はカンマで区切ってください。
*   コードを移動するタスクはバックポートと呼ばれますが、`backport`、`backports`、および `backporting` という単語はコミットメッセージ内のどこにも使用しないでください。
*   要約とは異なり、行を手動で折り返す必要はありません。必要に応じて、ログビューアが説明を自分で折り返すことができます。

<!--
### Props
-->

### Props (称賛)

<!--
Props should be given to all those who contributed to the final commit, whether through patches, refreshed patches, code suggested otherwise, design, writing, user testing, or other significant investments of time and effort. Usernames are parsed for the credits list and WordPress.org profiles.
-->

パッチ、更新されたパッチ、提案されたコード、デザイン、ライティング、ユーザーテスト、その他多大な時間と労力を費やして最終的なコミットに貢献したすべての人に称賛がおくられるべきです。ユーザー名はクレジットリストと WordPress.org プロフィールのために解析されます。

<!--
In the case of bug reports, props should also be given to the reporter of the bug.
-->

バグレポートの場合、バグの報告者にも props が与えられるべきです。

<!--
Check any tickets which were closed as a duplicate in case they contain contributions that warrant props too.
-->

重複としてクローズされたチケットも、props に値する貢献が含まれている可能性があるためチェックしてください。

<!--
#### Guidelines
-->

#### ガイドライン

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
#### Self props
-->

#### 自分の props

<!--
*   Prop yourself when the commit is the product of huge efforts involving multiple people, such a major feature, API, or particularly nasty bug.
*   Generally, giving contributors feedback on patches and giving them a chance to iterate is the recommended process. However, on the occasions where you as the committer complete the idea of a patch, you could write “props X for initial patch.”
*   It is normal for committers to adjust style or rearrange logic before a commit, or to account for a simple edge case. In these instances, omit yourself. Your name on the commit implies that you’ve reviewed and tested it, which is just as important as the contents of the commit.
*   If committing your own code, props are assumed, so omit yourself here as well.
-->

*   大きな機能、API、特にやっかいなバグなど、コミットが複数の人関わった多大な努力の結果である場合は、自分自身に props を与えてください。
*   一般的に、貢献者にパッチに対するフィードバックを提供し、反復する機会を与えることが推奨されるプロセスです。ただし、コミッターであるあなたがパッチのアイデアを完成させる場合には、「props X for initial patch.」と書くこともできます。
*   コミッターがコミットの前にスタイルを調整したり、ロジックを並べ替えたり、あるいは単純なエッジケースを考慮したりするのはよくあることです。このような場合、自分自身を省略してください。コミット上のあなたの名前は、あなたがそれをレビューしてテストしたことを暗示しており、これはコミットの内容と同じくらい重要です。
*   自分自身のコードをコミットする場合は、props が前提となりますので、ここでも自分自身を省略します。

<!--
For a more detailed guide about giving props to contributors, see the [Contributor Attribution (“Props”) page in the handbook](https://make.wordpress.org/core/handbook/best-practices/contributor-attribution-props/).
-->

貢献者へ props を付与することに関する詳細なガイドについては、[ハンドブックの貢献者の帰属 (「props」) ページ](https://make.wordpress.org/core/handbook/best-practices/contributor-attribution-props) を参照してください。

<!--
### Ticket references
-->

### チケットリファレンス

<!--
Trac will add commit messages as comments on all tickets referenced as “fixes” or “see”. If a commit message contains the text “Fixes [#12345](https://core.trac.wordpress.org/ticket/12345)“, Trac will close ticket [#12345](https://core.trac.wordpress.org/ticket/12345) and assign you as the owner if there isn’t one already.
-->

Trac は、「fixes」や「see」として参照されたチケットにコメントとしてコミットメッセージを追加します。コミットメッセージに「Fixes [#12345](https://core.trac.wordpress.org/ticket/12345)」というテキストが含まれている場合、Trac はチケット[#12345](https://core.trac.wordpress.org/ticket/12345)をクローズし、まだ所有者がいなければあなたを所有者にします。

<!--
#### Guidelines
-->

#### ガイドライン

<!--
*   Ticket references should be on their own line directly below any props. If there are no props, an empty newline should separate it from the content above.
*   Multiple tickets should be separated by a comma + space.
*   If referencing both fixed and related tickets, begin with “Fixes” and end each set with a period, e.g. “Fixes [#19867](https://core.trac.wordpress.org/ticket/19867), [#9864](https://core.trac.wordpress.org/ticket/9864). See [#31696](https://core.trac.wordpress.org/ticket/31696).”. If there are many items in a set, put it on its own line.
*   If you forget to include a ticket number, comment on the ticket (e.g., “Fixed in \[changeset\_number\]” with an optional copy of the commit message to help ensure traceability.
-->

*   チケットリファレンスは、props の直下の行に記述してください。props がない場合は、空の改行で上のコンテンツと区切ります。
*   複数のチケットはカンマとスペースで区切ります。
*   修正されたチケットと関連されたチケットの両方を参照する場合は、「Fixes」で始めて各セットをピリオドで終了します。たとえば「Fixes [#19867](https://core.trac.wordpress.org/ticket/19867), [#9864](https://core.trac.wordpress.org/ticket/9864). See [#31696](https://core.trac.wordpress.org/ticket/31696).」などです。セット内の項目が多い場合は、別の行に入れます。
*   チケット番号を入れ忘れた場合は、チケットにコメントを残します (例:「Fixed in \[changeset\_number\]」。オプションでコミットメッセージのコピーを付けると、トレーサビリティを確保しやすくなります)。

<!--
## Example
-->

## 例

<!--
Bad:
-->

悪い:

> Don’t use strict comparisons for term IDs. props booneiscool. fixes [#3398](https://core.trac.wordpress.org/ticket/3398).

<!--
Meh:
-->

まあまあ良い:

> Fixing \`wp\_dropdown\_categories()\` and other places that use term IDs.
>
> props boonerocks. fixes [#20000](https://core.trac.wordpress.org/ticket/20000).

<!--
Good:
-->

良い:

> Taxonomy: Relax term ID comparisons.
>
> Term IDs are sometimes provided as strings. This is particularly evident in \`wp\_dropdown\_categories()\`, where the \`selected\` argument was not being respected. Plugin authors should also be wary of using strict comparisons for term IDs.
>
> Props booneistheman.
> Fixes [#13237](https://core.trac.wordpress.org/ticket/13237).

<!--
## Automatically Pre-fill Commit Message
-->

## コミットメッセージを自動的に事前入力する

<!--
If you use Git (and possibly commit with git-svn), you can have a hook automatically fill a new commit message with the standard format.
-->

Git を使用している場合 (場合によっては git-svn を使用してコミットしている場合)、フックによって新しいコミットメッセージを標準形式で自動的に埋め込むことができます。

<!--
Create a `.git/hooks/prepare-commit-msg` file with the following script, and then `chmod +x .git/hooks/prepare-commit-msg`.
-->

次のスクリプトを使用して `.git/hooks/prepare-commit-msg` ファイルを作成し、`chmod +x .git/hooks/prepare-commit-msg` を実行します。

```bash
#!/bin/bash
COMMIT_MSG_FILE=$1
COMMIT_SOURCE=$2

if [ $COMMIT_SOURCE ]; then
	# A messages is already being provided via `commit -m`, rebase, etc.
	exit 0;
fi

template="Component: Brief summary.

Longer description with more details, such as a \`new_hook\` being introduced with the context of a \`\$post\` and a \`\$screen\`.

More paragraphs can be added as needed.

Props person, another.
Fixes #30000. See #20202, #105.
#
# See https://make.wordpress.org/core/handbook/best-practices/commit-messages/ for more detailed guidelines."

# Wrapping the variable in quotes preserves the newlines, because BASH is weird.
echo "$template" > $COMMIT_MSG_FILE
```

<!--
## Other tips for committers
-->

## コミッター向けのその他のヒント

<!--
While these are not about the commit message itself, the following guidelines are good to keep in mind.
-->

これらはコミットメッセージそのものに関するものではありませんが、以下のガイドラインは覚えておくとよいでしょう。

<!--
During the RC stage, [all patches must be reviewed by a second committer](https://make.wordpress.org/core/handbook/about/release-cycle/releasing-major-versions/#release-candidate) before being committed.
-->

RC のフェーズでは、コミットされる前に[すべてのパッチは2人目のコミッターのレビューを受ける必要があります](https://ja.wordpress.org/team/handbook/core/about/release-cycle/releasing-major-versions/#release-candidate)。

<!--
### Before a commit
-->

### コミットの前

<!--
*   If you have any doubts about whether or not a patch is acceptable, ask a few other committers for a second opinion.
*   Make sure the changed lines conform to [the coding standards](https://make.wordpress.org/core/handbook/best-practices/coding-standards/).
    *   PHP
        *   To check all lines in all changed files, run `phpcs $(git diff trunk --name-only)` or `phpcs $(svn stat | grep "\(M \|A \)" | grep -v "external item" | cut -c8-)` .
        *   To check only the changed lines, clone [wp-dev-lib](https://github.com/xwp/wp-dev-lib/) and [run](https://github.com/xwp/wp-dev-lib/#manually-invoking-pre-commit) `DIFF_BASE=trunk DEV_LIB_ONLY=phpsyntax,phpcs /path/to/wp-dev-lib/pre-commit`. Note that you need to be on a local branch other than `trunk`, and the changes need to be either committed, or staged for commit. Unstaged changes will not be scanned.
        *   Creating Bash aliases for the above commands is recommended for convenience.
    *   JavaScript
        *   [Run](https://make.wordpress.org/core/handbook/best-practices/coding-standards/javascript/#jshint) `npm run grunt jshint`. This will be done automatically by `npm run grunt precommit` as well.
    *   HTML, CSS, a11y
        *   These must be checked manually.
*   Run `npm run grunt build && npm run grunt precommit`. This runs the automated test suites for PHP and JavaScript, as well as various other tasks for CSS, images, etc.
    *   You may also need to manually run PHPUnit with various flags, depending on the change.
*   Check the full diff one last time (`svn diff`). If you’re using Git, interactive staging (`git add -p`) is a good way to review individual chunks.
*   Check the list of modified files (`svn stat`), making sure that new files are added. It is also good to double check the contents of new files, as applying patches that add new files can result in the content of new files being duplicated. Also make sure that new files are not named the same as something in the  `$_old_files` array, or else they will be deleted again right away. If one is, comment out the line from the array with a note indicating when a file with the same name was added back. Do not delete the line.
*   If deleting files, add them to the `$_old_files` array.
*   You can “cherry-pick” commits from `trunk` to a release branch via `svn switch ^/branches/4.3 && svn merge -c 12345 ^/trunk`. You will be prompted to edit the message prior to committing. See [Backporting Commits](https://make.wordpress.org/core/handbook/best-practices/backporting-commits/) for more details.
*   Instructions for tagging and branching a release can be found in the [Core section of the releasing major versions](https://make.wordpress.org/core/handbook/about/release-cycle/releasing-major-versions/#core) page.
*   Bonus: for viewing modified files without including untracked files, add this as a Bash alias or function: `svn stat --ignore-externals | grep '^[^?X]'`
-->

*   パッチが受け入れられるかどうか疑問がある場合は、他のコミッターにセカンドオピニオンを求めてください。
*   変更された行が[コーディング規約](https://ja.wordpress.org/team/handbook/core//best-practices/coding-standards/)に準拠していることを確認してください。
    *   PHP
        *   変更されたすべてのファイルのすべての行をチェックするには、`phpcs $(git diff trunk --name-only)` または `phpcs $(svn stat | grep "\(M \|A \)" | grep -v "external item" | cut -c8-)` を実行します。
        *   変更された行だけをチェックするには、[wp-dev-lib](https://github.com/xwp/wp-dev-lib/) をクローンし、`DIFF_BASE=trunk DEV_LIB_ONLY=phpsyntax,phpcs /path/to/wp-dev-lib/pre-commit` を[実行](https://github.com/xwp/wp-dev-lib/#manually-invoking-pre-commit)します。ローカルブランチが `trunk` 以外である必要があり、変更がコミットされているか、コミット用にステージされている必要があることに注意してください。ステージされていない変更はスキャンされません。
        *   これらのコマンドは、Bash でエイリアスを作成することをおすすめします。
    *   JavaScript
        *   `npm run grunt jshint` を[実行](https://ja.wordpress.org/team/handbook/core/best-practices/coding-standards/javascript/#jshint)します。これは `npm run grunt precommit` でも自動的に行われます。
    * HTML、CSS、a11y
        *   これらは手動でチェックする必要があります。
*   `npm run grunt build && npm run grunt precommit` を実行します。これにより、PHP と JavaScript の自動テストスイートが実行され、CSS や画像などのさまざまなタスクも実行されます。
    *   変更内容によっては、PHPUnit をさまざまなフラグをつけて手動で実行する必要があるかもしれません。
*   最後にもう一度完全な diff をチェックします (`svn diff`)。Git を使用している場合は、インタラクティブなステージング (`git add -p`) は個々のチャンクをレビューするのに良い方法です。
*   変更されたファイルのリストをチェックし (`svn stat`)、新しいファイルが追加されていることを確認します。ここで新しいファイルの内容の再確認をおすすめします。新しいファイルを追加するパッチを適用すると、新しいファイルの内容が重複する場合があるためです。また、新しいファイルの名前が `$_old_files` 配列にあるものと同じでないことを確認してください。そうしないと、すぐにまた削除されてしまいます。もし同じ名前がある場合は、同じ名前のファイルがいつ追加され、戻されたかを示すメモを添えて、配列からその行をコメントアウトしてください。その行は削除しないでください。
*   ファイルを削除する場合は、それらを `$_old_files` 配列に追加します。
*   `svn switch ^/branches/4.3 && svn merge -c 12345 ^/trunk` を使用して、`trunk` からリリースブランチへのコミットを「チェリーピック」できます。コミットする前にメッセージを編集するように求められます。詳しくは[コミットのバックポート](https://ja.wordpress.org/team/handbook/core/best-practices/backporting-commits/)を参照してください。
*   リリースのタグ付けとブランチの手順は、[メジャーバージョンのリリースのコアセクション](https://ja.wordpress.org/team/handbook/core/about/release-cycle/releasing-major-versions/#core)ページにあります。
*   ヒント: 追跡されていないファイルを含めずに変更されたファイルを表示するには、次のように Bash のエイリアスまたは関数として追加してください: `svn stat --ignore-externals | grep '^[^?X]'`

<!--
### After a commit
-->

### コミットの後

<!--
*   Monitor the corresponding job in [GitHub Actions](https://github.com/WordPress/wordpress-develop/actions), in case any tests fail in other environments.
-->

*   他の環境でテストが失敗した場合に備えて、[GitHub Actions](https://github.com/WordPress/wordpress-develop/actions) で対応するジョブを監視します。

<!--
## More resources
-->

## その他のリソース

*   [A Note About Git Commit Messages](http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html)
*   [5 Useful Tips For A Better Commit Message](https://robots.thoughtbot.com/5-useful-tips-for-a-better-commit-message)
*   [How to Write a Git Commit Message](http://chris.beams.io/posts/git-commit/)
