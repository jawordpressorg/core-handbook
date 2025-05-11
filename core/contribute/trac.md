<!--
# The Bug Tracker (Trac)
-->

# バグトラッカー (Trac)

<!--
[Trac](https://core.trac.wordpress.org/) is an open source project that serves as a bug tracker and project management tool for WordPress. Using Trac, developers can browse source code history as well as manage bug reports and feature development.
-->

[Trac](https://core.trac.wordpress.org/) は、WordPress のバグトラッカーおよびプロジェクト管理ツールとして機能するオープンソースプロジェクトです。Trac を使用することで、開発者はソースコードの履歴を閲覧するだけでなく、バグレポートや機能開発を管理できます。

<!--
[Tickets](https://make.wordpress.org/core/glossary/#ticket) are used for both bug reports and feature development, and may be created by anyone with a WordPress.org account.
-->

[チケット](https://make.wordpress.org/core/glossary/#ticket)は、バグレポートと機能開発の両方に使用され、WordPress.org のアカウントを持っている人なら誰でも作成できます。

<!--
## Ticket Properties
-->

## チケットのプロパティ

<!--
Tickets are assigned numerous properties that provide a snapshot of the status of the ticket.
-->

チケットには、チケットのステータスのスナップショットを提供する多くのプロパティが割り当てられています。

<!--
**Title and Description:** Provide a strong title and clear description. For the title, it is generally best to describe the problem, not a solution. Concentrating on the problem, rather than the solution, is a good mantra in general. For the description, it is generally best to include steps to reproduce, and actual versus expected results (for bugs), and proper rationale (for enhancements).
-->

**タイトルと説明:** 明確なタイトルと説明を提供します。タイトルについては、一般的に、解決策ではなく問題を記述することが最善です。解決策ではなく問題に集中することは、一般的に良いことです。説明には、一般的に、再現手順や期待される結果 (バグの場合)、適切な根拠 (機能強化の場合) を含めるとよいでしょう。

<!--
**Type:** A ticket falls under one of four types: defect (bug), enhancement, feature request, and task (blessed).
-->

**Type:** チケットは、defect (bug)、enhancement、feature request、task (blessed) の4つのタイプのいずれかに分類されます。

<!--
*   **Defect (bug):** A bug is an error or unexpected result. Performance improvements and code optimization are considered enhancements, not defects. After feature freeze, only bugs are dealt with, with regressions (adverse changes from the previous version) being the highest priority.
*   **Enhancements:** These are simple improvements to WordPress, such as the addition of a hook or an improvement to an existing feature.
*   **Feature requests:** These are proposals for new features. Feature proposals should generally begin the process in the ideas forum, on a mailing list, as a plugin, or brought to the attention of the core team, such as through scope meetings held for each major release. Unsolicited tickets of this variety are typically, therefore, discouraged.
*   **Tasks (blessed):** Feature development for the upcoming major release centers around task tickets, which are major features or important enhancements that have been blessed by the core team. A ticket should otherwise never receive this designation.
-->

*   **Defect (bug):** バグとは、エラーや予期せぬ結果のことです。パフォーマンスの改善やコードの最適化は、不具合ではなく、機能強化とみなされます。機能フリーズ後は、バグのみを処理し、リグレッション (前バージョンからの望ましくない変更) を最優先とします。
*   **Enhancements:** フックの追加や既存機能の改善など、WordPress の簡単な改善です。
*   **Feature requests:** これらは新機能の提案です。機能の提案は通常、アイデアフォーラムやメーリングリストで、またプラグインとして、またはメジャーリリースごとに開催されるスコープミーティングなどを通じてコアチームの注意を喚起することから始める必要があります。この種の一方的なチケットは、通常は推奨されません。
*   **Tasks (blessed):** 次のメジャーリリースのための機能開発は、コアチームによって承認された主要機能または重要な機能強化であるタスクチケットを中心に行われます。それ以外のチケットは、この指定を受けるべきではありません。

<!--
**Milestone:** The milestone is the WordPress release where that ticket is expected to be resolved, such as 3.7. By default, all tickets are assigned, upon creation, to the **Awaiting Review** milestone to prevent [scope creep](https://make.wordpress.org/core/glossary/#scope-creep). Only [committers](https://make.wordpress.org/core/handbook/about/organization/#the-wordpress-core-team) or [trusted core contributors](https://make.wordpress.org/core/handbook/about/organization/#contributing-developers) have the ability to change milestones.
-->

**Milestone:** マイルストーンは、そのチケットが解決されると予想される WordPress のリリースで、たとえば3.7などです。デフォルトでは、[スコープクリープ](https://make.wordpress.org/core/glossary/#scope-creep)を防止するために、すべてのチケットは作成時に **Awaiting Review** マイルストーンに割り当てられます。マイルストーンを変更できるのは、[コミッター](https://ja.wordpress.org/team/handbook/core/about/organization/#the-wordpress-core-team)または[信頼できるコア貢献者](https://ja.wordpress.org/team/handbook/core/about/organization/#core-contributors) のみです。

<!--
**Keywords:** After the milestone, the keywords field is the most important field. These are not like tags on a WordPress post, but rather a defined list of keywords that describe the ticket’s current status in our development workflow. We use these keywords to build important reports. As an example, tickets tagged with **needs-design-feedback** are pulled into a report on which the Design team heavily relies. See [Trac Workflow Keywords](https://make.wordpress.org/core/handbook/trac/keywords/) for a complete list of the keywords.
-->

**Keywords:** マイルストーンに続いて、キーワードフィールドは最も重要なフィールドです。これらは WordPress の投稿タグのようなものではなく、私たちの開発ワークフローにおけるチケットの現在の状態を説明するキーワードの定義リストです。私たちはこれらのキーワードを使用して、重要なレポートを作成します。たとえば、**needs-design-feedback** とタグ付けされたチケットは、デザインチームが大きく依存しているレポートに取り込まれます。キーワードの完全なリストは [Trac ワークフローキーワード](https://ja.wordpress.org/team/handbook/core/trac/keywords/)を参照してください。

<!--
**Component:** The component is the area of WordPress that the ticket affects. The UI team, for example, will often be working on tickets in the **Graphic Design**, **UI**, or **Accessibility** categories. Try to choose specific components (when applicable) over more generalized ones, such as **General** or **Administration**. Components are used in reports to provide a logical grouping of tickets by subject area.
-->

**Component:** コンポーネントは、チケットが影響する WordPress の範囲です。たとえば UI チームは、**Graphic Design**、**UI**、**Accessibility** のカテゴリーでチケットに取り組むことがよくあります。**General** や **Administration** などの一般的なコンポーネントよりも、特定のコンポーネント (該当する場合) を選択するようにしてください。コンポーネントは、チケットをテーマ別に論理的なグループ化を行うためにレポートで使用されます。

<!--
Tickets for core plugins, such as the importers, are managed under the **Plugins** or **Import** components, and current and former default themes are managed under the **Bundled Theme** component.
-->

インポーターなどのコアプラグインのチケットは **Plugins** または **Import** コンポーネントで管理され、現在および以前のデフォルトのテーマは **Bundled Theme** コンポーネントで管理されます。

<!--
Issues with the WordPress.org site were formerly managed on the same Trac as WordPress core. As of June 2013, [meta.trac.wordpress.org](https://meta.trac.wordpress.org/) is now the proper, canonical place for bug reports to be filed that are related to the WordPress.org site. See the [full components list](https://meta.trac.wordpress.org/#WhatcomponentsfallunderMeta) to determine if your issue should be reported there.
-->

WordPress.org サイトの問題は、以前は WordPress core と同じ Trac で管理されていました。2013年6月現在、WordPress.org サイトに関連するバグレポートは [meta.trac.wordpress.org](https://meta.trac.wordpress.org/) が正式な場所となりました。あなたの問題をそこで報告するべきかどうかを判断するには、[フルコンポーネントリスト](https://meta.trac.wordpress.org/#WhatcomponentsfallunderMeta)を参照してください。

<!--
**Resolution:** Upon one or more commits to the codebase, a ticket may be closed as **fixed**. Not all tickets result in a commit, however, and may be closed for other reasons:
-->

**Resolution:** コードベースへの1回以上のコミットにより、チケットは **fixed** としてクローズされることがあります。しかし、すべてのチケットがコミットに至るわけではなく、他の理由でクローズされる場合もあります。

<!--
*   **duplicate:** The ticket is a duplicate of an existing ticket, which will be referenced by the contributor closing the ticket.
*   **invalid:** The ticket is not a bug, or is a support request.
*   **worksforme:** The bug reported in the ticket cannot be reproduced. Sometimes, an existing plugin, hook, or feature may render the ticket moot, so the ticket can be closed without further action.
*   **wontfix:** The ticket will not be addressed. Occasionally, bugs are considered to be acceptable edge cases, and will not be addressed further. This is sometimes used when a request for an enhancement or feature has been rejected for core inclusion.
*   **maybelater:** Similar to **wontfix**, **maybelater** is used for a ticket that, while perhaps not outright rejected, has no current traction.
*   **reported-upstream:** The ticket is for an external library or component, has been reported in an upstream repository (e.g. Gutenberg), and will be addressed there.
-->

*   **duplicate:** このチケットは既存のチケットと重複しており、貢献者はこのチケットを閉じることで参照されることになります。
*   **invalid:** このチケットは、バグやサポートリクエストではありません。
*   **worksforme:** チケットで報告されたバグが再現されません。既存のプラグインやフック、機能によってチケットの意味がなくなり、チケットはそのまま閉じられることがあります。
*   **wontfix:** このチケットは取り組まれません。時には、バグが許容できるエッジケースであると見なされ、それ以上対処されないこともあります。これは、拡張や機能の要求がコアに含まれることを拒否されたときに使われることがあります。
*   **maybelater:** **wontfix** と同様に、**maybelater** は、おそらく完全には拒否されていないものの、現在活発ではないチケットに使用されます。
*   **reported-upstream:** このチケットは外部のライブラリやコンポーネントに関するもので、上流のリポジトリ (例: Gutenberg) で報告されており、そこで対処されます。

<!--
There is certainly some overlap among these five resolutions. It is not an exact science.
-->

これらの5つの分類は重なる部分もありますが、チケットの分類に正解はありません。

<!--
**Severity and Priority:** The [severity](https://make.wordpress.org/core/glossary/#severity) is the seriousness of the ticket in the eyes of the reporter. The [priority](https://make.wordpress.org/core/glossary/#priority-bug-tracker) is the seriousness of the ticket in the eyes of the project. Generally, severity is a judgment of how bad a bug is, while priority is its relationship to other bugs. Only [committers](https://make.wordpress.org/core/handbook/about/organization/#the-wordpress-core-team) and [trusted core contributors](https://make.wordpress.org/core/handbook/about/organization/#contributing-developers) have the ability to modify the priority.
-->

**Severity and Priority:** [Severity](https://make.wordpress.org/core/glossary/#severity) は報告者の目から見たチケットの重要度です。[Priority](https://make.wordpress.org/core/glossary/#priority-bug-tracker) はプロジェクト全体から見たチケットの優先度です。一般的に、重要度はバグがどの程度悪いかを判断するためのものであり、優先度は他のバグとの関係です。優先度を変更できるのは[コミッター](https://ja.wordpress.org/team/handbook/core/about/organization/#the-wordpress-core-team)と[信頼されたコア貢献者](https://ja.wordpress.org/team/handbook/core/about/organization/#core-contributors)だけです。

<!--
**Version:** The version of WordPress being used. Ideally, this would be the earliest affected or applicable version. It should not be updated to a later version once set, as we utilize this to track the age of tickets and bugs, regressions, and the like.
-->

**Version:** 使用している WordPress のバージョン。理想的には、影響を受けているまたは適用可能な最も古いバージョンであることです。チケットやバグ、リグレッションなどの経過を追跡するために利用するため、一度設定したらそれ以降のバージョンに更新してはいけません。

<!--
### Roles
-->

### 役割

<!--
Individuals have three roles on Trac tickets:
-->

Trac のチケットでは3つの役割が存在します。

<!--
**Reporter:** The person who opened the ticket.
-->

**Reporter:** チケットをオープンした人。

<!--
**Owner:** This field is typically left blank, even if you have contributed a patch. The Owner field is used by committers and trusted core contributors to accept and assign tickets among themselves. Committers utilize the field to offer traction for a ticket, to identify they are investigating, committing, or otherwise following a ticket, or to tentatively accept the bug or enhancement for core inclusion. It is also common during the feature development phase for developers to accept tasks in the area of responsibility for which they have volunteered, as well as related bug reports. Trusted contributors may assign tickets to others based on an inside knowledge of who should be responsible for reviewing it.
-->

**Owner:** このフィールドは、たとえあなたがパッチを提出していたとしても、通常は空白のままです。Owner フィールドは、コミッターと信頼されたコア貢献者によって、チケットの受け入れと割り当てのために使用されます。コミッターはこのフィールドを利用して、チケットに取り組むことを申し出たり、チケットの調査やコミット、その他のフォローをしたり、バグや機能強化をコアに取り込むことを暫定的に受け入れたりします。また機能開発の段階では、開発者が自発的に担当した分野のタスクや関連するバグレポートを受け入れることもあります。信頼できる貢献者は、誰がそのレビューに責任を持つべきかという自身の知識にもとづいて、他の人にチケットを割り当てるかもしれません。

<!--
**CC:** As long as your email address is [configured in Trac preferences](https://make.wordpress.org/core/handbook/working-with-trac/opening-a-ticket/#getting-started), you’ll receive email updates for any tickets you’ve created or ones you’ve commented on. The field is generally a visual confirmation you are adding yourself to the ticket and wish to receive updates. From time to time, it may make sense to add other individuals to the CC field, such as when a committer requests this. It should be noted that most committers and core developers read every ticket and comment anyway.
-->

**CC:** あなたのメールアドレスが [Trac preferences で設定](https://ja.wordpress.org/team/handbook/core/working-with-trac/opening-a-ticket/#getting-started)されていると、あなたが作成したチケットやあなたがコメントしたチケットの更新情報をメールで受け取ることができます。このフィールドは一般的に、あなたがチケットに自分自身を追加し、更新を受け取ることを希望していることを視覚的に確認するためのものです。時々、コミッターから要求された場合など、他の人を CC フィールドに追加することが意味を持つことがあります。ほとんどのコミッターとコア開発者は、すべてのチケットとコメントを読んでいることに注意してください。

<!--
## Triaging and Punting
-->

## トリアージと移動

<!--
New tickets are automatically assigned to the **Awaiting Review** milestone. Upon initial review, it may be recommended for closure, or require more feedback from the reporter or a core developer. Keywords often used here are **2nd-opinion**, **close**, **reporter-feedback**, and **dev-feedback**.
-->

新しいチケットは、自動的に **Awaiting Review** マイルストーンに割り当てられます。最初のレビューでは、クローズすることが推奨されたり、報告者やコア開発者からのフィードバックが必要だったりします。ここでよく使われるキーワードは **2nd-opinion**、**close**、**reporter-feedback**、**dev-feedback** です。

<!--
It may also be moved to a milestone by a committer or trusted core contributor:
-->

また、コミッターや信頼できるコア貢献者によってマイルストーンに移動されることもあります。

<!--
*   **The next point release milestone** (for example, 3.6.2 if the current release is 3.6.1) is for critical bugs and regressions. Our point releases are only for security fixes, critical bugs, and regressions in behavior from the previous version of WordPress. We do not fix regular bugs or enhancements in these releases.
*   **The next major release milestone** (for example, 3.7 if the current release is 3.6.1) is for tasks and features slated for the release, bugs affecting those features, and regressions in the current alpha or beta version over the latest release. Existing bugs may also be addressed, but this generally won’t be considered until a solution exists, unless the bug is sufficiently major to warrant priority. Enhancements may also be included at the discretion of committers, but only during alpha development (prior to the beta release). Larger enhancements are generally not considered for the next major release as they are out of scope.
*   **The Future Release milestone** is reserved for other tickets. It’s been determined as a potentially good enhancement or confirmed as a bug, but it is not slated for the next release of WordPress.
-->

*   **The next point release milestone** (たとえば、現在のリリースが3.6.1の場合、3.6.2) は、重大なバグとリグレッションのためのものです。ポイントリリースは、セキュリティ修正、重大なバグ、旧バージョンの WordPress からのリグレッションのみを対象としています。これらのリリースでは、通常のバグ修正や機能強化は行いません。
*   **The next major release milestone** (たとえば、現在のリリースが3.6.1の場合、3.7) は、リリース予定のタスクや機能、それらの機能に影響を与えるバグ、現在のアルファ版やベータ版の最新リリースに含まれるリグレッションが対象です。既存のバグが含まれることもありますが、そのバグが重大で優先すべきものでない限り、解決策が見つかるまで考慮されないことが一般的です。コミッターの判断で機能強化を含めることもできますが、アルファ版の開発中 (ベータ版のリリース前) に限ります。大規模な機能強化は通常スコープ外であるため、次のメジャーリリースでは検討されません。
*   **The Future Release milestone** は、他のチケットのために予約されています。潜在的に良い機能強化と判断されたり、バグと確認されたりしていますが、WordPress の次のリリースに予定されているわけではありません。

<!--
### Giving Feedback
-->

### フィードバックする

<!--
When reviewing a ticket, here’s your primary goal: participate in a constructive dialog with the reporter to get the ticket to some form of resolution. The resolution doesn’t need to be immediate, although it’s fun when it is – slow and steady progress is the name of the game. If you’re new to this, here’s some tips on how you might approach and handle a ticket.
-->

チケットをレビューする際の主な目標は以下の通りです。報告者と建設的な対話をし、チケットを何らかの形で解決に導くことです。解決されることはうれしいですが、すぐに解決する必要はなく、ゆっくり着実に進めていくことが大切です。初めての方は、チケットにどのようにアプローチし、対処するか、いくつかのヒントをご覧ください。

<!--
When giving feedback for a ticket:
-->

チケットに対してフィードバックする場合:

<!--
*   Thank the individual for the report. Some of these tickets are quite old; for those, a simple “Thanks for the report nacin. Sorry you never got a response.” is fine.
*   If this was one of the reporter’s first tickets, it will tell you above the comment box. Be nice. 🙂
*   If it’s a support request, you can refer them to the WordPress.org support forums and close the ticket as “invalid”.
*   If it’s a bug report that sounds like an enhancement, then change the ticket to an enhancement. Enhancements are a bit more difficult to triage (as the feedback is more subjective), so it’s much easier to start with bugs.
*   Consider a quick search to see if it is a duplicate of another ticket that may be farther along.
*   If there’s a component that is more appropriate for the ticket, feel free to move it.
-->

*   本人に対して、報告のお礼を言う。これらのチケットの中には、かなり古いものもあります。そのような場合は、「nacin さん、報告ありがとうございます。返信をしなくてすいません。」と言うだけで十分です。
*   報告者の初めてのチケットであった場合、コメント欄の上に表示されます。すばらしいですね。🙂
*   サポート依頼であれば、WordPress.org のサポートフォーラムを紹介し、チケットを「無効」として閉じることができます。
*   もし、バグレポートが機能強化のように見えるであれば、チケットを機能強化に変更します。機能強化はトリアージがやや難しいので (フィードバックがより主観的であるため)、バグから始めるほうがはるかに簡単です。
*   他のチケットと重複していないか、一度検索してみてください。
*   もし、このチケットにもっとふさわしいコンポーネントがあれば、遠慮なく移動してください。

<!--
If it’s a bug report:
-->

バグレポートの場合:

<!--
*   See if you can still reproduce it in trunk, and/or try the latest stable release. Some bug reports may have been invalid to begin with; others might have been fixed already.
*   If, when reproducing it, you feel you can elaborate on the issue, or write clearer steps to reproduce, please do so.
*   If you can’t reproduce it, ask the reporter for more information and add the **reporter-feedback** keyword. If you think the ticket should be closed, you can mark it with the **close** keyword. (There doesn’t need to be a rush to close the ticket.)
*   Reproducible bugs need patches (and unit tests, if applicable)!
-->

*   trunk で再現できるかどうか、最新の安定版リリースを試してみてください。バグレポートの中にはそもそも無効なものもあるかもしれませんし、すでに修正されているものもあるかもしれません。
*   再現するために、問題を詳しく説明したり、再現するための明確な手順を書くことができる場合は、ぜひそうしてください。
*   再現できない場合は、報告者に詳細を尋ね、**reporter-feedback** キーワードを追加してください。もしそのチケットがクローズされるべきだと思ったら、**close** キーワードでマークしてください (チケットのクローズを急ぐ必要はありません)。
*   再現性のあるバグにはパッチ (場合によってはユニットテストも) が必要です !

<!--
If it has a patch:
-->

パッチの場合:

<!--
*   Test it out – does it fix the problem? How did you test it? Did you notice any side effects?
*   If the patch doesn’t apply cleanly (as in, it fails when you try), add the **needs-refresh** keyword.
*   If you’re a developer, consider doing even just a cursory code review. Make sure it follows [WordPress coding standards](https://make.wordpress.org/core/handbook/coding-standards/).
*   If the **has-patch** workflow keyword is missing, add it. Or, if after review you don’t find the patch to be sufficient, you can set it to **needs-patch** instead.
*   If the patch touches on any WordPress internals, it probably needs [unit tests](https://make.wordpress.org/core/handbook/automated-testing/).
*   If you feel the patch is ready to be reviewed by a core developer to be considered for inclusion in WordPress, simply say so in a comment. Up until beta 1, you can file it against the current milestone. After beta 1, file it against **Future Release** with an **early** tag.
-->

*   テストしてみてください - それは問題を解決しますか ? どのようにそれをテストしましたか ? 何か副作用はありましたか ?
*   パッチがきれいに適用されない場合 (試したときに失敗するような場合) は、**needs-refresh** キーワードを追加してください。
*   もしあなたが開発者なら、ざっとコードレビューすることを検討してください。それが [WordPress コーディング規約](https://ja.wordpress.org/team/handbook/core/coding-standards/)に沿っているかどうか確認してください。
*   **has-patch** というワークフローキーワードがない場合は、追加してください。また、レビューの結果パッチが十分でないと判断した場合は、代わりに **needs-patch** と設定できます。
*   もしパッチが WordPress の内部構造に関わっているなら、おそらく[ユニットテスト](https://ja.wordpress.org/team/handbook/core/automated-testing/)が必要でしょう。
*   パッチがコア開発者がによってレビューされ、WordPress に含めることを検討する準備ができたと感じたら、コメントでそう言ってください。ベータ1までは、現在のマイルストーンに対してパッチを申請できます。ベータ1以降は、**Future Release** と **early** タグを付けてください。

<!--
It might take only a few minutes to triage some of the more straightforward tickets, especially once you get the hang of it. You could easily spend twenty or thirty minutes on others, or even longer if there’s a lot to test or if you have a lot of feedback to give.
-->

一度コツをつかめば、より簡単なチケットのトリアージには数分しかかからないかもしれません。20～30分はかかることもあるでしょうし、テストすることがたくさんあったり、フィードバックがたくさんある場合は、もっとかかるでしょう。

<!--
If you come across a ticket you like and want to write a patch for it, that’s great! Feel free to leave feedback on the ticket and start working on a patch.
-->

もし、あなたが気に入ったチケットを見つけ、そのチケットのパッチを書きたいと思ったら、それはすばらしいことです。そのチケットにフィードバックを残し、パッチの作成に取りかかることができます。

<!--
Triaging can be a great way to find tickets that interest you. You might find yourself timid to start – if so, find a buddy in [#core](https://wordpress.slack.com/messages/core/) and work collaboratively until you get comfortable.
-->

トリアージは、あなたが興味を持つチケットを見つけるためのすばらしい方法です。最初は戸惑うかもしれませんが、もしそうであるなら、[#core](https://wordpress.slack.com/messages/core/) で仲間を見つけ、慣れるまで共同作業をしてみてください。

<!--
### Punting Tickets
-->

### チケットの移動

<!--
Tickets are *punted* when they are moved out of a minor or major release milestone to a future milestone. This generally happens at different intervals in the cycle to lower priority tickets. Some tickets are individually deemed as too complex or out of scope, and are therefore moved.
-->

チケットは、マイナーまたはメジャーリリースのマイルストーンから将来のマイルストーンに変更されたときに、「移動」されます。これは一般に、優先度の低いチケットに対してサイクルの異なる間隔で起こります。いくつかのチケットは、個別に複雑すぎる、または範囲外であると判断され、移動されます。
