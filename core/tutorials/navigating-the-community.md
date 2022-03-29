# Navigating the Community

## Introduction:  

Before digging in, it might help to review the rest of the [Core Contributor Handbook](https://make.wordpress.org/core/handbook/). In particular, you might find the tutorials for [setting up your local environment helpful](https://make.wordpress.org/core/handbook/#tutorials-guides). Much of what’s shared in the rest of the handbook sets the foundation for what’s shared here. Separately, to help join the fun more directly, it’s strongly encouraged that you set up a [WordPress.org slack profile](https://make.wordpress.org/chat/). After you do so, you can participate in more community efforts including the twice per month new contributor meeting in [#core](https://make.wordpress.org/core/tag/core/). You can find all the meetings listed [here](https://make.wordpress.org/meetings/). Hope to see you there!

## Structure of WordPress.org Development

Keep in mind that if you want to read and learn more, there are various handbooks that you can read through, including the [Core Contributor Handbook](https://make.wordpress.org/core/handbook/) which has helpful resources like [common design decisions](https://make.wordpress.org/core/handbook/contribute/design-decisions/) that tend to come up frequently. 

**Release cycles**

[Gutenberg releases an update](https://github.com/WordPress/gutenberg/releases) every two weeks, whereas [WordPress core operates on a more spread out release cycle](https://wordpress.org/about/roadmap/). This can make keeping up with what Gutenberg versions are present in WordPress releases confusing, but [this page documenting what versions are present](https://developer.wordpress.org/block-editor/principles/versions-in-wordpress/) in each WordPress release should help!

**Contributors, Committers, Components, Component Maintainers, and Teams**

These terms listed above are all WordPress core specific and are used to describe the different roles people take on to move the project forward. To start, a contributor is simply someone who contributes to the WordPress project, whether with code, designs, documentation, etc. 

[Committers are](https://make.wordpress.org/core/handbook/contribute/#committers) “a type of WordPress contributor who has earned the community’s trust and been given the keys to “commit” code to WordPress core.” These are the people who play a leading role in making final decisions with WordPress Core.

[Components are defined](https://make.wordpress.org/core/components/) as “well-defined, functional areas of Core” that contributors can help get involved with. Component Maintainers are contributors who take on a logistical stewardship role for each component. You can read more specifically [about this role in this post](https://make.wordpress.org/core/2020/02/09/what-does-it-mean-to-be-a-component-maintainer-a-refresher/). 

There are also teams that exist on top of the component teams. You can find each team along with ways to get involved listed [here](https://make.wordpress.org/). They include [Core](https://make.wordpress.org/core/), [Mobile](https://make.wordpress.org/mobile/), [Design](https://make.wordpress.org/design/), [Accessibility](https://make.wordpress.org/accessibility/), [Polyglots](https://make.wordpress.org/polyglots/), [Support](https://make.wordpress.org/support/), [Documentation](https://make.wordpress.org/docs/), [Themes](https://make.wordpress.org/themes/), [Plugins](https://make.wordpress.org/plugins/), [Community](https://make.wordpress.org/community/), [Meta](https://make.wordpress.org/meta/), [Training](https://make.wordpress.org/training/), [Test](https://make.wordpress.org/test/), [TV](https://make.wordpress.org/tv/), [Marketing](https://make.wordpress.org/marketing/), [CLI](https://make.wordpress.org/cli/), [Hosting](https://make.wordpress.org/hosting/), and [Tide](https://make.wordpress.org/tide/). 

Finally, Gutenberg [has two separate teams](https://github.com/WordPress/gutenberg/blob/66b5777439abb510c7dfea9e513a7a73423d4ef3/docs/contributors/repository-management.md#teams): 

*   [Gutenberg Core](https://github.com/orgs/WordPress/teams/gutenberg-core/members): A team composed of people that are actively involved in the project: attending meetings regularly, participating in triage sessions, performing reviews regularly, working on features and bug fixes, and performing plugin and npm releases.
*   [Gutenberg](https://github.com/orgs/WordPress/teams/gutenberg/members): A team composed of contributors with at least 2–3 meaningful contributions to the project.

## Key Community Topics

These topics are ones that you might find will cause a lot of conversation and differing perspectives. Keep in mind that this doesn’t mean you shouldn’t try to engage with them! This is just a note to help give context for why some topics create more traction than others. This is not an all-encompassing list and is time-dependent based on what’s happening in the project as this is written.

**Keeping up with Gutenberg and Core**

Gutenberg development occurs in GitHub whereas Core WordPress development is [managed in Trac](https://core.trac.wordpress.org/). Because of the different tooling, naming, and release cycle, it’s created a feeling of separation between Gutenberg and Core to the point that [it can be difficult to distinguish between the two](https://make.wordpress.org/core/2020/07/25/open-agenda-item-core-privacy-and-gutenberg/#comment-39137).  

*Recommendation: depending on how large a change or idea is, remember that you might need to do more to raise awareness and share earlier than you might think to help more people have the chance to be well informed.* 

**Where does Gutenberg begin and Core start?**

Because [versions of Gutenberg plugin are included in each WordPress release](https://developer.wordpress.org/block-editor/principles/versions-in-wordpress/) and the editor experience has become quite incorporated into WordPress core, it can be difficult to distinguish between the two. As a result, you might be digging into one area only to find the solution that needs to be implemented elsewhere. Ultimately, keep in mind that Gutenberg is part of WordPress Core so the answer to this specific question is moot.

**Approaching accessibility (aka a11y)** 

Accessibility is an important part of development within Gutenberg and WordPress. You can find the [WordPress’ accessibility statement here](https://wordpress.org/about/accessibility/) for more context. As you’ll find, [Web Content Accessibility Guidelines (WCAG)](https://www.w3.org/WAI/standards-guidelines/wcag/) are often referenced as a result when it comes to making decisions and it’s recommended you review them. 

Thankfully, there’s an accessibility team that is dedicated to helping share best practices here and to help interpret those guidelines. To get the accessibility team’s attention, there are a11y labels to use as well as [weekly accessibility meetings](https://make.wordpress.org/meetings/) anyone can join. When in doubt, it’s best to flag items for review as a11y at large in the wider tech industry is typically sidelined and it’s important to include the team early.

*Recommendation: Join [#accessibility](https://make.wordpress.org/core/tag/accessibility/) in slack, sign up to receive* [*https://a11yweekly.com/*](https://a11yweekly.com/)  *or* [*https://a11y.coffee/*](https://a11y.coffee/) *newsletters, be sure to proactively label issues/PRs as you can for a11y help, and get a* [*basic understanding of WCAG*](https://www.w3.org/WAI/standards-guidelines/wcag/)*.* 

  
**The balance between sponsored contributors vs volunteers**

Within the community, there are sponsored contributors and volunteers who do this work in their free time. For sponsored contributors, this means you can often keep up with more, move faster, and contribute more. As a result, if you are a sponsored contributor, it makes following the community norms even more important as that often allows more people to participate no matter their time commitment. 

On the flip side, if you’re doing this as a volunteer, remember to be kind to yourself and never feel pressure to try to achieve the level of contribution of those who are sponsored full time. Find sustainable ways to give back that will allow you to do so for many months and years to come. 

## Explanation of Community Slack Channels & Make Blogs:

**Slack Channels**

What follows is a purposefully incomplete list that focuses mainly on the key slack channels you might find helpful. Feel free to explore more!

[#accessibility](https://make.wordpress.org/core/tag/accessibility/): for discussion accessibility related items. 

[#core](https://make.wordpress.org/core/tag/core/): for discussing Core WordPress. 

[#core-editor](https://make.wordpress.org/core/tag/core-editor/): for discussing the Block Editor aka Gutenberg. 

[#core-js](https://make.wordpress.org/core/tag/core-js/): for discussing all things JS in WordPress.

[#docs](https://make.wordpress.org/core/tag/docs/): for discussing and working on documentation efforts including developer docs.

[#design](https://make.wordpress.org/core/tag/design/): for discussion design related items. 

[#core-themes](https://make.wordpress.org/core/tag/core-themes/): for discussing themes including block-based themes. 

**Make Blogs**

The Make blogs are individual blogs focused on specific themes built around the teams involved in WordPress. This list is purposefully focused on the main ones you might interact with as a developer: 

*   [WordPress News](https://wordpress.org/news/): a blog specific for announcements (ex: WordPress releases)
*   [Make Core](https://make.wordpress.org/core/): a blog for Core WordPress development and related topics. 
*   [Make Design:](https://make.wordpress.org/design/) a blog for design efforts including user experience, user interface, and visual design efforts.   
*   [Make Documentation](https://make.wordpress.org/docs/): a blog for documentation efforts including developer specific items. 
*   [Make Themes](https://make.wordpress.org/themes/): a blog dedicated to themes including theme reviews, sharing best practices, block-based themes, and more.  

Like with any WordPress site, you can review specific tags to help narrow down information particularly on busier sites like Make Core:

*   Core chats: [https://make.wordpress.org/core/tag/dev-chat/](https://make.wordpress.org/core/tag/dev-chat/)
*   Core Editor chats: [https://make.wordpress.org/core/tag/core-editor-summary/](https://make.wordpress.org/core/tag/core-editor-summary/)
*   Core JS chats: [https://make.wordpress.org/core/tag/core-js/](https://make.wordpress.org/core/tag/core-js/)

## Communication Pathways:

These communication pathways start from the smallest action to increasingly more attention bringing steps you can take. These should help you figure out what “tools are in your toolbox” and how best to go about implementing ideas/proposals. 

If in doubt, feel free to ask first in [#core](https://make.wordpress.org/core/tag/core/) or [#core-editor](https://make.wordpress.org/core/tag/core-editor/) for advice. 

**Important Note on Timing:** 

Each of these communication pathways exist across different timeframes. Some you can lean on whenever whereas others happen on a specific cadence. This makes it even more important to share early and keep in mind that the process of moving things forward may take more time as you might, for example, need to wait to discuss something at a community meeting. 

**Important Note on Collaboration:** 

There might be push-back to a solution or idea you propose—try not to take it personally. In WordPress, there are many voices with different experiences, technology views, and philosophical differences. You might not always get your way, no matter how brilliant your contribution seems. Assume positive intent and discuss from a place of respect and appreciation for your fellow contributors.

**Share in WordPress.org Slack Channels ([#core](https://make.wordpress.org/core/tag/core/), [#core-editor](https://make.wordpress.org/core/tag/core-editor/), [#core-js](https://make.wordpress.org/core/tag/core-js/), etc)** 

If you have an initial idea or question, sharing in WordPress.org slack channels can be a good place to start. Sometimes this isn’t necessary, and you can go straight to [GitHub](https://github.com/wordpress/gutenberg/) or [Trac](https://make.wordpress.org/core/reports/) though! 

**Create a GitHub or Trac issue**

Remember that it often helps to share a [Trac](https://core.trac.wordpress.org/) or [GitHub](https://github.com/wordpress/gutenberg/issues) issue first before potentially offering a PR. Generally speaking, opening an issue is best for more practical explorations on short term items. Keep in mind that if you need to, you can get wider attention using the following handles in GitHub to alert people (use sparingly):

*   Alert the Gutenberg Development Team: @WordPress/gutenberg 
*   Alert the Gutenberg leads: @WordPress/gutenberg-core
*   Alert the triage team with this hande: @WordPress/gutenberg-triage-team 

Note: these handles do not work in slack. 

**Share in the Open Floor of Community meetings**

The meeting schedule can be found [here](https://make.wordpress.org/meetings/) and meetings are held in [WordPress.org Slack](https://make.wordpress.org/chat/). Each meeting has an open floor section where anyone can bring up a topic. If you are unable to make a meeting, you can comment on the agenda post for the meeting and the person running the meeting will raise it for you. Depending on the topic, it can be advantageous to be there to explain or to have some representation. If you’re unsure where to start, join the bimonthly new contributor and you’ll find people who can help you figure out where to go next. 

**Write a Personal Post**

Writing blog posts on your personal site is an effective way to get attention on new ideas within the community. The one catch to this is that there needs to be some level of distribution. Generally speaking, personal posts are best for big picture explorations/thoughts or more simplistic demos. Here are two good examples: [BlockBook](https://riad.blog/2020/07/22/introducing-blockbook-for-wordpress/) and [Collaborative Editing](https://riad.blog/2020/06/11/write-as-blocks-in-an-encrypted-collaborative-environment/).  

**If Gutenberg related, include in** [**What’s Next**](https://make.wordpress.org/core/tag/gutenberg-next/) **in Gutenberg posts**

These monthly posts are designed to set the framework for the next month but they can also be excellent ways to flag specific issues/ideas/PRs for attention as long as they fall within the realm of Gutenberg work and the focuses for that month. Here’s an example [from one of these posts](https://make.wordpress.org/core/2020/06/04/whats-next-in-gutenberg-june/):

“[@epiqueras](https://profiles.wordpress.org/epiqueras/) recently broke down all template tags alongside their block equivalent to lay the groundwork for Full Site Editing:  “The idea is for everyone in the community, especially those very familiar with traditional theme development, to contribute to this list. There might be things we are missing. There might be things we could lose.” Please check out [this overall issue](https://github.com/WordPress/gutenberg/issues/22724) and share what might be missing.” 

If you’re wanting an issue to be included, ping in [#core-editor](https://make.wordpress.org/core/tag/core-editor/) with context for why. Keep in mind these happen only once per month so if it’s more time sensitive it’s best to use a different pathway.  

**Write a Make Blog Post**

The Make Blog network is where asynchronous discussions, meeting notes, agendas, and ideas are shared. Generally speaking, it’s best to post here for big picture content that has built in team consensus or for things like [Dev Notes](https://make.wordpress.org/core/tag/dev-notes/) before major releases. Keep in mind that you’ll either need to get proper access to these sites or have someone with access to post for you. To get access, you’ll want to ask in the relevant team’s slack channel and explain why you’d like to be granted the ability to post. It’s also expected and commonplace that you’ll have someone review your post before publishing. When in doubt, feel free to share in [#core](https://make.wordpress.org/core/tag/core/) or [#core-editor](https://make.wordpress.org/core/tag/core-editor/) for a review. 

**Share at a WordCamp**

Similar to WPTavern or Post Status articles, WordCamps are ideal for larger, longer term efforts. A great example of this was around the initial Gutenberg launch and how much effort was put into sharing information about Gutenberg at WordCamps. [With each phase of Gutenberg](https://wordpress.org/about/roadmap/), more effort will need to be made to continue to help pave the way for adoption and acceptance. 

## Situationals

To help put the above communication pathways into practice and provide clarity, the following section contains example situationals. Remember that there’s a ton of nuances and it never hurts to have a second opinion! Feel free to ask in [#core](https://make.wordpress.org/core/tag/core/) or [#core-editor](https://make.wordpress.org/core/tag/core-editor/) for advice. 

**Need more attention on an issue**

*   Make sure the issue or PR is properly labeled so the appropriate teams are likely to find it. Note that for Gutenberg’s GitHub repo you need a certain level of access to properly label things. 
*   Share in WordPress.org Slack Channels ([#core](https://make.wordpress.org/core/tag/core/), [#core-editor](https://make.wordpress.org/core/tag/core-editor/), [#core-js](https://make.wordpress.org/core/tag/core-js/), etc) asking for someone to look into it.
*   Raise it in the open floor of a [core-editor, core, or new contributor meeting](https://make.wordpress.org/meetings/). If you can’t attend the meeting, add it to the agenda and it will be covered for you. It’s also common if you are in touch with other community members who can make the meeting to have them raise it for you. 
*   Use the group handles in GitHub to get the Gutenberg Leads’ (@WordPress/gutenberg) or Development Team’s attention (@WordPress/gutenberg-core). Note that these do not work in slack. 

**Need to introduce an idea**

*   DM different community members sharing the initial idea to gather interest. This can often be helpful to do internally first before opening up more widely. If you don’t know who to DM, just drop the idea in [#core-editor](https://make.wordpress.org/core/tag/core-editor/) or [#core](https://make.wordpress.org/core/tag/core/). 
*   Create a [GitHub](https://github.com/wordpress/gutenberg/issues) or [Trac](https://core.trac.wordpress.org/) issue explaining the idea at hand before sharing in the open floor of an appropriate meeting.
*   If it’s a larger scale idea or proposal, a Make Blog post might be best.

**Need to create momentum**

*   Share in the Open Floor of a meeting ideally with specific asks to focus efforts and spark more discussion. 
*   If related to Gutenberg, include the issue or topic in the [What’s Next](https://make.wordpress.org/core/tag/gutenberg-next/) in Gutenberg posts. To get included in those posts, please message in [#core-editor](https://make.wordpress.org/core/tag/core-editor/) and the people who organize these posts can decide if it fits.

## Helpful Hints

*   Create and update your [WordPress.org Profile](https://profiles.wordpress.org//profile/edit/group/1) to include relevant information (note: adding your WordPress origin story is an awesome way to connect with others).
*   Create a WordPress.org Slack account and make your profile descriptive so people can quickly get context about who you are. 
*   [Update your GitHub Profile](https://github.com/settings/profile) to include relevant information.
*   Connect your GitHub account to your WordPress.org Profile.
*   Share what you’re working on for Gutenberg in the [#core-editor](https://make.wordpress.org/core/tag/core-editor/) meetings or on [the agenda posts](https://make.wordpress.org/core/tag/core-editor-agenda/) if you can’t attend. This allows others to get to know you and what you’re working on naturally over time. 

## Keeping up with the community

It can be difficult and overwhelming to keep up with what’s happening in the community at large. Thankfully, there are various efforts to summarize and streamline content depending on your interests:

*   [Month in WordPress summaries](https://wordpress.org/news/category/month-in-wordpress/) (monthly)
*   [Index of Gutenberg Development](https://make.wordpress.org/core/handbook/keeping-up-with-gutenberg-index/) related items (regularly updated)
*   [What’s New in Gutenberg](https://make.wordpress.org/core/tag/gutenberg-new/) (biweekly) and [What’s Next in Gutenberg](https://make.wordpress.org/core/tag/gutenberg-next/) (monthly)
*   [Ways to keep up with Full Site Editing](https://make.wordpress.org/core/2020/05/20/ways-to-keep-up-with-full-site-editing-fse/).

Beyond these efforts, you can always follow individual Make Blogs like [WordPress.org News](https://wordpress.org/news/) or [Make Core](https://make.wordpress.org/core/) (core development efforts). To follow them, just use the “Subscribe” box in the sidebar of each Make Blog to get these posts sent to your email. 

[#meta](https://make.wordpress.org/core/tag/meta/)