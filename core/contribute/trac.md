# The Bug Tracker (Trac)

[Trac](https://core.trac.wordpress.org/) is an open source project that serves as a bug tracker and project management tool for WordPress. Using Trac, developers can browse source code history as well as manage bug reports and feature development.

[Tickets](https://make.wordpress.org/core/glossary/#ticket) are used for both bug reports and feature development, and may be created by anyone with a WordPress.org account.

## Ticket Properties

Tickets are assigned numerous properties that provide a snapshot of the status of the ticket.

**Title and Description:** Provide a strong title and clear description. For the title, it is generally best to describe the problem, not a solution. Concentrating on the problem, rather than the solution, is a good mantra in general. For the description, it is generally best to include steps to reproduce, and actual versus expected results (for bugs), and proper rationale (for enhancements).

**Type:** A ticket falls under one of four types: defect (bug), enhancement, feature request, and task (blessed).

*   **Defect (bug):** A bug is an error or unexpected result. Performance improvements and code optimization are considered enhancements, not defects. After feature freeze, only bugs are dealt with, with regressions (adverse changes from the previous version) being the highest priority.
*   **Enhancements:** These are simple improvements to WordPress, such as the addition of a hook or an improvement to an existing feature.
*   **Feature requests:** These are proposals for new features. Feature proposals should generally begin the process in the ideas forum, on a mailing list, as a plugin, or brought to the attention of the core team, such as through scope meetings held for each major release. Unsolicited tickets of this variety are typically, therefore, discouraged.
*   **Tasks (blessed):** Feature development for the upcoming major release centers around task tickets, which are major features or important enhancements that have been blessed by the core team. A ticket should otherwise never receive this designation.

**Milestone:** The milestone is the WordPress release where that ticket is expected to be resolved, such as 3.7. By default, all tickets are assigned, upon creation, to the **Awaiting Review** milestone to prevent [scope creep](https://make.wordpress.org/core/glossary/#scope-creep). Only [committers](https://make.wordpress.org/core/handbook/about/organization/#the-wordpress-core-team) or [trusted core contributors](https://make.wordpress.org/core/handbook/about/organization/#contributing-developers) have the ability to change milestones.

**Keywords:** After the milestone, the keywords field is the most important field. These are not like tags on a WordPress post, but rather a defined list of keywords that describe the ticket’s current status in our development workflow. We use these keywords to build important reports. As an example, tickets tagged with **needs-design-feedback** are pulled into a report on which the Design team heavily relies. See [Trac Workflow Keywords](https://make.wordpress.org/core/handbook/trac/keywords/) for a complete list of the keywords.

**Component:** The component is the area of WordPress that the ticket affects. The UI team, for example, will often be working on tickets in the **Graphic Design**, **UI**, or **Accessibility** categories. Try to choose specific components (when applicable) over more generalized ones, such as **General** or **Administration**. Components are used in reports to provide a logical grouping of tickets by subject area.

Tickets for core plugins, such as the importers, are managed under the **Plugins** or **Import** components, and current and former default themes are managed under the **Bundled Theme** component.

Issues with the WordPress.org site were formerly managed on the same Trac as WordPress core. As of June 2013, [meta.trac.wordpress.org](https://meta.trac.wordpress.org/) is now the proper, canonical place for bug reports to be filed that are related to the WordPress.org site. See the [full components list](https://meta.trac.wordpress.org/#WhatcomponentsfallunderMeta) to determine if your issue should be reported there.

**Resolution:** Upon one or more commits to the codebase, a ticket may be closed as **fixed**. Not all tickets result in a commit, however, and may be closed for other reasons:

*   **duplicate:** The ticket is a duplicate of an existing ticket, which will be referenced by the contributor closing the ticket.
*   **invalid:** The ticket is not a bug, or is a support request.
*   **worksforme:** The bug reported in the ticket cannot be reproduced. Sometimes, an existing plugin, hook, or feature may render the ticket moot, so the ticket can be closed without further action.
*   **wontfix:** The ticket will not be addressed. Occasionally, bugs are considered to be acceptable edge cases, and will not be addressed further. This is sometimes used when a request for an enhancement or feature has been rejected for core inclusion.
*   **maybelater:** Similar to **wontfix**, **maybelater** is used for a ticket that, while perhaps not outright rejected, has no current traction.
*   **reported-upstream:** The ticket is for an external library or component, has been reported in an upstream repository (e.g. Gutenberg), and will be addressed there.

There is certainly some overlap among these five resolutions. It is not an exact science.

**Severity and Priority:** The [severity](https://make.wordpress.org/core/glossary/#severity) is the seriousness of the ticket in the eyes of the reporter. The [priority](https://make.wordpress.org/core/glossary/#priority-bug-tracker) is the seriousness of the ticket in the eyes of the project. Generally, severity is a judgment of how bad a bug is, while priority is its relationship to other bugs. Only [committers](https://make.wordpress.org/core/handbook/about/organization/#the-wordpress-core-team) and [trusted core contributors](https://make.wordpress.org/core/handbook/about/organization/#contributing-developers) have the ability to modify the priority.

**Version:** The version of WordPress being used. Ideally, this would be the earliest affected or applicable version. It should not be updated to a later version once set, as we utilize this to track the age of tickets and bugs, regressions, and the like.

### Roles

Individuals have three roles on Trac tickets:

**Reporter:** The person who opened the ticket.

**Owner:** This field is typically left blank, even if you have contributed a patch. The Owner field is used by committers and trusted core contributors to accept and assign tickets among themselves. Committers utilize the field to offer traction for a ticket, to identify they are investigating, committing, or otherwise following a ticket, or to tentatively accept the bug or enhancement for core inclusion. It is also common during the feature development phase for developers to accept tasks in the area of responsibility for which they have volunteered, as well as related bug reports. Trusted contributors may assign tickets to others based on an inside knowledge of who should be responsible for reviewing it.

**CC:** As long as your email address is [configured in Trac preferences](https://make.wordpress.org/core/handbook/working-with-trac/opening-a-ticket/#getting-started), you’ll receive email updates for any tickets you’ve created or ones you’ve commented on. The field is generally a visual confirmation you are adding yourself to the ticket and wish to receive updates. From time to time, it may make sense to add other individuals to the CC field, such as when a committer requests this. It should be noted that most committers and core developers read every ticket and comment anyway.

## Triaging and Punting

New tickets are automatically assigned to the **Awaiting Review** milestone. Upon initial review, it may be recommended for closure, or require more feedback from the reporter or a core developer. Keywords often used here are **2nd-opinion**, **close**, **reporter-feedback**, and **dev-feedback**.

It may also be moved to a milestone by a committer or trusted core contributor:

*   **The next point release milestone** (for example, 3.6.2 if the current release is 3.6.1) is for critical bugs and regressions. Our point releases are only for security fixes, critical bugs, and regressions in behavior from the previous version of WordPress. We do not fix regular bugs or enhancements in these releases.
*   **The next major release milestone** (for example, 3.7 if the current release is 3.6.1) is for tasks and features slated for the release, bugs affecting those features, and regressions in the current alpha or beta version over the latest release. Existing bugs may also be addressed, but this generally won’t be considered until a solution exists, unless the bug is sufficiently major to warrant priority. Enhancements may also be included at the discretion of committers, but only during alpha development (prior to the beta release). Larger enhancements are generally not considered for the next major release as they are out of scope.
*   **The Future Release milestone** is reserved for other tickets. It’s been determined as a potentially good enhancement or confirmed as a bug, but it is not slated for the next release of WordPress.

### Giving Feedback

When reviewing a ticket, here’s your primary goal: participate in a constructive dialog with the reporter to get the ticket to some form of resolution. The resolution doesn’t need to be immediate, although it’s fun when it is – slow and steady progress is the name of the game. If you’re new to this, here’s some tips on how you might approach and handle a ticket.

When giving feedback for a ticket:

*   Thank the individual for the report. Some of these tickets are quite old; for those, a simple “Thanks for the report nacin. Sorry you never got a response.” is fine.
*   If this was one of the reporter’s first tickets, it will tell you above the comment box. Be nice. 🙂
*   If it’s a support request, you can refer them to the WordPress.org support forums and close the ticket as “invalid”.
*   If it’s a bug report that sounds like an enhancement, then change the ticket to an enhancement. Enhancements are a bit more difficult to triage (as the feedback is more subjective), so it’s much easier to start with bugs.
*   Consider a quick search to see if it is a duplicate of another ticket that may be farther along.
*   If there’s a component that is more appropriate for the ticket, feel free to move it.

If it’s a bug report:

*   See if you can still reproduce it in trunk, and/or try the latest stable release. Some bug reports may have been invalid to begin with; others might have been fixed already.
*   If, when reproducing it, you feel you can elaborate on the issue, or write clearer steps to reproduce, please do so.
*   If you can’t reproduce it, ask the reporter for more information and add the **reporter-feedback** keyword. If you think the ticket should be closed, you can mark it with the **close** keyword. (There doesn’t need to be a rush to close the ticket.)
*   Reproducible bugs need patches (and unit tests, if applicable)!

If it has a patch:

*   Test it out – does it fix the problem? How did you test it? Did you notice any side effects?
*   If the patch doesn’t apply cleanly (as in, it fails when you try), add the **needs-refresh** keyword.
*   If you’re a developer, consider doing even just a cursory code review. Make sure it follows [WordPress coding standards](https://make.wordpress.org/core/handbook/coding-standards/).
*   If the **has-patch** workflow keyword is missing, add it. Or, if after review you don’t find the patch to be sufficient, you can set it to **needs-patch** instead.
*   If the patch touches on any WordPress internals, it probably needs [unit tests](https://make.wordpress.org/core/handbook/automated-testing/).
*   If you feel the patch is ready to be reviewed by a core developer to be considered for inclusion in WordPress, simply say so in a comment. Up until beta 1, you can file it against the current milestone. After beta 1, file it against **Future Release** with an **early** tag.

It might take only a few minutes to triage some of the more straightforward tickets, especially once you get the hang of it. You could easily spend twenty or thirty minutes on others, or even longer if there’s a lot to test or if you have a lot of feedback to give.

If you come across a ticket you like and want to write a patch for it, that’s great! Feel free to leave feedback on the ticket and start working on a patch.

Triaging can be a great way to find tickets that interest you. You might find yourself timid to start – if so, find a buddy in [#core](https://wordpress.slack.com/messages/core/) and work collaboratively until you get comfortable.

### Punting Tickets

Tickets are *punted* when they are moved out of a minor or major release milestone to a future milestone. This generally happens at different intervals in the cycle to lower priority tickets. Some tickets are individually deemed as too complex or out of scope, and are therefore moved.