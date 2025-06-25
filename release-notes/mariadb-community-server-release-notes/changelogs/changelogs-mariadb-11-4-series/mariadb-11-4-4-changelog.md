# MariaDB 11.4.4 Changelog

The most recent release of [MariaDB 11.4](../../mariadb-11-4-series/what-is-mariadb-114.md) is:[**MariaDB 11.4.5**](../../mariadb-11-4-series/mariadb-11-4-5-release-notes.md) Stable (GA) [Download Now](https://mariadb.com/downloads/)[_Alternate download from mariadb.org_](https://downloads.mariadb.org/mariadb/11.4.5/)

[Download 11.4.4](https://downloads.mariadb.org/mariadb/11.4.4/)[Release Notes](../../mariadb-11-4-series/mariadb-11-4-4-release-notes.md)[Changelog](mariadb-11-4-4-changelog.md)[Overview of 11.4](../../mariadb-11-4-series/what-is-mariadb-114.md)

**Release date:** 1 Nov 2024

For the highlights of this release, see the[release notes](../../mariadb-11-4-series/mariadb-11-4-4-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/server/tree/11.4) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Includes all fixes from [MariaDB 11.2.6](../changelogs-mariadb-11-2-series/mariadb-11-2-6-changelog.md)
* Includes all fixes from [MariaDB 11.3.2](../changelogs-mariadb-11-3-series/mariadb-11-3-2-changelog.md)
* [Revision #e9a502df08](https://github.com/MariaDB/server/commit/e9a502df08)\
  2024-10-30 08:32:19 -0600
  * Testing fix for rpl\_semi\_sync\_cond\_var\_per\_thd failure
* Merge [Revision #c770bce898](https://github.com/MariaDB/server/commit/c770bce898) 2024-10-30 09:24:04 +0100 - Merge branch '11.2' into 11.4
* [Revision #973e641c32](https://github.com/MariaDB/server/commit/973e641c32)\
  2024-09-14 08:05:12 +0200
  * [MDEV-34318](https://jira.mariadb.org/browse/MDEV-34318) post-merge fix
* [Revision #9d09ef4863](https://github.com/MariaDB/server/commit/9d09ef4863)\
  2024-10-14 20:09:53 +0200
  * [MDEV-33556](https://jira.mariadb.org/browse/MDEV-33556): Document mariadb-import --parallel option in man page
* Merge [Revision #b53b81e937](https://github.com/MariaDB/server/commit/b53b81e937) 2024-10-03 14:32:14 +0300 - Merge 11.2 into 11.4
* [Revision #90f090f22c](https://github.com/MariaDB/server/commit/90f090f22c)\
  2024-10-02 09:41:28 +0200
  * Fix binlog.binlog\_mdev25611 test failure on non-debug build
* [Revision #d8d80bd503](https://github.com/MariaDB/server/commit/d8d80bd503)\
  2024-09-22 13:33:16 -0600
  * Fix a couple of `my_snprintf` arg mismatches
* [Revision #35c732cdde](https://github.com/MariaDB/server/commit/35c732cdde)\
  2024-09-18 14:19:52 +0200
  * [MDEV-25611](https://jira.mariadb.org/browse/MDEV-25611): RESET MASTER causes the server to hang
* Merge [Revision #7ea9e1358f](https://github.com/MariaDB/server/commit/7ea9e1358f) 2024-09-18 08:07:22 +0300 - Merge 11.2 into 11.4
* Merge [Revision #1f7f406b7b](https://github.com/MariaDB/server/commit/1f7f406b7b) 2024-09-18 11:27:53 +1000 - Merge branch '11.2' into 11.4
* Merge [Revision #762ad01c7f](https://github.com/MariaDB/server/commit/762ad01c7f) 2024-09-13 13:09:23 +0300 - Merge 11.2 into 11.4
* Merge [Revision #2c3b298337](https://github.com/MariaDB/server/commit/2c3b298337) 2024-09-09 14:40:02 +0300 - Merge 11.2 into 11.4
* [Revision #cbe13e9ec0](https://github.com/MariaDB/server/commit/cbe13e9ec0)\
  2024-09-04 11:13:36 +0200
  * Windows installer - ignore hashicorp-key-management, even if it was built.
* [Revision #9011e3be18](https://github.com/MariaDB/server/commit/9011e3be18)\
  2024-09-03 19:15:59 +0200
  * Update man pages, binary names, version
* Merge [Revision #44733aa8cf](https://github.com/MariaDB/server/commit/44733aa8cf) 2024-08-29 19:10:38 +0300 - Merge 11.2 into 11.4
* [Revision #18d3f63a4e](https://github.com/MariaDB/server/commit/18d3f63a4e)\
  2024-06-11 09:50:08 +1000
  * [MDEV-32627](https://jira.mariadb.org/browse/MDEV-32627) Spider: use CONNECTION string in SQLDriverConnect
* [Revision #fea36b1905](https://github.com/MariaDB/server/commit/fea36b1905)\
  2024-08-14 12:24:33 +1000
  * [MDEV-34754](https://jira.mariadb.org/browse/MDEV-34754) packaging prep for Oracular
* [Revision #bd54475efa](https://github.com/MariaDB/server/commit/bd54475efa)\
  2024-08-22 13:44:13 -0600
  * [MDEV-34779](https://jira.mariadb.org/browse/MDEV-34779): Sporadic test failure in rpl.rpl\_semi\_sync\_cond\_var\_per\_thd
* Merge [Revision #eb70e0d6e2](https://github.com/MariaDB/server/commit/eb70e0d6e2) 2024-08-21 09:30:54 +0200 - Merge branch '11.2' into 11.4
* [Revision #7318fa180d](https://github.com/MariaDB/server/commit/7318fa180d)\
  2024-08-17 12:29:00 +0200
  * Fix sporadic test failure of mariadb-backup.slave\_provision\_nolock
* [Revision #78fcb9474c](https://github.com/MariaDB/server/commit/78fcb9474c)\
  2024-08-19 20:49:28 +0200
  * Fix sporadic failure in test rpl.rpl\_rotate\_logs
* [Revision #5dc2fe4815](https://github.com/MariaDB/server/commit/5dc2fe4815)\
  2024-08-16 22:27:01 +0200
  * Fix sporadic failure in test rpl.rpl\_rotate\_logs
* Merge [Revision #341228105c](https://github.com/MariaDB/server/commit/341228105c) 2024-08-09 09:01:39 +0200 - Merge branch '11.4' into mariadb-11.4.3
* [Revision #edfeb079de](https://github.com/MariaDB/server/commit/edfeb079de)\
  2024-08-08 18:03:49 -0400
  * bump the VERSION

{% include "https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/~/reusable/vX1KAy0t1XuYJaGsK28T/" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
