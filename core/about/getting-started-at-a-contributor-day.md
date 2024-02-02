# Getting Started at a Contributor Day

*This guide is intended to help you get started at a contributor day. It includes a schematic outline of what the group does and how to quickly get started. If you need any help, talk to the contributor day organizer, or ask your question in the [#core](https://make.wordpress.org/core/tag/core/) channel in [Slack](https://chat.wordpress.org/).*

*This is a work in progress so don’t be afraid to amend the document or leave comments, particularly if you’re at a contributor day and find that we’ve missed something.*

**Regular Meeting Time:** Wednesdays at 21:00 UTC  
**New Contributor Meetings:** 2nd and 4th Wednesdays at 19:00 UTC**  
Where:** [#core](https://make.wordpress.org/core/tag/core/) channel on [Slack](https://chat.wordpress.org/)

## Group responsibilities

The responsibilities of the core group are:

*   To maintain the code and develop it for the future
*   Develop new features for WordPress
*   Maintain and improve design and UX
*   Design, develop, and maintain default themes
*   Maintain the utilities used to develop core
*   Maintain the bundled packages of default plugins
*   Maintain the bundled libraries available in core
*   Maintaining the bug tracker

## Common Tasks

As a member of the core group, some common tasks that you’ll carry out are:

*   Testing patches and fixing bugs
*   Handling stability and security issues
*   Code new features
*   Work on the user interface
*   User testing for new features
*   Writing unit tests to keep WordPress stable
*   Bug gardening
*   Review patches for [Coding Standards](https://make.wordpress.org/core/handbook/coding-standards/)
*   Review patches for accessibility and privacy concerns

## Prior Knowledge

Prior knowledge that you’ll find helpful for working on core is:

*   Grasp of whatever coding language you want to help out with, e.g. CSS, PHP, Javascript or React
*   Familiarity with WordPress is beneficial but you don’t need a deep understanding of core to get started

## Tools

*   A version control system: either [SVN](http://sourceforge.net/projects/win32svn/) or [Git](http://git-scm.com/)
*   a local development environment; for example, [MAMP](http://www.mamp.info/en/index.html), [WAMP](http://www.wampserver.com/en/), [Vagrant](//www.vagrantup.com/) [XAMPP](http://www.apachefriends.org/index.html), or [WP-ENV](https://make.wordpress.org/core/2020/03/03/wp-env-simple-local-environments-for-wordpress/)
*   for unit testing, [PHPUnit](http://phpunit.de/)
*   [Grunt](http://gruntjs.com/) for compiling assets, building release packages, and JavaScript and PHP testing
*   [QUnit](http://qunitjs.com/) for Javascript testing
*   [WPCS](https://github.com/WordPress/WordPress-Coding-Standards) rules for [PHP\_CodeSniffer](https://github.com/squizlabs/PHP_CodeSniffer)

## Essential Reading

*   Sections of the [Core Contributor Handbook](https://make.wordpress.org/core/handbook/) relevant to what you’re working on
*   If you’re writing code, the [WordPress Coding Standards](https://make.wordpress.org/core/handbook/coding-standards/)

## First Steps

The first step is to get set up with a local environment:

1\. Install SVN: [Installing a VCS](https://make.wordpress.org/core/handbook/tutorials/installing-a-vcs/)  
2\. Install a local server: [Mac](https://make.wordpress.org/core/handbook/tutorials/installing-a-local-server/mamp/) | [Windows](https://make.wordpress.org/core/handbook/installing-a-local-server/installing-xampp/) | [Windows](https://make.wordpress.org/core/handbook/tutorials/installing-a-local-server/wampserver/) (alternative)  
3\. [Check out the WordPress codebase using SVN](https://make.wordpress.org/core/handbook/tutorials/installing-wordpress-locally/from-svn/)

After that:

*   If you find an issue with WordPress you can [Open a ticket on Trac](https://make.wordpress.org/core/handbook/working-with-trac/opening-a-ticket/)
*   [Fix a bug](https://make.wordpress.org/core/handbook/fixing-bugs/)
*   [Create and apply a patch](https://make.wordpress.org/core/handbook/tutorials/working-with-patches/)

There are other ways that you can help out:

*   [Bug gardening](https://make.wordpress.org/core/handbook/bug-gardening/)
*   If a beta or release candidate is available try out some [Alpha or Beta testing](https://make.wordpress.org/core/handbook/testing/beta/)
*   [Writing unit tests](https://make.wordpress.org/core/handbook/automated-testing/)
*   If you want to help out with a UI\-centric feature, check out the [features as plugins information](https://make.wordpress.org/core/features-as-plugins/)
*   If you want to focus on a specific Component, check out the [WordPress Core Components](https://make.wordpress.org/core/components/) listing.

## Tasks

Some easy tasks for a first time contributor to get started at a contributor day are:

*   Check the [good first bug tag](https://core.trac.wordpress.org/query?status=!closed&keywords=~good-first-bug) for easy wins
*   Update the [Inline Docs](https://developer.wordpress.org/coding-standards/inline-documentation-standards/)
*   Work on the user interface, check out the [UI focus](https://core.trac.wordpress.org/focus/ui)
*   Provide [Developer feedback](https://core.trac.wordpress.org/tickets/dev-feedback)
*   Provide [Design feedback](https://core.trac.wordpress.org/tickets/ux-feedback)
*   Provide [Copy feedback](https://core.trac.wordpress.org/query?status=accepted&status=assigned&status=new&status=reopened&status=reviewing&keywords=~needs-copy-review&col=id&col=summary&col=status&col=owner&col=type&col=priority&col=milestone&order=priority)
*   Provide [Privacy feedback](https://core.trac.wordpress.org/query?status=accepted&status=assigned&status=new&status=reopened&status=reviewing&keywords=~needs-privacy-review&col=id&col=summary&col=status&col=owner&col=type&col=priority&col=milestone&order=priority)
*   [Refresh an existing patch](https://core.trac.wordpress.org/query?status=accepted&status=assigned&status=new&status=reopened&status=reviewing&keywords=~needs-refresh&col=id&col=summary&col=status&col=owner&col=type&col=priority&col=milestone&order=priority) that doesn’t apply or needs an update.
*   Try your hand at [bug gardening](https://make.wordpress.org/core/handbook/bug-gardening/) (Helen has a [good post to help you get started](http://helen.wordpress.com/2013/08/09/scared-of-wordpress-core-trac-but-want-to-give-it-a-shot-try-trac-gardening/))

## **Gutenberg Contributions**

### **Prerequisites**

*   A local dev environment running WordPress (we suggest [VVV](https://varyingvagrantvagrants.org/docs/en-US/installation/software-requirements/))
*   Latest [npm](https://nodejs.org/en/download/package-manager/) version. 

If you are unsure if you are on the latest npm version, run the following command:

```bash
 npm install npm@latest -g 
```

*    Docker – https://docs.docker.com/install/

A handy guide to setting up your local environment can be found in [**Contributing.md**](https://github.com/WordPress/gutenberg/blob/trunk/CONTRIBUTING.md) in the Gutenberg github repository. There you will find commands to help get your local environment up and running.  

Largely, the setup process can be finished end to end by running the following command from the Gutenberg directory (Powershell works well if you are on Windows.):

```bash
./bin/setup-local-env.sh
```

The script will go step by step through the process of validating prerequisites are met. If there is something missing, the script will report what needs to be done to complete the setup. Re running the script a few times after making the suggested changes will complete setup.  

Once you have the development version of Gutenberg running on your local environment you will need to run the following from within the Gutenberg directory:

```bash
npm run dev
```

This will monitor/update changes you make.  

***In order to avoid huge downloads at WordCamp Contributor Days it is recommended that the environment is configured before the event.***  

### **Good First Gutenberg Issues**

If you are looking for some unassigned first issues to get familiar with contribution to Gutenberg, [look here](https://github.com/WordPress/gutenberg/issues?utf8=%E2%9C%93&q=is%3Aopen+is%3Aissue+label%3A%22Good+First+Issue%22+-label%3A%22%5BStatus%5D+In+Progress%22+no%3Aassignee).

### **Gutenberg First issue steps**

1.  Fork the Gutenberg repository to your own account.
2.  Clone your fork locally to your ‘plugins’ directory using \`git clone\`
3.  Create a new branch in your fork with the the issue number somewhere in the branch name (example: ***\`fix-admin\-align-center-12306\`*** would be a good branch name for issue: ***“Latest Posts block “align center” has no effect in admin [#12306](https://core.trac.wordpress.org/ticket/12306)”)***
4.  Make an initial commit 
5.  Publish your branch using: 

```bash
git push -u origin <branch name>
```

Now you are ready to make your changes locally to fix the issue. When finished, commit your changes and push them to your branch.  

If you are ready to submit your changes for review to merge into Gutenberg, simply create a pull request via github.com by navigating to your branch. Create pull request and fill out the information requested in the form.