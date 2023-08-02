# WordPress Release Team and Focus Leads

**Each new WordPress software release is a substantial undertaking that can only succeed through the dedication and support of hundreds of contributors.** 

The work can span many months and involves all areas of the global project. Each release is managed by a changing group of active contributors who take ownership of its various aspects. This group is known as the ‘Release Team’ for the particular software version. It coordinates across all the teams to connect ideas and solutions and make the release as effective as possible.

Members of each Release Team come from a variety of backgrounds and skillsets. They should have a thorough understanding of the WordPress software and the community, but also of open source web development. In addition, they have good communication and project management skills.

This page explains the various roles involved with a given release and the type of tasks involved. 

## Release Team

The main focus of the release team is to lead the release from its beginning through to launch. This requires members to act as connectors and facilitators, resolving bottlenecks and issues. 

A new release affects all the moving parts of the software. Any newly introduced, or amended feature could potentially:

*   affect existing plugins
*   have an impact on the accessibility of both front-end and back-end of the platform
*   and so much more.

It is therefore vital to have representatives from all fields of expertise in the Release Team. Each will take responsibility for a particular aspect and act as an advocate during the process. 

In addition, it is crucial that all changes are thoroughly documented. This also helps all stakeholders to be involved.

During the course of a development cycle, the Release Team is joined by hundreds of contributors. These contributors collectively work on a range of tasks, guided and mentored by both Release Team members, and other experienced contributors. 

Historically, not all releases have included representatives from every area of the platform. Minor releases may not need the involvement of all teams. Some of the most commonly seen release team roles are listed below.

## Release team roles

### Shared Responsibilities

These are tasks and responsibilities that may be documented for specific roles below but can be taken on by anyone throughout the release cycle.

*   Communicating publicly as much as possible (on tickets, in component chats, Make/Core posts, etc.)
*   Identifying blockers to progress and asking for help from buddies, team leads, and/or the Release Lead
*   Being mindful of deadlines
*   Identifying changes that require documentation, HelpHub articles, or communication to the community at large (through dev notes, marketing, etc.)
*   Leading bug scrubs focused on your team’s tickets and tasks
*   Facilitating and participating in inter-team discussions

### Release lead

**Responsibilities**

*   Set the overall goals for the release
*   Make final decisions on merging feature plugins
*   Give final review to and publishing News blog post announcing the release
*   Coordinate with Matt to select release jazz musician

### Release Coordinator

**Responsibilities**

