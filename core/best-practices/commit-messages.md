# Commit Messages

Commit messages are a critical aspect of how WordPress is developed. They are an integral part of the project’s history, along with the changesets themselves. We write commit messages for multiple audiences: contemporaries (fellow core developers, plugin developers, anybody following along with core development), future contributors, and computers. Good commit messages serve each of these audiences well. They describe the *what* and the *why* of the changeset; the *how* is described by the diff itself.

Even if you are not a committer, you can make use of these guidelines while contributing to WordPress, as well as in your own projects. By describing your patch in a way that is sensitive to the concerns outlined here – or even drafting a commit message yourself – you make it easier for the committer process your contribution quickly.

Remember: Do not commit to multiple branches in the same commit. This will, at a minimum, break the Git mirrors.

## Format

The general format for a commit message is as follows:

> Component: Brief summary.
> 
> Longer description with more details, such as a \`new\_hook\` being introduced with the context of a \`$post\` and a \`$screen\`.
> 
> More paragraphs can be added as needed.
> 
> Props person, another.  
> Fixes [#30000](https://core.trac.wordpress.org/ticket/30000). See [#20202](https://core.trac.wordpress.org/ticket/20202), #105.

Generally, each line in a commit message should begin with a capital letter and end with a full stop/period. Code, such as the name of a function or a hook, should appear inside backticks, to ensure proper formatting in Trac and Slack. Ticket numbers preceded by a number sign [#20202](https://core.trac.wordpress.org/ticket/20202) and revision numbers inside square brackets [\[30000\]](https://core.trac.wordpress.org/changeset/30000) will auto-link in Trac, Slack, and here on make/core.

### Brief summary

The first line of a commit message is a brief summary of the changeset. The brief summary is used for email subject lines, Trac changelogs, and features prominently in most VCS log formats, such as `git log --format=oneline`. The high visibility of the summary makes it critical to craft something that is as descriptive as possible within space limits.

#### Guidelines

*   Must be one line; no line breaks.
*   Aim for around 50 characters or less, stopping at 70. This is important because log-viewing tools nearly all expect the first line of commit messages to fit within these limits. This difficult restriction may force you to think critically about the essence of your commit; if you can’t describe the change in a short sentence, the commit may not be atomic enough.
*   You may prefix the summary with the component or focus of the change. Such a prefix may make it easier for contributors to scan the changelog for commits of interest. See [\[33901\]](https://core.trac.wordpress.org/changeset/33901), [\[33883\]](https://core.trac.wordpress.org/changeset/33883), [\[33848\]](https://core.trac.wordpress.org/changeset/33848) for some examples. Note that the prefix counts toward the 50/70 character count.
*   Use the imperative mood when possible: “Relax term ID comparisons…” instead of “Relaxes term ID comparisons…”

### Description

The longer description of a commit should include more details about the commit and its repercussions for developers. These may include new hooks, “gotchas”, other solutions that were considered, or backstory. Consider your audiences when deciding what should go into the description: developers following along with the commit mailing list, volunteers collating information for each release’s dev notes and WordPress Core Weekly, and future code archaeologists trying to figure out who did what and why.

#### Guidelines

*   Must be separated from the summary by a blank line.
*   Can be multiple paragraphs if necessary, separated by blank lines. It is not unreasonable for a commit message to be more verbose than the final changeset itself.
*   Unlike the Summary, lines should not be manually wrapped – log viewers can take care of wrapping the description themselves, if they need to.

### Props

Props should be given to all those who contributed to the final commit, whether through patches, refreshed patches, code suggested otherwise, design, writing, user testing, or other significant investments of time and effort. Usernames are parsed for the credits list and WordPress.org profiles.

In the case of bug reports, props should also be given to the reporter of the bug.

Check any tickets which were closed as a duplicate in case they contain contributions that warrant props too.

#### Guidelines

*   Must be preceded by a blank line.
*   Usernames must not start with an `@` (at) sign.
*   Separate usernames by comma + space. Think: `/^props (\s*([^,]+),?)+$/`
*   Copy/paste usernames to avoid typos. (Sorry, rmccue; or is that rmmcue?)
*   If the user has a space in their displayed name, use the slug from their w.org profile URL. For example `Frank Klein` on Trac should get props as `frank-klein`.
*   Err on the side of giving props liberally. Props provide major encouragement for contributors.
*   If you forget to prop someone, check to see if they already have props in the current release as it won’t matter in the long run as they’ll be included in the release credits anyway. If they aren’t already propped, then you can flag it to the [Release Coordinator](https://make.wordpress.org/core/handbook/about/release-cycle/wordpress-release-team-and-focus-leads/#release-co-ordinator) so they can ensure that person is added on release day. It’s also recommended to reach out to the contributor in Slack or in a comment on the ticket as a courtesy and apologize for missing their name in the commit message and letting them know their contribution will be recognized and note how.

#### Self props

*   Prop yourself when the commit is the product of huge efforts involving multiple people, such a major feature, API, or particularly nasty bug.
*   Generally, giving contributors feedback on patches and giving them a chance to iterate is the recommended process. However, on the occasions where you as the committer complete the idea of a patch, you could write “props X for initial patch.”
*   It is normal for committers to adjust style or rearrange logic before a commit, or to account for a simple edge case. In these instances, omit yourself. Your name on the commit implies that you’ve reviewed and tested it, which is just as important as the contents of the commit.
*   If committing your own code, props are assumed, so omit yourself here as well.

### Ticket references

Trac will add commit messages as comments on all tickets referenced as “fixes” or “see”. If a commit message contains the text “Fixes [#12345](https://core.trac.wordpress.org/ticket/12345)“, Trac will close ticket [#12345](https://core.trac.wordpress.org/ticket/12345) and assign you as the owner if there isn’t one already.

#### Guidelines

*   Ticket references should be on their own line directly below any props. If there are no props, an empty newline should separate it from the content above.
*   Multiple tickets should be separated by a comma + space.
*   If referencing both fixed and related tickets, begin with “Fixes” and end each set with a period, e.g. “Fixes [#19867](https://core.trac.wordpress.org/ticket/19867), [#9864](https://core.trac.wordpress.org/ticket/9864). See [#31696](https://core.trac.wordpress.org/ticket/31696).”. If there are many items in a set, put it on its own line.
*   If you forget to include a ticket number, comment on the ticket (e.g., “Fixed in \[changeset\_number\]” with an optional copy of the commit message to help ensure traceability.

## Example

Bad:

> Don’t use strict comparisons for term IDs. props booneiscool. fixes [#3398](https://core.trac.wordpress.org/ticket/3398).

Meh:

> Fixing \`wp\_dropdown\_categories()\` and other places that use term IDs.
> 
> props boonerocks. fixes [#20000](https://core.trac.wordpress.org/ticket/20000).

Good:

> Taxonomy: Relax term ID comparisons.
> 
> Term IDs are sometimes provided as strings. This is particularly evident in \`wp\_dropdown\_categories()\`, where the \`selected\` argument was not being respected. Plugin authors should also be wary of using strict comparisons for term IDs.
> 
> Props booneistheman.  
> Fixes [#13237](https://core.trac.wordpress.org/ticket/13237).

## Automatically Pre-fill Commit Message

If you use Git (and possibly commit with git-svn), you can have a hook automatically fill a new commit message with the standard format.

Create a `.git/hooks/prepare-commit-msg` file with the following script, and then `chmod +x .git/hooks/prepare-commit-msg`.

```bash
#!/bin/bash
COMMIT_MSG_FILE=$1
COMMIT_SOURCE=$2

