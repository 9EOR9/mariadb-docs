# MariaDB 10.7.2 Changelog

The most recent release of [MariaDB 10.7](../../old-releases/release-notes-mariadb-10-7-series/what-is-mariadb-107.md) is:[**MariaDB 10.7.8**](../../old-releases/release-notes-mariadb-10-7-series/mariadb-10-7-8-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.7.8/)

[Download 10.7.2](https://mariadb.com/downloads/)[Release Notes](../../old-releases/release-notes-mariadb-10-7-series/mariadb-1072-release-notes.md)[Changelog](mariadb-1072-changelog.md)[Overview of 10.7](../../old-releases/release-notes-mariadb-10-7-series/what-is-mariadb-107.md)

**Release date:** 9 Feb 2022

For the highlights of this release, see the[release notes](../../old-releases/release-notes-mariadb-10-7-series/mariadb-1072-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/server/tree/10.7) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Includes all fixes from [MariaDB 10.6.6](../changelogs-mariadb-106-series/mariadb-1066-changelog.md)
* [Revision #cb1316b8d2](https://github.com/MariaDB/server/commit/cb1316b8d2)\
  2022-02-06 12:20:51 +0100
  * wrong merge
* Merge [Revision #2150ad3fdb](https://github.com/MariaDB/server/commit/2150ad3fdb) 2022-02-06 10:14:47 +0100 - Merge branch '10.6' into 10.7
* Merge [Revision #47f42ce130](https://github.com/MariaDB/server/commit/47f42ce130) 2022-02-04 14:53:19 +0100 - Merge branch '10.6' into 10.7
* Merge [Revision #9ed8deb656](https://github.com/MariaDB/server/commit/9ed8deb656) 2022-02-04 14:11:46 +0100 - Merge branch '10.6' into 10.7
* [Revision #3351dfaab0](https://github.com/MariaDB/server/commit/3351dfaab0)\
  2022-01-27 02:20:40 +0200
  * Skip list for UBSAN builder
* Merge [Revision #5e6fd4e804](https://github.com/MariaDB/server/commit/5e6fd4e804) 2022-01-20 08:02:58 +0200 - Merge 10.6 into 10.7
* Merge [Revision #b0998583f8](https://github.com/MariaDB/server/commit/b0998583f8) 2022-01-18 13:01:19 +0200 - Merge 10.6 into 10.7
* Merge [Revision #c669e764d8](https://github.com/MariaDB/server/commit/c669e764d8) 2022-01-14 19:30:14 +0200 - Merge 10.6 into 10.7
* [Revision #a90e1165fd](https://github.com/MariaDB/server/commit/a90e1165fd)\
  2022-01-12 17:38:15 +0530
  * [MDEV-27312](https://jira.mariadb.org/browse/MDEV-27312) LeakSanitizer error in trx\_mod\_table\_time\_t::start\_bulk\_insert
* [Revision #03ed2e9d97](https://github.com/MariaDB/server/commit/03ed2e9d97)\
  2021-12-27 16:17:29 +0530
  * [MDEV-27318](https://jira.mariadb.org/browse/MDEV-27318) Assertion \`data\_size < srv\_sort\_buf\_size' failed in row\_merge\_bulk\_buf\_add
* Merge [Revision #a23f3ee84e](https://github.com/MariaDB/server/commit/a23f3ee84e) 2022-01-12 13:14:58 +0200 - Merge 10.6 into 10.7
* Merge [Revision #ce663ad4e4](https://github.com/MariaDB/server/commit/ce663ad4e4) 2022-01-04 15:54:19 +0200 - Merge 10.6 into 10.7
* Merge [Revision #7dfaded962](https://github.com/MariaDB/server/commit/7dfaded962) 2022-01-04 09:55:58 +0200 - Merge 10.6 into 10.7
* [Revision #9f2a6bbe6b](https://github.com/MariaDB/server/commit/9f2a6bbe6b)\
  2021-12-23 12:50:00 +0530
  * [MDEV-27316](https://jira.mariadb.org/browse/MDEV-27316) Assertion \`!(index)->is\_spatial()' failed
* [Revision #1b8f0d4b67](https://github.com/MariaDB/server/commit/1b8f0d4b67)\
  2021-12-20 18:14:36 +0100
  * bump up server's maturity
* [Revision #db0ea46eab](https://github.com/MariaDB/server/commit/db0ea46eab)\
  2021-12-20 17:23:32 +0100
  * [MDEV-27261](https://jira.mariadb.org/browse/MDEV-27261) Change maturity of plugins for 10.7 GA
* Merge [Revision #92a4e76a2c](https://github.com/MariaDB/server/commit/92a4e76a2c) 2021-12-14 14:27:35 +0200 - Merge 10.6 into 10.7
* [Revision #b1d647ae85](https://github.com/MariaDB/server/commit/b1d647ae85)\
  2021-12-09 09:38:03 +0100
  * [MDEV-27001](https://jira.mariadb.org/browse/MDEV-27001) Galera crashes when converting table to partition
* [Revision #979b23d5bf](https://github.com/MariaDB/server/commit/979b23d5bf)\
  2021-12-10 13:04:46 +0200
  * Add forgotten changes to the parent commit
* [Revision #28b27b96d0](https://github.com/MariaDB/server/commit/28b27b96d0)\
  2021-12-10 12:26:26 +0200
  * Cleanup: Remove some ib::logger in recovery messages
* Merge [Revision #26fdbd7632](https://github.com/MariaDB/server/commit/26fdbd7632) 2021-12-10 11:32:49 +0200 - Merge 10.6 into 10.7
* [Revision #f502ae8226](https://github.com/MariaDB/server/commit/f502ae8226)\
  2021-12-08 14:57:37 +0100
  * SUMMARY/DESCRIPTION for compression provider RPMs
* Merge [Revision #ef77c05126](https://github.com/MariaDB/server/commit/ef77c05126) 2021-12-08 10:33:36 +0100 - Merge branch '10.6' into 10.7
* [Revision #60d565e66a](https://github.com/MariaDB/server/commit/60d565e66a)\
  2021-11-04 16:17:35 +0100
  * cmake: detect lz4 version, require >= 1.6
* Merge [Revision #182bf9b333](https://github.com/MariaDB/server/commit/182bf9b333) 2021-12-04 13:23:14 +0200 - Merge 10.6 into 10.7
* Merge [Revision #1e54a9716d](https://github.com/MariaDB/server/commit/1e54a9716d) 2021-12-02 17:22:06 +0200 - Merge 10.6 into 10.7
* Merge [Revision #c22107fd90](https://github.com/MariaDB/server/commit/c22107fd90) 2021-11-29 11:42:07 +0200 - Merge 10.6 into 10.7
* Merge [Revision #ac3b33d236](https://github.com/MariaDB/server/commit/ac3b33d236) 2021-11-25 18:51:12 +0200 - Merge 10.6 into 10.7
* [Revision #e8f6b3b20e](https://github.com/MariaDB/server/commit/e8f6b3b20e)\
  2021-11-25 18:50:29 +0200
  * Restore a DBUG\_SUICIDE for binlog.binlog\_truncate\_multi\_engine
* Merge [Revision #5f160b4d86](https://github.com/MariaDB/server/commit/5f160b4d86) 2021-11-25 08:10:02 +0200 - Merge 10.6 into 10.7
* [Revision #80834a8f5d](https://github.com/MariaDB/server/commit/80834a8f5d)\
  2021-11-19 17:46:28 +0200
  * Cleanup: Remove unused DBUG\_SUICIDE()
* [Revision #4489a89c71](https://github.com/MariaDB/server/commit/4489a89c71)\
  2021-11-19 17:46:16 +0200
  * [MDEV-27094](https://jira.mariadb.org/browse/MDEV-27094) Debug builds include useless InnoDB "disabled" options
* Merge [Revision #7e8a13d9d7](https://github.com/MariaDB/server/commit/7e8a13d9d7) 2021-11-19 17:45:52 +0200 - Merge 10.6 into 10.7
* [Revision #32e8e84795](https://github.com/MariaDB/server/commit/32e8e84795)\
  2021-11-19 18:06:48 +0300
  * [MDEV-27048](https://jira.mariadb.org/browse/MDEV-27048) UBSAN: runtime error: shift exponent 32 is too large for 32-bit type 'unsigned int'
* Merge [Revision #d9a5c5db07](https://github.com/MariaDB/server/commit/d9a5c5db07) 2021-11-12 00:34:37 +0100 - Merge branch '10.6' into 10.7
* Merge [Revision #06988bdcaa](https://github.com/MariaDB/server/commit/06988bdcaa) 2021-11-09 09:40:29 +0200 - Merge 10.6 into 10.7
* Merge [Revision #662fe08232](https://github.com/MariaDB/server/commit/662fe08232) 2021-11-08 19:43:43 +0100 - Merge branch '10.7' into bb-10.7-release
* [Revision #30b0aa72d6](https://github.com/MariaDB/server/commit/30b0aa72d6)\
  2021-11-08 11:37:22 -0500
  * bump the VERSION
* [Revision #3f3ec40c91](https://github.com/MariaDB/server/commit/3f3ec40c91)\
  2021-11-08 10:24:52 +0200
  * [MDEV-26664](https://jira.mariadb.org/browse/MDEV-26664) fixup: clang -Winconsistent-missing-override
* [Revision #8c9cc2fb6e](https://github.com/MariaDB/server/commit/8c9cc2fb6e)\
  2021-11-07 04:41:35 +0530
  * [MDEV-26956](https://jira.mariadb.org/browse/MDEV-26956) LeakSanitizer/Valgrind errors in trx\_mod\_table\_time\_t::start\_bulk\_insert upon adding system versioning
* Merge [Revision #d20de4d447](https://github.com/MariaDB/server/commit/d20de4d447) 2021-11-04 10:55:05 +0100 - Merge branch '10.6' into 10.7
* [Revision #d6e3cd6f23](https://github.com/MariaDB/server/commit/d6e3cd6f23)\
  2021-11-01 13:49:57 +0530
  * [MDEV-26947](https://jira.mariadb.org/browse/MDEV-26947) UNIQUE column checks fail in InnoDB resulting in table corruption

{% @marketo/form formid="4316" formId="4316" %}
