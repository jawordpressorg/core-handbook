# Opening a Ticket

## Overview

This article will walk you through the process of opening a ticket on [Trac](https://core.trac.wordpress.org/).

## Getting Started

[Trac](https://make.wordpress.org/core/glossary/#trac) requires that you log in with your WordPress.org account to open a ticket. If you do not have one, you will need to [register for an account](https://wordpress.org/support/register.php) before proceeding.

**Trac Preferences:** You will automatically receive email notifications for tickets you are involved in (you opened the ticket or commented on it). The email account you use for your WordPress.org account is automatically configured in your Trac preferences. You can check your preferences by logging in to Trac, then **clicking the [Preferences](https://core.trac.wordpress.org/prefs) link** at the bottom of the page. You should see the email address these notifications will be sent to when clicking on the *General* tab.

![Trac Preferences General Tab Screen](https://make.wordpress.org/core/files/2013/10/core-trac-preferences-general-tab1.png)

**Are you in the right place?** The information above the ticket form is important – it asks several questions that you need to answer to determine whether your issue is really a bug with WordPress core, a security issue, or a theme/plugin support issue, as well as steps for reporting bugs. It is strongly recommended that you read it before continuing.

**Is there an existing ticket?** Take the time to [search](https://core.trac.wordpress.org/search) for an existing ticket that describes the issue you are having, so you do not create a duplicate ticket. If you find an existing ticket for your issue, leave a comment that you are also experiencing the problem (including details). You can also click the star next to the ticket number in the upper left to watch the ticket if you wish to only receive activity notifications for that ticket.

## Create A New Ticket

Once you have determined your issue really is a bug, and searched for an existing ticket (and found none), it’s time to create a new ticket.

The following is an explanation of the fields to be completed when creating a new ticket. Use the image below as a visual reference for each of the fields.

![Trac Submit Ticket Form Screen](https://make.wordpress.org/core/files/2013/10/core-trac-submit-ticket-form.png)

**1\. Summary:** A brief summary of the issue that describes the problem.

**2\. Description:** A detailed description of the issue. Include steps to reproduce the issue consistently. For bugs, describe the actual versus expected results, and attach a screenshot if you need to visually demonstrate the issue. Describe a possible solution for the issue, if known. For enhancements, you should provide proper rationale for making the change.

**3\. Type:** Tickets fall under one of four types – [defect (bug)](https://make.wordpress.org/core/glossary/#bug), [enhancement](https://make.wordpress.org/core/glossary/#enhancement), [feature request](https://make.wordpress.org/core/glossary/#feature-request), and [task (blessed)](https://make.wordpress.org/core/glossary/#task-blessed).

*   **Defect (bug):** A defect (bug) is an error or unexpected result. After feature freeze, only bugs are dealt with, with regressions (adverse changes from the previous version) being the highest priority.
*   **Enhancement:** These are simple improvements to WordPress, such as the addition of a hook or an improvement to an existing feature.
*   **Feature requests** are proposals for new features, and **tasks (blessed)** are usually created by the core team for development of an approved feature. Most tickets will not have either of these types assigned to them.

**4\. Component:** The component is the area of WordPress that the ticket affects. Try to choose specific components, when applicable, over more generalized ones. **Note:** If the issue is related to the **WordPress.org site**, you will need to file the ticket on [meta.trac.wordpress.org](https://meta.trac.wordpress.org/) instead.

**5\. Version:** The version of WordPress being used. Ideally, this would be the earliest affected or applicable version.

If you have files to include with the ticket (screenshots or a patch), **check the box** next to **I have files to attach to this ticket**.

After completing the above fields, **click Continue To Preview** to ensure that you have included all of the information needed to report the bug. The ticket preview will display directly below the ticket form. Review the information, make any changes necessary, then **click Create Ticket**.

### Attach Files

After creating the ticket, the next step is to attach any files necessary to the ticket, such as screenshots or a patch.

Directly below the ticket detail is the **Attachments** section. **Click Attach File** to add a new file to the ticket.

![Trac Attach Files Screen](https://make.wordpress.org/core/files/2013/10/core-trac-add-attachments.png)

You will be presented with the **Attachment Info** screen.

![Core Trac Upload File Screen](https://make.wordpress.org/core/files/2013/10/core-trac-upload-file.png)

You will then **click Choose File**. A local window will open to locate the file you wish to attach. **Select the file**, then **click OK**. The filename you chose will display.

Next you can add a description of the file. While this is optional, it is helpful to provide more details about the file.

*   Screenshots should use `xxxxx.short-description-of-problem.png` as a filename, where `xxxxx` is the ticket number.
*   Patches should be named `xxxxx.diff` or `xxxxx.patch` – both extensions are acceptable.

For patches, Trac will automatically append an incremental number (`xxxxx.2.diff`) to the end of a patch filename to prevent an accidental overwrite of the existing file, in cases where the same patch is submitted multiple times due to needed changes.

After you have selected the file and provided an optional description, **click Agree and Upload** .

Once the upload is complete, a new comment will be automatically added to the ticket with the filename and description listed.

## Next Steps

*   [Submitting A Patch](https://make.wordpress.org/core/handbook/working-with-trac/submitting-a-patch/)

### Learn More

*   [Ticket Properties](https://make.wordpress.org/core/handbook/trac/#ticket-properties)
*   [Trac Workflow Keywords](https://make.wordpress.org/core/handbook/trac/keywords/)