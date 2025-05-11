<!--
# Glossary
-->

# 用語集

<!--
dl.glossary-list dd { margin-top: -50px; padding-top: 50px; }
-->

<!--
**a11y**
-->

## a11y

<!--
Accessibility, or the act of ensuring a high quality experience for all users regardless of blindness and low vision, deafness and hearing loss, learning disabilities, cognitive limitations, limited movement, speech disabilities, photosensitivity and combinations of these. [#](https://make.wordpress.org/core/handbook/glossary/#a11y)
-->

Accessibility の短縮形。アクセシビリティ。視覚障害や弱視、聴覚障害や難聴、学習障害、認知障害、運動障害、言語障害、光線過敏症、およびこれらの組み合わせにかかわらず、すべての利用者に質の高い体験を保証する行為。

<!--
**admin**
-->

## admin

<!--
(and super admin) [#](https://make.wordpress.org/core/handbook/glossary/#admin)
-->

管理者。なおマルチサイトネットワークの特権管理者は Super Admin。

<!--
**alpha (beta)**
-->

## alpha (beta) / アルファ (ベータ)

<!--
Pre-release version of software intended to signal desire for compatibility, functional, and unit tests and feedback. Also see [release candidate](#release-candidate). [#](https://make.wordpress.org/core/handbook/glossary/#alpha-beta)
-->

互換性テスト、機能テスト、ユニットテスト、フィードバックを求めることを目的とした、ソフトウェアのプレリリースバージョン。[release candidate](#release-candidate-%e3%83%aa%e3%83%aa%e3%83%bc%e3%82%b9%e5%80%99%e8%a3%9c) も参照してください。

<!--
**back compat**
-->

## back compat / 後方互換

<!--
Backward compatibility – a desire to ensure that plugins and themes do not break under new releases – is a driving philosophy of WordPress. While it is a commonly accepted software development practice to break compatibility in major releases, WordPress strives to avoid this at all costs. Any backward incompatible change is carefully considered by the entire core development team and announced, with affected plugins often contacted. It should be noted that external libraries, such as jQuery, do have backward incompatible changes between major releases, which is often going to be a greater concern for developers. [#](https://make.wordpress.org/core/handbook/glossary/#back-compat)
-->

Backward compatibility の省略形。後方互換性 (プラグインやテーマが新しいリリースで壊れないようにしたいという願望) は、WordPress の原動力となっている理念です。メジャーリリースで互換性を壊すことはソフトウェア開発の慣行として一般的に受け入れられていますが、WordPress はこれを何としても回避するよう努めています。後方互換性のない変更はすべて、コア開発チーム全体によって慎重に検討され、影響を受けるプラグインに頻繁に連絡をとりながら発表されます。jQuery などの外部ライブラリには、メジャーリリース間で後方互換性のない変更があり、これが開発者にとって大きな懸念となることが多いことに注意してください。
<!--
**backport**
-->

## backport / バックポート

<!--
A port is when code from one branch (or trunk) is merged into another branch or trunk. Some changes in WordPress point releases are the result of backporting code from trunk to the release branch. [#](https://make.wordpress.org/core/handbook/glossary/#backport)
-->

ポートとは、1つのブランチ (または trunk) のコードが別のブランチまたは trunk にマージされることです。WordPress ポイントリリースの一部の変更は、コードを trunk からリリースブランチにバックポートした結果です。

<!-- **bleeding edge** -->

## bleeding edge / 最前線

<!--
The latest revision of the software, generally in development and often unstable. Also known as [trunk](#trunk). [#](https://make.wordpress.org/core/handbook/glossary/#bleeding-edge)
-->

ソフトウェアの最新リビジョン。通常は開発中であり、多くの場合不安定です。[trunk](#trunk) とも呼ばれます。

<!--
**blocker**
-->

## blocker / ブロッカー

<!--
A bug which is so severe that it blocks a release. [#](https://make.wordpress.org/core/handbook/glossary/#blocker)
-->

リリースを妨げるほど深刻なバグ。

<!--
**blog**
-->

## blog / ブログ

<!--
(versus network, site) [#](https://make.wordpress.org/core/handbook/glossary/#blog)
-->

マルチサイトの「ネットワーク」や「サイト」に対する、単一の WordPress 環境を指します。

<!--
**branch**
-->

## branch / ブランチ

<!--
A directory in Subversion. WordPress uses branches to store the latest development code for each major release (3.9, 4.0, etc.). Branches are then updated with code for any minor releases of that branch. Sometimes, a major version of WordPress and its minor versions are collectively referred to as a “branch”, such as “the 4.0 branch”. [#](https://make.wordpress.org/core/handbook/glossary/#branch)
-->

Subversion のディレクトリ。WordPress はブランチを使用して、各メジャーリリース (3.9、4.0など) の最新の開発コードを保存します。ブランチは、そのブランチのマイナーリリースのコードで更新されます。WordPress のメジャーバージョンとそのマイナーバージョンをまとめて、そのマイナー バージョンをまとめて「ブランチ」(「4.0ブランチ」など) と呼ぶこともあります。

<!--
**bug**
-->

## bug / バグ

<!--
A bug is an error or unexpected result. Performance improvements, code optimization, and are considered enhancements, not defects. After feature freeze, only bugs are dealt with, with regressions (adverse changes from the previous version) being the highest priority. [#](https://make.wordpress.org/core/handbook/glossary/#bug)
-->

バグとは、エラーや予期しない結果のことです。パフォーマンスの改善やコードの最適化などは、不具合ではなく機能強化とみなされます。機能フリーズの後は、バグのみが扱われ、リグレッション (前バージョンからの望ましくない変更) が最優先されます。

<!--
**command line interface (CLI)**
-->

## command line interface (CLI) / コマンドラインインターフェース (CLI)

<!--
A type of human-computer interface (i.e., a way for humans to interact with computers) that relies solely on textual input and output. The entire display screen, or the currently active portion of it, shows only characters (and no images), and input is usually performed entirely with a keyboard. [#](https://make.wordpress.org/core/handbook/glossary/#command-line-interface)
-->

ヒューマン・コンピューター・インターフェース (人間がコンピューターと対話する方法) の一種で、文字による入出力のみに依存するもの。ディスプレイ画面全体、または現在アクティブな部分には文字のみが表示され (画像は表示されません)、入力は通常すべてキーボードで行われます。

<!--
**commit (noun)**
-->

## commit / コミット (名詞)

<!--
An individual change to WordPress, identified by an incremental revision number. Also called a **changeset**. [#](https://make.wordpress.org/core/handbook/glossary/#commit-noun)
-->

インクリメンタルリビジョン番号で識別される WordPress の個々の変更。**チェンジセット**とも呼ばれます。

<!--
**commit (verb)**
-->

## commit / コミット (動詞)

<!--
To make a change to WordPress. Only committers can commit code, but often the code is *contributed* by developers without commit access. [#](https://make.wordpress.org/core/handbook/glossary/#commit-verb)
-->

WordPress に変更を加えること。コードをコミットできるのはコミッターだけですが、多くの場合、コミット権限のない開発者がコードに**貢献**しています。

<!--
**committer**
-->

## committer / コミッター

<!--
A developer with commit access. WordPress has five lead developers and four permanent core developers with commit access. Additionally, the project usually has a few guest or component committers – a developer receiving commit access, generally for a single release cycle (sometimes renewed) and/or for a specific component. [#](https://make.wordpress.org/core/handbook/glossary/#committer)
-->

コミット権限を持つ開発者。WordPress では、5名のリード開発者と4名のレギュラーコア開発者がコミットアクセス権を持っています。さらに、プロジェクトには通常数人のゲストコミッターやコンポーネントコミッターがいます。開発者は、通常単一のリリースサイクル (更新される場合もあります) および/または特定のコンポーネントに対してコミット権限を持ちます。

<!--
**conflict**
-->

## conflict / コンフリクト

<!--
A conflict occurs when a patch changes code that was modified after the patch was created. These patches are considered *stale*, and will require a *refresh* of the changes before it can be applied, or the conflicts will need to be *resolved*. [#](https://make.wordpress.org/core/handbook/glossary/#conflict)
-->

コンフリクトは、パッチが作成された後に変更されたコードをパッチが変更したときに発生します。これらのパッチは「古い」とみなされ、適用する前に変更を「更新」するか競合を「解決」する必要があります。

<!--
**copyright license**
-->

## copyright license / 著作権ライセンス

<!--
Copyright holders may grant a license with various allowances including the ability to modify or distribute the copyrighted material. Also see [GPL](#gpl). [#](https://make.wordpress.org/core/handbook/glossary/#copyright-license)
-->

著作権所有者は、著作権で保護された素材を変更または配布する権限を含む、さまざまな許可を与えてライセンスを付与する場合があります。[GPL](#gpl) も参照してください。

<!--
**CRUD**
-->

## CRUD

<!--
Create, read, update and delete, the four basic functions of storing data. (More on [Wikipedia](http://en.wikipedia.org/wiki/Create,_read,_update_and_delete).) [#](https://make.wordpress.org/core/handbook/glossary/#crud)
-->

データを保存する4つの基本機能である、作成 (Create)、読み取り (Read)、更新 (Update)、削除 (Delete) の先頭文字を取ったもの。(詳細については、[Wikipedia](http://en.wikipedia.org/wiki/Create,_read,_update_and_delete) を参照してください)

<!--
**CSS**
-->

## CSS

<!--
Cascading Style Sheets. [#](https://make.wordpress.org/core/handbook/glossary/#css)
-->

カスケーディングスタイルシート。

<!--
**dev note**
-->

<<<<<<< HEAD
Each important change in WordPress Core is documented in a developers note, (usually called dev note). Good dev notes generally include a description of the change, the decision that led to this change, and a description of how developers are supposed to work with that change. Dev notes are published on Make/Core blog during the beta phase of WordPress release cycle. Publishing dev notes is particularly important when plugin/theme authors and WordPress developers need to be aware of those changes.In general, all dev notes are compiled into a Field Guide at the beginning of the release candidate phase. [#](https://make.wordpress.org/core/handbook/glossary/#dev-note)
=======
## dev note / 開発者ノート

<!--
Each important change in WordPress Core is documented in a developers note, (usually called dev note). Good dev notes generally include a description of the change, the decision that led to this change, and a description of how developers are supposed to work with that change. Dev notes are published on Make/Core blog during the beta phase of WordPress release cycle. Publishing dev notes is particularly important when plugin/theme authors and WordPress developers need to be aware of those changes.In general, all dev notes are compiled into a Field Guide at the beginning of the release candidate phase. [#](https://make.wordpress.org/core/handbook/glossary/#dev-note)
-->

Developer Note の省略形。開発者ノート。WordPress コアの重要な変更点はすべて、開発者ノートにドキュメント化されます。優れた開発者ノートには一般的に、変更点、その変更に至った決定、開発者がその変更点をどのように取り組むべきかについての説明が書かれています。開発者ノートは WordPress のリリースサイクルのベータフェーズで Make/Core ブログで公開されます。開発者ノートの公開は、プラグイン/テーマの作者や WordPress の開発者がそれらの変更を認識する必要がある場合に特に重要です。一般的に、すべての開発者ノートはリリース候補フェーズの最初にフィールドガイドにまとめられます。
>>>>>>> main

<!--
**docblock**
-->

## docblock

<!--
(phpdoc, xref, inline docs) [#](https://make.wordpress.org/core/handbook/glossary/#docblock)
-->

(phpdoc, xref, インラインドキュメントとも)

<!--
**dogfood**
-->

## dogfood / ドッグフード

<!--
The practice of using one’s own software, typically bleeding edge (trunk), thus “eating one’s own dogfood”. This also applies to using one’s own APIs internally. [#](https://make.wordpress.org/core/handbook/glossary/#dogfood)
-->

自身のソフトウェアを使用する習慣。通常は最先端 (trunk) であり、したがって「自分自身のドッグフードを食べる」ことを指します。これは、独自の API を内部で使用する場合にも当てはまります。

<!--
**enhancement**
-->

## enhancement / 機能強化

<!--
Enhancements are simple improvements to WordPress, such as the addition of a hook, a new feature, or an improvement to an existing feature. [#](https://make.wordpress.org/core/handbook/glossary/#enhancement)
-->

機能強化とは、フックの追加、新機能の追加、既存機能の改善など、WordPress の単純な改良です。

<!--
**feature request**
-->

## feature request / 機能リクエスト

<!--
A feature request should generally begin the process in the ideas forum, on a mailing list, as a plugin, or brought to the attention of the core team, such as through scope meetings held for each major release. Unsolicited tickets of this variety are typically, therefore, discouraged. [#](https://make.wordpress.org/core/handbook/glossary/#feature-request)
-->

機能リクエストは通常、アイデア フォーラムやメーリングリスト、プラグインとしてプロセスを開始するか、メジャーリリースごとに開催されるスコープミーティングなどを通じてコアチームに通知される必要があります。そのため、このような種類の一方的なチケットは、一般的に推奨されません。

<!--
**Field guide**
-->

## Field guide / フィールドガイド

<!--
The field guide is a type of blogpost published on Make/Core during the release candidate phase of the [WordPress release cycle](https://make.wordpress.org/core/handbook/about/release-cycle/). The field guide generally lists all the dev notes published during the beta cycle. This guide is linked in the about page of the corresponding version of WordPress, in the release post and in the HelpHub version page. [#](https://make.wordpress.org/core/handbook/glossary/#field-guide)
-->

フィールドガイドは、[WordPress リリースサイクル](https://ja.wordpress.org/team/handbook/core/about/release-cycle/)のリリース候補フェーズに Make/Core で公開されるブログ記事の一種です。フィールドガイドには通常、ベータサイクル中に公開されたすべての開発者ノートが含まれています。このガイドは、WordPress の対応するバージョンのアバウトページ、リリース投稿、HelpHub のバージョンページにリンクされています。

<!--
**GPL**
-->

## GPL

<!--
GNU General Public License. Also see [copyright license](#copyright-license). [#](https://make.wordpress.org/core/handbook/glossary/#gpl)
-->

GNU General Public License の略語。GNU 一般公的使用許諾。[copyright license](#copyright-license-%e8%91%97%e4%bd%9c%e6%a8%a9%e3%83%a9%e3%82%a4%e3%82%bb%e3%83%b3%e3%82%b9) も参照してください。

<!--
**hacked**
-->

<!--
[#](https://make.wordpress.org/core/handbook/glossary/#hacked)
-->

<!--
**HTML**
-->

## HTML

<!--
HyperText Markup Language. The semantic scripting language primarily used for outputting content in web browsers. [#](https://make.wordpress.org/core/handbook/glossary/#html)
-->

ハイパーテキスト・マークアップ・ランゲージ。主に Web ブラウザでコンテンツを出力するために使用されるセマンティックスクリプト言語。

<!--
**i18n**
-->

## i18n

<!--
Internationalization, or the act of writing and preparing code to be fully translatable into other languages. Also see [localization](#l10n). Often written with a lowercase i so it is not confused with a lowercase L or the numeral 1. Often an acquired skill. [#](https://make.wordpress.org/core/handbook/glossary/#i18n)
-->

Internationalization の短縮形。国際化。他の言語に完全に翻訳できるようにコードを書いたり準備したりする行為のこと。[localization](#l10n) も参照してください。小文字の L や数字の1と混同しないように、小文字の i で表記されます。一般に獲得するスキルです。

<!--
**IDE**
-->

## IDE

<!--
Integrated Development Environment. A software package that provides a full suite of functionality to software developers/programmers. Normally an IDE includes a source code editor, code-build tools and debugging functionality. [#](https://make.wordpress.org/core/handbook/glossary/#ide)
-->

Integrated Development Environment の略語。統合開発環境。ソフトウェア開発者やプログラマーに一連の機能を提供するソフトウェアパッケージ。通常、IDE にはソースコードエディター、コード構築ツール、デバッグ機能が含まれます。

<!--
**inline docs**
-->

## inline docs / インラインドキュメント

<!--
(phpdoc, docblock, xref) [#](https://make.wordpress.org/core/handbook/glossary/#inline-docs)
-->

(phpdoc, docblock, xref とも)

<!--
**invalid**
-->

## invalid

<!--
A resolution on the bug tracker (and generally common in software development, sometimes also *notabug*) that indicates the ticket is not a bug, is a support request, or is generally invalid. [#](https://make.wordpress.org/core/handbook/glossary/#invalid)
-->

チケットがバグではないこと、サポートリクエストであること、または一般的に無効であることを示す、バグトラッカーの解決策 (ソフトウェア開発では一般的で、**notabug** とも呼ばれます)。

<!--
**IRC**
-->

<<<<<<< HEAD
Internet Relay Chat, a network where users can have conversations online. IRC channels are used widely by open source projects, and by WordPress. The primary WordPress channels are **[#wordpress](https://make.wordpress.org/core/tag/wordpress/)** and **[#wordpress-dev](https://make.wordpress.org/core/tag/wordpress-dev/)**, on irc.freenode.net. [#](https://make.wordpress.org/core/handbook/glossary/#irc)
=======
## IRC

<!--
Internet Relay Chat, a network where users can have conversations online. IRC channels are used widely by open source projects, and by WordPress. The primary WordPress channels are **[#wordpress](https://make.wordpress.org/core/tag/wordpress/)** and **[#wordpress](https://make.wordpress.org/core/tag/wordpress/)\-dev**, on irc.freenode.net. [#](https://make.wordpress.org/core/handbook/glossary/#irc)
-->
>>>>>>> main

インターネット・リレー・チャット。ユーザーがオンラインで会話できるネットワーク。IRC チャンネルは、オープンソースプロジェクトや WordPress で広く使用されています。主要な WordPress チャンネルは、irc.freenode.net 上の **[#wordpress](https://make.wordpress.org/core/tag/wordpress/)** と **[#wordpress](https://make.wordpress.org/core)\-dev** です。

<!--
**JS**
-->

## JS

<!--
JavaScript, a web scripting language typically executed in the browser. Often used for advanced user interfaces and behaviors. [#](https://make.wordpress.org/core/handbook/glossary/#js)
-->

JavaScript の略語。通常はブラウザで実行される Web スクリプト言語。高度なユーザーインターフェースや動作によく使用されます。

<!--
**L10n**
-->

## L10n

<!--
Localization, or the act of translating code into one’s own language. Also see [internationalization](#i18n). Often written with an uppercase L so it is not confused with the capital letter i or the numeral 1. WordPress has a capable and dynamic group of polyglots who take WordPress to more than 70 different locales. [#](https://make.wordpress.org/core/handbook/glossary/#l10n)
-->

Localization の省略形。ローカライゼーション。コードを自分の言語に翻訳する行為。[internationalization](#i18n) も参照してください。大文字の i や数字の1と混同しないように、しばしば大文字の L で表記されます。WordPress には、WordPress を70以上の異なるロケールに対応させている、有能でダイナミックな多言語対応グループがいます。

<!--
**Locale**
-->

## Locale / ロケール

<!--
A locale is a combination of language and regional dialect. Usually locales correspond to countries, as is the case with Portuguese (Portugal) and Portuguese (Brazil). Other examples of locales include Canadian English and U.S. English. [#](https://make.wordpress.org/core/handbook/glossary/#locale)
-->

ロケールとは、言語と方言の組み合わせです。ポルトガル語 (ポルトガル) とポルトガル語 (ブラジル) などのように、通常、ロケールは国に対応しています。その他のロケールの例としては、カナダ英語やアメリカ英語などがあります。

<!--
**major release**
-->

## major release / メジャーリリース

<!--
A release, identified by the first two numbers (3.6), which is the focus of a full release cycle and feature development. WordPress uses decimaling count for major release versions, so 2.8, 2.9, 3.0, and 3.1 are sequential and comparable in scope. [#](https://make.wordpress.org/core/handbook/glossary/#major-release)
-->

最初の2つの数字 (3.6) で識別されるリリースで、完全なリリースサイクルと機能開発に焦点を当てます。WordPress ではメジャーリリースバージョンに小数点以下のカウントを使用するため、2.8、2.9、3.0、および3.1は連続しており、範囲も同じです。

<!--
**mu-plugins, must-use plugins**
-->

## mu-plugins, must-use plugins

<!--
(include old history as “multi-user”; x-ref with drop-ins) [#](https://make.wordpress.org/core/handbook/glossary/#mu-plugins-must-use-plugins)
-->

(TODO: mu が must use (必須) でなく multi user (マルチユーザー) だった時代背景を加えること。ドロップインと相互参照)

<!--
**multisite**
-->

## マルチサイト

<!--
Used to describe a WordPress installation with a network of multiple blogs, grouped by sites. This installation type has shared users tables, and creates separate database tables for each blog (wp\_posts becomes wp\_0\_posts). See also **network**, **blog**, **site** [#](https://make.wordpress.org/core/handbook/glossary/#multisite)
-->

サイトごとにグループ化された、複数のブログのネットワークを持つ WordPress インストールを説明するために使用されます。このインストールタイプは、共有されたユーザーテーブルを持ち、ブログごとに個別のデータベーステーブルを作成します (wp\_posts は wp\_0\_posts になります)。**network**、**blog**、**site** も参照してください。

<!--
**network**
-->

## network / ネットワーク

<!--
(versus site, blog) [#](https://make.wordpress.org/core/handbook/glossary/#network)
-->

「サイト」や「ブログ」に対する、マルチサイトネットワークを指す。

<!--
**P2**
-->

## P2

<!--
A [free theme for WordPress](http://p2theme.com/), known for front-end posting, used by WordPress for development updates and project management. See our [main development blog](https://make.wordpress.org/core/) and [other workgroup blogs](https://make.wordpress.org/). [#](https://make.wordpress.org/core/handbook/glossary/#p2)
-->

フロントエンドの投稿で知られる [WordPress 用の無料テーマ](http://p2theme.com/)で、WordPress による開発の更新やプロジェクト管理に使用されています。[メインの開発ブログ](https://make.wordpress.org/core/)と[その他のワークグループブログ](https://make.wordpress.org/)を参照してください。

<!--
**patch**
-->

## patch / パッチ

<!--
A special text file that describes changes to code, by identifying the files and lines which are added, removed, and altered. It may also be referred to as a **diff**. A patch can be *applied* to a codebase for testing. [#](https://make.wordpress.org/core/handbook/glossary/#patch)
-->

追加、削除、変更されたファイルや行を特定することで、コードの変更を記述する特別なテキストファイル。**diff** と呼ばれることもあります。パッチは、テストのためにコードベースに適用できます。

<!--
**PHP**
-->

<<<<<<< HEAD
The web scripting language in which WordPress is primarily architected. WordPress requires PHP 7.4 or higher [#](https://make.wordpress.org/core/handbook/glossary/#php)
=======
## PHP

<!--
The web scripting language in which WordPress is primarily architected. WordPress requires PHP 5.6.20 or higher [#](https://make.wordpress.org/core/handbook/glossary/#php)
-->
>>>>>>> main

WordPress が主に設計されている Web スクリプト言語。WordPress には PHP 7.0以上が必要です。

<!--
**PHPDoc**
-->

## PHPDoc

<!--
(**docblock**, **inline docs**) [#](https://make.wordpress.org/core/handbook/glossary/#phpdoc)
-->

(**docblock**, **インラインドキュメントとも**)

<!--
**point release**
-->

## point release / ポイントリリース

<!--
A minor release of WordPress, identified by the third number (the 2 in 3.5.2). These releases are for maintenance and security fixes only. Feature development is limited to major releases. Changes to point releases are carefully considered, and only critical or blocker\-level bugs, and security enhancements, hardening, and fixes are accepted. [#](https://make.wordpress.org/core/handbook/glossary/#point-release)
-->

WordPress のマイナーリリースで、3番目の番号 (3.5.2の2) で識別されます。これらのリリースはメンテナンスとセキュリティの修正のみです。機能開発はメジャーリリースに限定されます。ポイントリリースへの変更は慎重に検討され、重大なバグまたはブロッカーレベルのバグ、セキュリティの強化、堅牢化、修正のみが受け入れられます。

<!--
**priority (bug tracker)**
-->

## priority (bug tracker) / 優先度 (バグトラッカー)

<!--
The seriousness of a bug report or ticket in the eyes of the project. Generally, **severity** is a judgment of how bad a bug is, while priority is its relationship to other bugs. [#](https://make.wordpress.org/core/handbook/glossary/#priority-bug-tracker)
-->

プロジェクトから見たバグレポートやチケットの深刻さ。一般的に、**重要度**はバグがどの程度深刻であるかを判断するためのものであり、優先度は他のバグとの関係です。

<!--
**priority (hooks)**
-->

## priority (hooks) / 優先度 (フック)

<!--
(higher priority means lower number) [#](https://make.wordpress.org/core/handbook/glossary/#priority-hooks)
-->

(優先度が高いほど番号が小さいことを意味します)

<!--
**punt**
-->

## punt

<!--
Contributors sometimes use the verb “punt” when talking about a ticket. This means it is being pushed out to a future release. This typically occurs for lower priority tickets near the end of the release cycle that don’t “make the cut.” In this is colloquial usage of the word, it means to delay or equivocate. (It also describes a play in American football where a team essentially passes up on an opportunity, hoping to put themselves in a better position later to try again.) [#](https://make.wordpress.org/core/handbook/glossary/#punt)
-->

チケットについて話すとき、貢献者は「punt」という動詞を使うことがあります。これは、将来のリリースにプッシュされることを意味します。これは一般的に、リリースサイクルの終わりに近い優先度の低いチケットで、「基準を満たさなかった」場合に起こります。これは口語的な用法で、「遅らせる」「あいまいにする」という意味です。(またアメリカンフットボールでは、攻撃の機会を諦め、次のディフェンスのために陣地を挽回するプレイも意味します)。

<!--
**RC**
-->

## RC

<!--
A shortened name for [release candidate](https://make.wordpress.org/core/handbook/glossary/#release-candidate). [#](https://make.wordpress.org/core/handbook/glossary/#rc)
-->

[release candidate](#release-candidate-%e3%83%aa%e3%83%aa%e3%83%bc%e3%82%b9%e5%80%99%e8%a3%9c) の短縮形。

<!--
**regression**
-->

## regression / リグレッション

<!--
A software bug that breaks or degrades something that previously worked. Regressions are often treated as critical bugs or [blockers](#blocker). Recent regressions may be given higher priorities. A “3.6 regression” would be a bug in 3.6 that worked as intended in 3.5. [#](https://make.wordpress.org/core/handbook/glossary/#regression)
-->

以前は動作していたものを壊したり、機能を低下させたりするソフトウェアのバグ。リグレッションはしばしば重大なバグや[ブロッカー](#blocker-%e3%83%96%e3%83%ad%e3%83%83%e3%82%ab%e3%83%bc)として扱われます。新しいリグレッションは、より高い優先順位が与えられることがあります。「3.6のリグレッション」は、3.5で意図したとおりに動作していた3.6のバグのことです。

<!--
**release candidate**
-->

## release candidate / リリース候補

<!--
One of the final stages in the version release cycle, this version signals the potential to be a final release to the public. Also see [alpha (beta)](#alpha-beta). [#](https://make.wordpress.org/core/handbook/glossary/#release-candidate)
-->

バージョンリリースサイクルの最終フェーズの1つで、このバージョンは一般公開される最終リリースとなる可能性を示しています。[alpha (beta)](#alpha-beta-%e3%82%a2%e3%83%ab%e3%83%95%e3%82%a1-%e3%83%99%e3%83%bc%e3%82%bf) も参照してください。

<!--
**scope creep**
-->

## scope creep / スコープクリープ

<!--
The tendency for requirements to increase during a release’s development cycle beyond those originally approved for the upcoming release. Something to be avoided. Also known as feature creep. [#](https://make.wordpress.org/core/handbook/glossary/#scope-creep)
-->

リリースの開発サイクル中に、次のリリースで当初承認された要件を超えて要件が増加する傾向のことであり、避けるべきもの。フィーチャークリープとも呼ばれます。

<!--
**security issue**
-->

## security issue / セキュリティの問題

<!--
A security issue is a type of bug that can affect the security of WordPress installations. Specifically, it is a report of a bug that you have found in the WordPress core code, and that you have determined can be used to gain some level of access to a site running WordPress that you should not have. [#](https://make.wordpress.org/core/handbook/glossary/#security-issue)
-->

セキュリティの問題とは、WordPress インストールのセキュリティに影響を与える一種のバグです。具体的には、WordPress のコアコードにバグを発見し、そのバグを利用して、WordPress が稼働しているサイトに本来アクセスできないはずのアクセスが可能であると判断した場合に報告するものです。

<!--
**severity**
-->

## severity / 重要度

<!--
The seriousness of the ticket in the eyes of the reporter. Generally, severity is a judgment of how bad a bug is, while **priority** is its relationship to other bugs. [#](https://make.wordpress.org/core/handbook/glossary/#severity)
-->

報告者から見たチケットの重要度。一般的に、重要度はバグがどの程度深刻であるかを判断するためのものであり、**優先度** は他のバグとの関係です。

<!--
**SSL**
-->

## SSL

<!--
Secure Sockets Layer. Provides a secure means of sending data over the internet. Used for authenticated and private actions. [#](https://make.wordpress.org/core/handbook/glossary/#ssl)
-->

セキュア・ソケット・レイヤー。インターネット上でデータを送信する安全な手段を提供します。認証されたプライベートなアクションに使用されます。

<!--
**SVN**
-->

## SVN

<!--
Subversion, the popular version control system (VCS) by the Apache project, used by WordPress to manage changes to its codebase. [#](https://make.wordpress.org/core/handbook/glossary/#svn)
-->

Subversion の省略形。Apache プロジェクトによる一般的なバージョン管理システム (VCS) で、WordPress がコードベースの変更を管理するために使用されています。

<!--
**tag**
-->

## tag / タグ

<!--
A directory in Subversion. WordPress uses tags to store a single snapshot of a version (3.6, 3.6.1, etc.), the common convention of tags in version control systems. (Not to be confused with post tags.) [#](https://make.wordpress.org/core/handbook/glossary/#tag)
-->

Subversion のディレクトリ。WordPress はタグを使用して、バージョン (3.6、3.6.1など) の単一のスナップショットを保存します。これは、バージョン管理システムのタグの一般的な規則です (投稿タグと混同しないでください)。

<!--
**task (blessed)**
-->

## task (blessed) / タスク (blessed)

<!--
Feature development for an upcoming major release centers around task tickets, which are major features or important enhancements that have been blessed by the core team. A ticket should otherwise never receive this designation. [#](https://make.wordpress.org/core/handbook/glossary/#task-blessed)
-->

次のメジャーリリースのための機能開発は、コアチームによって受け入れられた主要な機能または重要な機能強化であるタスクチケットを中心に行われます。それ以外のチケットは、この指定を受けるべきではありません。

<!--
**ticket**
 -->

## ticket / チケット

<!--
Created for both bug reports and feature development on the bug tracker. [#](https://make.wordpress.org/core/handbook/glossary/#ticket)
-->

バグトラッカーで、バグレポートと機能開発の両方のために作成されます。

<!--
**Trac**
-->

## Trac

<!--
An open source project by Edgewall Software that serves as a bug tracker and project management tool for WordPress. [#](https://make.wordpress.org/core/handbook/glossary/#trac)
-->

Edgewall ソフトウェアによるオープンソースプロジェクトで、WordPress のバグトラッカーおよびプロジェクト管理ツールとして機能します。

<!--
**translation**
-->

## translation / 翻訳

<!--
The process (or result) of changing text, words, and display formatting to support another language. Also see [localization](#l10n), [internationalization](#i18n). [#](https://make.wordpress.org/core/handbook/glossary/#translation)
-->

別の言語をサポートするために、テキスト、単語、表示形式を変更するプロセス (または結果)。[localization](#l10n)、[internationalization](#i18n) も参照してください。

<!--
**triage**
-->

## triage / トリアージ

<!--
The act of evaluating and sorting bug reports, in order to decide priority, severity, and other factors. [#](https://make.wordpress.org/core/handbook/glossary/#triage)
-->

優先順位、重要度、その他の要素を決定するために、バグレポートを評価および分類すること。

<!--
**trunk**
-->

## trunk

<!--
A directory in Subversion containing the latest development code in preparation for the next major release cycle. If you are running “trunk”, then you are on the latest revision. [#](https://make.wordpress.org/core/handbook/glossary/#trunk)
-->

次のメジャーリリースサイクルに備えて、最新の開発コードを含む Subversion のディレクトリ。「trunk」を実行している場合は、最新リビジョンを使用しています。

<!--
**UI**
-->

## UI

<!--
User interface [#](https://make.wordpress.org/core/handbook/glossary/#ui)
-->

ユーザーインターフェース

<!--
**unit test**
-->

## unit test / ユニットテスト

<!--
Code written to test a small piece of code or functionality within a larger application. Everything from themes to WordPress core have a series of unit tests. Also see [regression](#regression). [#](https://make.wordpress.org/core/handbook/glossary/#unit-test)
-->

大規模のアプリケーションの中の小さなコードや機能をテストするために書かれたコード。テーマから WordPress のコアに至るまで、あらゆるものが一連のユニットテストを持っています。[regression](#regression-%e3%83%aa%e3%82%b0%e3%83%ac%e3%83%83%e3%82%b7%e3%83%a7%e3%83%b3) も参照してください。

<!--
**Unprops**
-->

## Unprops

<!--
A commit that removes code gone awry may include *unprops* as a sign of respect for the risk taken by the original people working on it. [#](https://make.wordpress.org/core/handbook/glossary/#unprops)
-->

失敗したコードを削除するコミットには、元々そのコードに取り組んでいた人たちが取ったリスクを尊重するため、「unprops」を含めることがあります。

<!--
**UX**
-->

## UX

<!--
User experience [#](https://make.wordpress.org/core/handbook/glossary/#ux)
-->

User Experience の省略形。ユーザー体験。

<!--
**version control**
-->

## version control / バージョン管理

<!--
A version control system keeps track of the source code and revisions to the source code. WordPress uses Subversion (SVN) for version control, with Git mirrors for most repositories. [#](https://make.wordpress.org/core/handbook/glossary/#version-control)
-->

バージョン管理システムは、ソースコードとソースコードのリビジョンを追跡します。WordPress はバージョン管理に Subversion (SVN) を使用し、ほとんどのリポジトリに Git ミラーを使用しています。

<!--
**wontfix**
-->

## wontfix

<!--
A resolution on the bug tracker (and generally common in software development) that indicates the ticket will not be addressed further. This may be used for acceptable edge cases (for bugs), or enhancements that have been rejected for core inclusion. [#](https://make.wordpress.org/core/handbook/glossary/#wontfix)
-->

チケットがこれ以上対処されないことを示す、バグトラッカーの解決策 (ソフトウェア開発では一般的です)。これは、(バグなどの) 許容可能なエッジケース、またはコアへの組込みが拒否された拡張機能に使用される場合があります。

<!--
**worksforme**
-->

## worksforme

<!--
A resolution on the bug tracker (and generally common in software development) that indicates the bug reported cannot be reproduced. [#](https://make.wordpress.org/core/handbook/glossary/#worksforme)
-->

報告されたバグが再現できないことを示す、バグトラッカーの解決策 (ソフトウェア開発では一般的です)。

<!--
**wpdevel**
-->

## wpdevel

<!--
Formerly the development updates P2 blog at wpdevel.wordpress.com. It is now **make/core** and resides at [make.wordpress.org/core](https://make.wordpress.org/core/). [#](https://make.wordpress.org/core/handbook/glossary/#wpdevel)
-->

以前は、開発者が wpdevel.wordpress.com で P2ブログを更新していました。現在は **make/core** で、[make.wordpress.org/core](https://make.wordpress.org/core/) にあります。

<!--
**xref**
-->

## xref

<!--
(php-xref, phpdoc, inline docs) [#](https://make.wordpress.org/core/handbook/glossary/#xref)
-->

(php-xref, phpdoc, インラインドキュメントとも)
