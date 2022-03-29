# Post &amp; Comment Guidelines

These guidelines were [initially proposed on make/core](https://make.wordpress.org/core/2015/09/30/proposal-makecore-post-guidelines/). If you have questions or feedback, please join Slack and ask in [#core](https://wordpress.slack.com/messages/C02RQBWTW).

## Introduction

The Make WordPress Core Blog (make/core) is the official blog of the WordPress core team. It is read by thousands of people, many of whom may not know the intricacies of core, or understand the process of core development.

Most make/core posts must serve one of two goals:

1.  Generate feedback (including testing) from the developer community
2.  Ensure developers know about changes and can plan accordingly

In order to ensure the best experience possible for the developer community, the guidelines on this page are written with unexperienced readers in mind.

## Posting

### When to write a post

Posting on make/core should be a common occurrence for committers, component maintainers, and other core contributors. There are many kinds of posts that should be written on a schedule:

*   **API changes.** There are a few examples of API changes that should be announced on make/core, including: new filters/actions, changed order of hooks, substantial enhancements to queries (the *Boone Gorges Rule*), changing the purpose of a parameter in a hook, new general helper functions, or any other significant changes in a release. These posts should be published on make/core within the first week of the beta period to ensure developers are aware of any upcoming changes.Grouping related changes into one post to accepted, so long as the post does not become too long. For example, a single post called “Customizer changes in WordPress 4.2” is fine, rather than individual changes about each commit. If in doubt, use the weekly devchat to discuss your proposed post(s).
*   **Meeting announcements.** Regular devchat meetings do not need to be announced, but an agenda post is helpful to developers who do not regularly follow the release. Other meetings should receive an initial post on make/core announcing the meeting, but do not need weekly announcements.
*   **Meeting notes.** Do you hold regular or one-off meetings? Post notes from your meeting on make/core to ensure those that couldn’t attend have an easy way to provide feedback. Devchats almost always receive an accompanying summary post for those who can’t attend. Component chats and feature plugin chats should also have summary posts after meetings.
*   **Feature Plugin-related posts.** Introducing your feature plugin idea to the world is best done at a weekly devchat or one of the semi-regular feature plugin chats. Once proposed, a post on make/core can make sense, depending on the stage of the idea. Merge proposals should also make their way to make/core, when asked for from a release lead.

Keep in mind that feedback on make/core will almost always be greater than that in Trac tickets. Announcing changes and posting early and often is helpful to the entire community.

### Peer Review

Whether it’s your first time posting or your millionth, it is strongly encouraged to ask a committer to proofread a post before publishing it. Peer review (like code review) helps makes sure your words are clear and working as intended, but also helps identify any phrases that might not translate well. Some posts (like weekly agendas) do not necessarily need peer review, but if it’s your first few times posting on make/core, it doesn’t hurt to ask.

Feature plugin merge proposals should *always* be read by the release lead (or designee) before posting. Release devnotesdev note Each important change in WordPress Core is documented in a developers note, (usually called dev note). Good dev notes generally include: a description of the change; the decision that led to this change a description of how developers are supposed to work with that change. Dev notes are published on Make/Core blog during the beta phase of WordPress release cycle. Publishing dev notes is particularly important when plugin/theme authors and WordPress developers need to be aware of those changes.In general, all dev notes are compiled into a Field Guide at the beginning of the release candidate phase. should be read by the release lead (or designee) before publishing.

See the Giving Proper Credit (Props) section below for information on how to make sure the proofreaders/peer reviewers are recognized.

### Style and Substance

The make/core blog is the official voice of the core team. As a result, you should keep your personal thoughts out of the body of the post, leaving them for the comments. Furthermore, **first person pronouns should be avoided**.

Similarly, **the word “we” should be avoided** in posts, unless its made very clear which group is speaking. An example of this is listing attendees of a meeting and, in the summary post, noting that “we, those present at the meeting” made a decision or agreed on a plan of action.

If you’re proposing a roadmap or making a request for comments, make sure to **highlight the draft/proposal status** in both the title and opening paragraph. This helps to avoid confusion about the status of your proposal.

Many people reading make/core don’t speak English as a first language. Keep that in mind when deciding how to phrase your post. For make/core, it’s always better to write simple instead of smart. In general, the tone should be similar to WordPress: Friendly.

*Check out the [Text-based Communication in Open Source](https://wordpress.org/contributor-training/lesson/text-based-communication-in-open-source/) and [Best Practices for Global Collaboration](https://wordpress.org/contributor-training/lesson/best-practices-for-global-collaboration/) pages on the [WordPress Contributor Training](https://wordpress.org/contributor-training/) site for more tips and best practices.*

### Giving Proper Credit (Props)

When a post is finally published, it goes out under one person’s name. However, posts are often the combined efforts of several contributors who deserve to be recognized. Noting who helped bring a post to a publishable state can also provide important context to readers and helps them understand who they would be addressing in discussion.

At the bottom of your post, include a footnote like so:

*Props @desrosj and @jeffpaul for providing historical background, @chanthaboune and @andreamiddleton for proofreading.*

### Tagging and Other Specifics

For each of the following types of post, there are some things to keep in mind:

*   **Component-related posts.** Almost all posts relate to a component. Please tag component-related posts with the component name. If your post covers multiple components, use multiple tags!
*   **API changes.** All API changes should be tagged with the related release number, the component name, and “dev-notes” to indicate that it is a note for developers.
*   **Release announcements.** All posts related to a specific release – including agendas, meeting summaries, API changes, week in core, etc – should be tagged with the related release.
*   **Feature plugins and other projects.** Each of these type of post should be consistently tagged with a project name. For example, if you’re working on a redesign of the admin called “MP6,” tag all related posts with MP6.
*   **Meeting announcements.** When posting about a meeting ahead of time (aka, not summary notes), use the [time shortcode](https://make.wordpress.org/meta/2013/04/03/time-shortcode-for-make-p2s/) so that readers know exactly when the meeting will take place in their local time.

## Comments

Discussion and criticism of ideas is important to the long-term success of WordPress. In support of this, all make/core posts have open comments. As a result, **commenters should be respectful and professional**, understanding that many other commenters and readers do not speak English as a first language. At times, it may make sense to over-communicate and be extra polite to ensure no misunderstandings occur.

If a comment is disrespectful and/or unprofessional, it may be edited at the discretion of the core team.

Editing of a comment will be done with the approval of at least two blog administrators. When a comment is edited, only the offending section will be edited with the intent of retaining as much of the expressed opinion. The administrators who edit the offending comment will add an editor’s note stating the reason for editing and the names of the administrators who took action. Additionally, the administrator doing the editing should retain a screenshot of the unedited comment, which can be uploaded to the Media Library on make/core, if necessary.

Comments will only be deleted when the offending comment is clearly spam that was not properly moderated.

[#core](https://make.wordpress.org/core/tag/core/)