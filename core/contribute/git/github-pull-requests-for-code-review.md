# GitHub Pull Requests for Code Review

WordPress development uses SVN, but many contributors prefer to work in Git though GitHub. Many contributors create pull requests using their own forks of the official [WordPress Develop mirror](https://github.com/wordpress/wordpress-develop) so that they can use features like continuous integration and inline code commenting.

An experimental feature has been added to Trac that will let you link GitHub pull requests opened against the official [WordPress Develop Git mirror](https://github.com/wordpress/wordpress-develop) to tickets. This makes GitHub contributions more visible directly in their related Trac tickets and makes collaborating across the two repositories easier.

**Note:** Pull requests on GitHub will **not** be merged. Code changes are still required to be made to the SVN repository by trusted long term contributors granted commit access.

## Link your WordPress profile to GitHub

*   [Edit your WordPress profile](https://profiles.wordpress.org/me/edit)
*   Navigate to the “Account & Security” tab
*   In the “Connections” section, click the link to connect your account
*   Once redirected to GitHub approve the connection
*   You will then be redirected back to your WordPress profile page

## In GitHub

*   Fork the official [WordPress Develop mirror](https://github.com/wordpress/wordpress-develop) on GitHub.
*   Create a branch on your fork, work on your changes, commit, and push.
*   Open a PR to [wordpress-develop](https://github.com/wordpress/wordpress-develop) with the full URL for the Trac ticket in the PR body. For example:
    
    > See https://core.trac.wordpress.org/ticket/49295
    
*   To make collaboration easier, make sure to check the “Allow edits and access to secrets by maintainers”. This will allow WordPress Core committers to push directly to the branch on your fork with larger suggested changes.

![](https://make.wordpress.org/core/files/2020/02/example-github-pr-1024x602.png)

## In Trac

*   The PR will be displayed below the attachments area on tickets with the following information:
    *   How many lines were modified
    *   Status of the PR checks (Draft/Closed, Travis CI, merge conflicts, etc.)
    *   A button to view the PR
    *   A button to view the raw diff
*   A bot comment will be added to the ticket’s timeline of events indicating when the ticket was mentioned and where.
*   Every time the PR receives a comment, a PR bot will post the comment onto the Trac ticket.

![A screenshot of a WordPress Core Trac ticket with the new linked Pull Requests between the ticket attachments and comments.](https://make.wordpress.org/core/files/2020/02/Screen-Shot-2020-02-20-at-20.42.53.png)

Pull requests show between Attachments and Change History.

## Important Notes

**When the PR bot syncs comments over to Trac, it will not trigger an email notification to the subscribers of the Trac ticket.** For this reason, it is recommended to provide some type of ticket update in Trac itself. Most likely there will be a need to update the keywords anyway (add has-patch or needs-testing, etc.).

**Inline comments made during a code review on the PR will not be posted to the Trac ticket.** These comments are contextual to specific lines at a specific state (commit) of a PR and would seem out of place as the branch’s code is iterated.

**Pull requests on GitHub are not monitored.** No one will be checking for new pull requests regularly. Pull requests **must** be attached to a Trac ticket to be considered for inclusion in WordPress Core.

**Clean up after yourself occasionally.** Right now, PRs are not automatically closed when the associated Trac ticket is resolved. If you open a PR, do your best to close PRs that have been merged into Core whenever you are able to.

And finally, **this is an experiment.** There will likely be some small bugs and things that can be improved since this is the first iteration. Please open up tickets in [Meta Trac](https://meta.trac.wordpress.org/) for any issues that you find. All feedback is welcome!