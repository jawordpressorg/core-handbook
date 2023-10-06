<!--
# Opening a Ticket
-->

# チケットを開く

<!--
## Overview
-->

## 概要

<!--
This article will walk you through the process of opening a ticket on [Trac](https://core.trac.wordpress.org/).
-->

この記事では、[Trac](https://core.trac.wordpress.org/) でチケットを作成する手順を説明します。

<!--
## Getting Started
-->

## はじめに

<!--
[Trac](https://make.wordpress.org/core/glossary/#trac) requires that you log in with your WordPress.org account to open a ticket. If you do not have one, you will need to [register for an account](https://wordpress.org/support/register.php) before proceeding.
-->

[Trac](https://make.wordpress.org/core/glossary/#trac) では、チケットを開くために WordPress.org アカウントでログインする必要があります。もし持っていない場合は、先に[アカウントを登録する](https://wordpress.org/support/register.php)必要があります。

<!--
**Trac Preferences:** You will automatically receive email notifications for tickets you are involved in (you opened the ticket or commented on it). The email account you use for your WordPress.org account is automatically configured in your Trac preferences. You can check your preferences by logging in to Trac, then **clicking the [Preferences](https://core.trac.wordpress.org/prefs) link** at the bottom of the page. You should see the email address these notifications will be sent to when clicking on the *General* tab.
-->

**Trac Preferences:** あなたが関与している (あなたが開いた、またはコメントした) チケットのメール通知を自動的に受け取ることができます。WordPress.org アカウントで使用しているメールアカウントは、Trac preferences で自動的に設定されます。設定内容は、Trac にログインし、ページ下部の **[Preferences](https://core.trac.wordpress.org/prefs) リンクをクリック**することで確認できます。**General** タブをクリックすると、これらの通知が送信されるメールアドレスが表示されます。

<!--
![Trac Preferences General Tab Screen](https://make.wordpress.org/core/files/2013/10/core-trac-preferences-general-tab1.png)
-->

![Trac Preferences General タブの画面](https://make.wordpress.org/core/files/2013/10/core-trac-preferences-general-tab1.png)

<!--
**Are you in the right place?** The information above the ticket form is important – it asks several questions that you need to answer to determine whether your issue is really a bug with WordPress core, a security issue, or a theme/plugin support issue, as well as steps for reporting bugs. It is strongly recommended that you read it before continuing.
-->

**正しい場所にいますか ?** チケットフォームの上にある情報は重要です。あなたの問題が本当に WordPress コアのバグなのか、セキュリティの問題なのか、テーマやプラグインのサポートの問題なのかを判断するために答える必要があるいくつかの質問と、バグを報告するための手順が書かれています。続行する前に、これを読むことを強くおすすめします。

<!--
**Is there an existing ticket?** Take the time to [search](https://core.trac.wordpress.org/search) for an existing ticket that describes the issue you are having, so you do not create a duplicate ticket. If you find an existing ticket for your issue, leave a comment that you are also experiencing the problem (including details). You can also click the star next to the ticket number in the upper left to watch the ticket if you wish to only receive activity notifications for that ticket.
-->

**既存のチケットはありますか ?** 重複したチケットを作成しないように、あなたが抱えている問題を説明する既存のチケットを[検索](https://core.trac.wordpress.org/search)することに時間をかけてください。あなたの問題に関係する既存のチケットが見つかったら、あなたもその問題を経験しているというコメントを残してください (詳細を含めて)。また、そのチケットのアクティビティ通知のみを受け取りたい場合は、左上のチケット番号の横にある星マークをクリックすると、そのチケットを監視できます。


<!--
## Create A New Ticket
-->

## 新しいチケットの作成

<!--
Once you have determined your issue really is a bug, and searched for an existing ticket (and found none), it’s time to create a new ticket.
-->

あなたの問題が本当にバグであると判断し、既存のチケットを検索したら (そして見つからなかったら)、新しいチケットを作成することになります。

<!--
The following is an explanation of the fields to be completed when creating a new ticket. Use the image below as a visual reference for each of the fields.
-->

以下は、新しくチケットを作成するときに記入する項目についての説明です。各項目については、以下の画像を参考にしてください。

<!--
![Trac Submit Ticket Form Screen](https://make.wordpress.org/core/files/2013/10/core-trac-submit-ticket-form.png)
-->

![Trac チケットを提出するフォームの画面](https://make.wordpress.org/core/files/2013/10/core-trac-submit-ticket-form.png)

<!--
**1\. Summary:** A brief summary of the issue that describes the problem.
-->

**1\. Summary:** 問題を説明する簡単な要約。

<!--
**2\. Description:** A detailed description of the issue. Include steps to reproduce the issue consistently. For bugs, describe the actual versus expected results, and attach a screenshot if you need to visually demonstrate the issue. Describe a possible solution for the issue, if known. For enhancements, you should provide proper rationale for making the change.
-->

**2\. Description:** 問題の詳細な説明。問題を一貫して再現するためのステップを含みます。バグについては、実際の結果と予想される結果を記述し、問題を視覚的に示す必要がある場合は、スクリーンショットを添付してください。問題に対する解決策がある場合は、それを記述します。機能強化の場合は、変更するための適切な根拠を示す必要があります。

<!--
**3\. Type:** Tickets fall under one of four types – [defect (bug)](https://make.wordpress.org/core/glossary/#bug), [enhancement](https://make.wordpress.org/core/glossary/#enhancement), [feature request](https://make.wordpress.org/core/glossary/#feature-request), and [task (blessed)](https://make.wordpress.org/core/glossary/#task-blessed).
-->

**3\. タイプ:** チケットは、[defect (bug)](https://make.wordpress.org/core/glossary/#bug)、[enhancement](https://make.wordpress.org/core/glossary/#enhancement)、[feature request](https://make.wordpress.org/core/glossary/#feature-request)、[task (blessed)](https://make.wordpress.org/core/glossary/#task-blessed) の4種類のいずれかに分類されます。

<!--
*   **Defect (bug):** A defect (bug) is an error or unexpected result. After feature freeze, only bugs are dealt with, with regressions (adverse changes from the previous version) being the highest priority.
*   **Enhancement:** These are simple improvements to WordPress, such as the addition of a hook or an improvement to an existing feature.
*   **Feature requests** are proposals for new features, and **tasks (blessed)** are usually created by the core team for development of an approved feature. Most tickets will not have either of these types assigned to them.
-->

*   **Defect (bug):** defect (bug) とは、エラーや予期せぬ結果のことです。機能フリーズ後はバグのみ対応し、リグレッション (前バージョンからの良くない変更) が最優先されます。
*   **Enhancement:** フックの追加や既存機能の改善など、WordPress の簡単な改善です。
*   **Feature requests** は新機能の提案で、**tasks (blessed)** は通常、承認された機能の開発のためにコアチームによって作成されます。ほとんどのチケットには、これらのタイプのいずれかが割り当てられることはありません。

<!--
**4\. Component:** The component is the area of WordPress that the ticket affects. Try to choose specific components, when applicable, over more generalized ones. **Note:** If the issue is related to the **WordPress.org site**, you will need to file the ticket on [meta.trac.wordpress.org](https://meta.trac.wordpress.org/) instead.
-->

**4\. コンポーネント:** コンポーネントは、チケットが影響する WordPress の範囲です。一般的なコンポーネントよりも、該当する場合は特定のコンポーネントを選択するようにしてください。**注意:** 問題が **WordPress.org サイト** に関連している場合、代わりに [meta.trac.wordpress.org](https://meta.trac.wordpress.org/) にチケットを提出する必要があります。

<!--
**5\. Version:** The version of WordPress being used. Ideally, this would be the earliest affected or applicable version.
-->

**5\. Version:** 使用されている WordPress のバージョンです。理想的には、影響を受けるか適用される最も古いバージョンです。

<!--
If you have files to include with the ticket (screenshots or a patch), **check the box** next to **I have files to attach to this ticket**.
-->

チケットに添付するファイル (スクリーンショットやパッチ) がある場合は、**I have files to attach to this ticket** の横にある**ボックスにチェックします**。

<!--
After completing the above fields, **click Continue To Preview** to ensure that you have included all of the information needed to report the bug. The ticket preview will display directly below the ticket form. Review the information, make any changes necessary, then **click Create Ticket**.
-->

上記の項目を入力したら、**Continue To Preview をクリック**し、バグレポートに必要なすべての情報が含まれていることを確認します。チケットのプレビューは、チケットフォームのすぐ下に表示されます。情報を確認し、必要な変更を加えた後、**チケットを作成する**をクリックしてください。

<!--
### Attach Files
-->

### ファイルの添付

<!--
After creating the ticket, the next step is to attach any files necessary to the ticket, such as screenshots or a patch.
-->

チケットを作成したら、次にスクリーンショットやパッチなど、チケットに必要なファイルを添付します。

<!--
Directly below the ticket detail is the **Attachments** section. **Click Attach File** to add a new file to the ticket.
-->

チケットの詳細のすぐ下には、**Attachments** セクションがあります。**Attach File をクリック**すると、チケットに新しいファイルが追加されます。

<!--
![Trac Attach Files Screen](https://make.wordpress.org/core/files/2013/10/core-trac-add-attachments.png)
-->

![Trac ファイルを添付する画面](https://make.wordpress.org/core/files/2013/10/core-trac-add-attachments.png)

<!--
You will be presented with the **Attachment Info** screen.
-->

**Attachment Info** 画面が表示されます。

<!--
![Core Trac Upload File Screen](https://make.wordpress.org/core/files/2013/10/core-trac-upload-file.png)
-->

![Core Trac ファイルアップロード画面](https://make.wordpress.org/core/files/2013/10/core-trac-upload-file.png)

<!--
You will then **click Choose File**. A local window will open to locate the file you wish to attach. **Select the file**, then **click OK**. The filename you chose will display.
-->

次に、**Choose File をクリック**します。ローカルウィンドウが開き、添付したいファイルを探します。**ファイルを選択**し、**OK をクリック**します。選択したファイル名が表示されます。

<!--
Next you can add a description of the file. While this is optional, it is helpful to provide more details about the file.
-->

次に、ファイルの説明を追加できます。これはオプションですが、ファイルについてより詳細な情報を提供するのに便利です。

<!--
*   Screenshots should use `xxxxx.short-description-of-problem.png` as a filename, where `xxxxx` is the ticket number.
*   Patches should be named `xxxxx.diff` or `xxxxx.patch` – both extensions are acceptable.
-->

* スクリーンショットのファイル名は `xxxxx.short-description-of-problem.png` とし、`xxxxx` はチケット番号です。
* パッチは `xxxxx.diff` または `xxxxx.patch` という名前で、拡張子はどちらでもかまいません。

<!--
For patches, Trac will automatically append an incremental number (`xxxxx.2.diff`) to the end of a patch filename to prevent an accidental overwrite of the existing file, in cases where the same patch is submitted multiple times due to needed changes.
-->

パッチは、同じパッチが必要な変更のために複数回提出された場合、誤って既存のファイルを上書きしないように、Trac はパッチファイル名の最後に増分番号 (`xxxxx.2.diff`) を自動的に付加します。

<!--
After you have selected the file and provided an optional description, **click Agree and Upload** .
-->

ファイルを選択し、任意の説明を入力したら、**Agree and Upload をクリック**します。

<!--
Once the upload is complete, a new comment will be automatically added to the ticket with the filename and description listed.
-->

アップロードが完了すると、チケットに新しいコメントが追加され、ファイル名と説明文が記載されます。

<!--
## Next Steps
-->

## 次のステップ

<!--
*   [Submitting A Patch](https://make.wordpress.org/core/handbook/working-with-trac/submitting-a-patch/)
-->

*   [パッチの提出](https://make.wordpress.org/core/handbook/working-with-trac/submitting-a-patch/)

<!--
### Learn More
-->

### より詳しく

<!--
*   [Ticket Properties](https://make.wordpress.org/core/handbook/trac/#ticket-properties)
*   [Trac Workflow Keywords](https://make.wordpress.org/core/handbook/trac/keywords/)
-->

*   [チケットのプロパティ](https://make.wordpress.org/core/handbook/trac/#ticket-properties)
*   [Trac ワークフローキーワード](https://make.wordpress.org/core/handbook/trac/keywords/)
