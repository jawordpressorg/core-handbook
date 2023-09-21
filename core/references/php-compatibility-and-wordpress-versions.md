<!--
# PHP Compatibility and WordPress Versions
-->

# PHP の互換性と WordPress のバージョン

<!--
WordPress aims to support new versions of PHP on the day they are released as much as possible. As a project, the process of supporting these new versions begins after each new PHP version has hit feature freeze and are tagging beta versions. This prevents having to revert or make additional changes to WordPress if a planned feature is removed or the implementation changes.
-->

WordPress は PHP の新しいバージョンがリリースされた当日に可能な限りサポートすることを目指しています。プロジェクトとして、これらの新しいバージョンをサポートするプロセスは、それぞれの新しい PHP バージョンが機能フリーズを迎え、ベータ版にタグ付けされたあとに開始されます。これにより、計画した機能が削除されたり実装が変更されたりしても、WordPress を元に戻したり追加の機能を加える必要がなくなります。

<!--
Past changes to supported PHP versions have been as followed:
-->

サポートされている PHP バージョンの過去の変更は以下のとおりです。

<!--
*   In WordPress version 4.1: Added support for PHP 5.6.
*   In WordPress 4.4: Added support for PHP 7.0 ([dev note](https://make.wordpress.org/core/2015/09/10/wordpress-and-php7/)).
*   In WordPress 4.7: Added support for PHP 7.1.
*   In WordPress 4.9: Added support for PHP 7.2.
*   In WordPress 5.0: Added support for PHP 7.3 ([dev note](https://make.wordpress.org/core/2018/10/15/wordpress-and-php-7-3/)).
*   In WordPress 5.2: [Dropped support](https://core.trac.wordpress.org/ticket/46594) for PHP 5.2, 5.3, 5.4, 5.5.
*   In WordPress 5.3: Added support for PHP 7.4 ([dev note](https://make.wordpress.org/core/2019/10/11/wordpress-and-php-7-4/)).
*   In WordPress 5.6: Added “beta support” for PHP 8.0 ([dev note](https://make.wordpress.org/core/2020/11/23/wordpress-and-php-8-0/)).
*   In WordPress 5.9: Added “beta support” for PHP 8.1 ([dev note](https://make.wordpress.org/core/2022/01/10/wordpress-5-9-and-php-8-0-8-1/)).
*   In WordPress 6.1: Added “beta support” for PHP 8.2 (dev note pending).
*   In WordPress 6.3:
    *   [Dropped support for PHP 5.6](https://make.wordpress.org/core/2023/07/05/dropping-support-for-php-5/).
    *   Raised PHP 8.0 to compatible with exceptions (dev note pending).
        *   Exceptions:
            *   Named parameters. WordPress does not support named parameters.
            *   [Filesystem `WP_Filesystem_FTPext` and `WP_Filesystem_SSH2` when connect fails](https://core.trac.wordpress.org/ticket/48689).
    *   Raised PHP 8.1 to compatible with exceptions (dev note pending).
        *   Exceptions:
            *   [`htmlentities()` et al needs the default value of the flags parameter explicitly set](https://core.trac.wordpress.org/ticket/53465).
            *   [Replace most `strip_tags()` with `wp_strip_tags()`](https://core.trac.wordpress.org/ticket/57579)
            *   [`unregister_setting()` for unknown setting](https://core.trac.wordpress.org/ticket/57674).
-->

*   WordPress 4.1: PHP 5.6をサポート。
*   WordPress 4.4: PHP 7.0をサポート ([dev note](https://make.wordpress.org/core/2015/09/10/wordpress-and-php7/))。
*   WordPress 4.7: PHP 7.1をサポート。
*   WordPress 4.9: PHP 7.2をサポート。
*   WordPress 5.0: PHP 7.3をサポート ([dev note](https://make.wordpress.org/core/2018/10/15/wordpress-and-php-7-3/))。
*   WordPress 5.2: PHP 5.2、5.3、5.4、5.5を[サポート廃止](https://core.trac.wordpress.org/ticket/46594)。
*   WordPress 5.3: PHP 7.4をサポート ([dev note](https://make.wordpress.org/core/2019/10/11/wordpress-and-php-7-4/))。
*   WordPress 5.6: PHP 8.0を「ベータサポート」([dev note](https://make.wordpress.org/core/2020/11/23/wordpress-and-php-8-0/))。
*   WordPress 5.9: PHP 8.1を「ベータサポート」([dev note](https://make.wordpress.org/core/2022/01/10/wordpress-5-9-and-php-8-0-8-1/))。
*   WordPress 6.1: PHP 8.2を「ベータサポート」(dev note は保留中)。
*   WordPress 6.3:
    *   [PHP 5.6をサポート廃止](https://make.wordpress.org/core/2023/07/05/dropping-support-for-php-5/).
    *   例外を除き、PHP 8.0と互換性のあるレベルに引き上げました (dev note は保留中)。
        *   例外:
            *   名前付きパラメータ。WordPress は名前付きパラメータをサポートしていません。
            *   [接続に失敗したときのファイルシステムである `WP_Filesystem_FTPext` と `WP_Filesystem_SSH2`](https://core.trac.wordpress.org/ticket/48689)。
    *   例外を除き、PHP 8.1と互換性のあるレベルに引き上げました (dev note は保留中)。
        *   例外:
            *   [`htmlentities()` などは flags パラメータのデフォルト値を明示的に設定する必要があります](https://core.trac.wordpress.org/ticket/53465)。
            *   [ほとんどの `strip_tags()` を `wp_strip_tags()` に置き換える](https://core.trac.wordpress.org/ticket/57579)
            *   [不明な設定のための `unregister_setting()`](https://core.trac.wordpress.org/ticket/57674)。

<!--
## Supported Version Chart
-->

## 対応バージョン一覧

<!--
| WP Version | [5.2](https://www.php.net/archive/2006.php) | [5.3](https://www.php.net/archive/2009.php#id2009-06-30-1) | [5.4](https://www.php.net/archive/2012.php#id2012-03-01-1) | [5.5](https://www.php.net/archive/2013.php#id2013-06-20-1) | [5.6](https://www.php.net/archive/2014.php#id2014-08-28-1) | [7.0](https://www.php.net/archive/2015.php#id2015-12-03-1) | [7.1](https://www.php.net/archive/2016.php#id2016-12-01-3) | [7.2](https://www.php.net/archive/2017.php#id2017-11-30-1) | [7.3](https://www.php.net/archive/2018.php#id2018-12-06-1) | [7.4](https://www.php.net/archive/2019.php#2019-11-28-1) | [8.0](https://www.php.net/archive/2020.php#2020-11-26-3) | [8.1](https://www.php.net/archive/2021.php#2021-11-25-1) | [8.2](https://www.php.net/archive/2022.php#2022-12-08-1) |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| [6.3](https://wordpress.org/news/2023/08/lionel/) | N | N | N | N | N | **Y** | **Y** | **Y** | **Y** | **Y** | **Y****e** | **Y****e** | **Y\*** |
| [6.2](https://wordpress.org/news/2023/03/dolphy/) | N | N | N | N | Y | Y | Y | Y | Y | Y | **Y\*** | **Y\*** | **Y\*** |
| [6.1](https://wordpress.org/news/2022/11/misha/) | N | N | N | N | **Y** | **Y** | **Y** | Y | **Y** | **Y** | **Y\*** | **Y\*** | **Y\*** |
| [6.0](https://wordpress.org/news/2022/05/arturo/) | N | N | N | N | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y\*** | **Y\*** | N |
| [5.9](https://wordpress.org/news/2022/01/josephine/) | N | N | N | N | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y**\* | **Y\*** | N |
| [5.8](https://wordpress.org/news/2021/07/tatum/) | N | N | N | N | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y\*** | N | N |
| [5.7](https://wordpress.org/news/2021/03/esperanza/) | N | N | N | N | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y**\* | N | N |
| [5.6](https://wordpress.org/news/2020/12/simone/) | N | N | N | N | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y\*** | N | N |
| [5.5](https://wordpress.org/news/2020/08/wordpress-5-5-eckstine/) | N | N | N | N | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | N | N | N |
| [5.4](https://wordpress.org/news/2020/03/adderley/) | N | N | N | N | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | N | N | N |
| [5.3](https://wordpress.org/news/2019/11/kirk/) | N | N | N | N | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | N | N | N |
| [5.2](https://wordpress.org/news/2019/05/jaco/) | N | N | N | N | **Y** | **Y** | **Y** | **Y** | **Y** | N | N | N | N |
| [5.1](https://wordpress.org/news/2019/02/betty/) | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | N | N | N | N |
| [5.0](https://wordpress.org/news/2018/12/bebo/) | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | N | N | N | N |
| [4.9](https://wordpress.org/news/2017/11/tipton/) | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | N | N | N | N | N |
| [4.8](https://wordpress.org/news/2017/06/evans/) | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | N | N | N | N | N | N |
| [4.7](https://wordpress.org/news/2016/12/vaughan/) | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | N | N | N | N | N | N |
| [4.6](https://wordpress.org/news/2016/08/pepper/) | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | N | N | N | N | N | N | N |
| [4.5](https://wordpress.org/news/2016/04/coleman/) | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | N | N | N | N | N | N | N |
| [4.4](https://wordpress.org/news/2015/12/clifford/) | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | N | N | N | N | N | N | N |
| [4.3](https://wordpress.org/news/2015/08/billie/) | **Y** | **Y** | **Y** | **Y** | **Y** | N | N | N | N | N | N | N | N |
| [4.2](https://wordpress.org/news/2015/04/powell/) | **Y** | **Y** | **Y** | **Y** | **Y** | N | N | N | N | N | N | N | N |
| [4.1](https://wordpress.org/news/2014/12/dinah/) | **Y** | **Y** | **Y** | **Y** | **Y** | N | N | N | N | N | N | N | N |
| [4.0](https://wordpress.org/news/2014/09/benny/) | **Y** | **Y** | **Y** | **Y** | N | N | N | N | N | N | N | N | N |
| [3.9](https://wordpress.org/news/2014/04/smith/) | **Y** | **Y** | **Y** | **Y** | N | N | N | N | N | N | N | N | N |
| [3.8](https://wordpress.org/news/2013/12/parker/) | **Y** | **Y** | **Y** | **Y** | N | N | N | N | N | N | N | N | N |
| [3.7](https://wordpress.org/news/2013/10/basie/) | **Y** | **Y** | **Y** | **Y** | N | N | N | N | N | N | N | N | N |
-->

| WP バージョン | [5.2](https://www.php.net/archive/2006.php) | [5.3](https://www.php.net/archive/2009.php#id2009-06-30-1) | [5.4](https://www.php.net/archive/2012.php#id2012-03-01-1) | [5.5](https://www.php.net/archive/2013.php#id2013-06-20-1) | [5.6](https://www.php.net/archive/2014.php#id2014-08-28-1) | [7.0](https://www.php.net/archive/2015.php#id2015-12-03-1) | [7.1](https://www.php.net/archive/2016.php#id2016-12-01-3) | [7.2](https://www.php.net/archive/2017.php#id2017-11-30-1) | [7.3](https://www.php.net/archive/2018.php#id2018-12-06-1) | [7.4](https://www.php.net/archive/2019.php#2019-11-28-1) | [8.0](https://www.php.net/archive/2020.php#2020-11-26-3) | [8.1](https://www.php.net/archive/2021.php#2021-11-25-1) | [8.2](https://www.php.net/archive/2022.php#2022-12-08-1) |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| [6.3](https://wordpress.org/news/2023/08/lionel/) | N | N | N | N | N | **Y** | **Y** | **Y** | **Y** | **Y** | **Y****e** | **Y****e** | **Y\*** |
| [6.2](https://wordpress.org/news/2023/03/dolphy/) | N | N | N | N | Y | Y | Y | Y | Y | Y | **Y\*** | **Y\*** | **Y\*** |
| [6.1](https://wordpress.org/news/2022/11/misha/) | N | N | N | N | **Y** | **Y** | **Y** | Y | **Y** | **Y** | **Y\*** | **Y\*** | **Y\*** |
| [6.0](https://wordpress.org/news/2022/05/arturo/) | N | N | N | N | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y\*** | **Y\*** | N |
| [5.9](https://wordpress.org/news/2022/01/josephine/) | N | N | N | N | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y**\* | **Y\*** | N |
| [5.8](https://wordpress.org/news/2021/07/tatum/) | N | N | N | N | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y\*** | N | N |
| [5.7](https://wordpress.org/news/2021/03/esperanza/) | N | N | N | N | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y**\* | N | N |
| [5.6](https://wordpress.org/news/2020/12/simone/) | N | N | N | N | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y\*** | N | N |
| [5.5](https://wordpress.org/news/2020/08/wordpress-5-5-eckstine/) | N | N | N | N | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | N | N | N |
| [5.4](https://wordpress.org/news/2020/03/adderley/) | N | N | N | N | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | N | N | N |
| [5.3](https://wordpress.org/news/2019/11/kirk/) | N | N | N | N | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | N | N | N |
| [5.2](https://wordpress.org/news/2019/05/jaco/) | N | N | N | N | **Y** | **Y** | **Y** | **Y** | **Y** | N | N | N | N |
| [5.1](https://wordpress.org/news/2019/02/betty/) | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | N | N | N | N |
| [5.0](https://wordpress.org/news/2018/12/bebo/) | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | N | N | N | N |
| [4.9](https://wordpress.org/news/2017/11/tipton/) | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | N | N | N | N | N |
| [4.8](https://wordpress.org/news/2017/06/evans/) | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | N | N | N | N | N | N |
| [4.7](https://wordpress.org/news/2016/12/vaughan/) | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | N | N | N | N | N | N |
| [4.6](https://wordpress.org/news/2016/08/pepper/) | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | N | N | N | N | N | N | N |
| [4.5](https://wordpress.org/news/2016/04/coleman/) | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | N | N | N | N | N | N | N |
| [4.4](https://wordpress.org/news/2015/12/clifford/) | **Y** | **Y** | **Y** | **Y** | **Y** | **Y** | N | N | N | N | N | N | N |
| [4.3](https://wordpress.org/news/2015/08/billie/) | **Y** | **Y** | **Y** | **Y** | **Y** | N | N | N | N | N | N | N | N |
| [4.2](https://wordpress.org/news/2015/04/powell/) | **Y** | **Y** | **Y** | **Y** | **Y** | N | N | N | N | N | N | N | N |
| [4.1](https://wordpress.org/news/2014/12/dinah/) | **Y** | **Y** | **Y** | **Y** | **Y** | N | N | N | N | N | N | N | N |
| [4.0](https://wordpress.org/news/2014/09/benny/) | **Y** | **Y** | **Y** | **Y** | N | N | N | N | N | N | N | N | N |
| [3.9](https://wordpress.org/news/2014/04/smith/) | **Y** | **Y** | **Y** | **Y** | N | N | N | N | N | N | N | N | N |
| [3.8](https://wordpress.org/news/2013/12/parker/) | **Y** | **Y** | **Y** | **Y** | N | N | N | N | N | N | N | N | N |
| [3.7](https://wordpress.org/news/2013/10/basie/) | **Y** | **Y** | **Y** | **Y** | N | N | N | N | N | N | N | N | N |

<!--
**\* indicates “beta support”**
**e indicates “compatible with exceptions”**
-->

**\* 「ベータサポート」を示します**
**e 「例外ありの互換」を示します**
