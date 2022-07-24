# Installing via SVN

## Overview

This article will walk you through installing the latest WordPress development version via Subversion (SVN).

### What You Will Need Before Starting

*   Create a new database in your local web server using phpMyAdmin. \[[MAMP](https://make.wordpress.org/core/handbook/tutorials/installing-a-local-server/mamp/)\] \[[WampServer](https://make.wordpress.org/core/handbook/tutorials/installing-a-local-server/wampserver/)\] \[[XAMPP](https://make.wordpress.org/core/handbook/tutorials/installing-a-local-server/xampp/)\]
    *   **Note:** If you are using DesktopServer as your local server, you’ll need to choose the **Blank (WordPress SVN)** option from the Blueprint dropdown when creating a new local development site. That will create your database and `wp-config.php` file. Once you’ve created the site, delete the `index.html` and `wp-config-sample.php` files in the development site’s folder (**wordpress-svn.dev**) before you check out a copy of WordPress trunk.
*   Subversion installed on your computer:
    *   Installing SVN on Windows
    *   [Installing SVN on MAC](https://make.wordpress.org/core/handbook/tutorials/installing-a-vcs/#installing-subversion-on-a%c2%a0mac)
    *   [Installing TortoiseSVN](https://make.wordpress.org/core/handbook/tutorials/installing-a-vcs/#installing-tortoisesvn) (Windows)
*   A command line client installed on your computer:
    *   Windows: [Cygwin](http://cygwin.com/)
    *   MAC: [Terminal](http://en.wikipedia.org/wiki/Terminal_(OS_X)) or [Bash](http://www.gnu.org/software/bash/)

## Installing WordPress Using Subversion

The 3.7 release cycle brought a [restructuring of the SVN repository](https://make.wordpress.org/core/2013/08/06/a-new-frontier-for-core-development/), to bring the code, unit tests, and tools together in one place for core contributors to work with.

You can still check out just the source code from [https://core.svn.wordpress.org/trunk/](https://core.svn.wordpress.org/trunk/) to install and test with; however, if you plan on contributing to core, it is recommended that you check out the source code, unit tests, and tools from the new repository to test, fix bugs, and create patches and unit tests with.

The steps outlined below are for installing WordPress via SVN using the new development repository.

### 1\. Check Out WordPress Trunk

#### 1.1 Using TortoiseSVN

Create a folder in your local web server’s public folder (**/htdocs** or **/www**) called **wordpress-svn**. Open that folder, right-click and **select SVN Checkout**.

![TortoiseSVN Checkout Context Menu Screen](https://make.wordpress.org/core/files/2013/09/tortoisesvn-checkout-1.png)

You will be presented with the checkout window. Enter the URL of the wordpress.org SVN repo in URL repository field.

![TortoiseSVN Checkout Window Screen](https://make.wordpress.org/core/files/2013/09/tortoisesvn-checkout-2.png)

The files will begin downloading to that folder.

![TortoiseSVN Checkout File Download Screen](https://make.wordpress.org/core/files/2013/09/tortoisesvn-checkout-3.png)

The green checkmark you see over the icons for the files and folders indicates that is now a versioned file. If you don’t see that icon, refresh the folder content list.

#### 1.2 Using Command Line

You can also use the command line to download the latest version of WordPress trunk. **Note:** Do not type the `$` characters from the examples below – it represents the command prompt.

Tip: you can use the **cd** command to change directories, and the **pwd** command to find out what your current directory is.

Create a directory in your local web server’s public folder called **wordpress-svn** using your command line client:

```bash
$ mkdir ~/wordpress-svn
```

Now switch to the directory you just created:

```bash
$ cd ~/wordpress-svn
```

Next you will check out a copy of WordPress trunk from SVN:

```bash
$ svn co https://develop.svn.wordpress.org/trunk/ .
```

The trailing slash on the URL, and the period at the end of the command, are both important – they make sure that downloaded files from the repository end up in the current directory. If you leave off that dot, you’ll end up creating a new installation directory called “trunk”, which is not what you want.

The following message may appear asking you to accept WordPress’ security certificate:

```bash
Error validating server certificate for 'https://plugins.svn.wordpress.org:443':
 - The certificate is not issued by a trusted authority. Use the
   fingerprint to validate the certificate manually!
Certificate information:
 - Hostname: *.svn.wordpress.org
 - Valid: from Thu, 21 Jun 2012 16:07:30 GMT until Wed, 15 Jul 2015 19:04:26 GMT
 - Issuer: 07969287, http://certificates.godaddy.com/repository, GoDaddy.com, Inc., Scottsdale, Arizona, US
 - Fingerprint: bf:08:a3:de:ab:e4:76:fd:d0:5d:10:d1:c8:de:19:12:5f:bf:71:25
(R)eject, accept (t)emporarily or accept (p)ermanently?
```

Type **p** to accept it permanently.

### 2\. Creating wp-config.php

There are two ways you can create the `wp-config.php` file:

*   **Manual:** Open `wp-config-sample.php` in your plain text editor and enter the `DB_NAME`, `DB_USER`, `DB_PASSWORD`, and `DB_HOST` information for your local web server, then save it as `wp-config.php` in the root directory of your local SVN repository (e.g. **wordpress-svn**).
*   **Automated:** Allow WordPress to create the file during the installation process. If there is no `wp-config.php` file present, you will be asked to create one at the beginning of the install process.

Both are acceptable – use the method that you prefer.

Remember that you will need to **create a MySQL database** to install WordPress in.

### 3\. Run the Install Script

In your web browser, navigate to [http://localhost/wordpress-svn/src/](http://localhost/wordpress-svn/src/) to run the installation process.

**If you created your `wp-config.php` file manually**, you will be presented with the standard WordPress installation screen. You will do the famous “5 minute install” – enter your site title, desired username, choice of a password (twice), and your e-mail address, then **click Install WordPress** to complete the installation. **Click Log In** on the Success screen, enter your username and password, and configure the settings for your preferences.

**If you prefer to let WordPress create the file**, you will be presented with a screen asking if you want to create the file now. **Click Create a Configuration File** to continue. Enter your database credentials for your local web server on the third screen, as well as the database table prefix you want to use (default is `wp_`). After you complete all the fields, **click Submit**. WordPress will check that it can connect to your database with the information you provided. If successful, **click Run the install** to proceed.

You will then do the “5 minute install”, complete all the fields, and **click Install WordPress** to complete the installation. **Click Log In** on the Success screen, enter your username and password, and configure your settings.

**Note:** Under the new configuration, WordPress will create the `wp-config.php` file in the root directory of your local repository, not in the `/src/` directory.

### 4\. Edit wp-config.php

Your local install will be used for beta testing, fixing bugs, creating/testing patches, and running unit tests, so it is important for you to see error messages and notices. Open `wordpress-svn/wp-config.php` in your plain text editor, and set `WP_DEBUG` to **true**:

```php
/**
 * For developers: WordPress debugging mode.
 *
 * Change this to true to enable the display of notices during development.
 * It is strongly recommended that plugin and theme developers use WP_DEBUG
 * in their development environments.
 */
define('WP_DEBUG', true);
```

### 5\. Updating Your Subversion Install

You will need to run the latest version of WordPress trunk on your local SVN install while testing, fixing bugs, and contributing patches.

WordPress 3.7 [introduces automatic updates](https://make.wordpress.org/core/2013/09/24/automatic-core-updates/) for minor stable WordPress releases (3.7.x). This feature, by default, does not work for Subversion installs.

You will need to manually update your local SVN install. The instructions below are for updating to the latest version of WordPress trunk using either TortoiseSVN or the command line.

#### 5.1 Using TortoiseSVN

To update your local WordPress SVN install using TortoiseSVN, right-click in the root folder (e.g. **wordpress-svn**) and **select SVN Update**.

![TortoiseSVN Update Local Subversion Screen](https://make.wordpress.org/core/files/2013/09/tortoisesvn-update-1.png)

The changed files will begin downloading. Most files will show the action as **Updated**, but you may see some with an action of **Added** (indicating a new file), or **Deleted** (indicating a file has been removed).

Once the update is complete, you will see a message at the bottom of the window with the revision number that the update included changed files for.

#### 5.2 Using Command Line

To update your local WordPress SVN install using the command line, **open your command line client** and change the directory to your WordPress SVN install:

```bash
$ cd ~/wordpress-svn
```

You will then use the SVN update command to download any changed files from the WordPress Subversion repository:

```bash
$ svn up
```

## Next Steps

*   [Beta Testing](https://make.wordpress.org/core/handbook/testing/beta/)
*   [Submitting a Patch](https://make.wordpress.org/core/handbook/tutorials/trac/submitting-a-patch/)

### Learn More

*   [Creating a WordPress site using SVN](http://ottopress.com/2011/creating-a-wordpress-site-using-svn/)
*   [WordPress Workflow Tips: Using Subversion Externals for Plugins, Themes and Core](http://kovshenin.com/2012/wordpress-workflow-tips-using-subversion-externals-for-plugins-themes-and-core/)
*   [Installing WordPress With Clean Subversion Repositories](https://codex.wordpress.org/Installing_WordPress_With_Clean_Subversion_Repositories)
*   [Installing/Updating WordPress with Subversion](https://codex.wordpress.org/Installing/Updating_WordPress_with_Subversion)