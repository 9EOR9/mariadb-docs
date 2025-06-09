# MariaDB 10.11.1 Changelog

The most recent release of [MariaDB 10.11](../../mariadb-community-server-release-notes/mariadb-10-11-series/what-is-mariadb-1011.md) is:[**MariaDB 10.11.11**](../../mariadb-community-server-release-notes/mariadb-10-11-series/mariadb-10-11-11-release-notes.md) Stable (GA) [Download Now](https://mariadb.com/downloads/)[_Alternate download from mariadb.org_](https://downloads.mariadb.org/mariadb/10.11.11/)

[Download 10.11.1](https://downloads.mariadb.org/mariadb/10.11.1/)[Release Notes](broken-reference)[Changelog](mariadb-10-11-1-changelog.md)[Overview of 10.11](../../mariadb-community-server-release-notes/mariadb-10-11-series/what-is-mariadb-1011.md)

[_Alternate download from mariadb.org_](https://downloads.mariadb.org/mariadb/10.11.1/)

**Release date:** 17 Nov 2022

For the highlights of this release, see the[release notes](broken-reference).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/server/tree/10.11) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Changes from [10.11.0](../../mariadb-community-server-release-notes/mariadb-10-11-series/mariadb-10-11-0-release-notes.md) are also included in this changelog
* Includes all fixes from [MariaDB 10.10.2](../changelogs-mariadb-10-10-series/mariadb-10-10-2-changelog.md)
* Merge [Revision #2437674291](https://github.com/MariaDB/server/commit/2437674291) 2022-11-14 19:10:21 +0100 - Merge branch '10.10' into 10.11
* [Revision #d186cb180e](https://github.com/MariaDB/server/commit/d186cb180e)\
  2022-11-08 14:35:16 +0100
  * [MDEV-26715](https://jira.mariadb.org/browse/MDEV-26715) Windows/installer - gssapi support
* [Revision #f97c8f7ece](https://github.com/MariaDB/server/commit/f97c8f7ece)\
  2022-08-26 00:38:00 +0200
  * [MDEV-26715](https://jira.mariadb.org/browse/MDEV-26715) Fix mysql\_install\_db\_win tests.
* [Revision #125e172a2b](https://github.com/MariaDB/server/commit/125e172a2b)\
  2022-05-20 16:32:35 +0200
  * [MDEV-26715](https://jira.mariadb.org/browse/MDEV-26715) Windows/installer - allow passwordless login for root
* Merge [Revision #e387b396d1](https://github.com/MariaDB/server/commit/e387b396d1) 2022-11-03 11:52:13 +0100 - Merge branch '10.10' into 10.11
* Merge [Revision #ad937cf33a](https://github.com/MariaDB/server/commit/ad937cf33a) 2022-11-02 10:42:34 +0100 - Merge branch '10.10' into 10.11
* [Revision #093ec49b6b](https://github.com/MariaDB/server/commit/093ec49b6b)\
  2022-10-21 16:50:55 +0200
  * Add magic database access to test and test\_% and removing the script from mysql-test-run.
* [Revision #0537ce4e9f](https://github.com/MariaDB/server/commit/0537ce4e9f)\
  2022-09-24 23:12:00 +0200
  * remove LEX\_USER->is\_public
* [Revision #5dc804c3bb](https://github.com/MariaDB/server/commit/5dc804c3bb)\
  2022-11-01 22:22:23 +0100
  * [MDEV-29752](https://jira.mariadb.org/browse/MDEV-29752) SHOW GRANTS for PUBLIC should work for all users
* [Revision #00c56e1c7c](https://github.com/MariaDB/server/commit/00c56e1c7c)\
  2022-09-24 22:38:12 +0200
  * compare public\_name by pointer
* [Revision #0b519a4075](https://github.com/MariaDB/server/commit/0b519a4075)\
  2022-09-24 11:26:08 +0200
  * cleanup
* [Revision #b4e7803a6f](https://github.com/MariaDB/server/commit/b4e7803a6f)\
  2022-11-01 21:52:23 +0100
  * [MDEV-5215](https://jira.mariadb.org/browse/MDEV-5215) post-review fixes
* [Revision #b0325bd6d6](https://github.com/MariaDB/server/commit/b0325bd6d6)\
  2021-12-13 16:15:21 +0100
  * [MDEV-5215](https://jira.mariadb.org/browse/MDEV-5215) Granted to PUBLIC
* [Revision #594bed9b42](https://github.com/MariaDB/server/commit/594bed9b42)\
  2022-06-13 14:37:59 +0200
  * [MDEV-5215](https://jira.mariadb.org/browse/MDEV-5215) prerequisite: remove test and test\_\* database hacks in the test suite
* [Revision #749c127822](https://github.com/MariaDB/server/commit/749c127822)\
  2022-06-13 09:44:40 +0200
  * [MDEV-5215](https://jira.mariadb.org/browse/MDEV-5215) prerequisite of prerequisite: if DB is not mentioned in connect ignore errors of switching to it
* [Revision #2bd41fc5bf](https://github.com/MariaDB/server/commit/2bd41fc5bf)\
  2022-10-27 22:18:51 +0200
  * Revert [MDEV-25292](https://jira.mariadb.org/browse/MDEV-25292) Atomic CREATE OR REPLACE TABLE
* [Revision #d15260990d](https://github.com/MariaDB/server/commit/d15260990d)\
  2022-10-27 19:41:19 +1100
  * [MDEV-22659](https://jira.mariadb.org/browse/MDEV-22659): Create one logrotate config - Deb/Rpm fix
* [Revision #ba16202e78](https://github.com/MariaDB/server/commit/ba16202e78)\
  2022-10-27 11:42:30 +0200
  * [MDEV-24377](https://jira.mariadb.org/browse/MDEV-24377): Accept comma separated addresses as --bind-address value (#2009)
* [Revision #fd0dcad676](https://github.com/MariaDB/server/commit/fd0dcad676)\
  2022-05-04 21:42:38 -0700
  * [MDEV-22659](https://jira.mariadb.org/browse/MDEV-22659): Create one single unified and optimal logrotate config
* [Revision #dc3be24268](https://github.com/MariaDB/server/commit/dc3be24268)\
  2022-10-21 21:40:48 +0200
  * [MDEV-29828](https://jira.mariadb.org/browse/MDEV-29828) Indicate that --dump-history only applies to timestamp-based versioning
* [Revision #c0fe0cce43](https://github.com/MariaDB/server/commit/c0fe0cce43)\
  2022-10-20 14:10:04 +0200
  * [MDEV-29830](https://jira.mariadb.org/browse/MDEV-29830) Assertion \`table->versioned()' in THD::vers\_insert\_history\_fast
* [Revision #7bdc024fb0](https://github.com/MariaDB/server/commit/7bdc024fb0)\
  2022-10-20 14:09:53 +0200
  * [MDEV-29830](https://jira.mariadb.org/browse/MDEV-29830) Assertion \`table->versioned()' in THD::vers\_insert\_history\_fast
* [Revision #a6f9694650](https://github.com/MariaDB/server/commit/a6f9694650)\
  2022-10-11 11:02:27 +0200
  * [MDEV-29736](https://jira.mariadb.org/browse/MDEV-29736) mysqldump sets system\_versioning\_insert\_history=1 twice and doesn't restore previous value
* [Revision #73b2a326d2](https://github.com/MariaDB/server/commit/73b2a326d2)\
  2022-10-10 19:45:10 +0200
  * [MDEV-29730](https://jira.mariadb.org/browse/MDEV-29730) mysqldump --dump-history creates broken dump if there are precision-versioned tables
* [Revision #d249761ae5](https://github.com/MariaDB/server/commit/d249761ae5)\
  2022-09-17 23:36:29 +0200
  * [MDEV-16029](https://jira.mariadb.org/browse/MDEV-16029) mysqldump: dump and restore historical data
* [Revision #a39b4848e4](https://github.com/MariaDB/server/commit/a39b4848e4)\
  2022-09-17 23:35:05 +0200
  * [MDEV-16733](https://jira.mariadb.org/browse/MDEV-16733) mysqldump --tab and --xml options are conflicting
* [Revision #a3dbd5de44](https://github.com/MariaDB/server/commit/a3dbd5de44)\
  2022-09-17 22:15:22 +0200
  * cleanup: mysqldump
* [Revision #ab50321508](https://github.com/MariaDB/server/commit/ab50321508)\
  2022-10-18 20:18:07 +0200
  * [MDEV-29813](https://jira.mariadb.org/browse/MDEV-29813) REPLACE/IGNORE does not work with historical records in InnoDB
* [Revision #3b6742a106](https://github.com/MariaDB/server/commit/3b6742a106)\
  2022-10-18 15:56:28 +0200
  * don't support REPLACE and INSERT ODKU with system\_versioning\_insert\_history
* [Revision #13901dafe1](https://github.com/MariaDB/server/commit/13901dafe1)\
  2022-10-18 13:45:10 +0200
  * cleanup
* [Revision #fe44d46a03](https://github.com/MariaDB/server/commit/fe44d46a03)\
  2022-10-17 19:09:47 +0200
  * [MDEV-29721](https://jira.mariadb.org/browse/MDEV-29721) Inconsistency upon inserting history with visible system versioning columns
* [Revision #b6a608700d](https://github.com/MariaDB/server/commit/b6a608700d)\
  2022-10-18 18:24:27 +0200
  * [MDEV-29805](https://jira.mariadb.org/browse/MDEV-29805) Attempt to insert into system versioning columns on old server may make slave data diverge
* [Revision #e536cb8845](https://github.com/MariaDB/server/commit/e536cb8845)\
  2022-10-10 20:27:26 +0200
  * [MDEV-29732](https://jira.mariadb.org/browse/MDEV-29732) mysqlbinlog produces syntactically incorrect output with system\_versioning\_insert\_history
* [Revision #4d1e3671d3](https://github.com/MariaDB/server/commit/4d1e3671d3)\
  2022-10-10 20:24:39 +0200
  * [MDEV-29741](https://jira.mariadb.org/browse/MDEV-29741) SHOW BINLOG EVENTS shows garbage with system\_versioning\_insert\_history=on
* [Revision #a858ff1731](https://github.com/MariaDB/server/commit/a858ff1731)\
  2022-10-10 17:35:23 +0200
  * different fix for [MDEV-26778](https://jira.mariadb.org/browse/MDEV-26778)
* [Revision #d94ed0bb2a](https://github.com/MariaDB/server/commit/d94ed0bb2a)\
  2022-10-10 10:30:51 +0200
  * [MDEV-29721](https://jira.mariadb.org/browse/MDEV-29721) Inconsistency upon inserting history with visible period columns
* [Revision #8d2ec37a40](https://github.com/MariaDB/server/commit/8d2ec37a40)\
  2022-09-06 19:28:42 +0200
  * [MDEV-16546](https://jira.mariadb.org/browse/MDEV-16546) post-review fixes
* [Revision #a2cda88631](https://github.com/MariaDB/server/commit/a2cda88631)\
  2022-08-28 22:44:56 +0300
  * [MDEV-16546](https://jira.mariadb.org/browse/MDEV-16546) System versioning setting to allow history modification
* [Revision #d9b0c9ad2b](https://github.com/MariaDB/server/commit/d9b0c9ad2b)\
  2022-09-16 11:29:46 +0200
  * cleanup: warnings, comments, whitespaces
* [Revision #adcbf015c9](https://github.com/MariaDB/server/commit/adcbf015c9)\
  2022-09-15 18:28:51 +0200
  * cleanup: read\_set/write\_set are based on metadata
* [Revision #bf62d8e7e7](https://github.com/MariaDB/server/commit/bf62d8e7e7)\
  2022-10-21 17:16:05 +0200
  * cleanup
* [Revision #1f7840088f](https://github.com/MariaDB/server/commit/1f7840088f)\
  2022-10-20 12:34:33 +0200
  * [MDEV-29833](https://jira.mariadb.org/browse/MDEV-29833) CREATE ... SELECT system\_versioned\_table causes invalid defaults
* [Revision #768a10d02a](https://github.com/MariaDB/server/commit/768a10d02a)\
  2022-10-26 14:54:53 +0200
  * [MDEV-22200](https://jira.mariadb.org/browse/MDEV-22200) maridb-dump add --header option
* [Revision #ad7631bdce](https://github.com/MariaDB/server/commit/ad7631bdce)\
  2022-07-18 17:48:01 +0200
  * [MDEV-28926](https://jira.mariadb.org/browse/MDEV-28926) Add time spent on query optimizer to JSON ANALYZE (#2193)
* [Revision #f45f60636f](https://github.com/MariaDB/server/commit/f45f60636f)\
  2022-10-20 18:42:48 +0100
  * [MDEV-22200](https://jira.mariadb.org/browse/MDEV-22200): maridb-dump add --header option
* [Revision #baf276e6d4](https://github.com/MariaDB/server/commit/baf276e6d4)\
  2022-10-24 20:46:43 +0530
  * [MDEV-19229](https://jira.mariadb.org/browse/MDEV-19229) Allow innodb\_undo\_tablespaces to be changed after database creation
* [Revision #307d935e2d](https://github.com/MariaDB/server/commit/307d935e2d)\
  2022-10-24 19:59:58 +0700
  * [MDEV-29858](https://jira.mariadb.org/browse/MDEV-29858) Missing DBUG\_RETURN or DBUG\_VOID\_RETURN in fill\_schema\_proc
* [Revision #af59b677ea](https://github.com/MariaDB/server/commit/af59b677ea)\
  2022-10-22 01:18:00 +0200
  * [MDEV-29104](https://jira.mariadb.org/browse/MDEV-29104) - fix test cases, for compilation without performance schema.
* [Revision #50c5743adc](https://github.com/MariaDB/server/commit/50c5743adc)\
  2022-09-12 18:20:12 +0200
  * [MDEV-15530](https://jira.mariadb.org/browse/MDEV-15530): Variable replicate\_rewrite\_db cannot be found in "show global variables"
* [Revision #1a057a923b](https://github.com/MariaDB/server/commit/1a057a923b)\
  2022-08-09 13:50:12 +0200
  * [MDEV-15530](https://jira.mariadb.org/browse/MDEV-15530): Variable replicate\_rewrite\_db cannot be found in "show global variables"
* [Revision #ccf0e27f28](https://github.com/MariaDB/server/commit/ccf0e27f28)\
  2022-10-17 19:34:25 +0200
  * version change
* Merge [Revision #4f13509eea](https://github.com/MariaDB/server/commit/4f13509eea) 2022-10-17 19:14:32 +0200 - Merge branch 'bb-10.10-release' into bb-10.11-release
* Merge [Revision #35b831d971](https://github.com/MariaDB/server/commit/35b831d971) 2022-10-17 19:12:21 +0200 - Merge branch 'bb-10.11-vp-[MDEV-27691](https://jira.mariadb.org/browse/MDEV-27691)' into 10.11
* [Revision #336dbe55f3](https://github.com/MariaDB/server/commit/336dbe55f3)\
  2022-09-28 16:07:21 +0700
  * [MDEV-27691](https://jira.mariadb.org/browse/MDEV-27691): make working view-protocol
* Merge [Revision #76aed6e844](https://github.com/MariaDB/server/commit/76aed6e844) 2022-09-28 13:57:55 +0700 - Merge branch 'bb-10.10-all-builders' into bb-10.11-all-builder
* [Revision #950e4f584d](https://github.com/MariaDB/server/commit/950e4f584d)\
  2022-10-16 19:18:40 +0200
  * [MDEV-6655](https://jira.mariadb.org/browse/MDEV-6655): mysqld\_multi default log location in wrong directory (#2285)
* [Revision #d9092e3de7](https://github.com/MariaDB/server/commit/d9092e3de7)\
  2022-09-19 21:36:09 +0700
  * [MDEV-29104](https://jira.mariadb.org/browse/MDEV-29104) Optimize queries to INFORMATION\_SCHEMA.PARAMETERS/ROUTINES
* [Revision #035feae610](https://github.com/MariaDB/server/commit/035feae610)\
  2022-09-16 15:04:54 +0400
  * [MDEV-29550](https://jira.mariadb.org/browse/MDEV-29550) Fix Valgrind/MSAN uninitialised value errors
* Merge [Revision #945a5439cc](https://github.com/MariaDB/server/commit/945a5439cc) 2022-10-13 11:03:21 +0300 - Merge 10.10 into 10.11
* [Revision #beb9a5459d](https://github.com/MariaDB/server/commit/beb9a5459d)\
  2022-09-12 14:28:00 +0700
  * [MDEV-20609](https://jira.mariadb.org/browse/MDEV-20609) Full table scan in INFORMATION\_SCHEMA.PARAMETERS/ROUTINES
* Merge [Revision #9206c1ea97](https://github.com/MariaDB/server/commit/9206c1ea97) 2022-10-04 13:55:38 +0200 - Merge branch '10.10' into 10.11
* [Revision #8759967d1c](https://github.com/MariaDB/server/commit/8759967d1c)\
  2022-09-26 19:21:24 +0200
  * [MDEV-29625](https://jira.mariadb.org/browse/MDEV-29625) Some clients/scripts refer to old slow log variables
* [Revision #05c11953ab](https://github.com/MariaDB/server/commit/05c11953ab)\
  2022-09-26 18:40:17 +0200
  * [MDEV-29595](https://jira.mariadb.org/browse/MDEV-29595) Adjust variable name for slow log file and help referring to the value
* [Revision #ef08810b8b](https://github.com/MariaDB/server/commit/ef08810b8b)\
  2022-09-12 11:34:29 +0200
  * [MDEV-7567](https://jira.mariadb.org/browse/MDEV-7567) Add aliases with prefix log\_slow for system variables relating to slow query log
* [Revision #af4918b41f](https://github.com/MariaDB/server/commit/af4918b41f)\
  2022-05-25 00:24:53 +0000
  * [MDEV-7567](https://jira.mariadb.org/browse/MDEV-7567) Add aliases with prefix log\_slow for system variables relating to slow query log.
* [Revision #315f2e8b81](https://github.com/MariaDB/server/commit/315f2e8b81)\
  2022-09-26 17:52:30 +0200
  * cleanup: remove _slow_\_basic tests
* [Revision #ba875e9396](https://github.com/MariaDB/server/commit/ba875e9396)\
  2022-09-30 23:58:08 +0300
  * [MDEV-29664](https://jira.mariadb.org/browse/MDEV-29664) Assertion \`!n\_mysql\_tables\_in\_use' failed in innobase\_close\_connection
* Merge [Revision #d026447101](https://github.com/MariaDB/server/commit/d026447101) 2022-09-30 10:39:47 +0200 - Merge branch '10.10' into 10.11
* [Revision #aa08a7442a](https://github.com/MariaDB/server/commit/aa08a7442a)\
  2022-09-27 13:44:30 +0300
  * [MDEV-29620](https://jira.mariadb.org/browse/MDEV-29620) Assertion \`next\_insert\_id == 0' failed in handler::ha\_external\_lock
* [Revision #c579d66ba6](https://github.com/MariaDB/server/commit/c579d66ba6)\
  2022-09-25 00:08:35 +0300
  * [MDEV-29628](https://jira.mariadb.org/browse/MDEV-29628) Memory leak after CREATE OR REPLACE with foreign key
* [Revision #cb583b2f1b](https://github.com/MariaDB/server/commit/cb583b2f1b)\
  2022-09-23 01:09:46 +0300
  * [MDEV-29609](https://jira.mariadb.org/browse/MDEV-29609) create\_not\_windows test fails with different result
* [Revision #dcd66c3814](https://github.com/MariaDB/server/commit/dcd66c3814)\
  2022-09-16 20:30:08 +0300
  * [MDEV-29544](https://jira.mariadb.org/browse/MDEV-29544) SIGSEGV in HA\_CREATE\_INFO::finalize\_locked\_tables
* [Revision #07581249e9](https://github.com/MariaDB/server/commit/07581249e9)\
  2022-09-26 20:26:29 +0200
  * [MDEV-29632](https://jira.mariadb.org/browse/MDEV-29632) SUPER users created before 10.11 should retain READ\_ONLY ADMIN privilege upon upgrade
* [Revision #e30f30d43b](https://github.com/MariaDB/server/commit/e30f30d43b)\
  2022-09-22 00:06:30 +0200
  * read\_only failures
* [Revision #47dccace13](https://github.com/MariaDB/server/commit/47dccace13)\
  2022-09-21 19:16:33 +0300
  * [MDEV-29596](https://jira.mariadb.org/browse/MDEV-29596) Separate SUPER and READ ONLY ADMIN privileges
* Merge [Revision #49cee4e21a](https://github.com/MariaDB/server/commit/49cee4e21a) 2022-09-21 11:25:57 +0300 - Merge 10.10 into 10.11
* Merge [Revision #6ebdd3013a](https://github.com/MariaDB/server/commit/6ebdd3013a) 2022-09-13 20:50:32 +0900 - Merge 10.10 into 10.11
* [Revision #8f9df08f02](https://github.com/MariaDB/server/commit/8f9df08f02)\
  2022-09-09 12:02:16 +0400
  * [MDEV-19246](https://jira.mariadb.org/browse/MDEV-19246) Change database and table used for Mariabackup's history
* [Revision #16c9718758](https://github.com/MariaDB/server/commit/16c9718758)\
  2022-08-12 19:03:12 +1000
  * [MDEV-25341](https://jira.mariadb.org/browse/MDEV-25341): innodb buffer pool soft decommit of memory
* Merge [Revision #3ec4241b00](https://github.com/MariaDB/server/commit/3ec4241b00) 2022-09-07 10:14:41 +0300 - Merge 10.10 into 10.11
* Merge [Revision #90608bd649](https://github.com/MariaDB/server/commit/90608bd649) 2022-09-06 11:32:54 +0300 - Merge 10.10 into 10.11
* [Revision #12c2364159](https://github.com/MariaDB/server/commit/12c2364159)\
  2022-08-31 22:05:02 +0900
  * [MDEV-28890](https://jira.mariadb.org/browse/MDEV-28890) Spider: remove #ifdef SPIDER\_XID\_USES\_xid\_cache\_iterate
* [Revision #cf6c517632](https://github.com/MariaDB/server/commit/cf6c517632)\
  2022-08-31 11:55:06 +0300
  * [MDEV-28933](https://jira.mariadb.org/browse/MDEV-28933) CREATE OR REPLACE fails to recreate same constraint name
* [Revision #f1e1c1335b](https://github.com/MariaDB/server/commit/f1e1c1335b)\
  2022-08-31 11:55:05 +0300
  * [MDEV-28933](https://jira.mariadb.org/browse/MDEV-28933) Moved RENAME\_CONSTRAINT\_IDS to include/sql\_funcs.h
* [Revision #a228ec80e3](https://github.com/MariaDB/server/commit/a228ec80e3)\
  2022-08-31 11:55:05 +0300
  * [MDEV-28956](https://jira.mariadb.org/browse/MDEV-28956) Locking is broken if CREATE OR REPLACE fails under LOCK TABLES
* [Revision #24fff8267d](https://github.com/MariaDB/server/commit/24fff8267d)\
  2022-08-31 11:55:05 +0300
  * [MDEV-25292](https://jira.mariadb.org/browse/MDEV-25292) gcol.gcol\_bugfixes --ps fix
* [Revision #2af15914cb](https://github.com/MariaDB/server/commit/2af15914cb)\
  2022-08-31 11:55:05 +0300
  * [MDEV-25292](https://jira.mariadb.org/browse/MDEV-25292) Disable atomic replace for slave-generated or-replace
* [Revision #34398a20b5](https://github.com/MariaDB/server/commit/34398a20b5)\
  2022-08-31 11:55:05 +0300
  * [MDEV-25292](https://jira.mariadb.org/browse/MDEV-25292) backup\_log improved
* [Revision #93c8252f02](https://github.com/MariaDB/server/commit/93c8252f02)\
  2022-08-31 11:55:04 +0300
  * [MDEV-25292](https://jira.mariadb.org/browse/MDEV-25292) Atomic CREATE OR REPLACE TABLE
* [Revision #86da0f4ee8](https://github.com/MariaDB/server/commit/86da0f4ee8)\
  2022-08-31 11:55:04 +0300
  * [MDEV-25292](https://jira.mariadb.org/browse/MDEV-25292) select\_create::create\_table removed
* [Revision #d145dda9c7](https://github.com/MariaDB/server/commit/d145dda9c7)\
  2022-08-31 11:55:04 +0300
  * [MDEV-25292](https://jira.mariadb.org/browse/MDEV-25292) Table\_name class for (db, table\_name, alias)
* [Revision #32d88faec5](https://github.com/MariaDB/server/commit/32d88faec5)\
  2022-08-31 11:55:03 +0300
  * [MDEV-25292](https://jira.mariadb.org/browse/MDEV-25292) Refactoring: removed TABLEOP\_HOOKS
* [Revision #409b8a86de](https://github.com/MariaDB/server/commit/409b8a86de)\
  2022-08-31 11:55:03 +0300
  * [MDEV-25292](https://jira.mariadb.org/browse/MDEV-25292) ha\_table\_exists() cleanup and improvement
* [Revision #65e0d0ea66](https://github.com/MariaDB/server/commit/65e0d0ea66)\
  2022-08-31 11:55:03 +0300
  * [MDEV-25292](https://jira.mariadb.org/browse/MDEV-25292) Removed thd argument in ddl\_log functions
* [Revision #595dad83ad](https://github.com/MariaDB/server/commit/595dad83ad)\
  2022-08-31 11:55:03 +0300
  * [MDEV-25292](https://jira.mariadb.org/browse/MDEV-25292) Cleanups
* [Revision #f02af1d229](https://github.com/MariaDB/server/commit/f02af1d229)\
  2022-08-31 11:55:02 +0300
  * [MDEV-25292](https://jira.mariadb.org/browse/MDEV-25292) Refactoring: moved select\_field\_count into Alter\_info.
* [Revision #5369df741b](https://github.com/MariaDB/server/commit/5369df741b)\
  2022-08-31 04:08:34 -0400
  * Remove FreeBSD CMake file (#2247)
* Merge [Revision #fe1f8f2c6b](https://github.com/MariaDB/server/commit/fe1f8f2c6b) 2022-08-30 13:36:30 +0300 - Merge 10.10 into 10.11
* Merge [Revision #62b418bd28](https://github.com/MariaDB/server/commit/62b418bd28) 2022-08-29 14:30:29 +0300 - Merge 10.10 to 10.11
* [Revision #80fbd0ee94](https://github.com/MariaDB/server/commit/80fbd0ee94)\
  2022-08-27 17:19:16 +0800
  * Remove redundant variable (#2237)
* [Revision #bc563f1a4b](https://github.com/MariaDB/server/commit/bc563f1a4b)\
  2022-08-16 15:39:15 +0200
  * Fix test result.
* Merge [Revision #6870f17b15](https://github.com/MariaDB/server/commit/6870f17b15) 2022-08-16 14:17:36 +0200 - Merge remote-tracking branch 'origin/bb-10.10-[MDEV-11026](https://jira.mariadb.org/browse/MDEV-11026)' into 10.11
* [Revision #c8e3bcf79b](https://github.com/MariaDB/server/commit/c8e3bcf79b)\
  2022-06-01 13:46:33 +0200
  * [MDEV-11026](https://jira.mariadb.org/browse/MDEV-11026) Make InnoDB number of IO write/read threads dynamic
* [Revision #49e660bb12](https://github.com/MariaDB/server/commit/49e660bb12)\
  2022-05-10 17:11:21 +0200
  * [MDEV-11026](https://jira.mariadb.org/browse/MDEV-11026) Make InnoDB number of IO write/read threads dynamic
* Merge [Revision #7253cdf892](https://github.com/MariaDB/server/commit/7253cdf892) 2022-08-15 15:22:19 +0200 - Merge branch '10.10' into 10.11
* Merge [Revision #04aab82830](https://github.com/MariaDB/server/commit/04aab82830) 2022-07-25 12:09:29 +0300 - Merge branch '10.10' into 10.11
* [Revision #dbaeeb6168](https://github.com/MariaDB/server/commit/dbaeeb6168)\
  2022-07-25 12:08:29 +0300
  * Create a 10.11 branch

{% @marketo/form formid="4316" formId="4316" %}
