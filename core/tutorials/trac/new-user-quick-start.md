# New User Quick Start Guide

## Who should use this guide?

If you are a developer who wants to contribute to WordPress core for the first time, this guide is designed to help you navigate and use [Trac](https://make.wordpress.org/core/handbook/contribute/trac/). This is meant as a high level overview to get you started quickly. This page should guide you through some overall knowledge you will need before contributing, the basic steps of working on a ticket and finally the layout of a Trac ticket. We highly encourage you to consult the [core handbook](https://make.wordpress.org/core/handbook/contribute/trac/) and [tutorials](https://make.wordpress.org/core/handbook/tutorials/working-with-patches/) to learn how to use Trac more thoroughly.

We are going to assume you already have a [WordPress.org account](https://login.wordpress.org/register), have thoroughly read [https://core.trac.wordpress.org/](https://core.trac.wordpress.org/), and already have access to the [make.wordpress.org Slack](https://chat.wordpress.org/) workspace, which is where you can ask for guidance and assistance.

## What You Should Know Before Getting Started

### Trac Functionalities

Trac is an open source, web-based project management and bug tracking system. It is used by many parts of the WordPress project, including Core, Meta and Theme Review. Trac is based on working in tickets. Contributors leverage the tool to find tickets in need of work, monitor progress on open tickets, contribute patches for WordPress core.

### How Core Contributors Communicate With Trac

Trac is the official record of work for WordPress core. The tickets written here become part of the living historical document of open source contributions. Because of this, the tone and language used in tickets and comments should be formal and to the point.

Because this is the official record, be sure to search thoroughly to see if there is an existing ticket for the bug or feature you want to log. If something already exists, please add your notes to that existing ticket. If what you have to add is related to an existing item or for something with a finished milestone, reference that ticket using the format #{ticket\_id} to automatically create a link between tickets: “This was previously discussed in [#99999](https://core.trac.wordpress.org/ticket/99999).” If you need to refer to a particular changeset (a set of code changes logged in Trac), you can link to it using the format \[{changeset\_id}\]: “The original bug was fixed in \[999999\].” Note, finished milestone tickets should never be reopened.

Please remember contributors are volunteers and this process takes time. Patience is always appreciated.

## Working On Open Trac Tickets

1.  Find a ticket ready for work by using [https://make.wordpress.org/core/reports/](https://make.wordpress.org/core/reports/)
2.  Check the attachments and see of there is a current patch being suggested.
3.  If no patch exists, time to replicate the scenario and [add a new patch](https://make.wordpress.org/core/handbook/tutorials/working-with-patches/).
4.  If there is a patch, it likely needs to be reviewed and tested, the comments will reveal the current status of things. Download the patch and test in your development environment. If works as expected, please provide appropriate feedback.
5.  If you make changes to the patch, please provide a link to the Diff (https://make.wordpress.org/themes/handbook/review/working-with-trac/#comparing-ticket-updates) as well as comment.
6.  Always leave a comment on the ticket describing what you changed and why you changed it. A patch upload itself does not trigger a notification. Please use \[attachment:{filename}\] in a comment to link to that patch.
7.  Make sure to adjust the keywords as necessary: [https://make.wordpress.org/core/handbook/contribute/trac/keywords/](https://make.wordpress.org/core/handbook/contribute/trac/keywords/)

If a ticket does not already exist for an issue, please open a new ticket: [https://make.wordpress.org/core/handbook/tutorials/trac/opening-a-ticket/](https://make.wordpress.org/core/handbook/tutorials/trac/opening-a-ticket/)

## Ticket Overview

[![Trac Ticket Overview](https://make.wordpress.org/core/files/2018/03/trac-ticket-overview-1024x1024.jpg)](https://make.wordpress.org/core/files/2018/03/trac-ticket-overview.jpg)

Trac Ticket Overview

1.  Ticket ID Number – When commenting please use the format #{ticket\_id} to automatically create a link between tickets.
2.  Type –
    1.  Defect (bug): There’s something wrong and it needs to be fixed.
    2.  Enhancements: An existing feature could use this improvement, like an additional hook or other modification.
    3.  Feature requests: This is a new item not currently represented in WordPress core or another Trac ticket.
    4.  Tasks (blessed): This option won’t appear when filing a new ticket. This status is only given to a ticket if a feature team has accepted it for development (hence, “blessed”).
3.  Milestone – This is set to “Awaiting Review” by default. Once accepted for development, this will be set to the specific version number slated for release. Only [trusted core contributors](https://make.wordpress.org/core/handbook/about/organization/#contributing-developers) can set a milestone.
4.  Severity – normal, major, minor, trivial, critical, or blocker., Only trusted core contributors have the ability to modify the severity.
5.  Component – Which specific part of the project are we working on? For a more detailed definition of each component, please read: [https://make.wordpress.org/core/components/](https://make.wordpress.org/core/components/)
6.  Focuses – Optional when creating a ticket. This indicates if a ticket is relevant to an area that encompasses multiple WordPress components. Options are: ui, accessibility, javascript, docs, rtl, admin, template, multisite, rest-api, performance, coding-standards
7.  Priority – How quickly this issue should be addressed. Options are: normal, low, high, lowest or highest omg bbq. Unless you have discussed a different status with a trusted core contributor, ‘normal’ should be used.
8.  Version (for bugs) – The earliest known version of WordPress affected by this bug. You should not change this.
9.  Keywords – These are like tags, used to track the current status of the ticket and required next steps. This will change as work progresses. For more definition of the available choices, refer to: [https://make.wordpress.org/core/handbook/contribute/trac/keywords/](https://make.wordpress.org/core/handbook/contribute/trac/keywords/)
10.  Description – The heart of the ticket. Please be as thorough and specific as possible. If this is a bug, include steps to reproduce the issue and what you expected to happen.
11.  Attachments – Add additional info, like screenshots, new patches or diff files for patches.
12.  Change History – This is where the conversation happens! This is open by default and you should read it all the way through before you begin work to see what has been tried and what others are actively doing.

## Resources

Printable high resolution of the above infographic are available in [JPG](https://make.wordpress.org/core/files/2018/03/trac-ticket-overview-print.jpg) and [PDF](https://make.wordpress.org/core/files/2018/03/trac-ticket-overview-print.pdf) formats.