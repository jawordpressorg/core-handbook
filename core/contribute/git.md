# The Code Repository (Git)

Alert: Contributors to WordPress may submit patches created via either **Git** or **[SVN](https://make.wordpress.org/core/handbook/contribute/svn/)**. This documentation focuses on the **Git** option.

## Summary

[Git](https://git-scm.com/) is a distributed version control system originally created by Linus Torvalds to assist with the management of the Linux kernel.

The canonical WordPress repository is managed using Subversion. To better support developers who are more comfortable working with Git, official, up-to-date Git mirrors of the WordPress repository are available at `git://develop.git.wordpress.org/` and `https://github.com/WordPress/wordpress-develop`.

**Please note:** while many people find it easier to use `git` to manage their patches, pull requests submitted to GitHub will not be merged there. Patches can be created and reviewed in GitHub pull requests, but they **must** be associated with a Trac ticket. To better understand what this means, see the [GitHub Pull Requests for Code Review page](https://make.wordpress.org/core/handbook/contribute/git/github-pull-requests-for-code-review/).

## Repository Structure

The WordPress Git mirror contains a complete history of the codebase. Each Subversion commit is represented by a Git changeset. Use the `git log` utility to browse the history of the project. The layout of the repository is as follows:

*   The **trunk** branch, which corresponds to SVN **trunk**. This is the bleeding-edge branch, containing the alpha version of the next major release. Except in special cases, contributors should prepare their patches against the trunk branch.
*   A branch exists corresponding to each major release series, named using the first two digits of versions in that series. For example, 4.5.1 was released from the `4.5` branch. Use `git branch -r` to view a complete list of branches in the remote repository, and use commands like `git checkout -b 4.5.x origin/4.5` to create local branches that track remote branches.
*   All WP releases (starting with 1.5.0) are represented by Git tags. Use `git tag` to see the list.

## Patches

Suggested improvements and bugfixes for WordPress should be submitted as **patches**. A [patch](https://make.wordpress.org/core/glossary/#patch) is a special text file that describes changes to code, by identifying the files and lines which are added, removed, and altered. It may also be referred to as a **diff** (after the Unix command to generate a differences file). Patches have the extension of either `.patch` or `.diff`. Patch files can then be submitted for consideration to [WordPress Trac](https://core.trac.wordpress.org/), the project’s official bugtracker.

Using the `git` cli client, you can create a patch file as follows:

1.  Clone the repository to your local machine: `$ git clone git://develop.git.wordpress.org/ /path/to/wordpress-develop`
2.  Create a working branch (it’s better not to modify `trunk` because this should always be the latest version of the official code). To keep your local checkout organized, it’s suggested that you use the Trac ticket number as part of your branch name, eg: `$ git checkout -b 30000-add-more-alots   `
3.  Make your modifications to the codebase. Stage the changes (`git add`), and commit (`git commit`).  [The official git documentation](https://git-scm.com/docs/gittutorial) includes a tutorial on this.
4.  Use `git diff` to review the differences between your local branch and the trunk branch: `$ git diff trunk 30000-add-more-alots` †
5.  Once you’re ready to submit your patch to Trac, generate a patch file using `git diff`, specifying that the output should be saved in a `.diff` file. In general, the file name should be the ticket number you are working on with `.diff` as the extension (or `.2.diff`, `.3.diff`, etc. if there are already patches on the ticket). Example command: `$ git diff trunk 30000-add-more-alots > 30000.diff`
6.  Upload the patch to the appropriate Trac ticket.

### Unit Tests

We strongly recommend [running the PHPUnit test suite](https://make.wordpress.org/core/handbook/testing/automated-testing/phpunit/) (and writing unit tests for your patch) before submitting it to Trac. This makes it many times easier for committers to review and commit your changes.

When downloading the repository from `git`, a few of the PHPUnit tests related to the importer plugin will fail because the `tests/phpunit/data/plugins/wordpress-importer` directory is not contained in the `git` repositories. Here’s how to fix that:

```
cd /path/to/wordpress-develop
cd tests/phpunit/data/plugins/
svn co \
    https://plugins.svn.wordpress.org/wordpress-importer/trunk/ \
    wordpress-importer
```

### Usage Notes for Git

† If your `trunk` branch has changed since you last worked on your patch (for example, if you’ve pulled down the latest code), you’ll need to [rebase](https://git-scm.com/book/en/v2/Git-Branching-Rebasing) your branch against the latest code. This is a great way to keep your patches up to date, and it’s much easier with Git than with svn. Here is an example sequence of commands to update your `trunk` branch then refresh your patch on top of the latest code (make sure you have [no uncommitted changes in your repository](https://stackoverflow.com/questions/52704/how-do-i-discard-unstaged-changes-in-git) first):

```
git fetch origin
git checkout origin/trunk -B trunk
git checkout 30000-add-more-alots
git rebase trunk
git diff trunk 30000-add-more-alots > 30000.x.diff
```