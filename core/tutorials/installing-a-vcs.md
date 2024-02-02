# Installing a Version Control System

When using an IDE (Integrated Developer Environment) application or a stand-alone GUI client application, chances are that a separate installation of Subversion or Git will not be needed. Most of these applications include a local copy of the version control system.

## Installing Subversion on a Mac

Prior to OS 10.8 (Mountain Lion), Macs came with Subversion pre-installed. Subversion has since been moved to the [Xcode developer package](https://developer.apple.com/xcode/).

This article will walk you through the steps to install Subversion on your Mac.

### 1\. Download The Package

You can install [Xcode](https://developer.apple.com/xcode/) to set up Subversion on your Mac; however, the download package is around 1.5 GB.

Instead, you can download Apple’s Command Line Tools from Apple’s Mac Developer website. You will need an Apple ID to download the files.

Log in to [Apple’s Developer tools](https://developer.apple.com/downloads/index.action). Search for Command Line Tools, and download the correct package for your operating system.

### 2\. Install

Install the package.

### 3\. Verify the installation

You can verify the installation by typing:

```bash
$  svn --version
```

You should see something like this:

```bash
svn, version 1.7.10 (r1485443)
   compiled Aug 13 2013, 15:31:22

Copyright (C) 2013 The Apache Software Foundation.
This software consists of contributions made by many people; see the NOTICE
file for more information.
Subversion is open source software, see http://subversion.apache.org/

The following repository access (RA) modules are available:

* ra_neon : Module for accessing a repository via WebDAV protocol using Neon.
  - handles 'http' scheme
  - handles 'https' scheme
* ra_svn : Module for accessing a repository using the svn network protocol.
  - handles 'svn' scheme
* ra_local : Module for accessing a repository on local disk.
  - handles 'file' scheme
* ra_serf : Module for accessing a repository via WebDAV protocol using serf.
  - handles 'http' scheme
  - handles 'https' scheme
```

Subversion is now installed and ready to use.

## Installing TortoiseSVN

[TortoiseSVN](http://tortoisesvn.net/) is an Apache Subversion (SVN) client, implemented as a Windows shell extension. It’s intuitive and easy to use, and doesn’t require the Subversion command line client to run.

This section will walk you through the steps to install TortoiseSVN on your computer.

### 1\. Downloading TortoiseSVN

Download the [latest version of TortoiseSVN](http://tortoisesvn.net/downloads.html), and save the installer file to your computer.

![Download TortoiseSVN](https://make.wordpress.org/core/files/2013/02/tortoisesvn-download.png)

### 2\. Installing TortoiseSVN

Next, you need to open the folder where you saved the file, and double-click the installer file. A security warning window will open, asking if you want to run this file. **Click Run** to start the installation process.

![TortoiseSVN Open File Warning Screen](https://make.wordpress.org/core/files/2013/02/tortoisesvn-installing-run-file1.png)

You will now see the welcome screen, which will confirm the version of TortoiseSVN that you are going to install. **Click Next** to continue.

![TortoiseSVN Installation Welcome Screen](https://make.wordpress.org/core/files/2013/02/tortoisesvn-installing-1.png)

The next screen you are presented with is the End-User License Agreement (EULA). Read the agreement, check the radio button next to **I accept the terms in the License Agreement**, then **click Next** to continue the installation.

![TortoiseSVN End-User License Agreement Screen](https://make.wordpress.org/core/files/2013/02/tortoisesvn-installing-21.png)

The Custom Setup screen will appear next. This screen will allow you to choose which components you would like to install. Unless you are dangerously low on disk space, you shouldn’t need to change anything. **Click Next** to continue.

![TortoiseSVN Custom Setup Screen](https://make.wordpress.org/core/files/2013/02/tortoisesvn-installing-3.png)

Once the Confirm Installation screen appears, you are ready to start the installation process. **Click Install** to begin the process.

![TortoiseSVN Confirm Installation Screen](https://make.wordpress.org/core/files/2013/02/tortoisesvn-installing-4.png)

The Installation Status screen will appear, which shows you the status of the installation process. Once the progress bar is completely green, **click Next**.

![TortoiseSVN Installation Status Screen](https://make.wordpress.org/core/files/2013/02/tortoisesvn-installing-5.png)

The Installation Complete screen will now appear. Congratulations, you have now installed TortoiseSVN. **Click Finish** to complete the installation.

![TortoiseSVN Installation Complete Screen](https://make.wordpress.org/core/files/2013/02/tortoisesvn-installing-7.png)

### 3\. Configuring TortoiseSVN

TortoiseSVN adds a few items to your context menu during installation, including a way to access the settings panel. To review and change any of the default settings, right-click inside any folder, go to **TortoiseSVN**, then select **Settings** in the submenu.

![TortoiseSVN Settings Menu Screen](https://make.wordpress.org/core/files/2013/02/tortoisesvn-settings-context-menu.png)

The first screen you see is for the **General Settings**. You can change your language, configure system sounds, and check for updates.

![TortoiseSVN General Settings Screen](https://make.wordpress.org/core/files/2013/02/tortoisesvn-settings-1.png)

Select **Context Menu** under **General** in the settings tree on the left side of the window. You can now choose which items will appear on the first-level context menu. The items you will be using often when contributing patches to WordPress will be **Checkout**, **Update**, **Show log**, **Repo-browser**, **Create Patch**, and **Apply Patch**.

![TortoiseSVN Context Menu Settings Screen](https://make.wordpress.org/core/files/2013/02/tortoisesvn-settings-2.png)

More information about the settings can be found in the [Settings section of the TortoiseSVN documention](http://tortoisesvn.net/docs/release/TortoiseSVN_en/tsvn-dug-settings.html).

## Next Steps

*   [Install WordPress locally with Subversion](https://make.wordpress.org/core/handbook/tutorials/installing-wordpress-locally/from-svn/)
*   [Working with Patches](https://make.wordpress.org/core/handbook/tutorials/working-with-patches/)