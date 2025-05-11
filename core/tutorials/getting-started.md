# Getting Started

This page gives you a clear guide on what you need to do in order to get started with contributing to WordPress core. Below you will find a list of items that need to be taken care of, with links leading to more specific tutorials on the individual steps.

Everything described here is recommended to efficiently contribute to WordPress core. Where possible, different choices are highlighted to leave enough flexibility to account for your typical workflows. If you are planning to join a contributor day in the WordPress core team, following these steps in advance will ensure you maximize your outcome of that day since often-times several of them can be time-consuming during contributor days, particularly due to slow internet connections.

## Joining communication channels

Communication in WordPress commonly happens either asynchronously on Trac, which is the issue tracker used by the project, or in live chat on Slack, which is a popular instant messaging service used by many organizations. Here is how you get access to these two tools:

1.  [Sign up for a wordpress.org account](https://login.wordpress.org/register) and complete the instructions. You may optionally sign up at [gravatar.com](https://gravatar.com/) with the same email address if you’d like to have a profile picture (recommended). This account can be used for all contributing activities.
2.  In order to join the international WordPress Slack team and thus be able to participate in core team meetings and other discussions, you need to receive an invite. Visit the [WordPress + Slack page](https://make.wordpress.org/chat/) while being logged in with your wordpress.org account, and click the link to receive the invite per email.
3.  Via the email, log in to the [Slack team](https://wordpress.slack.com). For email address, use `{username}@chat.wordpress.org` where `{username}` is your user name you picked for wordpress.org. If possible, pick the same username for Slack.

## Setting up your development environment

In order to contribute to WordPress core, you need a local development environment and a checkout of WordPress trunk, which is the development version of WordPress. Be aware that this is *not* the same as the latest downloadable WordPress release.

### Setting up a local server

Check out [options to download and install a local development environment](https://make.wordpress.org/core/handbook/contribute/#local-development-overview) on your machine.

### Setting up a version control system

Install a version control system to use for WordPress core. Here you have two options:

*   WordPress core by default uses Subversion (or SVN) for version control, which works relatively similar to Git, but is a little older. While most people prefer working with Git, the SVN commands you typically use when developing for WordPress core are trivial and almost the same as their Git counterparts. If you are using a [local environment like VVV](https://make.wordpress.org/core/handbook/contribute/#local-development-overview) your environment may already have SVN pre-installed. If you are using another environment or prefer to also use SVN directly on your computer, there is a [handbook tutorial guiding you through the process](https://make.wordpress.org/core/handbook/tutorials/installing-a-vcs/).
*   Alternatively, you can install Git from the [Git project website](https://git-scm.com/). On many environments, for example VVV, you will already find it pre-installed. If you prefer using a visual UI in addition, feel free to use a client app such as [Sourcetree](https://www.atlassian.com/software/sourcetree), or [GitHub Desktop](https://desktop.github.com/) (which works particularly well when used together with GitHub).

### Setting up the WordPress development repository

Set up the development version of WordPress in your development environment. How you proceed depends on whether you decided to use SVN or Git for version control in the second step:

*   If you are [cloning from GitHub](https://github.com/WordPress/wordpress-develop) and using the built-in [Docker](https://www.docker.com/) environment, you can run `npm run env:start` and `npm run env:install` from your WordPress Develop repository checkout to start a local server on `localhost`.
*   If you are using SVN and VVV, everything is already setup after the initial booting process. You can access your development version of WordPress under [http://src.wordpress-develop.test](http://src.wordpress-develop.test) with your VVV running. If you’re using SVN on another environment than VVV, please [follow the instructions on how to install WordPress from SVN](https://make.wordpress.org/core/handbook/tutorials/installing-wordpress-locally/from-svn/).
*   If you’re using Git and VVV, please [follow the optional instructions on how to change the included WordPress development repository to use Git instead of the default SVN](https://make.wordpress.org/core/handbook/tutorials/installing-a-local-server/installing-vvv/#5-create-github-repo-optional). If you’re using Git on another environment than VVV, create a GitHub fork of the [WordPress/wordpress-develop](https://github.com/WordPress/wordpress-develop) repository. Afterwards, you can proceed with the above instructions, just skip the first three points and instead of using develop.git.wordpress.org as upstream repository, use the GitHub version.

And with that, you’re ready to get started with contributing!

## What is next?

If you plan to attend a contributor day, the above prerequisites will give you a jumpstart so that you can immediately focus on learning how to actually contribute. If you are not visiting this page because you are going to attend a contributor day or if you are already interested in diving in deeper, the best way to proceed is to [learn more about why contributing to core is important and which processes are involved](https://make.wordpress.org/core/handbook/contribute/). In case you immediately prefer working with tickets instead, [this introduction to Trac will help you get familiar](https://make.wordpress.org/core/handbook/tutorials/trac/new-user-quick-start/).