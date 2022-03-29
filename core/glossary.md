# Glossary

dl.glossary-list dd { margin-top: -50px; padding-top: 50px; }

a11y

AccessibilityAccessibility Accessibility (commonly shortened to a11y) refers to the design of products, devices, services, or environments for people with disabilities. The concept of accessible design ensures both “direct access” (i.e. unassisted) and “indirect access” meaning compatibility with a person’s assistive technology (for example, computer screen readers). (https://en.wikipedia.org/wiki/Accessibility), or the act of ensuring a high quality experience for all users regardless of blindness and low vision, deafness and hearing loss, learning disabilities, cognitive limitations, limited movement, speech disabilities, photosensitivity and combinations of these. [#](https://make.wordpress.org/core/handbook/glossary/#a11y)

admin

(and super adminadmin (and super admin)) [#](https://make.wordpress.org/core/handbook/glossary/#admin)

alpha (beta)

Pre-release version of software intended to signal desire for compatibility, functional, and unit tests and feedback. Also see [release candidate](#release-candidate). [#](https://make.wordpress.org/core/handbook/glossary/#alpha-beta)

back compat

Backward compatibility – a desire to ensure that plugins and themes do not break under new releases – is a driving philosophy of WordPress. While it is a commonly accepted software development practice to break compatibility in major releases, WordPress strives to avoid this at all costs. Any backward incompatible change is carefully considered by the entire coreCore Core is the set of software required to run WordPress. The Core Development Team builds WordPress. development team and announced, with affected plugins often contacted. It should be noted that external libraries, such as jQuery, do have backward incompatible changes between major releases, which is often going to be a greater concern for developers. [#](https://make.wordpress.org/core/handbook/glossary/#back-compat)

backport

A port is when code from one branchbranch A directory in Subversion. WordPress uses branches to store the latest development code for each major release (3.9, 4.0, etc.). Branches are then updated with code for any minor releases of that branch. Sometimes, a major version of WordPress and its minor versions are collectively referred to as a "branch", such as "the 4.0 branch". (or trunktrunk A directory in Subversion containing the latest development code in preparation for the next major release cycle. If you are running "trunk", then you are on the latest revision.) is merged into another branch or trunk. Some changes in WordPress point releases are the result of backporting code from trunk to the release branch. [#](https://make.wordpress.org/core/handbook/glossary/#backport)

bleeding edge

The latest revision of the software, generally in development and often unstable. Also known as [trunk](#trunk). [#](https://make.wordpress.org/core/handbook/glossary/#bleeding-edge)

blocker

A bugbug A bug is an error or unexpected result. Performance improvements, code optimization, and are considered enhancements, not defects. After feature freeze, only bugs are dealt with, with regressions (adverse changes from the previous version) being the highest priority. which is so severe that it blocks a release. [#](https://make.wordpress.org/core/handbook/glossary/#blocker)

blog

(versus networknetwork (versus site, blog), site) [#](https://make.wordpress.org/core/handbook/glossary/#blog)

branch

A directory in Subversion. WordPress uses branches to store the latest development code for each major releasemajor release A release, identified by the first two numbers (3.6), which is the focus of a full release cycle and feature development. WordPress uses decimaling count for major release versions, so 2.8, 2.9, 3.0, and 3.1 are sequential and comparable in scope. (3.9, 4.0, etc.). Branches are then updated with code for any minor releases of that branchbranch A directory in Subversion. WordPress uses branches to store the latest development code for each major release (3.9, 4.0, etc.). Branches are then updated with code for any minor releases of that branch. Sometimes, a major version of WordPress and its minor versions are collectively referred to as a "branch", such as "the 4.0 branch".. Sometimes, a major version of WordPress and its minor versions are collectively referred to as a “branch”, such as “the 4.0 branch”. [#](https://make.wordpress.org/core/handbook/glossary/#branch)

bug

A bugbug A bug is an error or unexpected result. Performance improvements, code optimization, and are considered enhancements, not defects. After feature freeze, only bugs are dealt with, with regressions (adverse changes from the previous version) being the highest priority. is an error or unexpected result. Performance improvements, code optimization, and are considered enhancements, not defects. After feature freeze, only bugs are dealt with, with regressions (adverse changes from the previous version) being the highest priority. [#](https://make.wordpress.org/core/handbook/glossary/#bug)

command line interface (CLI)

A type of human-computer interface (i.e., a way for humans to interact with computers) that relies solely on textual input and output. The entire display screen, or the currently active portion of it, shows only characters (and no images), and input is usually performed entirely with a keyboard. [#](https://make.wordpress.org/core/handbook/glossary/#command-line-interface)

commit (noun)

An individual change to WordPress, identified by an incremental revision number. Also called a **changeset**. [#](https://make.wordpress.org/core/handbook/glossary/#commit-noun)

commit (verb)

To make a change to WordPress. Only committers can commit code, but often the code is *contributed* by developers without commit access. [#](https://make.wordpress.org/core/handbook/glossary/#commit-verb)

committer

A developer with commit access. WordPress has five lead developers and four permanent coreCore Core is the set of software required to run WordPress. The Core Development Team builds WordPress. developers with commit access. Additionally, the project usually has a few guest or component committers – a developer receiving commit access, generally for a single release cycle (sometimes renewed) and/or for a specific component. [#](https://make.wordpress.org/core/handbook/glossary/#committer)

conflict

A conflictconflict A conflict occurs when a patch changes code that was modified after the patch was created. These patches are considered *stale*, and will require a *refresh* of the changes before it can be applied, or the conflicts will need to be *resolved*. occurs when a patchpatch A special text file that describes changes to code, by identifying the files and lines which are added, removed, and altered. It may also be referred to as a **diff**. A patch can be *applied* to a codebase for testing. changes code that was modified after the patch was created. These patches are considered *stale*, and will require a *refresh* of the changes before it can be applied, or the conflicts will need to be *resolved*. [#](https://make.wordpress.org/core/handbook/glossary/#conflict)

copyright license

Copyright holders may grant a license with various allowances including the ability to modify or distribute the copyrighted material. Also see [GPL](#gpl). [#](https://make.wordpress.org/core/handbook/glossary/#copyright-license)

CRUD

Create, read, update and delete, the four basic functions of storing data. (More on [Wikipedia](http://en.wikipedia.org/wiki/Create,_read,_update_and_delete).) [#](https://make.wordpress.org/core/handbook/glossary/#crud)

CSS

Cascading Style Sheets. [#](https://make.wordpress.org/core/handbook/glossary/#css)

dev note

Each important change in WordPress CoreCore Core is the set of software required to run WordPress. The Core Development Team builds WordPress. is documented in a developers note, (usually called dev notedev note Each important change in WordPress Core is documented in a developers note, (usually called dev note). Good dev notes generally include: a description of the change; the decision that led to this change a description of how developers are supposed to work with that change. Dev notes are published on Make/Core blog during the beta phase of WordPress release cycle. Publishing dev notes is particularly important when plugin/theme authors and WordPress developers need to be aware of those changes.In general, all dev notes are compiled into a Field Guide at the beginning of the release candidate phase.dev note Each important change in WordPress Core is documented in a developers note, (usually called dev note). Good dev notesdev note Each important change in WordPress Core is documented in a developers note, (usually called dev note). Good dev notes generally include: a description of the change; the decision that led to this change a description of how developers are supposed to work with that change. Dev notes are published on Make/Core blog during the beta phase of WordPress release cycle. Publishing dev notes is particularly important when plugin/theme authors and WordPress developers need to be aware of those changes.In general, all dev notes are compiled into a Field Guide at the beginning of the release candidate phase. generally include: a description of the change; the decision that led to this change a description of how developers are supposed to work with that change. Dev notes are published on Make/Core blog during the beta phase of WordPress release cycle. Publishing dev notes is particularly important when plugin/theme authors and WordPress developers need to be aware of those changes.In general, all dev notes are compiled into a Field Guide at the beginning of the release candidate phase.). Good dev notesdev note Each important change in WordPress Core is documented in a developers note, (usually called dev note). Good dev notes generally include: a description of the change; the decision that led to this change a description of how developers are supposed to work with that change. Dev notes are published on Make/Core blog during the beta phase of WordPress release cycle. Publishing dev notes is particularly important when plugin/theme authors and WordPress developers need to be aware of those changes.In general, all dev notes are compiled into a Field Guide at the beginning of the release candidate phase. generally include:

*   a description of the change;
*   the decision that led to this change
*   a description of how developers are supposed to work with that change.

Dev notes are published on Make/Core blogblog (versus network, site) during the betaBeta A pre-release of software that is given out to a large group of users to trial under real conditions. Beta versions have gone through alpha testing in-house and are generally fairly close in look, feel and function to the final product; however, design changes often occur as part of the process. phase of WordPress release cycle. Publishing dev notes is particularly important when pluginPlugin A plugin is a piece of software containing a group of functions that can be added to a WordPress website. They can extend functionality or add new features to your WordPress websites. WordPress plugins are written in the PHP programming language and integrate seamlessly with WordPress. These can be free in the WordPress.org Plugin Directory https://wordpress.org/plugins/ or can be cost-based plugin from a third-party/theme authors and WordPress developers need to be aware of those changes.In general, all dev notes are compiled into a Field GuideField guide The field guide is a type of blogpost published on Make/Core during the release candidate phase of the [WordPress release cycle](https://make.wordpress.org/core/handbook/about/release-cycle/). The field guide generally lists all the dev notes published during the beta cycle. This guide is linked in the about page of the corresponding version of WordPress, in the release post and in the HelpHub version page. at the beginning of the release candidaterelease candidate One of the final stages in the version release cycle, this version signals the potential to be a final release to the public. Also see [alpha (beta)](#alpha-beta). phase. [#](https://make.wordpress.org/core/handbook/glossary/#dev-note)

docblock

(phpdocPHPDoc (**docblock**, **inline docs**), xrefxref (php-xref, phpdoc, inline docs), inline docsinline docs (phpdoc, docblock, xref)) [#](https://make.wordpress.org/core/handbook/glossary/#docblock)

dogfood

The practice of using one’s own software, typically bleeding edgebleeding edge The latest revision of the software, generally in development and often unstable. Also known as [trunk](#trunk). (trunktrunk A directory in Subversion containing the latest development code in preparation for the next major release cycle. If you are running "trunk", then you are on the latest revision.), thus “eating one’s own dogfooddogfood The practice of using one's own software, typically bleeding edge (trunk), thus "eating one's own dogfood". This also applies to using one's own APIs internally.”. This also applies to using one’s own APIs internally. [#](https://make.wordpress.org/core/handbook/glossary/#dogfood)

enhancement

Enhancements are simple improvements to WordPress, such as the addition of a hook, a new feature, or an improvement to an existing feature. [#](https://make.wordpress.org/core/handbook/glossary/#enhancement)

feature request

A feature requestfeature request A feature request should generally begin the process in the ideas forum, on a mailing list, as a plugin, or brought to the attention of the core team, such as through scope meetings held for each major release. Unsolicited tickets of this variety are typically, therefore, discouraged. should generally begin the process in the ideas forum, on a mailing list, as a pluginPlugin A plugin is a piece of software containing a group of functions that can be added to a WordPress website. They can extend functionality or add new features to your WordPress websites. WordPress plugins are written in the PHP programming language and integrate seamlessly with WordPress. These can be free in the WordPress.org Plugin Directory https://wordpress.org/plugins/ or can be cost-based plugin from a third-party, or brought to the attention of the coreCore Core is the set of software required to run WordPress. The Core Development Team builds WordPress. team, such as through scope meetings held for each major releasemajor release A release, identified by the first two numbers (3.6), which is the focus of a full release cycle and feature development. WordPress uses decimaling count for major release versions, so 2.8, 2.9, 3.0, and 3.1 are sequential and comparable in scope.. Unsolicited tickets of this variety are typically, therefore, discouraged. [#](https://make.wordpress.org/core/handbook/glossary/#feature-request)

Field guide

The field guideField guide The field guide is a type of blogpost published on Make/Core during the release candidate phase of the [WordPress release cycle](https://make.wordpress.org/core/handbook/about/release-cycle/). The field guide generally lists all the dev notes published during the beta cycle. This guide is linked in the about page of the corresponding version of WordPress, in the release post and in the HelpHub version page. is a type of blogpost published on Make/CoreCore Core is the set of software required to run WordPress. The Core Development Team builds WordPress. during the release candidaterelease candidate One of the final stages in the version release cycle, this version signals the potential to be a final release to the public. Also see [alpha (beta)](#alpha-beta). phase of the [WordPress release cycle](https://make.wordpress.org/core/handbook/about/release-cycle/). The field guide generally lists all the dev notesdev note Each important change in WordPress Core is documented in a developers note, (usually called dev note). Good dev notes generally include: a description of the change; the decision that led to this change a description of how developers are supposed to work with that change. Dev notes are published on Make/Core blog during the beta phase of WordPress release cycle. Publishing dev notes is particularly important when plugin/theme authors and WordPress developers need to be aware of those changes.In general, all dev notes are compiled into a Field Guide at the beginning of the release candidate phase. published during the betaBeta A pre-release of software that is given out to a large group of users to trial under real conditions. Beta versions have gone through alpha testing in-house and are generally fairly close in look, feel and function to the final product; however, design changes often occur as part of the process. cycle. This guide is linked in the about page of the corresponding version of WordPress, in the release post and in the HelpHub version page. [#](https://make.wordpress.org/core/handbook/glossary/#field-guide)

GPL

GNU General Public License. Also see [copyright license](#copyright-license). [#](https://make.wordpress.org/core/handbook/glossary/#gpl)

hacked

[#](https://make.wordpress.org/core/handbook/glossary/#hacked)

HTML

HyperText Markup Language. The semantic scripting language primarily used for outputting content in web browsers. [#](https://make.wordpress.org/core/handbook/glossary/#html)

i18n

Internationalization, or the act of writing and preparing code to be fully translatable into other languages. Also see [localization](#l10n). Often written with a lowercase i so it is not confused with a lowercase L or the numeral 1. Often an acquired skill. [#](https://make.wordpress.org/core/handbook/glossary/#i18n)

IDE

Integrated Development Environment. A software package that provides a full suite of functionality to software developers/programmers. Normally an IDEIDE Integrated Development Environment. A software package that provides a full suite of functionality to software developers/programmers. Normally an IDE includes a source code editor, code-build tools and debugging functionality. includes a source code editor, code-build tools and debugging functionality. [#](https://make.wordpress.org/core/handbook/glossary/#ide)

inline docs

(phpdocPHPDoc (**docblock**, **inline docs**), docblockdocblock (phpdoc, xref, inline docs), xrefxref (php-xref, phpdoc, inline docs)) [#](https://make.wordpress.org/core/handbook/glossary/#inline-docs)

invalid

A resolution on the bugbug A bug is an error or unexpected result. Performance improvements, code optimization, and are considered enhancements, not defects. After feature freeze, only bugs are dealt with, with regressions (adverse changes from the previous version) being the highest priority. tracker (and generally common in software development, sometimes also *notabug*) that indicates the ticketticket Created for both bug reports and feature development on the bug tracker. is not a bug, is a support request, or is generally invalidinvalid A resolution on the bug tracker (and generally common in software development, sometimes also *notabug*) that indicates the ticket is not a bug, is a support request, or is generally invalid.. [#](https://make.wordpress.org/core/handbook/glossary/#invalid)

IRC

Internet Relay Chat, a networknetwork (versus site, blog) where users can have conversations online. IRCIRC Internet Relay Chat, a network where users can have conversations online. IRC channels are used widely by open source projects, and by WordPress. The primary WordPress channels are **[#wordpress](https://make.wordpress.org/core/tag/wordpress/)** and **[#wordpress](https://make.wordpress.org/core/tag/wordpress/)\-dev**, on irc.freenode.net. channels are used widely by open sourceOpen Source Open Source denotes software for which the original source code is made freely available and may be redistributed and modified. Open Source \*\*must be\*\* delivered via a licensing model, see GPL. projects, and by WordPress. The primary WordPress channels are **[#wordpress](https://make.wordpress.org/core/tag/wordpress/)** and **[#wordpress](https://make.wordpress.org/core/tag/wordpress/)\-dev**, on irc.freenode.net. [#](https://make.wordpress.org/core/handbook/glossary/#irc)

JS

JavaScriptJavaScript JavaScript or JS is an object-oriented computer programming language commonly used to create interactive effects within web browsers. WordPress makes extensive use of JS for a better user experience. While PHP is executed on the server, JS executes within a user’s browser. [https://www.javascript.com/](https://www.javascript.com/)., a web scripting language typically executed in the browser. Often used for advanced user interfaces and behaviors. [#](https://make.wordpress.org/core/handbook/glossary/#js)

L10n

Localization, or the act of translating code into one’s own language. Also see [internationalization](#i18n). Often written with an uppercase L so it is not confused with the capital letter i or the numeral 1. WordPress has a capable and dynamic group of polyglots who take WordPress to more than 70 different locales. [#](https://make.wordpress.org/core/handbook/glossary/#l10n)

Locale

A localeLocale A locale is a combination of language and regional dialect. Usually locales correspond to countries, as is the case with Portuguese (Portugal) and Portuguese (Brazil). Other examples of locales include Canadian English and U.S. English. is a combination of language and regional dialect. Usually locales correspond to countries, as is the case with Portuguese (Portugal) and Portuguese (Brazil). Other examples of locales include Canadian English and U.S. English. [#](https://make.wordpress.org/core/handbook/glossary/#locale)

major release

A release, identified by the first two numbers (3.6), which is the focus of a full release cycle and feature development. WordPress uses decimaling count for major releasemajor release A release, identified by the first two numbers (3.6), which is the focus of a full release cycle and feature development. WordPress uses decimaling count for major release versions, so 2.8, 2.9, 3.0, and 3.1 are sequential and comparable in scope. versions, so 2.8, 2.9, 3.0, and 3.1 are sequential and comparable in scope. [#](https://make.wordpress.org/core/handbook/glossary/#major-release)

mu-plugins, must-use plugins

(include old history as “multi-user”; x-ref with drop-ins) [#](https://make.wordpress.org/core/handbook/glossary/#mu-plugins-must-use-plugins)

multisite

Used to describe a WordPress installation with a networknetwork (versus site, blog) of multiple blogs, grouped by sites. This installation type has shared users tables, and creates separate database tables for each blogblog (versus network, site) (wp\_posts becomes wp\_0\_posts). See also **network**, **blog**, **site** [#](https://make.wordpress.org/core/handbook/glossary/#multisite)

network

(versus site, blogblog (versus network, site)) [#](https://make.wordpress.org/core/handbook/glossary/#network)

P2

A [free theme for WordPress](http://p2theme.com/), known for front-end posting, used by WordPress for development updates and project management. See our [main development blog](https://make.wordpress.org/core/) and [other workgroup blogs](https://make.wordpress.org/). [#](https://make.wordpress.org/core/handbook/glossary/#p2)

patch

A special text file that describes changes to code, by identifying the files and lines which are added, removed, and altered. It may also be referred to as a **diff**. A patchpatch A special text file that describes changes to code, by identifying the files and lines which are added, removed, and altered. It may also be referred to as a **diff**. A patch can be *applied* to a codebase for testing. can be *applied* to a codebase for testing. [#](https://make.wordpress.org/core/handbook/glossary/#patch)

PHP

The web scripting language in which WordPress is primarily architected. WordPress requires PHPPHP The web scripting language in which WordPress is primarily architected. WordPress requires PHP 5.6.20 or higher 5.6.20 or higher [#](https://make.wordpress.org/core/handbook/glossary/#php)

PHPDoc

(**docblockdocblock (phpdoc, xref, inline docs)**, **inline docsinline docs (phpdoc, docblock, xref)**) [#](https://make.wordpress.org/core/handbook/glossary/#phpdoc)

point release

A minor releaseMinor Release A set of releases or versions having the same minor version number may be collectively referred to as .x , for example version 5.2.x to refer to versions 5.2, 5.2.1, 5.2.3, and all other versions in the 5.2 (five dot two) branch of that software. Minor Releases often make improvements to existing features and functionality. of WordPress, identified by the third number (the 2 in 3.5.2). These releases are for maintenance and security fixes only. Feature development is limited to major releases. Changes to point releases are carefully considered, and only critical or blockerblocker A bug which is so severe that it blocks a release.\-level bugs, and security enhancements, hardening, and fixes are accepted. [#](https://make.wordpress.org/core/handbook/glossary/#point-release)

priority (bug tracker)

The seriousness of a bugbug A bug is an error or unexpected result. Performance improvements, code optimization, and are considered enhancements, not defects. After feature freeze, only bugs are dealt with, with regressions (adverse changes from the previous version) being the highest priority. report or ticketticket Created for both bug reports and feature development on the bug tracker. in the eyes of the project. Generally, **severityseverity The seriousness of the ticket in the eyes of the reporter. Generally, severity is a judgment of how bad a bug is, while **priority** is its relationship to other bugs.** is a judgment of how bad a bug is, while priority is its relationship to other bugs. [#](https://make.wordpress.org/core/handbook/glossary/#priority-bug-tracker)

priority (hooks)

(higher priority means lower number) [#](https://make.wordpress.org/core/handbook/glossary/#priority-hooks)

punt

Contributors sometimes use the verb “puntpunt Contributors sometimes use the verb "punt" when talking about a ticket. This means it is being pushed out to a future release. This typically occurs for lower priority tickets near the end of the release cycle that don't "make the cut." In this is colloquial usage of the word, it means to delay or equivocate. (It also describes a play in American football where a team essentially passes up on an opportunity, hoping to put themselves in a better position later to try again.)” when talking about a ticketticket Created for both bug reports and feature development on the bug tracker.. This means it is being pushed out to a future release. This typically occurs for lower priority tickets near the end of the release cycle that don’t “make the cut.” In this is colloquial usage of the word, it means to delay or equivocate. (It also describes a play in American football where a team essentially passes up on an opportunity, hoping to put themselves in a better position later to try again.) [#](https://make.wordpress.org/core/handbook/glossary/#punt)

RC

A shortened name for [release candidate](https://make.wordpress.org/core/handbook/glossary/#release-candidate). [#](https://make.wordpress.org/core/handbook/glossary/#rc)

regression

A software bugbug A bug is an error or unexpected result. Performance improvements, code optimization, and are considered enhancements, not defects. After feature freeze, only bugs are dealt with, with regressions (adverse changes from the previous version) being the highest priority. that breaks or degrades something that previously worked. Regressions are often treated as critical bugs or [blockers](#blocker). Recent regressions may be given higher priorities. A “3.6 regressionregression A software bug that breaks or degrades something that previously worked. Regressions are often treated as critical bugs or [blockers](#blocker). Recent regressions may be given higher priorities. A "3.6 regression" would be a bug in 3.6 that worked as intended in 3.5.” would be a bug in 3.6 that worked as intended in 3.5. [#](https://make.wordpress.org/core/handbook/glossary/#regression)

release candidate

One of the final stages in the version release cycle, this version signals the potential to be a final release to the public. Also see [alpha (beta)](#alpha-beta). [#](https://make.wordpress.org/core/handbook/glossary/#release-candidate)

scope creep

The tendency for requirements to increase during a release’s development cycle beyond those originally approved for the upcoming release. Something to be avoided. Also known as feature creep. [#](https://make.wordpress.org/core/handbook/glossary/#scope-creep)

security issue

A security issuesecurity issue A security issue is a type of bug that can affect the security of WordPress installations. Specifically, it is a report of a bug that you have found in the WordPress core code, and that you have determined can be used to gain some level of access to a site running WordPress that you should not have. is a type of bugbug A bug is an error or unexpected result. Performance improvements, code optimization, and are considered enhancements, not defects. After feature freeze, only bugs are dealt with, with regressions (adverse changes from the previous version) being the highest priority. that can affect the security of WordPress installations. Specifically, it is a report of a bug that you have found in the WordPress coreCore Core is the set of software required to run WordPress. The Core Development Team builds WordPress. code, and that you have determined can be used to gain some level of access to a site running WordPress that you should not have. [#](https://make.wordpress.org/core/handbook/glossary/#security-issue)

severity

The seriousness of the ticketticket Created for both bug reports and feature development on the bug tracker. in the eyes of the reporter. Generally, severityseverity The seriousness of the ticket in the eyes of the reporter. Generally, severity is a judgment of how bad a bug is, while **priority** is its relationship to other bugs. is a judgment of how bad a bugbug A bug is an error or unexpected result. Performance improvements, code optimization, and are considered enhancements, not defects. After feature freeze, only bugs are dealt with, with regressions (adverse changes from the previous version) being the highest priority. is, while **priority** is its relationship to other bugs. [#](https://make.wordpress.org/core/handbook/glossary/#severity)

SSL

Secure Sockets Layer. Provides a secure means of sending data over the internet. Used for authenticated and private actions. [#](https://make.wordpress.org/core/handbook/glossary/#ssl)

SVN

Subversion, the popular version controlversion control A version control system keeps track of the source code and revisions to the source code. WordPress uses Subversion (SVN) for version control, with Git mirrors for most repositories. system (VCS) by the ApacheApache Apache is the most widely used web server software. Developed and maintained by [Apache Software Foundation](https://www.apache.org/). Apache is an Open Source software available for free. project, used by WordPress to manage changes to its codebase. [#](https://make.wordpress.org/core/handbook/glossary/#svn)

tag

A directory in Subversion. WordPress uses tags to store a single snapshot of a version (3.6, 3.6.1, etc.), the common convention of tags in version controlversion control A version control system keeps track of the source code and revisions to the source code. WordPress uses Subversion (SVN) for version control, with Git mirrors for most repositories. systems. (Not to be confused with post tags.) [#](https://make.wordpress.org/core/handbook/glossary/#tag)

task (blessed)

Feature development for an upcoming major releasemajor release A release, identified by the first two numbers (3.6), which is the focus of a full release cycle and feature development. WordPress uses decimaling count for major release versions, so 2.8, 2.9, 3.0, and 3.1 are sequential and comparable in scope. centers around task tickets, which are major features or important enhancements that have been blessed by the coreCore Core is the set of software required to run WordPress. The Core Development Team builds WordPress. team. A ticketticket Created for both bug reports and feature development on the bug tracker. should otherwise never receive this designation. [#](https://make.wordpress.org/core/handbook/glossary/#task-blessed)

ticket

Created for both bugbug A bug is an error or unexpected result. Performance improvements, code optimization, and are considered enhancements, not defects. After feature freeze, only bugs are dealt with, with regressions (adverse changes from the previous version) being the highest priority. reports and feature development on the bug tracker. [#](https://make.wordpress.org/core/handbook/glossary/#ticket)

Trac

An open sourceOpen Source Open Source denotes software for which the original source code is made freely available and may be redistributed and modified. Open Source \*\*must be\*\* delivered via a licensing model, see GPL. project by Edgewall Software that serves as a bugbug A bug is an error or unexpected result. Performance improvements, code optimization, and are considered enhancements, not defects. After feature freeze, only bugs are dealt with, with regressions (adverse changes from the previous version) being the highest priority. tracker and project management tool for WordPress. [#](https://make.wordpress.org/core/handbook/glossary/#trac)

translation

The process (or result) of changing text, words, and display formatting to support another language. Also see [localization](#l10n), [internationalization](#i18n). [#](https://make.wordpress.org/core/handbook/glossary/#translation)

triage

The act of evaluating and sorting bugbug A bug is an error or unexpected result. Performance improvements, code optimization, and are considered enhancements, not defects. After feature freeze, only bugs are dealt with, with regressions (adverse changes from the previous version) being the highest priority. reports, in order to decide priority, severityseverity The seriousness of the ticket in the eyes of the reporter. Generally, severity is a judgment of how bad a bug is, while **priority** is its relationship to other bugs., and other factors. [#](https://make.wordpress.org/core/handbook/glossary/#triage)

trunk

A directory in Subversion containing the latest development code in preparation for the next major releasemajor release A release, identified by the first two numbers (3.6), which is the focus of a full release cycle and feature development. WordPress uses decimaling count for major release versions, so 2.8, 2.9, 3.0, and 3.1 are sequential and comparable in scope. cycle. If you are running “trunktrunk A directory in Subversion containing the latest development code in preparation for the next major release cycle. If you are running "trunk", then you are on the latest revision.”, then you are on the latest revision. [#](https://make.wordpress.org/core/handbook/glossary/#trunk)

UI

User interface [#](https://make.wordpress.org/core/handbook/glossary/#ui)

unit test

Code written to test a small piece of code or functionality within a larger application. Everything from themes to WordPress coreCore Core is the set of software required to run WordPress. The Core Development Team builds WordPress. have a series of unit tests. Also see [regression](#regression). [#](https://make.wordpress.org/core/handbook/glossary/#unit-test)

Unprops

A commit that removes code gone awry may include *unpropsUnprops A commit that removes code gone awry may include *unprops* as a sign of respect for the risk taken by the original people working on it.* as a sign of respect for the risk taken by the original people working on it. [#](https://make.wordpress.org/core/handbook/glossary/#unprops)

UX

User experience [#](https://make.wordpress.org/core/handbook/glossary/#ux)

version control

A version controlversion control A version control system keeps track of the source code and revisions to the source code. WordPress uses Subversion (SVN) for version control, with Git mirrors for most repositories. system keeps track of the source code and revisionsRevisions The WordPress revisions system stores a record of each saved draft or published update. The revision system allows you to see what changes were made in each revision by dragging a slider (or using the Next/Previous buttons). The display indicates what has changed in each revision. to the source code. WordPress uses Subversion (SVNSVN Subversion, the popular version control system (VCS) by the Apache project, used by WordPress to manage changes to its codebase.) for version control, with GitGit Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency. Git is easy to learn and has a tiny footprint with lightning fast performance. Most modern plugin and theme development is being done with this version control system. [https://git-scm.com/](https://git-scm.com/). mirrors for most repositories. [#](https://make.wordpress.org/core/handbook/glossary/#version-control)

wontfix

A resolution on the bugbug A bug is an error or unexpected result. Performance improvements, code optimization, and are considered enhancements, not defects. After feature freeze, only bugs are dealt with, with regressions (adverse changes from the previous version) being the highest priority. tracker (and generally common in software development) that indicates the ticketticket Created for both bug reports and feature development on the bug tracker. will not be addressed further. This may be used for acceptable edge cases (for bugs), or enhancements that have been rejected for coreCore Core is the set of software required to run WordPress. The Core Development Team builds WordPress. inclusion. [#](https://make.wordpress.org/core/handbook/glossary/#wontfix)

worksforme

A resolution on the bugbug A bug is an error or unexpected result. Performance improvements, code optimization, and are considered enhancements, not defects. After feature freeze, only bugs are dealt with, with regressions (adverse changes from the previous version) being the highest priority. tracker (and generally common in software development) that indicates the bug reported cannot be reproduced. [#](https://make.wordpress.org/core/handbook/glossary/#worksforme)

wpdevel

Formerly the development updates P2P2 A [free theme for WordPress](http://p2theme.com/), known for front-end posting, used by WordPress for development updates and project management. See our [main development blog](https://make.wordpress.org/core/) and [other workgroup blogs](https://make.wordpress.org/). blogblog (versus network, site) at wpdevel.wordpress.comWordPress.com An online implementation of WordPress code that lets you immediately access a new WordPress environment to publish your content. WordPress.com is a private company owned by Automattic that hosts the largest multisite in the world. This is arguably the best place to start blogging if you have never touched WordPress before. [https://wordpress.com/](https://wordpress.com/). It is now **make/coreCore Core is the set of software required to run WordPress. The Core Development Team builds WordPress.** and resides at [make.wordpress.org/core](https://make.wordpress.org/core/). [#](https://make.wordpress.org/core/handbook/glossary/#wpdevel)

xref

(php-xrefxref (php-xref, phpdoc, inline docs), phpdocPHPDoc (**docblock**, **inline docs**), inline docsinline docs (phpdoc, docblock, xref)) [#](https://make.wordpress.org/core/handbook/glossary/#xref)