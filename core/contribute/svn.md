# The Code Repository (SVN)

Alert: WordPress supports patches being created from both [GIT](https://make.wordpress.org/core/handbook/contribute/git/) and SVNSVN Subversion, the popular version control system (VCS) by the Apache project, used by WordPress to manage changes to its codebase.. This documentation focuses on the SVN option.

## What is SVN?

WordPress uses [Subversion (SVN)](https://make.wordpress.org/core/glossary/#svn), a very popular version control system managed by the Apache project, to manage changes to its codebase. A change to the WordPress codebase increments the **revision** number. Individual changes are called [commits or changesets](https://make.wordpress.org/core/glossary/#commit-noun). These are denoted as either [r12345](https://core.trac.wordpress.org/changeset/12345) or \[[12345](https://core.trac.wordpress.org/changeset/12345)\]. Details of the SVN and Git repositories are located [here](https://make.wordpress.org/core/handbook/contribute/codebase/).

The WordPress repository of code is organized into three main directories: [tags](https://make.wordpress.org/core/glossary/#tag), [branches](https://make.wordpress.org/core/glossary/#branch), and [trunk](https://make.wordpress.org/core/glossary/#trunk).

*   The **trunk** directory contains the latest development code in preparation for the next major release cycle. The latest revision may be unstable or broken at times. The latest development code may be referred to as *trunk*.
*   The **tags** directory contains individual snapshots of each official release, such as the 3.4.0 or 3.5.1 tags. Once created, these are unmodified, and these are used to build the download packages.
*   The **branches** directory contains directories that consist of the latest code for each major release, such as the 3.4 and 3.5 branches. Minor release development occurs within the branch. For example, a critical bug that affects the latest release may be fixed in both trunk and the most recent branch, in preparation for a **point release** – i.e. 3.5.2, in the case of the 3.5 branch. These should generally be considered stable, but care should be taken when a minor release is being prepared.

## Finding an SVN Client

Most popular IDE (Integrated Developer Environment) applications include built-in support for SVN. Some also include enhanced support for WordPress development. This makes it very convenient to perform all source code version control tasks: synchronize, manage local copies, create patches, etc.

Alternatively some developers run SVN commands using the [command line interface](https://make.wordpress.org/core/glossary/#command-line-interface) (CLI), such as [Terminal](http://en.wikipedia.org/wiki/Terminal_(OS_X)) on the Mac. Even though most basic commands are simple, the command line is reasonably intimidating for many users. Many developers do rely on [GUI](http://en.wikipedia.org/wiki/GUI) applications though, either for regular use, or to handle complex actions more effectively.

When not using an IDE, or if a stand-alone GUI application is required, for Windows the recommended SVN client is [TortoiseSVN](http://tortoisesvn.net/), which is free and open source.

For Mac, the recommended SVN client is [Cornerstone](http://www.zennaware.com/cornerstone/), which must be purchased.

## Learn More

If you would like to learn more about working with Subversion, check out [Installing A Version Control System](https://make.wordpress.org/core/handbook/tutorials/installing-a-vcs/), [Installing WordPress Via SVN](https://make.wordpress.org/core/handbook/tutorials/installing-wordpress-locally/from-svn/), and [Working With Patches](https://make.wordpress.org/core/handbook/working-with-patches/) in the **Tutorials and Guides** section of this handbook.