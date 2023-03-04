# Releasing Major Versions

Some things may be out of date, or unclear. If you have questions, reach out to a [prior release lead](https://make.wordpress.org/core/tag/release-lead/).

Congratulations! You’re a release lead for WordPress! The next few months of your life will be a whirlwind of excitement, frustration, and fun. Leading a WordPress release isn’t *easy*, but you’ll have a great time anyway.

There have been many before you, and there will be many after you. While this page might help guide you to the finish line, each release lead brings their own touch to the release. When in doubt, talk with a [previous release lead](https://make.wordpress.org/core/tag/release-lead/) and ask for direction.

## Getting Started

It’s worth reading through the [Releasing Minor Versions](https://make.wordpress.org/core/handbook/about/release-cycle/releasing-minor-versions/) handbook page, since many of its points apply to major version releases, too. That’s especially true as you get closer to the release date.

Once you’ve been appointed lead for a given release, here are some things you should think about or do right away:

*   **Talk to leads, committers, and component maintainers.** On day one, you might have no idea what your release will contain. Spend some time with each of the various WordPress leads, committers, and component maintainers to see what they have in mind. These discussions can happen over days, weeks, or even months depending on when your release is scheduled.
*   **Set a schedule.** A good cadence for major releases is every four months —often April, August, and December—though that’s not set in stone. One of the best ways to set your schedule: pick a release date and work backward from that date. Check out the scheduling section below for some tips!
*   **Pick release deputies.** You don’t have to have a release deputy, but it’s *strongly encouraged*. Some release leads have two or more deputies, which is perfectly fine! The trick here is to pick deputies who can augment your talents and assist throughout the cycle. Don’t enjoy writing meeting notes or running meetings? Pick a deputy who does! Not a fan of triage? There’s a community member out there who would love to help. If you’re unsure who might be interested in being a deputy, [post on make/core with a call for volunteers](https://make.wordpress.org/core/tag/deputy/). (Be sure to tag your post!)
*   **Post a call for ideas.** WordPress is built by a large community of volunteers, only some of which are committers and component maintainers. Early on in the release cycle, [post on make/core asking for ideas for the release](https://make.wordpress.org/core/tag/wishlists/). From that post, you will get individual tickets and bigger feature ideas. Sorting through them all will take some time, but will give you a great list of things to investigate for your release.

### On Scheduling

As the WordPress project grows increasingly global, it gets harder to find perfect release dates. Here are a few best practices to keep in mind as you settle on the likely timeline:

*   Try to be firm on the release date itself, but be prepared to add betas if necessary, or adjust RC dates.
*   Check for major holidays (including religious holidays, banking holidays, national holidays, etc.)
*   Check for large events that the community attends (WCUS, WCEU, etc.)

### On Roles & Responsibilities

There are a [number of roles and responsibilities](https://make.wordpress.org/core/handbook/about/release-cycle/wordpress-release-team-and-focus-leads/) over the course of a release. In practice, if there’s not a release coordinator for a cycle, a release lead and their deputies act as project managers (and technical project managers) for the entire release cycle. Otherwise, a release coordinator takes on ensuring the various pieces are properly covered by the cohesive release squad.

**Important note:** Much of the tasks listed in this handbook page are done by those who act as “mission control” or MC. These are a very specific set of folks with a particular ability to perform larger meta\-tasks for the project. If you’re not sure how to do something or don’t have access, it’s likely a task for those folks to handle. 

Prior to considering the responsibilities of release leads and deputies, it’s important to understand a few qualities of effective release leads:

*   **An understanding of how WordPress – both the software and the community – works.** WordPress, the software, is vast. No single contributor understands the entire codebase. However, release leads and deputies should have a good understanding of how WordPress works and how the core community functions. Knowing who to ask about various tickets is an important skill for leading a release!
*   **Knowledge of how open source works.** Open source projects run quite a bit differently than most software projects. To be a release lead or deputy, it’s expected that you have the ability to work well as a part of an open source, global, distributed project.
*   **The ability to communicate well with the community.** Communication is incredibly important across every part of the WordPress community, so good communication is valued and expected. The core community communicates in English, on this site, and in Slack, even though many contributors speak English as a second language. As a result of the varying backgrounds in this global community, release leads and deputies should take care when communicating in official and unofficial channels. See also: [Post & Comment Guidelines](https://make.wordpress.org/core/handbook/best-practices/post-comment-guidelines/).

There are also a few responsibilities that release leads and deputies have over the course of a release cycle:

*   **Posting agendas, running weekly developer chats, and posting chat summaries.** The overall WordPress developer community should be kept informed throughout the release cycle. Not every community member can attend the weekly developer chats, so posting [agendas](https://make.wordpress.org/core/tag/agenda/) and [chat summaries](https://make.wordpress.org/core/tag/summary/) is a necessity.
*   **Triaging tickets and monitoring ticket reports.** There are many moving pieces to a release. Release leads and deputies should keep a watchful eye on incoming trunk tickets and monitor relevant [ticket reports](https://make.wordpress.org/core/reports/). This includes triaging new ticket reports (especially in unowned components) to check for blocking issues.
*   **Keeping the release on schedule.** [Deadlines are not arbitrary.](https://make.wordpress.org/core/handbook/about/philosophies/#deadlines-are-not-arbitrary) WordPress releases should strive to stay on schedule and the release lead and deputies are responsible for this schedule. (See “On Scheduling,” above.) There are many aspects to maintaining the release schedule, many of which are listed as responsibilities here.
*   **Running bug scrubs.** Weekly bug scrubs are a useful activity that encourages contributions from all kinds of contributors. They can be successfully run by release leads, deputies, and other contributors. Component maintainers can also run bug scrubs.
*   **Reviewing and responding to feature ideas.** WordPress contributors and users will post feature ideas throughout the release cycle, especially on [wishlist](https://make.wordpress.org/core/tag/wishlists/) posts. While it is not the responsibility of the release lead (or deputy) to develop each feature, they should review each feature idea and see if it warrants inclusion in their release. Many of these ideas will come from [feature projects](https://make.wordpress.org/core/features/), but some may be tickets that need attention.
*   **Tracking down contributors for help.** It is not the responsibility of the release lead to make every technical decision or even the majority of them. The release lead should know how and when to track down and solicit contributors for assistance. The core team is large with varied availability and the release lead should have a good understanding of which contributors are the best to provide feedback and support for a variety of tickets.
*   **Regularly chatting with contributors.** Keeping in close contact with regular contributors helps ensure that a given WordPress release is stable and ready for the public. Chatting with contributors on a regular basis ensures that the release lead knows both the availability of contributors and any potential blocking issues, among other things.
*   **Coordinating marketing efforts.** There are a number of marketing efforts that need to be managed and the release lead or deputy should have an awareness of them. The [About page](https://docs.google.com/document/d/13itxtCD2jkKIMUj8anKLNMKoIWXE3dtJ6FyfkF-XN4E/edit#heading=h.1voz9urseun7) in WordPress core, the /news/ post, and the video are all part of this effort (more below on these specific efforts). [As learned on 4.7](https://core.trac.wordpress.org/ticket/39560), we should avoid having videos set to autoplay simultaneously. Note that these efforts should be conducted in conjunction with the [marketing team](https://make.wordpress.org/marketing/) and the relevant component maintainers. [Reference this release cycle marketing and communications guide](https://make.wordpress.org/marketing/handbook/resources/marketing-communicationsrelease-cycle-guide/) for an in-depth handbook on release communications.
*   **Communicating any changes to the release or to features.** As releases proceed, there are times when big decisions need to be made and communicated appropriately by the release squad. This requires both coming together to find a way forward, sometimes involving project leadership, and doing the work to appropriately communicate any changes. Here are two examples in case the release squad you are a part of runs into similar situations: [Announcing a revised release schedule for WordPress 5.9](https://make.wordpress.org/core/2021/11/22/wordpress-5-9-revised-release-schedule/) and [Webfonts API changes for WordPress 6.0](https://make.wordpress.org/core/2022/04/22/status-of-webfonts-api-for-wordpress-6-0-inclusion/). 

#### Expectations

Focus leads should be available for at least 5-6 hours a week to perform their tasks, with more time as milestones like Betas, Release Candidates, and General release approach. On the days of those milestones, you might need to dedicate 4-6 hours to WordPress in one day.

There are no limitations to where you come from. We are a global community, open 24/7 so you will schedule scrubs, if needed, according to your availability and potentially find a deputy to cover other time zones.

### Helpful Hints

*   **Create a public slack channel for communication and perform weekly updates starting just before beta 1.** This helps both the release squad work out in the open for the benefit of future contributors and allows folks to follow along as they see fit. The [#meta](https://make.wordpress.org/core/tag/meta/) team can help facilitate this. 
*   **Ensure redundancy in the release squad and during release parties.** With the size of the project, it goes a long way to have multiple folks in key roles and to ensure that, during release parties, there are multiple folks who can accomplish tasks. For example, having multiple MCs helps ensure someone is available in case the pre-arranged MC has a late arising conflict and cannot participate. 
*   **Examine what folks have done for the last release.** Because this is an open source project, much of what you need to do can be learned by looking at those who came before you. Search slack for release parties, ask questions of prior release leads, look on Make for how prior decisions were handled, etc. 
*   **Recognize each part of the cycle has different restrictions and focuses.** As the release cycle goes on, the focus shifts and it’s important to shift with it. For example, RC requires double sign-off for Core commits so it’s important to plan any important work with that variable in mind. 
*   **Create release party scripts and get alignment well before release days.** It’s normal for there to be plenty of coordination ahead of time, including creating scripts for release parties, checking with folks to ensure they can take on specific steps, etc. Handle the necessary and known stressors so that when unexpected stressors come up you have more capacity to respond. 
*   **Share early and often, especially if you have concerns**. While something might feel obvious to you, it can easily be overlooked by the group if not expressed. 

## Pre Merge Window

*   Feature projects should prepare for merge consideration at the beginning of a release cycle. 
*   Merge proposals should be created and reviewed during this time.
*   Check to see if a new bundled theme will be included in this release.

## Merge Window

*   Decide which feature projects (if any) should be merged.
*   If a release video is required, kick off the work on that.

## Pre Beta 1

*   **[Compile and start to publish Dev notes](https://make.wordpress.org/core/handbook/tutorials/writing-developer-notes/)**. Start compiling and publishing posts that inform developers of breaking changes and major developer-focused updates of the release on [make/core using #dev-notes](https://make.wordpress.org/core/tag/dev-notes/).
*   **About Page**. Start compiling noteworthy features in the release and identifying a designer who can contribute illustrations. Words should be complete by RC1, images can update through RC2. Some [in-depth information on the About Page process](https://docs.google.com/document/d/13itxtCD2jkKIMUj8anKLNMKoIWXE3dtJ6FyfkF-XN4E/edit#heading=h.1voz9urseun7) is also available as well as the [marketing communications handbook](https://make.wordpress.org/marketing/handbook/resources/marketing-communicationsrelease-cycle-guide/).
*   **HelpHub Version Page**. Begin compiling noteworthy updates for designers, developers, and users. *The* [*5.2 version page*](https://wordpress.org/support/wordpress-version/version-5-2/) *can be used as an example, or reach out to the [Docs Team](https://make.wordpress.org/docs/) for help.*
*   Identify if any of the browsers listed on the [Browser support page](https://make.wordpress.org/core/handbook/best-practices/browser-support/) had dropped below the percentage required to support them in core and if any need updating plan for that now as that will be one of the final checks and updates in the [Pre Final Release phase below](https://make.wordpress.org/core/handbook/about/release-cycle/releasing-major-versions/#pre-final-release).

## Beta 1

The [process for a Beta release](https://make.wordpress.org/core/handbook/about/release-cycle/releasing-beta-versions/) is well-documented on a separate handbook page.

## Pre Release Candidate

*   There should be no open tickets on the release milestone.
*   The process for [publishing the Field Guide is documented on a separate handbook page](https://make.wordpress.org/core/handbook/tutorials/publishing-the-field-guide/).
*   All Plugin Authors (in the wp.org repo) should be emailed, letting them know to test their plugins for compatibility with the release. The email should link them to the Field Guide. [Contact the Plugin Team Rep to coordinate](https://make.wordpress.org/updates/team-reps/) or publish the draft release email on the [Plugin Review Team’s make site](https://make.wordpress.org/pluginrepo) ([sample from 5.3 here](https://make.wordpress.org/pluginrepo/2019/10/18/5-3-release-email/)).
*   Test the Classic Editor plugin to make sure it still works well.
*   Remind the Akismet team about the release schedule, to ensure they get any pending plugin updates released before our final release.
    *   Akismet is automatically checked for updates, and updated if required, on every WordPress commit
    *   The plugin is updated in trunk , the current stable branch and the current development branch (if it differs from trunk).
*   The Hosts Mailing List should be notified of an updated release date for the major version (handled by the [#hosting-community](https://wordpress.slack.com/messages/hosting-community/) team). Post a message in the [#hosting-community](https://wordpress.slack.com/messages/hosting-community/) Slack channel.
*   An announcement should be made about the [string freeze](https://make.wordpress.org/polyglots/handbook/glossary/#hard-freeze) on the Polyglots P2 ([example from 5.9](https://make.wordpress.org/polyglots/2021/12/16/wordpress-5-9-ready-to-be-translated/)).
*   Committers should be given a proactive reminder that the [Release Candidate com](https://make.wordpress.org/core/2022/05/04/wordpress-6-0-release-candidate-phase/)[mit policy](https://make.wordpress.org/core/2018/10/05/wordpress-5-0-commit-management/) is coming up when RC 1 is released, specifically that in the RC Phase all commits have to get double sign-off from committers. This begins *after* RC1 is released so, in the reminder, alert folks that the RC phase is coming up but has not yet begun.
*   Run the private security unit test suite.

## Release Candidate

A Release Candidate version is released as the last stage of the release cycle before the major version is released. The Release Candidate means that  the release squad feels confident that what is in trunk is good enough for the major release, and should be thoroughly tested by the community.

*   A [hard string freeze](https://make.wordpress.org/polyglots/handbook/glossary/#hard-freeze) takes effect at the Release Candidate stage, meaning text strings in the application can no longer be changed, including the About Page text.
*   Multiple Release Candidate versions should be released (e.g. RC1, RC2) as bugs reported against it are fixed.
*   Alert committers that all changes to src/ at the Release Candidate stage must be reviewed by two committers. When choosing a second committer to review your patch, look for a veteran committer with extensive experience in that area of the codebase, so that the patch can receive a meaningful critique. Committers can commit to tests/ at any time.
*   The [process for an RC release](https://make.wordpress.org/core/handbook/about/release-cycle/releasing-beta-versions/) is well-documented on a separate handbook page.
*   Following the first release candidate a branch for the release can be created so that early work on trunk can begin for the next release.
*   An announcement should be made on Make Core about the release candidate phase ([example from 6.0](https://make.wordpress.org/core/2022/05/04/wordpress-6-0-release-candidate-phase/)) and the various above protocols in order to better amplify this specific part of the release cycle and prepare the community.

### translate.WordPress.org

It’s time to ask the [Polyglots team](https://make.wordpress.org/polyglots/) to help translate the upcoming WordPress version. *In the list below, the example release is A.B.*

*   Create a A.B.x sub-project to the main WordPress project.
*   Copy the translation sets from the Development project.
*   Do the same for each Development sub-project.
*   Update [/home/rosetta/public\_html/wp-content/mu-plugins/rosetta/rosetta.php](https://dotorg.trac.wordpress.org/browser/wordpress/rosetta/website/wp-content/mu-plugins/rosetta/rosetta.php) to add mappings from GlotPress project to WordPress branch and the project name in Rosetta.
*   Update [/home/wporg/public\_html/translate/bin/update-all-core-packs.sh](https://dotorg.trac.wordpress.org/browser/wordpress/website/translate/bin/update-all-core-packs.sh) to use the A.B.x sub-project for A.B language packs.
*   Migrate existing translations for Gutenberg plugin to the WordPress project.
*   Notify the [Polyglots team](https://make.wordpress.org/polyglots/) of the strings.

## Branching Before Release

At this point, once the milestone is mostly clear, a branch for the release can be created, so that early work on trunk could start. The following files need to have version numbers updated when branching:

*   `src/wp-includes/version.php`
*   Both NPM files: `package.json` and `package-lock.json`
*   In trunk, update the `SECURITY.md` file to include the newly created branch in the list of versions receiving security updates

When branching before a release, there are two important things that need setting after branching has taken place. Ideally these should be done before any development work on trunk begins.

*   API: Set `WP_CORE_DEV_BRANCH` in [/home/wporg/public\_html/.config/versions.php](https://dotorg.trac.wordpress.org/browser/wordpress/website/.config/versions.php) to the branch, for example, 4.9. This is used in the core update check to keep Beta Tester plugin users on the branch development path (instead of pushing them into the super-alpha 5.0).
*   Translate: Update `DEV_BRANCH` in [/home/wporg/public\_html/translate/bin/update-originals-wp.sh](https://dotorg.trac.wordpress.org/browser/wordpress/website/translate/bin/update-originals-wp.sh) to cause GlotPress to know that the “WordPress Development” project should import strings (“originals”) from the branch rather than trunk. This is required to prevent any string changes in trunk affecting the translation files generated. This is often also set following releases for a few weeks while translation efforts continue on the latest stable version of WordPress, and trunk may have many iterations on string changes.
*   Translate: Update [/home/wporg/public\_html/translate/bin/update-all-core-packs.sh](https://dotorg.trac.wordpress.org/browser/wordpress/website/translate/bin/update-all-core-packs.sh) to use the branch for beta/RC packages.
*   Translate: Update [/home/rosetta/public\_html/wp-content/mu-plugins/rosetta/rosetta.php](https://dotorg.trac.wordpress.org/browser/wordpress/rosetta/website/wp-content/mu-plugins/rosetta/rosetta.php) to use the branch for the `wp/dev` project.

After branching is performed, the Test Old Branches GitHub Actions workflow needs to be updated. As an example, here is a [PR that would update the workflow file after 5.8 is branched](https://github.com/WordPress/wordpress-develop/pull/1199).

## Pre Final Release

This is your pre-release checklist. Do not skip it. To help with coordination, it’s recommended to [duplicate this sheet](https://docs.google.com/spreadsheets/d/1SQov6AK7ZM8O5TbSVlxNEul3HDHzqjANeRW61WTSyG4/edit#gid=546938884) and begin assigning tasks amongst the release squad, along with wider contributors who tend to step in during this part of the release cycle.

*   Publish a post summarizing the release process for those looking to help and/or follow along ([example from 5.1](https://make.wordpress.org/core/2019/02/21/wordpress-5-1-release-day/)).
*   Get the name of the release’s Jazz Musician (reach out to Matt or the current project director).
*   Gather the list of Noteworthy Contributors for the Credits page. [Utilize this template spreadsheet (showing sample data from 5.4) to help capture those users](https://docs.google.com/spreadsheets/d/1sejDx2WcH2XW_i_0PK6qtYzu7Vsh1jrasR1otPmTf1s/edit#gid=246976924). Ensure all Noteworthy Contributors have a photo in Gravatar.
    *   This should include props from Trac, Github, and any non-code props to add manually.
    *   There are sections: All Leads, Noteworthy Contributors (including Core Devs), All Contributors. *Leads and Noteworthy Contributors are compiled manually — ask each focus lead to review your list.*
    *   Ensure that Design leads in the release check for any missing designers as they may have been missed on code props.
*   The Credits API should be updated.
    *   Everyone in the first Noteworthy Contributors section (named `core-developers`, though not limited to developers) should get a Core Team badge.
*   Make sure the tagline is synced in about.php, freedoms.php, and credits.php.
*   Make sure the About page images use CDN URLs and any filler images are properly replaced with the final version.
*   Run the private security unit test suite.
*   The announcement post should be drafted. **DO NOT PUBLISH.**
    *   This is based on the copy from the About Page, but will also include video (if applicable) and props at the end.
    *   To display the list of props in the release post, use this shortcode: `[wpcredits X.Y]`, where X.Y is the release version. It fetches the data from the Credits API, so there is no need to generate a separate list of props for the release post as this will display automatically once the Credits API is updated for the release.
    *   Make sure the post includes a thank you note for support volunteers and translators after core props (see previous major release announcements for an example like [5.6](https://wordpress.org/news/2020/12/simone/)).
    *   Categorize post as “release” *only*, ***not*** as “release” *and* “development”.
    *   Update the tweet if desired, including the hashtag [#WordPress](https://make.wordpress.org/core/tag/wordpress/).
    *   Set a featured image which is used for the link preview when sharing the post. Ensure that previews on Twitter, Facebook, etc. do not crop of significant portions of the image. If need be, you can clear the cache on Facebook using [https://developers.facebook.com/tools/debug/](https://developers.facebook.com/tools/debug/) and on Twitter using [https://cards-dev.twitter.com/validator](https://cards-dev.twitter.com/validator).
    *   Adjust the excerpt.
        *   Append `&embed=true` to the preview URL to ensure the embed looks good.
*   Update the [Browser support page](https://make.wordpress.org/core/handbook/best-practices/browser-support/) if we end support for any browsers.

### Dry Run

24 hours before the release is scheduled, perform a dry run and walk through these steps:

*   Triage any bugs reported against trunk, most easily found at the top of [report 40](https://core.trac.wordpress.org/report/40).
*   Update `src/wp-admin/includes/update-core.php`
    *   Check for old files and see if they are in `$_old_files`:
        *   `svn diff --summarize [https://core.svn.wordpress.org/tags/4.4](https://core.svn.wordpress.org/tags/4.4) [https://core.svn.wordpress.org/trunk](https://core.svn.wordpress.org/trunk) | grep '^D'`
    *   Check for added files with names that are in `$_old_files`. Comment any out in `$_old_files` with the version where it was added back. Do not delete the lines, for the sake of history.
        *   `svn diff --summarize [https://core.svn.wordpress.org/tags/4.4](https://core.svn.wordpress.org/tags/4.4) [https://core.svn.wordpress.org/trunk](https://core.svn.wordpress.org/trunk) | grep '^A'`
    *   Check that `$_new_bundled_files` is up to date. This needs to be updated with every new default theme.
    *   **Note:** files removed from default themes should not be listed in `$_old_files`. Those are updated separately from Core updates, so including them is not necessary.
*   Run `npm run grunt prerelease`, to ensure all tests pass, and CSS and JS files conform to standards. (this takes a while)

### Notify Everyone

*   Notify hosts that a release is coming.
*   Notify the [polyglots team](https://make.wordpress.org/polyglots/) of string changes.
*   Notify the [systems team](https://make.wordpress.org/systems/) so they can have someone available during release. If you aren’t sure how best to do this, ask your release squad if anyone is a part of this team.

## Release Day

You’ve made it to release day!

### Core

1.  Ensure the top of [report 40](https://core.trac.wordpress.org/report/40) is triaged, preferably clear.
2.  Alert committers about the release and to pause committing:
    1.  Example: @committers Please refrain from committing until we get 5.8 released.
3.  If applicable, make the final commit to `about.php`, e.g. to include a release video or update final illustrations.
4.  Verify `package.json` is updated.
5.  Verify `src/wp-admin/includes/update-core.php`.
6.  *If there is a new default theme*, verify:
    1.  `WP_DEFAULT_THEME` in `src/wp-includes/default-constants.php`
    2.  `WP_Theme::$default_themes` in `src/wp-includes/class-wp-theme.php`
    3.  **Very important:** `WP_CORE_NEW_BUNDLED_VERSION` in `/home/wporg/public_html/.config/versions.php`
7.  Run unit tests.
8.  Run `npm run grunt prerelease`. This will also run the unit tests. Check for result of GitHub Actions (e.g., [https://github.com/WordPress/wordpress-develop/actions?query=branch%3A5.8](https://github.com/WordPress/wordpress-develop/actions?query=branch%3A5.8)).
9.  Update version in `src/wp-includes/version.php` to remove the RC identifier and changeset – eg. `5.3-src`.
10.  Tag the release. From branch:  
    `svn copy https://develop.svn.wordpress.org/branches/4.7 https://develop.svn.wordpress.org/tags/4.7 -m "Tag 4.7"`  
    If this command line fails, then attempt the same tag via a GUI interface such as TortoiseSVN.
11.  Create release packages via the form at mc.wordpress.org.
12.  Share in Slack: “Just a reminder: Do not tweet or share on any social media any of the links for the release. Sometimes things go wrong and packages need to be rebuilt. The release is not official until the post is published on the official news blog.”

### WordPress.org

1.  Check packages are showing up at [https://wordpress.org/download/releases/](https://wordpress.org/download/release-archive/).
2.  Download and unzip/untar packages. Verify they are the same. Check MD5 sums.
3.  Test the packages:
    1.  There are two ways to help test the package:
        1.  Use WP-CLI to test: `wp core update https://wordpress.org/wordpress-5.8.zip`
        2.  Directly download the Beta/RC version (e.g., [https://wordpress.org/wordpress-5.8.zip](https://wordpress.org/wordpress-5.8.zip))
    2.  In particular, testing the following types of installs and updates would be much appreciated:
        1.  Does a new WordPress install work correctly? This includes running through the manual install process, as well as WP-CLI or one-click installers.
        2.  Test upgrading from 4.0.33, 4.9.18, 5.7.2, and 5.8 RC 4 as well as any other versions possible.
        3.  Remove `wp-config.php` file and test fresh install.
        4.  Test single site and multisite/network (both subdirectory and subdomain) installs.
        5.  Does it upgrade correctly? Are the [files listed in `$_old_files`](https://core.trac.wordpress.org/browser/branches/5.8/src/wp-admin/includes/update-core.php#L21) removed when you upgrade?
        6.  Does Multisite upgrade properly?
    3.  Finally the following user flows, on desktop and mobile, would be great to validate work as expected:
        1.  Publish a post, including a variety of different blocks.
        2.  Comment on the post.
        3.  Install a new plugin/theme, or upgrade an existing one.
        4.  Change the site language.
        5.  If you’re a plugin developer, or if there are complex plugins you depend upon, test that they’re working correctly.
4.  Take a final screenshot of [the downloads counter](https://wordpress.org/download/counter/).
5.  Bump versions in `.config/versions.php`. (Do this on a WordPress.org sandbox so you can test update notifications before deploying.)
    
    *   Switch `WP_CORE_DEV_BRANCH` back to `trunk` if it was set to the branch during RC.Bump `WP_CORE_STABLE_BRANCH` if this is a major release.
    
    *   Bump `WP_CORE_LATEST_RELEASE`.
    *   Bump `WP_CORE_NEW_BUNDLED_VERSION` if there is a new default theme. **Important.**
    *   Update `wporg_get_secure_versions()` with the previous secure stable release, used by [an API endpoint used by Google Webmasters Tools](https://api.wordpress.org/core/stable-check/1.0/).
    *   Update `wporg_get_version_equivalents()` if required, used by the plugin directory.
    *   Automatic updates will commence once these changes are deployed – See the final step #9.
6.  Publish the [HelpHub release page](https://wordpress.org/support/wordpress-version/version-5-2/).
7.  Update the [relevant credits file](https://meta.trac.wordpress.org/browser/sites/trunk/api.wordpress.org/public_html/core/credits), and deploy the changes.
8.  Build language packs for the release by bumping versions in `translate/bin/update-all-core-packs.sh`.
9.  Deploy WordPress.org, `deploy-dotorg.sh wporg` from a sandbox.

### Tell the World

1.  (Publish the release video on WordPress.TV. **DO NOT Publicize**. Un-check the publicize button so the release video does not go out on Twitter/Facebook.)
2.  Publish announcement on wordpress.org/news. This will auto-publish to Twitter.
    1.  Update the slug to include only the name of the release jazzer, not the release number.
3.  Update the Codex.
    1.  Finalize Version Page in the Codex.
    2.  Update [CurrentVersion Template](https://codex.wordpress.org/Template:CurrentVersion) with the new version.
    3.  Update [WordPress Versions](https://codex.wordpress.org/WordPress_Versions) page.
        1.  Add:  
            `{{ ReleaseTableMajor | version = 4.4  | date = December 8, 2015 | musician = Clifford Brown | blog = https://wordpress.org/news/2015/12/clifford/  | db = 35700 }}`
        2.  Remove the version from the “Planned Versions” section.
    4.  Update [PHP Compatibility and WordPress Versions](https://make.wordpress.org/core/handbook/contribute/php-compatibility-and-wordpress-versions/) table.
    5.  Update [PHPUnit Compatibility and WordPress Versions](https://make.wordpress.org/core/handbook/references/phpunit-compatibility-and-wordpress-versions/) table.
4.  Stare at [download counter](https://wordpress.org/download/counter/) and rejoice.

## Post Release

1.  Bump the branch version to `X.Y.1-alpha-$REVNUM-src` and trunk to `X.Y+1-alpha-$REVNUM-src` along with the corresponding `package.json` and readme changes for both. Assuming the next release lead has commit privileges, they should be given the honors of the trunk bump.
2.  Force nightly builds. (Note: Checksums aren’t available for the nightly. WP-CLI grabs the checksums for both the installed version and the version you’re upgrading to, so it can remove old files.)
3.  In Trac, rename the `trunk` version to `X.Y` and create a new one for trunk. Complete the `X.Y` milestone and create new milestones for the new cycle and `X.Y.1`. This must be done by a Trac admin.
4.  Update various parts of the documentation:
    
    *   The current release sidebar on [make.wordpress.org/core](https://make.wordpress.org/core/).
    *   Update [make.wordpress.org/core/reports](https://make.wordpress.org/core/reports/) to modify the ‘Next Major Release’ version.  
        ***Note**: Edit using the Gutenberg Code editor, otherwise Dashicons will be stripped.*
    *   Update [wordpress.org/about/roadmap](https://wordpress.org/about/roadmap/) and [wordpress.org/about/history](https://wordpress.org/about/history/), removing the new release from the list of upcoming releases, adding the jazzer, and adding the release date. Note: the page content is in the [Meta SVN repository](https://meta.trac.wordpress.org/browser/sites/trunk/wordpress.org/public_html/wp-content/themes/pub/wporg-main/page-about-roadmap.php).
    *   Update [wordpress.org/support/article/history](https://wordpress.org/support/article/history/).
    *   Update [wordpress.org/support/article/wordpress-versions](https://wordpress.org/support/article/wordpress-versions/).
    
    *   The dev cycle docs (ex. https://make.wordpress.org/core/x-x/).
    *   Update the latest release under “Getting Started” on the front-page of [https://wordpress.org/support/](https://wordpress.org/support/).
    *   Update the sticky thread at the top of [https://wordpress.org/support/forum/how-to-and-troubleshooting/](https://wordpress.org/support/forum/how-to-and-troubleshooting/).
    *   Run `wp devhub parse --url=developer.wordpress.org` on a wordpress.org sandbox. That will update [the DevHub code reference](https://developer.wordpress.org/reference/) docs to parse the latest stable Core release.
5.  Don’t forget the polyglots team! Share the code version of the release post on the [#polyglots](https://make.wordpress.org/core/tag/polyglots/) channel so they can translate it easily. Open the release post in the editor, then go to Settings > Copy all content. Paste it as a snippet in the [#polyglots](https://make.wordpress.org/core/tag/polyglots/) channel on Slack.
6.  Identify folks who helped with significant testing during the release process and submit them for additions to the Credits API if they were not already credited in the release. This can be done via a Meta Trac ticket.
7.  During the week following the release:
    *   Publish a retrospective post if desired.
    *   Check in with the [Support Team](https://make.wordpress.org/support/) for any notable issues.
    *   Check in with the [Community Team](https://make.wordpress.org/community/) for any community feedback.
    *   Kick off the next cycle with the next lead.

**Congratulations! You did it!**

[#core](https://make.wordpress.org/core/tag/core/), [#hosting-community](https://make.wordpress.org/core/tag/hosting-community/)