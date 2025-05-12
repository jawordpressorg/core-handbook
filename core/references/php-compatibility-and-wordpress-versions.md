<!--
# PHP Compatibility and WordPress Versions
-->

# PHP の互換性と WordPress のバージョン

<!--
WordPress aims to support new versions of PHP on the day they are released as much as possible. As a project, the process of supporting these new versions begins after each new PHP version has hit feature freeze and are tagging beta versions. This prevents having to revert or make additional changes to WordPress if a planned feature is removed or the implementation changes.
-->

WordPress は PHP の新しいバージョンがリリースされた当日に可能な限りサポートすることを目指しています。プロジェクトとして、これらの新しいバージョンをサポートするプロセスは、それぞれの新しい PHP バージョンが機能フリーズを迎え、ベータ版にタグ付けされたあとに開始されます。これにより、計画した機能が削除されたり実装が変更されたりしても、WordPress を元に戻したり追加の機能を加える必要がなくなります。

<!--
## Supported PHP Versions
-->

## サポートされている PHP バージョン

<!--
| WP / PHP Version | [8.4](https://www.php.net/archive/2024.php#2024-11-21-4) | [8.3](https://www.php.net/archive/2023.php#2023-11-23-2) | [8.2](https://www.php.net/archive/2022.php#2022-12-08-1) | [8.1](https://www.php.net/archive/2021.php#2021-11-25-1) | [8.0](https://www.php.net/archive/2020.php#2020-11-26-3) | [7.4](https://www.php.net/archive/2019.php#2019-11-28-1) | [7.3](https://www.php.net/archive/2018.php#id2018-12-06-1) | [7.2](https://www.php.net/archive/2017.php#id2017-11-30-1) | [7.1](https://www.php.net/archive/2016.php#id2016-12-01-3) | [7.0](https://www.php.net/archive/2015.php#id2015-12-03-1) | 5.6 and older |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| [6.8](https://wordpress.org/news/2025/04/cecil/) | **Y**\* | **Y**\* | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | N | N | N |
| [6.7](https://wordpress.org/news/2024/11/rollins/) | **Y\*** | **Y**\* | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | N | N | N |
| [6.6](https://wordpress.org/news/2024/07/dorsey/) | N | **Y****\*** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | N | N | N |
| [6.5](https://wordpress.org/news/2024/04/wordpress-6-5-regina/) | N | **Y\*** | **Y\*** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | N |
| [6.4](https://wordpress.org/news/2023/11/shirley/) | N | **Y\*** | **Y\*** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | N |
| [6.3](https://wordpress.org/news/2023/08/lionel/) | N | N | **Y\*** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | N |
-->

| WP / PHP バージョン | [8.4](https://www.php.net/archive/2024.php#2024-11-21-4) | [8.3](https://www.php.net/archive/2023.php#2023-11-23-2) | [8.2](https://www.php.net/archive/2022.php#2022-12-08-1) | [8.1](https://www.php.net/archive/2021.php#2021-11-25-1) | [8.0](https://www.php.net/archive/2020.php#2020-11-26-3) | [7.4](https://www.php.net/archive/2019.php#2019-11-28-1) | [7.3](https://www.php.net/archive/2018.php#id2018-12-06-1) | [7.2](https://www.php.net/archive/2017.php#id2017-11-30-1) | [7.1](https://www.php.net/archive/2016.php#id2016-12-01-3) | [7.0](https://www.php.net/archive/2015.php#id2015-12-03-1) | 5.6 and older |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| [6.8](https://wordpress.org/news/2025/04/cecil/) | **Y**\* | **Y**\* | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | N | N | N |
| [6.7](https://wordpress.org/news/2024/11/rollins/) | **Y\*** | **Y**\* | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | N | N | N |
| [6.6](https://wordpress.org/news/2024/07/dorsey/) | N | **Y****\*** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | N | N | N |
| [6.5](https://wordpress.org/news/2024/04/wordpress-6-5-regina/) | N | **Y\*** | **Y\*** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | N |
| [6.4](https://wordpress.org/news/2023/11/shirley/) | N | **Y\*** | **Y\*** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | N |
| [6.3](https://wordpress.org/news/2023/08/lionel/) | N | N | **Y\*** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | N |

<!--
**\* indicates beta support**
-->

**\* 「ベータサポート」を示します**

<!--
Past changes to supported PHP versions have been as follows:
-->

サポートされている PHP バージョンの過去の変更は以下のとおりです。

<!--
*   In April 2025: use of the “compatible with exceptions” labeling was dropped.
*   In WordPress 6.7: Added beta support for PHP 8.4.
*   In WordPress 6.6:
    *   Raised PHP 8.2 to compatible with exceptions.
    *   [Dropped support for PHP 7.0 & 7.1](https://make.wordpress.org/core/2024/04/08/dropping-support-for-php-7-1/).
*   In WordPress 6.4: [Added beta support for PHP 8.3](https://wordpress.org/news/2023/10/wordpress-6-4s-php-compatibility/).
*   In WordPress 6.3:
    *   [Dropped support for PHP 5.6](https://make.wordpress.org/core/2023/07/05/dropping-support-for-php-5/).
    *   Raised PHP 8.1 to compatible with exceptions:
        *   [`htmlentities()` et al needs the default value of the flags parameter explicitly set](https://core.trac.wordpress.org/ticket/53465).
        *   [Replace most `strip_tags()` with `wp_strip_tags()`](https://core.trac.wordpress.org/ticket/57579)
        *   [`unregister_setting()` for unknown setting](https://core.trac.wordpress.org/ticket/57674).
    *   Raised PHP 8.0 to compatible with exceptions:
        *   WordPress does not support use of named parameters because parameter names are subject to change.
        *   [Filesystem `WP_Filesystem_FTPext` and `WP_Filesystem_SSH2` when connect fails](https://core.trac.wordpress.org/ticket/48689).
-->

*   2025年4月: 「例外ありで互換性あり」というラベルの使用は廃止されました。
*   WordPress 6.7: PHP 8.4をベータサポート。
*   WordPress 6.6:
    *   例外つきで PHP 8.2と互換性のあるレベルに引き上げました。
    *   [PHP 7.0と7.1のサポートを廃止](https://make.wordpress.org/core/2024/04/08/dropping-support-for-php-7-1/)。
*   WordPress 6.4: [PHP 8.3をベータサポート](https://wordpress.org/news/2023/10/wordpress-6-4s-php-compatibility/)。
*   WordPress 6.3:
    *   [PHP 5.6のサポートを廃止](https://make.wordpress.org/core/2023/07/05/dropping-support-for-php-5/).
    *   以下の例外を除き、PHP 8.1と互換性のあるレベルに引き上げました。
        *   [`htmlentities()` などは flags パラメータのデフォルト値を明示的に設定する必要があります](https://core.trac.wordpress.org/ticket/53465)。
        *   [ほとんどの `strip_tags()` を `wp_strip_tags()` に置き換える](https://core.trac.wordpress.org/ticket/57579)
        *   [不明な設定のための `unregister_setting()`](https://core.trac.wordpress.org/ticket/57674)。
    *   以下の例外を除き、PHP 8.0と互換性のあるレベルに引き上げました。
        *   パラメータ名は変更される可能性があるため、WordPress では名前付きパラメータの使用をサポートしていません。
        *   [接続に失敗したときのファイルシステムである `WP_Filesystem_FTPext` と `WP_Filesystem_SSH2`](https://core.trac.wordpress.org/ticket/48689)。

<!--
### Older WordPress Versions
-->

### 古いバージョンの WordPress

<!--
*   In WordPress 6.1: Added beta support for PHP 8.2.
*   In WordPress 5.9: [Added beta support for PHP 8.1](https://make.wordpress.org/core/2022/01/10/wordpress-5-9-and-php-8-0-8-1/).
*   In WordPress 5.6: [Added beta support for PHP 8.0](https://make.wordpress.org/core/2020/11/23/wordpress-and-php-8-0/).
*   In December 2022, [security support for WordPress 3.7-4.0 was dropped](https://make.wordpress.org/security/2022/09/07/dropping-security-updates-for-wordpress-versions-3-7-through-4-0/#comment-25).
*   In WordPress 5.2: [Dropped support for PHP 5.2 to 5.5](https://core.trac.wordpress.org/ticket/46594).
*   In WordPress 5.3: [Added support for PHP 7.4](https://make.wordpress.org/core/2019/10/11/wordpress-and-php-7-4/).
-->

*   WordPress 6.1: PHP 8.2をベータサポート。
*   WordPress 5.9: [PHP 8.1をベータサポート](https://make.wordpress.org/core/2022/01/10/wordpress-5-9-and-php-8-0-8-1/)。
*   WordPress 5.6: [PHP 8.0をベータサポート](https://make.wordpress.org/core/2020/11/23/wordpress-and-php-8-0/).
*   2022年12月: [WordPress 3.7から4.0までのセキュリティサポートを廃止](https://make.wordpress.org/security/2022/09/07/dropping-security-updates-for-wordpress-versions-3-7-through-4-0/#comment-25).
*   In WordPress 5.2: [PHP 5.2から5.5までのサポートを廃止](https://core.trac.wordpress.org/ticket/46594).
*   In WordPress 5.3: [PHP 7.4をサポート](https://make.wordpress.org/core/2019/10/11/wordpress-and-php-7-4/).

<!--
| WP / PHP Version | [8.3](https://www.php.net/archive/2023.php#2023-11-23-2) and newer | [8.2](https://www.php.net/archive/2022.php#2022-12-08-1) | [8.1](https://www.php.net/archive/2021.php#2021-11-25-1) | [8.0](https://www.php.net/archive/2020.php#2020-11-26-3) | [7.4](https://www.php.net/archive/2019.php#2019-11-28-1) | [7.3](https://www.php.net/archive/2018.php#id2018-12-06-1) | [7.2](https://www.php.net/archive/2017.php#id2017-11-30-1) | [7.1](https://www.php.net/archive/2016.php#id2016-12-01-3) | [7.0](https://www.php.net/archive/2015.php#id2015-12-03-1) | [5.6](https://www.php.net/archive/2014.php#id2014-08-28-1) | [5.5](https://www.php.net/archive/2013.php#id2013-06-20-1) and older |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| [6.2](https://wordpress.org/news/2023/03/dolphy/) | N | **Y\*** | **Y\*** | **Y\*** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | N |
| [6.1](https://wordpress.org/news/2022/11/misha/) | N | **Y\*** | **Y\*** | **Y\*** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | N |
| [6.0](https://wordpress.org/news/2022/05/arturo/) | N | N | **Y\*** | **Y\*** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | N |
| [5.9](https://wordpress.org/news/2022/01/josephine/) | N | N | **Y\*** | **Y**\* | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | N |
| [5.8](https://wordpress.org/news/2021/07/tatum/) | N | N | N | **Y\*** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | N |
| [5.7](https://wordpress.org/news/2021/03/esperanza/) | N | N | N | **Y**\* | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | N |
| [5.6](https://wordpress.org/news/2020/12/simone/) | N | N | N | **Y\*** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | N |
-->

| WP / PHP バージョン | [8.3](https://www.php.net/archive/2023.php#2023-11-23-2) and newer | [8.2](https://www.php.net/archive/2022.php#2022-12-08-1) | [8.1](https://www.php.net/archive/2021.php#2021-11-25-1) | [8.0](https://www.php.net/archive/2020.php#2020-11-26-3) | [7.4](https://www.php.net/archive/2019.php#2019-11-28-1) | [7.3](https://www.php.net/archive/2018.php#id2018-12-06-1) | [7.2](https://www.php.net/archive/2017.php#id2017-11-30-1) | [7.1](https://www.php.net/archive/2016.php#id2016-12-01-3) | [7.0](https://www.php.net/archive/2015.php#id2015-12-03-1) | [5.6](https://www.php.net/archive/2014.php#id2014-08-28-1) | [5.5](https://www.php.net/archive/2013.php#id2013-06-20-1) and older |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| [6.2](https://wordpress.org/news/2023/03/dolphy/) | N | **Y\*** | **Y\*** | **Y\*** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | N |
| [6.1](https://wordpress.org/news/2022/11/misha/) | N | **Y\*** | **Y\*** | **Y\*** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | N |
| [6.0](https://wordpress.org/news/2022/05/arturo/) | N | N | **Y\*** | **Y\*** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | N |
| [5.9](https://wordpress.org/news/2022/01/josephine/) | N | N | **Y\*** | **Y**\* | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | N |
| [5.8](https://wordpress.org/news/2021/07/tatum/) | N | N | N | **Y\*** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | N |
| [5.7](https://wordpress.org/news/2021/03/esperanza/) | N | N | N | **Y**\* | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | N |
| [5.6](https://wordpress.org/news/2020/12/simone/) | N | N | N | **Y\*** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | N |

<!--
**\* indicates beta support**
-->

**\* 「ベータサポート」を示します**

<!--
| WP / PHP Version | [8.0](https://www.php.net/archive/2020.php#2020-11-26-3) and newer | [7.4](https://www.php.net/archive/2019.php#2019-11-28-1) | [7.3](https://www.php.net/archive/2018.php#id2018-12-06-1) | [7.2](https://www.php.net/archive/2017.php#id2017-11-30-1) | [7.1](https://www.php.net/archive/2016.php#id2016-12-01-3) | [7.0](https://www.php.net/archive/2015.php#id2015-12-03-1) | [5.6](https://www.php.net/archive/2014.php#id2014-08-28-1) | [5.5](https://www.php.net/archive/2013.php#id2013-06-20-1) | [5.4](https://www.php.net/archive/2012.php#id2012-03-01-1) | [5.3](https://www.php.net/archive/2009.php#id2009-06-30-1) | [5.2](https://www.php.net/archive/2006.php) |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| [5.5](https://wordpress.org/news/2020/08/wordpress-5-5-eckstine/) | N | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | N | N | N | N |
| [5.4](https://wordpress.org/news/2020/03/adderley/) | N | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | N | N | N | N |
| [5.3](https://wordpress.org/news/2019/11/kirk/) | N | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | N | N | N | N |
| [5.2](https://wordpress.org/news/2019/05/jaco/) | N | N | **Y** | **Y** | **Y** | **Y** | **Y** | N | N | N | N |
| [5.1](https://wordpress.org/news/2019/02/betty/) | N | N | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** |
| [5.0](https://wordpress.org/news/2018/12/bebo/) | N | N | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** |
| [4.9](https://wordpress.org/news/2017/11/tipton/) | N | N | N | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** |
| [4.8](https://wordpress.org/news/2017/06/evans/) | N | N | N | N | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** |
| [4.7](https://wordpress.org/news/2016/12/vaughan/) | N | N | N | N | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** |
-->

| WP / PHP バージョン | [8.0](https://www.php.net/archive/2020.php#2020-11-26-3) and newer | [7.4](https://www.php.net/archive/2019.php#2019-11-28-1) | [7.3](https://www.php.net/archive/2018.php#id2018-12-06-1) | [7.2](https://www.php.net/archive/2017.php#id2017-11-30-1) | [7.1](https://www.php.net/archive/2016.php#id2016-12-01-3) | [7.0](https://www.php.net/archive/2015.php#id2015-12-03-1) | [5.6](https://www.php.net/archive/2014.php#id2014-08-28-1) | [5.5](https://www.php.net/archive/2013.php#id2013-06-20-1) | [5.4](https://www.php.net/archive/2012.php#id2012-03-01-1) | [5.3](https://www.php.net/archive/2009.php#id2009-06-30-1) | [5.2](https://www.php.net/archive/2006.php) |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| [5.5](https://wordpress.org/news/2020/08/wordpress-5-5-eckstine/) | N | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | N | N | N | N |
| [5.4](https://wordpress.org/news/2020/03/adderley/) | N | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | N | N | N | N |
| [5.3](https://wordpress.org/news/2019/11/kirk/) | N | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | N | N | N | N |
| [5.2](https://wordpress.org/news/2019/05/jaco/) | N | N | **Y** | **Y** | **Y** | **Y** | **Y** | N | N | N | N |
| [5.1](https://wordpress.org/news/2019/02/betty/) | N | N | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** |
| [5.0](https://wordpress.org/news/2018/12/bebo/) | N | N | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** |
| [4.9](https://wordpress.org/news/2017/11/tipton/) | N | N | N | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** |
| [4.8](https://wordpress.org/news/2017/06/evans/) | N | N | N | N | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** |
| [4.7](https://wordpress.org/news/2016/12/vaughan/) | N | N | N | N | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** |
