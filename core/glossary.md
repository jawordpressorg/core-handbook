# Glossary

dl.glossary-list dd { margin-top: -50px; padding-top: 50px; }

**a11y**

Accessibility, or the act of ensuring a high quality experience for all users regardless of blindness and low vision, deafness and hearing loss, learning disabilities, cognitive limitations, limited movement, speech disabilities, photosensitivity and combinations of these. [#](https://make.wordpress.org/core/handbook/glossary/#a11y)

**admin**

(and super admin) [#](https://make.wordpress.org/core/handbook/glossary/#admin)

**alpha (beta)**

Pre-release version of software intended to signal desire for compatibility, functional, and unit tests and feedback. Also see [release candidate](#release-candidate). [#](https://make.wordpress.org/core/handbook/glossary/#alpha-beta)

**back compat**

Backward compatibility – a desire to ensure that plugins and themes do not break under new releases – is a driving philosophy of WordPress. While it is a commonly accepted software development practice to break compatibility in major releases, WordPress strives to avoid this at all costs. Any backward incompatible change is carefully considered by the entire core development team and announced, with affected plugins often contacted. It should be noted that external libraries, such as jQuery, do have backward incompatible changes between major releases, which is often going to be a greater concern for developers. [#](https://make.wordpress.org/core/handbook/glossary/#back-compat)

**backport**

A port is when code from one branch (or trunk) is merged into another branch or trunk. Some changes in WordPress point releases are the result of backporting code from trunk to the release branch. [#](https://make.wordpress.org/core/handbook/glossary/#backport)

**bleeding edge**

The latest revision of the software, generally in development and often unstable. Also known as [trunk](#trunk). [#](https://make.wordpress.org/core/handbook/glossary/#bleeding-edge)

**blocker**

A bug which is so severe that it blocks a release. [#](https://make.wordpress.org/core/handbook/glossary/#blocker)

**blog**

(versus network, site) [#](https://make.wordpress.org/core/handbook/glossary/#blog)

**branch**

A directory in Subversion. WordPress uses branches to store the latest development code for each major release (3.9, 4.0, etc.). Branches are then updated with code for any minor releases of that branch. Sometimes, a major version of WordPress and its minor versions are collectively referred to as a “branch”, such as “the 4.0 branch”. [#](https://make.wordpress.org/core/handbook/glossary/#branch)

**bug**

A bug is an error or unexpected result. Performance improvements, code optimization, and are considered enhancements, not defects. After feature freeze, only bugs are dealt with, with regressions (adverse changes from the previous version) being the highest priority. [#](https://make.wordpress.org/core/handbook/glossary/#bug)

**command line interface (CLI)**

A type of human-computer interface (i.e., a way for humans to interact with computers) that relies solely on textual input and output. The entire display screen, or the currently active portion of it, shows only characters (and no images), and input is usually performed entirely with a keyboard. [#](https://make.wordpress.org/core/handbook/glossary/#command-line-interface)

**commit (noun)**

An individual change to WordPress, identified by an incremental revision number. Also called a **changeset**. [#](https://make.wordpress.org/core/handbook/glossary/#commit-noun)

**commit (verb)**

To make a change to WordPress. Only committers can commit code, but often the code is *contributed* by developers without commit access. [#](https://make.wordpress.org/core/handbook/glossary/#commit-verb)

**committer**

A developer with commit access. WordPress has five lead developers and four permanent core developers with commit access. Additionally, the project usually has a few guest or component committers – a developer receiving commit access, generally for a single release cycle (sometimes renewed) and/or for a specific component. [#](https://make.wordpress.org/core/handbook/glossary/#committer)

**conflict**

A conflict occurs when a patch changes code that was modified after the patch was created. These patches are considered *stale*, and will require a *refresh* of the changes before it can be applied, or the conflicts will need to be *resolved*. [#](https://make.wordpress.org/core/handbook/glossary/#conflict)

**copyright license**

Copyright holders may grant a license with various allowances including the ability to modify or distribute the copyrighted material. Also see [GPL](#gpl). [#](https://make.wordpress.org/core/handbook/glossary/#copyright-license)

**CRUD**

Create, read, update and delete, the four basic functions of storing data. (More on [Wikipedia](http://en.wikipedia.org/wiki/Create,_read,_update_and_delete).) [#](https://make.wordpress.org/core/handbook/glossary/#crud)

**CSS**

Cascading Style Sheets. [#](https://make.wordpress.org/core/handbook/glossary/#css)

**dev note**

Each important change in WordPress Core is documented in a developers note, (usually called dev note). Good dev notes generally include a description of the change, the decision that led to this change, and a description of how developers are supposed to work with that change. Dev notes are published on Make/Core blog during the beta phase of WordPress release cycle. Publishing dev notes is particularly important when plugin/theme authors and WordPress developers need to be aware of those changes.In general, all dev notes are compiled into a Field Guide at the beginning of the release candidate phase. [#](https://make.wordpress.org/core/handbook/glossary/#dev-note)

**docblock**

(phpdoc, xref, inline docs) [#](https://make.wordpress.org/core/handbook/glossary/#docblock)

**dogfood**

The practice of using one’s own software, typically bleeding edge (trunk), thus “eating one’s own dogfood”. This also applies to using one’s own APIs internally. [#](https://make.wordpress.org/core/handbook/glossary/#dogfood)

**enhancement**

Enhancements are simple improvements to WordPress, such as the addition of a hook, a new feature, or an improvement to an existing feature. [#](https://make.wordpress.org/core/handbook/glossary/#enhancement)

**feature request**

A feature request should generally begin the process in the ideas forum, on a mailing list, as a plugin, or brought to the attention of the core team, such as through scope meetings held for each major release. Unsolicited tickets of this variety are typically, therefore, discouraged. [#](https://make.wordpress.org/core/handbook/glossary/#feature-request)

**Field guide**

The field guide is a type of blogpost published on Make/Core during the release candidate phase of the [WordPress release cycle](https://make.wordpress.org/core/handbook/about/release-cycle/). The field guide generally lists all the dev notes published during the beta cycle. This guide is linked in the about page of the corresponding version of WordPress, in the release post and in the HelpHub version page. [#](https://make.wordpress.org/core/handbook/glossary/#field-guide)

**GPL**

GNU General Public License. Also see [copyright license](#copyright-license). [#](https://make.wordpress.org/core/handbook/glossary/#gpl)

**hacked**

[#](https://make.wordpress.org/core/handbook/glossary/#hacked)

**HTML**

HyperText Markup Language. The semantic scripting language primarily used for outputting content in web browsers. [#](https://make.wordpress.org/core/handbook/glossary/#html)

**i18n**

Internationalization, or the act of writing and preparing code to be fully translatable into other languages. Also see [localization](#l10n). Often written with a lowercase i so it is not confused with a lowercase L or the numeral 1. Often an acquired skill. [#](https://make.wordpress.org/core/handbook/glossary/#i18n)

**IDE**

Integrated Development Environment. A software package that provides a full suite of functionality to software developers/programmers. Normally an IDE includes a source code editor, code-build tools and debugging functionality. [#](https://make.wordpress.org/core/handbook/glossary/#ide)

**inline docs**

(phpdoc, docblock, xref) [#](https://make.wordpress.org/core/handbook/glossary/#inline-docs)

**invalid**

A resolution on the bug tracker (and generally common in software development, sometimes also *notabug*) that indicates the ticket is not a bug, is a support request, or is generally invalid. [#](https://make.wordpress.org/core/handbook/glossary/#invalid)

**IRC**

Internet Relay Chat, a network where users can have conversations online. IRC channels are used widely by open source projects, and by WordPress. The primary WordPress channels are **[#wordpress](https://make.wordpress.org/core/tag/wordpress/)** and **[#wordpress-dev](https://make.wordpress.org/core/tag/wordpress-dev/)**, on irc.freenode.net. [#](https://make.wordpress.org/core/handbook/glossary/#irc)

**JS**

JavaScript, a web scripting language typically executed in the browser. Often used for advanced user interfaces and behaviors. [#](https://make.wordpress.org/core/handbook/glossary/#js)

**L10n**

Localization, or the act of translating code into one’s own language. Also see [internationalization](#i18n). Often written with an uppercase L so it is not confused with the capital letter i or the numeral 1. WordPress has a capable and dynamic group of polyglots who take WordPress to more than 70 different locales. [#](https://make.wordpress.org/core/handbook/glossary/#l10n)

**Locale**

A locale is a combination of language and regional dialect. Usually locales correspond to countries, as is the case with Portuguese (Portugal) and Portuguese (Brazil). Other examples of locales include Canadian English and U.S. English. [#](https://make.wordpress.org/core/handbook/glossary/#locale)

**major release**

A release, identified by the first two numbers (3.6), which is the focus of a full release cycle and feature development. WordPress uses decimaling count for major release versions, so 2.8, 2.9, 3.0, and 3.1 are sequential and comparable in scope. [#](https://make.wordpress.org/core/handbook/glossary/#major-release)

**mu-plugins, must-use plugins**

(include old history as “multi-user”; x-ref with drop-ins) [#](https://make.wordpress.org/core/handbook/glossary/#mu-plugins-must-use-plugins)

**multisite**

Used to describe a WordPress installation with a network of multiple blogs, grouped by sites. This installation type has shared users tables, and creates separate database tables for each blog (wp\_posts becomes wp\_0\_posts). See also **network**, **blog**, **site** [#](https://make.wordpress.org/core/handbook/glossary/#multisite)

**network**

(versus site, blog) [#](https://make.wordpress.org/core/handbook/glossary/#network)

**P2**

A [free theme for WordPress](http://p2theme.com/), known for front-end posting, used by WordPress for development updates and project management. See our [main development blog](https://make.wordpress.org/core/) and [other workgroup blogs](https://make.wordpress.org/). [#](https://make.wordpress.org/core/handbook/glossary/#p2)

**patch**

A special text file that describes changes to code, by identifying the files and lines which are added, removed, and altered. It may also be referred to as a **diff**. A patch can be *applied* to a codebase for testing. [#](https://make.wordpress.org/core/handbook/glossary/#patch)

**PHP**

The web scripting language in which WordPress is primarily architected. WordPress requires PHP 7.4 or higher [#](https://make.wordpress.org/core/handbook/glossary/#php)

**PHPDoc**

(**docblock**, **inline docs**) [#](https://make.wordpress.org/core/handbook/glossary/#phpdoc)

**point release**

A minor release of WordPress, identified by the third number (the 2 in 3.5.2). These releases are for maintenance and security fixes only. Feature development is limited to major releases. Changes to point releases are carefully considered, and only critical or blocker\-level bugs, and security enhancements, hardening, and fixes are accepted. [#](https://make.wordpress.org/core/handbook/glossary/#point-release)

**priority (bug tracker)**

The seriousness of a bug report or ticket in the eyes of the project. Generally, **severity** is a judgment of how bad a bug is, while priority is its relationship to other bugs. [#](https://make.wordpress.org/core/handbook/glossary/#priority-bug-tracker)

**priority (hooks)**

(higher priority means lower number) [#](https://make.wordpress.org/core/handbook/glossary/#priority-hooks)

**punt**

Contributors sometimes use the verb “punt” when talking about a ticket. This means it is being pushed out to a future release. This typically occurs for lower priority tickets near the end of the release cycle that don’t “make the cut.” In this is colloquial usage of the word, it means to delay or equivocate. (It also describes a play in American football where a team essentially passes up on an opportunity, hoping to put themselves in a better position later to try again.) [#](https://make.wordpress.org/core/handbook/glossary/#punt)

**RC**

A shortened name for [release candidate](https://make.wordpress.org/core/handbook/glossary/#release-candidate). [#](https://make.wordpress.org/core/handbook/glossary/#rc)

**regression**

A software bug that breaks or degrades something that previously worked. Regressions are often treated as critical bugs or [blockers](#blocker). Recent regressions may be given higher priorities. A “3.6 regression” would be a bug in 3.6 that worked as intended in 3.5. [#](https://make.wordpress.org/core/handbook/glossary/#regression)

**release candidate**

One of the final stages in the version release cycle, this version signals the potential to be a final release to the public. Also see [alpha (beta)](#alpha-beta). [#](https://make.wordpress.org/core/handbook/glossary/#release-candidate)

**scope creep**

The tendency for requirements to increase during a release’s development cycle beyond those originally approved for the upcoming release. Something to be avoided. Also known as feature creep. [#](https://make.wordpress.org/core/handbook/glossary/#scope-creep)

**security issue**

A security issue is a type of bug that can affect the security of WordPress installations. Specifically, it is a report of a bug that you have found in the WordPress core code, and that you have determined can be used to gain some level of access to a site running WordPress that you should not have. [#](https://make.wordpress.org/core/handbook/glossary/#security-issue)

**severity**

The seriousness of the ticket in the eyes of the reporter. Generally, severity is a judgment of how bad a bug is, while **priority** is its relationship to other bugs. [#](https://make.wordpress.org/core/handbook/glossary/#severity)

**SSL**

Secure Sockets Layer. Provides a secure means of sending data over the internet. Used for authenticated and private actions. [#](https://make.wordpress.org/core/handbook/glossary/#ssl)

**SVN**

Subversion, the popular version control system (VCS) by the Apache project, used by WordPress to manage changes to its codebase. [#](https://make.wordpress.org/core/handbook/glossary/#svn)

**tag**

A directory in Subversion. WordPress uses tags to store a single snapshot of a version (3.6, 3.6.1, etc.), the common convention of tags in version control systems. (Not to be confused with post tags.) [#](https://make.wordpress.org/core/handbook/glossary/#tag)

**task (blessed)**

Feature development for an upcoming major release centers around task tickets, which are major features or important enhancements that have been blessed by the core team. A ticket should otherwise never receive this designation. [#](https://make.wordpress.org/core/handbook/glossary/#task-blessed)

**ticket**

Created for both bug reports and feature development on the bug tracker. [#](https://make.wordpress.org/core/handbook/glossary/#ticket)

**Trac**

An open source project by Edgewall Software that serves as a bug tracker and project management tool for WordPress. [#](https://make.wordpress.org/core/handbook/glossary/#trac)

**translation**

The process (or result) of changing text, words, and display formatting to support another language. Also see [localization](#l10n), [internationalization](#i18n). [#](https://make.wordpress.org/core/handbook/glossary/#translation)

**triage**

The act of evaluating and sorting bug reports, in order to decide priority, severity, and other factors. [#](https://make.wordpress.org/core/handbook/glossary/#triage)

**trunk**

A directory in Subversion containing the latest development code in preparation for the next major release cycle. If you are running “trunk”, then you are on the latest revision. [#](https://make.wordpress.org/core/handbook/glossary/#trunk)

**UI**

User interface [#](https://make.wordpress.org/core/handbook/glossary/#ui)

**unit test**

Code written to test a small piece of code or functionality within a larger application. Everything from themes to WordPress core have a series of unit tests. Also see [regression](#regression). [#](https://make.wordpress.org/core/handbook/glossary/#unit-test)

**Unprops**

A commit that removes code gone awry may include *unprops* as a sign of respect for the risk taken by the original people working on it. [#](https://make.wordpress.org/core/handbook/glossary/#unprops)

**UX**

User experience [#](https://make.wordpress.org/core/handbook/glossary/#ux)

**version control**

A version control system keeps track of the source code and revisions to the source code. WordPress uses Subversion (SVN) for version control, with Git mirrors for most repositories. [#](https://make.wordpress.org/core/handbook/glossary/#version-control)

**wontfix**

A resolution on the bug tracker (and generally common in software development) that indicates the ticket will not be addressed further. This may be used for acceptable edge cases (for bugs), or enhancements that have been rejected for core inclusion. [#](https://make.wordpress.org/core/handbook/glossary/#wontfix)

**worksforme**

A resolution on the bug tracker (and generally common in software development) that indicates the bug reported cannot be reproduced. [#](https://make.wordpress.org/core/handbook/glossary/#worksforme)

**wpdevel**

Formerly the development updates P2 blog at wpdevel.wordpress.com. It is now **make/core** and resides at [make.wordpress.org/core](https://make.wordpress.org/core/). [#](https://make.wordpress.org/core/handbook/glossary/#wpdevel)

**xref**

(php-xref, phpdoc, inline docs) [#](https://make.wordpress.org/core/handbook/glossary/#xref)