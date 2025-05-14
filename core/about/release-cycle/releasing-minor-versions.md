<!--
# Releasing Minor Versions
-->

# マイナーバージョンのリリース

<!--
So, you wanna ship a minor version of WordPress? Okay, maybe you don’t *want* to. Perhaps you *need* to ship a minor version of WordPress. A minor release is intended for bugfixes and enhancements that do not add new deployed files and are at the discretion of the release lead with suggestions/input from component maintainers and committers. There’s a lot involved with shipping these releases, as documented below. If you’ve been through the release process before and see something missing *please add it*.
-->

WordPress のマイナーバージョンをリリースしたいですか ? リリース**したくない**かもしれませんが、リリース**せざるを得ない**かもしれません。マイナーリリースは、新しくデプロイされるファイルを追加しないバグ修正や機能強化を目的としており、コンポーネントのメンテナーやコミッターからの提案やアドバイスを受け、リリースリードの裁量によって決定されます。以下に記載されているように、これらのリリースには多くのことが関係します。以前にリリースプロセスを実行したことがあり、何か不足しているものがある場合は**追加してください**。

<!--
## Before Release
-->

## リリースの前に

<!--
Before you’ve decided to release, there are a few things to consider \[TODO: Add more to this section\]:
-->

リリースを決定する前に、検討すべきことがいくつかあります \[TODO: このセクションにさらに追加する\]:

<!--
*   Is this release because of a security fix?
*   Will this release contain only security fixes?
*   What maintenance fixes should go into the release? Have those maintenance fixes been committed to trunk?
-->

*   このリリースはセキュリティ修正のためですか ?
*   このリリースにはセキュリティ修正だけが含まれますか ?
*   このリリースにはどのようなメンテナンス修正が含まれますか ? それらのメンテナンス修正は trunk にコミットされましたか ?

<!--
Depending on the focus of the minor release (security, maintenance, or both), there are a few things to consider.
-->

マイナーリリースのフォーカス (セキュリティ、メンテナンス、またはその両方) に応じて、考慮すべきことがいくつかあります。

<!--
### Security
-->

### セキュリティ

