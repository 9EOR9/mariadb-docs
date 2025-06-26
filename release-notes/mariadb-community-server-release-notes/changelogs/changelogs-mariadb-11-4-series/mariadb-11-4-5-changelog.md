# MariaDB 11.4.5 Changelog

[Download](https://mariadb.com/downloads/)[Release Notes](../../mariadb-11-4-series/mariadb-11-4-5-release-notes.md)[Changelog](mariadb-11-4-5-changelog.md)[Overview of 11.4](../../mariadb-11-4-series/what-is-mariadb-114.md)

[_Alternate download from mariadb.org_](https://downloads.mariadb.org/mariadb/11.4.5/)

**Release date:** 4 Feb 2025

For the highlights of this release, see the[release notes](../../mariadb-11-4-series/mariadb-11-4-5-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/server/tree/11.4) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Includes all fixes from [MariaDB 10.11.11](../changelogs-mariadb-10-11-series/mariadb-10-11-11-changelog.md)
* Includes all fixes from [MariaDB 11.2.6](../changelogs-mariadb-11-2-series/mariadb-11-2-6-changelog.md)
* Includes all fixes from [MariaDB 11.3.2](../changelogs-mariadb-11-3-series/mariadb-11-3-2-changelog.md)
* [Revision #0771110266](https://github.com/MariaDB/server/commit/0771110266)\
  2025-01-30 10:25:18 +0100
  * [MDEV-33658](https://jira.mariadb.org/browse/MDEV-33658) 1/2 FULLTEXT and SPATIAL keys are not "too long"
* Merge [Revision #7d657fda64](https://github.com/MariaDB/server/commit/7d657fda64) 2025-01-30 11:59:53 +0100 - Merge branch '10.11 into 11.4
* [Revision #5be38d14fc](https://github.com/MariaDB/server/commit/5be38d14fc)\
  2025-01-25 20:07:02 +0100
  * ColumnStore 23.10.3-1
* [Revision #92a6789638](https://github.com/MariaDB/server/commit/92a6789638)\
  2025-01-25 18:09:41 +0100
  * C/C 3.4.4
* [Revision #04bd6ed44c](https://github.com/MariaDB/server/commit/04bd6ed44c)\
  2025-01-17 17:54:59 +0100
  * [MDEV-35368](https://jira.mariadb.org/browse/MDEV-35368) Validation of SSL certificate fails for mariadb-backup
* [Revision #25b1c3505f](https://github.com/MariaDB/server/commit/25b1c3505f)\
  2025-01-27 16:17:48 +0400
  * [MDEV-35677](https://jira.mariadb.org/browse/MDEV-35677) Assertion \`thd->is\_error()' failed in virtual bool Field::sp\_prepare\_and\_store\_item(THD\*, Item)
* [Revision #95a0325b58](https://github.com/MariaDB/server/commit/95a0325b58)\
  2025-01-13 17:27:03 +0700
  * [MDEV-32575](https://jira.mariadb.org/browse/MDEV-32575) MSAN / Valgrind errors in test\_if\_cheaper\_ordering upon reaching in\_predicate\_conversion\_threshold
* [Revision #3a6af458e6](https://github.com/MariaDB/server/commit/3a6af458e6)\
  2024-10-10 15:43:36 +0300
  * [MDEV-34877](https://jira.mariadb.org/browse/MDEV-34877) Port "Bug #11745929 Change lock priority so that the transaction holding S-lock gets X-lock first" fix from MySQL to MariaDB
* [Revision #c1559f261f](https://github.com/MariaDB/server/commit/c1559f261f)\
  2025-01-20 19:53:25 +0400
  * [MDEV-35688](https://jira.mariadb.org/browse/MDEV-35688) UBSAN: SUMMARY: UndefinedBehaviorSanitizer: nullptr-with-offset in my\_casedn\_utf8mb3
* [Revision #6be42c7276](https://github.com/MariaDB/server/commit/6be42c7276)\
  2025-01-17 14:43:06 +0200
  * Removed test not related to utf8mb4\_0900 from ctype\_utf8mb4\_0900.test
* [Revision #653f68784a](https://github.com/MariaDB/server/commit/653f68784a)\
  2025-01-17 11:29:01 +0200
  * [MDEV-35865](https://jira.mariadb.org/browse/MDEV-35865) atomic.alter\_table times out often
* [Revision #b22eacc976](https://github.com/MariaDB/server/commit/b22eacc976)\
  2025-01-17 14:16:41 +0100
  * fix sporadic failures of main.alter\_table\_online
* [Revision #1643a258d2](https://github.com/MariaDB/server/commit/1643a258d2)\
  2025-01-15 21:23:33 +0100
  * update wsrep test for 26.4.21
* [Revision #904f2e4b2d](https://github.com/MariaDB/server/commit/904f2e4b2d)\
  2025-01-15 21:22:48 +0100
  * fix galera tests for 11.4
* [Revision #f1da9dbf5e](https://github.com/MariaDB/server/commit/f1da9dbf5e)\
  2025-01-15 09:51:19 +0100
  * [MDEV-20912](https://jira.mariadb.org/browse/MDEV-20912) fix test results
* [Revision #c40709660f](https://github.com/MariaDB/server/commit/c40709660f)\
  2025-01-15 09:49:33 +0100
  * [MDEV-35773](https://jira.mariadb.org/browse/MDEV-35773) fix test results
* Merge [Revision #f1a7693bc0](https://github.com/MariaDB/server/commit/f1a7693bc0) 2025-01-14 23:45:41 +0100 - Merge branch '10.11' into 11.4
* [Revision #f014d5872b](https://github.com/MariaDB/server/commit/f014d5872b)\
  2025-01-09 17:32:44 +1100
  * [MDEV-35554](https://jira.mariadb.org/browse/MDEV-35554) call to function show\_binlog\_space\_total()
* Merge [Revision #bca4cc0bd6](https://github.com/MariaDB/server/commit/bca4cc0bd6) 2025-01-09 14:02:19 +0200 - Merge 10.11 into 11.4
* Merge [Revision #17f01186f5](https://github.com/MariaDB/server/commit/17f01186f5) 2025-01-09 07:58:08 +0200 - Merge 10.11 into 11.4
* [Revision #437550b7cf](https://github.com/MariaDB/server/commit/437550b7cf)\
  2025-01-06 12:13:33 -0500
  * [MDEV-35773](https://jira.mariadb.org/browse/MDEV-35773) ER\_PSEUDO\_THREAD\_ID\_OVERWRITE in 11.4 shifts error messages
* [Revision #7fcaab7aaa](https://github.com/MariaDB/server/commit/7fcaab7aaa)\
  2024-12-15 15:57:53 +0200
  * [MDEV-20912](https://jira.mariadb.org/browse/MDEV-20912) Add support for utf8mb4\_0900\_\* collations in MariaDB Server
* [Revision #9e7762e718](https://github.com/MariaDB/server/commit/9e7762e718)\
  2024-12-03 17:18:23 +0100
  * [MDEV-35233](https://jira.mariadb.org/browse/MDEV-35233): RBR does not work with CSV tables
* [Revision #b66d421d60](https://github.com/MariaDB/server/commit/b66d421d60)\
  2024-12-13 10:40:04 +0100
  * [MDEV-35046](https://jira.mariadb.org/browse/MDEV-35046) update test results
* [Revision #4c9fd4f45b](https://github.com/MariaDB/server/commit/4c9fd4f45b)\
  2024-12-10 11:33:25 +0100
  * [CONC-743](https://jira.mariadb.org/browse/CONC-743) Enable parsec by default
* [Revision #f8eab69c3e](https://github.com/MariaDB/server/commit/f8eab69c3e)\
  2024-12-02 14:14:12 +0100
  * [MDEV-21858](https://jira.mariadb.org/browse/MDEV-21858): START/STOP ALL SLAVES does not return access errors
* [Revision #867b53cf4e](https://github.com/MariaDB/server/commit/867b53cf4e)\
  2024-11-30 22:41:45 +0100
  * [MDEV-31794](https://jira.mariadb.org/browse/MDEV-31794): Preserved unsupported table flags break replication
* [Revision #d13eb66f4f](https://github.com/MariaDB/server/commit/d13eb66f4f)\
  2024-11-29 20:44:13 +0100
  * [MDEV-13831](https://jira.mariadb.org/browse/MDEV-13831): Assertion on event group missing XID/COMMIT event
* [Revision #ec002a11e7](https://github.com/MariaDB/server/commit/ec002a11e7)\
  2024-11-29 10:58:05 +0100
  * [MDEV-11176](https://jira.mariadb.org/browse/MDEV-11176): FTWRL confusing state about "worker thread pool"
* [Revision #db8dfe0162](https://github.com/MariaDB/server/commit/db8dfe0162)\
  2024-12-05 12:07:39 +0100
  * After-merge fix, spider deprecation warning
* Merge [Revision #0f47db8525](https://github.com/MariaDB/server/commit/0f47db8525) 2024-12-05 11:01:42 +0100 - Merge 10.11 -> 11.4
* [Revision #e41145f76b](https://github.com/MariaDB/server/commit/e41145f76b)\
  2024-12-04 09:30:18 +0200
  * Update libmariadb
* Merge [Revision #2719cc4925](https://github.com/MariaDB/server/commit/2719cc4925) 2024-12-02 11:35:34 +0200 - Merge 10.11 into 11.4
* [Revision #866a8ea673](https://github.com/MariaDB/server/commit/866a8ea673)\
  2024-11-19 20:13:24 +0530
  * [MDEV-35398](https://jira.mariadb.org/browse/MDEV-35398) Improve shrinking of system tablespace
* [Revision #9da7b41151](https://github.com/MariaDB/server/commit/9da7b41151)\
  2024-09-20 18:02:17 -0600
  * Fix `DBUG_PRINT` format of `group_trp->records`
* [Revision #3f114a0930](https://github.com/MariaDB/server/commit/3f114a0930)\
  2024-11-14 11:48:30 -0500
  * [MDEV-35046](https://jira.mariadb.org/browse/MDEV-35046) SIGSEGV in list\_delete in optimized builds when using pseudo\_slave\_mode
* [Revision #41f54da46f](https://github.com/MariaDB/server/commit/41f54da46f)\
  2024-11-05 15:15:58 +0700
  * [MDEV-35342](https://jira.mariadb.org/browse/MDEV-35342) Server crashes when creating index on a rocksdb table
* [Revision #f10d12008c](https://github.com/MariaDB/server/commit/f10d12008c)\
  2024-10-31 14:20:01 +0200
  * [MDEV-35301](https://jira.mariadb.org/browse/MDEV-35301): Bump minimum cmake version to 3.12.0
* Merge [Revision #26514346bd](https://github.com/MariaDB/server/commit/26514346bd) 2024-11-04 08:58:46 +0100 - Merge branch '11.4' into mariadb-11.4.4
* [Revision #021343df27](https://github.com/MariaDB/server/commit/021343df27)\
  2024-11-01 11:39:00 -0400
  * bump the VERSION
* [Revision #2d4551eef1](https://github.com/MariaDB/server/commit/2d4551eef1)\
  2024-10-30 13:24:45 +1100
  * [MDEV-34272](https://jira.mariadb.org/browse/MDEV-34272) create server with odbc results in connection string

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
