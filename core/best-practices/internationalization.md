<!--
# Internationalization
-->

# 国際化 (i18n)

<!--
This page is still a draft and being actively written.
-->

\[alert\]このページはまだ下書きで、執筆中です。\[/alert\]

<!--
## What is Internationalization?
-->

## 国際化とは

<!--
Internationalization is the process of developing the codebase so that it can easily be translated into other languages. Internationalization is often abbreviated as `i18n` (because there are 18 letters between the i and the n).
-->

国際化とは、コードベースを他の言語に容易に翻訳できるように開発することです。国際化はしばしば `i18n` と略されます (i と n の間に18文字があるため)。

<!--
**Topics for this handbook page:**
-->

**このハンドブックページ用のトピック:**

<!--
*   Singular/plural forms; explain, that singular isn’t always used for 1 item
*   Translator comments for placeholders, requirement
*   Explain difference between context and translator comments
*   Escaping
*   Avoid HTML in strings if possible
*   Use HTML entities for dashes (`&mdash;`) and apostrophes (`&­#8217;`)
-->

* 単数形/複数形: 1つの項目に対して単数形が常に使われるわけではないことを説明する
* プレースホルダーに対する翻訳者コメント、要件
* コンテキストと翻訳者コメントの違いの説明
* エスケープ方法
* 可能な場合は、文字列内に HTML 含めるのを避ける
* ダッシュ記号 (`&mdash;`) とアポストロフィ記号 (`&#8217;`) には HTML エンティティを使用する。

<!--
### Localization
-->

### ローカリゼーション (l10)

<!--
#### Avoid fragmented or ‘patchwork’ messages
-->

#### フラグメント (断片的) または「パッチワーク」のメッセージを避ける

<!--
Languages have varying word orders, and complex grammatical and syntactic rules. “Lego” messages, put together from lots of pieces of text, possibly with some indirection, are very hard or impossible to translate.
-->

言語にはさまざまな語順があり、文法的または構文的な規則も複雑です。多くのテキストを組み合わせ、場合によっては間接的な表現も加えた「レゴ」のようなメッセージは、翻訳が非常に難しかったり、不可能だったりします。

<!--
It is better to make every message a complete sentence, each with a full stop at the end. Several sentences can usually be combined much more easily be into a text block, if needed.
-->

すべてのメッセージは完全な文章にし、各文章の最後に句点をつけましょう。もし必要であれば、たいていは複数の文章を1つのテキストのまとまりにできます。

<!--
#### Use full stops
-->

#### 句点を使う

<!--
Do terminate normal sentences with full stops. This is often the only indicator for a translator to know that they are not headlines or list items, which may need to be translated differently.
-->

通常の文章は句点で終わらせてください。こうすることで、翻訳者にとって、それが見出しやリスト項目でないことを知る唯一の指針となります。文章ではない場合は、別の方法で翻訳する必要がある場合もあります。

<!--
### Resources
-->

### リソース

*   [https://www.mediawiki.org/wiki/Localisation](https://www.mediawiki.org/wiki/Localisation)
*   [https://developer.wordpress.org/plugins/internationalization/](https://developer.wordpress.org/plugins/internationalization/)
