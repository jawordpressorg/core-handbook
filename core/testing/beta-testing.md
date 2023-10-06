<!--
# Beta Testing
-->

# ベータテスト

<!--
A valuable contribution an individual can make to WordPress development is to test WordPress, even if you are not a developer. Before every stable release of WordPress, pre-release versions are made available for testing. You can download the pre-releases and test them, so that the WordPress developers can fix problems before the new version is made available to the public.
-->

開発者でなくても WordPress の開発に個人ができる貴重な貢献は、WordPress をテストすることです。WordPress の安定版リリースの前には、プレリリース版がテスト用に提供されます。プレリリースをダウンロードしてテストすることで、WordPress の開発者は新バージョンが公開される前に問題を修正できます。

<!--
If you want to be on the bleeding edge of development, even before pre-release versions are put together, you can also check out the latest software from the [WordPress Subversion (SVN) repository](https://make.wordpress.org/core/handbook/tutorials/installing-wordpress-locally/from-svn/). Or, you can get the “[nightly build](https://wordpress.org/nightly-builds/wordpress-latest.zip)” (which is created from the Subversion repository) — almost as up-to-date as the instantaneous Subversion repository.
-->

プレリリースバージョンが作成される前から最新の開発版を確認したい場合は、[WordPress Subversion (SVN) リポジトリ](https://ja.wordpress.org/team/handbook/core/tutorials/installing-wordpress-locally/from-svn/)から最新のソフトウェアをチェックできます。または、「[ナイトリービルド](https://wordpress.org/nightly-builds/wordpress-latest.zip)」(Subversion リポジトリから作成されたもの) を入手できます。これは Subversion リポジトリとほぼ同等の最新版です。

<!--
To get started, install the [**WordPress Beta Tester**](https://wordpress.org/extend/plugins/wordpress-beta-tester/) plugin. Visit Plugins > Add New, type “wordpress beta tester” in the search field, and then click/tap “Install Now”.
-->

まずは、[**WordPress Beta Tester**](https://wordpress.org/extend/plugins/wordpress-beta-tester/) プラグインをインストールしてください。プラグイン > 新規追加にアクセスし、検索フィールドに「wordpress beta tester」と入力し、「インストール」をクリック・タップします。

<!--
1.  Backing up first is sensible.
2.  Go to Plugins > Add New and search for “WordPress Beta Tester”
3.  Click or tap the “Install Now” button for the WordPress Beta Tester plugin
4.  Go to Tools > Beta Testing (or Network Admin > Settings > Beta Testing on multisite)
5.  Select the  “Bleeding edge nightlies” option to follow development for the next major release of WordPress, or “Point release nightlies” to follow development of the next point release.
6.  Click or tap the “Save Changes” button
7.  Go to Dashboard > Updates
8.  Click or tap the “Update Now” button
9.  Return to Tools > Beta Testing to see options for Beta/RC to update to the next released beta or RC of the “Point release” or “Bleeding edge”.
-->

1.  まずバックアップを取ることがよいでしょう。
2.  プラグイン > 新規追加で「WordPress Beta Tester」を検索します
3.  WordPress Beta Tester プラグインの「今すぐインストール」ボタンをクリックまたはタップします
4.  ツール > ベータテスト (またはマルチサイトではネットワーク管理 > 設定 > ベータテスト) に進みます
5.  WordPress の次のメジャーリリースの開発をフォローするには「最前線」オプションを、次のポイントリリースの開発をフォローするには「ポイントリリース」オプションを選択します。
6.  「変更を保存」ボタンをクリックまたはタップします
7.  ダッシュボード > 更新へ移動します
8.  「今すぐアップデート」ボタンをクリックまたはタップします
9.  ツール > ベータテストに戻り、「ポイントリリース」または「最前線」の次にリリースされるベータ版または RC 版にアップデートするためのベータ版/RC 版のオプションを確認します。

<!--
Once the plugin is installed, navigate to Tools > Beta Testing and review the settings:
-->

プラグインをインストールしたら、ツール > ベータテストに移動し、設定を確認します:

<!--
*   **Point release nightlies.** The current release is 5.2.3. Selecting this will put you on the track for 5.2.x development.
*   **Bleeding edge nightlies.** Selecting this will put you on the track for 5.3 development.
*   **Beta/RC.** Selecting this will update to the next released beta or RC on whichever branch you are currently running.
-->

*   **ポイントリリース。** 現在のリリースは5.2.3です。これを選択すると、5.2.x の開発トラックを追跡できます。
*   **最前線。** これを選択すると、5.3の開発トラックを追跡できます。
*   **ベータ / RC のみ。** これを選択すると、現在実行しているブランチの次のリリースされたベータ版または RC 版に更新されます。

<!--
You can also use WP CLI to directly update your WordPress to trunk version by doing:
-->

WP CLI を使って、WordPress を trunk バージョンに直接アップデートすることもできます:

```
wp core update --version=trunk
```

<!--
If you find bugs while testing pre-release or already-released versions of WordPress, see [Reporting Bugs](https://make.wordpress.org/core/handbook/reporting-bugs/ "Reporting Bugs") or post in the [Alpha/Beta support forum](https://wordpress.org/support/forum/alphabeta).
-->

WordPress のプレリリース版やすでにリリースされているバージョンをテストしているときにバグを見つけた場合は、[バグの報告](https://ja.wordpress.org/team/handbook/core/reporting-bugs/)を参照するか、[Alpha/Beta サポートフォーラム](https://wordpress.org/support/forum/alphabeta)に投稿してください。

<!--
New features are often [developed as plugins](https://make.wordpress.org/core/features-as-plugins/). [Feature plugins](https://wordpress.org/plugins/browse/beta/) can be installed from the beta testing tab on the plugin install screen of your WordPress dashboard. Navigate to Plugins > Add New > Beta Testing.
-->

新機能はしばしば[プラグインとして開発](https://make.wordpress.org/core/features-as-plugins/)されます。[機能プラグイン](https://wordpress.org/plugins/browse/beta/)は、WordPress ダッシュボードのプラグインインストール画面のベータテストタブからインストールできます。プラグイン > 新規追加 > ベータテストに移動します。

[![Screen Shot 2015-05-23 at 10.28.50 AM](https://make.wordpress.org/core/files/2011/12/Screen-Shot-2015-05-23-at-10.28.50-AM-300x209.png)](https://make.wordpress.org/core/files/2011/12/Screen-Shot-2015-05-23-at-10.28.50-AM.png)

<!--
The plugins listed here are proposed for future versions of WordPress. They are glimpses of the future that are under active development. New versions are released regularly, sometimes daily. Some feature plugins require that you follow bleeding edge nightlies.
-->

ここに掲載されているプラグインは、WordPress の将来のバージョンで提案されているものです。これらのプラグインから、現在活発に開発されている未来の姿を垣間見ることができます。新しいバージョンは定期的に、時には毎日リリースされます。いくつかの機能プラグインは、最前線を追跡する必要があります。

<!--
Tracking bleeding edge nightlies with the beta tester plugin and installing feature plugins will make all of the latest software available for beta testing. If you go this route, here are some useful testing resources (and thank you very much):
-->

ベータテスタープラグインで最前線を追跡し、機能プラグインをインストールすることで、すべての最新ソフトウェアがベータテストで利用できます。もしこの方法を取るのであれば、次のような便利なテストリソースを利用できます:

<!--
*   [make/core](https://make.wordpress.org/core/) is the main WordPress development blog.  It is active and will keep you up-to-date on what’s happening right now in WordPress development.
*   [make/flow](https://make.wordpress.org/flow/) contains visual records and visual bug reports from the [Flow Patrol](https://make.wordpress.org/flow/handbook/) team.
*   The [Flow Patrol handbook](https://make.wordpress.org/flow/handbook/) includes information on [triage](https://make.wordpress.org/flow/handbook/triage/) if you want to get into triaging posts on make/flow.
-->

*   [make/core](https://make.wordpress.org/core/) は WordPress 開発のメインブログです。これはアクティブであり、WordPress 開発で今何が起きているのかについての最新情報を提供します。
*   [make/flow](https://make.wordpress.org/flow/) には、[Flow パトロール](https://make.wordpress.org/flow/handbook/)チームによるビジュアルに関する記録バグレポートが含まれています。
*   [Flow パトロールハンドブック](https://make.wordpress.org/flow/handbook/)には、make/flow で投稿を優先順位付けするための[トリアージ](https://make.wordpress.org/flow/handbook/triage/)に関する情報が含まれています。

<!--
When done testing, rolling your site back to the latest stable production release can be done with a tap/click of “Re-install Now ” on the Dashboard > Updates screen.
-->

テストが終了したら、ダッシュボード > 更新の画面で「今すぐ再インストール」をタップ・クリックするだけで、サイトを最新の安定したプロダクションリリースに戻すことができます。

[![Screen Shot 2015-06-29 at 1.25.59 pm](https://make.wordpress.org/core/files/2011/12/Screen-Shot-2015-06-29-at-1.25.59-pm-300x111.png)](https://make.wordpress.org/core/files/2011/12/Screen-Shot-2015-06-29-at-1.25.59-pm.png)

安定版リリースにロールバックするには、「今すぐ再インストール」をタップします
