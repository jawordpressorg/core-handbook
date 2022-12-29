# Installing MAMP

## Overview

[MAMP](http://www.mamp.info/en/index.html) is a local server package which runs on a Mac, similar to packages for Windows and Linux, and is easy to set up and configure.

This article will walk you through the steps to install MAMP on your computer.

## Installing MAMP

### 1\. Downloading MAMP

Download the installer package for the [latest free version of MAMP](http://www.mamp.info/en/) by **clicking on the gray elephant icon on the left**, and save the file to your computer. There is also a MAMP Pro version available which has more advanced options, but most users will find the free version works fine for their needs.

![Download MAMP Screen](https://make.wordpress.org/core/files/2013/06/download-mamp.png)

The installer package is around 140mb, so it will take a few minutes for the download to complete.

### 2\. Installing MAMP

Once the download is complete, **double-click the zip file** and extract the contents to your desktop. You will see an installer file called **MAMP\_2.1.4.pkg** (your version may be different) – **double-click that file** to run the installer. There are 7 steps in the MAMP install process:

*   **Introduction – Welcome to the MAMP Installer Screen**: MAMP will guide you through the steps necessary to install the application. **Click Continue** to go to the next step.
*   **Read Me – Important Information Screen**: The installer will install both the MAMP and MAMP PRO applications. Do not remove or rename the MAMP folder. **Click Continue** for the next step.
*   **License – Software License Agreement Screen**: Select the language you wish to use with MAMP. Read the license agreement, **click Agree** in the small dropdown to accept the agreement, then **click Continue**.
*   **Destination Select**: MAMP must be installed in the Applications folder to work properly. **Click Continue** for the next step.
*   **Installation Type – Standard Install on “Macintosh HD” Screen**: This screen tells you how much disk space MAMP will use on your hard drive. **Click Install** to perform a standard installation of MAMP for all users of your computer. You can **click the Customize** button, which will allow you to opt out of installing MAMP PRO. **Click Install** to continue. The installer will prompt you to authenticate with your admin username and password. Enter the information requested, then **click Install Software**.
*   **Installation – Installing MAMP Screen**: The installation process takes several minutes. The screen will show you what part of the process is occurring, along with the estimated time remaining until installation is complete.
*   **Summary – Success Screen**: MAMP has been installed successfully. **Click Close**.

### 3\. Starting MAMP

The MAMP Welcome page should automatically open in your browser after installation, which indicates that MAMP has been installed correctly. This page contains links to your PHP configuration (phpinfo), phpMyAdmin, as well as the standard MAMP configurations.

If you don’t see the Welcome page, go to [http://localhost:8888/MAMP/](http://localhost:8888/MAMP/) in your browser.

The Welcome page also shows you the MySQL connection information you will need when you install WordPress:

![MySQL Connection Information on Welcome Page Screen](https://make.wordpress.org/core/files/2013/02/mamp6.png)

The MAMP control panel also opens, which shows that your local MAMP server is working. You should see green indicators next to **Apache Server** and **MySQL Server**:

![MAMP Control Panel Screen](https://make.wordpress.org/core/files/2013/06/mamp-control-panel.png)

From the control panel, you can stop your local servers by clicking **Stop Servers**, or start them by clicking **Start Servers**. You can also **open the Welcome page**, and access **Preferences**.

Note: When starting and stopping services or changing the configuration, MAMP may ask you for your admin username and password, which is required to make system changes in OS X.

![MAMP Change Authentication Screen](https://make.wordpress.org/core/files/2013/06/mamp-change-authentication.png)

### 4\. Configuring MAMP

During installation, MAMP sets the default ports for both Apache (port 8888) and MySQL (port 8889). Normally, web servers use port 80 for Apache, and port 3306 for MySQL. This allows access to web pages without having to append a port number to the domain in the URL.

In MAMP, you have to append the port number to **localhost** in order to access web pages, i.e. [http://localhost:8888/wordpress-trunk/](http://localhost:8888/wordpress-trunk/).

You can change the ports to the normal Apache/MySQL ports by **clicking Preferences** in the control panel, then **clicking Ports**. You must have administrator privileges for your computer to do this.

![MAMP Change Default Ports Screen](https://make.wordpress.org/core/files/2013/06/mamp-change-ports.png)

Changing those ports would allow you to access your local WordPress install without the port number, i.e. [http://localhost/wordpress-trunk/](http://localhost/wordpress-trunk/).

**Caution:** There are other applications that use port 80, such as Skype. If you find you are unable to start Apache or access your local web pages, then you’ll need to find the conflicting application, and try to resolve the port conflict.

For Skype, go to **Tools > Options**, click on **Advanced**, and then **Connections**. Uncheck the box next to **Use port 80 and 443 as alternatives for incoming connections**. Click **Save Options**, then restart Skype.

### 5\. Creating a MySQL Database With MAMP

In MAMP, you need to **open phpMyAdmin** to create a MySQL database. If you have installed MAMP with the default ports, **open the Welcome page** in your browser ([http://localhost:8888/MAMP/](http://localhost:8888/MAMP/)), then **click the phpMyAdmin link** at the top of the screen.

The main phpMyAdmin screen will appear. To create a database, click **Databases** in the top navbar.

![MAMP Navbar On phpMyAdmin Main Screen](https://make.wordpress.org/core/files/2013/06/database-create-phpmyadmin-navbar.png)

On the screen that appears, you need to enter the database name (for example, **root\_wordpress-trunk**) in the left field, choose your database connection collation from the dropdown box (**utf8\_unicode\_ci**), then **click Create**.

![MAMP Create Database In phpMyAdmin Screen](https://make.wordpress.org/core/files/2013/06/database-create-name-collation.png)

You will see a success message once the database has been created, and your new database will appear in the list on the left.

![MAMP Database Creation Success Message Screen](https://make.wordpress.org/core/files/2013/06/database-create-success-message.png)

The default phpMyAdmin user, **root**, is automatically assigned to the database upon creation, and has a password of **root**. The database connection info you will need to use when installing WordPress locally is:

```php
/** The name of the database for WordPress */
define('DB_NAME', 'root_databasename');</p>
<p>/** MySQL database username */
define('DB_USER', 'root');</p>
<p>/** MySQL database password */
define('DB_PASSWORD', 'root');</p>
<p>/** MySQL hostname */
define('DB_HOST', 'localhost');
```

### 6\. Shutting Down MAMP

To shut down MAMP, you will need to **click Stop Servers** to shut down the Apache and MySQL services. The indicators will turn red once all services have been shut down. You will then **click Quit** to close the program.

![MAMP Shutdown Screen](https://make.wordpress.org/core/files/2013/06/mamp-shutdown.png)

## Next Steps

*   [Installing WordPress From A Zip File](https://make.wordpress.org/core/handbook/tutorials/installing-wordpress-locally/from-zip/)
*   [Installing WordPress Via SVN](https://make.wordpress.org/core/handbook/tutorials/installing-wordpress-locally/from-svn/)