<!--
**Security patches should be created well ahead of time**. Different patches may be necessary for trunk and stable branches. Currently, we make an effort to back port patches to [all versions of WordPress since 4.1](https://wordpress.org/news/2022/09/dropping-security-updates-for-wordpress-versions-3-7-through-4-0/). However, back porting patches is not always possible and those versions of WordPress are not officially supported as a result.
-->

**セキュリティパッチは、時間に余裕をもって作成すること**。trunk ブランチと安定版ブランチでは異なるパッチが必要になるかもしれません。現在、自動更新をサポートしている [WordPress のすべてのバージョン (4.1以降)](https://wordpress.org/news/2022/09/dropping-security-updates-for-wordpress-versions-3-7-through-4-0/)にパッチをバックポートするよう努めています。しかし、パッチのバックポートが常に可能であるとは限らず、そのため、これらのバージョンの WordPress は公式にはサポートされません。

<!--
Follow the process in the Security team handbook to make sure that patches are adequately tested for back-compat, bypasses, and real-world cases.
-->

セキュリティチームのハンドブックにあるプロセスに従って、パッチが後方互換、バイパス、実際のケースについて十分にテストされていることを確認してください。

<!--
All patches should be well-tested and receive sign-off from the WordPress Security Team at least five days ahead of the scheduled release date. It’s incredibly important to get this feedback early on as security fixes do not have a lot of time to bake on trunk.
-->

すべてのパッチは十分にテストされ、リリース予定日の少なくとも5日前には WordPress セキュリティチームの承認を受ける必要があります。セキュリティの修正には trunk で仕上げる十分な時間がないため、早期にこのフィードバックを得ることは非常に重要です。

<!--
For security fixes reported by third-parties, get information on how they would like to be credited. The announcement post on [wordpress.org/news/](https://wordpress.org/news/) credits third-parties as requested.
-->

サードパーティから報告されたセキュリティ修正については、彼らがどのようにクレジットされたいかについての情報を入手してください。[wordpress.org/news/](https://wordpress.org/news/) のアナウンス投稿では、サードパーティの要望に応じて、サードパーティの名前をクレジットします。

<!--
12 hours before release (or earlier), you’ll need to lower the TTL in the update API to 60 minutes. This means that, by the time you release, all WordPress installations will be checking for a new version of WordPress every hour. To lower the TTL, update the `WP_CORE_SHORT_API_TTL_VERSION` constant in `versions.php` to the impending release version number. This file requires access to a w.org sandbox, so one of them must be on hand for this.
-->

リリースの12時間前 (またはそれ以前) には、アップデート API の TTL を60分に下げる必要があります。これは、リリースまでに、すべての WordPress インストールが WordPress の新しいバージョンを1時間ごとにチェックすることを意味します。TTL を下げるには、`versions.php` 内の定数 `WP_CORE_SHORT_API_TTL_VERSION` をリリース予定のバージョン番号に更新します。このファイルは w.org サンドボックスへのアクセスを必要とするため、サンドボックスの1つが用意されている必要があります。

<!--
On release day, if a test fails or a security fix is no longer working properly, *punt*. Do not attempt last minute fixes. Either reschedule the release or do not include the fix in the release. Last minute fixes can lead to major bugs.
-->

リリース当日、テストが失敗したり、セキュリティ修正が正常に動作しなくなったりしたら、*punt* してください。直前になって修正しようとしないでください。リリースのスケジュールを変更するか、リリースに修正を含めないでください。直前の修正は大きなバグにつながる可能性があります。

<!--
Are your security fixes ready? Awesome. Got maintenance fixes? Keep reading. If not, skip the next section.
-->

セキュリティ修正は準備できましたか ? よいでしょう。メンテナンスの修正がありますか ? あるなら、続けて読んでください。なければ、次のセクションはスキップしてください。

<!--
### Maintenance
-->

### メンテナンス

<!--
Unlike security fixes, maintenance fixes can land on trunk any time. There’s a [Trac query](https://core.trac.wordpress.org/tickets/minor) dedicated to tickets targeted at the next minor release. If you’re considering a maintenance release, be sure to run through those tickets in addition to any tickets in mind. Once you’ve determined that your release is a maintenance release, start getting patches landed on the branches. The sooner, the better, so there’s less of a rush at the end.
-->

セキュリティの修正とは異なり、メンテナンスの修正はいつでも trunk に追加できます。[Trac のクエリー](https://core.trac.wordpress.org/tickets/minor)には、次のマイナーリリースを対象としたチケット専用のものがあります。メンテナンスリリースを考えているのであれば、念頭においているチケットに加えて、これらのチケットにも目を通すようにしてください。リリースがメンテナンスリリースであると判断したら、ブランチにパッチを追加し始めましょう。早ければ早いほどよいです。

<!--
Ideally, all patches land at least 48 hours before release and a release candidate is built. This can be a formal release candidate or a nightly build that includes all fixes. If you build a beta or release candidate, post about it on [make/core](https://make.wordpress.org/core/tag/release/) along with a list of what fixes are in the release. This will help encourage a wider audience to test the new build.
-->

理想的には、リリースの少なくとも48時間前にはすべてのパッチがリリースされ、リリース候補がビルドされます。これは正式なリリース候補でも、すべての修正を含むナイトリービルドでもかまいません。ベータ版やリリース候補版をビルドしたら、[make/core](https://make.wordpress.org/core/tag/release/) に、リリースに含まれる修正点のリストとともに投稿してください。こうすることで、より多くの人に新しいビルドをテストしてもらうことができます。

<!--
### Both
-->

### 両方

<!--
Regardless of which kind of release you’re planning, there are a number of things you need to do.
-->

どのようなリリースを計画している場合でも、やるべきことが沢山あります。

<!--
1.  Check for breaking changes that would require a dev note. Ensure that those are published ahead of the release and tagged with the minor release number, related major release number, and the dev notes tag (e.g., “4.9, 4.9.2, dev notes”).
2.  Verify that the latest version of Akismet is included in WordPress builds. You no longer need to reach out to the Akismet team to see if there is a plugin release coming soon to include in the update. This is is important and prevents a user from seeing an update prompt immediately after creating a new site. This has been automated ([related discussion](https://make.wordpress.org/systems/2020/03/20/build-svn-access-for-sergeybiryukov/#comment-1647)). [Here’s an example](https://build.trac.wordpress.org/changeset/38478) of a commit to build.svn that bumps the Akismet external to the latest version (this is the old, manually method).
3.  Ask a member of the Security team to run the private security unit test suite, to make sure no regressions are introduced. If any are found, avoid discussing the details publicly, because some sites (like wordpress.org) run `trunk` or beta/RCs in production. Instead, notify the Security team privately.
4.  You’ll want to notify hosts that a release is coming a couple of days ahead of time. Three days is the recommended time frame, but is not always possible depending on release timeline. The security team can assist you with the message to hosts. This message **should not go out until all security patches are ready** (if a security release).
5.  If there will be **string changes in your release, notify the Polyglots team ahead of time**.
6.  Do a diff on the `src/` directory between the last release tag and the release branch and confirm there are no new files introduced, since these will often break automatic upgrades.
7.  A news post is needed for the WordPress.org news blog. Generally speaking, you should start this at least a day ahead of time (the more time, the better). You can copy the format from [previous releases](https://wordpress.org/news/category/releases/). Be sure to grep logs to get a complete list of all contributors to the release. The list of props can most efficiently be gathered by someone who has access to a sandbox to run `wporg/bin/core/props-parser.php`.
8.  Alert the systems team (e.g. @barry, @abbe, @sysmonk) about your release so they can plan to have someone available in case there are any issues. The sooner you’ve set a time for release, the sooner you can do this.
9.  Prepare Codex pages for each version you intend to release, using the Wiki Template of [Release](https://codex.wordpress.org/Template:Release) (directions are included on that page). If your release is security-related, these pages can be mostly blank until the actual release day, but need to exist as we link to them in WordPress itself.
-->

1.   開発者ノートを必要とする重要な変更がないか確認します。これらはリリース前に公開され、マイナーリリース番号、関連するメジャーリリース番号、開発者ノートタグ (例:「4.9、4.9.2、dev notes」) がタグ付けされていることを確認してください。
2.   最新バージョンの Akismet が WordPress のビルドに含まれていることを確認します。現在では、Akismet チームに連絡して、アップデートに含めるプラグインのリリースが近いかどうかを確認する必要はありません。これは、ユーザーが新しいサイトを作成した直後にアップデートのプロンプトが表示されることを防ぐために重要なことです。これは自動化されています ([関連する議論](https://make.wordpress.org/systems/2020/03/20/build-svn-access-for-sergeybiryukov/#comment-1647))。build.svn にコミットして Akismet external を最新バージョンに更新する例は[こちら](https://build.trac.wordpress.org/changeset/38478)です (これは手作業による古い方法です)。
3.   セキュリティチームのメンバーにプライベート・セキュリティ・ユニットテストスイートを実行してもらい、リグレッションが発生しないことを確認します。一部のサイト (wordpress.org など) では本番環境で `trunk` またはベータ/RC が稼働しているため、見つかった場合はその詳細について公の場で議論することは避けてください。代わりに、セキュリティ・チームに個人的に通知してください。
4.   数日前に、リリースが予定されていることをホストに通知するとよいでしょう。3日前が推奨されますが、リリースのスケジュールによっては不可能な場合もあります。セキュリティチームがホストへのメッセージについてお手伝いします。このメッセージは、(セキュリティリリースの場合) **すべてのセキュリティパッチが準備できるまで出してはいけません**。
5.   リリースに **文字列の変更がある場合は、事前に Polyglots チームに知らせてください**。
6.   最後のリリースタグとリリースブランチの間の `src/` ディレクトリの差分をとり、新しいファイルが追加されていないことを確認します。これらのファイルは自動アップグレードを妨げることが多いためです。
7.   WordPress.org のニュースブログへの投稿が必要です。一般的には、少なくとも1日前には始めるべきです (時間があればあるほどよいでしょう)。[以前のリリース](https://wordpress.org/news/category/releases/)からフォーマットをコピーできます。リリースに貢献したすべての人の完全なリストを得るために、必ずログを grep してください。props のリストは、サンドボックスにアクセスできる人が `wporg/bin/core/props-parser.php` を実行することで最も効率的に集めることができます。
8.   システムチーム (例: @barry、@abbe、@sysmonk) にリリースについて知らせておくことで、何か問題があった場合に備えて、誰かが対応できるように計画しておくことができます。リリースの時間を早く設定すればするほど、より早くこれを行うことができます。
9.   リリースするバージョンごとに、[リリース](https://codex.wordpress.org/Template:Release) の Wiki テンプレートを使って、Codex ページを用意してください (手順はそのページに記載されています)。リリースがセキュリティに関するものである場合、これらのページは実際のリリース日までほとんど空白でもかまいませんが、WordPress 自体にリンクするため、存在する必要があります。

<!--
Now that you’ve done all of that, it’s on to release day.
-->

すべての作業が完了したら、いよいよリリース日を迎えます。

<!--
## Release Day
-->

## リリース日

<!--
You’ve made it. Release day can be stressful. The best way to survive release day is to *stay calm*. Things will go wrong. It’s okay, just regroup and keep moving forward. Ask for help from folks that have been through this before and have some confidence in yourself. But first, you need your release day team. You should try to get this team aligned one week before the release.
-->

リリース日はストレスになるかもしれません。リリース日を乗り切る最善の方法は、**冷静さを保つ**ことです。うまくいかないこともあるでしょう。大丈夫です、気を取り直してもう一度進んでみましょう。同じような経験をした人に助けを求め、自分に自信を持つようにしましょう。しかし、まずはリリース当日のチームが必要です。リリースの1週間前までに、チームをまとめるようにしましょう。

<!--
Often times one person can fill multiple roles. If you’re unsure who can do each of these, welcome to the club. Ask in your release channel or ask an experienced committer and someone should be able to help guide you.
-->

多くの場合、1人の人が複数の役割を担うことができます。それぞれの役割を誰が担えるかわからない場合は、ぜひご参加ください。リリースチャンネルで質問するか、経験豊富なコミッターに尋ねれば、きっと誰かが助けてくれるはずです。

<!--
*   A core committer to update the version strings
*   Someone with mission control access to build packages
*   Someone with meta commit to build language packs and enable auto-updates
*   Someone who can create and publish NPM packages (gutenberg\-core or github admin)
*   A trac admin
*   Someone with who can create pages in helphub to create the version page
*   Someone with announce in slack
*   A security team member who can run the automated security tests
*   Someone who can publish a post on /news
*   Someone who can check the spelling and grammar of the /news post (seriously)
-->

* バージョン文字列を更新するコアコミッター
* パッケージをビルドするためのミッションコントロール権限を持つ人
* 言語パックをビルドし、自動更新を有効にするメタコミット権限を持つ人
* NPM パッケージを作成・公開できる人 (gutenberg-core または github 管理者)
* Trac 管理者
* バージョンページを作成するためにヘルプハブにページを作成できる人
* Slack でアナウンスできる人
* 自動セキュリティテストを実行できるセキュリティチームメンバー
* /news に投稿できる人
* /news の投稿のスペルと文法をチェックできる人 (これは本当です)

<!--
When it’s time to start the release party, get yourself a glass of water and take a deep breath. There are two main phases of the release. Phase one is about about getting the release out and announced. Phase two is about setting up the next release for success.
-->

リリースパーティーを始める時間になったら、コップ一杯の水を用意して、深呼吸をしましょう。リリースには大きく分けて2つのフェーズがあります。フェーズ1はリリースの公開と発表です。フェーズ2は、次のリリースを成功させるための準備です。

<!--
### Phase One
-->

### フェーズ1

<!--
1.  If there are any update to the NPM packages, those need to be built and published. Please refer to the relevant documentation. ([Link](https://github.com/WordPress/gutenberg/blob/HEAD/docs/contributors/code/release.md#packages-releases-to-npm-and-wordpress-core-updates))
2.  If you’re running a security release, security patches need to be committed to all relevant branches.
3.  Ensure that all commits have synced to [https://build.trac.wordpress.org/](https://build.trac.wordpress.org/). If not, find someone that can raise a flag with the systems team.
4.  Once any security patches are committed, move the release process to the [#core](https://make.wordpress.org/core/tag/core/) channel.
    *   start by making an announcement (using the `/here` Slack command) welcoming people to the release party
    *   post a request that committers hold off on any commits until the conclusion of the release, for example: `@committers please refrain from committing during the release process`.
5.  Version bumps need to be committed on all relevant branches. [Here’s an example.](https://core.trac.wordpress.org/changeset/44078) Any core committer can do this step. When committing a version bump on the most recent branch please update both the version.php and about.php files. The `package.json`, `package-lock.json`, and `composer.json` files may already be updated for the current branch but will need to be updated for any previous branches ([example](https://core.trac.wordpress.org/changeset/39862)).
    *   `package.json`, `package-lock.json`, and `composer.json` have a single simple bump to `X.Y.Z` (this will likely already be correct, due to the post-release version bump described later in this doc).
    *   `version.php` has one bump to `X.Y.Z-src`. Note the `-src` suffix that should always be included when committing to develop.svn.
    *   `about.php` needs a number bump to `Z` in the “Maintenance and Security Release(s)” heading and a paragraph added describing the changes in the release, using existing strings as defined at the bottom. These strings differ from branch to branch, so please make sure to use the ones from the correct version. It is easiest to copy and paste the appropriate paragraph from elsewhere. If this is the first minor release for a branch, there is also a wrapping div and the aforementioned `h3` to add after the nav tabs. Make note of the possible string combinations for single and multiple security and/or bug fixes. Checkout [a more complete explanation](#selecting-strings) of the differences.
    *   Prepare these changes well in advance and ask for a review. This will help avoid hold-ups during the release process. The version bump and about page can be committed together, they do not need to be separate.
6.  Once again, ensure that all commits have synced to [https://build.trac.wordpress.org/](https://build.trac.wordpress.org/). If not, find someone that can raise a flag with the systems team. This will likely delay the release for a bit.
7.  On all branches, the release [needs to be tagged](https://build.trac.wordpress.org/browser/tags/). Many people run releases from SVN and rely on the tags to do that. Tagging can be completed by using following commands (be sure to update with your relevant branch and release): `svn cp https://develop.svn.wordpress.org/branches/5.7 https://develop.svn.wordpress.org/tags/5.7.2 -m "Tag 5.7.2"`
8.  The release packages need to be built in mission control, from the tag of each version being released. Once it’s packaged, it needs to be tested well, including manually testing updates. You should encourage everyone who is around to test as well. See the [script for major release testing](https://make.wordpress.org/core/handbook/about/release-cycle/hosting-release-parties/#host-script-based-on-beta-releases) for some verbiage.
9.  Kick off the [Installation Tests](https://github.com/WordPress/wordpress-develop/actions/workflows/install-testing.yml) and the [Upgrade Tests](https://github.com/WordPress/wordpress-develop/actions/workflows/upgrade-testing.yml) workflows once the packages have been built.
10.  Autoupdates need to be enabled in the `versions.php` file, located in the dotorg repository. (This file requires access to a dotorg sandbox, so one of them must be on hand for this.) To enable autoupdates, set the `WP_CORE_LATEST_RELEASE` constant to be the new version number, and set the time that autoupdates should start in `WP_CORE_AUTOUPDATE_RAMP_START`, this should be a few minutes after the anticipated deploy. You should also update the array `wporg_get_version_equivalents()` to match all of the new versions, and the corresponding old version should be added to the array of old versions.
    
    *   The percentage on offer will ramp up from 50% to 100% availability over the course of a specified time. This is controlled by the `WP_CORE_AUTOUPDATE_RAMP_START` and `WP_CORE_AUTOUPDATE_RAMP_PERIOD` constants. These work in conjunction with the previous `WP_CORE_AUTOUPDATE_PERCENT` constant to automate and remove the need for us to manually alter `WP_CORE_AUTOUPDATE_PERCENT` to a lower value during some releases.
    
    *   If it’s a security release, you should also bump `wporg_get_secure_versions()` to match the legacy versions within each branch that is not insecure.
    *   Deploy
11.  Verify that everything is working as expected, then bump `WP_CORE_AUTOUPDATE_RELEASE` and deploy.
12.  Check auto update stats to make sure they’re normal (success rate above 99.9%, with the remaining 0.1% being safely aborted or rolled back).
13.  Language packs for the release need to be built by bumping versions in `translate/bin/update-all-core-packs.sh` and deploying. (This file requires access to a dotorg sandbox.)
14.  Publish the helphub page for the new version. This should be linked from the news post so it needs to come first.
    *   Add [minor release version page](https://wordpress.org/support/wordpress-version/version-5-7-1/) with the [file diff list](https://codex.wordpress.org/Template:Release) and the link to the news post.
    *   Add version info and link to version page on [WordPress Versions](https://wordpress.org/support/article/wordpress-versions/).
15.  The wordpress.org/news/ post needs to be published.
16.  Thank attendees for their assistance testing during the release
17.  let committers know they can commit again: `@committers feel free to commit as usual, thank you for your patience during the release`
-->

1.  NPM パッケージにアップデートがある場合は、ビルドして公開する必要があります。関連ドキュメントをご参照ください。([リンク](https://github.com/WordPress/gutenberg/blob/HEAD/docs/contributors/code/release.md#packages-releases-to-npm-and-wordpress-core-updates))
2.  セキュリティリリースを実行する場合、セキュリティパッチをすべての関連ブランチにコミットする必要があります。
3.  すべてのコミットが [https://build.trac.wordpress.org/](https://build.trac.wordpress.org/) に同期されていることを確認してください。同期されていない場合は、システムチームに報告できる担当者を探してください。
4.  セキュリティパッチがコミットされたら、リリースプロセスを [#core](https://make.wordpress.org/core/tag/core/) チャンネルに移動してください。
    *   (`/here` Slack コマンドを使用して) リリースパーティーへの参加を歓迎するアナウンスを行うことから始めます。
    *   コミッターに対して、リリースが完了するまでコミットを控えるようリクエストを投稿します。例: `@committers please refrain from committing during the release process`。
5.   バージョンアップは関連するすべてのブランチでコミットする必要があります。[これがその例です](https://core.trac.wordpress.org/changeset/44078)。コアコミッターであれば誰でもこのステップを実行できます。最新のブランチでバージョンアップをコミットする際には、version.php と about.php の両方を更新してください。`package.json`、`package-lock.json`、`composer.json` ファイルは現在のブランチですでに更新されているはずですが、それ以前のブランチでは更新する必要があります ([例](https://core.trac.wordpress.org/changeset/39862))。
    *   `package.json`、`package-lock.json`、`composer.json` には `X.Y.Z` への単純なバージョンアップが1つあります (このドキュメントで後述するリリース後のバージョンアップのため、これはおそらくすでに正しいでしょう)。
    *   `version.php` には `X.Y.Z-src` へのバージョンアップが一つあります。接尾辞の `-src` は、develop.svn にコミットする際に常に含める必要があることに注意してください。
    * `about.php` の見出しである「Maintenance and Security Release(s)」に `Z` という数字を追加し、下部にある既存の文字列を使用して、リリースの変更点を説明する段落を追加する必要があります。これらの文字列はブランチによって異なりますので、必ず正しいバージョンのものを使用してください。他の場所から適切な段落をコピー & ペーストすることが一番簡単です。これがブランチの最初のマイナーリリースである場合、ナビゲ―ションタブの後に追加するラッパー div と前述の `h3` もあります。単一または複数のセキュリティやバグの修正について、考えられる文字列の組み合わせをメモしておきます。違いについては、[より完全な説明](https://ja.wordpress.org/team/handbook/core/about/release-cycle/releasing-minor-versions/#selecting-strings)をチェックしてください。
    *   これらの変更を事前に十分に準備し、レビューを依頼しましょう。そうすることで、リリースプロセスの停滞を避けることができます。バージョンアップとアバウトページは一緒にコミットでき、別々に行う必要はありません。
6.  もう一度言いますが、すべてのコミットが [https://build.trac.wordpress.org/](https://build.trac.wordpress.org/) に同期されていることを確認してください。同期されていない場合は、システムチームに報告できる担当者を探してください。これにより、リリースが少し遅れる可能性があります。
7.  すべてのブランチで、リリースには[タグが必要です](https://build.trac.wordpress.org/browser/tags/)。多くの人は SVN からリリースし、そのためにタグに依存しています。タグ付けは以下のコマンドで完了します (関連ブランチとリリースで必ず更新してください): `svn cp https://develop.svn.wordpress.org/branches/5.7 https://develop.svn.wordpress.org/tags/5.7.2 -m "Tag 5.7.2"`
8.  リリースパッケージは、リリースされる各バージョンのタグをもとにミッションコントロールでビルドする必要があります。パッケージ化されたら、手動での更新テストを含め、十分にテストする必要があります。周りの人全員にもテストを促しましょう。具体的な内容については、[メジャーリリースのテスト用スクリプト](https://ja.wordpress.org/team/handbook/core/about/release-cycle/hosting-release-parties/#host-script-based-on-beta-releases)をご覧ください。
9.  パッケージがビルドされたら、[インストールテスト](https://github.com/WordPress/wordpress-develop/actions/workflows/install-testing.yml)と[アップグレードテスト](https://github.com/WordPress/wordpress-develop/actions/workflows/upgrade-testing.yml)ワークフローを開始します。
10.  自動更新は dotorg リポジトリにある `versions.php` ファイルで有効にする必要があります。(このファイルは dotorg サンドボックスへのアクセスを必要とするため、サンドボックスが用意されている必要があります)。自動更新を有効にするには、`WP_CORE_LATEST_RELEASE` 定数に新しいバージョン番号を設定し、自動更新を開始する時間を `WP_CORE_AUTOUPDATE_RAMP_START` に設定します。これは予想されるデプロイの数分後であるはずです。また、すべての新しいバージョンと一致するように `wporg_get_version_equivalents()` 配列を更新し、対応する古いバージョンを古いバージョンの配列に追加する必要があります。
    *   提供されるパーセンテージは、指定された時間の間に50%から100%まで上昇します。これは `WP_CORE_AUTOUPDATE_RAMP_START` 定数と `WP_CORE_AUTOUPDATE_RAMP_PERIOD` 定数によって制御されます。これらは以前の定数 `WP_CORE_AUTOUPDATE_PERCENT` と連携して動作し、いくつかのリリース中に手動で `WP_CORE_AUTOUPDATE_PERCENT` を低い値に変更する必要性をなくし、自動化します。
    *   セキュリティリリースの場合は、`wporg_get_secure_versions()` を安全でない各ブランチ内のレガシーバージョンと一致させる必要があります。
    *   デプロイ
11.  すべてが期待通りに動作していることを確認してから、`WP_CORE_AUTOUPDATE_RELEASE` をバージョンアップしてデプロイします。
12.  自動アップデートの統計が正常であることを確認してください (成功率は99.9%以上で、残りの0.1%は安全に中断またはロールバックされます)。
13.  リリースの言語パックは、`translate/bin/update-all-core-packs.sh` のバージョンを上げてビルドし、デプロイする必要があります。(このファイルは dotorg サンドボックスへのアクセスを必要とします)。
14.  新しいバージョンの HelpHub ページを公開します。これはニュース記事からリンクする必要があるため、最初に公開する必要があります。
    *   [マイナーリリース版ページ](https://wordpress.org/support/wordpress-version/version-5-7-1/)に[ファイルの差分リスト](https://codex.wordpress.org/Template:Release)とニュース記事へのリンクを追加します。
    *   [WordPress Versions](https://wordpress.org/support/article/wordpress-versions/) にバージョン情報とバージョンページへのリンクを追加します。
15.  wordpress.org/news/ の投稿を公開する必要があります。
16.  リリース中にテストに協力してくれた参加者に感謝します。
17.  コミッターにコミットができるようになったことを伝えます: `@committers feel free to commit as usual, thank you for your patience during the release`

<!--
The release is now public, but your work is not done!
-->

リリースは公開されましたが、作業はまだ完了していません !

<!--
### Phase Two
-->

### フェーズ2

<!--
Some of these tasks are ok to do over the course of the next few hours, so now is a good time to get a fresh glass of water if you need one.
-->

これらの作業のいくつかは、今後数時間かけて実行しても問題ありません。そのため、必要な場合は休憩をとってください。

<!--
1.  Open a [Request for Minor Release Amplification](https://github.com/WordPress/Marketing-Team/issues/new?assignees=bjmcsherry%2Ceidolonnight&labels=amplification-request%2Crelease-amplification&projects=&template=3-request-for-release-amplification.yml&title=%5BAMPLIFY+RELEASE%5D%3A+WordPress+X.Y.Z) issue on the Marketing Team’s issue tracker detailing the version number, type of release and a link to the announcement post.
2.  Alert make/polyglots that you have released. Some locales produce their own builds instead of relying on the automatic builds and need to package things on their own. [Here’s an example](https://make.wordpress.org/polyglots/2021/04/15/35197/).
3.  Update all HelpHub Version pages:
    *   Add [minor release version page](https://wordpress.org/support/wordpress-version/version-5-7-1/) with the [file diff list](https://codex.wordpress.org/Template:Release) and the link to the news post.
    *   Add version info and link to version page on [WordPress Versions](https://wordpress.org/support/article/wordpress-versions/).
4.  Update the Codex [CurrentVersion Template](https://codex.wordpress.org/Template:CurrentVersion) with the new version.
5.  If there were any changes to the REST API, update the [REST API changelog](https://developer.wordpress.org/rest-api/changelog/) over at dev hub.
6.  In Trac, create (a) [new milestone](https://core.trac.wordpress.org/admin/ticket/milestones)(s) for `X.Y.Z+1` and mark the old milestone(s) as completed. This must be done by a Trac admin.
7.  In Trac, create a [new version](https://core.trac.wordpress.org/admin/ticket/versions) for the `X.Y.Z+1` release (including the most recent branch with backports). Delete the date from the `Released` date field. This too must be done by a Trac admin.
8.  Bump the latest stable branch version to `X.Y.Z+1-alpha-$REVNUM-src` and the `version` in both the `package.json` and `composer.json` files to `X.Y.Z+1` for the next release. **Note:** After updating, you will also need to run `npm install` to update the `package-lock.json` fie ([example commit](https://core.trac.wordpress.org/changeset/56924)).
9.  Rebuild the latest stable branch’s nightly (this is done by the person with MC access)
10.  Rebuild the [Developer Code Reference](https://developer.wordpress.org/reference/) if necessary (This is done by someone with a sandbox)
-->

1.  マーケティング チームの issue トラッカーで[マイナーリリースの拡張リクエスト](https://github.com/WordPress/Marketing-Team/issues/new?assignees=bjmcsherry%2Ceidolonnight&labels=amplification-request%2Crelease-amplification&projects=&template=3-request-for-release-amplification.yml&title=%5BAMPLIFY+RELEASE%5D%3A+WordPress+X.Y.Z) の issue を開き、バージョン番号、リリースの種類、アナウンス投稿へのリンクを詳細に記載します。
2.  リリースしたことを make/polyglots に知らせます。ロケールによっては、自動ビルドに頼らず独自のビルドを行い、独自にパッケージ化する必要があります。[これがその例です](https://make.wordpress.org/polyglots/2021/04/15/35197/)。
3.  すべての HelpHub バージョンページを更新します:
    *   [マイナーリリース版ページ](https://wordpress.org/support/wordpress-version/version-5-7-1/)に[ファイルの差分リスト](https://codex.wordpress.org/Template:Release)とニュース記事へのリンクを追加します。
    *   [WordPress Versions](https://wordpress.org/support/article/wordpress-versions/) にバージョン情報とバージョンページへのリンクを追加します。
4.   Codex の [CurrentVersion テンプレート](https://codex.wordpress.org/Template:CurrentVersion)を新しいバージョンに更新します。
5.   REST API に変更があった場合は、dev hub の [REST API changelog](https://developer.wordpress.org/rest-api/changelog/) を更新してください。
6.   Trac で、`X.Y.Z+1` の[新しいマイルストーン](https://core.trac.wordpress.org/admin/ticket/milestones)を作成し、古いマイルストーンを完了としてマークしてください。これは Trac の管理者が行う必要があります。
7.   Trac で、`X.Y.Z+1` リリース (バックポートを含む最新のブランチ) の[新しいバージョン](https://core.trac.wordpress.org/admin/ticket/versions)を作成してください。`Released` 日付フィールドから日付を削除してください。これも Trac の管理者が行う必要があります。
8.   次のリリースに備えて、最新の安定版ブランチのバージョンを `X.Y.Z+1-alpha-$REVNUM-src` に、`package.json` と `composer.json` のバージョンを `X.Y.Z+1` にバージョンアップします。更新した後に、`npm install` を実行して `package-lock.json` ファイルを更新する必要もあります ([コミット例](https://core.trac.wordpress.org/changeset/56924))。
9.   最新の安定版ブランチのナイトリーバージョンを再ビルドします (これは MC アクセス権を持つ人が行います)。
10.   必要に応じて、[開発者コードリファレンス](https://developer.wordpress.org/reference/)を再構築します (これはサンドボックスを持つ誰かが行います)。

<!--
## Schedule
-->

## スケジュール

<!--
Assuming you’re following the instructions above and have an ideal schedule (all the time in the world), you’ll want to use the following schedule:
-->

上記の手順に従い、(世界中のすべての時間で) 理想的なスケジュールを立てると仮定すると、次のようなスケジュールを使用するとよいでしょう:

<!--
| **When?** | **What?** |
| --- | --- |
| T-7:00:00 | Triage all [targeted tickets](https://core.trac.wordpress.org/tickets/minor). |
| T-5:00:00 | All security patches created, tested, and cleared by the WordPress Security team. |
| T-4:00:00 | Commit all non-security patches to the relevant branch(es). |
| T-4:00:00 | Run the private security unit test suite |
| T-3:00:00 | Notify hosts that a release is coming. |
| T-1:00:00 | Create the WordPress.org/news/ blog post (as draft). |
| T-0:12:00 | If there are security fixes, lower the TTL in the `version-check` API to 60 minutes. (`WP_CORE_SHORT_API_TTL_VERSION` constant in `version.php`.) |
| T-0:05:00 | Commit security patches and run unit tests and security tests. |
| T-0:00:31 | Version bumps on all relevant branches. |
| T-0:00:30 | Build the release package in mission control. Test package and manually test updates. |
| T-0:00:00 | Turn on autoupdates. (`WP_CORE_LATEST_RELEASE` constant, and the `wporg_get_versions()` and `wporg_get_version_equivalents()` functions in `version.php`.) |
| T+0:00:01 | Post the WordPress.org/news/ blog post. |
| T+0:00:15 | Update credits (before or after release). |
| T+0:01:00 | Autoupdates complete (for the most part). |
| T+0:01:00 | Tag the releases. Many people run WordPress from SVN and need a tagged release to deploy. |
-->

| **いつ ?** | **何を ?** |
| --- | --- |
| T-7:00:00 | すべての[対象チケット](https://core.trac.wordpress.org/tickets/minor)をトリアージする。 |
| T-5:00:00 | すべてのセキュリティパッチが、WordPress セキュリティチームによって作成、テスト、クリアされている。 |
| T-4:00:00 | セキュリティパッチ以外のすべてのパッチを関連するブランチにコミットする。 |
| T-4:00:00 | プライベート・セキュリティ・ユニットテストスイートを実行する。 |
| T-3:00:00 | リリースが近付いていることをホストに知らせる。 |
| T-1:00:00 | WordPress.org/news/ ブログ投稿を (下書きとして) 作成する。 |
| T-0:12:00 | セキュリティ修正がある場合は `version-check` API の TTL を60分に下げてください (`version.php` の `WP_CORE_SHORT_API_TTL_VERSION` 定数)。 |
| T-0:05:00 |セキュリティパッチをコミットし、ユニットテストとセキュリティテストを実行する。 |
| T-0:00:31 | 関連するすべてのブランチでバージョンアップを行う。 |
| T-0:00:30 | ミッション・コントロールでリリース・パッケージをビルドする。パッケージをテストし、アップデートを手動でテストする。 |
| T-0:00:00 | 自動更新を有効にする (`WP_CORE_LATEST_RELEASE` 定数、`version.php` の `wporg_get_versions()` 関数と `wporg_get_version_equivalents()` 関数)。 |
| T+0:00:01 | WordPress.org/news/ のブログ記事を投稿する。 |
| T+0:00:15 | クレジットを更新する (リリースの前または後)。 |
| T+0:01:00 | 自動更新が (ほとんどの部分で) 完了しました。 |
| T+0:01:00 | リリースにタグを付ける。多くの人が WordPress を SVN から実行しており、デプロイするためにタグ付けされたリリースが必要です。 |

<!--
## Extras
-->

## 追加のタスク

<!--
### Selecting About Page Strings
-->

### アバウトページの文字列を選択する

<!--
There are 5 options for strings to choose from for the About page paragraph describing the release.
-->

リリースを説明するアバウトページの段落には、文字列に関する5つのオプションがあります。

<!--
*   If there is 1 security issue and no bug fixes: `<strong>Version %s</strong> addressed one security issue.`
*   If there are more than one security issues and no bug fixes: `<strong>Version %s</strong> addressed some security issues.`
*   If there are one or more bugs, `_n()` is used with the strings `<strong>Version %1$s</strong> addressed %2$s bug.` and `<strong>Version %1$s</strong> addressed %2$s bugs.` to the determine the proper string for the locale.
*   If there is 1 security issue and one or more bug fixes, `_n()` is used with the strings `<strong>Version %1$s</strong> addressed a security issue and fixed %2$s bug.` and `<strong>Version %1$s</strong> addressed a security issue and fixed %2$s bugs.` to determine the proper string for the locale.
*   If there are more than one security issues and one or more bug fixes, `_n()` is used with the strings `<strong>Version %1$s</strong> addressed some security issues and fixed %2$s bug.` and `<strong>Version %1$s</strong> addressed some security issues and fixed %2$s bugs.` to determine the proper string for the locale.
-->

*   セキュリティの問題が1つあり、バグ修正がない場合: `<strong>Version %s</strong> addressed one security issue.`
*   複数のセキュリティ問題があり、バグ修正がない場合: `<strong>Version %s</strong> addressed some security issues.`
*   1つ以上のバグがある場合、`_n()` を `<strong>Version %1$s</strong> addressed %2$s bug.` と `<strong>Version %1$s</strong> addressed %2$s bugs.` という文字列と一緒に使用し、ロケールに適切な文字列が決定されるようにします。
*   セキュリティの問題が1つあり、バグが1つ以上修正されている場合、`_n()` を `<strong>Version %1$s</strong> addressed a security issue and fixed %2$s bug.` および `<strong>Version %1$s</strong> addressed a security issue and fixed %2$s bugs.` という文字列と一緒に使用し、ロケールに適切な文字列が決定されるようにします。
*   セキュリティの問題が1つ以上あり、バグが1つ以上修正されている場合、`_n()` を `<strong>Version %1$s</strong> addressed some security issues and fixed %2$s bug.` と `<strong>Version %1$s</strong> addressed some security issues and fixed %2$s bugs.` という文字列と一緒に使用し、ロケールに適切な文字列が決定されるようにします。

<!--
Defer to other recent point releases for examples on how the strings change along with the numbers. Check the strings and have them reviewed before commit.
-->

数字とともに文字列がどのように変化するかについては、他の最近のポイントリリースを参照してください。文字列をチェックし、コミットする前にレビューを受けてください。

<!--
### Testing Package Builds
-->

### パッケージビルドのテスト

<!--
There are a few ways to test package builds, but using WP-CLI is a fast, effective way. Here’s a run down of commands you can use to test upgrades between versions. This example will be testing between 4.5.2 and 4.5.3 and will assume that some version of WordPress >= 3.7 is already installed.
-->

パッケージのビルドをテストする方法はいくつかありますが、WP-CLI を使用することが早く効果的な方法です。ここでは、バージョン間のアップグレードをテストするために使用できるコマンドを紹介します。この例では、4.5.2と4.5.3の間をテストし、WordPress バージョン3.7以上がすでにインストールされていると仮定します。

<!--
*   `$ wp core download --version=4.5.2 --force` This will retrieve the version you want to start from.
*   `$ wp core update-db` Get the database where it needs to be.
*   `$ wp core update https://wordpress.org/wordpress-4.5.3.zip` Update to the package you’re testing.
*   `$ wp core update-db` Make sure any database updates run.
-->

*   `$ wp core download --version=4.5.2 --force` 開始したいバージョンを取得します。
*   `$ wp core update-db` 必要なデータベースを取得します。
*   `$ wp core update https://wordpress.org/wordpress-4.5.3.zip` テストするパッケージに更新します。
*   `$ wp core update-db` データベースのアップデートが実行されていることを確認します。

<!--
Then check your test site to make sure everything is well. Happy upgrade testing!
-->

その後、テストサイトをチェックして、すべてが正常であることを確認してください。アップグレードのテストを楽しんでください !
