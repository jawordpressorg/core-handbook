<!--
# JavaScript: QUnit
-->

# JavaScript: QUnit

<!--
> QUnit is a JavaScript unit testing framework.
-->
> QUnit は JavaScript のユニットテストのフレームワークです。

<!--
## Installation
-->

## インストール

<!--
**1. Set up your install.** Follow one of the guides to setup your local install [https://make.wordpress.org/core/handbook/tutorials/installing-wordpress-locally/](https://make.wordpress.org/core/handbook/tutorials/installing-wordpress-locally/).
-->

**1. インストールを設定する:** このガイドに従って、ローカル環境へインストールします。
[https://ja.wordpress.org/team/handbook/core/tutorials/installing-wordpress-locally/](https://ja.wordpress.org/team/handbook/core/tutorials/installing-wordpress-locally/)

<!--
**2. Install WordPress via SVN** Install WordPress via SVN or Git [https://make.wordpress.org/core/handbook/tutorials/installing-wordpress-locally/from-svn/](https://make.wordpress.org/core/handbook/tutorials/installing-wordpress-locally/from-svn/).
-->

**2. SVN 経由で WordPress をインストールする:** SVN か Git で WordPress をインストールします。
[https://ja.wordpress.org/team/handbook/core/tutorials/installing-wordpress-locally/from-svn/](https://ja.wordpress.org/team/handbook/core/tutorials/installing-wordpress-locally/from-svn/)

<!--
## Running the QUnit Test Suite
-->

## QUnit テストスイートを実行

<!--
From your now installed and configured WordPress testing installation navigate to `/tests/qunit/index.html`.
-->

WordPress をインストールし、設定したテスト環境から `/tests/qunit/index.html` に移動してください。

<!--
If your locally setup domain is `http://wp-test.dev` then `http://wp-test.dev/tests/qunit/index.html` is the URL you want.
-->

ローカルに設定したドメインが `http://wp-test.dev` であれば、`http://wp-test.dev/tests/qunit/index.html` が必要な URL です。

<!--
You can also run the tests directly in the browser without setting up a web server, append `/tests/qunit/index.html` to the the file path of your repo check out, for example `file:///Users/myusername/dev/develop.svn.wordpress.org/trunk/tests/qunit/index.html`
-->

Web サーバーを立ち上げずに、ブラウザ上で直接テストを実行することもできます。チェックアウトしたリポジトリのファイルパスに `/tests/qunit/index.html` を追加してください。たとえば、`file:///Users/musername/dev/develop.svn.wordpress.org/trunk/tests/qunit/index.html` というようにします。
