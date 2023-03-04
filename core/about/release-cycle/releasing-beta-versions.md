# Releasing Beta and RC Versions

These are the prescribed steps to take when releasing a beta version of WordPress. As you go through this process, please add any missing information to the steps below so future contributors have an easier experience.

*   Draft the announcement post.
    *   Copy a previous [wordpress.org/news/](https://wordpress.org/news/) post and start editing from there (e.g., [Beta 1](https://wordpress.org/news/2021/06/wordpress-5-8-beta-1/), [Beta 2](https://wordpress.org/news/2021/06/wordpress-5-8-beta-2/), [RC 1](https://wordpress.org/news/2021/06/wordpress-5-8-release-candidate/), [RC 2](https://wordpress.org/news/2021/07/wordpress-5-8-release-candidate-2/)).
    *   When drafting the post, ensure you check the “Enable public preview” option in the “Status & visibility” sidebar panel so you can copy and share that preview URL with others to help review and provide feedback before publishing.
    *   Ensure links, ticket counts, and other aspects are updated for your specific beta release. For Trac query links, ensure any dates in the URL are in the `YYYY-MM-DD` format for cross-locale compatibility.
    *   Obtain reviews for accuracy from release leads and copyediting from marketing or documentation folks. Ensure these folks get @mentioned at the end of the post.
    *   Note that if this Beta/RC release was originally unplanned (e.g., an additional Beta before RC, an additional RC before final release), then historically these announcement posts as “silent” in that they are not published on [wordpress.org/news/](https://wordpress.org/news/) and instead on [make.wordpress.org/core](https://make.wordpress.org/core/) (e.g., [5.7 RC 3](https://make.wordpress.org/core/2021/03/05/wordpress-5-7-release-candidate-3/)).
*   For Beta 1 releases, it is strongly recommended to coordinate with the FSE Outreach Experiment folks in [#fse-outreach-experiment](https://make.wordpress.org/core/tag/fse-outreach-experiment/) to publish and promote a “Help Test WordPress X.Y” post (e.g., [6.1 post](https://make.wordpress.org/test/2022/09/21/help-test-wordpress-6-1/), [6.1 Slack message](https://wordpress.slack.com/archives/C015GUFFC00/p1663781207569069)).
*   For Beta releases, ensure that the milestone is cleared of enhancement and feature request tickets (e.g., [Trac query for 6.1](https://core.trac.wordpress.org/query?status=accepted&status=assigned&status=new&status=reopened&status=reviewing&type=enhancement&type=feature+request&milestone=6.1&col=id&col=summary&col=status&col=owner&col=type&col=priority&col=milestone&order=priority)). If there is agreement within the release squad that a certain enhancement or feature request is critical for the release and thus needs to remain in the milestone, its ticket type should be changed to “Task (blessed)”. Also ensure with the Editor Tech Lead that enhancements/features merges from Gutenberg are similarly either cleared from the milestone or changed to a “Task (blessed)”.
*   For RC releases, ensure that the milestone is cleared of all tickets or otherwise have agreement within the release squad as to why any remain (e.g., [Trac query for 6.1](https://core.trac.wordpress.org/query?status=accepted&status=assigned&status=new&status=reopened&status=reviewing&milestone=6.1&col=id&col=summary&col=type&col=status&col=milestone&col=owner&col=priority&order=priority)). Also ensure with the Editor Tech Lead that all merges from Gutenberg are also cleared from the milestone.
*   Before starting, run all unit tests locally.
    *   Ensure NPM packages are updated locally to reflect the latest changes before running these tests
    *   `phpunit --stop-on-failure`
    *   `phpunit --group ajax --stop-on-failure`
    *   `phpunit -c tests/phpunit/multisite.xml --stop-on-failure`
*   For [Minor releases](https://make.wordpress.org/core/handbook/about/release-cycle/releasing-minor-versions/), verify that all closed tickets in the milestone have had their commits merged into the release (looking for tickets that lack `fixed-major` can narrow this down). Minor releases may optionally include beta releases. The decision is at the discretion of the release lead.
*   Announce in [#core](https://make.wordpress.org/core/tag/core/) so nobody tries to commit.
    *   Example ([archive](https://wordpress.slack.com/archives/C02RQBWTW/p1495228675132277)): @committers Please refrain from committing until we get 4.8-beta2 released.
*   Remind those attending the release party to not share links to the release package until after it’s been tested.
    *   Example ([archive](https://wordpress.slack.com/archives/C02RQBWTW/p1584479009394600)): **Reminder: Please do not share links to the package publicly until the all-clear is given after testing and the announcement post is published on WordPress.org.**
*   Verify latest GitHub Action checks are passing (i.e., all show ✅).
    *   Check the latest commit on https://github.com/WordPress/wordpress-develop/actions?query=event%3Apush+branch%3Atrunk
*   For Minor releases, check out the release branch: `svn switch '^/branches/4.7'` and remind people to update their current install or make a fresh install.
*   Ask a member of the Security team to run the private security unit test suite to make sure no regressions are introduced.
    *   If any are found, avoid discussing the details publicly, because some sites (like wordpress.org) run `trunk` or beta/RCs in production. Instead, notify the Security team privately.
*   Bump version.
    
    *   Update the `$wp_version` in `trunk/src/wp-includes/version.php` (e.g., $wp\_version = ‘5.8-beta1-src’;).
    *   Update the `version` in the `package.json` if it hasn’t been updated yet.
    *   If the `$wp_version` is `4.8.1-beta1` then the `version` in `package.json` should be just `4.8.1`.
    *   If you are releasing an RC, then the `$wp_version` would be `4.8.1-RC1-src`.
    *   Update `$wp_version` to add the appropriate version identifier and remove the SVN changeset number:![](https://make.wordpress.org/core/files/2017/06/pasted-image-0-1024x470.png)
    
    *   Ensure version bump appears on https://build.trac.wordpress.org/. *This only needs to be verified by the person releasing via Mission Control*.
*   Build the packages.
    
    *   The release package needs to be built in [Mission Control](https://mc.wordpress.org/release/). Once it’s packaged, it needs to be tested well, including manually testing updates. (How do you do that? Checkout the [docs](https://make.wordpress.org/core/handbook/about/release-cycle/releasing-minor-versions/#testing-packages).)
    
    *   Enter build name?
    *   Click button?
*   Test the packages.
    
    *   Ask people to [test](https://make.wordpress.org/core/handbook/about/release-cycle/releasing-minor-versions/#testing-packages) by sharing the URL (e.g., [https://wordpress.org/wordpress-4.9-beta2.zip](https://wordpress.org/wordpress-4.9-beta2.zip)).
    *   There are three ways to help test the package:
        *   Install and activate the [WordPress Beta Tester](https://wordpress.org/plugins/wordpress-beta-tester/) plugin
            *   For major RC releases, select the `Bleeding edge` channel and then `Beta/RC Only` stream.
            *   For a minor RC release, select the Point Release channel and the Nightlies stream (note that it is no longer possible to use beta tester to test the minor Beta/RC packages until after the nightlies have been built).
        *   Use WP-CLI to test: `wp core update https://wordpress.org/wordpress-4.9-beta2.zip`
        *   Directly download the Beta/RC version (e.g., https://wordpress.org/wordpress-5.8-RC4.zip)
    
    *   Note: If anyone reports files removed when updating via WP-CLI, make sure you verify that those files exist in the `$_old_files` variable.
    *   Note: Folks testing packages using the WP-CLI may report warnings related to checksums. This is expected because checksums are not available for nightlies.
    *   Ideal tests to run:
        *   Test from latest in 4.0.\* release series (e.g., 4.0.35 > 6.1 Beta 1)
        *   Test from latest in 4.9.\* release series (e.g., 4.9.21 > 6.1 Beta 1)
        *   Test from latest in current major release series (e.g., 5.7.2 > 5.8 Beta 2)
        *   Test from most recent Beta/RC release (e.g., Beta 2 > Beta 3, Beta 3 > RC 1, RC 1 > RC 2)
        *   Test fresh install
        *   Remove `wp-config.php` file and test fresh install
        *   Test single site and multisite/network (both subdirectory and subdomain) installs
*   Another version bump.
    *   Commit: Post WordPress 4.8 Beta 2 version bump.![](https://make.wordpress.org/core/files/2017/06/pasted-image-0-1-1024x547.png)
*   The nightly package now needs to be rebuilt in [Mission Control](https://mc.wordpress.org/release/) after the previous commit appears at [https://build.trac.wordpress.org/](https://build.trac.wordpress.org/)
*   Publish the announcement post (and the subsequent “Help Test WordPress X.Y” post if this is the Beta 1 release and a post was created).
    *   Matt can do this, or anyone with Admin or Editor access to [wordpress.org/news/](https://wordpress.org/news/).
    *   Share the post content in the [#polyglots](https://make.wordpress.org/core/tag/polyglots/) channel to help them generate translated versions (e.g., [Slack message for 6.1 Beta 1](https://wordpress.slack.com/archives/C02RP50LK/p1663780990205979) sharing the `code editor` content).
*   Announce in [#core](https://make.wordpress.org/core/tag/core/) that release is available.
    *   Example: /here WordPress 5.8 Beta 1 is now available. Please help test! There’s a *lot* to test this release.
    *   As a reminder, only tickets related to functionality added in 5.8, test changes, and documentation updates will be considered during beta this release.
*   Announce to Committers that SVN committing in [#core](https://make.wordpress.org/core/tag/core/) is open.
    
    *   Example: [@committers](https://wordpress.slack.com/admin/user_groups) Feel free to resume committing.
    
    *   For RC releases, note the `dev-feedback` and `dev-reviewed` workflow is required prior to committing, where each commit must get double-signoff.
        *   Example: [@committers](https://wordpress.slack.com/admin/user_groups) Feel free to resume committing. Reminder that we are now in the RC period so all commits will require double-signoff using the `dev-feedback` and `dev-reviewed` Trac keywords on each ticket.
*   Write a message in the [#props](https://wordpress.slack.com/messages/C0FRG66LR) channel thanking and giving props to everyone who tested or otherwise helped with the beta release process
    *   Example: Props to @mention, @mention2, …, @mentionN for helping test today’s 5.8 Beta 1 release!
*   For first Beta in the release cycle:
    *   Add a new Milestone to Core Trac for the next release version. For example, when releasing WordPress `5.0`, add a Milestone for `5.1`. *You may need to ask someone with admin rights on Trac to do this.*
    *   A member of the Security team should email participants in our HackerOne program, encouraging them to [find any new vulnerabilities before they make it into the stable release](https://make.wordpress.org/security/2019/02/13/doubling-bounties-for-vulnerabilities-discovered-before-release/). See the Security Team handbook for details.
*   For first RC in the release cycle:
    *   An announcement should be made on Make Core about the release candidate phase ([example from 6.0](https://make.wordpress.org/core/2022/05/04/wordpress-6-0-release-candidate-phase/)) and the various above protocols in order to better amplify this specific part of the release cycle and prepare the community.

[#props](https://make.wordpress.org/core/tag/props/)