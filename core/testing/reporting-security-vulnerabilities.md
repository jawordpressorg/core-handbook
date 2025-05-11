# Reporting Security Vulnerabilities

While we try to be proactive in preventing security problems, we do not assume they’ll never come up.

It is standard practice to **responsibly and privately disclose** to the vendor (the WordPress core development team, in this case) a security problem before publicizing, so a fix can be prepared, and damage from the vulnerability minimized.

## What is a “security” issue?

A security issue is a type of bug that can affect the security of WordPress installations.

Specifically, it is a report of a bug that you have found in the WordPress core code, and that you have determined can be used to gain some level of access to a site running WordPress that you should not have.

Your site being “hacked ” is **not** a security issue. The security issue will involve knowing how the attacker got in and hacked the site. If you have details on the attack, then contact us. If not, then the [Support Forums](https://wordpress.org/support/) are the most appropriate place to report such an issue.

You forgetting your password or losing access to your site is **not** a security issue. If you lost access through a bug in the WordPress code, then that might be a security issue.

Generally, security issues are complex problems. If you want to report a security issue, then that’s great! You’re in the right place. However, be sure that what you’re reporting is **actually** a security issue. The experts that you are reporting it to are very busy, and don’t usually respond to non-security issues.

The security reporting system is NOT for support. Don’t send general problems there.

## Enhanced bounty rewards during Beta and Release Candidate phases

To encourage proactive security assessments, the WordPress community offers monetary rewards for reporting new, unreleased security vulnerabilities. Notably, these rewards are doubled during the period between the release of Beta 1 and the final Release Candidate (RC) of a major WordPress version.

For instance, in the [WordPress 6.5 release cycle](https://make.wordpress.org/core/6-5/), this enhanced bounty period spanned from February 13, 2024 (Beta 1) to March 28, 2024 (final RC). *[source](https://make.wordpress.org/security/2024/02/12/welcoming-2024-with-wordpress-6-5-beta-1/)*

## Where do I report security issues?

*   If you are here to report any sort of security issue with [a site hosted on **WordPress.com**](https://en.support.wordpress.com/com-vs-org/), then please [submit a report at the Automattic HackerOne page](https://hackerone.com/automattic). If the issue you’re trying to report is on WordPress.com and is **not** a security issue, then please use their [support forums](https://en.forums.wordpress.com/) instead.
*   If you’re having an issue with your own self-hosted WordPress.org site that is **not** a security issue, then please use the WordPress.org [support forums](https://wordpress.org/support/).
*   For security issues with WordPress plugins, follow the information on [Reporting Plugin Security Issues](https://developer.wordpress.org/plugins/wordpress-org/plugin-security/reporting-plugin-security-issues/).
*   **For security issues with the self-hosted version of WordPress**, submit a report at the [WordPress HackerOne page](https://hackerone.com/wordpress). Include as much detail as you can. Please **always use HackerOne instead of Core Trac**, even if the vulnerability is only in `trunk`, or a beta/RC release, because there are some sites that run those in production.

In all cases, you should **not** share the details with anyone else until after the fix for the bug has been officially released to the public.

## Where do I report copyright infringements, libel, and other legal issues?

[WordPress.org](https://wordpress.org/) does not host sites. [WordPress.org](https://wordpress.org/) provides publishing software that anyone can download and use. The organization, [WordPress.org](https://wordpress.org/), has no control over who uses the software, or how they use it. In other words, [WordPress.org](https://wordpress.org/) does NOT have the power to take down comments, posts, sites, or anything else.

Instead of trying to contact WordPress, perform a [whois lookup](http://whois.domaintools.com/) to track down the operator or host of a particular site, then report the infringement to those organizations.

If you still can’t determine the organization, these following articles by Plagiarism Today may help:

*   [Finding the Host](https://www.plagiarismtoday.com/stopping-internet-plagiarism/3-finding-the-host/)
*   [6 Steps to Find a Host’s DMCA Contact](https://www.plagiarismtoday.com/2009/07/16/6-steps-to-find-a-hosts-dmca-contact/)

## I’ve been hacked. What do I do now?

Things you should do:

*   Change passwords for all users, especially Administrators and Editors.
*   If you upload files to your site via FTP, change your FTP password.
*   Re-install the latest version of WordPress.
*   Make sure all of your plugins and themes are up-to-date.
*   Update your [security keys](https://wordpress.org/support/article/editing-wp-config-php/#security-keys).
*   See [FAQ My Site Was Hacked](https://wordpress.org/support/article/faq-my-site-was-hacked/).

## Why are some users allowed to post unfiltered HTML?

Users with Administrator or Editor [roles](https://codex.wordpress.org/Roles_and_Capabilities#Roles) are allowed to publish unfiltered HTML in post titles, post content, and comments, and upload HTML files to the media library. WordPress is, after all, a publishing tool, and people need to be able to include whatever markup they need to communicate. Users with lesser privileges (Authors and Contributors) are not allowed to post unfiltered content or upload HTML files.

If you are running security tests against WordPress, use a lesser privileged user so that all content is filtered. If you are concerned about an Administrator or Editor putting XSS into content and stealing cookies, note that all cookies are marked for HTTP only delivery, and are divided into privileged cookies used for admin pages, and unprivileged cookies used for public facing pages. Content is never displayed unfiltered within the admin dashboard.

In WordPress Multisite, only Super Admins can publish unfiltered HTML, as all other users (including site Administrators) are considered untrusted.

To disable unfiltered HTML for all users, including administrators, you can add `define( 'DISALLOW_UNFILTERED_HTML', true );` to `wp-config.php`.

## Why are disclosures of usernames or user IDs not a security issue?

The WordPress project doesn’t consider usernames or user ids to be private or secure information. A username is part of your online identity. It is meant to identify, not verify, who you are saying you are. Verification is the job of the password.

This includes, for example, retrieving the list of site users through the [REST API Users endpoint](https://developer.wordpress.org/rest-api/reference/users/), `GET /wp-json/wp/v2/users`. Making this publicly accessible is intentional.

Generally speaking, people do not consider usernames to be secret, often sharing them openly. Additionally, many major online establishments — such as Google and Facebook — have done away with usernames in favor of email addresses, which are shared around constantly and freely. WordPress has also moved this way, allowing users to log in with an email address or username since version 4.5.

Instead of attempting to hide a public identifier, WordPress attempts to encourage users to choose strong passwords instead, through both user interface as well as education.

Note that WordPress is not the only open source project to believe this. [Drupal has similar arguments for the same thing.](https://www.drupal.org/node/1004778)

## Why are there path disclosures when directly loading certain files?

This is a server configuration problem. Never enable `display_errors` on a production site.

## Why did I get this “Password Reset” email?

If you get an email saying “Someone has asked to reset the password for the following site and username”, this means someone visited the password reset page on your site. Anyone can visit this page, since it must be open to all for it to be accessible to those who have lost their password. Your password can be reset only by those who can read your email. If your email account has not been compromised, you can ignore this email.