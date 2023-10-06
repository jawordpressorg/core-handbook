<!--
# Coordinating Devchat
-->

# 開発チャットの調整

<!--
## Running Weekly Meetings
-->

## 週次ミーティングの開催

<!--
The general flow of preparing for, hosting, and summarizing devchats is as follows:
-->

開発チャットの準備、開催、まとめの大まかな流れは以下の通りです。

<!--
1.  Publish an agenda ([example](https://make.wordpress.org/core/2019/08/14/dev-chat-agenda-august-14/)) at least 24 hours before the scheduled devchat time and including the relevant release number, “devchat”, and “agenda” tags to ensure it appears in relevant searches/filters elsewhere on Make/Core.
2.  Script your agenda topics so you can copy/paste into devchat ([example](https://make.wordpress.org/core/files/2020/08/devchat_script.txt)).
3.  Publish meeting summary ([example](https://make.wordpress.org/core/2018/10/10/dev-chat-summary-october-10-5-0-week-2/)) ideally within 24 hours after the completion of devchat and including the relevant release number, “devchat”, and “summary” tags to ensure it appears in relevant searches/filters elsewhere on Make/Core.
-->

1.  要約 ([例](https://make.wordpress.org/core/2019/08/14/dev-chat-agenda-august-14/)) を、予定されている開発チャットの時間の24時間前までに公開し、関連するリリース番号、「devchat」、「agenda」タグを含めて、Make/Core の他の場所で関連する検索/フィルターに表示されるようにします。
2.  要約のトピックをスクリプト化し、開発チャットにコピー/ペーストできるようにします ([例](https://make.wordpress.org/core/files/2020/08/devchat_script.txt))。
3.  ミーティングのサマリー ([例](https://make.wordpress.org/core/2018/10/10/dev-chat-summary-october-10-5-0-week-2/)) は、理想的には開発チャット終了後24時間以内に公開し、関連リリース番号、「devchat」、「summary」タグを含めて、Make/Core の他の関連する検索/フィルターに表示されるようにします。

<!--
As you’re writing agenda and summary posts, keep in mind the [Post & Comment Guidelines](https://make.wordpress.org/core/handbook/best-practices/post-comment-guidelines/).
-->

要約やまとめ記事を書く際には、[投稿・コメントガイドライン](https://make.wordpress.org/core/handbook/best-practices/post-comment-guidelines/)に気を付けてください。

<!--
### Devchat opening / closing tags
-->

### 開発チャットの開始 / 終了タグ

<!--
At the beginning of devchat, include a `<devchat>` opening tag ([example](https://wordpress.slack.com/archives/C02RQBWTW/p1594238418128700)). At the end of devchat, include a `</devchat>` closing tag ([example](https://wordpress.slack.com/archives/C02RQBWTW/p1594241878194300)). This makes it easier to find the devchat afterwards in the Slack logs.
-->

開発チャットの先頭には、`<devchat>` の開始タグ ([例](https://wordpress.slack.com/archives/C02RQBWTW/p1594238418128700)) を入れてください。開発チャットの終わりには、`</devchat>` 閉じタグ ([例](https://wordpress.slack.com/archives/C02RQBWTW/p1594241878194300)) を入れてください。これにより、Slack のログから開発チャットを後から簡単に見つけることができます。

<!--
### Devchat `@here` announcement
-->

### 開発チャットでの `@here` のアナウンス

<!--
In order to generate the `@here` channel notification to start the devchat meeting in [#core](https://wordpress.slack.com/archives/C02RQBWTW), you’ll need to use the `/here` command as `@here` has been disabled. If you do not have the access to use the `/here` command, then ask for the ability in [#meta](https://wordpress.slack.com/archives/C02QB8GMM) with an explanation that you’re helping coordinate devchat in [#core](https://wordpress.slack.com/archives/C02RQBWTW) and access should be added to your Slack account.
-->

[#core](https://wordpress.slack.com/archives/C02RQBWTW) の開発チャットミーティングを開始するために `@here` チャンネル通知を生成するには、`@here` が無効になっているため、`/here` コマンドを使用する必要があります。もし `/here` コマンドを使う権限がない場合は、[#meta](https://wordpress.slack.com/archives/C02QB8GMM) で、[#core](https://wordpress.slack.com/archives/C02RQBWTW) の開発チャットの調整を手伝っていることの説明とともに権限を申請すれば、あなたの Slack アカウントに権限が追加されるはずです。

<!--
### Devchat timing
-->

### 開発チャットのタイミング

<!--
Devchat’s timing doesn’t change with DST and it operates regularly at [05:00 UTC](https://time.is/0500_in_UTC) and [20:00 UTC](http://time.is/2000_in_UTC) on Wednesdays as noted on the [Weekly Developer Chats page](https://make.wordpress.org/core/weekly-developer-chats/).
-->

開発チャットのタイミングはサマータイムで変わることはなく、[Weekly Developer Chats ページ](https://make.wordpress.org/core/weekly-developer-chats/)にあるように、毎週水曜日の [05:00 UTC](https://time.is/0500_in_UTC) と [20:00 UTC](http://time.is/2000_in_UTC) で定期的に運用されています。

<!--
Devchat used to be once a week and its time would adjust as Daylight Saving Time (DST) adjusted around the world. This was originally desired as a way to keep the devchat meeting at the same time across timezones to allow folks to regularly plan on when to attend. However, the process for updating the meeting time as DST changed became more time-intensive than desired and with the addition of a second devchat each week there are now two conversations that folks can attend. With that, the change was made.
-->

かつて開発チャットは、世界中のサマータイム (DST) の調整に合わせて、週に一度時間を調整していました。これはもともと、タイムゾーンに関係なく同じ時間に開発チャットのミーティングを行うことで、参加する時間を定期的に計画できるようにするためでした。しかし、サマータイムの変更に伴う会議時間の更新に手間がかかるようになり、また、毎週2回目の開発チャットが追加されたことで、開発者が参加できる会話は2つになりました。そのため変更されました。
