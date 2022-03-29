# Writing Patches

## Picking a ticket

*   [Pick a bug to work on](https://make.wordpress.org/core/handbook/contribute/fixing-bugs/#finding-bugs-to-fix)
*   Work on the most important bugs first
*   Make sure documentation gets updated
*   Take extra time to do it right the first time
*   Test your code
*   Regressions are bad
*   Smaller patches get reviewed faster
*   Work on multiple bugs in parallel
*   Get advice before, not after
*   More detail for these guidelines here: [Mozilla Development Strategies](https://developer.mozilla.org/en/Mozilla_Development_Strategies)
*   Review disagreements best handled quickly in [Slack](https://make.wordpress.org/chat/) with summary on [Trac](https://core.trac.wordpress.org/)

## Requirements for patches

*   Inline documentation
*   [Automated testing (spin-off)](https://make.wordpress.org/core/handbook/automated-testing/)
*   Feature requests
*   [WP\_DEBUG](https://codex.wordpress.org/Debugging_in_WordPress#WP_DEBUG), [SCRIPT\_DEBUG](https://codex.wordpress.org/Debugging_in_WordPress#SCRIPT_DEBUG)
*   Patch development scripts, and don’t minimize
*   Images (attach originals)
*   Patches should be made against the latest code in the SVN repository
*   Patches should be made against the root WordPress directory (not against a subdirectory)
*   … however, if your patch includes tests, both the code changes and tests can be included in the same patch.
*   Patches should adhere to the [coding standards](https://make.wordpress.org/core/handbook/coding-standards/)

## Expectations for patches

*   Expect rounds of feedback
*   Expect potential for rejection (wontfix, invalid, plugin, etc.)
*   Understand it may not be a priority
*   Bugs: Expect steps to reproduce
*   Enhancements: Expect request for justification
*   UI/UX: There is a separate process

## Seeking feedback

*   Slack, bump, find committer, etc.
*   Knowing where to ask for help: https://make.wordpress.org/chat/

## Helpful tools/tips/code snippets/design patterns

*   parse\_args

## Pro tips

*   Good attributes of a core contributor
    *   Brevity (Patches, Comments, Personal Agendas)
    *   Thick Skin
    *   Don’t assume everyone is stupid
    *   Do your homework (study code and history)
    *   Constraints of pragmatism and back compat
    *   Constructive criticism
    *   Humility