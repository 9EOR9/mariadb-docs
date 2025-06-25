# MariaDB 10.6.15 Changelog

The most recent release of [MariaDB 10.6](../../mariadb-10-6-series/what-is-mariadb-106.md) is:[**MariaDB 10.6.21**](../../mariadb-10-6-series/mariadb-10-6-21-release-notes.md) Stable (GA) [Download Now](https://mariadb.com/downloads/)[_Alternate download from mariadb.org_](https://downloads.mariadb.org/mariadb/10.6.21/)

[Download 10.6.15](https://downloads.mariadb.org/mariadb/10.6.15/)[Release Notes](../../mariadb-10-6-series/mariadb-10-6-15-release-notes.md)[Changelog](mariadb-10-6-15-changelog.md)[Overview of 10.6](../../mariadb-10-6-series/what-is-mariadb-106.md)

**Release date:** 14 Aug 2023

For the highlights of this release, see the[release notes](../../mariadb-10-6-series/mariadb-10-6-15-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/server/tree/10.6) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Includes all fixes from [MariaDB 10.5.22](../changelogs-mariadb-105-series/mariadb-10-5-22-changelog.md)
* [Revision #8d210fc2aa](https://github.com/MariaDB/server/commit/8d210fc2aa)\
  2023-08-09 15:47:06 +0300
  * [MDEV-31877](https://jira.mariadb.org/browse/MDEV-31877): ASAN errors in Exec\_time\_tracker::get\_cycles with innodb slow log verbosity
* Merge [Revision #d28d636f57](https://github.com/MariaDB/server/commit/d28d636f57) 2023-08-08 13:20:58 +0200 - Merge branch '10.5' into 10.6
* Merge [Revision #4bc9d50f2f](https://github.com/MariaDB/server/commit/4bc9d50f2f) 2023-08-07 10:32:05 +0200 - Merge branch '10.5' into 10.6
* Merge [Revision #c7b6707fe1](https://github.com/MariaDB/server/commit/c7b6707fe1) 2023-08-04 12:14:00 +0200 - Merge branch '10.5' into 10.6
* [Revision #6eb69434c7](https://github.com/MariaDB/server/commit/6eb69434c7)\
  2023-08-04 10:30:30 +0200
  * Roksdb test postmerge fix
* [Revision #9aef479ac8](https://github.com/MariaDB/server/commit/9aef479ac8)\
  2023-08-04 10:24:40 +0200
  * fix postmerge view protocol test
* [Revision #6b8310c27a](https://github.com/MariaDB/server/commit/6b8310c27a)\
  2023-08-04 10:11:03 +0200
  * fix postmerge 32bit tests
* Merge [Revision #5ea5291d97](https://github.com/MariaDB/server/commit/5ea5291d97) 2023-08-02 20:20:50 +0200 - Merge branch '10.5' into 10.6
* [Revision #691e964d23](https://github.com/MariaDB/server/commit/691e964d23)\
  2023-08-01 13:29:06 +0300
  * [MDEV-31764](https://jira.mariadb.org/browse/MDEV-31764): ASAN use-after-poison in trace\_engine\_stats in ANALYZE JSON
* [Revision #138717b16f](https://github.com/MariaDB/server/commit/138717b16f)\
  2023-08-01 16:40:10 +0200
  * New CC 3.3
* Merge [Revision #6bf8483cac](https://github.com/MariaDB/server/commit/6bf8483cac) 2023-08-01 15:08:52 +0200 - Merge branch '10.5' into 10.6
* [Revision #72928e640e](https://github.com/MariaDB/server/commit/72928e640e)\
  2023-08-01 14:39:29 +0300
  * [MDEV-27593](https://jira.mariadb.org/browse/MDEV-27593): Crashing on I/O error is unhelpful
* [Revision #96cfdb8710](https://github.com/MariaDB/server/commit/96cfdb8710)\
  2023-08-01 13:22:16 +0300
  * [MDEV-31816](https://jira.mariadb.org/browse/MDEV-31816) fixup: Relax a debug assertion
* [Revision #d794d3484b](https://github.com/MariaDB/server/commit/d794d3484b)\
  2023-08-01 09:58:15 +0300
  * [MDEV-31816](https://jira.mariadb.org/browse/MDEV-31816) buf\_LRU\_free\_page() does not preserve ROW\_FORMAT=COMPRESSED block state
* [Revision #0d175968d1](https://github.com/MariaDB/server/commit/0d175968d1)\
  2023-07-28 12:36:45 +0300
  * [MDEV-31354](https://jira.mariadb.org/browse/MDEV-31354) SIGSEGV in log\_sort\_flush\_list() in InnoDB crash recovery
* [Revision #b102872ad5](https://github.com/MariaDB/server/commit/b102872ad5)\
  2023-07-25 11:40:58 +0300
  * [MDEV-31767](https://jira.mariadb.org/browse/MDEV-31767) InnoDB tables are being flagged as corrupted on an I/O bound server
* [Revision #9bb5b25325](https://github.com/MariaDB/server/commit/9bb5b25325)\
  2023-07-24 12:29:43 +0300
  * [MDEV-31120](https://jira.mariadb.org/browse/MDEV-31120) Duplicate entry allowed into a UNIQUE column
* [Revision #6e484c3bd9](https://github.com/MariaDB/server/commit/6e484c3bd9)\
  2023-07-06 10:41:46 +0300
  * [MDEV-31577](https://jira.mariadb.org/browse/MDEV-31577): Make ANALYZE FORMAT=JSON print innodb stats
* [Revision #a03ce7b99c](https://github.com/MariaDB/server/commit/a03ce7b99c)\
  2023-07-13 16:05:02 +0400
  * [MDEV-31521](https://jira.mariadb.org/browse/MDEV-31521) bzero wipes more bytes than necessary in set\_global\_from\_ddl\_log\_entry.
* [Revision #a4e103ad82](https://github.com/MariaDB/server/commit/a4e103ad82)\
  2023-07-12 22:55:26 +0300
  * Fixed bug in ddl log
* [Revision #feaeb27b69](https://github.com/MariaDB/server/commit/feaeb27b69)\
  2023-07-11 20:24:28 +0300
  * [MDEV-29152](https://jira.mariadb.org/browse/MDEV-29152): Assertion failed ... upon TO\_CHAR with wrong argument
* [Revision #090a84366a](https://github.com/MariaDB/server/commit/090a84366a)\
  2023-07-06 11:49:28 +0300
  * [MDEV-29311](https://jira.mariadb.org/browse/MDEV-29311) Server Status Innodb\_row\_lock\_time% is reported in seconds
* [Revision #6ed14bcc06](https://github.com/MariaDB/server/commit/6ed14bcc06)\
  2023-07-07 12:53:50 +0300
  * Disable view protocol for opt\_trace.test
* [Revision #99bd226059](https://github.com/MariaDB/server/commit/99bd226059)\
  2023-07-07 08:38:55 +0300
  * [MDEV-31558](https://jira.mariadb.org/browse/MDEV-31558) Add InnoDB engine information to the slow query log
* Merge [Revision #2855bc53bc](https://github.com/MariaDB/server/commit/2855bc53bc) 2023-07-05 16:40:22 +0300 - Merge 10.5 into 10.6
* [Revision #5b62644e68](https://github.com/MariaDB/server/commit/5b62644e68)\
  2023-07-05 08:48:37 +0300
  * [MDEV-31621](https://jira.mariadb.org/browse/MDEV-31621) Remove ibuf\_read\_merge\_pages() call from ibuf\_insert\_low()
* [Revision #46b79b8cd1](https://github.com/MariaDB/server/commit/46b79b8cd1)\
  2023-07-03 22:05:02 +0200
  * [MDEV-30084](https://jira.mariadb.org/browse/MDEV-30084) Shutdown hangs in some tests
* [Revision #f6ecadfee8](https://github.com/MariaDB/server/commit/f6ecadfee8)\
  2023-07-03 18:18:02 +0200
  * fix ASAN+safemalloc builds
* [Revision #af38a8b438](https://github.com/MariaDB/server/commit/af38a8b438)\
  2023-06-26 17:47:47 +0200
  * cleanup: move Type\_collection\_fbt<> template out of Type\_handler\_fbt<>
* [Revision #c09b1583f5](https://github.com/MariaDB/server/commit/c09b1583f5)\
  2023-06-26 14:33:35 +0200
  * cleanup: remove FixedBinTypeBundle
* [Revision #238cfcc729](https://github.com/MariaDB/server/commit/238cfcc729)\
  2023-06-26 17:22:26 +0200
  * cleanup: remove unused and unlinkable method
* [Revision #bbe44da240](https://github.com/MariaDB/server/commit/bbe44da240)\
  2023-06-25 16:38:57 +0200
  * cleanup: udt in sql\_yac.yy
* [Revision #5bf80af06e](https://github.com/MariaDB/server/commit/5bf80af06e)\
  2023-05-16 22:26:57 +0200
  * cleanup: remove Type\_collection::handler\_by\_name()
* [Revision #a4817e1520](https://github.com/MariaDB/server/commit/a4817e1520)\
  2023-06-27 14:09:52 +0200
  * cleanup: String::strstr() const
* [Revision #f6e488cc6d](https://github.com/MariaDB/server/commit/f6e488cc6d)\
  2023-01-17 10:58:00 +0100
  * [MDEV-26506](https://jira.mariadb.org/browse/MDEV-26506) Over-quoted JSON when combining JSON\_ARRAYAGG with JSON\_OBJECT
* [Revision #cb364a78d6](https://github.com/MariaDB/server/commit/cb364a78d6)\
  2023-07-04 15:24:57 +0300
  * [MDEV-31619](https://jira.mariadb.org/browse/MDEV-31619) dict\_stats\_persistent\_storage\_check() may show garbage during --bootstrap
* [Revision #f7b8a2c953](https://github.com/MariaDB/server/commit/f7b8a2c953)\
  2023-07-03 16:47:58 +0300
  * [MDEV-31607](https://jira.mariadb.org/browse/MDEV-31607) ER\_DUP\_KEY in mysql.innodb\_table\_stats upon RENAME on sequence
* [Revision #dc1bd1802a](https://github.com/MariaDB/server/commit/dc1bd1802a)\
  2023-07-03 14:39:29 +0300
  * [MDEV-31386](https://jira.mariadb.org/browse/MDEV-31386) InnoDB: Failing assertion: page\_type == i\_s\_page\_type\[page\_type].type\_value
* [Revision #3d90143859](https://github.com/MariaDB/server/commit/3d90143859)\
  2023-06-30 17:07:21 +0300
  * [MDEV-31559](https://jira.mariadb.org/browse/MDEV-31559) btr\_search\_hash\_table\_validate() does not check if CHECK TABLE is killed
* [Revision #6d911219d6](https://github.com/MariaDB/server/commit/6d911219d6)\
  2023-06-29 18:34:34 +0700
  * [MDEV-30639](https://jira.mariadb.org/browse/MDEV-30639) Upgrade to 10.8 and later does not work on Windows
* [Revision #3e89b4fcc6](https://github.com/MariaDB/server/commit/3e89b4fcc6)\
  2023-06-28 13:54:30 +0300
  * [MDEV-31570](https://jira.mariadb.org/browse/MDEV-31570) gap\_lock\_split.test hangs sporadically
* [Revision #687fd6bef5](https://github.com/MariaDB/server/commit/687fd6bef5)\
  2023-06-26 11:47:59 +0300
  * [MDEV-30648](https://jira.mariadb.org/browse/MDEV-30648) btr\_estimate\_n\_rows\_in\_range() accesses unfixed, unlatched page
* Merge [Revision #694ce0d08e](https://github.com/MariaDB/server/commit/694ce0d08e) 2023-06-27 13:03:32 +0300 - Merge 10.5 into 10.6
* Merge [Revision #493083833b](https://github.com/MariaDB/server/commit/493083833b) 2023-06-26 17:11:38 +0300 - Merge 10.5 into 10.6
* [Revision #14275b4715](https://github.com/MariaDB/server/commit/14275b4715)\
  2022-10-21 15:43:17 +0530
  * [MDEV-28915](https://jira.mariadb.org/browse/MDEV-28915): mysql\_upgrade fails due to old\_mode="", with "Cannot load from mysql.proc. The table is probably corrupted"
* [Revision #6daccd4e48](https://github.com/MariaDB/server/commit/6daccd4e48)\
  2023-06-25 16:26:28 +0300
  * Moved test from group\_min\_max.test to group\_min\_max\_not\_embedded.test
* [Revision #3c7fd3c89b](https://github.com/MariaDB/server/commit/3c7fd3c89b)\
  2023-06-01 19:03:56 +0300
  * [MDEV-23106](https://jira.mariadb.org/browse/MDEV-23106) Unable to recognize/import partitioned tables from physical MySQL databases
* [Revision #d671fec431](https://github.com/MariaDB/server/commit/d671fec431)\
  2023-06-05 10:42:04 +0300
  * Fixed some errors & warnings when running mariadb-upgrade on MySQL instance
* [Revision #324d8a6036](https://github.com/MariaDB/server/commit/324d8a6036)\
  2023-06-05 11:05:22 +0300
  * Fix segfault in find\_files if db is NULL and path does not exist or can't be read
* [Revision #38fe266ea9](https://github.com/MariaDB/server/commit/38fe266ea9)\
  2023-06-05 11:03:49 +0300
  * Fix gcc warning for wsrep\_plug
* [Revision #f20d556f19](https://github.com/MariaDB/server/commit/f20d556f19)\
  2023-06-05 11:00:44 +0300
  * Fix use of uninitialized variable
* [Revision #ecd8a52252](https://github.com/MariaDB/server/commit/ecd8a52252)\
  2023-06-05 10:42:51 +0300
  * Renamed 'mysql' -> 'mariadb' in mtr
* [Revision #c2d44ecb90](https://github.com/MariaDB/server/commit/c2d44ecb90)\
  2023-05-30 09:20:22 -0600
  * [MDEV-29894](https://jira.mariadb.org/browse/MDEV-29894): Calling a function from a different database in a slave side trigger crashes
* [Revision #8171f9da87](https://github.com/MariaDB/server/commit/8171f9da87)\
  2023-06-07 15:31:05 +0300
  * [MDEV-31423](https://jira.mariadb.org/browse/MDEV-31423): Make sure that datadir is available with SySV-init script
* [Revision #bf0a54df34](https://github.com/MariaDB/server/commit/bf0a54df34)\
  2023-06-08 16:32:14 +0530
  * [MDEV-31416](https://jira.mariadb.org/browse/MDEV-31416) ASAN errors in dict\_v\_col\_t::detach upon adding key to virtual column
* Merge [Revision #80585c9d6f](https://github.com/MariaDB/server/commit/80585c9d6f) 2023-06-08 10:42:56 +0300 - Merge 10.5 into 10.6
* [Revision #6882eeabb0](https://github.com/MariaDB/server/commit/6882eeabb0)\
  2023-06-08 09:23:01 +0300
  * [MDEV-30483](https://jira.mariadb.org/browse/MDEV-30483) fixup: Declare the test plugin for Debian
* Merge [Revision #04f0b955dd](https://github.com/MariaDB/server/commit/04f0b955dd) 2023-06-07 19:59:52 +0200 - Merge branch '10.6' into 10.6.14
* [Revision #a77939ec8c](https://github.com/MariaDB/server/commit/a77939ec8c)\
  2023-06-07 08:12:43 -0400
  * bump the VERSION
* [Revision #f569e06e03](https://github.com/MariaDB/server/commit/f569e06e03)\
  2023-06-02 11:06:09 +0300
  * [MDEV-31385](https://jira.mariadb.org/browse/MDEV-31385) Change buffer stale entries leads to corruption while reusing page
* [Revision #8a86df37ef](https://github.com/MariaDB/server/commit/8a86df37ef)\
  2023-06-02 10:44:34 +0300
  * [MDEV-31088](https://jira.mariadb.org/browse/MDEV-31088) Server freeze due to innodb\_change\_buffering
* Merge [Revision #548a41c5ec](https://github.com/MariaDB/server/commit/548a41c5ec) 2023-06-01 12:28:40 +0300 - Merge 10.5 into 10.6
* [Revision #5919f7b675](https://github.com/MariaDB/server/commit/5919f7b675)\
  2023-05-31 19:07:41 +0530
  * [MDEV-31264](https://jira.mariadb.org/browse/MDEV-31264) Purge trying to access freed secondary index page
* [Revision #e3b06156c6](https://github.com/MariaDB/server/commit/e3b06156c6)\
  2023-05-31 15:25:07 +0300
  * [MDEV-31347](https://jira.mariadb.org/browse/MDEV-31347) fil\_ibd\_create() may hijack the file handle of an old file
* [Revision #eb20e7c900](https://github.com/MariaDB/server/commit/eb20e7c900)\
  2023-05-31 15:20:54 +0300
  * [MDEV-31353](https://jira.mariadb.org/browse/MDEV-31353) InnoDB recovery hangs after reporting corruption
* [Revision #30fb72ca6e](https://github.com/MariaDB/server/commit/30fb72ca6e)\
  2023-05-30 09:15:11 +0300
  * [MDEV-31331](https://jira.mariadb.org/browse/MDEV-31331): Fix cut'n'paste variable name in Debian pre-inst script
* [Revision #a6c0a27696](https://github.com/MariaDB/server/commit/a6c0a27696)\
  2023-05-30 17:21:49 +0300
  * [MDEV-31362](https://jira.mariadb.org/browse/MDEV-31362) recv\_sys\_t::apply(bool): Assertion \`!last\_batch || recovered\_lsn == scanned\_lsn' failed
* [Revision #ea66df2f45](https://github.com/MariaDB/server/commit/ea66df2f45)\
  2023-05-27 22:42:59 -0700
  * Deb: Fix blocksize check to use $mysql\_datadir/$datadir correctly
* [Revision #ce547cfc05](https://github.com/MariaDB/server/commit/ce547cfc05)\
  2023-05-26 16:40:07 +0300
  * [MDEV-31350](https://jira.mariadb.org/browse/MDEV-31350): Hang in innodb.recovery\_memory
* [Revision #7b72fc0a57](https://github.com/MariaDB/server/commit/7b72fc0a57)\
  2023-05-26 16:40:02 +0300
  * [MDEV-22739](https://jira.mariadb.org/browse/MDEV-22739) !cursor->index->is\_committed() in row0ins.cc
* [Revision #e38c075aa0](https://github.com/MariaDB/server/commit/e38c075aa0)\
  2023-05-26 16:39:46 +0300
  * [MDEV-31346](https://jira.mariadb.org/browse/MDEV-31346) trx\_purge\_add\_undo\_to\_history() is not optimal
* [Revision #db8765500e](https://github.com/MariaDB/server/commit/db8765500e)\
  2023-05-26 16:16:10 +0300
  * [MDEV-31343](https://jira.mariadb.org/browse/MDEV-31343) Another server hang with innodb\_undo\_log\_truncate=ON
* [Revision #03a9366c73](https://github.com/MariaDB/server/commit/03a9366c73)\
  2023-05-26 16:04:02 +0400
  * Extra tests for [MDEV-30483](https://jira.mariadb.org/browse/MDEV-30483) After upgrade to 10.6 from Mysql 5.7 seeing "InnoDB: Column last\_update in table mysql.innodb\_table\_stats is BINARY(4) NOT NULL but should be INT UNSIGNED NOT NULL"
* [Revision #9edb1a5ce3](https://github.com/MariaDB/server/commit/9edb1a5ce3)\
  2023-05-24 13:17:47 +0400
  * [MDEV-30483](https://jira.mariadb.org/browse/MDEV-30483) After upgrade to 10.6 from Mysql 5.7 seeing "InnoDB: Column last\_update in table mysql.innodb\_table\_stats is BINARY(4) NOT NULL but should be INT UNSIGNED NOT NULL"
* [Revision #9b3084b7be](https://github.com/MariaDB/server/commit/9b3084b7be)\
  2023-05-24 17:32:19 +0300
  * Fixed typo in xtrabackup.c
* [Revision #d77d9e1f6f](https://github.com/MariaDB/server/commit/d77d9e1f6f)\
  2023-05-24 13:35:22 +0300
  * MENT-1703 Repeatable crash during backup after processing very large ibdata1
* [Revision #7737f15f87](https://github.com/MariaDB/server/commit/7737f15f87)\
  2023-05-24 14:34:57 +0530
  * [MDEV-31333](https://jira.mariadb.org/browse/MDEV-31333) fsp\_free\_page() fails to move the extent from FSP\_FREE\_FRAG to FSP\_FREE list
* Merge [Revision #2cd6a48e72](https://github.com/MariaDB/server/commit/2cd6a48e72) 2023-05-24 08:38:35 +0300 - Merge 10.5 into 10.6
* Merge [Revision #b220bb756b](https://github.com/MariaDB/server/commit/b220bb756b) 2023-05-24 08:37:19 +0300 - Merge bb-10.6-release into 10.6
* Merge [Revision #98de15aba1](https://github.com/MariaDB/server/commit/98de15aba1) 2023-05-24 08:36:30 +0300 - Merge bb-10.5-release into bb-10.6-release
* Merge [Revision #270eeeb523](https://github.com/MariaDB/server/commit/270eeeb523) 2023-05-23 12:25:39 +0300 - Merge 10.5 into 10.6
* [Revision #b0c285bb06](https://github.com/MariaDB/server/commit/b0c285bb06)\
  2023-05-22 11:27:00 +0300
  * Remove warning of not freed memory if mysqld aborts
* Merge [Revision #3bd10b57b2](https://github.com/MariaDB/server/commit/3bd10b57b2) 2023-05-22 17:11:41 +0300 - Merge 10.5 into 10.6
* [Revision #a5ce335ac9](https://github.com/MariaDB/server/commit/a5ce335ac9)\
  2023-05-22 17:10:25 +0300
  * [MDEV-29593](https://jira.mariadb.org/browse/MDEV-29593) fixup: Avoid a leak if rseg.undo\_cached is corrupted
* Merge [Revision #eb2e074494](https://github.com/MariaDB/server/commit/eb2e074494) 2023-05-22 08:38:21 +0300 - Merge 10.5 into 10.6
* [Revision #f307160218](https://github.com/MariaDB/server/commit/f307160218)\
  2023-04-19 16:51:55 +0300
  * [MDEV-29293](https://jira.mariadb.org/browse/MDEV-29293) MariaDB stuck on starting commit state
* [Revision #d2420669bd](https://github.com/MariaDB/server/commit/d2420669bd)\
  2023-05-19 15:38:48 +0300
  * [MDEV-31309](https://jira.mariadb.org/browse/MDEV-31309) Innodb\_buffer\_pool\_read\_requests is not updated correctly
* [Revision #df524dc06f](https://github.com/MariaDB/server/commit/df524dc06f)\
  2023-05-19 15:29:26 +0300
  * [MDEV-31308](https://jira.mariadb.org/browse/MDEV-31308) InnoDB monitor trx\_rseg\_history\_len was accidentally disabled by default
* [Revision #f2c17cc9d9](https://github.com/MariaDB/server/commit/f2c17cc9d9)\
  2023-05-19 15:20:07 +0300
  * [MDEV-29911](https://jira.mariadb.org/browse/MDEV-29911) InnoDB recovery and mariadb-backup --prepare fail to report detailed progress
* Merge [Revision #1fe830b56a](https://github.com/MariaDB/server/commit/1fe830b56a) 2023-05-19 14:24:09 +0300 - Merge 10.5 into 10.6
* Merge [Revision #347e22fbf8](https://github.com/MariaDB/server/commit/347e22fbf8) 2023-05-19 14:23:53 +0300 - Merge bb-10.6-release into 10.6
* [Revision #e5933b99d5](https://github.com/MariaDB/server/commit/e5933b99d5)\
  2023-05-19 12:25:30 +0300
  * [MDEV-31234](https://jira.mariadb.org/browse/MDEV-31234) related cleanup
* Merge [Revision #37492960f3](https://github.com/MariaDB/server/commit/37492960f3) 2023-05-19 12:24:58 +0300 - Merge 10.5 into 10.6
* Merge [Revision #a3e5b5c4db](https://github.com/MariaDB/server/commit/a3e5b5c4db) 2023-05-15 09:02:32 +0300 - Merge 10.5 into 10.6
* [Revision #f522b0f230](https://github.com/MariaDB/server/commit/f522b0f230)\
  2023-05-10 11:57:48 +0300
  * [MDEV-30951](https://jira.mariadb.org/browse/MDEV-30951): Fix small perlcritic and enable modern Perl
* Merge [Revision #c271057288](https://github.com/MariaDB/server/commit/c271057288) 2023-05-11 13:27:01 +0300 - Merge 10.5 into 10.6
* [Revision #7124911a2c](https://github.com/MariaDB/server/commit/7124911a2c)\
  2023-05-11 08:43:00 +0300
  * [MDEV-31158](https://jira.mariadb.org/browse/MDEV-31158): Potential hang with ROW\_FORMAT=COMPRESSED tables
* [Revision #38ed782f55](https://github.com/MariaDB/server/commit/38ed782f55)\
  2023-05-11 08:42:28 +0300
  * [MDEV-30812](https://jira.mariadb.org/browse/MDEV-30812) fixup: GCC 12.2.0 -Wmaybe-uninitialized
* Merge [Revision #522a52498c](https://github.com/MariaDB/server/commit/522a52498c) 2023-05-11 08:41:23 +0300 - Merge mariadb-10.6.13 into 10.6
* [Revision #afe44ef212](https://github.com/MariaDB/server/commit/afe44ef212)\
  2023-05-10 08:45:08 -0400
  * bump the VERSION
* [Revision #2740b657ce](https://github.com/MariaDB/server/commit/2740b657ce)\
  2023-05-08 11:35:32 +0300
  * [MDEV-31216](https://jira.mariadb.org/browse/MDEV-31216): Make sure that lsof does not fail on install
* [Revision #50cdf0b5ea](https://github.com/MariaDB/server/commit/50cdf0b5ea)\
  2023-03-30 13:58:54 +0300
  * [MDEV-30952](https://jira.mariadb.org/browse/MDEV-30952): Reformat Debian pre- and postscripts if-clauses
* [Revision #8febdfa342](https://github.com/MariaDB/server/commit/8febdfa342)\
  2023-03-29 12:42:12 +0300
  * [MDEV-30952](https://jira.mariadb.org/browse/MDEV-30952): Fix shellcheck problems on Debian scripts
* [Revision #7cbb45d1d4](https://github.com/MariaDB/server/commit/7cbb45d1d4)\
  2023-03-29 12:28:51 +0300
  * [MDEV-30952](https://jira.mariadb.org/browse/MDEV-30952): Reformat Debian post and pre scripts

{% include "https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/~/reusable/vX1KAy0t1XuYJaGsK28T/" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
