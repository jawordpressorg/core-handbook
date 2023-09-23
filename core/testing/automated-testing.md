<!--
# Automated Testing
-->

# 自動化されたテスト

<!--
This is an overview of running and writing tests for WordPress. Automated testing is running test cases where manual intervention is not required to run each one. This is usually in the form of writing test suites which have multiple test cases and a library and command line tool that runs the test suite or suites.
-->

WordPress のテストの実行と書き方について説明します。自動化されたテストとは、テストケースを実行する際に手作業が不要な状態を指します。これは通常、複数のテストケースを含むテストスイートと、そのテストスイートを実行するためのライブラリやコマンドラインツールを作成する形で行われます。

<!--
The test suites WordPress uses are PHPUnit for PHP and QUnit for JavaScript.
-->

WordPress で使用されるテストスイートは PHP 用の PHPUnit と、JavaScript 用の QUnit です。

<!--
Execution is usually manual, from the developer choosing which suites on the command line to run, but this isn’t required. The process could be automated and looked over from time to time to ensure that when the code changed, no problems were introduced.
-->

実行は通常、開発者がコマンドラインでどのスイートを実行するかを選択することから手作業で行われますが、これは必須ではありません。このプロセスを自動化し、コードが変更されたときに問題が発生しないように、時々目を通すこともできます。

<!--
For more information on getting started installing the test suites and running and writing tests, follow the links below:
-->

テストスイートのインストール、テストの実行と書き込みを始めるための詳細については、以下のリンクを参照してください。

<!--
*   [Testing PHP with PHPUnit](https://make.wordpress.org/core/handbook/testing/phpunit/)
*   [Testing JavaScript with QUnit](https://make.wordpress.org/core/handbook/testing/phpunit/qunit/)
-->

*   [PHPUnit を用いた PHP のテスト](https://make.wordpress.org/core/handbook/testing/phpunit/)
*   [QUnit を用いた JavaScript のテスト](https://make.wordpress.org/core/handbook/testing/phpunit/qunit/)

<!--
Note: If writing a test requiring a YouTube or Vimeo URL/embed, please use the WP 5.0 release YouTube video and the official Vimeo test video:
-->

備考: YouTube や Vimeo の URL または埋め込みが必要なテストを書く場合は、WP 5.0のリリース YouTube 動画と Vimeo の公式テスト動画を使用してください。

<!--
*   YouTube: [https://www.youtube.com/watch?v=72xdCU\_\_XCk](https://www.youtube.com/watch?v=72xdCU__XCk)
*   Vimeo: [https://vimeo.com/76979871](https://vimeo.com/76979871)
-->

*   YouTube: [https://www.youtube.com/watch?v=72xdCU\_\_XCk](https://www.youtube.com/watch?v=72xdCU__XCk)
*   Vimeo: [https://vimeo.com/76979871](https://vimeo.com/76979871)
