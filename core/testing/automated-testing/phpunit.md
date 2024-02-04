# PHP: PHPUnit

<!--
PHPUnit is the official testing framework chosen by the core team to test our PHP code.
-->

PHPUnit は、PHP コードをテストするためにコアチームが選んだ公式のテストフレームワークです。

<!--
## Setup
-->

## セットアップ

<!--
**Step 1: Check out the test repository.**
-->

### ステップ1: テストリポジトリをチェックアウトする

<!--
The WordPress tests live in the core development repository, available via SVN at:
-->

WordPress のテストは、SVN 経由で利用可能なコア開発リポジトリにあります:

```bash
svn co https://develop.svn.wordpress.org/trunk/ wordpress-develop
cd wordpress-develop
```

<!--
Or Git:
-->

または Git で:

```bash
git clone git://develop.git.wordpress.org/ wordpress-develop
cd wordpress-develop
```

<!--
**Step 2: Set up a config file.**
-->

### ステップ2: config ファイルを設定する

<!--
Copy `wp-tests-config-sample.php` to `wp-tests-config.php`, and enter your database credentials. *Use a separate database.*
-->

`wp-tests-config-sample.php` を `wp-tests-config.php` にコピーし、データベースの認証情報を入力します。**別のデータベースを使用してください。**

<!--
### Test running workflow options
-->

## テストを実行するためのワークフローオプション

<!--
There are several different ways of running the PHPUnit tests. It’s up to you to choose whichever workflow suits you best.
-->

PHPUnit テストを実行するには、いくつかの方法があります。どのワークフローを選択するかはあなた次第です。

<!--
Some workflows require more set-up than others, when in doubt, we recommend you start with the Docker workflow as that will do most setup for you.
-->

ワークフローによってはより多くの設定が必要なものがあります。迷った場合は、ほとんどのセットアップが自動的に行われる Docker ワークフローから始めることをおすすめします。

<!--
1.  Docker container
2.  Composer
3.  PHPUnit PHAR file with Composer available
4.  PHPUnit PHAR file without Composer
-->

1.  Docker コンテナ
2.  Composer
3.  PHPUnit PHAR ファイルを Composer で実行する
4.  Composer を使わずに PHPUnit PHAR ファイルを実行する

<!--
**Pre-requisite for non-Docker workflows:**
-->

### Docker 以外のワークフローに必要な前提条件

<!--
For non-Docker workflows, you need to make sure that PHP and MySQL/MariaDB are available.
-->

Docker 以外のワークフローでは、PHP と MySQL/MariaDB が利用可能であることを確認する必要があります。

