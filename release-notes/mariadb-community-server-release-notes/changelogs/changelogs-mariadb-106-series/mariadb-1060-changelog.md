# MariaDB 10.6.0 Changelog

The most recent release of [MariaDB 10.6](../../mariadb-10-6-series/what-is-mariadb-106.md) is:[**MariaDB 10.6.21**](../../mariadb-10-6-series/mariadb-10-6-21-release-notes.md) Stable (GA) [Download Now](https://mariadb.com/downloads/)[_Alternate download from mariadb.org_](https://downloads.mariadb.org/mariadb/10.6.21/)

[Download 10.6.0](https://downloads.mariadb.org/mariadb/10.6.0/)[Release Notes](../../mariadb-10-6-series/mariadb-1060-release-notes.md)[Changelog](mariadb-1060-changelog.md)[Overview of 10.6](../../mariadb-10-6-series/what-is-mariadb-106.md)

**Release date:** 26 Apr 2021

**Do not use&#x20;**_**alpha**_**&#x20;releases in production!**

For the highlights of this release, see the[release notes](../../mariadb-10-6-series/mariadb-1060-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/server/tree/10.6) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Includes all fixes from [MariaDB 10.5.9](../changelogs-mariadb-105-series/mariadb-1059-changelog.md)
* [Revision #1a647b700f](https://github.com/MariaDB/server/commit/1a647b700f)\
  2021-04-23 10:07:08 +0300
  * [MDEV-25487](https://jira.mariadb.org/browse/MDEV-25487) Assertion failed in lock\_rec\_move
* [Revision #ee20e26dbb](https://github.com/MariaDB/server/commit/ee20e26dbb)\
  2021-04-23 11:58:39 +0530
  * [MDEV-20220](https://jira.mariadb.org/browse/MDEV-20220) post push fix
* Merge [Revision #bfc0110b9b](https://github.com/MariaDB/server/commit/bfc0110b9b) 2021-04-22 18:39:40 +0300 - Null-merge the revert of [MDEV-24589](https://jira.mariadb.org/browse/MDEV-24589)
* [Revision #1636db5443](https://github.com/MariaDB/server/commit/1636db5443)\
  2021-04-22 14:57:23 +0300
  * Revert "[MDEV-24589](https://jira.mariadb.org/browse/MDEV-24589) DROP TABLE is not crash-safe"
* Merge [Revision #18f35a8608](https://github.com/MariaDB/server/commit/18f35a8608) 2021-04-22 18:13:47 +0300 - Merge 10.5 into 10.6
* [Revision #21973d0d8e](https://github.com/MariaDB/server/commit/21973d0d8e)\
  2021-04-02 00:33:13 +0100
  * [MDEV-22953](https://jira.mariadb.org/browse/MDEV-22953) main.flush\_read\_lock failed in buildbot with XAER\_NOTA: Unknown XID
* [Revision #8121d03fd4](https://github.com/MariaDB/server/commit/8121d03fd4)\
  2021-04-22 15:43:30 +0300
  * [MDEV-25404](https://jira.mariadb.org/browse/MDEV-25404) fixup: Fix ssux\_lock\_low::u\_wr\_upgrade()
* Merge [Revision #54c460ace6](https://github.com/MariaDB/server/commit/54c460ace6) 2021-04-22 08:43:03 +0300 - Merge 10.5 into 10.6
* Merge [Revision #df33b719ca](https://github.com/MariaDB/server/commit/df33b719ca) 2021-04-22 08:25:40 +0300 - Merge 10.4 into 10.5
* Merge [Revision #ee455e6f2e](https://github.com/MariaDB/server/commit/ee455e6f2e) 2021-04-22 07:51:33 +0300 - Merge 10.3 into 10.4
* Merge [Revision #6f271302b6](https://github.com/MariaDB/server/commit/6f271302b6) 2021-04-22 07:32:51 +0300 - Merge 10.2 into 10.3
* [Revision #fb96ac0a49](https://github.com/MariaDB/server/commit/fb96ac0a49)\
  2021-04-21 21:12:33 +0530
  * [MDEV-25474](https://jira.mariadb.org/browse/MDEV-25474) Background thread returns uninitialized statistics to mysql interpreter
* [Revision #64eeb250eb](https://github.com/MariaDB/server/commit/64eeb250eb)\
  2021-04-20 22:33:22 +0300
  * [MDEV-25457](https://jira.mariadb.org/browse/MDEV-25457) Server crashes in row\_undo\_mod\_clust\_low upon rollback of read-only transaction
* [Revision #2a7dd64425](https://github.com/MariaDB/server/commit/2a7dd64425)\
  2021-01-05 18:08:25 +0200
  * [MDEV-24526](https://jira.mariadb.org/browse/MDEV-24526) binlog rotate via FLUSH LOGS may obsolate binlog file for recovery too eary
* [Revision #ef2749c90d](https://github.com/MariaDB/server/commit/ef2749c90d)\
  2021-04-21 09:21:24 +0300
  * Fixup: Event\_queue\_element\_for\_exec initializer list not supported on gcc-4.1
* [Revision #9e6e0eaee2](https://github.com/MariaDB/server/commit/9e6e0eaee2)\
  2021-04-20 12:10:24 +0900
  * fixed some korean error messages
* [Revision #df18fa4cae](https://github.com/MariaDB/server/commit/df18fa4cae)\
  2021-04-21 02:44:14 +0300
  * Smoke test collection should not be executable
* [Revision #3635280cf7](https://github.com/MariaDB/server/commit/3635280cf7)\
  2021-04-21 01:03:32 +0300
  * [MDEV-25288](https://jira.mariadb.org/browse/MDEV-25288) Create a list of tests for distributions
* [Revision #6244876488](https://github.com/MariaDB/server/commit/6244876488)\
  2021-04-20 23:09:01 +0300
  * [MDEV-24807](https://jira.mariadb.org/browse/MDEV-24807):A possibility for double free in dtor of Event\_queue\_element\_for\_exec in the case of OOM
* [Revision #0d267f7caa](https://github.com/MariaDB/server/commit/0d267f7caa)\
  2021-04-22 07:36:04 +0300
  * [MDEV-25362](https://jira.mariadb.org/browse/MDEV-25362) after-merge fix: Remove unnecessary code
* [Revision #cbbca7edf6](https://github.com/MariaDB/server/commit/cbbca7edf6)\
  2021-04-22 08:13:57 +0300
  * [MDEV-25483](https://jira.mariadb.org/browse/MDEV-25483): Shutdown crash during innodb.innodb\_buffer\_pool\_resize\_temporary
* [Revision #9abc6fd73f](https://github.com/MariaDB/server/commit/9abc6fd73f)\
  2021-04-21 12:44:23 +0300
  * Cleanup: constexpr PFS\_table\_context::m\_word\_size
* [Revision #b59d07624c](https://github.com/MariaDB/server/commit/b59d07624c)\
  2021-04-21 12:34:54 +0300
  * WITH\_UBSAN: shift is too large for 32-bit int
* [Revision #b728c3dbd9](https://github.com/MariaDB/server/commit/b728c3dbd9)\
  2021-04-22 08:42:55 +0300
  * fixup dd6ad3806856221f1af302e61ebd985905a00060: remove dead code
* [Revision #bc04ded235](https://github.com/MariaDB/server/commit/bc04ded235)\
  2021-04-21 15:17:39 +0300
  * Follow-up post JSON\_TABLE merge, table\_join\_options is not used
* [Revision #3019d1cb43](https://github.com/MariaDB/server/commit/3019d1cb43)\
  2021-04-21 14:51:15 +0300
  * Update columnstore to following cleanup of SELECT\_LEX
* [Revision #aeccdddedd](https://github.com/MariaDB/server/commit/aeccdddedd)\
  2021-04-18 22:58:34 +0300
  * [MDEV-25441](https://jira.mariadb.org/browse/MDEV-25441) WITH TIES is not respected with SQL\_BUFFER\_RESULT and constant in ORDER BY
* [Revision #44a6af65f5](https://github.com/MariaDB/server/commit/44a6af65f5)\
  2021-04-16 20:02:10 +0300
  * [MDEV-25430](https://jira.mariadb.org/browse/MDEV-25430): ROW | ROWS should be a required keyword after OFFSET start
* [Revision #299b935320](https://github.com/MariaDB/server/commit/299b935320)\
  2021-03-28 21:41:50 +0300
  * [MDEV-23908](https://jira.mariadb.org/browse/MDEV-23908): Implement SELECT ... OFFSET ... FETCH ...
* [Revision #2d595319bf](https://github.com/MariaDB/server/commit/2d595319bf)\
  2021-03-28 21:09:51 +0300
  * cleanup: Select\_limit\_counters rename set\_unlimited to clear
* [Revision #3fcc4f6fc2](https://github.com/MariaDB/server/commit/3fcc4f6fc2)\
  2021-03-07 13:07:10 +0200
  * cleanup: make\_aggr\_tables\_info pass parameters from existing local variables
* [Revision #7e7ca09ce1](https://github.com/MariaDB/server/commit/7e7ca09ce1)\
  2021-01-19 10:12:37 +0200
  * cleanup: test\_if\_subpart documented to highlight side effect
* [Revision #d028fb9ffa](https://github.com/MariaDB/server/commit/d028fb9ffa)\
  2020-12-28 18:27:09 +0200
  * cleanup: reduce indentation of end\_send
* [Revision #d624464b50](https://github.com/MariaDB/server/commit/d624464b50)\
  2021-03-07 13:00:21 +0200
  * cleanup: remove table\_options and corresponding accessor function
* [Revision #5e72099b83](https://github.com/MariaDB/server/commit/5e72099b83)\
  2020-12-28 17:13:46 +0200
  * cleanup: Delete unused function Select\_limit\_counters::is\_unrestricted
* [Revision #13cf8f5e9a](https://github.com/MariaDB/server/commit/13cf8f5e9a)\
  2020-12-19 13:59:37 +0200
  * cleanup: Refactor select\_limit in select lex
* [Revision #dd6ad38068](https://github.com/MariaDB/server/commit/dd6ad38068)\
  2021-04-21 12:32:58 +0300
  * Code cleanup: merge walk\_items\_for\_table\_list with walk\_table\_functions\_for\_list
* Merge [Revision #4930f9c94b](https://github.com/MariaDB/server/commit/4930f9c94b) 2021-04-21 11:45:00 +0300 - Merge 10.5 into 10.6
* Merge [Revision #d104fe6f73](https://github.com/MariaDB/server/commit/d104fe6f73) 2021-04-21 10:27:13 +0300 - Merge 10.4 into 10.5
* [Revision #ceed768eea](https://github.com/MariaDB/server/commit/ceed768eea)\
  2021-04-21 10:06:31 +0300
  * [MDEV-25362](https://jira.mariadb.org/browse/MDEV-25362) after-merge fix: GCC -Og -Wmaybe-uninitialized
* Merge [Revision #80ed136e6d](https://github.com/MariaDB/server/commit/80ed136e6d) 2021-04-21 09:01:01 +0300 - Merge 10.4 into 10.5
* Merge [Revision #a0588d54a2](https://github.com/MariaDB/server/commit/a0588d54a2) 2021-04-21 07:58:42 +0300 - Merge 10.3 into 10.4
* Merge [Revision #75c01f39b1](https://github.com/MariaDB/server/commit/75c01f39b1) 2021-04-21 07:25:48 +0300 - Merge 10.2 into 10.3
* Merge [Revision #922e676b43](https://github.com/MariaDB/server/commit/922e676b43) 2021-04-20 17:33:36 +0300 - [MDEV-25466](https://jira.mariadb.org/browse/MDEV-25466) Merge new release of InnoDB 5.7.34 to 10.2
* [Revision #72432ec7b3](https://github.com/MariaDB/server/commit/72432ec7b3)\
  2021-02-24 07:49:37 +0530
  * Bug #32032897 DEADLOCKING WAIT GRAPH ON BUSY SERVER
* [Revision #635b5ce355](https://github.com/MariaDB/server/commit/635b5ce355)\
  2021-04-16 09:53:16 -0700
  * [MDEV-25362](https://jira.mariadb.org/browse/MDEV-25362) Incorrect name resolution for subqueries in ON expressions
* [Revision #73bf62469e](https://github.com/MariaDB/server/commit/73bf62469e)\
  2020-11-20 16:55:03 +1100
  * [MDEV-15064](https://jira.mariadb.org/browse/MDEV-15064): IO\_CACHE mysys read\_pos, not libmaria rc\_pos
* [Revision #ab5dc62545](https://github.com/MariaDB/server/commit/ab5dc62545)\
  2021-04-13 20:32:16 +0300
  * [MDEV-25407](https://jira.mariadb.org/browse/MDEV-25407): EXISTS subquery with correlation in ON expression crashes
* [Revision #a3871cd283](https://github.com/MariaDB/server/commit/a3871cd283)\
  2021-03-31 16:36:36 +0300
  * [MDEV-22255](https://jira.mariadb.org/browse/MDEV-22255) SIGABRT: Assertion `id' failed in trx_write_trx_id on INSERT | Assertion` id > 0' failed in trx\_write\_trx\_id | Assertion `val > 0' failed in row_upd_index_entry_sys_field | Assertion` thr\_get\_trx(thr)->id || index->table->no\_rollback()' failed.
* [Revision #7fa12b1e34](https://github.com/MariaDB/server/commit/7fa12b1e34)\
  2021-04-12 21:18:14 +0530
  * [MDEV-23026](https://jira.mariadb.org/browse/MDEV-23026) purge fails with assert !rw\_lock\_own\_flagged(lock, RW\_LOCK\_FLAG\_X | RW\_LOCK\_FLAG\_S)
* [Revision #343fe4e232](https://github.com/MariaDB/server/commit/343fe4e232)\
  2021-04-14 20:01:51 +0200
  * update C/C
* [Revision #499e617182](https://github.com/MariaDB/server/commit/499e617182)\
  2021-04-13 19:52:40 +0200
  * [MDEV-25403](https://jira.mariadb.org/browse/MDEV-25403) ALTER TABLE wrongly checks for field's default value if AFTER is used
* [Revision #3ebd6cd3ad](https://github.com/MariaDB/server/commit/3ebd6cd3ad)\
  2021-03-30 18:48:56 +0100
  * signal handler, display coredump file pattern similarly to [MDEV-25294](https://jira.mariadb.org/browse/MDEV-25294) but for FreeBSD, thankfully the sysctl OID is the same.
* [Revision #022d3fa652](https://github.com/MariaDB/server/commit/022d3fa652)\
  2021-04-14 14:46:47 +0200
  * Update mysqlbinlog man page with --table option
* [Revision #7b791b82b8](https://github.com/MariaDB/server/commit/7b791b82b8)\
  2021-04-13 18:32:05 +0200
  * [MDEV-25363](https://jira.mariadb.org/browse/MDEV-25363) binlog\_stm\_datetime\_ranges\_mdev15289 failed in bb
* [Revision #2557064873](https://github.com/MariaDB/server/commit/2557064873)\
  2021-04-14 02:17:48 +0200
  * [MDEV-25354](https://jira.mariadb.org/browse/MDEV-25354): Fix my\_print\_defaults wording
* [Revision #562bbf5212](https://github.com/MariaDB/server/commit/562bbf5212)\
  2021-04-13 23:56:49 +0300
  * [MDEV-25327](https://jira.mariadb.org/browse/MDEV-25327) Unexpected ER\_DUP\_ENTRY upon dropping PK column from system-versioned table
* [Revision #cc3105e100](https://github.com/MariaDB/server/commit/cc3105e100)\
  2020-12-20 20:52:51 +0200
  * Fix riscv64 build failure by linking correctly with pthread
* [Revision #031f11717d](https://github.com/MariaDB/server/commit/031f11717d)\
  2021-04-18 15:29:13 +0300
  * Fix all warnings given by UBSAN
* [Revision #eb4123eefc](https://github.com/MariaDB/server/commit/eb4123eefc)\
  2021-04-14 22:40:46 +0200
  * More fixes to variable wsrep\_on
* [Revision #57caff245c](https://github.com/MariaDB/server/commit/57caff245c)\
  2021-04-11 09:37:36 +0300
  * [MDEV-25423](https://jira.mariadb.org/browse/MDEV-25423) : Donor node fails to shutdown after mysqldump SST
* [Revision #c3b016efde](https://github.com/MariaDB/server/commit/c3b016efde)\
  2021-02-05 11:06:25 +0100
  * [MDEV-22668](https://jira.mariadb.org/browse/MDEV-22668): "Flush SSL" command doesn't reload wsrep cert
* [Revision #675c22c065](https://github.com/MariaDB/server/commit/675c22c065)\
  2020-06-05 16:18:02 +0300
  * [MDEV-22757](https://jira.mariadb.org/browse/MDEV-22757) Assertion !binlog || exist\_hton\_without\_prepare' failed in MYSQL\_BIN\_LOG::unlog\_xa\_prepare
* [Revision #0620ccf3ea](https://github.com/MariaDB/server/commit/0620ccf3ea)\
  2021-04-19 14:31:57 +0300
  * Fixed failing test spider/bugfix.mdev\_22246
* [Revision #502b769561](https://github.com/MariaDB/server/commit/502b769561)\
  2021-04-20 14:44:24 +0400
  * [MDEV-17399](https://jira.mariadb.org/browse/MDEV-17399) JSON\_TABLE.
* [Revision #41e368f22d](https://github.com/MariaDB/server/commit/41e368f22d)\
  2021-04-15 11:52:22 +0400
  * [MDEV-25149](https://jira.mariadb.org/browse/MDEV-25149) JSON\_TABLE: Inconsistency in implicit data type conversion.
* [Revision #0a09525625](https://github.com/MariaDB/server/commit/0a09525625)\
  2021-04-17 18:23:15 +0300
  * [MDEV-25202](https://jira.mariadb.org/browse/MDEV-25202): JSON\_TABLE: Early table reference leads to unexpected result set
* [Revision #e4665f417b](https://github.com/MariaDB/server/commit/e4665f417b)\
  2021-04-17 10:55:35 +0300
  * [MDEV-25202](https://jira.mariadb.org/browse/MDEV-25202): JSON\_TABLE: Early table reference leads to unexpected result set
* [Revision #a4353c25ca](https://github.com/MariaDB/server/commit/a4353c25ca)\
  2021-04-17 09:25:23 +0400
  * [MDEV-25420](https://jira.mariadb.org/browse/MDEV-25420) JSON\_TABLE: ASAN heap-buffer-overflow in Protocol::net\_store\_data or consequent failur es.
* [Revision #b0817ff8de](https://github.com/MariaDB/server/commit/b0817ff8de)\
  2021-04-16 19:50:08 +0300
  * [MDEV-25202](https://jira.mariadb.org/browse/MDEV-25202): JSON\_TABLE: Early table reference leads to unexpected result set
* [Revision #0984b8ed08](https://github.com/MariaDB/server/commit/0984b8ed08)\
  2021-04-16 15:12:46 +0400
  * [MDEV-25420](https://jira.mariadb.org/browse/MDEV-25420) JSON\_TABLE: ASAN heap-buffer-overflow in Protocol::net\_store\_data or consequent failures.
* [Revision #91cd3c8f5b](https://github.com/MariaDB/server/commit/91cd3c8f5b)\
  2021-04-16 13:24:48 +0400
  * [MDEV-25353](https://jira.mariadb.org/browse/MDEV-25353) JSON\_TABLE: Illegal mix of collations upon executing PS once, or SP/function twice.
* [Revision #59f3399e29](https://github.com/MariaDB/server/commit/59f3399e29)\
  2021-04-16 11:55:52 +0400
  * [MDEV-25420](https://jira.mariadb.org/browse/MDEV-25420) JSON\_TABLE: ASAN heap-buffer-overflow in Protocol::net\_store\_data or consequent failures.
* [Revision #277aa532f3](https://github.com/MariaDB/server/commit/277aa532f3)\
  2021-04-15 14:23:52 +0400
  * [MDEV-25408](https://jira.mariadb.org/browse/MDEV-25408) JSON\_TABLE: AddressSanitizer CHECK failed in Binary\_string::realloc\_raw
* [Revision #991bfebe8f](https://github.com/MariaDB/server/commit/991bfebe8f)\
  2021-04-13 14:18:04 +0400
  * [MDEV-25379](https://jira.mariadb.org/browse/MDEV-25379) JSON\_TABLE: ERROR ON clauses are ignored if a column is not on select list.
* [Revision #1eda21be1f](https://github.com/MariaDB/server/commit/1eda21be1f)\
  2021-04-13 12:37:47 +0300
  * Code cleanup: thd->lex->current\_select->context == s\_lex here, so use s\_lex
* [Revision #a96408092c](https://github.com/MariaDB/server/commit/a96408092c)\
  2021-04-13 12:34:14 +0300
  * [MDEV-25397](https://jira.mariadb.org/browse/MDEV-25397): JSON\_TABLE: Unexpected ER\_MIX\_OF\_GROUP\_FUNC\_AND\_FIELDS
* [Revision #f82947e48d](https://github.com/MariaDB/server/commit/f82947e48d)\
  2021-04-12 13:04:01 +0400
  * [MDEV-17399](https://jira.mariadb.org/browse/MDEV-17399) JSON\_TABLE.
* [Revision #a5b454f98a](https://github.com/MariaDB/server/commit/a5b454f98a)\
  2021-04-13 03:28:56 +0400
  * [MDEV-25259](https://jira.mariadb.org/browse/MDEV-25259) JSON\_TABLE: Illegal mix of collations upon executing query with combination of charsets via view.
* [Revision #a2ce788f02](https://github.com/MariaDB/server/commit/a2ce788f02)\
  2021-04-12 23:17:32 +0400
  * [MDEV-25259](https://jira.mariadb.org/browse/MDEV-25259) JSON\_TABLE: Illegal mix of collations upon executing query with combination of charsets via view.
* [Revision #67b31a6e4c](https://github.com/MariaDB/server/commit/67b31a6e4c)\
  2021-04-12 23:07:00 +0400
  * [MDEV-17399](https://jira.mariadb.org/browse/MDEV-17399) JSON\_TABLE.
* [Revision #1db1f85996](https://github.com/MariaDB/server/commit/1db1f85996)\
  2021-04-12 18:11:32 +0400
  * [MDEV-17399](https://jira.mariadb.org/browse/MDEV-17399) JSON\_TABLE.
* [Revision #6bac48d0cf](https://github.com/MariaDB/server/commit/6bac48d0cf)\
  2021-04-12 16:43:45 +0300
  * [MDEV-25381](https://jira.mariadb.org/browse/MDEV-25381): JSON\_TABLE: ER\_WRONG\_OUTER\_JOIN upon query with LEFT and RIGHT joins and view
* [Revision #4a10dd0253](https://github.com/MariaDB/server/commit/4a10dd0253)\
  2021-04-12 14:11:37 +0300
  * [MDEV-25380](https://jira.mariadb.org/browse/MDEV-25380): JSON\_TABLE: Assertion \`join->best\_read < double(1.797...) fails
* [Revision #eb2550ee78](https://github.com/MariaDB/server/commit/eb2550ee78)\
  2021-04-12 13:16:20 +0300
  * [MDEV-25346](https://jira.mariadb.org/browse/MDEV-25346): JSON\_TABLE: Server crashes in Item\_field::fix\_outer\_field ...
* [Revision #1b81e23737](https://github.com/MariaDB/server/commit/1b81e23737)\
  2021-04-12 13:24:02 +0400
  * [MDEV-17339](https://jira.mariadb.org/browse/MDEV-17339) JSON\_TABLE.
* [Revision #90629aa83c](https://github.com/MariaDB/server/commit/90629aa83c)\
  2021-04-09 00:37:57 +0300
  * [MDEV-25346](https://jira.mariadb.org/browse/MDEV-25346): JSON\_TABLE: Server crashes in Item\_field::fix\_outer\_field ...
* [Revision #bd1d6ee4b1](https://github.com/MariaDB/server/commit/bd1d6ee4b1)\
  2021-04-08 20:46:49 +0300
  * [MDEV-25352](https://jira.mariadb.org/browse/MDEV-25352): JSON\_TABLE: Inconsistent name resolution and ER\_VIEW\_INVALID
* [Revision #74895090b3](https://github.com/MariaDB/server/commit/74895090b3)\
  2021-04-08 20:21:34 +0300
  * [MDEV-25202](https://jira.mariadb.org/browse/MDEV-25202): JSON\_TABLE: Early table reference leads to unexpected result set
* [Revision #5a8abbb77d](https://github.com/MariaDB/server/commit/5a8abbb77d)\
  2021-04-06 12:18:02 +0400
  * [MDEV-17399](https://jira.mariadb.org/browse/MDEV-17399) JSON\_TABLE.
* [Revision #1be9c51beb](https://github.com/MariaDB/server/commit/1be9c51beb)\
  2021-04-06 11:27:59 +0300
  * [MDEV-25202](https://jira.mariadb.org/browse/MDEV-25202): JSON\_TABLE: Early table reference leads to unexpected result set
* [Revision #0fedaf2183](https://github.com/MariaDB/server/commit/0fedaf2183)\
  2021-04-05 16:10:46 +0300
  * Update result for perfschema.start\_server\_low\_digest\_sql\_length
* [Revision #84cf9c2e11](https://github.com/MariaDB/server/commit/84cf9c2e11)\
  2021-04-05 14:15:05 +0300
  * [MDEV-25202](https://jira.mariadb.org/browse/MDEV-25202): JSON\_TABLE: Early table reference leads to unexpected result set
* [Revision #13390a70e2](https://github.com/MariaDB/server/commit/13390a70e2)\
  2021-03-28 18:02:58 +0400
  * [MDEV-25255](https://jira.mariadb.org/browse/MDEV-25255) JSON\_TABLE: CREATE TABLE ignores NULL ON ERROR (implicit or explicit) and fails.
* [Revision #d2e2219e46](https://github.com/MariaDB/server/commit/d2e2219e46)\
  2021-03-26 13:53:40 +0400
  * [MDEV-25146](https://jira.mariadb.org/browse/MDEV-25146) JSON\_TABLE: Non-descriptive + wrong error messages upon trying to store array or object.
* [Revision #48dffa3c30](https://github.com/MariaDB/server/commit/48dffa3c30)\
  2021-03-26 12:18:02 +0400
  * [MDEV-25155](https://jira.mariadb.org/browse/MDEV-25155) JSON\_TABLE: Status variable Feature\_json is not incremented.
* [Revision #e2d5eb67a1](https://github.com/MariaDB/server/commit/e2d5eb67a1)\
  2021-03-26 11:03:40 +0400
  * [MDEV-25263](https://jira.mariadb.org/browse/MDEV-25263) JSON\_TABLE: json\_table test fails with valgrind.
* [Revision #11c8ce4348](https://github.com/MariaDB/server/commit/11c8ce4348)\
  2021-03-26 10:15:32 +0400
  * [MDEV-25138](https://jira.mariadb.org/browse/MDEV-25138) JSON\_TABLE: A space between JSON\_TABLE and opening bracket causes syntax error.
* [Revision #0cea1ea7d3](https://github.com/MariaDB/server/commit/0cea1ea7d3)\
  2021-03-25 11:18:28 +0400
  * [MDEV-25183](https://jira.mariadb.org/browse/MDEV-25183) JSON\_TABLE: CREATE VIEW involving NESTED PATH ends up with invalid frm.
* [Revision #22e0a317be](https://github.com/MariaDB/server/commit/22e0a317be)\
  2021-03-25 10:34:13 +0400
  * The ha\_partition::table\_type() method was just never called before.
* [Revision #3edc4a0998](https://github.com/MariaDB/server/commit/3edc4a0998)\
  2021-03-24 23:37:05 +0400
  * [MDEV-25229](https://jira.mariadb.org/browse/MDEV-25229) SON\_TABLE: Server crashes in hton\_name upon MATCH .. AGAINST.
* [Revision #6a5f86bf59](https://github.com/MariaDB/server/commit/6a5f86bf59)\
  2021-03-24 16:36:50 +0400
  * [MDEV-25230](https://jira.mariadb.org/browse/MDEV-25230) JSON\_TABLE: CREATE VIEW with 2nd level NESTED PATH ends up with invalid frm, Assertion \`m\_status == DA\_ERROR || m\_status == DA\_OK || m\_status == DA\_OK\_BULK' failed.
* [Revision #707d8653c4](https://github.com/MariaDB/server/commit/707d8653c4)\
  2021-03-24 15:05:24 +0400
  * [MDEV-25228](https://jira.mariadb.org/browse/MDEV-25228) JSON\_TABLE: Server crashes in Query\_cache::unlink\_table.
* [Revision #7075955f4e](https://github.com/MariaDB/server/commit/7075955f4e)\
  2021-03-23 13:58:40 +0400
  * [MDEV-25189](https://jira.mariadb.org/browse/MDEV-25189) SON\_TABLE: Assertion \`l\_offset >= 0 && table->s->rec\_buff\_length - l\_offset > 0' failed upon CREATE .. SELECT.
* [Revision #46d592a047](https://github.com/MariaDB/server/commit/46d592a047)\
  2021-03-23 13:23:37 +0400
  * [MDEV-25188](https://jira.mariadb.org/browse/MDEV-25188) JSON\_TABLE: ASAN use-after-poison in Field\_long::reset / Table\_function\_json\_table::setup or malloc(): invalid size.
* [Revision #0eda81e4d9](https://github.com/MariaDB/server/commit/0eda81e4d9)\
  2021-03-22 16:07:25 +0400
  * [MDEV-25186](https://jira.mariadb.org/browse/MDEV-25186) JSON\_TABLE: ASAN global-buffer-overflow in my\_strnncoll\_binary upon inserting query with join into query cache.
* [Revision #90c4dff5ab](https://github.com/MariaDB/server/commit/90c4dff5ab)\
  2021-03-22 15:34:27 +0400
  * [MDEV-25178](https://jira.mariadb.org/browse/MDEV-25178) JSON\_TABLE: ASAN use-after-poison in my\_fill\_8bit Json\_table\_column::On\_response::respond.
* [Revision #6f56458a76](https://github.com/MariaDB/server/commit/6f56458a76)\
  2021-03-19 11:05:14 +0400
  * [MDEV-25183](https://jira.mariadb.org/browse/MDEV-25183) JSON\_TABLE: CREATE VIEW involving NESTED PATH ends up with invalid frm.
* [Revision #51ac57fbbe](https://github.com/MariaDB/server/commit/51ac57fbbe)\
  2021-03-18 15:36:28 +0400
  * [MDEV-25151](https://jira.mariadb.org/browse/MDEV-25151) JSON\_TABLE: Unexpectedly padded values in a PATH column.
* [Revision #047eb2258d](https://github.com/MariaDB/server/commit/047eb2258d)\
  2021-03-17 18:28:31 +0400
  * [MDEV-25141](https://jira.mariadb.org/browse/MDEV-25141) JSON\_TABLE: SELECT into outfile bypasses file privilege check.
* [Revision #abdc39b0a7](https://github.com/MariaDB/server/commit/abdc39b0a7)\
  2021-03-17 10:51:44 +0400
  * [MDEV-25143](https://jira.mariadb.org/browse/MDEV-25143) JSON\_TABLE: Server crashes in handler::print\_error / hton\_name upon ERROR ON EMPTY.
* [Revision #99fc076fea](https://github.com/MariaDB/server/commit/99fc076fea)\
  2021-03-16 17:06:28 +0300
  * [MDEV-25145](https://jira.mariadb.org/browse/MDEV-25145): JSON\_TABLE: Assertion fixed == 1 failed .. on 2nd execution
* [Revision #98556ef84a](https://github.com/MariaDB/server/commit/98556ef84a)\
  2021-03-16 16:15:06 +0300
  * [MDEV-25142](https://jira.mariadb.org/browse/MDEV-25142): JSON\_TABLE: CREATE VIEW involving EXISTS PATH ends up with invalid frm
* [Revision #93daad3a1e](https://github.com/MariaDB/server/commit/93daad3a1e)\
  2021-03-15 17:03:52 +0300
  * [MDEV-17399](https://jira.mariadb.org/browse/MDEV-17399): JSON\_TABLE: cleanup table dependency code
* [Revision #2f650fb955](https://github.com/MariaDB/server/commit/2f650fb955)\
  2021-03-15 14:22:21 +0300
  * [MDEV-17399](https://jira.mariadb.org/browse/MDEV-17399): JSON\_TABLE: Fix the problem with cross-nested-join dependency
* [Revision #e9fd327ee3](https://github.com/MariaDB/server/commit/e9fd327ee3)\
  2021-03-17 09:03:45 +0400
  * [MDEV-17399](https://jira.mariadb.org/browse/MDEV-17399) Add support for JSON\_TABLE.
* [Revision #a3099a3b4a](https://github.com/MariaDB/server/commit/a3099a3b4a)\
  2020-11-18 16:04:57 +0100
  * [MDEV-24312](https://jira.mariadb.org/browse/MDEV-24312) master\_host has 60 character limit, increase to 255 bytes
* [Revision #8751aa7397](https://github.com/MariaDB/server/commit/8751aa7397)\
  2021-04-19 18:15:49 +0300
  * [MDEV-25404](https://jira.mariadb.org/browse/MDEV-25404): ssux\_lock\_low: Introduce a separate writer mutex
* [Revision #040c16ab8b](https://github.com/MariaDB/server/commit/040c16ab8b)\
  2021-04-19 17:47:21 +0300
  * [MDEV-25404](https://jira.mariadb.org/browse/MDEV-25404): Optimize srw\_mutex on Linux, OpenBSD, Windows
* [Revision #af418bb9ef](https://github.com/MariaDB/server/commit/af418bb9ef)\
  2021-04-18 09:31:21 +1000
  * [MDEV-25433](https://jira.mariadb.org/browse/MDEV-25433): SKIP LOCKED should imply NOWAIT
* [Revision #bfedf1eb4b](https://github.com/MariaDB/server/commit/bfedf1eb4b)\
  2021-04-11 09:37:36 +0300
  * Improve Galera SST tests
* [Revision #fd9ca569f2](https://github.com/MariaDB/server/commit/fd9ca569f2)\
  2021-03-06 19:32:39 +0200
  * [MDEV-25359](https://jira.mariadb.org/browse/MDEV-25359) : Improve mariadb-backup SST script compliance with native MariaDB SSL practices and configuration.
* [Revision #2656e87682](https://github.com/MariaDB/server/commit/2656e87682)\
  2021-04-15 00:19:13 +0300
  * Cleanup: fake\_select\_lex->select\_number=FAKE\_SELECT\_LEX\_ID, not \[U]INT\_MAX
* [Revision #3f138fa3a5](https://github.com/MariaDB/server/commit/3f138fa3a5)\
  2021-04-16 18:23:46 +1000
  * Deb: Use build flag to enforce default charset as utf8mb4
* Merge [Revision #f862f39f46](https://github.com/MariaDB/server/commit/f862f39f46) 2021-04-16 18:23:18 +1000 - Merge branch '10.5' into 10.6
* [Revision #fce3e4ee8f](https://github.com/MariaDB/server/commit/fce3e4ee8f)\
  2021-04-16 18:21:52 +1000
  * Revert "Deb: Use build flag to enforce default charset as utf8mb4"
* [Revision #62f5a4f065](https://github.com/MariaDB/server/commit/62f5a4f065)\
  2021-03-31 08:07:44 -0700
  * Deb: Update Conflicts/Replaces/Replaces for all upgrade scenarios
* [Revision #fc65417e7b](https://github.com/MariaDB/server/commit/fc65417e7b)\
  2021-04-04 09:05:29 -0700
  * Deb: Move my\_print\_defaults to MariaDB client core package
* [Revision #f55d53e26d](https://github.com/MariaDB/server/commit/f55d53e26d)\
  2020-06-04 22:06:06 +0300
  * Deb: Move client programs to client package from MariaDB server package
* [Revision #410832313e](https://github.com/MariaDB/server/commit/410832313e)\
  2021-04-16 09:11:48 +0530
  * [MDEV-16437](https://jira.mariadb.org/browse/MDEV-16437): merge 5.7 P\_S replication instrumentation and tables
* [Revision #767648cc2b](https://github.com/MariaDB/server/commit/767648cc2b)\
  2021-04-16 09:05:39 +0530
  * [MDEV-16437](https://jira.mariadb.org/browse/MDEV-16437): merge 5.7 P\_S replication instrumentation and tables
* [Revision #70642871bc](https://github.com/MariaDB/server/commit/70642871bc)\
  2021-04-16 09:02:00 +0530
  * [MDEV-16437](https://jira.mariadb.org/browse/MDEV-16437): merge 5.7 P\_S replication instrumentation and tables
* [Revision #2674365c8e](https://github.com/MariaDB/server/commit/2674365c8e)\
  2021-04-16 08:48:15 +0530
  * [MDEV-16437](https://jira.mariadb.org/browse/MDEV-16437): merge 5.7 P\_S replication instrumentation and tables
* Merge [Revision #5c76e1e693](https://github.com/MariaDB/server/commit/5c76e1e693) 2021-04-15 20:21:11 +0300 - Merge 10.5 into 10.6
* [Revision #3f8df01194](https://github.com/MariaDB/server/commit/3f8df01194)\
  2021-04-15 11:40:43 +0300
  * [MDEV-25425](https://jira.mariadb.org/browse/MDEV-25425) Useless message "If the mysqld execution user is authorized page cleaner thread priority can be changed."
* [Revision #de746304c9](https://github.com/MariaDB/server/commit/de746304c9)\
  2020-12-20 20:52:51 +0200
  * Fix riscv64 build failure by linking correctly with pthread
* [Revision #f26e3259a1](https://github.com/MariaDB/server/commit/f26e3259a1)\
  2020-12-20 23:48:20 +0200
  * Deb: Use build flag to enforce default charset as utf8mb4
* [Revision #1715fef107](https://github.com/MariaDB/server/commit/1715fef107)\
  2021-04-14 10:17:16 +0200
  * Fix cross-compile to consider CMAKE\_CROSSCOMPILING\_EMULATOR
* [Revision #a3e3225cd3](https://github.com/MariaDB/server/commit/a3e3225cd3)\
  2021-04-11 08:22:28 -0700
  * [MCOL-4535](https://jira.mariadb.org/browse/MCOL-4535): Clean up libreadline as ColumnStore no longer needs it
* [Revision #f82e69735e](https://github.com/MariaDB/server/commit/f82e69735e)\
  2021-04-13 20:54:37 +1000
  * io\_liburing: ENOMEM handling - use io\_uring\_mlock\_size
* [Revision #f46536e7c3](https://github.com/MariaDB/server/commit/f46536e7c3)\
  2021-04-14 23:09:06 +0300
  * fix perfschema tests in a non-perfschema builds
* Merge [Revision #c071cc3455](https://github.com/MariaDB/server/commit/c071cc3455) 2021-04-14 15:48:05 +0300 - Merge 10.5 into 10.6
* [Revision #d1f2001ee6](https://github.com/MariaDB/server/commit/d1f2001ee6)\
  2021-04-14 15:23:00 +0300
  * fixup 6c3e860cbf36831c118f6ea183acbbeb3c889bed
* [Revision #ee87850461](https://github.com/MariaDB/server/commit/ee87850461)\
  2021-04-14 14:01:12 +0300
  * [MDEV-16708](https://jira.mariadb.org/browse/MDEV-16708): Unsupported commands for prepared statements
* Merge [Revision #6729dd894c](https://github.com/MariaDB/server/commit/6729dd894c) 2021-04-14 13:39:28 +0300 - Merge 10.5 into 10.6
* Merge [Revision #8d472f2b78](https://github.com/MariaDB/server/commit/8d472f2b78) 2021-04-14 12:48:48 +0300 - Merge 10.4 into 10.5
* [Revision #767d63374e](https://github.com/MariaDB/server/commit/767d63374e)\
  2021-04-14 12:43:36 +0300
  * After-merge fix: Make GCC 4.8.5 happy
* [Revision #9a3cbc0541](https://github.com/MariaDB/server/commit/9a3cbc0541)\
  2021-04-13 20:23:46 +0100
  * mysqld: print status display subset of memory usage.
* Merge [Revision #d2e2d32933](https://github.com/MariaDB/server/commit/d2e2d32933) 2021-04-14 12:32:27 +0300 - Merge 10.5 into 10.6
* Merge [Revision #6c3e860cbf](https://github.com/MariaDB/server/commit/6c3e860cbf) 2021-04-14 11:35:39 +0300 - Merge 10.4 into 10.5
* Merge [Revision #5008171b05](https://github.com/MariaDB/server/commit/5008171b05) 2021-04-14 10:33:59 +0300 - Merge 10.3 into 10.4
* [Revision #13d0641710](https://github.com/MariaDB/server/commit/13d0641710)\
  2021-04-14 10:09:04 +0300
  * Fixup merge 6e6318b29b446f76f01f2ef65d1460870b607d2a
* Merge [Revision #ef26a30486](https://github.com/MariaDB/server/commit/ef26a30486) 2021-04-14 07:54:43 +0300 - Merge 10.2 into 10.3
* [Revision #55a7682a30](https://github.com/MariaDB/server/commit/55a7682a30)\
  2021-04-13 16:44:09 +0200
  * -DMYSQL\_MAINTAINER\_MODE=NO
* [Revision #b8c8692fd9](https://github.com/MariaDB/server/commit/b8c8692fd9)\
  2021-04-13 10:28:13 +0300
  * [MDEV-24620](https://jira.mariadb.org/browse/MDEV-24620) ASAN heap-buffer-overflow in btr\_pcur\_restore\_position()
* Merge [Revision #6e6318b29b](https://github.com/MariaDB/server/commit/6e6318b29b) 2021-04-13 10:26:01 +0300 - Merge 10.2 into 10.3
* [Revision #e262eb165c](https://github.com/MariaDB/server/commit/e262eb165c)\
  2021-04-13 10:09:16 +0530
  * [MDEV-24971](https://jira.mariadb.org/browse/MDEV-24971) InnoDB access freed virtual column after rollback of secondary index
* [Revision #f776fa96b4](https://github.com/MariaDB/server/commit/f776fa96b4)\
  2021-02-03 12:04:06 +0300
  * [MDEV-24135](https://jira.mariadb.org/browse/MDEV-24135): Print warnings in XML, save test retries in XML, save the combinations in XML, replace the special symbols in the XML comment
* [Revision #68e0defc5b](https://github.com/MariaDB/server/commit/68e0defc5b)\
  2021-04-12 15:46:23 +0200
  * [MDEV-25182](https://jira.mariadb.org/browse/MDEV-25182) Complex query in Store procedure corrupts results
* [Revision #f8bf2a0170](https://github.com/MariaDB/server/commit/f8bf2a0170)\
  2021-04-12 19:28:10 +0700
  * [MDEV-25108](https://jira.mariadb.org/browse/MDEV-25108): Running of the EXPLAIN EXTENDED statement produces extra warning in case it is executed in PS (prepared statement) mode
* [Revision #e95cdc451a](https://github.com/MariaDB/server/commit/e95cdc451a)\
  2021-04-12 04:11:28 +0200
  * [MDEV-21484](https://jira.mariadb.org/browse/MDEV-21484): galera\_sst\_mariadb-backup\_encrypt\_with\_key test failed
* [Revision #cf2c6b7f8d](https://github.com/MariaDB/server/commit/cf2c6b7f8d)\
  2021-04-09 21:30:43 +0530
  * [MDEV-24971](https://jira.mariadb.org/browse/MDEV-24971) InnoDB access freed virtual column after rollback of secondary index
* [Revision #ea2d44d01b](https://github.com/MariaDB/server/commit/ea2d44d01b)\
  2021-04-12 11:29:32 +0300
  * [MDEV-18802](https://jira.mariadb.org/browse/MDEV-18802) Assertion table->stat\_initialized failed in dict\_stats\_update\_if\_needed()
* [Revision #75dd7a0483](https://github.com/MariaDB/server/commit/75dd7a0483)\
  2021-04-12 10:53:08 +0300
  * [MDEV-24434](https://jira.mariadb.org/browse/MDEV-24434) Assertion trx->in\_rw\_trx\_list... in trx\_sys\_any\_active\_transactions()
* [Revision #058d93d47a](https://github.com/MariaDB/server/commit/058d93d47a)\
  2021-04-11 22:05:52 -0700
  * Deb: Stop depending on empty transitional package dh-systemd
* [Revision #966c5a35af](https://github.com/MariaDB/server/commit/966c5a35af)\
  2021-04-01 07:01:11 +0200
  * [MDEV-25307](https://jira.mariadb.org/browse/MDEV-25307): The value of the auto-increment variables changes during the test
* [Revision #3eecb8db22](https://github.com/MariaDB/server/commit/3eecb8db22)\
  2021-04-11 17:07:36 +0200
  * [MDEV-25356](https://jira.mariadb.org/browse/MDEV-25356): SST scripts should use the new mariadb-backup interface
* [Revision #bf1e09e0c4](https://github.com/MariaDB/server/commit/bf1e09e0c4)\
  2021-04-07 16:53:23 +0200
  * Removed extra spaces in generated command lines (minor "cosmetic" change after [MDEV-24197](https://jira.mariadb.org/browse/MDEV-24197))
* [Revision #d5dacca4c5](https://github.com/MariaDB/server/commit/d5dacca4c5)\
  2021-04-07 16:49:10 +0200
  * Clarified abbreviated option names in some tests, to avoid problems with ambiguous options in the future.
* [Revision #8ff0ac45dc](https://github.com/MariaDB/server/commit/8ff0ac45dc)\
  2021-04-07 16:44:30 +0200
  * [MDEV-25328](https://jira.mariadb.org/browse/MDEV-25328): --innodb command line option causes mariadb-backup to fail
* [Revision #1ac4d0c168](https://github.com/MariaDB/server/commit/1ac4d0c168)\
  2021-04-09 17:38:21 +0530
  * BtrBulk::table\_name(): Return the table name while displaying table name for fts diagnostics
* Merge [Revision #450c017c2d](https://github.com/MariaDB/server/commit/450c017c2d) 2021-04-09 14:32:06 +0300 - Merge 10.2 into 10.3
* [Revision #5a3151bcda](https://github.com/MariaDB/server/commit/5a3151bcda)\
  2021-04-09 12:01:42 +0530
  * Improve diagnostics in order to catch [MDEV-18868](https://jira.mariadb.org/browse/MDEV-18868) and similar bugs
* [Revision #c6d0531cad](https://github.com/MariaDB/server/commit/c6d0531cad)\
  2021-04-08 09:46:56 +0300
  * [MDEV-13467](https://jira.mariadb.org/browse/MDEV-13467) fixup: Improve error handling
* [Revision #72da83ff99](https://github.com/MariaDB/server/commit/72da83ff99)\
  2021-03-30 18:42:28 +0530
  * [MDEV-25019](https://jira.mariadb.org/browse/MDEV-25019) memory allocation failures during startup because server failure in different, confusing ways
* [Revision #82a2ea64b4](https://github.com/MariaDB/server/commit/82a2ea64b4)\
  2021-03-19 17:11:04 +0700
  * Fix postinst trigger when systemd is not running (Closes: #983563)
* [Revision #c32edd7515](https://github.com/MariaDB/server/commit/c32edd7515)\
  2021-04-06 18:51:41 +0530
  * [MDEV-25295](https://jira.mariadb.org/browse/MDEV-25295) Aborted FTS\_DOC\_ID\_INDEX considered as existing FTS\_DOC\_ID\_INDEX during DDL
* [Revision #6fe624b5ac](https://github.com/MariaDB/server/commit/6fe624b5ac)\
  2021-04-03 12:12:15 +0200
  * [MDEV-25242](https://jira.mariadb.org/browse/MDEV-25242) Server crashes in check\_grant upon invoking function with userstat enabled
* [Revision #fb9d151934](https://github.com/MariaDB/server/commit/fb9d151934)\
  2021-04-01 21:47:30 +0200
  * [MDEV-25321](https://jira.mariadb.org/browse/MDEV-25321): mariadb-backup failed if password is passed via environment variable
* [Revision #5bc5ecce08](https://github.com/MariaDB/server/commit/5bc5ecce08)\
  2021-04-01 15:03:59 +0530
  * [MDEV-24197](https://jira.mariadb.org/browse/MDEV-24197): Add "innodb\_force\_recovery" for "mariadb-backup --prepare"
* [Revision #f93e087d74](https://github.com/MariaDB/server/commit/f93e087d74)\
  2021-03-31 11:29:51 +0200
  * [MDEV-25047](https://jira.mariadb.org/browse/MDEV-25047): SIGSEGV in mach\_read\_from\_n\_little\_endian
* [Revision #453bac08c2](https://github.com/MariaDB/server/commit/453bac08c2)\
  2021-03-31 14:26:10 +0200
  * CMake - when searching bison, look also for win\_bison
* [Revision #08cb5d8483](https://github.com/MariaDB/server/commit/08cb5d8483)\
  2021-03-31 14:23:56 +0200
  * [MDEV-25221](https://jira.mariadb.org/browse/MDEV-25221) Do not remove source file, if copy\_file() fails in mariadb-backup --move-back
* [Revision #35ee4aa4e3](https://github.com/MariaDB/server/commit/35ee4aa4e3)\
  2021-03-31 09:06:44 +0300
  * [MDEV-13103](https://jira.mariadb.org/browse/MDEV-13103) fixup: Actually fix a crash during IMPORT TABLESPACE
* [Revision #4c80dcda46](https://github.com/MariaDB/server/commit/4c80dcda46)\
  2021-04-01 16:49:07 +0300
  * fix gcc optimized build
* [Revision #77ffbbca49](https://github.com/MariaDB/server/commit/77ffbbca49)\
  2021-03-24 20:34:16 +0300
  * [MDEV-25172](https://jira.mariadb.org/browse/MDEV-25172) Wrong error message for ADD COLUMN .. AS ROW START
* [Revision #0c99e6e9a6](https://github.com/MariaDB/server/commit/0c99e6e9a6)\
  2021-02-14 23:26:12 +0300
  * [MDEV-22562](https://jira.mariadb.org/browse/MDEV-22562) Assertion \`next\_insert\_id == 0' upon UPDATE on system-versioned table
* [Revision #af52a0e516](https://github.com/MariaDB/server/commit/af52a0e516)\
  2021-02-05 01:52:21 +0300
  * [MDEV-24690](https://jira.mariadb.org/browse/MDEV-24690) Dropping primary key column from versioned table always fails with 1072
* [Revision #b9d1c6574b](https://github.com/MariaDB/server/commit/b9d1c6574b)\
  2021-01-25 13:02:28 +0300
  * [MDEV-23446](https://jira.mariadb.org/browse/MDEV-23446) goto error cleanup
* [Revision #61f84bba60](https://github.com/MariaDB/server/commit/61f84bba60)\
  2021-04-13 09:38:32 +0700
  * [MDEV-25197](https://jira.mariadb.org/browse/MDEV-25197): The statement set password=password('') executed in PS mode fails in case it is run by a user with expired password
* [Revision #e14b682636](https://github.com/MariaDB/server/commit/e14b682636)\
  2021-04-12 17:49:36 +0300
  * Fixed assert in WSREP if one started with --wsrep\_provider=.. --wsrep\_on=OFF
* [Revision #c03841ec0e](https://github.com/MariaDB/server/commit/c03841ec0e)\
  2021-04-08 17:25:02 +0300
  * [MDEV-23634](https://jira.mariadb.org/browse/MDEV-23634): Select query hanged the server and leads to OOM ...
* [Revision #9ff737b25e](https://github.com/MariaDB/server/commit/9ff737b25e)\
  2021-04-13 04:51:11 +0200
  * [MDEV-25307](https://jira.mariadb.org/browse/MDEV-25307): The value of the auto-increment variables changes during the test
* [Revision #58f184a4cb](https://github.com/MariaDB/server/commit/58f184a4cb)\
  2021-04-13 16:15:15 +0300
  * [MDEV-24745](https://jira.mariadb.org/browse/MDEV-24745) Generic CRC-32C computation wrongly uses SSE4.2 instructions
* [Revision #18a8290126](https://github.com/MariaDB/server/commit/18a8290126)\
  2021-03-09 21:30:30 +0100
  * [MDEV-23015](https://jira.mariadb.org/browse/MDEV-23015): mariadb-setpermission seems incompatible with DBI:MariaDB
* [Revision #9636b7cf55](https://github.com/MariaDB/server/commit/9636b7cf55)\
  2021-04-12 20:42:41 +0400
  * [MDEV-25393](https://jira.mariadb.org/browse/MDEV-25393) Fix mysql-test/lib/mtr\_cases.pm to search tests in submodules
* [Revision #72e0601d11](https://github.com/MariaDB/server/commit/72e0601d11)\
  2021-04-14 12:31:51 +0300
  * [MDEV-24966](https://jira.mariadb.org/browse/MDEV-24966) fixup: cmake -DWITH\_WSREP=OFF
* [Revision #a1e70388c4](https://github.com/MariaDB/server/commit/a1e70388c4)\
  2021-02-28 19:33:30 +0200
  * [MDEV-24966](https://jira.mariadb.org/browse/MDEV-24966) Galera multi-master regression
* [Revision #f74704c7d9](https://github.com/MariaDB/server/commit/f74704c7d9)\
  2020-04-14 20:38:44 +0300
  * [MDEV-18019](https://jira.mariadb.org/browse/MDEV-18019), [MDEV-18135](https://jira.mariadb.org/browse/MDEV-18135): Renew test OpenSSL certs at level 3 security
* [Revision #88af187db9](https://github.com/MariaDB/server/commit/88af187db9)\
  2021-04-10 11:18:05 +1000
  * Revert "[MDEV-13115](https://jira.mariadb.org/browse/MDEV-13115): SKIP LOCKED postfix"
* [Revision #51630d595d](https://github.com/MariaDB/server/commit/51630d595d)\
  2021-04-10 07:40:38 +1000
  * [MDEV-13115](https://jira.mariadb.org/browse/MDEV-13115): SKIP LOCKED postfix
* [Revision #de119fa2b6](https://github.com/MariaDB/server/commit/de119fa2b6)\
  2021-04-09 09:18:07 +0300
  * [MDEV-25297](https://jira.mariadb.org/browse/MDEV-25297) Assertion: trx->roll\_limit <= trx->undo\_no in ROLLBACK TO SAVEPOINT
* [Revision #7588049374](https://github.com/MariaDB/server/commit/7588049374)\
  2021-04-08 17:30:04 +1000
  * [MDEV-25280](https://jira.mariadb.org/browse/MDEV-25280): cpack\_rpm - MariaDB-client file moves
* [Revision #1fde581237](https://github.com/MariaDB/server/commit/1fde581237)\
  2021-04-08 18:01:27 +0300
  * [MDEV-25315](https://jira.mariadb.org/browse/MDEV-25315) Crash in SHOW ENGINE INNODB STATUS
* [Revision #f9bd7f2012](https://github.com/MariaDB/server/commit/f9bd7f2012)\
  2021-04-08 17:12:59 +0530
  * [MDEV-20220](https://jira.mariadb.org/browse/MDEV-20220): Merge 5.7 P\_S replication table 'replication\_applier\_status\_by\_worker
* [Revision #036ee61246](https://github.com/MariaDB/server/commit/036ee61246)\
  2021-04-08 16:09:09 +0530
  * [MDEV-20220](https://jira.mariadb.org/browse/MDEV-20220): Merge 5.7 P\_S replication table 'replication\_applier\_status\_by\_worker
* [Revision #94f1d0f84d](https://github.com/MariaDB/server/commit/94f1d0f84d)\
  2021-04-08 15:49:32 +0530
  * [MDEV-20220](https://jira.mariadb.org/browse/MDEV-20220): Merge 5.7 P\_S replication table 'replication\_applier\_status\_by\_worker
* [Revision #7c524d4414](https://github.com/MariaDB/server/commit/7c524d4414)\
  2021-04-08 13:32:16 +0300
  * [MDEV-25371](https://jira.mariadb.org/browse/MDEV-25371) Potential hang in wsrep\_is\_BF\_lock\_timeout()
* Merge [Revision #1900c2ede5](https://github.com/MariaDB/server/commit/1900c2ede5) 2021-04-08 10:11:36 +0300 - Merge 10.5 into 10.6
* [Revision #0ba845a8c7](https://github.com/MariaDB/server/commit/0ba845a8c7)\
  2021-04-08 09:24:03 +0300
  * [MDEV-17913](https://jira.mariadb.org/browse/MDEV-17913) fixup: Correct a DBUG\_PRINT format string
* Merge [Revision #b4f09aa268](https://github.com/MariaDB/server/commit/b4f09aa268) 2021-04-08 08:15:11 +0300 - Merge 10.4 into 10.5
* [Revision #4e2ca42225](https://github.com/MariaDB/server/commit/4e2ca42225)\
  2021-04-06 16:37:11 +0300
  * [MDEV-25334](https://jira.mariadb.org/browse/MDEV-25334) FTWRL/Backup blocks DDL on temporary tables with binlog enabled, assertion fails in Diagnostics\_area::set\_error\_status
* Merge [Revision #2a7810759d](https://github.com/MariaDB/server/commit/2a7810759d) 2021-04-08 08:08:53 +0300 - [MDEV-22775](https://jira.mariadb.org/browse/MDEV-22775): Merge 10.4 into 10.5
* [Revision #58780b5afb](https://github.com/MariaDB/server/commit/58780b5afb)\
  2021-03-25 06:55:18 +0400
  * [MDEV-22775](https://jira.mariadb.org/browse/MDEV-22775) \[HY000]\[1553] Changing name of primary key column with foreign key constraint fails.
* Merge [Revision #7b48da4d7e](https://github.com/MariaDB/server/commit/7b48da4d7e) 2021-04-08 07:47:49 +0300 - Merge 10.4 into 10.5
* [Revision #f69c1c9dcb](https://github.com/MariaDB/server/commit/f69c1c9dcb)\
  2021-04-06 16:57:38 +1000
  * [MDEV-19508](https://jira.mariadb.org/browse/MDEV-19508): SI\_KERNEL is not on all implementations
* [Revision #5b71e0424c](https://github.com/MariaDB/server/commit/5b71e0424c)\
  2021-04-06 15:33:13 +0300
  * [MDEV-21402](https://jira.mariadb.org/browse/MDEV-21402) : sql\_safe\_updates breaks Galera 4
* [Revision #f8488370d6](https://github.com/MariaDB/server/commit/f8488370d6)\
  2021-03-31 14:59:50 +0200
  * [MDEV-24956](https://jira.mariadb.org/browse/MDEV-24956): ALTER TABLE not replicated with Galera in [MariaDB 10.5.9](../../old-releases/mariadb-10-5-series/mariadb-1059-release-notes.md)
* [Revision #915983e1cc](https://github.com/MariaDB/server/commit/915983e1cc)\
  2021-03-24 10:55:27 +0100
  * [MDEV-25226](https://jira.mariadb.org/browse/MDEV-25226) Assertion when wsrep\_on set OFF with SR transaction
* [Revision #880baedcf6](https://github.com/MariaDB/server/commit/880baedcf6)\
  2021-04-02 18:13:46 +0300
  * [MDEV-17913](https://jira.mariadb.org/browse/MDEV-17913) Encrypted transactional Aria tables remain corrupt after crash recovery, automatic repairment does not work
* [Revision #81258f1432](https://github.com/MariaDB/server/commit/81258f1432)\
  2021-04-02 22:00:36 +0300
  * [MDEV-17913](https://jira.mariadb.org/browse/MDEV-17913) Encrypted transactional Aria tables remain corrupt after crash recovery, automatic repairment does not work
* [Revision #76db096ae6](https://github.com/MariaDB/server/commit/76db096ae6)\
  2021-03-25 18:37:07 +1100
  * GIS skip\_locked\_nowait test needs fixing
* [Revision #f41f719924](https://github.com/MariaDB/server/commit/f41f719924)\
  2021-03-13 13:53:33 +1100
  * [MDEV-13115](https://jira.mariadb.org/browse/MDEV-13115): Add Oracle SKIP LOCKED tests cases
* [Revision #553ef1a78b](https://github.com/MariaDB/server/commit/553ef1a78b)\
  2021-03-05 17:25:15 +1100
  * [MDEV-13115](https://jira.mariadb.org/browse/MDEV-13115): Implement SELECT SKIP LOCKED
* [Revision #058484687a](https://github.com/MariaDB/server/commit/058484687a)\
  2021-03-24 15:41:10 +1100
  * Add TL\_FIRST\_WRITE in SQL layer for determining R/W
* [Revision #cf552f5886](https://github.com/MariaDB/server/commit/cf552f5886)\
  2021-04-07 18:01:13 +0300
  * [MDEV-25312](https://jira.mariadb.org/browse/MDEV-25312) Replace fil\_space\_t::name with fil\_space\_t::name()
* [Revision #c2a63ac526](https://github.com/MariaDB/server/commit/c2a63ac526)\
  2020-04-12 12:33:44 +1000
  * unittest: my\_getopt-t errors on -ve ul{l,}
* [Revision #46852b3bbb](https://github.com/MariaDB/server/commit/46852b3bbb)\
  2020-04-11 15:03:54 +1000
  * [MDEV-22219](https://jira.mariadb.org/browse/MDEV-22219): error on parsing negative unsigned options
* Merge [Revision #609e8e38bb](https://github.com/MariaDB/server/commit/609e8e38bb) 2021-04-01 10:00:46 +0300 - Merge 10.5 into 10.6
* [Revision #7f75acc05c](https://github.com/MariaDB/server/commit/7f75acc05c)\
  2021-04-01 09:36:37 +0300
  * [MDEV-25313](https://jira.mariadb.org/browse/MDEV-25313): Assertion pending==log\_requests.start... failed
* [Revision #1d41e9df4a](https://github.com/MariaDB/server/commit/1d41e9df4a)\
  2021-04-01 09:19:21 +0300
  * [MDEV-25314](https://jira.mariadb.org/browse/MDEV-25314) Assertion \`trx.is\_wsrep()' failed in wsrep\_is\_BF\_lock\_timeout()
* [Revision #1bd4115841](https://github.com/MariaDB/server/commit/1bd4115841)\
  2021-03-31 22:15:54 +0300
  * After-merge fix: WITH\_WSREP=ON CMAKE\_BUILD\_TYPE=RelWithDebInfo
* Merge [Revision #82e44d60d1](https://github.com/MariaDB/server/commit/82e44d60d1) 2021-03-31 15:50:59 +0300 - Merge 10.5 into 10.6
* [Revision #147a317e81](https://github.com/MariaDB/server/commit/147a317e81)\
  2021-03-31 14:11:56 +0300
  * [MDEV-25072](https://jira.mariadb.org/browse/MDEV-25072): Livelock due to innodb\_change\_buffering\_debug
* Merge [Revision #176aaf93d1](https://github.com/MariaDB/server/commit/176aaf93d1) 2021-03-31 12:04:50 +0300 - Merge 10.5 into 10.6
* Merge [Revision #5eae8c2742](https://github.com/MariaDB/server/commit/5eae8c2742) 2021-03-31 11:05:21 +0300 - Merge 10.4 into 10.5
* [Revision #8341f582b2](https://github.com/MariaDB/server/commit/8341f582b2)\
  2021-03-31 10:55:21 +0300
  * [MDEV-15527](https://jira.mariadb.org/browse/MDEV-15527) fixup for innodb\_checksum\_algorithm=full\_crc32
* Merge [Revision #50de71b026](https://github.com/MariaDB/server/commit/50de71b026) 2021-03-31 09:47:14 +0300 - Merge 10.3 into 10.4
* Merge [Revision #d6d3d9ae2f](https://github.com/MariaDB/server/commit/d6d3d9ae2f) 2021-03-31 08:01:03 +0300 - Merge 10.2 into 10.3
* [Revision #99945d77d7](https://github.com/MariaDB/server/commit/99945d77d7)\
  2021-03-30 09:24:25 +0100
  * [MDEV-25294](https://jira.mariadb.org/browse/MDEV-25294) signal handler display coredump on mac
* [Revision #b771ab242b](https://github.com/MariaDB/server/commit/b771ab242b)\
  2021-03-29 18:51:36 +0530
  * [MDEV-25200](https://jira.mariadb.org/browse/MDEV-25200) Index count mismatch due to aborted FULLTEXT INDEX
* [Revision #108ba4c380](https://github.com/MariaDB/server/commit/108ba4c380)\
  2021-03-30 20:34:39 +0530
  * [MDEV-15527](https://jira.mariadb.org/browse/MDEV-15527) page\_compressed compressed page partially during import tablespace
* [Revision #7c423c26d9](https://github.com/MariaDB/server/commit/7c423c26d9)\
  2021-03-30 16:14:19 +0300
  * Add missing have\_perfschema.inc
* [Revision #c468d5cb50](https://github.com/MariaDB/server/commit/c468d5cb50)\
  2021-03-30 15:18:06 +0530
  * [MDEV-15527](https://jira.mariadb.org/browse/MDEV-15527) page\_compressed compressed page partially during import tablespace
* [Revision #dfda1c9283](https://github.com/MariaDB/server/commit/dfda1c9283)\
  2021-03-30 08:08:21 +0300
  * Add supression for warning.
* [Revision #d217a925b2](https://github.com/MariaDB/server/commit/d217a925b2)\
  2021-03-03 12:14:23 +0200
  * [MDEV-24923](https://jira.mariadb.org/browse/MDEV-24923) : Port selected Galera conflict resolution changes from 10.6
* [Revision #c44273329e](https://github.com/MariaDB/server/commit/c44273329e)\
  2021-03-30 16:18:30 +1100
  * remove broken tests/grant.pl
* [Revision #fb3b2eb517](https://github.com/MariaDB/server/commit/fb3b2eb517)\
  2021-03-30 16:16:24 +1100
  * mallinfo2: whitespace fix
* [Revision #add24e7889](https://github.com/MariaDB/server/commit/add24e7889)\
  2021-03-29 14:32:36 +0200
  * Windows - suppress nonsensical(for this OS) system check.
* [Revision #85b6a81805](https://github.com/MariaDB/server/commit/85b6a81805)\
  2021-01-14 16:55:35 +1100
  * [MDEV-24586](https://jira.mariadb.org/browse/MDEV-24586): remove mysql\_to\_mariadb.sql
* [Revision #4d870b591d](https://github.com/MariaDB/server/commit/4d870b591d)\
  2021-03-15 14:35:08 +0200
  * Don't pass password to innobackup via command line, use environment instead
* [Revision #94dea8ef5b](https://github.com/MariaDB/server/commit/94dea8ef5b)\
  2021-03-27 22:54:18 +0400
  * [MDEV-25457](https://jira.mariadb.org/browse/MDEV-25457) CREATE / DROP PROCEDURE not logged with audit plugin.
* [Revision #c0ca3c4ffa](https://github.com/MariaDB/server/commit/c0ca3c4ffa)\
  2021-03-26 18:01:10 +0700
  * [MDEV-25240](https://jira.mariadb.org/browse/MDEV-25240) minor upgrade does not perform server restart
* [Revision #2fc76a5022](https://github.com/MariaDB/server/commit/2fc76a5022)\
  2021-03-27 21:02:09 +0100
  * [MDEV-13467](https://jira.mariadb.org/browse/MDEV-13467): Feature request: Support for ST\_Distance\_Sphere()
* [Revision #5eda18f0ca](https://github.com/MariaDB/server/commit/5eda18f0ca)\
  2021-03-27 10:54:57 +0100
  * [MDEV-25272](https://jira.mariadb.org/browse/MDEV-25272): Wrong function name in error messages upon ST\_GeomFromGeoJSON call
* [Revision #6769d1a078](https://github.com/MariaDB/server/commit/6769d1a078)\
  2020-10-29 01:40:31 +0100
  * [MDEV-13467](https://jira.mariadb.org/browse/MDEV-13467): Feature request: Support for ST\_Distance\_Sphere()
* [Revision #96475b78c5](https://github.com/MariaDB/server/commit/96475b78c5)\
  2021-03-27 23:07:31 +0400
  * [MDEV-25457](https://jira.mariadb.org/browse/MDEV-25457) CREATE / DROP PROCEDURE not logged with audit plugin.
* [Revision #bf310b4cfb](https://github.com/MariaDB/server/commit/bf310b4cfb)\
  2021-03-30 16:17:10 +0300
  * [MDEV-25305](https://jira.mariadb.org/browse/MDEV-25305): MyRocks: Killing server during RESET MASTER can lose last transactions
* [Revision #5b678d9ea4](https://github.com/MariaDB/server/commit/5b678d9ea4)\
  2021-03-28 23:45:04 +0300
  * [MDEV-25251](https://jira.mariadb.org/browse/MDEV-25251): main.derived\_split\_innodb fails on ICC release binary
* [Revision #eb2d36296e](https://github.com/MariaDB/server/commit/eb2d36296e)\
  2021-03-30 18:47:05 +0300
  * [MDEV-25305](https://jira.mariadb.org/browse/MDEV-25305): MyRocks: Killing server during RESET MASTER can lose last transactions
* [Revision #ed221980fc](https://github.com/MariaDB/server/commit/ed221980fc)\
  2021-03-30 16:17:10 +0300
  * [MDEV-25305](https://jira.mariadb.org/browse/MDEV-25305): MyRocks: Killing server during RESET MASTER can lose last transactions
* Merge [Revision #75db05c599](https://github.com/MariaDB/server/commit/75db05c599) 2021-03-30 13:28:05 +0300 - Merge 10.5 into 10.6 (except [MDEV-24630](https://jira.mariadb.org/browse/MDEV-24630))
* [Revision #76d2846a71](https://github.com/MariaDB/server/commit/76d2846a71)\
  2021-03-30 15:57:14 +0800
  * [MDEV-24630](https://jira.mariadb.org/browse/MDEV-24630): MY\_RELAX\_CPU assembly instruction upgrade/research for memory barrier on ARM
* [Revision #8c2e3259c1](https://github.com/MariaDB/server/commit/8c2e3259c1)\
  2021-03-30 09:58:24 +0300
  * [MDEV-24302](https://jira.mariadb.org/browse/MDEV-24302) follow-up: RESET MASTER hangs
* [Revision #49ddfb6378](https://github.com/MariaDB/server/commit/49ddfb6378)\
  2021-03-30 14:57:58 +1100
  * revert make\_binary\_distribution script creation
* Merge [Revision #6ca07c2109](https://github.com/MariaDB/server/commit/6ca07c2109) 2021-03-30 14:43:25 +1100 - Merge 10.5 into 10.6
* [Revision #0df74a0197](https://github.com/MariaDB/server/commit/0df74a0197)\
  2021-03-11 22:04:22 +0200
  * Deb: Fix failing Salsa-CI by syncing fixes from downstream to upstream
* [Revision #5a4daa9099](https://github.com/MariaDB/server/commit/5a4daa9099)\
  2020-12-27 01:45:40 +0200
  * Deb: Add Breaks/Replaces
* [Revision #ab3777a3bf](https://github.com/MariaDB/server/commit/ab3777a3bf)\
  2020-12-26 20:35:52 +0200
  * Revert "[MDEV-23342](https://jira.mariadb.org/browse/MDEV-23342) MariaDB cannot be installed over MySQL 5.7.30 on Bionic anymore"
* [Revision #831adb1e5c](https://github.com/MariaDB/server/commit/831adb1e5c)\
  2021-03-30 09:38:34 +1100
  * [MDEV-17239](https://jira.mariadb.org/browse/MDEV-17239) default max\_recursive\_iterations 4G -> 1000
* Merge [Revision #2ad61c6782](https://github.com/MariaDB/server/commit/2ad61c6782) 2021-03-29 16:16:12 +0300 - Merge 10.5 into 10.6
* [Revision #e8b7fceb82](https://github.com/MariaDB/server/commit/e8b7fceb82)\
  2021-03-29 15:16:23 +0300
  * [MDEV-24302](https://jira.mariadb.org/browse/MDEV-24302): RESET MASTER hangs
* [Revision #8e2d69f7b8](https://github.com/MariaDB/server/commit/8e2d69f7b8)\
  2021-03-28 18:43:14 +0300
  * Fixed access to undefined memory
* [Revision #0f6f72965b](https://github.com/MariaDB/server/commit/0f6f72965b)\
  2021-03-29 11:51:00 +0800
  * [MDEV-25281](https://jira.mariadb.org/browse/MDEV-25281): Switch to use non-atomic (vs atomic) distributed counter to track page-access counter
* [Revision #8048831a5b](https://github.com/MariaDB/server/commit/8048831a5b)\
  2021-03-29 14:32:36 +0200
  * Windows - suppress nonsensical(for this OS) system check.
* [Revision #bd43f39bd5](https://github.com/MariaDB/server/commit/bd43f39bd5)\
  2021-03-29 00:33:27 +0300
  * [MDEV-24325](https://jira.mariadb.org/browse/MDEV-24325): Optimizer trace doesn't cover LATERAL DERIVED
* [Revision #e1a514d565](https://github.com/MariaDB/server/commit/e1a514d565)\
  2021-03-29 08:59:40 +1100
  * [MDEV-5536](https://jira.mariadb.org/browse/MDEV-5536): socket activation info - verbose
* [Revision #cba6bbbfef](https://github.com/MariaDB/server/commit/cba6bbbfef)\
  2021-03-27 18:13:51 +1100
  * [MDEV-5536](https://jira.mariadb.org/browse/MDEV-5536): Deb - socket activation - service enable
* [Revision #99f85eec88](https://github.com/MariaDB/server/commit/99f85eec88)\
  2021-03-19 13:42:40 +1100
  * [MDEV-5536](https://jira.mariadb.org/browse/MDEV-5536): Debian systemd socket activation
* [Revision #460d480c74](https://github.com/MariaDB/server/commit/460d480c74)\
  2015-03-12 07:26:04 +1100
  * [MDEV-5536](https://jira.mariadb.org/browse/MDEV-5536): add systemd socket activation
* [Revision #fa0ad2fb11](https://github.com/MariaDB/server/commit/fa0ad2fb11)\
  2021-03-18 14:35:47 +0100
  * Add mariadb-dumpslow to scripts.
* [Revision #d1ee7163bc](https://github.com/MariaDB/server/commit/d1ee7163bc)\
  2021-03-28 12:48:53 +1100
  * mariadb-tzinfo-to-sql,mariadb-dumpslow as Client components
* [Revision #f377081ea9](https://github.com/MariaDB/server/commit/f377081ea9)\
  2021-03-18 09:42:45 +1100
  * [MDEV-23429](https://jira.mariadb.org/browse/MDEV-23429): WITHOUT\_SERVER don't install sst/systemd scripts
* [Revision #09202b2e6d](https://github.com/MariaDB/server/commit/09202b2e6d)\
  2021-03-17 09:14:21 +0100
  * Separate client and server components (man/scripts)
* [Revision #3523aedbdf](https://github.com/MariaDB/server/commit/3523aedbdf)\
  2018-10-27 14:34:15 +0200
  * Make `replace` utility a Client component
* [Revision #27decbbfe6](https://github.com/MariaDB/server/commit/27decbbfe6)\
  2021-03-15 15:25:29 +0100
  * Since PR #1566 my\_print\_defaults is a client so should be man page
* [Revision #4f8945e0ce](https://github.com/MariaDB/server/commit/4f8945e0ce)\
  2020-05-31 14:40:22 +0200
  * Make my\_print\_default a client app (required by mytop)
* [Revision #4cea38431e](https://github.com/MariaDB/server/commit/4cea38431e)\
  2021-03-18 08:48:19 +1100
  * Remove server man pages from WITHOUT\_SERVER
* [Revision #67eeb7770b](https://github.com/MariaDB/server/commit/67eeb7770b)\
  2021-03-15 11:37:19 +0100
  * [MDEV-23429](https://jira.mariadb.org/browse/MDEV-23429): Remove WSREP when using WITHOUT\_SERVER
* Merge [Revision #e538cb095f](https://github.com/MariaDB/server/commit/e538cb095f) 2021-03-27 18:03:03 +0200 - Merge 10.5 into 10.6
* Merge [Revision #80459bcbd4](https://github.com/MariaDB/server/commit/80459bcbd4) 2021-03-27 17:37:42 +0200 - Merge 10.4 into 10.5
* Merge [Revision #7ae37ff74f](https://github.com/MariaDB/server/commit/7ae37ff74f) 2021-03-27 17:12:28 +0200 - Merge 10.3 into 10.4
* Merge [Revision #3157fa182a](https://github.com/MariaDB/server/commit/3157fa182a) 2021-03-27 16:11:26 +0200 - Merge 10.2 into 10.3
* [Revision #48141f3c17](https://github.com/MariaDB/server/commit/48141f3c17)\
  2021-03-26 20:48:59 +0100
  * Replace mallinfo with mallinfo2 on supported systems
* [Revision #36a05268e7](https://github.com/MariaDB/server/commit/36a05268e7)\
  2021-03-24 13:17:49 +0300
  * cmake cleanup: drop support for ancient clang in WITH\_ASAN option
* [Revision #dfae51de36](https://github.com/MariaDB/server/commit/dfae51de36)\
  2021-03-24 13:15:03 +0300
  * [MDEV-25238](https://jira.mariadb.org/browse/MDEV-25238) add support for -fsanitize-address-use-after-scope
* [Revision #a6d66fe75e](https://github.com/MariaDB/server/commit/a6d66fe75e)\
  2021-03-26 14:12:39 +0200
  * [MDEV-24786](https://jira.mariadb.org/browse/MDEV-24786): row\_upd\_clust\_step() skips mtr\_t::commit() on virtual column error
* [Revision #da26e2e673](https://github.com/MariaDB/server/commit/da26e2e673)\
  2021-03-25 08:41:27 +0100
  * Cleanup - reduce duplicate code, in SSL IO error handling.
* [Revision #5a79807119](https://github.com/MariaDB/server/commit/5a79807119)\
  2021-03-24 23:12:16 +0100
  * [MDEV-25242](https://jira.mariadb.org/browse/MDEV-25242) Server crashes in check\_grant upon invoking function with userstat enabled
* [Revision #cdb86faf82](https://github.com/MariaDB/server/commit/cdb86faf82)\
  2021-03-24 08:55:36 +0100
  * [MDEV-23740](https://jira.mariadb.org/browse/MDEV-23740) postfix - potentially uninitialized variable passed to vio\_socket\_io\_wait.
* [Revision #c4807c107a](https://github.com/MariaDB/server/commit/c4807c107a)\
  2021-03-23 21:53:27 +0100
  * [MDEV-24879](https://jira.mariadb.org/browse/MDEV-24879) Client crash on undefined charsetsdir
* [Revision #3dae564703](https://github.com/MariaDB/server/commit/3dae564703)\
  2021-03-22 11:36:33 +0100
  * Follow up fixes for making @@wsrep\_provider read-only
* [Revision #9e57bd278f](https://github.com/MariaDB/server/commit/9e57bd278f)\
  2021-03-23 12:37:55 +0700
  * fixed typo in postinst script
* [Revision #8f7a6cde58](https://github.com/MariaDB/server/commit/8f7a6cde58)\
  2021-03-22 22:04:54 -0700
  * [MDEV-24767](https://jira.mariadb.org/browse/MDEV-24767) Wrong result when forced BNLH is used for join supported by compound index
* [Revision #56274bd5e4](https://github.com/MariaDB/server/commit/56274bd5e4)\
  2021-03-22 18:11:44 +0200
  * [MDEV-23076](https://jira.mariadb.org/browse/MDEV-23076) Misleading "InnoDB: using atomic writes"
* [Revision #0f8caadc96](https://github.com/MariaDB/server/commit/0f8caadc96)\
  2021-03-22 17:46:49 +0200
  * [MDEV-22653](https://jira.mariadb.org/browse/MDEV-22653): Remove the useless parameter innodb\_simulate\_comp\_failures
* [Revision #0e96570171](https://github.com/MariaDB/server/commit/0e96570171)\
  2021-03-22 18:55:59 +0700
  * Added missed ' -- ' between the end of the lldb command options and the beginning of the arguments.
* [Revision #b58b289827](https://github.com/MariaDB/server/commit/b58b289827)\
  2021-03-19 10:56:10 +1100
  * [MDEV-25195](https://jira.mariadb.org/browse/MDEV-25195): pam check getgrouplist function
* [Revision #209e8ecf9a](https://github.com/MariaDB/server/commit/209e8ecf9a)\
  2021-03-20 10:46:43 +0200
  * [MDEV-22240](https://jira.mariadb.org/browse/MDEV-22240): don't use pc.splitbrain=true on node2 in galera.galera\_gcache\_recover
* [Revision #96dd4b53c1](https://github.com/MariaDB/server/commit/96dd4b53c1)\
  2021-03-19 16:10:33 +0200
  * [MDEV-8708](https://jira.mariadb.org/browse/MDEV-8708) fixup: Remove dead code
* [Revision #a74fa579b9](https://github.com/MariaDB/server/commit/a74fa579b9)\
  2021-03-19 03:24:55 +0100
  * [MDEV-24903](https://jira.mariadb.org/browse/MDEV-24903): mariadb-backup SST fails while adding --log-bin in startup command
* [Revision #480a06718d](https://github.com/MariaDB/server/commit/480a06718d)\
  2021-03-23 20:54:54 -0700
  * [MDEV-25128](https://jira.mariadb.org/browse/MDEV-25128) Wrong result from join with materialized semi-join and splittable derived
* [Revision #7d5ec9f1ae](https://github.com/MariaDB/server/commit/7d5ec9f1ae)\
  2021-03-23 12:37:55 +0700
  * fixed typo in postinst script
* [Revision #61e00db6ad](https://github.com/MariaDB/server/commit/61e00db6ad)\
  2021-03-22 15:22:59 +0200
  * [MDEV-24796](https://jira.mariadb.org/browse/MDEV-24796) Assertion \`page\_has\_next... failed in btr\_pcur\_store\_position()
* [Revision #d1ff2c583f](https://github.com/MariaDB/server/commit/d1ff2c583f)\
  2021-03-16 12:53:40 +0100
  * [MDEV-21697](https://jira.mariadb.org/browse/MDEV-21697): Galera assertion !wsrep\_has\_changes(thd) || (thd->lex->sql\_command == SQLCOM\_CREATE\_TABLE && !thd->is\_current\_stmt\_binlog\_format\_row())
* [Revision #161f4036c4](https://github.com/MariaDB/server/commit/161f4036c4)\
  2021-03-25 07:37:50 +0200
  * [MDEV-24954](https://jira.mariadb.org/browse/MDEV-24954) : 10.5.9 crashes on int wsrep::client\_state::ordered\_commit(): Assertion \`owning\_thread\_id\_ == wsrep::this\_thread::get\_id()' failed.
* [Revision #2eae1376fe](https://github.com/MariaDB/server/commit/2eae1376fe)\
  2021-03-23 12:37:55 +0700
  * fixed typo in postinst script
* [Revision #aba7884138](https://github.com/MariaDB/server/commit/aba7884138)\
  2021-03-21 12:08:54 -0700
  * [MDEV-25206](https://jira.mariadb.org/browse/MDEV-25206) Crash with CREATE VIEW .. SELECT with non-existing field in ON condition
* Merge [Revision #356c149603](https://github.com/MariaDB/server/commit/356c149603) 2021-03-26 11:50:32 +0200 - Merge 10.5 into 10.6
* [Revision #2e67b9f665](https://github.com/MariaDB/server/commit/2e67b9f665)\
  2021-03-26 09:58:52 +0200
  * [MDEV-25265](https://jira.mariadb.org/browse/MDEV-25265): ALTER TABLE...IMPORT TABLESPACE fails after DROP INDEX
* [Revision #bcb9ca4105](https://github.com/MariaDB/server/commit/bcb9ca4105)\
  2021-03-23 18:16:20 +1100
  * MEM\_CHECK\_DEFINED: replace HAVE\_valgrind
* [Revision #e731a28394](https://github.com/MariaDB/server/commit/e731a28394)\
  2021-03-23 16:20:15 +0200
  * [MDEV-24589](https://jira.mariadb.org/browse/MDEV-24589) DROP TABLE is not crash-safe
* [Revision #8b11550356](https://github.com/MariaDB/server/commit/8b11550356)\
  2021-03-23 14:58:04 +0200
  * fixup cebf9ee2040195a61fbed32d06cc2e335e9f8dfd
* [Revision #8f23aab068](https://github.com/MariaDB/server/commit/8f23aab068)\
  2021-03-23 14:47:04 +0200
  * [MDEV-15528](https://jira.mariadb.org/browse/MDEV-15528) fixup: Remove dict\_table\_open\_on\_index\_id()
* [Revision #df931d888f](https://github.com/MariaDB/server/commit/df931d888f)\
  2021-03-23 12:37:55 +0700
  * fixed typo in postinst script
* [Revision #d902b53cfe](https://github.com/MariaDB/server/commit/d902b53cfe)\
  2021-03-22 17:53:39 +0200
  * Fixed wrong usage strlen(), should be sizeof()
* [Revision #cebf9ee204](https://github.com/MariaDB/server/commit/cebf9ee204)\
  2020-12-20 21:07:38 +0200
  * Fix various spelling errors still found in code
* [Revision #e9e1890162](https://github.com/MariaDB/server/commit/e9e1890162)\
  2021-03-25 15:17:36 +0300
  * [MDEV-25223](https://jira.mariadb.org/browse/MDEV-25223) follow-up: do not create an iterator from nullptr
* [Revision #b5cea823d7](https://github.com/MariaDB/server/commit/b5cea823d7)\
  2021-03-24 18:56:31 +0200
  * [MDEV-21452](https://jira.mariadb.org/browse/MDEV-21452) fixup: Correct a comment
* [Revision #1274bb7729](https://github.com/MariaDB/server/commit/1274bb7729)\
  2021-03-20 01:31:01 +0300
  * [MDEV-25223](https://jira.mariadb.org/browse/MDEV-25223) change fil\_system\_t::space\_list and fil\_system\_t::named\_spaces from UT\_LIST to ilist
* [Revision #cb545f1116](https://github.com/MariaDB/server/commit/cb545f1116)\
  2021-03-23 09:41:50 +0100
  * CMake cleanup
* [Revision #2e31b2ffe9](https://github.com/MariaDB/server/commit/2e31b2ffe9)\
  2021-03-08 13:13:14 +1100
  * purge HAVE\_CLOSE\_SERVER\_SOCK from sql/mysqld.cc
* [Revision #1170794747](https://github.com/MariaDB/server/commit/1170794747)\
  2021-03-23 12:37:55 +0700
  * fixed typo in postinst script
* [Revision #43ea3d2520](https://github.com/MariaDB/server/commit/43ea3d2520)\
  2020-09-29 12:24:48 +0530
  * [MDEV-21365](https://jira.mariadb.org/browse/MDEV-21365): Check $MARIADB\_HOME/my.cnf in addition to $MYSQL\_HOME/my.cnf
* [Revision #81b5e7dd68](https://github.com/MariaDB/server/commit/81b5e7dd68)\
  2021-03-21 14:18:46 +0300
  * [MDEV-7317](https://jira.mariadb.org/browse/MDEV-7317): Make an index ignorable to the optimizer
* [Revision #c22e6eeda8](https://github.com/MariaDB/server/commit/c22e6eeda8)\
  2021-03-19 22:55:40 +0200
  * Fix compiler warnings in connect engine
* [Revision #93bb755dc8](https://github.com/MariaDB/server/commit/93bb755dc8)\
  2021-03-19 18:35:17 +0200
  * Fixed crash with listen\_sockets when shutdown and kill was run simultaneously
* [Revision #d7d1023217](https://github.com/MariaDB/server/commit/d7d1023217)\
  2021-03-19 18:10:23 +0200
  * Changed std::vector\<MYSQL\_SOCKET> listen\_sockets to Dynamic\_array
* [Revision #cccc96d66c](https://github.com/MariaDB/server/commit/cccc96d66c)\
  2021-03-19 18:15:23 +0200
  * Fixed wrong initializations of Dynamic\_array
* [Revision #8f33f49ebe](https://github.com/MariaDB/server/commit/8f33f49ebe)\
  2021-03-19 14:46:38 +0200
  * Aria: Add transaction id to log of create table
* Merge [Revision #1055cf967f](https://github.com/MariaDB/server/commit/1055cf967f) 2021-03-20 18:40:07 +0200 - Merge 10.5 into 10.6
* [Revision #e7ddf46632](https://github.com/MariaDB/server/commit/e7ddf46632)\
  2021-03-20 13:47:05 +0200
  * [MDEV-25211](https://jira.mariadb.org/browse/MDEV-25211) Remove useless counter Innodb\_buffered\_aio\_submitted
* Merge [Revision #8570a6a093](https://github.com/MariaDB/server/commit/8570a6a093) 2021-03-20 13:34:38 +0200 - Merge 10.4 into 10.5
* Merge [Revision #d8dc8537e4](https://github.com/MariaDB/server/commit/d8dc8537e4) 2021-03-20 13:04:36 +0200 - Merge 10.3 into 10.4
* [Revision #0f3045e432](https://github.com/MariaDB/server/commit/0f3045e432)\
  2021-03-19 17:29:18 +0100
  * fix for engines/funcs/rpl\_sp.test
* Merge [Revision #93d8f887a0](https://github.com/MariaDB/server/commit/93d8f887a0) 2021-03-19 13:33:46 +0200 - Merge 10.2 into 10.3
* [Revision #4e825b0e8a](https://github.com/MariaDB/server/commit/4e825b0e8a)\
  2021-03-19 11:46:07 +0100
  * update libmariadb
* [Revision #4ca4d606ac](https://github.com/MariaDB/server/commit/4ca4d606ac)\
  2021-03-19 11:14:47 +1100
  * myseek: AIX has no "tell"
* [Revision #b34bb81eaf](https://github.com/MariaDB/server/commit/b34bb81eaf)\
  2021-03-15 22:48:30 -0700
  * [MDEV-25112](https://jira.mariadb.org/browse/MDEV-25112) MIN/MAX aggregation over an indexed column may return wrong result
* [Revision #2944d7e692](https://github.com/MariaDB/server/commit/2944d7e692)\
  2021-03-19 12:20:50 +0100
  * fix for tests from engines/funcs
* [Revision #1bacab8ab9](https://github.com/MariaDB/server/commit/1bacab8ab9)\
  2021-03-19 09:31:27 +0000
  * mariadb-backup little FreeBSD update support.
* [Revision #8bdffb3750](https://github.com/MariaDB/server/commit/8bdffb3750)\
  2021-03-19 15:44:07 +0100
  * fix for tests from engines/funcs
* [Revision #e8113f7572](https://github.com/MariaDB/server/commit/e8113f7572)\
  2021-03-20 16:23:47 +0200
  * CMake cleanup: Make WITH\_URING, WITH\_PMEM Boolean
* [Revision #4eeea4e212](https://github.com/MariaDB/server/commit/4eeea4e212)\
  2021-03-20 15:10:36 +1100
  * [MDEV-25207](https://jira.mariadb.org/browse/MDEV-25207) mysql\_install\_db doesn't create sys schema (fix)
* [Revision #47c8896240](https://github.com/MariaDB/server/commit/47c8896240)\
  2021-03-20 00:14:45 +0100
  * [MDEV-25207](https://jira.mariadb.org/browse/MDEV-25207) mysql\_install\_db doesn't create sys schema
* [Revision #b3c470a3c7](https://github.com/MariaDB/server/commit/b3c470a3c7)\
  2021-03-19 18:12:26 +0300
  * [MDEV-23646](https://jira.mariadb.org/browse/MDEV-23646): Optimizer trace: optimize\_cond() should show ON expression processing
* [Revision #b9a45ba40f](https://github.com/MariaDB/server/commit/b9a45ba40f)\
  2021-03-19 17:32:08 +0300
  * [MDEV-23645](https://jira.mariadb.org/browse/MDEV-23645): Optimizer trace: print conditions after substitute\_for\_best\_equal\_field
* Merge [Revision #00528a0445](https://github.com/MariaDB/server/commit/00528a0445) 2021-03-19 13:35:18 +0200 - Merge 10.5 into 10.6
* [Revision #233c09138f](https://github.com/MariaDB/server/commit/233c09138f)\
  2021-03-19 13:10:12 +0200
  * Disable crashing Galera tests: [MDEV-18534](https://jira.mariadb.org/browse/MDEV-18534), [MDEV-24485](https://jira.mariadb.org/browse/MDEV-24485)
* Merge [Revision #be881ec457](https://github.com/MariaDB/server/commit/be881ec457) 2021-03-19 13:06:31 +0200 - Merge 10.4 into 10.5
* [Revision #550cf13eb3](https://github.com/MariaDB/server/commit/550cf13eb3)\
  2021-03-19 11:53:49 +0200
  * Disable failing Galera tests
* Merge [Revision #44d70c01f0](https://github.com/MariaDB/server/commit/44d70c01f0) 2021-03-19 11:42:44 +0200 - Merge 10.3 into 10.4
* [Revision #867724fd30](https://github.com/MariaDB/server/commit/867724fd30)\
  2021-03-18 13:36:02 +0200
  * [MDEV-25125](https://jira.mariadb.org/browse/MDEV-25125) Assertion failure in fetch\_data\_into\_cache\_low()
* Merge [Revision #19052b6deb](https://github.com/MariaDB/server/commit/19052b6deb) 2021-03-18 12:34:48 +0200 - Merge 10.2 into 10.3
* [Revision #c557e9540a](https://github.com/MariaDB/server/commit/c557e9540a)\
  2021-03-18 12:22:11 +0200
  * [MDEV-10682](https://jira.mariadb.org/browse/MDEV-10682) Race condition between ANALYZE and STATS\_AUTO\_RECALC
* [Revision #6505662c23](https://github.com/MariaDB/server/commit/6505662c23)\
  2021-03-18 12:18:16 +0200
  * [MDEV-25121](https://jira.mariadb.org/browse/MDEV-25121): innodb\_flush\_method=O\_DIRECT fails on compressed tables
* [Revision #00f620b27e](https://github.com/MariaDB/server/commit/00f620b27e)\
  2021-03-17 12:12:10 +0100
  * [MDEV-21584](https://jira.mariadb.org/browse/MDEV-21584) - portability fix
* [Revision #14a8b700f3](https://github.com/MariaDB/server/commit/14a8b700f3)\
  2021-03-17 14:09:05 +0200
  * Cleanup: Remove unused OS\_DATA\_TEMP\_FILE
* [Revision #c9ba668992](https://github.com/MariaDB/server/commit/c9ba668992)\
  2021-03-16 13:02:44 +0200
  * [MDEV-24916](https://jira.mariadb.org/browse/MDEV-24916) : Assertion \`current\_stmt\_binlog\_format == BINLOG\_FORMAT\_STMT || current\_stmt\_binlog\_format == BINLOG\_FORMAT\_ROW' failed in THD::is\_current\_stmt\_binlog\_format\_row
* [Revision #f4e14f0e24](https://github.com/MariaDB/server/commit/f4e14f0e24)\
  2021-03-17 12:58:32 +0200
  * [MDEV-18874](https://jira.mariadb.org/browse/MDEV-18874) : Galera test MW-286 causes Mutex = TTASEventMutex]: Assertion \`!is\_owned()' failed. assertion
* [Revision #6974058121](https://github.com/MariaDB/server/commit/6974058121)\
  2021-03-18 14:35:52 +1100
  * mariadb.pc: plugindir is used
* [Revision #66106130a6](https://github.com/MariaDB/server/commit/66106130a6)\
  2021-03-17 11:01:15 +0300
  * switch off storage/innobase/.clang-format: InnoDB uses a common formatting style for all new code
* [Revision #bf303e824c](https://github.com/MariaDB/server/commit/bf303e824c)\
  2021-02-17 04:45:53 +0100
  * [MDEV-21039](https://jira.mariadb.org/browse/MDEV-21039): Server fails to start with unknown mysqld\_safe options
* [Revision #f2c79eda4b](https://github.com/MariaDB/server/commit/f2c79eda4b)\
  2021-03-16 00:15:34 +0100
  * [MDEV-24554](https://jira.mariadb.org/browse/MDEV-24554) Windows authenticode signing stopped working
* [Revision #987cfa227d](https://github.com/MariaDB/server/commit/987cfa227d)\
  2020-10-12 21:15:24 +0200
  * [MDEV-23740](https://jira.mariadb.org/browse/MDEV-23740) - X509\_R\_CERT\_ALREADY\_IN\_HASH\_TABLE when establishing SSL connection connection.
* [Revision #30dea4599e](https://github.com/MariaDB/server/commit/30dea4599e)\
  2021-03-04 14:28:50 +0200
  * [MDEV-24978](https://jira.mariadb.org/browse/MDEV-24978) : SIGABRT in libc\_message
* [Revision #ba7d86a659](https://github.com/MariaDB/server/commit/ba7d86a659)\
  2021-03-12 10:35:08 +0100
  * update libmariadb
* [Revision #390de205cc](https://github.com/MariaDB/server/commit/390de205cc)\
  2021-02-26 20:38:20 +0530
  * [MDEV-24519](https://jira.mariadb.org/browse/MDEV-24519): Server crashes in Charset::set\_charset upon SELECT
* [Revision #1f3f90318f](https://github.com/MariaDB/server/commit/1f3f90318f)\
  2021-03-10 11:52:06 +0200
  * Update sponsors
* [Revision #374ec82f08](https://github.com/MariaDB/server/commit/374ec82f08)\
  2021-03-09 15:11:44 -0800
  * [MDEV-24597](https://jira.mariadb.org/browse/MDEV-24597) Explicit column name error in CTE of UNION
* [Revision #90780bb5a9](https://github.com/MariaDB/server/commit/90780bb5a9)\
  2021-03-10 17:26:43 -0800
  * [MDEV-21104](https://jira.mariadb.org/browse/MDEV-21104) Wrong result (extra rows and wrong values) with incremental BNLH
* [Revision #1af8558193](https://github.com/MariaDB/server/commit/1af8558193)\
  2021-03-10 11:08:51 +0200
  * [MDEV-25101](https://jira.mariadb.org/browse/MDEV-25101) Assertion !strcmp(field->name, "table\_name") failed
* [Revision #ee12b055ff](https://github.com/MariaDB/server/commit/ee12b055ff)\
  2021-03-01 14:29:29 +0100
  * reenable tests from engines/funcs
* [Revision #4020e4aee0](https://github.com/MariaDB/server/commit/4020e4aee0)\
  2021-03-04 23:02:47 -0800
  * [MDEV-25002](https://jira.mariadb.org/browse/MDEV-25002) ON expressions cannot contain outer references
* [Revision #dc6667805d](https://github.com/MariaDB/server/commit/dc6667805d)\
  2021-03-07 01:33:51 +0100
  * Correct the value of global memory\_used
* [Revision #2c0b3141f3](https://github.com/MariaDB/server/commit/2c0b3141f3)\
  2021-03-08 14:53:54 +0100
  * update wsrep service version after 7345d371418
* [Revision #7345d37141](https://github.com/MariaDB/server/commit/7345d37141)\
  2021-03-08 05:03:06 +0100
  * [MDEV-24853](https://jira.mariadb.org/browse/MDEV-24853): Duplicate key generated during cluster configuration change
* [Revision #dbe941e06f](https://github.com/MariaDB/server/commit/dbe941e06f)\
  2021-03-17 10:03:06 +0300
  * cleanup: os\_thread\_create -> std::thread
* [Revision #da3428805e](https://github.com/MariaDB/server/commit/da3428805e)\
  2021-03-16 23:34:55 +0300
  * cleanup: os\_thread\_yield() -> std::this\_thread::yield()
* [Revision #62e4aaa240](https://github.com/MariaDB/server/commit/62e4aaa240)\
  2021-03-16 16:09:41 +0300
  * cleanup: os\_thread\_sleep() -> std::this\_thread::sleep\_for()
* [Revision #40fd42f7f5](https://github.com/MariaDB/server/commit/40fd42f7f5)\
  2021-03-18 22:41:45 +0100
  * [MDEV-25193](https://jira.mariadb.org/browse/MDEV-25193) - remove attempt to tame Aria.
* [Revision #de91ece1d5](https://github.com/MariaDB/server/commit/de91ece1d5)\
  2021-03-18 22:36:58 +0100
  * [MDEV-25193](https://jira.mariadb.org/browse/MDEV-25193) - temporarily switch storage engine to MyISAM for sys.sys\_config
* [Revision #2b3fd5dff0](https://github.com/MariaDB/server/commit/2b3fd5dff0)\
  2021-03-18 21:04:33 +0300
  * [MDEV-23677](https://jira.mariadb.org/browse/MDEV-23677): Optimizer trace: remove "no predicate for first keypart" (not)
* [Revision #4903031baa](https://github.com/MariaDB/server/commit/4903031baa)\
  2021-03-18 17:05:31 +0200
  * [MDEV-23497](https://jira.mariadb.org/browse/MDEV-23497) fixup: Do not warn for ALTER TABLE conversion
* [Revision #e0c3b5f9a5](https://github.com/MariaDB/server/commit/e0c3b5f9a5)\
  2021-03-18 16:28:09 +0200
  * [MDEV-24883](https://jira.mariadb.org/browse/MDEV-24883) fixup: Avoid io\_uring in ./mtr --rr
* [Revision #8d1098a565](https://github.com/MariaDB/server/commit/8d1098a565)\
  2021-03-18 16:22:51 +0200
  * fixup 7627bfa0a1fd7d44b8564c10cfbcefb4efb7fe07
* [Revision #7627bfa0a1](https://github.com/MariaDB/server/commit/7627bfa0a1)\
  2021-03-18 15:09:07 +0100
  * [MDEV-9077](https://jira.mariadb.org/browse/MDEV-9077) - rerecord test result
* Merge [Revision #ccfbeafc45](https://github.com/MariaDB/server/commit/ccfbeafc45) 2021-03-18 15:46:28 +0200 - Merge 10.5 into 10.6
* Merge [Revision #190a8312f5](https://github.com/MariaDB/server/commit/190a8312f5) 2021-03-18 15:07:01 +0200 - Merge 10.4 into 10.5
* [Revision #126725421e](https://github.com/MariaDB/server/commit/126725421e)\
  2021-03-18 14:43:08 +0200
  * [MDEV-25121](https://jira.mariadb.org/browse/MDEV-25121): innodb\_flush\_method=O\_DIRECT fails on compressed tables
* Merge [Revision #39c015b77e](https://github.com/MariaDB/server/commit/39c015b77e) 2021-03-18 14:17:58 +0200 - Merge 10.3 into 10.4
* [Revision #eb7c5530ec](https://github.com/MariaDB/server/commit/eb7c5530ec)\
  2021-03-06 05:55:14 +0530
  * [MDEV-24730](https://jira.mariadb.org/browse/MDEV-24730) Insert log operation fails after purge resets n\_core\_fields
* [Revision #5511c21b41](https://github.com/MariaDB/server/commit/5511c21b41)\
  2021-03-16 13:13:50 +0200
  * [MDEV-23851](https://jira.mariadb.org/browse/MDEV-23851) BF-BF Conflict issue because of UK GAP locks
* [Revision #f4e4bff992](https://github.com/MariaDB/server/commit/f4e4bff992)\
  2021-03-16 13:02:44 +0200
  * [MDEV-24916](https://jira.mariadb.org/browse/MDEV-24916) : Assertion \`current\_stmt\_binlog\_format == BINLOG\_FORMAT\_STMT || current\_stmt\_binlog\_format == BINLOG\_FORMAT\_ROW' failed in THD::is\_current\_stmt\_binlog\_format\_row
* [Revision #5dbea46cfd](https://github.com/MariaDB/server/commit/5dbea46cfd)\
  2021-03-16 15:37:14 +1100
  * crc32c: Fix AIX compulation - ALIGN defined
* [Revision #60d1461a28](https://github.com/MariaDB/server/commit/60d1461a28)\
  2021-02-26 16:22:24 +0100
  * CRC32 on AIX
* [Revision #9c7bd4f283](https://github.com/MariaDB/server/commit/9c7bd4f283)\
  2021-03-17 16:51:56 +0300
  * [MDEV-25069](https://jira.mariadb.org/browse/MDEV-25069): Assertion \`root->weight >= ...' failed in SEL\_ARG::tree\_delete #2
* [Revision #7e3806ce24](https://github.com/MariaDB/server/commit/7e3806ce24)\
  2020-12-21 20:42:26 +0200
  * Deb: Sync updates to debconf templates and translations from downstream
* [Revision #bac931303d](https://github.com/MariaDB/server/commit/bac931303d)\
  2020-12-20 23:00:00 +0200
  * Deb: Add Finnish and Vietnamese debconf translations
* [Revision #7887d45352](https://github.com/MariaDB/server/commit/7887d45352)\
  2021-03-18 14:13:10 +0100
  * [MDEV-9077](https://jira.mariadb.org/browse/MDEV-9077) - fix README.md
* [Revision #fce1a53d55](https://github.com/MariaDB/server/commit/fce1a53d55)\
  2021-03-09 17:17:03 +0100
  * [MDEV-9077](https://jira.mariadb.org/browse/MDEV-9077) sys schema . use 'mariadb.sys'@'localhost' as definer for views
* [Revision #5ce22bac07](https://github.com/MariaDB/server/commit/5ce22bac07)\
  2021-03-03 10:35:25 +0100
  * [MDEV-9077](https://jira.mariadb.org/browse/MDEV-9077) - sysschema test suite.
* [Revision #f6bb1c117e](https://github.com/MariaDB/server/commit/f6bb1c117e)\
  2021-03-03 10:34:28 +0100
  * [MDEV-9077](https://jira.mariadb.org/browse/MDEV-9077) - do not dump sys schema by default (MySQL bug#76735)
* [Revision #aa2ff62082](https://github.com/MariaDB/server/commit/aa2ff62082)\
  2021-03-03 10:30:29 +0100
  * [MDEV-9077](https://jira.mariadb.org/browse/MDEV-9077) Use sys schema in bootstrapping, incl. mtr
* [Revision #9186ff88da](https://github.com/MariaDB/server/commit/9186ff88da)\
  2021-03-03 10:24:16 +0100
  * [MDEV-9077](https://jira.mariadb.org/browse/MDEV-9077) - sys schema preparation - increase MAX\_BOOTSTRAP\_QUERY\_SIZE (sys.schema has SP over 50K large) don't allocate bootstrap query on heap anymore. - support DELIMITER in bootstrap
* [Revision #601c577142](https://github.com/MariaDB/server/commit/601c577142)\
  2021-03-17 23:22:01 +0100
  * [MDEV-9077](https://jira.mariadb.org/browse/MDEV-9077) - port sys schema to MariaDB
* [Revision #4bac804c90](https://github.com/MariaDB/server/commit/4bac804c90)\
  2021-03-17 17:57:11 +0100
  * [MDEV-9077](https://jira.mariadb.org/browse/MDEV-9077) add sys\_schema from [mysql-sys](https://github.com/mysql/mysql-sys)
* [Revision #7c5c6fa65c](https://github.com/MariaDB/server/commit/7c5c6fa65c)\
  2021-03-17 13:17:39 +0200
  * [MDEV-25090](https://jira.mariadb.org/browse/MDEV-25090): Depend on libpmem where available
* [Revision #418381bf99](https://github.com/MariaDB/server/commit/418381bf99)\
  2021-03-10 09:51:42 +0200
  * [MDEV-25090](https://jira.mariadb.org/browse/MDEV-25090): Deb: Use libpmem-dev when available
* Merge [Revision #124b72cb83](https://github.com/MariaDB/server/commit/124b72cb83) 2021-03-17 13:23:06 +0200 - Merge 10.5 into 10.6
* [Revision #dfa6fba959](https://github.com/MariaDB/server/commit/dfa6fba959)\
  2021-03-17 10:35:04 +0100
  * Skip tests that dump thread\_stack, for ASAN
* [Revision #825c0e2abe](https://github.com/MariaDB/server/commit/825c0e2abe)\
  2021-03-16 12:03:41 +0100
  * [MDEV-24601](https://jira.mariadb.org/browse/MDEV-24601): INFORMATION\_SCHEMA doesn't differentiate between column and table-level CHECK constraints
* [Revision #c236f69d95](https://github.com/MariaDB/server/commit/c236f69d95)\
  2021-03-16 20:57:36 +0300
  * Rename IGNORED INDEX tests to match the SQL syntax
* [Revision #707101d377](https://github.com/MariaDB/server/commit/707101d377)\
  2021-03-16 20:53:33 +0300
  * [MDEV-7317](https://jira.mariadb.org/browse/MDEV-7317): Make an index ignorable to the optimizer: more tests
* [Revision #d9c5eb2f33](https://github.com/MariaDB/server/commit/d9c5eb2f33)\
  2021-03-11 03:22:59 +0530
  * [MDEV-25078](https://jira.mariadb.org/browse/MDEV-25078): ALTER INDEX is inconsistent with ADD/DROP/RENAME index
* [Revision #0540e50873](https://github.com/MariaDB/server/commit/0540e50873)\
  2021-03-08 01:20:58 +0530
  * [MDEV-25075](https://jira.mariadb.org/browse/MDEV-25075): Ignorable index makes the resulting CREATE TABLE invalid
* [Revision #a4d3e04659](https://github.com/MariaDB/server/commit/a4d3e04659)\
  2021-03-16 16:40:08 +0300
  * [MDEV-24883](https://jira.mariadb.org/browse/MDEV-24883) follow up: unset variables in CMake
* Merge [Revision #f87a944c79](https://github.com/MariaDB/server/commit/f87a944c79) 2021-03-16 15:51:26 +0200 - Merge 10.5 into 10.6
* [Revision #8cbada87f0](https://github.com/MariaDB/server/commit/8cbada87f0)\
  2021-03-15 16:11:23 +0300
  * [MDEV-24184](https://jira.mariadb.org/browse/MDEV-24184) InnoDB RENAME TABLE recovery failure if names are reused
* [Revision #031b3dfc22](https://github.com/MariaDB/server/commit/031b3dfc22)\
  2021-03-12 08:43:37 +0100
  * [MDEV-25123](https://jira.mariadb.org/browse/MDEV-25123) support MSVC ASAN
* [Revision #8ea923f55b](https://github.com/MariaDB/server/commit/8ea923f55b)\
  2021-03-16 15:21:34 +0200
  * [MDEV-24818](https://jira.mariadb.org/browse/MDEV-24818): Optimize multi-statement INSERT into an empty table
* [Revision #92b2a911e5](https://github.com/MariaDB/server/commit/92b2a911e5)\
  2021-03-11 18:36:09 +0200
  * [MDEV-24818](https://jira.mariadb.org/browse/MDEV-24818) Concurrent use of InnoDB table is impossible until the first transaction is finished
* [Revision #8dd35a2507](https://github.com/MariaDB/server/commit/8dd35a2507)\
  2021-03-15 20:19:04 +0100
  * update libmariadb
* [Revision #2f53ad4b7d](https://github.com/MariaDB/server/commit/2f53ad4b7d)\
  2021-03-15 12:36:30 +0100
  * update libmariadb
* [Revision #a0558b8c96](https://github.com/MariaDB/server/commit/a0558b8c96)\
  2021-03-15 12:11:29 +0200
  * [MDEV-24883](https://jira.mariadb.org/browse/MDEV-24883) fixup: Add a dependency
* [Revision #211e9b3e0a](https://github.com/MariaDB/server/commit/211e9b3e0a)\
  2021-03-15 11:33:15 +0200
  * [MDEV-24927](https://jira.mariadb.org/browse/MDEV-24927): Deb: Use liburing-dev instead of libaio-dev
* [Revision #783625d78f](https://github.com/MariaDB/server/commit/783625d78f)\
  2021-03-15 11:30:17 +0200
  * [MDEV-24883](https://jira.mariadb.org/browse/MDEV-24883) add io\_uring support for tpool
* [Revision #3dfda08702](https://github.com/MariaDB/server/commit/3dfda08702)\
  2021-03-12 14:09:39 +0200
  * [MDEV-21212](https://jira.mariadb.org/browse/MDEV-21212) fixup: GCC -Wclass-memaccess
* [Revision #8d4e3ec2f7](https://github.com/MariaDB/server/commit/8d4e3ec2f7)\
  2021-03-06 12:49:33 +0800
  * [MDEV-21212](https://jira.mariadb.org/browse/MDEV-21212): buf\_page\_get\_gen -> buf\_pool->stat.n\_page\_gets++ is a cpu waste
* Merge [Revision #4984449956](https://github.com/MariaDB/server/commit/4984449956) 2021-03-12 08:36:26 +0200 - Merge 10.5 into 10.6
* [Revision #4c2b6be38e](https://github.com/MariaDB/server/commit/4c2b6be38e)\
  2021-03-11 21:43:43 +0200
  * One more try: Fix -Wconversion on GCC 4 to 9
* Merge [Revision #64f89b1f60](https://github.com/MariaDB/server/commit/64f89b1f60) 2021-03-11 21:03:59 +0200 - Merge 10.5 into 10.6
* [Revision #abe25c31a6](https://github.com/MariaDB/server/commit/abe25c31a6)\
  2021-03-11 21:02:15 +0200
  * After-merge fix: -Wconversion in GCC 4 to 9
* Merge [Revision #a43ff483fa](https://github.com/MariaDB/server/commit/a43ff483fa) 2021-03-11 20:20:07 +0200 - Merge 10.5 into 10.6
* Merge [Revision #a4b7232b2c](https://github.com/MariaDB/server/commit/a4b7232b2c) 2021-03-11 20:09:34 +0200 - Merge 10.4 into 10.5
* Merge [Revision #1ea6ac3c95](https://github.com/MariaDB/server/commit/1ea6ac3c95) 2021-03-11 19:33:45 +0200 - Merge 10.3 into 10.4
* [Revision #08e8ad7c71](https://github.com/MariaDB/server/commit/08e8ad7c71)\
  2021-03-11 12:50:04 +0200
  * [MDEV-25106](https://jira.mariadb.org/browse/MDEV-25106) Deprecation warning for innodb\_checksum\_algorithm=none,innodb,...
* [Revision #6e7ac4060d](https://github.com/MariaDB/server/commit/6e7ac4060d)\
  2021-03-11 12:34:56 +0200
  * [MDEV-25070](https://jira.mariadb.org/browse/MDEV-25070) fixup: Correct the result
* [Revision #cc9c303a45](https://github.com/MariaDB/server/commit/cc9c303a45)\
  2021-03-10 16:46:42 +0530
  * [MDEV-25070](https://jira.mariadb.org/browse/MDEV-25070) SIGSEGV in fts\_create\_in\_mem\_aux\_table
* [Revision #75f781f0d2](https://github.com/MariaDB/server/commit/75f781f0d2)\
  2021-03-05 17:51:17 +0000
  * [MDEV-24868](https://jira.mariadb.org/browse/MDEV-24868) Server crashes in optimize\_schema\_tables\_memory\_usage after select from information\_schema.innodb\_sys\_columns
* [Revision #2c3014e8a7](https://github.com/MariaDB/server/commit/2c3014e8a7)\
  2021-03-11 19:14:35 +0200
  * [MDEV-24668](https://jira.mariadb.org/browse/MDEV-24668) fixup: uninitialized return value with Galera
* [Revision #06df0b0dce](https://github.com/MariaDB/server/commit/06df0b0dce)\
  2021-03-11 20:52:30 +0530
  * [MDEV-25107](https://jira.mariadb.org/browse/MDEV-25107) Check TABLE miscalutates the length of column
* [Revision #fa5f60681f](https://github.com/MariaDB/server/commit/fa5f60681f)\
  2020-06-18 01:11:39 +0300
  * [MDEV-20946](https://jira.mariadb.org/browse/MDEV-20946): Hard FTWRL deadlock under user level locks
* [Revision #8f4a3bf07c](https://github.com/MariaDB/server/commit/8f4a3bf07c)\
  2021-03-05 13:35:29 +0530
  * [MDEV-25057](https://jira.mariadb.org/browse/MDEV-25057) Assertion \`n\_fields < dtuple\_get\_n\_fields(entry)' failed in dtuple\_convert\_big\_rec
* [Revision #1dff411e84](https://github.com/MariaDB/server/commit/1dff411e84)\
  2021-03-08 18:54:58 +0000
  * arguments overflow fix proposal. the list is assumed to be implictly null terminated at usage time.
* [Revision #e3a597378e](https://github.com/MariaDB/server/commit/e3a597378e)\
  2021-02-03 19:44:34 +0000
  * mariadb-backup utility, binary path implementation for Mac.
* [Revision #1d762ee8fe](https://github.com/MariaDB/server/commit/1d762ee8fe)\
  2021-03-08 17:51:33 +0200
  * [MDEV-24363](https://jira.mariadb.org/browse/MDEV-24363) (followup fix) mysql.user view should
* [Revision #01a0d739c8](https://github.com/MariaDB/server/commit/01a0d739c8)\
  2021-03-07 01:53:52 +0100
  * [MDEV-24975](https://jira.mariadb.org/browse/MDEV-24975) Server consumes extra 4G memory upon querying INFORMATION\_SCHEMA.OPTIIMIZER\_TRACE
* [Revision #f24038b851](https://github.com/MariaDB/server/commit/f24038b851)\
  2021-03-07 14:06:01 +0100
  * mark Aria allocations for temp tables as MY\_THREAD\_SPECIFIC
* [Revision #9742cf4203](https://github.com/MariaDB/server/commit/9742cf4203)\
  2021-03-06 12:31:02 +0100
  * [MDEV-24668](https://jira.mariadb.org/browse/MDEV-24668) debug assert on SET PASSWORD when binlog fails
* [Revision #cf1ca57e75](https://github.com/MariaDB/server/commit/cf1ca57e75)\
  2021-03-06 12:18:48 +0100
  * cleanup: renames, no need to create a new .inc file
* [Revision #44b85406b8](https://github.com/MariaDB/server/commit/44b85406b8)\
  2021-03-05 11:11:13 +0200
  * [MDEV-24363](https://jira.mariadb.org/browse/MDEV-24363) (followup refactor) avoid listing mysql.user
* [Revision #363ba10784](https://github.com/MariaDB/server/commit/363ba10784)\
  2021-02-02 14:57:16 +0200
  * [MDEV-24363](https://jira.mariadb.org/browse/MDEV-24363) mysql.user password\_expired column is incorrect
* [Revision #a8650b64ed](https://github.com/MariaDB/server/commit/a8650b64ed)\
  2021-03-10 19:33:09 +0200
  * [MDEV-25110](https://jira.mariadb.org/browse/MDEV-25110) \[FATAL] InnoDB: Trying to write ... outside the bounds
* [Revision #549a70d7f0](https://github.com/MariaDB/server/commit/549a70d7f0)\
  2021-03-09 18:03:31 +0200
  * [MDEV-25031](https://jira.mariadb.org/browse/MDEV-25031) Not applying INSERT\_\*\_REDUNDANT due to corruption on page
* [Revision #a6cd4612a9](https://github.com/MariaDB/server/commit/a6cd4612a9)\
  2021-03-10 16:02:55 +0000
  * connect storage, little compile issues fix proposal.
* [Revision #f11b60879b](https://github.com/MariaDB/server/commit/f11b60879b)\
  2021-02-23 16:21:30 +0800
  * [MDEV-24949](https://jira.mariadb.org/browse/MDEV-24949): Enabling idle flushing (possible regression from [MDEV-23855](https://jira.mariadb.org/browse/MDEV-23855))
* [Revision #1799caa3a1](https://github.com/MariaDB/server/commit/1799caa3a1)\
  2021-03-10 17:27:01 +0200
  * [MDEV-24422](https://jira.mariadb.org/browse/MDEV-24422) Server crashes in ha\_connect::GetRealType upon ALTER TABLE
* [Revision #322129dfb4](https://github.com/MariaDB/server/commit/322129dfb4)\
  2021-03-10 10:31:22 +0200
  * Skip mysql\_json\_mysql\_upgrade if plugin is not built
* [Revision #bba6c38630](https://github.com/MariaDB/server/commit/bba6c38630)\
  2021-03-09 11:27:47 +0200
  * Deb: Sync downstream changes upstream
* [Revision #baddbaa0e3](https://github.com/MariaDB/server/commit/baddbaa0e3)\
  2021-03-09 11:44:29 +0100
  * fixup 449871458b49f224b27b26858784ef5408353f1b
* [Revision #449871458b](https://github.com/MariaDB/server/commit/449871458b)\
  2021-03-08 18:00:55 +0100
  * Fix Windows clang build with newest cmake
* [Revision #7a4fbb55b0](https://github.com/MariaDB/server/commit/7a4fbb55b0)\
  2021-03-11 11:56:35 +0200
  * [MDEV-25105](https://jira.mariadb.org/browse/MDEV-25105) Remove innodb\_checksum\_algorithm values none,innodb,...
* [Revision #0da6d67a3a](https://github.com/MariaDB/server/commit/0da6d67a3a)\
  2021-03-11 10:21:52 +0200
  * Deb: Rename mariadb.init 10.5->10.6 on 10.6 branch
* [Revision #f386fdd70e](https://github.com/MariaDB/server/commit/f386fdd70e)\
  2021-03-11 09:50:29 +0800
  * Fix several typos in sql/item\_jsonfunc.cc
* [Revision #bda8a2a63a](https://github.com/MariaDB/server/commit/bda8a2a63a)\
  2021-03-09 08:58:28 +0200
  * [MDEV-24671](https://jira.mariadb.org/browse/MDEV-24671) fixup: Merge lock\_sys\_t::wait\_pending into wait\_count
* [Revision #78284a4c11](https://github.com/MariaDB/server/commit/78284a4c11)\
  2021-03-09 08:29:38 +0200
  * [MDEV-25085](https://jira.mariadb.org/browse/MDEV-25085): Simplify instrumentation for LRU eviction
* [Revision #d317350a76](https://github.com/MariaDB/server/commit/d317350a76)\
  2021-01-31 19:41:29 +0600
  * Remove trailing newline from error message in dlerror() on Windows
* [Revision #37546842a9](https://github.com/MariaDB/server/commit/37546842a9)\
  2021-02-24 22:37:53 +0530
  * [MDEV-24963](https://jira.mariadb.org/browse/MDEV-24963): Document `flush-ssl` in the mysqladmin manpage.
* [Revision #563aef8050](https://github.com/MariaDB/server/commit/563aef8050)\
  2021-03-06 16:03:10 +0900
  * Update sql\_table.cc
* Merge [Revision #b930a1900e](https://github.com/MariaDB/server/commit/b930a1900e) 2021-03-08 11:40:21 +0200 - Merge 10.5 into 10.6
* [Revision #d2ddf82a0e](https://github.com/MariaDB/server/commit/d2ddf82a0e)\
  2021-03-08 11:39:09 +0200
  * After-merge fix: GCC -Wconversion
* Merge [Revision #d346763479](https://github.com/MariaDB/server/commit/d346763479) 2021-03-08 10:51:31 +0200 - Merge 10.5 into 10.6
* Merge [Revision #a5d3c1c819](https://github.com/MariaDB/server/commit/a5d3c1c819) 2021-03-08 10:16:20 +0200 - Merge 10.4 into 10.5
* Merge [Revision #a26e7a3726](https://github.com/MariaDB/server/commit/a26e7a3726) 2021-03-08 09:39:54 +0200 - Merge 10.3 into 10.4
* [Revision #ecc1cd219d](https://github.com/MariaDB/server/commit/ecc1cd219d)\
  2021-03-05 14:12:35 +0200
  * Fixed that unit.pcre\_test works again.
* Merge [Revision #bcd160753c](https://github.com/MariaDB/server/commit/bcd160753c) 2021-03-05 10:06:42 +0200 - Merge 10.2 into 10.3
* [Revision #545cba13eb](https://github.com/MariaDB/server/commit/545cba13eb)\
  2021-03-04 23:09:22 +0100
  * [MDEV-22929](https://jira.mariadb.org/browse/MDEV-22929) fixup. Print "completed OK!" if page corruption and --log-innodb-page-corruption
* [Revision #7759991a06](https://github.com/MariaDB/server/commit/7759991a06)\
  2021-03-04 18:11:25 +0200
  * fixup 58b56f14a096285a0e51b2233fc35398f1b01f5a: Remove dead code
* [Revision #978e48c96c](https://github.com/MariaDB/server/commit/978e48c96c)\
  2021-03-04 17:15:38 +0200
  * [MDEV-25051](https://jira.mariadb.org/browse/MDEV-25051) Race condition between persistent statistics and RENAME TABLE or TRUNCATE
* Merge [Revision #e9b8b76f47](https://github.com/MariaDB/server/commit/e9b8b76f47) 2021-03-04 16:04:30 +0200 - Merge branch '10.2' into 10.3
* [Revision #5da6ffe227](https://github.com/MariaDB/server/commit/5da6ffe227)\
  2021-03-02 15:37:12 +0200
  * [MDEV-25032](https://jira.mariadb.org/browse/MDEV-25032): Window functions without column references get removed from ORDER BY
* [Revision #b044898b97](https://github.com/MariaDB/server/commit/b044898b97)\
  2021-03-01 21:16:13 +0530
  * [MDEV-24748](https://jira.mariadb.org/browse/MDEV-24748) extern column check missing in btr\_index\_rec\_validate()
* [Revision #f080863501](https://github.com/MariaDB/server/commit/f080863501)\
  2021-03-03 15:37:03 +0530
  * [MDEV-20648](https://jira.mariadb.org/browse/MDEV-20648) InnoDB: Failing assertion: !(\*node)->being\_extended, innodb.log\_data\_file\_size failed in buildbot, assertion \`!space->is\_stopping()'
* Merge [Revision #39e2c95771](https://github.com/MariaDB/server/commit/39e2c95771) 2021-03-08 09:09:31 +0200 - Merge 10.3 into 10.4
* [Revision #08d8bce583](https://github.com/MariaDB/server/commit/08d8bce583)\
  2021-03-03 22:48:39 -0800
  * [MDEV-22786](https://jira.mariadb.org/browse/MDEV-22786) Crashes with nested table value constructors
* Merge [Revision #03ff588d15](https://github.com/MariaDB/server/commit/03ff588d15) 2021-03-05 16:05:47 +0200 - Merge 10.5 into 10.6
* [Revision #f6cb9e6e2d](https://github.com/MariaDB/server/commit/f6cb9e6e2d)\
  2021-03-05 12:59:07 +0200
  * Cleanup: add override qualifiers to item.h
* [Revision #e5e0e519f4](https://github.com/MariaDB/server/commit/e5e0e519f4)\
  2021-03-05 12:55:46 +0200
  * [MDEV-24600](https://jira.mariadb.org/browse/MDEV-24600) fixup: Remove unused trx\_register\_for\_2pc()
* Merge [Revision #10d544aa7b](https://github.com/MariaDB/server/commit/10d544aa7b) 2021-03-05 12:54:43 +0200 - Merge 10.4 into 10.5
* [Revision #fcc9f8b10c](https://github.com/MariaDB/server/commit/fcc9f8b10c)\
  2021-03-05 10:40:16 +0200
  * Remove unused HA\_EXTRA\_FAKE\_START\_STMT
* Merge [Revision #8bab5bb332](https://github.com/MariaDB/server/commit/8bab5bb332) 2021-03-05 10:36:51 +0200 - Merge 10.3 into 10.4
* [Revision #5bd994b0d5](https://github.com/MariaDB/server/commit/5bd994b0d5)\
  2021-03-03 10:13:56 +0200
  * [MDEV-24811](https://jira.mariadb.org/browse/MDEV-24811) Assertion find(table) failed with innodb\_evict\_tables\_on\_commit\_debug
* Merge [Revision #ddbc612692](https://github.com/MariaDB/server/commit/ddbc612692) 2021-03-03 09:41:50 +0200 - Merge 10.2 into 10.3
* [Revision #676987c4a1](https://github.com/MariaDB/server/commit/676987c4a1)\
  2021-03-02 14:08:38 +0200
  * [MDEV-24532](https://jira.mariadb.org/browse/MDEV-24532) Table corruption ER\_NO\_SUCH\_TABLE\_IN\_ENGINE .. on table with foreign key
* [Revision #fc77431624](https://github.com/MariaDB/server/commit/fc77431624)\
  2021-03-02 19:09:44 +0700
  * [MDEV-25006](https://jira.mariadb.org/browse/MDEV-25006): Failed assertion on executing EXPLAIN DELETE statement as a prepared statement
* [Revision #dd9e5827a6](https://github.com/MariaDB/server/commit/dd9e5827a6)\
  2021-02-25 14:10:25 +0100
  * mtr --gdb: fix for --rr and for a warning
* [Revision #259e5243fa](https://github.com/MariaDB/server/commit/259e5243fa)\
  2021-02-25 14:20:11 +0700
  * [MDEV-24860](https://jira.mariadb.org/browse/MDEV-24860): Incorrect behaviour of SET STATEMENT in case it is executed as a prepared statement
* [Revision #0f81ca6a0b](https://github.com/MariaDB/server/commit/0f81ca6a0b)\
  2021-03-01 09:40:33 -0800
  * [MDEV-24919](https://jira.mariadb.org/browse/MDEV-24919) Crash with subselect formed by table value constructor and used in set function
* [Revision #c25e6f91da](https://github.com/MariaDB/server/commit/c25e6f91da)\
  2021-03-01 22:08:47 +0200
  * Fixed typo in comment
* [Revision #3f15d3bad9](https://github.com/MariaDB/server/commit/3f15d3bad9)\
  2021-03-01 17:51:44 +0200
  * Fixed unit test to not 'bail out' if some tests are not compiled.
* [Revision #415409579a](https://github.com/MariaDB/server/commit/415409579a)\
  2021-03-01 14:44:18 +0200
  * [MDEV-24958](https://jira.mariadb.org/browse/MDEV-24958) Server crashes in my\_strtod ... with DEFAULT(blob)
* [Revision #6983ce704b](https://github.com/MariaDB/server/commit/6983ce704b)\
  2021-02-27 19:56:46 +0200
  * [MDEV-24710](https://jira.mariadb.org/browse/MDEV-24710) Uninitialized value upon CREATE .. SELECT ... VALUE...
* [Revision #43a0a81397](https://github.com/MariaDB/server/commit/43a0a81397)\
  2021-02-27 19:42:43 +0200
  * Fixed printing of wring filname "maria\_open" in maria.maria-recovery2.test
* [Revision #a18b39e3f4](https://github.com/MariaDB/server/commit/a18b39e3f4)\
  2021-03-01 20:08:14 +0400
  * [MDEV-24965](https://jira.mariadb.org/browse/MDEV-24965) With ALTER USER ...IDENTIFIED BY command, password doesn't replaced by asterisks in audit log.
* [Revision #25ecf8ed4b](https://github.com/MariaDB/server/commit/25ecf8ed4b)\
  2021-02-26 13:26:00 +0400
  * [MDEV-24965](https://jira.mariadb.org/browse/MDEV-24965) With ALTER USER ...IDENTIFIED BY command, password doesn't replaced by asterisks in audit log.
* [Revision #1d80e8e4f3](https://github.com/MariaDB/server/commit/1d80e8e4f3)\
  2021-02-25 11:55:08 +0200
  * MENT-1098 Crash during update on 10.4.17 after upgrade from 10.4.10
* [Revision #82efe4a15a](https://github.com/MariaDB/server/commit/82efe4a15a)\
  2021-03-02 14:13:39 +0200
  * [MDEV-23843](https://jira.mariadb.org/browse/MDEV-23843) Assertions in Diagnostics\_area upon table operations under FTWRL
* [Revision #aa4f76bed7](https://github.com/MariaDB/server/commit/aa4f76bed7)\
  2021-03-01 23:07:12 +0530
  * [MDEV-25018](https://jira.mariadb.org/browse/MDEV-25018) \[FATAL] InnoDB: Unable to read page (of a dropped tablespace)
* [Revision #33cf577ad8](https://github.com/MariaDB/server/commit/33cf577ad8)\
  2021-03-03 20:07:13 +0800
  * [MDEV-25029](https://jira.mariadb.org/browse/MDEV-25029): Reduce dict\_sys mutex contention for read-only workload
* [Revision #7947c549aa](https://github.com/MariaDB/server/commit/7947c549aa)\
  2021-03-05 13:04:42 +1100
  * [MDEV-6536](https://jira.mariadb.org/browse/MDEV-6536): mtr main.bind\_address\_resolution
* [Revision #6b8a896837](https://github.com/MariaDB/server/commit/6b8a896837)\
  2021-03-05 11:29:28 +1100
  * [MDEV-6536](https://jira.mariadb.org/browse/MDEV-6536): postfix win32 handle\_connections\_win type fix
* [Revision #1e7fed721b](https://github.com/MariaDB/server/commit/1e7fed721b)\
  2021-03-04 12:12:24 +1100
  * mtr: perfschema.socket\_{connect,instances\_func} "Expect X"
* [Revision #d2dce1c945](https://github.com/MariaDB/server/commit/d2dce1c945)\
  2021-03-04 11:19:26 +1100
  * [MDEV-6536](https://jira.mariadb.org/browse/MDEV-6536): galera IPv6 tests to connect using IPv6
* [Revision #b3abcf80a1](https://github.com/MariaDB/server/commit/b3abcf80a1)\
  2020-09-10 03:39:20 +0300
  * [MDEV-6536](https://jira.mariadb.org/browse/MDEV-6536): make --bind=hostname to listen on both IPv6 and IPv4 addresses
* [Revision #f691d9865b](https://github.com/MariaDB/server/commit/f691d9865b)\
  2021-02-25 19:59:51 +0530
  * [MDEV-7317](https://jira.mariadb.org/browse/MDEV-7317): Make an index ignorable to the optimizer
* Merge [Revision #71d30d01aa](https://github.com/MariaDB/server/commit/71d30d01aa) 2021-03-03 13:55:43 +0200 - Merge 10.5 into 10.6
* [Revision #4b166ca901](https://github.com/MariaDB/server/commit/4b166ca901)\
  2021-02-25 20:51:30 +0530
  * [MDEV-24863](https://jira.mariadb.org/browse/MDEV-24863) AHI entries mismatch with the index while reloading the evicted tables.
* [Revision #1c7d4f8de7](https://github.com/MariaDB/server/commit/1c7d4f8de7)\
  2021-03-03 13:49:49 +0200
  * [MDEV-25016](https://jira.mariadb.org/browse/MDEV-25016) Race condition between lock\_sys\_t::cancel() and page split or merge
* [Revision #80ac9ec1cc](https://github.com/MariaDB/server/commit/80ac9ec1cc)\
  2021-03-02 14:32:37 +0200
  * [MDEV-24973](https://jira.mariadb.org/browse/MDEV-24973) Performance schema duplicates rarely executed code for mutex operations
* Merge [Revision #33aec68a87](https://github.com/MariaDB/server/commit/33aec68a87) 2021-03-02 14:30:50 +0200 - Merge 10.5 into 10.6
* [Revision #01b44c054d](https://github.com/MariaDB/server/commit/01b44c054d)\
  2021-03-02 11:51:22 +0200
  * [MDEV-25026](https://jira.mariadb.org/browse/MDEV-25026) Various code paths are accessing freed pages
* [Revision #1f1f61a9de](https://github.com/MariaDB/server/commit/1f1f61a9de)\
  2021-03-01 16:53:09 +0100
  * [MDEV-24858](https://jira.mariadb.org/browse/MDEV-24858) SIGABRT in DbugExit from my\_malloc in Query\_cache::init\_cache Regression
* [Revision #6976bb94b4](https://github.com/MariaDB/server/commit/6976bb94b4)\
  2021-02-20 15:13:12 +0000
  * [MDEV-24858](https://jira.mariadb.org/browse/MDEV-24858) SIGABRT in DbugExit from my\_malloc in Query\_cache::init\_cache Regression
* [Revision #8d714db622](https://github.com/MariaDB/server/commit/8d714db622)\
  2021-02-26 19:02:26 +0530
  * [MDEV-24997](https://jira.mariadb.org/browse/MDEV-24997) Assertion mtr->is\_named\_space(page\_id.space()) in ibuf0ibuf.cc:624
* [Revision #18535a4028](https://github.com/MariaDB/server/commit/18535a4028)\
  2021-03-01 16:26:45 +0200
  * [MDEV-24811](https://jira.mariadb.org/browse/MDEV-24811) Assertion find(table) failed with innodb\_evict\_tables\_on\_commit\_debug
* [Revision #8513007c84](https://github.com/MariaDB/server/commit/8513007c84)\
  2021-03-01 15:14:25 +0200
  * Cleanup: Remove some lock accessor functions
* [Revision #8d16da1487](https://github.com/MariaDB/server/commit/8d16da1487)\
  2021-02-28 13:46:16 +0200
  * [MDEV-24789](https://jira.mariadb.org/browse/MDEV-24789): Reduce lock\_sys mutex contention further
* [Revision #ebb2db5912](https://github.com/MariaDB/server/commit/ebb2db5912)\
  2021-03-01 15:21:31 +0200
  * [MDEV-20715](https://jira.mariadb.org/browse/MDEV-20715) : Implement system variable to disallow local GTIDs in Galera
* Merge [Revision #b47304eb02](https://github.com/MariaDB/server/commit/b47304eb02) 2021-02-26 15:02:13 +0200 - Merge 10.5 into 10.6
* Merge [Revision #1696e4df3f](https://github.com/MariaDB/server/commit/1696e4df3f) 2021-02-26 13:25:04 +1100 - Merge remote-tracking branch 10.4 into 10.5
* Merge [Revision #a6c6c4f463](https://github.com/MariaDB/server/commit/a6c6c4f463) 2021-02-25 12:31:26 +0200 - Merge 10.3 into 10.4
* Merge [Revision #4473d17430](https://github.com/MariaDB/server/commit/4473d17430) 2021-02-25 12:19:11 +0200 - Merge 10.2 into 10.3
* [Revision #0a95c922c8](https://github.com/MariaDB/server/commit/0a95c922c8)\
  2021-02-25 12:42:01 +0530
  * Fixed the innodb\_ext\_key test by adding replace\_column
* Merge [Revision #86d60fc9e7](https://github.com/MariaDB/server/commit/86d60fc9e7) 2021-02-25 20:05:35 +1100 - Merge remote-tracking branch 'origin/10.4' into 10.5
* Merge [Revision #ef96ec3b51](https://github.com/MariaDB/server/commit/ef96ec3b51) 2021-02-25 15:46:32 +1100 - Merge branch '10.3' into 10.4
* [Revision #48b5f8a544](https://github.com/MariaDB/server/commit/48b5f8a544)\
  2021-02-25 15:44:45 +1100
  * mysys: lf\_hash - fix l\_search size\_t keylen
* Merge [Revision #36810342d5](https://github.com/MariaDB/server/commit/36810342d5) 2021-02-25 13:16:10 +1100 - Merge branch '10.3' into 10.4
* Merge [Revision #3e2afcb3f4](https://github.com/MariaDB/server/commit/3e2afcb3f4) 2021-02-25 12:16:13 +1100 - Merge remote-tracking branch 'origin/10.2' into 10.3
* [Revision #577c970c52](https://github.com/MariaDB/server/commit/577c970c52)\
  2021-01-29 09:37:22 +1100
  * [MDEV-24728](https://jira.mariadb.org/browse/MDEV-24728): Debian include client caching\_sha2\_password plugin
* [Revision #1635686b50](https://github.com/MariaDB/server/commit/1635686b50)\
  2021-02-15 12:31:31 +1100
  * [MDEV-23510](https://jira.mariadb.org/browse/MDEV-23510): arm64 lf\_hash alignment of pointers
* [Revision #bf6484e7bb](https://github.com/MariaDB/server/commit/bf6484e7bb)\
  2021-02-24 13:51:47 -0800
  * [MDEV-24910](https://jira.mariadb.org/browse/MDEV-24910) Crash with SELECT that uses table value constructor as a subselect
* [Revision #d1eeb4b839](https://github.com/MariaDB/server/commit/d1eeb4b839)\
  2021-02-24 12:02:54 +0200
  * [MDEV-24964](https://jira.mariadb.org/browse/MDEV-24964) : Heap-buffer-overflow on wsrep\_schema.cc ::remove\_fragments
* [Revision #f2428b9c24](https://github.com/MariaDB/server/commit/f2428b9c24)\
  2021-02-24 13:30:35 +0200
  * [MDEV-24967](https://jira.mariadb.org/browse/MDEV-24967) : Signal 11 on ha\_innodb.cc::bg\_wsrep\_kill\_trx line 18611
* [Revision #2628fa2dba](https://github.com/MariaDB/server/commit/2628fa2dba)\
  2021-02-05 12:52:48 +1100
  * [MDEV-20857](https://jira.mariadb.org/browse/MDEV-20857): perf schema conflict name filename\_hash
* [Revision #e0ba68ba34](https://github.com/MariaDB/server/commit/e0ba68ba34)\
  2021-02-15 12:31:31 +1100
  * [MDEV-23510](https://jira.mariadb.org/browse/MDEV-23510): arm64 lf\_hash alignment of pointers
* [Revision #cea03285ec](https://github.com/MariaDB/server/commit/cea03285ec)\
  2021-02-24 13:30:35 +0200
  * [MDEV-24967](https://jira.mariadb.org/browse/MDEV-24967) : Signal 11 on ha\_innodb.cc::bg\_wsrep\_kill\_trx line 18611
* [Revision #f83e2ecc50](https://github.com/MariaDB/server/commit/f83e2ecc50)\
  2021-02-23 23:38:57 +0300
  * [MDEV-24953](https://jira.mariadb.org/browse/MDEV-24953): 10.5.9 crashes with large IN() list
* [Revision #7cf4419fc4](https://github.com/MariaDB/server/commit/7cf4419fc4)\
  2021-02-26 14:52:51 +0200
  * [MDEV-24789](https://jira.mariadb.org/browse/MDEV-24789): Reduce lock\_sys.wait\_mutex contention
* [Revision #d9898c9a71](https://github.com/MariaDB/server/commit/d9898c9a71)\
  2021-02-21 09:30:20 +0000
  * [MDEV-7409](https://jira.mariadb.org/browse/MDEV-7409) On RBR, extend the PROCESSLIST info to include at least the name of the recently used table
* [Revision #27d66d644c](https://github.com/MariaDB/server/commit/27d66d644c)\
  2020-11-03 10:44:26 +0200
  * MENT-411 : Implement wsrep\_replicate\_aria
* [Revision #74281fe1fb](https://github.com/MariaDB/server/commit/74281fe1fb)\
  2021-02-24 15:52:55 +0200
  * [MDEV-24884](https://jira.mariadb.org/browse/MDEV-24884) fixup: Remove a bogus assertion
* [Revision #5c9229b96f](https://github.com/MariaDB/server/commit/5c9229b96f)\
  2021-02-24 15:49:58 +0200
  * [MDEV-24951](https://jira.mariadb.org/browse/MDEV-24951) Assertion m.first->second.valid(trx->undo\_no) failed
* [Revision #21987e5919](https://github.com/MariaDB/server/commit/21987e5919)\
  2021-02-22 18:32:51 +0200
  * [MDEV-20612](https://jira.mariadb.org/browse/MDEV-20612) fixup: Reduce hash table lookups
* Merge [Revision #7953bae22a](https://github.com/MariaDB/server/commit/7953bae22a) 2021-02-24 09:30:17 +0200 - Merge 10.5 into 10.6
* Merge [Revision #f159061510](https://github.com/MariaDB/server/commit/f159061510) 2021-02-24 08:54:44 +0200 - Merge 10.4 into 10.5
* Merge [Revision #ad0f0d2b1a](https://github.com/MariaDB/server/commit/ad0f0d2b1a) 2021-02-23 21:44:22 +0200 - Merge branch '10.3' into 10.4
* Merge [Revision #13f0e1e139](https://github.com/MariaDB/server/commit/13f0e1e139) 2021-02-23 21:43:05 +0200 - Merge branch '10.2' into 10.3
* [Revision #9e259d58c2](https://github.com/MariaDB/server/commit/9e259d58c2)\
  2021-02-18 15:30:03 +0200
  * Remove race condition during `make dist`
* Merge [Revision #3c9d03edda](https://github.com/MariaDB/server/commit/3c9d03edda) 2021-02-23 14:11:08 +0200 - Merge 10.3 into 10.4
* Merge [Revision #69bf55ffb6](https://github.com/MariaDB/server/commit/69bf55ffb6) 2021-02-23 10:56:00 +0200 - Merge 10.2 into 10.3
* [Revision #787c47586e](https://github.com/MariaDB/server/commit/787c47586e)\
  2021-02-23 13:55:39 +0530
  * [MDEV-24913](https://jira.mariadb.org/browse/MDEV-24913) Assertion !recv\_no\_log\_write in log\_write\_up\_to()
* Merge [Revision #f33e57a9e6](https://github.com/MariaDB/server/commit/f33e57a9e6) 2021-02-23 13:01:27 +0100 - Merge branch '10.4' into 10.5
* Merge [Revision #245d33db4e](https://github.com/MariaDB/server/commit/245d33db4e) 2021-02-23 10:35:16 +0100 - Merge branch 'github/10.4' into 10.4
* [Revision #8b77e6c676](https://github.com/MariaDB/server/commit/8b77e6c676)\
  2020-12-15 17:39:24 +0200
  * [MDEV-24114](https://jira.mariadb.org/browse/MDEV-24114) SHOW CREATE USER doesnt display correct password expiry status
* Merge [Revision #e841957416](https://github.com/MariaDB/server/commit/e841957416) 2021-02-23 00:56:14 +0100 - Merge branch '10.3' into 10.4
* [Revision #640f42311a](https://github.com/MariaDB/server/commit/640f42311a)\
  2021-02-20 14:46:19 +0200
  * [MDEV-24929](https://jira.mariadb.org/browse/MDEV-24929) Server crash in thr\_multi\_unlock or in get\_schema\_tables\_result
* Merge [Revision #0ab1e3914c](https://github.com/MariaDB/server/commit/0ab1e3914c) 2021-02-22 21:25:16 +0100 - Merge branch '10.2' into 10.3
* [Revision #3c021485c9](https://github.com/MariaDB/server/commit/3c021485c9)\
  2021-02-19 16:54:58 +0100
  * fix binlog\_xa\_recover test
* [Revision #bb98c6bf44](https://github.com/MariaDB/server/commit/bb98c6bf44)\
  2021-02-19 16:48:19 +0100
  * cleanup: renames, no need to create a new .inc file
* [Revision #7fe351aba4](https://github.com/MariaDB/server/commit/7fe351aba4)\
  2021-02-03 16:59:26 +0100
  * mtr fixes for old (5.10.1) perl
* [Revision #77c23c62ae](https://github.com/MariaDB/server/commit/77c23c62ae)\
  2021-01-26 11:56:17 +0100
  * support for mtr --valgdb
* [Revision #feacc0aaf2](https://github.com/MariaDB/server/commit/feacc0aaf2)\
  2021-01-25 13:16:04 +0100
  * unify mtr handling of debuggers
* [Revision #3b0b4e614c](https://github.com/MariaDB/server/commit/3b0b4e614c)\
  2021-01-24 21:57:37 +0100
  * cleanup: remove dead code in mtr
* [Revision #c4f0133444](https://github.com/MariaDB/server/commit/c4f0133444)\
  2021-02-01 13:16:40 +0100
  * cleanup: stat tables
* [Revision #06a791aa12](https://github.com/MariaDB/server/commit/06a791aa12)\
  2021-02-01 13:01:12 +0100
  * [MDEV-23753](https://jira.mariadb.org/browse/MDEV-23753): SIGSEGV in Column\_stat::store\_stat\_fields
* [Revision #caad32ca92](https://github.com/MariaDB/server/commit/caad32ca92)\
  2021-02-01 12:57:14 +0100
  * Revert "[MDEV-23753](https://jira.mariadb.org/browse/MDEV-23753): SIGSEGV in Column\_stat::store\_stat\_fields"
* Merge [Revision #a638f1577a](https://github.com/MariaDB/server/commit/a638f1577a) 2021-02-22 18:43:03 +0100 - Merge branch 'bb-10.2-release' into 10.2
* [Revision #6aa909745d](https://github.com/MariaDB/server/commit/6aa909745d)\
  2021-02-22 10:04:25 -0500
  * bump the VERSION
* [Revision #d7fc4f5236](https://github.com/MariaDB/server/commit/d7fc4f5236)\
  2021-02-22 18:07:15 +0530
  * [MDEV-24863](https://jira.mariadb.org/browse/MDEV-24863) AHI entries mismatch with the index while reloading the evicted tables.
* [Revision #374f4c3f8c](https://github.com/MariaDB/server/commit/374f4c3f8c)\
  2021-02-18 10:09:30 +0200
  * Suppress warning on galera\_ssl\_upgrade test.
* [Revision #5ecaf52d42](https://github.com/MariaDB/server/commit/5ecaf52d42)\
  2021-02-16 12:19:19 +0200
  * [MDEV-24873](https://jira.mariadb.org/browse/MDEV-24873) : galera.galera\_as\_slave\_ctas MTR failed: Assertion \`(&(\&LOCK\_thd\_data)->m\_mutex)->count > 0 && pthread\_equal(pthread\_self(), (&(\&LOCK\_thd\_data)->m\_mutex)->thread)' failed in sql\_class.cc on THD::awake(killed\_state)
* [Revision #45e33e05e2](https://github.com/MariaDB/server/commit/45e33e05e2)\
  2021-02-16 12:05:45 +0200
  * [MDEV-24872](https://jira.mariadb.org/browse/MDEV-24872) : galera.galera\_insert\_multi MTR failed: crash with SIGABRT
* [Revision #4d300ab1a8](https://github.com/MariaDB/server/commit/4d300ab1a8)\
  2021-02-16 11:52:50 +0200
  * [MDEV-24867](https://jira.mariadb.org/browse/MDEV-24867) : wsrep.variables MTR failed: Result length mismatch
* [Revision #067465cd2f](https://github.com/MariaDB/server/commit/067465cd2f)\
  2021-02-16 12:07:48 +0200
  * [MDEV-15641](https://jira.mariadb.org/browse/MDEV-15641) fixup: Make the test faster
* [Revision #3544643f09](https://github.com/MariaDB/server/commit/3544643f09)\
  2021-02-15 16:30:55 +0530
  * [MDEV-23291](https://jira.mariadb.org/browse/MDEV-23291): SUM column from a derived table returns invalid values
* [Revision #7e9a6b7f09](https://github.com/MariaDB/server/commit/7e9a6b7f09)\
  2021-02-15 16:28:44 +0530
  * [MDEV-24779](https://jira.mariadb.org/browse/MDEV-24779): main.subselect fails in buildbot with --ps-protocol
* [Revision #a461e4d306](https://github.com/MariaDB/server/commit/a461e4d306)\
  2021-02-09 20:27:21 +0530
  * [MDEV-19474](https://jira.mariadb.org/browse/MDEV-19474): Histogram statistics are used even with optimizer\_use\_condition\_selectivity=3
* [Revision #e926964cb8](https://github.com/MariaDB/server/commit/e926964cb8)\
  2021-02-15 18:04:17 +0200
  * Remove useless test innodb.innodb\_bug60049
* [Revision #6f14230643](https://github.com/MariaDB/server/commit/6f14230643)\
  2021-02-15 13:41:44 +0100
  * [MDEV-11862](https://jira.mariadb.org/browse/MDEV-11862) rpl.rpl\_semi\_sync\_event\_after\_sync 'fails if there is no semisync plugin
* [Revision #da3211e487](https://github.com/MariaDB/server/commit/da3211e487)\
  2021-02-12 14:03:25 +0200
  * [MDEV-24763](https://jira.mariadb.org/browse/MDEV-24763) fixup: Use deterministic ORDER BY
* [Revision #6f3f191cfa](https://github.com/MariaDB/server/commit/6f3f191cfa)\
  2021-02-12 09:48:36 +0200
  * [MDEV-24763](https://jira.mariadb.org/browse/MDEV-24763) ALTER TABLE fails to rename a column in SYS\_FIELDS
* [Revision #028ba10d0b](https://github.com/MariaDB/server/commit/028ba10d0b)\
  2021-02-12 09:41:15 +0200
  * [MDEV-18468](https://jira.mariadb.org/browse/MDEV-18468) fixup: Make test case robust w.r.t. deferred DROP TABLE
* [Revision #95003eab45](https://github.com/MariaDB/server/commit/95003eab45)\
  2021-02-10 14:04:25 +0100
  * [MDEV-19950](https://jira.mariadb.org/browse/MDEV-19950): Galera test failure on galera\_ssl\_upgrade
* [Revision #362dcf9e01](https://github.com/MariaDB/server/commit/362dcf9e01)\
  2021-02-11 08:02:24 +0200
  * Update Galera disabled.def
* [Revision #afc5bac49d](https://github.com/MariaDB/server/commit/afc5bac49d)\
  2021-02-05 19:50:05 +0400
  * [MDEV-24790](https://jira.mariadb.org/browse/MDEV-24790) CAST('0e1111111111' AS DECIMAL(38,0)) returns a wrong result
* [Revision #739abf5195](https://github.com/MariaDB/server/commit/739abf5195)\
  2021-02-07 14:31:48 +0200
  * Make innodb\_gis.rtree\_purge run faster
* [Revision #eef4c5d378](https://github.com/MariaDB/server/commit/eef4c5d378)\
  2021-01-18 14:00:13 +0530
  * [MDEV-22741](https://jira.mariadb.org/browse/MDEV-22741): \*SAN: ERROR: AddressSanitizer: use-after-poison on address in instrings/strmake.c:36 from change\_master (on optimized builds)
* [Revision #6ede84f477](https://github.com/MariaDB/server/commit/6ede84f477)\
  2021-02-02 10:28:31 +0100
  * [MDEV-24762](https://jira.mariadb.org/browse/MDEV-24762) - HeidiSQL 11.2
* [Revision #ceb3976191](https://github.com/MariaDB/server/commit/ceb3976191)\
  2021-02-01 17:59:38 +0530
  * Updating test results in rocksdb test suite after [MDEV-11172](https://jira.mariadb.org/browse/MDEV-11172) is fixed
* [Revision #26f5033555](https://github.com/MariaDB/server/commit/26f5033555)\
  2021-01-31 19:55:07 +0530
  * [MDEV-23449](https://jira.mariadb.org/browse/MDEV-23449): alias do not exist and a query do not report an error
* [Revision #072b39da66](https://github.com/MariaDB/server/commit/072b39da66)\
  2021-01-30 22:36:51 +0530
  * [MDEV-22583](https://jira.mariadb.org/browse/MDEV-22583): Selectivity for BIT columns in filtered column for EXPLAIN is incorrect
* [Revision #b87c342da5](https://github.com/MariaDB/server/commit/b87c342da5)\
  2021-01-29 00:27:19 +0530
  * [MDEV-11172](https://jira.mariadb.org/browse/MDEV-11172): EXPLAIN shows non-sensical value for key\_len with type=index
* [Revision #0921656734](https://github.com/MariaDB/server/commit/0921656734)\
  2021-01-28 23:29:43 +0200
  * Skip TokuDB within autobake-deb.sh
* [Revision #a4d4836f2b](https://github.com/MariaDB/server/commit/a4d4836f2b)\
  2021-01-29 19:31:07 +0200
  * List of unstable tests for 10.2.37 release
* Merge [Revision #ca126d96f5](https://github.com/MariaDB/server/commit/ca126d96f5) 2021-02-22 19:46:21 +0100 - Merge branch 'bb-10.3-release' into 10.3
* [Revision #a5b18613ec](https://github.com/MariaDB/server/commit/a5b18613ec)\
  2021-02-21 22:01:24 -0800
  * [MDEV-24936](https://jira.mariadb.org/browse/MDEV-24936) EXPLAIN for query based on table value constructor lacks info on used subqueries
* [Revision #a49ce0bf93](https://github.com/MariaDB/server/commit/a49ce0bf93)\
  2021-02-22 09:44:23 -0500
  * bump the VERSION
* [Revision #8db5274dce](https://github.com/MariaDB/server/commit/8db5274dce)\
  2021-02-21 20:38:32 +0200
  * [MDEV-22703](https://jira.mariadb.org/browse/MDEV-22703) DEFAULT() on a BLOB column can overwrite the default record
* [Revision #da88e1ec12](https://github.com/MariaDB/server/commit/da88e1ec12)\
  2021-02-10 23:38:52 -0800
  * [MDEV-24840](https://jira.mariadb.org/browse/MDEV-24840) Crash caused by query with IN subquery containing union of two table value costructors
* Merge [Revision #34fcd726a6](https://github.com/MariaDB/server/commit/34fcd726a6) 2021-02-23 00:08:56 +0100 - Merge branch 'bb-10.4-release' into 10.4
* [Revision #7b8dacc488](https://github.com/MariaDB/server/commit/7b8dacc488)\
  2021-02-22 09:43:28 -0500
  * bump the VERSION
* [Revision #901bcde2dd](https://github.com/MariaDB/server/commit/901bcde2dd)\
  2021-02-16 01:11:41 +0100
  * galera.galera\_gra\_log crashes
* [Revision #a5bcec727b](https://github.com/MariaDB/server/commit/a5bcec727b)\
  2021-02-16 08:46:14 +0200
  * [MDEV-24865](https://jira.mariadb.org/browse/MDEV-24865) : Server crashes when truncate mysql user table
* [Revision #d0defd1ea2](https://github.com/MariaDB/server/commit/d0defd1ea2)\
  2021-02-14 17:43:31 +0200
  * In case of an abort, write "handling fatal signal" to DBUG log.
* [Revision #af31e2c55d](https://github.com/MariaDB/server/commit/af31e2c55d)\
  2021-02-14 17:42:19 +0200
  * [MDEV-23843](https://jira.mariadb.org/browse/MDEV-23843) Assertions in Diagnostics\_area upon table operations under FTWRL
* [Revision #3cd32a9baf](https://github.com/MariaDB/server/commit/3cd32a9baf)\
  2021-02-12 17:56:46 +0200
  * Remove extra (not needed) error from multi-table-update for killed query
* [Revision #23833dce05](https://github.com/MariaDB/server/commit/23833dce05)\
  2021-02-12 11:28:42 +0300
  * [MDEV-24792](https://jira.mariadb.org/browse/MDEV-24792) Assertion \`!newest\_lsn || fil\_page\_get\_type(page)' failed upon mariadb-backup prepare in buf\_flush\_init\_for\_writing with innodb\_log\_optimize\_ddl=off
* [Revision #cb4434c44a](https://github.com/MariaDB/server/commit/cb4434c44a)\
  2021-02-13 10:28:10 +0200
  * [MDEV-24856](https://jira.mariadb.org/browse/MDEV-24856) : Server crashes when wsrep\_provider\_options set to NULL
* [Revision #542d769ea1](https://github.com/MariaDB/server/commit/542d769ea1)\
  2020-11-11 09:22:05 +0100
  * [MDEV-18280](https://jira.mariadb.org/browse/MDEV-18280): Galera test failure on galera\_split\_brain and galera\_kill\_nochanges
* Merge [Revision #1a0526e2f2](https://github.com/MariaDB/server/commit/1a0526e2f2) 2021-02-23 09:27:02 +0100 - Merge branch 'bb-10.5-release' into 10.5
* [Revision #85bec9d691](https://github.com/MariaDB/server/commit/85bec9d691)\
  2021-02-22 09:40:30 -0500
  * bump the VERSION
* [Revision #208233be5a](https://github.com/MariaDB/server/commit/208233be5a)\
  2021-02-10 09:53:37 +0200
  * [MDEV-24830](https://jira.mariadb.org/browse/MDEV-24830) : Write a warning to error log if Galera replicates InnoDB table with no primary key
* [Revision #420f8e24ab](https://github.com/MariaDB/server/commit/420f8e24ab)\
  2021-02-20 11:58:58 +0200
  * [MDEV-24854](https://jira.mariadb.org/browse/MDEV-24854): Change innodb\_flush\_method=O\_DIRECT by default
* [Revision #43b239a081](https://github.com/MariaDB/server/commit/43b239a081)\
  2021-02-18 12:16:51 +0200
  * [MDEV-24915](https://jira.mariadb.org/browse/MDEV-24915) Galera conflict resolution is unnecessarily complex
* [Revision #18dc5b0192](https://github.com/MariaDB/server/commit/18dc5b0192)\
  2021-02-18 12:02:36 +0200
  * [MDEV-20612](https://jira.mariadb.org/browse/MDEV-20612) fixup: Remove a redundant check
* [Revision #9a90786863](https://github.com/MariaDB/server/commit/9a90786863)\
  2021-02-17 16:30:50 +0200
  * [MDEV-24887](https://jira.mariadb.org/browse/MDEV-24887) Tests fail on macos because mysqltest can't use nonblock API
* Merge [Revision #94b4578704](https://github.com/MariaDB/server/commit/94b4578704) 2021-02-17 19:39:05 +0200 - Merge 10.5 into 10.6
* Merge [Revision #16388f393c](https://github.com/MariaDB/server/commit/16388f393c) 2021-02-17 16:19:49 +0200 - Merge mariadb-10.5.9
* [Revision #d82386b6b9](https://github.com/MariaDB/server/commit/d82386b6b9)\
  2021-02-17 16:18:55 +0200
  * [MDEV-24848](https://jira.mariadb.org/browse/MDEV-24848) Assertion rlen\<llen failed when applying MEMSET
* [Revision #fc5e03f093](https://github.com/MariaDB/server/commit/fc5e03f093)\
  2021-02-15 20:21:12 +0200
  * Ignore reporting in thd\_progress\_report() if we cannot lock LOCK\_thd\_data
* [Revision #8eaf4bc5ec](https://github.com/MariaDB/server/commit/8eaf4bc5ec)\
  2021-02-15 13:57:35 +0300
  * Comment on assertion in row\_rename\_table\_for\_mysql()
* [Revision #34c654024c](https://github.com/MariaDB/server/commit/34c654024c)\
  2021-02-15 01:33:06 +0200
  * [MDEV-24855](https://jira.mariadb.org/browse/MDEV-24855) ER\_CRASHED\_ON\_USAGE or Assertion \`length <= column->length'
* [Revision #b3df194e31](https://github.com/MariaDB/server/commit/b3df194e31)\
  2021-02-12 20:40:25 +0200
  * [MDEV-24833](https://jira.mariadb.org/browse/MDEV-24833) : Signal 11 on wsrep\_can\_run\_in\_toi at wsrep\_mysqld.cc:1994
* [Revision #7fb528d722](https://github.com/MariaDB/server/commit/7fb528d722)\
  2021-02-05 14:48:40 +0200
  * Deb: Remove build depencency libreadline-gplv2-dev no longer available
* [Revision #2405752855](https://github.com/MariaDB/server/commit/2405752855)\
  2021-02-10 12:14:56 +0200
  * Salsa-CI: Install readline from Buster as it was removed from Sid
* [Revision #66b8edf8a5](https://github.com/MariaDB/server/commit/66b8edf8a5)\
  2021-02-17 22:43:15 +0530
  * [MDEV-19168](https://jira.mariadb.org/browse/MDEV-19168): Add ssl-flush command. (#1749)
* [Revision #9f13670004](https://github.com/MariaDB/server/commit/9f13670004)\
  2021-02-17 17:44:23 +0200
  * [MDEV-24738](https://jira.mariadb.org/browse/MDEV-24738) fixup: heap-use-after-poison in lock\_sys\_t::deadlock\_check()
* [Revision #e92c34ce34](https://github.com/MariaDB/server/commit/e92c34ce34)\
  2021-02-17 14:25:35 +0100
  * Keep old GCC quiet.
* [Revision #c68007d958](https://github.com/MariaDB/server/commit/c68007d958)\
  2021-02-17 12:43:33 +0200
  * [MDEV-24738](https://jira.mariadb.org/browse/MDEV-24738) Improve the InnoDB deadlock checker
* [Revision #3ddb4fddf1](https://github.com/MariaDB/server/commit/3ddb4fddf1)\
  2021-02-15 17:21:42 +0200
  * [MDEV-24738](https://jira.mariadb.org/browse/MDEV-24738): Extend the test innodb.deadlock\_detect
* [Revision #272a1289ad](https://github.com/MariaDB/server/commit/272a1289ad)\
  2021-02-17 12:34:06 +0200
  * [MDEV-24884](https://jira.mariadb.org/browse/MDEV-24884) Hang in ssux\_lock\_low::write\_lock()
* [Revision #584e52118c](https://github.com/MariaDB/server/commit/584e52118c)\
  2021-02-17 12:18:03 +0200
  * [MDEV-20612](https://jira.mariadb.org/browse/MDEV-20612) fixup: Make comments refer to lock\_sys.latch
* [Revision #1146e98b3a](https://github.com/MariaDB/server/commit/1146e98b3a)\
  2021-02-16 11:06:36 +0100
  * [MDEV-24341](https://jira.mariadb.org/browse/MDEV-24341) - followup remove assert.
* [Revision #e5d83ad472](https://github.com/MariaDB/server/commit/e5d83ad472)\
  2021-02-16 11:27:13 +0200
  * [MDEV-20612](https://jira.mariadb.org/browse/MDEV-20612) fixup: Fix a memory leak in buffer pool resize
* [Revision #2e84846ec0](https://github.com/MariaDB/server/commit/2e84846ec0)\
  2021-02-15 10:15:00 +0200
  * [MDEV-24861](https://jira.mariadb.org/browse/MDEV-24861) Assertion \`trx->rsegs.m\_redo.rseg' failed in innodb\_prepare\_commit\_versioned
* [Revision #4df0249b9a](https://github.com/MariaDB/server/commit/4df0249b9a)\
  2021-02-14 18:30:39 +0100
  * [MDEV-24341](https://jira.mariadb.org/browse/MDEV-24341) Innodb - do not block in foreground thread in log\_write\_up\_to(
* [Revision #a1542f8a57](https://github.com/MariaDB/server/commit/a1542f8a57)\
  2021-02-12 17:43:10 +0200
  * [MDEV-24643](https://jira.mariadb.org/browse/MDEV-24643): Assertion failed in rw\_lock::update\_unlock()
* [Revision #26d6224dd6](https://github.com/MariaDB/server/commit/26d6224dd6)\
  2021-02-12 17:42:18 +0200
  * [MDEV-20612](https://jira.mariadb.org/browse/MDEV-20612): Enable concurrent lock\_release()
* [Revision #b08448de64](https://github.com/MariaDB/server/commit/b08448de64)\
  2021-02-12 17:35:42 +0200
  * [MDEV-20612](https://jira.mariadb.org/browse/MDEV-20612): Partition lock\_sys.latch
* [Revision #b01d8e1a33](https://github.com/MariaDB/server/commit/b01d8e1a33)\
  2021-02-11 14:52:10 +0200
  * [MDEV-20612](https://jira.mariadb.org/browse/MDEV-20612): Replace lock\_sys.mutex with lock\_sys.latch
* [Revision #903464929c](https://github.com/MariaDB/server/commit/903464929c)\
  2021-02-11 14:36:11 +0200
  * [MDEV-20612](https://jira.mariadb.org/browse/MDEV-20612) preparation: LockMutexGuard
* [Revision #2e64513fba](https://github.com/MariaDB/server/commit/2e64513fba)\
  2021-02-05 18:29:30 +0200
  * [MDEV-20612](https://jira.mariadb.org/browse/MDEV-20612) preparation: Fewer calls to buf\_page\_t::id()
* Merge [Revision #b19ec8848c](https://github.com/MariaDB/server/commit/b19ec8848c) 2021-02-11 09:26:53 +0200 - Merge 10.5 into 10.6
* [Revision #c7edbe5bb1](https://github.com/MariaDB/server/commit/c7edbe5bb1)\
  2021-02-11 12:45:24 +1100
  * [MDEV-24366](https://jira.mariadb.org/browse/MDEV-24366): s3 test postfix - use default for S3\_BUCKET
* [Revision #bfb4761ca0](https://github.com/MariaDB/server/commit/bfb4761ca0)\
  2021-02-10 14:15:51 +0200
  * [MDEV-24834](https://jira.mariadb.org/browse/MDEV-24834) Assertion mtr->memo\_contains\_flagged() in btr0cur.cc:1500
* [Revision #a2fbbba2e3](https://github.com/MariaDB/server/commit/a2fbbba2e3)\
  2021-02-10 15:27:25 +0530
  * [MDEV-24832](https://jira.mariadb.org/browse/MDEV-24832) Root page AHI removal fails during rollback of bulk insert
* [Revision #786bc312b8](https://github.com/MariaDB/server/commit/786bc312b8)\
  2021-02-07 13:21:18 +0200
  * Cleanup: Replace mysql\_cond\_t with pthread\_cond\_t
* Merge [Revision #520c76bfb4](https://github.com/MariaDB/server/commit/520c76bfb4) 2021-02-07 12:32:33 +0200 - Merge 10.5 into 10.6
* [Revision #74ab97f58f](https://github.com/MariaDB/server/commit/74ab97f58f)\
  2021-02-07 11:18:21 +0200
  * Cleanup: Remove lock\_trx\_lock\_list\_init(), lock\_table\_get\_n\_locks()
* [Revision #487fbc2e15](https://github.com/MariaDB/server/commit/487fbc2e15)\
  2021-02-05 16:37:06 +0200
  * [MDEV-21452](https://jira.mariadb.org/browse/MDEV-21452) fixup: Introduce trx\_t::mutex\_is\_owner()
* [Revision #455514c800](https://github.com/MariaDB/server/commit/455514c800)\
  2021-02-05 16:16:44 +0200
  * [MDEV-24789](https://jira.mariadb.org/browse/MDEV-24789): Try to reduce mutex contention
* [Revision #3e45f8e36a](https://github.com/MariaDB/server/commit/3e45f8e36a)\
  2021-02-05 13:10:26 +0200
  * [MDEV-24789](https://jira.mariadb.org/browse/MDEV-24789): Reduce sizeof(trx\_lock\_t)
* [Revision #465bdabb7a](https://github.com/MariaDB/server/commit/465bdabb7a)\
  2021-02-04 17:26:08 +0200
  * Cleanup: Reduce some lock\_sys.mutex contention
* [Revision #de407e7cb4](https://github.com/MariaDB/server/commit/de407e7cb4)\
  2021-02-05 08:35:15 +0200
  * [MDEV-24731](https://jira.mariadb.org/browse/MDEV-24731) fixup: bogus assertion
* [Revision #c42ee8a7cf](https://github.com/MariaDB/server/commit/c42ee8a7cf)\
  2021-02-05 08:32:57 +0200
  * [MDEV-24781](https://jira.mariadb.org/browse/MDEV-24781) fixup: Adjust innodb.innodb-index-debug
* [Revision #597510adfc](https://github.com/MariaDB/server/commit/597510adfc)\
  2021-02-04 14:23:01 +0530
  * [MDEV-24781](https://jira.mariadb.org/browse/MDEV-24781) Assertion \`mode == 16 || mode == 12 || fix\_block->page.status != buf\_page\_t::FREED' failed in buf\_page\_get\_low
* [Revision #5f46385764](https://github.com/MariaDB/server/commit/5f46385764)\
  2021-02-04 16:38:07 +0200
  * [MDEV-24731](https://jira.mariadb.org/browse/MDEV-24731) Excessive mutex contention in DeadlockChecker::check\_and\_resolve()
* [Revision #43ca6059ca](https://github.com/MariaDB/server/commit/43ca6059ca)\
  2021-02-02 19:24:05 +0530
  * [MDEV-24720](https://jira.mariadb.org/browse/MDEV-24720) AHI removal during rollback of bulk insert
* Merge [Revision #1110beccd4](https://github.com/MariaDB/server/commit/1110beccd4) 2021-02-02 15:15:53 +0200 - Merge 10.5 into 10.6
* [Revision #8a495d7f90](https://github.com/MariaDB/server/commit/8a495d7f90)\
  2021-01-30 15:50:14 +0800
  * [MDEV-24647](https://jira.mariadb.org/browse/MDEV-24647) Columnstore storage engine cannot be compiled with mariadb server on aarch64 platform (#1742)
* [Revision #c411393a84](https://github.com/MariaDB/server/commit/c411393a84)\
  2021-01-28 15:26:53 +0200
  * [MDEV-24715](https://jira.mariadb.org/browse/MDEV-24715) Assertion !node->table->skip\_alter\_undo in CREATE...REPLACE SELECT
* [Revision #68b2819342](https://github.com/MariaDB/server/commit/68b2819342)\
  2021-01-27 18:41:58 +0200
  * Cleanup: Remove many C-style lock\_get\_ accessors
* [Revision #cbb0a60c57](https://github.com/MariaDB/server/commit/cbb0a60c57)\
  2021-01-27 18:02:11 +0200
  * Cleanup: Remove lock\_get\_size()
* [Revision #5dd028f8ee](https://github.com/MariaDB/server/commit/5dd028f8ee)\
  2021-01-27 11:05:15 +0200
  * [MDEV-24700](https://jira.mariadb.org/browse/MDEV-24700) Assertion "lock not found"==0 in lock\_table\_x\_unlock()
* [Revision #121d0f7f53](https://github.com/MariaDB/server/commit/121d0f7f53)\
  2021-01-26 17:10:56 +0200
  * [MDEV-20612](https://jira.mariadb.org/browse/MDEV-20612): Speed up lock\_table\_other\_has\_incompatible()
* [Revision #3329f0ed0c](https://github.com/MariaDB/server/commit/3329f0ed0c)\
  2021-01-26 16:28:02 +0200
  * Cleanup: Remove LOCK\_REC (which was mutually exclusive with LOCK\_TABLE)
* [Revision #b32f057da7](https://github.com/MariaDB/server/commit/b32f057da7)\
  2021-01-15 16:32:37 +0200
  * Cleanup: Remove ib\_lock\_t::type\_mode\_string()
* [Revision #462cb66662](https://github.com/MariaDB/server/commit/462cb66662)\
  2021-01-15 16:26:54 +0200
  * Cleanup: Replace lock\_mode\_string() with a table lookup
* [Revision #e71e613353](https://github.com/MariaDB/server/commit/e71e613353)\
  2021-01-26 16:39:56 +0200
  * [MDEV-24671](https://jira.mariadb.org/browse/MDEV-24671): Replace lock\_wait\_timeout\_task with mysql\_cond\_timedwait()
* [Revision #7f1ab8f742](https://github.com/MariaDB/server/commit/7f1ab8f742)\
  2021-01-26 09:05:46 +0200
  * Cleanups:
* [Revision #ff3f07ce82](https://github.com/MariaDB/server/commit/ff3f07ce82)\
  2021-01-19 15:20:26 +0200
  * Cleanup: Remove unused query node declarations
* [Revision #898dcf93a8](https://github.com/MariaDB/server/commit/898dcf93a8)\
  2021-01-26 09:00:43 +0200
  * Cleanup the lock creation
* [Revision #469da6c34d](https://github.com/MariaDB/server/commit/469da6c34d)\
  2021-01-26 08:39:11 +0200
  * Cleanup: Remove trx\_get\_id\_for\_print()
* [Revision #7ebabea5d3](https://github.com/MariaDB/server/commit/7ebabea5d3)\
  2020-11-05 23:38:18 +0100
  * [MDEV-23959](https://jira.mariadb.org/browse/MDEV-23959) GSSAPI plugin - support AD or local group name , and SIDs on Windows
* [Revision #c310f4c381](https://github.com/MariaDB/server/commit/c310f4c381)\
  2021-01-27 14:17:43 +0100
  * [MDEV-24685](https://jira.mariadb.org/browse/MDEV-24685) - remove IO thread states output from SHOW ENGINE INNODB STATUS
* [Revision #95a2bca01f](https://github.com/MariaDB/server/commit/95a2bca01f)\
  2020-12-08 10:07:45 +0100
  * [MDEV-20008](https://jira.mariadb.org/browse/MDEV-20008): Galera strict mode
* [Revision #3f871b3394](https://github.com/MariaDB/server/commit/3f871b3394)\
  2021-01-25 19:48:09 +0200
  * [MDEV-515](https://jira.mariadb.org/browse/MDEV-515) fixup: Cover dict\_table\_t::clear() during ADD INDEX
* [Revision #3cef4f8f0f](https://github.com/MariaDB/server/commit/3cef4f8f0f)\
  2021-01-25 18:41:27 +0200
  * [MDEV-515](https://jira.mariadb.org/browse/MDEV-515) Reduce InnoDB undo logging for insert into empty table
* [Revision #7aed5eb76f](https://github.com/MariaDB/server/commit/7aed5eb76f)\
  2021-01-25 15:14:46 +0200
  * [MDEV-24642](https://jira.mariadb.org/browse/MDEV-24642) Assertion r->emplace... failed in sux\_lock::s\_lock\_register()
* Merge [Revision #e9fc61053d](https://github.com/MariaDB/server/commit/e9fc61053d) 2021-01-25 15:12:24 +0200 - Merge 10.5 into 10.6
* Merge [Revision #46234f03c8](https://github.com/MariaDB/server/commit/46234f03c8) 2021-01-25 12:56:30 +0200 - Merge 10.5 into 10.6
* [Revision #0d7380fdac](https://github.com/MariaDB/server/commit/0d7380fdac)\
  2021-01-21 17:02:13 +0530
  * [MDEV-24637](https://jira.mariadb.org/browse/MDEV-24637) fts\_slots is being accessed after it gets freed
* [Revision #1936b3c873](https://github.com/MariaDB/server/commit/1936b3c873)\
  2021-01-21 17:16:32 +0100
  * -s stands for silent, copy-paste mistake? (#1733)
* [Revision #fa14c423cd](https://github.com/MariaDB/server/commit/fa14c423cd)\
  2016-06-22 15:52:07 +0200
  * [MDEV-10271](https://jira.mariadb.org/browse/MDEV-10271): add master host/port info to slave thread exit messages
* [Revision #9a08fcbf60](https://github.com/MariaDB/server/commit/9a08fcbf60)\
  2021-01-15 17:54:27 +1100
  * .gitattributes - correct language detection
* [Revision #0dfabf6e40](https://github.com/MariaDB/server/commit/0dfabf6e40)\
  2021-01-14 17:35:07 +0200
  * Fixup 92abdcca5a5324f0727112ab2417d10c7a8d5094
* Merge [Revision #394fc71f4f](https://github.com/MariaDB/server/commit/394fc71f4f) 2021-01-14 16:35:05 +0200 - [MDEV-24569](https://jira.mariadb.org/browse/MDEV-24569): Merge 10.5 into 10.6
* Merge [Revision #6d05a95c65](https://github.com/MariaDB/server/commit/6d05a95c65) 2021-01-14 16:13:31 +0200 - Merge 10.5 into 10.6
* Merge [Revision #666565c7f0](https://github.com/MariaDB/server/commit/666565c7f0) 2021-01-11 17:32:08 +0200 - Merge 10.5 into 10.6
* Merge [Revision #92abdcca5a](https://github.com/MariaDB/server/commit/92abdcca5a) 2021-01-07 09:08:09 +0200 - Merge 10.5 into 10.6
* [Revision #8a4ca33938](https://github.com/MariaDB/server/commit/8a4ca33938)\
  2021-01-05 14:13:52 +0200
  * Cleanup: Declare trx\_weight\_ge() inline
* [Revision #bd52f1a2dd](https://github.com/MariaDB/server/commit/bd52f1a2dd)\
  2021-01-04 15:30:34 +0200
  * Cleanup: Remove lock\_number\_of\_rows\_locked()
* [Revision #3dabe637ca](https://github.com/MariaDB/server/commit/3dabe637ca)\
  2021-01-04 13:47:27 +0200
  * Clarify some comments
* Merge [Revision #6268bdadf7](https://github.com/MariaDB/server/commit/6268bdadf7) 2021-01-04 10:52:32 +0200 - Merge 10.5 into 10.6
* [Revision #3f38e2a452](https://github.com/MariaDB/server/commit/3f38e2a452)\
  2021-01-01 16:04:00 +0200
  * [MDEV-24503](https://jira.mariadb.org/browse/MDEV-24503) Assertion m\_prebuilt->trx == thd\_to\_trx(m\_user\_thd) failed in ha\_innobase::is\_read\_only
* [Revision #9118fd360a](https://github.com/MariaDB/server/commit/9118fd360a)\
  2020-12-25 13:16:46 +0100
  * [MDEV-24142](https://jira.mariadb.org/browse/MDEV-24142) - Windows - do not use WaitOnAddress-based ssux\_lock.
* [Revision #f02c8ffa34](https://github.com/MariaDB/server/commit/f02c8ffa34)\
  2020-12-23 19:11:43 +0800
  * [MDEV-24031](https://jira.mariadb.org/browse/MDEV-24031): remove maria\_ft\_boolean\_check\_syntax\_string
* [Revision #3b7dbdf080](https://github.com/MariaDB/server/commit/3b7dbdf080)\
  2020-12-22 07:42:03 +0200
  * [MDEV-24449](https://jira.mariadb.org/browse/MDEV-24449) cleanup: Remove a timeout
* [Revision #2f6970ef1c](https://github.com/MariaDB/server/commit/2f6970ef1c)\
  2020-12-20 01:50:16 +0900
  * [MDEV-24424](https://jira.mariadb.org/browse/MDEV-24424) Unnecessary usage of to\_float() for INSERT into the Spider table with float column
* [Revision #10bec91890](https://github.com/MariaDB/server/commit/10bec91890)\
  2020-12-21 21:30:01 +0200
  * [MDEV-24448](https://jira.mariadb.org/browse/MDEV-24448) fixup: Correct a typo in a comment
* Merge [Revision #ad436d9221](https://github.com/MariaDB/server/commit/ad436d9221) 2020-12-21 19:52:49 +0200 - Merge 10.5 into 10.6
* [Revision #8c68b54981](https://github.com/MariaDB/server/commit/8c68b54981)\
  2020-12-21 19:47:17 +0200
  * [MDEV-21452](https://jira.mariadb.org/browse/MDEV-21452) fixup: Fix fake server hang reports
* Merge [Revision #30dc4287ec](https://github.com/MariaDB/server/commit/30dc4287ec) 2020-12-19 12:23:06 +0200 - Merge 10.5 into 10.6
* Merge [Revision #4e0004ea13](https://github.com/MariaDB/server/commit/4e0004ea13) 2020-12-18 10:23:49 +0200 - Merge 10.5 into 10.6
* Merge [Revision #c36a2a0d1c](https://github.com/MariaDB/server/commit/c36a2a0d1c) 2020-12-17 14:56:08 +0200 - Merge 10.5 into 10.6
* [Revision #af1335c2d6](https://github.com/MariaDB/server/commit/af1335c2d6)\
  2020-12-16 20:01:41 +0200
  * Speed up mariadb-backup.xb\_compressed\_encrypted
* [Revision #07e4b6b276](https://github.com/MariaDB/server/commit/07e4b6b276)\
  2020-12-16 17:45:01 +0200
  * [MDEV-24167](https://jira.mariadb.org/browse/MDEV-24167) fixup: Wake up all update\_lock() in u\_unlock()
* [Revision #cf2480dd77](https://github.com/MariaDB/server/commit/cf2480dd77)\
  2020-12-15 17:45:19 +0200
  * [MDEV-21452](https://jira.mariadb.org/browse/MDEV-21452): Retain the watchdog only on dict\_sys.mutex, for performance
* [Revision #ff5d306e29](https://github.com/MariaDB/server/commit/ff5d306e29)\
  2020-12-04 19:02:58 +0200
  * [MDEV-21452](https://jira.mariadb.org/browse/MDEV-21452): Replace ib\_mutex\_t with mysql\_mutex\_t
* [Revision #db006a9a43](https://github.com/MariaDB/server/commit/db006a9a43)\
  2020-12-04 18:07:25 +0200
  * [MDEV-21452](https://jira.mariadb.org/browse/MDEV-21452): Remove os\_event\_t, MUTEX\_EVENT, TTASEventMutex, sync\_array
* [Revision #38fd7b7d91](https://github.com/MariaDB/server/commit/38fd7b7d91)\
  2020-12-04 16:18:04 +0200
  * [MDEV-21452](https://jira.mariadb.org/browse/MDEV-21452): Replace all direct use of os\_event\_t
* [Revision #59b2848af6](https://github.com/MariaDB/server/commit/59b2848af6)\
  2020-12-15 17:53:44 +0200
  * Fix the SRW\_LOCK\_DUMMY build with PLUGIN\_PERFSCHEMA=NO
* [Revision #20da7b222d](https://github.com/MariaDB/server/commit/20da7b222d)\
  2020-12-15 16:52:25 +0200
  * [MDEV-24410](https://jira.mariadb.org/browse/MDEV-24410): Bug in SRW\_LOCK\_DUMMY rw\_lock\_t wrapper
* [Revision #43d3dad114](https://github.com/MariaDB/server/commit/43d3dad114)\
  2020-12-15 14:29:40 +0200
  * [MDEV-24142](https://jira.mariadb.org/browse/MDEV-24142)/[MDEV-24167](https://jira.mariadb.org/browse/MDEV-24167) fixup: Split ssux\_lock and srw\_lock
* [Revision #1c660211bb](https://github.com/MariaDB/server/commit/1c660211bb)\
  2020-12-14 19:50:42 +0200
  * [MDEV-23659](https://jira.mariadb.org/browse/MDEV-23659) Update Galera disabled.def file
* Merge [Revision #9ecd766526](https://github.com/MariaDB/server/commit/9ecd766526) 2020-12-14 18:02:40 +0200 - Merge 10.5 into 10.6
* [Revision #d79c3f3297](https://github.com/MariaDB/server/commit/d79c3f3297)\
  2020-12-09 19:21:23 +0530
  * [MDEV-24353](https://jira.mariadb.org/browse/MDEV-24353): Adding GROUP BY slows down a query
* Merge [Revision #be4d266553](https://github.com/MariaDB/server/commit/be4d266553) 2020-12-09 16:57:24 +0200 - Merge 10.5 into 10.6
* Merge [Revision #ca821692af](https://github.com/MariaDB/server/commit/ca821692af) 2020-12-09 14:36:38 +0200 - Merge 10.5 into 10.6
* [Revision #e9f33b7760](https://github.com/MariaDB/server/commit/e9f33b7760)\
  2020-12-03 17:42:07 +0200
  * [MDEV-24142](https://jira.mariadb.org/browse/MDEV-24142): Avoid block\_lock alignment loss on 64-bit systems
* [Revision #ba2d45dc54](https://github.com/MariaDB/server/commit/ba2d45dc54)\
  2020-12-03 14:49:41 +0200
  * [MDEV-24142](https://jira.mariadb.org/browse/MDEV-24142): Remove INFORMATION\_SCHEMA.INNODB\_MUTEXES
* [Revision #9702be2c73](https://github.com/MariaDB/server/commit/9702be2c73)\
  2020-12-03 14:20:27 +0200
  * [MDEV-24142](https://jira.mariadb.org/browse/MDEV-24142): Remove FILE,LINE related to buf\_block\_t::lock
* [Revision #ac028ec5d8](https://github.com/MariaDB/server/commit/ac028ec5d8)\
  2020-12-03 14:17:22 +0200
  * [MDEV-24142](https://jira.mariadb.org/browse/MDEV-24142): Remove the LatchDebug interface to rw-locks
* [Revision #06efef4be3](https://github.com/MariaDB/server/commit/06efef4be3)\
  2020-11-30 15:21:13 +0200
  * [MDEV-24308](https://jira.mariadb.org/browse/MDEV-24308): Windows improvements
* [Revision #03ca6495df](https://github.com/MariaDB/server/commit/03ca6495df)\
  2020-12-03 15:18:51 +0200
  * [MDEV-24142](https://jira.mariadb.org/browse/MDEV-24142): Replace InnoDB rw\_lock\_t with sux\_lock
* [Revision #d46b42489a](https://github.com/MariaDB/server/commit/d46b42489a)\
  2020-12-03 10:42:18 +0200
  * [MDEV-24142](https://jira.mariadb.org/browse/MDEV-24142) preparation: Add srw\_mutex and srw\_lock::u\_lock()
* [Revision #3872e585f3](https://github.com/MariaDB/server/commit/3872e585f3)\
  2020-12-03 15:15:47 +0200
  * [MDEV-24167](https://jira.mariadb.org/browse/MDEV-24167): Stabilize perfschema.sxlock\_func
* [Revision #1669c8890c](https://github.com/MariaDB/server/commit/1669c8890c)\
  2020-12-03 09:55:53 +0200
  * [MDEV-24167](https://jira.mariadb.org/browse/MDEV-24167) fixup: Improve the PERFORMANCE\_SCHEMA instrumentation
* [Revision #260161fc9f](https://github.com/MariaDB/server/commit/260161fc9f)\
  2020-12-03 09:11:31 +0200
  * [MDEV-24167](https://jira.mariadb.org/browse/MDEV-24167) fixup: Avoid hangs in SRW\_LOCK\_DUMMY
* Merge [Revision #a13fac9eee](https://github.com/MariaDB/server/commit/a13fac9eee) 2020-12-03 08:12:47 +0200 - Merge 10.5 into 10.6
* [Revision #e28d9c15c3](https://github.com/MariaDB/server/commit/e28d9c15c3)\
  2020-12-01 10:10:41 +0200
  * [MDEV-24167](https://jira.mariadb.org/browse/MDEV-24167) fixup: Improve perfschema.sxlock\_func test
* Merge [Revision #cde525f94a](https://github.com/MariaDB/server/commit/cde525f94a) 2020-11-30 14:04:01 +0200 - Merge 10.5 into 10.6
* [Revision #fc6a7e90ea](https://github.com/MariaDB/server/commit/fc6a7e90ea)\
  2020-11-28 15:00:54 +0200
  * row\_search\_index\_entry(): Simplify some assertions
* [Revision #1fdc161d8f](https://github.com/MariaDB/server/commit/1fdc161d8f)\
  2020-11-30 11:47:09 +0200
  * [MDEV-24167](https://jira.mariadb.org/browse/MDEV-24167) fixup: Always derive srw\_lock from rw\_lock
* Merge [Revision #565b0dd17d](https://github.com/MariaDB/server/commit/565b0dd17d) 2020-11-30 11:30:26 +0200 - Merge 10.5 into 10.6
* Merge [Revision #ccb5cf20ca](https://github.com/MariaDB/server/commit/ccb5cf20ca) 2020-11-28 11:58:03 +0200 - Merge 10.5 into 10.6
* Merge [Revision #8b8969929d](https://github.com/MariaDB/server/commit/8b8969929d) 2020-11-26 07:36:53 +0200 - Merge 10.5 into 10.6
* [Revision #581aebe29f](https://github.com/MariaDB/server/commit/581aebe29f)\
  2020-11-24 21:01:22 +0200
  * [MDEV-24167](https://jira.mariadb.org/browse/MDEV-24167): Fix -DPLUGIN\_PERFSCHEMA=NO and Windows debug builds
* [Revision #4e359eb88f](https://github.com/MariaDB/server/commit/4e359eb88f)\
  2020-11-23 08:06:30 +0200
  * Cleanup: Reduce trx\_t::mutex hold time
* [Revision #814bc21305](https://github.com/MariaDB/server/commit/814bc21305)\
  2020-11-23 07:49:43 +0200
  * Cleanup: Use Atomic\_relaxed for trx\_t::state
* [Revision #0bee3b8d65](https://github.com/MariaDB/server/commit/0bee3b8d65)\
  2020-11-20 12:28:47 +0200
  * Cleanup: Use Atomic\_relaxed for dict\_sys.row\_id
* [Revision #edbde4a11f](https://github.com/MariaDB/server/commit/edbde4a11f)\
  2020-11-20 12:30:55 +0200
  * [MDEV-24167](https://jira.mariadb.org/browse/MDEV-24167): Replace fil\_space::latch
* [Revision #bdd88cfa34](https://github.com/MariaDB/server/commit/bdd88cfa34)\
  2020-11-09 11:22:32 +0200
  * [MDEV-24167](https://jira.mariadb.org/browse/MDEV-24167): Replace fts\_cache\_rw\_lock, fts\_cache\_init\_rw\_lock with mutex
* [Revision #1a1b7a6f16](https://github.com/MariaDB/server/commit/1a1b7a6f16)\
  2020-11-20 09:31:27 +0200
  * [MDEV-24167](https://jira.mariadb.org/browse/MDEV-24167): Replace dict\_operation\_lock (dict\_sys.latch)
* [Revision #06ef5509d0](https://github.com/MariaDB/server/commit/06ef5509d0)\
  2020-11-20 09:18:41 +0200
  * [MDEV-24167](https://jira.mariadb.org/browse/MDEV-24167): Replace trx\_purge\_latch
* [Revision #63dd2a97e4](https://github.com/MariaDB/server/commit/63dd2a97e4)\
  2020-11-20 09:17:27 +0200
  * [MDEV-24167](https://jira.mariadb.org/browse/MDEV-24167): Replace trx\_i\_s\_cache\_lock
* [Revision #c561f9e6e8](https://github.com/MariaDB/server/commit/c561f9e6e8)\
  2020-11-24 15:41:03 +0200
  * [MDEV-24167](https://jira.mariadb.org/browse/MDEV-24167): Use lightweight srw\_lock for btr\_search\_latch
* Merge [Revision #f87e4b4e4d](https://github.com/MariaDB/server/commit/f87e4b4e4d) 2020-11-24 15:25:32 +0200 - Merge 10.5 into 10.6
* [Revision #c2ea036b7f](https://github.com/MariaDB/server/commit/c2ea036b7f)\
  2020-11-24 09:09:40 +0200
  * After-merge fix: Update ColumnStore
* [Revision #540e2f78a6](https://github.com/MariaDB/server/commit/540e2f78a6)\
  2020-11-23 20:18:29 +0100
  * Fix GCC warning/error.
* [Revision #295f3e4cfb](https://github.com/MariaDB/server/commit/295f3e4cfb)\
  2020-11-23 19:24:31 +0100
  * [MDEV-19237](https://jira.mariadb.org/browse/MDEV-19237) Skip sending metadata when possible for binary protocol.
* Merge [Revision #a62a675fd2](https://github.com/MariaDB/server/commit/a62a675fd2) 2020-11-23 17:57:58 +0200 - Merge 10.5 into 10.6
* [Revision #c3d4e57182](https://github.com/MariaDB/server/commit/c3d4e57182)\
  2020-11-17 17:52:08 +0100
  * [MDEV-19162](https://jira.mariadb.org/browse/MDEV-19162) anonymous derived tables part
* Merge [Revision #10aa576483](https://github.com/MariaDB/server/commit/10aa576483) 2020-11-14 20:05:35 +0100 - Merge branch '10.5' into 10.6
* [Revision #6083c5a054](https://github.com/MariaDB/server/commit/6083c5a054)\
  2020-11-14 14:13:33 +0000
  * This patch puts MCS debian packaging files and part of debian/control into the engine directory
* [Revision #f950559f66](https://github.com/MariaDB/server/commit/f950559f66)\
  2020-11-12 21:26:34 +0000
  * Windows : reduce useless system checks
* Merge [Revision #254bb1c35b](https://github.com/MariaDB/server/commit/254bb1c35b) 2020-11-12 15:54:08 +0200 - Merge 10.5 into 10.6
* [Revision #ef639f1a93](https://github.com/MariaDB/server/commit/ef639f1a93)\
  2020-11-12 15:37:10 +0200
  * [MDEV-23497](https://jira.mariadb.org/browse/MDEV-23497) fixup: Fix galera.galera\_load\_data
* [Revision #16f86e69b5](https://github.com/MariaDB/server/commit/16f86e69b5)\
  2020-11-12 08:31:56 +0200
  * [MDEV-22343](https://jira.mariadb.org/browse/MDEV-22343) fixup: Fix a memory leak
* [Revision #5407117a59](https://github.com/MariaDB/server/commit/5407117a59)\
  2020-11-11 11:02:27 +0200
  * [MDEV-22343](https://jira.mariadb.org/browse/MDEV-22343) Remove SYS\_TABLESPACES and SYS\_DATAFILES
* [Revision #9bc874a594](https://github.com/MariaDB/server/commit/9bc874a594)\
  2020-11-10 17:21:16 +0200
  * [MDEV-23497](https://jira.mariadb.org/browse/MDEV-23497) Make ROW\_FORMAT=COMPRESSED read-only by default
* Merge [Revision #c498250888](https://github.com/MariaDB/server/commit/c498250888) 2020-11-03 19:11:36 +0200 - Merge 10.5 into 10.6
* Merge [Revision #09a1f0075a](https://github.com/MariaDB/server/commit/09a1f0075a) 2020-11-02 12:49:19 +0200 - Merge 10.5 into 10.6
* [Revision #e6f95b23f4](https://github.com/MariaDB/server/commit/e6f95b23f4)\
  2020-04-16 00:44:20 +0900
  * [MDEV-20100](https://jira.mariadb.org/browse/MDEV-20100) [MariaDB 10.3.9](../../old-releases/release-notes-mariadb-10-3-series/mariadb-1039-release-notes.md) Crash "\[ERROR] mysqld got signal 11 ;"
* [Revision #5d4599f975](https://github.com/MariaDB/server/commit/5d4599f975)\
  2020-10-11 12:26:38 +0000
  * [MDEV-22596](https://jira.mariadb.org/browse/MDEV-22596): DELETE FOR PORTION does not obey "Expression in FOR PORTION OF must be constant" limitation, data can be easily lost
* [Revision #8a884a9fa5](https://github.com/MariaDB/server/commit/8a884a9fa5)\
  2020-04-15 13:54:49 +0300
  * Travis-CI: Use new Ubuntu 20.04 as base, streamline and document
* [Revision #b4fb15ccd4](https://github.com/MariaDB/server/commit/b4fb15ccd4)\
  2020-10-05 10:30:26 +0300
  * [MDEV-16664](https://jira.mariadb.org/browse/MDEV-16664): Remove innodb\_lock\_schedule\_algorithm
* Merge [Revision #3b72b35a77](https://github.com/MariaDB/server/commit/3b72b35a77) 2020-09-24 16:36:23 +0300 - Merge 10.5 into 10.6
* Merge [Revision #6ce0a6f9ad](https://github.com/MariaDB/server/commit/6ce0a6f9ad) 2020-09-24 10:21:26 +0300 - Merge 10.5 into 10.6
* [Revision #b5c050563b](https://github.com/MariaDB/server/commit/b5c050563b)\
  2020-09-21 23:15:58 +0200
  * [MDEV-23783](https://jira.mariadb.org/browse/MDEV-23783) Get rid of FreeConsole() call on mariadbd startup
* [Revision #46fab5b32a](https://github.com/MariaDB/server/commit/46fab5b32a)\
  2020-09-04 22:10:57 +0900
  * [MDEV-7098](https://jira.mariadb.org/browse/MDEV-7098) spider/bg.spider\_fixes failed in buildbot with safe\_mutex: Trying to unlock mutex conn->mta\_conn\_mutex that wasn't locked at storage/spider/spd\_db\_conn.cc, line 671
* Merge [Revision #5edf3e0388](https://github.com/MariaDB/server/commit/5edf3e0388) 2020-09-02 14:36:14 +0200 - Merge branch '10.5' into 10.6
* [Revision #32a29afea7](https://github.com/MariaDB/server/commit/32a29afea7)\
  2020-08-11 12:11:07 +0000
  * [MDEV-23238](https://jira.mariadb.org/browse/MDEV-23238) - remove async client from server code.
* [Revision #72f0f0db9c](https://github.com/MariaDB/server/commit/72f0f0db9c)\
  2020-08-26 22:25:26 +0900
  * Fix a compiler warning
* [Revision #75b7aef2c0](https://github.com/MariaDB/server/commit/75b7aef2c0)\
  2020-08-25 20:41:33 +0900
  * [MDEV-23561](https://jira.mariadb.org/browse/MDEV-23561) Spider doesn't work with ps protocol
* [Revision #2b113185c0](https://github.com/MariaDB/server/commit/2b113185c0)\
  2020-08-24 10:29:23 +0900
  * Fix indents of Spider
* [Revision #1a09081d19](https://github.com/MariaDB/server/commit/1a09081d19)\
  2020-08-23 12:30:14 +0900
  * [MDEV-22246](https://jira.mariadb.org/browse/MDEV-22246) Result rows duplicated by spider engine
* [Revision #07d57e0e1d](https://github.com/MariaDB/server/commit/07d57e0e1d)\
  2020-08-17 09:45:03 +0900
  * [MDEV-20827](https://jira.mariadb.org/browse/MDEV-20827) Wrong param parsing in spider\_direct\_sql() when param contain comma
* [Revision #582290dacd](https://github.com/MariaDB/server/commit/582290dacd)\
  2020-08-13 05:36:23 +0900
  * [MDEV-19794](https://jira.mariadb.org/browse/MDEV-19794) Spider crash with XA
* [Revision #e12ed97675](https://github.com/MariaDB/server/commit/e12ed97675)\
  2020-08-12 16:23:36 +0200
  * Fix merge.
* [Revision #32798e154f](https://github.com/MariaDB/server/commit/32798e154f)\
  2020-08-12 14:43:15 +0300
  * [MDEV-23397](https://jira.mariadb.org/browse/MDEV-23397) fixup: Remove removed options from tests
* Merge [Revision #0e34bb3e97](https://github.com/MariaDB/server/commit/0e34bb3e97) 2020-08-12 14:39:53 +0300 - Merge 10.5 into 10.6
* [Revision #1ddff751eb](https://github.com/MariaDB/server/commit/1ddff751eb)\
  2020-08-10 21:38:51 +0900
  * MENT-807 Crash with CREATE TEMPORARY TABLE .. ENGINE=SPIDER .. wrapper "odbc"
* [Revision #09be96ff08](https://github.com/MariaDB/server/commit/09be96ff08)\
  2020-08-05 10:10:33 +0900
  * \[Spider] Add add checking default\_value for default\_file, host, port
* [Revision #5585c9f984](https://github.com/MariaDB/server/commit/5585c9f984)\
  2020-07-01 09:10:22 +0900
  * add a table parameter "driver" to Spider
* [Revision #0dffe33c93](https://github.com/MariaDB/server/commit/0dffe33c93)\
  2020-07-01 08:59:45 +0900
  * add a table parameter "filedsn" to Spider
* [Revision #e685809a3b](https://github.com/MariaDB/server/commit/e685809a3b)\
  2020-08-04 12:51:59 +0300
  * [MDEV-23397](https://jira.mariadb.org/browse/MDEV-23397) Remove deprecated InnoDB options in 10.6
* [Revision #2f4bcc2494](https://github.com/MariaDB/server/commit/2f4bcc2494)\
  2020-08-04 07:57:11 +0300
  * Post-merge fix: Change one more 10.6
* Merge [Revision #9a7948e3f6](https://github.com/MariaDB/server/commit/9a7948e3f6) 2020-08-04 07:55:16 +0300 - Merge 10.5 into 10.6
* [Revision #56990b18d9](https://github.com/MariaDB/server/commit/56990b18d9)\
  2020-07-20 08:08:00 +0200
  * [MDEV-23224](https://jira.mariadb.org/browse/MDEV-23224) better defaults for Windows native threadpool implementation
* [Revision #f026d4df61](https://github.com/MariaDB/server/commit/f026d4df61)\
  2020-07-15 21:54:07 +0300
  * [MDEV-21612](https://jira.mariadb.org/browse/MDEV-21612): Fix -Wunused-function for -DEMBEDDED\_LIBRARY
* [Revision #d2ca5e4811](https://github.com/MariaDB/server/commit/d2ca5e4811)\
  2020-07-15 20:30:00 +0900
  * change version for spider\_rewrite to 10.7
* [Revision #d61c800308](https://github.com/MariaDB/server/commit/d61c800308)\
  2020-07-14 16:24:50 +0300
  * [MDEV-23024](https://jira.mariadb.org/browse/MDEV-23024) Remove Cassandra Storage Engine
* [Revision #b0d2a59d9a](https://github.com/MariaDB/server/commit/b0d2a59d9a)\
  2020-07-08 18:31:00 +0200
  * [MDEV-21612](https://jira.mariadb.org/browse/MDEV-21612) - remove COM\_MULTI from server and C/C
* [Revision #1a2b494100](https://github.com/MariaDB/server/commit/1a2b494100)\
  2020-07-08 17:38:59 +0200
  * [MDEV-23124](https://jira.mariadb.org/browse/MDEV-23124) Eliminate the overhead of system call access() on every USE(or connection)
* [Revision #7148b84673](https://github.com/MariaDB/server/commit/7148b84673)\
  2020-07-08 20:43:57 +0530
  * [MDEV-13694](https://jira.mariadb.org/browse/MDEV-13694): Wrong result upon GROUP BY with orderby\_uses\_equalities=on
* [Revision #9701759b3d](https://github.com/MariaDB/server/commit/9701759b3d)\
  2020-07-04 18:24:40 +0200
  * [MDEV-23043](https://jira.mariadb.org/browse/MDEV-23043) Refactor Windows service handling
* Merge [Revision #d46576b35a](https://github.com/MariaDB/server/commit/d46576b35a) 2020-07-04 18:14:41 +0200 - merge 10.5
* Merge [Revision #272828a171](https://github.com/MariaDB/server/commit/272828a171) 2020-07-03 21:49:45 +0200 - Merge branch '10.5' into 10.6
* [Revision #d15c839c0d](https://github.com/MariaDB/server/commit/d15c839c0d)\
  2020-06-26 14:43:56 +0200
  * [MDEV-22990](https://jira.mariadb.org/browse/MDEV-22990) Threadpool : Optimize network/named pipe IO for Windows
* [Revision #b3acad4a48](https://github.com/MariaDB/server/commit/b3acad4a48)\
  2020-05-28 17:59:53 +0200
  * Update server.cnf section to mariadb-10.6
* [Revision #97b4686e2c](https://github.com/MariaDB/server/commit/97b4686e2c)\
  2020-05-16 00:19:00 +0200
  * [MDEV-7021](https://jira.mariadb.org/browse/MDEV-7021) allow config file parameter for mysql\_install\_db.exe
* [Revision #e2bc029211](https://github.com/MariaDB/server/commit/e2bc029211)\
  2020-05-11 22:01:40 +0200
  * [MDEV-7021](https://jira.mariadb.org/browse/MDEV-7021) Pass directory security descriptor from mysql\_install\_db.exe to bootstrap
* [Revision #d9b81210fd](https://github.com/MariaDB/server/commit/d9b81210fd)\
  2020-05-01 18:06:50 +0200
  * [MDEV-22175](https://jira.mariadb.org/browse/MDEV-22175) windows installer - create SeLockMemoryPrivilege for Service account
* [Revision #a42a0979c5](https://github.com/MariaDB/server/commit/a42a0979c5)\
  2020-04-30 09:53:36 +0200
  * Fix whitespacing (end of line space)
* [Revision #e7b139ca57](https://github.com/MariaDB/server/commit/e7b139ca57)\
  2020-04-30 09:52:40 +0200
  * Look also for mariadbd.exe when looking for mariadb service.
* [Revision #8cb3060c5c](https://github.com/MariaDB/server/commit/8cb3060c5c)\
  2020-04-28 01:06:11 +0200
  * [MDEV-22272](https://jira.mariadb.org/browse/MDEV-22272) Windows installer - run service unter virtual service account
* [Revision #57e654f59b](https://github.com/MariaDB/server/commit/57e654f59b)\
  2020-05-16 09:40:18 +0300
  * Bugfix: Typo in 4501c7e875 that made mariadb-client-core conflict itself
* [Revision #3dd0b2a340](https://github.com/MariaDB/server/commit/3dd0b2a340)\
  2020-05-15 17:35:47 +0200
  * Update 10.6 man pages
* [Revision #4501c7e875](https://github.com/MariaDB/server/commit/4501c7e875)\
  2020-05-14 18:00:13 +0300
  * Deb: Rename relevant occurrences of 10.5 to 10.6 now in 10.6 series
* [Revision #20fa250959](https://github.com/MariaDB/server/commit/20fa250959)\
  2020-05-14 12:38:52 +0300
  * Change version to 10.6.0
* [Revision #7924158496](https://github.com/MariaDB/server/commit/7924158496)\
  2020-05-14 10:11:47 +0300
  * [MDEV-19780](https://jira.mariadb.org/browse/MDEV-19780) Remove the TokuDB storage engine

**Do not use&#x20;**_**alpha**_**&#x20;releases in production!**

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
