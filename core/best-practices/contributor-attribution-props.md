# Contributor Attribution (&#8220;Props&#8221;)

One of the greatest things about open source is that contributions come in many shapes and sizes. Anyone can contribute regardless of skill set, experience, time zone, or background. There are countless ways for someone to get involved with open source projects.

WordPress is no different. Contributors submitting code modifications are only a small subset of the larger community. Recognizing all types of contributions in all locations is essential to establishing a healthy contributor base. Contributors who feel recognized and valued are more likely to continue contributing.

**The responsibility for this falls on the shoulders of the project’s maintainers.** When work is done, and changes are made, the project tracks them by giving “props” to all contributors involved.

## What are “props”?

“Props” is short for “proper respect” and is used in WordPress to signify thanks for a contribution. This practice began in [\[1102\]](https://core.trac.wordpress.org/changeset/1102) when the first contributor was given props for a contribution to WordPress. Since then, props have been used as a way to recognize and track contributions throughout the project’s history. Contributions to Core take on many forms, from things that directly impact the code (such as writing and reviewing patches) to things like design, testing, and well-written bug reports.

## Who gives props?

The props (or credits) within a release are collected using a script on WordPress.org that parses commit logs to extract all props given to contributors by committers and maintainers using the specific formats detailed below. The commit log files are carefully scoped to represent all activity for the specific date or commit ranges representing the current release cycle. The results are embedded in the About Page, Release Announcement Post, and committed to the [w.org Credits API](https://api.wordpress.org/core/credits/1.1/), which is used to list contributors on the Credits page in the WordPress admin area.

Additional non-code contributions are gathered by the Release Squad, and focus leads to be added to the Credits API as necessary. For example, any props given in Slack for helping to test release packages, facilitating meetings, writing developer notes, etc., are currently *not* automatically compiled.

The Credits API currently only contains contributor lists for WordPress >= 3.2.

## When should props be given?

Err on the side of giving props liberally. Props can provide major encouragement for contributors and ensure people receive recognition for their contributions.

Props should be given to all those who contributed to the final commit, whether through patches, refreshed patches, code suggested otherwise, design, writing, user testing, or other significant investments of time and effort.

In the case of bug reports, props should also be given to the reporter of the bug. Check any tickets that were closed as duplicates in case they contain contributions that warrant props, too.

## How are props given?

Because contributions happen in multiple locations using many different tools, there are some nuances to how props should be formatted. Below is how props are given in SVN and Git repositories.

### wordpress-develop commits in SVN

When Core Committers deem a change ready and record a transaction in the canonical subversion repository, aka committing code. 

`Props desrosj, jorbin, jeffpaul.`

The full [commit message guide covers this](https://make.wordpress.org/core/handbook/best-practices/commit-messages/) in-depth, but the standard rules are:

*   Props must be preceded by a blank line.
*   There should be no semi-colon (`:`) between “Props” and the w.org usernames.
*   Usernames must not start with an @ (at) sign.
*   Separate usernames by comma + space. Think: /^props (\\s\*(\[^,\]+),?)+$/
*   Copy/paste usernames to avoid typos. (Sorry, rmccue; or is that rmmcue?)
*   If the user has a space in their displayed name, use the slug from their w.org profile URL. For example, Frank Klein on Trac should get props as frank-klein.
*   The props line should only include the word props, wordpress.org usernames, spaces, and punctuation.
*   The `props` line must end with a period.

### GitHub repositories/merge commits

When merging code through a pull request on GitHub, maintainers are required to copy and paste the list of contributors provided by the Props Bot GitHub Action into the bottom of the merge commit message.

Always review the list of GitHub accounts included to ensure all who have contributed meaningfully to the PR or any linked issues are credited.

Some technical notes:

*   The list of `Co-authored-by` trailers must be preceded by a blank line.
*   `Co-authored-by` trailers should be the last thing in a commit message.
*   The unlinked contributors must come before the `Co-authored-by` trailers.
*   Unlinked contributors should be entered in one line preceded by `Unlinked contributors:`, each one separated by a comma and a space (`,` ), and a period after the last one. Example: `Unlinked contributors: nacin, matt.`
*   Usernames must not start with an `@` (at) sign.
*   When manually adding someone, please only use their GitHub and WordPress.org usernames in the following format: `Co-authored-by: githubusername <[dotorgusername@git.wordpress.org](mailto:dotorgusername@git.wordpress.org)>`.
*   The only accounts that are allowed to be noted with a non-w.org email are bot accounts (`dependabot` or `github-actions`). It’s important to leave these bots as listed by the GitHub generated `Co-authored-by` trailer so future contributors know which bots were involved in the changes.
*   If there are contributors already noted with `Co-authored-by` in the suggested commit message, verify they are also included in the list provided by Props Bot before removing. These will be in **GitHub format and should be converted to the above w.org format**. Deleting the GitHub formatted ones will ensure an accurate contributor count for each commit, but it’s not required. Non w.org emails will be ignored by the props parsing scripts.
*   If a contributor’s w.org username is unknown, add their GitHub username to the “Unlinked contributors” list.
*   If there are `Signed-off-by` trailers in the suggested commit message, leave them in place above `Co-authored-by` trailers. These serve a different purpose and are ignored in the context of collecting props.

#### Props Bot

A GitHub Action, [WordPress Props](https://github.com/WordPress/props-bot-action), has been created and should be utilized in GitHub repos across the WordPress project to help identify, capture, and include contributors within the props in merge commits. If you need help setting up that as an action within your repo, please [open a ticket with the Meta team](https://meta.trac.wordpress.org/newticket).

## General Rules and best practices

*   Always manually review any generated list to ensure that no contributions go unrecognized.
*   When someone does not contribute in a meaningful way, it’s sometimes appropriate to remove them from a props list. Use your best judgment to decide whether someone was trying to be helpful. If they only commented, “Why is this still broken?” or “When will this be fixed?” they have not really positively impacted the eventual solution. On the other hand, while a comment like “I’m seeing this on my site using updating to x.y” may seem unhelpful at first, it’s providing important detailed information that could be used to substantiate a report and under which conditions.
*   If you’re ever unsure, please ask in the \[#core-committers channel in Slack\](https://wordpress.slack.com/archives/C18723MQ8).

### `wordpress-develop` specific notes

*   Prop yourself when the commit is the product of huge efforts involving multiple people, such as a major feature, API, or particularly nasty bug.
*   If committing your own code, props are assumed, so omit yourself here as well.
*   If you forget to prop someone, check to see if they already have props in the current release. It will not matter in the long run, as they will be included in the release credits anyway. If they are not already propped, then you can flag it to the [Release Coordinator](https://make.wordpress.org/core/handbook/about/release-cycle/wordpress-release-team-and-focus-leads/#release-co-ordinator) so they can ensure that person is added on release day. It is also recommended to reach out to the contributor in Slack or in a comment on the ticket as a courtesy, apologize for missing their name in the commit message, and let them know their contribution will be recognized. Note how. Also, use the [core props tool](https://make.wordpress.org/core/wp-admin/admin.php?page=props-edit-core) to ensure people are properly credited on their profiles.
*   When listing props while committing, avoid including anything that is not part of a w.org username. There’s no need to say `Props jorbin for testing.` or `Props nacin for the initial implementation.`. This can create false positives when using a script to extract contributor usernames ([implementation is not a w.org contributor](https://profiles.wordpress.org/implementation/)). 
*   It is normal for committers to adjust style or rearrange logic before a commit or to account for a simple edge case. In these instances, omit yourself. Your name on the commit implies that you have reviewed and tested it, which is just as important as the contents of the commit.

### GitHub specific notes

*   **Always include yourself in the props list, even if it’s noted that you will be the author of the merge commit.** The w.org style credit is required attribute your contribution to your w.org profile. See [WordPress/props-bot-action#46](https://github.com/WordPress/props-bot-action/issues/46) for more context.
*   **Do not use personal emails or GitHub-specific emails** ([`ID+USERNAME@users.noreply.github.com`](mailto:ID+USERNAME@users.noreply.github.com) or `USERNAME@users.noreply.github.com`).
*   There’s currently no automated way to add a contributor who is not included in the list prepared by Props Bot. To find someone’s w.org profile, visit `[https://profiles.wordpress.org/github:GHUSERNAME](https://profiles.wordpress.org/github:GHUSERNAME)`, replacing `GHUSERNAME` with the contributor’s GitHub username. This will redirect you to the person’s w.org profile if they have connected their account. Add their GitHub username (without an `@`) to the `Unlinked contributors:` list when there’s no connection.

### Major Release Credits

The .org props script will attempt to detect spelling mistakes and match unlinked GitHub accounts as best as possible. But there will always be some manual review that needs to take place. The contributor running the props script can easily perform most of this. Here are some tips for reviewing and improving the accuracy of the contributor list for a release.

*   [https://profiles.wordpress.org/github:username](https://profiles.wordpress.org/github:noisysocks) will redirect to a contributor’s w.org profile when a valid connection exists.
*   [https://profiles.wordpress.org/$slack\_user\_id](https://profiles.wordpress.org/%24slack_id) will redirect to a contributor’s w.org profile. The Slack ID comes from the details view for a user in Slack (Click on avatar > View full profile > More \[…\] > Copy ID).
*   For unlinked GitHub accounts, perform a reasonable amount of detective work trying to confirm a contributor’s identity.
    *   Use any details listed on the user’s GitHub profile page (listed name, email, etc.) or website/social profile.
    *   Look for review commits and append `.patch` to the commit URL. Sometimes, there are different names and emails listed there.
*   That information can then be used to search profiles on WordPress.org to find a potential match. An example search query for search engines is `site:profiles.wordpress.org desrosj.`

Once a match has been identified, refer the GitHub account owner through Slack or a PR they participated in to the [handbook page about linking GitHub and WordPress.org accounts](https://make.wordpress.org/core/handbook/tutorials/linking-your-github-and-w-org-profiles/). This will be helpful in the future to avoid the same research effort in future releases.

## Props and About Pages

## Props and Release Announcements

All associated props for each release should always be listed towards the bottom of the matching announcement post. There are two ways to do this.

In major release posts, props should be listed using the `[wpcredits x.y]` shortcode. For example, the following is how the shortcode would be used for WordPress 6.5: `[wpcredits 6.5]`. 

The Credits API does support listing credits for each minor version. Instead, contributors for minor versions that did not also contribute to the corresponding major version are just added to the API under the major version. Because of this, an HTML list should be used instead of the shortcode. Someone with access to a wordpress.org sandbox will be able to generate this list using a script. Each contributor’s name as configured on their w.org profile, should be used and linked to their profile page.

* * *

Additional resources:

*   [https://make.wordpress.org/core/handbook/best-practices/commit-messages/#props](https://make.wordpress.org/core/handbook/best-practices/commit-messages/#props)
*   [https://make.wordpress.org/core/handbook/about/release-cycle/preparing-the-about-page/#props](https://make.wordpress.org/core/handbook/about/release-cycle/preparing-the-about-page/#props)
*   [https://helen.wordpress.com/2019/01/22/what-are-commit-props/](https://helen.wordpress.com/2019/01/22/what-are-commit-props/)