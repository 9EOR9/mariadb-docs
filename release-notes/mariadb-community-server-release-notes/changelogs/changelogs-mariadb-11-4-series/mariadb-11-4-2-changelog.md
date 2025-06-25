# MariaDB 11.4.2 Changelog

The most recent release of [MariaDB 11.4](../../mariadb-11-4-series/what-is-mariadb-114.md) is:[**MariaDB 11.4.5**](../../mariadb-11-4-series/mariadb-11-4-5-release-notes.md) Stable (GA) [Download Now](https://mariadb.com/downloads/)[_Alternate download from mariadb.org_](https://downloads.mariadb.org/mariadb/11.4.5/)

[Download 11.4.2](https://downloads.mariadb.org/mariadb/11.4.2)[Release Notes](../../mariadb-11-4-series/mariadb-11-4-2-release-notes.md)[Changelog](mariadb-11-4-2-changelog.md)[Overview of 11.4](../../mariadb-11-4-series/what-is-mariadb-114.md)

**Release date:** 29 May 2024

For the highlights of this release, see the[release notes](../../mariadb-11-4-series/mariadb-11-4-2-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/server/tree/11.4) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Includes all fixes from [MariaDB 11.3.2](../changelogs-mariadb-11-3-series/mariadb-11-3-2-changelog.md)
* Includes all fixes from [MariaDB 11.2.4](../changelogs-mariadb-11-2-series/mariadb-11-2-4-changelog.md)
* [Revision #3fca5ed772](https://github.com/MariaDB/server/commit/3fca5ed772)\
  2024-05-26 11:48:57 +0200
  * update C/C: fix memory leaks
* Merge [Revision #e9a5b25dfd](https://github.com/MariaDB/server/commit/e9a5b25dfd) 2024-05-24 09:39:24 +0200 - Merge branch '11.4' into 11.4.2
* [Revision #2dfc6c4410](https://github.com/MariaDB/server/commit/2dfc6c4410)\
  2024-05-23 11:18:19 +0400
  * [MDEV-33729](https://jira.mariadb.org/browse/MDEV-33729) UBSAN negation of -X cannot be represented in type 'long long int'; cast to an unsigned type to negate this value to itself in my\_strntoll\_mb2\_or\_mb4
* [Revision #727b549310](https://github.com/MariaDB/server/commit/727b549310)\
  2024-05-22 12:30:30 +0300
  * [MDEV-34212](https://jira.mariadb.org/browse/MDEV-34212) InnoDB transaction recovery is incorrect
* [Revision #6c0eb29ddd](https://github.com/MariaDB/server/commit/6c0eb29ddd)\
  2024-05-22 13:16:10 +0530
  * [MDEV-34200](https://jira.mariadb.org/browse/MDEV-34200) InnoDB tries to write to read-only system tablespace in buf\_dblwr\_t::init\_or\_load\_pages()
* Merge [Revision #d2c9d86ed9](https://github.com/MariaDB/server/commit/d2c9d86ed9) 2024-05-22 17:35:26 +0300 - Merge 11.2 into 11.4
* [Revision #b793feb1d6](https://github.com/MariaDB/server/commit/b793feb1d6)\
  2024-05-22 16:54:33 +0300
  * [MDEV-34216](https://jira.mariadb.org/browse/MDEV-34216) Possible corruption when shrinking the system tablespace on innodb\_fast\_shutdown=0
* [Revision #eede2221c0](https://github.com/MariaDB/server/commit/eede2221c0)\
  2024-05-22 10:59:52 +0200
  * new CC 3.4
* Merge [Revision #cb273d53d3](https://github.com/MariaDB/server/commit/cb273d53d3) 2024-05-22 09:19:25 +0300 - Merge 11.2 into 11.4
* [Revision #ff377d3bea](https://github.com/MariaDB/server/commit/ff377d3bea)\
  2024-05-22 08:33:43 +0300
  * [MDEV-34209](https://jira.mariadb.org/browse/MDEV-34209) InnoDB is disregarding read-only mode on slow shutdown
* [Revision #19f7edf420](https://github.com/MariaDB/server/commit/19f7edf420)\
  2024-03-15 18:42:06 +0100
  * mysqltest: support MARIADB\_OPT\_RESTRICTED\_AUTH
* [Revision #1588e61566](https://github.com/MariaDB/server/commit/1588e61566)\
  2024-03-15 14:48:06 +0100
  * small cleanup: mysqltest
* [Revision #84f99acbe8](https://github.com/MariaDB/server/commit/84f99acbe8)\
  2024-03-15 18:42:56 +0100
  * fix SSL tests for the new C/C 3.4
* Merge [Revision #99b370e023](https://github.com/MariaDB/server/commit/99b370e023) 2024-05-21 19:38:51 +0200 - Merge branch '11.2' into 11.4
* Merge [Revision #dfe030fda6](https://github.com/MariaDB/server/commit/dfe030fda6) 2024-05-20 11:11:32 +0300 - Merge 11.1 into 11.2
* Merge [Revision #6fd4fa7d71](https://github.com/MariaDB/server/commit/6fd4fa7d71) 2024-05-20 11:05:03 +0300 - Merge 11.0 into 11.1
* [Revision #d1e230d9db](https://github.com/MariaDB/server/commit/d1e230d9db)\
  2024-05-07 11:28:21 -0700
  * [MDEV-34112](https://jira.mariadb.org/browse/MDEV-34112) Replace one operator name keyword
* [Revision #2e267a4a35](https://github.com/MariaDB/server/commit/2e267a4a35)\
  2024-05-20 11:02:25 +0300
  * [MDEV-33588](https://jira.mariadb.org/browse/MDEV-33588)/[MDEV-33325](https://jira.mariadb.org/browse/MDEV-33325) after-merge fix
* [Revision #339aba04d3](https://github.com/MariaDB/server/commit/339aba04d3)\
  2024-05-15 10:54:58 -0400
  * bump the VERSION
* [Revision #fcee83f01d](https://github.com/MariaDB/server/commit/fcee83f01d)\
  2024-05-15 10:55:43 -0400
  * bump the VERSION
* [Revision #b86a2f03b6](https://github.com/MariaDB/server/commit/b86a2f03b6)\
  2024-05-06 14:46:18 +1000
  * [MDEV-32640](https://jira.mariadb.org/browse/MDEV-32640) Reset thd->lex->mi.connection\_name.str towards the end of mysql\_execute\_command
* [Revision #0e8e157510](https://github.com/MariaDB/server/commit/0e8e157510)\
  2024-05-06 15:01:32 +0400
  * [MDEV-34085](https://jira.mariadb.org/browse/MDEV-34085) Server crash ASAN used-after-poison upon 2nd execution of PS with erroneous timestamp conversion
* [Revision #3fa2caf553](https://github.com/MariaDB/server/commit/3fa2caf553)\
  2024-04-30 14:00:19 +0300
  * [MDEV-31404](https://jira.mariadb.org/browse/MDEV-31404) post-push for rpl.max\_binlog\_total\_size
* [Revision #e25edf2f46](https://github.com/MariaDB/server/commit/e25edf2f46)\
  2024-04-15 12:15:04 -0400
  * [MDEV-33616](https://jira.mariadb.org/browse/MDEV-33616) Tests failing on macOS
* [Revision #24dd78e583](https://github.com/MariaDB/server/commit/24dd78e583)\
  2024-03-05 14:46:28 +1100
  * [MDEV-33592](https://jira.mariadb.org/browse/MDEV-33592): Use X509v3 for compatibility with libraries
* [Revision #435a10e4dc](https://github.com/MariaDB/server/commit/435a10e4dc)\
  2024-03-25 13:55:45 -0300
  * [MDEV-33659](https://jira.mariadb.org/browse/MDEV-33659) Fix crash in kdf() without parameters
* [Revision #9d806a0f76](https://github.com/MariaDB/server/commit/9d806a0f76)\
  2024-03-12 13:09:11 +1100
  * [MDEV-33608](https://jira.mariadb.org/browse/MDEV-33608) Skip spider/bugfix.quick\_mode\_N for valgrind builds
* [Revision #53a359cf0d](https://github.com/MariaDB/server/commit/53a359cf0d)\
  2024-02-29 18:16:06 +0100
  * [MDEV-33554](https://jira.mariadb.org/browse/MDEV-33554) Upgrade from 11.2 to 11.3 changes root's privileges
* [Revision #ec3d9dafe4](https://github.com/MariaDB/server/commit/ec3d9dafe4)\
  2024-02-21 10:38:17 +0100
  * [MDEV-33459](https://jira.mariadb.org/browse/MDEV-33459) upgrades 11.X.2→11.(X+1).2
* [Revision #058510a62f](https://github.com/MariaDB/server/commit/058510a62f)\
  2024-02-26 13:01:38 +0200
  * Moved test for online alter in connect to separate test
* [Revision #aea1af0df6](https://github.com/MariaDB/server/commit/aea1af0df6)\
  2024-02-23 00:31:23 +0200
  * Fixed failure in innodb.corrupted\_during\_recovery
* [Revision #8d5512ee7e](https://github.com/MariaDB/server/commit/8d5512ee7e)\
  2024-02-22 21:39:21 +0200
  * Fixed bug in semi-sync that caused rpl.rpl\_semi\_sync\_slave\_reply\_fail to fail
* [Revision #ae6684d79f](https://github.com/MariaDB/server/commit/ae6684d79f)\
  2024-02-20 11:55:34 +1100
  * [MDEV-32546](https://jira.mariadb.org/browse/MDEV-32546): debian files - erronus install of plugin\_auth\_common.h
* [Revision #ccee2f059f](https://github.com/MariaDB/server/commit/ccee2f059f)\
  2024-02-19 09:12:57 +0200
  * [MDEV-32546](https://jira.mariadb.org/browse/MDEV-32546): Make sure that debian control files are also in order
* [Revision #88d79539b0](https://github.com/MariaDB/server/commit/88d79539b0)\
  2023-10-23 10:00:51 +0300
  * [MDEV-32546](https://jira.mariadb.org/browse/MDEV-32546): Make sure that Debian .install files are alphabetically ordered
* [Revision #9b6e267bfd](https://github.com/MariaDB/server/commit/9b6e267bfd)\
  2024-02-16 16:40:32 -0500
  * bump the VERSION

{% @marketo/form formid="4316" formId="4316" %}
