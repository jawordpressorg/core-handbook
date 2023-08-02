# PHPUnit Compatibility and WordPress Versions

Changes to supported [PHPUnit](https://phpunit.de/index.html) versions have been as followed:

*   In WordPress 4.4: Added support for PHPUnit 5 was added on PHP 7.0.
*   In WordPress 4.7: Added support for PHPUnit 6 on PHP 7.0 and 7.1.
*   In WordPress 5.1: Added support for PHPUnit 7 on PHP 7.1, 7.2, and 7.3. PHP 7.0 remains at PHPUnit 6.
*   In WordPress 5.2: Added support for PHPUnit 7 on PHP 7.0, and PHPUnit 5 on PHP 5.6.
*   In WordPress 5.9: Added a dependency on the external [PHPUnit Polyfills](https://github.com/Yoast/PHPUnit-Polyfills/), which enabled support for PHPUnit 8 and 9, making it so the tests can now run on the most appropriate PHPUnit version for each PHP version.

## Supported Version Chart

| WP | PHP Unit Version | [5.2](https://www.php.net/archive/2006.php) | [5.3](https://www.php.net/archive/2009.php#id2009-06-30-1) | [5.4](https://www.php.net/archive/2012.php#id2012-03-01-1) | [5.5](https://www.php.net/archive/2013.php#id2013-06-20-1) | [5.6](https://www.php.net/archive/2014.php#id2014-08-28-1) | [7.0](https://www.php.net/archive/2015.php#id2015-12-03-1) | [7.1](https://www.php.net/archive/2016.php#id2016-12-01-3) | [7.2](https://www.php.net/archive/2017.php#id2017-11-30-1) | [7.3](https://www.php.net/archive/2018.php#id2018-12-06-1) | [7.4](https://www.php.net/archive/2019.php#2019-11-28-1) | [8.0](https://www.php.net/archive/2020.php#2020-11-26-3) | [8.1](https://www.php.net/archive/2021.php#2021-11-25-1) | 8.2 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| [6.1](https://wordpress.org/news/2022/11/misha/) | x | x | x | x | 5 | 6 | 7 | 8 | 9 | 9 | 9 | 9 | 9 |
| [6.0](https://wordpress.org/news/2022/05/arturo/) | x | x | x | x | 5 | 6 | 7 | 8 | 9 | 9 | 9 | 9 | x |
| [5.9](https://wordpress.org/news/2022/01/josephine/) | x | x | x | x | 5 | 6 | 7 | 8 | 9 | 9 | 9 | 9 | x |
| [5.8](https://wordpress.org/news/2021/07/tatum/) | x | x | x | x | 5 | 5 | 7 | 7 | 7 | 7 | 7\* | x | x |
| [5.7](https://wordpress.org/news/2021/03/esperanza/) | x | x | x | x | 5 | 5 | 7 | 7 | 7 | 7 | 7\* | x | x |
| [5.6](https://wordpress.org/news/2020/12/simone/) | x | x | x | x | 5 | 5 | 7 | 7 | 7 | 7 | 7\* | x | x |
| [5.5](https://wordpress.org/news/2020/08/wordpress-5-5-eckstine/) | x | x | x | x | 5 | 5 | 7 | 7 | 7 | 7 | x | x | x |
| [5.4](https://wordpress.org/news/2020/03/adderley/) | x | x | x | x | 5 | 5 | 7 | 7 | 7 | 7 | x | x | x |
| [5.3](https://wordpress.org/news/2019/11/kirk/) | x | x | x | x | 5 | 5 | 7 | 7 | 7 | 7 | x | x | x |
| [5.2](https://wordpress.org/news/2019/05/jaco/) | x | x | x | x | 5 | 5 | 7 | 7 | 7 | x | x | x | x |
| [5.1](https://wordpress.org/news/2019/02/betty/) | 3.6 | 4 | 4 | 4 | 4 | 6 | 7 | 7 | 7 | x | x | x | x |
| [5.0](https://wordpress.org/news/2018/12/bebo/) | 3.6 | 4 | 4 | 4 | 4 | 6 | 6 | 6 | 6 | x | x | x | x |
| [4.9](https://wordpress.org/news/2017/11/tipton/) | 3.6 | 4 | 4 | 4 | 4 | 6 | 6 | 6 | x | x | x | x | x |
| [4.8](https://wordpress.org/news/2017/06/evans/) | 3.6 | 4 | 4 | 4 | 4 | 6 | 6 | x | x | x | x | x | x |
| [4.7](https://wordpress.org/news/2016/12/vaughan/) | 3.6 | 4 | 4 | 4 | 4 | 6 | 6 | x | x | x | x | x | x |
| [4.6](https://wordpress.org/news/2016/08/pepper/) | 3.6 | 4 | 4 | 4 | 4 | 5 | x | x | x | x | x | x | x |
| [4.5](https://wordpress.org/news/2016/04/coleman/) | 3.6 | 4 | 4 | 4 | 4 | 5 | x | x | x | x | x | x | x |
| [4.4](https://wordpress.org/news/2015/12/clifford/) | 3.6 | 4 | 4 | 4 | 4 | 5 | x | x | x | x | x | x | x |
| [4.3](https://wordpress.org/news/2015/08/billie/) | 3.6 | 4 | 4 | 4 | 4 | x | x | x | x | x | x | x | x |
| [4.2](https://wordpress.org/news/2015/04/powell/) | 3.6 | 4 | 4 | 4 | 4 | x | x | x | x | x | x | x | x |
| [4.1](https://wordpress.org/news/2014/12/dinah/) | 3.6 | 4 | 4 | 4 | 4 | x | x | x | x | x | x | x | x |
| [4.0](https://wordpress.org/news/2014/09/benny/) | 3.6 | 4 | 4 | 4 | x | x | x | x | x | x | x | x | x |
| [3.9](https://wordpress.org/news/2014/04/smith/) | 3.6 | 4 | 4 | 4 | x | x | x | x | x | x | x | x | x |
| [3.8](https://wordpress.org/news/2013/12/parker/) | 3.6 | 4 | 4 | 4 | x | x | x | x | x | x | x | x | x |
| [3.7](https://wordpress.org/news/2013/10/basie/) | 3.6 | 4 | 4 | 4 | x | x | x | x | x | x | x | x | x |

**\*** The core test suite in these branches runs a modified version of PHPUnit 7 (which on its own is not compatible) on PHP 8. See [#50902](https://core.trac.wordpress.org/ticket/50902) for more information.