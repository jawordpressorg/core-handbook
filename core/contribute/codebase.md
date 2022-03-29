# The WordPress Codebase

WordPress is managed by a centralized version control system called [Subversion](http://subversion.tigris.org/). A mirror of this repository is also available via [Git](http://git-scm.com/), a distributed VCS.

The WordPress codebase can be accessed in a number of ways: using Subversion, using Git, through Trac (the bug tracker), and via direct download:

*   **Subversion:** The repository is located at [https://develop.svn.wordpress.org/](https://develop.svn.wordpress.org/). The main development branch – called trunk– is [https://develop.svn.wordpress.org/trunk](https://develop.svn.wordpress.org/trunk).
*   **Git:** The repository is located at git://develop.git.wordpress.org/. There is also a [mirror of the WordPress repository on Github](https://github.com/wordpress/wordpress), though issues and pull requests on Github are not currently accepted.
*   **Trac:** The repository can be viewed through the browser at [https://core.trac.wordpress.org/browser/](https://core.trac.wordpress.org/browser/). A log of changesets can be viewed at [https://core.trac.wordpress.org/log/](https://core.trac.wordpress.org/log/).
*   **Download:** The latest stable version of WordPress can be downloaded at [https://wordpress.org/latest.zip](https://wordpress.org/latest.zip). The latest nightly build (2300 GMT) can be found at [https://wordpress.org/nightly-builds/wordpress-latest.zip](https://wordpress.org/nightly-builds/wordpress-latest.zip).

## How Code In WordPress Is Organized

If you are using the “develop” repository, as mentioned above, the core codebase is in the `src` directory. A downloaded package serves a “built” version of this directory, thus placing these files in the root. The codebase consists of around 1000 files and directories.

Initial bootstrap files, such as `index.php`, `wp-load.php`, `wp-blog-header.php`, and `wp-settings.php`, appear in this `src` directory. Special handlers such as the XML-RPC, trackback, and comment submission endpoints, are also in the root.

The remaining files are divided into three distinct directories: **wp-admin**, **wp-includes**, and, to some extent, **wp-content**.

### wp-content

The **wp-content** directory consists of user-defined and site-specific files, including themes, plugins, and uploads. The repository only contains a **wp-content** directory for the bundled plugins (e.g. Hello Dolly) and themes (e.g. Twenty Fifteen).

### wp-includes

The **wp-includes** directory consists of the primary core and third-party libraries for WordPress. Many of these files are loaded as the application is bootstrapped.

The files in **wp-includes** go by a (mostly) standard set of prefixes and suffixes:

*   `class-*.php` – PHP classes. Some of these are external libraries.
*   `ms-*.php` – Code specific to WordPress multisite functionality.
*   `default-*.php` – Code that implements or defines default functionality, namely constants, widgets, and filters.
*   `*deprecated.php` – Functions which are deprecated.
*   `*-template.php` – Template functions for the relevant API.

The files in **wp-admin/includes** follow similar naming conventions.

### wp-admin

The **wp-admin** directory contains the code powering the administration area of WordPress. The primary bootstrap is `wp-admin/admin.php`. Other special files include `admin-header.php` and `admin-footer.php`, the AJAX handler `admin-ajax.php`, and the generic POST handler `admin-post.php`. Most of the files in the **wp-admin** directory are pages in the WordPress admin interface.

The **wp-admin/includes** directory consists of the primary core and third-party libraries available and used in the administration area. Some of these are loaded as the admin is bootstrapped; see `wp-admin/includes/admin.php` for the primary list of files included.

### JavaScript and CSS

The **wp-admin** and **wp-includes** directories also have **js** and **css** directories, for scripts and styles, respectively. Third-party scripts are packaged in a compressed and minified state, which are available at [https://wordpress.org/download/source/](https://wordpress.org/download/source/). Both minified and development versions are included for core scripts and styles, with the minified versions receiving the suffixes `.min.js` and `.min.css`.

The **wp-includes** directory has a number of third-party libraries in folders. The **wp-includes/js** directory, in particular, has **jquery** and **tinymce** directories, with the former holding jQuery, jQuery UI, and various plugins, and the latter holding TinyMCE and various TinyMCE core and WordPress-specific extensions.

The `wp-includes/script-loader.php` file registers all bundled scripts and styles. Each script and style is given a date-specific version number (yyyymmdd), which is bumped by a committer when the stylesheet changes. The version number is added to the URL, forcing the browser cache to clear and the new CSS or JavaScript to be loaded.

## Searching and Browsing Code History

To search the codebase, developers rely on either a project search tool in their code editor or IDE, or command-line utilities such as **ack** or **grep**. Browsing the codebase on Trac is manageable, but one particular feature is noteworthy: Trac includes an excellent user interface for the Subversion **blame** command.

To **blame** a line of code means to determine who last edited that line and when. To access this in Trac when browsing a file, click the **Annotate** link in the top right corner. Most consider the UI far more efficient than individual svn blame commands.

Core committers do not make changes to WordPress lightly, and commits should never occur without as complete understanding of the existing code as possible. If the code causes a bug, was that always the case? When was it introduced? Why? Is the code in question a fix for a different bug? These questions are very important.

Note: To learn more about code history, read the section on [Researching Code History With Subversion Annotate](https://make.wordpress.org/core/handbook/svn/code-history/).

## Installation

When a WordPress install is initially run, if a `wp-config.php` file cannot be located, the `wp-load.php` file will suggest you visit `wp-admin/setup-config.php` to create the configuration file.

Once this is done, you’ll be taken to `wp-admin/install.php`. At this point, the database tables are created. The database schema is stored in `wp-admin/includes/schema.php`, and the installation libraries are primarily located in `wp-admin/includes/upgrade.php` *(where else are they located? we should be specific here)*.

## Database Upgrades

Database upgrade instructions are included in `wp-admin/includes/upgrade.php`. Whenever a database change is needed with a new version of WordPress – whether that means altering the database structure, or updating some database content – an upgrade routine can be triggered. Indeed, you can safely update from WordPress 0.70 to the latest version and the database will keep up with the more than a decade of changes.

Knowing *when* to upgrade is handled by a number in `wp-includes/version.php`, the WordPress database version. This number corresponds to a revision number of the codebase, generally the revision that last introduced a database upgrade routine. When the number in the code differs from the number stored in the database, the routines in `wp-admin/includes/upgrade.php` are run.

The function `wp_upgrade()` calls `upgrade_all()` (among other functions), which will run the appropriate routines in sequence. In order to trigger a new routine, a “schema bump” – changing the right numbers, including the WordPress database version in `version.php` – needs to occur.

Changes to the database structure are handled by a function called `dbDelta()`, which takes the table definitions, compares them to the existing schema, and makes any changes that are required – for example, adding new tables, altering fields, adding indexes. For `dbDelta()` to run over the core table definitions, the DB version in `version.php` simply needs to be bumped.

## File Updates

Core developers generally distinguish between database “upgrades” and version “updates.” Updating WordPress to the newest codebase (via the user interface) triggers a complex series of actions.

Prior to any update, WordPress has already polled **api.wordpress.org** to determine whether it needs to update, and if so, where to find the new version. Once the update is triggered, WordPress will download the ZIP archive and unzip it into a temporary directory in **wp-content/upgrade**. A single file, `wp-admin/includes/update-core.php`, will be copied out of the temporary directory and over the existing `wp-admin/includes/update-core.php`, at which point it will be executed. Thus, the newly downloaded code handles the main process of copying over the new files. This allows us to provide instructions specific to the new version, such as which files are old and can be removed.

## Exploring The Code

These tools may be useful in exploring the WordPress codebase:

*   [The Official WordPress Code Reference](https://developer.wordpress.org/reference/)
*   [QueryPosts.com](http://queryposts.com/)
*   [Westi’s PHPXref](http://phpxref.ftwr.co.uk/wordpress/nav.html?index.html)
*   [The Git mirror, mirrored to GitHub](https://github.com/WordPress/WordPress/)