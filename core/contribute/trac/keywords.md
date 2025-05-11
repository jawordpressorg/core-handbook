# Trac Workflow Keywords

There are a number of **keywords** with a defined meaning. These are commonly used to manage the workflows of specific tickets, as well as releases, and to generate reports. Keywords should not be thought of as generic “tags,” which are not necessary.

## Status-based Keywords

**changes-requested**

Feedback has been provided, and the attached patch needs to be updated.

**close**

The ticket is a candidate for closure with a disposition other than fixed (i.e. **wontfix**, **worksforme**, **invalid**, or **duplicate**). Often seen with **reporter-feedback** or **2nd-opinion**; otherwise, the ticket would have been closed in lieu of adding the **close** keyword.

**early**

This keyword should only be applied by committers. The keyword signals that the ticket is a priority, and should be handled early in the next release cycle.

**good-first-bug**

This keyword signals that the ticket would be a good starting point for new contributors to get used to the process before tackling more complicated tickets.

**has-patch**

A proposed solution to the ticket has been attached, and it is ready for review.

**has-screenshots**

Serves as a partner to *needs-screenshots*. Once a ticket has at least one screenshot, tag it with has-screenshots. If more screenshots are needed, leave needs-screenshots on the ticket until all screenshots are provided. [#has-screenshots](https://core.trac.wordpress.org/query?status=accepted&status=assigned&status=closed&status=new&status=reopened&status=reviewing&keywords=~has-screenshots&col=id&col=summary&col=status&col=owner&col=type&col=priority&col=milestone&col=changetime&order=priority) is used to create visual changelogs and the [Today in the Nightly](https://make.wordpress.org/core/tag/today-in-the-nightly/) posts. Do not clear this tag from closed tickets. has-screenshot and needs-screenshots are part of the post-commit diligence lifecycle and are expected to exist on closed tickets. need-screenshots exists temporarily until all screenshots are provided and has-screenshots exists permanently.

**has-unit-tests**

The ticket has been reviewed, found to be desirable to solve, and the latest patch contains unit tests. Like *needs-unit-tests*, this keyword indicates the proposed changes constitute a high risk of causing other issues.

**needs-codex**

Documentation in the Codex needs updating or expanding. Remove the keyword from the ticket once the Codex is updated.

**needs-docs**

Inline documentation for the code is needed. These are either place holder tickets for individual files, or tickets with patches for new functions which need documenting before they are committed.

**needs-patch**

The ticket has been reviewed, found to be desirable to solve, and marked as especially needing a patch, or the submitted patch doesn’t work and needs to be redone.

**needs-refresh**

A submitted patch no longer applies cleanly to the WordPress core files, usually because nearby code has been modified since the patch was submitted. The patch needs to be merged and re-submitted.

**needs-screenshots**

Patches and commits that change UI need screenshots. Document visual iterations. Upload screenshots directly to the ticket or post to [make/flow](https://make.wordpress.org/flow/) for more involved visual documentation such as visual records or visual surveys. Cross-link any make/flow posts with the ticket. Remove the needs-screenshots keyword from the ticket once screenshots for both a desktop and a phone, at the least, are provided. Full context screenshots taken on physical devices are preferred. New patches require new screenshots. Once a ticket has at least one of the needed screenshots, tag it with has-screenshots. [#needs-screenshots](https://core.trac.wordpress.org/query?status=accepted&status=assigned&status=closed&status=new&status=reopened&status=reviewing&keywords=~needs-screenshots&col=id&col=summary&col=status&col=owner&col=type&col=priority&col=milestone&order=priority)

**needs-unit-tests**

The ticket has been reviewed, found to be desirable to solve, and we would like some unit tests written to test the functionality and any patch that may exist before committing a change, as the risk of causing other issues is high.

**phpNN**

When paired with the `php-compatibility` focus, this manually added keyword identifies the specific PHP version (i.e. `NN`) that first introduced a compatibility issue or task. For example, `php80` keyword identifies that PHP 8.0 is the version that first introduced the incompatibility.

## Action-based Keywords

**2nd-opinion**

Another person is needed to express an opinion about the problem or the solution.

**commit**

The patch has been reviewed and tested by a trusted member of the development community; therefore, the patch should be considered a commit candidate, and is ready to be added to the WordPress core files.

**dev-feedback**

A response is wanted from a [core developer](https://make.wordpress.org/core/handbook/about/organization/#the-wordpress-core-team) or trusted members of the development community. For example, use this keyword when double sign-off is required to [backport changes during RC](https://make.wordpress.org/core/handbook/best-practices/backporting-commits/#backport-process).

**dev-reviewed**

After a branch has been created for a release, each change (except for build and test suite changes) needs to be reviewed by two permanent committers. The first reviewer should set the keywords “commit dev-feedback”, and the second reviewer should set the keywords “commit dev-reviewed”. If a permanent committer created the patch, only one additional review is necessary.

**fixed-major**

Only used late in the development cycle (after a branch has been created for a release) to indicate that an issue has been “fixed” in the next “major” version (trunk) and needs to be merged back to the branch for the upcoming release by a permanent committer.  (There is also “fixed-minor” which indicates that an issue needs to be merged back into trunk from a minor release branch; more info about these keywords in this post: [The keywords “fixed-major” and “fixed-minor”](https://make.wordpress.org/core/2011/04/06/the-keywords-fixed-major-and-fixed/).)

**has-copy-review**

Input has been given from a copywriter reviewing the suggested verbiage changes.

**has-dev-note**

A [dev note](https://make.wordpress.org/core/tag/dev-notes/) has been published on the make core blog outlining this change. This change provides significant new functionality, a large refactor, or includes a breaking change.

**has-privacy-review**

Input has been given from the [core privacy team](https://make.wordpress.org/core/components/privacy/) reviewing the privacy implications of the suggested changes.

**i18n\-change**

Only used late in the development cycle (after string freeze) to track potential string changes, as translators need to be notified.

**needs-copy-review**

Input is needed from a copywriter with regards to the suggested verbiage changes.

**needs-design**

A designer should create a prototype of how the suggested changes should look/behave before writing code.

**needs-design-feedback**

A designer should review and give feedback on the proposed changes.

**needs-dev-note**

This change is one that warrants a [dev note](https://make.wordpress.org/core/tag/dev-notes/) on the make core blog. If a change is significant new functionality, a large refactor, or includes a breaking change, it always requires a dev note.

**needs-privacy-review**

Input is needed from the [core privacy team](https://make.wordpress.org/core/components/privacy/) with regards to the privacy implications of the suggested changes.

**needs-testing**

One or more people are needed to test the solution. When testing a patch, please comment with the patch filename that was tested, how the patch was tested, and which version of WordPress was used (including the SVN revision number, if it is not an officially released version).

**reporter-feedback**

A response is needed from the reporter. Further investigation is unlikely without a response to the questions from someone experiencing the problem.