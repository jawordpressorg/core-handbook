<!--
# Features as Plugins
-->

# プラグインとしての機能

<!--
The Features as Plugins model was introduced in 3.7 as the way for features to be developed for inclusion in WordPress core. This model allows a feature to be built, tested, refined, and polished before it is considered as a merge candidate. Features as plugins in progress can be tracked [on a dedicated page of the Make WordPress Core blog](https://make.wordpress.org/core/features/).
-->

「プラグインとしての機能モデル」は、WordPress コアに含めるための機能を開発する方法として3.7で導入されました。このモデルでは、機能を構築し、テストし、改良し、洗練されてから、マージ候補として検討します。進行中のプラグインとしての機能は、[Make WordPress Core ブログの専用ページ](https://make.wordpress.org/core/features/)で追跡できます]。

<!--
A community member or new contributor, such as yourself, can propose an idea for a new feature plugin during the [Feature Plugin Chat](https://make.wordpress.org/core/2015/07/10/feature-plugin-chat-on-july-14/), usually held around the time a new release cycle starts.
-->

コミュニティメンバーや新しいコントリビューターは、通常新しいリリースサイクルが始まるころに開催される[機能プラグインチャット](https://make.wordpress.org/core/2015/07/10/feature-plugin-chat-on-july-14/)において、新しい機能プラグインのアイデアを提案できます。

<!--
The chat is for putting forward an idea you have, and plan on taking an active and primary role in developing. Other contributors who are interested in your idea can join the effort. The date and time of the chat are [announced in a post](https://make.wordpress.org/core/2015/07/10/feature-plugin-chat-on-july-14/) on the [Make/Core blog](https://make.wordpress.org/core/), and ideas are added in the comments in the form of a short proposal:
-->

このチャットは、あなたが持っていて、開発に積極的かつ主要な役割を果たすことを計画しているアイデアを提出するためのものです。あなたのアイデアに興味を持った他の貢献者が、その取り組みに参加できます。チャットの日時は [Make/Core ブログ](https://make.wordpress.org/core/)において[投稿で発表](https://make.wordpress.org/core/2015/07/10/feature-plugin-chat-on-july-14/)され、アイデアは短い提案書の形でコメントに追加されます。

<!--
*   A brief (one paragraph) overview of your feature plugin proposal.
*   Current plugin status (idea stage, planning stage, under development, existing feature plugin, prior work, etc).
*   A list of those involved or already interested in your feature plugin (including you).
*   What you would like help with (scoping, planning, wireframing, development, design, etc).
-->

*   提案する機能プラグインの概要 (一段落)。
*   現在のプラグインの状態 (アイデアの段階、計画の段階、開発中、既存機能のプラグイン、先行作業など)。
*   あなたの機能プラグインに関係する、またはすでに興味を持っている人たちのリスト (あなたを含みます)。
*   手伝っていただきたいこと (スコーピング、プランニング、ワイヤーフレーム、開発、デザインなど)。

<!--
The feature plugin development period allows for experimentation and, depending on the complexity of the plugin, may take multiple release cycles to complete before being ready to present to the Core team as a merge candidate.
-->

機能プラグインの開発期間は、プラグインの複雑さによっては、コアチームにマージ候補として提案する準備ができるまで、複数のリリースサイクルをかけて実験できます。

<!--
Without experimentation, some ideas might not otherwise be developed into potential features. But experimentation can also lead to a fully-scoped or even fully-developed feature that never makes it into core because, after hashing out the details, it’s realized the feature isn’t something that belongs in core.
-->

実験がなければ、アイデアは潜在的な機能として開発されないかもしれません。しかし、実験をすることで、完全に開発された機能がコアに入らないこともあります。なぜなら、詳細を検討した結果、その機能はコアにふさわしくないと分かったからです。

<!--
Don’t let that discourage you – trial and error is part of the process, and will result in better features, and a better WordPress. Features that don’t get included in core can continue to live on as awesome plugins, and the whole ecosystem benefits. In the past, the Core team would have suggested that a feature start as a plugin anyway; this process is now formalized.
-->

がっかりしないでください。試行錯誤はプロセスの一部であり、より良い機能、より良い WordPress を生み出すことになります。コアに含まれない機能は、すばらしいプラグインとして存在し続けることができ、エコシステム全体が恩恵を受けることになります。以前は、コアチームがプラグインとして始めることを提案することもありましたが、現在はこのプロセスが正式なものとなっています。

<!--
Ultimately, the decision on whether a feature makes it into core rests in the hands of the Core team. To ensure you’re on the right track, keep in contact with the lead developers and the upcoming release lead to ensure they understand what problem you’re trying to solve, and why the direction you chose is the appropriate one to solve that problem.
-->

ある機能がコアに入るかどうかの決定は、最終的にコアチームの判断に委ねられます。あなたの方向性が正しいことを確認するために、リード開発者や次期リリースリードと連絡を取り合い、あなたが解決しようとしている問題や、あなたが選んだ方向性がその問題を解決するためになぜ適切なものであるかを理解してもらうようにしましょう。

<!--
## Timeline
-->

## タイムライン

<!--
For feature plugins to be included in a release, they must be [proposed](https://make.wordpress.org/core/tag/proposal+feature-plugins/) during the kickoff of a release and be ready to merge at the beginning of the merge window. At that point, the release lead will review current feature plugins, and along with core developers, determine if they’re fully baked and ready for merging into core.
-->

機能プラグインがリリースに含まれるためには、リリースのキックオフ時に[提案](https://make.wordpress.org/core/tag/proposal+feature-plugins/)して、マージウィンドウの最初にマージできる状態である必要があります。その時点で、リリースリードは現在の機能プラグインをレビューし、コア開発者とともに、それらが完全なものでありコアにマージする準備ができているかどうかを判断します。

<!--
The release lead will look for a number of things (see the checklist below), including a strong and well-tested user experience, fully-baked design, positive feedback from the community, core-quality code, no major bugs or issues, and a belief that the feature belongs in WordPress core. Every feature is different, so “ready” will mean different things depending on the specific feature. Ultimately, a release lead must feel comfortable taking on primary responsibility for a feature, and the Core team must be comfortable taking on responsibility for the long term.
-->

リリースリードは、強力で十分にテストされたユーザー体験、完成したデザイン、コミュニティからのポジティブなフィードバック、コア品質のコード、大きなバグや問題がないこと、その機能が WordPress コアに取り込まれるべきかどうかなど、さまざまなことを確認します (以下のチェックリストを参照してください)。すべての機能は異なるため、「準備完了」の意味は特定の機能によって異なります。最終的には、リリースリードがその機能について主要な責任を引き受けられること、そしてコアチームが長期的な責任を引き受けられることが必要です。


<!--
If the core developers decide a feature isn’t ready for core, they’ll let the feature lead know why, and what can be done to prepare the feature for a future release.
-->

もしコア開発者がその機能をコアに搭載する準備ができていないと判断した場合、その理由と、将来のリリースに向けてその機能を準備するために何ができるかを、機能リードに知らせます。

<!--
Features that have been approved for inclusion will have a **merge window of about two weeks** to get their code into core and wrestle with any latent issues getting it merged. However, as stated above, features must be ready for merging at the start of the merge window.
-->

組み込まれることが承認された機能は、そのコードをコアに取り込み、マージするための潜在的な問題に取り組むための**約2週間のマージウィンドウ**を持つことになります。しかし、上に述べたように、機能はマージウィンドウの開始時にマージする準備が整っていなければなりません。

<!--
## Who is responsible for features?
-->

## 機能の責任者は誰ですか ?

<!--
After a feature gets merged into core, the **feature team remains responsible** for the feature, with added support from the Core team. As with any part of WordPress, feedback will come in from the entire community, more so after a feature is merged into core. The increased visibility requires the feature team to be more focused to ensure the feature ships.
-->

機能がコアにマージされた後も、コアチームのサポートを受けながら、**機能チームがその機能に対する責任**を負います。WordPress の他の部分と同様に、コミュニティ全体からフィードバックが寄せられますが、機能がコアにマージされた後はより多く寄せられます。可視性が高まったことで、機能チームは機能をより確実なものにするために、より集中する必要があります。

<!--
Keep in mind that while the team remains responsible for the feature in core, **ultimate decision-making rests in the hands of the Core team**, as with any part of core. The release lead will work closely with the feature lead and entire team.
-->

チームはコアの機能に対して責任を持ちますが、**最終的な意思決定はコアチーム**の手に委ねられていることを心にとどめておいてください。リリースリードは、機能リードやチーム全体と密接に連携して作業を進めます。

<!--
## Feature Plugin Merge Criteria
-->

## 機能プラグインをマージする基準

<!--
Below is a list of some of the requirements a feature plugin team should meet when developing a plugin to be merged into core. Keep in mind each feature is different and requirements will vary.
-->

以下は、プラグイン開発チームがコアにマージされるプラグインを開発する際に満たすべき要件のリストです。それぞれの機能は異なるものであり、要件も異なることを覚えておいてください。

<!--
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
-->

*   [WordPress の公式プラグインリポジトリ](https://wordpress.org/plugins/)に存在し、定期的に更新され、コミュニティによって使用・テストされているプラグイン。
*   [ウィークリーチャット](https://make.wordpress.org/core/tag/feature-plugins+chats/)が Slack で行われており、機能リードが毎週行われる core dev チャットに参加している。
*   [キックオフに関する投稿](https://make.wordpress.org/core/tag/feature-plugins+kickoff/)と[定期的な更新に関する投稿](https://make.wordpress.org/core/tag/feature-plugins+updates/)が公開され、機能プラグインの進捗と主要な決定事項を追跡している。
*   機能は、[WordPress が公式にサポートしているブラウザ](http://browsehappy.com/)のすべてで動作する。
*   タッチデバイスに関しては、すべての機能を支障なく使用でき、[Make/Flow](https://make.wordpress.org/flow/) に投稿されたすべてのデバイスにおいて、新しいインターフェースを通じた主要なフローについての視覚的な記録を持っている。[Flow チーム](https://make.wordpress.org/flow/)にレビューを依頼し、モバイルで正しく機能することを確認してください。
*   既存のインターフェースを変更したり置き換えたりする機能については、[旧フローと新フローを比較する視覚的な記録](https://make.wordpress.org/flow/tag/visual-comparison,flow-comparison/)を提供しすること。
*   [WordPress コーディング規約](https://make.wordpress.org/core/handbook/coding-standards/)に準拠したコード。
*   同様に、コードがよくテストされ、[ユニットテスト](https://make.wordpress.org/core/handbook/automated-testing/)を備えている。
*   コードは十分に文書化されている (必ず [インラインドキュメントチーム](https://make.wordpress.org/docs/handbook/core/inline-docs/) にレビューしてもらいましょう)。
*   コードは[プラグインセキュリティのベストプラクティス](https://developer.wordpress.org/plugins/security/)に従っており、セキュリティ監査を受けている。
*   ユーザーインターフェース・エクスペリエンスは、ユーザーテストによって検証され、適切なフィードバックが取り入れられている (必ず[デザインチーム](https://make.wordpress.org/design/)にレビューしてもらいましょう)。
*   デザインは、あらゆるモバイルデバイスで適切に表示される完全なレスポンシブデザインで、高解像度・レティーナディスプレイにも対応したグラフィックスを使用している。
*   HTML が適切な doctype で検証されている。
*   このコードには、ローカライズのための適切なフックがすべて用意されている (必ず [Polyglots チーム](https://make.wordpress.org/polyglots/) にレビューを依頼してください)。
*   WordPressは引き続き機能し、JavaScript をオフにした状態でも、この機能は使用可能である。
*   この機能は、キーボードだけで使用できる。
*   (これらに限定されませんが) オフスクリーンテキスト、ARIA、JS-assisted など、必要なアクセシビリティのサポートが追加されている (必ず[アクセシビリティチーム](https://make.wordpress.org/accessibility/)に聞いてください)。
*   プラグインの準備が整い次第、[Make/Core ブログ](https://make.wordpress.org/core/)に[マージの提案](https://make.wordpress.org/core/)が公開されている。

<!--
## Feature Plugin Merge Checklist
-->

## 機能プラグインをマージするためのチェックリスト

<!--
*   Make sure the feature plugin noops once the feature is merged. This means the plugin won’t [break with a Fatal Error](https://wordpress.slack.com/archives/core-restapi/p1445528753000394) after code is merged from the plugin to core. (Use `(class|function)_exists()` for example.)
*   If code from another plugin is used, [make sure there are no clashes](https://github.com/Automattic/jetpack/issues/3447) with that plugin once the feature merges.
-->

*   機能がマージされたら、機能プラグインがループしないことを確認してください。これは、プラグインからコアにコードがマージされた後に、プラグインが [Fatal Error で壊れない](https://wordpress.slack.com/archives/core-restapi/p1445528753000394)ことを意味します (たとえば `(class|function)_exists()` を使ってください)。
*   他のプラグインのコードを使用する場合は、機能がマージされた後にそのプラグインと[衝突しないことを確認](https://github.com/Automattic/jetpack/issues/3447)してください。
