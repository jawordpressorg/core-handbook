<!--
# Design Decisions
-->

# 設計上の決定事項

<!--
This page lists a number of important design decisions that come up frequently, and attempts to explain and cross-reference the reasoning behind them.
-->

このページでは、頻繁に登場する重要な設計上の決定をリストアップし、その理由を説明したり、相互参照したりすることを意図しています。

<!--
## Absolute versus relative URLs
-->

## 絶対 URL と相対 URL

<!--
WordPress stores absolute URLs in the database. Relative URLs are not used for a variety of reasons. Dynamically generated websites need permanent URLs (permalinks), so absolute URIs make more sense. WordPress has a [variety of functions](https://codex.wordpress.org/Function_Reference/site_url#Related) to call a site domain and various folders in plugins and themes so that relative URLs are not necessary. When moving domains, there are search and replace tools for switching domains in the database.
-->

WordPress は絶対 URL をデータベースに保存します。相対 URL は、さまざまな理由から使用されません。動的に生成されるサイトには永続的な URL (パーマリンク) が必要ですので、絶対 URI の方が理にかなっています。WordPress には、サイトドメインやプラグイン、テーマの各種フォルダーを呼び出す[様々な機能](https://codex.wordpress.org/Function_Reference/site_url#Related)があるので、相対 URL は必要ありません。ドメインを移動する場合、データベース内のドメインを切り替えるための検索・置換ツールがあります。

<!--
### Why relative URLs are not good
-->

### 相対 URL はなぜ良くないのか

<!--
Content is migratory. That is to say that the content, which is in the database, might not always be displayed within the context of “your site”. Content can be displayed in a variety of places. For example, an RSS feed of your content can be pulled into Google Reader and displayed there. Or users can use feed readers of their own. Or the content can be pulled from your site using microformats and displayed somewhere else. A user will never know where the content is going to be. Therefore an absolute URL is necessary within that content to ensure that it always points to a specific point, regardless of where it’s displayed.
-->

コンテンツは移動するものです。つまり、データベース内にあるコンテンツは、必ずしも「あなたのサイト」のコンテキスト内で表示されるとは限らないということです。コンテンツは、さまざまな場所で表示できます。たとえば、コンテンツの RSS フィードを Google リーダーに取り込み、そこに表示させることができます。あるいは、ユーザーは自分のフィードリーダーを使用でき、マイクロフォーマットを使ってあなたのサイトから引き出され、どこか別の場所で表示されることもあります。ユーザーは、コンテンツがどこにあるのかを知ることはありません。したがって、コンテンツがどこに表示されるかにかかわらず、常に特定のポイントを指していることを保証するために、そのコンテンツ内では絶対 URL が必要です。

<!--
Permalinks are malleable. The content of a post can be displayed on `http://example.com/`, on `http://example.com/archive/`, `http://example.com/2012/01/single-post`, and so on. A relative URL would not be valid unless it is “root-relative”, meaning that it started with a / character, to refer to the root of the site. Even then, if a site is moved from one subdirectory to another, the root-relative URL would still need to change, and changing the content in the database to adjust would be necessary.
-->

パーマリンクは変更可能です。ある記事のコンテンツは、`http://example.com/`、`http://example.com/archive/`、`http://example.com/2012/01/single-post` などで表示できます。相対 URL は、「ルート相対」、つまりサイトのルートを参照するために	スラッシュ文字で始まるものでなければ有効ではありません。その場合でも、サイトがあるサブディレクトリから別のサブディレクトリに移動した場合は、ルート相対 URL を変更する必要があり、それに合わせてデータベースのコンテンツを変更する必要があります。

<!--
Moving is easier with absolute URLs. For example, assume a user is moving from `http://foo.com` to `http://bar.com`. Doing a search and replace in the database for `"http://foo.com"` and replacing that is very easy and unlikely to be problematic. One might say that a root-relative URL would not need to change at all in such a case, and this is true, but what if the content needs to be moved from `http://foo.com/dev/` to `http://bar.com`? The root-relative URLs still need to change in such a case, and now there isn’t a simple to find string, such as `"http://foo.com/dev/"` to search and replace on.
-->

移動は絶対 URL の方が簡単です。たとえば、あるユーザーが `http://foo.com` から `http://bar.com` に移動するとします。データベースで `"http://foo.com"` を検索して置き換えるのはとても簡単で、問題になることはまずありません。このような場合、ルート相対 URL はまったく変更する必要がないと言われるかもしれませんし、これは事実です。しかし、コンテンツを `http://foo.com/dev/` から `http://bar.com` に移動させる必要がある場合はどうでしょうか。このような場合にもルート相対 URL は変更する必要があり、検索したり置換するための `"http://foo.com/dev/"` のような簡単に見つけることができる文字列は存在しません。

<!--
Also, within the content of posts themselves, absolute URLs are easier to manage.
-->

また投稿の内容自体も、絶対 URL の方が管理しやすいでしょう。

<!--
It has been suggested that if WordPress were to be able to do all of this over, [we may have instead opted for relative URLs](https://core.trac.wordpress.org/ticket/17048#comment:46). This is true, and making adjustments to our current approach – or reconsidering it in its entirety – does remain a distinct possibility in the future. See [#17048](https://core.trac.wordpress.org/ticket/17048).
-->

もし WordPress がこのすべてをやり直すことができるのであれば、[私たちは相対 URL を選んだかもしれない](https://core.trac.wordpress.org/ticket/17048#comment:46)と提案されています。これは事実であり、現在のアプローチを調整すること、あるいは全体を見直すことは、将来的にはっきりとした可能性として残されています。[#17048](https://core.trac.wordpress.org/ticket/17048)を参照してください。

<!--
## No support for forwarding headers for HTTPS or IP addresses
-->

## HTTPS や IP アドレスの転送ヘッダーをサポートしない

<!--
Many load balancers and proxy servers forward HTTP headers for HTTPS, IP addresses, and more. These typically take the form of HTTP\_X\_FORWARDED\_FOR (X-Forwarded-For), for remote IP addresses, and HTTP\_X\_FORWARDED\_PROTO (X-Forwarded-Proto), for whether traffic is going over the HTTPS protocol. Occasionally other information needs to be forwarded, like the server port.
-->

多くのロードバランサーやプロキシサーバーは、HTTPS や IP アドレスなどのために HTTP ヘッダーを転送します。これらは通常、リモート IP アドレスについては HTTP_X_FORWARDED_FOR (X-Forwarded-For)、HTTPS プロトコルでトラフィックが移動しているかどうかについては HTTP_X_FORWARDED_PROTO (X-Forwarded-Proto) という形式になっています。場合によっては、サーバーポートのような他の情報も転送する必要があります。

<!--
If WordPress blindly listened to these headers – especially for protocols – there is a risk of infinite redirects and general breakage. To make matters worse, these are not formal standards, and are rather freeform. As a result, many web server and  configurations do this differently. For example, one configuration might prepend “HTTP\_”, resulting in HTTP\_HTTPS. What should be done instead is a server should either pass properly mapped headers to PHP, or some code can do the mapping in `wp-config.php`. For example:
-->

WordPress がこれらのヘッダーをやみくもに参照すると、特にプロトコルの場合に無限リダイレクトや一般的な破損が発生するリスクがあります。さらに悪いことに、これらは正式な標準ではなく自由な形式なのです。その結果、多くの Web サーバーや構成はこれを異なる方法で行います。たとえばある構成では、「HTTP_」を先頭につけて HTTP_HTTPS となることがあります。代わりに行われるべきことは、サーバーが適切にマッピングされたヘッダーを PHP に渡すか、あるいは `wp-config.php` でマッピングを行うコードが書かれるかです。たとえば、以下のようになります。

```php
if (
	isset( $_SERVER['HTTP_X_FORWARDED_PROTO'] ) &&
	'https' === $_SERVER['HTTP_X_FORWARDED_PROTO']
) {
	$_SERVER['HTTPS'] = 'on';
}
```

<!--
See also: [#9235](https://core.trac.wordpress.org/ticket/9235), [#15009](https://core.trac.wordpress.org/ticket/15009), [#15733](https://core.trac.wordpress.org/ticket/15733), [#19337](https://core.trac.wordpress.org/ticket/19337), [#24394](https://core.trac.wordpress.org/ticket/24394), etc.
-->

こちらも参照してください。[#9235](https://core.trac.wordpress.org/ticket/9235)、[#15009](https://core.trac.wordpress.org/ticket/15009)、[#15733](https://core.trac.wordpress.org/ticket/15733)、[#19337](https://core.trac.wordpress.org/ticket/19337)、[#24394](https://core.trac.wordpress.org/ticket/24394)など。

<!--
## Adding new oEmbed providers
-->

## 新しい oEmbed プロバイダの追加

<!--
We have a certain standard for oEmbed providers in core. In order to add a new one to the existing allow-list, they must:
-->

コアの oEmbed プロバイダには、一定の基準があります。既存の許可リストに新しいものを追加するためには、これらが必要です。

<!--
*   be well-established, popular, and mainstream services,
*   properly and fully implement [the oEmbed specification](http://oembed.com/),
*   and clearly be a trusted provider.
-->

*   確立されており、人気がある、主流のサービスであること、
*   [oEmbed の仕様](http://oembed.com/)を適切かつ完全に実装していること、
*   そして、明らかに信頼できるプロバイダであること。

<!--
Security is important with oEmbed, because it is dealing with raw, unfiltered HTML, which is inherently dangerous due to arbitrary JavaScript and object embedding. It is therefore paramount that the provider can be trusted. But trust is more than about security — the service must also be “built to last.” If a provider ever stops supporting oEmbed, sites start to lose content they previously trusted would stay embedded permanently.  Or, if a dead startup’s domain expires or is acquired, it could be an easy vector for malware. Nascent services are just too fragile to be added for core.
-->

oEmbed はフィルタリングされていない未加工の HTML を扱うため、セキュリティが重要です。これは、任意の JavaScript やオブジェクトを埋め込むことができるため、本質的に危険です。従って、プロバイダが信頼できることが最も重要です。しかし、信頼とはセキュリティだけではありません。サービスは「永続的に使える」ものでなければなりません。もしプロバイダが oEmbed のサポートを停止した場合、サイトは、以前は永久に埋め込まれていると信じられていたコンテンツを失い始めます。あるいは、消滅したスタートアップのドメインが期限切れとなったり買収されたりすると、マルウェアの格好の餌食となる可能性もあります。新興のサービスは、コアに追加するにはあまりにも脆弱なのです。

<!--
With regards to establishment and popularity, there are a number of things that can be considered, such as:
-->

定着度や人気度については、次のようなにいろいろと考えられます。

<!--
*   Is the service is popular enough for core developers to have heard of it before? Is it “mainstream?”
*   If similar services are already supported, how does this service compare in terms of size, features, and backing?
*   Does this service have an established social media presence?
*   Is its oEmbed endpoint clearly established and properly documented? (Sometimes, they are just a developer’s pet project that may not be supported.)
*   Does the oEmbed endpoint work with WordPress’ oEmbed auto-discovery? If not, could it be made to work with additional HTML tags or attributes being added to the allow-list?
*   Does the service make an effort to build relationships with developers, such as through robust APIs?
*   How old is the service?
*   Does it have a well-established Wikipedia article? (Seriously.)
*   Has anyone written a WordPress plugin that leverages the service in some way, whether adding it as an oEmbed provider, creating a shortcode, or leveraging other APIs of the service? Do these plugins have any noticeable adoption or traction that would indicate usage and demand?
*   Is the provider frequently proposed?
-->

*   コア開発者が聞いたことがあるような人気のあるサービスですか ?「主流」ですか ?
*   同様のサービスがすでにサポートされている場合、このサービスは規模、機能、支持者の面ではどのように比較されますか ?
*   このサービスは、ソーシャルメディアにおいて確立された存在感を示していますか ?
*   その oEmbed エンドポイントは明確に確立され、適切にドキュメント化されていますか ? (時には、開発者の趣味であるプロジェクトに過ぎず、サポートされていない場合もあります)。
*   oEmbed エンドポイントは、WordPress の oEmbed 自動検出で機能しますか ? そうでない場合、HTML タグや属性を許可リストに追加して動作させることは可能ですか ?
*   API を充実させるなど、開発者との関係作りに力を入れていますか ?
*   サービスはいつ開始しましたか ?
*   ウィキペディアの記事が定着していますか ? (これは真面目な話です)
*   oEmbed プロバイダとして追加したり、ショートコードを作成したり、サービスの他の API を利用したりと、何らかの方法でサービスを活用する WordPress プラグインを作った人はいますか ? これらのプラグインは、使用状況や需要を示すような注目すべき採用実績や活発さがありますか ?
*   そのプロバイダは頻繁に提案されていますか ?

<!--
Individually, these are all very anecdotal. But when considered holistically, it paints a pretty decent picture.
-->

個別に見れば、これらはすべて裏付けが乏しいものかもしれません。しかし総合的に考えると、理にかなっているでしょう。

<!--
## Unfiltered HTML for editors, administrators; multisite
-->

## 編集者、管理者向けのフィルタリングされていない HTML とマルチサイト

<!--
Users with Administrator or Editor roles are allowed to publish unfiltered HTML in post titles, post content, and comments. WordPress is, after all, a publishing tool, and people need to be able to include whatever markup they need to communicate. Users with lesser privileges are not allowed to post unfiltered content.
-->

管理者または編集者権限を持つユーザーは、投稿タイトル、投稿コンテンツ、およびコメントにフィルタリングされていない HTML を公開することが許可されています。WordPress は、結局のところパブリッシングツールであり、人々はコミュニケーションに必要なあらゆるマークアップを含めることができるようにする必要があります。より低い権限を持つユーザーは、フィルタリングされていないコンテンツを投稿できません。

<!--
If you are running security tests against WordPress, use a lesser privileged user so that all content is filtered. You may report security issues to security@wordpress.org. For more, see [Reporting Security Vulnerabilities](https://make.wordpress.org/core/handbook/reporting-security-vulnerabilities/).
-->

WordPress に対してセキュリティテストを行う場合は、より低い権限のユーザーを使用して、すべてのコンテンツがフィルタリングされるようにしてください。セキュリティに関する問題は、security@wordpress.org に報告できます。詳しくは、[セキュリティ脆弱性の報告](https://ja.wordpress.org/team/handbook/core/reporting-security-vulnerabilities/)をご覧ください。

<!--
If you are concerned about an Administrator putting XSS into content and stealing cookies, note that all cookies are marked for HTTP only delivery and are divided into privileged cookies used for admin pages and lesser-privileged cookies used for public-facing pages. Content is never displayed unfiltered in the admin. Regardless, an Administrator has wide-ranging super powers among which unfiltered HTML is a lesser one.
-->

管理者がコンテンツに XSS を入れたり、Cookie を盗んだりすることを心配するかもしれませんが、すべての Cookie は HTTP のみの配信にマークされており、管理者ページで使われる特権的な Cookie と一般向けのページで使われるより低い特権的な Cookie に分けられています。管理画面では、コンテンツがフィルタリングされずに表示されることはありません。とはいえ、管理者には幅広い権限があり、フィルタリングされていない HTML はそのうちの一つです。

<!--
In WordPress multisite, only super administrators can publish unfiltered HTML, as all other users are considered untrusted.
-->

WordPress のマルチサイトでは、特権管理者のみがフィルタリングされていない HTML を公開ができ、それ以外のユーザーは信頼されていないとみなされます。

<!--
To disable unfiltered HTML for all users, including administrators and super administrators, you can add `define( 'DISALLOW_UNFILTERED_HTML', true );` to `wp-config.php`.
-->

管理者や特権管理者を含むすべてのユーザーに対してフィルタリングされていない HTML を無効にするには、`wp-config.php` に `define( 'DISALLOW_UNFILTERED_HTML', true );` を追加してください。

<!--
## Only owner-writeable is supported on upgrade, not group writeable
-->

## アップグレード時にサポートされるのはオーナー書き込み可能なもののみで、グループ書き込み可能なものはサポートされません

<!--
See [#10205](https://core.trac.wordpress.org/ticket/10205).
-->

[#10205](https://core.trac.wordpress.org/ticket/10205)を参照してください。

<!--
## Some esoteric MySQL settings are not supported
-->

## 一部の複雑な MySQL 設定はサポ―トしていません

<!--
WordPress does not support MySQL strict mode or autocommit = 0. [#8857](https://core.trac.wordpress.org/ticket/8857), [#16821](https://core.trac.wordpress.org/ticket/16821), [#16429](https://core.trac.wordpress.org/ticket/16429).
-->

WordPress は、MySQL の strict モードや autocommit = 0 をサポートしていません。[#8857](https://core.trac.wordpress.org/ticket/8857)、[#16821](https://core.trac.wordpress.org/ticket/16821)、[#16429](https://core.trac.wordpress.org/ticket/16429)。