if [ $COMMIT_SOURCE ]; then
	# A messages is already being provided via `commit -m`, rebase, etc.
	exit 0;
fi

template="Component: Brief summary.

Longer description with more details, such as a \`new_hook\` being introduced with the context of a \`\$post\` and a \`\$screen\`.

More paragraphs can be added as needed.

Props person, another.
Fixes #30000. See #20202, #105.
#
# See https://make.wordpress.org/core/handbook/best-practices/commit-messages/ for more detailed guidelines."

# Wrapping the variable in quotes preserves the newlines, because BASH is weird.
echo "$template" > $COMMIT_MSG_FILE
```

## Other tips for committers

While these are not about the commit message itself, the following guidelines are good to keep in mind.

During the RC stage, [all patches must be reviewed by a second committer](https://make.wordpress.org/core/handbook/about/release-cycle/releasing-major-versions/#release-candidate) before being committed.

### Before a commit

*   If you have any doubts about whether or not a patch is acceptable, ask a few other committers for a second opinion.
*   Make sure the changed lines conform to [the coding standards](https://make.wordpress.org/core/handbook/best-practices/coding-standards/).
    *   PHP
        *   To check all lines in all changed files, run `phpcs $(git diff trunk --name-only)` or `phpcs $(svn stat | grep "\(M \|A \)" | grep -v "external item" | cut -c8-)` .
        *   To check only the changed lines, clone [wp-dev-lib](https://github.com/xwp/wp-dev-lib/) and [run](https://github.com/xwp/wp-dev-lib/#manually-invoking-pre-commit) `DIFF_BASE=trunk DEV_LIB_ONLY=phpsyntax,phpcs /path/to/wp-dev-lib/pre-commit`. Note that you need to be on a local branch other than `trunk`, and the changes need to be either committed, or staged for commit. Unstaged changes will not be scanned.
        *   Creating Bash aliases for the above commands is recommended for convenience.
    *   JavaScript
        *   [Run](https://make.wordpress.org/core/handbook/best-practices/coding-standards/javascript/#jshint) `npm run grunt jshint`. This will be done automatically by `npm run grunt precommit` as well.
    *   HTML, CSS, a11y
        *   These must be checked manually.
*   Run `npm run grunt build && npm run grunt precommit`. This runs the automated test suites for PHP and JavaScript, as well as various other tasks for CSS, images, etc.
    *   You may also need to manually run PHPUnit with various flags, depending on the change.
*   Check the full diff one last time (`svn diff`). If you’re using Git, interactive staging (`git add -p`) is a good way to review individual chunks.
*   Check the list of modified files (`svn stat`), making sure that new files are added. It is also good to double check the contents of new files, as applying patches that add new files can result in the content of new files being duplicated. Also make sure that new files are not named the same as something in the  `$_old_files` array, or else they will be deleted again right away. If one is, comment out the line from the array with a note indicating when a file with the same name was added back. Do not delete the line.
*   If deleting files, add them to the `$_old_files` array.
*   You can “cherry-pick” commits from `trunk` to a release branch via `svn switch ^/branches/4.3 && svn merge -c 12345 ^/trunk`. You will be prompted to edit the message prior to committing. See [Backporting Commits](https://make.wordpress.org/core/handbook/best-practices/backporting-commits/) for more details.
*   Instructions for tagging and branching a release can be found in the [Core section of the releasing major versions](https://make.wordpress.org/core/handbook/about/release-cycle/releasing-major-versions/#core) page.
*   Bonus: for viewing modified files without including untracked files, add this as a Bash alias or function: `svn stat --ignore-externals | grep '^[^?X]'`

### After a commit

*   Monitor the corresponding job in [GitHub Actions](https://github.com/WordPress/wordpress-develop/actions), in case any tests fail in other environments.

## More resources

*   [A Note About Git Commit Messages](http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html)
*   [5 Useful Tips For A Better Commit Message](https://robots.thoughtbot.com/5-useful-tips-for-a-better-commit-message)
*   [How to Write a Git Commit Message](http://chris.beams.io/posts/git-commit/)