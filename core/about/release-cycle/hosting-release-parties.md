# Hosting Release Parties

The [WordPress release cycle](https://make.wordpress.org/core/handbook/about/release-cycle/) has several milestones. Once the release hits Beta status, release parties happen in the [#core](https://wordpress.slack.com/archives/C02RQBWTW) Slack channel. These parties step through the various release tasks required to create a public release.

A more technical Handbook page about the process for [Releasing Beta Versions](https://make.wordpress.org/core/handbook/about/release-cycle/releasing-beta-versions/) has technical instructions for committers and Mission Control. This page exists as a guide for the host, or “emcee”, of release parties, and it omits most of the technical detail that’s not needed to facilitate the release process itself.

This page should be updated as processes are improved after receiving feedback from contributors.

## Roles needed during a release party

Note: Some or all of these roles may be performed by the same contributor, depending on availability.

*   **A Party Host** (referred to as `@emcee` in this document). Typically, this is one of the release coordinators. If a release coordinator is not available, an alternate from the release squad can fill in. As a last resort, the role can be filled by a trusted contributor not part of the current squad.
*   **A Core Committer** (`@corecommitter`). This contributor will perform the “version bump” actions. The current list of core committers can be found [here](https://make.wordpress.org/core/handbook/about/organization/#committers).
*   **A member of the Security Team** (`@securityteammember`). This contributor will verify that the non-public security tests pass for the latest set of code set to be released.
*   **A person with Mission Control access** (`@mcpilot`). A contributor with this level of access is needed to package the release and refresh the nightly. The list of active contributors with this access is very small, so finding a person to fill this role ahead of time is crucial.
*   **A member of the marketing team, or a marketing release lead** (`@marketingteamember`). The person in charge of drafting the release announcement post.

## Pre-release check-in – one hour before the party starts

Before the scheduled time, check the current release leads channel (usually named `#x.x-release-leads`) to confirm that all relevant teams are prepared. If more time is needed and a delay is necessary, a message in the [#core](https://make.wordpress.org/core/tag/core/) channel should note the reason for the delay along with an expected time that the party will start.

## Host script based on Beta releases

The following script contains several placeholders highlighted in blue. It’s common for the @corecommitter, @securityteammember, and @missioncontrol to be the same person; adjust the script accordingly.

| **Steps and actions** | **Script for host** | **Who** |
| --- | --- | --- |
|  | `/here` Welcome to the WordPress `` `X.Y-Z` `` release party.  
  
I will be your host for this event, with @corecommitter and @mcpilot acting as behind-the-scenes drivers. (Be sure to adapt this message to the actual participants, taking into account any contributor filling multiple roles).  
  
For those who haven’t attended a release party before, welcome! Here’s the step-by-step guide from the handbook that details the release process: [https://make.wordpress.org/core/handbook/about/release-cycle/releasing-beta-versions/](https://make.wordpress.org/core/handbook/about/release-cycle/releasing-beta-versions/)  
 |  |
| **Step 1:** Ensure the announcement post for the blog is ready | Let’s start by ensuring the release post is ready to be published. @marketingteammember, what’s the status of the post?  
  
A public preview should be made available so anyone wanting to help proofread the post can do so. Just double-check the `@props` to credit them. | Marketing Leads |
| **Step 2:** Announce in Core to pause commits and don’t share links to the package until tested | @committers. Please refrain from committing until `X.Y-Z` has been released. :thank-you:  
  
:siren: Please remember not to share links to the package publicly until the “all clear” is given after testing and the announcement post is published on WordPress.org. :siren: | All attendees |
| **Step 3:** Run all unit tests locally | Time to run all unit tests. @corecommitter, please confirm. | Core Committer |
| **Step 4:** Verify that the latest [GitHub Action checks](https://github.com/WordPress/wordpress-develop/actions) are passing. | @corecommitter, can you also confirm that GitHub Action checks are passing? | Core Committer |
| **Step 5:** Ask a Security team member to verify the private security unit tests are passing for the most recent commit to ensure no regressions are introduced. | @securityteammember, please verify the private security unit tests pass for the latest commit. Thanks! | Security Team Member |
| **Step 6:** Bump version | @corecommitter, will you please commit the first version bump?  
  
*\[Wait for the commit to appear\]* | Core Committer |
| **Step 7:** Build the packages. | @mcpilot please proceed to package the release and post the link to the package here. | Core Committer |
| **Step 8:** Package Reminder | \[*While the package is being built, once again, remind attendees not to publicly share the link to the package until it’s been tested and the release post has been published. Sometimes, errors can happen during packaging, and the package needs to be rebuilt.*\]  
  
:siren: Please remember not to share links to the package publicly until the “all clear” is given after testing and the announcement post is published on WordPress.org. :siren:  
  
*\[Wait until the link to the \*.zip file is posted\]* | Emcee |
| **Step 8:** Testing | I**t’s testing time**!  
  
There are several ways to test, so pick whatever feels most comfortable and report back as you go:  
  
1\. Install and activate the [WordPress Beta Tester](https://wordpress.org/plugins/wordpress-beta-tester/) plugin. Select the Bleeding edge channel and then Beta/RC Only stream.  
2\. Use WP-CLI to test: wp core update –version=`X.Y-Z`  
3\. Directly download the Beta/RC version from https://wordpress.org/wordpress-`X.Y-Z`.zip  
  
**Here are a few scenarios to test:**  
– Test from latest in 4.0.\* release series (e.g., 4.0.35 > `X.Y-Z`)  
– Test from latest in 4.9.\* release series (e.g., 4.9.21 > `X.Y-Z`)  
– Test from the latest version in the current major release series (e.g., 6.1.1 > `X.Y-Z`)  
– Test from the most recent Beta/RC release (e.g., Beta 4 > `X.Y-Z`)  
– Test fresh installation  
– Remove `wp-config.php` file and test a fresh installation  
– Test single site and multisite/network (both subdirectory and subdomain) installations  
  
You can report back by sharing how you tested and what the result was with an emoji. For example:  
– 6.2-beta1 > `X.Y-Z` via beta tester  
If it works, add :white\_check\_mark:  
If any issues happen, add :red\_circle: so we can investigate. | Everyone |
| **Optional**: Summarize any issues found | *\[If any issues are found during testing, rely on this section*.\]  
Thanks, everyone, for testing! For now, we’re tracking the following issues: | Emcee |
| **Step 9:** Second version bump | Please, @corecommitter, proceed with the second version bump.  
  
*\[Wait for the commit to appear\]* | Core Committer |
| **Step 10:** Rebuild the Nightly Package in Mission Control | @mcpilot, can you please refresh the nightly build?  
  
*\[Wait for confirmation\]* | Mission Control |
| **Step 11**: Publish the announcement post | The release post can now be published! @marketingteammember, please proceed. | Marketing Team Member |
| **Step 12**: Announce in [#core](https://make.wordpress.org/core/tag/core/) that the release is available | @here WordPress `X.Y-Z` is now available: **insert link from the announcement post**  
Please help test and give feedback! | Emcee |
| **Step 13:** Announce that committers is open again | @committers, you can now resume committing.  
  
If this is a Release Candidate release, also remind committers that the `dev-feedback` and `dev-reviewed` workflow is required for all commits to the X.X branch. | Emcee |
| **Step 14**: Outro | The party is over! Props to @corecommitter, @securityteammember, @mcpilot for helping with the various release tasks.  
Thanks, everyone, for joining in and helping make WordPress! Hope to see you at future release parties.   
`</x.x-release-party>` | Emcee |
| **Step 15**: Props | Write a message in the [#props](https://wordpress.slack.com/messages/C0FRG66LR) channel thanking and giving props to everyone who tested or helped with the release process. | Emcee |

Script to host Beta/RC release parties

**Share reminders**

Before we go, here are a few reminders: 

*   Here’s a post that covers all you need to know ahead of release day: https://make.wordpress.org/core/2022/10/25/wordpress-6-0-release-day-process-2/ (An example from WP 6.0 that can be adapted to the current release.)
*   The dry run before the 24-hour code freeze is planned for date **(insert date for one day before public release date)**
*   The public release is planned for **(insert the current cycle release date)**. The exact time will be announced after the Dry Run finishes. You’re invited back for the biggest event of this release season!
*   According to the Bug Scrub Schedule **(insert a link to pinned post in Make/Core)**, the remaining bug scrubs before the stable release party are as follows:
    *   **List dates**