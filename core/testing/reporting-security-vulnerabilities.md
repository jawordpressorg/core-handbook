<!--
# Reporting Security Vulnerabilities
-->

# セキュリティ脆弱性の報告

<!--
While we try to be proactive in preventing security problems, we do not assume they’ll never come up.
-->

私たちはセキュリティno\\の問題を未然に防ぐために積極的に努めていますが、セキュリティの問題が決して起きないとは考えていません。

<!--
It is standard practice to **responsibly and privately disclose** to the vendor (the WordPress core development team, in this case) a security problem before publicizing, so a fix can be prepared, and damage from the vulnerability minimized.
-->

セキュリティの問題を公開する前に、**責任を持って非公開で**ベンダー (この場合は WordPress コア開発チーム) に開示することが標準的な方法です。これにより、修正が準備され、脆弱性による被害が最小限に抑えられます。

<!--
## What is a “security” issue?
-->

## 「セキュリティ」の問題とは ?

<!-- A security issue is a type of bug that can affect the security of WordPress installations. -->

セキュリティの問題とは、WordPress インストールのセキュリティに影響を与える一種のバグです。

<!--
Specifically, it is a report of a bug that you have found in the WordPress core code, and that you have determined can be used to gain some level of access to a site running WordPress that you should not have.
-->

具体的には、WordPress のコアコードにバグを発見し、そのバグを利用して、WordPress が稼働しているサイトに本来アクセスできないはずのアクセスが可能であると判断した場合に報告するものです。

