# Block Editor Release Process for Major Releases

This guide will clarify how to handle the block editor portion of a major WordPress release. This is a living document, and feedback is welcomed as the hope is this can be continually improved as more people get experience managing this side of a release cycle. 

## Release Team Roles Involved

### Editor tech leads

Coordinate merging of new features from Gutenberg plugin into core. This involves making sure all relevant feature work is merged and stable in the plugin before updating the npm packages and then updating the package versions in core. It also involves making sure any relevant PHP changes are manually added to the core codebase.

### Editor triage leads

Set up and manage the release project board on GitHub and triage incoming bug reports for issues that need fixing during the release cycle. Run regular triage sessions in WordPress Slack, both synchronously and async. Ping Editor tech leads and feature developers as needed about any urgent bugs.

### Documentation leads

Wrangle dev notes for any new features or changes that impact the developer/extender community.

## Quick Reference Timeline

This is a list of the major time-critical tasks, sorted by when they should be done:

**2 months before Beta 1**

*   Set up the release project board on GitHub.
*   Audit experimental APIs in Gutenberg
*   Create an overview issue of PHP changes that need to be manually added in core.

**1 month before Beta 1**

*   Update Trunk with the latest Gutenberg packages and PHP changes.
*   Create tracking issue for dev notes (dev notes should be published by RC1 and need plenty of time to wrangle).

**Between Beta 1 and last RC**

*   Triage recent bug reports and unlabelled issues for critical regressions.

**The week before each Beta/RC release**

