# Installing WampServer

## Overview

[WampServer](http://www.wampserver.com/en/) is a local server package for Windows, allowing you to install and host web applications that use Apache, PHP and MySQL.

This article will walk you through the steps to install WampServer on your computer.

## Installing WampServer

### 1\. Downloading WampServer

Download the installer file for the [latest version of WampServer](http://www.wampserver.com/en/#download-wrapper), and save the file to your computer.

![Download WampServer Screen](https://make.wordpress.org/core/files/2013/06/download-wampserver.png)

Make sure you select the correct installer file for your version of Windows. If you don’t know if your system is 32-bit or 64-bit, **right-click on My Computer**, and then **click Properties**.

![Windows 7 System Type Settings](https://make.wordpress.org/core/files/2013/06/windows7-system-type-64x.png)

*   For Vista, Windows 7, and Windows 8, look for **System Type**.
*   For Windows XP, look for **x64** in the **System description**.

### 2\. Installing WampServer

To start the installation process, you need to open the folder where you saved the file, and **double-click the installer file**. A security warning window will open, asking if you are sure you want to run this file. **Click Run** to start the installation process.

Next you will see the Welcome To The WampServer Setup Wizard screen. **Click Next** to continue the installation.

![Welcome To The WampServer Setup Wizard Screen](https://make.wordpress.org/core/files/2013/06/installing-wamp-2.png)

The next screen you are presented with is the License Agreement. Read the agreement, check the radio button next to **I accept the agreement**, then **click Next** to continue the installation.

![Installing WampServer: License Agreement Screen](https://make.wordpress.org/core/files/2013/06/installing-wamp-3.png)

Next you will see the Select Destination Location screen. Unless you would like to install WampServer on another drive, you should not need to change anything. **Click Next** to continue.

![Installing WampServer: Choose Install Location Screen](https://make.wordpress.org/core/files/2013/06/installing-wamp-4.png)

The next screen you are presented with is the Select Additional Tasks screen. You will be able to select whether you would like a Quick Launch icon added to the taskbar or a Desktop icon created once installation is complete. Make your selections, then **click Next** to continue.

![Installing WampServer: Select Additional Tasks Screen](https://make.wordpress.org/core/files/2013/06/installing-wamp-5.png)

Next you will see the Ready To Install screen. You can review your setup choices, and change any of them by **clicking Back** to the appropriate screen, if you choose to. Once you have reviewed your choices, **click Install** to continue.

![Installing WampServer: Ready To Install Screen](https://make.wordpress.org/core/files/2013/06/installing-wamp-6.png)

WampServer will begin extracting files to the location you selected.

![Installing WampServer: Unpacking Files Screen](https://make.wordpress.org/core/files/2013/06/installing-wamp-7.png)

Once the files are extracted, you will be asked to select your default browser. WampServer defaults to Internet Explorer upon opening the local file browser window. If your default browser isn’t IE, then look in the following locations for the corresponding .exe file:

*   **Opera:** C:\\Program Files (x86)\\Opera\\opera.exe
*   **Firefox:** C:\\Program Files (x86)\\Mozille Firefox\\firefox.exe
*   **Safari:** C:\\Program Files (x86)\\Safari\\safari.exe
*   **Chrome:** C:\\Users\\xxxxx\\AppData\\Local\\Google\\Chrome\\Application\\chrome.exe

Select your default browser’s .exe file, then **click Open** to continue.

![Installing WampServer: Choose Default Browser Screen](https://make.wordpress.org/core/files/2013/06/installing-wamp-8.png)

A Windows Security Alert window will open, saying that Windows Firewall has blocked some features of the program. Check whether you want to allow Apache HTTP Server to communicate on a private or public network, then **click Allow Access**.

The Setup screen will appear next, showing you the status of the installation process.

![Installing WampServer: Finishing Installation Screen](https://make.wordpress.org/core/files/2013/06/installing-wamp-10.png)

Once the progress bar is completely green, the PHP Mail Parameters screen will appear. Leave the SMTP server as **localhost**, and change the email address to one of your choosing. **Click Next** to continue.

![Installing WampServer: PHP Mail Parameters Screen](https://make.wordpress.org/core/files/2013/06/installing-wamp-11.png)

The Installation Complete screen will now appear. **Check the Launch WampServer Now** box, then **click Finish** to complete the installation.

![Installing WampServer: Completing The WampServer Setup Wizard Screen](https://make.wordpress.org/core/files/2013/06/installing-wamp-12.png)

You should see the WampServer icon appear in the systray on the right side of your taskbar. If the icon is green, then everything is working properly. If the icon is orange, then there are issues with one of the services. If the icon is red, then both Apache and MySQL services aren’t running. You will need to resolve those issues before continuing.

![WampServer: Server Status Screen](https://make.wordpress.org/core/files/2013/06/wampserver-server-status.png)

### 3\. Testing WampServer

Once you have completed the installation process, test that your installation is working properly by going to [http://localhost/](http://localhost/) in your browser. You should see the WampServer homepage displayed.

![WampServer Homepage Screen](https://make.wordpress.org/core/files/2013/06/wampserver-homepage.png)

If the WampServer homepage does not display, you will want to check that your [hosts file](http://en.wikipedia.org/wiki/Hosts_(file)) has **localhost mapped to 127.0.0.1**, and you aren’t running any other services on port 80, such as another local server (XAMPP, DesktopServer, etc.), WebDAV, or Skype.

You also need to check that phpMyAdmin is working by going to [http://localhost/phpmyadmin/](http://localhost/phpmyadmin/) in your browser. If you get the **Cannot connect: invalid settings** error message, then you’ll need to edit the **C:\\wamp\\apps\\phpmyadmin3.5.1\\config.inc.php** file in a plain text editor (your version number may be different), and ensure this option is set to **true**:

$cfg\['Servers'\]\[$i\]\['AllowNoPassword'\] = true;

### 4\. Configuring WampServer

After you’ve installed and tested WampServer, you will need to adjust some configuration options to complete your local setup.

#### 4.1 PHP Configuration

Click on the WampServer icon, go to the **php menu**, and **click on the php.ini** option. This will open the **php.ini** file in your plain text editor. Adjust the following settings:

*   Set level of error reporting – remove the `;` at beginning of line to enable:  
    `error_reporting = E_ALL ^ E_DEPRECATED` (~line 112)
*   Log PHP errors – remove the `;` at beginning of line to enable:  
    `error_log = "c:/wamp/logs/php_error.log"` (~line 639)
*   Increase maximum size of POST data that PHP will accept – change the value:  
    `post_max_size = 50M` (~line 734)
*   Increase maximum allowed size for uploaded files – change the value:  
    `upload_max_filesize = 50M` (~line 886)

Once you have made the above changes, **click Save**.

#### 4.2 Apache Configuration

To use custom permalinks in WordPress, you will need to enable Apache’s `rewrite_module`. **Click on the WampServer icon**, go to the **Apache > Apache modules** menu, then find and **click rewrite\_module** to ensure it is enabled. WampServer will change the **httpd.conf** file, and restart Apache automatically.

![Enable rewrite_module Apache Module Screen](https://make.wordpress.org/core/files/2013/06/wampserver-enable-rewrite-module.png)

### 5\. Creating A MySQL Database With WampServer

Creating a database in WampServer is done via phpMyAdmin. You can access phpMyAdmin by entering [http://localhost/phpmyadmin/](http://localhost/phpmyadmin/) in your web browser.

The main phpMyAdmin screen will appear. On the left is a list of databases that already exist: **information\_schema**, **mysql**, **performance\_schema**, and **test**. Do not delete these, as they are necessary for WampServer and phpMyAdmin to run properly.

To create a database, **click Databases** in the main navbar at the top.

![WampServer Navbar On phpMyAdmin Main Screen](https://make.wordpress.org/core/files/2013/06/database-create-phpmyadmin-navbar.png)

On the Databases screen, you will need to enter the database name (for example, **root\_wordpress-trunk**) in the left field, choose your database collation from the Collation dropdown box (**utf8\_unicode\_ci**), then **click Create**.

![WampServer Create Database In phpMyAdmin Screen](https://make.wordpress.org/core/files/2013/06/database-create-name-collation.png)

You will see a success message once the database has been created, and your new database will appear in the list on the left.

![WampServer Database Creation Success Message Screen](https://make.wordpress.org/core/files/2013/06/database-create-success-message.png)

The default phpMyAdmin user, **root**, is automatically assigned to the database upon creation, and has no password. The database connection info you will need to use when installing WordPress locally will be:

/\*\* The name of the database for WordPress \*/
define('DB\_NAME', 'root\_databasename');

/\*\* MySQL database username \*/
define('DB\_USER', 'root');

/\*\* MySQL database password \*/
define('DB\_PASSWORD', '');

/\*\* MySQL hostname \*/
define('DB\_HOST', 'localhost');

### 6\. Shutting Down WampServer

To shut down WampServer, **click on the systray icon** and **select Stop All Services** to shut down the Apache and MySQL services. The icon will turn red once all services have been shut down.

![WampServer: Stop All Services Screen](https://make.wordpress.org/core/files/2013/06/shutdown-wamp-1.png)

Next you will **right-click on the WampServer systray icon** and **click Exit** to close the program.

![WampServer: Exit Program Screen](https://make.wordpress.org/core/files/2013/06/shutdown-wamp-2.png)

## Next Steps

*   [Installing WordPress From A Zip File](https://make.wordpress.org/core/handbook/tutorials/installing-wordpress-locally/from-zip/)
*   [Installing WordPress Via SVN](https://make.wordpress.org/core/handbook/tutorials/installing-wordpress-locally/from-svn/)