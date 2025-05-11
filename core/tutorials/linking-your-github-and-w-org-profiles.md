<!--
# Linking your GitHub and w.org profiles
-->

# GitHub と w.org プロフィールをリンクする

<!--
In the WordPress project, contributions are collected and compiled into the WordPress.org Credits API by WordPress.org usernames. Though contributions happen in many different ways using many different tools, connecting efforts back to an individual’s w.org profile is required to receive attribution for your efforts.
-->

WordPress プロジェクトでは、WordPress.org のユーザー名によって貢献が収集され、WordPress.org のクレジット API にコンパイルされます。貢献はさまざまなツールを使用してさまざまな方法で行われますが、取り組みの帰属を受け取るには、その取り組みを個人の w.org プロフィールに結び付ける必要があります。

<!--
To ensure that you receive credit for any contributions submitted through GitHub, you must link your GitHub and WordPress.org profiles. This includes contributions to Gutenberg, using [GitHub pull requests for code review](https://make.wordpress.org/core/handbook/contribute/git/github-pull-requests-for-code-review/), and contributing to feature plugins under the WordPress organization, such as the [Performance plugin](https://github.com/wordpress/performance).
-->

GitHub を通じて送られた貢献に対するクレジットを確実に受け取るには、GitHub と WordPress.org のプロフィールをリンクする必要があります。これには、[コードレビューのための GitHub プルリクエスト](https://ja.wordpress.org/team/handbook/core/contribute/git/github-pull-requests-for-code-review/)を通じた Gutenberg への貢献や、WordPress 組織に属する[パフォーマンスプラグイン](https://github.com/wordpress/performance)などの機能プラグインへの貢献が含まれます。

<!--
# How to connect your accounts
-->

# アカウントを接続する方法

<!--
WordPress.org uses an oAuth flow to grant a WordPress GitHub application [read-only access](https://make.wordpress.org/core/2021/05/03/expired-github-and-wordpress-org-profile-connections/#comment-41291) to your GitHub account’s public information. This proves that you own both the GitHub account and the WordPress.org account and links the two accounts.
-->

WordPress.org は oAuth フローを使用して、WordPress GitHub アプリケーションに GitHub アカウントの公開情報への[読み取り専用アクセス](https://make.wordpress.org/core/2021/05/03/expired-github-and-wordpress-org-profile-connections/#comment-41291)を付与します。これは、GitHub アカウントと WordPress.org アカウントの両方を所有しており、2つのアカウントをリンクしていることを証明します。

### 1\. Log in to WordPress.org and edit profile

### 1\. WordPress.org にログインしてプロフィールを編集する

「link your GitHub account」をクリックしてプロセスを開始します。

[![](https://make.wordpress.org/core/files/2020/03/profile-edit.png)](https://make.wordpress.org/core/files/2020/03/profile-edit.png)

<!--
### 2\. Authorize WordPress.org Profiles application
-->

### 2\. WordPress.org プロフィールアプリケーションを承認する

<!--
Grant the WordPress Profiles GitHub application read-only access to your public information.
-->

WordPress プロフィール GitHub アプリケーションに公開情報への読み取り専用アクセスを許可します。

[![](https://make.wordpress.org/core/files/2020/03/oauth-screen.png)](https://make.wordpress.org/core/files/2020/03/oauth-screen.png)

<!--
### 3\. Verify Connection
-->

### 3\. 接続を確認する

<!--
Confirm your account is now connected.
-->

アカウントが接続されたことを確認します。

[![](https://make.wordpress.org/core/files/2020/03/profile-edit-with-connection-1024x833.png)](https://make.wordpress.org/core/files/2020/03/profile-edit-with-connection.png)

<!--
Access can be revoked at any time on the Edit Profile screen on WordPress.org.
-->

アクセスは、WordPress.org のプロフィール編集画面でいつでも取り消すことができます。

<!--
### 4\. Add your WordPress.org Git email to your GitHub email list
-->

### 4\. WordPress.org Git メールを GitHub メールリストに追加する

<!--
Visit the [email settings](https://github.com/settings/emails) page on GitHub and add `dotOrgUsername@git.wordpress.org` as an email on your GitHub account.
-->

GitHub の [email settings](https://github.com/settings/emails) ページにアクセスし、GitHub アカウントのメールアドレスとして `dotOrgUsername@git.wordpress.org` を追加します。

<!--
This is not an actual email, but adding this alias will ensure your contributions appear on your GitHub profile. This is what you should see once you’ve added your w.org email.
-->

これは実際のメールアドレスではありませんが、このエイリアスを追加すると、貢献が確実に GitHub プロフィールに表示されます。w.org メールを追加すると、次の画面が表示されます。

[![](https://make.wordpress.org/core/files/2024/01/Screenshot-2024-01-26-at-3.16.17-PM.png)](https://make.wordpress.org/core/files/2024/01/Screenshot-2024-01-26-at-3.16.17-PM.png)

<!--
## How do I know if my accounts are connected?
-->

## 自分のアカウントが接続されていること確認するにはどうすればよいですか ?

<!--
There are a few other ways to check whether your accounts are connected.
-->

アカウントが接続されているかどうかを確認する方法は他にもいくつかあります。

<!--
### Check your w.org profile
-->

### w.org プロフィールを確認する

<!--
If you have connected your accounts, you’ll notice a “GitHub” field on your profile.
-->

アカウントを接続している場合は、プロフィールに「GitHub」フィールドがあることに気付くでしょう。

[![](https://make.wordpress.org/core/files/2024/01/gh-connected-w.org-profile.png)](https://make.wordpress.org/core/files/2024/01/gh-connected-w.org-profile.png)

<!--
### Check for a w.org redirect
-->

### w.org リダイレクトを確認する

<!--
When visiting `https://profiles.wordpress.org/github:GHUSERNAME`, redirect to the connected w.org profile for `GHUSERNAME` if there is a preexisting connection. There is no active connection if you’re redirected to a GitHub w.org profile.
-->

`https://profiles.wordpress.org/github:GHUSERNAME` にアクセスすると、既存の接続がある場合は `GHUSERNAME` が接続された w.org プロフィールにリダイレクトします。GitHub w.org プロフィールにリダイレクトされる場合、アクティブな接続はありません。

<!--
### Check against the w.org API
-->

### w.org API で確認する

<!--
There’s also an available API to check whether a w.org profile has been connected to a GitHub account.
-->

w.org プロフィールが GitHub アカウントに接続されているかどうかを確認するための API も利用できます。

<!--
#### Example
-->

#### 例

<!--
This command will check whether the `desrosj` and `nacin` GitHub accounts are connected to w.org profiles.
-->

このコマンドは、`desrosj` および `nacin` GitHub アカウントが w.org プロフィールに接続されているかどうかを確認します。

```bash
curl https://profiles.wordpress.org/wp-json/wporg-github/v1/lookup/ --data 'github_user[]=desrosj&github_user[]=nacin' -s | jq
```

<!--
#### Results
-->

#### 結果

<!--
When a connection is active, the slug and profile URL will be returned. `false` is returned when no connection exists. The results are keyed by the GitHub usernames that were passed.
-->

接続がアクティブな場合、スラッグとプロフィールの URL が返されます。接続が存在しない場合は `false` を返します。結果は、渡された GitHub ユーザー名をキーにしています。

```json
{
  "desrosj": {
    "slug": "desrosj",
    "profile": "https://profiles.wordpress.org/desrosj"
  },
  "nacin": false
}
```

<!--
## Helpful links
-->

## 役に立つリンク

<!--
*   [GitHub Pull Requests for Code Contribution](https://make.wordpress.org/core/handbook/contribute/git/github-pull-requests-for-code-review/)
*   [Initial feature announcement](https://make.wordpress.org/core/2020/03/19/associating-github-accounts-with-wordpress-org-profiles/) (2020)
*   [Notice of expired profile connections](https://make.wordpress.org/core/2021/05/03/expired-github-and-wordpress-org-profile-connections/) (2021)
-->

*   [コードレビューのための GitHub プルリクエスト](https://ja.wordpress.org/team/handbook/core/contribute/git/github-pull-requests-for-code-review/)
*   [最初の機能のアナウンス](https://make.wordpress.org/core/2020/03/19/associating-github-accounts-with-wordpress-org-profiles/) (2020)
*   [期限が切れたプロフィール接続の通知](https://make.wordpress.org/core/2021/05/03/expired-github-and-wordpress-org-profile-connections/) (2021)
