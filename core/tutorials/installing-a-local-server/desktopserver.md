# Installing DesktopServer

## Overview

[DesktopServer](http://serverpress.com/products/desktopserver/) is a local server package that runs on Mac and Windows. The installation, configuration, and site creation steps are almost identical for both platforms.

This article will walk you through the steps to install DesktopServer on your computer.

## Installing DesktopServer

### 1\. Downloading DesktopServer

Download the installer file for the [latest free version of DesktopServer](http://serverpress.com/downloads/) (currently 3.9.4), and save the file to your computer. Scroll down the page to download the free version for your operating system.

![Download DesktopServer Screen](https://make.wordpress.org/core/files/2013/07/desktopserver-download.png)

The download is about 100mb, so it will take a few minutes.

### 2\. Installing DesktopServer

Once the download is complete, extract the contents of the zip file to a folder on your computer.

You should use the DesktopServer installer for new installations, as it performs checks for conflicts on your computer. The installer file’s icon is a blue box with a green arrow. **Open the installer file** to begin the installation.

The first screen that appears will ask you whether you want to install, upgrade, or uninstall DesktopServer. **Choose New DesktopServer Limited Installation**, then **click Continue**.

![DesktopServer Choose New Installation Screen](https://make.wordpress.org/core/files/2013/07/desktopserver-install-1.png)

You will be presented with the License Agreement screen next. Read the agreement, then **click Accept**.

![DesktopServer License Agreement Screen](https://make.wordpress.org/core/files/2013/07/desktopserver-install-2.png)

The next screen shows DesktopServer extracting the files into the correct location on your computer:

*   **Mac:** Macintosh HD/Applications/XAMPP/
*   **Windows:** C:/xampplite/

![DesktopServer Unpacking Files Screen](https://make.wordpress.org/core/files/2013/07/desktopserver-install-3.png)

Once all of the files have been extracted, the Installation Complete screen will appear. **Click Finish** to complete the installation.

![DesktopServer Installation Complete Screen](https://make.wordpress.org/core/files/2013/07/desktopserver-install-4.png)

A small window will appear, with the install location and how to start DesktopServer. **Click OK** to close the window, then **click Finish** on the main screen to close the installer.

![DesktopServer Close Installer Screen](https://make.wordpress.org/core/files/2013/07/desktopserver-install-5.png)

### 3\. Configuring DesktopServer

DesktopServer includes the latest stable release of WordPress when you install the program (currently 3.6.1). The program also allows you to add other versions of WordPress in the Blueprints folder, including beta releases, as well as create a custom package for installing WordPress via Subversion (SVN). Any new packages you create will automatically show up in the Blueprint dropdown when you create a new local site. The following shows the location of the Blueprints folder:

*   **Mac:** Macintosh HD/Applications/XAMPP/blueprints/
*   **Windows:** C:/xampplite/blueprints/

To add the latest alpha release, **download the zip file of the [latest nightly build](https://wordpress.org/nightly-builds/wordpress-latest.zip)**, and place it in the Blueprints folder. Make sure the zip file has the appropriate beta release name (e.g. **wordpress-3.8-alpha.zip**).

![DesktopServer Blueprints Folder File Structure](https://make.wordpress.org/core/files/2013/07/desktopserver-blueprints-file-structure-1.png)

To create a blank package for installing WordPress via SVN, **create a new subfolder** called **Blank (WordPress SVN)** in the Blueprints folder. **Copy the `index.html` file** from the **Blank (non-WordPress)** subfolder, then add a copy of the `wp-config-sample.php` file from the latest WordPress release. This file is needed during site creation so DesktopServer can create a `wp-config.php` file with the database credentials for that local site.

![DesktopServer Blank (WordPress SVN) File Structure](https://make.wordpress.org/core/files/2013/07/desktopserver-blueprints-file-structure-2.png)

### 4\. Starting DesktopServer

Once you’ve completed the installation and configuration process, **navigate to the install directory** and open the program.

Tip: Create a program shortcut (or alias) on your desktop or dock to make it easier to start DesktopServer each time.

DesktopServer needs to run with Administrator Privileges on both Mac and Windows. On the start-up screen, **select Yes**, then **click Next** to restart DesktopServer and grant those privileges.

![DesktopServer Grant Administrator Privileges Screen](https://make.wordpress.org/core/files/2013/07/desktopserver-start-1.png)

Next you will need to start Apache and MySQL services. On the next screen, **select Yes**, then **click Next**.

![DesktopServer Start Apache and MySQL Services Screen](https://make.wordpress.org/core/files/2013/07/desktopserver-start-2.png)

The final startup screen will appear, indicating that both services have been started. **Click Next** to create your first local site.

![DesktopServer Services Started Screen](https://make.wordpress.org/core/files/2013/07/desktopserver-start-3.png)

### 5\. Creating A New Local Site

Now it’s time for you to create your first local site to use for testing WordPress. **Select Create a New Development Website**, then **click Next**.

![DesktopServer Create A New Development Website Screen](https://make.wordpress.org/core/files/2013/07/desktopserver-create-new-site-1.png)

The next screen asks for the information about the site you want to create.

*   **Site Name:** Enter your desired site name (e.g. **wordpress-trunk**) in the first box.
*   **Blueprint:** To install the WordPress alpha release, you will **choose WordPress-3.8-alpha.zip** (or the latest beta release) for your blueprint.
*   **Site Root:** DesktopServer will automatically display the default location where WordPress will be installed. If you would like to change the location to another folder (such as **/htdocs/**), **click Browse**, select the desired folder, then **click Okay**.

Once you have completed all 3 fields, **click Create**.

![DesktopServer Create A New Development Website With 3.6 Beta4 Selected Screen](https://make.wordpress.org/core/files/2013/07/desktopserver-create-new-site-2.png)

Next, DesktopServer will create the source folder, virtual host, and server name entries; create a database and pre-configure the `wp-config.php` file with the database information; and restart the Apache and MySQL services. Once those are done, **click Next** to continue.

![DesktopServer Create Local Site Process Screen](https://make.wordpress.org/core/files/2013/07/desktopserver-create-new-site-3.png)

You will be able to access your WordPress install at the URL listed on the next screen. Clicking the URL will bring up the WordPress install screen, where you will enter your site title, desired username, choice of a password (twice), and your e-mail address. **Click Install WordPress** to complete the installation.

![DesktopServer Access New Site Screen](https://make.wordpress.org/core/files/2013/07/desktopserver-access-new-site.png)

**Note:** After you have finished installing the latest WordPress beta release, you will need to do the following 2 things:

*   It is important that you to set `WP_DEBUG` to **true** in your `wp-config.php` file to display errors, warnings, etc. during testing:
    
    /\*\*
     \* For developers: WordPress debugging mode.
     \*
     \* Change this to true to enable the display of notices during development.
     \* It is strongly recommended that plugin and theme developers use WP\_DEBUG
     \* in their development environments.
     \*/
    define('WP\_DEBUG', true);
    
*   You will need to install and activate the [WordPress Beta Tester plugin](https://wordpress.org/extend/plugins/wordpress-beta-tester/) to upgrade the install from the latest beta release to the latest bleeding-edge version of WordPress trunk. Once installed, **follow the directions** for [configuring the plugin](https://make.wordpress.org/core/handbook/installing-wordpress-locally/installing-from-a-zip-file/#4-install-the-beta-tester-plugin) to update to the bleeding edge nightlies.

### 6\. Shutting Down DesktopServer

To shut down DesktopServer, double-click the shortcut on your screen. On the first screen, **select Stop or restart web and database services**, then **click Next**.

![DesktopServer Stop Services Screen](https://make.wordpress.org/core/files/2013/07/desktopserver-shutdown-1.png)

You will be asked to confirm whether you want to restart or stop the services. **Select Stop web and database services**, then **click Next**.

![DesktopServer Confirm Stop Services Screen](https://make.wordpress.org/core/files/2013/07/desktopserver-shutdown-2.png)

DesktopServer will then shut down the Apache and MySQL services. Once this task is completed, **click Close** to exit the program.

![DesktopServer Close Program Screen](https://make.wordpress.org/core/files/2013/07/desktopserver-shutdown-3.png)

## Next Steps

*   [Installing WordPress Via SVN](https://make.wordpress.org/core/handbook/tutorials/installing-wordpress-locally/from-svn/)