*   Publish the weekly dev chat agendas
*   Run the weekly dev chat in [#core](https://make.wordpress.org/core/tag/core/)
*   Run various release processes in Slack (beta, release candidate, release)
*   Write blog posts for various milestones
*   Keep an eye on the deadlines in the handbook and contact the different teams involved (ping plugin, theme, ping polyglots, etc.)
*   Remind people of said deadlines
*   Take notes on the procedures outlined in the handbook to propose changes if needed
*   Facilitate inter-team discussions if needed
*   Maintain a birds-eye view of the moving parts for any red flags, blockers, or additional help needed for teams

### Core Triage Lead

**Responsibilities**

*   Run Bug Scrubs
*   Run dev chats when Release Coordinator is unavailable
*   Run various release processes in Slack with the Release Coordinator (beta, release candidate, release)
*   Attempt to triage tickets in the release’s milestone
*   Prioritize tickets to ensure that the most time-sensitive and urgent issues are given the necessary exposure within the group to garner a fast resolution
*   Communicate with component maintainers to gauge where more resources/attention is needed

### Core Tech Lead

**Responsibilities**

*   Review patches and changesets for feasibility, code quality, technical design, and coding standards compliance. Ensure they follow the overall software architecture
*   Provide a “second opinion” and technical guidance where requested or needed
*   Ensure the release cycle stages are followed by all contributors. For example, no enhancements during the beta, unless an exception was proposed and approved by project leadership
*   Ensure the beta, RC and final release processes run as smoothly as possible on the technical side, and all release steps are completed
*   This role is also responsible for escalating cases and helping to make decisions when new features, enhancements, and (large) bug-fixes are not ready in time. For example, if a new feature is not 100% complete before beta, and/or the code is still “alpha” quality and needs more work, facilitate reviews and gather more information in order to make a decision whether to proceed with the feature or add it in the next release. These cases are usually escalated to project leadership

### Core Design Lead

**Responsibilities**

*   Provide design input, guidance, and mockups for key Trac tickets

### Documentation Wrangling

**Responsibilities**

*   Keep track of changes within the release that require dev notes
*   Coordinate with the participants of those tickets with the best understanding of the changes (the committer, component maintainers, contributors owned a ticket, and lead the charge) to draft dev notes
*   Ensure all dev notes are written with enough time to proofread, reviewed, and published prior to the field guide (which publishes at the same time as release candidate 1)
*   If a ticket participant is not available to write a dev note, finding someone to write one, or writing one yourself
*   Ensure any documentation pages required for new features are created before the release
*   Write and publish the release changelog on HelpHub
*   Update WordPress versions page on the Codex

### Documentation Review

**Responsibilities**

*   Proofread and review dev notes as they are available from the Documentation Wrangling team
*   Verify code examples
*   Make suggestions for additional examples
*   Ensure the developer notes accurately and thoroughly describe the problem, solution, and identify proper usage of the changes

### MarComms (Marketing and Communications) Lead

**Responsibilities**

*   Work with leads to draft the About page seen in the WordPress Admin after upgrading
*   Work with leads to draft the WordPress.org News blog announcement post
*   [View a comprehensive guide for this role’s tasks here.](https://make.wordpress.org/marketing/handbook/resources/marketing-communicationsrelease-cycle-guide/)

### Editor Tech Lead 

**Responsibilities**

*   Loosely help define what Gutenberg features can/should get included in the release
*   Triage and review patches and PRs, test RCs, and coordinates meetings for the block editor
*   Ensure all Gutenberg features and bug fixes land on time before each Core beta/RC
*   Gather a list of important Gutenberg bugs and regressions that need to be fixed on each release. Ensure the contributors know about these and their importance (Project board)
*   Help with Gutenberg ⇔ Core sync/updates through Trac tickets
*   Make sure the Gutenberg props get collected properly
*   Make sure the Gutenberg release notes get published on time
*   Communication with the rest of the release squad about:
    *   document the updates from Gutenberg included in the release and on each Core beta/RC
    *   highlight the important features and updates for the marketing team and for the About page.
    *   co-ordination with other leads
*   Make sure Gutenberg updates get shipped in Core releases on time, with as few bugs as possible, and get communicated properly

### Editor Triage Lead

**Responsibilities**

*   Run Bug Scrubs focused on Editor items.
*   Review incoming tickets to the [Gutenberg GitHub repo](https://github.com/WordPress/gutenberg/issues) to ensure items are labeled appropriately for further review, including adding anything necessary to the appropriate release specific project board.
*   Communicate with the Core Editor Tech leads to help gauge where more resources/attention is needed.
*   Help prioritize any key issues throughout the release cycle to ensure time sensitive and urgent problems are resolved promptly.

### Editor Design Lead

**Responsibilities**

*   Provide design input, guidance, and mockups for key block editor tickets

### Accessibility Lead

**Responsibilities**

*   Set up priorities for the release and define a general scope for the accessibility focus
*   Triage all other tickets that are not in the main priority for the release and make choices based on priority/severity
*   Organize/run accessibility bug scrubs (1 accessibility focused scrub per week)
*   Contribute to tickets from various components to give accessibility feedback on both Trac and Gutenberg GitHub repository
*   Write accessibility-related documentation and publish it on Make/Core (dev notes) or HelpHub as necessary
*   Coordinate with the design and media teams to keep the release scope on its way.
*   Open tickets/issues on Trac/GitHub to handle potential accessibility regressions on all the components during the entirety of the release process
*   Communicate about the release scope and progress updates on Make/Accessibility and during core dev chats
*   Ensure patches are solid, reviewed, and committed in time
*   Contribute to ticket patches with code, tests, screenshots, code, and design reviews, etc
*   Provide accessibility-related reviews and contributions to ensure accessibility standards are met

### Default Theme

A new default theme will be bundled together with the last release of the year. This task needs a number of roles. 

#### Default Theme Design

**Responsibilities**

*   Create drafts for the default theme design, iterate on those drafts, and polish the design selected as the final candidate
*   Introduce the design on the Make Core/Make Themes blogs
*   Update the design as needed throughout the process
*   Participate in meetings (and occasionally lead them) in [#core-themes](https://make.wordpress.org/core/tag/core-themes/)
*   Contribute code to the theme, mostly front-end heavy stuff
*   Document the theme features and behavior, both to guide development (in issues and PRs) and for the support pages on WordPress.org
*   Review issues and PRs, primarily design-related ones

#### Default Theme Development

**Responsibilities**

*   Leading implementation for major designs crafted by Default Theme Design Lead
*   Providing technical guidance and review for others assisting with implementing designs from Default Theme Design Lead
*   Create issues and PR’s as I found bugs within the theme
*   Organize issues and PR’s with labels
*   Run the weekly new default theme meeting in [#core-themes](https://make.wordpress.org/core/tag/core-themes/)
*   Close duplicate issues and issues which were not within the scope of our timeline or were decided against by the [#core-themes](https://make.wordpress.org/core/tag/core-themes/) team
*   Review issues and PRs, marking them for \`commit\` them as needed
*   Approve and review default theme tickets (other than a new default theme being built for the same release) in the milestone and punt tickets when necessary
*   Manage the development of the new default theme and help everyone involved stay focused on tasks and the short timeline
*   Package the theme for upload to the theme directory for each phase of the release

#### Default Theme Wrangler

**Responsibilities**

*   Guarantee that all default themes fully support any new features added in the current release
*   Triage tickets in the Bundled Theme component in Trac
*   Manage tickets and decide what is ready, what is not, and what should not be included
*   Mark tickets for \`commit\` when they are tested and confirmed to be ready
*   Communicate with the new default theme designers and developers to use a common approach when adding support for new features

### Support

**Responsibilities**

*   Have a presence in the WordPress.org support forums during phases 2-4 of the release cycle keeping an eye on the [Alpha/Beta/RC forum](https://wordpress.org/support/forum/alphabeta/)
*   Bring any potential problems reported there to the attention of the appropriate release team member
*   Help respond to [posts with no replies](https://wordpress.org/support/view/no-replies/)
*   If you speak a language other than English, check out the [list of non-English support forums](https://make.wordpress.org/support/handbook/contributing-to-the-wordpress-forums/support-forums-in-your-language/) and provide support
*   If there are common questions appearing in the forums, bring it to the attention of the release team so that new user documentation pages can be created.

### Test

**Responsibilities**

*   Coordinating and leading efforts to increase testing of beta releases, release candidate releases, final release, and where feasible everyday trunk/nightly builds in an effort to provide real-world testing feedback to the rest of the release team.
*   Amplify testing efforts and opportunities, including helping onboard folks who are interested in helping or [doing round up posts for feature specific testing](https://make.wordpress.org/test/2021/11/30/help-test-wordpress-5-9-features/). 
*   Attend test meetings as much as possible to communicate priorities for testing to the community.
*   Work with teams to ensure any necessary testing for new features or big changes (example: [Gallery Block refactor](https://make.wordpress.org/core/2021/08/20/gallery-block-refactor-dev-note/)).
*   As possible, improve documentation for testing related items to help more folks get involved.

The section above outlines the roles for the Release Team rather than the work of the individual core teams and their work towards a release launch. To learn more about how the Make Teams contribute to the current release cycle, [visit the development blog.](https://make.wordpress.org/core/)

## Further resources

> [How the Release Cycle Works](https://make.wordpress.org/core/handbook/about/release-cycle/)

> [Releasing Major Versions](https://make.wordpress.org/core/handbook/about/release-cycle/releasing-major-versions/)