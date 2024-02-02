# Internationalization

This page is still a draft and being actively written.

## What is Internationalization?

Internationalization is the process of developing the codebase so that it can easily be translated into other languages. Internationalization is often abbreviated as `i18n` (because there are 18 letters between the i and the n).

**Topics for this handbook page:**

*   Singular/plural forms; explain, that singular isn’t always used for 1 item
*   Translator comments for placeholders, requirement
*   Explain difference between context and translator comments
*   Escaping
*   Avoid HTML in strings if possible
*   Use HTML entities for dashes (`&mdash;`) and apostrophes (`&­#8217;`)

### Localization

#### Avoid fragmented or ‘patchwork’ messages

Languages have varying word orders, and complex grammatical and syntactic rules. “Lego” messages, put together from lots of pieces of text, possibly with some indirection, are very hard or impossible to translate.

It is better to make every message a complete sentence, each with a full stop at the end. Several sentences can usually be combined much more easily be into a text block, if needed.

#### Use full stops

Do terminate normal sentences with full stops. This is often the only indicator for a translator to know that they are not headlines or list items, which may need to be translated differently.

### Resources

*   [https://www.mediawiki.org/wiki/Localisation](https://www.mediawiki.org/wiki/Localisation)
*   [https://developer.wordpress.org/plugins/internationalization/](https://developer.wordpress.org/plugins/internationalization/)