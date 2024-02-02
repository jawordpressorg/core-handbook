# PHP: PHPUnit

PHPUnit is the official testing framework chosen by the core team to test our PHP code.

## Setup

**Step 1: Check out the test repository.**

The WordPress tests live in the core development repository, available via SVN at:

```bash
svn co https://develop.svn.wordpress.org/trunk/ wordpress-develop
cd wordpress-develop
```

Or Git:

```bash
git clone git://develop.git.wordpress.org/ wordpress-develop
cd wordpress-develop
```

**Step 2: Set up a config file.**

Copy `wp-tests-config-sample.php` to `wp-tests-config.php`, and enter your database credentials. *Use a separate database.*

### Test running workflow options

There are several different ways of running the PHPUnit tests. It’s up to you to choose whichever workflow suits you best.

Some workflows require more set-up than others, when in doubt, we recommend you start with the Docker workflow as that will do most setup for you.

1.  Docker container
2.  Composer
3.  PHPUnit PHAR file with Composer available
4.  PHPUnit PHAR file without Composer

**Pre-requisite for non-Docker workflows:**

For non-Docker workflows, you need to make sure that PHP and MySQL/MariaDB are available.

For more information on setting up PHP and a database locally, please see the [Installing a local server](https://make.wordpress.org/core/handbook/tutorials/installing-a-local-server/) handbook pages.

Please note that both [PHPUnit](https://docs.phpunit.de/en/9.6/installation.html#requirements), as well as the WordPress test suite have requirements for [certain PHP extensions](https://make.wordpress.org/hosting/handbook/server-environment/#php-extensions) to be enabled in your install to be able to run the full test suite.

Typical extensions which should be enabled are: `gd`, `mysql[i]`, `zip`, `exif`, `intl`, `mbstring`, `xml`, `xsl`.

Optionally, the PHP external extensions Xdebug, MemCache and Imagick should also be installed and enabled.

#### Workflow 1: Setting up the Docker container environment

**Step 1**: Install and then start [Docker](https://www.docker.com/products/docker-desktop)

**Step 2**: Install [NPM](https://nodejs.org/en/download/)

**Step 3**: Make sure you are in the root directory of where you installed WordPress

**Step 4**: Run from the command-line:

```bash
npm install
npm run build:dev
npm run env:start
npm run env:install
```

**Running the tests**

Once the docker container is set up and provisioned, you can run the tests from the command-line: `npm run test:php`.

If you want to pass additional command-line arguments to PHPUnit, you will need to add an extra double-dash separator between the NPM command and the extra PHPUnit arguments to get NPM to pass them onto PHPUnit.

#### Workflow 2: Setting up the Composer environment

**Step 1**: Install [Composer](https://getcomposer.org/download/)

**Step 2**: Make sure you are in the root directory of where you installed WordPress

**Step 3**: Run from the command-line: `composer update -W`

**Running the tests**

Once the Composer dependencies are installed, you can run the tests from the command-line: `vendor/bin/phpunit`.

#### Workflow 3: Setting up to run with the PHPUnit PHAR file with Composer available

**Step 1**: Install PHPUnit Phar

Install the PHAR which is [appropriate for your PHP version](https://phpunit.de/supported-versions.html). Installation instructions can be found in [the PHPUnit manual](https://docs.phpunit.de/en/9.6/installation.html) or on [the PHPUnit website](https://phpunit.de/getting-started/phpunit-9.html).

**Step 2**: Install [Composer](https://getcomposer.org/download/)

**Step 3**: Make sure you are in the root directory of where you installed WordPress

**Step 4**: Install Composer dependencies

Run from the command-line: `composer update -W`

**Running the tests**

Once the PHPUnit PHAR and the Composer dependencies are installed, you can run the tests from the command-line: `[path/to/]phpunit`.

#### Workflow 4: Setting up to run with the PHPUnit PHAR file without Composer

This method is most suitable if you want to install PHPUnit and the PHPUnit Polyfills globally and run tests in multiple directories.

**Step 1**: Install PHPUnit PHAR

Install the PHAR which is [appropriate for your PHP version](https://phpunit.de/supported-versions.html). Installation instructions can be found in [the PHPUnit manual](https://docs.phpunit.de/en/9.6/installation.html) or on [the PHPUnit website](https://phpunit.de/getting-started/phpunit-9.html).

**Step 2**: Install [PHPUnit Polyfills](https://github.com/Yoast/PHPUnit-Polyfills/)

Typically, you would clone the GitHub repository:

```bash
git clone git@github.com:Yoast/PHPUnit-Polyfills.git [target/path]
```

**Step 3**: Define path to Polyfills

Once the Polyfills are installed, tell the WordPress test bootstrap where to find them by passing the path via a `WP_TESTS_PHPUNIT_POLYFILLS_PATH` constant.

This constant can be declared in the `phpunit.xml[.dist]` file like this:

```php
<php>
     <const name="WP_TESTS_PHPUNIT_POLYFILLS_PATH" value="path/to/yoast/phpunit-polyfills"/>
</php>

```

or can be declared as a PHP constant in the `wp-tests-config.php` file.

**Running the tests**

Once the PHPUnit PHAR and Polyfills are installed, you can run the tests from the root directory of your WordPress install via the command-line: `[path/to/]phpunit`.

If you use this workflow, please ensure you keep your local clone of the PHPUnit Polyfills up to date.  

## Running the Test Suite

Once you have chosen your preferred workflow and set up your machine according to the above instructions, you can run the tests via the command listed with your preferred workflow above.

All examples below will use `phpunit`. Replace this with your workflow specific command for running these examples locally.

You should see output that looks roughly like the following:

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

What each symbol means:

*   `.` – Each dot signifies one “test” that passed.
*   `S` means a test was skipped. This usually means that the test is only valid in certain configurations, such as when a test requires Multisite or a certain PHP extension.
*   `F` means a test failed. More output will be shown for what exactly failed and where.
*   `E` means a test failed due to a PHP error, warning, or notice.
*   `R` means a test is marked as “risky”. What will be marked as risky, very much depends on the configuration in the `phpunit.xml.dist` file. This can be tests which are particularly slow or don’t perform assertions.
*   `I` means a test was marked as incomplete, i.e. not yet implemented.

On Windows and seeing weird codes in your command-line screen output? Try running with `--colors=never`.

### Running Specific Tests

#### Individual Tests

To run an **individual class**, use `--filter` with the name of the class:

```bash
phpunit --filter Tests_Formatting_wpParseStr
```

The `--filter` option in PHPUnit is very flexible and has lots of supported options. Please see the [PHPUnit Manual](https://docs.phpunit.de/en/9.6/textui.html#textui-examples-filter-patterns) for more examples.

#### Groups

To run a **group of tests** – defined by `@group` in code comments:

```bash
phpunit --group dependencies
phpunit --group themes
```

You may also combine groups: (Depending on your platform you may have to wrap the groups in double quotes)

```bash
phpunit --group shortcode,17657,6562,14050
```

```bash
...
OK (229 tests, 417 assertions)
```

Many tests are marked with a `@ticket` annotation, which indicates they were the result of that WordPress Trac ticket.

The `@ticket` annotation is an alias for the `@group` annotation, so any tests linked to any individual Trac ticket can be run by passing the Trac ticket number as the “group”.

To view all groups:

```bash
phpunit --list-groups
```

To see information about skipped and incomplete tests, use `--verbose`:

```bash
phpunit --group wpdb --verbose
```

```bash
 
There was 1 skipped test: 
1) Tests_DB::test_charset_switched_to_utf8
This test requires utf8mb4 to not be supported.

tests/phpunit/tests/db.php:1332
```

By default, the **AJAX tests** (tests written for core’s use of `wp-admin/admin-ajax.php`) are not run. To run these:

```bash
phpunit --group ajax
```

To run the tests under **multisite**, you must switch to the `multisite.xml` configuration file:

```bash
phpunit -c tests/phpunit/multisite.xml
```

#### With Grunt

Additionally, you can `npm run grunt phpunit` and run PHPUnit tests, including the ajax and multisite tests.

#### Running Continuously

Rather than having to switch to a terminal and manually run a test group repeatedly while working on a patch, you can keep it running continuously. Whenever you save any file, the group will run again automatically. This lets you instantly know when a change you’ve made breaks a test, or causes it to pass.

To run PHPUnit tests *and* all other watch tasks, use:

```bash
npm run grunt watch -- --phpunit --group={testgroup}
```

To run *only* the PHPUnit watch task, use:

```bash
npm run grunt watch:phpunit -- --group={testgroup}
```

Run multiple groups by comma-separating them:

```bash
﻿npm run grunt watch:phpunit -- --group=community-events,privacy
```

#### Optimizing

You can speed up the suite in some cases by defining the `WP_TESTS_SKIP_INSTALL` environment variable to `1`, so that the suite will skip the install step. While this shouldn’t be used for full test runs, it’s useful for saving time when running small groups of tests.

```bash
WP_TESTS_SKIP_INSTALL=1 phpunit --group=privacy
```

## Writing Tests

We’ve written [a guide](https://make.wordpress.org/core/handbook/testing/automated-testing/writing-phpunit-tests/) for getting started writing PHPUnit tests for WordPress.

## Contributing Tests to WordPress

There are three primary ways to contribute:

**Write tests for a reported bug.** A great way to contribute is to write tests that demonstrate an existing bug report. The core developers are reluctant to consider patches for many sensitive areas in core without test coverage. Well-written tests can help confirm that a patch fixes a problem without side effects, and can prevent any regressions from occurring in the future. When tests are particularly needed or desired for a ticket to proceed, they receive the [needs-unit-tests](https://core.trac.wordpress.org/query?keywords=~needs-unit-tests) workflow keyword. You can submit tests for existing tickets directly on the WordPress core Trac. Bonus points for submitting a bug report with a test case included.

**Write new tests to improve our code coverage.** Many areas of WordPress do not have adequate test coverage. Pick a function, class, or component and write tests for it. You can submit these tests on [the WordPress Trac](https://core.trac.wordpress.org/).

**Fix or improve our existing test cases.** There are many opportunities for improvement in the existing tests. Some of them are ancient and others are slow or fragile. Some do not tests well in multisite or under certain conditions. Some individual tests try to test too much, and [could be improved by using](https://docs.phpunit.de/en/9.6/writing-tests-for-phpunit.html) data providers, dependencies, and more narrow assertions.

## JavaScript Unit Tests

Unit tests for JavaScript code are currently much more limited in WordPress Core in comparison to PHP unit tests. For more information on JS unit tests, see the [Make/Core post](https://make.wordpress.org/core/2013/09/13/javascript-unit-tests-for-core/ "JavaScript Unit Tests for Core") or the [QUnit section of this Handbook](https://make.wordpress.org/core/handbook/testing/automated-testing/qunit/).

## Further Reading

*   [PHPUnit Manual](https://docs.phpunit.de/)
*   [PHPUnit on Github](https://github.com/sebastianbergmann/phpunit)