# Contribute with Code

Alert: This page is being actively worked on, expanded, and improved.

Thank you for your interest in contributing to WordPress! This Quick Start Guide to contributing code to WordPress Core is a central hub where you can find all resources needed to take you through the process of submitting your first patch.

Note: Interested in contributing to another part of WordPress? Visit [make.wordpress.org](https://make.wordpress.org) to see the many ways you can contribute to WordPress.

This guide is geared toward new contributors, giving you quick access to resources and answering some of the more common questions new contributors have when diving in. As a collaboration between new and veteran contributors, this guide has been developed to better identify the pain points in getting started and will be continuously updated with improvements.

Tip: There are no wrong questions. The WordPress community is always more than happy to help. Have questions along the way? Join #coreCore Core is the set of software required to run WordPress. The Core Development Team builds WordPress. in SlackSlack Slack is a Collaborative Group Chat Platform [https://slack.com/](https://slack.com/). The WordPress community has its own Slack Channel at [https://make.wordpress.org/chat/](https://make.wordpress.org/chat/). and ask away.

Before starting to contribute, it’s important to understand a bit of background on why people contribute and how we interact online.

## Why Contribute?

It is *vital* for the future success of WordPress to have a healthy group of contributors. There are many open tickets containing great ideas and many ask why these great ideas have not been implemented. The simple answer is that WordPress relies on people like you to turn those ideas into reality. WordPress is a user- and volunteer-driven project; every enhancement and each improvement depends on the community.

## We’re All Human

When contributing to WordPress, it’s important to remember that everyone is human. We all come from varying backgrounds and speak a variety of languages. There are a number of roles within the core contributor community, ranging from bug gardeners to committers, and each helps move the development process forward. Contributors are easily accessible and, as a result, expect a high level of respect, which they in turn provide to the community-at-large.

As mentioned, one big difference between WordPress and other communities is that WordPress contributors are very accessible. Looking for a lead developer or committer? Ask them a question in a public channel on Slack. Don’t be afraid to approach folks, but keep in mind that contacting people is better through public channels than unsolicited DMs. In Slack, the best place to ask a question about core is [#core](https://make.wordpress.org/core/tag/core/), however there are several sub-channels that discuss specific parts of core. Don’t worry if you’re directed to another channel; we’re here to help!

One of the best places to find contributors is at WordCamps, where you shouldn’t hesitate to approach them. Some WordCamps host contributor days, which is the best time to find a contributor and ask for help.

## Committers

Alert:  This section needs to be expanded. Perhaps we should also include a link to [Nacin’s post](https://nacin.com/2014/02/07/how-wordpress-chooses-committers/).

Committers are a type of WordPress contributor who has earned the trust of the community and been given the keys to “commit” code to WordPress core. Committers use their judgement to commit their own code as well as code from other contributors.

## Component Maintainers

WordPress is organized into a few dozen well-defined, functional areas called [components](https://make.wordpress.org/core/components/). Many contributors take a particular interest in certain areas, whether it is maintaining the [HTTP API](https://make.wordpress.org/core/components/http-api/), improving the [Editor](https://make.wordpress.org/core/components/editor/), or advancing the [Customizer](https://make.wordpress.org/core/components/customize/), among many others.

Contributors that help maintain components are called, logically, component maintainers. These maintainers are vital to keeping WordPress development running as smoothly as possible. Maintainers can take on a number of tasks, including: triaging new tickets, furthering existing tickets, mentoring tasks, pitching new ideas, curating roadmaps, and providing feedback to other contributors. Longtime maintainers have a deep understanding of their area of core and are always seeking to mentor others to impart their knowledge.

Want to help? Get started by following a component you’re interested in. [Adjust your notifications here](https://make.wordpress.org/core/notifications/).

## The Repositories

WordPress primarily uses [Subversion (SVN)](https://make.wordpress.org/core/glossary/#svn), a version control system managed by the Apache project, to manage changes to its codebase.

The [develop repository](https://develop.svn.wordpress.org/trunk/) is available for download. This repository includes core unit tests, build scripts, and by default uses the unminified and unconcatenated Javascript. Everyone has read privileges to these repos.  For more information on the structure of this repository, see the [The Code Repository (SVN)](https://make.wordpress.org/core/handbook/contribute/svn/).

It’s also possible to contribute to WordPress core using `git`. For more information about this process, see [The Code Repository (Git)](https://make.wordpress.org/core/handbook/contribute/git/).

Please note: pull requests submitted to GitHub will not be reviewed or merged there. Please use Trac to submit your patches.

## Patches

While it takes a developer with commit access (called a [committer](https://make.wordpress.org/core/glossary/#committer)) to change the WordPress codebase, anyone can suggest a change in the form of a patch. A [patch](https://make.wordpress.org/core/glossary/#patch) is a special text file that describes changes to code, by identifying the files and lines which are added, removed, and altered. It may also be referred to as a **diff** (after the Unix command to generate a differences file). Patches have the extension of either `.patch` or `.diff` (`.diff` is preferred).

Patches are created using a working copy of WordPress trunk that has been checked out of one of the repositories above. Subversion and Git both keep a history of the code and provide a centralized repository so that committers do not overwrite each others’ changes. (A [conflict](https://make.wordpress.org/core/glossary/#conflict) occurs when a patch changes code that has since been modified.) For this system to work, each committer keeps a working copy of the same repository. Code is checked out as a local working copy, and then checked in ([committed](https://make.wordpress.org/core/glossary/#commit-verb)) to the centralized repository.

Contributors follow the same process, but they generate a patch that shows their changes, since they cannot modify the central repository directly. This patch can then be applied to the individual working copies of other contributors or committers, so it may be reviewed, tested, and potentially committed.

When writing a patch, it is important to always update to the latest version of trunk. Patches should never be written against a released version, such as a tag or branch, with very rare exceptions (e.g. during the preparation of [point releases](https://make.wordpress.org/core/glossary/#point-release)). Trunk is, however, a moving target, which can cause patches to become **stale** and require a **refresh** – they no longer apply properly, because code in the central repository no longer matches what the patch is attempting to change. Patches that alter a significant number of lines or files should generally be brought to the attention of committers sooner rather than later. \[Link: Getting Your Patch Committed\]

## Local Development Overview

In order to contribute to core, we strongly recommend that you install a local instance of WordPress. With WordPress running on your machine, you’ll be able to make changes and test patches without interfering with a live site. There are a variety of ways you can configure a local dev environment. We have tutorials on the following methods: [VVV](https://make.wordpress.org/core/handbook/tutorials/installing-a-local-server/installing-vvv/), [DesktopServer,](https://make.wordpress.org/core/handbook/tutorials/installing-a-local-server/desktopserver/) [MAMP,](https://make.wordpress.org/core/handbook/tutorials/installing-a-local-server/mamp/) [WampServer](https://make.wordpress.org/core/handbook/tutorials/installing-a-local-server/wampserver/), [XAMPP](https://make.wordpress.org/core/handbook/tutorials/installing-a-local-server/xampp/).

If you’re not sure which to choose, we recommend the [VVV (sometimes referred to as Vagrant) method](https://make.wordpress.org/core/handbook/tutorials/installing-a-local-server/installing-vvv/).

## Introduction to Trac

[Trac](https://core.trac.wordpress.org/) is open source software that the WordPress community uses as a bug tracker and project management tool. Using Trac, developers can browse source code history as well as manage bug reports and feature development.

[Tickets](https://make.wordpress.org/core/glossary/#ticket) are used for both bug reports and feature development, and may be created by anyone with a WordPress.org account.

Trac tickets are organized into components (see “Component Maintainers” above), and use keywords to identify further details of the ticket. If your ticket is ever labeled with a keyword you’re unfamiliar with, reference the complete list of [Trac Workflow Keywords](https://make.wordpress.org/core/handbook/contribute/trac/keywords/).

### Good First Bugs

To make it easier for new contributors, some tickets have been marked as [Good First Bugs](https://core.trac.wordpress.org/tickets/good-first-bugs), using the “good-first-bug” keyword. These tickets are not always the easiest to work on, but are self-contained and have support from the core team. Usually, the ticket has been investigated and a path forward has been decided. All that’s left is creating the final patch to commit. Tickets like these help get new contributors (like you!) comfortable with the process of contributing and working in both Trac and development environments.

### Submitting Tickets

Everyone is encouraged to submit bug reports and feature requests directly to trac, but certain tickets are better than others. Here’s some advice on ensuring your ticket is well-formed:

*   Summary – Write a clear summary that sums up exactly what you are reporting or requesting. As you write your summary, a list of related tickets will appear. If you see a ticket that is a duplicate of your issue or feature, there’s no need to file a new ticket. Read through the current ticket and verify that there is no *additional* information you can provide. If you think of something, add your comment.
    *   Bad summary: “Media modal is broken!”
    *   Good summary: “Media modal errors when \_\_\_ is clicked”
*   Description – When reporting a bug be as descriptive as possible. The more descriptive you are, the easier it will be for core contributors to assist you. If applicable, list the steps needed to reproduce the error. If you are submitting a feature request, include a thorough description of your idea, stating use cases and/or user experience improvements.
*   Keywords – Before submitting your ticket, ensure that you have used the keyword “needs-patch” or “needs-feedback” (see Trac Workflow Keywords \[link\] for more information) and set the appropriate component that your ticket applies to. This will help component maintainers as they garden tickets.

### Reporting Security Vulnerabilities

WordPress developers do their best to prevent security issues, but from time-to-time they appear and need to be reported.

It is standard practice to responsibly and privately disclose security issues to the vendor – in this case, the WordPress core development team. WordPress contributors practice responsible disclosure when reporting issues to other vendors as well. Reporting issues responsibly, prior to publishing, gives the vendor time to fix a security vulnerability and minimize damage to users.

In short, be courteous and aware before you file a ticket that might include a security vulnerability. Refer to the [Reporting Security Vulnerabilities](https://make.wordpress.org/core/handbook/testing/reporting-security-vulnerabilities/) page of this handbook for instructions on how to responsibly report issues to the WordPress Security Team.

## Your First Patch

Once you’ve made changes to your WordPress development environment and are happy with those changes, you’ll want to create a patch that can be attached to your trac ticket. There are many ways to do this.

From command line in the SVN root directory (located in the wordpress-develop folder of your VVV instance) you can run this command to generate a patch: svn diff > 00000.diff

There are other, UI\-based ways to create patches as well. [SourceTree](http://www.sourcetreeapp.com/) is an excellent alternative to using the command line. Josh Pollock has [written a tutorial](http://code.tutsplus.com/tutorials/creating-and-submitting-a-patch-to-wordpress-core--cms-20658) on how to create a patch using this method.

WordPress development happens through our official SVN and GIT repositories. As a result, we do not monitor or accept pull requests (PRs) from GitHub. However, you can still create a patch from your git repository and attach the patch to your ticket. To do so:

Alert: We need to add information on creating a GitGit Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency. Git is easy to learn and has a tiny footprint with lightning fast performance. Most modern plugin and theme development is being done with this version control system. [https://git-scm.com/](https://git-scm.com/). patchpatch A special text file that describes changes to code, by identifying the files and lines which are added, removed, and altered. It may also be referred to as a **diff**. A patch can be *applied* to a codebase for testing. here.

### Researching History

Sometimes you may find yourself in a ticket that has been open for many years. More often than not these tickets have patches that need a refresh. It’s important to know why code has changed and how the refresh needs to be handled. If you [browse trunk](https://core.trac.wordpress.org/browser/trunk/src/) you will see that you can view the code of each file that makes up WordPress.

As an example, look at [/wp-admin/media.php](https://core.trac.wordpress.org/browser/trunk/src/wp-admin/media.php). If you follow the link you will see the url at the top of your browser looks similar to the file structure of WordPress. If you append [?annotate=blame](https://core.trac.wordpress.org/browser/trunk/src/wp-admin/media.php?annotate=blame) to the url, the page will load with a new colored sidebar on the left. These are the changesets that have been made to the file. This will help you identify the reasoning the code has changed and allows you to find the ticket associated to better understand the conversation that resulted in the changes. (Usually looks like Fixes:xxxxx)

### Unit Testing

Alert: This section needs to be created. 

### Patch Feedback

When working with tickets and patches, feedback is always encouraged. If you have a question or comment about the direction a ticket or patch is going, add your comment to the ticket.

As mentioned early on this page, WordPress is a global project with contributors from all backgrounds, so please be as respectful and courteous as possible with your feedback. The social norms that apply to your life may be very different than those of other contributors. In turn, be sure to consider how others give you feedback and keep in mind that their comments may come across in a different way than intended due to cultural or lingual differences.

Don’t let this discourage you! From time-to-time, we all give and receive constructive feedback and may take it personally. It’s not personal. Contributors intention is to make WordPress better, just like you!

### Patch Won’t Apply

As mentioned earlier, older tickets often have attached patches that no longer apply to the current codebase. The older the ticket, the lower the likelihood that the associated patch will apply cleanly. If you find a ticket with a patch that does not apply, add the “needs-refresh” keyword to indicate this.

Over time, code shifts around and sometimes these patches only need a bit of reorganization to apply. Other times, you may find code that has been refactored and needs an alternative solution for the proposed bug/enhancement. Once this has been done, create a new patch with the clean code and submit it to the ticket.

(Speaking of refactoring code, the core team almost never takes patches that only refactor code. See the [Code Refactoring](https://make.wordpress.org/core/handbook/contribute/code-refactoring/) page for more information..)

### Commit Ready

Once you think your patch is ready for commit, it’s time to find a committer to review it and commit it to WordPress core. The most appropriate reviewer for your code is usually the component maintainer \[link\] (see above), however any committer can review your patch and commit it.

Another way to get feedback on your patch is to ask for feedback during the “open floor” at the end of the [weekly core developer chat](https://make.wordpress.org/core/tag/agenda/) (see below). If you go this route, be sure to wait until the end of the meeting and not during the chat.

Sometimes, tickets and patches don’t get the attention they need and linger in trac. In these cases, ping a component maintainer or committer and ask for feedback.

## Meetings

Alert:  This section needs to be created.