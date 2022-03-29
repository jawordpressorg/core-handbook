# Researching Code History

## Using Subversion Annotate

When you need to investigate code, you’ll often have questions about why the code is written the way it is, what it looked like before, who wrote it, and if you can find any more details about it. Subversion annotate (also called **svn blame** or **svn praise**), combined with Core Trac, can help you answer these questions.

To get started, open the [Trac browser](https://core.trac.wordpress.org/browser/trunk), and navigate to the file you want to investigate. Click the Blame link at the top right of the page. You’ll see a new column appear on the left-hand side with the changeset that is associated with each line of the file.

## Anatomy Of A Changeset

When you click on the changeset, a new dialog appears with the following information:

*   Changeset number (also called revision number) – Click the number in the title for a link to the changeset.
*   Timestamp – When the change was committed to WordPress core.
*   Author – Who committed the code.
*   Message – Why the change was made. Often, this includes any associated trac tickets (e.g. [#12345](https://core.trac.wordpress.org/ticket/12345)), associated unit test tickets (e.g. #UT12345), and the user who wrote the accepted patch (e.g. props username).
*   Changed files – A list of added and removed files, and an inline diff of modified files.

## Associating Code With A WordPress Release

To find out when a piece of code was released, look at the associated revision number and find the next highest revision number on the [WordPress tags browser](https://core.trac.wordpress.org/browser?order=name#tags). For example, if you want to know when revision 14377 shipped, you can see that 3.0 was tagged as 15274 and 2.9.2 was tagged as 13165. Revision 14377 was too late to ship with 2.9.2, so it must have shipped with 3.0. You can also verify this by looking at the associated ticket. Revision 14377 is associated with [#12637](https://core.trac.wordpress.org/ticket/12637), which has a milestone of 3.0.

## Using The Command Line

If you prefer using the command line, you can use the **svn blame** (or **svn annotate**, **svn ann**, or **svn praise**) command. The syntax is: `svn blame [filename]`. Since the output can be verbose, you probably want to pipe it to less. For example: `svn blame wp-includes/formatting.php | less`.

Once you see a specific revision you want to investigate, use **svn diff** to find exactly what changed. The syntax is `svn diff -r [revision number - 1]:[revision number]`. For example, to view changes made in revision 2000, type `svn diff -r 1999:2000`.

To view the full commit message, including the committer and timestamp, use **svn log**. The syntax is `svn log -r [revision number]`. For example, to view the commit message for revision 14377, type `svn log -r 14377`.