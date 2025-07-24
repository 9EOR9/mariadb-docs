# MariaDB 10.7.5 Changelog

The most recent release of [MariaDB 10.7](../../old-releases/release-notes-mariadb-10-7-series/what-is-mariadb-107.md) is:[**MariaDB 10.7.8**](../../old-releases/release-notes-mariadb-10-7-series/mariadb-10-7-8-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.7.8/)

[Download 10.7.5](https://downloads.mariadb.org/mariadb/10.7.5/)[Release Notes](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-7-series)[Changelog](mariadb-1075-changelog.md)[Overview of 10.7](../../old-releases/release-notes-mariadb-10-7-series/what-is-mariadb-107.md)

**Release date:** 15 Aug 2022

For the highlights of this release, see the [Release Notes](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-7-series).

The revision number links will take you to the revision's page on GitHub. On [GitHub](https://github.com/MariaDB/server/tree/10.7) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Includes all fixes from [MariaDB 10.6.9](../changelogs-mariadb-106-series/mariadb-1069-changelog.md)
* Merge [Revision #98d7ac1fbe](https://github.com/MariaDB/server/commit/98d7ac1fbe) 2022-08-10 13:25:05 +0200 - Merge branch '10.6' into 10.7
* Merge [Revision #65a963f755](https://github.com/MariaDB/server/commit/65a963f755) 2022-08-10 13:12:32 +0200 - Merge branch '10.6' into 10.7
* [Revision #fbfd44be3c](https://github.com/MariaDB/server/commit/fbfd44be3c)\
  2022-08-09 16:52:53 +0530
  * [MDEV-28400](https://jira.mariadb.org/browse/MDEV-28400) Leak in trx\_mod\_time\_t::start\_bulk\_insert()
* Merge [Revision #1d48041982](https://github.com/MariaDB/server/commit/1d48041982) 2022-08-08 17:12:32 +0200 - Merge branch '10.6' into 10.7
* [Revision #3ebbfd88a0](https://github.com/MariaDB/server/commit/3ebbfd88a0)\
  2022-08-02 16:23:08 +0400
  * [MDEV-29159](https://jira.mariadb.org/browse/MDEV-29159) Patch for [MDEV-28918](https://jira.mariadb.org/browse/MDEV-28918) introduces more inconsistency than it solves, breaks usability
* Merge [Revision #97d16c7544](https://github.com/MariaDB/server/commit/97d16c7544) 2022-08-02 08:30:18 +0300 - Merge 10.6 into 10.7
* [Revision #3330f8d156](https://github.com/MariaDB/server/commit/3330f8d156)\
  2022-08-01 14:44:55 +0530
  * [MDEV-28400](https://jira.mariadb.org/browse/MDEV-28400) Leak in trx\_mod\_time\_t::start\_bulk\_insert()
* Merge [Revision #742e1c727f](https://github.com/MariaDB/server/commit/742e1c727f) 2022-07-27 18:26:21 +0300 - Merge 10.6 into 10.7
* [Revision #19283c67c6](https://github.com/MariaDB/server/commit/19283c67c6)\
  2022-07-26 11:25:32 +0530
  * [MDEV-28679](https://jira.mariadb.org/browse/MDEV-28679) After upgrade to 10.7.3-1 with enabled data-at-rest encryption unable to restore dump file.
* [Revision #3808ffbcb5](https://github.com/MariaDB/server/commit/3808ffbcb5)\
  2022-07-13 21:06:59 +0530
  * [MDEV-28242](https://jira.mariadb.org/browse/MDEV-28242) Assertion \`!check\_foreigns' failed in trx\_t::check\_bulk\_buffer
* [Revision #48f3cf7570](https://github.com/MariaDB/server/commit/48f3cf7570)\
  2022-07-25 09:33:11 +0900
  * [MDEV-28795](https://jira.mariadb.org/browse/MDEV-28795) Deprecate spider\_bka\_table\_name\_type
* [Revision #c3ddffe29c](https://github.com/MariaDB/server/commit/c3ddffe29c)\
  2022-07-09 16:51:55 +0300
  * Fix mysqld--help.test
* [Revision #380874549c](https://github.com/MariaDB/server/commit/380874549c)\
  2022-07-08 15:29:23 +0400
  * [MDEV-29062](https://jira.mariadb.org/browse/MDEV-29062) Wrong result set metadata for a mix of INT+ENUM
* [Revision #a5f78505d7](https://github.com/MariaDB/server/commit/a5f78505d7)\
  2022-06-29 14:56:10 +0200
  * [MDEV-28838](https://jira.mariadb.org/browse/MDEV-28838) password\_reuse\_check plugin mixes username and password
* [Revision #c12192b1c6](https://github.com/MariaDB/server/commit/c12192b1c6)\
  2022-07-05 11:39:40 +0400
  * [MDEV-27015](https://jira.mariadb.org/browse/MDEV-27015) Assertion \`!is\_null()' failed in FixedBinTypeBundle::Fbt FixedBinTypeBundle::Field\_fbt::to\_fbt()
* Merge [Revision #3dff84cd15](https://github.com/MariaDB/server/commit/3dff84cd15) 2022-07-01 17:45:29 +0300 - Merge 10.6 into 10.7
* Merge [Revision #cac6f0a8c4](https://github.com/MariaDB/server/commit/cac6f0a8c4) 2022-06-29 16:17:14 +0300 - Merge 10.6 into 10.7
* Merge [Revision #ac0af4ec4a](https://github.com/MariaDB/server/commit/ac0af4ec4a) 2022-06-28 08:34:12 +0300 - Merge 10.6 into 10.7
* [Revision #4a7e337e5f](https://github.com/MariaDB/server/commit/4a7e337e5f)\
  2022-06-27 18:01:16 +0400
  * [MDEV-28963](https://jira.mariadb.org/browse/MDEV-28963) Incompatible data type assignment through SP vars is not consistent with columns
* [Revision #c4bfb61803](https://github.com/MariaDB/server/commit/c4bfb61803)\
  2022-06-27 22:51:37 +0900
  * [MDEV-28479](https://jira.mariadb.org/browse/MDEV-28479) fixup: Update spider/bg and spider/handler suites
* [Revision #0bed4d72c0](https://github.com/MariaDB/server/commit/0bed4d72c0)\
  2022-06-24 17:21:31 +0400
  * [MDEV-28918](https://jira.mariadb.org/browse/MDEV-28918) Implicit cast from INET6 UNSIGNED works differently on UPDATE vs ALTER
* [Revision #925999bb97](https://github.com/MariaDB/server/commit/925999bb97)\
  2022-06-21 17:02:04 +0900
  * [MDEV-28829](https://jira.mariadb.org/browse/MDEV-28829) Deprecate spider\_semi\_table\_lock and spider\_semi\_table\_lock\_connection
* [Revision #8e6c8967a1](https://github.com/MariaDB/server/commit/8e6c8967a1)\
  2022-06-20 16:12:16 +0900
  * [MDEV-28479](https://jira.mariadb.org/browse/MDEV-28479) Deprecate Spider's high availability feature
* [Revision #2c83fc87c2](https://github.com/MariaDB/server/commit/2c83fc87c2)\
  2022-02-15 13:37:59 +0400
  * [MDEV-27832](https://jira.mariadb.org/browse/MDEV-27832) disable binary logging for SQL SERVICE.
* Merge [Revision #5d0496c749](https://github.com/MariaDB/server/commit/5d0496c749) 2022-06-23 13:20:25 +0300 - Merge 10.6 into 10.7
* Merge [Revision #8ebff3bcb0](https://github.com/MariaDB/server/commit/8ebff3bcb0) 2022-06-22 08:34:29 +0300 - Merge 10.6 into 10.7
* Merge [Revision #6680fd8d4b](https://github.com/MariaDB/server/commit/6680fd8d4b) 2022-06-21 18:02:41 +0300 - Merge 10.6 into 10.7
* [Revision #2643aa43ae](https://github.com/MariaDB/server/commit/2643aa43ae)\
  2022-06-16 22:39:35 +0200
  * fix spider.variable\_deprecation test
* [Revision #5ad9a41301](https://github.com/MariaDB/server/commit/5ad9a41301)\
  2022-06-11 16:15:26 +0200
  * re-enable innodb.innodb\_page\_compressed tests
* Merge [Revision #a8c22dae8b](https://github.com/MariaDB/server/commit/a8c22dae8b) 2022-06-16 10:50:58 +0300 - Merge 10.6 into 10.7
* Merge [Revision #42d3a7b63d](https://github.com/MariaDB/server/commit/42d3a7b63d) 2022-06-14 15:35:49 +0300 - Merge 10.6 into 10.7
* Merge [Revision #ddf511c44d](https://github.com/MariaDB/server/commit/ddf511c44d) 2022-06-14 10:17:36 +0300 - Merge 10.6 into 10.7
* [Revision #1bcd87cdcc](https://github.com/MariaDB/server/commit/1bcd87cdcc)\
  2022-06-13 16:10:41 +0300
  * Fixed maria.maria-recover and maria.encrypt-no-key test files
* Merge [Revision #fe75e5e5b1](https://github.com/MariaDB/server/commit/fe75e5e5b1) 2022-06-09 14:11:43 +0300 - Merge 10.6 into 10.7
* Merge [Revision #09dc322342](https://github.com/MariaDB/server/commit/09dc322342) 2022-06-07 08:44:20 +0300 - Merge 10.6 into 10.7
* Merge [Revision #7e39470e33](https://github.com/MariaDB/server/commit/7e39470e33) 2022-06-06 14:56:20 +0300 - Merge 10.6 into 10.7
* [Revision #477776bfed](https://github.com/MariaDB/server/commit/477776bfed)\
  2022-06-03 17:34:22 +0400
  * [MDEV-28491](https://jira.mariadb.org/browse/MDEV-28491) Uuid. "UPDATE/DELETE" not working "WHERE id IN (SELECT id FROM ..)"
* Merge [Revision #712b443a3c](https://github.com/MariaDB/server/commit/712b443a3c) 2022-06-02 07:48:30 +0300 - Merge 10.6 into 10.7
* [Revision #52be05be15](https://github.com/MariaDB/server/commit/52be05be15)\
  2022-06-01 00:22:06 +0900
  * [MDEV-27926](https://jira.mariadb.org/browse/MDEV-27926) Deprecate spider\_init\_sql\_alloc\_size
* [Revision #61727fa40f](https://github.com/MariaDB/server/commit/61727fa40f)\
  2022-05-24 17:11:01 +1000
  * man: adjust major version to 10.7
* Merge [Revision #f00ac20b03](https://github.com/MariaDB/server/commit/f00ac20b03) 2022-05-24 09:49:48 +0300 - Merge 10.6 into 10.7
* [Revision #2577ff2667](https://github.com/MariaDB/server/commit/2577ff2667)\
  2022-05-21 15:38:57 +0900
  * [MDEV-28560](https://jira.mariadb.org/browse/MDEV-28560) Deprecate spider\_buffer\_size
* Merge [Revision #3fe2d8e619](https://github.com/MariaDB/server/commit/3fe2d8e619) 2022-05-20 21:32:50 +0200 - Merge branch '10.7' into bb-10.7-release
* [Revision #6a67c33867](https://github.com/MariaDB/server/commit/6a67c33867)\
  2022-05-20 12:57:28 -0400
  * bump the VERSION

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
