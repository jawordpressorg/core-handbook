# Design Decisions

This page lists a number of important design decisions that come up frequently, and attempts to explain and cross-reference the reasoning behind them.

## Absolute versus relative URLs

WordPress stores absolute URLs in the database. Relative URLs are not used for a variety of reasons. Dynamically generated websites need permanent URLs (permalinks), so absolute URIs make more sense. WordPress has a [variety of functions](https://codex.wordpress.org/Function_Reference/site_url#Related) to call a site domain and various folders in plugins and themes so that relative URLs are not necessary. When moving domains, there are search and replace tools for switching domains in the database.

### Why relative URLs are not good

Content is migratory. That is to say that the content, which is in the database, might not always be displayed within the context of “your site”. Content can be displayed in a variety of places. For example, an RSS feed of your content can be pulled into Google Reader and displayed there. Or users can use feed readers of their own. Or the content can be pulled from your site using microformats and displayed somewhere else. A user will never know where the content is going to be. Therefore an absolute URL is necessary within that content to ensure that it always points to a specific point, regardless of where it’s displayed.

Permalinks are malleable. The content of a post can be displayed on `http://example.com/`, on `http://example.com/archive/`, `http://example.com/2012/01/single-post`, and so on. A relative URL would not be valid unless it is “root-relative”, meaning that it started with a / character, to refer to the root of the site. Even then, if a site is moved from one subdirectory to another, the root-relative URL would still need to change, and changing the content in the database to adjust would be necessary.

Moving is easier with absolute URLs. For example, assume a user is moving from `http://foo.com` to `http://bar.com`. Doing a search and replace in the database for `"http://foo.com"` and replacing that is very easy and unlikely to be problematic. One might say that a root-relative URL would not need to change at all in such a case, and this is true, but what if the content needs to be moved from `http://foo.com/dev/` to `http://bar.com`? The root-relative URLs still need to change in such a case, and now there isn’t a simple to find string, such as `"http://foo.com/dev/"` to search and replace on.

Also, within the content of posts themselves, absolute URLs are easier to manage.

It has been suggested that if WordPress were to be able to do all of this over, [we may have instead opted for relative URLs](https://core.trac.wordpress.org/ticket/17048#comment:46). This is true, and making adjustments to our current approach – or reconsidering it in its entirety – does remain a distinct possibility in the future. See [#17048](https://core.trac.wordpress.org/ticket/17048).

## No support for forwarding headers for HTTPS or IP addresses

Many load balancers and proxy servers forward HTTP headers for HTTPS, IP addresses, and more. These typically take the form of HTTP\_X\_FORWARDED\_FOR (X-Forwarded-For), for remote IP addresses, and HTTP\_X\_FORWARDED\_PROTO (X-Forwarded-Proto), for whether traffic is going over the HTTPS protocol. Occasionally other information needs to be forwarded, like the server port.

If WordPress blindly listened to these headers – especially for protocols – there is a risk of infinite redirects and general breakage. To make matters worse, these are not formal standards, and are rather freeform. As a result, many web server and  configurations do this differently. For example, one configuration might prepend “HTTP\_”, resulting in HTTP\_HTTPS. What should be done instead is a server should either pass properly mapped headers to PHP, or some code can do the mapping in `wp-config.php`. For example:

```php
if (
	isset( $_SERVER['HTTP_X_FORWARDED_PROTO'] ) && 
	'https' === $_SERVER['HTTP_X_FORWARDED_PROTO'] 
) {
	$_SERVER['HTTPS'] = 'on';
}
```

See also: [#9235](https://core.trac.wordpress.org/ticket/9235), [#15009](https://core.trac.wordpress.org/ticket/15009), [#15733](https://core.trac.wordpress.org/ticket/15733), [#19337](https://core.trac.wordpress.org/ticket/19337), [#24394](https://core.trac.wordpress.org/ticket/24394), etc.

## Adding new oEmbed providers

We have a certain standard for oEmbed providers in core. In order to add a new one to the existing allow-list, they must:

*   be well-established, popular, and mainstream services,
*   properly and fully implement [the oEmbed specification](http://oembed.com/),
*   and clearly be a trusted provider.

Security is important with oEmbed, because it is dealing with raw, unfiltered HTML, which is inherently dangerous due to arbitrary JavaScript and object embedding. It is therefore paramount that the provider can be trusted. But trust is more than about security — the service must also be “built to last.” If a provider ever stops supporting oEmbed, sites start to lose content they previously trusted would stay embedded permanently.  Or, if a dead startup’s domain expires or is acquired, it could be an easy vector for malware. Nascent services are just too fragile to be added for core.

With regards to establishment and popularity, there are a number of things that can be considered, such as:

*   Is the service is popular enough for core developers to have heard of it before? Is it “mainstream?”
*   If similar services are already supported, how does this service compare in terms of size, features, and backing?
*   Does this service have an established social media presence?
*   Is its oEmbed endpoint clearly established and properly documented? (Sometimes, they are just a developer’s pet project that may not be supported.)
*   Does the oEmbed endpoint work with WordPress’ oEmbed auto-discovery? If not, could it be made to work with additional HTML tags or attributes being added to the allow-list?
*   Does the service make an effort to build relationships with developers, such as through robust APIs?
*   How old is the service?
*   Does it have a well-established Wikipedia article? (Seriously.)
*   Has anyone written a WordPress plugin that leverages the service in some way, whether adding it as an oEmbed provider, creating a shortcode, or leveraging other APIs of the service? Do these plugins have any noticeable adoption or traction that would indicate usage and demand?
*   Is the provider frequently proposed?

Individually, these are all very anecdotal. But when considered holistically, it paints a pretty decent picture.

## Unfiltered HTML for editors, administrators; multisite

Users with Administrator or Editor roles are allowed to publish unfiltered HTML in post titles, post content, and comments. WordPress is, after all, a publishing tool, and people need to be able to include whatever markup they need to communicate. Users with lesser privileges are not allowed to post unfiltered content.

If you are running security tests against WordPress, use a lesser privileged user so that all content is filtered. See the [Reporting Security Vulnerabilities](https://make.wordpress.org/core/handbook/reporting-security-vulnerabilities/) page for further information.

If you are concerned about an Administrator putting XSS into content and stealing cookies, note that all cookies are marked for HTTP only delivery and are divided into privileged cookies used for admin pages and lesser-privileged cookies used for public-facing pages. Content is never displayed unfiltered in the admin. Regardless, an Administrator has wide-ranging super powers among which unfiltered HTML is a lesser one.

In WordPress multisite, only super administrators can publish unfiltered HTML, as all other users are considered untrusted.

To disable unfiltered HTML for all users, including administrators and super administrators, you can add `define( 'DISALLOW_UNFILTERED_HTML', true );` to `wp-config.php`.

## Only owner-writeable is supported on upgrade, not group writeable

See [#10205](https://core.trac.wordpress.org/ticket/10205).

## Some esoteric MySQL settings are not supported

WordPress does not support MySQL strict mode or autocommit = 0. [#8857](https://core.trac.wordpress.org/ticket/8857), [#16821](https://core.trac.wordpress.org/ticket/16821), [#16429](https://core.trac.wordpress.org/ticket/16429).