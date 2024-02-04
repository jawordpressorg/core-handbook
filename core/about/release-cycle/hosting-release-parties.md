<!--
# Hosting Release Parties
-->

# リリースパーティーの開催

<!--
The [WordPress release cycle](https://make.wordpress.org/core/handbook/about/release-cycle/) has several milestones. Once the release hits Beta status, release parties happen in the [#core](https://wordpress.slack.com/archives/C02RQBWTW) Slack channel. These parties step through the various release tasks required to create a public release.
-->

[WordPress のリリースサイクル](https://ja.wordpress.org/team/handbook/core/about/release-cycle/)にはいくつかのマイルストーンがあります。リリースがベータステータスになると、[#core](https://wordpress.slack.com/archives/C02RQBWTW) Slack チャンネルでリリースパーティが行われます。これらのパーティは、公開リリースを作成するために必要なさまざまなリリースタスクを段階的に進めていきます。

<!--
A more technical Handbook page about the process for [Releasing Beta Versions](https://make.wordpress.org/core/handbook/about/release-cycle/releasing-beta-versions/) has technical instructions for committers and Mission Control. This page exists as a guide for the host, or “emcee”, of release parties, and it omits most of the technical detail that’s not needed to facilitate the release process itself.
-->

[ベータ版のリリース](https://ja.wordpress.org/team/handbook/core/about/release-cycle/releasing-beta-versions/)のプロセスについてのより技術的なハンドブックページには、コミッターとミッションコントロールのための技術的な手順が記載されています。このページはリリースパーティのホスト、つまり「司会者」のためのガイドとして存在しており、リリースプロセスそのものを促進するために必要でない技術的な詳細のほとんどは省略されています。

<!--
This page should be updated as processes are improved after receiving feedback from contributors.
-->

このページは、貢献者からのフィードバックを受けてプロセスが改善されたときに更新されるはずです。

<!--
## Roles needed during a release party
-->

## リリースパーティで必要な役割

<!--
Note: Some or all of these roles may be performed by the same contributor, depending on availability.
-->

備考: これらの役割の一部または全部は、都合により同じ貢献者が行う場合があります。

> **Note**
> 「Host script based on Beta releases (ベータリリースにもとづく開催スクリプト)」のセクションは、GitHub 原文ではセル内で改行されており、またインラインハイライトが使用されています。どちらもマークダウン上では利用出来ないため、セル内の改行については `<br />` タグに置き換えています。このセクションの更新を WordPres ページに反映するときは、原文を参照の上、適切に改行・ハイライトを行って下さい。

<!--
*   **A Party Host** (referred to as `@emcee` in this document). Typically, this is one of the release coordinators. If a release coordinator is not available, an alternate from the release squad can fill in. As a last resort, the role can be filled by a trusted contributor not part of the current squad.
*   **A Core Committer** (`@corecommitter`). This contributor will perform the “version bump” actions. The current list of core committers can be found [here](https://make.wordpress.org/core/handbook/about/organization/#committers).
*   **A member of the Security Team** (`@securityteammember`). This contributor will verify that the non-public security tests pass for the latest set of code set to be released.
*   **A person with Mission Control access** (`@mcpilot`). A contributor with this level of access is needed to package the release and refresh the nightly. The list of active contributors with this access is very small, so finding a person to fill this role ahead of time is crucial.
*   **A member of the marketing team, or a marketing release lead** (`@marketingteamember`). The person in charge of drafting the release announcement post.
-->

*   **パーティのホスト** (このドキュメントでは `@emcee`)。通常、これはリリースコーディネーターの一人です。リリースコーディネーターが不在の場合は、リリースチームからの誰かがその役割を果たすことができます。最後の手段として、現在のチームのメンバーではない信頼できる貢献者がその役割を担うこともできます。
*   **コアコミッター** (`@corecommitter`)。この貢献者は「バージョンアップ」アクションを実行します。現在のコアコミッターのリストは[ここ](https://ja.wordpress.org/team/handbook/core/about/organization/#committers)にあります。
*   **セキュリティチームのメンバー** (`@securityteammember`)。この貢献者は、リリースされる最新のコードセットが非公開のセキュリティテストに合格していることを確認します。
*   **ミッションコントロールのアクセス権を持つ人** (`@mcpilot`)。このレベルのアクセス権を持つ貢献者は、リリースをパッケージ化し、ナイトリーを更新するために必要です。このアクセス権を持つアクティブな貢献者のリストは非常に少ないので、前もってこの役割を果たす人を見つけておくことが重要です。
*   **マーケティングチームのメンバー、またはマーケティングリリースリード** (`@marketingteamember`)。リリースアナウンスの投稿を下書きする担当者。

<!--
## Pre-release check-in – one hour before the party starts
-->

## リリース前のチェックイン – パーティが始まる1時間前

<!--
Before the scheduled time, check the current release leads channel (usually named `#x.x-release-leads`) to confirm that all relevant teams are prepared. If more time is needed and a delay is necessary, a message in the [#core](https://make.wordpress.org/core/tag/core/) channel should note the reason for the delay along with an expected time that the party will start.
-->

予定時刻の前に、現在のリリースリードチャンネル (通常 `#x.x-release-leads` という名前) をチェックして、関連するすべてのチームが準備できていることを確認します。さらに時間がかかり遅延が必要な場合は、[#core](https://make.wordpress.org/core/tag/core/) チャンネルに遅延の理由とパーティの開始予定時刻をメッセージで知らせる必要があります。

<!--
## Host script based on Beta releases
-->

## ベータリリースにもとづく開催スクリプト

<!--
The following script contains several placeholders highlighted in blue. It’s common for the @corecommitter, @securityteammember, and @missioncontrol to be the same person; adjust the script accordingly.
-->

以下のスクリプトには、青字でハイライトされたプレースホルダーがいくつか含まれています。@corecommitter、@securityteammember、@missioncontrol が同じ人であることはよくあることですので、それに応じてスクリプトを調整してください。

<!--
| **Steps and actions** | **Script for host** | **Who** |
| --- | --- | --- |
|  | `/here` Welcome to the WordPress `` `X.Y-Z` `` release party.  
  
I will be your host for this event, with @corecommitter and @mcpilot acting as behind-the-scenes drivers. (Be sure to adapt this message to the actual participants, taking into account any contributor filling multiple roles).  
  
For those who haven’t attended a release party before, welcome! Here’s the step-by-step guide from the handbook that details the release process: [https://make.wordpress.org/core/handbook/about/release-cycle/releasing-beta-versions/](https://make.wordpress.org/core/handbook/about/release-cycle/releasing-beta-versions/)  
 |  |
| **Step 1:** Ensure the announcement post for the blog is ready | Let’s start by ensuring the release post is ready to be published. @marketingteammember, what’s the status of the post?  
  
A public preview should be made available so anyone wanting to help proofread the post can do so. Just double-check the `@props` to credit them. | Marketing Leads |
| **Step 2:** Announce in Core to pause commits and don’t share links to the package until tested | @committers. Please refrain from committing until `X.Y-Z` has been released. :thank-you:  
  
:siren: Please remember not to share links to the package publicly until the “all clear” is given after testing and the announcement post is published on WordPress.org. :siren: | All attendees |
| **Step 3:** Run all unit tests locally | Time to run all unit tests. @corecommitter, please confirm. | Core Committer |
| **Step 4:** Verify that the latest [GitHub Action checks](https://github.com/WordPress/wordpress-develop/actions) are passing. | @corecommitter, can you also confirm that GitHub Action checks are passing? | Core Committer |
| **Step 5:** Ask a Security team member to verify the private security unit tests are passing for the most recent commit to ensure no regressions are introduced. | @securityteammember, please verify the private security unit tests pass for the latest commit. Thanks! | Security Team Member |
| **Step 6:** Bump version | @corecommitter, will you please commit the first version bump?  
  
*\[Wait for the commit to appear\]* | Core Committer |
| **Step 7:** Build the packages. | @mcpilot please proceed to package the release and post the link to the package here. | Core Committer |
| **Step 8:** Package Reminder | \[*While the package is being built, once again, remind attendees not to publicly share the link to the package until it’s been tested and the release post has been published. Sometimes, errors can happen during packaging, and the package needs to be rebuilt.*\]  
  
:siren: Please remember not to share links to the package publicly until the “all clear” is given after testing and the announcement post is published on WordPress.org. :siren:  
  
*\[Wait until the link to the \*.zip file is posted\]* | Emcee |
| **Step 8:** Testing | I**t’s testing time**!  
  
There are several ways to test, so pick whatever feels most comfortable and report back as you go:  
  
1\. Install and activate the [WordPress Beta Tester](https://wordpress.org/plugins/wordpress-beta-tester/) plugin. Select the Bleeding edge channel and then Beta/RC Only stream.  
2\. Use WP-CLI to test: wp core update –version=`X.Y-Z`  
3\. Directly download the Beta/RC version from https://wordpress.org/wordpress-`X.Y-Z`.zip  
  
**Here are a few scenarios to test:**  
– Test from latest in 4.0.\* release series (e.g., 4.0.35 > `X.Y-Z`)  
– Test from latest in 4.9.\* release series (e.g., 4.9.21 > `X.Y-Z`)  
– Test from the latest version in the current major release series (e.g., 6.1.1 > `X.Y-Z`)  
– Test from the most recent Beta/RC release (e.g., Beta 4 > `X.Y-Z`)  
– Test fresh installation  
– Remove `wp-config.php` file and test a fresh installation  
– Test single site and multisite/network (both subdirectory and subdomain) installations  
  
You can report back by sharing how you tested and what the result was with an emoji. For example:  
– 6.2-beta1 > `X.Y-Z` via beta tester  
If it works, add :white\_check\_mark:  
If any issues happen, add :red\_circle: so we can investigate.  
  
Please note that language packs are built in a later step of the process, so it is normal for there to be notices such as `**Warning: Checksums not available for WordPress 6.3.2/fr_FR. Please cleanup files manually.**` | Everyone |
| **Optional**: Summarize any issues found | *\[If any issues are found during testing, rely on this section*.\]  
Thanks, everyone, for testing! For now, we’re tracking the following issues: | Emcee |
| **Step 9:** Second version bump | Please, @corecommitter, proceed with the second version bump.  
  
*\[Wait for the commit to appear\]* | Core Committer |
| **Step 10:** Rebuild the Nightly Package in Mission Control | @mcpilot, can you please refresh the nightly build?  
  
*\[Wait for confirmation\]* | Mission Control |
| **Step 11**: Publish the announcement post | The release post can now be published! @marketingteammember, please proceed. | Marketing Team Member |
| **Step 12**: Announce in [#core](https://make.wordpress.org/core/tag/core/) that the release is available | @here WordPress `X.Y-Z` is now available: **insert link from the announcement post**  
Please help test and give feedback! | Emcee |
| **Step 13:** Announce that committers is open again | @committers, you can now resume committing.  
  
If this is a Release Candidate release, also remind committers that the `dev-feedback` and `dev-reviewed` workflow is required for all commits to the X.X branch. | Emcee |
| **Step 14**: Outro | The party is over! Props to @corecommitter, @securityteammember, @mcpilot for helping with the various release tasks.  
Thanks, everyone, for joining in and helping make WordPress! Hope to see you at future release parties.   
`</x.x-release-party>` | Emcee |
| **Step 15**: Props | Write a message in the [#props](https://wordpress.slack.com/messages/C0FRG66LR) channel thanking and giving props to everyone who tested or helped with the release process. | Emcee |
-->

| **ステップとアクション** | **開催用のスクリプト** | **発言者** |
| --- | --- | --- |
|  | `/here` Welcome to the WordPress `X.Y-Z` release party.<br /><br />I will be your host for this event, with @corecommitter and @mcpilot acting as behind-the-scenes drivers. (Be sure to adapt this message to the actual participants, taking into account any contributor filling multiple roles).<br /><br />For those who haven’t attended a release party before, welcome! Here’s the step-by-step guide from the handbook that details the release process: [https://make.wordpress.org/core/handbook/about/release-cycle/releasing-beta-versions/](https://make.wordpress.org/core/handbook/about/release-cycle/releasing-beta-versions/) |  |
| **ステップ1:** ブログのアナウンス記事が準備できていることを確認する | Let’s start by ensuring the release post is ready to be published. @marketingteammember, what’s the status of the post?<br /><br />A public preview should be made available so anyone wanting to help proofread the post can do so. Just double-check the `@props` to credit them. | マーケティングリード |
| **ステップ2:** コミットを一時停止し、テストされるまでパッケージへのリンクを共有しないようアナウンスする | @committers. Please refrain from committing until `X.Y-Z` has been released. :thank-you:<br /><br />:siren: Please remember not to share links to the package publicly until the “all clear” is given after testing and the announcement post is published on WordPress.org. :siren: | すべての参加者 |
| **ステップ3:** すべてのユニットテストをローカルで実行する | Time to run all unit tests. @corecommitter, please confirm. | コアコミッター |
| **ステップ4:** 最新の [GitHub Action checks](https://github.com/WordPress/wordpress-develop/actions) がパスしていることを確認する | @corecommitter, can you also confirm that GitHub Action checks are passing? | コアコミッター |
| **ステップ5:** セキュリティチームのメンバーに、最新のコミットでプライベートセキュリティユニットテストがパスしていることを確認してもらい、リグレッションが発生していないことを確認してもらう | @securityteammember, please verify the private security unit tests pass for the latest commit. Thanks! | セキュリティチームのメンバー |
| **ステップ6:** バージョンアップ | @corecommitter, will you please commit the first version bump?<br /><br />**\[コミットされるのを待つ\]** | コアコミッター |
| **ステップ7:** パッケージをビルドする | @mcpilot please proceed to package the release and post the link to the package here. | コアコミッター |
| **ステップ8:** パッケージに関するお知らせ | \[**パッケージがビルドされている間は、テストが終わってリリースの投稿が公開されるまで、パッケージへのリンクを公の場に共有しないよう、もう一度参加者に注意してください。パッケージング中にエラーが起こり、パッケージの再構築が必要になることがあります。**\]<br /><br />:siren: Please remember not to share links to the package publicly until the “all clear” is given after testing and the announcement post is published on WordPress.org. :siren:<br /><br />**\[.zip ファイルへのリンクが貼られるまで待つ。\]** | ホスト |
| **ステップ8:** テスト | I**t’s testing time**!<br /><br />There are several ways to test, so pick whatever feels most comfortable and report back as you go:<br /><br />1\. Install and activate the [WordPress Beta Tester](https://wordpress.org/plugins/wordpress-beta-tester/) plugin. Select the Bleeding edge channel and then Beta/RC Only stream.<br />2\. Use WP-CLI to test: wp core update –version=`X.Y-Z`<br />3\. Directly download the Beta/RC version from https://wordpress.org/wordpress-`X.Y-Z`.zip<br /><br />**Here are a few scenarios to test:**<br />– Test from latest in 4.0.\* release series (e.g., 4.0.35 > `X.Y-Z`)<br />– Test from latest in 4.9.\* release series (e.g., 4.9.21 > `X.Y-Z`)<br />– Test from the latest version in the current major release series (e.g., 6.1.1 > `X.Y-Z`) – Test from the most recent Beta/RC release (e.g., Beta 4 > `X.Y-Z`) – Test fresh installation<br />– Remove `wp-config.php` file and test a fresh installation<br />– Test single site and multisite/network (both subdirectory and subdomain) installations<br /><br />You can report back by sharing how you tested and what the result was with an emoji. For example:<br />– 6.2-beta1 > `X.Y-Z` via beta tester<br />If it works, add :white\_check\_mark:<br />If any issues happen, add :red\_circle: so we can investigate. | 全員 |
| **Optional**: 見つかった問題点をまとめる | **\[テスト中に問題が見つかった場合は、このセクションを参照してください。\]**<br />Thanks, everyone, for testing! For now, we’re tracking the following issues: | ホスト |
| **ステップ9:** 2番目のバージョンアップ | Please, @corecommitter, proceed with the second version bump.<br /><br />**\[コミットされるのを待つ\]** | コアコミッター |
| **ステップ10:** ミッションコントロールでナイトリーパッケージを再ビルドする | @mcpilot, can you please refresh the nightly build?<br /><br />**\[確認を待つ\]** | ミッションコントロール |
| **ステップ11**: アナウンス記事を投稿する | The release post can now be published! @marketingteammember, please proceed. | マーケティングチームのメンバー |
| **ステップ12**: [#core](https://make.wordpress.org/core/tag/core/)でリリースをアナウンスする | @here WordPress `X.Y-Z` is now available: **アナウンス記事のリンクを挿入する**<br />Please help test and give feedback! | ホスト |
| **ステップ13:** コミッター再開について知らせる | @committers, you can now resume committing.<br /><br />If this is a Release Candidate release, also remind committers that the `dev-feedback` and `dev-reviewed` workflow is required for all commits to the X.X branch. | ホスト |
| **ステップ14**: アウトロ | The party is over! Props to @corecommitter, @securityteammember, @mcpilot for helping with the various release tasks.<br />Thanks, everyone, for joining in and helping make WordPress! Hope to see you at future release parties. `</x.x-release-party>` | ホスト |
| **ステップ15**: Props | Write a message in the [#props](https://wordpress.slack.com/messages/C0FRG66LR) channel thanking and giving props to everyone who tested or helped with the release process. | ホスト |

<!--
Script to host Beta/RC release parties
-->

ベータ/RC リリースパーティを開催するためのスクリプト

<!--
**Share reminders**
-->

## 注意事項

<!--
Before we go, here are a few reminders: 
-->

始める前に、いくつか注意事項を記載しておきます:

<!--
*   Here’s a post that covers all you need to know ahead of release day: https://make.wordpress.org/core/2022/10/25/wordpress-6-0-release-day-process-2/ (An example from WP 6.0 that can be adapted to the current release.)
*   The dry run before the 24-hour code freeze is planned for date **(insert date for one day before public release date)**
*   The public release is planned for **(insert the current cycle release date)**. The exact time will be announced after the Dry Run finishes. You’re invited back for the biggest event of this release season!
*   According to the Bug Scrub Schedule **(insert a link to pinned post in Make/Core)**, the remaining bug scrubs before the stable release party are as follows:
    *   **List dates**
-->

*   リリース日の前に知っておくべきことをすべてカバーした投稿は次のとおりです: https://make.wordpress.org/core/2022/10/25/wordpress-6-0-release-day-process-2/ (WP 6.0の例で、現在のリリースに合わせることができます)。
*   24時間コードフリーズ前のドライランは、**(公開日の1日前の日付が入る)** の日付に計画されています。
*   公開リリースは、**(現在のサイクルのリリース日が入ります)** に予定されています。正確な時間はドライラン終了後に発表されます。このリリースシーズン最大のイベントに、再びご招待します !
*   バグスクラブスケジュール **(Make/Core にピン留めされた投稿へのリンクを挿入)** によると、安定版リリースパーティまでに残っているバグスクラブは以下の通りです:
    *   **日程一覧**
