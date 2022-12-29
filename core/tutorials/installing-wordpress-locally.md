<!--
# Installing WordPress Locally
-->

# WordPress をローカルにインストールする

<!--
This section of the handbook contains tutorials that will walk you through the process of installing WordPress locally.
-->

このセクションでは、WordPress をローカルにインストールする手順を説明するチュートリアルが含まれています。

<!--
## Why do I need a local WordPress install?
-->

## なぜ WordPress のローカルインストールが必要なのですか?

<!--
If you want to contribute to WordPress core, you need to have a local install of WordPress on your computer to break, play with, and develop with. A local WordPress install allows you to create/test patches, find/fix bugs, and help develop/test new features during a release cycle.
-->

WordPress コアに貢献したい場合は、開発を行うために、コンピュータに WordPress をローカルインストールする必要があります。WordPress をローカルにインストールすることで、パッチの作成とテスト、バグの発見と修正、リリースサイクル中の新機能の開発とテストに貢献できます。

<!--
There are two steps to installing WordPress on your computer for contributing to core:
-->

コアに貢献するための WordPress をコンピュータにインストールするには、2つのステップがあります。

<!--
1.  Choose and install a local server
2.  Install WordPress trunk
-->

1.  ローカルサーバーの選択とインストール
2.  WordPress trunk のインストール

<!--
If you haven’t [installed a local server](https://make.wordpress.org/core/handbook/installing-a-local-server/) yet, you’ll need to do that before continuing.
-->

もし、まだ[ローカルサーバーをインストール](https://make.wordpress.org/core/handbook/installing-a-local-server/)していないなら、先にそれを行うする必要があります。

<!--
## Zip File, SVN, or Git?
-->

## Zip ファイル、SVN、それとも Git ?

<!--
Once you have your local server installed, you can download a zip file of the [latest nightly release](https://wordpress.org/nightly-builds/wordpress-latest.zip), check out a copy of WordPress trunk [using Subversion (SVN)](https://wordpress.org/download/source/), or install from our [GitHub mirror](https://github.com/WordPress/wordpress-develop).
-->

ローカルサーバーにインストールしたら、[最新のナイトリーリリース](https://wordpress.org/nightly-builds/wordpress-latest.zip)の zip ファイルをダウンロードするか、WordPress trunk のコピーを [Subversion (SVN) を使って](https://wordpress.org/download/source/)チェックアウトするか、私たちの [GitHub ミラー](https://github.com/WordPress/wordpress-develop) からインストールできます。

<!--
Installing the latest nightly release from a zip file will allow you to [beta test](https://make.wordpress.org/core/handbook/testing/beta/) the code, and contribute bug reports. However, if you want to [contribute patches](https://make.wordpress.org/core/handbook/working-with-patches/) along with those bug reports, you’ll need to install a version-controlled copy of WordPress trunk.
-->

zip ファイルから最新のナイトリーリリースをインストールすると、コードの [ベータテスト](https://make.wordpress.org/core/handbook/testing/beta/) を行ったり、バグレポートに貢献できます。しかし、バグレポートと一緒に [パッチを提供](https://make.wordpress.org/core/handbook/working-with-patches/) をしたい場合は、バージョン管理された WordPress trunk のコピーをインストールする必要があります。

<!--
SVN and Git are both [version control systems](https://make.wordpress.org/core/handbook/glossary/#version-control). You’ll become very familiar with them when you are contributing to core.
-->

SVN と Git はどちらも[バージョン管理システム](https://make.wordpress.org/core/handbook/glossary/#version-control)です。コアにコントリビュートしているうちに、それらに慣れていくでしょう。

<!--
*   Subversion (SVN) is the official version control system used by the WordPress Project.
*   For those who prefer working with Git, a mirror of the SVN repository is [hosted on GitHub](https://github.com/WordPress/wordpress-develop). You can make a pull request on GitHub, but please make sure there is a corresponding [Trac](https://core.trac.wordpress.org/) ticket open and link your pull request to it.
-->

*   Subversion (SVN) は、WordPress プロジェクトで使用されている公式のバージョン管理システムです。
*   Git での作業を好む人のために、SVN リポジトリのミラーが [GitHub でホストされています](https://github.com/WordPress/wordpress-develop) 。GitHub でプルリクエストを提出できますが、対応する [Trac](https://core.trac.wordpress.org/) チケットが開かれていることを確認し、プルリクエストをそれにリンクしてください。
