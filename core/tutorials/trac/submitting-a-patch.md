# Submitting a Patch

## Overview

Once you’ve edited the file and tested it, you need to create a patch and upload it to the corresponding Trac ticket so other people can see and test the changes. You can create a *patch* a number of ways.

When using an IDE or a Subversion client a patch can be created directly by the application. The patch should be created from the root directory (the folder that contains the `/src` directory, the `wp-config-sample.php` file, etc.).

### Windows

**If you are on Windows,** consider using [Tortoise SVN](http://tortoisesvn.net/). You can [read our tutorial on creating a patch with Tortoise SVN.](https://make.wordpress.org/core/handbook/tutorials/working-with-patches/#creating-a-patch-with-tortoisesvn).

### Mac/Linux Command Line

From [Mark Jaquith’s Tutorial](http://markjaquith.wordpress.com/2005/11/02/my-wordpress-toolbox/)

Make a patch, for filename.php:

`$ svn diff filename.php > filename.diff`

Make a patch for all files modified in the checkout:

`$ svn diff > big_patch.diff`

Apply a patch from someone else:

`$ patch -p0 < patch.diff`

There are some GUI options for the Mac, as well — you just need it to create patch files (Versions cannot, for example).

Also: [creating SVN patches using Git](http://scribu.net/wordpress/svn-patches-from-git.html), from Cristi Burca.

## Adding your GitHub fork to your WP trunk copy

First of all you need your own WordPress fork somewhere, usually on GitHub (also because there is the [mirror](http://github.com/wordpress/wordpress-develop)). After creating a fork, a branch (is important to not work on the master/trunk branch to avoid conflicts) you need to add this new remote to your git instance.

`git remote add fork git@github.com:WordPress/wordpress-develop.git`

Change in this command with the repo url or the git url as you prefer

Now it is time to a command to align your local git instance `git fetch --all`

Now you are able to switch to a master from your fork with this command as example `git checkout fork/44722` or create a new branch like `git checkout -b 44722`, this command require to switch to the fork instead of the official version and you can achieve it with `git checkout fork master`.

Now you can use as usual git and create all the code changes that you need, commit and so on. If you open now the [GitHub mirror](https://github.com/wordpress/wordpress-develop) (and you associated your WP profile to GitHub) you get a on the GH page a button to create a new pull request because it detected this change.

The next step is to add a name to the pull request that need to include the ticket number as explained [here](https://make.wordpress.org/core/handbook/contribute/git/github-pull-requests-for-code-review/). For other information about GitHub integration check this documentation page.