# Installing WordPress Locally

This section of the handbook contains tutorials that will walk you through the process of installing WordPress locally.

## Why do I need a local WordPress install?

If you want to contribute to WordPress core, you need to have a local install of WordPress on your computer to break, play with, and develop with. A local WordPress install allows you to create/test patches, find/fix bugs, and help develop/test new features during a release cycle.

There are two steps to installing WordPress on your computer for contributing to core:

1.  Choose and install a local server
2.  Install WordPress trunk

If you haven’t [installed a local server](https://make.wordpress.org/core/handbook/contribute/#local-development-overview) yet, you’ll need to do that before continuing.

## Zip File, SVN, or Git?

Once you have your local server installed, you can download a zip file of the [latest nightly release](https://wordpress.org/nightly-builds/wordpress-latest.zip), check out a copy of WordPress trunk [using Subversion (SVN)](https://wordpress.org/download/source/), or install from our [GitHub mirror](https://github.com/WordPress/wordpress-develop).

Installing the latest nightly release from a zip file will allow you to [beta test](https://make.wordpress.org/core/handbook/testing/beta/) the code, and contribute bug reports. However, if you want to [contribute patches](https://make.wordpress.org/core/handbook/working-with-patches/) along with those bug reports, you’ll need to install a version-controlled copy of WordPress trunk.

SVN and Git are both [version control systems](https://make.wordpress.org/core/handbook/glossary/#version-control). You’ll become very familiar with them when you are contributing to core.

*   Subversion (SVN) is the official version control system used by the WordPress Project.
*   For those who prefer working with Git, a mirror of the SVN repository is [hosted on GitHub](https://github.com/WordPress/wordpress-develop). You can make a pull request on GitHub, but please make sure there is a corresponding [Trac](https://core.trac.wordpress.org/) ticket open and link your pull request to it.