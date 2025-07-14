# MariaDB 10.6.8 Changelog

The most recent release of [MariaDB 10.6](../../mariadb-10-6-series/what-is-mariadb-106.md) is:[**MariaDB 10.6.21**](../../mariadb-10-6-series/mariadb-10-6-21-release-notes.md) Stable (GA) [Download Now](https://mariadb.com/downloads/)[_Alternate download from mariadb.org_](https://downloads.mariadb.org/mariadb/10.6.21/)

[Download 10.6.8](https://mariadb.org/download/?tab=mariadb\&release=10.6.8\&product=mariadb)[Release Notes](../../mariadb-10-6-series/mariadb-1068-release-notes.md)[Changelog](mariadb-1068-changelog.md)[Overview of 10.6](../../mariadb-10-6-series/what-is-mariadb-106.md)

**Release date:** 20 May 2022

For the highlights of this release, see the[release notes](../../mariadb-10-6-series/mariadb-1068-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/server/tree/10.6) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Includes all fixes from [MariaDB 10.5.16](../changelogs-mariadb-105-series/mariadb-10516-changelog.md)
* Merge [Revision #b2187662bc](https://github.com/MariaDB/server/commit/b2187662bc) 2022-05-18 10:30:47 +0200 - Merge branch '10.5' into 10.6
* [Revision #98ca71ab28](https://github.com/MariaDB/server/commit/98ca71ab28)\
  2022-05-11 13:12:48 +0300
  * [MDEV-28461](https://jira.mariadb.org/browse/MDEV-28461) semisync-slave server recovery fails to rollback prepared transaction
* [Revision #e03e72234a](https://github.com/MariaDB/server/commit/e03e72234a)\
  2022-05-15 17:59:43 +0300
  * Fixed warning from UBSAN
* [Revision #f027c1217b](https://github.com/MariaDB/server/commit/f027c1217b)\
  2022-05-13 13:13:45 +0200
  * [MDEV-28471](https://jira.mariadb.org/browse/MDEV-28471) mysql\_install\_db.exe does not work with --innodb-page-size=64K
* [Revision #c1063a1bed](https://github.com/MariaDB/server/commit/c1063a1bed)\
  2022-04-22 06:34:12 -0700
  * [MDEV-28342](https://jira.mariadb.org/browse/MDEV-28342): sys.create\_synonym\_db fails when a temporary table masks a base table
* [Revision #b729896d00](https://github.com/MariaDB/server/commit/b729896d00)\
  2022-05-10 11:47:20 +0300
  * [MDEV-28073](https://jira.mariadb.org/browse/MDEV-28073) Query performance degradation in newer MariaDB versions when using many tables
* [Revision #f7dd8799e7](https://github.com/MariaDB/server/commit/f7dd8799e7)\
  2022-05-05 09:51:49 +0300
  * Fixed bug in alter\_table\_lock.result
* Merge [Revision #daa2680c78](https://github.com/MariaDB/server/commit/daa2680c78) 2022-05-12 08:11:57 +0300 - Merge 10.5 into 10.6
* [Revision #7da0f30ccc](https://github.com/MariaDB/server/commit/7da0f30ccc)\
  2022-05-11 14:48:51 +0400
  * [MDEV-28446](https://jira.mariadb.org/browse/MDEV-28446) mariadb-backup prepare fails for incrementals if a new schema is created after full backup is taken
* [Revision #a917be3e7f](https://github.com/MariaDB/server/commit/a917be3e7f)\
  2022-05-10 20:24:42 +0200
  * fix galera.[MDEV-26575](https://jira.mariadb.org/browse/MDEV-26575) failures
* Merge [Revision #3bc98a4ec4](https://github.com/MariaDB/server/commit/3bc98a4ec4) 2022-05-10 11:53:59 +0200 - Merge branch '10.5' into 10.6
* [Revision #f4d671bff2](https://github.com/MariaDB/server/commit/f4d671bff2)\
  2022-05-08 09:37:58 +0200
  * New CC (v3.2)
* [Revision #f67d65e331](https://github.com/MariaDB/server/commit/f67d65e331)\
  2022-05-06 11:23:13 +0300
  * [MDEV-28484](https://jira.mariadb.org/browse/MDEV-28484) InnoDB encryption key rotation is not being marked completed
* Merge [Revision #57a9626fe4](https://github.com/MariaDB/server/commit/57a9626fe4) 2022-05-06 11:11:04 +0300 - Merge 10.5 into 10.6
* [Revision #06a4193cc3](https://github.com/MariaDB/server/commit/06a4193cc3)\
  2022-05-04 04:58:02 -0500
  * [MDEV-28391](https://jira.mariadb.org/browse/MDEV-28391): table\_exists procedure fails when arguments contain escaped backticks as an quoted identifiers
* [Revision #bc113b873f](https://github.com/MariaDB/server/commit/bc113b873f)\
  2022-05-03 17:49:26 +0300
  * [MDEV-28465](https://jira.mariadb.org/browse/MDEV-28465) Some calls to btr\_pcur\_close() are unnecessary
* [Revision #c844a5881a](https://github.com/MariaDB/server/commit/c844a5881a)\
  2022-05-03 13:31:59 +0300
  * [MDEV-21452](https://jira.mariadb.org/browse/MDEV-21452) fixup: Remove an unused variable
* [Revision #caa985e6e6](https://github.com/MariaDB/server/commit/caa985e6e6)\
  2022-05-03 13:31:40 +0300
  * [MDEV-28454](https://jira.mariadb.org/browse/MDEV-28454) Latching order violation (and hang) in ibuf\_insert\_low
* [Revision #d8b943fb68](https://github.com/MariaDB/server/commit/d8b943fb68)\
  2022-05-02 13:13:18 +0530
  * [MDEV-28449](https://jira.mariadb.org/browse/MDEV-28449) Assertion \`index->lock.have\_x() == has\_index\_lock' failed in row\_log\_apply\_op
* [Revision #fc391df546](https://github.com/MariaDB/server/commit/fc391df546)\
  2022-04-28 15:15:37 +0530
  * [MDEV-28399](https://jira.mariadb.org/browse/MDEV-28399) Assertion failure in dict\_table\_check\_for\_dup\_indexes upon concurrent DML/DDL
* [Revision #a42e327afe](https://github.com/MariaDB/server/commit/a42e327afe)\
  2022-04-29 21:26:02 +0200
  * columnstore-6.3.1-1
* [Revision #2b4754f1b3](https://github.com/MariaDB/server/commit/2b4754f1b3)\
  2022-04-30 11:48:12 +0300
  * [MDEV-28445](https://jira.mariadb.org/browse/MDEV-28445) fixup: Restore submodules
* [Revision #b6e41e3872](https://github.com/MariaDB/server/commit/b6e41e3872)\
  2022-04-29 12:42:29 +0300
  * [MDEV-28445](https://jira.mariadb.org/browse/MDEV-28445) Secondary index locking invokes costly trx\_sys.get\_min\_trx\_id()
* [Revision #0f717d03b9](https://github.com/MariaDB/server/commit/0f717d03b9)\
  2022-04-29 13:34:53 +0530
  * [MDEV-28443](https://jira.mariadb.org/browse/MDEV-28443): [MDEV-15250](https://jira.mariadb.org/browse/MDEV-15250) causes latch order violation
* [Revision #8c1c61309d](https://github.com/MariaDB/server/commit/8c1c61309d)\
  2022-04-29 12:32:44 +0300
  * [MDEV-27274](https://jira.mariadb.org/browse/MDEV-27274): DROP TABLE does not delete detached InnoDB files
* [Revision #03e703fd74](https://github.com/MariaDB/server/commit/03e703fd74)\
  2022-04-27 09:08:01 +0200
  * Fix build dependency.
* [Revision #6350a52445](https://github.com/MariaDB/server/commit/6350a52445)\
  2022-04-27 09:54:42 +1000
  * tpool: liburing typo in error
* [Revision #2c005261cb](https://github.com/MariaDB/server/commit/2c005261cb)\
  2022-04-26 18:09:14 +0300
  * [MDEV-26753](https://jira.mariadb.org/browse/MDEV-26753) Assertion state == TRX\_STATE\_PREPARED ||... failed
* [Revision #2ca1123464](https://github.com/MariaDB/server/commit/2ca1123464)\
  2022-04-26 18:09:03 +0300
  * [MDEV-26217](https://jira.mariadb.org/browse/MDEV-26217) Failing assertion: list.count > 0 in ut\_list\_remove or Assertion \`lock->trx == this' failed in dberr\_t trx\_t::drop\_table
* [Revision #ec85e7b196](https://github.com/MariaDB/server/commit/ec85e7b196)\
  2022-04-21 18:14:58 +0200
  * [MDEV-28340](https://jira.mariadb.org/browse/MDEV-28340) Add tests for versioning, sequence, I\_S table
* [Revision #489011dd0f](https://github.com/MariaDB/server/commit/489011dd0f)\
  2021-04-26 23:56:13 +0100
  * [MDEV-28340](https://jira.mariadb.org/browse/MDEV-28340) Don't try to create temptables in system DBs, support table\_type='SYSTEM VIEW'
* [Revision #3fe656e629](https://github.com/MariaDB/server/commit/3fe656e629)\
  2021-04-26 23:24:18 +0100
  * [MDEV-28340](https://jira.mariadb.org/browse/MDEV-28340) On table\_type='SYSTEM VERSIONED' return 'BASE TABLE' instead of failing
* [Revision #81862dbb08](https://github.com/MariaDB/server/commit/81862dbb08)\
  2021-04-26 23:00:33 +0100
  * [MDEV-28340](https://jira.mariadb.org/browse/MDEV-28340) sys.table\_exists: support table\_type=SEQUENCE
* Merge [Revision #e135edec3a](https://github.com/MariaDB/server/commit/e135edec3a) 2022-04-26 15:21:20 +0300 - Merge 10.5 into 10.6
* [Revision #7725f870b0](https://github.com/MariaDB/server/commit/7725f870b0)\
  2022-04-26 15:13:39 +0300
  * [MDEV-15250](https://jira.mariadb.org/browse/MDEV-15250) fixup: Remove MY\_GNUC\_PREREQ
* [Revision #7c0b9c6020](https://github.com/MariaDB/server/commit/7c0b9c6020)\
  2022-04-26 16:18:45 +0530
  * [MDEV-15250](https://jira.mariadb.org/browse/MDEV-15250) UPSERT during ALTER TABLE results in 'Duplicate entry' error for alter
* [Revision #cad792c686](https://github.com/MariaDB/server/commit/cad792c686)\
  2022-04-26 06:11:33 +0200
  * [MDEV-28377](https://jira.mariadb.org/browse/MDEV-28377): galera\_as\_slave\_nonprim bind: Address already in use
* [Revision #4b80c11f52](https://github.com/MariaDB/server/commit/4b80c11f52)\
  2022-04-25 13:36:56 +0530
  * [MDEV-15250](https://jira.mariadb.org/browse/MDEV-15250) UPSERT during ALTER TABLE results in 'Duplicate entry' error for alter
* [Revision #4ed30b2ac5](https://github.com/MariaDB/server/commit/4ed30b2ac5)\
  2022-04-25 09:25:30 +0400
  * [MDEV-27690](https://jira.mariadb.org/browse/MDEV-27690) Crash on `CHARACTER SET csname COLLATE DEFAULT` in column definition
* Merge [Revision #fae0ccad6e](https://github.com/MariaDB/server/commit/fae0ccad6e) 2022-04-21 17:46:40 +0300 - Merge 10.5 into 10.6
* [Revision #1b558dd462](https://github.com/MariaDB/server/commit/1b558dd462)\
  2022-04-15 18:21:54 +0300
  * [MDEV-27919](https://jira.mariadb.org/browse/MDEV-27919) mariadb-backup --log-copy-interval is measured in millisecondss in 10.5 and in microseconds in 10.6
* [Revision #f0c52bfe3b](https://github.com/MariaDB/server/commit/f0c52bfe3b)\
  2022-04-21 17:18:41 +1000
  * [MDEV-28263](https://jira.mariadb.org/browse/MDEV-28263): mariadb-tzinfo-to-sql (postfix)
* [Revision #c47069ead7](https://github.com/MariaDB/server/commit/c47069ead7)\
  2022-04-21 16:49:15 +1000
  * [MDEV-28313](https://jira.mariadb.org/browse/MDEV-28313) InnoDB transactions are not aligned at cache lines (postfix)
* [Revision #b8398ee1fd](https://github.com/MariaDB/server/commit/b8398ee1fd)\
  2022-04-20 13:11:33 +1000
  * [MDEV-21208](https://jira.mariadb.org/browse/MDEV-21208): mysql\_tzinfo\_to\_sql does not work in strict mode
* [Revision #13e77930e6](https://github.com/MariaDB/server/commit/13e77930e6)\
  2022-04-06 13:12:21 +1000
  * [MDEV-28263](https://jira.mariadb.org/browse/MDEV-28263): mariadb-tzinfo-to-sql improve wsrep and binlog cases
* [Revision #d91c268096](https://github.com/MariaDB/server/commit/d91c268096)\
  2022-04-20 18:46:50 +0530
  * [MDEV-28370](https://jira.mariadb.org/browse/MDEV-28370) ASAN failure: InnoDB fails to free the memory allocated on dict\_load\_indexes()
* [Revision #d1edb011ee](https://github.com/MariaDB/server/commit/d1edb011ee)\
  2022-04-19 13:49:52 +0300
  * Cleanup: Remove os0thread
* Merge [Revision #7da351d804](https://github.com/MariaDB/server/commit/7da351d804) 2022-04-15 21:02:10 +0300 - Merge 10.5 into 10.6
* [Revision #2aed566d22](https://github.com/MariaDB/server/commit/2aed566d22)\
  2022-04-14 10:40:26 +0300
  * Cleanup: alignas(CPU\_LEVEL1\_DCACHE\_LINESIZE)
* [Revision #03f9bb8c90](https://github.com/MariaDB/server/commit/03f9bb8c90)\
  2022-04-14 10:21:43 +0300
  * [MDEV-28313](https://jira.mariadb.org/browse/MDEV-28313): Shrink ReadView::m\_mutex
* [Revision #8074ab5784](https://github.com/MariaDB/server/commit/8074ab5784)\
  2022-04-14 10:10:44 +0300
  * [MDEV-28313](https://jira.mariadb.org/browse/MDEV-28313): Shrink rw\_trx\_hash\_element\_t::mutex
* [Revision #0cd2e6c614](https://github.com/MariaDB/server/commit/0cd2e6c614)\
  2022-04-14 10:06:34 +0300
  * [MDEV-28313](https://jira.mariadb.org/browse/MDEV-28313): InnoDB transactions are not aligned at cache lines
* [Revision #f7f0bc748e](https://github.com/MariaDB/server/commit/f7f0bc748e)\
  2022-04-13 13:16:49 +0200
  * cleanup: un-inline dtype\_get\_mblen()
* [Revision #fc8396448c](https://github.com/MariaDB/server/commit/fc8396448c)\
  2022-04-13 00:49:22 +0200
  * [MDEV-27767](https://jira.mariadb.org/browse/MDEV-27767) poor scaling with InnoDB and utf8mb3 because of charset stats
* [Revision #5615a78a69](https://github.com/MariaDB/server/commit/5615a78a69)\
  2022-04-08 10:37:17 +0200
  * [MDEV-28266](https://jira.mariadb.org/browse/MDEV-28266) Crash in Field\_string::type\_handler when calling procedures
* Merge [Revision #cdc0bbdd87](https://github.com/MariaDB/server/commit/cdc0bbdd87) 2022-04-12 14:53:31 +0300 - Merge 10.5 into 10.6
* Merge [Revision #ca3bbf4c0c](https://github.com/MariaDB/server/commit/ca3bbf4c0c) 2022-04-12 09:26:02 +0300 - Merge 10.5 into 10.6
* [Revision #bc75f7ed6d](https://github.com/MariaDB/server/commit/bc75f7ed6d)\
  2022-02-10 14:52:32 +0200
  * [MDEV-28194](https://jira.mariadb.org/browse/MDEV-28194): Remove unneeded path from MariaDB server postinst script
* [Revision #840bab858b](https://github.com/MariaDB/server/commit/840bab858b)\
  2022-04-11 14:41:24 +0300
  * [MDEV-28289](https://jira.mariadb.org/browse/MDEV-28289) fts\_optimize\_sync\_table() is acquiring dict\_sys.latch while holding it
* [Revision #7bccf3dd74](https://github.com/MariaDB/server/commit/7bccf3dd74)\
  2022-04-11 10:22:40 +0300
  * [MDEV-28274](https://jira.mariadb.org/browse/MDEV-28274) Assertion s <= READ\_FIX failed in buf\_page\_t::set\_state
* [Revision #5a4a37076d](https://github.com/MariaDB/server/commit/5a4a37076d)\
  2022-04-08 18:54:26 +0200
  * [MDEV-10183](https://jira.mariadb.org/browse/MDEV-10183) implement service\_manager\_extend\_timeout on Windows
* [Revision #284ff64cd6](https://github.com/MariaDB/server/commit/284ff64cd6)\
  2022-04-10 14:46:24 +0400
  * 10.6 tests for [MDEV-26507](https://jira.mariadb.org/browse/MDEV-26507) Assertion \`tmp != ((long long) 0x8000000000000000LL)' failed in TIME\_from\_longlong\_datetime\_packed
* [Revision #d90c5ddd8b](https://github.com/MariaDB/server/commit/d90c5ddd8b)\
  2022-04-09 11:12:34 +0300
  * [MDEV-27234](https://jira.mariadb.org/browse/MDEV-27234) fixup: Add a result file
* [Revision #27b0030b9d](https://github.com/MariaDB/server/commit/27b0030b9d)\
  2022-04-04 13:00:03 +0530
  * [MDEV-27783](https://jira.mariadb.org/browse/MDEV-27783) InnoDB: Failing assertion: table->get\_ref\_count() == 0 upon ALTER TABLE ... MODIFY COLUMN
* [Revision #4e1ca38838](https://github.com/MariaDB/server/commit/4e1ca38838)\
  2022-04-06 12:51:27 +0300
  * [MDEV-26781](https://jira.mariadb.org/browse/MDEV-26781) InnoDB hangs when using SUX\_LOCK\_GENERIC
* Merge [Revision #ff99413804](https://github.com/MariaDB/server/commit/ff99413804) 2022-04-06 12:45:14 +0300 - [MDEV-25975](https://jira.mariadb.org/browse/MDEV-25975): Merge 10.5 into 10.6
* Merge [Revision #9d94c60f2b](https://github.com/MariaDB/server/commit/9d94c60f2b) 2022-04-06 12:08:30 +0300 - Merge 10.5 into 10.6
* [Revision #d6758efbe1](https://github.com/MariaDB/server/commit/d6758efbe1)\
  2021-10-21 14:49:51 +0300
  * [MDEV-23328](https://jira.mariadb.org/browse/MDEV-23328) Server hang due to Galera lock conflict resolution
* Merge [Revision #8d9c2561cd](https://github.com/MariaDB/server/commit/8d9c2561cd) 2022-04-05 10:08:44 +0300 - Merge 10.5 into 10.6
* [Revision #8c919330a7](https://github.com/MariaDB/server/commit/8c919330a7)\
  2022-03-26 14:55:44 -0700
  * Deb: Sync Salsa-CI from Debian [MariaDB 10.6](../../mariadb-10-6-series/what-is-mariadb-106.md)
* [Revision #28116ca361](https://github.com/MariaDB/server/commit/28116ca361)\
  2022-04-01 17:22:23 +1100
  * MDBF-348: innodb aix htm support
* Merge [Revision #0a573e7e63](https://github.com/MariaDB/server/commit/0a573e7e63) 2022-03-29 19:49:29 +0300 - Merge 10.5 into 10.6
* [Revision #792972a6f7](https://github.com/MariaDB/server/commit/792972a6f7)\
  2022-03-29 16:33:41 +0300
  * [MDEV-27234](https://jira.mariadb.org/browse/MDEV-27234) fixup with [MDEV-27557](https://jira.mariadb.org/browse/MDEV-27557)
* Merge [Revision #b242c3141f](https://github.com/MariaDB/server/commit/b242c3141f) 2022-03-29 16:16:21 +0300 - Merge 10.5 into 10.6
* [Revision #b2fa874e46](https://github.com/MariaDB/server/commit/b2fa874e46)\
  2022-03-28 11:35:10 +0300
  * [MDEV-28181](https://jira.mariadb.org/browse/MDEV-28181) The innochecksum -w option was inadvertently removed
* [Revision #8f8ba75855](https://github.com/MariaDB/server/commit/8f8ba75855)\
  2022-03-21 17:15:06 +0200
  * [MDEV-27234](https://jira.mariadb.org/browse/MDEV-27234): Data dictionary recovery was not READ COMMITTED
* [Revision #2ab9410843](https://github.com/MariaDB/server/commit/2ab9410843)\
  2022-03-28 08:34:17 +0300
  * Cleanup: Invoke sql\_print\_error() directly
* [Revision #a6dbb6b264](https://github.com/MariaDB/server/commit/a6dbb6b264)\
  2022-03-28 08:33:52 +0300
  * Fix main.create\_or\_replace better
* [Revision #f92388fa14](https://github.com/MariaDB/server/commit/f92388fa14)\
  2022-03-24 15:43:20 +0100
  * [MDEV-27900](https://jira.mariadb.org/browse/MDEV-27900) fixes
* [Revision #e9e6db9355](https://github.com/MariaDB/server/commit/e9e6db9355)\
  2022-03-25 09:23:16 +0200
  * Fix g++-12 -O2 -Wstringop-overflow
* [Revision #63f76d3b98](https://github.com/MariaDB/server/commit/63f76d3b98)\
  2022-03-18 17:36:53 +1100
  * Deb: enable pmem on riscv64
* [Revision #1b2ee693b7](https://github.com/MariaDB/server/commit/1b2ee693b7)\
  2022-03-18 12:20:09 +1100
  * [MDEV-28153](https://jira.mariadb.org/browse/MDEV-28153): Debian autobake- use absolute dependencies rather than a buildtime detection
* Merge [Revision #ec62f46a61](https://github.com/MariaDB/server/commit/ec62f46a61) 2022-03-25 11:31:49 +1100 - Merge 10.5 to 10.6
* [Revision #0da5f45a50](https://github.com/MariaDB/server/commit/0da5f45a50)\
  2022-03-22 16:52:00 +0530
  * [MDEV-27819](https://jira.mariadb.org/browse/MDEV-27819): func\_2.xxx\_charset skipped after renaming utf8 to utf8mb3
* [Revision #8684af76e3](https://github.com/MariaDB/server/commit/8684af76e3)\
  2022-03-24 16:09:04 +0200
  * [MDEV-28137](https://jira.mariadb.org/browse/MDEV-28137) Some memory transactions are unnecessarily complex
* [Revision #5ccd845d51](https://github.com/MariaDB/server/commit/5ccd845d51)\
  2022-02-10 19:17:06 +0200
  * [MDEV-27760](https://jira.mariadb.org/browse/MDEV-27760) event may non stop replicate in circular semisync setup
* [Revision #35725df6e2](https://github.com/MariaDB/server/commit/35725df6e2)\
  2022-03-22 03:23:32 +0100
  * [MDEV-27524](https://jira.mariadb.org/browse/MDEV-27524) addendum: fix for bug introduced by automatic migration
* [Revision #8840583a92](https://github.com/MariaDB/server/commit/8840583a92)\
  2022-03-18 10:52:08 +0200
  * [MDEV-27909](https://jira.mariadb.org/browse/MDEV-27909) InnoDB: Failing assertion: state == TRX\_STATE\_NOT\_STARTED ... on DDL
* Merge [Revision #065f995e6d](https://github.com/MariaDB/server/commit/065f995e6d) 2022-03-18 11:33:07 +1100 - Merge branch 10.5 into 10.6
* [Revision #ee80c19633](https://github.com/MariaDB/server/commit/ee80c19633)\
  2022-03-16 17:19:13 +0200
  * [MDEV-26551](https://jira.mariadb.org/browse/MDEV-26551) InnoDB crash on multiple concurrent SHOW TABLE STATUS
* [Revision #31ad9277fe](https://github.com/MariaDB/server/commit/31ad9277fe)\
  2022-03-16 14:30:36 +0530
  * [MDEV-28079](https://jira.mariadb.org/browse/MDEV-28079) Shutdown hangs after altering innodb partition fts table
* [Revision #b2c81e06b0](https://github.com/MariaDB/server/commit/b2c81e06b0)\
  2022-02-28 10:16:26 +1100
  * [MDEV-27955](https://jira.mariadb.org/browse/MDEV-27955) main.func\_json\_notembedded test fails on out-of-memory
* Merge [Revision #4ef44cc2f9](https://github.com/MariaDB/server/commit/4ef44cc2f9) 2022-03-15 14:49:24 +0200 - Merge 10.5 into 10.6
* [Revision #dafc5fb9c1](https://github.com/MariaDB/server/commit/dafc5fb9c1)\
  2022-02-04 03:56:08 +0000
  * [MDEV-27342](https://jira.mariadb.org/browse/MDEV-27342): Fix issue of recovery failure using new server id
* Merge [Revision #572e34304e](https://github.com/MariaDB/server/commit/572e34304e) 2022-03-14 10:59:46 +0200 - Merge 10.5 into 10.6
* [Revision #3b49967936](https://github.com/MariaDB/server/commit/3b49967936)\
  2022-03-14 08:01:40 +0200
  * [MDEV-28049](https://jira.mariadb.org/browse/MDEV-28049) Error on compiling trx0purge.cc
* [Revision #e0dc22b2d4](https://github.com/MariaDB/server/commit/e0dc22b2d4)\
  2022-03-11 20:17:01 +0100
  * [MDEV-27753](https://jira.mariadb.org/browse/MDEV-27753) Incorrect ENGINE type of table after crash for CONNECT table
* [Revision #f4fb6cb3fe](https://github.com/MariaDB/server/commit/f4fb6cb3fe)\
  2022-03-10 18:15:25 +1100
  * [MDEV-27900](https://jira.mariadb.org/browse/MDEV-27900): aio handle partial reads/writes (uring)
* Merge [Revision #bd1ba7801f](https://github.com/MariaDB/server/commit/bd1ba7801f) 2022-03-12 16:16:03 +1100 - Merge branch 10.5 into 10.6
* Merge [Revision #77c7390fc8](https://github.com/MariaDB/server/commit/77c7390fc8) 2022-03-11 14:36:50 +0200 - Merge 10.5 into 10.6
* Merge [Revision #42cb400562](https://github.com/MariaDB/server/commit/42cb400562) 2022-03-11 13:35:35 +0200 - Merge 10.5 into 10.6
* [Revision #2a4bba2743](https://github.com/MariaDB/server/commit/2a4bba2743)\
  2022-03-09 21:57:42 +0530
  * [MDEV-28030](https://jira.mariadb.org/browse/MDEV-28030) row\_discard\_tablespace\_for\_mysql() can unlock data dictionary without locking data dictionary
* [Revision #16c9eb5687](https://github.com/MariaDB/server/commit/16c9eb5687)\
  2022-03-09 18:17:10 +0530
  * [MDEV-27672](https://jira.mariadb.org/browse/MDEV-27672) Assertion \`!table->fts->in\_queue' failed in fts\_optimize\_remove\_table
* [Revision #9b8d9a1db3](https://github.com/MariaDB/server/commit/9b8d9a1db3)\
  2022-03-11 10:47:32 +0200
  * Fix main.create\_or\_replace
* Merge [Revision #be6f9593fe](https://github.com/MariaDB/server/commit/be6f9593fe) 2022-03-11 09:53:40 +0200 - Merge 10.5 into 10.6
* [Revision #fabaac86a1](https://github.com/MariaDB/server/commit/fabaac86a1)\
  2022-02-25 18:24:01 +1100
  * [MDEV-27956](https://jira.mariadb.org/browse/MDEV-27956) hardware lock ellision on s390x/ppc64{,le}
* [Revision #06ec439b8c](https://github.com/MariaDB/server/commit/06ec439b8c)\
  2022-03-10 15:23:28 +0200
  * [MDEV-27058](https://jira.mariadb.org/browse/MDEV-27058) fixup: Relax a debug assertion
* [Revision #36a19f94ce](https://github.com/MariaDB/server/commit/36a19f94ce)\
  2022-03-10 18:47:54 +1100
  * [MDEV-27936](https://jira.mariadb.org/browse/MDEV-27936) hardware lock elision on ppc64{,le} failing to compile
* [Revision #e8fc62b9d7](https://github.com/MariaDB/server/commit/e8fc62b9d7)\
  2022-03-02 11:48:24 +1100
  * [MDEV-27936](https://jira.mariadb.org/browse/MDEV-27936) hardware lock elision on ppc64{,le} failing to compile
* [Revision #c61249eef1](https://github.com/MariaDB/server/commit/c61249eef1)\
  2022-03-06 15:43:27 -0800
  * Fix failing Gitlab-CI by fixing CentOS 8 repo urls
* [Revision #ffb7f8854a](https://github.com/MariaDB/server/commit/ffb7f8854a)\
  2022-03-02 19:46:07 -0800
  * Fix failing Gitlab-CI by adding pcre2-devel as a build dependency
* [Revision #fbef100530](https://github.com/MariaDB/server/commit/fbef100530)\
  2022-03-08 09:04:48 +0200
  * Fix an uninitialized variable in debug builds
* [Revision #af345b72a9](https://github.com/MariaDB/server/commit/af345b72a9)\
  2022-03-08 09:04:24 +0200
  * [MDEV-27891](https://jira.mariadb.org/browse/MDEV-27891): Make the test work with debug builds
* [Revision #ed20e5b111](https://github.com/MariaDB/server/commit/ed20e5b111)\
  2022-03-08 09:04:03 +0200
  * After-merge fixes
* Merge [Revision #202316a38f](https://github.com/MariaDB/server/commit/202316a38f) 2022-03-07 18:42:47 +0300 - Merge 10.5 into 10.6
* [Revision #b6a2472489](https://github.com/MariaDB/server/commit/b6a2472489)\
  2022-02-22 17:42:59 +1100
  * [MDEV-27891](https://jira.mariadb.org/browse/MDEV-27891): SIGSEGV in InnoDB buffer pool resize
* [Revision #1fa872f6ef](https://github.com/MariaDB/server/commit/1fa872f6ef)\
  2022-03-02 18:18:43 -0800
  * Fix various spelling errors
* [Revision #2db80c3773](https://github.com/MariaDB/server/commit/2db80c3773)\
  2022-03-01 17:52:45 +0200
  * [MDEV-27973](https://jira.mariadb.org/browse/MDEV-27973) SIGSEGV in ha\_innobase::reset() after TRUNCATE of TEMPORARY TABLE
* Merge [Revision #d96433ad20](https://github.com/MariaDB/server/commit/d96433ad20) 2022-03-01 17:40:27 +0200 - Merge 10.5 into 10.6
* [Revision #fd5a6d0f75](https://github.com/MariaDB/server/commit/fd5a6d0f75)\
  2022-03-01 09:22:52 +0200
  * [MDEV-27964](https://jira.mariadb.org/browse/MDEV-27964): Test ENCRYPT() only in main.func\_crypt
* Merge [Revision #07f4a4a6d1](https://github.com/MariaDB/server/commit/07f4a4a6d1) 2022-03-01 09:15:25 +0200 - Merge 10.5 into 10.6
* Merge [Revision #edb311ae58](https://github.com/MariaDB/server/commit/edb311ae58) 2022-02-28 18:41:39 +0200 - Merge 10.5 into 10.6
* Merge [Revision #5c21cba602](https://github.com/MariaDB/server/commit/5c21cba602) 2022-02-28 14:14:23 +0200 - Merge 10.5 into 10.6
* Merge [Revision #6daf8f8a0d](https://github.com/MariaDB/server/commit/6daf8f8a0d) 2022-02-25 13:48:47 +0200 - Merge 10.5 into 10.6
* Merge [Revision #06eaca9b86](https://github.com/MariaDB/server/commit/06eaca9b86) 2022-02-25 12:15:16 +0200 - Merge 10.5 into 10.6 ([MDEV-27913](https://jira.mariadb.org/browse/MDEV-27913))
* Merge [Revision #e04b5eaa79](https://github.com/MariaDB/server/commit/e04b5eaa79) 2022-02-25 12:01:21 +0200 - Merge 10.5 into 10.6
* [Revision #83212632e4](https://github.com/MariaDB/server/commit/83212632e4)\
  2022-02-24 16:46:40 +0800
  * [MDEV-27935](https://jira.mariadb.org/browse/MDEV-27935): Enable performance\_schema profiling for trx\_rseg\_t latch
* Merge [Revision #164a6aa41c](https://github.com/MariaDB/server/commit/164a6aa41c) 2022-02-23 16:19:45 +0200 - Merge 10.5 into 10.6
* [Revision #d3e06dbbe3](https://github.com/MariaDB/server/commit/d3e06dbbe3)\
  2022-02-23 11:34:52 +0200
  * [MDEV-27924](https://jira.mariadb.org/browse/MDEV-27924) page\_zip\_copy\_recs() corrupts ROW\_FORMAT=COMPRESSED block descriptor
* Merge [Revision #92f79a22e6](https://github.com/MariaDB/server/commit/92f79a22e6) 2022-02-22 12:12:49 +0200 - Merge 10.5 into 10.6
* [Revision #120480d15b](https://github.com/MariaDB/server/commit/120480d15b)\
  2022-02-20 21:46:37 -0600
  * [MDEV-27394](https://jira.mariadb.org/browse/MDEV-27394) added memset to zero out addr.un.sun\_path string
* [Revision #4030a9fb2e](https://github.com/MariaDB/server/commit/4030a9fb2e)\
  2022-02-18 15:13:56 +0200
  * [MDEV-26476](https://jira.mariadb.org/browse/MDEV-26476): Implement futex for FreeBSD, DragonFly BSD
* Merge [Revision #f04b459fb7](https://github.com/MariaDB/server/commit/f04b459fb7) 2022-02-17 14:37:17 +0200 - Merge 10.5 into 10.6
* [Revision #8bc5bf2cb6](https://github.com/MariaDB/server/commit/8bc5bf2cb6)\
  2022-02-17 10:19:20 +0100
  * [MDEV-26789](https://jira.mariadb.org/browse/MDEV-26789) Fix stall of group commit waiters
* Merge [Revision #497809d26d](https://github.com/MariaDB/server/commit/497809d26d) 2022-02-15 11:32:15 +0300 - Merge 10.5 into 10.6
* Merge [Revision #f2f22c382b](https://github.com/MariaDB/server/commit/f2f22c382b) 2022-02-14 18:30:51 +0300 - Merge 10.5 into 10.6
* [Revision #7aa09af488](https://github.com/MariaDB/server/commit/7aa09af488)\
  2022-02-14 12:04:50 +0100
  * Fix whitespaces
* [Revision #e9e6b23987](https://github.com/MariaDB/server/commit/e9e6b23987)\
  2022-02-14 12:04:08 +0100
  * [MDEV-27828](https://jira.mariadb.org/browse/MDEV-27828) : Windows - major MSI upgrade fails, complaining that install directory not empty
* Merge [Revision #feb8004b58](https://github.com/MariaDB/server/commit/feb8004b58) 2022-02-14 09:16:41 +0200 - Merge 10.5 into 10.6
* [Revision #7b891008ce](https://github.com/MariaDB/server/commit/7b891008ce)\
  2022-02-13 17:33:40 +0200
  * [MDEV-27817](https://jira.mariadb.org/browse/MDEV-27817) InnoDB recovery of recently created files is not crash-safe
* Merge [Revision #f1e08eaa5d](https://github.com/MariaDB/server/commit/f1e08eaa5d) 2022-02-13 17:10:15 +0200 - Merge mariadb-10.6.7 into 10.6
* [Revision #d0e853b38e](https://github.com/MariaDB/server/commit/d0e853b38e)\
  2022-02-12 13:59:39 -0500
  * bump the VERSION
* [Revision #fb875055c6](https://github.com/MariaDB/server/commit/fb875055c6)\
  2022-02-11 18:10:50 +0800
  * [MDEV-27805](https://jira.mariadb.org/browse/MDEV-27805): tpcc workload shows regression with MDB-10.6

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
