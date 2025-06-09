# MariaDB 10.6.17 Changelog

The most recent release of [MariaDB 10.6](../../mariadb-community-server-release-notes/mariadb-10-6-series/what-is-mariadb-106.md) is:[**MariaDB 10.6.21**](../../mariadb-community-server-release-notes/mariadb-10-6-series/mariadb-10-6-21-release-notes.md) Stable (GA) [Download Now](https://mariadb.com/downloads/)[_Alternate download from mariadb.org_](https://downloads.mariadb.org/mariadb/10.6.21/)

[Download 10.6.17](https://downloads.mariadb.org/mariadb/10.6.17/)[Release Notes](../../mariadb-community-server-release-notes/mariadb-10-6-series/mariadb-10-6-17-release-notes.md)[Changelog](mariadb-10-6-17-changelog.md)[Overview of 10.6](../../mariadb-community-server-release-notes/mariadb-10-6-series/what-is-mariadb-106.md)

**Release date:** 7 Feb 2024

For the highlights of this release, see the[release notes](../../mariadb-community-server-release-notes/mariadb-10-6-series/mariadb-10-6-17-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/server/tree/10.6) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Includes all fixes from [MariaDB 10.5.24](../changelogs-mariadb-105-series/mariadb-10-5-24-changelog.md)
* [Revision #15c75ad083](https://github.com/MariaDB/server/commit/15c75ad083)\
  2024-02-01 11:26:36 +0100
  * pcre.cmake: always check the library with check\_library\_exists()
* [Revision #2278f3503e](https://github.com/MariaDB/server/commit/2278f3503e)\
  2024-01-31 22:02:59 +0100
  * fix columnstore compilation on fc39
* Merge [Revision #3f6038bc51](https://github.com/MariaDB/server/commit/3f6038bc51) 2024-01-31 17:51:58 +0100 - Merge branch '10.5' into 10.6
* [Revision #4dbf55bbfc](https://github.com/MariaDB/server/commit/4dbf55bbfc)\
  2024-01-27 16:47:00 +0200
  * Disable perfschema.misc\_session\_status for 32 bit
* [Revision #ed76a2e8ac](https://github.com/MariaDB/server/commit/ed76a2e8ac)\
  2024-01-27 16:32:49 +0200
  * Updated some 32 bit result files in sys\_vars
* [Revision #e20693c167](https://github.com/MariaDB/server/commit/e20693c167)\
  2024-01-27 16:29:16 +0200
  * Fixed some wrong printf() usage after changing m\_table\_id to ulonglong
* [Revision #daca0c059b](https://github.com/MariaDB/server/commit/daca0c059b)\
  2024-01-26 12:24:50 +0530
  * fix failing test on buildbot for [MDEV-27087](https://jira.mariadb.org/browse/MDEV-27087)
* [Revision #220c0fb405](https://github.com/MariaDB/server/commit/220c0fb405)\
  2024-01-26 11:21:14 +0200
  * [MDEV-33317](https://jira.mariadb.org/browse/MDEV-33317) \[Warning] InnoDB: Could not free any blocks in the buffer pool!
* [Revision #c9c4f15e99](https://github.com/MariaDB/server/commit/c9c4f15e99)\
  2024-01-25 14:44:42 +0100
  * Remove bogus "perl not found" on Windows.
* [Revision #9d88c5b8b4](https://github.com/MariaDB/server/commit/9d88c5b8b4)\
  2024-01-23 23:56:40 +0400
  * [MDEV-31616](https://jira.mariadb.org/browse/MDEV-31616) Problems with a stored function EMPTY() on upgrade to 10.6.
* [Revision #011d666ada](https://github.com/MariaDB/server/commit/011d666ada)\
  2024-01-23 20:53:52 +0530
  * reorder the log columns for [MDEV-27087](https://jira.mariadb.org/browse/MDEV-27087)
* [Revision #26c86c39fc](https://github.com/MariaDB/server/commit/26c86c39fc)\
  2024-01-21 19:10:37 +0200
  * Fixed some mtr tests that failed on windows
* [Revision #6085fb199a](https://github.com/MariaDB/server/commit/6085fb199a)\
  2024-01-21 16:52:19 +0200
  * Fixed compiler error/warning in backup\_copy.cc
* [Revision #286d6f239a](https://github.com/MariaDB/server/commit/286d6f239a)\
  2024-01-20 17:41:33 +0200
  * Fixed main.strict test to work with icc compiler
* [Revision #d2c431bccb](https://github.com/MariaDB/server/commit/d2c431bccb)\
  2024-01-20 17:09:38 +0200
  * Disable main.gis from embedded
* [Revision #c777429cf9](https://github.com/MariaDB/server/commit/c777429cf9)\
  2024-01-19 12:01:28 +0200
  * [MDEV-33279](https://jira.mariadb.org/browse/MDEV-33279) Disable transparent huge pages after page buffers has been allocatedDisable transparent huge pages (THP)
* [Revision #740d3e7a74](https://github.com/MariaDB/server/commit/740d3e7a74)\
  2024-01-05 15:29:07 +0200
  * Trivial fixes:
* [Revision #3c63e2f890](https://github.com/MariaDB/server/commit/3c63e2f890)\
  2023-12-27 19:58:59 +0200
  * Temporary table name used by multip-update has 'null' as part of the name
* [Revision #6f65e08277](https://github.com/MariaDB/server/commit/6f65e08277)\
  2023-12-22 13:53:57 +0200
  * [MDEV-33118](https://jira.mariadb.org/browse/MDEV-33118) optimizer\_adjust\_secondary\_key\_costs variable
* [Revision #c49fd90263](https://github.com/MariaDB/server/commit/c49fd90263)\
  2023-12-21 18:25:39 +0200
  * Ensure keyread\_tmp variable is assigned.
* [Revision #2fcb5d651b](https://github.com/MariaDB/server/commit/2fcb5d651b)\
  2023-12-12 15:26:04 +0200
  * Fixed possible mutex-wrong-order with KILL USER
* [Revision #1ca813bf76](https://github.com/MariaDB/server/commit/1ca813bf76)\
  2023-12-25 15:30:03 +0200
  * Added socketpair.c as a replacement for 'pipe()' call for Windows.
* [Revision #7af50e4df4](https://github.com/MariaDB/server/commit/7af50e4df4)\
  2023-11-08 16:57:58 -0700
  * [MDEV-32551](https://jira.mariadb.org/browse/MDEV-32551): "Read semi-sync reply magic number error" warnings on master
* [Revision #ee7cc0a466](https://github.com/MariaDB/server/commit/ee7cc0a466)\
  2024-01-09 15:19:29 +0530
  * [MDEV-32906](https://jira.mariadb.org/browse/MDEV-32906): The SQL error plugin prints (null) as database if the mariadb client is not using any database to execute the SQL.
* [Revision #90cd712b84](https://github.com/MariaDB/server/commit/90cd712b84)\
  2023-11-13 23:21:49 +0530
  * [MDEV-27087](https://jira.mariadb.org/browse/MDEV-27087): Add thread ID and database / table, where the error occured to SQL error plugin
* Merge [Revision #4ef9c9bb75](https://github.com/MariaDB/server/commit/4ef9c9bb75) 2024-01-23 15:25:42 +1100 - Merge remote-tracking branch 10.5 into 10.6
* [Revision #19f3796ec3](https://github.com/MariaDB/server/commit/19f3796ec3)\
  2024-01-22 15:57:05 +0100
  * new CC 3.3
* [Revision #495e7f1b3d](https://github.com/MariaDB/server/commit/495e7f1b3d)\
  2024-01-22 08:24:08 +0200
  * [MDEV-33053](https://jira.mariadb.org/browse/MDEV-33053) fixup: Correct a condition before a message
* Merge [Revision #5c243d4caf](https://github.com/MariaDB/server/commit/5c243d4caf) 2024-01-22 08:20:08 +0200 - Merge 10.5 into 10.6
* [Revision #e237925963](https://github.com/MariaDB/server/commit/e237925963)\
  2024-01-22 08:19:00 +0200
  * [MDEV-33031](https://jira.mariadb.org/browse/MDEV-33031) test fixup for HAVE\_PERFSCHEMA=NO
* [Revision #0c23f84d8d](https://github.com/MariaDB/server/commit/0c23f84d8d)\
  2023-12-11 10:15:55 +1100
  * [MDEV-32983](https://jira.mariadb.org/browse/MDEV-32983) cosmetic improvement on path separator near ib\_buffer\_pool
* [Revision #3a33ae8601](https://github.com/MariaDB/server/commit/3a33ae8601)\
  2024-01-12 16:57:37 +0100
  * [MDEV-33091](https://jira.mariadb.org/browse/MDEV-33091) pcre2 headers aren't found on Solaris
* [Revision #21560bee9d](https://github.com/MariaDB/server/commit/21560bee9d)\
  2024-01-19 12:46:11 +0200
  * Revert "[MDEV-32899](https://jira.mariadb.org/browse/MDEV-32899) InnoDB is holding shared dict\_sys.latch while waiting for FOREIGN KEY child table lock on DDL"
* [Revision #7e65e3027e](https://github.com/MariaDB/server/commit/7e65e3027e)\
  2024-01-19 12:40:32 +0200
  * [MDEV-33275](https://jira.mariadb.org/browse/MDEV-33275) buf\_flush\_LRU(): mysql\_mutex\_assert\_owner(\&buf\_pool.mutex) failed
* [Revision #d34479dc66](https://github.com/MariaDB/server/commit/d34479dc66)\
  2024-01-19 12:40:16 +0200
  * [MDEV-33053](https://jira.mariadb.org/browse/MDEV-33053) InnoDB LRU flushing does not run before running out of buffer pool
* [Revision #16f2f8e5a7](https://github.com/MariaDB/server/commit/16f2f8e5a7)\
  2024-01-17 20:32:51 +0100
  * new CC 3.3
* [Revision #82e8633420](https://github.com/MariaDB/server/commit/82e8633420)\
  2024-01-19 15:24:19 +1100
  * innodb: IO Error message missing space
* [Revision #a6290a5bc5](https://github.com/MariaDB/server/commit/a6290a5bc5)\
  2024-01-15 09:04:19 +0200
  * [MDEV-33095](https://jira.mariadb.org/browse/MDEV-33095) innodb\_flush\_method=O\_DIRECT creates excessive errors on Solaris
* [Revision #f63045b119](https://github.com/MariaDB/server/commit/f63045b119)\
  2024-01-18 10:14:21 +0200
  * [MDEV-33213](https://jira.mariadb.org/browse/MDEV-33213) fixup: GCC 5 -Wconversion
* Merge [Revision #3a96eba25f](https://github.com/MariaDB/server/commit/3a96eba25f) 2024-01-17 13:35:05 +0200 - Merge 10.5 into 10.6
* [Revision #6a514ef672](https://github.com/MariaDB/server/commit/6a514ef672)\
  2024-01-17 12:50:44 +0200
  * [MDEV-30940](https://jira.mariadb.org/browse/MDEV-30940): Try to fix the test
* [Revision #f8c88d905b](https://github.com/MariaDB/server/commit/f8c88d905b)\
  2024-01-17 11:14:24 +0200
  * [MDEV-33213](https://jira.mariadb.org/browse/MDEV-33213) History list is not shrunk unless there is a pause in the workload
* [Revision #931df937e9](https://github.com/MariaDB/server/commit/931df937e9)\
  2024-01-16 17:17:50 +1100
  * [MDEV-32559](https://jira.mariadb.org/browse/MDEV-32559) failing spider signal\_ddl\_recovery\_done callback should result in spider deinit
* Merge [Revision #d06b6de305](https://github.com/MariaDB/server/commit/d06b6de305) 2024-01-11 12:59:22 +1100 - Merge branch '10.5' into 10.6
* [Revision #3613fb2aa8](https://github.com/MariaDB/server/commit/3613fb2aa8)\
  2024-01-10 11:53:00 +0200
  * [MDEV-33112](https://jira.mariadb.org/browse/MDEV-33112) innodb\_undo\_log\_truncate=ON is blocking page write
* [Revision #593278f927](https://github.com/MariaDB/server/commit/593278f927)\
  2024-01-10 11:52:26 +0200
  * [MDEV-32050](https://jira.mariadb.org/browse/MDEV-32050) fixup: Remove srv\_purge\_rseg\_truncate\_frequency
* [Revision #4cbf75dd33](https://github.com/MariaDB/server/commit/4cbf75dd33)\
  2024-01-10 07:51:37 +0200
  * [MDEV-33137](https://jira.mariadb.org/browse/MDEV-33137): Assertion end\_lsn == page\_lsn failed in recv\_recover\_page
* [Revision #c6c2a2b8d4](https://github.com/MariaDB/server/commit/c6c2a2b8d4)\
  2024-01-02 22:23:26 +0100
  * [MDEV-33150](https://jira.mariadb.org/browse/MDEV-33150) double-locking of LOCK\_thd\_kill in performance\_schema.session\_status
* [Revision #0a122637b5](https://github.com/MariaDB/server/commit/0a122637b5)\
  2024-01-09 15:54:36 +0100
  * cleanup: change a function, that always return 0, to void
* [Revision #23e107d751](https://github.com/MariaDB/server/commit/23e107d751)\
  2023-12-28 15:23:40 +0100
  * [MDEV-33031](https://jira.mariadb.org/browse/MDEV-33031) Assertion failure upon reading from performance schema with binlog enabled
* [Revision #b3065af6e6](https://github.com/MariaDB/server/commit/b3065af6e6)\
  2023-12-28 15:19:42 +0100
  * cleanup: spider status variables
* [Revision #c44cac91ab](https://github.com/MariaDB/server/commit/c44cac91ab)\
  2023-12-27 17:04:43 +0100
  * [MDEV-33031](https://jira.mariadb.org/browse/MDEV-33031) Assertion failure upon reading from performance schema with binlog enabled
* [Revision #022ae42155](https://github.com/MariaDB/server/commit/022ae42155)\
  2023-12-14 15:17:59 +0100
  * [MDEV-11777](https://jira.mariadb.org/browse/MDEV-11777) REGEXP\_REPLACE converts utf8mb4 supplementary characters to '?'
* Merge [Revision #6538a91e94](https://github.com/MariaDB/server/commit/6538a91e94) 2024-01-08 14:39:56 +0200 - Merge 10.5 into 10.6
* Merge [Revision #8bd5a3de7f](https://github.com/MariaDB/server/commit/8bd5a3de7f) 2024-01-03 14:24:47 +0200 - Merge 10.5 into 10.6
* Merge [Revision #e23c695250](https://github.com/MariaDB/server/commit/e23c695250) 2024-01-02 17:37:58 +0200 - Merge 10.5 into 10.6
* [Revision #9f40f02a8d](https://github.com/MariaDB/server/commit/9f40f02a8d)\
  2023-12-22 17:55:30 +0100
  * Fix galera.galera\_kill\_ddl test errors in debug mode.
* [Revision #bdaa6bac05](https://github.com/MariaDB/server/commit/bdaa6bac05)\
  2023-12-22 14:17:26 +1100
  * \[fixup] Spider: correct init queries after merge
* [Revision #91d53ea339](https://github.com/MariaDB/server/commit/91d53ea339)\
  2023-12-12 11:01:54 +0200
  * [MDEV-33000](https://jira.mariadb.org/browse/MDEV-33000): Fix test result file on some test cases
* [Revision #a31598b3b1](https://github.com/MariaDB/server/commit/a31598b3b1)\
  2023-12-21 16:00:12 +0100
  * [MDEV-33046](https://jira.mariadb.org/browse/MDEV-33046) - reschedule dict\_stats\_func() if there work left to do.
* [Revision #91a118d55e](https://github.com/MariaDB/server/commit/91a118d55e)\
  2023-12-21 15:09:03 +0100
  * Cleanup - reuse background THD in dict\_stats\_func()
* Merge [Revision #8e6a476be1](https://github.com/MariaDB/server/commit/8e6a476be1) 2023-12-21 21:33:01 +0100 - Merge branch '10.5' into 10.6
* [Revision #c1cc264f12](https://github.com/MariaDB/server/commit/c1cc264f12)\
  2023-12-21 18:24:19 +0200
  * Fix an intermittent test failure
* [Revision #cf86e075c0](https://github.com/MariaDB/server/commit/cf86e075c0)\
  2023-12-21 12:58:39 +0200
  * Add an end-of-test marker
* Merge [Revision #a81a138aab](https://github.com/MariaDB/server/commit/a81a138aab) 2023-12-21 12:16:33 +0200 - Merge 10.5 into 10.6
* [Revision #f9ae553067](https://github.com/MariaDB/server/commit/f9ae553067)\
  2023-12-20 15:56:00 +0200
  * [MDEV-33098](https://jira.mariadb.org/browse/MDEV-33098): Disable the test
* Merge [Revision #2b01e5103d](https://github.com/MariaDB/server/commit/2b01e5103d) 2023-12-19 18:41:42 +0200 - Merge 10.5 into 10.6
* [Revision #98287bd2d6](https://github.com/MariaDB/server/commit/98287bd2d6)\
  2023-12-19 11:15:08 +0200
  * [MDEV-33009](https://jira.mariadb.org/browse/MDEV-33009) Server hangs for a long time with innodb\_undo\_log\_truncate=ON
* [Revision #aff5ed3988](https://github.com/MariaDB/server/commit/aff5ed3988)\
  2023-12-16 19:46:58 +0100
  * [MDEV-33046](https://jira.mariadb.org/browse/MDEV-33046) race condition in InnoDB dict\_stats\_schedule()
* [Revision #0930eb86cb](https://github.com/MariaDB/server/commit/0930eb86cb)\
  2023-12-15 19:58:31 +0100
  * Spider cannot run DDL (e.g. create tables) before ddl recovery
* Merge [Revision #e95bba9c58](https://github.com/MariaDB/server/commit/e95bba9c58) 2023-12-15 20:00:58 +0100 - Merge branch '10.5' into 10.6
* [Revision #686865e112](https://github.com/MariaDB/server/commit/686865e112)\
  2023-12-15 15:29:26 +0530
  * Adjust the [MDEV-26052](https://jira.mariadb.org/browse/MDEV-26052) test case for [MDEV-29092](https://jira.mariadb.org/browse/MDEV-29092)
* [Revision #655f78a238](https://github.com/MariaDB/server/commit/655f78a238)\
  2023-12-14 15:24:19 +0200
  * [MDEV-18322](https://jira.mariadb.org/browse/MDEV-18322) Assertion "wrong page type" on instant ALTER TABLE
* [Revision #f21a6cbf6e](https://github.com/MariaDB/server/commit/f21a6cbf6e)\
  2023-12-14 13:16:28 +0200
  * [MDEV-32939](https://jira.mariadb.org/browse/MDEV-32939) If tables are frequently created, renamed, dropped, a backup cannot be restored
* [Revision #0f510d8b5a](https://github.com/MariaDB/server/commit/0f510d8b5a)\
  2023-12-14 13:15:51 +0200
  * [MDEV-32751](https://jira.mariadb.org/browse/MDEV-32751) fixup: cmake -DPLUGIN\_PERFSCHEMA=NO
* [Revision #736a54f49c](https://github.com/MariaDB/server/commit/736a54f49c)\
  2023-12-13 00:37:57 +0100
  * perfschema: use LOCK\_thd\_kill to "keep THD during materialization"
* [Revision #d9cb1a2b7e](https://github.com/MariaDB/server/commit/d9cb1a2b7e)\
  2023-11-24 17:45:16 +0100
  * [MDEV-32751](https://jira.mariadb.org/browse/MDEV-32751) sys schema view session\_ssl\_status is empty
* [Revision #4231cf6d3f](https://github.com/MariaDB/server/commit/4231cf6d3f)\
  2023-11-08 15:44:18 +0100
  * [MDEV-32617](https://jira.mariadb.org/browse/MDEV-32617) deprecate secure\_auth=0
* [Revision #c2a5d93580](https://github.com/MariaDB/server/commit/c2a5d93580)\
  2023-11-21 12:01:31 +0100
  * main.long\_host failures
* [Revision #bb565ee566](https://github.com/MariaDB/server/commit/bb565ee566)\
  2023-12-10 10:53:27 +0100
  * [MDEV-32884](https://jira.mariadb.org/browse/MDEV-32884) backward compatibility fixes
* [Revision #47f2b16a8c](https://github.com/MariaDB/server/commit/47f2b16a8c)\
  2023-12-07 20:16:41 +0700
  * [MDEV-31296](https://jira.mariadb.org/browse/MDEV-31296): Crash in Item\_func::fix\_fields when prepared statement with subqueries and window function is executed with sql\_mode = ONLY\_FULL\_GROUP\_BY
* [Revision #4ced4898fd](https://github.com/MariaDB/server/commit/4ced4898fd)\
  2023-12-07 17:44:43 +0400
  * [MDEV-32958](https://jira.mariadb.org/browse/MDEV-32958) Unusable key notes do not get reported for some operations
* [Revision #bc5e904043](https://github.com/MariaDB/server/commit/bc5e904043)\
  2023-12-07 11:47:45 +0000
  * [MDEV-32884](https://jira.mariadb.org/browse/MDEV-32884) Improve S3 options comaptibility
* [Revision #ecbdd72953](https://github.com/MariaDB/server/commit/ecbdd72953)\
  2023-12-06 16:18:53 +0400
  * [MDEV-32957](https://jira.mariadb.org/browse/MDEV-32957) Unusable key notes report wrong predicates for > and >=
* [Revision #f074223ae7](https://github.com/MariaDB/server/commit/f074223ae7)\
  2023-12-05 12:31:29 +0200
  * [MDEV-32068](https://jira.mariadb.org/browse/MDEV-32068) Some calls to buf\_read\_ahead\_linear() seem to be useless
* [Revision #768a736174](https://github.com/MariaDB/server/commit/768a736174)\
  2023-12-04 11:47:19 +0200
  * [MDEV-32899](https://jira.mariadb.org/browse/MDEV-32899) instrumentation fixup
* [Revision #1ac03fd914](https://github.com/MariaDB/server/commit/1ac03fd914)\
  2023-12-04 11:21:58 +0200
  * Fix occasional failure of encryption.corrupted\_during\_recovery
* [Revision #be1c4bd1bd](https://github.com/MariaDB/server/commit/be1c4bd1bd)\
  2023-12-04 11:17:46 +0200
  * Fix occasional failure of innodb.innodb-alter-tempfile
* [Revision #99cab7ee57](https://github.com/MariaDB/server/commit/99cab7ee57)\
  2023-11-29 14:36:03 +1100
  * [MDEV-32903](https://jira.mariadb.org/browse/MDEV-32903) [MDEV-32532](https://jira.mariadb.org/browse/MDEV-32532) Assertion failure in ddl\_log\_increment\_phase\_no\_lock upon ..
* [Revision #4bd94afbd3](https://github.com/MariaDB/server/commit/4bd94afbd3)\
  2023-11-26 11:53:12 +0200
  * [MDEV-32884](https://jira.mariadb.org/browse/MDEV-32884) Make s3\_debug dynamic
* [Revision #18166e4501](https://github.com/MariaDB/server/commit/18166e4501)\
  2023-11-24 11:23:30 +0200
  * mysqladmin -vv processlist now shows more information
* Merge [Revision #b3a628c7d4](https://github.com/MariaDB/server/commit/b3a628c7d4) 2023-11-30 10:45:01 +0200 - Merge 10.5 into 10.6
* [Revision #bb511def1d](https://github.com/MariaDB/server/commit/bb511def1d)\
  2023-11-30 10:35:53 +0200
  * [MDEV-32371](https://jira.mariadb.org/browse/MDEV-32371) Deadlock between buf\_page\_get\_zip() and buf\_pool\_t::corrupted\_evict()
* [Revision #0ee9b119bf](https://github.com/MariaDB/server/commit/0ee9b119bf)\
  2023-11-30 09:46:25 +0200
  * [MDEV-31817](https://jira.mariadb.org/browse/MDEV-31817) SIGSEGV after btr\_page\_get\_father\_block() returns nullptr on corrupted data
* [Revision #ba6bf7ad9e](https://github.com/MariaDB/server/commit/ba6bf7ad9e)\
  2023-11-29 10:48:10 +0200
  * [MDEV-32899](https://jira.mariadb.org/browse/MDEV-32899) instrumentation
* [Revision #569da6a7ba](https://github.com/MariaDB/server/commit/569da6a7ba)\
  2023-11-28 15:50:41 +0200
  * [MDEV-32899](https://jira.mariadb.org/browse/MDEV-32899) InnoDB is holding shared dict\_sys.latch while waiting for FOREIGN KEY child table lock on DDL
* [Revision #20b0ec9aae](https://github.com/MariaDB/server/commit/20b0ec9aae)\
  2023-11-27 09:56:21 +0400
  * [MDEV-32879](https://jira.mariadb.org/browse/MDEV-32879) Server crash in my\_decimal::operator= or unexpected ER\_DUP\_ENTRY upon comparison with INET6 and similar types
* [Revision #2f467de4c4](https://github.com/MariaDB/server/commit/2f467de4c4)\
  2023-11-24 14:25:32 +0200
  * [MDEV-32873](https://jira.mariadb.org/browse/MDEV-32873) Test innodb.innodb-index-online occasionally fails
* Merge [Revision #d963584d4c](https://github.com/MariaDB/server/commit/d963584d4c) 2023-11-22 16:56:47 +0200 - Merge 10.5 into 10.6
* [Revision #4c16ec3e77](https://github.com/MariaDB/server/commit/4c16ec3e77)\
  2023-11-21 12:42:00 +0200
  * [MDEV-32050](https://jira.mariadb.org/browse/MDEV-32050) fixup: Stabilize tests
* Merge [Revision #9c5600adde](https://github.com/MariaDB/server/commit/9c5600adde) 2023-11-21 09:33:06 +0200 - Merge 10.5 into 10.6
* Merge [Revision #0ead203111](https://github.com/MariaDB/server/commit/0ead203111) 2023-11-21 09:18:31 +0200 - Merge 10.5 into 10.6
* [Revision #cd04673a17](https://github.com/MariaDB/server/commit/cd04673a17)\
  2023-11-20 16:57:57 +0200
  * [MDEV-32050](https://jira.mariadb.org/browse/MDEV-32050) fixup: innodb.instant\_alter\_crash (take 2)
* [Revision #eb1f8b2919](https://github.com/MariaDB/server/commit/eb1f8b2919)\
  2023-11-17 15:07:51 +0200
  * [MDEV-32027](https://jira.mariadb.org/browse/MDEV-32027) Opening all .ibd files on InnoDB startup can be slow
* Merge [Revision #44b9e41694](https://github.com/MariaDB/server/commit/44b9e41694) 2023-11-17 13:07:35 +0200 - Merge 10.5 into 10.6
* [Revision #5a1f821b93](https://github.com/MariaDB/server/commit/5a1f821b93)\
  2023-11-16 16:57:42 +0200
  * [MDEV-31861](https://jira.mariadb.org/browse/MDEV-31861) Empty INSERT crashes with innodb\_force\_recovery=6 or innodb\_read\_only=ON
* [Revision #55a96c055a](https://github.com/MariaDB/server/commit/55a96c055a)\
  2023-11-16 16:39:02 +0200
  * [MDEV-32050](https://jira.mariadb.org/browse/MDEV-32050) fixup: innodb.instant\_alter\_crash
* [Revision #ea6ca01397](https://github.com/MariaDB/server/commit/ea6ca01397)\
  2023-11-15 14:11:38 +0200
  * [MDEV-32757](https://jira.mariadb.org/browse/MDEV-32757): rollback crash on corruption
* Merge [Revision #5dbe7a8c9a](https://github.com/MariaDB/server/commit/5dbe7a8c9a) 2023-11-15 14:11:24 +0200 - Merge 10.5 into 10.6
* Merge [Revision #52ca2e65af](https://github.com/MariaDB/server/commit/52ca2e65af) 2023-11-15 14:10:21 +0200 - Merge 10.5 into 10.6
* [Revision #c11610f590](https://github.com/MariaDB/server/commit/c11610f590)\
  2023-11-06 09:06:00 +0200
  * [MDEV-32689](https://jira.mariadb.org/browse/MDEV-32689): Remove Ubuntu Bionic
* Merge [Revision #4a824c0cf0](https://github.com/MariaDB/server/commit/4a824c0cf0) 2023-11-14 08:56:16 +0100 - Merge branch '10.6' into mariadb-10.6.16
* [Revision #91835ef378](https://github.com/MariaDB/server/commit/91835ef378)\
  2023-11-13 13:22:44 -0500
  * bump the VERSION
* [Revision #dec4d0badc](https://github.com/MariaDB/server/commit/dec4d0badc)\
  2023-11-13 14:35:33 +0200
  * [MDEV-32788](https://jira.mariadb.org/browse/MDEV-32788): Debug build failure with SUX\_LOCK\_GENERIC
* [Revision #04477bd936](https://github.com/MariaDB/server/commit/04477bd936)\
  2023-11-08 12:00:29 +0100
  * [MDEV-28836](https://jira.mariadb.org/browse/MDEV-28836) fix crashing PFS unit tests on Windows.
