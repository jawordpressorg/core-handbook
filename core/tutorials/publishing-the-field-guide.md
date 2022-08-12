# Publishing the Field Guide

The Field Guide is published on [Make/Core](https://make.wordpress.org/core/) and highlights the developer-focuses changes in a major release. Ideally all new and modified hooks are noted in a bulleted list (e.g., [4.8](https://make.wordpress.org/core/2017/05/26/wordpress-4-8-field-guide/)).

Start drafting the Field Guide early in the release cycle (generally around Beta 1) and slowly embed [dev notes](https://make.wordpress.org/core/handbook/tutorials/writing-developer-notes/) as they get published. A week or so before Release Candidate 1 you will want to reserve 2-4 hours to work on copy, formatting, link updating and other tweaks to have the first real draft of the Field Guide ready. Around this time you will want to send the Slack group direct messages to Component Maintainers to give them all a couple days to provide feedback on the bullet points in the `But Wait, There Is More` section. At the same time you will want to obtain reviews from others on the release squad so that all feedback completes around the same time and allows publishing the Field Guide as close to RC1 as possible.

The following is a general process that the Release Coordinator and/or Documentation Lead will use to craft the Field Guide for a release:

*   Copy previous release Field Guide (e.g. [5.6](https://make.wordpress.org/core/2020/11/20/wordpress-5-6-field-guide/)), rename and update copy to current release version number
*   Update all links to point to current release version number
*   Remove previously embedded dev notes
*   As new dev notes for the current release cycle get published, embed them in the respective section of the Field Guide
*   Update the Field Guide heading with the major focuses from the release
*   Update section listings to relate to areas receiving dev notes
*   Add/update section summary pulling major highlights from embedded dev notes to help developers know whether those dev notes are relevant to them or not
*   Each Component team is sent a group direct message in Slack, pulling the list of maintainers from the [individual component pages](https://make.wordpress.org/core/components/):

> It’s that time again `Component Name` component maintainer(s)… are there any tickets in the X.Y release that you’d like called out in the Field Guide that aren’t already included in a Dev Note? As a reference, here are the ## tickets currently in the milestone for you: [https://core.trac.wordpress.org/query?component=ComponentName&milestone=X.Y&col=id&col=summary&col=milestone&col=owner&col=type&col=status&col=priority&order=priority](https://core.trac.wordpress.org/query?component=ComponentName&milestone=X.Y&col=id&col=summary&col=milestone&col=owner&col=type&col=status&col=priority&order=priority). Note that we intend to publish the Field Guide next week, so the sooner you can respond the better… thanks!

*   The responses are added into the `But Wait, There is More!` section of the Field Guide as individual bullet items in the format of:
    *   Component Name: Trac Ticket Summary ([#Trac-Number](https://make.wordpress.org/core/tag/trac-number/)).

Find at least one reviewer from the release squad, but ideally one technical review and one marketing/copy review, to ensure the Field Guide is as well-written as possible within your timeframe. From there it’s published with the version number “X-Y” and “field-guide” tags.