# Features as Plugins

The Features as Plugins model was introduced in 3.7 as the way for features to be developed for inclusion in WordPress core. This model allows a feature to be built, tested, refined, and polished before it is considered as a merge candidate. Features as plugins in progress can be tracked [on a dedicated page of the Make WordPress Core blog](https://make.wordpress.org/core/features/).

A community member or new contributor, such as yourself, can propose an idea for a new feature plugin during the [Feature Plugin Chat](https://make.wordpress.org/core/2015/07/10/feature-plugin-chat-on-july-14/), usually held around the time a new release cycle starts.

The chat is for putting forward an idea you have, and plan on taking an active and primary role in developing. Other contributors who are interested in your idea can join the effort. The date and time of the chat are [announced in a post](https://make.wordpress.org/core/2015/07/10/feature-plugin-chat-on-july-14/) on the [Make/Core blog](https://make.wordpress.org/core/), and ideas are added in the comments in the form of a short proposal:

*   A brief (one paragraph) overview of your feature plugin proposal.
*   Current plugin status (idea stage, planning stage, under development, existing feature plugin, prior work, etc).
*   A list of those involved or already interested in your feature plugin (including you).
*   What you would like help with (scoping, planning, wireframing, development, design, etc).

The feature plugin development period allows for experimentation and, depending on the complexity of the plugin, may take multiple release cycles to complete before being ready to present to the Core team as a merge candidate.

Without experimentation, some ideas might not otherwise be developed into potential features. But experimentation can also lead to a fully-scoped or even fully-developed feature that never makes it into core because, after hashing out the details, it’s realized the feature isn’t something that belongs in core.

Don’t let that discourage you – trial and error is part of the process, and will result in better features, and a better WordPress. Features that don’t get included in core can continue to live on as awesome plugins, and the whole ecosystem benefits. In the past, the Core team would have suggested that a feature start as a plugin anyway; this process is now formalized.

Ultimately, the decision on whether a feature makes it into core rests in the hands of the Core team. To ensure you’re on the right track, keep in contact with the lead developers and the upcoming release lead to ensure they understand what problem you’re trying to solve, and why the direction you chose is the appropriate one to solve that problem.

## Timeline

For feature plugins to be included in a release, they must be [proposed](https://make.wordpress.org/core/tag/proposal+feature-plugins/) during the kickoff of a release and be ready to merge at the beginning of the merge window. At that point, the release lead will review current feature plugins, and along with core developers, determine if they’re fully baked and ready for merging into core.

The release lead will look for a number of things (see the checklist below), including a strong and well-tested user experience, fully-baked design, positive feedback from the community, core-quality code, no major bugs or issues, and a belief that the feature belongs in WordPress core. Every feature is different, so “ready” will mean different things depending on the specific feature. Ultimately, a release lead must feel comfortable taking on primary responsibility for a feature, and the Core team must be comfortable taking on responsibility for the long term.

If the core developers decide a feature isn’t ready for core, they’ll let the feature lead know why, and what can be done to prepare the feature for a future release.

Features that have been approved for inclusion will have a **merge window of about two weeks** to get their code into core and wrestle with any latent issues getting it merged. However, as stated above, features must be ready for merging at the start of the merge window.

## Who is responsible for features?

After a feature gets merged into core, the **feature team remains responsible** for the feature, with added support from the Core team. As with any part of WordPress, feedback will come in from the entire community, more so after a feature is merged into core. The increased visibility requires the feature team to be more focused to ensure the feature ships.

Keep in mind that while the team remains responsible for the feature in core, **ultimate decision-making rests in the hands of the Core team**, as with any part of core. The release lead will work closely with the feature lead and entire team.

## Feature Plugin Merge Criteria

Below is a list of some of the requirements a feature plugin team should meet when developing a plugin to be merged into core. Keep in mind each feature is different and requirements will vary.

*   A plugin exists in the [official WordPress plugin repository](https://wordpress.org/plugins/), is updated regularly, and is used/tested by the community.
*   [Weekly chats](https://make.wordpress.org/core/tag/feature-plugins+chats/) are taking place on Slack, and the feature lead is attending the weekly core dev chat.
*   A [kickoff post](https://make.wordpress.org/core/tag/feature-plugins+kickoff/) and [regular update posts](https://make.wordpress.org/core/tag/feature-plugins+updates/) are published publicly, tracking the progress and major decisions of the feature plugin.
*   The feature works in all of the [browsers that WordPress officially supports](http://browsehappy.com/).
*   Touch devices can use the entire feature with no hindrance, with visual records for major flows through all new interfaces on all devices posted on [Make/Flow](https://make.wordpress.org/flow/). Make sure it functions properly on mobile by asking the [Flow team](https://make.wordpress.org/flow/) to review it.
*   [Visual records comparing old flow with new flow](https://make.wordpress.org/flow/tag/visual-comparison,flow-comparison/) are provided for any feature that changes or replaces existing interfaces.
*   The code conforms to the [WordPress coding standards](https://make.wordpress.org/core/handbook/coding-standards/).
*   Similarly, the code is well-tested, and has [unit tests](https://make.wordpress.org/core/handbook/automated-testing/).
*   The code is well-documented. (Be sure to ask the [Inline Docs team](https://make.wordpress.org/docs/handbook/core/inline-docs/) to review it.)
*   The code follows the [plugin security best practices](https://developer.wordpress.org/plugins/security/), and has undergone a security audit.
*   The user interface/experience has been tested through user testing, and appropriate feedback was incorporated. (Be sure and ask the [Design team](https://make.wordpress.org/design/) to review it.)
*   The design is fully responsive, displaying properly on any mobile device, and using graphics that are ready for hi-dpi/retina displays.
*   HTML validates to the proper doctype.
*   The code has all of the proper hooks in place for localization. (Be sure to ask the [Polyglots team](https://make.wordpress.org/polyglots/) to review it.)
*   WordPress continues to function, and the feature is still usable, with JavaScript turned off.
*   The feature can be used with just a keyboard.
*   Any required accessibility support has been added, including (but not limited to) off-screen text, ARIA, and JS\-assisted. (Be sure to ask the [Accessibility team](https://make.wordpress.org/accessibility/) to review it.)
*   A [merge proposal](https://make.wordpress.org/core/tag/feature-plugins+merge+proposal/) has been published on the [Make/Core blog](https://make.wordpress.org/core/) once the plugin is ready.

## Feature Plugin Merge Checklist

*   Make sure the feature plugin noops once the feature is merged. This means the plugin won’t [break with a Fatal Error](https://wordpress.slack.com/archives/core-restapi/p1445528753000394) after code is merged from the plugin to core. (Use `(class|function)_exists()` for example.)
*   If code from another plugin is used, [make sure there are no clashes](https://github.com/Automattic/jetpack/issues/3447) with that plugin once the feature merges.