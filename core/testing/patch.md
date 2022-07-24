# Testing a Patch

Alert: This page is under construction and may contain inaccurate information. Want to help fix it? Ping the [#docs](https://make.wordpress.org/core/tag/docs/) channel in WordPress Slack.

Testing patches is an important part of ensuring the quality of WordPress releases.

## Setting up without VVV

If you use VVV, skip to the section below.

Grunt is a command runner that allows you to test patches that have been uploaded to Trac. To use Grunt, follow these steps:

1.  Install `nodejs` and `npm` to your development environment.
2.  Clone the *develop* WordPress repository located at https://develop.svn.wordpress.org/
3.  Run `npm install` to get all the dependencies.
4.  Run `npm run grunt build` to get the fully-built version
5.  Setup your server to use `/build` as the root (varies depending on how your development environment is setup).
6.  In order for changes to `/src` to be reflected in `/build`, run `npm run grunt watch` while you are working.
7.  **Alternatively**, you can [use /src as your document root](https://make.wordpress.org/core/2018/12/24/build-tools-weve-enabled-running-wordpress-from-src-again/), which may be much more convenient for PHP\-focused development. You’ll need to run `npm run grunt build -- --dev` once, but after that you don’t need `npm run grunt watch` at all, unless you’re changing JavaScript/CSS. If you are, then use `npm run grunt watch -- --dev` instead of `npm run grunt watch`.

## Setting up with VVV

VVV includes support for [WP Core Development](https://github.com/Varying-Vagrant-Vagrants/custom-site-template-develop/), and you can find the settings on the [config.yml](https://github.com/Varying-Vagrant-Vagrants/VVV/blob/develop/config/default-config.yml) file.

If you use VVV, a site can be added that contains a full [WP Core development build](https://github.com/Varying-Vagrant-Vagrants/custom-site-template-develop/). If you open `config/config.yml` there is a site pre-pepared for this, but disabled out of the box. Look for `wordpress-trunk` and change `skip_provisioning` from `true` to `false`, it should look like this:

```yaml
  wordpress-trunk:
    skip_provisioning: true
    description: "An git based WP Core trunk dev setup, useful for contributor days, Trac tickets, patches"
    repo: https://github.com/Varying-Vagrant-Vagrants/custom-site-template-develop.git
    hosts:
      - trunk.wordpress.test
    custom:
      vcs: git # using 'svn' will force this vcs
```

Once saved, reprovision with `vagrant up --provision`. VVV will download and prepare a developer environment for working on core and testing. This new site will be located in the `www/wordpress-trunk/public_html` folder.

Inside the site there will be 2 folders, `src` and `build`. Changes made in the `src` folder are processed by a tool called `grunt` and put in the `build` folder. This happens automatically by running the command `npm run grunt watch` in the `www/wordpress-trunk/public_html` folder. For example:

```bash
vagrant ssh
cd /srv/www/wordpress-trunk/public_html
npm run grunt watch
```

## Testing with Grunt

Now that [Grunt](https://make.wordpress.org/core/handbook/tutorials/working-with-patches/#creating-and-applying-patches-with-grunt) is setup, type in `npm run grunt patch:####`, replacing `####` with either a ticket number from Trac or a patch URL. This will download the patch and apply the changes to your development environment.

Note: If you receive a `Cannot find module 'grunt-cli/bin/grunt'` error, run the following and then try again:

`rm -rf node_modules && npm install`

Ready to test your environment? Use `npm run grunt test` to automatically run automated tests. Note that this step requires PHPUnit to be installed.

If you’re a committer, be sure to run `npm run grunt precommit` before committing code, *especially* code that touches anything on the front-end (CSS/JS).

## Testing without Grunt

See [https://make.wordpress.org/core/handbook/tutorials/working-with-patches/#applying-a-patch-with-the-command-line](https://make.wordpress.org/core/handbook/tutorials/working-with-patches/#applying-a-patch-with-the-command-line)