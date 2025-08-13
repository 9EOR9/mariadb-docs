# MariaDB 10.11.10 Changelog

{% include "../../../../.gitbook/includes/latest-10-11.md" %}

<a href="https://downloads.mariadb.org/mariadb/10.11.10/" class="button primary">Download</a> <a href="../../mariadb-10-11-series/mariadb-10-11-10-release-notes.md" class="button secondary">Release Notes</a> <a href="mariadb-10-11-10-changelog.md" class="button secondary">Changelog</a> <a href="../../mariadb-10-11-series/what-is-mariadb-1011.md" class="button secondary">Overview of 10.11</a>

**Release date:** 1 Nov 2024

For the highlights of this release, see the [release notes](../../mariadb-10-11-series/mariadb-10-11-10-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On [GitHub](https://github.com/MariaDB/server/tree/10.11) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Includes all fixes from [MariaDB 10.6.20](../changelogs-mariadb-106-series/mariadb-10-6-20-changelog.md)
* Merge [Revision #3d0fb15028](https://github.com/MariaDB/server/commit/3d0fb15028) 2024-10-29 15:24:38 +0100 - Merge branch '10.6' into 10.11
* [Revision #db3be9b434](https://github.com/MariaDB/server/commit/db3be9b434)\
  2024-10-29 15:03:23 +0530
  * [MDEV-35237](https://jira.mariadb.org/browse/MDEV-35237) Bulk insert fails to apply buffered operation during CREATE..SELECT statement
* [Revision #63a7e4c96b](https://github.com/MariaDB/server/commit/63a7e4c96b)\
  2024-10-28 07:44:18 +0200
  * [MDEV-35257](https://jira.mariadb.org/browse/MDEV-35257) Backup fails during an ALTER TABLE with FULLTEXT INDEX
* [Revision #abc46259c6](https://github.com/MariaDB/server/commit/abc46259c6)\
  2024-10-18 16:49:51 +0200
  * [MDEV-34753](https://jira.mariadb.org/browse/MDEV-34753) memory pressure - erroneous termination condition
* [Revision #eb29190398](https://github.com/MariaDB/server/commit/eb29190398)\
  2024-08-14 08:03:37 +1000
  * [MDEV-34753](https://jira.mariadb.org/browse/MDEV-34753) memory pressure - erroneous termination condition
* [Revision #eca552a1a4](https://github.com/MariaDB/server/commit/eca552a1a4)\
  2024-10-18 10:12:47 +0300
  * [MDEV-34830](https://jira.mariadb.org/browse/MDEV-34830): LSN in the future is not being treated as serious corruption
* [Revision #3b58c6b93f](https://github.com/MariaDB/server/commit/3b58c6b93f)\
  2024-10-04 18:40:34 +0200
  * [MDEV-35079](https://jira.mariadb.org/browse/MDEV-35079) Migrate MySQL5.7 to [MariaDB 10.4](../../../mariadb-community-server-release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/), then to [MariaDB 10.11](../../mariadb-10-11-series/what-is-mariadb-1011.md) Failed
* [Revision #7842cab8c0](https://github.com/MariaDB/server/commit/7842cab8c0)\
  2024-09-14 08:01:31 +0200
  * [MDEV-34318](https://jira.mariadb.org/browse/MDEV-34318) post-merge fix
* [Revision #649e08f8b3](https://github.com/MariaDB/server/commit/649e08f8b3)\
  2024-10-15 14:17:24 +0200
  * new libfmt 11.0.2
* [Revision #f27b69a447](https://github.com/MariaDB/server/commit/f27b69a447)\
  2024-10-15 09:25:05 +0200
  * fix [MDEV-26459](https://jira.mariadb.org/browse/MDEV-26459) test on 32bit systems.
* [Revision #8a6a4c947a](https://github.com/MariaDB/server/commit/8a6a4c947a)\
  2024-10-04 13:41:12 +0300
  * Cleanup: Replace some is\_predefined\_tablespace()
* [Revision #b249a059da](https://github.com/MariaDB/server/commit/b249a059da)\
  2024-10-04 13:38:21 +0300
  * [MDEV-34850](https://jira.mariadb.org/browse/MDEV-34850): Busy work while parsing FILE\_ records
* [Revision #590718cadc](https://github.com/MariaDB/server/commit/590718cadc)\
  2024-10-03 17:01:29 +0300
  * [MDEV-31221](https://jira.mariadb.org/browse/MDEV-31221) after-merge fix for test
* Merge [Revision #63913ce5af](https://github.com/MariaDB/server/commit/63913ce5af) 2024-10-03 10:55:08 +0300 - Merge 10.6 into 10.11
* [Revision #21b20712a3](https://github.com/MariaDB/server/commit/21b20712a3)\
  2024-03-19 00:11:11 +0000
  * Replace using of internal fmt lib API with public API
* [Revision #da322f19c6](https://github.com/MariaDB/server/commit/da322f19c6)\
  2021-10-01 11:00:29 +0200
  * [MDEV-26459](https://jira.mariadb.org/browse/MDEV-26459) Assertion \`block\_size <= 0xFFFFFFFFL' failed in calculate\_block\_sizes for 10.7 only
* [Revision #dd5ce6b0c4](https://github.com/MariaDB/server/commit/dd5ce6b0c4)\
  2024-09-30 13:36:38 +0300
  * [MDEV-34450](https://jira.mariadb.org/browse/MDEV-34450) os\_file\_write\_func() is an overkill for ib\_logfile0
* [Revision #2d3ddaef35](https://github.com/MariaDB/server/commit/2d3ddaef35)\
  2024-09-27 12:31:37 +0300
  * [MDEV-34907](https://jira.mariadb.org/browse/MDEV-34907) Bogus assertion failure and busy work while parsing FILE\_ records
* [Revision #6acada713a](https://github.com/MariaDB/server/commit/6acada713a)\
  2024-09-26 18:47:12 +0300
  * [MDEV-34062](https://jira.mariadb.org/browse/MDEV-34062): Implement innodb\_log\_file\_mmap on 64-bit systems
* Merge [Revision #971cf59579](https://github.com/MariaDB/server/commit/971cf59579) 2024-09-24 08:49:20 +0300 - Merge 10.6 into 10.11
* [Revision #9ea7f7129a](https://github.com/MariaDB/server/commit/9ea7f7129a)\
  2024-09-20 15:29:56 +0300
  * [MDEV-34909](https://jira.mariadb.org/browse/MDEV-34909) DDL hang during SET GLOBAL innodb\_log\_file\_size on PMEM
* [Revision #cb83ae210c](https://github.com/MariaDB/server/commit/cb83ae210c)\
  2024-09-19 09:02:46 +0200
  * galera mtr suite: fixes for unstable tests
* [Revision #391c9db486](https://github.com/MariaDB/server/commit/391c9db486)\
  2024-09-18 16:41:57 +1000
  * [MDEV-34952](https://jira.mariadb.org/browse/MDEV-34952) main.log\_slow test failure on opensuse builder
* Merge [Revision #f176248d4b](https://github.com/MariaDB/server/commit/f176248d4b) 2024-09-17 01:21:26 +0200 - Merge branch '10.6' into '10.11'
* Merge [Revision #b187414764](https://github.com/MariaDB/server/commit/b187414764) 2024-09-16 10:58:40 +0300 - Merge 10.6 into 10.11
* [Revision #e3f653ca66](https://github.com/MariaDB/server/commit/e3f653ca66)\
  2024-09-14 10:35:28 +0300
  * [MDEV-34750](https://jira.mariadb.org/browse/MDEV-34750) fixup: -Wconversion on 32-bit
* Merge [Revision #a8c5717223](https://github.com/MariaDB/server/commit/a8c5717223) 2024-09-12 10:44:13 +1000 - Merge branch '10.6' into 10.11
* Merge [Revision #b168859d1e](https://github.com/MariaDB/server/commit/b168859d1e) 2024-09-11 16:10:53 +1000 - Merge branch '10.6' into 10.11
* [Revision #2496779d69](https://github.com/MariaDB/server/commit/2496779d69)\
  2024-07-23 13:30:17 +1000
  * [MDEV-34617](https://jira.mariadb.org/browse/MDEV-34617) galera.galera\_ist\_mariadb-backup\_verify\_ca fails on FreeBSD
* [Revision #24d67aaf9c](https://github.com/MariaDB/server/commit/24d67aaf9c)\
  2024-09-09 14:13:38 +1000
  * [MDEV-34825](https://jira.mariadb.org/browse/MDEV-34825) FreeBSD fails to build under clang natively (postfix)
* [Revision #ccb4bc7754](https://github.com/MariaDB/server/commit/ccb4bc7754)\
  2024-09-09 14:05:02 +1000
  * [MDEV-33894](https://jira.mariadb.org/browse/MDEV-33894): Resurrect innodb\_log\_write\_ahead\_size (postfix)
* [Revision #852d42e993](https://github.com/MariaDB/server/commit/852d42e993)\
  2024-09-09 16:47:35 +0300
  * [MDEV-34483](https://jira.mariadb.org/browse/MDEV-34483) Backup may copy unnecessarily much log
* Merge [Revision #d002b1f503](https://github.com/MariaDB/server/commit/d002b1f503) 2024-09-09 11:34:19 +1000 - Merge branch '10.6' into 10.11
* Merge [Revision #f9f92b480e](https://github.com/MariaDB/server/commit/f9f92b480e) 2024-09-06 16:17:42 +0300 - Merge 10.6 into 10.11
* Merge [Revision #2da4839bb6](https://github.com/MariaDB/server/commit/2da4839bb6) 2024-09-06 14:45:22 +0300 - Merge 10.6 into 10.11
* [Revision #4972f9fc0f](https://github.com/MariaDB/server/commit/4972f9fc0f)\
  2024-09-05 16:24:16 +0530
  * [MDEV-33087](https://jira.mariadb.org/browse/MDEV-33087) ALTER TABLE...ALGORITHM=COPY should build indexes more efficiently
* [Revision #fe5829a121](https://github.com/MariaDB/server/commit/fe5829a121)\
  2024-09-04 14:24:30 +0300
  * [MDEV-34446](https://jira.mariadb.org/browse/MDEV-34446) SIGSEGV on SET GLOBAL innodb\_log\_file\_size with memory-mapped log file
* [Revision #b3cc952916](https://github.com/MariaDB/server/commit/b3cc952916)\
  2024-09-03 05:57:22 +0200
  * galera tests: updated .result for galera\_gtid\_2\_cluster test
* [Revision #72243bc236](https://github.com/MariaDB/server/commit/72243bc236)\
  2023-06-14 08:55:58 +0300
  * [MDEV-31173](https://jira.mariadb.org/browse/MDEV-31173) : Server crashes when setting wsrep\_cluster\_address after adding invalid value to wsrep\_allowlist table
* Merge [Revision #d058be62b8](https://github.com/MariaDB/server/commit/d058be62b8) 2024-09-02 03:42:02 +0200 - Merge branch '10.6' into '10.11'
* [Revision #984606d747](https://github.com/MariaDB/server/commit/984606d747)\
  2024-08-29 14:53:08 +0300
  * [MDEV-34750](https://jira.mariadb.org/browse/MDEV-34750) SET GLOBAL innodb\_log\_file\_size is not crash safe
* Merge [Revision #3a1ff7398a](https://github.com/MariaDB/server/commit/3a1ff7398a) 2024-08-29 12:14:44 +0200 - Merge branch '10.6' into 10.11
* Merge [Revision #cfcf27c6fe](https://github.com/MariaDB/server/commit/cfcf27c6fe) 2024-08-29 07:47:29 +0300 - Merge 10.6 into 10.11
* [Revision #22b48bb393](https://github.com/MariaDB/server/commit/22b48bb393)\
  2024-08-21 18:58:20 +0530
  * [MDEV-34756](https://jira.mariadb.org/browse/MDEV-34756) Validation of new foreign key skipped if innodb\_alter\_copy\_bulk=ON
* Merge [Revision #70afc62750](https://github.com/MariaDB/server/commit/70afc62750) 2024-08-20 10:00:39 +0200 - Merge branch '10.6' into 10.11
* Merge [Revision #62bfcfd8b2](https://github.com/MariaDB/server/commit/62bfcfd8b2) 2024-08-14 11:36:52 +0300 - Merge 10.6 into 10.11
* Merge [Revision #f8a735d6d8](https://github.com/MariaDB/server/commit/f8a735d6d8) 2024-08-09 08:53:20 +0200 - Merge branch '10.11' into mariadb-10.11.9
* [Revision #8da477414b](https://github.com/MariaDB/server/commit/8da477414b)\
  2024-08-08 18:00:06 -0400
  * bump the VERSION
* [Revision #e515e80773](https://github.com/MariaDB/server/commit/e515e80773)\
  2024-08-03 13:11:35 +0530
  * [MDEV-34689](https://jira.mariadb.org/browse/MDEV-34689) Redo log corruption at high load

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
