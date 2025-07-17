# MariaDB 10.6.19 Changelog

{% include "../../../.gitbook/includes/latest-10-6.md" %}

<a href="https://downloads.mariadb.org/mariadb/10.6.19/" class="button primary">Download</a> <a href="../../mariadb-10-6-series/mariadb-10-6-19-release-notes.md" class="button secondary">Release Notes</a> <a href="mariadb-10-6-19-changelog.md" class="button secondary">Changelog</a> <a href="../../mariadb-10-6-series/what-is-mariadb-106.md" class="button secondary">Overview of 10.6</a>

**Release date:** 8 Aug 2024

For the highlights of this release, see the [release notes](../../mariadb-10-6-series/mariadb-10-6-19-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On [GitHub](https://github.com/MariaDB/server/tree/10.6) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Includes all fixes from [MariaDB 10.5.26](../changelogs-mariadb-105-series/mariadb-10-5-26-changelog.md)
* Merge [Revision #8f020508c8](https://github.com/MariaDB/server/commit/8f020508c8) 2024-08-03 09:04:24 +0200 - Merge branch '10.5' into 10.6
* [Revision #811614d412](https://github.com/MariaDB/server/commit/811614d412)\
  2024-07-19 22:57:51 +0000
  * [MDEV-34625](https://jira.mariadb.org/browse/MDEV-34625) Fix undefined behavior of using uninitialized member variables
* [Revision #ee5f7692d7](https://github.com/MariaDB/server/commit/ee5f7692d7)\
  2024-07-23 17:37:34 +0530
  * [MDEV-34357](https://jira.mariadb.org/browse/MDEV-34357) InnoDB: Assertion failure in file ./storage/innobase/page/page0zip.cc line 4211
* [Revision #4bf7c966b3](https://github.com/MariaDB/server/commit/4bf7c966b3)\
  2024-07-27 13:34:26 +0300
  * [MDEV-34664](https://jira.mariadb.org/browse/MDEV-34664): Add an option to fix InnoDB's doubling of secondary index cardinalities
* [Revision #3359ac09a4](https://github.com/MariaDB/server/commit/3359ac09a4)\
  2024-07-23 21:35:27 +0530
  * [MDEV-34066](https://jira.mariadb.org/browse/MDEV-34066) Output of SHOW ENGINE INNODB STATUS uses the nanoseconds suffix for microseconds
* [Revision #216fdb1556](https://github.com/MariaDB/server/commit/216fdb1556)\
  2024-07-17 14:03:19 -0400
  * [MDEV-33971](https://jira.mariadb.org/browse/MDEV-33971) fix --view-protocol test failure
* Merge [Revision #a938503cfb](https://github.com/MariaDB/server/commit/a938503cfb) 2024-07-20 08:12:42 +0200 - Merge branch '10.5' into 10.6
* [Revision #a94fd87420](https://github.com/MariaDB/server/commit/a94fd87420)\
  2024-07-19 13:46:35 +0200
  * New CC 3.3
* Merge [Revision #9af2caca33](https://github.com/MariaDB/server/commit/9af2caca33) 2024-07-18 16:25:33 +0200 - Merge branch '10.5' into 10.6
* [Revision #e644e130b0](https://github.com/MariaDB/server/commit/e644e130b0)\
  2024-07-16 12:43:53 +0300
  * [MDEV-30623](https://jira.mariadb.org/browse/MDEV-30623): Fix the testcase
* Merge [Revision #f071b7620b](https://github.com/MariaDB/server/commit/f071b7620b) 2024-07-16 15:54:22 +0800 - Merge branch '10.5' into 10.6
* [Revision #6264950c4f](https://github.com/MariaDB/server/commit/6264950c4f)\
  2024-03-06 14:55:44 +0100
  * Small cleanup of replication code (log.cc)
* [Revision #0802e5a7eb](https://github.com/MariaDB/server/commit/0802e5a7eb)\
  2024-07-13 04:38:10 +0200
  * [MDEV-34505](https://jira.mariadb.org/browse/MDEV-34505): galera.mariadb\_tzinfo\_to\_sql fails deterministically on Ubuntu 24.04
* [Revision #02e38e2ece](https://github.com/MariaDB/server/commit/02e38e2ece)\
  2024-04-26 12:13:31 -0400
  * [MDEV-33971](https://jira.mariadb.org/browse/MDEV-33971) NAME\_CONST in WHERE clause replaced by inner item
* Merge [Revision #a0a7b1c128](https://github.com/MariaDB/server/commit/a0a7b1c128) 2024-07-10 18:28:06 +0200 - Merge 10.5 into 10.6
* Merge [Revision #d9ffefdaac](https://github.com/MariaDB/server/commit/d9ffefdaac) 2024-07-10 14:57:28 +0530 - Merge 10.5 into 10.6
* Merge [Revision #4026f04425](https://github.com/MariaDB/server/commit/4026f04425) 2024-07-09 11:51:46 +0200 - Merge branch 10.5 into 10.6
* [Revision #b418b60ebf](https://github.com/MariaDB/server/commit/b418b60ebf)\
  2024-06-19 12:56:45 +1100
  * [MDEV-30623](https://jira.mariadb.org/browse/MDEV-30623) JSON\_TABLE in subquery not correctly marked as correlated
* Merge [Revision #e56040fee8](https://github.com/MariaDB/server/commit/e56040fee8) 2024-07-08 18:52:21 +0400 - Merge remote-tracking branch 'origin/10.5' into 10.6
* [Revision #eb4458e993](https://github.com/MariaDB/server/commit/eb4458e993)\
  2024-02-29 11:51:09 -0700
  * [MDEV-33465](https://jira.mariadb.org/browse/MDEV-33465): an option to enable semisync recovery
* [Revision #e40d232ad6](https://github.com/MariaDB/server/commit/e40d232ad6)\
  2024-06-21 12:30:02 +0300
  * Stabilize analyze\_engine\_stats2.test
* [Revision #513c827041](https://github.com/MariaDB/server/commit/513c827041)\
  2024-05-27 17:00:12 +0300
  * [MDEV-34190](https://jira.mariadb.org/browse/MDEV-34190): r\_engine\_stats.pages\_read\_count is unrealistically low
* [Revision #8ed3c37592](https://github.com/MariaDB/server/commit/8ed3c37592)\
  2024-07-04 09:27:30 +0200
  * Make PROTECT\_STATEMENT\_MEMROOT default for version less then 11.2
* [Revision #d58975bbef](https://github.com/MariaDB/server/commit/d58975bbef)\
  2024-07-03 14:10:01 -0600
  * [MDEV-9159](https://jira.mariadb.org/browse/MDEV-9159): Bring back assert in semisync\_master.cc
* [Revision #73ad436e16](https://github.com/MariaDB/server/commit/73ad436e16)\
  2024-07-03 11:07:13 +0530
  * [MDEV-34458](https://jira.mariadb.org/browse/MDEV-34458) wait\_for\_read in buf\_page\_get\_low hurts performance
* Merge [Revision #dcd8a64892](https://github.com/MariaDB/server/commit/dcd8a64892) 2024-07-03 13:27:23 +0200 - Merge branch '10.5' into 10.6
* [Revision #f6fcfc1a6a](https://github.com/MariaDB/server/commit/f6fcfc1a6a)\
  2024-06-20 12:34:55 +0300
  * [MDEV-33064](https://jira.mariadb.org/browse/MDEV-33064) amendment: replace trx->wsrep=0 with an assert in trx\_rollback\_for\_mysql()
* [Revision #cfbd57dfb7](https://github.com/MariaDB/server/commit/cfbd57dfb7)\
  2023-12-25 13:59:07 +0300
  * [MDEV-33064](https://jira.mariadb.org/browse/MDEV-33064): Sync trx->wsrep state from THD on trx start
* [Revision #d472391471](https://github.com/MariaDB/server/commit/d472391471)\
  2024-06-29 14:44:05 +1000
  * tpool: correct LIBAIO\_REQIRED typo
* [Revision #d1ecf5cc5f](https://github.com/MariaDB/server/commit/d1ecf5cc5f)\
  2024-06-28 15:57:07 +0300
  * [MDEV-32176](https://jira.mariadb.org/browse/MDEV-32176) Contention in ha\_innobase::info\_low()
* [Revision #c9212b7a43](https://github.com/MariaDB/server/commit/c9212b7a43)\
  2024-06-26 11:08:56 +0800
  * [MDEV-33746](https://jira.mariadb.org/browse/MDEV-33746) \[fixup] Add suggested overrides in mroonga
* Merge [Revision #d7042ec4da](https://github.com/MariaDB/server/commit/d7042ec4da) 2024-06-26 09:16:54 +0800 - Merge branch '10.5' into 10.6
* Merge [Revision #0076eb3d4e](https://github.com/MariaDB/server/commit/0076eb3d4e) 2024-06-24 13:09:47 +0300 - Merge 10.5 into 10.6
* [Revision #49b4a6e26d](https://github.com/MariaDB/server/commit/49b4a6e26d)\
  2024-06-21 10:52:09 +0300
  * Fix the testcase for [MDEV-31558](https://jira.mariadb.org/browse/MDEV-31558): log\_slow\_verbosity\_innodb
* [Revision #0a199cb810](https://github.com/MariaDB/server/commit/0a199cb810)\
  2024-06-20 11:59:06 +0300
  * [MDEV-34108](https://jira.mariadb.org/browse/MDEV-34108) Inappropriate semi-consistent read in RC if innodb\_snapshot\_isolation=ON
* [Revision #279aa1e6b4](https://github.com/MariaDB/server/commit/279aa1e6b4)\
  2024-06-12 12:27:55 +0300
  * Disable new connections in case of fatal signal
* [Revision #3541bd63f0](https://github.com/MariaDB/server/commit/3541bd63f0)\
  2024-05-15 12:20:27 +0300
  * [MDEV-33582](https://jira.mariadb.org/browse/MDEV-33582) Add more warnings to be able to better diagnose network issues
* [Revision #6c2cd4cf56](https://github.com/MariaDB/server/commit/6c2cd4cf56)\
  2024-06-19 17:06:00 +0200
  * [MDEV-34428](https://jira.mariadb.org/browse/MDEV-34428) bootstrap can't delete tempfile, it is already gone
* [Revision #6382339144](https://github.com/MariaDB/server/commit/6382339144)\
  2024-06-16 14:01:36 +0300
  * [MDEV-34311](https://jira.mariadb.org/browse/MDEV-34311): Alter USER should reset all account limit counters
* [Revision #2d8d813941](https://github.com/MariaDB/server/commit/2d8d813941)\
  2024-06-16 14:00:39 +0300
  * cleanup, refactor
* [Revision #5d49a2add7](https://github.com/MariaDB/server/commit/5d49a2add7)\
  2024-05-15 17:42:08 +0300
  * [MDEV-33935](https://jira.mariadb.org/browse/MDEV-33935) fix deadlock counter
* [Revision #ee974ca5e0](https://github.com/MariaDB/server/commit/ee974ca5e0)\
  2024-05-13 08:55:36 +0300
  * [MDEV-31658](https://jira.mariadb.org/browse/MDEV-31658) : Deadlock found when trying to get lock during applying
* [Revision #5b26a07698](https://github.com/MariaDB/server/commit/5b26a07698)\
  2024-06-19 13:41:11 +0300
  * [MDEV-34178](https://jira.mariadb.org/browse/MDEV-34178): Enable spinloop for index\_lock
* [Revision #f8d213bd0e](https://github.com/MariaDB/server/commit/f8d213bd0e)\
  2024-06-19 13:40:57 +0300
  * [MDEV-34178](https://jira.mariadb.org/browse/MDEV-34178): Improve the spin loops
* [Revision #6cde03aedc](https://github.com/MariaDB/server/commit/6cde03aedc)\
  2024-06-19 13:30:23 +0300
  * [MDEV-34178](https://jira.mariadb.org/browse/MDEV-34178): Improve PERFORMANCE\_SCHEMA instrumentation
* [Revision #2bd661ca10](https://github.com/MariaDB/server/commit/2bd661ca10)\
  2024-06-18 18:22:28 +0300
  * [MDEV-34178](https://jira.mariadb.org/browse/MDEV-34178): Simplify the U lock
* [Revision #83d3ed4908](https://github.com/MariaDB/server/commit/83d3ed4908)\
  2024-06-17 15:41:46 +0400
  * [MDEV-34014](https://jira.mariadb.org/browse/MDEV-34014) mysql\_upgrade failed
* [Revision #ef9e3e73ed](https://github.com/MariaDB/server/commit/ef9e3e73ed)\
  2024-06-11 16:20:00 +0300
  * [MDEV-30651](https://jira.mariadb.org/browse/MDEV-30651): Assertion \`sel->quick' in make\_range\_rowid\_filters
* Merge [Revision #e60acae655](https://github.com/MariaDB/server/commit/e60acae655) 2024-06-17 08:40:07 +0300 - Merge 10.5 into 10.6
* Merge [Revision #32202c30bc](https://github.com/MariaDB/server/commit/32202c30bc) 2024-06-13 19:58:11 +0300 - Merge 10.5 into 10.6
* [Revision #c849952b71](https://github.com/MariaDB/server/commit/c849952b71)\
  2024-06-13 19:57:40 +0300
  * [MDEV-33840](https://jira.mariadb.org/browse/MDEV-33840): Fix GCC -Wreorder
* Merge [Revision #fc9005adc4](https://github.com/MariaDB/server/commit/fc9005adc4) 2024-06-12 07:51:28 +0300 - Merge 10.5 into 10.6
* [Revision #fcd21d3e40](https://github.com/MariaDB/server/commit/fcd21d3e40)\
  2024-06-10 12:27:18 -0600
  * [MDEV-34355](https://jira.mariadb.org/browse/MDEV-34355): rpl.rpl\_semi\_sync\_no\_missed\_ack\_after\_add\_slave ‘server\_3 should have sent…’
* Merge [Revision #27834ebc91](https://github.com/MariaDB/server/commit/27834ebc91) 2024-06-10 15:22:15 +0300 - Merge 10.5 into 10.6
* Merge [Revision #a687cf8661](https://github.com/MariaDB/server/commit/a687cf8661) 2024-06-07 10:03:51 +0300 - Merge 10.5 into 10.6
* [Revision #699d38d951](https://github.com/MariaDB/server/commit/699d38d951)\
  2024-06-06 14:38:42 +0300
  * [MDEV-34296](https://jira.mariadb.org/browse/MDEV-34296) extern thread\_local is a CPU waste
* [Revision #9fac857f26](https://github.com/MariaDB/server/commit/9fac857f26)\
  2024-06-06 13:03:34 +0300
  * [MDEV-34283](https://jira.mariadb.org/browse/MDEV-34283) A misplaced btr\_cur\_need\_opposite\_intention() check may fail to prevent hangs
* [Revision #bc3660925d](https://github.com/MariaDB/server/commit/bc3660925d)\
  2024-06-06 10:18:42 +0300
  * [MDEV-34307](https://jira.mariadb.org/browse/MDEV-34307) On startup, \[FATAL] InnoDB: Page ... still fixed or dirty
* [Revision #b12c14e3b4](https://github.com/MariaDB/server/commit/b12c14e3b4)\
  2024-05-30 17:14:01 +0530
  * [MDEV-34265](https://jira.mariadb.org/browse/MDEV-34265) Possible hang during IO burst with innodb\_flush\_sync enabled
* [Revision #b204817986](https://github.com/MariaDB/server/commit/b204817986)\
  2024-05-30 10:45:58 +0300
  * [MDEV-34261](https://jira.mariadb.org/browse/MDEV-34261): Detect if build is running under 32-bit container
* [Revision #58a0e1e3dd](https://github.com/MariaDB/server/commit/58a0e1e3dd)\
  2024-06-03 14:01:42 +0530
  * [MDEV-34223](https://jira.mariadb.org/browse/MDEV-34223) Innodb - add status variable for number of bulk inserts
* Merge [Revision #f2302a62e3](https://github.com/MariaDB/server/commit/f2302a62e3) 2024-05-31 09:10:17 +1000 - Merge branch '10.5' into 10.6
* Merge [Revision #5ba542e9ee](https://github.com/MariaDB/server/commit/5ba542e9ee) 2024-05-30 14:27:07 +0300 - Merge 10.5 into 10.6
* [Revision #36ab6cc80c](https://github.com/MariaDB/server/commit/36ab6cc80c)\
  2024-05-12 19:10:47 +0300
  * [MDEV-34125](https://jira.mariadb.org/browse/MDEV-34125): ANALYZE FORMAT=JSON: r\_engine\_stats.pages\_read\_time\_ms has wrong scale
* [Revision #2d5cba22a9](https://github.com/MariaDB/server/commit/2d5cba22a9)\
  2024-05-16 13:10:44 +0530
  * [MDEV-34167](https://jira.mariadb.org/browse/MDEV-34167) We fail to terminate transaction early with ER\_LOCK\_TABLE\_FULL when lock memory is growing
* [Revision #8047c8bc71](https://github.com/MariaDB/server/commit/8047c8bc71)\
  2024-05-15 19:47:56 +0530
  * [MDEV-28800](https://jira.mariadb.org/browse/MDEV-28800) SIGABRT due to running out of memory for InnoDB locks
* [Revision #9a95f6b53b](https://github.com/MariaDB/server/commit/9a95f6b53b)\
  2024-05-15 10:53:41 -0400
  * bump the VERSION
* [Revision #5e6c122427](https://github.com/MariaDB/server/commit/5e6c122427)\
  2024-05-06 20:10:06 +0700
  * [MDEV-33769](https://jira.mariadb.org/browse/MDEV-33769): Memory leak found in the test main.rownum run with --ps-protocol against a server built with the option -DWITH\_PROTECT\_STATEMENT\_MEMROOT
* [Revision #6bf2b64a97](https://github.com/MariaDB/server/commit/6bf2b64a97)\
  2024-05-10 12:49:16 +0300
  * [MDEV-34118](https://jira.mariadb.org/browse/MDEV-34118) fsp\_alloc\_free\_extent() fails to flag DB\_OUT\_OF\_FILE\_SPACE

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
