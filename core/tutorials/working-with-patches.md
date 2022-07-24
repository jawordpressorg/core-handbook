# Working with Patches

This section of the handbook contains tutorials that will help you learn how to create, apply, and revert patches.

Patches are the only way that a contributor, like you, can submit code to the WordPress project.

Whether you are fixing a bug or contributing to a new feature, a patch is required so the core developers and committers can consider your code for inclusion in the repository.

For beta testing the latest development version of WordPress, you will need to be able to apply patches that other contributors have created to determine if the patch fixes the issue.

## SVN Client or Command Line Interface?

Many developers prefer to work with Subversion (SVN) using the [command line interface](https://make.wordpress.org/core/glossary/#command-line-interface) (CLI), while others prefer to use a [GUI](http://en.wikipedia.org/wiki/GUI) application. Both are acceptable, and will allow you to create, apply, and revert patches.

For command line users, there are programs such as [Cygwin](http://cygwin.com/) (Windows), [Terminal](http://en.wikipedia.org/wiki/Terminal_(OS_X)) (Mac), and [Bash](http://www.gnu.org/software/bash/) (Mac).

If you prefer to use a GUI application, the recommended SVN clients are [TortoiseSVN](http://tortoisesvn.net/) (Windows, free/open-source), and [Cornerstone](http://www.zennaware.com/cornerstone/) (Mac, purchase).

## Creating and Applying Patches with Grunt

If you like to automatically submit the created patch to an existing ticket, there is an easy-to-use [Grunt](https://gruntjs.com/getting-started) command available that can take care of both creating the patch and uploading it. In order to use the command, you need to have [Node.js](https://nodejs.org/) and [Grunt-CLI](https://gruntjs.com/getting-started#installing-the-cli) globally installed, and you need to ensure that the WordPress development dependencies are installed locally, which you can do by running `npm install`.

### Apply a patch from the command line

1.  Have a diff or a patch file in your working Directory, then run `grunt patch`. If multiple files are found, you’ll be asked which one to apply.
2.  Enter a ticket number, e.g.

> `grunt patch:15705`

3.  Enter a ticket url, e.g.

> `grunt patch:https://core.trac.wordpress.org/ticket/15705`

4.  Enter a patch url, e.g.

> `grunt patch:https://core.trac.wordpress.org/attachment/ticket/11817/13711.diff`

5.  Enter a github url that points to a changeset such as a Pull Request, e.g.

> `grunt patch:https://github.com/muhammadfaizanhaidar/develop.wordpress/pull/23`

### Upload a patch from the command line

After you’ve made changes to your local WordPress develop repository, you can upload a patch file directly to a Trac ticket. e.g. given the ticket number is 2907,

```
grunt upload_patch:2907
```

You can also store your WordPress.org credentials in environment variables. Please exercise caution when using this option, as it may cause your credentials to be leaked!

```
export WPORG_USERNAME=matt
export WPORG_PASSWORD=MyPasswordIsVerySecure12345
grunt uploadPatch:40000
```

## Creating and Applying Patches with TortoiseSVN

Before starting, you need:

*   [TortoiseSVN installed on your computer](https://make.wordpress.org/core/handbook/tutorials/installing-a-vcs/)
*   A plain text editor, such as [Notepad++](http://notepad-plus-plus.org/), installed on your computer

### Creating a Patch with TortoiseSVN

#### 1\. Editing/Saving a File

Open the folder, and find the file you need to change. Open it in your favorite plain-text editor. **Note:** Do not use a rich-text editor such as Word or OpenOffice to edit the files.

Make the changes necessary, then save the file.

You will notice that the green checkmark has changed to a red exclamation point. That means the file has been changed, and is no longer in sync with the repo version.

![TortoiseSVN Changed File Indicator](https://make.wordpress.org/core/files/2013/02/tortoisesvn-changed-file.png)

#### 2\. Creating/Naming a Patch

Next you will create the patch file. Right-click in the root directory of your SVN checkout folder, and select **SVN Create Patch**.

It is important to create patches from the root directory (the folder containing all of the WordPress files). To do that, either right-click on white space in the folder or move one level up from that folder and right-click on it.

![TortoiseSVN Create Patch Context Menu](https://make.wordpress.org/core/files/2013/02/tortoisesvn-create-patch-1.png)

A pop-up window will show you the list of changed files. Make sure the file(s) you want to include in the patch are checked, then **click OK**.

![Check the box for all file(s) that should be included in the patch](https://make.wordpress.org/core/files/2013/02/tortoisesvn-create-patch-2.png)

You will be prompted to save the file. Create a folder called **patches**, then type in the filename you want to save it as. Use the format **ticket#.diff**.

The TortoiseUDiff editor will open and show you the patch file you just created.

![TortoiseUDiff Editor](https://make.wordpress.org/core/files/2013/02/tortoisesvn-22121-patch.png)

### Applying a Patch with TortoiseSVN

Got a patch you want to test with your local environment? Follow these steps to test your patch.

#### 1\. Downloading a Patch

Part of the troubleshooting/testing process involves downloading and applying patches to your local WordPress trunk install from a Trac ticket that you are involved in.

To download a patch, **click on the Download icon** next to the patch filename in the **Attachments** section of the ticket (just below the **Description** section), and save it to a folder called **patches**.

![Download A Patch From Trac Ticket Screen](https://make.wordpress.org/core/files/2013/04/tortoisesvn-apply-patch-download-file.png)

#### 2\. Applying a Patch with TortoiseSVN

To apply the patch you just downloaded, **right-click in the folder** for your working copy of WordPress, which will bring up a context menu. Click on **SVN Apply Patch**.

![TortoiseSVN Apply Patch Context Menu Screen](https://make.wordpress.org/core/files/2013/03/tortoisesvn-apply-patch-context-menu.png)

This will bring up a file open dialog window, allowing you to select the patch file to apply. By default, only **.patch** or **.diff** files are shown, but you can change the file type to **All files** if you don’t see the patch file you are looking for.

![TortoiseSVN Select Local File Screen](https://make.wordpress.org/core/files/2013/03/tortoisesvn-apply-patch-select-local-file.png)

Applying a patch file to your working copy of WordPress should be done at the same folder level as was used to create the patch. If you are in the correct working copy, but picked the wrong folder level, TortoiseSVN will display a notice, suggesting the correct level, and allows you to select that.

![TortoiseSVN Wrong Directory Screen](https://make.wordpress.org/core/files/2013/03/tortoisesvn-apply-patch-wrong-directory.png)

Once you have selected the patch file and correct working copy location, TortoiseMerge will run to merge the changes from the patch file with your working copy. A small window lists the files which have been changed. **Double-click each filename**, review the changes, and save the patched file to your working copy.

![TortoiseSVN File Patched Screen](https://make.wordpress.org/core/files/2013/03/tortoisesvn-apply-patch-files-patched.png)

## Creating and Applying Patches with the Command Line

This article will walk you through creating, applying, and reverting a patch using the command line. Before starting, you’ll need the following:

*   A plain text editor, such as [Notepad++](http://notepad-plus-plus.org/) (Windows) or [TextMate](http://macromates.com/) (Mac), installed on your computer
*   A copy of WordPress trunk, [checked out via SVN](https://make.wordpress.org/core/handbook/tutorials/installing-wordpress-locally/from-svn/)
*   A command line client installed on your computer:
    *   Windows: [Cygwin](http://cygwin.com/)
    *   MAC: [Terminal](http://en.wikipedia.org/wiki/Terminal_(OS_X)) or [Bash](http://www.gnu.org/software/bash/)

### Creating a Patch with the Command Line

During beta testing, you may run across a bug that you are able to fix. Before you submit the Trac ticket, however, you should create a patch with the proposed fix so you can attach it to the ticket.

Open the folder where you have WordPress installed via SVN, and find the file you need to change. Open the file in your favorite plain-text editor. Make the changes necessary to fix the bug, then save the file. Do not create patches for minified JS files or RTL CSS files. These are generated automatically from source files. Read more about [this build process](https://make.wordpress.org/core/2013/08/06/a-new-frontier-for-core-development/).

Next you will create the patch file, which records the differences between your version of the files and those from WordPress trunk. Patches should be created from the root directory of your WordPress SVN install.

To do so, ensure that you are in the root directory created by your SVN checkout (**wordpress-svn**), then run the following command, where `00000` is replaced with the ticket number from Trac:

```bash
svn diff > 00000.diff
```

If you also like to automatically submit the created patch to an existing ticket, there is an easy-to-use [Grunt](https://make.wordpress.org/core/handbook/tutorials/working-with-patches/#creating-and-applying-patches-with-grunt) command available that can take care of both creating the patch and uploading it. In order to use the command, you need to have [Node.js](https://nodejs.org/) and Grunt-CLI globally installed, and you need to ensure that the WordPress development dependencies are installed locally, which you can do by running `npm install`.

The actual command to create and upload a patch works as follows:

```bash
grunt upload_patch:00000
```

Make sure to replace `00000` with the ticket number from Trac. During execution of the command, you may be asked for your wordpress.org user name and password.

### Applying a Patch with the Command Line

Part of the troubleshooting/testing process involves downloading and applying patches to your local WordPress trunk install from a Trac ticket that you are involved in.

To download a patch, click on the handy download icon next to the patch’s name in trac:

[![Download a Patch from Trac Ticket Screen](https://make.wordpress.org/core/files/2013/07/smpxJogJyp-300x102.png)](https://make.wordpress.org/core/files/2013/07/smpxJogJyp.png)

On a Mac, this will save it to your default downloads folder, from where you can move it to your chosen **wordpress-svn** directory. On a Windows machine, this will prompt you to save it in your chosen location, which should be the aforementioned directory.

You can also download a patch via command line. Make sure that you are in the **wordpress-svn** directory, then download the patch into the **patches** folder.

```bash
curl -O https://core.trac.wordpress.org/raw-attachment/ticket/00000/00000.diff
```

Note: If you download the patch this way, make sure that it is coming from the **raw-attachment** directory on the Trac server. You can get this URL by clicking on the patch in Trac, then grabbing the URL linked to by **Original Format** at the bottom of the page.

You will need to apply the patch from the **wordpress-svn** directory, where you have downloaded the patch file. Use the following command to apply the patch:

```
patch -p 0 < 00000.diff
```

Now, the **wordpress-svn** code has been patched with the file you downloaded, giving you the version of the code that the developer who submitted that patch was working with.

Note: If the patch fails to apply cleanly, you will need to leave a note on the Trac ticket that the patch needs to be refreshed, and add the **needs-refresh** keyword to the ticket.

To make this process a little easier for you, there is another [Grunt](https://make.wordpress.org/core/handbook/tutorials/working-with-patches/#creating-and-applying-patches-with-grunt) command available that takes care of both downloading a patch from an existing ticket and applying it. As mentioned before, in order to use it, you need to have both [Node.js](https://nodejs.org/) and Grunt-CLI globally installed, and you also need to have the local dependencies set up, which you can do by using the command `npm install`.

You can then use the following command:

```bash
grunt patch:00000
```

Make sure to replace `00000` with the ticket number from Trac. The command will automatically download the patch file from the ticket if there is only a single patch available. Otherwise, you can select which patch to download from a list, using the arrow keys on your keyboard.

### Reverting a Patch with the Command Line

When you have finished testing, it is best to revert your SVN install back to the latest version of trunk, removing all applied patches and any changes you have made. You will use the following command to revert all patches/changes:

```bash
svn revert -R *
```

## Download a GitHub pull request

With [hub](https://hub.github.com/) is very easy to download a pull request from a WordPress fork on a Git repo (like on GitHub). For the purpose of this section you need to install this tool on your system.

Now you have a super version of Git that include the Hub version so inside the \``public_html` on VVV or your WP trunk folder you can execute this command (as example):

`git checkout https://github.com/WordPress/wordpress-develop/pull/195`

This command will create automatically for you a new branch with the content of this pull request, with the ability to update that branch with the code over there.

Otherwise you can download the patch or diff version of a pull request appending to the pull request url `.patch` or `.diff` like:

*   [https://patch-diff.githubusercontent.com/raw/WordPress/wordpress-develop/pull/195.diff](https://patch-diff.githubusercontent.com/raw/WordPress/wordpress-develop/pull/195.diff)
*   [https://patch-diff.githubusercontent.com/raw/WordPress/wordpress-develop/pull/195.patch](https://patch-diff.githubusercontent.com/raw/WordPress/wordpress-develop/pull/195.patch)

## Next Steps

*   [Submitting a Patch](https://make.wordpress.org/core/handbook/tutorials/trac/submitting-a-patch/)