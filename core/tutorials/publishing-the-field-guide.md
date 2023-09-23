<!--
# Publishing the Field Guide
-->

# フィールドガイドの投稿

<!--
The Field Guide is published on [Make/Core](https://make.wordpress.org/core/) and highlights the developer-focuses changes in a major release. Ideally all new and modified hooks are noted in a bulleted list (e.g., [4.8](https://make.wordpress.org/core/2017/05/26/wordpress-4-8-field-guide/)).
-->

フィールドガイドは [Make/Core](https://make.wordpress.org/core/) で公開され、メジャーリリースにおける開発者向けの変更点をハイライトしています。理想的には、すべての新しいフックと修正されたフックが箇条書きリスト (例: [4.8](https://make.wordpress.org/core/2017/05/26/wordpress-4-8-field-guide/)) に記されます。

<!--
Start drafting the Field Guide early in the release cycle (generally around Beta 1) and slowly embed [dev notes](https://make.wordpress.org/core/handbook/tutorials/writing-developer-notes/) as they get published. A week or so before Release Candidate 1 you will want to reserve 2-4 hours to work on copy, formatting, link updating and other tweaks to have the first real draft of the Field Guide ready. Around this time you will want to send the Slack group direct messages to Component Maintainers to give them all a couple days to provide feedback on the bullet points in the `But Wait, There Is More` section. At the same time you will want to obtain reviews from others on the release squad so that all feedback completes around the same time and allows publishing the Field Guide as close to RC1 as possible.
-->

フィールドガイドの草稿をリリースサイクルの早い段階 (一般的にはベータ1のころ) から作り始め、[開発者ノート](https://make.wordpress.org/core/handbook/tutorials/writing-developer-notes/)が公開されるにつれてゆっくりと埋め込んでください。リリース候補1の1週間ほど前には、コピー、フォーマット、リンクの更新、その他の微調整に2～4時間を確保し、フィールドガイドの最初の本格的なドラフトを準備してください。このころ、あなたは Slack グループのコンポーネントメンテナーにダイレクトメッセージを送り、`But Wait, There Is More` セクションの箇条書きについてフィードバックを提供するために数日の時間を与えたいと思うでしょう。同時に、すべてのフィードバックが同じ時期に完了し、フィールドガイドをできるだけ RC1に近い形で公開できるように、リリースチームの他のメンバーからもレビューを得たいと思うでしょう。

<!--
The following is a general process that the Release Coordinator and/or Documentation Lead will use to craft the Field Guide for a release:
-->

以下は、リリースコーディネーターおよび/またはドキュメントリーダーが、リリースのためのフィールドガイドを作成するために使用する一般的なプロセスです:

<!--
*   Copy previous release Field Guide (e.g. [5.6](https://make.wordpress.org/core/2020/11/20/wordpress-5-6-field-guide/)), rename and update copy to current release version number
*   Update all links to point to current release version number
*   Remove previously embedded dev notes
*   As new dev notes for the current release cycle get published, embed them in the respective section of the Field Guide
*   Update the Field Guide heading with the major focuses from the release
*   Update section listings to relate to areas receiving dev notes
*   Add/update section summary pulling major highlights from embedded dev notes to help developers know whether those dev notes are relevant to them or not
*   Each Component team is sent a group direct message in Slack, pulling the list of maintainers from the [individual component pages](https://make.wordpress.org/core/components/):
-->

*   以前のリリースのフィールドガイド (例: [5.6](https://make.wordpress.org/core/2020/11/20/wordpress-5-6-field-guide/)) をコピーし、名前を変更し、コピーを現在のリリースバージョン番号に更新する
*   すべてのリンクを現在のリリースのバージョン番号に更新する
*   以前埋め込まれていた開発ノートを削除する
*   現在のリリースサイクルの新しい開発ノートが発行されたら、フィールドガイドのそれぞれのセクションに埋め込む
*   フィールドガイドの見出しを、リリースの重要な点で更新する
*   開発ノートを受け取った分野に関連するセクションのリストを更新する
*   埋め込まれた開発者ノートから主要なハイライトを抜き出し、開発者がその開発者ノートが自分に関連するかどうかを知ることができるように、セクションの要約を追加・更新する
*   各コンポーネントチームには、[個々のコンポーネントページ](https://make.wordpress.org/core/components/)からメンテナーのリストを抽出して、Slack でグループダイレクトメッセージを送信する:

> It’s that time again `Component Name` component maintainer(s)… are there any tickets in the X.Y release that you’d like called out in the Field Guide that aren’t already included in a Dev Note? As a reference, here are the ## tickets currently in the milestone for you: [https://core.trac.wordpress.org/query?component=ComponentName&milestone=X.Y&col=id&col=summary&col=milestone&col=owner&col=type&col=status&col=priority&order=priority](https://core.trac.wordpress.org/query?component=ComponentName&milestone=X.Y&col=id&col=summary&col=milestone&col=owner&col=type&col=status&col=priority&order=priority). Note that we intend to publish the Field Guide next week, so the sooner you can respond the better… thanks!

<!--
*   The responses are added into the `But Wait, There is More!` section of the Field Guide as individual bullet items in the format of:
    *   Component Name: Trac Ticket Summary ([#Trac-Number](https://make.wordpress.org/core/tag/trac-number/)).
-->

*   その回答は、フィールドガイドの `But Wait, There is More!` セクションに、箇条書きの項目として追加されます:
    *   コンポーネント名: Trac チケットの要約 ([#Trac-Number](https://make.wordpress.org/core/tag/trac-number/))。

<!--
Find at least one reviewer from the release squad, but ideally one technical review and one marketing/copy review, to ensure the Field Guide is as well-written as possible within your timeframe. From there it’s published with the version number “X-Y” and “field-guide” tags.
-->

リリースチームから少なくとも一人、理想的には技術レビュー一人とマーケティング/コピーレビュー一人のレビュアーを見つけて、あなたの時間内で可能な限り、フィールドガイドがよくまとめられていることを確認します。そこから、バージョン番号「X-Y」と「field-guide」タグを付けて投稿します。
