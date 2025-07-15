# MariaDB 10.6.22 Changelog

<a href="https://mariadb.com/downloads/community" class="button primary">Download</a> <a href="../../mariadb-10-6-series/mariadb-10-6-22-release-notes.md" class="button secondary">Release Notes</a> <a href="mariadb-10-6-22-changelog.md" class="button secondary">Changelog</a> <a href="../../mariadb-10-6-series/what-is-mariadb-106.md" class="button secondary">Overview of 10.6</a>

[_Alternate download from mariadb.org_](https://downloads.mariadb.org/mariadb/10.6.22/)

**Release date:** 8 May 2025

For the highlights of this release, see the [release notes](../../mariadb-10-6-series/mariadb-10-6-22-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On [GitHub](https://github.com/MariaDB/server/tree/10.6) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Includes all fixes from [MariaDB 10.5.29](../changelogs-mariadb-105-series/mariadb-10-5-29-changelog.md)
* Merge [Revision #19644f6821](https://github.com/MariaDB/server/commit/19644f6821) 2025-04-26 10:41:52 +0200 - Merge branch '10.5' into 10.6
* [Revision #9b0294cd12](https://github.com/MariaDB/server/commit/9b0294cd12)\
  2025-04-25 01:06:07 +0400
  * [MDEV-36666](https://jira.mariadb.org/browse/MDEV-36666) - atomic.alter\_table still times out often
* [Revision #47e687b109](https://github.com/MariaDB/server/commit/47e687b109)\
  2025-04-22 15:49:53 +0300
  * [MDEV-36639](https://jira.mariadb.org/browse/MDEV-36639) innodb\_snapshot\_isolation=1 gives error for not committed row changes
* [Revision #4bedb222a8](https://github.com/MariaDB/server/commit/4bedb222a8)\
  2025-04-22 17:11:56 +0530
  * [MDEV-36304](https://jira.mariadb.org/browse/MDEV-36304) InnoDB: Missing FILE\_CREATE, FILE\_DELETE or FILE\_MODIFY error during mariadb-backup --prepare
* [Revision #dac3d702f7](https://github.com/MariaDB/server/commit/dac3d702f7)\
  2025-04-21 13:45:38 +0530
  * [MDEV-36649](https://jira.mariadb.org/browse/MDEV-36649) dict\_acquire\_mdl\_shared() aborts when table mode is DICT\_TABLE\_OP\_OPEN\_ONLY\_IF\_CACHED
* Merge [Revision #a135551569](https://github.com/MariaDB/server/commit/a135551569) 2025-04-21 10:43:17 +0200 - Merge branch '10.5' into 10.6
* [Revision #236dec69b7](https://github.com/MariaDB/server/commit/236dec69b7)\
  2025-04-20 20:48:21 +0200
  * new CC
* [Revision #35c25cd107](https://github.com/MariaDB/server/commit/35c25cd107)\
  2025-04-03 18:56:25 +0300
  * [MDEV-36412](https://jira.mariadb.org/browse/MDEV-36412) Concerns compilation issue on community edition for x86\_64 with X32 ABI
* [Revision #51c5b75335](https://github.com/MariaDB/server/commit/51c5b75335)\
  2025-03-13 17:29:22 +0200
  * Always call mysql\_cond\_broadcast(\&rli->data\_cond) under data\_lock
* [Revision #5b1bdf6076](https://github.com/MariaDB/server/commit/5b1bdf6076)\
  2025-04-14 16:37:30 -0600
  * [MDEV-36359](https://jira.mariadb.org/browse/MDEV-36359): Patch NULL deref after disabling Semi-Sync primary
* [Revision #839e8bfe9f](https://github.com/MariaDB/server/commit/839e8bfe9f)\
  2025-04-16 10:36:33 +1000
  * [MDEV-36182](https://jira.mariadb.org/browse/MDEV-36182): liburing - incorrect error handing.
* [Revision #73cdeda347](https://github.com/MariaDB/server/commit/73cdeda347)\
  2025-04-16 10:24:33 +1000
  * tpool: remove m\_group\_enqueued (unused)
* [Revision #1055bc957e](https://github.com/MariaDB/server/commit/1055bc957e)\
  2025-04-16 10:12:49 +1000
  * [MDEV-36182](https://jira.mariadb.org/browse/MDEV-36182): Revert "[MDEV-26674](https://jira.mariadb.org/browse/MDEV-26674): Set innodb\_use\_native\_aio=OFF
* [Revision #51179067fc](https://github.com/MariaDB/server/commit/51179067fc)\
  2025-04-16 10:09:57 +1000
  * [MDEV-36182](https://jira.mariadb.org/browse/MDEV-36182): Revert "[MDEV-26674](https://jira.mariadb.org/browse/MDEV-26674) workaround for mariadb-backup"
* [Revision #5f2562291c](https://github.com/MariaDB/server/commit/5f2562291c)\
  2025-04-08 09:56:47 +0300
  * [MDEV-36509](https://jira.mariadb.org/browse/MDEV-36509) : Galera test failure on galera\_sr.mysql-wsrep-features#165
* [Revision #ee947fae80](https://github.com/MariaDB/server/commit/ee947fae80)\
  2025-04-02 14:44:41 +0300
  * [MDEV-36464](https://jira.mariadb.org/browse/MDEV-36464) : Galera test failure on galera\_3nodes.galera\_gtid\_2\_cluster
* [Revision #0403f0147f](https://github.com/MariaDB/server/commit/0403f0147f)\
  2025-04-07 17:40:33 +0200
  * [MDEV-33136](https://jira.mariadb.org/browse/MDEV-33136): backport corrections from 10.11+
* Merge [Revision #88dfa6bcee](https://github.com/MariaDB/server/commit/88dfa6bcee) 2025-04-15 01:49:48 +0200 - Merge branch '10.5' into '10.6'
* [Revision #14389b6993](https://github.com/MariaDB/server/commit/14389b6993)\
  2025-04-14 09:22:39 +0300
  * [MDEV-36510](https://jira.mariadb.org/browse/MDEV-36510) InnoDB fails to compile with clang++-20
* [Revision #690b2cf776](https://github.com/MariaDB/server/commit/690b2cf776)\
  2025-03-20 09:54:12 +1100
  * test: archive-big test too big for msan
* [Revision #93ea4f29a4](https://github.com/MariaDB/server/commit/93ea4f29a4)\
  2025-04-01 16:40:30 +1100
  * [MDEV-36347](https://jira.mariadb.org/browse/MDEV-36347) UBSAN: plugins.auth\_v0100 - runtime error: call to function do\_auth\_0x0100
* [Revision #3995de0318](https://github.com/MariaDB/server/commit/3995de0318)\
  2025-04-01 16:22:05 +1100
  * [MDEV-36341](https://jira.mariadb.org/browse/MDEV-36341) UBSAN: FederatedX fill\_server runtime error: applying non-zero offset to null pointer
* [Revision #13dd073742](https://github.com/MariaDB/server/commit/13dd073742)\
  2025-04-01 16:11:09 +1100
  * [MDEV-31846](https://jira.mariadb.org/browse/MDEV-31846): enable cursor protocol for test federatedx\_create\_handlers
* [Revision #b316a7135b](https://github.com/MariaDB/server/commit/b316a7135b)\
  2025-03-28 18:12:24 +1100
  * mroonga: undefined behaviour fix
* [Revision #2ba49bd804](https://github.com/MariaDB/server/commit/2ba49bd804)\
  2025-03-28 18:11:09 +1100
  * mroonga: correct offsetof calculation
* [Revision #db4763a0d1](https://github.com/MariaDB/server/commit/db4763a0d1)\
  2025-04-07 10:25:34 +0300
  * Fix a slow test
* [Revision #b11772d9a5](https://github.com/MariaDB/server/commit/b11772d9a5)\
  2025-04-03 16:43:01 +0530
  * [MDEV-33167](https://jira.mariadb.org/browse/MDEV-33167) ASAN errors in dict\_sys\_t::load\_table / get\_foreign\_key\_info after failing to load a table
* [Revision #0d7ef4f478](https://github.com/MariaDB/server/commit/0d7ef4f478)\
  2025-04-03 12:19:36 +0530
  * [MDEV-36236](https://jira.mariadb.org/browse/MDEV-36236) Instant alter aborts when InnoDB fails to rollback instant operation
* [Revision #e7442e5eb9](https://github.com/MariaDB/server/commit/e7442e5eb9)\
  2025-04-02 12:53:21 +0300
  * [MDEV-36226](https://jira.mariadb.org/browse/MDEV-36226) fixup: format mismatch
* [Revision #4c0e2f1aca](https://github.com/MariaDB/server/commit/4c0e2f1aca)\
  2025-04-02 08:12:29 +0300
  * [MDEV-35813](https://jira.mariadb.org/browse/MDEV-35813): even more robust test case
* [Revision #c01bff4a10](https://github.com/MariaDB/server/commit/c01bff4a10)\
  2025-03-25 13:59:00 +0300
  * [MDEV-36360](https://jira.mariadb.org/browse/MDEV-36360): Don't grab table-level X locks for applied inserts
* [Revision #b983a911e9](https://github.com/MariaDB/server/commit/b983a911e9)\
  2025-04-02 03:51:44 +0200
  * galera mtr tests: synchronization between branches and editions
* [Revision #5003dac220](https://github.com/MariaDB/server/commit/5003dac220)\
  2025-04-02 04:00:04 +0200
  * [MDEV-36116](https://jira.mariadb.org/browse/MDEV-36116): Post-merge correction for 10.6+
* Merge [Revision #03c31ab099](https://github.com/MariaDB/server/commit/03c31ab099) 2025-04-02 04:43:24 +0200 - Merge branch '10.5' into '10.6'
* [Revision #77bebe9eb0](https://github.com/MariaDB/server/commit/77bebe9eb0)\
  2025-03-10 12:39:56 +0530
  * [MDEV-36226](https://jira.mariadb.org/browse/MDEV-36226) Stall and crash when page cleaner fails to generate free pages during Async flush
* Merge [Revision #51cc77f212](https://github.com/MariaDB/server/commit/51cc77f212) 2025-03-31 11:40:23 +0200 - Merge branch '10.5' into 10.6
* [Revision #da9d575516](https://github.com/MariaDB/server/commit/da9d575516)\
  2025-03-21 19:31:47 +0100
  * [MDEV-35653](https://jira.mariadb.org/browse/MDEV-35653) Assertion \`commit\_trx' failed in int innobase\_commit(handlerton\*, THD\*, bool)
* [Revision #31c06951c6](https://github.com/MariaDB/server/commit/31c06951c6)\
  2025-03-28 09:05:20 +0200
  * [MDEV-36420](https://jira.mariadb.org/browse/MDEV-36420) Assertion failure in SET GLOBAL innodb\_ft\_aux\_table
* [Revision #1b9d5cdb83](https://github.com/MariaDB/server/commit/1b9d5cdb83)\
  2025-03-28 08:38:04 +0200
  * [MDEV-35813](https://jira.mariadb.org/browse/MDEV-35813): Valgrind test fixup
* Merge [Revision #191209d8ab](https://github.com/MariaDB/server/commit/191209d8ab) 2025-03-26 17:09:57 +0200 - Merge 10.5 into 10.6
* [Revision #6066e5d13c](https://github.com/MariaDB/server/commit/6066e5d13c)\
  2025-03-26 14:23:45 +0200
  * [MDEV-36122](https://jira.mariadb.org/browse/MDEV-36122): Work around missing MDL in purge
* [Revision #67caeca284](https://github.com/MariaDB/server/commit/67caeca284)\
  2025-03-26 14:22:58 +0200
  * [MDEV-36122](https://jira.mariadb.org/browse/MDEV-36122): Protect table references with a lock
* [Revision #337bf8ac4b](https://github.com/MariaDB/server/commit/337bf8ac4b)\
  2025-03-26 14:22:40 +0200
  * [MDEV-36122](https://jira.mariadb.org/browse/MDEV-36122) Assertion ctx0->old\_table->get\_ref\_count() == 1
* [Revision #1f4a901576](https://github.com/MariaDB/server/commit/1f4a901576)\
  2025-03-25 20:03:14 +0530
  * [MDEV-36281](https://jira.mariadb.org/browse/MDEV-36281) DML aborts during online virtual index
* [Revision #a390aaaf23](https://github.com/MariaDB/server/commit/a390aaaf23)\
  2025-03-26 11:15:09 +0530
  * [MDEV-36180](https://jira.mariadb.org/browse/MDEV-36180) Doublewrite recovery of innodb\_checksum\_algorithm=full\_crc32 page\_compressed pages does not work
* [Revision #19c4e1abe4](https://github.com/MariaDB/server/commit/19c4e1abe4)\
  2025-03-20 15:20:44 +0200
  * [MDEV-24035](https://jira.mariadb.org/browse/MDEV-24035) fixup: GCC 4.8.5 CMAKE\_BUILD\_TYPE=Debug
* [Revision #d84ceb586a](https://github.com/MariaDB/server/commit/d84ceb586a)\
  2025-03-25 12:15:46 +0200
  * [MDEV-36378](https://jira.mariadb.org/browse/MDEV-36378) Recognize innodb\_purge\_rseg\_truncate\_frequency
* [Revision #3d54cd6cf5](https://github.com/MariaDB/server/commit/3d54cd6cf5)\
  2025-03-25 10:13:47 +1100
  * update C/C
* [Revision #05be1865a9](https://github.com/MariaDB/server/commit/05be1865a9)\
  2025-03-07 02:04:01 -0500
  * Fix building with Clang and GCC on RISC-V
* [Revision #2ae721f2ad](https://github.com/MariaDB/server/commit/2ae721f2ad)\
  2025-03-19 16:05:35 +0400
  * [MDEV-36179](https://jira.mariadb.org/browse/MDEV-36179) Assertion \`0' failed in virtual bool Type\_handler\_row::Item\_save\_in\_value(THD\*, Item\*, st\_value\*) const
* [Revision #1756b0f37d](https://github.com/MariaDB/server/commit/1756b0f37d)\
  2025-03-18 10:41:38 +0200
  * [MDEV-35813](https://jira.mariadb.org/browse/MDEV-35813): more robust test case
* [Revision #0e8e0065d6](https://github.com/MariaDB/server/commit/0e8e0065d6)\
  2025-03-17 16:21:09 +0200
  * [MDEV-35813](https://jira.mariadb.org/browse/MDEV-35813) test case
* [Revision #c3c5cd9377](https://github.com/MariaDB/server/commit/c3c5cd9377)\
  2025-03-14 13:06:37 +0200
  * [MDEV-35813](https://jira.mariadb.org/browse/MDEV-35813) Unnecessary InnoDB log writes in INSERT…SELECT
* [Revision #04e114aec0](https://github.com/MariaDB/server/commit/04e114aec0)\
  2025-03-13 18:58:12 +0100
  * Fix sporadic failure of rpl.parallel\_backup\_xa\_debug
* [Revision #6810cdae1b](https://github.com/MariaDB/server/commit/6810cdae1b)\
  2025-03-13 11:25:40 +0100
  * Add --source include/long\_test.inc to a few long-running tests
* [Revision #2641409731](https://github.com/MariaDB/server/commit/2641409731)\
  2025-03-08 11:11:58 +0100
  * Fix redundant ER\_PRIOR\_COMMIT\_FAILED in parallel replication
* [Revision #eef94c9d46](https://github.com/MariaDB/server/commit/eef94c9d46)\
  2025-03-09 14:34:54 +0200
  * [MDEV-36248](https://jira.mariadb.org/browse/MDEV-36248) Connect crashes server because of duplicate 'free()' in GetUser
* [Revision #64a1458847](https://github.com/MariaDB/server/commit/64a1458847)\
  2025-03-07 19:24:10 +0200
  * Ensure that ER\_CONNECTION\_KILLED error message is not lost
* [Revision #b12e8d9095](https://github.com/MariaDB/server/commit/b12e8d9095)\
  2025-03-03 12:27:43 +0200
  * MENT-2235 Aria engine: log initialization failed
* [Revision #1331c73243](https://github.com/MariaDB/server/commit/1331c73243)\
  2025-02-27 10:24:05 +0200
  * Moved server\_threads.erase(thd) to end of handle\_slave\_sql()
* [Revision #cc4d9200c4](https://github.com/MariaDB/server/commit/cc4d9200c4)\
  2025-02-26 16:32:06 +0200
  * [MDEV-33813](https://jira.mariadb.org/browse/MDEV-33813) ERROR 1021 (HY000): Disk full (./org/test1.MAI); waiting for someone to free some space... (errno: 28 "No space left on device")
* Merge [Revision #15139c88a8](https://github.com/MariaDB/server/commit/15139c88a8) 2025-03-05 01:54:40 +0100 - Merge branch '10.5' into '10.6'
* [Revision #e95a8f84de](https://github.com/MariaDB/server/commit/e95a8f84de)\
  2025-02-27 11:33:44 +1100
  * [MDEV-36156](https://jira.mariadb.org/browse/MDEV-36156): MSAN Compile and Link flags needed for compile/run checks
* [Revision #7bb0885397](https://github.com/MariaDB/server/commit/7bb0885397)\
  2025-02-21 13:24:27 +1100
  * fixup of [MDEV-35959](https://jira.mariadb.org/browse/MDEV-35959)
* Merge [Revision #e3d7d5ca26](https://github.com/MariaDB/server/commit/e3d7d5ca26) 2025-02-27 03:59:30 +0100 - Merge branch '10.5' into '10.6'
* [Revision #bac2358c9d](https://github.com/MariaDB/server/commit/bac2358c9d)\
  2025-02-23 16:59:04 +0200
  * Removed outdated code comment
* [Revision #a20c8fabe7](https://github.com/MariaDB/server/commit/a20c8fabe7)\
  2025-02-19 10:43:36 +0000
  * Fix sporadic failure of rpl.rpl\_parallel\_innodb\_lock\_conflict
* [Revision #f1d7e0c17e](https://github.com/MariaDB/server/commit/f1d7e0c17e)\
  2025-02-13 12:18:03 +0200
  * [MDEV-35436](https://jira.mariadb.org/browse/MDEV-35436) dict\_stats\_fetch\_from\_ps() unnecessarily holds exclusive dict\_sys.latch
* [Revision #7587b0ec84](https://github.com/MariaDB/server/commit/7587b0ec84)\
  2025-02-12 14:24:19 +0200
  * [MDEV-36061](https://jira.mariadb.org/browse/MDEV-36061) Incorrect error handling on DDL with FULLTEXT INDEX
* [Revision #c07e355c40](https://github.com/MariaDB/server/commit/c07e355c40)\
  2025-02-12 10:14:10 +0200
  * [MDEV-36015](https://jira.mariadb.org/browse/MDEV-36015): unrepresentable value in row\_parse\_int()
* [Revision #44e1f7238a](https://github.com/MariaDB/server/commit/44e1f7238a)\
  2025-02-12 01:29:09 +0100
  * [MDEV-35941](https://jira.mariadb.org/browse/MDEV-35941) addendum: additional corrections for mtr tests
* [Revision #3009b5439d](https://github.com/MariaDB/server/commit/3009b5439d)\
  2025-02-10 09:19:23 +0200
  * [MDEV-35941](https://jira.mariadb.org/browse/MDEV-35941) : galera\_bf\_abort\_lock\_table fails with wait for metadata lock
* [Revision #6e6fcf4d43](https://github.com/MariaDB/server/commit/6e6fcf4d43)\
  2025-01-31 14:32:22 +0300
  * [MDEV-34489](https://jira.mariadb.org/browse/MDEV-34489) innodb.innodb\_row\_lock\_time\_ms fails
* [Revision #64b964e757](https://github.com/MariaDB/server/commit/64b964e757)\
  2025-02-04 10:11:58 -0500
  * bump the VERSION
* Merge [Revision #d6f31ed263](https://github.com/MariaDB/server/commit/d6f31ed263) 2025-02-03 10:44:13 +0100 - Merge branch '10.5' into '10.6'
* [Revision #1f93aece3d](https://github.com/MariaDB/server/commit/1f93aece3d)\
  2024-11-07 14:41:02 +0200
  * [MDEV-24485](https://jira.mariadb.org/browse/MDEV-24485) : galera.galera\_bf\_kill\_debug MTR failed: A long semaphore wait
* [Revision #75b24a002f](https://github.com/MariaDB/server/commit/75b24a002f)\
  2025-02-03 08:29:52 +0200
  * Suppress processist\_state='buffer pool load'
* [Revision #f6fd591a08](https://github.com/MariaDB/server/commit/f6fd591a08)\
  2025-02-03 08:28:01 +0200
  * mtr: Globally suppress some rare warnings
* [Revision #900bbbe4a8](https://github.com/MariaDB/server/commit/900bbbe4a8)\
  2025-02-03 08:11:43 +0200
  * [MDEV-33295](https://jira.mariadb.org/browse/MDEV-33295) innodb.doublewrite occasionally fails
* [Revision #9389428380](https://github.com/MariaDB/server/commit/9389428380)\
  2023-07-17 17:29:20 +0300
  * [MDEV-27861](https://jira.mariadb.org/browse/MDEV-27861): Creating partitioned tables should not be allowed with wsrep\_osu\_method=TOI and wsrep\_strict\_ddl=ON
* [Revision #b3925982a0](https://github.com/MariaDB/server/commit/b3925982a0)\
  2023-05-02 04:57:30 +0200
  * [MDEV-29755](https://jira.mariadb.org/browse/MDEV-29755) post-merge for 10.6+
* [Revision #0784dd32b1](https://github.com/MariaDB/server/commit/0784dd32b1)\
  2023-04-13 13:45:00 +0300
  * [MDEV-29775](https://jira.mariadb.org/browse/MDEV-29775) : Assertion \`0' failed in void Protocol::end\_statement() when adding data to the MyISAM table after setting wsrep\_mode=replicate\_myisam
* Merge [Revision #53c693ec2f](https://github.com/MariaDB/server/commit/53c693ec2f) 2025-02-02 12:36:10 +0100 - Merge branch '10.5' into '10.6'
* [Revision #f1276aa1bc](https://github.com/MariaDB/server/commit/f1276aa1bc)\
  2024-07-09 08:59:59 -0600
  * [MDEV-26652](https://jira.mariadb.org/browse/MDEV-26652): xa transactions binlogged in wrong order

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
