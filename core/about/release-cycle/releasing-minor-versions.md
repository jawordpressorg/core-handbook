# Releasing Minor Versions

So, you wanna ship a minor version of WordPress? Okay, maybe you don’t *want* to. Perhaps you *need* to ship a minor version of WordPress. A minor release is intended for bugfixes and enhancements that do not add new deployed files and are at the discretion of the release lead with suggestions/input from component maintainers and committers. There’s a lot involved with shipping these releases, as documented below. If you’ve been through the release process before and see something missing *please add it*.

## Before Release

Before you’ve decided to release, there are a few things to consider \[TODO: Add more to this section\]:

*   Is this release because of a security fix?
*   Will this release contain only security fixes?
*   What maintenance fixes should go into the release? Have those maintenance fixes been committed to trunk?

Depending on the focus of the minor release (security, maintenance, or both), there are a few things to consider.

### Security

**Security patches should be created well ahead of time**. Different patches may be necessary for trunk and stable branches. Currently, we make an effort to back port patches to all versions of WordPress that support autoupdates (4.1+). However, back porting patches is not always possible and those versions of WordPress are not officially supported as a result.

Follow the process in the Security team handbook to make sure that patches are adequately tested for back-compat, bypasses, and real-world cases.

All patches should be well-tested and receive sign-off from the WordPress Security Team at least five days ahead of the scheduled release date. It’s incredibly important to get this feedback early on as security fixes do not have a lot of time to bake on trunk.

