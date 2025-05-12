<!--
# Preparing the About Page
-->

# アバウトページの準備

<!--
Every WordPress release has an About page. It is shown to users after they finish updating to the new version and includes what the new features are and who contributed to making them.
-->

すべての WordPress のリリースには必ずアバウトページがあります。これは、新しいバージョンへのアップデートが完了した後にユーザーに表示され、新機能の内容や誰が新機能の作成に貢献したかが含まれます。

<!--
This is a great marketing opportunity as lots of people get to see this page. It would be fun to have each major About page customized by one of the designers in the WordPress community (otherwise, we fall back on an existing design).
-->

多くの人がこのページを見ることになるので、これはすばらしいマーケティングの機会です。WordPress コミュニティのデザイナーの誰かによってカスタマイズされた、各メジャーバージョンのアバウトページを見ることも楽しいでしょう (そうでなければ、既存のデザインに頼ることになります)。

<!--
This trend started with WordPress 4.7, you can view the previous designs on Figma: [https://www.figma.com/file/LrjiQZDts99EakxvZ6YcuMIr/About-Page](https://www.figma.com/file/LrjiQZDts99EakxvZ6YcuMIr/About-Page)
-->

この傾向は WordPress 4.7から始まりました。Figma で以前のデザインを見ることができます: [https://www.figma.com/file/LrjiQZDts99EakxvZ6YcuMIr/About-Page](https://www.figma.com/file/LrjiQZDts99EakxvZ6YcuMIr/About-Page)

<!--
If you want to create a page like this, here are the steps to follow:
-->

このようなページを作りたい場合は、以下の手順に従ってください:

<!--
## Steps
-->

## 手順

<!--
*   **Know your deadline**: Work on the About page starts once the release reaches Beta 1 and should be complete by RC1.
*   Create a ticket for the About page kick-off, like this: [https://core.trac.wordpress.org/ticket/46901](https://core.trac.wordpress.org/ticket/46901)
*   Clearly state what steps are:
    *   Coordinate between release leads and either marketing or a copywriter to draft initial page copy
        *   Draft in a google doc so multiple people can write and suggest edits
        *   Check-in with release leads about headline features
        *   Check-in with any feature leads if you’re unclear about details
        *   Go through Beta posts on /news/ to populate features and find copy inspiration
        *   Go through dev notes on make/core to populate developer happiness section
        *   Make sure to go through the features of Gutenberg and create a section to call it out with “new editor feature this release.”
    *   Create images — could be illustrations, icons, or screenshots
    *   Finalize copy (after the release lead’s last review)
    *   Finalize design
    *   Get the page made up
    *   Test the page in various browsers, checking for image quality
*   Release Post (for those leading a release)
    *   Draft new post on wordpress.org/news
    *   Copy content over from the About page
    *   Add images, changing size, alignment, or positioning to fit the blog layout
    *   Pass off to release lead to include credits shortcode and release name
    *   Get the musician’s name from the release squad lead.
    *   Post slug should be wp.org/news/yyyy/mm/musician.
    *   Keep the post with an “album cover” feel.
-->

*   **期限を確認してください**: リリースがベータ1を迎えた時点でアバウトページの作業を開始し、RC1までに完了する必要があります。
*   以下のように、アバウトページのキックオフ用チケットを作成してください: [https://core.trac.wordpress.org/ticket/46901](https://core.trac.wordpress.org/ticket/46901)
*   どのような手順であるかを明確にします:
    *   リリースリードとマーケティングまたはコピーライターの間で調整し、最初のページコピーの草案を作成する
        *   複数の人が書いたり編集を提案できるように、google ドキュメントでドラフトを作成する
        *   ヘッドライン機能についてリリースリードに確認する
        *   詳細が不明な場合、その機能のリードにも確認する
        *   /news/ にあるベータ版の投稿を参照して機能を追加し、コピーのヒントを見つける
        *   make/core の開発者ノートを参照して、開発者のためになるセクションを入力する
        *   Gutenberg の機能を確認し、「このリリースの新しいエディター機能」と呼びかけるセクションを作る
    *   画像の作成 - イラスト、アイコン、スクリーンショットなど
    *   コピーを完成させる (リリースリードの最後のレビュー後に)
    *   デザインを完成させる
    *   ページを作成する
    *   さまざまなブラウザでページをテストし、画質をチェックする
*   リリース投稿 (リリースをリードする人向け)
    *   wordpress.org/news に新しい投稿の下書きを作成する
    *   アバウトページからコンテンツをコピーする
    *   ブログのレイアウトに合わせて画像を追加したり、サイズ、配置、位置を変更したりする
    *   クレジットのショートコードとリリース名を含めるために、リリースリードに引き継ぐ
    *   リリースチームからミュージシャンの名前を取得する。
    *   投稿のスラッグは wp.org/news/yyyy/mm/musician である必要があります。
    *   「アルバムの表紙」のような雰囲気の投稿を心がけます。

<!--
## Copy
-->

## コピー

<!--
*   **Audience**: WordPress users and practitioners who are not active in contributing. Assume non-technical.
*   **Purpose**: To highlight the immediately interesting things and inspire people to experiment and/or learn more. Assume no need to sell WordPress to them.
*   **Property**: WordPress software
*   **Assets**: Assume that the copy flow will follow the design flow.
*   **Voice**: Aim for the positive side of neutral, though you can go all the way to cheerfully American Southern. Not a sales-y voice, since these are people already using WordPress.
-->

*   **対象者**: 積極的に貢献していない WordPress ユーザー。技術的ではないことを想定します。
*   **目的**: すぐに興味をひかれるものを強調し、人々に実験や学習を促すこと。彼らに WordPress を売り込む必要はありません。
*   **プロパティ**: WordPress ソフトウェア
*   **アセット**: コピーの流れはデザインの流れに従うと想定します。
*   **トーン**: 陽気な感じでも良いですが、ニュートラルでポジティブであることを目指します。すでに WordPress を使っている人たちですので、営業的な口調ではありません。

<!--
## Design
-->

## デザイン

<!--
The About Page has a set framework and it is not meant to be redesigned from scratch each release.
-->

アバウトページには決まったフレームワークがあり、リリースのたびに最初から再設計されるものではありません。

<!--
The layout should be considered a stack of containers, which can be 1-4 columns. The content in the columns can be anything — text, video, images, embeds, etc. These containers can have no background color, a “subtle” background color, or “accent” background color (these change with each About page using colors from the header feature). Columns can also have one of these background colors. Containers are stacked on top of each other to create the page.
-->

レイアウトは、1-4カラムのコンテナの積み重ねと考えるべきです。カラム内のコンテンツは、テキスト、ビデオ、画像、埋め込みなど何でもかまいません。これらのコンテナは、背景色なし、「わずかな」背景色、または「アクセント」背景色を持つことができます (これらは、ヘッダー機能からの色を使用して、各アバウトページで変更されます)。カラムもこれらの背景色のいずれかを持つことができます。コンテナを積み重ねて、ページを作成します。

<!--
Wondering why the About Page is not done in the block editor? The biggest blocker is translations. Every string on the page is wrapped in a translation function, with additional translation notes as needed. We’d need to find a way to do that with Gutenberg as well. 
-->

なぜブロックエディターでアバウトページが作成されないのか疑問に思いませんか ? 最大の障害は翻訳です。ページ上のすべての文字列は翻訳関数で囲まれ、必要に応じて翻訳メモが追加されます。Gutenberg ではまだそのようなことができません。

<!--
Some items to watch for:
-->

いくつか注意すべき点があります:

<!--
*   The header has the most freedom. It can have a design element background or text effect. Check that it is accessible.
*   Images, illustrations, and videos are allowed in the content.
*   There can be 1, 2, 3, or 4 columns and have a colored background.
*   For technical documentation, see [the about patterns demo plugin](https://github.com/ryelle/about-patterns).
*   Talk to @ryelle about it. She is in charge of coding and committing the About Page.
-->

*   ヘッダーが一番自由度が高いです。デザイン要素の背景やテキスト効果を含めることができます。アクセシブルであることを確認してください。
*   コンテンツに画像、イラスト、動画を使用できます。
*   1、2、3、または4カラムがあり、色付きの背景を持つことができます。
*   技術的なドキュメントは [about patterns demo plugin](https://github.com/ryelle/about-patterns) を参照してください。
*   @ryelle に相談してください。彼女はアバウトページのコーディングとコミットを担当しています。

<!--
Examples of how the boxes can look like:
-->

ボックスがどのように見えるかの例:

[![](https://make.wordpress.org/core/files/2021/06/about-demo-2col-162x300.png)](https://make.wordpress.org/core/files/2021/06/about-demo-2col.png)

[![](https://make.wordpress.org/core/files/2021/06/about-demo-3col-1024x488.png)](https://make.wordpress.org/core/files/2021/06/about-demo-3col.png)

[![](https://make.wordpress.org/core/files/2021/06/about-demo-4col-1024x432.png)](https://make.wordpress.org/core/files/2021/06/about-demo-4col.png)

[![](https://make.wordpress.org/core/files/2023/07/Screen-Shot-2023-07-18-at-14.40.20-1024x296.png)](https://make.wordpress.org/core/files/2023/07/Screen-Shot-2023-07-18-at-14.40.20.png)

<!--
### Images
-->

### 画像

<!--
For better understanding see the image above. Some things to consider:
-->

よりよく理解するには、上の画像を参照してください。考慮すべき点がいくつかあります:

<!--
*   Images can be edge-to-edge or have a 32px padding on all four sides.
*   Images and videos resize a bit on mobile.
*   Images should be decorative, just illustrating the content they’re next to — if an image conveys meaning, it needs to have alt text.
*   Images should limit or avoid English text, including UI text, because we don’t currently have a method for [translating screenshots](https://core.trac.wordpress.org/ticket/58354).
*   Use icons to accent smaller columns/content
-->

*   画像は端から端まで表示することも、4辺すべてに32ピクセルのパディングを付けることもできます。
*   モバイルでは、画像や動画のサイズが少し変わります。
*   画像は、隣にあるコンテンツを示すだけの装飾的なものである必要があります。画像が意味を伝える場合は、代替テキストが必要です。
*   [スクリーンショットを翻訳する](https://core.trac.wordpress.org/ticket/58354)方法が現在ないので、画像は UI テキストを含む英語のテキストを制限するか避けるべきです。
*   アイコンを使用して小さなカラム/コンテンツを強調します。

<!--
### Videos
-->

### ビデオ

<!--
**For accessibility,** if the video has voice audio, a text equivalent needs to be provided. If the video shows a flow or action being performed, then the process needs to be described in the text. The key thing is remembering the audience for the text description need to get the same level of information as a sighted audience gets from watching.
-->

**アクセシビリティのため、** ビデオに音声が含まれる場合は、同等のテキストを提供する必要があります。ビデオでフローやアクションの実行が示されている場合は、そのプロセスをテキストで説明する必要があります。重要なことは、テキストによる説明を読む人は、視聴者が観るものと同じレベルの情報を得る必要があることを覚えておくことです。

<!--
What matters is that it’s clear that the video’s description is associated with the video, use figure and figcaption for this.
-->

重要なことは、動画の説明が動画に関連付けられていることが明らかであることで、これには図と図のキャプションを使用します。

<!--
**Tech reqs**
-->

**技術的な要件**

<!--
*   Videos must be 480px wide (in general, most users will see this video at 436px wide, large phone sizes might see it up to 488px)
*   The space for a full-width video is 1000px wide, and for a wider 2 column layout is 536px.
*   Record using Kap (this is different than the recommendation in the post but @joen recommended this instead of Screeny)
*   Convert .mov files to .mp4 using FFMPEG. Kap does appear to have the ability to export as MP4 and WebM though. Using that is preferable to converting if it works well.
*   [How to: Good UI demo videos](https://automattic.design/2019/11/12/good-ui-demo-videos/)
-->

*   動画は480ピクセル幅でなければなりません (一般的に、ほとんどのユーザーは436ピクセル幅でこのビデオを見るでしょう、大きな携帯電話のサイズでは最大488ピクセルで表示される場合があります)。
*   全幅ビデオのスペースは幅1000ピクセルで、ワイドな2カラムレイアウトの場合は536ピクセルです。
*   Kap を使って録画します (これは投稿の推奨とは異なりますが、@joen は Screeny の代わりにこれを推奨しています)。
*   FFMPEG を使用して .mov ファイルを .mp4 に変換します。Kap には MP4 や WebM としてエクスポートする機能があるようです。うまく機能する場合は、変換するよりもそれを使用することをおすすめします。
*   [ハウツー: 優れた UI を持つデモビデオ](https://automattic.design/2019/11/12/good-ui-demo-videos/)

<!--
## Development
-->

## 開発

<!--
While the “About page” typically means `/wp-admin/about.php`, the updates in this ticket usually also apply to the whole section, `/wp-admin/contribute.php`, `/wp-admin/credits.php`, `/wp-admin/freedoms.php`, and `/wp-admin/privacy.php`. The content on the other pages rarely changes.
-->

「アバウトページ」は通常 `/wp-admin/about.php` を指しますが、このチケットの更新は通常 `/wp-admin/contribute.php`、`/wp-admin/credits.php`、`/wp-admin/freedoms.php`、`/wp-admin/privacy.php` のセクション全体にも適用されます。他のページのコンテンツはほとんど変更されません。

<!--
Once a content draft & layout have been signed off by the marketing & design teams, the page can begin in code.
-->

コンテンツのドラフトとレイアウトがマーケティングとデザインのチームによって承認されると、ページのコードを書き始めることができます。

<!--
### Copy content from the doc
-->

### ドキュメントからコンテンツをコピーする

<!--
Lay the content out in sections & columns to match the design. Make sure to wrap content in translation functions. If there are links, use `printf` and placeholders, and maybe translate the destination link too.
-->

デザインに合わせて、セクションやカラムにコンテンツをレイアウトします。コンテンツは必ず翻訳関数で囲んでください。リンクがある場合は、`printf` とプレースホルダーを使用し、場合によってはリンク先のリンクも翻訳します。

<!--
### Update the color custom properties
-->

### カラーカスタムプロパティを更新する

<!--
If the colors have changed, update these in `/css/about.css`. Sometimes some color properties are not used, you can leave them alone — some are used on other pages (for example, contribute uses `has-subtle-background-color`). Use the [about-patterns plugin](https://github.com/ryelle/about-patterns) to help test out your CSS changes.
-->

色が変わった場合は、`/css/about.css` で更新します。いくつかの色のプロパティは使用されない場合がありますが、そのままにしておくことができます。一部は他のページで使用されます (たとえば、contribute は `has-subtle-background-color` を使用します)。[about-patterns プラグイン](https://github.com/ryelle/about-patterns)を使用すると、CSS の変更をテストできます。

<!--
### Export assets from Figma
-->

### Figma からアセットをエクスポートする

<!--
The following are exported as SVG and saved locally. Use something like [svgomgui](https://jakearchibald.github.io/svgomg/) to optimize SVGs before saving them in `/wp-admin/images/`.
-->

以下は SVG としてエクスポートし、ローカルに保存したものです。[svgomgui](https://jakearchibald.github.io/svgomg/) のようなものを使って、`/wp-admin/images/` に保存する前に SVG を最適化します。

<!--
*   Page headers, export without the text, `about-header-*.svg`
*   Illustrations on freedoms, privacy, and contribute, `freedom-1.svg`, `freedom-2.svg`, etc; `privacy.svg`, `contribute-1.svg`, etc.
*   Release badge, `about-release-badge.svg`
-->

*   ページヘッダー: テキストなしでエクスポート、`about-header-*.svg`
*   自由、プライバシー、貢献に関するイラスト: `freedom-1.svg`、`freedom-2.svg`、`privacy.svg`、`contribute-1.svg` など。
*   リリースバッジ: `about-release-badge.svg`

<!--
The icons in the About page content are SVGs used inline, so export those and make sure `aria-hidden="true" focusable="false"` are on the `svg` tag.
-->

アバウトページのコンテンツのアイコンはインラインで使用される SVG ですので、それらをエクスポートし、`aria-hidden="true" focusable="false"` が `svg` タグにあることを確認してください。

<!--
The feature screenshots are raster images, export these at 2x and convert to webp. They’re added to the page from external links, so use make.w.org if they’re still in flux. When finalized, upload to the s.w.org CDN (needs dotorg committer).
-->

機能のスクリーンショットはラスターイメージですので、2倍でエクスポートして WebP に変換します。これらは外部リンクからページに追加されるため、まだ流動的な場合は make.w.org を使用してください。完成したら、s.w.org CDN にアップロードします (dotorg コミッターが必要です)。

<!--
### Update URLs in the content
-->

### コンテンツ内の URL を更新する

<!--
Local images usually use a query string to break caching, so update the version before release. For example, [see this line in freedoms.php](https://github.com/WordPress/wordpress-develop/blob/d6f72bad6f224a36627a5500a9c3e8ffb4eee524/src/wp-admin/freedoms.php#L61). This is not necessary for CDN images since those URLs change each release.
-->

ローカル画像は通常、キャッシュを更新するためのクエリー文字列を使用するので、リリース前にバージョンを更新してください。たとえば、[freedoms.php のこの行を参照してください](https://github.com/WordPress/wordpress-develop/blob/d6f72bad6f224a36627a5500a9c3e8ffb4eee524/src/wp-admin/freedoms.php#L61)。CDN イメージの場合はリリースごとに URL が変更されるため、これは必要ありません。

<!--
The [field guide URL in `about.php`](https://github.com/WordPress/wordpress-develop/blob/d6f72bad6f224a36627a5500a9c3e8ffb4eee524/src/wp-admin/about.php#L272) should also be updated when that post is published (usually around RC). The release notes URL is generated and should work once that page is published, but [the version number should be updated here](https://github.com/WordPress/wordpress-develop/blob/d6f72bad6f224a36627a5500a9c3e8ffb4eee524/src/wp-admin/about.php#L285-L298).
-->

また、[`about.php` のフィールドガイド URL](https://github.com/WordPress/wordpress-develop/blob/d6f72bad6f224a36627a5500a9c3e8ffb4eee524/src/wp-admin/about.php#L272) も、その投稿が公開されたとき (通常は RC のころ) に更新する必要があります。リリースノートの URL が生成され、そのページが公開されれば機能するはずですが、[バージョン番号はここで更新される必要があります](https://github.com/WordPress/wordpress-develop/blob/d6f72bad6f224a36627a5500a9c3e8ffb4eee524/src/wp-admin/about.php#L285-L298)。

<!--
If any content in the page had links using placeholders, update those.
-->

ページ内のコンテンツにプレースホルダーを使ったリンクが含まれているは、それらを更新してください。

<!--
### Development timeline
-->

### 開発スケジュール

<!--
The timeline for this page depends on multiple teams, and there are a lot of things to wrangle, so the timeline needs to be flexible.
-->

このページのタイムラインは複数のチームに依存しており、議論すべきことがたくさんあるため、タイムラインは柔軟である必要があります。

<!--
*   beta3 (or the last beta before release): Commit the first-final draft of the page, basic layout and design.
*   RC1: Commit the final draft of the page, update any finalized assets.
*   During RC: Upload and commit the feature screenshots, update any URLs, update finalized assets.
-->

*   ベータ3 (またはリリース前の最後のベータ): ページの最初の最終案、基本的なレイアウトとデザインをコミットします
*   RC1: ページの最終的な下書きをコミットし、完成したアセットを更新します。
*   RC 中: 機能のスクリーンショットをアップロードしてコミットし、URL を更新し、完成したなアセットを更新します。

<!--
No string changes should happen after RC1, but exceptions are made, for example if something is technically inaccurate.
-->

RC1以降に文字列の変更は行うべきではありませんが、技術的に不正確な場合などは例外が発生します。

<!--
## Development
-->

## 開発

<!--
While the “About page” typically means `/wp-admin/about.php`, the updates in this ticket usually also apply to the whole section, `/wp-admin/contribute.php`, `/wp-admin/credits.php`, `/wp-admin/freedoms.php`, and `/wp-admin/privacy.php`. The content on the other pages rarely changes.
-->

「アバウトページ」は通常 `/wp-admin/about.php` を指しますが、このチケットでの更新は通常、`/wp-admin/contribute.php`、`/wp-admin/credits.php`、`/wp-admin/freedoms.php`、`/wp-admin/privacy.php` セクション全体に適用されます。他のページのコンテンツはほとんど変更されません。

<!--
Once a content draft & layout have been signed off by the marketing & design teams, the page can begin in code.
-->

マーケティングチームとデザインチームがコンテンツのドラフトとレイアウトを承認したら、ページのコード作成を開始できます。

<!--
### Copy content from the doc
-->

### ドキュメントからコンテンツをコピーする

<!--
Lay the content out in sections & columns to match the design. Make sure to wrap content in translation functions. If there are links, use `printf` and placeholders, and maybe translate the destination link too.
-->

デザインに合わせて、コンテンツをセクションと列にレイアウトします。翻訳関数でコンテンツを囲むようにしてください。リンクがある場合は、`printf` とプレースホルダーを使用し、リンク先も翻訳するとよいでしょう。

<!--
### Update the color custom properties
-->

### 色のカスタムプロパティを更新する

<!--
If the colors have changed, update these in `/css/about.css`. Sometimes some color properties are not used, you can leave them alone — some are used on other pages (for example, contribute uses `has-subtle-background-color`). Use the [about-patterns plugin](https://github.com/ryelle/about-patterns) to help test out your CSS changes.
-->

色が変更された場合は、`/css/about.css` でこれらのプロパティを更新します。場合によっては、他のページで使用されている色プロパティ (例えば、contribute では `has-subtle-background-color` を使用しています) があるため、そのままにしておくことができます。[about-patterns プラグイン](https://github.com/ryelle/about-patterns)を使用すると、CSS の変更をテストしやすくなります。

<!--
### Export assets from Figma
-->

### Figma からアセットをエクスポートする

<!--
The following are exported as SVG and saved locally. Use something like [svgomgui](https://jakearchibald.github.io/svgomg/) to optimize SVGs before saving them in `/wp-admin/images/`.
-->

以下のアセットは SVG としてエクスポートされ、ローカルに保存されます。[svgomgui](https://jakearchibald.github.io/svgomg/) などのツールを使用して SVG を最適化してから、`/wp-admin/images/` に保存してください。

<!--
*   Page headers, export without the text, `about-header-*.svg`
*   Illustrations on freedoms, privacy, and contribute, `freedom-1.svg`, `freedom-2.svg`, etc; `privacy.svg`, `contribute-1.svg`, etc.
*   Release badge, `about-release-badge.svg`
-->

*   ページヘッダー (テキストを除いたエクスポート): `about-header-*.svg`
*   自由、プライバシー、貢献に関するイラスト: `freedom-1.svg`、`freedom-2.svg` など。`privacy.svg`、`contribute-1.svg` など。
*   リリースバッジ: `about-release-badge.svg`

<!--
The icons in the About page content are SVGs used inline, so export those and make sure `aria-hidden="true" focusable="false"` are on the `svg` tag.
-->

アバウトページのコンテンツ内アイコンはインライン SVG なので、エクスポートし、`aria-hidden="true" focusable="false"` が `svg` タグに設定されていることを確認してください。

<!--
The feature screenshots are raster images, export these at 2x and convert to webp. They’re added to the page from external links, so use make.w.org if they’re still in flux. When finalized, upload to the s.w.org CDN (needs dotorg committer).
-->

機能のスクリーンショットはラスター画像なので、2倍でエクスポートし、webp に変換してください。これらは外部リンクからページに追加されるため、まだ準備段階であれば make.w.org を使用してください。完成したら、s.w.org CDN にアップロードしてください (dotorg コミッターの協力が必要です)。

<!--
### Update URLs in the content
-->

### コンテンツ内の URL を更新する

<!--
Local images usually use a query string to break caching, so update the version before release. For example, [see this line in freedoms.php](https://github.com/WordPress/wordpress-develop/blob/d6f72bad6f224a36627a5500a9c3e8ffb4eee524/src/wp-admin/freedoms.php#L61). This is not necessary for CDN images since those URLs change each release.
-->

ローカル画像は通常、キャッシュを解除するためにクエリー文字列を使用しているため、リリース前にバージョンを更新してください。たとえば、[freedoms.php のこの行を参照してください](https://github.com/WordPress/wordpress-develop/blob/d6f72bad6f224a36627a5500a9c3e8ffb4eee524/src/wp-admin/freedoms.php#L61)。CDN 画像の場合は、URL がリリースごとに変更されるため、この作業は不要です。

<!--
The [field guide URL in `about.php`](https://github.com/WordPress/wordpress-develop/blob/d6f72bad6f224a36627a5500a9c3e8ffb4eee524/src/wp-admin/about.php#L272) should also be updated when that post is published (usually around RC). The release notes URL is generated and should work once that page is published, but [the version number should be updated here](https://github.com/WordPress/wordpress-develop/blob/d6f72bad6f224a36627a5500a9c3e8ffb4eee524/src/wp-admin/about.php#L285-L298).
-->

[`about.php` 内のフィールドガイドの URL](https://github.com/WordPress/wordpress-develop/blob/d6f72bad6f224a36627a5500a9c3e8ffb4eee524/src/wp-admin/about.php#L272) も、その投稿が公開された際 (通常はリリース版前後) に更新する必要があります。リリースノートの URL は生成され、そのページが公開されると有効になるはずですが、[ここでバージョン番号を更新する必要があります](https://github.com/WordPress/wordpress-develop/blob/d6f72bad6f224a36627a5500a9c3e8ffb4eee524/src/wp-admin/about.php#L285-L298)。

<!--
If any content in the page had links using placeholders, update those.
-->

ページ内のコンテンツにプレースホルダーを使用したリンクがある場合は、それらを更新してください。

<!--
### Development timeline
-->

### 開発のタイムライン

<!--
The timeline for this page depends on multiple teams, and there are a lot of things to wrangle, so the timeline needs to be flexible.
-->

このページのタイムラインは複数のチームに依存しており、調整すべき事項が多数あるため、タイムラインは柔軟に対応する必要があります。

<!--
*   beta3 (or the last beta before release): Commit the first-final draft of the page, basic layout and design.
*   RC1: Commit the final draft of the page, update any finalized assets.
*   During RC: Upload and commit the feature screenshots, update any URLs, update finalized assets.
-->

*   ベータ3 (またはリリース前の最後のベータ): ページの最初の最終ドラフト、基本的なレイアウトとデザインをコミットします。
*   RC1: ページの最終ドラフトをコミットし、確定済みのアセットを更新します。
*   RC 中: 機能のスクリーンショットをアップロードしてコミットし、URL を更新し、確定​​済みのアセットを更新します。

<!--
No string changes should happen after RC1, but exceptions are made, for example if something is technically inaccurate.
-->

RC1以降は文字列の変更は行いませんが、技術的に不正確な点がある場合などは、例外が認められます。

## Props

<!--
The props (or credits) within a release are collected by the Release Squad, and embedded in the About Page (and Release Announcement Post) via a shortcode. Gutenberg credits are collected via GitHub and added to the Credits API via a Meta Trac ticket (e.g., [5.7](https://meta.trac.wordpress.org/ticket/5649)). All non-code contributions are gathered by the Release Squad focus leads and also added to the Credits API. Finally the list of Noteworthy Contributors is assembled by the Release Squad and submitted as a Credits API update (e.g., [5.7](https://docs.google.com/spreadsheets/d/11pA2LM67fQ3q89ok-oMcGlzE1_vOJkPBMkn1tLGtWbI/edit#gid=1989970429)).
-->

リリース内の prop (またはクレジット) はリリースチームによって収集され、ショートコードを介してアバウトページ (およびリリースを告知する投稿) に埋め込まれます。Gutenberg のクレジットは GitHub 経由で収集され、Meta Trac チケット (例: [5.7](https://meta.trac.wordpress.org/ticket/5649)) 経由でクレジット API に追加されます。コード以外の貢献はすべてリリースチームのフォーカスリードによって集められ、同じくクレジット API に追加されます。最後に、注目すべき貢献者のリストがリリースチームによってまとめられ、クレジット API の更新として提出されます (例: [5.7](https://docs.google.com/spreadsheets/d/11pA2LM67fQ3q89ok-oMcGlzE1_vOJkPBMkn1tLGtWbI/edit#gid=1989970429))。

<!--
When working to match GitHub usernames to WordPress.org usernames you can use [`https://profiles.wordpress.org/github:username`](https://profiles.wordpress.org/github:noisysocks) where putting the GitHub username at the end of that URL will translate to the respective WordPress.org profile. This will work for any user who has [associated their GitHub account with their WordPress.org profile](https://make.wordpress.org/core/2020/03/19/associating-github-accounts-with-wordpress-org-profiles/). There is a similar method for converting a Slack username to a WordPress.org username by using [`https://profiles.wordpress.org/$slack_id`](https://profiles.wordpress.org/%24slack_id) where the Slack ID comes from a Slack user’s details (Click and avatar > View full profile > More \[…\] > Copy ID).
-->

GitHub のユーザー名と WordPress.org のユーザー名を一致させるには、[`https://profiles.wordpress.org/github:username`](https://profiles.wordpress.org/github:noisysocks) を使います。URL の末尾に GitHub のユーザー名をつけると、それぞれの WordPress.org のプロフィールに変換されます。これは、[GitHub アカウントと WordPress.org プロフィールを関連付けている](https://make.wordpress.org/core/2020/03/19/associating-github-accounts-with-wordpress-org-profiles/)ユーザーであれば誰でも機能します。[`https://profiles.wordpress.org/$slack_id`](https://profiles.wordpress.org/%24slack_id) を使用して Slack ユーザー名を WordPress.org ユーザー名に変換する同様の方法もあります。Slack ID は Slack ユーザーの詳細 (クリックしてアバター > プロフィールをすべて表示 > もっと見る[...] > ID をコピー) から取得します。