<!--
For more information on setting up PHP and a database locally, please see the [Installing a local server](https://make.wordpress.org/core/handbook/tutorials/installing-a-local-server/) handbook pages.
-->

PHP とデータベースをローカルにセットアップする方法については、[ローカルサーバーのインストール](https://ja.wordpress.org/team/handbook/core/tutorials/installing-a-local-server/)についてのハンドブックページを参照してください。

<!--
Please note that both [PHPUnit](https://docs.phpunit.de/en/9.6/installation.html#requirements), as well as the WordPress test suite have requirements for [certain PHP extensions](https://make.wordpress.org/hosting/handbook/server-environment/#php-extensions) to be enabled in your install to be able to run the full test suite.
-->

完全なテストスイートを実行するには、[PHPUnit](https://docs.phpunit.de/en/9.6/installation.html#requirements) と WordPress のテストスイートの両方で[特定の PHP 拡張モジュール](https://make.wordpress.org/hosting/handbook/server-environment/#php-extensions)を有効にする必要があることに注意してください。

<!--
Typical extensions which should be enabled are: `gd`, `mysql[i]`, `zip`, `exif`, `intl`, `mbstring`, `xml`, `xsl`.
-->

有効にしておくべき代表的な拡張機能は次の通りです: `gd`、`mysql[i]`、`zip`、`exif`、`intl`、`mbstring`、`xml`、`xsl`

<!--
Optionally, the PHP external extensions Xdebug, MemCache and Imagick should also be installed and enabled.
-->

オプションとして、PHP の外部拡張である Xdebug、MemCache および Imagick もインストールして有効にしておく必要があります。

<!--
#### Workflow 1: Setting up the Docker container environment
-->

### ワークフロー1: Docker コンテナ環境のセットアップ

<!--
**Step 1**: Install and then start [Docker](https://www.docker.com/products/docker-desktop)
-->

**ステップ1**: [Docker](https://www.docker.com/products/docker-desktop) をインストールし、起動する

<!--
**Step 2**: Install [NPM](https://nodejs.org/en/download/)
-->

**ステップ2**: [NPM](https://nodejs.org/en/download/) をインストールする

<!--
**Step 3**: Make sure you are in the root directory of where you installed WordPress
-->

**ステップ3**: WordPress をインストールしたディレクトリのルートディレクトリにいることを確認する

<!--
**Step 4**: Run from the command-line:
-->

**ステップ4**: コマンドラインから次のコマンドを実行する:

```bash
npm install
npm run build:dev
npm run env:start
npm run env:install
```

<!--
**Running the tests**
-->

#### テストの実行

<!--
Once the docker container is set up and provisioned, you can run the tests from the command-line: `npm run test:php`.
-->

docker コンテナをセットアップしてプロビジョニングされたら、コマンドラインからテストを実行できます: `npm run test:php`。

<!--
If you want to pass additional command-line arguments to PHPUnit, you will need to add an extra double-dash separator between the NPM command and the extra PHPUnit arguments to get NPM to pass them onto PHPUnit.
-->

追加のコマンドライン引数を PHPUnit に渡す場合は、NPM コマンドと追加の PHPUnit 引数の間に二重ダッシュ区切り文字を追加して、NPM がそれらを PHPUnit に渡すようにする必要があります。

<!--
#### Workflow 2: Setting up the Composer environment
-->

### ワークフロー2: Composer 環境のセットアップ

<!--
**Step 1**: Install [Composer](https://getcomposer.org/download/)
-->

**ステップ1**: [Composer](https://getcomposer.org/download/) をインストールする

<!--
**Step 2**: Make sure you are in the root directory of where you installed WordPress
-->

**ステップ2**: WordPress をインストールしたディレクトリのルートディレクトリにいることを確認する

<!--
**Step 3**: Run from the command-line: `composer update -W`
-->

**ステップ3**: コマンドラインから次のコマンドを実行する: `composer update -W`

<!--
**Running the tests**
-->

#### テストの実行

<!--
Once the Composer dependencies are installed, you can run the tests from the command-line: `vendor/bin/phpunit`.
-->

Composer の依存関係がインストールされたら、コマンドラインから次のコマンドを使用してテストを実行できます: `vendor/bin/phpunit`

<!--
#### Workflow 3: Setting up to run with the PHPUnit PHAR file with Composer available
-->

### ワークフロー3: PHPUnit PHAR ファイルを Composer で実行するための設定

<!--
**Step 1**: Install PHPUnit Phar
-->

**ステップ1**: PHPUnit Phar をインストールする

<!--
Install the PHAR which is [appropriate for your PHP version](https://phpunit.de/supported-versions.html). Installation instructions can be found in [the PHPUnit manual](https://docs.phpunit.de/en/9.6/installation.html) or on [the PHPUnit website](https://phpunit.de/getting-started/phpunit-9.html).
-->

[PHP のバージョンに適した](https://phpunit.de/supported-versions.html) PHAR をインストールします。インストール手順は、[PHPUnit のマニュアル](https://docs.phpunit.de/en/9.6/installation.html)または [PHPUnit の Web サイト](https://phpunit.de/getting-started/phpunit-9.html) を参照してください。

<!--
**Step 2**: Install [Composer](https://getcomposer.org/download/)
-->

**ステップ2**: [Composer](https://getcomposer.org/download/) をインストールする

<!--
**Step 3**: Make sure you are in the root directory of where you installed WordPress
-->

**ステップ3**: WordPress をインストールしたディレクトリのルートディレクトリにいることを確認する

<!--
**Step 4**: Install Composer dependencies
-->

**ステップ4**: Composer の依存関係をインストールする

<!--
Run from the command-line: `composer update -W`
-->

コマンドラインから次のコマンドを実行する: `composer update -W`

<!--
**Running the tests**
-->

#### テストの実行

<!--
Once the PHPUnit PHAR and the Composer dependencies are installed, you can run the tests from the command-line: `[path/to/]phpunit`.
-->

PHPUnit PHAR と Composer の依存関係がインストールされたら、コマンドラインから次のコマンドを使用してテストを実行できます: `[path/to/]phpunit`

<!--
#### Workflow 4: Setting up to run with the PHPUnit PHAR file without Composer
-->

### ワークフロー4: Composer を使わずに PHPUnit PHAR ファイルを実行するように設定する

<!--
This method is most suitable if you want to install PHPUnit and the PHPUnit Polyfills globally and run tests in multiple directories.
-->

この方法は、PHPUnit と PHPUnit ポリフィルをグローバルにインストールし、複数のディレクトリでテストを実行する場合に最適です。

<!--
**Step 1**: Install PHPUnit PHAR
-->

**ステップ1**: PHPUnit PHAR をインストールする

<!--
Install the PHAR which is [appropriate for your PHP version](https://phpunit.de/supported-versions.html). Installation instructions can be found in [the PHPUnit manual](https://docs.phpunit.de/en/9.6/installation.html) or on [the PHPUnit website](https://phpunit.de/getting-started/phpunit-9.html).
-->

[PHP のバージョンに適した](https://phpunit.de/supported-versions.html) PHAR をインストールします。インストール手順は、[PHPUnit のマニュアル](https://docs.phpunit.de/en/9.6/installation.html)または [PHPUnit の Web サイト](https://phpunit.de/getting-started/phpunit-9.html) を参照してください。

<!--
**Step 2**: Install [PHPUnit Polyfills](https://github.com/Yoast/PHPUnit-Polyfills/)
-->

**ステップ2**: [PHPUnit](https://github.com/Yoast/PHPUnit-Polyfills/) ポリフィルをインストールする

<!--
Typically, you would clone the GitHub repository:
-->

通常は、GitHub リポジトリのクローンを作成します:

```bash
git clone git@github.com:Yoast/PHPUnit-Polyfills.git [target/path]
```

<!--
**Step 3**: Define path to Polyfills
-->

**ステップ3**: ポリフィルへのパスを定義する

<!--
Once the Polyfills are installed, tell the WordPress test bootstrap where to find them by passing the path via a `WP_TESTS_PHPUNIT_POLYFILLS_PATH` constant.
-->

ポリフィルをインストールしたら、定数 `WP_TESTS_PHPUNIT_POLYFILLS_PATH` でパスを定義して、Polyfills がどこにあるかを WordPress のテスト用ブートストラップに伝えます。

<!--
This constant can be declared in the `phpunit.xml[.dist]` file like this:
-->

この定数は、`phpunit.xml[.dist]` ファイルで次のように宣言します:

```php
<php>
     <const name="WP_TESTS_PHPUNIT_POLYFILLS_PATH" value="path/to/yoast/phpunit-polyfills"/>
</php>

```

<!--
or can be declared as a PHP constant in the `wp-tests-config.php` file.
-->

または、`wp-tests-config.php` ファイルで PHP 定数として宣言できます。

<!--
**Running the tests**
-->

#### テストの実行

<!--
Once the PHPUnit PHAR and Polyfills are installed, you can run the tests from the root directory of your WordPress install via the command-line: `[path/to/]phpunit`.
-->

PHPUnit PHAR とポリフィルをインストールしたら、コマンドラインから次のコマンドを使用してテストを実行できます: `[path/to/]phpunit`

<!--
If you use this workflow, please ensure you keep your local clone of the PHPUnit Polyfills up to date.  
-->

\[info\]このワークフローを使用する場合は、PHPUnit ポリフィルのローカルクローンを常に最新の状態にしておくようにしましょう。\[/info\]

<!--
## Running the Test Suite
-->

## テストスイートの実行

<!--
Once you have chosen your preferred workflow and set up your machine according to the above instructions, you can run the tests via the command listed with your preferred workflow above.
-->

<!--
All examples below will use `phpunit`. Replace this with your workflow specific command for running these examples locally.
-->

\[info\]
好みのワークフローを選び、上記の手順に従ってマシンをセットアップしたら、上記の好みのワークフローに記載されているコマンドでテストを実行できます。

以下のすべての例では `phpunit` を使用します。これらの例をローカルで実行する場合は、このコマンドをワークフロー固有のコマンドに置き換えてください。
\[/info\]

<!--
You should see output that looks roughly like the following:
-->

おおよそ以下のような出力が表示されるはずです:

```bash
...........................................................    59 / 12524 (  0%)
...........................................................   118 / 12524 (  0%)
...........................................................   177 / 12524 (  1%)
...........................................................   236 / 12524 (  1%)
...........................................................   295 / 12524 (  2%)
.......SS..................................................   354 / 12524 (  2%)
...
........................................................... 12449 / 12524 ( 99%)
........................................................... 12508 / 12524 ( 99%)
................                                            12524 / 12524 (100%)

Time: 01:46.744, Memory: 235.10 MB

OK, but incomplete or skipped tests!
Tests: 12524, Assertions: 57712, Skipped: 56.

```

<!--
What each symbol means:
-->

各記号の意味は次の通りです:

<!--
*   `.` – Each dot signifies one “test” that passed.
*   `S` means a test was skipped. This usually means that the test is only valid in certain configurations, such as when a test requires Multisite or a certain PHP extension.
*   `F` means a test failed. More output will be shown for what exactly failed and where.
*   `E` means a test failed due to a PHP error, warning, or notice.
*   `R` means a test is marked as “risky”. What will be marked as risky, very much depends on the configuration in the `phpunit.xml.dist` file. This can be tests which are particularly slow or don’t perform assertions.
*   `I` means a test was marked as incomplete, i.e. not yet implemented.
-->

*   `.` – それぞれのドットは合格した一つの「テスト」を意味します。
*   `S` はテストがスキップされたことを意味します。これは通常、テストがマルチサイトや特定の PHP 拡張モジュールを必要とするなど、特定の設定でのみ有効であることを意味します。
*   `F` はテストが失敗したことを意味します。何がどこで失敗したのか、より詳細な出力が表示されます。
*   `E` は、PHP のエラー、警告、通知によってテストが失敗したことを意味します。
*   `R` はテストが「危険」と判定されたことを意味します。何が危険と判定されるかは、`phpunit.xml.dist` ファイルの設定に大きく依存します。これは、特に遅いテストやアサーションを実行しないテストなどです。
*   `I` は、テストが不完全である、たとえばまだ実装されていないことを意味します。

<!--
On Windows and seeing weird codes in your command-line screen output? Try running with `--colors=never`.
-->

\[info\]Windows で、コマンドラインの画面出力に奇妙なコードが表示されていますか ? `--colors=never` で実行してみてください。\[/info\]

<!--
### Running Specific Tests
-->

### 特定のテストの実行

<!--
#### Individual Tests
-->

#### 個別テスト

<!--
To run an **individual class**, use `--filter` with the name of the class:
-->

**個別のクラス** を実行するには、`--filter` を使用してクラス名を指定します:

```bash
phpunit --filter Tests_Formatting_wpParseStr
```

<!--
The `--filter` option in PHPUnit is very flexible and has lots of supported options. Please see the [PHPUnit Manual](https://docs.phpunit.de/en/9.6/textui.html#textui-examples-filter-patterns) for more examples.
-->

PHPUnit の `--filter` オプションは非常に柔軟で、さまざまなオプションをサポートしています。[PHPUnit のマニュアル](https://docs.phpunit.de/en/9.6/textui.html#textui-examples-filter-patterns)を参照ください。

<!--
#### Groups
-->

#### グループ

<!--
To run a **group of tests** – defined by `@group` in code comments:
-->

**テストのグループ** を実行するには、コードのコメントで定義されている `@group` を使用します:

```bash
phpunit --group dependencies
phpunit --group themes
```

<!--
You may also combine groups: (Depending on your platform you may have to wrap the groups in double quotes)
-->

グループを組み合わせることもできます (プラットフォームによっては、グループを二重引用符で囲む必要がある場合があります)。

```bash
phpunit --group shortcode,17657,6562,14050
```

```bash
...
OK (229 tests, 417 assertions)
```

<!--
Many tests are marked with a `@ticket` annotation, which indicates they were the result of that WordPress Trac ticket.
-->

<!--
The `@ticket` annotation is an alias for the `@group` annotation, so any tests linked to any individual Trac ticket can be run by passing the Trac ticket number as the “group”.
-->

\[info\]
多くのテストには `@ticket` というアノテーションがついており、WordPress の Trac チケットの結果であることを示しています。

`@ticket` アノテーションは `@group` アノテーションのエイリアスであるため、Trac チケット番号を「group」として渡すことで、個々の Trac チケットにリンクされたテストを実行できます。
\[/info\]

<!--
To view all groups:
-->

すべてのグループを表示するには:

```bash
phpunit --list-groups
```

<!--
To see information about skipped and incomplete tests, use `--verbose`:
-->

スキップされたテストや不完全なテストに関する情報を見るには、`--verbose` を使用します:

```bash
phpunit --group wpdb --verbose
```

```bash

There was 1 skipped test:
1) Tests_DB::test_charset_switched_to_utf8
This test requires utf8mb4 to not be supported.

tests/phpunit/tests/db.php:1332
```

<!--
By default, the **AJAX tests** (tests written for core’s use of `wp-admin/admin-ajax.php`) are not run. To run these:
-->

デフォルトでは、**AJAX テスト** (コアが `wp-admin/admin-ajax.php` を使用するために作成されたテスト) は実行されません。これらを実行するには:

```bash
phpunit --group ajax
```

<!--
To run the tests under **multisite**, you must switch to the `multisite.xml` configuration file:
-->

**マルチサイト**でテストを実行するには、`multisite.xml` 設定ファイルに切り替える必要があります:

```bash
phpunit -c tests/phpunit/multisite.xml
```

<!--
#### With Grunt
-->

#### Grunt を使用する

<!--
Additionally, you can `npm run grunt phpunit` and run PHPUnit tests, including the ajax and multisite tests.
-->

さらに、`npm run grunt phpunit` を実行することで、ajax テストや multisite テストを含む PHPUnit テストを実行できます。

<!--
#### Running Continuously
-->

#### 継続的に実行する

<!--
Rather than having to switch to a terminal and manually run a test group repeatedly while working on a patch, you can keep it running continuously. Whenever you save any file, the group will run again automatically. This lets you instantly know when a change you’ve made breaks a test, or causes it to pass.
-->

パッチの作業中にターミナルに切り替えて手動でテストグループを繰り返し実行するのではなく、継続的に実行し続けることができます。ファイルを保存するたびに、テストグループは自動的に再実行されます。これにより、ある変更によってテストが壊れたり合格したりしたことをすぐに知ることができます。

<!--
To run PHPUnit tests *and* all other watch tasks, use:
-->

PHPUnit テスト**および**その他のすべての監視タスクを実行するには、次のようにします:

```bash
npm run grunt watch -- --phpunit --group={testgroup}
```

<!--
To run *only* the PHPUnit watch task, use:
-->

PHPUnit 監視タスク**のみ**を実行するには、次のようにします:

```bash
npm run grunt watch:phpunit -- --group={testgroup}
```

<!--
Run multiple groups by comma-separating them:
-->

カンマ区切りで複数のグループを実行します:

```bash
﻿npm run grunt watch:phpunit -- --group=community-events,privacy
```

<!--
#### Optimizing
-->

#### 最適化

<!--
You can speed up the suite in some cases by defining the `WP_TESTS_SKIP_INSTALL` environment variable to `1`, so that the suite will skip the install step. While this shouldn’t be used for full test runs, it’s useful for saving time when running small groups of tests.
-->

環境変数 `WP_TESTS_SKIP_INSTALL` を `1` に定義することで、スイートがインストール手順をスキップするようになり、スイートの速度を向上させることができます。これは完全なテストの実行には使用すべきではありませんが、小さなテストグループの実行時間を節約することに役立ちます。

```bash
WP_TESTS_SKIP_INSTALL=1 phpunit --group=privacy
```

<!--
## Writing Tests
-->

## テストを作成する

<!--
We’ve written [a guide](https://make.wordpress.org/core/handbook/testing/automated-testing/writing-phpunit-tests/) for getting started writing PHPUnit tests for WordPress.
-->

WordPress の PHPUnit テストを作成し始めるための[ガイド](https://ja.wordpress.org/team/handbook/core/testing/automated-testing/writing-phpunit-tests/)を作成しました。

<!--
## Contributing Tests to WordPress
-->

## テストで WordPress に貢献する

<!--
There are three primary ways to contribute:
-->

貢献するためには、主に3つの方法があります:

<!--
**Write tests for a reported bug.** A great way to contribute is to write tests that demonstrate an existing bug report. The core developers are reluctant to consider patches for many sensitive areas in core without test coverage. Well-written tests can help confirm that a patch fixes a problem without side effects, and can prevent any regressions from occurring in the future. When tests are particularly needed or desired for a ticket to proceed, they receive the [needs-unit-tests](https://core.trac.wordpress.org/query?keywords=~needs-unit-tests) workflow keyword. You can submit tests for existing tickets directly on the WordPress core Trac. Bonus points for submitting a bug report with a test case included.
-->

**報告されたバグのテストを作成する。** 貢献するすばらしい方法は、既存のバグレポートを実証するテストを作成することです。コア開発者は、テストカバレッジのないコアの多くの繊細な部分のパッチを検討することに消極的です。適切に作成されたテストは、パッチが副作用なしに問題を修正することを確認するのに役立ち、将来的にリグレッションが発生することを防ぐことができます。チケットを進めるためにテストが特に必要であったり望ましい場合は、[needs-unit-tests](https://core.trac.wordpress.org/query?keywords=~needs-unit-tests) ワークフローキーワードを受け取ります。既存のチケットのテストは WordPress コアの Trac で直接提出できます。テストケースを含むバグレポートを提出するとよりよいでしょう。

<!--
**Write new tests to improve our code coverage.** Many areas of WordPress do not have adequate test coverage. Pick a function, class, or component and write tests for it. You can submit these tests on [the WordPress Trac](https://core.trac.wordpress.org/).
-->

**コードカバレッジを向上させるために新しいテストを作成する。** WordPress の多くの領域で、十分なテストカバレッジを持っていません。関数、クラス、コンポーネントを選んで、そのテストを作成してください。これらのテストは [WordPress Trac](https://core.trac.wordpress.org/) で提出できます。

<!--
**Fix or improve our existing test cases.** There are many opportunities for improvement in the existing tests. Some of them are ancient and others are slow or fragile. Some do not tests well in multisite or under certain conditions. Some individual tests try to test too much, and [could be improved by using](https://docs.phpunit.de/en/9.6/writing-tests-for-phpunit.html) data providers, dependencies, and more narrow assertions.
-->

**既存のテストケースを修正または改善する。** 既存のテストには改善の余地がたくさんあります。古いものもあれば、速度が遅い、または壊れやすいものもあります。マルチサイトや特定の条件下でうまくテストできてないものもあります。一部の個別のテストより多くのことをテストしようとしており、データプロバイダ、依存関係、より限定的なアサーションを[使用することで改善できる可能性があります](https://docs.phpunit.de/en/9.6/writing-tests-for-phpunit.html)。

<!--
## JavaScript Unit Tests
-->

## JavaScript ユニットテスト

<!--
Unit tests for JavaScript code are currently much more limited in WordPress Core in comparison to PHP unit tests. For more information on JS unit tests, see the [Make/Core post](https://make.wordpress.org/core/2013/09/13/javascript-unit-tests-for-core/ "JavaScript Unit Tests for Core") or the [QUnit section of this Handbook](https://make.wordpress.org/core/handbook/testing/automated-testing/qunit/).
-->

JavaScript コードのユニットテストは、PHP のユニットテストに比べて WordPress コアではかなり制限されています。JS ユニットテストの詳細については、[Make/Core の投稿](https://make.wordpress.org/core/2013/09/13/javascript-unit-tests-for-core/)や[ハンドブックの QUnit セクション](https://ja.wordpress.org/team/handbook/core/testing/automated-testing/qunit/)を参照してください。

<!--
## Further Reading
-->

## 参考資料

<!--
*   [PHPUnit Manual](https://docs.phpunit.de/)
*   [PHPUnit on Github](https://github.com/sebastianbergmann/phpunit)
-->
