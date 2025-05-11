# Beta Testing

A valuable contribution an individual can make to WordPress development is to test WordPress, even if you are not a developer. Before every stable release of WordPress, pre-release versions are made available for testing. You can download the pre-releases and test them, so that the WordPress developers can fix problems before the new version is made available to the public.

If you want to be on the bleeding edge of development, even before pre-release versions are put together, you can also check out the latest software from the [WordPress Subversion (SVN) repository](https://make.wordpress.org/core/handbook/tutorials/installing-wordpress-locally/from-svn/). Or, you can get the “[nightly build](https://wordpress.org/nightly-builds/wordpress-latest.zip)” (which is created from the Subversion repository) — almost as up-to-date as the instantaneous Subversion repository.

To get started, install the [**WordPress Beta Tester**](https://wordpress.org/extend/plugins/wordpress-beta-tester/) plugin. Visit Plugins > Add New, type “wordpress beta tester” in the search field, and then click/tap “Install Now”.

1.  Backing up first is sensible.
2.  Go to Plugins > Add New and search for “WordPress Beta Tester”
3.  Click or tap the “Install Now” button for the WordPress Beta Tester plugin
4.  Go to Tools > Beta Testing (or Network Admin > Settings > Beta Testing on multisite)
5.  Select the  “Bleeding edge nightlies” option to follow development for the next major release of WordPress, or “Point release nightlies” to follow development of the next point release.
6.  Click or tap the “Save Changes” button
7.  Go to Dashboard > Updates
8.  Click or tap the “Update Now” button
9.  Return to Tools > Beta Testing to see options for Beta/RC to update to the next released beta or RC of the “Point release” or “Bleeding edge”.

Once the plugin is installed, navigate to Tools > Beta Testing and review the settings:

*   **Point release nightlies.** This keeps you on the same major version but provides nightly builds for the next minor version. For example, when the stable version is 6.6.2, selecting this will provide updates being prepared for the unreleased 6.6.3 version. After 6.6.3 is released, this will provide the nightly build of 6.6.4.
*   **Bleeding edge nightlies.** Selecting this will put you on the track for the next major version and provide nightly builds. These are often unstable and changes will happen frequently.
*   **Beta/RC.** Selecting this will update to the next released beta or RC on whichever branch you are currently running.

You can also use WP CLI to directly update your WordPress to trunk version by doing:

```
wp core update --version=trunk
```

If you find bugs while testing pre-release or already-released versions of WordPress, see [Reporting Bugs](https://make.wordpress.org/core/handbook/reporting-bugs/ "Reporting Bugs") or post in the [Alpha/Beta support forum](https://wordpress.org/support/forum/alphabeta).

New features are often [developed as plugins](https://make.wordpress.org/core/features-as-plugins/). [Feature plugins](https://wordpress.org/plugins/browse/beta/) can be installed from the beta testing tab on the plugin install screen of your WordPress dashboard. Navigate to Plugins > Add New > Beta Testing.

[![Screen Shot 2015-05-23 at 10.28.50 AM](https://make.wordpress.org/core/files/2011/12/Screen-Shot-2015-05-23-at-10.28.50-AM-300x209.png)](https://make.wordpress.org/core/files/2011/12/Screen-Shot-2015-05-23-at-10.28.50-AM.png)

The plugins listed here are proposed for future versions of WordPress. They are glimpses of the future that are under active development. New versions are released regularly, sometimes daily. Some feature plugins require that you follow bleeding edge nightlies.

Tracking bleeding edge nightlies with the beta tester plugin and installing feature plugins will make all of the latest software available for beta testing. If you go this route, here are some useful testing resources (and thank you very much):

*   [make/core](https://make.wordpress.org/core/) is the main WordPress development blog.  It is active and will keep you up-to-date on what’s happening right now in WordPress development.
*   [make/flow](https://make.wordpress.org/flow/) contains visual records and visual bug reports from the [Flow Patrol](https://make.wordpress.org/flow/handbook/) team.
*   The [Flow Patrol handbook](https://make.wordpress.org/flow/handbook/) includes information on [triage](https://make.wordpress.org/flow/handbook/triage/) if you want to get into triaging posts on make/flow.

When done testing, rolling your site back to the latest stable production release can be done with a tap/click of “Re-install Now ” on the Dashboard > Updates screen.

[![Screen Shot 2015-06-29 at 1.25.59 pm](https://make.wordpress.org/core/files/2011/12/Screen-Shot-2015-06-29-at-1.25.59-pm-300x111.png)](https://make.wordpress.org/core/files/2011/12/Screen-Shot-2015-06-29-at-1.25.59-pm.png)

Tap Re-Install Now to roll back to a stable release