<!--
# The Code Repository (SVN)
-->

# コードリポジトリ (SVN)

<!--
Alert: WordPress supports patches being created from both [GIT](https://make.wordpress.org/core/handbook/contribute/git/) and SVN. This documentation focuses on the SVN option.
-->

注: WordPress は、 [GIT](https://make.wordpress.org/core/handbook/contribute/git/) と SVN の両方から作成されるパッチをサポートしています。このドキュメントは、Git オプションにフォーカスしています。

<!--
## What is SVN?
-->

## SVN とは

<!--
WordPress uses [Subversion (SVN)](https://make.wordpress.org/core/glossary/#svn), a very popular version control system managed by the Apache project, to manage changes to its codebase. A change to the WordPress codebase increments the **revision** number. Individual changes are called [commits or changesets](https://make.wordpress.org/core/glossary/#commit-noun). These are denoted as either [r12345](https://core.trac.wordpress.org/changeset/12345) or \[[12345](https://core.trac.wordpress.org/changeset/12345)\]. Details of the SVN and Git repositories are located [here](https://make.wordpress.org/core/handbook/contribute/codebase/).
-->

WordPress は、Apache プロジェクトが管理する非常に一般的なバージョン管理システムである [Subversion (SVN)](https://make.wordpress.org/core/glossary/#svn) を使用して、コードベースへの変更を管理しています。WordPress のコードベースへの変更は、**リビジョン**という番号を増加させます。それぞれの変更は [コミットまたはチェンジセット](https://make.wordpress.org/core/glossary/#commit-noun) と呼ばれます。これらは、[r12345](https://core.trac.wordpress.org/changeset/12345) または \[[12345](https://core.trac.wordpress.org/changeset/12345)\] のように表記されます。SVN と Git のリポジトリの詳細は[こちら]((https://make.wordpress.org/core/handbook/contribute/codebase/))です。

<!--
The WordPress repository of code is organized into three main directories: [tags](https://make.wordpress.org/core/glossary/#tag), [branches](https://make.wordpress.org/core/glossary/#branch), and [trunk](https://make.wordpress.org/core/glossary/#trunk).
-->

WordPress のコードのリポジトリは、主に3つのディレクトリで構成されています。[tag](https://make.wordpress.org/core/glossary/#tag)、[branches](https://make.wordpress.org/core/glossary/#branch)、[trunk](https://make.wordpress.org/core/glossary/#trunk) です。

<!--
*   The **trunk** directory contains the latest development code in preparation for the next major release cycle. The latest revision may be unstable or broken at times. The latest development code may be referred to as *trunk*.
*   The **tags** directory contains individual snapshots of each official release, such as the 3.4.0 or 3.5.1 tags. Once created, these are unmodified, and these are used to build the download packages.
*   The **branches** directory contains directories that consist of the latest code for each major release, such as the 3.4 and 3.5 branches. Minor release development occurs within the branch. For example, a critical bug that affects the latest release may be fixed in both trunk and the most recent branch, in preparation for a **point release** – i.e. 3.5.2, in the case of the 3.5 branch. These should generally be considered stable, but care should be taken when a minor release is being prepared.
-->

*   **trunk** ディレクトリには、次のメジャーリリースサイクルに備えて、最新の開発コードが含まれています。最新のリビジョンは、不安定であったり壊れたりすることがあります。最新の開発コードは、*trunk* と呼ばれることがあります。
*   **tags** ディレクトリには、3.4.0や3.5.1のタグのような、各公式リリースの個別のスナップショットが含まれています。一度作成されると、これらは変更されず、ダウンロードパッケージの構築に使用されます。
*   **branches** ディレクトリには、3.4ブランチや3.5ブランチなど、各メジャーリリースの最新コードで構成されるディレクトリがあります。マイナーリリースの開発は、ブランチ内で行われます。たとえば、最新リリースに影響する重大なバグは、**ポイントリリース** に向けて、trunk と最新ブランチの両方で修正されることがあります。つまり、3.5ブランチの場合、3.5.2です。これらは一般的に安定版とみなされるべきものですが、マイナーリリースが準備されているときには注意が必要です。

<!--
## Finding an SVN Client
-->

## SVN クライアントを探す

<!--
Most popular IDE (Integrated Developer Environment) applications include built-in support for SVN. Some also include enhanced support for WordPress development. This makes it very convenient to perform all source code version control tasks: synchronize, manage local copies, create patches, etc.
-->

一般的な IDE (統合開発環境) アプリケーションの多くは、SVN をビルトインでサポートしています。また、WordPress の開発用にサポートが強化されているものもあります。これにより、同期、ローカルコピーの管理、パッチの作成など、あらゆるソースコードのバージョン管理作業を行うことができ、非常に便利になります。

<!--
Alternatively some developers run SVN commands using the [command line interface](https://make.wordpress.org/core/glossary/#command-line-interface) (CLI), such as [Terminal](http://en.wikipedia.org/wiki/Terminal_(OS_X)) on the Mac. Even though most basic commands are simple, the command line is reasonably intimidating for many users. Many developers do rely on [GUI](http://en.wikipedia.org/wiki/GUI) applications though, either for regular use, or to handle complex actions more effectively.
-->

あるいは、Mac の [ターミナル](http://en.wikipedia.org/wiki/Terminal_(OS_X)) などの [コマンドラインインターフェース](https://make.wordpress.org/core/glossary/#command-line-interface) (CLI) を使って SVN コマンドを実行する開発者もいます。ほとんどの基本的なコマンドは簡単ですが、コマンドラインは多くのユーザーにとってとっつきにくいものです。しかし、多くの開発者は、通常の使用や複雑な操作をより効果的に行うために、[GUI](http://en.wikipedia.org/wiki/GUI) アプリケーションに頼っています。

<!--
When not using an IDE, or if a stand-alone GUI application is required, for Windows the recommended SVN client is [TortoiseSVN](http://tortoisesvn.net/), which is free and open source.
-->

IDE を使用しない場合、またはスタンドアローンの GUI アプリケーションが必要な場合、Windows では、推奨される SVN クライアントはフリーでオープンソースの [TortoiseSVN](http://tortoisesvn.net/) です。

<!--
For Mac, the recommended SVN client is [Cornerstone](http://www.zennaware.com/cornerstone/), which must be purchased.
-->

Mac の場合、推奨される SVN クライアントは [Cornerstone](http://www.zennaware.com/cornerstone/) で、購入する必要があります。

<!--
## Learn More
-->

## より詳しく

<!--
If you would like to learn more about working with Subversion, check out [Installing A Version Control System](https://make.wordpress.org/core/handbook/tutorials/installing-a-vcs/), [Installing WordPress Via SVN](https://make.wordpress.org/core/handbook/tutorials/installing-wordpress-locally/from-svn/), and [Working With Patches](https://make.wordpress.org/core/handbook/working-with-patches/) in the **Tutorials and Guides** section of this handbook.
-->

Subversion での作業についてもっと知りたい方は、このハンドブックの**チュートリアルとガイド**セクションの[バージョン管理システムのインストール](https://make.wordpress.org/core/handbook/tutorials/installing-a-vcs/)、[SVN による WordPress のインストール](https://make.wordpress.org/core/handbook/tutorials/installing-wordpress-locally/from-svn/)、[パッチでの作業](https://make.wordpress.org/core/handbook/working-with-patches/)をご覧ください。