<!--
Your site being “hacked ” is **not** a security issue. The security issue will involve knowing how the attacker got in and hacked the site. If you have details on the attack, then contact us. If not, then the [Support Forums](https://wordpress.org/support/) are the most appropriate place to report such an issue.
-->

あなたのサイトが「ハッキング」されることは、セキュリティの問題**ではありません**。セキュリティの問題は、攻撃者がどのようにして侵入し、サイトをハッキングしたかを把握することです。攻撃に関する詳細をお持ちの場合は、私たちにご連絡ください。そうでない場合は、[サポートフォーラム](https://wordpress.org/support/)がそのような問題を報告する最も適切な場所です。

<!--
You forgetting your password or losing access to your site is **not** a security issue. If you lost access through a bug in the WordPress code, then that might be a security issue.
-->

パスワードを忘れたり、サイトにアクセスできなくなったりすることは、セキュリティの問題**ではありません**。WordPress コードのバグによってアクセスできなくなった場合は、セキュリティの問題かもしれません。

<!--
Generally, security issues are complex problems. If you want to report a security issue, then that’s great! You’re in the right place. However, be sure that what you’re reporting is **actually** a security issue. The experts that you are reporting it to are very busy, and don’t usually respond to non-security issues.
-->

一般的に、セキュリティの問題は複雑な問題です。セキュリティの問題を報告したいのであれば、それはすばらしいことです ! あなたの考えは正しいでしょう。ただし、報告する内容が**本当に**セキュリティの問題であるかどうかを確認してください。あなたが報告しようとしている専門家はとても忙しく、通常はセキュリティ以外の問題には対応しません。

<!--
The security reporting system is NOT for support. Don’t send general problems there.
-->

セキュリティ報告システムはサポート用ではありません。一般的な問題をそこに送らないでください。

<!--
## Where do I report security issues?
-->

## セキュリティの問題はどこに報告すればよいですか ?

<!--
*   If you are here to report any sort of security issue with [a site hosted on **WordPress.com**](https://en.support.wordpress.com/com-vs-org/), then please [submit a report at the Automattic HackerOne page](https://hackerone.com/automattic). If the issue you’re trying to report is on WordPress.com and is **not** a security issue, then please use their [support forums](https://en.forums.wordpress.com/) instead.
*   If you’re having an issue with your own self-hosted WordPress.org site that is **not** a security issue, then please use the WordPress.org [support forums](https://wordpress.org/support/).
*   For security issues with WordPress plugins, follow the information on [Reporting Plugin Security Issues](https://developer.wordpress.org/plugins/wordpress-org/plugin-security/reporting-plugin-security-issues/).
*   **For security issues with the self-hosted version of WordPress**, submit a report at the [WordPress HackerOne page](https://hackerone.com/wordpress). Include as much detail as you can. Please **always use HackerOne instead of Core Trac**, even if the vulnerability is only in `trunk`, or a beta/RC release, because there are some sites that run those in production.
-->

*   [**WordPress.com** でホストされているサイト](https://en.support.wordpress.com/com-vs-org/)のセキュリティ上の問題を報告する場合は、[Automattic HackerOne ページでレポートを提出してください](https://hackerone.com/automattic)。報告しようとしている問題が WordPress.com のもので、セキュリティの問題**ではない**場合は、[サポートフォーラム](https://en.forums.wordpress.com/)を利用してください。
*   セキュリティの問題**ではなく**、セルフホストの WordPress.org サイトに問題がある場合は、WordPress.org の[サポートフォーラム](https://wordpress.org/support/)を利用してください。
*   WordPress プラグインのセキュリティ問題については、[プラグインのセキュリティ問題の報告](https://developer.wordpress.org/plugins/wordpress-org/plugin-security/reporting-plugin-security-issues/)にある情報を参照してください。
*   **WordPress のセルフホストバージョンに関するセキュリティの問題**については、[WordPress HackerOne ページ](https://hackerone.com/wordpress)でレポートを提出し、できる限り詳細を記載してください。脆弱性が `trunk` またはベータ/RC リリースにのみ存在する場合でも、**コア Trac ではなく常に HackerOne を使用してください**。これらを本番環境で実行しているサイトがいくつかあるためです。

<!--
In all cases, you should **not** share the details with anyone else until after the fix for the bug has been officially released to the public.
-->

どのような場合でも、バグの修正が正式に公開されるまでは、その詳細を他の人と**共有してはいけません**。

<!--
## Where do I report copyright infringements, libel, and other legal issues?
-->

## 著作権侵害、名誉毀損、その他の法的な問題はどこに報告すればよいですか ?

<!--
[WordPress.org](https://wordpress.org/) does not host sites. [WordPress.org](https://wordpress.org/) provides publishing software that anyone can download and use. The organization, [WordPress.org](https://wordpress.org/), has no control over who uses the software, or how they use it. In other words, [WordPress.org](https://wordpress.org/) does NOT have the power to take down comments, posts, sites, or anything else.
-->

[WordPress.org](https://wordpress.org/) はサイトをホストしていません。[WordPress.org](https://wordpress.org/) は、誰でもダウンロードして使用できる公開ソフトウェアを提供しています。組織である [WordPress.org](https://wordpress.org/) は、誰がどのようにソフトウェアを使用するかを管理できません。言い換えれば、[WordPress.org](https://wordpress.org/) は、コメント、投稿、サイト、その他のものを削除する権限を持っていません。

<!--
Instead of trying to contact WordPress, perform a [whois lookup](http://whois.domaintools.com/) to track down the operator or host of a particular site, then report the infringement to those organizations.
-->

WordPress に連絡しようとするのではなく、[whois lookup](http://whois.domaintools.com/) を実行して特定のサイトの運営者やホストを追跡し、それらの組織に侵害を報告してください。

<!--
If you still can’t determine the organization, these following articles by Plagiarism Today may help:
-->

それでも組織を特定できない場合は、Plagiarism Today による以下の記事が役に立つかもしれません:

<!--
*   [Finding the Host](https://www.plagiarismtoday.com/stopping-internet-plagiarism/3-finding-the-host/)
*   [6 Steps to Find a Host’s DMCA Contact](https://www.plagiarismtoday.com/2009/07/16/6-steps-to-find-a-hosts-dmca-contact/)
-->

* [ホストを見つける](https://www.plagiarismtoday.com/stopping-internet-plagiarism/3-finding-the-host/)
* [ホストの DMCA 連絡先を見つけるための6つのステップ](https://www.plagiarismtoday.com/2009/07/16/6-steps-to-find-a-hosts-dmca-contact/)

<!--
## I’ve been hacked. What do I do now?
-->

## ハッキングされました。何をすればいいでしょうか ?

<!--
Things you should do:
-->

やるべきこと:

<!--
*   Change passwords for all users, especially Administrators and Editors.
*   If you upload files to your site via FTP, change your FTP password.
*   Re-install the latest version of WordPress.
*   Make sure all of your plugins and themes are up-to-date.
*   Update your [security keys](https://wordpress.org/support/article/editing-wp-config-php/#security-keys).
*   See [FAQ My Site Was Hacked](https://wordpress.org/support/article/faq-my-site-was-hacked/).
-->

*   すべてのユーザー、特に管理者と編集者のパスワードを変更してください。
*   FTP でファイルをアップロードしている場合は、FTP パスワードを変更してください。
*   WordPress の最新バージョンを再インストールしてください。
*   すべてのプラグインとテーマが最新であることを確認してください。
*   [セキュリティキー](https://wordpress.org/support/article/editing-wp-config-php/#security-keys)を更新してください。
*   [FAQ サイトがハッキングされました](https://wordpress.org/support/article/faq-my-site-was-hacked/)を参照してください。

<!--
## Why are some users allowed to post unfiltered HTML?
-->

## 一部のユーザーがフィルタリングされていない HTML を投稿できるのはなぜですか ?

<!--
Users with Administrator or Editor [roles](https://codex.wordpress.org/Roles_and_Capabilities#Roles) are allowed to publish unfiltered HTML in post titles, post content, and comments, and upload HTML files to the media library. WordPress is, after all, a publishing tool, and people need to be able to include whatever markup they need to communicate. Users with lesser privileges (Authors and Contributors) are not allowed to post unfiltered content or upload HTML files.
-->

管理者または編集者[権限](https://codex.wordpress.org/Roles_and_Capabilities#Roles)を持つユーザーは、投稿タイトル、投稿コンテンツ、コメントにフィルタリングされていない HTML を公開し、メディアライブラリに HTML ファイルをアップロードできます。WordPress は結局のところ投稿ツールであり、人々はコミュニケーションに必要なあらゆるマークアップを含めることができる必要があります。より低い権限を持つユーザー (投稿者と寄稿者) は、フィルタリングされていないコンテンツを投稿したり、HTML ファイルをアップロードできません。

<!--
If you are running security tests against WordPress, use a lesser privileged user so that all content is filtered. If you are concerned about an Administrator or Editor putting XSS into content and stealing cookies, note that all cookies are marked for HTTP only delivery, and are divided into privileged cookies used for admin pages, and unprivileged cookies used for public facing pages. Content is never displayed unfiltered within the admin dashboard.
-->

WordPress に対してセキュリティテストを実行する場合は、すべてのコンテンツがフィルタリングされるように、より低い権限のユーザーを使用してください。管理者や編集者がコンテンツに XSS を入れたり、Cookie を盗んだりすることを心配する場合、すべての Cookie は HTTP のみの配信にマークされ、管理者ページで使用される特権 Cookie と、一般向けページで使用される非特権 Coolie に分けられていることに注意してください。管理ダッシュボード内で、コンテンツがフィルタリングされずに表示されることはありません。

<!--
In WordPress Multisite, only Super Admins can publish unfiltered HTML, as all other users (including site Administrators) are considered untrusted.
-->

WordPress のマルチサイトでは、(サイト管理者を含む) 他のすべてのユーザーは信頼できないとみなされ、特権管理者のみがフィルタリングされていない HTML を公開できます。

<!--
To disable unfiltered HTML for all users, including administrators, you can add `define( 'DISALLOW_UNFILTERED_HTML', true );` to `wp-config.php`.
-->

管理者を含むすべてのユーザーに対してフィルタリングされていない HTML を無効にするには、`wp-config.php` に `define( 'DISALLOW_UNFILTERED_HTML', true );` を追加します。

<!--
## Why are disclosures of usernames or user IDs not a security issue?
-->

## なぜユーザー名やユーザー ID の漏洩はセキュリティ上の問題ではないのですか ?

<!--
The WordPress project doesn’t consider usernames or user ids to be private or secure information. A username is part of your online identity. It is meant to identify, not verify, who you are saying you are. Verification is the job of the password.
-->

WordPress プロジェクトは、ユーザー名やユーザー ID を個人情報または安全な情報とはみなしません。ユーザー名はオンライン ID の一部です。これは、あなたが誰であるかを確認することではなく、識別するためのものです。検証はパスワードの仕事です。

<!--
Generally speaking, people do not consider usernames to be secret, often sharing them openly. Additionally, many major online establishments — such as Google and Facebook — have done away with usernames in favor of email addresses, which are shared around constantly and freely. WordPress has also moved this way, allowing users to log in with an email address or username since version 4.5.
-->

一般的に、人々はユーザー名が秘密であるとは考えず、しばしばオープンに共有します。さらに、Google や Facebook などの多くの主要なオンライン企業は、ユーザー名を廃止し、常に自由に共有されるメールアドレスを採用しています。WordPress もこの方法に移行し、バージョン4.5以降では、ユーザーはメールアドレスまたはユーザー名でログインできるようになりました。

<!--
Instead of attempting to hide a public identifier, WordPress attempts to encourage users to choose strong passwords instead, through both user interface as well as education.
-->

WordPress は公開された識別子を隠そうとするのではなく、ユーザーインターフェイスと教育の両方を通じてユーザーに強力なパスワードを選択することを促そうとしています。

<!--
Note that WordPress is not the only open source project to believe this. [Drupal has similar arguments for the same thing.](https://www.drupal.org/node/1004778)
-->

これを信じているオープンソースプロジェクトは WordPress だけではありません。[Drupal でも同じことについて同様の議論があります。](https://www.drupal.org/node/1004778)

<!--
## Why are there path disclosures when directly loading certain files?
-->

## 特定のファイルを直接ロードするときにパスが開示されるのはなぜですか ?

<!--
This is a server configuration problem. Never enable `display_errors` on a production site.
-->

これはサーバー設定の問題です。本番サイトでは決して `display_errors` を有効にしないでください。

<!--
## Why did I get this “Password Reset” email?
-->

## なぜ「パスワードリセット」メールが届いたのですか ?

<!--
If you get an email saying “Someone has asked to reset the password for the following site and username”, this means someone visited the password reset page on your site. Anyone can visit this page, since it must be open to all for it to be accessible to those who have lost their password. Your password can be reset only by those who can read your email. If your email account has not been compromised, you can ignore this email.
-->

「誰かが次のサイトとユーザー名のパスワードのリセットを要求しました」というメールを受け取った場合、これは誰かがあなたのサイトのパスワードリセットページにアクセスしたことを意味します。パスワードを紛失した人がアクセスできるようにするには、全員に公開する必要があるため、誰でもこのページにアクセスできます。パスワードをリセットできるのは、メールを読むことができる人だけです。メールアカウントが侵害されていない場合は、このメールを無視してもかまいません。
