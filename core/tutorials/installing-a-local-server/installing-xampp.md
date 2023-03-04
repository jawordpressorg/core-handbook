# Installing XAMPP

## Overview

[XAMPP](http://www.apachefriends.org/en/xampp.html) is an easy to install Apache distribution containing MySQL, PHP and Perl. There are packages for [Windows](http://www.apachefriends.org/en/xampp-windows.html), [Mac](http://www.apachefriends.org/en/xampp-macosx.html), and [Linux](http://www.apachefriends.org/en/xampp-linux.html).

This article will walk you through the steps to install XAMPP on your computer.

Note: These are the Windows installation instructions – see the Apache Friends website for the [Mac](http://www.apachefriends.org/en/xampp-macosx.html) and [Linux](http://www.apachefriends.org/en/xampp-linux.html) installation instructions.

## Installing XAMPP

### 1\. Downloading XAMPP

Download the installer file for the [latest version of XAMPP](http://www.apachefriends.org/en/xampp-windows.html#641), and save the file to your computer.

![Download XAMPP Screen](https://make.wordpress.org/core/files/2013/03/download-xampp.png)

### 2\. Installing XAMPP

Next, you need to open the folder where you saved the file, and double-click the installer file.

You will be prompted to select the language you wish to use in XAMPP. **Click the arrow** in the dropdown box, **select your language** in the list, then **click OK** to continue the installation process.

![Installing XAMPP: Select Your Language Screen](https://make.wordpress.org/core/files/2013/03/installing-xampp-1.png)

For Windows 7 users, you will see a window pop up, warning you about User Account Control (UAC) being active on your system. **Click OK** to continue the installation.

![Installing XAMPP: UAC Warning Screen](https://make.wordpress.org/core/files/2013/03/installing-xampp-2.png)

Next you will see the Welcome To The XAMPP Setup Wizard screen. **Click Next** to continue the installation.

![Installing XAMPP: Welcome To The XAMPP Setup Wizard Screen](https://make.wordpress.org/core/files/2013/03/installing-xampp-3.png)

The Choose Components screen will appear next. This screen will allow you to choose which components you would like to install. To run XAMPP properly, all components checked need to be installed. **Click Next** to continue.

![Installing XAMPP: Choose Components Screen](https://make.wordpress.org/core/files/2013/03/installing-xampp-4.png)

Next you will see the Choose Install Location screen. Unless you would like to install XAMPP on another drive, you should not need to change anything. **Click Install** to continue.

![Installing XAMPP: Choose Install Location Screen](https://make.wordpress.org/core/files/2013/03/installing-xampp-5.png)

XAMPP will begin extracting files to the location you selected in the previous step.

![Installing XAMPP: Unpacking Files Screen](https://make.wordpress.org/core/files/2013/03/installing-xampp-6.png)

Once all of the files have been extracted, the Completing The XAMPP Setup Wizard screen will appear. **Click Finish** to complete the installation.

![Installing XAMPP: Completing The XAMPP Setup Wizard Screen](https://make.wordpress.org/core/files/2013/03/installing-xampp-7.png)

The Installation Complete screen will now appear. **Click Finish** to begin using XAMPP.

![Installing XAMPP: Installation Complete Screen](https://make.wordpress.org/core/files/2013/03/installing-xampp-81.png)

After clicking Finish in the previous screen, you will be asked if you want to open the XAMPP Control Panel. **Click Yes**.

![Installing XAMPP: Open Control Panel Screen](https://make.wordpress.org/core/files/2013/03/installing-xampp-9.png)

### 3\. Starting XAMPP

The XAMPP Control Panel allows you to manually start and stop Apache and MySQL, or install them as services.

![XAMPP Control Panel Screen](https://make.wordpress.org/core/files/2013/03/xampp-control-panel-1.png)

To start Apache or MySQL manually, **click the Start button** under **Actions** next to that module.

![Start XAMPP Modules Manually Screen](https://make.wordpress.org/core/files/2013/03/xampp-control-panel-2.png)

Depending on your security settings, Windows 7 users will probably have a small window open, asking if you want to allow **xampp-control.exe** to make modifications to your computer. **Click Yes** to allow Apache or MySQL to start.

If you plan on using XAMPP frequently, you may want to consider installing Apache and MySQL as services on your computer. The advantage to this is that both modules will already be running once the XAMPP control panel opens.

To install Apache and MySQL as services, **click the red X** to the left of each module under **Services**. You will see a small window open, asking you to confirm that you want to install it as a service. **Click Yes** to complete the installation. Repeat for the other module.

![Installing Apache As A Service Screen](https://make.wordpress.org/core/files/2013/03/xampp-control-panel-3.png)

Once again, you may have a security window open, asking if you want to allow the modifications to your computer. **Click Yes** to allow it.

The **red X** will change to a **green check mark** once the service has been installed successfully.

**Important:** After the initial setup is complete, you will need to run XAMPP as an administrator on Windows 7 when you start the program again. To do that, **click Start**, find **XAMPP Control Panel** in your Programs list, then right-click and select **Run As Administrator**.

![Run XAMPP As Administrator](https://make.wordpress.org/core/files/2013/03/xampp-run-as-admin.png)

### 4\. Configuring XAMPP

The default XAMPP install is already pre-configured to run a local web server comparable to most web hosting servers. However, there are a couple basic configuration changes you can make to increase your productivity.

The first change will be to set the default text editor. As you can see, XAMPP defaults to Notepad, the native Windows text editor. **Click the folder button** to the right to open the file explorer. Navigate to the folder for your favorite text editor, **select the .exe file**, then **click Open**.

![Configuring XAMPP: Set Default Text Editor Screen](https://make.wordpress.org/core/files/2013/03/configure-xampp-2.png)

The next change is to select your desired font for the logs that XAMPP creates. If you are trying to track down an issue, you will spend time reading different logs, so choose a font that is easy for you to read. Click on **Log Options**, then select your desired font and font size, then **click Save**.

![Configuring XAMPP: Set Default Font For Logs Screen](https://make.wordpress.org/core/files/2013/03/configure-xampp-3.png)

After making those changes, **click Save** in the main configuration window.

![Configuring XAMPP: Save Settings Screen](https://make.wordpress.org/core/files/2013/03/configure-xampp-4.png)

If you find that you need to make a configuration change to Apache, PHP, or MySQL, **click the Config button** for that module to bring up a context menu with links to the config files for that module. The file will open in the default text editor you chose earlier.

![Configuring XAMPP: Advanced Settings Screen](https://make.wordpress.org/core/files/2013/03/configure-xampp-1.png)

### 5\. Securing Your XAMPP Install

Once the configuration is done, go to **http://localhost/** in your web browser. You will see the XAMPP splash screen first, asking you to select your language. The web-based XAMPP panel will then appear.

![XAMPP Web Panel Welcome Screen](https://make.wordpress.org/core/files/2013/03/xampp-web-panel-welcome.png)

It is recommended that you secure your XAMPP install with a unique username and password for both the web panel and for phpMyAdmin.

Click the **Security** link in the left sidebar. The **XAMPP Security** screen will appear. A table will show you the current security status for each component.

To secure the XAMPP panel and phpMyAdmin, click the **http://localhost/security/xamppsecurity.php** link to open the Security Console.

![XAMPP Security Console Screen](https://make.wordpress.org/core/files/2013/03/xampp-security-console.png)

The first section deals with the MySQL user. By default, the MySQL administrator (root) has no password in XAMPP. To secure MySQL, enter your desired password in the **New Password** field, then again in the **Repeat the new password** box. Choose your authentication method (http or cookie), then click **Password Changing**.

The second section deals with securing the XAMPP web panel. Enter a unique username in the **Username** field, a strong password in the **Password** field, then **click Make safe the XAMPP directory**.

Navigate to the XAMPP Security section to check the security status of each component after completing these steps. The XAMPP directory, MySQL, and phpMyAdmin should now have a **Secure** status next to them.

![XAMPP Security Status Screen](https://make.wordpress.org/core/files/2013/03/xampp-security-status.png)

### 6\. Creating a MySQL Database With XAMPP

In XAMPP, a database is created and accessed via phpMyAdmin. You can access phpMyAdmin by entering **http://localhost/phpmyadmin/** in your web browser.

The phpMyAdmin login screen will appear first. Select your language, then enter the username (root) and unique password you created for the MySQL user in the previous section.

![phpMyAdmin Login Screen](https://make.wordpress.org/core/files/2013/03/xampp-phpmyadmin-login.png)

The main phpMyAdmin screen will appear. On the left is a list of databases that already exist: **cdcol, information\_schema, mysql, performance\_schema, phpmyadmin, test,** and **webauth**. Do not delete these, as they are necessary for XAMPP and phpMyAdmin to run properly.

To create a database, **click Databases** in the top navbar.

![XAMPP: Navbar On phpMyAdmin Main Screen](https://make.wordpress.org/core/files/2013/06/database-create-phpmyadmin-navbar.png)

On the screen that appears, you need to enter the database name (for example, **root\_wordpress-trunk**) in the left field, choose your database collation from the Collation dropdown box (**utf8\_unicode\_ci**), then **click Create**.

![XAMPP: Create Database In phpMyAdmin Screen](https://make.wordpress.org/core/files/2013/06/database-create-name-collation.png)

You will see a success message once the database has been created.

![XAMPP: Database Creation Success Message Screen](https://make.wordpress.org/core/files/2013/06/database-create-success-message.png)

The default phpMyAdmin user, **root**, is automatically assigned to the database upon creation, and has the unique password you created in the previous step. The database connection info you will need to use when installing WordPress locally is:

```php
/** The name of the database for WordPress */
define('DB_NAME', 'root_databasename');

/** MySQL database username */
define('DB_USER', 'root');

/** MySQL database password */
define('DB_PASSWORD', 'yourmysqlpassword');

/** MySQL hostname */
define('DB_HOST', 'localhost');
```

### 7\. Shutting Down XAMPP

You can shut down XAMPP from the main control panel by **clicking Stop** next to each of the services that are running, then **click Quit**.

![XAMPP Shutdown: Control Panel Screen](https://make.wordpress.org/core/files/2013/03/stopping-xampp-1.png)

**Helpful tip:** You can also shut down XAMPP from the systray icon. **Right-click the XAMPP icon**, and a context menu will appear. Hover over the first service running, then **click Stop**. The green light will turn red once it has stopped. Repeat for the other services running, then **click Quit** to exit the program.

![XAMPP Shutdown: Context Menu Screen](https://make.wordpress.org/core/files/2013/03/stopping-xampp-2.png)

## Next Steps

*   [Installing WordPress From A Zip File](https://make.wordpress.org/core/handbook/tutorials/installing-wordpress-locally/from-zip/)
*   [Installing WordPress Via SVN](https://make.wordpress.org/core/handbook/installing-wordpress-locally/installing-via-svn/)