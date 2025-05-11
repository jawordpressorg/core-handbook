# Installing VVV

## Overview

Varying Vagrant Vagrants is an open source [Vagrant](https://www.vagrantup.com) configuration focused on [WordPress](https://wordpress.org) development. VVV is [MIT Licensed](https://github.com/varying-vagrant-vagrants/vvv/blob/master/LICENSE).

VVV is ideal for developing themes and plugins as well as for [contributing to WordPress core](https://make.wordpress.org/core/).

This article will walk you through the steps to install VVV on your Mac, PC, or Linux computer.

**For the official VVV instructions, [visit the official VVV documentation here](https://varyingvagrantvagrants.org/docs/en-US/installation/).**

## Running a Contributor Day

If you’re running a contributor day for a WordCamp, you should use the contributor day set up script. Setting up a local environment over conference Wifi can cause problems for all, so the script generates a pre-built version.

This pre-built version comes with instructions and a full environment needed for contributor day. These then get copied on to USB drives and handed out at the beginning on contributor day. The entire process can be performed offline using only the contents of the USB drive.

[Click here for information about the VVV contributor day USB drive generator](https://github.com/Varying-Vagrant-Vagrants/CD-USB-Generator)

## Installing VVV

VVV requires recent versions of both [Vagrant](https://www.vagrantup.com/) and [VirtualBox](https://www.virtualbox.org/) (or similar) to be installed.

Vagrant is a “tool for building and distributing development environments”. It works with [virtualization](https://en.wikipedia.org/wiki/X86_virtualization) software such as VirtualBox to provide a virtual machine sandboxed from your local environment.

### 1\. Downloading VirtualBox

Navigate to the [Downloads](https://www.virtualbox.org/wiki/Downloads) page on the VirtualBox site. Just like with Vagrant, there are several different download packages available depending on your operating system. Choose the one that’s right for you.

Depending on your operating system, the installer package will vary in size, so it may take a few minutes to download. Once the download is completed, run the installer.

### 2\. Downloading Vagrant

Navigate to the [Downloads](https://www.vagrantup.com/downloads.html) page on the Vagrant site. There are a variety of download packages available depending on your operating system, whether that is Mac OS X or Windows. If you’re running Linux, packages are available for 32- and 64-bit Debian and CentOS distributions. Choose the one that’s right for you to download

Depending on your operating system, the installer package will vary in size, so it may take a few minutes to download. Once the download is completed, run the installer.

### 3\. Grabbing VVV

The official [official instructions for installing VVV are here](https://varyingvagrantvagrants.org/docs/en-US/installation/).

### 4\. Start up VVV

*   In a command prompt, change to the directory VVV is installed to. You can sometimes drag and drop the folder on to the terminal as a fast way to type the path of the directory. **If you are on Windows this must be a ran with elevated administrator privileges**.
*   Start the VVV environment with `vagrant up --provision`
*   Be patient as the magic happens. This could take a while on the first run as your local machine downloads the required files.
*   Watch as the script ends, as an administrator or `su` ***password may be required*** to properly modify the hosts file on your local machine.
*   Do not use `sudo` with the `vagrant` command.

Once the provisioning script has run its course, visit the VVV dashboard at  [http://vvv.test](http://vvv.test) in your browser. You should see a listing of all the sites VVV created, as well as links to other administration-related tools:

*   [http://one.wordpress.test/](http://one.wordpress.test/) A standard WP install, useful for building plugins, testing things, etc.
*   [http://two.wordpress.test/](http://two.wordpress.test/) A second standard WP install, useful for building plugins, testing things, etc.

### 5\. Enabling Trunk and The Meta Environment

There are also 2 environments that are disabled by default:

*   [http://trunk.wordpress.test/](http://trunk.wordpress.test/) An svn-based WordPress Core trunk dev setup, useful for contributor days, Trac tickets, patches, general core contributing, etc.
*   [http://wpmeta.test](http://wpmeta.test) A collection of sites for contributing to WordPress.org and WordCamps

To enable these, open `vvv-custom.yml`, find `skip_provisioning: true` for the desired site, and change `true` to `false`. Save the file and reprovision to apply changes using `vagrant reload --provision`. This will take some time to run.

You can also setup additional sites, [to learn how to do that click here](https://varyingvagrantvagrants.org/docs/en-US/adding-a-new-site/).

### 6\. Create a GitHub Repo (optional)

Pull requests on GitHub provide a convenient way to receive feedback and also to share the patch for your contributions. You can add “`.diff`” to any pull request URL and GitHub will return a diff file which you can then attach to a Trac ticket. You can also just add a link to the pull request in a Trac ticket comment. There is currently no Git repo clone for `develop.git.wordpress.org` located on GitHub, so you have to set this up yourself:

1.  Have VVV set up (above).
2.  Swap out your SVN repo with a Git one in VVV via: `vagrant ssh -c /srv/www/wordpress-trunk/bin/develop_git`
3.  [Create](https://github.com/new) an empty “wordpress-develop” on GitHub (you can name this however you like).
4.  Run these commands to set this new repo as your origin remote: `cd ...vvv/www/wordpress-trunk/public_html && git remote set-url origin https://github.com/YOURNAME/wordpress-develop.git && git remote add upstream git://develop.git.wordpress.org/`
5.  Check out the master branch: `git checkout master`
6.  Create a feature branch based on the Trac ticket (e.g. 12345) you want to work on: `git checkout -b trac-12345`
7.  Add commits for your fixes and `git push` (see also [Caching your GitHub password in Git](https://help.github.com/articles/caching-your-github-password-in-git/) to prevent having to re-enter your GitHub password each time).
8.  Go to GitHub and open a pull request to your `master` branch.
9.  With the newly-created pull request in hand, copy the URL and paste it into a new comment on WordPress Trac and solicit for feedback. Ideally you should also attach a diff of your patch, and again you can do this just by adding “`.diff`” to any pull request URL, for example: [https://github.com/xwp/wordpress-develop/pull/61.diff](https://github.com/xwp/wordpress-develop/pull/61.diff)