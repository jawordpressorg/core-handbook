# Updating Bundled Theme Versions

## The Process

Every release, if there have been any changes in a bundled theme, we ship a new version to the WordPress.org theme directory. What follows are detailed steps to update the themes.

1.  Read each theme’s changelog in Trac, and create a changelog file with the highlights (used in Trac tickets, both core and theme review). The changelog should start at the last version of the theme released.
    *   [Twenty Twenty-One](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentytwentyone/)
    *   [Twenty Twenty](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentytwenty/)
    *   [Twenty Nineteen](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentynineteen/)
    *   [Twenty Seventeen](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentyseventeen/)
    *   [Twenty Sixteen](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentysixteen/)
    *   [Twenty Fifteen](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentyfifteen/)
    *   [Twenty Fourteen](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentyfourteen/)
    *   [Twenty Thirteen](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentythirteen/)
    *   [Twenty Twelve](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentytwelve/)
    *   [Twenty Eleven](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentyeleven/)
    *   [Twenty Ten](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentyten/)
2.  Create a new core Trac ticket (like [#54783](https://core.trac.wordpress.org/ticket/54783)) to bump the POT and versions for each theme.
3.  Locally, check out the current version of the theme from the WordPress.org theme directory, e.g., the largest number in each of these directories:
    *   [](https://themes.svn.wordpress.org/twentytwenty/)[Twenty Twenty-One](https://themes.svn.wordpress.org/twentytwenty/)
    *   [Twenty Twenty](https://themes.svn.wordpress.org/twentytwenty/)
    *   [Twenty Nineteen](https://themes.svn.wordpress.org/twentynineteen/)
    *   [Twenty Seventeen](https://themes.svn.wordpress.org/twentyseventeen/)
    *   [Twenty Sixteen](https://themes.svn.wordpress.org/twentysixteen/)
    *   [Twenty Fifteen](https://themes.svn.wordpress.org/twentyfifteen/)
    *   [Twenty Fourteen](https://themes.svn.wordpress.org/twentyfourteen/)
    *   [Twenty Thirteen](https://themes.svn.wordpress.org/twentythirteen/)
    *   [Twenty Twelve](https://themes.svn.wordpress.org/twentytwelve/)
    *   [Twenty Eleven](https://themes.svn.wordpress.org/twentyeleven/)
    *   [Twenty Ten](https://themes.svn.wordpress.org/twentyten/)
4.  Compare with a diff tool to the theme versions in core trunk, is there anything to test or note specifically? Any big unexpected changes?
5.  Test! Load the themes on all recent versions of WordPress (five back is a good place to start). Run the [Theme Check plugin](https://wordpress.org/plugins/theme-check/), and check for any errors or things we didn’t catch in the core cycle.
6.  Bump the theme versions by 0.1 in core, in each stylesheet.
7.  Bump the theme versions by 0.1 in core, in each `package.json` and `package-lock.json` file.
8.  Update “Tested up to” in each readme.
9.  If you’re updating Twenty Ten or Twenty Eleven, wait for the POT update for each theme to be committed, then proceed to make the ZIP packages (a committer is needed to trigger the POT files update). This can be done like this example `php makepot.php wp-theme ../../src/wp-content/themes/twentyeleven twentyeleven.pot`. Run that from the `tools/i18n` directory. For all other default themes, translations are managed by WordPress.org GlotPress, outside of the theme. So this step isn’t necessary for Twenty Twelve and later.
10.  Run the theme build script when one is present (currently Twenty Nineteen, Twenty Twenty, and Twenty Twenty-One). Some themes copy the version into generated files (RTL stylesheets, etc.).
11.  Prepare the new version of each theme.
    *   `svn export` from core repository to a temporary location on your local hard drive.
    *   Do another quick diff with the previous version for a final sanity check.
    *   Zip it: `zip -r [name].zip name` **(Be sure the file name is the same as the theme directory path, otherwise the theme repository will consider the theme new on upload.)**
12.  All contributors with WordPress Core commit access are able to upload new versions of the default themes to WordPress.org through the [theme uploader](https://wordpress.org/themes/getting-started/). **Note**: theme updates will go live *automatically* if manual intervention is not taken beforehand by the theme or meta team. If this is not desired, contact them first to prevent the go-live process. If needed: note in the ticket, “Do not approve yet, please. We’d like to coordinate with the core release*.”*
13.  Ping the release lead to coordinate with the main release process. The updates should be approved automatically. [@Otto42](https://profiles.wordpress.org/Otto42/) can help if anything goes wrong, and the release should know when everything is uploaded and live.

## Tips

*   If a major version of WordPress is also being released with a new bundled theme, the oldest theme being bundled needs to be removed from the build script. **To keep packages sizes down, only the 3 most recent default themes should be included in WordPress packages.**
*   If a theme has any code changes, that means it should get a version number bump and changelog update. Not updating the version number means a new version of the theme can’t be uploaded to the theme directory.
*   Sometimes when looking at the diff of changes after a theme is uploaded, you may notice image or font files showing up as changed when they haven’t been changed. This is a [Trac oddity](https://wordpress.slack.com/archives/core-themes/p1471287983000406).
*   All default themes are marked as special cases on WordPress.org Themes Trac. Themes marked as special still show the theme check errors, but they upload anyway.