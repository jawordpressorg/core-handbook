# Bug Gardening

Not only is it important to [beta test](https://make.wordpress.org/core/handbook/testing/beta/) point release and bleeding edge WordPress nightly builds, but it’s also important to test and confirm reported bugs, and test patches submitted for possible inclusion to WordPress before they ever make it into the nightly builds. This job is mostly handled by volunteers (such as yourself) that serve as **bug gardeners**.

The [bug tracker](https://make.wordpress.org/core/handbook/trac/) contains numerous, wildly different [workflows](https://make.wordpress.org/core/handbook/trac/keywords/) through which all types of reported bugs, enhancements, new features, and various tasks are handled by reporters, gardeners, developers, and committers. It can be incredibly confusing trying to grasp the big picture all at once, but you don’t have to.

If you are new to the bug tracker and want to help out, here’s how you can get started with your first simple workflow. Once you have spent some time in this workflow, the rest of the tracker will become much more familiar, and you can feel confident in exploring other areas of Trac that also need help.

Keep an eye on [upcoming WordPress meetings](https://make.wordpress.org/meetings/) to join a bug scrub.

## The Bugfix Review Workflow

In this workflow, we are only going to work on tickets categorized as **bugs/defects**, and also just the ones with patches attached that supposedly fix those bugs. Additionally, this workflow only involves tickets in the **Awaiting Review** or the **Future Release** milestones, meaning that these are mostly reported bugs and patches that have not been reviewed or thoroughly tested yet. The [Patches to Defects That Need Review](https://core.trac.wordpress.org/report/46) report in Trac handles these filters for you already, so go ahead and open that now.

There are over 600 unique tickets in the report (at the time of this writing), so the first step is to choose one of those to start with. If you are just starting out as a bug gardener, we recommend avoiding any tickets more than 12 months old. Older tickets usually involve some controversial changes, or involve complex problems with complex solutions, requiring a heavier review process, which is usually why they have been stuck in the review process for more than a year.

You should try to work on tickets related to parts of WordPress that you are familiar with. The report is grouped by component, which makes the task of finding your first ticket to work on much easier.

Last, you should skip over any tickets with the **reporter-feedback** or **dev-feedback** keywords – you won’t be able to do anything with those tickets without more information from the reporter or a core developer.

Once you have found a ticket you want to work on, continue reading the rest of the instructions here for how you should address the ticket you have picked out.

### 1\. Ensure The Ticket Is A Bug

The first step required for any of the tickets in this report is to ensure that the ticket is in fact a bug, and not a feature request or enhancement.

Since new tickets are assigned to the **Awaiting Review** milestone by default, this report will include completely fresh issues, assuming the reporter attached a patch and added the **has-patch** keyword properly upon submission. Some of these tickets have not been through an initial review to ensure it was submitted with the proper issue type, component, and keywords. The documentation on the [ticket properties](https://make.wordpress.org/core/handbook/trac/#ticket-properties) should help clarify exactly which values the ticket type and component should be set as, and what keywords the ticket should have.

Considering what is involved for new tickets to be included in this report, the reporters submitting tickets listed here usually have a fairly good feel for the ticket properties and how they should be set. However, this is one of those exceptions to the rule – you will need to be much more critical of this in other workflows.

The most common problem you need to watch for in this workflow are tickets that have been submitted as a **defect**, but in reality, the issue (and patch) is actually an **enhancement** or a **feature request**. If the ticket describes new functionality, or even a change to existing functionality that is working perfectly fine (but perhaps not in the most ideal way), then the ticket type needs to be set as an enhancement (in the case of a change/addition to an existing component), or as a feature request (in the case of entirely new features). If this happens, fix the ticket type, and move on to the next ticket.

If the ticket is actually a bug, you need to confirm that the reported bug is, in fact, one that can be reproduced.

### 2\. Confirm The Bug

You should always test for the bug using a [SVN trunk](https://make.wordpress.org/core/handbook/svn/) checkout of WordPress. In the rare cases of critical bugs and regressions, then you should also test for the bug in the latest stable release of WordPress too.

Remember that it’s possible the bug only exhibits itself under specific versions of PHP, MySQL, browsers, and/or certain WordPress settings (i.e. multisite, roles/capabilities, different plugins/themes).

*   If the reporter wasn’t clear and you can’t reproduce it, ask for clarification from the reporter, and add the **reporter-feedback** keyword to the ticket.
*   If the reporter was very clear, and you still can’t reproduce the bug under their claimed conditions, leave a note that you tested it and couldn’t reproduce the bug.
*   If you are the second tester (besides the reporter) that can’t reproduce the bug, there’s a chance that something else could be wrong with the reporter’s installation/configuration. If this happens, add the **dev-feedback** keyword to the ticket, and move to the next ticket.

### 3\. Confirm The Patch

If you were able to reproduce the bug, then it is time to confirm the patch. Don’t worry too much about how the patch was written, unless you are a more experienced developer and can immediately spot problems with the way the patch was written.

[Download and apply the suggested patch](https://make.wordpress.org/core/handbook/tutorials/working-with-patches/#creating-and-applying-patches-with-grunt) to the same installation you were able to confirm the bug on. Sometimes a ticket will have multiple patches attached, and, if so, usually only the latest suggested patch needs testing; however, you might need to test the other patches too, if they haven’t been tested.

If any of the following conditions apply, remove the **has-patch** keyword, and add the **needs-patch** keyword:

*   The patch does not apply cleanly, or does not follow the [coding standards](https://make.wordpress.org/core/handbook/coding-standards/). Add the **needs-refresh** keyword for this case.
*   The patch does not fix the bug. This seems obvious, but some patches might not have been written for the development version of WordPress, yet still apply cleanly where things have changed. The patch might only fix the bug under a specific version of PHP and MySQL, or won’t fix the bug in multisite.
*   The patch introduces new errors or warning messages. Remember to test with debug turned on.
*   New [unit tests](https://make.wordpress.org/core/handbook/automated-testing/) fail with the patch applied.
*   The patch does not use appropriate [data validation and output sanitization](https://codex.wordpress.org/Data_Validation), or doesn’t make checks against user roles and capabilities when it should.
*   The patch is not adequate for any other reason not covered here. We strive for legible, efficient, and secure code in WordPress, so don’t be afraid to point out areas of a patch that should be improved, even if it does actually fix the bug.

Make sure you explain why the patch cannot be accepted in the ticket notes, in addition to removing the **has-patch** keyword and adding **needs-patch**. If, however, the patch looks good on all fronts, then you should explain what aspects of the patch you tested in the ticket notes, and triage the ticket next.

### 4\. Triage The Ticket

With both the bug and patch confirmed, the priority of the ticket often still needs to be adjusted in this workflow. We also need to decide whether the patch should be applied in the next [point release](https://make.wordpress.org/core/glossary/#point-release) (x.x.x), the next [major release](https://make.wordpress.org/core/glossary/#major-release) (x.x), or if it should still be delayed farther into the future.

**Note:** New Trac users do not have the ability to adjust the priority of a ticket or move it to a different milestone by default, so until you feel comfortable with this workflow and Trac in general, this step will require you to simply add a note to the ticket explaining that the priority or milestone should be adjusted. One of the other bug gardeners will see the update, and adjust the ticket accordingly if it looks correct. When you feel comfortable making these adjustments yourself, you can request access on the [Make WordPress Core](https://make.wordpress.org/core/) blog.

Tickets related to [regressions](https://make.wordpress.org/core/glossary/#regression) and critical bugs should be immediately set to the highest priority, and assigned to the next point release milestone. Regressions are broken features that were working perfectly fine in the latest release or the WordPress release before that, and we take these seriously. The same goes for critical bugs which may not be a regression, but still involves an aspect of a major feature being broken for a majority of users. This mostly refers to bugs with high exposure, such as breaking the public-facing side of WordPress, or major breaks in the administration panel. This should be very rare, and should be used sparingly.

Tickets involving patches that fix simple typos, add [inline documentation](https://make.wordpress.org/core/glossary/#inline-docs), or fix minor style/appearance issues, should be set to a lower priority.

All remaining tickets in this workflow should be triaged to the next major release milestone. This does not normally apply to all tickets in general, just confirmed defects with quality patches, which is all this workflow deals with. If the WordPress development cycle is in the middle of release candidates for the next major release, critical bug fixes should still be assigned to the **Next Release** milestone; however, everything else should be moved to the **Future Release** milestone, and should also be tagged with the keyword **x.x-early** (where x.x is the next major release after the one with a release candidate out). For example, during the 3.6 release candidate phase, confirmed fixes for non-critical bugs should be tagged with the **3.7-early** keyword.

## Learn More

*   [Get Involved With Trac Bug Gardening](http://helen.wordpress.com/2013/08/09/scared-of-wordpress-core-trac-but-want-to-give-it-a-shot-try-trac-gardening/)