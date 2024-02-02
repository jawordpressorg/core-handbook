# Leading Bug Scrubs

Ensuring tickets move towards a resolution is one of the most important aspects of maintaining the WordPress project. Bug Scrubs serve as one of the ways to make this happen.

Bug Scrubs can have a general focus, focus on a specific component, or focus on a specific report (such as ancient tickets).

Want to learn more? Here is a list of “Potentially Asked Questions”.

### Who can run a Bug Scrub?

You! Leading a Bug Scrub is something **any** interested community member can do.

### What is a Bug Scrub?

Bug Scrubs are set and announced meetings where the goal is to go through a list of tickets and move them towards a resolution. They are also something where anyone is welcome to run them!

### Where do I get a list of tickets for my Bug Scrub?

There are many [pre-generated reports](https://make.wordpress.org/core/reports/) that you can use, such as:

*   specific component reports such as for [Bootstrap/Load](https://core.trac.wordpress.org/component/Bootstrap/Load)
*   focus oriented ones such as for [JavaScript](https://core.trac.wordpress.org/focus/javascript)
*   [all tickets requesting dev feedback](https://core.trac.wordpress.org/tickets/dev-feedback)

You can also create a custom query. For example, here’s one for [defects discussed during the last cycle that don’t have a resolution yet](https://core.trac.wordpress.org/query?status=accepted&status=assigned&status=new&status=reopened&status=reviewing&changetime=04%2F12%2F16..08%2F16%2F16&type=defect+(bug)&col=id&col=summary&col=status&col=owner&col=type&col=priority&col=milestone&order=priority).

### What does it mean to move tickets towards a resolution?

There are a number of possible resolutions to a ticket. Moving a ticket towards a resolution might involve:

*   Pinging a specific person for feedback/information
*   Reviewing a patch and providing feedback on it
*   Adding a new keyword to a ticket

Almost always, it should include a summary of the discussion.

### How many tickets should be reviewed in a Bug Scrub?

There is no magic number for Bug Scrubs. It is entirely up to the organizers.

Bug Scrubs work best when they have a specific end goal. This may be a number of tickets or this may be a time period. Generally, 1 hour is a good amount of time and no more than 5 minutes is enough for each ticket.

### How do I run a Bug Scrub?

Let’s walk through the steps:

1.  At the start of the scrub, you should:
    *   Announce it by opening the Bug Scrub `<bug-scrub>` tag and welcoming people
    *   Then link to the list of tickets you will be going through. This list should either be a pre-existing report on Trac or a query that you generate.
2.  Then post the first ticket for discussion. Make sure to mention it via number or a link so that slack auto posts a link so someone can see this ticket was discussed.
3.  Then take a moment to review the ticket and discuss what it needs to move forward. You may call for volunteers for specific tasks.
    *   Tip: Sometimes cutting off discussion and moving it back to the ticket with some summary of thoughts makes the most sense. That’s a decision you need to make, though anyone should feel free to suggest it.
4.  Finally, make sure one person is responsible for updating the ticket with whatever decision is made.
5.  Repeat steps 2-4 for the next ticket on the list.
6.  When done, make sure to close `</bug-scrub>` and thank everyone who helped.

### What do I need to organize a Bug Scrub?

You’ll need:

*   An internet connection
*   An account on both WordPress.org and [wordpress.slack.com](https://wordpress.slack.com/) ( which you can get through [https://make.wordpress.org/chat/](https://make.wordpress.org/chat/) with your WordPress.org account)
*   A willingness to devote some time to help WordPress 

You don’t need to be:

*   A core committer or someone that would be called a “core dev” (whatever that means) to lead a Bug Scrub.
*   A developer at all. Designers, project managers, QA engineers, and product managers can be great Bug Scrub leaders.

People that are successful at running Bug Scrubs are people that can communicate well and are familiar with [the trac workflow](https://make.wordpress.org/core/handbook/contribute/trac/) and [how WordPress uses keywords on trac](https://make.wordpress.org/core/handbook/contribute/trac/keywords/).

Running a Bug Scrub involves [Bug Gardening](https://make.wordpress.org/core/handbook/testing/bug-gardening/), so a tester mindset and understanding users helps as well.

### I want to lead one, what do I need to do?

Awesome! Thank you!

You are welcome to schedule a scrub at any time. You will get the most attendees by ensuring it is announced and publicized in advance. Three ways to ensure that happen are: pinging the Core Triage lead for the current release, announcing it during the Core Dev chat open floor time, or by commenting on the Core Dev chat agenda/summary posts with your interest.

Have the report or list of tickets that you want to go through in mind, and someone will make sure your scrub is scheduled in the most appropriate Slack room.

Most scrubs will happen in the [#core](https://make.wordpress.org/core/tag/core/) room, though some components have their own rooms where it makes sense to hold the scrub.

If you are new to leading bug scrubs, you can be paired up with an experience scrubber to help guide you through the process!

### What should I do if a ticket won’t realistically get completed in its “milestoned” release?

If a ticket will not likely be completed in a timely manner for a given release, you will want to “punt” it from the milestone. The best approach is to change the milestone to `Future Release` and not the next major or minor release as this typically ends up with a large amount of open tickets rolling over from release to release. “Punting” them to `Future Release` allows component maintainers and people particularly passionate about the issue to purposefully, intentionally milestone it for a release.

### What if no one else shows up?

This sometimes happens and is fine. It just means you end up publicly sharing your thoughts on how to move a ticket forward. Sometimes people will start to chime in once they see someone being active.

An active bug tracker is one sign of a healthy project. Help ensure the health of WordPress by running a Bug Scrub.

*This page is a modified version of the [Bug Scrubs for 4.7](https://make.wordpress.org/core/2016/08/25/bug-scrubs-for-4-7/) post on [Making WordPress Core](https://make.wordpress.org/core/). Props to @jorbin for writing that post.*