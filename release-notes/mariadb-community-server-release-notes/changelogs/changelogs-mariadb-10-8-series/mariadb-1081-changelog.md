# MariaDB 10.8.1 Changelog

[Download](https://mariadb.com/downloads/)[Release Notes](../../old-releases/release-notes-mariadb-10-8-series/mariadb-1081-release-notes.md)[Changelog](mariadb-1081-changelog.md)[Overview of 10.8](../../old-releases/release-notes-mariadb-10-8-series/what-is-mariadb-108.md)

[_Alternate download from mariadb.org_](https://mariadb.org/download/?tab=mariadb\&release=10.8.1\&product=mariadb)

**Release date:** 9 Feb 2022

For the highlights of this release, see the[release notes](../../old-releases/release-notes-mariadb-10-8-series/mariadb-1081-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/server/tree/10.8) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Changes from 10.8.0 are also included in this changelog
* Includes all fixes from [MariaDB 10.7.2](../changelogs-mariadb-10-7-series/mariadb-1072-changelog.md)
* [Revision #307b2991d6](https://github.com/MariaDB/server/commit/307b2991d6)\
  2022-02-07 08:44:32 +0100
  * Fix JSON statistics time format and added tests for it and server version.
* Merge [Revision #34564587f4](https://github.com/MariaDB/server/commit/34564587f4) 2022-02-06 18:05:12 +0100 - Merge branch '10.7' into 10.8
* [Revision #5ded88ebb3](https://github.com/MariaDB/server/commit/5ded88ebb3)\
  2022-02-04 19:45:45 +0100
  * Remove incorrect narrowing size\_t->ulong casts. Fix printf format error.
* [Revision #4c2c1e6185](https://github.com/MariaDB/server/commit/4c2c1e6185)\
  2022-02-04 21:20:36 +0100
  * enable main.mysqldump-system test
* [Revision #6009f9b859](https://github.com/MariaDB/server/commit/6009f9b859)\
  2022-02-04 14:56:20 +0100
  * make zstd in C/C optional and disable it for now in RPM/DEB
* [Revision #e70bd5f695](https://github.com/MariaDB/server/commit/e70bd5f695)\
  2022-02-04 14:57:21 +0100
  * .gitignore
* Merge [Revision #2f29d0eaab](https://github.com/MariaDB/server/commit/2f29d0eaab) 2022-02-04 14:53:58 +0100 - Merge branch '10.7' into 10.8
* [Revision #64e358821e](https://github.com/MariaDB/server/commit/64e358821e)\
  2022-02-04 14:52:03 +0100
  * Revert "don't build with OpenSSL 3.0, it doesn't work before [MDEV-25785](https://jira.mariadb.org/browse/MDEV-25785)"
* Merge [Revision #4fb2cb1a30](https://github.com/MariaDB/server/commit/4fb2cb1a30) 2022-02-04 14:50:25 +0100 - Merge branch '10.7' into 10.8
* [Revision #c0f5fd2754](https://github.com/MariaDB/server/commit/c0f5fd2754)\
  2022-02-03 12:44:09 +0100
  * [MDEV-27683](https://jira.mariadb.org/browse/MDEV-27683) EXCHANGE PARTITION allows different index direction, but causes further errors
* [Revision #a450d58ad0](https://github.com/MariaDB/server/commit/a450d58ad0)\
  2022-02-03 12:34:34 +0100
  * fix a copy-paste error
* [Revision #e4d7886cc5](https://github.com/MariaDB/server/commit/e4d7886cc5)\
  2022-02-02 17:17:27 +0200
  * [MDEV-11675](https://jira.mariadb.org/browse/MDEV-11675). rpl\_start\_alter\_ftwrl.test is refined
* [Revision #12f29a4bc0](https://github.com/MariaDB/server/commit/12f29a4bc0)\
  2022-02-02 11:30:16 +0200
  * [MDEV-11675](https://jira.mariadb.org/browse/MDEV-11675) fixup: GCC -Og -Wmaybe-uninitialized
* [Revision #2b95c36b4b](https://github.com/MariaDB/server/commit/2b95c36b4b)\
  2022-02-02 01:35:40 +0100
  * fix clang-cl warnings
* [Revision #83cdcf5bf2](https://github.com/MariaDB/server/commit/83cdcf5bf2)\
  2022-02-01 15:08:13 +0100
  * new CC 3.3
* [Revision #2b55411673](https://github.com/MariaDB/server/commit/2b55411673)\
  2022-02-01 17:12:05 +0200
  * [MDEV-27687](https://jira.mariadb.org/browse/MDEV-27687) Assertion \`!thd->rgi\_fake || ...
* [Revision #fe2d90cca9](https://github.com/MariaDB/server/commit/fe2d90cca9)\
  2022-01-31 19:27:22 +0200
  * [MDEV-11675](https://jira.mariadb.org/browse/MDEV-11675). Convert the new session var to bool type and test changes
* [Revision #a64991df9d](https://github.com/MariaDB/server/commit/a64991df9d)\
  2022-01-30 15:32:56 -0700
  * [MDEV-4989](https://jira.mariadb.org/browse/MDEV-4989): Support for GTID in mysqlbinlog
* [Revision #0c5d1342ae](https://github.com/MariaDB/server/commit/0c5d1342ae)\
  2021-01-29 11:59:14 +0000
  * [MDEV-11675](https://jira.mariadb.org/browse/MDEV-11675) Lag Free Alter On Slave
* [Revision #c64e507fad](https://github.com/MariaDB/server/commit/c64e507fad)\
  2022-01-27 16:17:40 +0200
  * [MDEV-27621](https://jira.mariadb.org/browse/MDEV-27621) Backup fails with FATAL ERROR: Was only able to copy log
* [Revision #79e3ee00fa](https://github.com/MariaDB/server/commit/79e3ee00fa)\
  2021-08-11 11:29:37 -0600
  * [MDEV-4989](https://jira.mariadb.org/browse/MDEV-4989): Support for GTID in mysqlbinlog
* [Revision #343134fc18](https://github.com/MariaDB/server/commit/343134fc18)\
  2022-01-26 20:35:41 +0100
  * bump the version and maturity
* [Revision #5217211e07](https://github.com/MariaDB/server/commit/5217211e07)\
  2021-09-01 19:09:01 +0530
  * [MDEV-26238](https://jira.mariadb.org/browse/MDEV-26238): Remove inconsistent behaviour of --default-\* options in my\_print\_defaults
* [Revision #b18697fd3e](https://github.com/MariaDB/server/commit/b18697fd3e)\
  2022-01-01 17:20:52 +0100
  * [MDEV-27398](https://jira.mariadb.org/browse/MDEV-27398) DESC index causes wrong (empty) result on Federated tables
* [Revision #f00236ac23](https://github.com/MariaDB/server/commit/f00236ac23)\
  2022-01-01 16:25:48 +0100
  * cleanup: FederatedX
* [Revision #820aa11ef1](https://github.com/MariaDB/server/commit/820aa11ef1)\
  2022-01-25 12:20:03 +0100
  * [MDEV-27581](https://jira.mariadb.org/browse/MDEV-27581) Wrong result with DESC key on partitioned Spider table
* [Revision #24ee346a8d](https://github.com/MariaDB/server/commit/24ee346a8d)\
  2022-01-24 17:36:46 +0100
  * [MDEV-27590](https://jira.mariadb.org/browse/MDEV-27590) Auto-increment on Spider tables with DESC PK does not work properly
* [Revision #d751f42a02](https://github.com/MariaDB/server/commit/d751f42a02)\
  2022-01-24 21:26:07 +0100
  * [MDEV-27586](https://jira.mariadb.org/browse/MDEV-27586) Auto-increment does not work with DESC on MERGE table
* [Revision #72b5b8b2e3](https://github.com/MariaDB/server/commit/72b5b8b2e3)\
  2022-01-08 15:08:21 +0100
  * [MDEV-27434](https://jira.mariadb.org/browse/MDEV-27434) DESC attribute does not work with auto-increment on secondary column of multi-part index
* [Revision #9b6d2ad745](https://github.com/MariaDB/server/commit/9b6d2ad745)\
  2022-01-06 18:12:37 +0100
  * ORDER BY index traversal direction in the optimizer trace
* [Revision #d7e7f48eb4](https://github.com/MariaDB/server/commit/d7e7f48eb4)\
  2022-01-03 17:45:54 +0100
  * [MDEV-27407](https://jira.mariadb.org/browse/MDEV-27407) Different ASC/DESC index attributes on MERGE and underlying table can cause wrong results
* [Revision #58195449ee](https://github.com/MariaDB/server/commit/58195449ee)\
  2022-01-03 17:20:58 +0100
  * [MDEV-27406](https://jira.mariadb.org/browse/MDEV-27406) Index on a HEAP table retains DESC attribute despite being hash
* [Revision #aea076dc21](https://github.com/MariaDB/server/commit/aea076dc21)\
  2022-01-02 12:26:38 +0100
  * [MDEV-27393](https://jira.mariadb.org/browse/MDEV-27393) Timezone tables cannot have descending indexes
* [Revision #ddbb3d1447](https://github.com/MariaDB/server/commit/ddbb3d1447)\
  2021-12-21 01:01:49 +0100
  * [MDEV-27309](https://jira.mariadb.org/browse/MDEV-27309) Server crash or ASAN memcpy-param-overlap upon INSERT into Aria/MyISAM table with DESC key
* [Revision #799a30660e](https://github.com/MariaDB/server/commit/799a30660e)\
  2021-12-21 13:54:32 +0100
  * cleanup: reduce code duplication
* [Revision #775e7ce6d6](https://github.com/MariaDB/server/commit/775e7ce6d6)\
  2021-12-20 19:10:20 +0100
  * [MDEV-27303](https://jira.mariadb.org/browse/MDEV-27303) Table corruption after insert into a non-InnoDB table with DESC index
* [Revision #d6ab34b3da](https://github.com/MariaDB/server/commit/d6ab34b3da)\
  2022-01-02 12:08:21 +0100
  * [MDEV-27396](https://jira.mariadb.org/browse/MDEV-27396) DESC index attribute remains in Archive table definition, despite being apparently ignored
* [Revision #4c6e8fc572](https://github.com/MariaDB/server/commit/4c6e8fc572)\
  2022-01-24 18:38:12 +0100
  * [MDEV-27591](https://jira.mariadb.org/browse/MDEV-27591) Connect tables (FIX/DOS) don't work with DESC keys - wrong results
* [Revision #ae8600d514](https://github.com/MariaDB/server/commit/ae8600d514)\
  2022-01-03 19:22:30 +0100
  * [MDEV-27408](https://jira.mariadb.org/browse/MDEV-27408) DESC index on a Mroonga table causes wrong order of result set
* [Revision #918f524490](https://github.com/MariaDB/server/commit/918f524490)\
  2021-12-16 13:31:55 +0100
  * RocksDB doesn't support DESC indexes yet
* [Revision #fca37e49bb](https://github.com/MariaDB/server/commit/fca37e49bb)\
  2022-01-19 10:05:50 +0300
  * [MDEV-27529](https://jira.mariadb.org/browse/MDEV-27529) Wrong result upon query using index\_merge with DESC key (#2)
* [Revision #62760af4df](https://github.com/MariaDB/server/commit/62760af4df)\
  2022-01-10 16:19:03 +0300
  * [MDEV-27426](https://jira.mariadb.org/browse/MDEV-27426) Wrong result upon query using index\_merge with DESC key
* [Revision #96bdda6c96](https://github.com/MariaDB/server/commit/96bdda6c96)\
  2021-12-22 17:19:48 +0300
  * [MDEV-26996](https://jira.mariadb.org/browse/MDEV-26996) Reverse-ordered indexes: improve print-out
* [Revision #d6c6f79f5d](https://github.com/MariaDB/server/commit/d6c6f79f5d)\
  2021-12-20 23:51:55 +0300
  * [MDEV-26996](https://jira.mariadb.org/browse/MDEV-26996) Reverse-ordered indexes: remove SEL\_ARG::is\_ascending
* [Revision #cbfe6a5e86](https://github.com/MariaDB/server/commit/cbfe6a5e86)\
  2021-12-14 16:39:37 +0300
  * [MDEV-26996](https://jira.mariadb.org/browse/MDEV-26996) Support descending indexes in the range optimizer
* [Revision #3a82c256da](https://github.com/MariaDB/server/commit/3a82c256da)\
  2021-12-14 15:35:10 +0300
  * Descending indexes code exposed a gap in fix for [MDEV-25858](https://jira.mariadb.org/browse/MDEV-25858).
* [Revision #791146b9d2](https://github.com/MariaDB/server/commit/791146b9d2)\
  2021-12-14 01:47:01 +0300
  * [MDEV-26996](https://jira.mariadb.org/browse/MDEV-26996) Support descending indexes in the range optimizer
* [Revision #a4cac0e07a](https://github.com/MariaDB/server/commit/a4cac0e07a)\
  2021-11-24 16:50:21 +0100
  * [MDEV-26938](https://jira.mariadb.org/browse/MDEV-26938) Support descending indexes internally in InnoDB (server part)
* [Revision #358921ce32](https://github.com/MariaDB/server/commit/358921ce32)\
  2022-01-26 11:01:39 +0200
  * [MDEV-26938](https://jira.mariadb.org/browse/MDEV-26938) Support descending indexes internally in InnoDB
* [Revision #349a595bc4](https://github.com/MariaDB/server/commit/349a595bc4)\
  2021-12-20 18:57:52 +0100
  * cleanup: tests
* Merge [Revision #c1cef1afa9](https://github.com/MariaDB/server/commit/c1cef1afa9) 2022-01-26 13:57:00 +0100 - Merge remote-tracking branch 'origin/bb-10.8-wlad' into 10.8
* [Revision #9d93b51eff](https://github.com/MariaDB/server/commit/9d93b51eff)\
  2022-01-26 13:28:10 +0100
  * [MDEV-14425](https://jira.mariadb.org/browse/MDEV-14425) fix inadverent changes on Windows
* [Revision #db2013787d](https://github.com/MariaDB/server/commit/db2013787d)\
  2021-12-03 02:55:34 +0400
  * [MDEV-23570](https://jira.mariadb.org/browse/MDEV-23570) deprecate keep\_files\_on\_create
* [Revision #93756c992f](https://github.com/MariaDB/server/commit/93756c992f)\
  2022-01-25 09:00:18 +0200
  * [MDEV-27229](https://jira.mariadb.org/browse/MDEV-27229) fixup: GCC -Wunused-function
* [Revision #050508672c](https://github.com/MariaDB/server/commit/050508672c)\
  2021-11-26 06:56:04 +0400
  * A clean-up for [MDEV-10654](https://jira.mariadb.org/browse/MDEV-10654) add support IN, OUT, INOUT parameter qualifiers for stored functions
* [Revision #4572dc23f7](https://github.com/MariaDB/server/commit/4572dc23f7)\
  2021-09-25 22:20:22 +0530
  * [MDEV-10654](https://jira.mariadb.org/browse/MDEV-10654) add support IN, OUT, INOUT parameter qualifiers for stored functions
* [Revision #5595ed9d9f](https://github.com/MariaDB/server/commit/5595ed9d9f)\
  2022-01-19 14:17:36 +0900
  * [MDEV-27521](https://jira.mariadb.org/browse/MDEV-27521) SIGSEGV in spider\_parse\_connect\_info in [MDEV-27106](https://jira.mariadb.org/browse/MDEV-27106) branch
* [Revision #0599dd9014](https://github.com/MariaDB/server/commit/0599dd9014)\
  2022-01-24 15:44:23 +0900
  * [MDEV-26858](https://jira.mariadb.org/browse/MDEV-26858) Spider: Remove dead code related to HandlerSocket
* [Revision #72f34df349](https://github.com/MariaDB/server/commit/72f34df349)\
  2021-11-25 17:03:02 +0900
  * [MDEV-27106](https://jira.mariadb.org/browse/MDEV-27106) Spider: specify connection to data node by engine-defined attributes
* [Revision #c5d09f731a](https://github.com/MariaDB/server/commit/c5d09f731a)\
  2021-11-05 16:39:28 +0900
  * [MDEV-5271](https://jira.mariadb.org/browse/MDEV-5271) Support engine-defined attributes per partition
* [Revision #83dd7db69d](https://github.com/MariaDB/server/commit/83dd7db69d)\
  2022-01-24 17:27:56 +1100
  * [MDEV-27314](https://jira.mariadb.org/browse/MDEV-27314) InnoDB Buffer Pool Resize output cleanup (mtr postfix)
* [Revision #d0ca235d16](https://github.com/MariaDB/server/commit/d0ca235d16)\
  2022-01-22 17:13:14 -0600
  * [MDEV-27314](https://jira.mariadb.org/browse/MDEV-27314) InnoDB Buffer Pool Resize output cleanup
* [Revision #c5c61b51b6](https://github.com/MariaDB/server/commit/c5c61b51b6)\
  2021-10-11 12:53:11 -0700
  * Extend the Gitlab-CI pipeline to run mini benchmark
* [Revision #1f5fc7b745](https://github.com/MariaDB/server/commit/1f5fc7b745)\
  2022-01-22 10:24:47 +0200
  * [MDEV-27208](https://jira.mariadb.org/browse/MDEV-27208): mtr --ps-protocol test fixup
* [Revision #5b3ad94c7b](https://github.com/MariaDB/server/commit/5b3ad94c7b)\
  2022-01-21 19:24:00 +0200
  * [MDEV-27208](https://jira.mariadb.org/browse/MDEV-27208): Extend CRC32() and implement CRC32C()
* [Revision #b07920b634](https://github.com/MariaDB/server/commit/b07920b634)\
  2022-01-21 16:16:32 +0200
  * [MDEV-27199](https://jira.mariadb.org/browse/MDEV-27199): Remove FIL\_PAGE\_FILE\_FLUSH\_LSN
* [Revision #88d9fbb484](https://github.com/MariaDB/server/commit/88d9fbb484)\
  2022-01-21 16:13:28 +0200
  * Disable adaptive spinning on buf\_pool.mutex
* [Revision #5d54fd611f](https://github.com/MariaDB/server/commit/5d54fd611f)\
  2022-01-21 16:13:04 +0200
  * Cleanup: Replace ut\_crc32c(x,y) with my\_crc32c(0,x,y)
* [Revision #685d958e38](https://github.com/MariaDB/server/commit/685d958e38)\
  2022-01-21 16:03:47 +0200
  * [MDEV-14425](https://jira.mariadb.org/browse/MDEV-14425) Improve the redo log for concurrency
* [Revision #baef53a70c](https://github.com/MariaDB/server/commit/baef53a70c)\
  2022-01-20 15:48:08 +0100
  * [MDEV-27540](https://jira.mariadb.org/browse/MDEV-27540) Different OpenSSL versions mix up in build depending on cmake options
* [Revision #d42c2efbaa](https://github.com/MariaDB/server/commit/d42c2efbaa)\
  2021-11-08 18:48:19 +0100
  * [MDEV-25785](https://jira.mariadb.org/browse/MDEV-25785) Add support for OpenSSL 3.0
* Merge [Revision #a855d6d93a](https://github.com/MariaDB/server/commit/a855d6d93a) 2022-01-20 08:24:12 +0200 - Merge 10.7 into 10.8
* [Revision #852534dc99](https://github.com/MariaDB/server/commit/852534dc99)\
  2022-01-20 08:24:03 +0200
  * [MDEV-26519](https://jira.mariadb.org/browse/MDEV-26519) fixup: GCC 11 -Og -Wmaybe-uninitialized
* Merge [Revision #da78030ec8](https://github.com/MariaDB/server/commit/da78030ec8) 2022-01-19 18:35:27 +0300 - Merge [MDEV-26519](https://jira.mariadb.org/browse/MDEV-26519): JSON\_HB histograms into 10.8
* [Revision #ce4956f322](https://github.com/MariaDB/server/commit/ce4956f322)\
  2022-01-19 18:02:40 +0300
  * Code cleanup
* [Revision #f7e49c98e6](https://github.com/MariaDB/server/commit/f7e49c98e6)\
  2022-01-19 15:54:38 +0300
  * Switch the default histogram\_type to still be DOUBLE\_PREC\_HB
* [Revision #4842a56356](https://github.com/MariaDB/server/commit/4842a56356)\
  2022-01-14 20:04:19 +0300
  * JSON\_HB histogram: represent values of BIT() columns in hex always
* [Revision #dae20dde4e](https://github.com/MariaDB/server/commit/dae20dde4e)\
  2022-01-11 17:09:55 +0300
  * [MDEV-26901](https://jira.mariadb.org/browse/MDEV-26901): Estimation for filtered rows less precise ... #4
* [Revision #db8f15be93](https://github.com/MariaDB/server/commit/db8f15be93)\
  2022-01-11 16:58:51 +0300
  * [MDEV-27229](https://jira.mariadb.org/browse/MDEV-27229): Estimation for filtered rows less precise ... #5
* [Revision #d3e511d421](https://github.com/MariaDB/server/commit/d3e511d421)\
  2022-01-08 22:54:23 +0300
  * [MDEV-27243](https://jira.mariadb.org/browse/MDEV-27243): Estimation for filtered rows less precise ... #7
* [Revision #531dd708ef](https://github.com/MariaDB/server/commit/531dd708ef)\
  2022-01-08 22:36:12 +0300
  * [MDEV-27229](https://jira.mariadb.org/browse/MDEV-27229): Estimation for filtered rows less precise ... #5
* [Revision #67d4d0426f](https://github.com/MariaDB/server/commit/67d4d0426f)\
  2021-12-14 14:45:47 +0300
  * Update test results
* [Revision #905634dc3f](https://github.com/MariaDB/server/commit/905634dc3f)\
  2021-12-13 23:46:04 +0300
  * [MDEV-27230](https://jira.mariadb.org/browse/MDEV-27230): Estimation for filtered rows less precise ...
* [Revision #08f1c4a2e0](https://github.com/MariaDB/server/commit/08f1c4a2e0)\
  2021-12-13 22:54:33 +0300
  * [MDEV-27203](https://jira.mariadb.org/browse/MDEV-27203): Valgrind / MSAN errors in Histogram\_json\_hb::parse\_bucket
* [Revision #d8d57d2c27](https://github.com/MariaDB/server/commit/d8d57d2c27)\
  2021-12-03 20:13:43 +0300
  * [MDEV-26764](https://jira.mariadb.org/browse/MDEV-26764): JSON\_HB Histograms: handle BINARY and unassigned characters
* [Revision #748b293c14](https://github.com/MariaDB/server/commit/748b293c14)\
  2021-12-03 19:03:42 +0300
  * More test coverage
* [Revision #c2d2c1e727](https://github.com/MariaDB/server/commit/c2d2c1e727)\
  2021-12-03 18:08:10 +0300
  * [MDEV-26519](https://jira.mariadb.org/browse/MDEV-26519): Improved histograms
* [Revision #a0916cf5a2](https://github.com/MariaDB/server/commit/a0916cf5a2)\
  2021-12-02 20:47:08 +0300
  * [MDEV-26519](https://jira.mariadb.org/browse/MDEV-26519): Improved histograms: Better error reporting, test coverage
* [Revision #a0f93f433a](https://github.com/MariaDB/server/commit/a0f93f433a)\
  2021-12-02 14:38:51 +0300
  * Rename histogram\_hb\_v2 -> histogram\_hb
* [Revision #1d14176ec4](https://github.com/MariaDB/server/commit/1d14176ec4)\
  2021-12-02 11:54:10 +0300
  * [MDEV-26519](https://jira.mariadb.org/browse/MDEV-26519): Improved histograms: Make JSON parser efficient
* [Revision #be55ad0d34](https://github.com/MariaDB/server/commit/be55ad0d34)\
  2021-11-29 16:11:18 +0300
  * [MDEV-27062](https://jira.mariadb.org/browse/MDEV-27062): Make histogram\_type=JSON\_HB the new default
* [Revision #eb6a9ad705](https://github.com/MariaDB/server/commit/eb6a9ad705)\
  2021-11-26 20:03:08 +0300
  * [MDEV-26886](https://jira.mariadb.org/browse/MDEV-26886): Estimation for filtered rows less precise with JSON histogram
* [Revision #106c785e2d](https://github.com/MariaDB/server/commit/106c785e2d)\
  2021-11-02 15:18:50 +0300
  * [MDEV-26911](https://jira.mariadb.org/browse/MDEV-26911): Unexpected ER\_DUP\_KEY, ASAN errors, double free detected in ...
* [Revision #ac0194bd0e](https://github.com/MariaDB/server/commit/ac0194bd0e)\
  2021-10-24 20:31:08 +0300
  * [MDEV-26892](https://jira.mariadb.org/browse/MDEV-26892): JSON histograms become invalid with a specific (corrupt) value ..
* [Revision #05877df472](https://github.com/MariaDB/server/commit/05877df472)\
  2021-10-22 19:43:19 +0300
  * [MDEV-26849](https://jira.mariadb.org/browse/MDEV-26849): JSON Histograms: point selectivity estimates are off
* [Revision #f3f78bed85](https://github.com/MariaDB/server/commit/f3f78bed85)\
  2021-10-18 16:31:18 +0300
  * [MDEV-26750](https://jira.mariadb.org/browse/MDEV-26750): Estimation for filtered rows is far off with JSON\_HB histogram
* [Revision #27539cd2c8](https://github.com/MariaDB/server/commit/27539cd2c8)\
  2021-10-11 22:47:26 +0300
  * [MDEV-26801](https://jira.mariadb.org/browse/MDEV-26801): Valgrind/MSAN errors in Column\_statistics\_collected::finish ...
* [Revision #93d5980435](https://github.com/MariaDB/server/commit/93d5980435)\
  2021-10-11 17:07:28 +0300
  * [MDEV-26709](https://jira.mariadb.org/browse/MDEV-26709): JSON histogram may contain bucketS than histogram\_size allows
* [Revision #3936dc3353](https://github.com/MariaDB/server/commit/3936dc3353)\
  2021-10-10 11:51:04 +0300
  * [MDEV-26724](https://jira.mariadb.org/browse/MDEV-26724) Endless loop in json\_escape\_to\_string upon ... empty string
* [Revision #8e0a342b91](https://github.com/MariaDB/server/commit/8e0a342b91)\
  2021-10-05 11:16:54 +0300
  * Update test results
* [Revision #b17f33a04b](https://github.com/MariaDB/server/commit/b17f33a04b)\
  2021-10-04 22:37:59 +0300
  * [MDEV-26737](https://jira.mariadb.org/browse/MDEV-26737): Outdated VARIABLE\_COMMENT for HISTOGRAM\_TYPE in I\_S.SYSTEM\_VARIABLES
* [Revision #943b8fccf9](https://github.com/MariaDB/server/commit/943b8fccf9)\
  2021-10-01 23:24:05 +0300
  * [MDEV-26710](https://jira.mariadb.org/browse/MDEV-26710): Histogram field in mysql.column\_stats is too short
* [Revision #5d66eeb3a1](https://github.com/MariaDB/server/commit/5d66eeb3a1)\
  2021-10-01 20:50:43 +0300
  * [MDEV-26724](https://jira.mariadb.org/browse/MDEV-26724) Endless loop in json\_escape\_to\_string upon ... empty string
* [Revision #43a8d9f156](https://github.com/MariaDB/server/commit/43a8d9f156)\
  2021-10-01 14:33:23 +0300
  * [MDEV-26595](https://jira.mariadb.org/browse/MDEV-26595): ASAN use-after-poison my\_strnxfrm\_simple\_internal / Histogram\_json\_hb::range\_selectivity
* [Revision #5ef350a7f1](https://github.com/MariaDB/server/commit/5ef350a7f1)\
  2021-10-01 14:24:41 +0300
  * [MDEV-26589](https://jira.mariadb.org/browse/MDEV-26589): Assertion failure upon DECODE\_HISTOGRAM with NULLs
* [Revision #5c709ef18c](https://github.com/MariaDB/server/commit/5c709ef18c)\
  2021-10-01 14:15:17 +0300
  * [MDEV-26724](https://jira.mariadb.org/browse/MDEV-26724) Endless loop in json\_escape\_to\_string upon ... empty string
* [Revision #61cd4f4412](https://github.com/MariaDB/server/commit/61cd4f4412)\
  2021-09-29 20:11:48 +0300
  * [MDEV-26711](https://jira.mariadb.org/browse/MDEV-26711): Values in JSON histograms are not properly quoted
* [Revision #d03daaf8a8](https://github.com/MariaDB/server/commit/d03daaf8a8)\
  2021-09-14 20:18:07 +0300
  * Use JSON\_NAME, not the "histogram\_hb\_v2" constant
* [Revision #702f4efcd9](https://github.com/MariaDB/server/commit/702f4efcd9)\
  2021-09-14 17:36:10 +0300
  * More "straightforward" memory management
* [Revision #28ad128585](https://github.com/MariaDB/server/commit/28ad128585)\
  2021-09-14 14:29:41 +0300
  * Fix off-by-one error in Histogram\_json\_hb::find\_bucket
* [Revision #b179640219](https://github.com/MariaDB/server/commit/b179640219)\
  2021-09-13 14:55:10 +0300
  * [MDEV-26590](https://jira.mariadb.org/browse/MDEV-26590): Stack smashing/buffer overflow in Histogram\_json\_hb::parse
* [Revision #382250c05c](https://github.com/MariaDB/server/commit/382250c05c)\
  2021-09-11 19:43:08 +0300
  * Address review input
* [Revision #cf8927e9cb](https://github.com/MariaDB/server/commit/cf8927e9cb)\
  2021-09-10 20:02:46 +0300
  * Fix the previous cset: next() should have element\_count as parameter
* [Revision #b6121ca36a](https://github.com/MariaDB/server/commit/b6121ca36a)\
  2021-09-10 19:49:33 +0300
  * Fix compile warnings/error on Windows
* [Revision #6375873c9a](https://github.com/MariaDB/server/commit/6375873c9a)\
  2021-09-10 17:49:32 +0300
  * Fixes in opt\_histogram\_json.cc in the last commits
* [Revision #49a7bbb1f6](https://github.com/MariaDB/server/commit/49a7bbb1f6)\
  2021-09-10 17:16:43 +0300
  * Valgrind fixes, poor .result fixes, code cleanups
* [Revision #ace961a1e7](https://github.com/MariaDB/server/commit/ace961a1e7)\
  2021-09-10 14:59:32 +0300
  * Fix compile error on windows
* [Revision #f460272054](https://github.com/MariaDB/server/commit/f460272054)\
  2021-09-10 10:45:04 +0300
  * [MDEV-26519](https://jira.mariadb.org/browse/MDEV-26519): JSON Histograms: improve histogram collection
* [Revision #d64e104810](https://github.com/MariaDB/server/commit/d64e104810)\
  2021-09-07 10:38:36 +0300
  * Fix compilation on windows
* [Revision #5ddbd72af4](https://github.com/MariaDB/server/commit/5ddbd72af4)\
  2021-09-06 18:18:08 +0300
  * Correctly decode string field values for pos\_in\_interval\_for\_string call
* [Revision #223fa6a891](https://github.com/MariaDB/server/commit/223fa6a891)\
  2021-09-04 23:17:39 +0300
  * Make tests pass
* [Revision #e0f42d32e5](https://github.com/MariaDB/server/commit/e0f42d32e5)\
  2021-09-04 18:18:19 +0300
  * Fix compilation on windows part #3
* [Revision #00377dbae8](https://github.com/MariaDB/server/commit/00377dbae8)\
  2021-09-04 18:00:21 +0300
  * Fix embedded to work
* [Revision #716c98b15d](https://github.com/MariaDB/server/commit/716c98b15d)\
  2021-09-04 17:54:07 +0300
  * Fix compilation on windows part 2
* [Revision #1861a2a2cd](https://github.com/MariaDB/server/commit/1861a2a2cd)\
  2021-09-04 17:37:24 +0300
  * Rollback a change from previous commit
* [Revision #9271bd17f7](https://github.com/MariaDB/server/commit/9271bd17f7)\
  2021-09-04 17:24:47 +0300
  * More code cleanups
* [Revision #1d98168547](https://github.com/MariaDB/server/commit/1d98168547)\
  2021-09-04 17:11:16 +0300
  * Move JSON histograms code into its own files
* [Revision #4ab2b78b65](https://github.com/MariaDB/server/commit/4ab2b78b65)\
  2021-09-04 16:28:10 +0300
  * Histogram code cleanup and fixes
* [Revision #a9c1feea60](https://github.com/MariaDB/server/commit/a9c1feea60)\
  2021-08-31 23:58:03 +0300
  * Fix statistics\_upgrade.test
* [Revision #9de81b2cde](https://github.com/MariaDB/server/commit/9de81b2cde)\
  2021-08-31 17:46:07 +0300
  * Handle upgrades
* [Revision #e675f44624](https://github.com/MariaDB/server/commit/e675f44624)\
  2021-08-31 16:17:06 +0300
  * Code cleanup: don't duplicate the position-in-interval code
* [Revision #899dfb078e](https://github.com/MariaDB/server/commit/899dfb078e)\
  2021-08-31 14:17:33 +0300
  * Code cleanups part #3
* [Revision #859c14ff01](https://github.com/MariaDB/server/commit/859c14ff01)\
  2021-08-31 13:47:21 +0300
  * Better names: s/histogram\_/histogram/, s/Histogram\_json/Histogram\_json\_hb/
* [Revision #fc6a4a33b2](https://github.com/MariaDB/server/commit/fc6a4a33b2)\
  2021-08-31 13:39:39 +0300
  * Cleanup histogram collection code
* [Revision #02a67307d3](https://github.com/MariaDB/server/commit/02a67307d3)\
  2021-08-31 11:09:02 +0300
  * Fix compiation on windows
* [Revision #3486bf4110](https://github.com/MariaDB/server/commit/3486bf4110)\
  2021-08-31 00:53:09 +0300
  * Code cleanup + reduce the diff size
* [Revision #229c836d6a](https://github.com/MariaDB/server/commit/229c836d6a)\
  2021-08-31 00:31:29 +0300
  * Fix valgrind failure
* [Revision #dde6d76995](https://github.com/MariaDB/server/commit/dde6d76995)\
  2021-08-30 12:31:42 +0300
  * Trivial code cleanup
* [Revision #a93b377863](https://github.com/MariaDB/server/commit/a93b377863)\
  2021-08-29 23:55:39 +0300
  * Fix histogram memory management
* [Revision #032587e2dc](https://github.com/MariaDB/server/commit/032587e2dc)\
  2021-08-29 21:24:19 +0300
  * Code cleanup part #3
* [Revision #fcf58a5e0f](https://github.com/MariaDB/server/commit/fcf58a5e0f)\
  2021-08-29 19:32:25 +0300
  * Code cleanup part#2: do not copy key values in xxx\_selectivity() functions
* [Revision #2a1cdbabec](https://github.com/MariaDB/server/commit/2a1cdbabec)\
  2021-08-29 14:37:45 +0300
  * Fix JSON parsing: future-proof data representation in JSON, code cleanup
* [Revision #a0b4a86822](https://github.com/MariaDB/server/commit/a0b4a86822)\
  2021-08-28 12:31:13 +0300
  * Code cleanup part #2.
* [Revision #1496a52d6d](https://github.com/MariaDB/server/commit/1496a52d6d)\
  2021-08-28 12:31:00 +0300
  * Update test results (new histogram type: JSON\_HB)
* [Revision #72c0ba43b2](https://github.com/MariaDB/server/commit/72c0ba43b2)\
  2021-08-27 22:28:59 +0300
  * Code cleanup part #1
* [Revision #f76e310ace](https://github.com/MariaDB/server/commit/f76e310ace)\
  2021-08-27 16:57:22 +0300
  * Rename histogram\_type=JSON to JSON\_HB
* [Revision #a48e63c5fe](https://github.com/MariaDB/server/commit/a48e63c5fe)\
  2021-08-27 16:49:45 +0300
  * Fix compile error and test failure:
* [Revision #096995b106](https://github.com/MariaDB/server/commit/096995b106)\
  2021-08-22 17:31:44 +0100
  * Fix column range cardinality crash when histogram is null
* [Revision #058a90e6f5](https://github.com/MariaDB/server/commit/058a90e6f5)\
  2021-08-22 15:37:14 +0100
  * Use existing statistics test to improve coverage for JSON statistics
* [Revision #3692adebd4](https://github.com/MariaDB/server/commit/3692adebd4)\
  2021-08-22 08:54:52 +0100
  * Fix avg\_frequency statistics and remove stderr dumps
* [Revision #bff65a813e](https://github.com/MariaDB/server/commit/bff65a813e)\
  2021-08-21 09:17:23 +0100
  * Implement point selectivity for JSON histograms
* [Revision #547f805311](https://github.com/MariaDB/server/commit/547f805311)\
  2021-08-21 01:09:39 +0100
  * Refactor histogram point selectivity
* [Revision #e10d99ce87](https://github.com/MariaDB/server/commit/e10d99ce87)\
  2021-08-21 00:50:55 +0100
  * Backfill json histogram bounds during building
* [Revision #3d952cd8bd](https://github.com/MariaDB/server/commit/3d952cd8bd)\
  2021-08-19 14:38:11 +0100
  * Improve tests and test results to cover larger cases
* [Revision #63cbd0748b](https://github.com/MariaDB/server/commit/63cbd0748b)\
  2021-08-17 09:54:04 +0100
  * replace range\_selectivity methods for Histograms and add tests
* [Revision #c129689ddc](https://github.com/MariaDB/server/commit/c129689ddc)\
  2021-08-16 10:09:56 +0100
  * Use binary search to compute range selectivity \* it also adds an "explain select" statement to the test so that the fprintf calls can print the computed intervals to mysqld.1.err
* [Revision #c605285bb8](https://github.com/MariaDB/server/commit/c605285bb8)\
  2021-08-11 07:19:39 +0100
  * fix returned value type for empty json objects
* [Revision #69f24c238e](https://github.com/MariaDB/server/commit/69f24c238e)\
  2021-08-11 06:58:18 +0100
  * Use generic Histogram\_base class for Histogram\_builders
* [Revision #21e0f5487f](https://github.com/MariaDB/server/commit/21e0f5487f)\
  2021-08-06 20:08:16 +0300
  * [MDEV-21130](https://jira.mariadb.org/browse/MDEV-21130): Histograms: use JSON as on-disk format
* [Revision #e778d12f83](https://github.com/MariaDB/server/commit/e778d12f83)\
  2021-08-05 23:49:44 +0100
  * report parse error when parsing JSON histogram fails
* [Revision #fe2e516a50](https://github.com/MariaDB/server/commit/fe2e516a50)\
  2021-07-31 20:21:38 +0100
  * inform test result of zero hist\_size for json histogram
* [Revision #bf4d0dcfe2](https://github.com/MariaDB/server/commit/bf4d0dcfe2)\
  2021-07-30 06:55:17 +0100
  * implement parse and serialize for histogram json
* [Revision #9bba595528](https://github.com/MariaDB/server/commit/9bba595528)\
  2021-07-29 23:21:43 +0100
  * remove unneeded shared methods
* [Revision #1fa7af749e](https://github.com/MariaDB/server/commit/1fa7af749e)\
  2021-07-28 05:19:06 +0100
  * Split histogram classes and into JSON and binary classes
* [Revision #1998b787ac](https://github.com/MariaDB/server/commit/1998b787ac)\
  2021-07-23 01:26:50 +0300
  * [MDEV-21130](https://jira.mariadb.org/browse/MDEV-21130): Histograms: use JSON as on-disk format
* [Revision #fb2edab3eb](https://github.com/MariaDB/server/commit/fb2edab3eb)\
  2021-07-23 08:57:41 +0100
  * Extract json parser functions from class
* [Revision #6bc2df5fa4](https://github.com/MariaDB/server/commit/6bc2df5fa4)\
  2021-07-21 07:23:01 +0100
  * Add parser to read JSON array (of histograms) into string vector
* [Revision #524322ad3e](https://github.com/MariaDB/server/commit/524322ad3e)\
  2021-07-07 22:45:43 +0100
  * Properly initialize bucket bounds vector
* [Revision #d4d539803b](https://github.com/MariaDB/server/commit/d4d539803b)\
  2021-07-02 10:50:51 +0100
  * Fix garbage null values at end of histogram json
* [Revision #a378735862](https://github.com/MariaDB/server/commit/a378735862)\
  2021-07-02 10:31:25 +0100
  * Fix garbage null values at end of json array elements
* [Revision #9954aecc2b](https://github.com/MariaDB/server/commit/9954aecc2b)\
  2021-06-30 05:51:08 +0100
  * Store bucket bounds and extend test cases for JSON histogram
* [Revision #237447de63](https://github.com/MariaDB/server/commit/237447de63)\
  2021-06-24 07:41:09 +0100
  * rough base for json histogram builder
* [Revision #567552b410](https://github.com/MariaDB/server/commit/567552b410)\
  2021-06-22 18:41:37 +0100
  * Update test results to match updated system tables
* [Revision #2373133f99](https://github.com/MariaDB/server/commit/2373133f99)\
  2021-06-16 09:54:34 +0100
  * record statistics\_json test
* [Revision #79cdb535da](https://github.com/MariaDB/server/commit/79cdb535da)\
  2021-06-14 17:14:11 +0100
  * add json statistics test and change histogram column type to blob
* [Revision #2aca7b0c33](https://github.com/MariaDB/server/commit/2aca7b0c33)\
  2021-06-09 20:39:50 +0100
  * Prepare JSON as valid histogram\_type
* Merge [Revision #e222e44d1b](https://github.com/MariaDB/server/commit/e222e44d1b) 2022-01-18 21:37:52 +0100 - Merge branch 'preview-10.8-[MDEV-26713](https://jira.mariadb.org/browse/MDEV-26713)-Windows-i18-support' into 10.8
* [Revision #2e48fbe3f5](https://github.com/MariaDB/server/commit/2e48fbe3f5)\
  2022-01-18 17:32:53 +0100
  * [MDEV-27525](https://jira.mariadb.org/browse/MDEV-27525) Invalid (non-UTF8) characters found for option 'plugin\_dir'
* [Revision #71966c7306](https://github.com/MariaDB/server/commit/71966c7306)\
  2021-11-26 18:41:35 +0100
  * [MDEV-26713](https://jira.mariadb.org/browse/MDEV-26713) allow users with non-UTF8 passwords to login after upgrade.
* [Revision #9ea83f7fbd](https://github.com/MariaDB/server/commit/9ea83f7fbd)\
  2021-11-29 19:47:36 +0100
  * [MDEV-26713](https://jira.mariadb.org/browse/MDEV-26713) set console codepage to what user set in --default-character-set
* [Revision #74f2e6c85e](https://github.com/MariaDB/server/commit/74f2e6c85e)\
  2021-11-24 10:15:11 +0100
  * [MDEV-26713](https://jira.mariadb.org/browse/MDEV-26713) Add test for mysql\_install\_db creating service, with i18
* [Revision #57d52657a2](https://github.com/MariaDB/server/commit/57d52657a2)\
  2021-11-23 13:05:25 +0100
  * [MDEV-26713](https://jira.mariadb.org/browse/MDEV-26713) UTF8 support on Windows , add mysql\_install\_db tests
* [Revision #825f9c7b50](https://github.com/MariaDB/server/commit/825f9c7b50)\
  2021-11-23 12:28:28 +0100
  * [MDEV-27227](https://jira.mariadb.org/browse/MDEV-27227) mysqltest, Windows - support background execution in 'exec' command
* [Revision #6b4b625da3](https://github.com/MariaDB/server/commit/6b4b625da3)\
  2021-12-11 04:25:22 +0100
  * [MDEV-26713](https://jira.mariadb.org/browse/MDEV-26713) UTF8 support on Windows, convert my.ini from ANSI to UTF8
* [Revision #a296c52627](https://github.com/MariaDB/server/commit/a296c52627)\
  2021-11-22 13:22:05 +0100
  * [MDEV-26713](https://jira.mariadb.org/browse/MDEV-26713) UTF8 support on Windows, mysql\_upgrade\_service preparation
* [Revision #a4fc41b6b4](https://github.com/MariaDB/server/commit/a4fc41b6b4)\
  2021-11-22 12:34:10 +0100
  * [MDEV-26713](https://jira.mariadb.org/browse/MDEV-26713) Treat codepage 65001 as utf8mb4, not utf8mb3
* [Revision #ba9d231b5a](https://github.com/MariaDB/server/commit/ba9d231b5a)\
  2021-11-22 12:29:15 +0100
  * [MDEV-26713](https://jira.mariadb.org/browse/MDEV-26713) Set activeCodePage=UTF8 for windows programs
* [Revision #4d3ac32848](https://github.com/MariaDB/server/commit/4d3ac32848)\
  2021-11-19 14:14:38 +0100
  * [MDEV-27093](https://jira.mariadb.org/browse/MDEV-27093) Do not pass root password in HEX(clear text) from mariadb-install-db.exe to bootstrap
* [Revision #ea0a5cb0a4](https://github.com/MariaDB/server/commit/ea0a5cb0a4)\
  2021-11-19 14:03:51 +0100
  * [MDEV-27092](https://jira.mariadb.org/browse/MDEV-27092) Windows - services that have non-ASCII characters do not work with activeCodePage=UTF8
* [Revision #99e5ae3b1a](https://github.com/MariaDB/server/commit/99e5ae3b1a)\
  2021-11-19 12:03:48 +0100
  * [MDEV-27090](https://jira.mariadb.org/browse/MDEV-27090) Windows client - ReadConsoleA does not work correctly with UTF8 codepage
* [Revision #9e9b211f22](https://github.com/MariaDB/server/commit/9e9b211f22)\
  2021-12-10 23:35:04 +0100
  * [MDEV-27089](https://jira.mariadb.org/browse/MDEV-27089) Windows : incorrect handling of non-ASCIIs in get\_tty\_password
* [Revision #d9f7a6b331](https://github.com/MariaDB/server/commit/d9f7a6b331)\
  2021-12-03 12:12:14 +1100
  * [MDEV-27158](https://jira.mariadb.org/browse/MDEV-27158): humanize the bytes in innodb info/error messages
* [Revision #d434250ee1](https://github.com/MariaDB/server/commit/d434250ee1)\
  2021-12-02 14:30:26 +1100
  * [MDEV-25342](https://jira.mariadb.org/browse/MDEV-25342): autosize innodb\_buffer\_pool\_chunk\_size
* Merge [Revision #e5b75ac3d7](https://github.com/MariaDB/server/commit/e5b75ac3d7) 2022-01-18 13:19:00 +0200 - Merge 10.7 into 10.8
* [Revision #4775a40627](https://github.com/MariaDB/server/commit/4775a40627)\
  2020-02-20 13:05:15 +0200
  * Deb: Track libmariadb3 ABI explicitly to detect future symbol changes
* Merge [Revision #347f6d01e3](https://github.com/MariaDB/server/commit/347f6d01e3) 2022-01-14 19:47:33 +0200 - Merge 10.7 into 10.8
* Merge [Revision #4b14874c28](https://github.com/MariaDB/server/commit/4b14874c28) 2022-01-12 17:08:08 +0200 - Merge 10.7 into 10.8
* [Revision #f825954558](https://github.com/MariaDB/server/commit/f825954558)\
  2022-01-03 15:17:04 +0100
  * C/C 3.3
* [Revision #a81c75f5a9](https://github.com/MariaDB/server/commit/a81c75f5a9)\
  2021-10-14 23:10:18 +0000
  * [MDEV-27435](https://jira.mariadb.org/browse/MDEV-27435): Support extra initialization file for mysql\_install\_db
* [Revision #4f4d9586de](https://github.com/MariaDB/server/commit/4f4d9586de)\
  2022-01-06 09:42:06 +1100
  * mysys: my\_rdtsc note about ARM counter
* [Revision #d18f6f2631](https://github.com/MariaDB/server/commit/d18f6f2631)\
  2022-01-04 13:59:59 +1100
  * [MDEV-27429](https://jira.mariadb.org/browse/MDEV-27429): Support RISC-V cycle timer
* Merge [Revision #b0d632a840](https://github.com/MariaDB/server/commit/b0d632a840) 2022-01-04 15:56:14 +0200 - Merge 10.7 into 10.8
* Merge [Revision #daf4fa5238](https://github.com/MariaDB/server/commit/daf4fa5238) 2022-01-04 10:30:45 +0200 - Merge 10.7 into 10.8
* [Revision #756568f26c](https://github.com/MariaDB/server/commit/756568f26c)\
  2021-12-29 22:50:10 +0400
  * [MDEV-22256](https://jira.mariadb.org/browse/MDEV-22256) Assertion \`length == pack\_length()' failed in Field\_timestamp\_with\_dec::sort\_string
* [Revision #c9fcea14e9](https://github.com/MariaDB/server/commit/c9fcea14e9)\
  2021-12-15 21:11:26 +0200
  * [MDEV-27036](https://jira.mariadb.org/browse/MDEV-27036): re-enable my\_json\_writer-t unit test
* [Revision #6208228b78](https://github.com/MariaDB/server/commit/6208228b78)\
  2021-12-15 15:43:03 +0100
  * disable galera\_3nodes.galera\_ipv6\_mariadb-backup
* Merge [Revision #4434fb4a75](https://github.com/MariaDB/server/commit/4434fb4a75) 2021-12-14 14:29:04 +0200 - Merge 10.7 into 10.8
* [Revision #ea94895369](https://github.com/MariaDB/server/commit/ea94895369)\
  2021-12-09 11:05:14 +0200
  * [MDEV-27206](https://jira.mariadb.org/browse/MDEV-27206): \[ERROR] Duplicated key: cause, Assertion \`is\_uniq\_key' failed with optimizer trace
* Merge [Revision #ccdf5711a8](https://github.com/MariaDB/server/commit/ccdf5711a8) 2021-12-10 13:05:06 +0200 - Merge 10.7 into 10.8
* Merge [Revision #978116d991](https://github.com/MariaDB/server/commit/978116d991) 2021-12-10 12:29:14 +0200 - Merge 10.7 into 10.8
* [Revision #c88e37ff85](https://github.com/MariaDB/server/commit/c88e37ff85)\
  2021-12-09 16:49:40 +0300
  * [MDEV-27204](https://jira.mariadb.org/browse/MDEV-27204): \[ERROR] Json\_writer: a member name was expected, Assertion \`got\_name
* [Revision #1e8bcbd0a0](https://github.com/MariaDB/server/commit/1e8bcbd0a0)\
  2021-12-07 09:57:51 +0100
  * Revert "[MDEV-27036](https://jira.mariadb.org/browse/MDEV-27036): re-enable my\_json\_writer-t unit test"
* [Revision #23bfacf1cc](https://github.com/MariaDB/server/commit/23bfacf1cc)\
  2021-12-06 18:42:58 +0100
  * Revert "Improve LibFMT detection"
* [Revision #2d21917e7d](https://github.com/MariaDB/server/commit/2d21917e7d)\
  2021-11-30 18:11:14 -0700
  * [MDEV-27036](https://jira.mariadb.org/browse/MDEV-27036): re-enable my\_json\_writer-t unit test
* [Revision #9feaa6be07](https://github.com/MariaDB/server/commit/9feaa6be07)\
  2021-11-17 09:41:13 +0200
  * Improve LibFMT detection
* Merge [Revision #467c7b2b24](https://github.com/MariaDB/server/commit/467c7b2b24) 2021-12-04 13:43:52 +0200 - Merge 10.7 into 10.8
* Merge [Revision #e384299ec2](https://github.com/MariaDB/server/commit/e384299ec2) 2021-12-02 17:59:45 +0200 - Merge 10.7 into 10.8
* [Revision #02de93d158](https://github.com/MariaDB/server/commit/02de93d158)\
  2021-12-02 04:59:49 +0400
  * [MDEV-27154](https://jira.mariadb.org/browse/MDEV-27154) allkeys.txt based tests for Unicode-4.0.0 and 5.2.0
* Merge [Revision #897d8c57b6](https://github.com/MariaDB/server/commit/897d8c57b6) 2021-11-29 11:58:15 +0200 - Merge 10.7 into 10.8
* [Revision #4f7574b10c](https://github.com/MariaDB/server/commit/4f7574b10c)\
  2021-11-29 09:24:58 +0200
  * [MDEV-27042](https://jira.mariadb.org/browse/MDEV-27042) fixup: GCC 11 -Og -Wmaybe-uninitialized
* [Revision #5be1d7f2a0](https://github.com/MariaDB/server/commit/5be1d7f2a0)\
  2021-11-15 05:57:25 +0200
  * [MDEV-27036](https://jira.mariadb.org/browse/MDEV-27036): unittest JSON object member name collision
* [Revision #3a96a61eae](https://github.com/MariaDB/server/commit/3a96a61eae)\
  2021-11-12 03:36:10 +0200
  * [MDEV-27036](https://jira.mariadb.org/browse/MDEV-27036): add assert to detect duplicated JSON keys
* [Revision #73df7a3009](https://github.com/MariaDB/server/commit/73df7a3009)\
  2021-11-14 09:48:20 +0200
  * [MDEV-27036](https://jira.mariadb.org/browse/MDEV-27036): resolve duplicated key issues of JSON tracing outputs:
* [Revision #a01c82ef2e](https://github.com/MariaDB/server/commit/a01c82ef2e)\
  2021-11-15 00:42:26 +0200
  * Json\_writer\_object add integers
* [Revision #cddbd25df5](https://github.com/MariaDB/server/commit/cddbd25df5)\
  2021-11-22 20:52:45 +0200
  * [MDEV-27036](https://jira.mariadb.org/browse/MDEV-27036): temporarily disable my\_json\_writer-t test
* Merge [Revision #124d74f5eb](https://github.com/MariaDB/server/commit/124d74f5eb) 2021-11-25 19:52:52 +0200 - Merge 10.7 into 10.8
* Merge [Revision #c41cbfaf1a](https://github.com/MariaDB/server/commit/c41cbfaf1a) 2021-11-25 08:47:54 +0200 - Merge 10.7 into 10.8
* [Revision #6a282df0be](https://github.com/MariaDB/server/commit/6a282df0be)\
  2021-11-05 19:03:38 +0100
  * Remove DYNAMIC\_ARRAY get\_index\_dynamic()
* [Revision #f9ad8072cd](https://github.com/MariaDB/server/commit/f9ad8072cd)\
  2021-11-14 07:09:08 +0400
  * [MDEV-27042](https://jira.mariadb.org/browse/MDEV-27042) UCA: Resetting contractions to ignorable does not work well
* [Revision #0a3d1d106a](https://github.com/MariaDB/server/commit/0a3d1d106a)\
  2021-11-13 18:49:24 +0400
  * Refactoring for [MDEV-27042](https://jira.mariadb.org/browse/MDEV-27042) and [MDEV-27009](https://jira.mariadb.org/browse/MDEV-27009)
* Merge [Revision #86891b8538](https://github.com/MariaDB/server/commit/86891b8538) 2021-11-19 17:59:01 +0200 - Merge 10.7 into 10.8
* [Revision #9db45d280a](https://github.com/MariaDB/server/commit/9db45d280a)\
  2021-11-19 18:06:48 +0300
  * [MDEV-27048](https://jira.mariadb.org/browse/MDEV-27048) UBSAN: runtime error: shift exponent 32 is too large for 32-bit type 'unsigned int'
* [Revision #0102732686](https://github.com/MariaDB/server/commit/0102732686)\
  2021-11-19 09:46:57 +0100
  * Revert "[MDEV-26713](https://jira.mariadb.org/browse/MDEV-26713) Windows - improve utf8 support for command line tools"
* [Revision #220dc1fd59](https://github.com/MariaDB/server/commit/220dc1fd59)\
  2021-11-18 17:19:52 +0100
  * xxx
* [Revision #2dcb823631](https://github.com/MariaDB/server/commit/2dcb823631)\
  2021-11-18 14:23:24 +0100
  * [MDEV-26713](https://jira.mariadb.org/browse/MDEV-26713) Windows- UTF8 encoding in the installer
* [Revision #68b16d80c9](https://github.com/MariaDB/server/commit/68b16d80c9)\
  2021-11-11 02:44:37 +0100
  * [MDEV-26713](https://jira.mariadb.org/browse/MDEV-26713) Windows- UTF8 encoding in the installer
* [Revision #012d3cecb8](https://github.com/MariaDB/server/commit/012d3cecb8)\
  2021-11-10 10:27:17 +0100
  * [MDEV-26713](https://jira.mariadb.org/browse/MDEV-26713) Windows - improve utf8 support for command line tools
* [Revision #e36a257323](https://github.com/MariaDB/server/commit/e36a257323)\
  2021-11-01 15:21:33 -0700
  * Modify PR template to encourage contribution of automated tests
* Merge [Revision #5566cbadb0](https://github.com/MariaDB/server/commit/5566cbadb0) 2021-11-12 00:36:05 +0100 - Merge branch '10.7' into 10.8
* Merge [Revision #bc57ff7cf7](https://github.com/MariaDB/server/commit/bc57ff7cf7) 2021-11-09 09:52:56 +0200 - Merge 10.7 into 10.8
* Merge [Revision #e54a4060b6](https://github.com/MariaDB/server/commit/e54a4060b6) 2021-11-08 12:42:30 +0200 - Merge 10.7 into 10.8
* Merge [Revision #2b5fdddb1b](https://github.com/MariaDB/server/commit/2b5fdddb1b) 2021-11-04 11:29:51 +0100 - Merge branch '10.7' into 10.8
* [Revision #ccb345e2a3](https://github.com/MariaDB/server/commit/ccb345e2a3)\
  2021-11-02 16:47:33 +0100
  * Spider fix for 10.8+
* [Revision #892153bd72](https://github.com/MariaDB/server/commit/892153bd72)\
  2021-11-02 16:04:32 +0100
  * 10.8 branch

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
