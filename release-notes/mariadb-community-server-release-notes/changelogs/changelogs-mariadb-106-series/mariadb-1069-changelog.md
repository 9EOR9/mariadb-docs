# MariaDB 10.6.9 Changelog

The most recent release of [MariaDB 10.6](../../mariadb-10-6-series/what-is-mariadb-106.md) is:[**MariaDB 10.6.21**](../../mariadb-10-6-series/mariadb-10-6-21-release-notes.md) Stable (GA) [Download Now](https://mariadb.com/downloads/)[_Alternate download from mariadb.org_](https://downloads.mariadb.org/mariadb/10.6.21/)

[Download 10.6.9](https://downloads.mariadb.org/mariadb/10.6.9/)[Release Notes](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/changelogs/changelogs-mariadb-106-series/broken-reference/README.md)[Changelog](mariadb-1069-changelog.md)[Overview of 10.6](../../mariadb-10-6-series/what-is-mariadb-106.md)

**Release date:** 15 Aug 2022

For the highlights of this release, see the[release notes](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/changelogs/changelogs-mariadb-106-series/broken-reference/README.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/server/tree/10.6) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Includes all fixes from [MariaDB 10.5.17](../changelogs-mariadb-105-series/mariadb-10517-changelog.md)
* [Revision #b8f6d315fe](https://github.com/MariaDB/server/commit/b8f6d315fe)\
  2022-08-02 14:35:48 +1000
  * [MDEV-29222](https://jira.mariadb.org/browse/MDEV-29222) - Fix mysqld\_safe script
* Merge [Revision #c442e1ae21](https://github.com/MariaDB/server/commit/c442e1ae21) 2022-08-10 13:06:08 +0200 - Merge branch '10.5' into 10.6
* [Revision #4f54c219e7](https://github.com/MariaDB/server/commit/4f54c219e7)\
  2022-08-08 13:00:36 +0200
  * update columnstore
* [Revision #c980350438](https://github.com/MariaDB/server/commit/c980350438)\
  2022-08-05 11:02:18 +0300
  * [MDEV-13542](https://jira.mariadb.org/browse/MDEV-13542) fixup: Improve a recovery error message
* [Revision #5dc8605069](https://github.com/MariaDB/server/commit/5dc8605069)\
  2022-08-05 08:48:25 +0200
  * fix tests
* Merge [Revision #ee620a7416](https://github.com/MariaDB/server/commit/ee620a7416) 2022-08-04 16:58:42 +0200 - Merge branch '10.5' into 10.6
* [Revision #558f1eff64](https://github.com/MariaDB/server/commit/558f1eff64)\
  2022-08-04 09:30:53 +0300
  * [MDEV-29115](https://jira.mariadb.org/browse/MDEV-29115) mariadb-backup.[MDEV-14447](https://jira.mariadb.org/browse/MDEV-14447) started failing in a new way
* [Revision #c1ea55ddb0](https://github.com/MariaDB/server/commit/c1ea55ddb0)\
  2022-08-03 13:32:06 +0200
  * New CC
* Merge [Revision #d2f1c3ed6c](https://github.com/MariaDB/server/commit/d2f1c3ed6c) 2022-08-03 10:47:52 +0200 - Merge branch '10.5' into bb-10.6-release
* [Revision #212994f704](https://github.com/MariaDB/server/commit/212994f704)\
  2022-08-01 16:40:14 +0300
  * [MDEV-28974](https://jira.mariadb.org/browse/MDEV-28974): mariadb-backup --prepare fails
* [Revision #34cdc00628](https://github.com/MariaDB/server/commit/34cdc00628)\
  2022-08-01 16:39:44 +0300
  * [MDEV-13542](https://jira.mariadb.org/browse/MDEV-13542) fixup: Improve page reorganize
* [Revision #84d26f98c7](https://github.com/MariaDB/server/commit/84d26f98c7)\
  2022-08-01 04:27:33 -0700
  * [MDEV-28315](https://jira.mariadb.org/browse/MDEV-28315) Fix ASAN stack-buffer-overflow in String::copy\_aligned
* [Revision #63478e72de](https://github.com/MariaDB/server/commit/63478e72de)\
  2022-08-01 11:25:50 +0300
  * [MDEV-21098](https://jira.mariadb.org/browse/MDEV-21098): Assertion failure in rec\_get\_offsets\_func()
* [Revision #a6f7c8edc9](https://github.com/MariaDB/server/commit/a6f7c8edc9)\
  2022-07-29 15:57:51 +0530
  * [MDEV-28762](https://jira.mariadb.org/browse/MDEV-28762): recursive call of some json functions without stack control
* [Revision #05a407b239](https://github.com/MariaDB/server/commit/05a407b239)\
  2022-07-20 10:26:51 -0700
  * [MDEV-28782](https://jira.mariadb.org/browse/MDEV-28782): modify mariadb-tzinfo-to-sql to set 'wsrep\*' variables appropriately in cases where Galera is not compiled in
* [Revision #38d0256b14](https://github.com/MariaDB/server/commit/38d0256b14)\
  2022-07-28 21:03:32 +0530\
  \*
  * Fixed the change\_column\_collation test case to avoid the loss of debug sync signal
* [Revision #2658410afc](https://github.com/MariaDB/server/commit/2658410afc)\
  2022-07-28 15:53:56 +1000
  * [MDEV-29187](https://jira.mariadb.org/browse/MDEV-29187): Deadlock output in InnoDB status always shows transaction (0)
* Merge [Revision #30914389fe](https://github.com/MariaDB/server/commit/30914389fe) 2022-07-27 17:52:37 +0300 - Merge 10.5 into 10.6
* [Revision #772e3f61eb](https://github.com/MariaDB/server/commit/772e3f61eb)\
  2022-07-27 08:25:13 +0300
  * [MDEV-28950](https://jira.mariadb.org/browse/MDEV-28950): Add a test case
* [Revision #8d238d4726](https://github.com/MariaDB/server/commit/8d238d4726)\
  2022-06-30 15:46:19 +0300
  * [MDEV-28609](https://jira.mariadb.org/browse/MDEV-28609) refine gtid-strict-mode to ignore same server-id gtid from the past
* [Revision #552919d041](https://github.com/MariaDB/server/commit/552919d041)\
  2022-07-25 21:00:47 +1000
  * [MDEV-29166](https://jira.mariadb.org/browse/MDEV-29166): reduce locking of innodb rseg for user exposure of innodb\_history\_list\_length
* Merge [Revision #b9eb63618e](https://github.com/MariaDB/server/commit/b9eb63618e) 2022-07-26 11:37:36 +0300 - Merge 10.5 into 10.6
* [Revision #1d3629875e](https://github.com/MariaDB/server/commit/1d3629875e)\
  2022-07-26 11:33:52 +0530
  * [MDEV-29137](https://jira.mariadb.org/browse/MDEV-29137) mariadb-backup excessive logging of ddl tracking
* [Revision #e94902c062](https://github.com/MariaDB/server/commit/e94902c062)\
  2022-06-22 14:37:52 +0530
  * [MDEV-28762](https://jira.mariadb.org/browse/MDEV-28762): recursive call of some json functions without stack control
* [Revision #222e800e24](https://github.com/MariaDB/server/commit/222e800e24)\
  2022-06-06 14:31:19 +0300
  * [MDEV-21136](https://jira.mariadb.org/browse/MDEV-21136) InnoDB's records\_in\_range estimates can be way off
* [Revision #6156a2be30](https://github.com/MariaDB/server/commit/6156a2be30)\
  2022-07-25 17:00:51 +0530
  * [MDEV-29137](https://jira.mariadb.org/browse/MDEV-29137) mariadb-backup excessive logging of ddl tracking
* [Revision #654236c06d](https://github.com/MariaDB/server/commit/654236c06d)\
  2022-07-20 14:13:07 +0200
  * [MDEV-26456](https://jira.mariadb.org/browse/MDEV-26456): SIGSEGV in flush\_tables\_with\_read\_lock on FLUSH TABLE
* [Revision #0ea221e12b](https://github.com/MariaDB/server/commit/0ea221e12b)\
  2022-06-22 14:37:52 +0530
  * [MDEV-28762](https://jira.mariadb.org/browse/MDEV-28762): recursive call of some json functions without stack control
* [Revision #3a9cb4c1d7](https://github.com/MariaDB/server/commit/3a9cb4c1d7)\
  2022-05-27 11:30:24 -0700
  * Fix Ninja builds on Gitlab-CI by limiting parallelism
* [Revision #8299f88228](https://github.com/MariaDB/server/commit/8299f88228)\
  2022-07-18 17:18:26 +0200
  * [MDEV-28562](https://jira.mariadb.org/browse/MDEV-28562) main.secure\_file\_priv\_win fails with ps-protocol due to missing warnings
* [Revision #f8240a2723](https://github.com/MariaDB/server/commit/f8240a2723)\
  2022-07-04 11:15:15 +0300
  * [MDEV-26294](https://jira.mariadb.org/browse/MDEV-26294) Duplicate entries in unique index not detected when changing collation
* Merge [Revision #f43145a0e3](https://github.com/MariaDB/server/commit/f43145a0e3) 2022-07-04 16:12:44 +0300 - Merge 10.5 into 10.6
* [Revision #494a75c851](https://github.com/MariaDB/server/commit/494a75c851)\
  2022-07-03 15:49:41 +0200
  * [MDEV-28888](https://jira.mariadb.org/browse/MDEV-28888) : Embedded MariaDB does not build on Windows
* [Revision #0c62b6d565](https://github.com/MariaDB/server/commit/0c62b6d565)\
  2022-06-30 06:54:07 -0500
  * Format properly mtr report for the test case that is not completed
* Merge [Revision #62a20f8047](https://github.com/MariaDB/server/commit/62a20f8047) 2022-07-01 15:24:50 +0300 - Merge 10.5 into 10.6
* [Revision #ba3354fca6](https://github.com/MariaDB/server/commit/ba3354fca6)\
  2022-07-01 13:04:44 +0200
  * [MDEV-28995](https://jira.mariadb.org/browse/MDEV-28995) Sporadic Assertion on shutdown in threadpool\_winsockets.cc
* Merge [Revision #90792e4a43](https://github.com/MariaDB/server/commit/90792e4a43) 2022-06-30 19:41:07 +0300 - Merge 10.5 into 10.6
* [Revision #eb7e24932b](https://github.com/MariaDB/server/commit/eb7e24932b)\
  2022-06-13 21:32:06 +0530
  * [MDEV-28806](https://jira.mariadb.org/browse/MDEV-28806) Assertion \`flag == 1' failure in row\_build\_index\_entry\_low upon concurrent ALTER and UPDATE
* [Revision #85c0f4d2de](https://github.com/MariaDB/server/commit/85c0f4d2de)\
  2022-05-30 16:04:09 +0200
  * C/C 3.3
* [Revision #c1e3fc0e0d](https://github.com/MariaDB/server/commit/c1e3fc0e0d)\
  2022-06-29 15:48:44 +0300
  * [MDEV-28977](https://jira.mariadb.org/browse/MDEV-28977): mariadb-backup.huge\_lsn,strict\_full\_crc32 fails in 10.8
* [Revision #2fa3ada072](https://github.com/MariaDB/server/commit/2fa3ada072)\
  2022-06-28 20:58:45 +0300
  * Fix a sporadic failure of main.backup\_locks
* [Revision #5e40934d24](https://github.com/MariaDB/server/commit/5e40934d24)\
  2022-06-28 15:57:41 +0300
  * [MDEV-28897](https://jira.mariadb.org/browse/MDEV-28897) Wrong table.get\_ref\_count() upon concurrent truncate and backup stage operation
* [Revision #02a313dc56](https://github.com/MariaDB/server/commit/02a313dc56)\
  2022-06-28 12:29:30 +0300
  * [MDEV-18976](https://jira.mariadb.org/browse/MDEV-18976) fixup: encryption.innodb-redo-nokeys
* [Revision #1ae8160710](https://github.com/MariaDB/server/commit/1ae8160710)\
  2022-06-27 16:51:53 +0300
  * [MDEV-26979](https://jira.mariadb.org/browse/MDEV-26979) heap-use-after-free or SIGSEGV when accessing INNODB\_SYS\_TABLESTATS during DDL
* Merge [Revision #20cf63fe8b](https://github.com/MariaDB/server/commit/20cf63fe8b) 2022-06-27 16:51:27 +0300 - Merge 10.5 into 10.6
* [Revision #39f45f6f89](https://github.com/MariaDB/server/commit/39f45f6f89)\
  2022-06-27 12:32:03 +0300
  * [MDEV-28950](https://jira.mariadb.org/browse/MDEV-28950) Assertion \`\*err == DB\_SUCCESS' failed in btr\_page\_split\_and\_insert
* [Revision #7d92c9d212](https://github.com/MariaDB/server/commit/7d92c9d212)\
  2022-06-27 11:03:52 +0300
  * Suppress a message that may be emitted on slow systems
* Merge [Revision #87bd79b1e7](https://github.com/MariaDB/server/commit/87bd79b1e7) 2022-06-27 10:59:31 +0300 - Merge 10.5 into 10.6
* [Revision #d96436c999](https://github.com/MariaDB/server/commit/d96436c999)\
  2022-06-23 15:37:11 +0200
  * [MDEV-28935](https://jira.mariadb.org/browse/MDEV-28935) crash in io\_slots::release
* [Revision #f2f18e20eb](https://github.com/MariaDB/server/commit/f2f18e20eb)\
  2022-06-23 13:17:20 +0300
  * [MDEV-28923](https://jira.mariadb.org/browse/MDEV-28923) atomic.rename\_table occasionally fails
* Merge [Revision #eb7f46ca1e](https://github.com/MariaDB/server/commit/eb7f46ca1e) 2022-06-23 06:29:57 +0200 - Merge remote-tracking branch 'origin/10.5' into 10.6
* [Revision #0f0a45b2dc](https://github.com/MariaDB/server/commit/0f0a45b2dc)\
  2022-06-22 17:27:49 +0300
  * [MDEV-18976](https://jira.mariadb.org/browse/MDEV-18976) fixup: encryption.innodb-redo-badkey
* [Revision #6f4d0659dd](https://github.com/MariaDB/server/commit/6f4d0659dd)\
  2022-06-22 10:04:28 +0300
  * [MDEV-22388](https://jira.mariadb.org/browse/MDEV-22388) Corrupted undo log record leads to server crash
* [Revision #0fa19fdebf](https://github.com/MariaDB/server/commit/0fa19fdebf)\
  2022-06-22 08:23:32 +0300
  * [MDEV-28836](https://jira.mariadb.org/browse/MDEV-28836) fixup
* [Revision #3794673111](https://github.com/MariaDB/server/commit/3794673111)\
  2022-06-21 16:59:49 +0300
  * [MDEV-28836](https://jira.mariadb.org/browse/MDEV-28836): Memory alignment cleanup
* [Revision #2e43af69e3](https://github.com/MariaDB/server/commit/2e43af69e3)\
  2022-06-21 16:59:21 +0300
  * [MDEV-28870](https://jira.mariadb.org/browse/MDEV-28870) InnoDB: Missing FILE\_CREATE, FILE\_DELETE or FILE\_MODIFY before FILE\_CHECKPOINT
* [Revision #55f02c24a6](https://github.com/MariaDB/server/commit/55f02c24a6)\
  2022-06-21 14:40:40 +0300
  * [MDEV-28845](https://jira.mariadb.org/browse/MDEV-28845) fixup: Prevent an infinite loop
* [Revision #3b662c6ebd](https://github.com/MariaDB/server/commit/3b662c6ebd)\
  2022-06-21 14:40:31 +0300
  * [MDEV-28782](https://jira.mariadb.org/browse/MDEV-28782) fixup: ./mtr --embedded
* [Revision #0e4cf497ca](https://github.com/MariaDB/server/commit/0e4cf497ca)\
  2022-06-09 18:27:59 +1000
  * [MDEV-28782](https://jira.mariadb.org/browse/MDEV-28782) mariadb-tzinfo-to-sql to work in bootstrap mode
* Merge [Revision #5bb90cb2ac](https://github.com/MariaDB/server/commit/5bb90cb2ac) 2022-06-16 10:01:29 +0300 - Merge 10.5 into 10.6
* [Revision #e99ba4ac8d](https://github.com/MariaDB/server/commit/e99ba4ac8d)\
  2022-06-16 09:53:46 +0300
  * [MDEV-28864](https://jira.mariadb.org/browse/MDEV-28864) Assertion \`trx\_id <= create\_id' failed in innodb\_check\_version()
* [Revision #253806dffc](https://github.com/MariaDB/server/commit/253806dffc)\
  2022-06-15 17:00:05 +0300
  * [MDEV-28845](https://jira.mariadb.org/browse/MDEV-28845) InnoDB: Failing assertion: bpage->can\_relocate() in buf0lru.cc
* [Revision #0850267d00](https://github.com/MariaDB/server/commit/0850267d00)\
  2022-06-15 13:30:44 +0300
  * [MDEV-13542](https://jira.mariadb.org/browse/MDEV-13542) fixup: Relax an assertion
* [Revision #6c82ab4f72](https://github.com/MariaDB/server/commit/6c82ab4f72)\
  2022-06-14 15:33:11 +0300
  * [MDEV-28840](https://jira.mariadb.org/browse/MDEV-28840) innodb\_undo\_log\_truncate is not crash-safe
* [Revision #6c669b9586](https://github.com/MariaDB/server/commit/6c669b9586)\
  2022-06-14 16:52:47 +0530
  * [MDEV-25581](https://jira.mariadb.org/browse/MDEV-25581) Allow user thread to do InnoDB fts cache sync
* Merge [Revision #1f1fa7e09c](https://github.com/MariaDB/server/commit/1f1fa7e09c) 2022-06-14 09:49:47 +0300 - Merge 10.5 into 10.6
* [Revision #1f3f457193](https://github.com/MariaDB/server/commit/1f3f457193)\
  2022-06-13 17:05:31 +0300
  * [MDEV-28802](https://jira.mariadb.org/browse/MDEV-28802) DROP DATABASE in InnoDB still is case-insensitive
* [Revision #65dd31088a](https://github.com/MariaDB/server/commit/65dd31088a)\
  2022-06-13 15:40:51 +0300
  * Update magic file with Aria table files and ddl log
* [Revision #1fd7d3a9ad](https://github.com/MariaDB/server/commit/1fd7d3a9ad)\
  2022-06-07 10:07:13 +0530
  * [MDEV-25581](https://jira.mariadb.org/browse/MDEV-25581) Allow user thread to do InnoDB fts cache sync
* [Revision #51ca5d517e](https://github.com/MariaDB/server/commit/51ca5d517e)\
  2022-06-10 08:59:23 +0300
  * Fix ./mtr --embedded
* Merge [Revision #e11b82f8f5](https://github.com/MariaDB/server/commit/e11b82f8f5) 2022-06-09 13:34:52 +0300 - Merge 10.5 into 10.6
* [Revision #77b3959b5c](https://github.com/MariaDB/server/commit/77b3959b5c)\
  2022-06-08 14:53:24 +0300
  * [MDEV-28457](https://jira.mariadb.org/browse/MDEV-28457) Crash in page\_dir\_find\_owner\_slot()
* [Revision #892c426371](https://github.com/MariaDB/server/commit/892c426371)\
  2022-06-08 09:48:12 +0300
  * [MDEV-13542](https://jira.mariadb.org/browse/MDEV-13542): Do not crash on decryption failure
* [Revision #c9498f33de](https://github.com/MariaDB/server/commit/c9498f33de)\
  2022-06-08 09:20:48 +0300
  * [MDEV-18519](https://jira.mariadb.org/browse/MDEV-18519): Assertion failure in btr\_page\_reorganize\_low()
* [Revision #3d241eb948](https://github.com/MariaDB/server/commit/3d241eb948)\
  2022-06-06 15:22:24 +0300
  * Improve error reporting in Aria
* [Revision #1de18a836f](https://github.com/MariaDB/server/commit/1de18a836f)\
  2022-06-03 19:08:30 +0300
  * Updated aria\_dump\_log
* [Revision #31811cf81d](https://github.com/MariaDB/server/commit/31811cf81d)\
  2022-05-22 20:46:03 +0300
  * Make join->key\_dependent up to date for derived tables
* [Revision #432a4ebe5c](https://github.com/MariaDB/server/commit/432a4ebe5c)\
  2022-05-18 22:17:32 +0300
  * Improve table pruning in optimizer with up to date key\_dependent map
* [Revision #64f24b776d](https://github.com/MariaDB/server/commit/64f24b776d)\
  2022-05-15 15:46:29 +0300
  * greedy\_search() and best\_extension\_by\_limited\_search() scrambled table order
* [Revision #f0ea7f7f33](https://github.com/MariaDB/server/commit/f0ea7f7f33)\
  2022-06-06 22:21:22 +0300
  * [MDEV-28749](https://jira.mariadb.org/browse/MDEV-28749): restore\_prev\_nj\_state() doesn't update cur\_sj\_inner\_tables correctly
* [Revision #46c4fd45c3](https://github.com/MariaDB/server/commit/46c4fd45c3)\
  2022-06-02 14:15:35 +0300
  * Fixed cost calculation for SELECT STRAIGHT\_JOIN
* [Revision #e240e8d062](https://github.com/MariaDB/server/commit/e240e8d062)\
  2022-06-02 19:02:01 +0300
  * removed some compiler warnings
* [Revision #9e6fd2995b](https://github.com/MariaDB/server/commit/9e6fd2995b)\
  2022-06-07 10:53:33 +0300
  * [MDEV-25506](https://jira.mariadb.org/browse/MDEV-25506) fixup: Wait for TRUNCATE recovery
* [Revision #4b6f5aec55](https://github.com/MariaDB/server/commit/4b6f5aec55)\
  2022-06-07 08:33:50 +0300
  * main.mysqladmin: Prefer restarting to killing
* Merge [Revision #814c69ea30](https://github.com/MariaDB/server/commit/814c69ea30) 2022-06-06 17:41:46 +0300 - Merge remote-tracking branch 'origin/10.5' into 10.6
* [Revision #4179f93d28](https://github.com/MariaDB/server/commit/4179f93d28)\
  2022-06-06 14:05:01 +0300
  * [MDEV-18976](https://jira.mariadb.org/browse/MDEV-18976) Implement OPT\_PAGE\_CHECKSUM log record for improved validation
* [Revision #cc4eabc7b2](https://github.com/MariaDB/server/commit/cc4eabc7b2)\
  2022-06-06 14:04:45 +0300
  * [MDEV-13542](https://jira.mariadb.org/browse/MDEV-13542): Implement page read fault injection
* [Revision #0b47c126e3](https://github.com/MariaDB/server/commit/0b47c126e3)\
  2022-06-06 14:03:22 +0300
  * [MDEV-13542](https://jira.mariadb.org/browse/MDEV-13542): Crashing on corrupted page is unhelpful
* [Revision #75096c84b4](https://github.com/MariaDB/server/commit/75096c84b4)\
  2022-06-06 11:56:29 +0300
  * [MDEV-28525](https://jira.mariadb.org/browse/MDEV-28525) Some conditions around btr\_latch\_mode could be eliminated
* [Revision #aa45850687](https://github.com/MariaDB/server/commit/aa45850687)\
  2022-06-06 11:55:29 +0300
  * Cleanup: Make fil\_space\_t::freed\_ranges private
* [Revision #b29a8118dd](https://github.com/MariaDB/server/commit/b29a8118dd)\
  2022-06-06 11:54:17 +0300
  * Cleanup: Remove fil\_space\_t::magic\_n
* [Revision #c86d1daa62](https://github.com/MariaDB/server/commit/c86d1daa62)\
  2022-06-06 10:01:32 +0300
  * Cleanup: Remove some redundant reads
* [Revision #a98ac43649](https://github.com/MariaDB/server/commit/a98ac43649)\
  2022-06-06 09:58:42 +0300
  * [MDEV-28752](https://jira.mariadb.org/browse/MDEV-28752) Rollback of RENAME is broken if innodb\_file\_per\_table=0
* [Revision #1b03db11d2](https://github.com/MariaDB/server/commit/1b03db11d2)\
  2022-06-06 09:52:11 +0300
  * [MDEV-15528](https://jira.mariadb.org/browse/MDEV-15528) fixup: Remove some dead code
* Merge [Revision #2f8d0af883](https://github.com/MariaDB/server/commit/2f8d0af883) 2022-06-02 17:39:13 +0300 - Merge 10.5 into 10.6
* [Revision #a61603562e](https://github.com/MariaDB/server/commit/a61603562e)\
  2022-05-18 17:10:57 +0530
  * [MDEV-25875](https://jira.mariadb.org/browse/MDEV-25875): JSON\_TABLE: extract document fragment into JSON column
* [Revision #a9f6abedde](https://github.com/MariaDB/server/commit/a9f6abedde)\
  2021-05-31 13:48:09 +0400
  * [MDEV-25875](https://jira.mariadb.org/browse/MDEV-25875): JSON\_TABLE: extract document fragment into JSON column
* [Revision #6b6d745b9e](https://github.com/MariaDB/server/commit/6b6d745b9e)\
  2021-05-30 05:42:35 +0400
  * let numeric in the DEMAULT.
* Merge [Revision #05d049bdbe](https://github.com/MariaDB/server/commit/05d049bdbe) 2022-05-25 14:39:42 +0300 - Merge 10.5 into 10.6
* [Revision #db0fde3f24](https://github.com/MariaDB/server/commit/db0fde3f24)\
  2022-05-25 13:18:24 +0300
  * [MDEV-28665](https://jira.mariadb.org/browse/MDEV-28665) aio\_uring::thread\_routine terminates prematurely, causing hang
* Merge [Revision #57e66dc7e6](https://github.com/MariaDB/server/commit/57e66dc7e6) 2022-05-24 22:10:38 +0200 - Merge branch 'bb-10.6-release' into 10.6
* [Revision #e8cb91943c](https://github.com/MariaDB/server/commit/e8cb91943c)\
  2022-05-24 11:02:46 +0200
  * fix a bad merge in ec62f46a612b
* [Revision #771c61e965](https://github.com/MariaDB/server/commit/771c61e965)\
  2022-05-24 17:12:54 +1000
  * man: merge error in mysqld.8
* [Revision #571a8f4a08](https://github.com/MariaDB/server/commit/571a8f4a08)\
  2022-05-09 21:08:33 -0700
  * [MDEV-27892](https://jira.mariadb.org/browse/MDEV-27892) Improve an error message for foreign server exists (backport)
* Merge [Revision #a2bdd52835](https://github.com/MariaDB/server/commit/a2bdd52835) 2022-05-24 10:56:25 +1000 - Merge branch 10.5 into 10.6
* [Revision #443590406c](https://github.com/MariaDB/server/commit/443590406c)\
  2022-05-11 11:45:57 +0300
  * [MDEV-28376](https://jira.mariadb.org/browse/MDEV-28376): Make sure available Perl MariaDB DBI driver is chosen
* [Revision #99566fc894](https://github.com/MariaDB/server/commit/99566fc894)\
  2022-05-09 21:08:33 -0700
  * [MDEV-27892](https://jira.mariadb.org/browse/MDEV-27892) Improve an error message for foreign server exists
* [Revision #0d9aba05ec](https://github.com/MariaDB/server/commit/0d9aba05ec)\
  2022-05-24 08:54:14 +1000
  * [MDEV-28153](https://jira.mariadb.org/browse/MDEV-28153): Debian autobake to get control (postfix)
* [Revision #babb803222](https://github.com/MariaDB/server/commit/babb803222)\
  2022-05-23 14:38:56 +0200
  * [MDEV-28648](https://jira.mariadb.org/browse/MDEV-28648) main.ssl\_timeout fails with OpenSSL 3.0.3
* [Revision #78412ab028](https://github.com/MariaDB/server/commit/78412ab028)\
  2022-02-08 16:39:10 +0100
  * [MDEV-27778](https://jira.mariadb.org/browse/MDEV-27778) md5 in FIPS crashes with OpenSSL 3.0.0
* [Revision #987d16a0b4](https://github.com/MariaDB/server/commit/987d16a0b4)\
  2022-02-04 14:52:03 +0100
  * Revert "don't build with OpenSSL 3.0, it doesn't work before [MDEV-25785](https://jira.mariadb.org/browse/MDEV-25785)"
* [Revision #f0fa40efad](https://github.com/MariaDB/server/commit/f0fa40efad)\
  2021-11-08 18:48:19 +0100
  * [MDEV-25785](https://jira.mariadb.org/browse/MDEV-25785) Add support for OpenSSL 3.0
* Merge [Revision #e86c1e671a](https://github.com/MariaDB/server/commit/e86c1e671a) 2022-05-23 08:28:10 +0300 - Merge 10.5 into 10.6
* Merge [Revision #20d192bcfc](https://github.com/MariaDB/server/commit/20d192bcfc) 2022-05-20 19:31:48 +0200 - Merge branch '10.6' into bb-10.6-release
* [Revision #55266b05bd](https://github.com/MariaDB/server/commit/55266b05bd)\
  2022-05-20 12:31:26 -0400
  * bump the VERSION
* [Revision #06f043d717](https://github.com/MariaDB/server/commit/06f043d717)\
  2022-03-29 10:25:50 +0300
  * [MDEV-28191](https://jira.mariadb.org/browse/MDEV-28191): Suspend Lintian problems in mariadb-test-data package

{% @marketo/form formid="4316" formId="4316" %}