For security fixes reported by third-parties, get information on how they would like to be credited. The announcement post on [wordpress.org/news/](https://wordpress.org/news/) credits third-parties as requested.

12 hours before release (or earlier), you’ll need to lower the TTL in the update API to 60 minutes. This means that, by the time you release, all WordPress installations will be checking for a new version of WordPress every hour. To lower the TTL, update the `WP_CORE_SHORT_API_TTL_VERSION` constant in `versions.php` to the impending release version number. This file requires access to a w.org sandbox, so one of them must be on hand for this.

On release day, if a test fails or a security fix is no longer working properly, *punt*. Do not attempt last minute fixes. Either reschedule the release or do not include the fix in the release. Last minute fixes can lead to major bugs.

Are your security fixes ready? Awesome. Got maintenance fixes? Keep reading. If not, skip the next section.

### Maintenance

Unlike security fixes, maintenance fixes can land on trunk any time. There’s a [Trac query](https://core.trac.wordpress.org/tickets/minor) dedicated to tickets targeted at the next minor release. If you’re considering a maintenance release, be sure to run through those tickets in addition to any tickets in mind. Once you’ve determined that your release is a maintenance release, start getting patches landed on the branches. The sooner, the better, so there’s less of a rush at the end.

Ideally, all patches land at least 48 hours before release and a release candidate is built. This can be a formal release candidate or a nightly build that includes all fixes. If you build a beta or release candidate, post about it on [make/core](https://make.wordpress.org/core/tag/release/) along with a list of what fixes are in the release. This will help encourage a wider audience to test the new build.

### Both

Regardless of which kind of release you’re planning, there are a number of things you need to do.

*   Check for breaking changes that would require a dev note. Ensure that those are published ahead of the release and tagged with the minor release number, related major release number, and the dev notes tag (e.g., “4.9, 4.9.2, dev notes”).
*   Verify that the latest version of Akismet is included in WordPress builds. You no longer need to reach out to the Akismet team to see if there is a plugin release coming soon to include in the update. This is is important and prevents a user from seeing an update prompt immediately after creating a new site. This has been automated ([related discussion](https://make.wordpress.org/systems/2020/03/20/build-svn-access-for-sergeybiryukov/#comment-1647)). [Here’s an example](https://build.trac.wordpress.org/changeset/38478) of a commit to build.svn that bumps the Akismet external to the latest version (this is the old, manually method).
*   Ask a member of the Security team to run the private security unit test suite, to make sure no regressions are introduced. If any are found, avoid discussing the details publicly, because some sites (like wordpress.org) run `trunk` or beta/RCs in production. Instead, notify the Security team privately.
*   You’ll want to notify hosts that a release is coming a couple of days ahead of time. Three days is the recommended time frame, but is not always possible depending on release timeline. The security team can assist you with the message to hosts. This message **should not go out until all security patches are ready** (if a security release).
*   If there will be **string changes in your release, notify the Polyglots team ahead of time**.
*   Do a diff on the `src/` directory between the last release tag and the release branch and confirm there are no new files introduced, since these will often break automatic upgrades.
*   A news post is needed for the WordPress.org news blog. Generally speaking, you should start this at least a day ahead of time (the more time, the better). You can copy the format from [previous releases](https://wordpress.org/news/category/releases/). Be sure to grep logs to get a complete list of all contributors to the release. The list of props can most efficiently be gathered by someone who has access to a sandbox to run `wporg/bin/core/props-parser.php`.
*   Alert the systems team (e.g. @barry, @abbe, @sysmonk) about your release so they can plan to have someone available in case there are any issues. The sooner you’ve set a time for release, the sooner you can do this.
*   Prepare Codex pages for each version you intend to release, using the Wiki Template of [Release](https://codex.wordpress.org/Template:Release) (directions are included on that page). If your release is security-related, these pages can be mostly blank until the actual release day, but need to exist as we link to them in WordPress itself.

Now that you’ve done all of that, it’s on to release day.

## Release Day

You’ve made it. Release day can be stressful. The best way to survive release day is to *stay calm*. Things will go wrong. It’s okay, just regroup and keep moving forward. Here’s a list of things that need to get done on release day:

*   The relevant credits file needs to be updated to list any new contributors. That file lives [in the meta repository](https://meta.trac.wordpress.org/browser/sites/trunk/api.wordpress.org/public_html/core/credits).
*   If you’re running a security release, security patches need to be committed to all relevant branches.
*   Once any security patches are committed, move the release process to the [#core](https://make.wordpress.org/core/tag/core/) channel.
    *   start by making an announcement (using the `/here` Slack command) welcoming people to the release party
    *   post a request that committers hold off on any commits until the conclusion of the release, for example: `@committers please refrain from committing during the release process`.
*   Version bumps need to be committed on all relevant branches. [Here’s an example.](https://core.trac.wordpress.org/changeset/44078) Any core committer can do this step. When committing a version bump on the most recent branch please update both the version.php and about.php files. The package.json file should already be updated for the current branch but will need to be updated for any previous branches ([example](https://core.trac.wordpress.org/changeset/39862)).
    *   `package.json` has a single simple bump to `X.Y.Z` (this will likely already be correct, due to the post-release version bump described later in this doc).
    *   `version.php` has one bump to `X.Y.Z-src`. Note the `-src` suffix that should always be included when committing to develop.svn.
    *   `about.php` needs a number bump to `Z` in the “Maintenance and Security Release(s)” heading and a paragraph added describing the changes in the release, using existing strings as defined at the bottom. These strings differ from branch to branch, so please make sure to use the ones from the correct version. It is easiest to copy and paste the appropriate paragraph from elsewhere. If this is the first minor release for a branch, there is also a wrapping div and the aforementioned `h3` to add after the nav tabs. Make note of the possible string combinations for single and multiple security and/or bug fixes. Checkout [a more complete explanation](#selecting-strings) of the differences.
    *   Prepare these changes well in advance and ask for a review. This will help avoid hold-ups during the release process. The version bump and about page can be committed together, they do not need to be separate.
*   On all branches, the release [needs to be tagged](https://build.trac.wordpress.org/browser/tags/). Many people run releases from SVN and rely on the tags to do that. Tagging can be completed by using following commands (be sure to update with your relevant branch and release): `svn cp https://develop.svn.wordpress.org/branches/5.7 https://develop.svn.wordpress.org/tags/5.7.2 -m "Tag 5.7.2"` If you’ve double- and triple-checked to ensure that `https://develop.svn.wordpress.org` is the repository root for your checkout, you can use the `^` shortcut, which would result in this command: `svn cp ^/branches/5.7 ^/tags/5.7.2 -m "Tag 5.7.2"`
*   The release packages need to be built in mission control, from the tag of each version being released. Once it’s packaged, it needs to be tested well, including manually testing updates. (How do you do that? Checkout the [docs](#testing-packages).)
*   Autoupdates need to be enabled in the `versions.php` file, located in the dotorg repository. (This file requires access to a dotorg sandbox, so one of them must be on hand for this.) To enable autoupdates, set the `WP_CORE_LATEST_RELEASE` constant to be the new version number, and set the time that autoupdates should start in `WP_CORE_AUTOUPDATE_RAMP_START`, this should be a few minutes after the anticipated deploy. You should also update the array `wporg_get_version_equivalents()` to match all of the new versions, and the corresponding old version should be added to the array of old versions.
    
    *   The percentage on offer will ramp up from 50% to 100% availability over the course of a specified time. This is controlled by the `WP_CORE_AUTOUPDATE_RAMP_START` and `WP_CORE_AUTOUPDATE_RAMP_PERIOD` constants. These work in conjunction with the previous `WP_CORE_AUTOUPDATE_PERCENT` constant to automate and remove the need for us to manually alter `WP_CORE_AUTOUPDATE_PERCENT` to a lower value during some releases.
    
    *   If it’s a security release, you should also bump `wporg_get_secure_versions()` to match the legacy versions within each branch that is not insecure.
    *   Deploy
*   Verify that everything is working as expected, then bump `WP_CORE_AUTOUPDATE_RELEASE` and deploy.
*   Check auto update stats to make sure they’re normal (success rate above 99.9%, with the remaining 0.1% being safely aborted or rolled back).
*   Language packs for the release need to be built by bumping versions in `translate/bin/update-all-core-packs.sh` and deploying. (This file requires access to a dotorg sandbox.)
*   The wordpress.org/news/ post needs to be published.
*   At this point the release party is complete as only administrative tasks remains
    *   thank attendees for their assistance testing during the release
    *   let committers know they can commit again: `@committers feel free to commit as usual, thank you for your patience during the release`
*   Alert make/polyglots that you have released. Some locales produce their own builds instead of relying on the automatic builds and need to package things on their own. [Here’s an example](https://make.wordpress.org/polyglots/2021/04/15/35197/).
*   Update all HelpHub Version pages:
    *   Add [minor release version page](https://wordpress.org/support/wordpress-version/version-5-7-1/) with the [file diff list](https://codex.wordpress.org/Template:Release) and the link to the news post.
    *   Add version info and link to version page on [WordPress Versions](https://wordpress.org/support/article/wordpress-versions/).
*   Update the Codex [CurrentVersion Template](https://codex.wordpress.org/Template:CurrentVersion) with the new version.
*   If there were any changes to the REST API, update the [REST API changelog](https://developer.wordpress.org/rest-api/changelog/) over at dev hub.
*   In Trac, create (a) [new milestone](https://core.trac.wordpress.org/admin/ticket/milestones)(s) for `X.Y.Z+1` and mark the old milestone(s) as completed. This must be done by a Trac admin.
*   In Trac, create a [new version](https://core.trac.wordpress.org/admin/ticket/versions) for the `X.Y.Z+1` release (including the most recent branch with backports). Delete the date from the `Released` date field. This too must be done by a Trac admin.
*   Bump the latest stable branch version to `X.Y.Z+1-alpha-$REVNUM-src` and the `package.json` version to `X.Y.Z+1` for the next release. After updating, you will also need to run `npm install` to update the `package-lock.json` fie ([example commit](https://core.trac.wordpress.org/changeset/56924)).
*   Rebuild the latest stable branch’s nightly

## Schedule

Assuming you’re following the instructions above and have an ideal schedule (all the time in the world), you’ll want to use the following schedule:

| **When?** | **What?** |
| --- | --- |
| T-7:00:00 | Triage all [targeted tickets](https://core.trac.wordpress.org/tickets/minor). |
| T-5:00:00 | All security patches created, tested, and cleared by the WordPress Security team. |
| T-4:00:00 | Commit all non-security patches to the relevant branch(es). |
| T-4:00:00 | Run the private security unit test suite |
| T-3:00:00 | Notify hosts that a release is coming. |
| T-1:00:00 | Create the WordPress.org/news/ blog post (as draft). |
| T-0:12:00 | If there are security fixes, lower the TTL in the `version-check` API to 60 minutes. (`WP_CORE_SHORT_API_TTL_VERSION` constant in `version.php`.) |
| T-0:05:00 | Commit security patches and run unit tests and security tests. |
| T-0:00:31 | Version bumps on all relevant branches. |
| T-0:00:30 | Build the release package in mission control. Test package and manually test updates. |
| T-0:00:00 | Turn on autoupdates. (`WP_CORE_LATEST_RELEASE` constant, and the `wporg_get_versions()` and `wporg_get_version_equivalents()` functions in `version.php`.) |
| T+0:00:01 | Post the WordPress.org/news/ blog post. |
| T+0:00:15 | Update credits (before or after release). |
| T+0:01:00 | Autoupdates complete (for the most part). |
| T+0:01:00 | Tag the releases. Many people run WordPress from SVN and need a tagged release to deploy. |

## Extras

### Selecting About Page Strings

There are 5 options for strings to choose from for the About page paragraph describing the release.

*   If there is 1 security issue and no bug fixes: `<strong>Version %s</strong> addressed one security issue.`
*   If there are more than one security issues and no bug fixes: `<strong>Version %s</strong> addressed some security issues.`
*   If there are one or more bugs, `_n()` is used with the strings `<strong>Version %1$s</strong> addressed %2$s bug.` and `<strong>Version %1$s</strong> addressed %2$s bugs.` to the determine the proper string for the locale.
*   If there is 1 security issue and one or more bug fixes, `_n()` is used with the strings `<strong>Version %1$s</strong> addressed a security issue and fixed %2$s bug.` and `<strong>Version %1$s</strong> addressed a security issue and fixed %2$s bugs.` to determine the proper string for the locale.
*   If there are more than one security issues and one or more bug fixes, `_n()` is used with the strings `<strong>Version %1$s</strong> addressed some security issues and fixed %2$s bug.` and `<strong>Version %1$s</strong> addressed some security issues and fixed %2$s bugs.` to determine the proper string for the locale.

Defer to other recent point releases for examples on how the strings change along with the numbers. Check the strings and have them reviewed before commit.  

### Testing Package Builds

There are a few ways to test package builds, but using WP-CLI is a fast, effective way. Here’s a run down of commands you can use to test upgrades between versions. This example will be testing between 4.5.2 and 4.5.3 and will assume that some version of WordPress >= 3.7 is already installed.

*   `$ wp core download --version=4.5.2 --force` This will retrieve the version you want to start from.
*   `$ wp core update-db` Get the database where it needs to be.
*   `$ wp core update https://wordpress.org/wordpress-4.5.3.zip` Update to the package you’re testing.
*   `$ wp core update-db` Make sure any database updates run.

Then check your test site to make sure everything is well. Happy upgrade testing!