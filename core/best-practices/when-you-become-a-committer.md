# When you become a committer

Welcome to being a committer! Here are some things you should know:

*   Make sure you have a strong password: it should be long, random, and stored in the password manager of your choice.
    *   Bad: X\*7z7XL{kZvky7E(
    *   Good: aLy%t;67zvy3VdFwVPKA@VGV?i7oq.63Lj.2aKZ@Tw3\].Eu4kVUJJVGyXH7oRL\*a
*   Make sure you have two-factor auth enabled for GitHub and your WordPress.org account. It’s also a very good idea to enable it for any service you use, since hackers will often leverage access to a low priority account to gain access to a high priority account.
*   Join the [#core-committers](https://make.wordpress.org/core/tag/core-committers/) channel on Slack.  This channel is for onboarding and questions from committers about the act of committing, tips and tricks for SVN, etc. You’re welcome and encouraged to ask here whenever you have a question about committing (e.g., SVN syntax, backports, etc). Anything that is relevant to non-committers (e.g., whether or not a patch is ready for commit, project philosophy, proposals, etc) should still take place in [#core](https://make.wordpress.org/core/tag/core/) to avoid excluding other contributors.
*   Please add `svnusername@git.wordpress.org` (e.g.`pento@git.wordpress.org`) to your GitHub account: https://github.com/settings/emails . This will allow the new GitHub mirror (https://github.com/WordPress/wordpress-develop) to correctly attribute your commits. GitHub will try to send a verification email, but it won’t be delivered. There’s no need to verify this email address for commit attribution purposes.
*   Read through [this guide on commit messages](https://make.wordpress.org/core/handbook/best-practices/commit-messages/) for a primer on what’s considered best practices.

Some things to know when making your first few commits:

*   Please ask a relevant committer to peer-review your first few prospective patches and commit messages before you commit them. This serves as a safety check to make sure you know what to look out for before you actually commit. It also gives you a chance to ask any questions you have about process, standards, norms, etc.
*   It can also be a good idea to ask for peer-review from another committer whenever you have any doubts about a patch, especially if you’re committing outside an area that you normally work on.

And finally some other general things to keep in mind as a Core Committer:

*   When attending contributor day of WordCamps, you are strongly encouraged to commit someone else’s code, ideally, an attendee that is there working on a patch. It’s also good to encourage inactive committers to dip their toes back in at these events.

## Tasks to add a committer

*   Ensure the committer has completed the above steps.
*   On a WordPress.org Sandbox, add them to the following lists:
    *   `/home/svn/etc/develop.svn.wordpress.org` in Deploy SVN
    *   `$committers` in `.config/capes.php`
    *   `wpTracContributorLabels` in the [Trac SVN](https://meta.svn.wordpress.org/sites/trunk/trac.wordpress.org) file `templates/core/site-specific.html`
*   Additionally, add them to the following groups:
    *   The Core Committers user group in WordPress Slack
    *   The [WordPress Core Team](https://github.com/orgs/WordPress/teams/wordpress-core) on GitHub
    *   The Committer group on [Core Trac](https://core.trac.wordpress.org/admin)
*   Add them to the [Current Committers list on the Project Organization page](https://make.wordpress.org/core/handbook/about/organization/) of the handbook.
*   Make sure the committer is an editor on this site
*   If the committer will be working on security issues, refer to the Security Team handbook for onboarding tasks.