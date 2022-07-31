# Writing developer notes

A Developer note (or “dev note” for short) is a blog post on the [Making WordPress Core](https://make.wordpress.org/core/) blog that details a technical change in an upcoming release and what developers need to know about that change.

Dev notes are an important part of the WordPress Core release cycle. They keep the developer community informed by calling out changes that could impact how they build on WordPress, and supplements inline documentation by explaining the problems, solutions, best practices, and edge cases related to the change.

The best dev notes are clear, concise, and complete.

## How do you know what needs a dev note?

For each release, tickets that may need developer notes are given the `needs-dev-note` keyword on Trac. When a note has been published for a ticket, that keyword is replaced with the `has-dev-note` keyword and a link to the note is included in a comment.

**It’s important to remember that not all tickets in a milestone marked `needs-dev-note` on Trac end up being committed and included in that release.**

For that reason, care should be taken to only write notes for tickets and changes once it becomes clear that the changes will be included in the release. Usually, that means tickets with the `closed` status (and sometimes `reopened`) are where the focus should be.

## Who should write dev notes?

The hierarchy for who should author a dev note is as follows:

*   Someone with deep, working knowledge of the changes. This is usually the committer that made the change, a component maintainer that helped craft/test the changes, or any other contributor that helped push that change forward.
*   Someone with a good technical foundation that did not work on the change, but can review the code changes in detail to convey the right message.
*   Someone that is less technical, but is comfortable interviewing or asking someone in the above groups questions about the changes in order to have the information needed to write the note.  
    

## What should a dev note include?

Each note will be unique, but every dev note should clearly define a problem that is being solved, how that problem was solved, and what developers need to know about the related changes. It usually contains a mix of the following:

*   Clear identification of a problem
*   Description of why this is problematic
*   Are developers currently solving the problem in a less than ideal way?
*   Are there established patterns in the wild within plugins and themes addressing this problem already?
*   Documents current practices or usage, and how the current state of the code base may contribute to the issue.
*   Describes what the ideal behavior would be and why,
*   Explains the changes made to achieve the desired behavior/outcome
*   Provides examples for how to correctly use the function/feature/API after these changes (establish a best practice)
*   Identifies backwards compatibility considerations, explains how they were addressed in Core, and how they should be addressed within plugins and themes.
*   Details possible edge cases that have been identified
*   Links to additional reading materials about the change as necessary, such as Trac or GitHub tickets, changesets, past dev notes, past posts on Make blogs, etc.

Sometimes, there are a large handful of changes that deserve to be called out, but are not detailed enough to warrant individual dev notes. **It is more than fine to group multiple changes together in a single dev note.**

It is common for component maintainers to publish a single dev note for their component to detail several different changes. It’s also common for a more generic “Miscellaneous developer focused changes in X.X” dev note to be published collecting any other remaining smaller changes that should receive a call out.

**After researching the ticket but before writing the dev note, ask “Is this a change that needs to be documented at length? Is a one sentence call out sufficient? Or does the change not have anything technical that actually needs to be called out”**

The goal is to find a balance between post length, related changes and topics, and the number of dev notes published during a release. More dev notes are better than less. However, it is important to keep in mind that readers should not get tired of the notes and stop reading them.

## Should dev notes be reviewed?

Every post on a [Making WordPress](https://make.wordpress.org/) blog should be peer reviewed by at least one other person. **For dev notes, each one must have *at least* two reviewers**: 

*   One technical review to verify the accuracy of the post and ensure no important details were missed.
*   One copy review to help spot grammatical, spelling, and other errors.

After receiving at least two reviews, reach out to the Documentation lead for the release. They will have a high level overview of all dev notes planned or in progress and can help recommend a publish window. It’s important to spread out dev notes to prevent “dev note fatigue”. For example, 3 or more dev notes should not be published on the same day.

## When should a dev note be published?

A dev note can be published any time during the release cycle. If a change to the code base is committed today, the dev note could be published tomorrow. However, it’s usually best to wait a while after the changes are committed to allow several days for testing.

A handful of WordPress contributors run `trunk` on their websites in order to test every change after it’s made. On occasion, an issue does come up requiring adjustments to be made. Waiting to publish the dev note ensures that only one note is required for a change, avoiding the potential for confusion and making more work for developers.

**However, all dev notes for a changes in a specific release should be published before the first release candidate for that release.**

To help organize documentation about the upcoming release, a Field Guide collated and published for every major version of WordPress at the same time as [Release Candidate 1](https://make.wordpress.org/core/handbook/about/release-cycle/releasing-major-versions/#release-candidate). Field Guides are a collection of all relevant dev notes and tickets for an upcoming release.

All field guides for previous releases can be found here: [make.wordpress.org/core/tag/field-guide](https://make.wordpress.org/core/tag/field-guide).

## Other Tips

Here are some additional resources and tips to help write developer notes

### Tone and style

When writing or reviewing any post on the [Making WordPress Core blog,](https://make.wordpress.org/core/) it’s important to remember the [Post & Comment Guidelines](https://make.wordpress.org/core/handbook/best-practices/post-comment-guidelines/). The Style and Substance section is particularly important. The guidelines on that page help ensure clear communication with a consistent tone and voice throughout all official WordPress channels.

### Tagging and categorizing

After writing a developer note, it is also important to make sure it is tagged correctly. The tags that every dev note should have are `dev-notes`, and a specific version tag (`5.5`, for example). Additional tags can be added as necessary, and usually include specific component tags.

Properly tagging notes is important to make them easier to find and revisit later.

[dev notes for a particular release](https://make.wordpress.org/core/tag/dev-notes+5.5/), all the [dev notes written on the blog](https://make.wordpress.org/core/tag/dev-notes), or the [dev notes for a particular component](https://make.wordpress.org/core/tag/dev-notes+rest-api/).

## Attribution

When the dev note is published, a “props” line at the very bottom should always be included. For example: “*Props* [](https://wordpress.slack.com/team/U02SVSW3U)*@janedoe for technical review,* [](https://wordpress.slack.com/team/U02RR5UTA)*@johndoe for proofreading.*“

This ensures everyone that contributed to the post receives proper recognition, helps the reader know the voices behind the post, and who they are addressing if there are comments or questions.