*   Go through all merged Pull Requests labeled [Backport to WP Beta/RC](https://github.com/WordPress/gutenberg/issues?q=label%3A%22Backport+to+WP+Beta%2FRC%22+is%3Aclosed) and check that they are OK to include.
*   Review any open Pull Requests with the same label.
*   Start package update/core patch process (described below).

## Planning before the first Major Release Beta

**Planning the last editor release and communicating deadlines**

At the start of each release cycle, a planning post is published ([example from 5.6](https://make.wordpress.org/core/2020/08/13/wordpress-5-6-release-planning/)) that shows key milestones leading up to a major WordPress release. With Gutenberg releases happening biweekly, you can then determine which Gutenberg release is scheduled closest to Beta 1 and, if necessary, rearrange the plugin release date so it aligns better with the Beta 1 date. Ideally, the Gutenberg RC should be cut 4-5 days before Beta 1 to give plenty of time for any bugs to be identified and fixed, as well as publishing the npm packages and updating their versions in core.

As part of this planning, be sure to include a communication plan with deadlines that features need to be merged by in order to be included in a major release. The best place to share these deadlines is on Make Core and in [#core-editor](https://make.wordpress.org/core/tag/core-editor/) slack channel as a pinned post. You may also want to give a heads up for specific deadlines as they get closer in the core editor meetings. 

**Project Board Management**

**How to set up a project board**

To help coordinate tasks for release, it’s become a best practice to create a “Must Haves” board” for the major release in Gutenberg’s GitHub repo. [Here’s an example from 5.5](https://github.com/WordPress/gutenberg/projects/45). This board  should contain issues and PRs along with meta tasks like audits, discussion points, etc.

Generally speaking, the following columns are recommended:

*   To do: Contained issues/cards with all the tasks for which there is no progress yet. Try to keep items ordered by priority.
*   In Progress: Contained tasks that must be done and had someone working on them.
*   Needs reviews: Tasks that needed a review.
*   Research/Discussions in progress: An area to record issues that may be a must for a release but where there was no conclusion. Some possible reasons for not having a conclusion are:
    *   The problem was critical but was impossible to replicate, so it’s a matter of waiting for more information to understand the specific conditions where the problem happens.
    *   It is not clear yet if the issue is a regression or not, or it is not clear if the issue is a bug or desired behavior.
    *   The issue required a very complex testing setup or trying to replicate it takes a lot of time. In that case, it’s recommended that you write a comment upon finding the issue saying what needed to be done to test it. This helps make it easier for others to jump in to help with testing. If needed, you may need to add the “needs-testing” label as well. From there, make sure to include it in the issue part of the board so you don’t lose track. As soon as things are tested, you can move the issue to the “To do” column if it should be fixed or archive/close the issue if it does not need a fix. 
*   Approved: Tasks that were ready to merge (reviewed and approved). This is helpful to see at a glance any issues that might be approved but that the PR author hasn’t merged yet and can enable you to keep PRs moving. 
*   Done: Tasks that were finished, merged, etc. and didn’t require any additional work.
*   Notes, Useful Links, Etc: this is a helpful column to add relevant information like:
    *   The version of Gutenberg that the last WordPress release included and the version of Gutenberg that we were going to include in the next major release. 
    *   Link to the WordPress release cycle page.
    *   Link to the WordPress Planning Roundup post that included the most relevant editor features.
    *   During the release, you’ll find many people will ask questions. If a question was repeated multiple times, that was a signal to include the information people were asking in this column.

After creating the board, it’s recommended that you [configure GitHub automation](https://docs.github.com/en/free-pro-team@latest/github/managing-your-work-on-github/configuring-automation-for-project-boards) to move tasks to “Done” when the relevant PRs are merged or issues are closed and to move PRs to needs review when they are pending approval. This will lessen the amount of meta work that needs to be done.

**How to keep the project board useful for others**

Since the project board will be a place that meetings reference and people bookmark, it’s important to take steps to keep it current and useful for others. The following actions are recommended and can be divided up:

*   Sort items in “To do” column by priority. Keep the highest priority items at the top so more people will see them and perhaps jump in to help or at least be aware of current challenges. 
*   When an issue gets a PR associated, or a card got an issue, archive the issue or card and add the PR or issue to the board. 
*   Regularly move items to the most relevant columns as the status of a task changes. This is particularly important to do if automation doesn’t automatically catch them. For example, this can happen with meta tasks without any associated PRs. 

**Where to share the project board**

To help others discover the project board, it’s recommended that you share the link to it regularly in both the core editor meetings and in the general slack channel as helpful. This will get people in the habit of checking the project board and for them to share it in turn. 

**Assigning Tasks From the Board**

For items in the “To Do” column, it’s recommended that you find someone assigned in time before the release milestones. The easiest way to do this is to ask in the [#core-editor](https://make.wordpress.org/core/tag/core-editor/) channel for volunteers to pick tasks from that column. If no one volunteers, you will need to do some research to find the people familiar with the items needing help (checking previous Gutenberg PRs can be helpful here) and asking them if they can take on that work or help another person do so. 

## Knowing which features to include in the release

**Review [release roadmap post](https://make.wordpress.org/core/2023/05/18/roadmap-to-6-3/) and recent** [**“What’s New”**](https://make.wordpress.org/core/tag/gutenberg-new/) **release posts to determine important features**

The release roadmap post lists the features considered top priority for each release. Special attention should be given to these to make sure they land in core in a timely and stable manner.

To get a sense of all the features currently being worked on, as well as smaller enhancements and bug fixes, it’s good to review plugin release posts too.

For experimental features in particular, it helps to ping the developers working on them and discuss whether they are ready to be included in core or not.

**Deciding on additional features to include**

Outside of the main features of a release, there are often in progress additional features that are still helpful to include to help complement the release as a whole. This might include features that were missed in the last major release as well as simply more minor features or updates to include. Whether you can include these depends on various factors including but not limited to:

*   What features might be important to finish. 
*   The complexity/risk of each feature. 
*   How complementary they are to the main features for the release.
*   Whether there are individuals working on the feature. 

For any feature you do decide to add, remember to add it to the release “Must Haves” Project Board in GitHub. As you can, do your best to help move these features along whether through helping with PRs, unblocking the original authors, etc. 

If there’s an additional feature you want to include that you don’t have anyone actively working on, please ask for volunteers in the [#core-editor](https://make.wordpress.org/core/tag/core-editor/) meetings during the Open Floor time. If you know of any developer who may be a good person to work on a given feature, it’s often best to ping them directly and ask if they are able to do so. Even if they can’t, they may be able to point you to someone who can!

**How to handle removing features**

As with any release, there are going to be tough calls that have to be made. What follows are the best steps you can take to communicate effectively and, if needed, make the call to not include a feature in a release:

*   Communicate as early as you can with the people working on the feature that it is at risk of not being included and clearly state what needs to be done by when in order to change that. 
*   Give updates to the release squad as things do or do not progress alongside updates in [#core-editor](https://make.wordpress.org/core/tag/core-editor/) meetings. 
*   If the decision is made to remove a feature, please write a post on Make Core announcing the final decision. [Here’s an example from a past release](https://make.wordpress.org/core/2020/02/07/navigation-block-exclusion-from-wp-5-4/). 

The key in all of this is clear, timely communication so all involved (contributors, release squad members, etc) can prepare appropriately. 

## Experimental API Management

Since the [private-apis](https://github.com/WordPress/gutenberg/tree/trunk/packages/private-apis) system was created in early 2023, the system for managing experimental APIs changed, and everything that is not stable or not meant to be available as a public API is kept private.

However, there are still many older experimental APIs in Gutenberg, which can be recognised by their `__experimental` prefix. These can be functions, properties or variables and they can be found throughout the codebase. Every release it’s customary to do an audit of these and check if any are ready for stabilisation. It’s important that stabilisation be done before the first beta 1 release (ideally at least two weeks beforehand) as renames during the beta phase are not possible.

**How to run the audit**

Generally speaking, the process is as follows:

*   Use the script below to audit experimental APIs
*   [Use git blame](https://docs.github.com/en/free-pro-team@latest/github/managing-files-in-a-repository/tracking-changes-in-a-file) to identify who was involved with each API
*   Create an overview issue in GitHub tracking each experimental API pinging those involved to decide whether an API needs to be stabilized ([example from 6.2](https://github.com/WordPress/gutenberg/issues/47196)).

**Task Breakdown**

To get started, here’s a script to use to begin auditing the experimental APIs:

[https://raw.githubusercontent.com/WordPress/gutenberg/trunk/bin/list-experimental-api-matches.sh](https://raw.githubusercontent.com/WordPress/gutenberg/trunk/bin/list-experimental-api-matches.sh)

With the information from the report and any information manually collected, it can help to then group related experimental APIs to get a sense of what’s in place currently. From there, use git blame to know who was involved in each API in order to ping them. You can then create a new overview issue in GitHub that lists out a checkbox for each API where one can see at a glance the status of whether a decision has been made around the API being stabilized or not. 

## Communication Management

**Planning and Writing Dev Notes**

*For more context on Dev Note best practices, check out* [*this handbook page*](https://make.wordpress.org/core/handbook/tutorials/writing-developer-notes/)*.*

In order to know what needs a Dev Note, you can check all PRs [labeled with  “Needs Dev Note”.](https://github.com/WordPress/gutenberg/issues?q=label%3A%22Needs+Dev+Note%22.) You might find that there are more PRs than you can feasible write individual posts for without overwhelming the community with information. The best thing to do if you find too many PRs with that label is to group related changes and propose a dev note for each group.

Once you have a sense of the different dev notes that are needed, create a GitHub issue ([previous example](https://github.com/WordPress/gutenberg/issues/20185)) detailing the plan: what posts need to be done, what sections for each post, and which PRs are included in each. When doing so, make sure to ping the people that had PRs needing dev notes to contribute to this effort. Your job ideally should be to wrangle the updates from each PR author and plan out the timeline for sharing each dev note so that you don’t share too many in a short period of time. To help with this, it’s recommended to share target dates in order to help space out and plan appropriately. 

Keep in mind that dev notes are extremely collaborative efforts requiring help from many different people! This might mean that some people you need information from didn’t see the ping the first time or don’t have the availability to take writing one note. It’s okay and expected that follow-up will be needed, likely in the form of additional pings or even DMs in Slack to get updates. When each section is done for each dev note, you can then check the checkbox to show progress made and to help others see what’s left. 

As you compile each dev note, particularly if you are combining multiple PRs into one dev note, make sure you share the posts with those involved for review so everyone is on the same page. Once there’s consensus there, make sure to then share the dev notes with those involved in the major release squad to get a final review. Finally, make sure not to share too many dev notes in a short period of time.  

## General Triage Management

**Regular Triage**

Because months pass between core releases, it’s important to regularly check in on GitHub to triage issues (ideally weekly) particularly [new ones that are unlabeled](https://github.com/WordPress/gutenberg/issues?q=is%3Aissue+is%3Aopen+no%3Alabel+sort%3Acreated-desc). The key is to not miss anything that might be critical. 

**High Level Triage**

Outside of reviewing unlabeled issues, it’s important to take time to review all reported issues since a major release occurred to spot any key critical issues to resolve. This is a great task to divide up among others. The easiest way to do this is to divide the work into month-long increments ([example link for all bugs reported in October 2019](https://github.com/WordPress/gutenberg/issues?page=2&q=is%3Aissue+is%3Aopen+label%3A%22%5BType%5D+Bug%22+created%3A2019-10-01..2019-10-31+sort%3Acreated-asc&utf8=%E2%9C%93)).

**Important Note For Determining How Critical A Bug Is**

When reviewing bug reports and trying to determine how critical they are, it becomes even more important to know the version that introduced the particular bug. For example, you might find a bug that was introduced in many core WordPress versions ago but that doesn’t have many comments. This is a good sign that the bug is not truly critical to fix. Because after the first Beta, you can only include bug fixes for issues that regressed during the alpha phase, it’s essential to know if the bug you are reviewing affects the latest stable release of WordPress. This might require having multiple testing environments with different setups in order to determine the impact (current version of WordPress, beta version of core Release, and the latest version of Gutenberg). It might also mean following up with those who reported issues to get more information about their particular setup like if they are using Gutenberg and, if so, what version. 

## Managing the first WordPress Beta release

**Important Context**

The first beta is a very significant deadline since no additional features or enhancements can be included after this milestone. Exceptions for enhancements to new features can be made: these must be discussed with the release team, and if approved a Trac ticket should be created for each feature with the type “task (blessed)”. All enhancements to these tasks must be finished before RC1.

**To make the process easier, start updating trunk as early as possible before Beta 1**

As the volume of changes for each release is quite high, it helps to start adding new features to core trunk as early as possible in the cycle. This means both updating the `@wordpress` npm packages used by core, and manually syncing any PHP changes from the `lib` and `phpunit` folders in Gutenberg.

**Make sure any experimental features are behind feature flags in Gutenberg so they don’t accidentally get included in core**

In order to safely update the npm packages in core, experimental Gutenberg features that aren’t slated for inclusion in core must be safely behind feature flags. `IS_GUTENBERG_PLUGIN` flag is commonly used for this purpose, or a specific feature filter may be used, such as in [this example](https://github.com/WordPress/gutenberg/pull/52579) for the interactivity API.

**List PHP changes to be manually synced**

Create an overview issue of all the changes from the `lib` and `phpunit` folders that need to be manually synced. Using git blame, find the authors of those changes and ping them to create core PRs for them.

The PHP files in `block-library` package don’t need to be manually synced, as they are auto-generated in core based on the npm package.

## Managing Weekly Beta and RC releases

After the first beta, there are weekly beta releases leading up to the Release Candidate. At this point, there are three main tasks to take care of: triage new issues, cherry-pick PRs for inclusion in the release, and update package and core paths. The following section is broken down into these three areas. 

**Triage New Issues**

Throughout the week, it is best to check all new issues reported since the last release to make sure no regressions have been found. If issues have been created for regressions, add those issues to the “Must Haves” project board immediately. 

When PR’s are submitted for issues on the “Must Haves” project board, add the “Backport to WP Beta/RC” label to the issue so you can keep track of what to include in the next beta release. 

Outside of triaging these issues for inclusion in the “Must Haves” project board, it’s important to make sure that any issues added are assigned to someone to resolve, particularly with beta releases occuring on a weekly schedule.. 

**Cherry-picking PRs for Release**

Once tasks on the “Must Haves” board are completed they need to be backported into the core to be available on the next beta or RC version. This is the process to do it:

*   If a wp/x.x (should have the correct WP release number) hasn’t been created yet, create it and push it to the remote repo.
*   Review all PRs with the label [“Backport to WP Beta/RC”](https://github.com/WordPress/gutenberg/pulls?q=label%3A%22Backport+to+WP+Core%22+sort%3Acreated-desc+). Verify if everything is expected, and that the PRs are not “risky” to go into a core release.
*   Create a branch based on wp/trunk and named in accordance with the release being prepared e.g: wp/trunk-5-4-0-rc-1.
*   Cherry-pick each PR into the newly created branch.

    *   There is [a convenient cherry-picking automation](https://developer.wordpress.org/block-editor/contributors/code/release/auto-cherry-picking/) available via `npm run cherry-pick`. It finds all merged Pull Requests with the “Backport to WP Beta/RC” label, cherry-picks them, and asks whether to automatically comment on the relevant PRs and push the branch to Github. You can also pass another label as the first argument.

    *   You can also do it manually. The hash of the commit can be extracted from the GitHub pull request page. In order to avoid merge conflicts, it is important to make sure the commits are cherry-picked in the same order they were made in the master branch. This will likely not be the same order that appears in the label view, so double-check the merge date and if necessary refer to the [commit history](https://github.com/WordPress/gutenberg/commits/master). You can combine multiple commits in a single command, like so: `git cherry-pick c82094d8389b1756f05d4079ba98e4ee25961502 && git cherry-pick 548e600f14924d7fcfdb5250f45f718d3759d022 && git cherry-pick b72b41e27f008540410c45023b655c8ee20b67ae`
*   Merge conflicts may still happen. If they do, you will have to resolve them, and if you are unsure how, message the PR author for assistance. Take notes about what steps were taken to resolve the conflict.
*   After solving a conflict execute the cherry-pick command (or the cherry-pick automation) with the remaining commits to merge.
*   Push the branch to GitHub.
*   Create a pull request on GitHub from the branch you created into the wp-trunk branch. The PR description should include a table that lists all the PRs that were cherry-picked, the authors (pinging the authors with a mention so the authors are aware that the PR will be part of the next WordPress release) and specify the changes that were made to solve the conflicts (in case there was a conflict). A sample PR can be checked at  [https://github.com/WordPress/gutenberg/pull/21083](https://href.li/?https://github.com/WordPress/gutenberg/pull/21083).
*   Verify that continuous integration executed with success for the PR.
*   If there were merge conflicts to solve, you might want to ping the authors of the conflicting commits to double-check they were solved correctly. Otherwise, if all tests pass on CI, it’s fine to go ahead and merge the PR to the release branch.
*   After merging, run the package publish task from the release branch:
    *   On [this page](https://github.com/WordPress/gutenberg/actions/workflows/publish-npm-packages.yml), click on the “Run workflow” button, choose the release branch, release type should be “wp” and the release version should be added underneath.
    *   Once the workflow appears in the list below, click through to authorise it. If you don’t have `gutenberg-core` access, ask someone who does to approve it for you.
    *   This workflow will publish the npm packages with a dist tag corresponding to the release, which can then be used to select the correct package versions in core.

**Package updates and core patch**es

*   After merging the cherry picking PR switch to the `wp/trunk` branch and run `git pull`.
*   Run the relevant Github action to update the `@wordpress` npm packages for a WordPress release as documented at [https://github.com/WordPress/gutenberg/blob/trunk/docs/contributors/code/release.md#wordpress-releases](https://github.com/WordPress/gutenberg/blob/trunk/docs/contributors/code/release.md#wordpress-releases)
*   Update the packages using the automated script by running `npm run sync-gutenberg-packages -- --dist-tag=wp-<VERSION>` in the wordpress-develop folder. Remember to use the same dist-tag as the newly released `@wordpress` packages, e.g. `wp-6.2` for the 6.2 major version.
*   Then run `npm run postsync-gutenberg-packages` in the wordpress-develop folder. It includes any new Gutenberg blocks in core and runs the required builds.
*   Verify the issues that were supposed to be resolved are in fact resolved on the WordPress trunk.
*   Create a [Trac](https://core.trac.wordpress.org/) ticket for the package updates in Core.
*   Submit a PR against wordpress-develop to make sure the continuous integration tests pass, and add the Trac ticket number to the description. This ensures the PR gets linked to the ticket, and the patch will then be created automatically. For example, here’s the PR from WordPress 6.0 release cycle: [#2564](https://github.com/WordPress/wordpress-develop/pull/2564)
*   Ask for reviews. During the beta stage a review is recommended but not mandatory; during the RC process a double signoff by two different committers is required. If you are a committer and are confident with the changes you can be one of the approvers and add the “dev-feedback” keyword.
*   When approved, commit the patch or coordinate with a committer to make sure it is committed in case you are not a committer.
*   If a branch for the WordPress release already exists, backporting the commit from trunk to the release branch is required.
