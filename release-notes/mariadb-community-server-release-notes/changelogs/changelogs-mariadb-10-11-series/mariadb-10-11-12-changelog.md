# MariaDB 10.11.12 Changelog

{% include "../../../../.gitbook/includes/latest-10.11 (2).md" %}

<a href="https://downloads.mariadb.org/mariadb/10.11.12/" class="button primary">Download</a> <a href="../../mariadb-10-11-series/mariadb-10-11-12-release-notes.md" class="button secondary">Release Notes</a> <a href="mariadb-10-11-12-changelog.md" class="button secondary">Changelog</a> <a href="../../mariadb-10-11-series/what-is-mariadb-1011.md" class="button secondary">Overview of 10.11</a>

**Release date:** 6 May 2025

For the highlights of this release, see the release notes.

The revision number links will take you to the revision's page on GitHub. On [GitHub](https://github.com/MariaDB/server/tree/10.11) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Includes all fixes from MariaDB 10.6.22
* [Revision #cafd22db79](https://github.com/MariaDB/server/commit/cafd22db79)\
  2025-04-22 15:29:48 +0300
  * Code cleanup in mark\_common\_columns(): nj\_col\_2 is non-NULL here
* [Revision #5033da6ed6](https://github.com/MariaDB/server/commit/5033da6ed6)\
  2025-04-28 15:12:44 +0300
  * Fix rocksdb\_sys\_vars.rocksdb\_stats\_level\_basic test
* Merge [Revision #4d41ec081e](https://github.com/MariaDB/server/commit/4d41ec081e) 2025-04-26 10:47:03 +0200 - Merge branch '10.6' into 10.11
* [Revision #ddd5ba3a00](https://github.com/MariaDB/server/commit/ddd5ba3a00)\
  2025-02-28 14:43:20 +0200
  * [MDEV-14432](https://jira.mariadb.org/browse/MDEV-14432) mysqldump does not preserve case of table names in generated sql
* [Revision #05813f54cf](https://github.com/MariaDB/server/commit/05813f54cf)\
  2025-04-24 00:23:48 +0400
  * [MDEV-36648](https://jira.mariadb.org/browse/MDEV-36648) - main.mdl\_sync extra test.t2 row in I\_S.metadata\_lock\_info
* [Revision #5f69e18152](https://github.com/MariaDB/server/commit/5f69e18152)\
  2025-04-24 13:46:43 +0530
  * [MDEV-36682](https://jira.mariadb.org/browse/MDEV-36682) Conflict between [MDEV-36504](https://jira.mariadb.org/browse/MDEV-36504) and [MDEV-16329](https://jira.mariadb.org/browse/MDEV-16329)
* [Revision #1d5557d9c0](https://github.com/MariaDB/server/commit/1d5557d9c0)\
  2025-04-22 20:15:08 -0600
  * [MDEV-36663](https://jira.mariadb.org/browse/MDEV-36663) Semi-sync Replica Can't Kill Dump Thread When Using SSL
* [Revision #f1a8b7fe95](https://github.com/MariaDB/server/commit/f1a8b7fe95)\
  2025-04-23 15:42:12 +0300
  * [MDEV-36646](https://jira.mariadb.org/browse/MDEV-36646): innodb\_buffer\_pool\_size change aborted
* [Revision #1a044437a3](https://github.com/MariaDB/server/commit/1a044437a3)\
  2025-03-21 11:43:31 +0200
  * [MDEV-16523](https://jira.mariadb.org/browse/MDEV-16523) update RocksDB to 6.29fb
* Merge [Revision #75ad1e9f00](https://github.com/MariaDB/server/commit/75ad1e9f00) 2025-04-23 08:53:53 +0300 - Merge 10.6 into 10.11
* [Revision #8c7c144f19](https://github.com/MariaDB/server/commit/8c7c144f19)\
  2025-04-14 16:49:25 +0300
  * [MDEV-36592](https://jira.mariadb.org/browse/MDEV-36592): In JOIN ... USING(columns), query plan depends on join order
* [Revision #7b0820b8b7](https://github.com/MariaDB/server/commit/7b0820b8b7)\
  2025-04-21 15:06:30 +0200
  * cleanup: redundant my\_casedn\_str()
* [Revision #ab71860161](https://github.com/MariaDB/server/commit/ab71860161)\
  2025-04-21 15:03:55 +0200
  * cleanup: check\_column\_name(const Lex\_ident \&name)
* [Revision #63a69ab936](https://github.com/MariaDB/server/commit/63a69ab936)\
  2025-04-21 15:03:01 +0200
  * cleanup: remote automatic conversion char\* -> Lex\_ident
* [Revision #588f7a5af7](https://github.com/MariaDB/server/commit/588f7a5af7)\
  2025-01-13 11:17:55 -0700
  * [MDEV-35694](https://jira.mariadb.org/browse/MDEV-35694): Mysqlbinlog --stop-position should warn if EOF not reached with --read-from-remote-server
* Merge [Revision #20b818f45e](https://github.com/MariaDB/server/commit/20b818f45e) 2025-04-21 11:23:11 +0200 - Merge branch '10.6' into 10.11
* [Revision #7d9660ed93](https://github.com/MariaDB/server/commit/7d9660ed93)\
  2024-12-12 14:55:56 +1100
  * item\_json\*: handle memory allocations
* [Revision #ca144971e1](https://github.com/MariaDB/server/commit/ca144971e1)\
  2024-12-12 15:14:23 +1100
  * [MDEV-35614](https://jira.mariadb.org/browse/MDEV-35614): json\_unescape for comparison uses utf8mb4\_bin
* [Revision #ccbcafc22e](https://github.com/MariaDB/server/commit/ccbcafc22e)\
  2024-12-12 15:02:46 +1100
  * [MDEV-35614](https://jira.mariadb.org/browse/MDEV-35614): JSON\_UNQUOTE doesn't work with emojis
* [Revision #5a536adb03](https://github.com/MariaDB/server/commit/5a536adb03)\
  2024-12-12 14:58:59 +1100
  * Arg\_comparator::compare\_{e\_,}json\_str\_basic unescaping warnings
* [Revision #ea20948b8a](https://github.com/MariaDB/server/commit/ea20948b8a)\
  2024-12-12 14:49:20 +1100
  * json: escaping/unescaping errors should be handled.
* [Revision #f699010c0f](https://github.com/MariaDB/server/commit/f699010c0f)\
  2024-12-12 14:48:09 +1100
  * json\_unescape: don't fill unconverted characters with ?
* [Revision #459dfe99d1](https://github.com/MariaDB/server/commit/459dfe99d1)\
  2025-04-18 19:53:55 +0200
  * Fix appveyor config
* [Revision #15fd232da4](https://github.com/MariaDB/server/commit/15fd232da4)\
  2025-04-09 13:57:09 -0400
  * [MDEV-36235](https://jira.mariadb.org/browse/MDEV-36235) Incorrect result for BETWEEN over unique blob prefix
* [Revision #07b442aa68](https://github.com/MariaDB/server/commit/07b442aa68)\
  2025-04-16 13:36:05 +1100
  * [MDEV-36607](https://jira.mariadb.org/browse/MDEV-36607) find\_order\_in\_list mismatch when order item needs fixing()
* [Revision #c25237c28d](https://github.com/MariaDB/server/commit/c25237c28d)\
  2025-04-04 16:07:27 -0400
  * [MDEV-36211](https://jira.mariadb.org/browse/MDEV-36211) Incorrect query result for binary\_column NOT LIKE binary\_column
* [Revision #23cc3eb1f7](https://github.com/MariaDB/server/commit/23cc3eb1f7)\
  2025-04-17 15:11:21 +0300
  * [MDEV-36257](https://jira.mariadb.org/browse/MDEV-36257): Fix a debug assertion
* [Revision #f388222d49](https://github.com/MariaDB/server/commit/f388222d49)\
  2025-04-17 10:28:17 +0530
  * [MDEV-36504](https://jira.mariadb.org/browse/MDEV-36504) Memory leak after CREATE TABLE..SELECT
* Merge [Revision #1a013cea95](https://github.com/MariaDB/server/commit/1a013cea95) 2025-04-15 21:40:26 +0200 - Merge branch '10.6' into '10.11'
* [Revision #4c9ff3c1be](https://github.com/MariaDB/server/commit/4c9ff3c1be)\
  2025-04-15 15:42:10 +0200
  * Improve AppVeyor CI configuration
* [Revision #6edfdae44d](https://github.com/MariaDB/server/commit/6edfdae44d)\
  2025-04-09 17:00:42 +0200
  * [MDEV-35983](https://jira.mariadb.org/browse/MDEV-35983) Avoid install failures by using retry logic for file operations
* [Revision #1f5d2b2010](https://github.com/MariaDB/server/commit/1f5d2b2010)\
  2025-03-29 20:36:08 +0200
  * [MDEV-33671](https://jira.mariadb.org/browse/MDEV-33671): Remove hardcoded open-files-limit in safe\_process.cc
* [Revision #a524ec5951](https://github.com/MariaDB/server/commit/a524ec5951)\
  2025-04-14 10:33:22 +0300
  * [MDEV-36587](https://jira.mariadb.org/browse/MDEV-36587) InnoDB uses too much memory
* [Revision #a096f12ff7](https://github.com/MariaDB/server/commit/a096f12ff7)\
  2025-04-14 08:33:10 +0300
  * [MDEV-29445](https://jira.mariadb.org/browse/MDEV-29445) fixup: debug assertion
* [Revision #60638a84e8](https://github.com/MariaDB/server/commit/60638a84e8)\
  2025-04-13 12:11:34 +0200
  * [MDEV-36586](https://jira.mariadb.org/browse/MDEV-36586) USER\_STATISTICS.BUSY\_TIME is in microseconds
* [Revision #acd071f599](https://github.com/MariaDB/server/commit/acd071f599)\
  2025-04-10 13:02:17 +0300
  * [MDEV-21923](https://jira.mariadb.org/browse/MDEV-21923): LSN allocation is a bottleneck
* [Revision #0bcc03a2e6](https://github.com/MariaDB/server/commit/0bcc03a2e6)\
  2025-04-10 12:58:10 +0300
  * Recovery cleanup
* [Revision #00fa5b8676](https://github.com/MariaDB/server/commit/00fa5b8676)\
  2025-02-04 13:42:18 -0500
  * [MDEV-35721](https://jira.mariadb.org/browse/MDEV-35721) UBSAN: runtime error: -nan outside range
* [Revision #669f719cc2](https://github.com/MariaDB/server/commit/669f719cc2)\
  2025-04-07 11:01:17 +0300
  * [MDEV-36489](https://jira.mariadb.org/browse/MDEV-36489) 10.11 crashes during bootstrap on macOS
* [Revision #b005b6097f](https://github.com/MariaDB/server/commit/b005b6097f)\
  2025-04-03 12:25:44 +0200
  * Cleanup CMake code (Windows-specific)
* [Revision #ff4209fa0d](https://github.com/MariaDB/server/commit/ff4209fa0d)\
  2025-04-01 10:39:25 +0200
  * Fix broken clang-cl compilation
* [Revision #dca2e5509e](https://github.com/MariaDB/server/commit/dca2e5509e)\
  2025-04-04 16:22:30 +1100
  * [MDEV-36480](https://jira.mariadb.org/browse/MDEV-36480) USAN: checking identifier names for 0 length names
* [Revision #c06c36218a](https://github.com/MariaDB/server/commit/c06c36218a)\
  2024-11-25 19:06:51 +0200
  * [MDEV-35506](https://jira.mariadb.org/browse/MDEV-35506) commit policy of one-phase-commit even at errored-out binlogging leads to assert
* [Revision #1b4efbeb8c](https://github.com/MariaDB/server/commit/1b4efbeb8c)\
  2024-11-25 19:48:23 +0200
  * [MDEV-35207](https://jira.mariadb.org/browse/MDEV-35207) ignored error at binlogging by CREATE-TABLE-SELECT leads to assert
* [Revision #58a3677309](https://github.com/MariaDB/server/commit/58a3677309)\
  2025-04-02 15:56:22 +0300
  * [MDEV-29445](https://jira.mariadb.org/browse/MDEV-29445) fixup: Do not skip a test
* Merge [Revision #373071b956](https://github.com/MariaDB/server/commit/373071b956) 2025-04-02 15:55:46 +0300 - Merge 10.6 into 10.11
* Merge [Revision #aaec841865](https://github.com/MariaDB/server/commit/aaec841865) 2025-04-02 09:33:20 +0300 - Merge 10.6 into 10.11
* [Revision #4d1484f045](https://github.com/MariaDB/server/commit/4d1484f045)\
  2025-04-02 09:33:09 +0300
  * Merge fixup
* Merge [Revision #74f0b99edf](https://github.com/MariaDB/server/commit/74f0b99edf) 2025-04-02 05:50:52 +0200 - Merge branch '10.6' into '10.11'
* [Revision #0545695de7](https://github.com/MariaDB/server/commit/0545695de7)\
  2025-03-31 15:21:14 +0200
  * [MDEV-36426](https://jira.mariadb.org/browse/MDEV-36426) Crash handler output needs newline before "Optimizer switch"
* [Revision #a632a69386](https://github.com/MariaDB/server/commit/a632a69386)\
  2025-03-28 13:28:28 +0100
  * [MDEV-36127](https://jira.mariadb.org/browse/MDEV-36127) Add MTR test for mariadb-upgrade-service on Windows
* [Revision #fc60b89d0c](https://github.com/MariaDB/server/commit/fc60b89d0c)\
  2025-03-28 12:16:51 +0100
  * [MDEV-36283](https://jira.mariadb.org/browse/MDEV-36283) "OpenEvent() failed" fatal error in mariadb-upgrade-service
* Merge [Revision #730dcf7e6d](https://github.com/MariaDB/server/commit/730dcf7e6d) 2025-03-31 17:57:43 +0200 - Merge branch '10.6' into 10.11
* [Revision #6e339baad5](https://github.com/MariaDB/server/commit/6e339baad5)\
  2025-03-30 14:22:45 +0200
  * [MDEV-28908](https://jira.mariadb.org/browse/MDEV-28908) Confusing documentation and help output for --ssl-verify-server-cert
* [Revision #7d17ee97c2](https://github.com/MariaDB/server/commit/7d17ee97c2)\
  2025-03-30 12:43:35 +0200
  * [MDEV-36437](https://jira.mariadb.org/browse/MDEV-36437) mariadb-backup - confusing error message when running out of file handles with partitioned MyISAM
* [Revision #8363d05f4d](https://github.com/MariaDB/server/commit/8363d05f4d)\
  2025-03-25 18:49:03 +0100
  * Fix Windows build to use dynamic DLL runtime (MD) by default
* [Revision #8896de2baa](https://github.com/MariaDB/server/commit/8896de2baa)\
  2025-03-24 20:21:45 +0100
  * [MDEV-35746](https://jira.mariadb.org/browse/MDEV-35746) support fmtlib-11.1.0
* [Revision #56b19ac030](https://github.com/MariaDB/server/commit/56b19ac030)\
  2025-03-22 21:40:06 +0100
  * [MDEV-35953](https://jira.mariadb.org/browse/MDEV-35953) mysql\_stmt\_errno() returns 0 after an error in mysql\_stmt\_execute()
* [Revision #0b37c2e7a8](https://github.com/MariaDB/server/commit/0b37c2e7a8)\
  2025-02-14 14:58:31 +0100
  * [MDEV-36084](https://jira.mariadb.org/browse/MDEV-36084) mariadb-hotcopy requires '--port' set for operation since 10.11
* Merge [Revision #7335e9b8ef](https://github.com/MariaDB/server/commit/7335e9b8ef) 2025-03-28 10:55:40 +0200 - Merge 10.6 into 10.11
* [Revision #c61345169a](https://github.com/MariaDB/server/commit/c61345169a)\
  2025-03-28 02:53:59 +0100
  * galera tests: synchronization after merge
* [Revision #027d815546](https://github.com/MariaDB/server/commit/027d815546)\
  2025-03-27 14:52:07 +0200
  * [MDEV-29445](https://jira.mariadb.org/browse/MDEV-29445) fixup: Make Valgrind fair again
* [Revision #9a6540cb84](https://github.com/MariaDB/server/commit/9a6540cb84)\
  2025-03-27 08:54:00 +0200
  * [MDEV-29445](https://jira.mariadb.org/browse/MDEV-29445) fixup: galera\_sst\_mariadb-backup\_use\_memory
* [Revision #d68f5ea9f0](https://github.com/MariaDB/server/commit/d68f5ea9f0)\
  2025-03-27 08:19:40 +0200
  * [MDEV-35000](https://jira.mariadb.org/browse/MDEV-35000) fixup: galera.[MDEV-33136](https://jira.mariadb.org/browse/MDEV-33136)
* Merge [Revision #ab0f2a00b6](https://github.com/MariaDB/server/commit/ab0f2a00b6) 2025-03-27 08:01:47 +0200 - Merge 10.6 into 10.11
* [Revision #ba81009f63](https://github.com/MariaDB/server/commit/ba81009f63)\
  2025-03-26 17:05:48 +0200
  * [MDEV-34863](https://jira.mariadb.org/browse/MDEV-34863) RAM Usage Changed Significantly Between 10.11 Releases
* [Revision #b6923420f3](https://github.com/MariaDB/server/commit/b6923420f3)\
  2025-03-26 17:05:44 +0200
  * [MDEV-29445](https://jira.mariadb.org/browse/MDEV-29445): Reimplement SET GLOBAL innodb\_buffer\_pool\_size
* [Revision #3b4de4c281](https://github.com/MariaDB/server/commit/3b4de4c281)\
  2025-03-24 13:07:36 +0200
  * [MDEV-32084](https://jira.mariadb.org/browse/MDEV-32084): Assertion in best\_extension\_by\_limited\_search() ...
* [Revision #d1a6792324](https://github.com/MariaDB/server/commit/d1a6792324)\
  2025-03-26 14:31:44 +0200
  * [MDEV-36122](https://jira.mariadb.org/browse/MDEV-36122): Protect table references with a lock
* [Revision #4a21cba7fc](https://github.com/MariaDB/server/commit/4a21cba7fc)\
  2025-03-26 14:30:46 +0200
  * [MDEV-36122](https://jira.mariadb.org/browse/MDEV-36122) Assertion ctx0->old\_table->get\_ref\_count() == 1
* [Revision #47d11328c9](https://github.com/MariaDB/server/commit/47d11328c9)\
  2025-03-25 14:42:58 +0200
  * [MDEV-36381](https://jira.mariadb.org/browse/MDEV-36381): Comment "Procedure of keys generation ..." is in the wrong place
* [Revision #33a462e0b1](https://github.com/MariaDB/server/commit/33a462e0b1)\
  2025-03-25 08:48:08 +0200
  * [MDEV-36373](https://jira.mariadb.org/browse/MDEV-36373) Bogus Warning: ... storage is corrupted
* [Revision #b0ec99398f](https://github.com/MariaDB/server/commit/b0ec99398f)\
  2025-01-20 23:16:53 +0000
  * [MDEV-21375](https://jira.mariadb.org/browse/MDEV-21375): Get option group suffix from $MARIADB\_GROUP\_SUFFIX in addition to $MYSQL\_GROUP\_SUFFIX
* [Revision #4c695c85bd](https://github.com/MariaDB/server/commit/4c695c85bd)\
  2025-03-24 09:01:07 +0300
  * [MDEV-34775](https://jira.mariadb.org/browse/MDEV-34775) Wrong reopen of already open routine due to auto-create in SP
* [Revision #f813c8541a](https://github.com/MariaDB/server/commit/f813c8541a)\
  2025-03-14 03:30:33 +0200
  * [MDEV-34621](https://jira.mariadb.org/browse/MDEV-34621) Fix division by zero in mariadb-slap when iterations=0
* [Revision #2a92cf8b0c](https://github.com/MariaDB/server/commit/2a92cf8b0c)\
  2025-03-20 15:29:43 +0200
  * [MDEV-35000](https://jira.mariadb.org/browse/MDEV-35000) fixup: GCC 4.8.5 -Wconversion
* [Revision #b50df7bbd4](https://github.com/MariaDB/server/commit/b50df7bbd4)\
  2025-03-06 11:21:18 +1100
  * [MDEV-36220](https://jira.mariadb.org/browse/MDEV-36220) Correct length in memcpy saving and restoring found NULL record in loose index scan of min
* [Revision #15848a75a7](https://github.com/MariaDB/server/commit/15848a75a7)\
  2025-03-06 22:06:53 -0700
  * [MDEV-36238](https://jira.mariadb.org/browse/MDEV-36238) Functional Tests for --master-info-file and --show-slave-auth-info
* [Revision #408a637b87](https://github.com/MariaDB/server/commit/408a637b87)\
  2025-03-14 12:43:22 +0700
  * [MDEV-29344](https://jira.mariadb.org/browse/MDEV-29344): engines/iuds.insert\_time cannot run with PS protocol (syntax error)
* [Revision #a8e35a1cc6](https://github.com/MariaDB/server/commit/a8e35a1cc6)\
  2025-03-11 12:13:05 +0530
  * [MDEV-36149](https://jira.mariadb.org/browse/MDEV-36149) UBSAN in X is outside the range of representable values of type 'unsigned long' | page\_cleaner\_flush\_pages\_recommendation
* [Revision #839828e57f](https://github.com/MariaDB/server/commit/839828e57f)\
  2024-11-05 12:44:58 +0000
  * [MDEV-36009](https://jira.mariadb.org/browse/MDEV-36009): Systemd: Restart on OOM
* [Revision #55efe47d3c](https://github.com/MariaDB/server/commit/55efe47d3c)\
  2025-03-11 15:28:52 +1100
  * [MDEV-36118](https://jira.mariadb.org/browse/MDEV-36118) Fix wrong result with MAX in loose index scan
* [Revision #652f33e0a4](https://github.com/MariaDB/server/commit/652f33e0a4)\
  2025-03-10 08:48:43 +0200
  * [MDEV-30000](https://jira.mariadb.org/browse/MDEV-30000): Force an InnoDB checkpoint in mariadb-backup
* [Revision #5b686cc8f9](https://github.com/MariaDB/server/commit/5b686cc8f9)\
  2025-03-10 11:11:50 +0530
  * [MDEV-36253](https://jira.mariadb.org/browse/MDEV-36253) Redundant check in wf\_incremental\_process()
* [Revision #0331f1fff7](https://github.com/MariaDB/server/commit/0331f1fff7)\
  2025-03-07 10:52:59 +0200
  * [MDEV-36227](https://jira.mariadb.org/browse/MDEV-36227) Race condition between ALTER TABLE…EXCHANGE PARTITION and SELECT
* [Revision #6e6a1b316c](https://github.com/MariaDB/server/commit/6e6a1b316c)\
  2025-02-28 09:00:16 +0200
  * [MDEV-35000](https://jira.mariadb.org/browse/MDEV-35000): dict\_table\_close() breaks STATS\_AUTO\_RECALC
* [Revision #1ed09cfdcb](https://github.com/MariaDB/server/commit/1ed09cfdcb)\
  2025-02-28 08:55:16 +0200
  * [MDEV-35000](https://jira.mariadb.org/browse/MDEV-35000) preparation: Clean up dict\_table\_t::stat
* [Revision #1965b2be16](https://github.com/MariaDB/server/commit/1965b2be16)\
  2024-07-15 16:00:32 +0300
  * [MDEV-34620](https://jira.mariadb.org/browse/MDEV-34620): Lots of index\_merge created and discarded for many-way OR
* [Revision #733852d4c3](https://github.com/MariaDB/server/commit/733852d4c3)\
  2025-02-26 17:57:43 +0700
  * BKA join cache buffer is employed despite join\_cache\_level=3 (flat BNLH)
* [Revision #937ae4137e](https://github.com/MariaDB/server/commit/937ae4137e)\
  2025-02-26 18:49:15 +1100
  * [MDEV-36155](https://jira.mariadb.org/browse/MDEV-36155): MSAN use-of-uninitialized-value innodb.log\_file\_size\_online
* [Revision #2c0ba2680b](https://github.com/MariaDB/server/commit/2c0ba2680b)\
  2025-02-25 15:45:44 +0200
  * load\_db\_opt was always doing a file access if db.opt file did not exist
* [Revision #cf01bfe811](https://github.com/MariaDB/server/commit/cf01bfe811)\
  2025-02-25 15:43:20 +0200
  * Extended mariadb-test-run to define MARIADB\_TOPDIR and MARIADB\_DATADIR
* [Revision #7b59a4dbc2](https://github.com/MariaDB/server/commit/7b59a4dbc2)\
  2025-02-25 15:50:23 +0200
  * Allow 'mariadb' as a connection wrapper name for FederatedX.
* [Revision #aea440d3e7](https://github.com/MariaDB/server/commit/aea440d3e7)\
  2025-02-09 14:48:38 +0200
  * Fixed mysqld\_list\_processes to remove a possibility to access null pointers
* [Revision #809a0cebdc](https://github.com/MariaDB/server/commit/809a0cebdc)\
  2025-02-25 11:41:49 +0200
  * [MDEV-36152](https://jira.mariadb.org/browse/MDEV-36152) mariadb-backup --backup crash during innodb\_undo\_log\_truncate=ON, innodb\_encrypt\_log=ON
* Merge [Revision #0c204bfb87](https://github.com/MariaDB/server/commit/0c204bfb87) 2025-02-25 10:23:24 +0200 - Merge 10.6 into 10.11
* [Revision #49d976feaa](https://github.com/MariaDB/server/commit/49d976feaa)\
  2025-01-15 18:10:16 +1100
  * [MDEV-29605](https://jira.mariadb.org/browse/MDEV-29605) Reset queued ping info of all spider connections associated with a closed spider handler
* [Revision #7e001b2a3c](https://github.com/MariaDB/server/commit/7e001b2a3c)\
  2025-02-17 15:55:58 +0200
  * [MDEV-36082](https://jira.mariadb.org/browse/MDEV-36082) Race condition between log\_t::resize\_start() and log\_t::resize\_abort()
* [Revision #43c5d1303f](https://github.com/MariaDB/server/commit/43c5d1303f)\
  2025-02-10 14:36:56 +0200
  * [MDEV-35958](https://jira.mariadb.org/browse/MDEV-35958) Cost estimates for materialized derived tables are poor
* [Revision #c9fe55ff7a](https://github.com/MariaDB/server/commit/c9fe55ff7a)\
  2025-02-10 14:32:47 +0100
  * [MDEV-36056](https://jira.mariadb.org/browse/MDEV-36056) Fix VS2019 compilation
* Merge [Revision #565a0cebd8](https://github.com/MariaDB/server/commit/565a0cebd8) 2025-02-10 14:45:18 +0200 - Merge 10.6 into 10.11
* [Revision #91de54e098](https://github.com/MariaDB/server/commit/91de54e098)\
  2025-02-04 21:46:42 +0200
  * Remove redundant if-statement in Index\_prefix\_calc::get\_avg\_frequency
* [Revision #0e80d3bba8](https://github.com/MariaDB/server/commit/0e80d3bba8)\
  2025-02-04 11:18:48 -0500
  * bump the VERSION
* Merge [Revision #72f21560d5](https://github.com/MariaDB/server/commit/72f21560d5) 2025-02-02 22:29:42 +0100 - Merge branch '10.6' into '10.11'
* [Revision #5f68fd52a9](https://github.com/MariaDB/server/commit/5f68fd52a9)\
  2025-01-30 16:30:56 +0200
  * [MDEV-35955](https://jira.mariadb.org/browse/MDEV-35955) Wrong result for UPDATE ... ORDER BY LIMIT which uses tmp.table

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
