# FAQ for New Contributors

This Frequently Asked Questions list comes from questions that new Core contributors ask in *New Contributors Meetings*.

Look for the list to grow over time as more questions get asked and answered.

## How do I get started?

There’s a lot of documentation out there. You’ll want to get a sense of what it covers and where the various parts and pieces live, start by going through it with an eye toward figuring out where things are, how they’re structured and what the topics are that particularly appeal to you.

You’ll probably forget the details, but you’ll know you can find things again with a search. Go ahead and bookmark those pages for further reference.

You’ll also want to set up Slack and join a few channels.

Start going to the [scheduled meetings](https://make.wordpress.org/meetings/) just to get an idea of how things get done:

*   what each group talks about,
*   what gets a lot of attention across groups and, therefore,
*   what the priorities are.

You also will want to go through the posts on [Make WordPress Core](https://make.wordpress.org/core/) to read meeting summaries from a while back, for context and to see how things get priority. Along with your other reading, you’ll start to get an idea of what the focus areas are and where you’d like to focus your time.

## Are there specific people who can help me get started?

There are. [@desrosj](https://profiles.wordpress.org/desrosj/), [@flixos90](https://profiles.wordpress.org/flixos90/), [@adamsilverstein](https://profiles.wordpress.org/adamsilverstein/), [@welcher](https://profiles.wordpress.org/welcher/), [@audrasjb](https://profiles.wordpress.org/audrasjb/), [@costdev](https://profiles.wordpress.org/costdev/), [@mike](https://profiles.wordpress.org/mike/), [@oglekler](https://profiles.wordpress.org/oglekler/), and [@SergeyBiryukov](https://profiles.wordpress.org/SergeyBiryukov/) run the New Core Contributors Bimonthly Chats on Slack; plan to start going to a few. The schedule is on [Make/Meetings](https://make.wordpress.org/meetings/), and they’ll welcome your questions.

You can also ping them on Slack. If you have questions after a meeting, or you have a question you’d rather not ask publicly, you’re more than welcome to ping them throughout the week.

## Given that most tickets already have a patch submitted, where should I start on Trac?

It’s true that some tickets already have patches.

But patched rarely means finished. Generally, patches need review and feedback from other contributors. And from [component](https://make.wordpress.org/core/components/) maintainers.

Sometimes a first patch takes significant edits. Sometimes you might see multiple patches at the same time, iterating on a solution or exploring a variety of approaches.

That’s why you see tickets that already have a patch, and why we don’t just automatically commit them. They still need testing, plus all those reviews and feedback we just mentioned. In fact, testing an existing patch and giving feedback is an excellent way for you to get involved, and a critical step in the process that moves them forward.

So once you’ve done your thing, whether patching or testing or reviewing, how do you get more eyes on a ticket?

The ticket comments are your best friend. When you leave a comment, the ticket automatically pings everyone on the ticket: its owner, people who are watching the ticket and, best of all, one or more relevant component maintainers. And they have every interest in the world in getting that ticket committed and merged – it’s what we do as contributors to WordPress.

You can also bring it up in [#core](https://wordpress.slack.com/archives/C02RQBWTW) on Slack any time outside of any ongoing meeting (or in the open floor section of the weekly dev meeting).

## Are there specific priorities or components that need more help than others? Where can I help the most?

Start with the list of [good first bugs](https://core.trac.wordpress.org/tickets/good-first-bugs) in core or [good first issues](https://github.com/WordPress/gutenberg/contribute) in Gutenberg.

These are well-contained tasks designed to help you get familiar with WordPress core code, processes and contributing. And they likely won’t send you down a rabbit hole.

If nothing catches your eye on that list, start looking at the [tickets marked as needs-patch, needs-testing, needs-design, or needs-design-feedback](https://core.trac.wordpress.org/query?status=!closed&keywords=~good-first-bug&keywords=~needs-patch&keywords=~needs-testing&keywords=~needs-design&keywords=~needs-design-feedback&group=milestone&order=priority) in the current milestone. They have a higher priority and need the most attention.

You can run a query for tickets with no patch: [https://core.trac.wordpress.org/tickets/no-patch](https://core.trac.wordpress.org/tickets/no-patch)

## How can I get involved with Bug Gardening? Can I pick any ticket that seems interesting?

Bug Gardening is a great way to contribute. And, yes. Feel free to pick any ticket that seems interesting.

Do start by reading the [handbook entry on Bug Gardening](https://make.wordpress.org/core/handbook/testing/bug-gardening/).

There’s a Triage Team that’s looking for contributors. Its mission is to go through every open ticket in Trac to review and triage each one, aiming to lower the absolute number of tickets in the short term and keep that number low going forward.

Some recommended reading on that:

*   [Introducing the WordPress Triage Team](https://make.wordpress.org/core/2019/03/01/introducing-the-wordpress-triage-team/)
*   [Triage Team Meeting Summary – March 11, 2019](https://make.wordpress.org/core/2019/03/13/triage-team-meeting-summary-march-11-2019/)
*   [WordPress Triage Team: A 3 Month Reflection](https://jonathandesrosiers.com/2019/06/wordpress-triage-team-3-month-reflection/)

## While I browsed Trac, I replied to some tickets. Where can I find them again?

Bookmark this: [https://core.trac.wordpress.org/my-comments](https://core.trac.wordpress.org/my-comments)

## How do core maintainers choose what goes into a next release?

Generally, the release leads and component maintainers have some tasks they would like to prioritize for the release. For reference, [see the proposed scope for 5.4](https://make.wordpress.org/core/2020/01/14/wordpress-5-4-planning-roundup/).

Plus, from Trac, we merge a lot of small bug fixes and enhancements across every component.

Also, in the earliest weeks, there’s an [open call for tickets](https://make.wordpress.org/core/2019/12/04/wordpress-5-4-open-call-for-tickets/) so teams can get a better idea of what’s important to the community. Then, component maintainers and committers go over the results and add tickets that make sense, based on the overall priorities of the release.

## What do all those keywords on the tickets mean? What are they for?

See [Trac workflow keywords glossary](https://make.wordpress.org/core/handbook/contribute/trac/keywords/).

## How do I make patches with Git?

See these articles for more information on creating patches with Git:

*   [The Code Repository (Git)](https://make.wordpress.org/core/handbook/contribute/git/)
*   [Contributing To WordPress (Using Git)](http://scribu.net/wordpress/contributing-to-wordpress-using-github.html)
*   [Contributing to WordPress using Git and GitHub PRs](https://make.wordpress.org/core/handbook/contribute/git/github-pull-requests-for-code-review/)

Find out more on the [Contributing with Code Handbook page](https://make.wordpress.org/core/handbook/contribute/).

## How should I name my patches?

If there are other patches on the ticket, add a numeric increment to your version, separated with a dot. Otherwise, name your patch after the ticket number.

For example, if your patch is the first for ticket 12345, name your file 12345.diff. If there are 2 other patches, name your file 12345.2.diff.

If you want, you can include a very shortened purpose to your filename.

## Where can I learn more about working with Trac?

See the related [Core Handbook Page](https://make.wordpress.org/core/handbook/tutorials/trac/new-user-quick-start/).

Also, check the [bug scrub schedule](https://make.wordpress.org/core/2020/01/20/bug-scrub-schedule-for-5-4/) and go to some scrubs. You’ll learn a lot by doing!
