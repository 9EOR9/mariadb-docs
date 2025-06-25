# MariaDB 10.6.12 Changelog

[Download](https://mariadb.com/downloads/)[Release Notes](../../mariadb-10-6-series/mariadb-10-6-12-release-notes.md)[Changelog](mariadb-10-6-12-changelog.md)[Overview of 10.6](../../mariadb-10-6-series/what-is-mariadb-106.md)

[_Alternate download from mariadb.org_](https://downloads.mariadb.org/mariadb/10.6.12/)

**Release date:** 6 Feb 2023

For the highlights of this release, see the[release notes](../../mariadb-10-6-series/mariadb-10-6-12-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/server/tree/10.6) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Includes all fixes from [MariaDB 10.5.19](../changelogs-mariadb-105-series/mariadb-10-5-19-changelog.md)
* [Revision #4c79e15cc3](https://github.com/MariaDB/server/commit/4c79e15cc3)\
  2023-02-01 15:57:22 +0100
  * [MDEV-30536](https://jira.mariadb.org/browse/MDEV-30536): no expected deadlock in galera\_insert\_bulk test
* [Revision #901870440b](https://github.com/MariaDB/server/commit/901870440b)\
  2023-02-01 14:05:00 +0100
  * Fix results in real ps-protocol:
* [Revision #1c926b6263](https://github.com/MariaDB/server/commit/1c926b6263)\
  2023-02-01 10:55:49 +0200
  * [MDEV-30527](https://jira.mariadb.org/browse/MDEV-30527) Assertion !m\_freed\_pages in mtr\_t::start() on DROP TEMPORARY TABLE
* [Revision #ccafd2d49d](https://github.com/MariaDB/server/commit/ccafd2d49d)\
  2023-01-31 16:38:11 +0200
  * [MDEV-30524](https://jira.mariadb.org/browse/MDEV-30524) btr\_cur\_t::open\_leaf() opens non-leaf page in BTR\_MODIFY\_LEAF mode
* Merge [Revision #c3a5cf2b5b](https://github.com/MariaDB/server/commit/c3a5cf2b5b) 2023-01-31 09:31:42 +0100 - Merge branch '10.5' into 10.6
* [Revision #81196469bb](https://github.com/MariaDB/server/commit/81196469bb)\
  2023-01-25 12:36:57 +0530
  * [MDEV-30429](https://jira.mariadb.org/browse/MDEV-30429) InnoDB: Failing assertion: stat\_value != UINT64\_UNDEFINED in storage/innobase/dict/dict0stats.cc line 3647
* [Revision #82b18a8361](https://github.com/MariaDB/server/commit/82b18a8361)\
  2023-01-25 10:56:07 +0200
  * [MDEV-29374](https://jira.mariadb.org/browse/MDEV-29374) fixup: Suppress an error in a test
* [Revision #509c7f66bd](https://github.com/MariaDB/server/commit/509c7f66bd)\
  2023-01-24 14:36:54 +0200
  * [MDEV-27977](https://jira.mariadb.org/browse/MDEV-27977) : galera.galera\_UK\_conflict fails with wrong result
* [Revision #15226a2822](https://github.com/MariaDB/server/commit/15226a2822)\
  2023-01-24 16:29:17 +0100
  * Add missing include for std::runtime\_error
* [Revision #de4030e4d4](https://github.com/MariaDB/server/commit/de4030e4d4)\
  2023-01-24 14:09:21 +0200
  * [MDEV-30400](https://jira.mariadb.org/browse/MDEV-30400) Assertion height == btr\_page\_get\_level(...) on INSERT
* [Revision #39f4674599](https://github.com/MariaDB/server/commit/39f4674599)\
  2022-12-05 17:03:32 +0300
  * [MDEV-24623](https://jira.mariadb.org/browse/MDEV-24623) Replicate bulk insert as table-level exclusive key
* [Revision #a10003bd68](https://github.com/MariaDB/server/commit/a10003bd68)\
  2023-01-24 13:31:07 +1100
  * rpm: ignore man3
* [Revision #ef6b3806bb](https://github.com/MariaDB/server/commit/ef6b3806bb)\
  2023-01-23 18:06:13 +0530
  * [MDEV-30393](https://jira.mariadb.org/browse/MDEV-30393) InnoDB: Assertion failure in dict0dict.cc upon ADD FULLTEXT INDEX
* [Revision #8c2dcfab03](https://github.com/MariaDB/server/commit/8c2dcfab03)\
  2023-01-23 12:54:13 +0200
  * Update 10.6 HELP tables
* [Revision #e41fb3697c](https://github.com/MariaDB/server/commit/e41fb3697c)\
  2023-01-23 14:52:49 +0200
  * Revert "[MDEV-30400](https://jira.mariadb.org/browse/MDEV-30400) Assertion height == btr\_page\_get\_level(...) on INSERT"
* Merge [Revision #851c56771e](https://github.com/MariaDB/server/commit/851c56771e) 2023-01-23 13:15:41 +0200 - Merge 10.5 into 10.6
* [Revision #1bbf37e0db](https://github.com/MariaDB/server/commit/1bbf37e0db)\
  2023-01-23 13:05:52 +0200
  * [MDEV-515](https://jira.mariadb.org/browse/MDEV-515): Improve test coverage
* [Revision #f9cac8d2cb](https://github.com/MariaDB/server/commit/f9cac8d2cb)\
  2023-01-19 17:19:18 +0200
  * [MDEV-30400](https://jira.mariadb.org/browse/MDEV-30400) Assertion height == btr\_page\_get\_level(...) on INSERT
* [Revision #67dc8af2a7](https://github.com/MariaDB/server/commit/67dc8af2a7)\
  2023-01-19 16:10:29 +0200
  * [MDEV-30289](https://jira.mariadb.org/browse/MDEV-30289): Implement small\_vector for mtr\_t::m\_memo
* [Revision #7fa5cce305](https://github.com/MariaDB/server/commit/7fa5cce305)\
  2023-01-19 16:10:18 +0200
  * [MDEV-30289](https://jira.mariadb.org/browse/MDEV-30289): Remove the pointer indirection for mtr\_t::m\_memo
* Merge [Revision #a01abad619](https://github.com/MariaDB/server/commit/a01abad619) 2023-01-18 16:33:06 +0100 - Merge branch '10.5' into 10.6
* Merge [Revision #a8c5635cf1](https://github.com/MariaDB/server/commit/a8c5635cf1) 2023-01-17 20:02:29 +0200 - Merge 10.5 into 10.6
* [Revision #95de5248c7](https://github.com/MariaDB/server/commit/95de5248c7)\
  2022-06-17 15:16:23 +0300
  * [MDEV-26391](https://jira.mariadb.org/browse/MDEV-26391) BF abortable mariadb-backup execution
* Merge [Revision #3386b30975](https://github.com/MariaDB/server/commit/3386b30975) 2023-01-13 10:45:41 +0200 - Merge 10.5 into 10.6
* [Revision #5aa58a0d39](https://github.com/MariaDB/server/commit/5aa58a0d39)\
  2023-01-12 15:14:37 +0100
  * [MDEV-30374](https://jira.mariadb.org/browse/MDEV-30374) Windows, MSI - do not cache error, if install directory changes.
* Merge [Revision #56c9b0bca0](https://github.com/MariaDB/server/commit/56c9b0bca0) 2023-01-10 13:54:17 +0200 - Merge 10.5 into 10.6
* [Revision #12a85c6caf](https://github.com/MariaDB/server/commit/12a85c6caf)\
  2023-01-05 11:06:35 +0530
  * [MDEV-30346](https://jira.mariadb.org/browse/MDEV-30346) Avoid block device required error in innodb\_fts.misc\_debug
* [Revision #fe38d7cad4](https://github.com/MariaDB/server/commit/fe38d7cad4)\
  2023-01-04 10:04:58 +0200
  * Remove redundant statements from a test
* Merge [Revision #e441c32a0b](https://github.com/MariaDB/server/commit/e441c32a0b) 2023-01-03 18:13:11 +0200 - Merge 10.5 into 10.6
* [Revision #fce80b6ae1](https://github.com/MariaDB/server/commit/fce80b6ae1)\
  2022-12-24 18:53:16 +0100
  * sporadic failures of perfschema.statement\_program\_concurrency
* [Revision #5e3c948cc9](https://github.com/MariaDB/server/commit/5e3c948cc9)\
  2022-11-18 18:22:19 +0100
  * [MDEV-29852](https://jira.mariadb.org/browse/MDEV-29852) SIGSEGV in mysql\_create\_routine or is\_acl\_user on 2nd execution, ASAN use-after-poison in get\_current\_user (sql\_acl.cc)
* [Revision #4493642e4c](https://github.com/MariaDB/server/commit/4493642e4c)\
  2022-12-22 12:47:45 +0200
  * [MDEV-29562](https://jira.mariadb.org/browse/MDEV-29562) fixup: ASAN global-buffer-overflow
* [Revision #5cec83476d](https://github.com/MariaDB/server/commit/5cec83476d)\
  2022-12-21 13:41:10 +0200
  * [MDEV-29896](https://jira.mariadb.org/browse/MDEV-29896): mariadb-backup --backup --incremental --throttle=... hangs
* [Revision #5eb545e5c2](https://github.com/MariaDB/server/commit/5eb545e5c2)\
  2022-12-07 20:19:05 +1100
  * [MDEV-29562](https://jira.mariadb.org/browse/MDEV-29562) Spider table charset error should happen correctly.
* [Revision #76c2402812](https://github.com/MariaDB/server/commit/76c2402812)\
  2022-12-09 00:26:20 +0000
  * Fix build failure in sanitizer on GitLab-CI
* [Revision #0a67daad06](https://github.com/MariaDB/server/commit/0a67daad06)\
  2022-12-15 16:18:43 +0200
  * [MDEV-30235](https://jira.mariadb.org/browse/MDEV-30235) InnoDB crash on table-rebuilding DDL when the statistics tables are corrupted
* Merge [Revision #4f6830255c](https://github.com/MariaDB/server/commit/4f6830255c) 2022-12-15 16:18:28 +0200 - Merge 10.5 into 10.6
* [Revision #4ca5a0ec98](https://github.com/MariaDB/server/commit/4ca5a0ec98)\
  2022-12-15 19:05:08 +1100
  * [MDEV-30172](https://jira.mariadb.org/browse/MDEV-30172): galera mtr disables
* Merge [Revision #fa01ffb08e](https://github.com/MariaDB/server/commit/fa01ffb08e) 2022-12-15 18:27:11 +1100 - Merge branch '10.5' into 10.6
* Merge [Revision #7df06dcbc3](https://github.com/MariaDB/server/commit/7df06dcbc3) 2022-12-15 09:32:54 +1100 - Merge branch 10.5 into 10.6
* Merge [Revision #4b2e7616f8](https://github.com/MariaDB/server/commit/4b2e7616f8) 2022-12-14 12:25:57 +1100 - Merge branch '10.5' into 10.6
* Merge [Revision #a8a5c8a1b8](https://github.com/MariaDB/server/commit/a8a5c8a1b8) 2022-12-13 16:58:58 +0200 - Merge 10.5 into 10.6
* Merge [Revision #04efe13501](https://github.com/MariaDB/server/commit/04efe13501) 2022-12-13 12:59:17 +1100 - Merge branch '10.5' into 10.6
* Merge [Revision #3b249a6e56](https://github.com/MariaDB/server/commit/3b249a6e56) 2022-12-13 10:28:19 +1100 - Merge branch '10.5' into 10.6
* [Revision #1862273c43](https://github.com/MariaDB/server/commit/1862273c43)\
  2022-12-12 11:41:12 +0200
  * [MDEV-30209](https://jira.mariadb.org/browse/MDEV-30209) Race condition between fil\_node\_open\_file() and renaming files
* [Revision #cf437f6be9](https://github.com/MariaDB/server/commit/cf437f6be9)\
  2022-12-12 08:07:47 +0200
  * Fix GCC -Og -Wmaybe-uninitialized
* [Revision #c4d7939989](https://github.com/MariaDB/server/commit/c4d7939989)\
  2022-12-12 07:54:38 +0200
  * [MDEV-30180](https://jira.mariadb.org/browse/MDEV-30180) Server hang with innodb\_undo\_log\_truncate=ON
* [Revision #dd5f4b3625](https://github.com/MariaDB/server/commit/dd5f4b3625)\
  2022-12-08 12:10:58 +0200
  * Fixed bug in Aria when used with enterprise mariadb-backup
* [Revision #9044e016c5](https://github.com/MariaDB/server/commit/9044e016c5)\
  2022-12-06 13:31:11 +0100
  * [MDEV-29822](https://jira.mariadb.org/browse/MDEV-29822) - disable a test that fails sporadically
* Merge [Revision #e55397a46d](https://github.com/MariaDB/server/commit/e55397a46d) 2022-12-05 18:04:23 +0200 - Merge 10.5 into 10.6
* [Revision #0a7d85c97f](https://github.com/MariaDB/server/commit/0a7d85c97f)\
  2022-12-05 18:00:22 +0200
  * [MDEV-30148](https://jira.mariadb.org/browse/MDEV-30148) Race condition between non-persistent statistics and purge
* [Revision #95d71272ef](https://github.com/MariaDB/server/commit/95d71272ef)\
  2022-11-11 14:21:56 -0800
  * Gitlab-CI: Upgrade Fedora build always use latest (now 37) version
* [Revision #e0dbec1ce3](https://github.com/MariaDB/server/commit/e0dbec1ce3)\
  2022-12-02 18:21:52 +0300
  * [MDEV-29129](https://jira.mariadb.org/browse/MDEV-29129): Performance regression starting in 10.6: select order by limit ...
* [Revision #072b3668ca](https://github.com/MariaDB/server/commit/072b3668ca)\
  2022-11-29 15:19:37 +1100
  * [MDEV-28206](https://jira.mariadb.org/browse/MDEV-28206): SIGSEGV in Item\_field::fix\_fields when using LEAD...OVER
* [Revision #4783f37cf7](https://github.com/MariaDB/server/commit/4783f37cf7)\
  2022-11-30 12:06:52 +0200
  * [MDEV-30069](https://jira.mariadb.org/browse/MDEV-30069) fixup: Do not truncate files on recovery
* [Revision #15ab2e122d](https://github.com/MariaDB/server/commit/15ab2e122d)\
  2022-11-30 10:54:03 +0200
  * [MDEV-30132](https://jira.mariadb.org/browse/MDEV-30132) Crash after recovery, with InnoDB: Tried to read ...
* [Revision #fc1403d3a9](https://github.com/MariaDB/server/commit/fc1403d3a9)\
  2022-11-30 10:41:11 +0200
  * Cleanup: Remove fil\_space\_t::is\_deferred()
* [Revision #1188ef4ade](https://github.com/MariaDB/server/commit/1188ef4ade)\
  2022-11-30 10:35:40 +0200
  * [MDEV-30132](https://jira.mariadb.org/browse/MDEV-30132) Crash after recovery, with InnoDB: Tried to read ... bytes at offset
* Merge [Revision #d32b2e7e8e](https://github.com/MariaDB/server/commit/d32b2e7e8e) 2022-11-30 08:32:57 +0200 - Merge 10.5 into 10.6
* Merge [Revision #c59985fcf5](https://github.com/MariaDB/server/commit/c59985fcf5) 2022-11-30 07:06:41 +0200 - Merge 10.5 into 10.6
* [Revision #bb29712b45](https://github.com/MariaDB/server/commit/bb29712b45)\
  2022-11-29 17:19:30 +0530
  * [MDEV-30119](https://jira.mariadb.org/browse/MDEV-30119) INFORMATION\_SCHEMA.INNODB\_TABLESPACES\_ENCRYPTION.NAME is NULL for undo tablespaces
* [Revision #c1de3776a6](https://github.com/MariaDB/server/commit/c1de3776a6)\
  2022-11-29 05:08:14 -0800
  * Extend GitLab CI with build and test jobs for sanitizers (#2174)
* Merge [Revision #fdc582fd98](https://github.com/MariaDB/server/commit/fdc582fd98) 2022-11-28 12:20:17 +0200 - Merge 10.5 into 10.6
* [Revision #05cd10b74c](https://github.com/MariaDB/server/commit/05cd10b74c)\
  2022-11-24 16:46:34 +0200
  * [MDEV-29603](https://jira.mariadb.org/browse/MDEV-29603) fixup: GCC -Wunused-but-set-variable
* [Revision #604e844944](https://github.com/MariaDB/server/commit/604e844944)\
  2022-11-24 15:04:25 +0200
  * [MDEV-21452](https://jira.mariadb.org/browse/MDEV-21452) fixup: Remove PFS\_NOT\_INSTRUMENTED
* [Revision #36fcca635e](https://github.com/MariaDB/server/commit/36fcca635e)\
  2022-11-23 17:20:59 +0200
  * Fixed a memory leak in aria\_read\_log
* Merge [Revision #6d40274f65](https://github.com/MariaDB/server/commit/6d40274f65) 2022-11-23 18:13:28 +0200 - Merge 10.5 into 10.6
* [Revision #46f8c46e94](https://github.com/MariaDB/server/commit/46f8c46e94)\
  2022-11-22 15:00:26 +0200
  * [MDEV-30069](https://jira.mariadb.org/browse/MDEV-30069) InnoDB: Trying to write ... bytes at ... outside the bounds
* Merge [Revision #377ec1b5c9](https://github.com/MariaDB/server/commit/377ec1b5c9) 2022-11-21 12:23:58 +0100 - Merge branch '10.5' into 10.6
* [Revision #2a4bd038f7](https://github.com/MariaDB/server/commit/2a4bd038f7)\
  2022-11-21 11:14:54 +0100
  * [MDEV-30055](https://jira.mariadb.org/browse/MDEV-30055) - fix race condition in shutdown\_debug.test
* Merge [Revision #6b083ce851](https://github.com/MariaDB/server/commit/6b083ce851) 2022-11-20 11:35:09 +0200 - Merge 10.5 into 10.6
* Merge [Revision #9aea7d83c8](https://github.com/MariaDB/server/commit/9aea7d83c8) 2022-11-17 08:37:35 +0200 - Merge 10.5 into 10.6
* [Revision #24fe53477c](https://github.com/MariaDB/server/commit/24fe53477c)\
  2022-11-17 08:19:01 +0200
  * [MDEV-29603](https://jira.mariadb.org/browse/MDEV-29603) btr\_cur\_open\_at\_index\_side() is missing some consistency checks
* [Revision #89ec4b53ac](https://github.com/MariaDB/server/commit/89ec4b53ac)\
  2022-11-16 09:43:48 +0200
  * [MDEV-29603](https://jira.mariadb.org/browse/MDEV-29603): Implement btr\_cur\_t::open\_leaf()
* [Revision #6b2d6a81d4](https://github.com/MariaDB/server/commit/6b2d6a81d4)\
  2022-11-10 18:26:33 +0200
  * Cleanup: Remove btr\_pcur\_t::old\_stored
* [Revision #8442bc6e13](https://github.com/MariaDB/server/commit/8442bc6e13)\
  2022-11-10 18:18:58 +0200
  * Cleanup: Remove an unnecessary page lookup
* [Revision #a5ed56cd4f](https://github.com/MariaDB/server/commit/a5ed56cd4f)\
  2022-11-10 18:18:48 +0200
  * Cleanup: Remove BTR\_MODIFY\_EXTERNAL
* [Revision #af7bd64edb](https://github.com/MariaDB/server/commit/af7bd64edb)\
  2022-11-10 18:18:40 +0200
  * Cleanup: Use BTR\_INSERT\_TREE for pessimistic insert
* [Revision #b363d9758a](https://github.com/MariaDB/server/commit/b363d9758a)\
  2022-11-10 18:18:30 +0200
  * Cleanup: Use the alias BTR\_PURGE\_TREE for pessimistic delete
* Merge [Revision #ae6ebafd81](https://github.com/MariaDB/server/commit/ae6ebafd81) 2022-11-14 15:44:55 +0200 - Merge 10.5 into 10.6
* [Revision #c82f3f1b04](https://github.com/MariaDB/server/commit/c82f3f1b04)\
  2022-11-14 13:08:00 +0200
  * [MDEV-29978](https://jira.mariadb.org/browse/MDEV-29978) Corruption errors upon CHECK on temporary InnoDB table
* [Revision #704c74cd99](https://github.com/MariaDB/server/commit/704c74cd99)\
  2022-11-14 16:08:13 +0530
  * [MDEV-29987](https://jira.mariadb.org/browse/MDEV-29987) Bogus errors about file size in the test mariadb-backup.defer\_space
* [Revision #505da21e33](https://github.com/MariaDB/server/commit/505da21e33)\
  2022-11-11 12:28:44 +0400
  * [MDEV-27214](https://jira.mariadb.org/browse/MDEV-27214) Import with disabled keys corrupts meta-data like rows, indexes, ...
* [Revision #f4adf35474](https://github.com/MariaDB/server/commit/f4adf35474)\
  2022-11-10 23:51:34 -0800
  * Misc Debian/Salsa-CI fixes (#2299)
* [Revision #67f4ba240e](https://github.com/MariaDB/server/commit/67f4ba240e)\
  2022-11-10 17:30:55 +0200
  * [MDEV-29996](https://jira.mariadb.org/browse/MDEV-29996) Duplicated call to buf\_page\_t::set\_ibuf\_exist() on recovery
* Merge [Revision #da21f3f428](https://github.com/MariaDB/server/commit/da21f3f428) 2022-11-10 17:30:15 +0200 - Merge 10.5 into 10.6
* [Revision #fef9d6ef1d](https://github.com/MariaDB/server/commit/fef9d6ef1d)\
  2022-11-10 09:21:51 +0200
  * Add STATS\_PERSISTENT=0 to a test
* [Revision #6b671aeee3](https://github.com/MariaDB/server/commit/6b671aeee3)\
  2022-11-10 08:54:57 +0200
  * [MDEV-29710](https://jira.mariadb.org/browse/MDEV-29710): Disable some more tests on Valgrind
* [Revision #a75ec07b42](https://github.com/MariaDB/server/commit/a75ec07b42)\
  2022-11-09 16:45:36 +0200
  * [MDEV-27234](https://jira.mariadb.org/browse/MDEV-27234) fixup: Remove a bogus assertion
* [Revision #e56c12b3cd](https://github.com/MariaDB/server/commit/e56c12b3cd)\
  2022-11-09 12:02:04 +0200
  * Add an end marker to a test
* Merge [Revision #ab44e1f87c](https://github.com/MariaDB/server/commit/ab44e1f87c) 2022-11-09 09:32:58 +0200 - Merge 10.5 into 10.6
* Merge [Revision #2ac1edb1c3](https://github.com/MariaDB/server/commit/2ac1edb1c3) 2022-11-08 17:37:22 +0200 - Merge 10.5 into 10.6
* [Revision #e572c745dc](https://github.com/MariaDB/server/commit/e572c745dc)\
  2022-11-08 17:34:34 +0200
  * [MDEV-29504](https://jira.mariadb.org/browse/MDEV-29504)/[MDEV-29849](https://jira.mariadb.org/browse/MDEV-29849) TRUNCATE breaks FOREIGN KEY locking
* [Revision #f4519fb772](https://github.com/MariaDB/server/commit/f4519fb772)\
  2022-11-07 17:14:07 +0530
  * [MDEV-28797](https://jira.mariadb.org/browse/MDEV-28797) Assertion \`page\_rec\_is\_user\_rec(rec)' failed in PageBulk::getSplitRec
* [Revision #db85d8b093](https://github.com/MariaDB/server/commit/db85d8b093)\
  2022-11-03 18:47:14 +0530
  * [MDEV-29853](https://jira.mariadb.org/browse/MDEV-29853) Assertion \`!strstr(table->name.m\_name, "/FTS\_") || purge\_sys.must\_wait\_FTS()' failed in trx\_t::commit
* [Revision #689e951227](https://github.com/MariaDB/server/commit/689e951227)\
  2022-10-31 13:34:25 +0530
  * [MDEV-29518](https://jira.mariadb.org/browse/MDEV-29518) ASAN Failure on i\_s query when tablespace does rename operation
* [Revision #e3a5a69524](https://github.com/MariaDB/server/commit/e3a5a69524)\
  2022-11-08 08:02:18 +0100
  * [MDEV-29822](https://jira.mariadb.org/browse/MDEV-29822) - make mysqltest fail loudly when out of memory
* Merge [Revision #c4ce012e4b](https://github.com/MariaDB/server/commit/c4ce012e4b) 2022-11-07 16:33:00 +0100 - Merge branch '10.6' into bb-10.6-release
* [Revision #118d39d3ee](https://github.com/MariaDB/server/commit/118d39d3ee)\
  2022-11-07 09:45:23 -0500
  * bump the VERSION
* [Revision #18a0f0c178](https://github.com/MariaDB/server/commit/18a0f0c178)\
  2022-10-19 16:41:24 +1100
  * Fix AIX compulation (break addr resolution)

{% include "https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/~/reusable/vX1KAy0t1XuYJaGsK28T/" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
