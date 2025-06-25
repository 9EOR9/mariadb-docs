# MariaDB 10.10.1 Changelog

The most recent release of [MariaDB 10.10](../../old-releases/release-notes-mariadb-10-10-series/what-is-mariadb-1010.md) is:[**MariaDB 10.10.7**](../../old-releases/release-notes-mariadb-10-10-series/mariadb-10-10-7-release-notes.md) **Stable (GA)** [Download Now](https://downloads.mariadb.org/mariadb/10.10.7)

[Download 10.10.1](https://downloads.mariadb.org/mariadb/10.10.1/)[Release Notes](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/changelogs/changelogs-mariadb-10-10-series/broken-reference/README.md)[Changelog](mariadb-10101-changelog.md)[Overview of 10.10](../../old-releases/release-notes-mariadb-10-10-series/what-is-mariadb-1010.md)

**Release date:** 22 Aug 2022

For the highlights of this release, see the[release notes](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/changelogs/changelogs-mariadb-10-10-series/broken-reference/README.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/server/tree/10.10) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Changes from [10.10.0](../../old-releases/release-notes-mariadb-10-10-series/mariadb-10100-release-notes.md) are also included in this changelog
* Includes all fixes from [MariaDB 10.9.2](../changelogs-mariadb-109-series/mariadb-1092-changelog.md)
* [Revision #b74dbcb157](https://github.com/MariaDB/server/commit/b74dbcb157)\
  2022-08-09 14:21:38 +0200
  * [MDEV-23149](https://jira.mariadb.org/browse/MDEV-23149) Server crashes in my\_convert / ErrConvString::ptr / Item\_char\_typecast::check\_truncation\_with\_warn
* [Revision #9d2b28d7cc](https://github.com/MariaDB/server/commit/9d2b28d7cc)\
  2022-08-09 13:12:13 +0200
  * bump the version
* [Revision #d8f172c11c](https://github.com/MariaDB/server/commit/d8f172c11c)\
  2022-02-25 13:54:59 +0400
  * [MDEV-27266](https://jira.mariadb.org/browse/MDEV-27266) Improve UCA collation performance for utf8mb3 and utf8mb4
* [Revision #a0858b2cff](https://github.com/MariaDB/server/commit/a0858b2cff)\
  2022-02-24 17:54:52 +0400
  * [MDEV-27265](https://jira.mariadb.org/browse/MDEV-27265) Improve contraction performance in UCA collations
* [Revision #133446828c](https://github.com/MariaDB/server/commit/133446828c)\
  2021-11-28 16:55:15 +0400
  * [MDEV-27009](https://jira.mariadb.org/browse/MDEV-27009) Add UCA-14.0.0 collations
* [Revision #6bc10f8026](https://github.com/MariaDB/server/commit/6bc10f8026)\
  2021-11-28 16:48:13 +0400
  * [MDEV-27009](https://jira.mariadb.org/browse/MDEV-27009) Add UCA-14.0.0 collations - adding version aware implicit weight handling
* [Revision #d7ffb7c3dd](https://github.com/MariaDB/server/commit/d7ffb7c3dd)\
  2021-11-25 06:48:17 +0400
  * [MDEV-27009](https://jira.mariadb.org/browse/MDEV-27009) Add UCA-14.0.0 collations - dump logical positions and contractions
* [Revision #0736c03d56](https://github.com/MariaDB/server/commit/0736c03d56)\
  2021-11-24 15:11:49 +0400
  * [MDEV-27009](https://jira.mariadb.org/browse/MDEV-27009) Add UCA-14.0.0 collations - Adding implicit weight handling for Unicode-14.0.0
* [Revision #bb84f61a26](https://github.com/MariaDB/server/commit/bb84f61a26)\
  2021-11-23 16:33:08 +0400
  * [MDEV-27009](https://jira.mariadb.org/browse/MDEV-27009) Add UCA-14.0.0 collations - adding uca-dump into build targets
* [Revision #45e0373a78](https://github.com/MariaDB/server/commit/45e0373a78)\
  2022-06-12 22:01:56 +0200
  * [MDEV-28632](https://jira.mariadb.org/browse/MDEV-28632) Change default of explicit\_defaults\_for\_timestamp to ON
* [Revision #c38b8f49b8](https://github.com/MariaDB/server/commit/c38b8f49b8)\
  2022-07-03 17:35:27 +0200
  * cleanup: consolidate binlog-related THD::\*\_used into one bitmap
* [Revision #4ce1470a70](https://github.com/MariaDB/server/commit/4ce1470a70)\
  2022-07-29 12:39:37 +0200
  * cleanup: tests
* Merge [Revision #1c192843f2](https://github.com/MariaDB/server/commit/1c192843f2) 2022-08-10 14:19:15 +0200 - Merge branch '10.9' into 10.10
* Merge [Revision #47d5cfc650](https://github.com/MariaDB/server/commit/47d5cfc650) 2022-08-09 09:47:48 +0200 - Merge branch 'bb-10.9-release' into bb-10.10-release
* Merge [Revision #adddde76a1](https://github.com/MariaDB/server/commit/adddde76a1) 2022-08-09 09:00:00 +0200 - Merge branch 'bb-10.8-release' into bb-10.9-release
* [Revision #fccbe2bf99](https://github.com/MariaDB/server/commit/fccbe2bf99)\
  2022-08-09 08:59:29 +0200
  * fix tests
* Merge [Revision #4c18f68d59](https://github.com/MariaDB/server/commit/4c18f68d59) 2022-08-09 09:47:16 +0200 - Merge branch '10.9' into 10.10
* Merge [Revision #564d374704](https://github.com/MariaDB/server/commit/564d374704) 2022-08-08 17:17:45 +0200 - Merge branch '10.8' into 10.9
* Merge [Revision #50b270525a](https://github.com/MariaDB/server/commit/50b270525a) 2022-08-08 17:15:13 +0200 - Merge branch '10.7' into 10.8
* [Revision #360d99429c](https://github.com/MariaDB/server/commit/360d99429c)\
  2022-06-27 12:29:10 -0600
  * [MDEV-27161](https://jira.mariadb.org/browse/MDEV-27161): Add option for SQL thread to limit maximum execution time per query replicated
* [Revision #7864d955f3](https://github.com/MariaDB/server/commit/7864d955f3)\
  2022-06-12 10:39:15 +0300
  * Fixed regression on SST tests. We incorrectly used my\_thread\_end(), which sets mysys\_var pointer to NULL, so the next THD::THD will crash. Removed my\_thread\_init()/end() pairs and because Wsrep\_allowlist\_service::allowlist\_cb is not always called from a new thread added a thread to do so.
* [Revision #15783d7ce5](https://github.com/MariaDB/server/commit/15783d7ce5)\
  2022-08-02 17:24:50 +0300
  * Test cleanup
* [Revision #7fdc993ec6](https://github.com/MariaDB/server/commit/7fdc993ec6)\
  2021-12-16 09:39:26 +0100
  * [MDEV-27263](https://jira.mariadb.org/browse/MDEV-27263) Cluster bootstrap node shows duplicate wsrep allowlist IP warning messages on each restart.
* [Revision #9743d0043e](https://github.com/MariaDB/server/commit/9743d0043e)\
  2021-11-22 13:04:40 +0100
  * [MDEV-27246](https://jira.mariadb.org/browse/MDEV-27246) Implement a method to add IPs to allowlist for Galera Cluster node addresses that can make SST/IST requests
* [Revision #b3372d6422](https://github.com/MariaDB/server/commit/b3372d6422)\
  2022-07-29 19:39:55 +0200
  * use my\_random\_bytes() that correctly detects error conditions
* [Revision #2119647f7d](https://github.com/MariaDB/server/commit/2119647f7d)\
  2022-07-29 19:26:17 +0200
  * remove dead code
* [Revision #0caa6bf14e](https://github.com/MariaDB/server/commit/0caa6bf14e)\
  2022-07-27 17:46:49 +0200
  * [MDEV-25704](https://jira.mariadb.org/browse/MDEV-25704) more tests
* [Revision #3607da3c4e](https://github.com/MariaDB/server/commit/3607da3c4e)\
  2022-07-27 17:05:51 +0200
  * [MDEV-25704](https://jira.mariadb.org/browse/MDEV-25704) RANDOM\_BYTES - post-review fixes
* [Revision #d7e3265dd3](https://github.com/MariaDB/server/commit/d7e3265dd3)\
  2022-07-23 15:58:13 +1000
  * [MDEV-29154](https://jira.mariadb.org/browse/MDEV-29154) Excessive warnings upon a call to RANDOM\_BYTES
* [Revision #7f06f68108](https://github.com/MariaDB/server/commit/7f06f68108)\
  2022-07-19 14:01:17 +1000
  * [MDEV-29108](https://jira.mariadb.org/browse/MDEV-29108) RANDOM\_BYTES - assertion in Create\_tmp\_table::finalize
* [Revision #a95268c5b3](https://github.com/MariaDB/server/commit/a95268c5b3)\
  2022-07-06 14:14:53 +1000
  * [MDEV-29028](https://jira.mariadb.org/browse/MDEV-29028) Queries using RANDOM\_BYTES get stored in query cache
* [Revision #8b9ac5bfe0](https://github.com/MariaDB/server/commit/8b9ac5bfe0)\
  2022-07-05 17:37:26 +1000
  * [MDEV-29029](https://jira.mariadb.org/browse/MDEV-29029) RANDOM\_BYTES cannot be virtual column
* [Revision #3c2b0cac52](https://github.com/MariaDB/server/commit/3c2b0cac52)\
  2022-02-13 23:19:02 +1000
  * [MDEV-25704](https://jira.mariadb.org/browse/MDEV-25704) Add RANDOM\_BYTES function
* [Revision #0fbbf2ee78](https://github.com/MariaDB/server/commit/0fbbf2ee78)\
  2022-07-30 09:37:35 +0300
  * [MDEV-19801](https://jira.mariadb.org/browse/MDEV-19801): Correct a test result
* [Revision #e3543c6c8a](https://github.com/MariaDB/server/commit/e3543c6c8a)\
  2022-07-30 09:20:54 +0300
  * [MDEV-28929](https://jira.mariadb.org/browse/MDEV-28929) fixup: Adjust a test result
* [Revision #e1caa4bd5e](https://github.com/MariaDB/server/commit/e1caa4bd5e)\
  2022-06-17 21:20:43 +0200
  * don't use ssl for windows named pipes - it doesn't work
* [Revision #ce9385b73c](https://github.com/MariaDB/server/commit/ce9385b73c)\
  2022-05-23 12:43:22 +0200
  * [MDEV-27105](https://jira.mariadb.org/browse/MDEV-27105) --ssl option set as default for mariadb CLI
* Merge [Revision #4ce6e78059](https://github.com/MariaDB/server/commit/4ce6e78059) 2022-07-28 11:25:21 +0300 - Merge 10.9 into 10.10
* [Revision #0149abf66f](https://github.com/MariaDB/server/commit/0149abf66f)\
  2022-07-28 11:23:41 +0300
  * [MDEV-28929](https://jira.mariadb.org/browse/MDEV-28929) fixup: Adjust a test result.
* [Revision #24174cfdfc](https://github.com/MariaDB/server/commit/24174cfdfc)\
  2022-07-18 11:43:57 +0200
  * fix func\_encrypt\_nossl test to work as it was supposed to
* [Revision #fe8b99dd5c](https://github.com/MariaDB/server/commit/fe8b99dd5c)\
  2022-06-18 23:23:28 +0200
  * [MDEV-27104](https://jira.mariadb.org/browse/MDEV-27104) deprecate DES\_ENCRYPT/DECRYPT functions
* [Revision #90c3b2835d](https://github.com/MariaDB/server/commit/90c3b2835d)\
  2022-06-07 20:06:42 -0600
  * [MDEV-20122](https://jira.mariadb.org/browse/MDEV-20122): Deprecate MASTER\_USE\_GTID=Current\_Pos to favor new MASTER\_DEMOTE\_TO\_SLAVE option
* [Revision #5ab5ff08b0](https://github.com/MariaDB/server/commit/5ab5ff08b0)\
  2022-05-23 14:14:00 -0600
  * [MDEV-19801](https://jira.mariadb.org/browse/MDEV-19801): Change defaults for CHANGE MASTER TO so that GTID-based replication is used by default if master supports it
* [Revision #8c2faad576](https://github.com/MariaDB/server/commit/8c2faad576)\
  2022-07-19 14:13:17 +0300
  * [MDEV-28929](https://jira.mariadb.org/browse/MDEV-28929): Plan selection takes forever with [MDEV-28852](https://jira.mariadb.org/browse/MDEV-28852) ... Part #2: Extend heuristic pruning to use multiple tables as the "Model tables".
* [Revision #afadd58ee5](https://github.com/MariaDB/server/commit/afadd58ee5)\
  2022-07-07 19:57:38 +0400
  * [MDEV-28881](https://jira.mariadb.org/browse/MDEV-28881) Fix memory leak caused by STL usage
* [Revision #c03d50fccf](https://github.com/MariaDB/server/commit/c03d50fccf)\
  2022-07-06 16:00:12 +0400
  * [MDEV-28881](https://jira.mariadb.org/browse/MDEV-28881) Server crash in Dep\_analysis\_context::create\_table\_value
* [Revision #7f0201a2b5](https://github.com/MariaDB/server/commit/7f0201a2b5)\
  2022-02-17 22:53:37 +0700
  * [MDEV-26278](https://jira.mariadb.org/browse/MDEV-26278) Add functionality to eliminate derived tables from the query
* [Revision #1f0187ff8d](https://github.com/MariaDB/server/commit/1f0187ff8d)\
  2022-06-03 13:24:18 +0300
  * Reduced size of POSITION
* [Revision #fbbc63453b](https://github.com/MariaDB/server/commit/fbbc63453b)\
  2022-06-03 11:55:23 +0300
  * Added current\_cost and best\_cost to optimizer trace when pruning by cost
* [Revision #515b9ad05a](https://github.com/MariaDB/server/commit/515b9ad05a)\
  2022-06-02 19:47:23 +0300
  * Added EQ\_REF chaining to the greedy\_optimizer
* [Revision #6e7376eb59](https://github.com/MariaDB/server/commit/6e7376eb59)\
  2022-06-01 17:11:40 +0300
  * Remove unnecessary testing of join dependency when sorting tables
* [Revision #318a74f1aa](https://github.com/MariaDB/server/commit/318a74f1aa)\
  2022-06-01 15:56:24 +0300
  * Added get\_allowed\_nj\_tables() to speed up gready\_search()
* [Revision #b3c74bdc1f](https://github.com/MariaDB/server/commit/b3c74bdc1f)\
  2022-05-31 17:36:32 +0300
  * Improve pruning in greedy\_search by sorting tables during search
* [Revision #213772f99a](https://github.com/MariaDB/server/commit/213772f99a)\
  2022-07-25 11:44:10 +0300
  * Revert the commit with [MDEV-28926](https://jira.mariadb.org/browse/MDEV-28926): Add time spent on query optimizer to JSON ANALYZE
* [Revision #2ccdfba8ee](https://github.com/MariaDB/server/commit/2ccdfba8ee)\
  2022-07-18 17:48:01 +0200
  * [MDEV-28926](https://jira.mariadb.org/browse/MDEV-28926) Add time spent on query optimizer to JSON ANALYZE (#2193)
* [Revision #88b22356e6](https://github.com/MariaDB/server/commit/88b22356e6)\
  2022-06-08 15:12:03 +0400
  * [MDEV-23287](https://jira.mariadb.org/browse/MDEV-23287) The INET4 data type
* Merge [Revision #975b40ea99](https://github.com/MariaDB/server/commit/975b40ea99) 2022-06-29 16:22:45 +0300 - Merge 10.9 into 10.10
* Merge [Revision #63961a08a6](https://github.com/MariaDB/server/commit/63961a08a6) 2022-06-28 12:33:39 +0300 - Merge 10.9 into 10.10
* Merge [Revision #ada82805da](https://github.com/MariaDB/server/commit/ada82805da) 2022-06-23 13:48:09 +0300 - Merge 10.9 into 10.10
* Merge [Revision #9810a4ecdf](https://github.com/MariaDB/server/commit/9810a4ecdf) 2022-06-21 18:27:54 +0300 - Merge 10.9 into 10.10
* Merge [Revision #891bf1d8ce](https://github.com/MariaDB/server/commit/891bf1d8ce) 2022-06-20 10:18:52 +0300 - Merge 10.9 into 10.10
* [Revision #f774c33a9d](https://github.com/MariaDB/server/commit/f774c33a9d)\
  2022-06-20 12:57:47 +0900
  * [MDEV-27809](https://jira.mariadb.org/browse/MDEV-27809) Spider: remove #ifdef SPIDER\_I\_S\_USE\_SHOW\_FOR\_COLUMN
* [Revision #0aadb58e22](https://github.com/MariaDB/server/commit/0aadb58e22)\
  2022-06-20 00:25:56 +0900
  * [MDEV-27811](https://jira.mariadb.org/browse/MDEV-27811) Spider: remove #ifdef SPIDER\_MDEV\_16246
* Merge [Revision #d371e35257](https://github.com/MariaDB/server/commit/d371e35257) 2022-06-17 11:31:53 +0300 - Merge 10.9 into 10.10
* Merge [Revision #a629d3b703](https://github.com/MariaDB/server/commit/a629d3b703) 2022-06-17 08:37:01 +0200 - Merge branch '10.9' into 10.10
* [Revision #dcb780d28f](https://github.com/MariaDB/server/commit/dcb780d28f)\
  2022-06-17 14:31:07 +0900
  * [MDEV-27808](https://jira.mariadb.org/browse/MDEV-27808) Spider: remove #ifdef SPIDER\_LIKE\_FUNC\_HAS\_GET\_NEGATED
* [Revision #970aa41176](https://github.com/MariaDB/server/commit/970aa41176)\
  2022-06-15 22:13:50 +0900
  * [MDEV-28362](https://jira.mariadb.org/browse/MDEV-28362) Spider: remove #ifdef SPIDER\_ITEM\_STRING\_WITHOUT\_SET\_STR\_WITH\_COPY
* Merge [Revision #51a4fcd565](https://github.com/MariaDB/server/commit/51a4fcd565) 2022-06-15 10:07:31 +0300 - Merge 10.9 into 10.10
* Merge [Revision #32edabd1f2](https://github.com/MariaDB/server/commit/32edabd1f2) 2022-06-09 15:26:09 +0300 - Merge 10.9 into 10.10
* [Revision #978eb616ca](https://github.com/MariaDB/server/commit/978eb616ca)\
  2022-05-10 22:26:36 +0900
  * [MDEV-27256](https://jira.mariadb.org/browse/MDEV-27256) Delete spider\_use\_handler and related code (3/3)
* [Revision #57d233e2a6](https://github.com/MariaDB/server/commit/57d233e2a6)\
  2022-06-09 17:20:05 +0900
  * [MDEV-27256](https://jira.mariadb.org/browse/MDEV-27256) Delete spider\_use\_handler and related code (2/3)
* [Revision #48409dd929](https://github.com/MariaDB/server/commit/48409dd929)\
  2022-05-10 11:20:49 +0900
  * [MDEV-27256](https://jira.mariadb.org/browse/MDEV-27256) Delete spider\_use\_handler and related code (1/3)
* [Revision #8756d253f3](https://github.com/MariaDB/server/commit/8756d253f3)\
  2022-06-08 14:12:13 +0900
  * [MDEV-28364](https://jira.mariadb.org/browse/MDEV-28364) Spider: remove #ifdef SPIDER\_HAS\_EXPR\_CACHE\_ITEM
* Merge [Revision #d491062368](https://github.com/MariaDB/server/commit/d491062368) 2022-06-07 09:42:02 +0300 - Merge 10.9 into 10.10
* [Revision #039d83b8a7](https://github.com/MariaDB/server/commit/039d83b8a7)\
  2022-06-07 09:39:28 +0300
  * [MDEV-28554](https://jira.mariadb.org/browse/MDEV-28554) fixup: Do not overflow the ib\_logfile0 header
* [Revision #fdc039db29](https://github.com/MariaDB/server/commit/fdc039db29)\
  2022-05-13 18:07:39 +0300
  * [MDEV-28540](https://jira.mariadb.org/browse/MDEV-28540) Deprecate and ignore the parameter innodb\_prefix\_index\_cluster\_optimization
* [Revision #0dab74ff3f](https://github.com/MariaDB/server/commit/0dab74ff3f)\
  2022-05-13 16:39:45 +0300
  * [MDEV-28539](https://jira.mariadb.org/browse/MDEV-28539) Some InnoDB counters are duplicating generic SHOW STATUS
* [Revision #6b9bba41e8](https://github.com/MariaDB/server/commit/6b9bba41e8)\
  2022-05-25 09:20:04 +0300
  * [MDEV-28554](https://jira.mariadb.org/browse/MDEV-28554): Remove innodb\_version
* [Revision #12aeb9fa15](https://github.com/MariaDB/server/commit/12aeb9fa15)\
  2022-05-13 16:13:13 +0300
  * [MDEV-28542](https://jira.mariadb.org/browse/MDEV-28542) Useless output in SHOW ENGINE INNODB STATUS
* [Revision #643fd51db5](https://github.com/MariaDB/server/commit/643fd51db5)\
  2022-05-31 22:43:53 +0900
  * [MDEV-28365](https://jira.mariadb.org/browse/MDEV-28365) Spider: remove #ifdef SPIDER\_ITEM\_HAS\_CMP\_TYPE
* [Revision #081a284712](https://github.com/MariaDB/server/commit/081a284712)\
  2022-05-31 11:38:02 +0900
  * [MDEV-28360](https://jira.mariadb.org/browse/MDEV-28360) Spider: remove #ifdef SPIDER\_use\_LEX\_CSTRING\_for\_KEY\_Field\_name
* [Revision #b3df1ec97a](https://github.com/MariaDB/server/commit/b3df1ec97a)\
  2022-05-19 19:18:26 +0000
  * [MDEV-24815](https://jira.mariadb.org/browse/MDEV-24815) Add 'allow-suspicious-udfs' and 'skip-grant-tables' to system variables
* Merge [Revision #3cc8539d84](https://github.com/MariaDB/server/commit/3cc8539d84) 2022-05-25 09:15:08 +0300 - Merge 10.9 into 10.10
* [Revision #956d93b581](https://github.com/MariaDB/server/commit/956d93b581)\
  2022-05-19 13:26:54 +0300
  * [MDEV-28587](https://jira.mariadb.org/browse/MDEV-28587): Remove '-10.9' suffixes entries from Debian control Conflicts/Replaces
* [Revision #289b9e4155](https://github.com/MariaDB/server/commit/289b9e4155)\
  2022-05-20 01:40:59 +0900
  * [MDEV-28361](https://jira.mariadb.org/browse/MDEV-28361) Spider: remove #ifdef SPIDER\_ITEM\_STRING\_WITHOUT\_SET\_STR\_WITH\_COPY\_AND\_THDPTR
* [Revision #6b5a629ec3](https://github.com/MariaDB/server/commit/6b5a629ec3)\
  2022-05-19 23:37:54 +0900
  * [MDEV-28359](https://jira.mariadb.org/browse/MDEV-28359) Spider: remove #ifdef SPIDER\_HAS\_MY\_CHARLEN
* [Revision #77a18e8217](https://github.com/MariaDB/server/commit/77a18e8217)\
  2022-05-14 16:37:23 +0900
  * [MDEV-28006](https://jira.mariadb.org/browse/MDEV-28006) Delete Spider plugin variables regarding UDFs and related code
* [Revision #e98e8c7f7e](https://github.com/MariaDB/server/commit/e98e8c7f7e)\
  2022-05-15 19:08:55 +0300
  * Adjust plugin maturity in test result
* Merge [Revision #7eb47aa414](https://github.com/MariaDB/server/commit/7eb47aa414) 2022-05-14 18:07:10 +0300 - Merge 10.9 into 10.10
* [Revision #4652c1775b](https://github.com/MariaDB/server/commit/4652c1775b)\
  2022-05-13 13:54:14 +0300
  * Create a 10.10 branch

{% @marketo/form formid="4316" formId="4316" %}
