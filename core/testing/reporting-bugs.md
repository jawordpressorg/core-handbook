<!--
# Reporting Bugs
-->

# バグの報告

<!--
## Reporting Security Issues
-->

## セキュリティに関する問題の報告

<!--
While we try to be proactive in preventing security problems, we do not assume they’ll never come up. If you believe you’ve found a security problem in a release of WordPress, please see the [Security FAQ](https://make.wordpress.org/core/handbook/reporting-security-vulnerabilities/) for information on how to report the problem.
-->

私たちはセキュリティの問題を未然に防ぐために積極的に取り組んでいますが、セキュリティの問題が絶対に起きないとは考えていません。WordPress のリリースにセキュリティの問題を発見したと思われる場合、[セキュリティに関する FAQ](https://ja.wordpress.org/team/handbook/core/reporting-security-vulnerabilities/) で問題の報告方法についてご覧ください。

<!--
It is standard practice to notify the vendor (the WordPress security team, in this case) of a security problem before publicizing, so a fix can be prepared, and public damage due to the vulnerability minimized.
-->

セキュリティの問題を公表する前にベンダー (この場合は WordPress のセキュリティチーム) に通知するのが標準的な慣行であり、修正プログラムを準備し、脆弱性による被害を最小限に抑えることができます。

<!--
## Overview of Bug Reporting and Resolution
-->

## バグレポートと解決の概要

<!--
There are many steps in the process of reporting and resolving a bug in WordPress. Here is an overview:
-->

WordPress のバグを報告し解決するプロセスには多くのステップがあります。ここではその概要を説明します:

<!--
*   A user finds a bug that appears to be in the core of WordPress (not a theme or a plugin).
*   The user confirms it is actually a bug which has not yet been reported.
*   The user submits a bug report, called a [ticket](https://make.wordpress.org/core/handbook/glossary/#ticket), to [Trac, the WordPress Bug Tracker](https://make.wordpress.org/core/handbook/trac/).
*   A WordPress developer (who is a volunteer, like you) confirms that the bug does actually exist, and that it should be fixed, and comments as such.
*   A WordPress developer (which could be you) decides to fix the bug. The developer figures out how to fix the bug, create a patch, and uploads the patch to Trac.
*   Members of the WordPress development community test the patch to see if it fixes the bug, and doesn’t break anything else. They may also run [Automated Tests](https://make.wordpress.org/core/handbook/automated-testing/) against the bug and patch, and write new tests (or suggest new tests be written).
*   One of the WordPress developers with authority to modify the official WordPress source code [commits](https://make.wordpress.org/core/handbook/glossary/#commit-verb) the patch to the core code in the SVN repository. They are more likely to do this if the bug and patch has been verified by someone they trust – WordPress development operates largely on a system of trust and merit.
*   The person who commits the patch closes the bug as **fixed**.
-->

*   (テーマやプラグインではなく) WordPress のコアにあると思われるバグをユーザーが見つけた場合。
*   ユーザーは、それが実際にまだ報告されていないバグであることを確認します。
*   ユーザーが [WordPress のバグトラッカーである Trac](https://ja.wordpress.org/team/handbook/core/trac/) に [ticket](https://ja.wordpress.org/team/handbook/core/glossary/#ticket) と呼ばれるバグレポートを提出します。
*   WordPress 開発者 (あなたのようなボランティアです) が、バグが実際に存在し、修正されるべきであると確認し、そのようにコメントします。
*   WordPress 開発者 (あなたかもしれません) がバグを修正することを決定します。開発者はバグを修正する方法を考え、パッチを作成し、パッチを Trac にアップロードします。
*   WordPress 開発コミュニティのメンバーがパッチをテストし、バグが修正されているか、他に何も壊れていないかを確認します。また、バグとパッチに対して[自動テスト](https://ja.wordpress.org/team/handbook/core/automated-testing/)を実行したり、新しいテストを書いたりします (または新しいテストを書くように提案します)。
*   公式の WordPress ソースコードを修正する権限を持つ WordPress 開発者の一人が、SVN リポジトリのコアコードにパッチを[コミット](https://ja.wordpress.org/team/handbook/core/glossary/#commit-verb)します。そのバグやパッチが信頼できる人によって検証されたものであれば、そのようなことをする可能性は高くなります。WordPress の開発は主に信頼と功績のシステムで運営されています。
*   パッチをコミットした人はバグを**修正済み**として閉じます。

<!--
## Before You Report a Bug
-->

## バグを報告する前に

<!--
With large projects like WordPress, so many users report bugs that there’s a good chance your bug has already been reported. Because of this, it’s very important to check to ensure it’s not already in the system before you submit it. If you are new to reporting bugs in WordPress, it is also a good idea to discuss the issue with more experienced developers before reporting it.
-->

WordPress のような大規模なプロジェクトでは、非常に多くのユーザーがバグを報告するため、あなたのバグがすでに報告されている可能性が高いです。このため、バグを報告する前に、そのバグがすでにシステムに登録されていないか確認することが非常に重要です。WordPress でバグを報告するのが初めての場合は、経験豊富な開発者に相談してから報告するのもよい方法です。

<!--
**1\. Make sure the bug is actually caused by WordPress core.**
-->

**1\. バグが実際に WordPress コアに起因していることを確認してください。**

<!--
Just because an error message points to a core file, doesn’t mean that’s where the problem is. You may want to use a plugin like [Debug Bar](https://wordpress.org/extend/plugins/debug-bar/) to track down the problem. A simple script like this [debugging file](http://gist.github.com/625769) could help you see where exactly the error is coming from. (You can place this file in your **wp-content/mu-plugins** directory; create it if it doesn’t exist.)
-->

エラーメッセージがコアファイルを指しているからといって、そこに問題があるとは限りません。[Debug Bar](https://wordpress.org/extend/plugins/debug-bar/) のようなプラグインを使って問題を突きとめたほうがいいかもしれません。この[デバッグファイル](http://gist.github.com/625769)のような簡単なスクリプトを使えば、エラーの原因がどこにあるのかを正確に突きとめることができます。(このファイルは **wp-content/mu-plugins** ディレクトリに置くことができます。存在しない場合は作成してください)。

<!--
Another key strategy is to try and replicate the bug in a fresh WordPress install with no extra plugins or themes. While this may not always be possible, if you can find it in a fresh install, the issue is much more likely to be in core.
-->

もう一つの重要な戦略は、プラグインやテーマを追加していない、新しい WordPress インストールでバグを再現してみることです。これは常に可能ではないかもしれませんが、新しいインストールでもバグが見つかれば、問題はコアにある可能性が高いです。

<!--
**2\. [Search](https://core.trac.wordpress.org/search) for your bug or enhancement request.**
-->

**2\. バグや機能強化の要望を[検索](https://core.trac.wordpress.org/search)してください。**

<!--
*   If your issue has already been reported, please do not report a duplicate bug. If you have further information to contribute, add a note to the existing bug.
*   If your issue is similar, but not quite the same as another issue, you may decide whether to add a note to the similar issue, or report a new one. In general, if you just have more information to contribute to a current, open issue, simply add a note to that issue. If you have a different enough issue, or if you are experiencing a recurrence of an issue that was previously resolved, report a new bug. Either way, core contributors will offer you guidance once you’ve posted about your issue.
*   If your issue was recently reported and then closed, and you do not agree with the resolution, you can still post comments as to your reasoning.
*   It is best not to re-open bugs that have been closed for some time. If the bug was closed as **fixed** for a version of WordPress that has been released already (see the **Milestone** field), open a new ticket.
*   The **Version** field relates to the version in which the bug was originally discovered. If you’re seeing the same bug in a newer version, mention so in a comment, but please do not change the version number.
-->

*   あなたの問題がすでに報告されている場合、重複したバグを報告しないでください。さらに貢献できる情報がある場合は、既存のバグにメモを追加してください。
*   あなたの問題が他の問題と類似しているが、まったく同じではない場合、類似した問題にメモを追加するか、新しい問題を報告するかを決めることができます。一般的に、現在進行中の未解決の issue に貢献できる情報があれば、その issue にメモを追加してください。別の十分な問題がある場合、または以前に解決した問題が再発した場合は、新しいバグを報告してください。いずれにせよ、あなたが問題を投稿すれば、コアの貢献者がアドバイスを提供してくれるでしょう。
*   あなたの問題が最近報告され、その後クローズされ、あなたがその解決策に同意しない場合でも、あなたの理由をコメントとして投稿できます。
*   クローズされたバグを再オープンしないことがベストです。そのバグがすでにリリースされた WordPress のバージョンで**修正済み**としてクローズされた場合 (**Milestone** フィールドを参照)、新しいチケットを開いてください。
*   **Version** フィールドは、バグが最初に発見されたバージョンに関連します。新しいバージョンで同じバグが見つかった場合は、コメントでその旨を書いてください。ただし、バージョン番号は変更しないでください。

<!--
**3\. Consider discussing a possible bug before reporting it.**
-->

**3\. バグを報告する前に、可能性のあるバグについて議論することを検討してください。**

<!--
*   If you aren’t sure that you’ve found a bug, you should attempt to discuss it with a developer before reporting it. You can discuss your issue on the [WordPress Slack Channel](https://make.wordpress.org/chat/), post a question on the [WordPress Support Forum](https://wordpress.org/support/), or start an email discussion on the [wp-testers](https://codex.wordpress.org/Mailing_Lists#Testers) or [wp-hackers](https://codex.wordpress.org/Mailing_Lists#Hackers) mailing lists.
-->

*   バグを見つけたかどうか確信が持てない場合は、報告する前に開発者と話し合うようにしてください。[WordPress Slack チャンネル](https://make.wordpress.org/chat/)で議論したり、[WordPress サポートフォーラム](https://wordpress.org/support/)に質問を投稿したり、[wp-testers](https://codex.wordpress.org/Mailing_Lists#Testers) や [wp-hackers](https://codex.wordpress.org/Mailing_Lists#Hackers) のメーリングリストでメールディスカッションを始めることができます。

<!--
## Reporting a Bug
-->

## バグを報告する

<!--
Trac is the name of the official WordPress bug tracker. It uses the open source bug tracking software Trac, by Edgewall Software. To learn more about Trac, see [The Bug Tracker (Trac)](https://make.wordpress.org/core/handbook/trac/). To create a good bug report:
-->

Trac は WordPress の公式バグトラッカーの名前です。Edgewall Software によるオープンソースのバグトラッキングソフトウェア Trac を使用しています。Trac について詳しくは、[バグトラッカー (Trac)](https://ja.wordpress.org/team/handbook/core/trac/) を参照してください。良いバグレポートを作成するには:

<!--
1.  Read the section above about what to do [before reporting a bug](#before-you-report-a-bug).
2.  Log onto [WordPress Trac](https://core.trac.wordpress.org/) using your [support forum](https://wordpress.org/support/) username and password. If you don’t have an account at the support forums, you can [register](https://wordpress.org/support/register.php).
3.  Click [New Ticket](https://core.trac.wordpress.org/newticket) in Trac to reach the bug reporting page.
4.  Fill in the title, summary, and other fields. For more, see the section on [Ticket Properties](https://make.wordpress.org/core/handbook/trac/#ticket-properties).
5.  Click **Submit Ticket** after previewing it.
-->

1.  [バグを報告する前に](#%e3%83%90%e3%82%b0%e3%82%92%e5%a0%b1%e5%91%8a%e3%81%99%e3%82%8b%e5%89%8d%e3%81%ab)行うべきことについては、上記のセクションを参照してください。
2.  [サポートフォーラム](https://wordpress.org/support/)のユーザー名とパスワードを使って [WordPress Trac](https://core.trac.wordpress.org/) にログインします。サポートフォーラムのアカウントを持っていない場合は、[登録](https://wordpress.org/support/register.php)してください。
3.  Trac の [New Ticket](https://core.trac.wordpress.org/newticket) をクリックして、バグレポートページにアクセスします。
4.  タイトル、概要、その他のフィールドを記入してください。詳しくは [チケットのプロパティ](https://ja.wordpress.org/team/handbook/core/trac/#ticket-properties)を参照してください。
5.  プレビュー後、**Submit Ticket** をクリックしてください。

<!--
Your involvement doesn’t end after you’ve submitted a ticket. Developers may need more information as they review the ticket (and may specifically request more information from you by tagging the ticket with **reporter-feedback**).
-->

あなたがチケットを提出したからといって、あなたのやることが終わったわけではありません。開発者はチケットをレビューする際に、より多くの情報を必要とするかもしれません (そして、チケットに **reporter-feedback** というタグをつけて、特にあなたに詳細な情報を求めるかもしれません)。

<!--
You can also help by verifying that proposed fixes solve the problem you were experiencing. The processing of your bug may require your participation, so please be willing and prepared to aid the developers in resolving the issue. If you’d like to help fix the bug, see the section on [Fixing Bugs](https://make.wordpress.org/core/handbook/fixing-bugs/).
-->

また、提案された修正によってあなたが遭遇した問題が解決されるかどうかを確認することも役立ちます。バグの処理にはあなたの協力が必要な場合がありますので、開発者が問題を解決することを手助けできるよう準備してください。バグの修正にご協力いただける場合は、[バグの修正](https://ja.wordpress.org/team/handbook/core/fixing-bugs/)セクションをご覧ください。

<!--
You will be automatically emailed when your tickets are updated if you’ve entered your email address in [your Trac preferences](https://core.trac.wordpress.org/prefs).
-->

[Trac 設定](https://core.trac.wordpress.org/prefs)にメールアドレスを入力していれば、チケットが更新されたときに自動的に電子メールが送信されます。
