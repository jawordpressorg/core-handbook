# Spelling

## Terminology

The following conventions of spelling and terminology apply to the manuals, web pages, comments, and (except where they require spaces or hyphens to be used) function and variable names, although consistency in user-visible documentation and diagnostics is more important than that in comments and code. Also don’t forget that the [Code Reference](https://developer.wordpress.org/reference/) is auto-generated from the code. The following table lists some simple cases:

| Use… | …instead of | Notes |
| --- | --- | --- |
| American spelling (in particular -ize, -or) | British spelling (in particular -ise, -our) |   |
| “a user” or “a URL” | “an user” or “an URL” | [#31894](https://core.trac.wordpress.org/ticket/31894), [#36218](https://core.trac.wordpress.org/ticket/36218) |
| “Ajax” | “ajax” or “AJAX” | “The name \[Ajax\] is shorthand for Asynchronous JavaScript + XML, and it represents a fundamental shift in what’s possible on the Web.” ([Source](http://adaptivepath.org/ideas/ajax-new-approach-web-applications/)) |
| “allowed list”, “allowed”, “permitted” | “whitelist” | “Whitelist” can be considered racially insensitive and is also ambiguous. Try using one of the suggested alternatives, or rewording to describe what is actually being allowed more clearly. |
| “Auto-update” or “auto-update” | “auto update” or “autoupdate” |   |
| “back end” (noun) | “back-end” or “backend” | [](https://core.trac.wordpress.org/ticket/34887)[](https://core.trac.wordpress.org/ticket/34887)[](https://core.trac.wordpress.org/ticket/34887)[#34887](https://core.trac.wordpress.org/ticket/34887) |
| “back-end” (adjective) | “back end” or “backend” | [](https://core.trac.wordpress.org/ticket/34887)[](https://core.trac.wordpress.org/ticket/34887)[](https://core.trac.wordpress.org/ticket/34887)[#34887](https://core.trac.wordpress.org/ticket/34887) |
| “backward compatibility” or “back-compat” | “backwards compatibility” or “backwards compat” | [#36835](https://core.trac.wordpress.org/ticket/36835) |
| “block list”, “disallowed list”, “disallowed” | “blacklist” | “Blacklist” can be considered racially insensitive and is also ambiguous. Try using one of the suggested alternatives, or rewording to describe what is actually being blocked more clearly. |
| “block editor” or “block-based editor” | “Block Editor” or “Gutenberg” | When referring to the new editor. |
| “block theme” | “block-based theme” |  |
| “Classic Editor” | “classic editor” | When referring to the [Classic Editor plugin](https://wordpress.org/plugins/classic-editor/). |
| “classic editor” | “Classic Editor” | When referring to the classic editor interface and not the plugin. |
| “visual editor” | “Visual Editor” | When referring to the visual editor interface. |
| “code editor” | “Code Editor” | When referring to the code editor interface. |
| “Customizer” | “Theme Customizer” or “customizer” | The Customizer isn’t necessarily theme-specific, [#29947](https://core.trac.wordpress.org/ticket/29947) |
| “Dark Mode” | “dark mode” or “dark-mode” | [Twenty Twenty-One #855](https://github.com/WordPress/twentytwentyone/pull/855) |
| “email” | “e-mail” | [#26156](https://core.trac.wordpress.org/ticket/26156) |
| “front end” (noun) | “front-end” or “frontend” | [](https://core.trac.wordpress.org/ticket/34887)[](https://core.trac.wordpress.org/ticket/34887)[](https://core.trac.wordpress.org/ticket/34887)[#34887](https://core.trac.wordpress.org/ticket/34887) |
| “front-end” (adjective) | “front end” or “frontend” | [](https://core.trac.wordpress.org/ticket/34887)[](https://core.trac.wordpress.org/ticket/34887)[](https://core.trac.wordpress.org/ticket/34887)[#34887](https://core.trac.wordpress.org/ticket/34887) |
| “full site editing” | “Full Site Editing” or “full-site editing” |  |
| “homepage” (noun) | “home page” | [#41828](https://core.trac.wordpress.org/ticket/41828) |
| “installation” (noun) | “install” | The word “install” is not a noun. When referring to an instance of WordPress, the correct word to use is “installation”.  
[#41620](https://core.trac.wordpress.org/ticket/41620) |
| “JavaScript” | “Javascript” or “javascript” | [#30569](https://core.trac.wordpress.org/ticket/30569) |
| “log in” (verb) | “login” | The word “login” is not a verb. When referring to the action of logging in, the correct phrase to use is “log in”.  
[#18294](https://core.trac.wordpress.org/ticket/18294) |
| “meta box” | “metabox” |   |
| “oEmbed” | “embed” |   |
| “Paragraph block” | “Paragraph Block” or “paragraph block” | When referring to blocks capitalize the block name and keep ‘block’ lowercase. [github#16118](https://github.com/WordPress/gutenberg/issues/16118#issuecomment-501458511) |
| “retrieve” | “retreive” or “retrive” | “retreive” or “retrive” aren’t words, [\[2465\]](https://core.trac.wordpress.org/changeset/2465) |
| “term meta” | “termmeta” |   |
| “WordPress” | “WP” | “WordPress” is preferred when referring to the CMS, project, or community.  One exception is when referencing a specific version, e.g. “WP 5.0”, or where the trademark rules prohibit the use of “WordPress”. |

Inspired by the [GCC Coding Convention](https://gcc.gnu.org/codingconventions.html#Spelling).

## Capitalization

*   Labels
*   Button labels
*   Actions

## Abbreviations and Acronyms

Use abbreviations and acronyms only when they are familiar.

## Quotation marks

In DocBlock comments use the *straight* sin­gle quote (`'`) or the straight dou­ble quote (`"`). In strings, which are visible to users, use *curly* quotes: The open­ing sin­gle quote (`‘`), the clos­ing sin­gle quote (`’`), the open­ing dou­ble quote (`“`), and the clos­ing dou­ble quote (`”`).  
See also [Butterick’s Practical Typography](http://practicaltypography.com/straight-and-curly-quotes.html).