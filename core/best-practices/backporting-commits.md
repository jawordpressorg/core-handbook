# Backporting Commits

When porting a commit from `trunk` back to versioned branches, it’s best done by different committer than the one who made the `trunk` commit, as an extra layer of review. During the RC phase, at least two committers must sign off on any commit.

Do not commit to multiple branches in the same commit. This will, at a minimum, break the Git mirrors.

A basic SVN flow to backport a commit could look like this:

1.  `$ svn switch '^/branches/5.9'`
2.  `$ svn merge -c 12345 '^/trunk'`
3.  `$ svn ci`

If the fix in `trunk` required multiple separate commits, you can backport them all in a single command like this:

`svn merge -c 10001,10002 '^/trunk'`

For merges you should generally use a pristine `branches/5.9` checkout that has no code changes other than what’s being merged and a test site for testing the merged commit on (which you should always do).

Also, although you’ll probably never need it, if you’re merging multiple commits one after each other, don’t forget to run `svn up` between them. If what you need to merge has multiple commits, also feel free to squash them down for the branch commit to make it easier for everyone reading.

Sometimes multiple changes to the same code are made in `trunk` before they are ported to a branch.  In this case, you will get conflicts, so be sure to port the older changesets as well.  Committers asking for a backport should indicate this situation on the ticket.

To add the merge info afterwards you can run `svn merge --record-only -c 12345 '^/trunk'`.

The branch commit message will generally be copied from the `trunk` commit(s), but adds a new line between `Props` and `Fixes` which says, “Merges \[`trunk changeset ID`\] to the 5.0 branch.” For an example, see [r43276](https://core.trac.wordpress.org/changeset/43276/).

Make sure to run the above commands from the branch root, and not from a sub directory. The reason for this is that the `svn:mergeinfo` is a SVN property on `/branches/5.9` which the SVN client sets, it’s not a server side thing.

At the bottom of https://core.trac.wordpress.org/browser/branches/5.9 you see two links, ‘merged’ and ‘eligible’. The second one shouldn’t list commits which are already merged.

### Security Backports

Security fixes are backported to many versions, and are not committed until the day of a release. Because of this, the process can be streamlined a bit.

You should still make individual commits to `trunk` and the current branch, but on the older branches you can make a single commit with all of the fixes for that branch. Do not commit to multiple branches at once, though.

When committing the bulk patch to each branch, you still need to record the merge metadata with:

```
svn merge --record-only -c 12345,12347,12349 '^/trunk'
```