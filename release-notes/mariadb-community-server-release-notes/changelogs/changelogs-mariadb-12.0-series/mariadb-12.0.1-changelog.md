# MariaDB 12.0.1 Changelog

<a href="https://mariadb.com/downloads" class="button primary">Download</a>  <a href="../../release-notes-mariadb-12.0-rolling-releases/mariadb-12.0.1-release-notes.md" class="button secondary">Release Notes</a>  <a href="mariadb-12.0.1-changelog.md" class="button secondary">Changelog</a>  <a href="../../release-notes-mariadb-12.0-rolling-releases/what-is-mariadb-120.md" class="button secondary">Overview of 12.0</a>

[<sup>_Alternate download from mariadb.org_</sup>](https://downloads.mariadb.org/mariadb/12.0.1/)

For the highlights of this release, see the [release notes](../../release-notes-mariadb-12.0-rolling-releases/mariadb-12.0.1-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On [GitHub](https://github.com/MariaDB/server/tree/11.8) you can view more details of the revision and view diffs of the code modified in that revision.

* Includes all fixes from [MariaDB 11.8.2](../changelogs-mariadb-10-8-series/mariadb-1082-changelog.md)
* <sup>_Merge_</sup> [<sup>_Revision #f1102da37a_</sup>](https://github.com/MariaDB/server/commit/f1102da37a) <sup>_2025-05-22 09:22:55 +0200 - Merge branch '11.8' into 12.0_</sup>
* [Revision #00a9afb581](https://github.com/MariaDB/server/commit/00a9afb581) 2025-05-09 20:28:19 +0700
  * Fix unstable opt\_hints\_join\_order.test
* [Revision #51c0afcd24](https://github.com/MariaDB/server/commit/51c0afcd24) 2024-09-26 04:27:56 +0200
  * [MDEV-34822](https://jira.mariadb.org/browse/MDEV-34822) addendum: minor test corrections after fix
* [Revision #1cb59a9bd4](https://github.com/MariaDB/server/commit/1cb59a9bd4) 2024-08-16 12:45:38 +0300
  * [MDEV-34822](https://jira.mariadb.org/browse/MDEV-34822): Skip FK checks in Galera during applying in IST
* [Revision #c5d8b9963a](https://github.com/MariaDB/server/commit/c5d8b9963a) 2025-04-30 14:04:43 +0400
  * [MDEV-36716](https://jira.mariadb.org/browse/MDEV-36716) A case expression with ROW arguments in THEN crashes
* [Revision #4fc1063796](https://github.com/MariaDB/server/commit/4fc1063796) 2025-05-05 12:36:06 +0700
  * [MDEV-34870](https://jira.mariadb.org/browse/MDEV-34870) Fix post-rebase conflicts
* [Revision #b11767846f](https://github.com/MariaDB/server/commit/b11767846f) 2025-04-30 13:28:44 +0700
  * [MDEV-36486](https://jira.mariadb.org/browse/MDEV-36486) Forbid placing optimizer hints at the INSERT part of INSERT..SELECT
* [Revision #fa929a2be6](https://github.com/MariaDB/server/commit/fa929a2be6) 2025-04-08 16:59:28 +0700
  * [MDEV-36486](https://jira.mariadb.org/browse/MDEV-36486) Optimizer hints are resolved against the INSERT part of INSERT..SELECT
* [Revision #b89a1e7f35](https://github.com/MariaDB/server/commit/b89a1e7f35) 2025-04-07 21:06:06 +0300
  * [MDEV-36169](https://jira.mariadb.org/browse/MDEV-36169): Two subqueries with LOOSESCAN hints create invalid query plan
* [Revision #453a86f68e](https://github.com/MariaDB/server/commit/453a86f68e) 2025-02-21 13:48:28 +0700
  * [MDEV-36133](https://jira.mariadb.org/browse/MDEV-36133) BNL() hint doesn't work with join\_cache\_level>=5
* [Revision #6e2a0501b6](https://github.com/MariaDB/server/commit/6e2a0501b6) 2025-04-22 21:47:12 +0700
  * [MDEV-36638](https://jira.mariadb.org/browse/MDEV-36638) Some optimizer hint warnings are returned as errors
* [Revision #6cd27dbc43](https://github.com/MariaDB/server/commit/6cd27dbc43) 2025-04-26 14:06:24 +0700
  * [MDEV-33281](https://jira.mariadb.org/browse/MDEV-33281) Fix after-rebase commits
* [Revision #0737d8f35d](https://github.com/MariaDB/server/commit/0737d8f35d) 2025-04-26 13:50:30 +0700
  * [MDEV-33281](https://jira.mariadb.org/browse/MDEV-33281) Fix mysql-test-run to correctly handle hints
* [Revision #a0e89070cc](https://github.com/MariaDB/server/commit/a0e89070cc) 2025-04-23 19:26:58 +0700
  * [MDEV-36675](https://jira.mariadb.org/browse/MDEV-36675) Optimizer hints parser catches irrelevant \`thd->is\_error()\` set by multi-RENAME TABLE
* [Revision #349f5bf2da](https://github.com/MariaDB/server/commit/349f5bf2da) 2025-01-30 20:56:36 +0700
  * [MDEV-34870](https://jira.mariadb.org/browse/MDEV-34870): implement join order hints
* [Revision #c4fe794d22](https://github.com/MariaDB/server/commit/c4fe794d22) 2024-12-08 22:03:01 +0200
  * [MDEV-33281](https://jira.mariadb.org/browse/MDEV-33281) Optimizer hints code cleanup: - remove get\_args\_printer() from hints printing - add append\_hint\_arguments(THD \*thd, opt\_hints\_enum hint, String \*str) - add more comments - rename st\_opt\_hint\_info::hint\_name to hint\_type - add pptimizer trace support for hints - add dbug\_print\_hints() - make print\_warn() not be a template - introduce Printable\_parser\_rule interface, make grammar rules that emit warnings implement it and print\_warn invokes its function) - remove Parser::Hint::append\_args() as it is not used anywhere (it used to be necessary call print\_warn(... (Parser::Hint\*)NULL);
* [Revision #0e088b5d7e](https://github.com/MariaDB/server/commit/0e088b5d7e) 2024-12-07 21:15:32 +0700
  * [MDEV-34860](https://jira.mariadb.org/browse/MDEV-34860) Fix opt\_hint\_timeout.test for embedded; fix mariadb client
* [Revision #d2918e10fc](https://github.com/MariaDB/server/commit/d2918e10fc) 2024-12-06 14:12:26 +0200
  * [MDEV-33281](https://jira.mariadb.org/browse/MDEV-33281) Optimizer hints cleanup: - add a comment that opt\_hints\_global->check\_unresolved() is never called - improve comments - rename everything with "resolved\_children" to "fully\_resolved\_children" - Opt\_hints\_table::adjust\_key\_hints() now returns value - less "reach-back-to-parent" logic - rename Hint "adjustment" and "resolution" (yes, both terms were used) to "fixing". "Resolution" is already used for parse-tree objects
* [Revision #2c8f6058c1](https://github.com/MariaDB/server/commit/2c8f6058c1) 2024-09-11 19:53:57 +0700
  * [MDEV-34888](https://jira.mariadb.org/browse/MDEV-34888) Implement SEMIJOIN() and SUBQUERY() hints
* [Revision #e3bf4c826c](https://github.com/MariaDB/server/commit/e3bf4c826c) 2024-12-02 14:01:47 +0700
  * [MDEV-34860](https://jira.mariadb.org/browse/MDEV-34860) Make the hint override global/session/statement setting of max\_statement\_time
* [Revision #af14196b8a](https://github.com/MariaDB/server/commit/af14196b8a) 2024-11-27 14:34:24 +0700
  * [MDEV-33281](https://jira.mariadb.org/browse/MDEV-33281) Make BNL() hint enable hashed join buffers
* [Revision #67319f3e8d](https://github.com/MariaDB/server/commit/67319f3e8d) 2024-08-07 22:10:50 +0700
  * [MDEV-34860](https://jira.mariadb.org/browse/MDEV-34860) Implement MAX\_EXECUTION\_TIME hint
* [Revision #1e2774d829](https://github.com/MariaDB/server/commit/1e2774d829) 2024-09-16 21:53:20 +0700
  * [MDEV-33281](https://jira.mariadb.org/browse/MDEV-33281) Make BNL() hint work for join\_cache\_levels from 0 to 3
* [Revision #e4af72bd5d](https://github.com/MariaDB/server/commit/e4af72bd5d) 2024-09-10 18:59:08 +0300
  * [MDEV-33281](https://jira.mariadb.org/browse/MDEV-33281) Optimizer hints cleanup: add \`const\` specifiers, comments
* [Revision #cd9ac306c3](https://github.com/MariaDB/server/commit/cd9ac306c3) 2024-08-30 21:50:32 +0700
  * [MDEV-33281](https://jira.mariadb.org/browse/MDEV-33281) Make BNL() hint work for join\_cache\_level=0
* [Revision #1cd928c297](https://github.com/MariaDB/server/commit/1cd928c297) 2024-08-21 13:55:44 +0700
  * [MDEV-33281](https://jira.mariadb.org/browse/MDEV-33281) Implement optimizer hints
* [Revision #4bb2669d18](https://github.com/MariaDB/server/commit/4bb2669d18) 2024-07-17 16:50:14 +0700
  * [MDEV-33281](https://jira.mariadb.org/browse/MDEV-33281) Optimizer hints Cleanup: fix formatting, rename objects
* [Revision #bd30c796fa](https://github.com/MariaDB/server/commit/bd30c796fa) 2024-07-15 14:29:47 +0400
  * [MDEV-33281](https://jira.mariadb.org/browse/MDEV-33281) Implement optimizer hints
* [Revision #877e4a386c](https://github.com/MariaDB/server/commit/877e4a386c) 2024-07-05 19:10:36 +0700
  * [MDEV-33281](https://jira.mariadb.org/browse/MDEV-33281) Implement optimizer hints
* [Revision #6340c23933](https://github.com/MariaDB/server/commit/6340c23933) 2024-06-21 12:26:28 +0400
  * [MDEV-33281](https://jira.mariadb.org/browse/MDEV-33281) Implement optimizer hints
* [Revision #495d96709f](https://github.com/MariaDB/server/commit/495d96709f) 2025-04-15 11:17:57 +1000
  * [MDEV-35866](https://jira.mariadb.org/browse/MDEV-35866) CHECK TABLE get number of rows without HA\_STATS\_RECORDS\_IS\_EXACT
* [Revision #d52ddae57b](https://github.com/MariaDB/server/commit/d52ddae57b) 2025-05-02 10:44:45 +1000
  * [MDEV-22491](https://jira.mariadb.org/browse/MDEV-22491) Support mariadb-check and CHECK TABLE with SEQUENCE
* [Revision #26ea37be5d](https://github.com/MariaDB/server/commit/26ea37be5d) 2025-04-25 17:45:59 +0200
  * [MDEV-36405](https://jira.mariadb.org/browse/MDEV-36405) Session tracking does not report changes from COM\_CHANGE\_USER
* [Revision #07de0ac69e](https://github.com/MariaDB/server/commit/07de0ac69e) 2025-02-23 12:59:38 +0100
  * [MDEV-20299](https://jira.mariadb.org/browse/MDEV-20299) SET SESSION AUTHORIZATION
* [Revision #0f4a35a327](https://github.com/MariaDB/server/commit/0f4a35a327) 2025-03-03 11:43:49 +0100
  * cleanup: extract reusable code chunks
* [Revision #78d23a3e60](https://github.com/MariaDB/server/commit/78d23a3e60) 2025-03-02 17:47:03 +0100
  * fix error messages
* [Revision #02b81afff8](https://github.com/MariaDB/server/commit/02b81afff8) 2025-02-21 20:55:54 +0100
  * cleanup: THD::change\_user
* [Revision #fa47c73561](https://github.com/MariaDB/server/commit/fa47c73561) 2025-03-19 22:20:35 +0100
  * [MDEV-12182](https://jira.mariadb.org/browse/MDEV-12182) post-merge
* [Revision #1aba30b8f9](https://github.com/MariaDB/server/commit/1aba30b8f9) 2024-06-04 23:58:37 +0000
  * [MDEV-12182](https://jira.mariadb.org/browse/MDEV-12182) Add Client TCP Port Number to MySQL Audit Plugin Logs
* [Revision #c1f2b5a141](https://github.com/MariaDB/server/commit/c1f2b5a141) 2025-03-19 21:33:46 +0100
  * [MDEV-33834](https://jira.mariadb.org/browse/MDEV-33834) post-merge
* [Revision #2b464774f2](https://github.com/MariaDB/server/commit/2b464774f2) 2024-02-23 19:40:13 +0000
  * [MDEV-33834](https://jira.mariadb.org/browse/MDEV-33834) Extend audit plugin to include tls\_version and tls\_version\_length variables
* [Revision #88cc11dc54](https://github.com/MariaDB/server/commit/88cc11dc54) 2025-04-29 13:28:31 -0600
  * [MDEV-36714](https://jira.mariadb.org/browse/MDEV-36714): Rows\_log\_event::write\_data\_header overallocates buffer size
* [Revision #3e9e1a25b7](https://github.com/MariaDB/server/commit/3e9e1a25b7) 2025-04-29 19:06:32 +0200
  * [MDEV-36566](https://jira.mariadb.org/browse/MDEV-36566) SELECT create\_temporary\_table\_binlog\_formats should show exactly what it is SET to
* [Revision #ee9359de89](https://github.com/MariaDB/server/commit/ee9359de89) 2025-04-30 12:32:50 +0200
  * [MDEV-36425](https://jira.mariadb.org/browse/MDEV-36425) fix test results
* [Revision #c29e83f226](https://github.com/MariaDB/server/commit/c29e83f226) 2025-03-11 22:48:54 -0600
  * [MDEV-30189](https://jira.mariadb.org/browse/MDEV-30189) Add remaining replication options as system variables
* [Revision #74c189c312](https://github.com/MariaDB/server/commit/74c189c312) 2025-04-29 09:57:52 -0600
  * [MDEV-35304](https://jira.mariadb.org/browse/MDEV-35304): Fix multi\_source.connects\_tried
* [Revision #e1da2c3d67](https://github.com/MariaDB/server/commit/e1da2c3d67) 2025-04-25 16:29:35 +0200
  * increase tolerance in socket\_summary\_check.inc
* [Revision #16c4621400](https://github.com/MariaDB/server/commit/16c4621400) 2025-02-18 12:49:31 +0100
  * remove unused non-standard tokens from the parser
* [Revision #11f6b9d12a](https://github.com/MariaDB/server/commit/11f6b9d12a) 2025-02-15 16:42:53 +0100
  * remove features that were deprecated in 10.5
* [Revision #24fd8c7856](https://github.com/MariaDB/server/commit/24fd8c7856) 2025-02-15 16:21:11 +0100
  * update deprecation.h to match the latest policy changes
* [Revision #068fc787ee](https://github.com/MariaDB/server/commit/068fc787ee) 2025-04-29 17:00:32 +1000
  * [MDEV-36168](https://jira.mariadb.org/browse/MDEV-36168) ASAN error in Item\_func\_latlongfromgeohash::decode\_geohash (postfix)
* [Revision #36dfe08672](https://github.com/MariaDB/server/commit/36dfe08672) 2025-03-31 21:46:50 -0500
  * Clarify .frm field parsing comments: use C-style block comments, reposition loop comment, and add end marker
* [Revision #1b95e46524](https://github.com/MariaDB/server/commit/1b95e46524) 2025-04-07 20:13:58 +0300
  * Fix typos in mysql-test/
* [Revision #40c5b62531](https://github.com/MariaDB/server/commit/40c5b62531) 2025-04-21 18:27:56 +0300
  * Fix remaining typos
* [Revision #bc87abc381](https://github.com/MariaDB/server/commit/bc87abc381) 2025-04-25 12:02:22 -0400
  * [MDEV-36694](https://jira.mariadb.org/browse/MDEV-36694) spatial\_utility\_function{\_collect,\_isvalid} broken for --view-protocol
* [Revision #4042652d7f](https://github.com/MariaDB/server/commit/4042652d7f) 2025-04-17 10:32:09 +0300
  * Improvements to mtr
* [Revision #ce8a74f235](https://github.com/MariaDB/server/commit/ce8a74f235) 2025-03-31 20:07:13 +0300
  * [MDEV-36425](https://jira.mariadb.org/browse/MDEV-36425) Extend read\_only to also block share locks and super user
* [Revision #595e834946](https://github.com/MariaDB/server/commit/595e834946) 2025-03-26 16:49:59 +0200
  * Galera mtr results updated
* [Revision #23eb9d6821](https://github.com/MariaDB/server/commit/23eb9d6821) 2025-03-25 17:02:19 +0200
  * Improve mtr replication setup
* [Revision #bb5ae63aef](https://github.com/MariaDB/server/commit/bb5ae63aef) 2025-03-09 22:15:23 +0200
  * Add memory allocated by my\_once\_alloc() to memory status
* [Revision #2c4fee8376](https://github.com/MariaDB/server/commit/2c4fee8376) 2025-02-26 14:38:54 +0200
  * Fixed that HA\_EXTRA\_FLUSH in Aria and MyISAM flushes all data to disk
* [Revision #7728b90a0d](https://github.com/MariaDB/server/commit/7728b90a0d) 2025-02-09 18:46:02 +0200
  * Removed possible deadlock betwen LOCK\_log and LOCK\_global\_system\_variables
* [Revision #f099f778b3](https://github.com/MariaDB/server/commit/f099f778b3) 2025-01-26 20:17:17 +0200
  * Do not log ALTER table to ddl log for REPAIR
* [Revision #aae9b50a53](https://github.com/MariaDB/server/commit/aae9b50a53) 2025-01-20 19:30:19 +0200
  * Added VALGRIND\_YIELD to be able to abort from busy loops
* [Revision #d9c3b775b8](https://github.com/MariaDB/server/commit/d9c3b775b8) 2025-01-05 17:33:10 +0200
  * Comment and indentation improvements
* [Revision #4992aaf9a2](https://github.com/MariaDB/server/commit/4992aaf9a2) 2025-01-05 17:32:39 +0200
  * Always use all arguments for ddl\_log\_write\_execute\_entry()
* [Revision #c234a312d7](https://github.com/MariaDB/server/commit/c234a312d7) 2025-01-05 14:50:45 +0200
  * Added make\_tmp\_table\_name() to simplify creating temporary table names
* [Revision #efc5d3f84d](https://github.com/MariaDB/server/commit/efc5d3f84d) 2025-01-14 10:59:06 +0200
  * rename binlog\_show\_create\_table\_() to binlog\_show\_create\_table()
* [Revision #1f85eeeb53](https://github.com/MariaDB/server/commit/1f85eeeb53) 2022-08-31 11:55:02 +0300
  * [MDEV-25292](https://jira.mariadb.org/browse/MDEV-25292) Refactoring: moved select\_field\_count into Alter\_info.
* [Revision #f8ba5ced55](https://github.com/MariaDB/server/commit/f8ba5ced55) 2025-02-15 14:08:11 +0200
  * [MDEV-36099](https://jira.mariadb.org/browse/MDEV-36099) Ensure that creation and usage of temporary tables in replication is predictable
* [Revision #a9bdfccbc6](https://github.com/MariaDB/server/commit/a9bdfccbc6) 2025-03-12 10:46:09 +1100
  * [MDEV-34712](https://jira.mariadb.org/browse/MDEV-34712) Add support to sha2 and pbkdf2 key derivation in file\_key\_management
* [Revision #ec6f320883](https://github.com/MariaDB/server/commit/ec6f320883) 2025-04-10 11:25:41 +1000
  * [MDEV-32732](https://jira.mariadb.org/browse/MDEV-32732) Support DESC indexes in loose scan optimization
* [Revision #8c6a606429](https://github.com/MariaDB/server/commit/8c6a606429) 2025-04-26 14:27:10 +0200
  * Workaround ICC compiler bug
* [Revision #cbd6755869](https://github.com/MariaDB/server/commit/cbd6755869) 2025-03-10 21:42:14 -0600
  * [MDEV-27669](https://jira.mariadb.org/browse/MDEV-27669): Add \`skip-slave-start\` info message
* [Revision #48a20c737f](https://github.com/MariaDB/server/commit/48a20c737f) 2025-04-22 15:46:16 -0400
  * Fix MSAN failures in main.gis and main.spatial\_utility\_function\_validate
* [Revision #7a1c3666d7](https://github.com/MariaDB/server/commit/7a1c3666d7) 2025-04-21 09:03:31 -0400
  * Fix conflict on rebase of GIS functions to main branch
* [Revision #db49003660](https://github.com/MariaDB/server/commit/db49003660) 2025-04-15 06:40:45 -0400
  * Initialize pointers to avoid MSAN warnings
* [Revision #1a8854fdba](https://github.com/MariaDB/server/commit/1a8854fdba) 2025-04-07 09:25:43 -0400
  * [MDEV-36491](https://jira.mariadb.org/browse/MDEV-36491) Server crashes in Item\_func\_group\_concat::print
* [Revision #eaba4975c9](https://github.com/MariaDB/server/commit/eaba4975c9) 2025-03-28 10:30:33 -0400
  * [MDEV-36167](https://jira.mariadb.org/browse/MDEV-36167) Assertion in Item\_sum\_st with st\_collect and group by
* [Revision #1528ad075a](https://github.com/MariaDB/server/commit/1528ad075a) 2025-03-27 10:55:57 -0400
  * [MDEV-34158](https://jira.mariadb.org/browse/MDEV-34158) st\_geohash error reporting and null handling
* [Revision #53f82a9c3d](https://github.com/MariaDB/server/commit/53f82a9c3d) 2025-03-18 15:01:45 -0400
  * [MDEV-36042](https://jira.mariadb.org/browse/MDEV-36042) Assertion failed in Binary\_string::q\_append
* [Revision #29c9dbb883](https://github.com/MariaDB/server/commit/29c9dbb883) 2025-03-26 16:53:30 -0400
  * [MDEV-36168](https://jira.mariadb.org/browse/MDEV-36168) ASAN error in Item\_func\_latlongfromgeohash::decode\_geohash
* [Revision #8055a00ab5](https://github.com/MariaDB/server/commit/8055a00ab5) 2025-03-18 14:21:30 -0400
  * Fix spatial\_utility\_function\_simplify 'unknown column' errors
* [Revision #d5cb996270](https://github.com/MariaDB/server/commit/d5cb996270) 2025-01-29 16:46:24 -0500
  * [MDEV-35975](https://jira.mariadb.org/browse/MDEV-35975) Server crashes after CREATE VIEW as SELECT ST\_COLLECT...
* [Revision #b93e8c1556](https://github.com/MariaDB/server/commit/b93e8c1556) 2024-12-18 10:26:33 -0500
  * [MDEV-35102](https://jira.mariadb.org/browse/MDEV-35102) CREATE TABLE AS SELECT ST\_collect ... does not work
* [Revision #38cc216634](https://github.com/MariaDB/server/commit/38cc216634) 2025-03-05 15:15:53 +0400
  * [MDEV-35960](https://jira.mariadb.org/browse/MDEV-35960) st\_isvalid(NULL) should not end up with an error, but return NULL.
* [Revision #4b720b027d](https://github.com/MariaDB/server/commit/4b720b027d) 2024-12-20 16:01:03 -0500
  * [MDEV-35126](https://jira.mariadb.org/browse/MDEV-35126) Wrong results from st\_isvalid for multipolygon.
* [Revision #79a1fdd964](https://github.com/MariaDB/server/commit/79a1fdd964) 2024-12-16 15:57:17 -0500
  * [MDEV-35103](https://jira.mariadb.org/browse/MDEV-35103) CREATE TABLE AS SELECT ST\_VALIDATE creates a column with datatype point, not geometry
* [Revision #8c2a207d58](https://github.com/MariaDB/server/commit/8c2a207d58) 2024-10-24 12:12:04 -0400
  * [MDEV-35062](https://jira.mariadb.org/browse/MDEV-35062) Assertion failed in Binary\_string::q\_append
* [Revision #dc9b43a71e](https://github.com/MariaDB/server/commit/dc9b43a71e) 2024-09-17 17:10:36 -0400
  * [MDEV-34940](https://jira.mariadb.org/browse/MDEV-34940): Fix Item\_func\_collect inheritance
* [Revision #e2bb06b124](https://github.com/MariaDB/server/commit/e2bb06b124) 2024-10-02 09:50:57 -0400
  * [MDEV-34969](https://jira.mariadb.org/browse/MDEV-34969): test main.spatial\_utility\_function\_simplify fails
* [Revision #b9b38f0e4b](https://github.com/MariaDB/server/commit/b9b38f0e4b) 2024-09-16 12:22:09 -0400
  * GIS update get\_copy overrides to do\_get\_copy const
* [Revision #771ed65ba7](https://github.com/MariaDB/server/commit/771ed65ba7) 2024-09-15 08:12:17 +0200
  * GIS fixes for --view
* [Revision #2831eeeb51](https://github.com/MariaDB/server/commit/2831eeeb51) 2024-08-14 18:24:21 +0200
  * [MDEV-34278](https://jira.mariadb.org/browse/MDEV-34278): Implements DISTINCT for ST\_Collect
* [Revision #b07cf471b5](https://github.com/MariaDB/server/commit/b07cf471b5) 2021-01-08 18:26:04 +0100
  * [MDEV-34278](https://jira.mariadb.org/browse/MDEV-34278): Implement the GIS function ST\_Collect
* [Revision #b50366667b](https://github.com/MariaDB/server/commit/b50366667b) 2015-01-26 13:56:12 +0530
  * [MDEV-34137](https://jira.mariadb.org/browse/MDEV-34137): Implement the GIS function ST\_Validate
* [Revision #869b4c243e](https://github.com/MariaDB/server/commit/869b4c243e) 2024-07-02 10:56:22 +0200
  * [MDEV-34276](https://jira.mariadb.org/browse/MDEV-34276): Implements the function ST\_IsValid
* [Revision #ba66f8f37b](https://github.com/MariaDB/server/commit/ba66f8f37b) 2024-06-07 16:20:10 +0200
  * [MDEV-34141](https://jira.mariadb.org/browse/MDEV-34141): Implements the function ST\_Simplify
* [Revision #d232e4fd4f](https://github.com/MariaDB/server/commit/d232e4fd4f) 2024-07-22 17:20:07 +0200
  * fix typo spatial\_ref\_sys
* [Revision #1656b5c10f](https://github.com/MariaDB/server/commit/1656b5c10f) 2024-07-02 10:56:22 +0200
  * [MDEV-34276](https://jira.mariadb.org/browse/MDEV-34276): Implements the function ST\_IsValid
* [Revision #eac552e3db](https://github.com/MariaDB/server/commit/eac552e3db) 2024-08-05 22:41:49 +0200
  * [MDEV-34177](https://jira.mariadb.org/browse/MDEV-34177): Implements ST\_PointFromGeoHash
* [Revision #e2017a5dc0](https://github.com/MariaDB/server/commit/e2017a5dc0) 2024-07-17 17:10:31 +0200
  * [MDEV-34160](https://jira.mariadb.org/browse/MDEV-34160): Implements ST\_LongFromGeoHash
* [Revision #f357b47c70](https://github.com/MariaDB/server/commit/f357b47c70) 2024-07-17 12:31:15 +0200
  * [MDEV-34159](https://jira.mariadb.org/browse/MDEV-34159): Implements ST\_LatFromGeoHash
* [Revision #1401d2fcd0](https://github.com/MariaDB/server/commit/1401d2fcd0) 2024-06-25 22:28:57 +0200
  * [MDEV-34138](https://jira.mariadb.org/browse/MDEV-34138): Implements the function MBRCoveredBy
* [Revision #47ed8c0416](https://github.com/MariaDB/server/commit/47ed8c0416) 2014-07-24 14:18:54 +0200
  * [MDEV-34158](https://jira.mariadb.org/browse/MDEV-34158): Implement the GIS function ST\_Geohash
* [Revision #f8bc40ef5f](https://github.com/MariaDB/server/commit/f8bc40ef5f) 2025-04-14 22:14:57 -0600
  * [MDEV-36340](https://jira.mariadb.org/browse/MDEV-36340): Reset \`Connects\_Tried\` with \`Master\_Retry\_Count=X\`
* [Revision #8a95409393](https://github.com/MariaDB/server/commit/8a95409393) 2025-02-20 12:46:31 +0100
  * [MDEV-31134](https://jira.mariadb.org/browse/MDEV-31134): sync galera settings with KB doc
* [Revision #18115d392f](https://github.com/MariaDB/server/commit/18115d392f) 2025-03-27 18:27:44 -0600
  * [MDEV-35304](https://jira.mariadb.org/browse/MDEV-35304) fixup: Timing-independent MTR test
* [Revision #ddfebd48f5](https://github.com/MariaDB/server/commit/ddfebd48f5) 2021-04-04 10:21:04 -0700
  * [MDEV-23538](https://jira.mariadb.org/browse/MDEV-23538): Rename mariadb.pc to mariadb-server-embedded.pc to avoid confusion
* [Revision #ecb7c9b692](https://github.com/MariaDB/server/commit/ecb7c9b692) 2025-04-19 18:36:03 +0700
  * [MDEV-10164](https://jira.mariadb.org/browse/MDEV-10164): Add support for TRIGGERS that fire on multiple events
* [Revision #86ec20189a](https://github.com/MariaDB/server/commit/86ec20189a) 2025-02-17 14:50:01 +0100
  * [MDEV-14091](https://jira.mariadb.org/browse/MDEV-14091) Support password protected SSL key in server.
* [Revision #173b16f3bc](https://github.com/MariaDB/server/commit/173b16f3bc) 2025-01-23 22:23:07 +0000
  * [MDEV-11341](https://jira.mariadb.org/browse/MDEV-11341) STR\_TO\_DATE does not return NULL for invalid dates
* [Revision #f11504af51](https://github.com/MariaDB/server/commit/f11504af51) 2023-09-14 07:01:32 +0400
  * [MDEV-20034](https://jira.mariadb.org/browse/MDEV-20034) Add support for the pre-defined weak SYS\_REFCURSOR
* [Revision #1e00b9ec2a](https://github.com/MariaDB/server/commit/1e00b9ec2a) 2025-04-11 19:26:24 +0300
  * Fix typos in user-facing messages
* [Revision #c36cd56049](https://github.com/MariaDB/server/commit/c36cd56049) 2024-08-22 13:38:55 +0200
  * Update THIRDPARTY license file to reflect reality
* [Revision #f02ad2f641](https://github.com/MariaDB/server/commit/f02ad2f641) 2025-04-18 15:06:50 +0200
  * bump the version
* <sup>_Merge_</sup> [<sup>_Revision #9b824e62d4_</sup>](https://github.com/MariaDB/server/commit/9b824e62d4) <sup>_2025-04-18 12:07:02 +0200 - Merge branch '11.8' into main_</sup>
* [Revision #cb2d6abae1](https://github.com/MariaDB/server/commit/cb2d6abae1) 2025-01-29 18:53:39 +0000
  * [MDEV-31334](https://jira.mariadb.org/browse/MDEV-31334): Consider dates ending in 'T' as malformed
* [Revision #22efc2c784](https://github.com/MariaDB/server/commit/22efc2c784) 2025-03-23 08:08:11 +0200
  * Fix typos in C comments inside storage/
* [Revision #3b3c512feb](https://github.com/MariaDB/server/commit/3b3c512feb) 2025-03-18 10:27:40 +0100
  * [MDEV-36265](https://jira.mariadb.org/browse/MDEV-36265): Unique error for changing Domain ID with open temporary tables
* [Revision #ab468e33af](https://github.com/MariaDB/server/commit/ab468e33af) 2025-03-24 10:30:39 +0100
  * Add a sanity check for backups
* [Revision #5f7c2a617f](https://github.com/MariaDB/server/commit/5f7c2a617f) 2025-03-22 15:26:51 +0200
  * Fix typos in C comments in miscellaneous files
* [Revision #5f7e883336](https://github.com/MariaDB/server/commit/5f7e883336) 2025-03-20 18:38:09 +0400
  * [MDEV-36322](https://jira.mariadb.org/browse/MDEV-36322) Comparison ROW(stored\_func(),1)=ROW(1,1) calls the function twice per row
* [Revision #c34bb80b3d](https://github.com/MariaDB/server/commit/c34bb80b3d) 2025-03-21 16:51:56 +0100
  * MDBF-1000: wrong urls
* [Revision #31adb3030c](https://github.com/MariaDB/server/commit/31adb3030c) 2025-03-20 16:37:49 +0100
  * MDBF-1000: implement an export for the server repository
* [Revision #923094b4cd](https://github.com/MariaDB/server/commit/923094b4cd) 2025-02-19 06:52:16 -0500
  * [MDEV-36094](https://jira.mariadb.org/browse/MDEV-36094) Row ID filtering for reverse-ordered scans
* [Revision #24b5c3021d](https://github.com/MariaDB/server/commit/24b5c3021d) 2025-02-19 07:22:05 -0500
  * [MDEV-36094](https://jira.mariadb.org/browse/MDEV-36094) Row ID filtering for reverse-ordered scans
* [Revision #7e4233746e](https://github.com/MariaDB/server/commit/7e4233746e) 2025-02-10 13:56:25 -0500
  * [MDEV-34413](https://jira.mariadb.org/browse/MDEV-34413) Index Condition Pushdown for reverse ordered scans
* [Revision #261d5520a2](https://github.com/MariaDB/server/commit/261d5520a2) 2025-02-07 11:20:23 -0500
  * [MDEV-34413](https://jira.mariadb.org/browse/MDEV-34413) Index Condition Pushdown for reverse-ordered scans
* [Revision #c3f21762e9](https://github.com/MariaDB/server/commit/c3f21762e9) 2025-03-18 15:46:47 +0400
  * Corrections to parent "speedup collation" commit
* [Revision #543ebbcf8e](https://github.com/MariaDB/server/commit/543ebbcf8e) 2025-03-09 19:39:27 +0530
  * [MDEV-35876](https://jira.mariadb.org/browse/MDEV-35876) - speedup collation/charset lookup
* [Revision #feb1cf9086](https://github.com/MariaDB/server/commit/feb1cf9086) 2025-03-14 00:38:52 +0400
  * Corrections to parent "fix typos" commmit
* [Revision #717c12de0e](https://github.com/MariaDB/server/commit/717c12de0e) 2025-03-09 18:19:33 +0200
  * Fix typos in C comments inside sql/
* <sup>_Merge_</sup> [<sup>_Revision #153778437d_</sup>](https://github.com/MariaDB/server/commit/153778437d) <sup>_2025-03-05 21:20:02 +0200 - Merge 11.8 into main_</sup>
* [Revision #689bed1940](https://github.com/MariaDB/server/commit/689bed1940) 2025-02-18 14:07:14 +0200
  * [MDEV-23818](https://jira.mariadb.org/browse/MDEV-23818) mysql option --script-dir
* [Revision #3a81664cb8](https://github.com/MariaDB/server/commit/3a81664cb8) 2025-03-03 12:00:36 +0100
  * Review fixes
* [Revision #1fecf581ac](https://github.com/MariaDB/server/commit/1fecf581ac) 2025-02-25 14:27:10 +0100
  * Rewrite the 'Types' chapter in coding standards.
* [Revision #5091986cea](https://github.com/MariaDB/server/commit/5091986cea) 2025-02-10 22:29:43 -0700
  * misc. \`sql/slave.cc\` & co. refactor
* [Revision #e2dbd9b6ac](https://github.com/MariaDB/server/commit/e2dbd9b6ac) 2025-02-20 16:56:12 -0700
  * [MDEV-35304](https://jira.mariadb.org/browse/MDEV-35304): Add \`Connects\_Tried\` and \`Master\_Retry\_Count\` to SSS
* [Revision #7094a75596](https://github.com/MariaDB/server/commit/7094a75596) 2025-02-19 16:51:54 -0700
  * [MDEV-25674](https://jira.mariadb.org/browse/MDEV-25674): Add CHANGE MASTER TO master\_retry\_count
* [Revision #66f52ba630](https://github.com/MariaDB/server/commit/66f52ba630) 2025-02-04 17:38:23 -0700
  * slave.cc \`try\_to\_reconnect\` remove \`retry\_counter\`
* [Revision #3a43b7c60b](https://github.com/MariaDB/server/commit/3a43b7c60b) 2025-02-06 23:01:45 +0000
  * [MDEV-36124](https://jira.mariadb.org/browse/MDEV-36124) Fix missing binary failures from test\_upgrade.sh
* [Revision #c92add291e](https://github.com/MariaDB/server/commit/c92add291e) 2025-02-12 11:16:50 +0100
  * 12.0 branch

{% include "https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/~/reusable/vX1KAy0t1XuYJaGsK28T/" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
