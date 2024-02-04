# Linking your GitHub and w.org profiles

In the WordPress project, contributions are collected and compiled into the WordPress.org Credits API by WordPress.org usernames. Though contributions happen in many different ways using many different tools, connecting efforts back to an individual’s w.org profile is required to receive attribution for your efforts.

To ensure that you receive credit for any contributions submitted through GitHub, you must link your GitHub and WordPress.org profiles. This includes contributions to Gutenberg, using [GitHub pull requests for code review](https://make.wordpress.org/core/handbook/contribute/git/github-pull-requests-for-code-review/), and contributing to feature plugins under the WordPress organization, such as the [Performance plugin](https://github.com/wordpress/performance).

# How to connect your accounts

WordPress.org uses an oAuth flow to grant a WordPress GitHub application [read-only access](https://make.wordpress.org/core/2021/05/03/expired-github-and-wordpress-org-profile-connections/#comment-41291) to your GitHub account’s public information. This proves that you own both the GitHub account and the WordPress.org account and links the two accounts.

### 1\. Log in to WordPress.org and edit profile

Click “link your GitHub account” to initiate the process.

[![](https://make.wordpress.org/core/files/2020/03/profile-edit.png)](https://make.wordpress.org/core/files/2020/03/profile-edit.png)

### 2\. Authorize WordPress.org Profiles application

Grant the WordPress Profiles GitHub application read-only access to your public information.

[![](https://make.wordpress.org/core/files/2020/03/oauth-screen.png)](https://make.wordpress.org/core/files/2020/03/oauth-screen.png)

### 3\. Verify Connection

Confirm your account is now connected.

[![](https://make.wordpress.org/core/files/2020/03/profile-edit-with-connection-1024x833.png)](https://make.wordpress.org/core/files/2020/03/profile-edit-with-connection.png)

Access can be revoked at any time on the Edit Profile screen on WordPress.org.

### 4\. Add your WordPress.org Git email to your GitHub email list

Visit the [email settings](https://github.com/settings/emails) page on GitHub and add `dotOrgUsername@git.wordpress.org` as an email on your GitHub account.

This is not an actual email, but adding this alias will ensure your contributions appear on your GitHub profile. This is what you should see once you’ve added your w.org email.

[![](https://make.wordpress.org/core/files/2024/01/Screenshot-2024-01-26-at-3.16.17-PM.png)](https://make.wordpress.org/core/files/2024/01/Screenshot-2024-01-26-at-3.16.17-PM.png)

## How do I know if my accounts are connected?

There are a few other ways to check whether your accounts are connected.

### Check your w.org profile

If you have connected your accounts, you’ll notice a “GitHub” field on your profile.

[![](https://make.wordpress.org/core/files/2024/01/gh-connected-w.org-profile.png)](https://make.wordpress.org/core/files/2024/01/gh-connected-w.org-profile.png)

### Check for a w.org redirect

When visiting `https://profiles.wordpress.org/github:GHUSERNAME`, redirect to the connected w.org profile for `GHUSERNAME` if there is a preexisting connection. There is no active connection if you’re redirected to a GitHub w.org profile.

### Check against the w.org API

There’s also an available API to check whether a w.org profile has been connected to a GitHub account.

#### Example

This command will check whether the `desrosj` and `nacin` GitHub accounts are connected to w.org profiles.

```bash
curl https://profiles.wordpress.org/wp-json/wporg-github/v1/lookup/ --data 'github_user[]=desrosj&github_user[]=nacin' -s | jq
```

#### Results

When a connection is active, the slug and profile URL will be returned. `false` is returned when no connection exists. The results are keyed by the GitHub usernames that were passed.

```json
{
  "desrosj": {
    "slug": "desrosj",
    "profile": "https://profiles.wordpress.org/desrosj"
  },
  "nacin": false
}
```

## Helpful links

*   [GitHub Pull Requests for Code Contribution](https://make.wordpress.org/core/handbook/contribute/git/github-pull-requests-for-code-review/)
*   [Initial feature announcement](https://make.wordpress.org/core/2020/03/19/associating-github-accounts-with-wordpress-org-profiles/) (2020)
*   [Notice of expired profile connections](https://make.wordpress.org/core/2021/05/03/expired-github-and-wordpress-org-profile-connections/) (2021)