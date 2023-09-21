<!--
# Writing Patches
-->

# パッチを書く

<!--
## Picking a ticket
-->

## チケットを選ぶ

<!--
*   [Pick a bug to work on](https://make.wordpress.org/core/handbook/contribute/fixing-bugs/#finding-bugs-to-fix)
*   Work on the most important bugs first
*   Make sure documentation gets updated
*   Take extra time to do it right the first time
*   Test your code
*   Regressions are bad
*   Smaller patches get reviewed faster
*   Work on multiple bugs in parallel
*   Get advice before, not after
*   More detail for these guidelines here: [Mozilla Development Strategies](https://developer.mozilla.org/en/Mozilla_Development_Strategies)
*   Review disagreements best handled quickly in [Slack](https://make.wordpress.org/chat/) with summary on [Trac](https://core.trac.wordpress.org/)
-->

*   [取り組むべきバグを選ぶ](https://make.wordpress.org/core/handbook/contribute/fixing-bugs/#finding-bugs-to-fix)
*   最初に最も重要なバグに取り組む
*   ドキュメントが更新されていることを確認する
*   最初から正しく行うために、時間をかける
*   コードをテストする
*   リグレッションは良くない
*   小さなパッチほどはやくレビューされる
*   複数のバグに並行して取り組む
*   後ではなく事前にアドバイスを得る
*   これらのガイドラインの詳細については、こちらをご覧ください: [Mozilla 開発戦略](https://developer.mozilla.org/en/Mozilla_Development_Strategies)
*   レビューの相違は [Slack](https://make.wordpress.org/chat/) ですばやく処理し、[Trac](https://core.trac.wordpress.org/) にまとめることがベストです

<!--
## Requirements for patches
-->

## パッチの要件

<!--
*   Inline documentation
*   [Automated testing (spin-off)](https://make.wordpress.org/core/handbook/automated-testing/)
*   Feature requests
*   [WP\_DEBUG](https://codex.wordpress.org/Debugging_in_WordPress#WP_DEBUG), [SCRIPT\_DEBUG](https://codex.wordpress.org/Debugging_in_WordPress#SCRIPT_DEBUG)
*   Patch development scripts, and don’t minimize
*   Images (attach originals)
*   Patches should be made against the latest code in the SVN repository
*   Patches should be made against the root WordPress directory (not against a subdirectory)
*   … however, if your patch includes tests, both the code changes and tests can be included in the same patch.
*   Patches should adhere to the [coding standards](https://make.wordpress.org/core/handbook/coding-standards/)
-->

*   インラインドキュメント
*   [自動テスト (スピンオフ)](https://make.wordpress.org/core/handbook/automated-testing/)
*   機能リクエスト
*   [WP\_DEBUG](https://codex.wordpress.org/Debugging_in_WordPress#WP_DEBUG) と [SCRIPT\_DEBUG](https://codex.wordpress.org/Debugging_in_WordPress#SCRIPT_DEBUG)
*   開発スクリプトにパッチを適用し、最小化しない
*   画像 (オリジナルを添付すること)
*   パッチは SVN リポジトリの最新のコードに対して作成されるべきです
*   パッチは WordPress のルートディレクトリに対して作成されるべきです (サブディレクトリに対してではありません)
*   ただし、パッチにテストが含まれている場合は、コードの変更とテストの両方を同じパッチに含めることができます。
*   パッチが[コーディング規約](https://make.wordpress.org/core/handbook/coding-standards/)に従っていること

<!--
## Expectations for patches
-->

## パッチに期待されること

<!--
*   Expect rounds of feedback
*   Expect potential for rejection (wontfix, invalid, plugin, etc.)
*   Understand it may not be a priority
*   Bugs: Expect steps to reproduce
*   Enhancements: Expect request for justification
*   UI/UX: There is a separate process
-->

*   一連のフィードバック
*   却下される可能性もあります (wontfix、無効、プラグインなど)
*   優先順位が低いかもしれないこと
*   バグの場合、再現するためのステップ
*   機能強化の場合、正当性があること
*   UI/UX の場合は、別のプロセスがあります

<!--
## Seeking feedback
-->

## フィードバックを求める

<!--
*   Slack, bump, find committer, etc.
*   Knowing where to ask for help: https://make.wordpress.org/chat/
-->

*   Slack、bump、コミッターを探す、など。
*   どこに助けを求めればいいかを知る: https://make.wordpress.org/chat/

<!--
## Helpful tools/tips/code snippets/design patterns
-->

## 役立つツール・ヒント・コードやスニペット・デザインパターン

*   parse\_args

<!--
## Pro tips
-->

## プロのヒント

<!--
*   Good attributes of a core contributor
    *   Brevity (Patches, Comments, Personal Agendas)
    *   Thick Skin
    *   Don’t assume everyone is stupid
    *   Do your homework (study code and history)
    *   Constraints of pragmatism and back compat
    *   Constructive criticism
    *   Humility
-->

*   コア貢献者の良い特徴
    *   簡潔さ (パッチ、コメント、個人的なアジェンダ)
    *   打たれ強いこと
    *   みんなが愚かであると思わないこと
    *   下調べをする (コードと歴史を勉強する)
    *   実用性と後方互換の制約
    *   建設的な批判
    *   謙虚さ
