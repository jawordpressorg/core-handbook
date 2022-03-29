# Coordinating Devchat

## Running Weekly Meetings

The general flow of preparing for, hosting, and summarizing devchats is as follows:

1.  Publish an agenda ([example](https://make.wordpress.org/core/2019/08/14/dev-chat-agenda-august-14/)) at least 24 hours before the scheduled devchat time and including the relevant release number, “devchat”, and “agenda” tags to ensure it appears in relevant searches/filters elsewhere on Make/Core.
2.  Script your agenda topics so you can copy/paste into devchat ([example](https://make.wordpress.org/core/files/2020/08/devchat_script.txt)).
3.  Publish meeting summary ([example](https://make.wordpress.org/core/2018/10/10/dev-chat-summary-october-10-5-0-week-2/)) ideally within 24 hours after the completion of devchat and including the relevant release number, “devchat”, and “summary” tags to ensure it appears in relevant searches/filters elsewhere on Make/Core.

As you’re writing agenda and summary posts, keep in mind the [Post & Comment Guidelines](https://make.wordpress.org/core/handbook/best-practices/post-comment-guidelines/).

### Devchat opening / closing tags

At the beginning of devchat, include a `<devchat>` opening tag ([example](https://wordpress.slack.com/archives/C02RQBWTW/p1594238418128700)). At the end of devchat, include a `</devchat>` closing tag ([example](https://wordpress.slack.com/archives/C02RQBWTW/p1594241878194300)). This makes it easier to find the devchat afterwards in the Slack logs.

### Devchat `@here` announcement

In order to generate the `@here` channel notification to start the devchat meeting in [#core](https://wordpress.slack.com/archives/C02RQBWTW), you’ll need to use the `/here` command as `@here` has been disabled. If you do not have the access to use the `/here` command, then ask for the ability in [#meta](https://wordpress.slack.com/archives/C02QB8GMM) with an explanation that you’re helping coordinate devchat in [#core](https://wordpress.slack.com/archives/C02RQBWTW) and access should be added to your Slack account.

### Devchat timing

Devchat’s timing doesn’t change with DST and it operates regularly at [05:00 UTC](https://time.is/0500_in_UTC) and [20:00 UTC](http://time.is/2000_in_UTC) on Wednesdays as noted on the [Weekly Developer Chats page](https://make.wordpress.org/core/weekly-developer-chats/).

Devchat used to be once a week and its time would adjust as Daylight Saving Time (DST) adjusted around the world. This was originally desired as a way to keep the devchat meeting at the same time across timezones to allow folks to regularly plan on when to attend. However, the process for updating the meeting time as DST changed became more time-intensive than desired and with the addition of a second devchat each week there are now two conversations that folks can attend. With that, the change was made.