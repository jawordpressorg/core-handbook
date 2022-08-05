<!-- 
# Core Contributor Handbook
 -->
# コアコントリビューターハンドブック

<!-- 
Welcome to the Core Contributor Handbook, the place to learn how to get involved with the WordPress core development community, and start contributing to WordPress core.
 -->
コアコントリビューターハンドブックへようこそ。ここはコア開発コミュニティに参加し、WordPress コアへの貢献を開始する方法を学ぶ場です。

<!-- 
Whether you are a beta tester, casual contributor, or serious contributor, this handbook will provide the information you need to get started.
 -->
あなたがベータテスターであっても、カジュアルな貢献者であっても、本格的な貢献者であっても、このハンドブックは、あなたが始めるために必要な情報を提供します。

<!-- 
Here you can learn about how the WordPress project is organized, communication channels, best practices, the Trac workflow process, and more. There are also guides to help you set up the tools you’ll need to start contributing to WordPress core.
 -->
ここでは、WordPress プロジェクトがどのように組織されているか、コミュニケーションチャネル、ベストプラクティス、Trac のワークフロープロセスなどについて学ぶことができます。また、WordPress コアへの貢献を開始するために必要なツールのセットアップを支援するガイドもあります。

<!-- ## Contribute with Testing -->
## テストでコントビュートする

<!-- Testing is a very important part of the release cycle. You can install the latest development version locally to test new features, and how the changes work with your site setup (theme/plugins/etc.). You can [start testing](https://make.wordpress.org/core/handbook/testing/) as soon as a new development version is available (alpha), and continue throughout the release cycle to ensure the next version of WordPress is as bug\-free as possible. -->
テストは、リリースサイクルの非常に重要な部分です。最新の開発版をローカルにインストールし、新機能や、サイトの設定 (テーマ/プラグイン/その他) での変更点の動作をテストすることができます。新しい開発版 (アルファ版) が利用可能になるとすぐに [テストを開始](https://make.wordpress.org/core/handbook/testing/) することができ、次のバージョンの WordPress ができるだけバグがないことを保証するためにリリースサイクル全体を通して継続します。

<!-- You don’t need to know how to code or create a patch, just provide a [well-written bug report](https://make.wordpress.org/core/handbook/testing/reporting-bugs/), with details of the issue and steps to reproduce. You can confirm the issue is fixed once a patch is committed and a new bleeding edge nightly version released. -->
コーディングやパッチの作成方法を知っている必要はありません。問題の詳細と再現手順を記載した [well-written bug report](https://make.wordpress.org/core/handbook/testing/reporting-bugs/) を提供してください。パッチがコミットされ、新しい最先端のナイトリーバージョンがリリースされた時点で、問題が修正されたことを確認できます。

<!-- Found a security vulnerability? WordPress believes in responsible and private disclosure. [Report it directly to our security team.](https://make.wordpress.org/core/handbook/testing/reporting-security-vulnerabilities/) -->
セキュリティの脆弱性を発見されましたか ?WordPress は、責任ある非公開の情報公開を信条としています。[私たちのセキュリティチームに直接報告してください](https://make.wordpress.org/core/handbook/testing/reporting-security-vulnerabilities/)

<!-- 
## Contribute with Code
 -->
## コードで貢献する

<!--
Whether you need to report one bug and provide a patch to fix it, or wish to become involved in maintaining one or more WordPress components, contributing code is a great way to improve WordPress. This section walks through [the WordPress codebase](https://make.wordpress.org/core/handbook/contribute/codebase/) and how it’s laid out, then teaches you more about [the code repository](https://make.wordpress.org/core/handbook/contribute/svn/) and [our bug tracker (Trac)](https://make.wordpress.org/core/handbook/contribute/trac/).
 -->
バグを報告して修正パッチを提供する必要がある場合でも、1つ以上の WordPress コンポーネントのメンテナンスに関与したい場合でも、コードの貢献は WordPress を改善する素晴らしい方法です。
このセクションでは、[WordPress のコードベース](https://make.wordpress.org/core/handbook/contribute/codebase/) とそのレイアウトについて説明し、[コードリポジトリ](https://make.wordpress.org/core/handbook/contribute/svn/) と [Trac](https://make.wordpress.org/core/handbook/contribute/trac/) について詳しく説明します。

<!-- 
[Design decisions](https://make.wordpress.org/core/handbook/contribute/design-decisions/) made within WordPress are often a consideration when contributing code and are outlined in this section as well. Finally, if you’re interested in [fixing bugs](https://make.wordpress.org/core/handbook/contribute/fixing-bugs/), our walkthrough is made to get you quickly started.
 -->
WordPress の[デザインの決定](https://make.wordpress.org/core/handbook/contribute/design-decisions/) は、コードを提供する際にしばしば考慮されることであり、このセクションでも説明されています。最後に、もしあなたが [バグ修正](https://make.wordpress.org/core/handbook/contribute/fixing-bugs/) に興味があるなら、私たちのウォークスルーはあなたがすぐに始められるように作られています。

<!-- 
## Best Practices
 -->
## ベストプラクティス

<!-- 
Over time, the WordPress community has developed some [best practices](https://make.wordpress.org/core/handbook/best-practices/), which keep the code base consistent and understandable by the community.
 -->
時間をかけて、WordPress コミュニティはいくつかの[ベストプラクティス](https://make.wordpress.org/core/handbook/best-practices/)を開発し、コードベースの一貫性とコミュニティの理解力を維持しています。

In the best practices section, we outline the [coding standards](https://make.wordpress.org/core/handbook/best-practices/coding-standards/) for [CSS](https://make.wordpress.org/core/handbook/best-practices/coding-standards/css/), [HTML](https://make.wordpress.org/core/handbook/best-practices/coding-standards/html/), [JavaScript](https://make.wordpress.org/core/handbook/best-practices/coding-standards/javascript/), and [PHP](https://make.wordpress.org/core/handbook/best-practices/coding-standards/php/). Additionally, [inline documentation standards](https://make.wordpress.org/core/handbook/best-practices/inline-documentation-standards/) for both [JavaScript](https://make.wordpress.org/core/handbook/best-practices/inline-documentation-standards/javascript/) and [PHP](https://make.wordpress.org/core/handbook/best-practices/inline-documentation-standards/php/) are documented in-depth.

Finally, the section walks through the [Core APIs](https://make.wordpress.org/core/handbook/best-practices/core-apis/) and the best practices to follow when [writing patches](https://make.wordpress.org/core/handbook/best-practices/writing-patches/).

## Tutorials & Guides

Completely new to WordPress development? In this section, we include a number of [tutorials and guides](https://make.wordpress.org/core/handbook/tutorials/) to help get you setup. Whether you want to [setup WordPress for local development](https://make.wordpress.org/core/handbook/tutorials/installing-wordpress-locally/), [install a local server](https://make.wordpress.org/core/handbook/tutorials/installing-a-local-server/), [install a version control system (VCS)](https://make.wordpress.org/core/handbook/tutorials/installing-a-vcs/), understand how to [work with patches](https://make.wordpress.org/core/handbook/tutorials/working-with-patches/), or better understand how to [work with Trac](https://make.wordpress.org/core/handbook/tutorials/trac/), we have you covered.

## Need help?

We all start somewhere. If you’re having trouble getting involved with contributing to WordPress core, come find us on [Slack](https://chat.wordpress.org/) in [#core](https://make.wordpress.org/core/tag/core/). We don’t bite. 😊

Note: If you’re interested in improving this handbook, leave a message in #coreCore Core is the set of software required to run WordPress. The Core Development Team builds WordPress.\-docs.
