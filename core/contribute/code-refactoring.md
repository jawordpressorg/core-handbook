<!--
# Code Refactoring
-->

# コードリファクタリング

<!--
Code refactoring should not be done just because we can. There are a number of “refactoring” tickets that have been opened over time, such as suggestions to rename long-standing functions or conform to more-recently established coding standards. Meanwhile, plenty of tasks are far more worthy of effort. Here are some suggested guidelines on what these tickets need in order to warrant review:
-->

コードのリファクタリングは、できることだからという理由で行うべきではありません。長い間使用されてきた関数の名前を変更する提案や、より最近に確立されたコーディング標準に準拠する提案など、時間の経過によって開かれた「リファクタリング」チケットは数多くあります。一方で、もっと価値のあるタスクがたくさんあります。ここでは、これらのチケットがレビューの対象となるために必要なガイドラインをいくつか提案します。

<!--
*   **Unit tests**, even if the code was not previously covered. We can’t afford regressions, and this will improve our test coverage.
*   **Performance benchmarks**, before and after. We can’t afford regressions.
*   **Proper justification and clear rationale** of changes are both necessary. Too often it is impossible to determine the purpose, objective, or focus of these patches. Code should not be rewritten under the cloaks of readability, narrow personal opinion, or general subjectiveness.
-->

*   **ユニットテスト**。たとえ、そのコードが以前はカバーされていなかったとしてもです。リグレッションは避けるべきであり、これによりテストのカバー率を向上させることができます。
*   適用前と適用後の**パフォーマンスベンチマーク**。リグレッションは避けるべきです。
*   変更についての**適切な正当性と明確な根拠**の両方が必要です。多くの場合、これらのパッチの目的、目標、またはフォーカスを決定できません。可読性、個人的な狭い意見、一般的な主観などを口実として、コードを書き換えるべきではありません。

<!--
When none of this is followed, the end result is that reviewers and committers are distracted, which drains important attention and focus that should be spent elsewhere.
-->

これらが守られないと、レビュアーやコミッターの気が散ってしまい、費やすべき重要な注意力や集中力が削がれてしまいます。

<!--
In addition, code refactoring can cause existing, more important patches to unnecessarily become stale.
-->

またコードのリファクタリングによって、より重要な既存のパッチが不必要に古くなる可能性もあります。

<!--
There’s a document on contributing to the Linux kernel with [a section on pitfalls](https://dri.freedesktop.org/docs/drm/development-process/4.Coding.html#coding-style) when handling coding standards. I believe this can apply to the wider picture of refactoring as well (emphasis added):
-->

Linux カーネルへの貢献に関する文書に、コーディング標準を扱う際の[落とし穴に関するセクション](https://dri.freedesktop.org/docs/drm/development-process/4.Coding.html#coding-style)があります。これは、リファクタリングという広い視野にも適用されると思います (強調は引用者)。

<!--
> The kernel has long had a standard coding style, described in Documentation/CodingStyle. For much of that time, the policies described in that file were taken as being, at most, advisory. As a result, there is a substantial amount of code in the kernel which does not meet the coding style guidelines. The presence of that code leads to two independent hazards for kernel developers.
>
> **The first of these is to believe that the kernel coding standards do not matter and are not enforced. … The other trap is to assume that code which is already in the kernel is urgently in need of coding style fixes.**
-->

> カーネルは長い間、Documentation/CodingStyle に記述された標準的なコーディングスタイルを持っていました。その多くの期間、このファイルに記述されたポリシーは、せいぜい勧告的なものとして扱われてきました。このようなコードの存在は、カーネル開発者にとって2つの独立した危険性をもたらします。
>
> **これらのうち最初のものは、カーネルのコーディング規約は重要でなく、強制されるものではないと信じてしまうことです。もう一つの罠は、すでにカーネルにあるコードについて、早急にコーディングスタイルを修正する必要があると思い込んでしまうことです。**

<!--
That said, we want to be internally consistent and follow our own rules. Code is poetry, and our code should be beautiful.
-->

とはいえ、内部的には一貫性を保ち、自分たちのルールに従いたいものです。コードは詩であり、私たちのコードは美しくあるべきです。
