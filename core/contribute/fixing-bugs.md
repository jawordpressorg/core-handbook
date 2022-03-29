# Fixing Bugs

A great way to contribute to the development of WordPress is to help patch bugs. Having a good working knowledge of PHP, JavaScript, or CSS is recommended.

First, if you have found a bug in WordPress, please make sure you [report it](https://make.wordpress.org/core/handbook/testing/reporting-bugs/). Please [search Trac](https://core.trac.wordpress.org/search) first to see if the bug has already been reported before creating a new ticket.

Once you’ve either found an existing Trac ticket or created a new ticket for the bug, you can get to work.

If you want to help, but don’t know which bugs to fix, review the [Finding Bugs to Fix](#finding-bugs-to-fix) section below.

## Overview

WordPress uses Subversion for source control. You will want to *check out* a working copy of WordPress using a Subversion client (such as Tortoise SVN on Windows, using the command line on Mac and Linux). For more, read the [Subversion](https://make.wordpress.org/core/handbook/svn/) article.

One of the many benefits to using a version control system is that you can create a simple text file, called a [patch](https://make.wordpress.org/core/glossary/#patch), that shows exactly what you’ve changed – the lines of code you added, modified, and removed. A patch is also called a *diff*, for differences.

If you are not familiar with how WordPress is written and organized, read the article on [the WordPress Codebase](https://make.wordpress.org/core/handbook/contribute/codebase/).

Once you’ve figured out how to fix the bug by modifying WordPress core files, you should create a *patch*. Review the [Creating a Patch](https://make.wordpress.org/core/handbook/submitting-a-patch/ "Creating a Patch") documentation.

Once you’ve created a patch, upload it to the Trac ticket using the *Attach file* button, and add *has-patch* to the workflow keywords. Please don’t overwrite any existing, previous patches.

## Finding Bugs to Fix

If you want to fix bugs in the core parts of WordPress, but don’t know what to fix, here are some suggestions on finding one:

*   Try starting with tickets that have been [tagged with the ‘good-first-bug’ keyword](https://core.trac.wordpress.org/tickets/good-first-bugs). They’re great for getting familiar with the process before attempting to solve more complicated problems.
*   Look through the [ticket report for the latest release](https://core.trac.wordpress.org/report/6), in particular the **Needs Patch** group.
*   Look through the [ticket report for “early” tickets](https://core.trac.wordpress.org/report/14). These tickets have been marked by contributing developers as needing attention early in the WordPress release cycle. Generally, this means a trusted core contributor has shown interest in it, “blessing” the ticket to a certain extent.
*   Look through the [Awaiting Review report](https://core.trac.wordpress.org/report/40). These tickets have not yet been slated for the next release of WordPress, but if a developer takes an interest in it, that can change.
*   There are individual reports of tickets for a number of specialized areas: you may be interested in writing unit tests (see [Automated Testing](https://make.wordpress.org/core/handbook/automated-testing/)), working on or providing feedback for [user interfaces and user experiences](https://core.trac.wordpress.org/report/35), [tickets of interest to the mobile development team](https://core.trac.wordpress.org/report/42), and [tickets requiring more documentation in the Codex](https://core.trac.wordpress.org/report/36).
*   If you are interested in tickets from a particular component, you can use the [Query](https://core.trac.wordpress.org/query) feature of Trac. For example, [all open XML-RPC tickets](https://core.trac.wordpress.org/query?status=!closed&component=XML-RPC), all [open Multisite](https://core.trac.wordpress.org/query?status=!closed&component=Multisite&group=milestone) tickets grouped by milestones, and all [open Accessibility tickets](https://core.trac.wordpress.org/query?status=!closed&component=Accessibility).
*   The WordPress development team has daily discussions on bug triage, and weekly project meetings. For dates and times, see the sidebar on [Make WordPress Core](https://make.wordpress.org/core/).
*   Consider joining the [wp-trac](http://lists.automattic.com/mailman/listinfo/wp-trac) mailing list to follow the discussions in every Trac ticket. Also follow along on [Make WordPress Core](https://make.wordpress.org/core/), and potentially [other Make WordPress blogs](http://make.wordpress.org).