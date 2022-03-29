# Installing from a Zip File

## Overview

This article will walk you through installing the latest WordPress development version from a zip file.

### What You Will Need Before Starting

*   Create a new database in your local web server using phpMyAdmin. \[[MAMP](https://make.wordpress.org/core/handbook/installing-a-local-server/installing-mamp/#5-creating-a-mysql-database-with-mamp)\] \[[WampServer](https://make.wordpress.org/core/handbook/installing-a-local-server/installing-wampserver/#5-creating-a-mysql-database-with-wampserver)\] \[[XAMPP](https://make.wordpress.org/core/handbook/installing-a-local-server/installing-xampp/#6-creating-a-mysql-database-with-xampp)\]

**Note:** If you are using DesktopServer as your local server, you’ll need to follow those [instructions for creating a new local development site](https://make.wordpress.org/core/handbook/installing-a-local-server/installing-desktopserver/#5-creating-a-new-local-site) instead of the instructions listed below.

## Installing WordPress Trunk from a Zip File

### 1\. Download/Extract WordPress

Download the [latest nightly build](https://wordpress.org/nightly-builds/wordpress-latest.zip) of the WordPress development version and save it to your computer.

Next you will need to open the zip file, and extract the contents into the root of your local web server’s public folder:

*   **MAMP**: Applications/MAMP/htdocs/
*   **WampServer**: wamp/www/
*   **XAMPP**: xampp/htdocs/

A new folder will appear in your local web server’s public folder named **wordpress**. Rename this folder **wordpress-trunk**.

### 2\. Creating wp-config.php

There are two ways you can create the `wp-config.php` file:

*   **Manual:** Open `wp-config-sample.php` in your plain text editor and enter the `DB_NAME`, `DB_USER`, `DB_PASSWORD`, and `DB_HOST` information for your local web server, then **Save the file** as `wp-config.php` in the root of the folder WordPress will be installed in (e.g. **wordpress-trunk**).
*   **Automated:** Allow WordPress to create the file during the installation process. If there is no `wp-config.php` file present, you will be asked to create one at the beginning of the install process.

Both are acceptable – use the method that you prefer.

### 3\. Run the Install Script

In your web browser, navigate to [http://localhost/wordpress-trunk/](http://localhost/wordpress-trunk/) to run the installation process.

**If you created your `wp-config.php` file manually**, you will be presented with the standard WordPress installation screen. You will do the famous “5 minute install” – enter your site title, desired username, choice of a password (twice), and your e-mail address, then **click Install WordPress** to complete the installation. **Click Log In** on the Success screen, enter your username and password, and configure the settings for your preferences.

**If you prefer to let WordPress create the file**, you will be presented with a screen asking if you want to create the file now. **Click Create a Configuration File** to continue. Enter your database credentials for your local web server on the third screen, as well as the database table prefix you want to use (default is `wp_`). After you complete all the fields, **click Submit**. WordPress will check that it can connect to your database with the information you provided. If successful, **click Run the install** to proceed.

You will then do the “5 minute install”, complete all the fields, and **click Install WordPress** to complete the installation. **Click Log In** on the Success screen, enter your username and password, and configure your settings.

### 4\. Edit wp-config.php

Your local install will be used for beta testing and reporting bugs, so it is important for you to see error messages and notices. Open `wordpress-svn/wp-config.php` in your plain text editor, and set `WP_DEBUG` to **true**:

/\*\*
 \* For developers: WordPress debugging mode.
 \*
 \* Change this to true to enable the display of notices during development.
 \* It is strongly recommended that plugin and theme developers use WP\_DEBUG
 \* in their development environments.
 \*/
define('WP\_DEBUG', true);

### 5\. Updating Your Local Install

WordPress 3.7 [introduced automatic updates](https://codex.wordpress.org/Configuring_Automatic_Background_Updates) for minor stable WordPress releases (3.7.x). This feature, by default, will also automatically update your development install daily.

You will need to visit your local install once daily to make the cron task run that triggers the automatic update.

You can check what version you’re using either on the **Dashboard**, or by checking the footer of any admin page (*You are using a development version (3.8-alpha). Cool! Please stay updated.*).

## Next Steps

*   [Beta Testing](https://make.wordpress.org/core/handbook/testing/beta/)