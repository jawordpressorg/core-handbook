# JavaScript Docs

This initiative follows the [inline docs initiative](https://make.wordpress.org/docs/handbook/core/inline-docs/) with a specific focus on JavaScript. The goal is to get all JavaScript files in WordPress well documented and make this documentation easily accessible. JavaScript development within WordPress core is speeding up fast and becoming more and more prominent given the current core editor and REST API focuses. To help these developments progress as smoothly as possible, we need to make sure the existing code is documented well.

If you’re not familiar with what inline documentation is, read our page [on inline documentation standards](https://make.wordpress.org/core/handbook/best-practices/inline-documentation-standards/).

## Which JS files should be documented?

There are three pages tracking JS files for documentation:

*   [Unclaimed JS docs files](https://make.wordpress.org/core/2018/01/31/js-docs-initiative-add-inline-docs-for-javascript/): Nobody is working on documenting these files yet. You can claim a file by commenting on the post.
*   [In progress JS docs file tickets](https://make.wordpress.org/core/handbook/docs/inline/js/in-progress-tickets/): These files have patches with documentation or someone is working on creating a documentation patch.
*   [Closed JS docs file tickets](https://make.wordpress.org/core/handbook/docs/inline/js/closed-tickets/): These files have been documented already.

## How to get involved

Inline documentation is considered to be “technical” documentation, so some familiarity with the WordPress codebase will be necessary – you have to understand the code to write about it.

1\. Familiarize yourself with the [JavaScript documentation standard](https://make.wordpress.org/core/handbook/best-practices/inline-documentation-standards/javascript/), as well as the [formatting guidelines](https://make.wordpress.org/core/handbook/best-practices/inline-documentation-standards/php/#formatting-guidelines) and [documenting tips](https://make.wordpress.org/core/handbook/best-practices/inline-documentation-standards/javascript/#documenting-tips).

2\. Set up a local copy of the developer version of the WordPress codebase using [Varying Vagrant Vagrants](https://make.wordpress.org/core/handbook/tutorials/installing-a-local-server/installing-vvv/) (VVV). WordPress is versioning using SVN, but you can also use Git (the VVV link for how to do that).

3\. Read [Opening a Ticket](https://make.wordpress.org/core/handbook/working-with-trac/opening-a-ticket/) to learn how to create a Trac ticket.

4\. Creating patches:

*   [Claim a file to start documenting](https://make.wordpress.org/core/2018/01/31/js-docs-initiative-add-inline-docs-for-javascript/).
*   Always update your local copy of WordPress trunk before editing the file and creating patches. Use `svn up` or `git pull`, as appropriate.
*   Generate the patch from the root directory of your WordPress SVN or Git checkout.
*   It is best to name your patch file with the Trac ticket number you created, such as **12345.patch** or **12345.diff**. Either file extension is acceptable.

5\. How to submit a patch:

*   Create a [new ticket](https://core.trac.wordpress.org/newticket) on Core Trac for the file:
    *   Suggested *Title* formats could be “JSDoc correction for path/to/file.js” or “Improve documentation for path/to/file.js”.
    *   The *Type* should be **defect (bug)**.
    *   Assign the ticket to the *Component* the file is associated with.
    *   Leave the *Version* blank.
    *   Add the **docs** and the **JavaScript** *Focus* by clicking on it.
    *   Here’s a shortcut link to create a new ticket in the `Media` component with the `docs` and `javascript` focuses and the title `JSDocs correction for`, all that is left to add is the filename in the title: [New JSDocs Ticket](https://core.trac.wordpress.org/newticket?component=Media&focuses=docs%20javascript&summary=JSDocs%20correction%20for%20)
*   Upload your patch to the Trac ticket you created, and add the keyword **has-patch**.
*   Make sure to leave a comment describing your newly-uploaded patch. Simply uploading patches doesn’t trigger a notification for anyone watching the ticket.
*   Note: Documentation changes should not mix with code changes (even whitespacing) unless the ticket specifically calls for both.

6\. You can also contribute to [inline docs-related Trac tickets](https://core.trac.wordpress.org/query?status=!closed&focuses=~docs) that need iteration.

*   If a ticket is marked **needs-patch** or **needs-refresh**, it’s possible the existing patch(es) might just need a touch-up or be refreshed against the latest trunk. Every little bit helps!

## Points of contact

For any questions, pop by the [#docs](https://wordpress.slack.com/messages/docs/) channel in [Slack](https://make.wordpress.org/chat/). For JavaScript specific questions, you can also join the [#core-js](https://wordpress.slack.com/messages/core-js/) channel.

## Resources

*   [JS Documentation Standard](https://make.wordpress.org/core/handbook/best-practices/inline-documentation-standards/javascript/)