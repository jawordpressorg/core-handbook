# Block Editor Release Process for Major Releases

This guide will clarify how to handle the Editor (Gutenberg) portion of a major WordPress release. This is a living document. You are encouraged to leave feedback and provide updates.

## Release team roles

It takes a team to manage the Editor release process for each major version of WordPress. You can learn more about the roles and responsibilities of each key role below. 

*   [Editor Tech Leads](https://make.wordpress.org/core/handbook/about/release-cycle/wordpress-release-team-and-focus-leads/#editor-tech-lead)
*   [Editor Triage Leads](https://make.wordpress.org/core/handbook/about/release-cycle/wordpress-release-team-and-focus-leads/#editor-triage-lead)
*   [Documentation Leads](https://make.wordpress.org/core/handbook/about/release-cycle/wordpress-release-team-and-focus-leads/#documentation-wrangling)

## Quick reference timeline

Here’s a list of the significant time-critical tasks, sorted by when they should be completed. More details about each task are available later in this document.

**Two months before Beta 1**

*   Set up the release project board on GitHub
*   Audit experimental APIs in Gutenberg
*   Create an overview issue for PHP changes that need to be manually added in Core. The issue should have the label “🤖 Sync Backport Changelog” and the WP version x.x in the title, so that the PR list is auto-generated.

**One month before Beta 1**

*   Update trunk with the latest Gutenberg packages and PHP changes
*   Create a tracking issue for dev notes, which should be published by RC1 and require plenty of time to wrangle

**Between Beta 1 and the last RC**

*   Create a label “Backport to WP x.x Beta/RC”.
*   Triage recent bug reports and unlabelled issues for critical regressions
*   Fix all critical regressions and as many bug fixes related to the release as possible

**The week before each Beta/RC release**

*   Go through all PRs labeled “Backport to WP x.x Beta/RC” and check that they are ok to include in the release. Check the merged PRs with this label for any auto-cherry-pick failures.
*   Review any open PRs with the same label
*   Go through the commits on the wp/x.x branch to ensure the PR should be included in the release.
*   Start package update/core patch process

## Planning before the first Major Release Beta

At the start of each release cycle, a planning roundup post should be published ([example from 6.3](https://make.wordpress.org/core/2023/05/18/wordpress-6-3-planning-roundup/)) that details key milestones leading up to the major WordPress release. This post includes deadlines for all Beta and RC releases and the names of all release team members. 

### Scheduling the last editor release and communicating deadlines

Gutenberg releases happen biweekly, so you can determine which Gutenberg release is scheduled closest to Beta 1 and, if necessary, rearrange the plugin release date to align better with Beta 1. 

Ideally, this last Gutenberg RC should be released 4-5 days before Beta 1. This schedule will give plenty of time for any bugs to be identified and fixed while allowing the team to publish npm packages and update their versions in Core. 

If a contributor wants to include a new Editor feature in the major release, it must be included in this last Gutenberg RC. Therefore, once you have identified the final Gutenberg release, share it in the [#core-editor](https://wordpress.slack.com/archives/C02QB2JS7) Slack channel and during the weekly Editor Weekly Chat meeting to allow contributors to prepare appropriately.

### The Roadmap post

A Roadmap post identifies the features, enhancements, and bug fixes slated for the current major release ([example from 6.3](https://make.wordpress.org/core/2023/05/18/roadmap-to-6-3/)). The creation of this resource is a collaborative effort between release leads and contributors.

You should become familiar with this post if you are an Editor Tech or Triage lead. It’s an excellent resource for knowing what should be included in the release. It’s also invaluable for determining which reported issues are related to the release and which need to be added to the project board. More on that below. 

## Managing the project board

Creating a “project board” for the major release in Gutenberg’s [GitHub repository](https://github.com/WordPress/gutenberg/projects?query=is%3Aopen) has become a best practice. [This board](https://github.com/WordPress/gutenberg/projects/45) helps coordinate tasks and should contain all issues and PRs related to the release.

### Setting up the project board

Beginning with WordPress 6.3, a template has been created to help you set up the project board. 

*   Navigate to the template: [WordPress (X.X) Editor Tasks](https://github.com/orgs/WordPress/projects/126)
*   Click on the “Use this template” button to create a new board
*   Update the title of the board using the format “WordPress X.X Editor Tasks”
*   Update the “Punted to 6.X.1” and “Punted to 6.Y” column titles
*   Navigate to the [Gutenberg Projects](https://github.com/WordPress/gutenberg/projects?query=is%3Aopen) page and click the “Link Project” to link the newly created project to the Gutenberg repository. 

The template will contain the following columns:

*   Triage – All new issues enter the board in this column. Release leads then decide if the issues belong in the “Todo”, “In discussion / Needs decision” or other columns as needed. Issues can also be removed from the board completely if there is a general consensus among leads.
*   In Discussion / Needs Decision –  Contains issues or PRs that the team needs more time to consider for the release. Some possible reasons for not having a conclusion are:
    *   The problem was critical but was impossible to replicate, so it’s a matter of waiting for more information to understand the specific conditions where the problem happens.
    *   It still needs to be clarified if the issue is a regression or not, or it is not clear if the issue is a bug or desired behavior.
    *   The issue requires a complex testing setup, and replicating it takes time. In this case, you should write a comment upon finding the issue, saying what must be done to test it. This helps make it easier for others to help with testing. If needed, you may need to add the “needs-testing” label as well. Once the issue is tested and confirmed, move it to the “Todo” column. 
*   Todo – Contains issues that the team has determined should be fixed by the release but do not have a PR associated with them.
*   In Progress – Contains issues that the team has determined should be fixed by the release and have a PR associated with them.
*   Needs Review – Contains PRs associated with issues in the “In Progress” columns that are not yet merged and need review.
*   Needs Core Commit – Contains PRs that need an additional Core commit, which the Editor Tech Leads determine. 
*   Done – Contains issues and PRs that are complete.
*   Punted to 6.X.1 – Contains issues and PRs that the team has determined should be punted to the next minor release.
*   Punted to 6.Y – Contains issues and PRs that the team has determined should be punted to the next major release.

After you have created the project board, make sure to review the project board from the prior release and migrate over all punted issues and PRs. Remove each from the old project board once you have moved everything over.

[![](https://make.wordpress.org/core/files/2023/08/project-board-1024x541.png)](https://make.wordpress.org/core/files/2023/08/project-board.png)

An example of the WordPress 6.4 Editor Tasks project board.

Note that “punting” is a sports metaphor from [American football](https://en.wikipedia.org/wiki/Punt_\(gridiron_football\)). If you punt something, you decide not to include it in the current release, and it’s “punted” to the next minor or major release.

### Keeping the project board updated

Since the project board will be a place that meetings reference and people bookmark, it’s important to take steps to keep it current and useful for others. The following actions are recommended and can be divided up:

*   The release leads, and members of the Gutenberg Triage Team should regularly review new [Gutenberg issues](https://github.com/WordPress/gutenberg/issues) and add those relevant to the current release to the project in the “Triage” column.
*   Sort items in “Todo” column by priority. Keep the highest priority items at the top so more people will see them. Issues with the `Regression` label should always be at the top. 
*   When an issue gets a PR associated, move the issue to the “In Progress” column and add the PR to the “In Review” column.
*   PRs associated with issues on the board also need to be added to the project board. 
*   Ensure all issues and PRs are properly labeled.

Share the link to the project board regularly in the Editor Weekly Chat meetings and the [#core-editor](https://wordpress.slack.com/archives/C02QB2JS7) Slack channel as helpful. This will get people in the habit of checking the project board and for them to share it in turn. You can also encourage contributors with permission to add issues they think are important to the “Triage” column. The Editor Triage leads will handle it from there. 

### Running asynchronous triage sessions

During the Beta release cycle, the weekly triage sessions in the [#core-editor](https://wordpress.slack.com/archives/C02QB2JS7) Slack channel are suspended. They are replaced with asynchronous triage sessions to specifically handle the project board, especially the “Triage” and “In Discussion / Needs Decision” column. These meetings allow the Editor Tech and Triage leads to efficiently “vote” on how issues and PR should be prioritized and managed.

Often a release team consists of members across various time zones, so an asynchronous meeting allows everyone to participate when convenient. 

You create an initial announcement for the meeting in the [#core-editor](https://wordpress.slack.com/archives/C02QB2JS7) Slack channel and add each PR and issue in a thread. The leads then vote using emojis and can add additional comments in the thread. 

These meetings are held publicly so all other contributors can see the decisions being made. Below is an example of a meeting for 6.3, but feel free to modify it as needed.

[![](https://make.wordpress.org/core/files/2023/08/async-triage-slack-1024x517.png)](https://make.wordpress.org/core/files/2023/08/async-triage-slack.png)

An example asynchronous triage session held during the WordPress 6.3 release cycle.

### Assigning tasks from the board

For items in the “Todo” column, it’s recommended that you find someone assigned in time before the release milestones. The easiest way to do this is to ask in the [#core-editor](https://wordpress.slack.com/archives/C02QB2JS7) channel for volunteers to pick tasks from that column. If no one volunteers, you will need to research to find contributors familiar with the items needing help (checking previous Gutenberg PRs can be helpful here) and ask them if they can take on that work or help another person do so. 

If issues seem critical to the release but nobody is picking them up, alert the Editor Tech Leads as soon as possible. 

## Knowing which features to include in the release

**Review [the release roadmap post](https://make.wordpress.org/core/2023/05/18/roadmap-to-6-3/) and recent Gutenberg [“What’s New”](https://make.wordpress.org/core/tag/gutenberg-new/) release posts to determine essential features.**

The release roadmap post lists the features considered a top priority for each release. Special attention should be given to these to ensure they land in Core in a timely and stable manner.

It’s good to review Gutenberg release posts too. They will give you a sense of all the features currently being worked on, as well as smaller enhancements and bug fixes.

For experimental features in particular, it helps to ping the developers working on them and discuss whether they are ready to be included in Core.

### Deciding on additional features to include

Outside of the main features of a release, there are often in progress additional features that are still helpful to include to help complement the release as a whole. This might include features that were missed in the last major release as well as simply more minor updates to include. Whether you can include these depends on various factors, including but not limited to the following:

*   What features might be important to finish? 
*   What is the complexity/risk of each feature? 
*   How complementary they are to the main features of the release.
*   Are there contributors actively working on the feature? 

For any feature you do decide to add, remember to add it to the release project board in GitHub. Do your best to help move these features along, whether through helping with PRs, unblocking the original authors, etc. 

If there’s an additional feature you want to include that you don’t have anyone actively working on, please ask for volunteers in the [#core-editor](https://wordpress.slack.com/archives/C02QB2JS7) meetings. If you know of any developer who may be a good person to work on a given feature, it’s often best to ping them directly and ask if they can do so. Even if they can’t, they may be able to point you to someone who can.

### How to handle removing features

As with any release, there will be tough calls that must be made. What follows are the best steps you can take to communicate effectively and, if needed, make the call to not include a feature in a release:

*   Communicate as early as you can with the people working on the feature that it is at risk of not being included and clearly state what needs to be done by when in order to change that. 
*   Give updates to the release squad as things do or do not progress alongside updates in [#core-editor](https://wordpress.slack.com/archives/C02QB2JS7) meetings. 
*   If you decide to remove a feature, please write a post on Make Core announcing the final decision. [Here’s an example from a past release](https://make.wordpress.org/core/2020/02/07/navigation-block-exclusion-from-wp-5-4/). 

The key is clear, timely communication so all involved (contributors, release squad members, etc) can prepare appropriately.

## Experimental API management

Since the [private-apis](https://github.com/WordPress/gutenberg/tree/trunk/packages/private-apis) system was created in early 2023, the system for managing experimental APIs has changed. Everything that is unstable or not meant to be available as a public API is kept private.

However, there are still many older experimental APIs in Gutenberg that can be recognized by the `__experimental` prefix. These can be functions, properties, or variables found throughout the codebase. For every release, it’s customary to audit these and check if any are ready for stabilization. Stabilization must be done before the Beta 1 release (ideally at least two weeks beforehand), as renames during the Beta phase are not possible.

There’s two solutions to an experimental/unstable API: either make it public, or make it completely private. In either case the original function should be kept and deprecated.

### Updating the Private API consent string

The consent string for unlocking private APIs is intended to change on a regular basis. To update the consent string:

1.  Come up with a new consent string, the string should mention that themes or plugins opting in to unstable and private features will break in future versions of WordPress.
2.  Ensure the consent string has not being used previously.
3.  Append the new string to the history list in the Private API package’s read me.
4.  Replace the consent string in the following locations:
    *   in the getting started section of the Private API package’s read me
    *   in the `src/implementation.js` file of the Private API package
    *   in the `src/lock-unlock.js` file located in packages consuming private APIs
    *   search the full code base for any other occurrences

**Note**: The consent string is not used for user facing content and as such should *not* be made translatable via the internationalization features of WordPress.

Updating the consent string is considered a task and can be done during the late stages of a WordPress release.

### How to run the audit

Generally speaking, the process is as follows:

*   Use the script below for auditing experimental APIs
*   [Use git blame](https://docs.github.com/en/free-pro-team@latest/github/managing-files-in-a-repository/tracking-changes-in-a-file) to identify who was involved with each API
*   Create an overview issue in GitHub tracking each experimental API pinging those involved to decide whether an API needs to be stabilized ([example from 6.2](https://github.com/WordPress/gutenberg/issues/47196)).

To get started, here’s a script to use to begin auditing the experimental APIs:

[https://raw.githubusercontent.com/WordPress/gutenberg/trunk/bin/list-experimental-api-matches.sh](https://raw.githubusercontent.com/WordPress/gutenberg/trunk/bin/list-experimental-api-matches.sh)

It can help to group related experimental APIs from the report and any information manually collected to get a sense of what’s currently in place. From there, use git blame to know which contributors were involved in each API to ping them and inquire if the API can be stabilized. You can then create a new overview issue in GitHub that lists out a checkbox for each API where you can easily see whether a decision has been made around stabilizing the API.

## Planning and writing dev notes

*Check out* [*this handbook page*](https://make.wordpress.org/core/handbook/tutorials/writing-developer-notes/) *for more context on dev note best practices.*

You can check all PRs labeled with [`Needs Dev Note`](https://github.com/WordPress/gutenberg/issues?q=label%3A%22Needs+Dev+Note%22.) to know what needs a dev note. You might find that there are more PRs than you can feasibly write individual posts for without overwhelming the community with information. In this case, group PRs with the same label and propose a dev note for each group.

Once you have a sense of the needed dev notes, create a GitHub issue ([previous example](https://github.com/WordPress/gutenberg/issues/20185)) detailing the plan: 

*   What posts need to be done 
*   What are the essential sections of each post
*   What PRs should be included in each 

When doing so, ping the people with PRs needing dev notes to contribute to this effort. Ideally, your job should be to wrangle the updates from each PR author and plan the timeline for sharing each dev note so that you don’t share too many in a short time. Sharing target dates is recommended to help space out and plan appropriately. 

Keep in mind that dev notes are extremely collaborative efforts requiring help from many people. This might mean that some people you need information from didn’t see the ping the first time or are unavailable to write a note. It’s okay and expected that follow-up will be required, likely in the form of additional pings or even DMs in Slack to get updates. When each section is done for each dev note, you can check the checkbox to show progress and help others see what’s left. 

As you compile each dev note, particularly if you combine multiple PRs into one dev note, ensure you share the posts with those involved for review so everyone is on the same page. Once there’s consensus, share the dev notes with those involved in the major release squad for a final review. 

### Getting a list of commits

Release coordinators may require total numbers of Editor commits made during the major cycle. To do this go to the Gutenberg

## General triage management

### Routine triage

Because months pass between Core releases, it’s important to regularly check in on GitHub to triage issues (ideally weekly), particularly new ones that are unlabeled. The key is not to miss anything that might be critical. 

### Release-specific triage

Outside of reviewing unlabeled issues, it’s important to review all reported issues since a major release occurred to spot any critical issues that need to be resolved. While this is primarily the job of the Editor Triage Leads, this is a great task to divide up among other contributors. 

### Determining how critical a bug is

When reviewing bug reports and trying to determine how critical they are, it becomes even more important to know the version that introduced the particular bug. For example, you might find a bug introduced many WordPress versions ago, but it doesn’t have many recent comments. This is a good sign that the bug is not critical to fix. 

After the first Beta, you can only include bug fixes for issues that regressed during the Alpha phase. It’s essential to know if the bug you are reviewing affects the latest stable release of WordPress. This might require multiple testing environments with different setups to determine the impact, for example, the current version of WordPress, the Beta version, and the latest version of Gutenberg. It might also mean following up with those who reported issues to get more information about their particular setup, like if they are using Gutenberg and, if so, what version.

## Managing the first WordPress Beta release

**Beta 1 is a very significant deadline.** 

No additional features or enhancements can be included after this milestone. Exceptions for enhancements to new features can be made, but these must be discussed with the release team. If approved, a Trac ticket should be created for each feature with the type “task (blessed)”. All enhancements to these tasks must be finished before RC1.

**To make the Beta 1 release process easier, start updating trunk as early as possible.**

As the volume of changes for each release is quite high, it helps to start adding new features to Core trunk as early as possible in the cycle. This means both updating the `@wordpress` npm packages used by Core and manually syncing any PHP changes from the `lib` and `phpunit` folders in Gutenberg.

**Make sure any experimental features are behind feature flags in Gutenberg, so they don’t accidentally get included in Core.**

In order to safely update the npm packages in Core, experimental Gutenberg features that aren’t slated for inclusion in Core must be safely behind feature flags. `IS_GUTENBERG_PLUGIN` flag is commonly used for this purpose, or a specific feature filter may be used, such as in [this example](https://github.com/WordPress/gutenberg/pull/52579) for the interactivity API.

**List PHP changes to be manually synced.**

Create an overview issue of all the changes from the `lib` and `phpunit` folders that need to be manually synced.

There is now automation available in the Gutenberg repo to create the contents of this Issue for you:

*   Create an issue with the WP version number in the title, e.g. “Backports for WP x.x”. Add the label “🤖 Sync Backport Changelog”, and whenever trunk is updated, new entries in the [backport-changelog](https://github.com/WordPress/gutenberg/tree/trunk/backport-changelog) folder will be synced to this issue.
*   Github will add link previews so it’s easy to see the status of each core PR.

The PHP files in `block-library` package don’t need to be manually synced, as they are auto-generated in Core based on the npm package.

## Managing weekly Beta and RC releases

After the first Beta, there are weekly Beta releases leading up to the Release Candidate (RC). At this point, there are three main tasks to take care of: triage new issues, cherry-pick PRs for inclusion in the release, and update both package and Core paths.

### Triaging new issues

Throughout the week, you should closely monitor all new Gutenberg issues since the last release to ensure no regressions have been found. If you identify regressions, immediately add those issues to the “WordPress X.X Editor Tasks” project board in the “Triage” column for further investigation. 

When PRs are submitted for issues on the project board, add the `Backport to WP Beta/RC` label to the PR so you can track what needs to be included in the next Beta release. 

Outside of looking for issues that need to be added to the project board, it’s important to ensure all issues on the board are assigned to someone to resolve, especially with Beta releases occurring on a weekly schedule.

### Syncing Gutenberg code to WordPress Core

Once PRs on the project board are completed, they must be backported into the Core to be available on the next Beta or RC version. Follow this process:

#### Review the PRs

*   Review all the closed PRs marked with “Backport to WP x.x Beta/RC” label, and PRs auto-cherry-picked to the wp/x.x branch.
*   Check for PRs that contain [PHP changes that might require a *manual* backport](https://github.com/WordPress/gutenberg/blob/trunk/docs/contributors/code/back-merging-to-wp-core.md). If any are required, either raise the backport PR in the WP Core repo or prompt the contributor to do so.
*   Audit the PRs and confirm they are suitable to be included in the current phase of the release. For example, the RC phase is intended as “complete software” has specific requirements. Refer to the Editor Tech Leads and Core Tech Leads for guidance.

#### Cherry Picking PRs

Cherry picking PRs has been completely automated. If a PR has the “Backport to WP x.x Beta/RC” label, it will be cherry-picked to the wp/x.x branch on merge. Applying the label after merge will also trigger a cherry-pick.

Please note that the automation can fail when there are conflicts, so you must still check the “Backport to WP x.x Beta/RC” label for closed PRs. Normally an automated comment is left to encourge the PR author to create a manual cherry-pick PR (with wp/x.x as the base). After merging the manual cherry-pick, you should remove the “Backport to WP x.x Beta/RC” label and add the “Backported to WP Core” label to the *original* PR.

Pre-automation instructions, in case it completely failed.

Only follow these steps if automation *completely* fails for *all* PRs. Do not use these steps for conflict failures!

*   If a `wp/x.x` (use the correct WordPress release number) has yet to be created, create it and push it to the Gutenberg remote repository.
*   Create *another* branch (the “cherry picking” branch) *based on* the `wp/x.x` branch.
*   Cherry-pick each PR into the newly created branch:
    *   There is [cherry-picking automation](https://developer.wordpress.org/block-editor/contributors/code/release/auto-cherry-picking/) available via `npm run other:cherry-pick`. It finds all merged PRs with the `Backport to WP Beta/RC` label, cherry-picks them, and asks whether to automatically comment on the relevant PRs and push the branch to GitHub. You can also pass another label as the first argument.
    *   You can also do it manually. The hash of the commit is extracted from the GitHub pull request page. To avoid merge conflicts, cherry-pick the commits in the same order they were made in trunk. The order will likely not be the same as the PRs appear in the label view, so double-check the merge date and refer to the [commit history](https://github.com/WordPress/gutenberg/commits/master). You can combine multiple commits in a single command, like so: `git cherry-pick c82094d8389b1756f05d4079ba98e4ee25961502 && git cherry-pick 548e600f14924d7fcfdb5250f45f718d3759d022 && git cherry-pick b72b41e27f008540410c45023b655c8ee20b67ae`
*   Merge conflicts may still happen. If they do, you will have to resolve them. If you need help with this, message the PR author for assistance.
*   Sometimes a conflict happens because the cherry-picked commit depends on another commit that wasn’t included in the release branch. This may be an accidental omission, so it’s good to double-check by pinging the authors of the PRs.
*   After manually solving a conflict, return to the original PR and
    *   remove the `Backport to WP Beta/RC` label.
    *   *add* the `Backported to WP Core` label.
    *   comment that the PR was cherry picked into `{link_to_your_branch}`.
*   Create a pull request on GitHub from the cherry pick branch and use the Github UI to set it to merge into the `wp/x.x` branch.
*   Verify that continuous integration is executed with success for the PR.
*   If there were merge conflicts to solve, you should ping the authors of the conflicting commits to double-check they were solved correctly.
*   Before merging, always [double-check that *all* the necessary PRs have been identified and cherry picked](https://github.com/WordPress/gutenberg/issues?q=is%3Aissue+is%3Aclosed+label%3A%22Backport+to+WP+Beta%2FRC%22) as the automation is prone to occasional errors.
*   Once all tests pass on CI, use the Github UI to `Rebase and Merge` the branch (check the target branch is the `wp/X.X` branch). Be sure to change to `Rebase` and not the default `Squash` as this allows for a full history of commits to the `wp/X.X` branch.

#### Publish Packages to NPM

*   After merging, check the CI tests pass on the `wp/X.X` branch.
*   If they do, now it’s time to run the package publish task from the release branch so that the `@wordpress/*` packages will be published to NPM under the correct `dist-tag` .
*   On [the Actions tab in the Gutenberg repository in Github](https://github.com/WordPress/gutenberg/actions/workflows/publish-npm-packages.yml), click the “Run workflow” button and choose:
    *   Use workflow from: `trunk`
    *   Release type: `wp`
    *   WordPress major version: `X.X`
*   Once the workflow appears in the list below, click through to authorize it. If you don’t have `gutenberg-core` access, ask someone who does to approve it for you.
*   This workflow will publish the npm packages with a dist tag corresponding to the release, which can then be used to select the correct package versions in Core.
*   Once workflow is complete check `npm` registry has updated
    *   pick a `@wordpress/*` package (e.g. `@wordpress/block-library` )
    *   goto [https://www.npmjs.com/package/@wordpress/block-library?activeTab=versions](https://www.npmjs.com/package/@wordpress/block-library?activeTab=versions)
    *   click the `Versions` tab.
    *   Scroll down to find the `Tag` for the release (e.g. `wp-6.5` ). Note the release number.
    *   Scroll down further to find the `Version History` heading and check that the release number is the same as the latest release.

#### Package updates and Core patches

*   Once the npm packages are published, they can be updated in the `wp-develop` repo using the automated script: `npm run sync-gutenberg-packages -- --dist-tag=wp-<VERSION>`. Remember to use the same dist-tag as the newly released `@wordpress` packages, e.g. `wp-6.2` for the 6.2 major version.
*   Then run `npm run postsync-gutenberg-packages` in the `wordpress-develop` folder. It includes any new Gutenberg blocks in Core and runs the required builds.
*   If any new front-end scripts have been added to dynamic blocks, these need to be referenced manually in the [webpack block config](https://github.com/WordPress/wordpress-develop/blob/trunk/tools/webpack/blocks.js#L67).
*   After running both sync and postsync tasks, verify that the correct files have been updated for any blocks with changes to their PHP or block.json files and that files have been generated for any brand new blocks.
*   **Note**: changes to `script-loader-packages.min.php` should only be expected *if* there are **JavaScript** changes in the packages update. If there are no JavaScript changes (for example when changes are purely CSS) then the hashes remain the same because the compiled contents are identical.
*   In your local WordPress development environment, check that the issues that were supposed to be resolved are in fact resolved.
*   Create a [Trac](https://core.trac.wordpress.org/) ticket for the package updates in Core.
*   Submit a PR against `wordpress-develop` to ensure the continuous integration tests pass, and add the Trac ticket number to the description. This ensures the PR gets linked to the ticket, and the patch will then be created automatically ([previous example](https://github.com/WordPress/wordpress-develop/pull/2564)). You should include a list of all the PRs included in the sync (see below).
*   To get a list of the PRs that were committed since the last release you can use this command substituting `{LAST_COMMIT_HASH}` for the commit hash of the last published commit:

```
git --no-pager log --pretty='format:%s' {LAST_COMMIT_HASH}..HEAD
```

*   Ask for reviews. During the Beta stage, a review is recommended but not mandatory. A double signoff by two different committers is required during the RC process. If you are a committer and are confident with the changes, you can be one of the approvers and add the “dev-feedback” keyword.
*   When approved, commit the patch or coordinate with a committer to ensure it’s committed if you are not a committer.
*   If a branch in SVN for the WordPress release already exists (usually happens shortly after RC1), [backporting the commit from the `trunk` to the release branch](https://make.wordpress.org/core/handbook/best-practices/backporting-commits/) is required. This must be undertaken by a different committer than the person who committed to `trunk`.

[#core-editor](https://make.wordpress.org/core/tag/core-editor/)