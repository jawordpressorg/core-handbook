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

To cover all situations, ideally each lead role in a release should have at least two people.

### Shared Responsibilities

These are tasks and responsibilities that may be documented for specific roles below but can be taken on by anyone throughout the release cycle.

*   Communicating publicly as much as possible (on tickets, in component chats, Make/Core posts, issue and PR threads on Github, etc.).
*   Identifying blockers to progress and asking for help from buddies, team leads, and/or the Release Lead.
*   Being mindful of deadlines.
*   Identifying changes that require documentation, HelpHub articles, or communication to the community at large (through dev notes, marketing, P2 posts, etc.), and communicating with the documentation team about such changes.
*   Leading bug scrubs focused on your team’s tickets and tasks.
*   Facilitating and participating in inter-team discussions.
*   Always be testing!

### Release lead

**Responsibilities**

*   Set the overall goals and main focus for the release
*   Make final decisions on merging [feature plugins](https://make.wordpress.org/core/handbook/about/release-cycle/features-as-plugins/)
*   Give final review to and publish news blog post announcing the release. Older ones can be [found on this page](https://wordpress.org/news/category/releases/)

### Release Coordination

**Responsibilities**

*   Run various release processes in Slack (beta, release candidate, release).
*   Write [blog posts for various milestones](https://make.wordpress.org/core/tag/releases/).
*   Keep an eye on the deadlines in the handbook and contact the different teams involved (ping plugin, theme, ping polyglots, etc.). Remind people of said deadlines when needed.
*   Take notes on the procedures outlined in the handbook to propose changes if needed.
*   Facilitate inter-team discussions if needed.
*   Maintain a birds-eye view of the moving parts for any red flags, blockers, or additional help needed for teams.
*   Coordinate with the WordPress Executive Director to ensure a jazz musician is selected to name the release. This involves reaching out to the WordPress Executive Director to start the process in the week before the final Release Candidate. The WordPress Executive Director will then work with Matt Mullenweg to finalize. This is only done for major releases and should be done in the week before the last planned Release Candidate. Past jazzers are documented on the [WordPress versions](https://wordpress.org/documentation/article/wordpress-versions/) page.

### Core Triage Lead

**Responsibilities**

*   [Run Bug Scrubs](https://make.wordpress.org/core/handbook/tutorials/leading-bug-scrubs/)
*   Run various release processes in Slack with the Release Coordinator (beta, release candidate, release). These are detailed in the process [detailed in this document](https://make.wordpress.org/core/handbook/about/release-cycle/releasing-major-versions).
*   Attempt to triage core tickets(in trac) in the release’s milestone
*   Prioritize tickets to ensure that the most time-sensitive and urgent issues are given the necessary exposure within the group to garner a fast resolution
*   Communicate with component maintainers to gauge where more resources/attention is needed

### Core Tech Lead

**Responsibilities**

*   Review core patches and changesets for feasibility, code quality, technical design, and [coding standards](https://developer.wordpress.org/coding-standards/wordpress-coding-standards/) compliance. Ensure they follow the overall software architecture.
*   Provide a “second opinion” and technical guidance where requested or needed.
*   Ensure the release cycle stages are followed by all contributors. For example — no enhancements during the beta, unless an exception was proposed and approved by project leadership
*   Ensure the beta, RC and final release processes run as smoothly as possible on the technical side, and all release steps are completed
*   This role is also responsible for escalating cases and helping to make decisions when new features, enhancements, and (large) bug-fixes are not ready in time. For example — if a new feature is not 100% complete before beta, and/or the code is still “alpha” quality and needs more work. In such cases, the core tech lead would facilitate reviews and gather more information to decide whether to proceed with the feature or add it in the next release. These cases are usually escalated to project leadership.

### Design Lead

**Responsibilities**

*   This role is split into two main areas – Product, and release.
    *   The “product” area comprises the work going into the actual UI/UX of WordPress.
    *   The “release” area includes coordinating release-specific materials (like the About page).
*   Provide guidance and decision-making on core and block editor tickets that need any design input.
*   Coordinate design and copy for various release assets.
    *   Guiding the creation of the highlight grid and microsite for each WordPress release. This includes the unique about page that ships with each major release, and shows up in wp-admin. Examples of previous highlight grids for reference:
        *   [6.5 microsite](https://wordpress.org/download/releases/6-5/)
        *   [6.4 microsite](https://wordpress.org/download/releases/6-4/)
        *   [6.3 microsite](https://wordpress.org/download/releases/6-3/)
    *   Work on, and provide design support for creating social media assets for each release.
    *   Decide and design the artwork for the jazz musician associated with each major release

### Documentation Wrangling

**Responsibilities**

*   [Write and publish the Field Guide](https://make.wordpress.org/core/handbook/tutorials/publishing-the-field-guide/) on RC1 release date ([Example from the WP 6.6 release](https://make.wordpress.org/core/2024/06/25/wordpress-6-6-field-guide/)) 
*   Manage [writing and publishing of dev notes](https://make.wordpress.org/core/handbook/tutorials/writing-developer-notes/)
    *   Keep track of changes within the release that require dev notes. This includes Gutenberg PRs for all releases of the plugin between two core releases
    *   Coordinate with the participants of those tickets/PRs with the best understanding of the changes (the committer, component maintainers, contributors who own a ticket/PR) to draft dev notes
    *   Ensure all dev notes are written with enough time to proofread, reviewed, and published before the Field Guide (which publishes at the same time as Release Candidate 1)
    *   Proofread and review dev notes before publication.
    *   If a ticket participant is not available to write a dev note, finding someone to write one, or writing one yourself
*   Ensure any documentation pages required for new features are created before the release. Check out the [Documentation process during a major version release](https://make.wordpress.org/docs/handbook/workflows/documentation-process-during-a-major-version-release/) to prepare for release day.

### MarComms (Marketing and Communications) Lead

**Responsibilities**

*   Collaborate with release leads and contributors to draft Marketing and Communications (MarComms) deliverables, including:
    *   Beta & Release Candidate announcement posts
    *   General release announcement post
    *   About page and microsite content
*   Ensure the content for these deliverables is written and ready for proofreading and review with enough time, follows the [WordPress.org Brand Writing Style Guide](https://make.wordpress.org/marketing/handbook/resources/style-guide-and-brand-book/), and accurately reflects the release features and benefits.
*   Collaborate with release design contributors on creative and visual assets such as the highlight grid, featurettes, and/or other social media visuals for release marketing and communication purposes.
*   Help develop or collaborate with marketing contributors on a social media posting plan to promote the release milestones and key features.
*   For a comprehensive guide to this role’s tasks, visit the [Marketing Communications Release Cycle Guide](https://make.wordpress.org/marketing/handbook/resources/marketing-communications-release-cycle-guide/).

### Editor Tech Lead 

**Responsibilities**

*   Loosely help define what Gutenberg features can/should get included in the release
*   Triage and review patches and PRs, test RCs, and coordinates meetings for the block editor
*   Ensure all Gutenberg features and bug fixes land on time before each Core beta/RC
*   Gather a list of important Gutenberg bugs and regressions that need to be fixed on each release. Ensure the contributors know about these and their importance ([Project board example](https://github.com/orgs/WordPress/projects/179))
*   Help with Gutenberg ⇔ Core sync/updates through Trac tickets ([More details here](https://make.wordpress.org/core/handbook/about/release-cycle/block-editor-release-process-for-major-releases/))
*   Make sure the Gutenberg props get collected properly
*   Communication with the rest of the release squad about:
    *   Documenting the updates from Gutenberg included in the release and on each Core beta/RC
    *   Highlighting the important features and updates for the marketing team and for the About page.
    *   Co-ordination with other leads
*   Make sure Gutenberg updates get shipped in Core releases on time, with as few bugs as possible, and get communicated properly. 
*   Communication with all contributors to get features and enhancements ready in time, help them out if needed.

### Editor Triage Lead

**Responsibilities**

*   This role is similar to the Core triage lead role, but focuses mainly on the development of the block editor, and integrating it in core releases.
*   Run Bug Scrubs focused on Editor items. This is done in the [#core-editor](https://make.wordpress.org/core/tag/core-editor/) channel on Slack.
*   Review incoming tickets to the [Gutenberg GitHub repo](https://github.com/WordPress/gutenberg/issues) to ensure items are labeled appropriately for further review, including adding anything necessary to the appropriate release specific project board.
*   Communicate with the Core Editor Tech leads to help gauge where more resources/attention is needed.
*   Help prioritize any key issues throughout the release cycle to ensure time sensitive and urgent problems are resolved promptly.

This work is done in collaboration and coordination with the Core Tech leads so please refer to [Block Editor Release Process for Major Releases](https://make.wordpress.org/core/handbook/about/release-cycle/block-editor-release-process-for-major-releases/) for a more detailed and practical look.

### Accessibility Lead

**Responsibilities**

*   Set up priorities for the release and define a general scope for the accessibility focus
*   Triage all other tickets that are not in the main priority for the release and make choices based on priority/severity
*   Organize/run accessibility bug scrubs (1 accessibility focused scrub per week)
*   Contribute to tickets from various components to give accessibility feedback on both Trac and Gutenberg GitHub repository
*   Write accessibility-related documentation and publish it on Make/Core ([dev notes](https://make.wordpress.org/core/handbook/tutorials/writing-developer-notes/)) or [HelpHub](https://wordpress.org/documentation/) as necessary
*   Coordinate with the design and media teams to keep the release scope on its way.
*   Open tickets/issues on Trac/GitHub to handle potential accessibility regressions on all the components during the entirety of the release process
*   Communicate about the release scope and progress updates on Make/Accessibility and during core dev chats
*   Ensure patches are solid, reviewed, and committed in time
*   Contribute to ticket patches with code, tests, screenshots, code, and design reviews, etc
*   Provide accessibility-related reviews and contributions to ensure accessibility standards are met

### Performance Lead

**Responsibilities**

*   Set up priorities for the release and define a general scope for the [performance focus](https://core.trac.wordpress.org/query?status=accepted&status=assigned&status=new&status=reopened&status=reviewing&focuses=~performance) by estimating both horizontal impact (“how many sites does this apply to?”) and vertical impact (“how much does this improve performance for sites where it applies?”)
*   Regularly triage tickets in the milestone that fall outside of the main priorities, following up with the reporter and other contributors involved
*   Assess feasibility of committing a fix for specific tickets in the current release cycle, based on priority, severity, effort and time needed, contributor availability, time left in the cycle
*   Join or lead regular performance bug scrubs and other [performance related meetings](https://make.wordpress.org/performance/#block-3)
*   Benchmark performance of relevant pull requests / patches from various components (in both [Trac](https://core.trac.wordpress.org/) and [Gutenberg](https://github.com/WordPress/gutenberg/issues)), both proactively and on demand, focusing primarily on tickets that are one of the following:
    *   A new feature or API planned for the release
    *   A performance enhancement or fix that is intended to improve performance
    *   Another change that suggests to have a measurable performance impact (whether positive or negative)
*   Work with team members to ensure [performance measurement best practices](https://make.wordpress.org/performance/handbook/measuring-performance/) are followed and clearly communicated
*   Monitor the [WordPress core performance dashboard](https://www.codevitals.run/project/wordpress) regularly to identify potential performance regressions and report them back to the relevant ticket for which the underlying change was committed
*   Coordinate with other release leads, primarily the Core Tech and Editor Tech Leads to support their priorities with performance guidance
*   Communicate about the release scope and progress updates in the release leads Slack channel and during core dev chats
*   Work with the Documentation Lead to ensure timely publishing of performance related dev note posts prior to or early in the beta phase
*   Support team members contributing to tickets in the performance focus, e.g. through triaging, coordinating team members to help with feedback, code review, and benchmarking, as well as guidance on communication and documentation related tasks such as enhancing WordPress core documentation or writing dev notes
*   Coordinate the contributions to tickets, pull requests/patches, tests, performance benchmarks, code reviews, etc.
*   Run benchmarks to assess the performance of the release compared to the previous stable release, once the Beta or RC is available
*   Draft and publish a Make Core post highlighting the release’s performance improvements and sharing key metrics from the benchmarks

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

*   Guarantee that all default themes fully support any new features added in the current release (as deemed appropriate).
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

[#core](https://make.wordpress.org/core/tag/core/)