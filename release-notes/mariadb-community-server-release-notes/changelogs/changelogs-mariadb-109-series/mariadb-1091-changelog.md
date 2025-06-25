# MariaDB 10.9.1 Changelog

The most recent release of [MariaDB 10.9](../../old-releases/release-notes-mariadb-10-9-series/what-is-mariadb-109.md) is:[**MariaDB 10.9.8**](../../old-releases/release-notes-mariadb-10-9-series/mariadb-10-9-8-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.9.8/)

[Download 10.9.1](https://mariadb.org/download/?tab=mariadb\&release=10.9.1\&product=mariadb)[Release Notes](../../old-releases/release-notes-mariadb-10-9-series/mariadb-1091-release-notes.md)[Changelog](mariadb-1091-changelog.md)[Overview of 10.9](../../old-releases/release-notes-mariadb-10-9-series/what-is-mariadb-109.md)

**Release date:** 20 May 2022

For the highlights of this release, see the[release notes](../../old-releases/release-notes-mariadb-10-9-series/mariadb-1091-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/server/tree/10.9) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Changes from 10.9.0 are also included in this changelog
* Includes all fixes from [MariaDB 10.8.3](../changelogs-mariadb-10-8-series/mariadb-1083-changelog.md)
* Merge [Revision #f14f13a1c9](https://github.com/MariaDB/server/commit/f14f13a1c9) 2022-05-18 15:04:50 +0200 - Merge branch '10.8' into 10.9
* [Revision #5dba54bfef](https://github.com/MariaDB/server/commit/5dba54bfef)\
  2022-05-14 20:24:09 +0300
  * Correct misplaced parentheses in an assertion
* [Revision #f1ac8305bc](https://github.com/MariaDB/server/commit/f1ac8305bc)\
  2022-05-14 13:02:51 +0300
  * [MDEV-20119](https://jira.mariadb.org/browse/MDEV-20119) fixup: GCC 12 -Wmaybe-uninitialized, -Wunused-but-set-variable
* [Revision #ee2613c730](https://github.com/MariaDB/server/commit/ee2613c730)\
  2022-05-13 17:02:12 +0200
  * Versions fix
* [Revision #353746918b](https://github.com/MariaDB/server/commit/353746918b)\
  2022-05-07 19:10:59 +0300
  * Optimizer trace: Make ref\_optimizer\_key\_uses\[\*] show the index name
* [Revision #b9adaeb491](https://github.com/MariaDB/server/commit/b9adaeb491)\
  2022-05-12 10:55:18 +0400
  * [MDEV-28481](https://jira.mariadb.org/browse/MDEV-28481) SIGSEGV in Lex\_charset\_collation\_st::find\_bin\_collation
* [Revision #404984980f](https://github.com/MariaDB/server/commit/404984980f)\
  2022-05-10 08:22:21 +0200
  * [MDEV-28500](https://jira.mariadb.org/browse/MDEV-28500): Hashicorp: Debian packaging is broken
* [Revision #2e14f2c889](https://github.com/MariaDB/server/commit/2e14f2c889)\
  2022-05-06 15:01:08 +0200
  * [MDEV-28279](https://jira.mariadb.org/browse/MDEV-28279): Hashicorp: Cannot migrate hexadecimal keys from file key management
* [Revision #94841ba656](https://github.com/MariaDB/server/commit/94841ba656)\
  2022-04-29 18:01:34 +0200
  * Hashicorp plugin: typo fixed
* [Revision #8ae5408cab](https://github.com/MariaDB/server/commit/8ae5408cab)\
  2022-04-29 06:57:18 +0200
  * [MDEV-28442](https://jira.mariadb.org/browse/MDEV-28442): Hashicorp: refactoring to wrap static variables into a class
* [Revision #e571174e80](https://github.com/MariaDB/server/commit/e571174e80)\
  2022-04-28 15:06:16 +0200
  * [MDEV-28291](https://jira.mariadb.org/browse/MDEV-28291): Hashicorp: Cache variables claim to be dynamic but changes are ignored
* [Revision #0902cfaec8](https://github.com/MariaDB/server/commit/0902cfaec8)\
  2022-04-28 14:56:41 +0200
  * [MDEV-28330](https://jira.mariadb.org/browse/MDEV-28330): Hashicorp: Key caching doesn't appear to be working
* [Revision #3d1f765066](https://github.com/MariaDB/server/commit/3d1f765066)\
  2022-04-19 04:34:48 +0200
  * [MDEV-28276](https://jira.mariadb.org/browse/MDEV-28276): Hashicorp: checking that kv storage is created with version 2+
* [Revision #1c22a9d8ae](https://github.com/MariaDB/server/commit/1c22a9d8ae)\
  2022-04-28 13:33:23 +0200
  * [MDEV-28277](https://jira.mariadb.org/browse/MDEV-28277): Checking for mandatory "/v1/" prefix in the URL
* [Revision #35989d9cc1](https://github.com/MariaDB/server/commit/35989d9cc1)\
  2022-04-28 13:10:39 +0200
  * [MDEV-28281](https://jira.mariadb.org/browse/MDEV-28281): Hashicorp: Key ID is not indicated in the log record
* [Revision #0c5d8b8730](https://github.com/MariaDB/server/commit/0c5d8b8730)\
  2022-04-18 16:44:28 +0200
  * [MDEV-28275](https://jira.mariadb.org/browse/MDEV-28275): Hashicorp: ASAN heap-use-after-free in get\_version()
* [Revision #1146b713b2](https://github.com/MariaDB/server/commit/1146b713b2)\
  2020-07-13 19:12:00 +0200
  * [MDEV-19281](https://jira.mariadb.org/browse/MDEV-19281): Plugin implementation for the Hashicorp Vault KMS
* [Revision #706a8232da](https://github.com/MariaDB/server/commit/706a8232da)\
  2022-05-06 10:45:18 +0300
  * [MDEV-25477](https://jira.mariadb.org/browse/MDEV-25477) Auto-create breaks replication when triggering event was not replicated
* [Revision #92bfc0e8c4](https://github.com/MariaDB/server/commit/92bfc0e8c4)\
  2022-05-06 10:45:17 +0300
  * [MDEV-17554](https://jira.mariadb.org/browse/MDEV-17554) Auto-create new partition for system versioned tables with history partitioned by INTERVAL/LIMIT
* [Revision #75ede427e4](https://github.com/MariaDB/server/commit/75ede427e4)\
  2022-05-06 10:45:17 +0300
  * [MDEV-27328](https://jira.mariadb.org/browse/MDEV-27328) Change of SYSTEM\_TIME partitioning options is not possible without data copy
* [Revision #93e64d1f58](https://github.com/MariaDB/server/commit/93e64d1f58)\
  2022-05-06 10:45:17 +0300
  * cleanup: log\_current\_statement and OPTION\_KEEP\_LOG
* [Revision #c8bcb6e809](https://github.com/MariaDB/server/commit/c8bcb6e809)\
  2022-05-06 12:00:01 +1000
  * Deb: dh\_missing --fail-missing - columnstore
* [Revision #e6df7a4c9f](https://github.com/MariaDB/server/commit/e6df7a4c9f)\
  2022-05-06 10:25:25 +1000
  * Deb: dh\_missing --fail-missing/ man3 pages
* [Revision #d426d0782d](https://github.com/MariaDB/server/commit/d426d0782d)\
  2022-05-02 22:07:58 -0700
  * Deb: Use --fail-missing and ensure the not-installed list is up-to-date
* [Revision #a82cdb0690](https://github.com/MariaDB/server/commit/a82cdb0690)\
  2022-04-30 23:27:39 -0700
  * Deb: Finalize the version less Debian package transition
* [Revision #dde5988306](https://github.com/MariaDB/server/commit/dde5988306)\
  2022-04-30 23:14:19 -0700
  * Deb: Don't Conflicts/Replaces with a 10.9 provided by the same package
* [Revision #ff1d8fa7b0](https://github.com/MariaDB/server/commit/ff1d8fa7b0)\
  2022-05-02 20:31:15 -0700
  * Deb: Clean away Buster to Bookworm upgrade tests in Salsa-CI
* [Revision #e3a7d13b11](https://github.com/MariaDB/server/commit/e3a7d13b11)\
  2022-04-30 23:14:59 -0700
  * Deb: Remove from Salsa-CI buster-backports as it does not have libfmt 7+
* [Revision #2c52941423](https://github.com/MariaDB/server/commit/2c52941423)\
  2022-05-04 00:23:27 -0700
  * Deb: Run wrap-and-sort -av
* [Revision #0b14dbd45b](https://github.com/MariaDB/server/commit/0b14dbd45b)\
  2022-05-02 09:21:19 +0300
  * [MDEV-28124](https://jira.mariadb.org/browse/MDEV-28124) fixup: Tests depend on PLUGIN\_PERFSCHEMA
* [Revision #4d03269425](https://github.com/MariaDB/server/commit/4d03269425)\
  2022-05-02 09:14:32 +0300
  * After-merge fixes
* [Revision #9841a8080b](https://github.com/MariaDB/server/commit/9841a8080b)\
  2022-04-29 11:49:42 +0300
  * Fix comment.
* Merge [Revision #94dc0bffa3](https://github.com/MariaDB/server/commit/94dc0bffa3) 2022-04-29 11:09:52 +0300 - Merge [MDEV-27021](https://jira.mariadb.org/browse/MDEV-27021), [MDEV-10000](https://jira.mariadb.org/browse/MDEV-10000) into 10.9
* [Revision #8db9aa496c](https://github.com/MariaDB/server/commit/8db9aa496c)\
  2022-04-26 23:29:29 +0300
  * [MDEV-28268](https://jira.mariadb.org/browse/MDEV-28268): Server crashes in Expression\_cache\_tracker::fetch\_current\_stats
* [Revision #3f68c2169e](https://github.com/MariaDB/server/commit/3f68c2169e)\
  2022-04-04 12:32:22 +0300
  * [MDEV-28201](https://jira.mariadb.org/browse/MDEV-28201): Server crashes upon SHOW ANALYZE/EXPLAIN FORMAT=JSON
* [Revision #02c3babdec](https://github.com/MariaDB/server/commit/02c3babdec)\
  2022-03-27 11:58:27 +0700
  * [MDEV-28124](https://jira.mariadb.org/browse/MDEV-28124) Server crashes in Explain\_aggr\_filesort::print\_json\_members
* [Revision #a0475cb9ca](https://github.com/MariaDB/server/commit/a0475cb9ca)\
  2022-02-16 13:03:46 +0700
  * [MDEV-27021](https://jira.mariadb.org/browse/MDEV-27021) Add explicit indication of SHOW EXPLAIN/ANALYZE.
* [Revision #d1a1ad4c28](https://github.com/MariaDB/server/commit/d1a1ad4c28)\
  2022-02-02 19:44:43 +0700
  * [MDEV-27021](https://jira.mariadb.org/browse/MDEV-27021) Add support of FORMAT=JSON for SHOW ANALYZE
* [Revision #e7fcd496d4](https://github.com/MariaDB/server/commit/e7fcd496d4)\
  2021-12-24 17:27:03 +0300
  * [MDEV-27021](https://jira.mariadb.org/browse/MDEV-27021) Implement SHOW ANALYZE command
* [Revision #328684833b](https://github.com/MariaDB/server/commit/328684833b)\
  2022-01-11 20:25:11 +0300
  * [MDEV-10000](https://jira.mariadb.org/browse/MDEV-10000) Add EXPLAIN \[FORMAT=JSON] FOR CONNECTION syntax support
* [Revision #51b28b24ca](https://github.com/MariaDB/server/commit/51b28b24ca)\
  2022-04-28 10:06:47 -0600
  * [MDEV-28435](https://jira.mariadb.org/browse/MDEV-28435): rpl.rpl\_mysqlbinlog\_slave\_consistency fails intermittently on tables comparison
* Merge [Revision #504a3b32f6](https://github.com/MariaDB/server/commit/504a3b32f6) 2022-04-28 15:54:03 +0300 - Merge 10.8 into 10.9
* [Revision #43fa8e0b8f](https://github.com/MariaDB/server/commit/43fa8e0b8f)\
  2022-04-18 22:30:20 +0530
  * [MDEV-28319](https://jira.mariadb.org/browse/MDEV-28319): Assertion \`cur\_step->type & JSON\_PATH\_KEY' failed in json\_find\_path
* [Revision #4730a6982f](https://github.com/MariaDB/server/commit/4730a6982f)\
  2022-04-19 21:43:31 +0530
  * [MDEV-28350](https://jira.mariadb.org/browse/MDEV-28350): Test failing on buildbot with UBSAN
* [Revision #3716eaff4e](https://github.com/MariaDB/server/commit/3716eaff4e)\
  2022-04-18 15:31:36 +0530
  * [MDEV-28326](https://jira.mariadb.org/browse/MDEV-28326): Server crashes in json\_path\_parts\_compare
* [Revision #375b8f40ce](https://github.com/MariaDB/server/commit/375b8f40ce)\
  2022-04-11 11:32:26 +0300
  * [MDEV-27033](https://jira.mariadb.org/browse/MDEV-27033): Remove version suffix from Debian packages
* [Revision #72a1250585](https://github.com/MariaDB/server/commit/72a1250585)\
  2022-03-09 20:50:49 +0530
  * [MDEV-28029](https://jira.mariadb.org/browse/MDEV-28029): No warnings if server starts with "--old" Analysis: When --old option is used, the corresponding --old-mode variables are set but warning is not given. Fix: Use sql\_print\_warning() to give warning.
* [Revision #5945e420f1](https://github.com/MariaDB/server/commit/5945e420f1)\
  2021-08-13 15:49:16 +0530
  * [MDEV-24920](https://jira.mariadb.org/browse/MDEV-24920): Merge "old" SQL variable to "old\_mode" sql variable
* [Revision #c132bce1a1](https://github.com/MariaDB/server/commit/c132bce1a1)\
  2022-02-03 08:31:05 -0700
  * [MDEV-20119](https://jira.mariadb.org/browse/MDEV-20119): Implement the --do-domain-ids, --ignore-domain-ids, and --ignore-server-ids options for mysqlbinlog
* [Revision #f326b43cb9](https://github.com/MariaDB/server/commit/f326b43cb9)\
  2022-04-15 01:28:33 +0530
  * Fixing merge conflicts for 10.9 json task and related bugs
* [Revision #c69d72c2e4](https://github.com/MariaDB/server/commit/c69d72c2e4)\
  2022-03-21 12:43:17 +0530
  * [MDEV-28072](https://jira.mariadb.org/browse/MDEV-28072): JSON\_EXTRACT has inconsistent behavior with '0' value in json path (when range is used)
* [Revision #95a9078efc](https://github.com/MariaDB/server/commit/95a9078efc)\
  2022-03-21 21:19:10 +0530
  * [MDEV-28071](https://jira.mariadb.org/browse/MDEV-28071): JSON\_EXISTS returns always 1 if it is used range notation for json path Analysis: When searching for the given path in json string, if the current step is of array range type, then path was considered reached which meant path exists. So output was always true. The end indexes of range were not evaluated. Fix: If the current step type for a path is array range, then check if the value array\_counter\[] is in range of n\_item and n\_item\_end. If it is, then path exists. Only then return true. If the range criteria is never met then return false.
* [Revision #e6511a39f8](https://github.com/MariaDB/server/commit/e6511a39f8)\
  2022-03-18 18:12:59 +0530
  * vcol.wrong\_arena failing on buildbot when current date is '2022-03-17'
* [Revision #c781cefd8a](https://github.com/MariaDB/server/commit/c781cefd8a)\
  2022-03-05 01:03:49 +0530
  * [MDEV-27911](https://jira.mariadb.org/browse/MDEV-27911): Implement range notation for json path
* [Revision #abe9712194](https://github.com/MariaDB/server/commit/abe9712194)\
  2022-03-01 16:14:36 +0530
  * [MDEV-27972](https://jira.mariadb.org/browse/MDEV-27972): Unexpected behavior with negative zero (-0) in JSON Path
* [Revision #dfcbb30a92](https://github.com/MariaDB/server/commit/dfcbb30a92)\
  2021-11-22 22:59:30 +0530
  * [MDEV-22224](https://jira.mariadb.org/browse/MDEV-22224): Support JSON Path negative index
* Merge [Revision #e98013cb5c](https://github.com/MariaDB/server/commit/e98013cb5c) 2022-04-13 13:39:00 +0300 - Merge 10.8 into 10.9
* [Revision #bea47a6f59](https://github.com/MariaDB/server/commit/bea47a6f59)\
  2022-04-13 15:05:19 +1000
  * [MDEV-27791](https://jira.mariadb.org/browse/MDEV-27791): rocksdb\_log\_dir test postfix
* [Revision #1ac87d6dd4](https://github.com/MariaDB/server/commit/1ac87d6dd4)\
  2022-01-19 23:40:41 +0000
  * [MDEV-27791](https://jira.mariadb.org/browse/MDEV-27791): Create a new MyRocks parameter rocksdb\_log\_dir
* [Revision #ef8d203a31](https://github.com/MariaDB/server/commit/ef8d203a31)\
  2022-04-12 11:33:52 +0300
  * Added scripts/wsrep\_sst\_backup to .gitignore
* [Revision #22f7190e85](https://github.com/MariaDB/server/commit/22f7190e85)\
  2022-04-12 11:32:02 +0300
  * [MDEV-28074](https://jira.mariadb.org/browse/MDEV-28074) mysqldump --order-by-size
* [Revision #161fd2d29c](https://github.com/MariaDB/server/commit/161fd2d29c)\
  2022-04-07 23:49:19 -0700
  * [MDEV-28226](https://jira.mariadb.org/browse/MDEV-28226) Spider: remove #ifdef HANDLER\_HAS\_NEED\_INFO\_FOR\_AUTO\_INC
* Merge [Revision #6cb6ba8b7b](https://github.com/MariaDB/server/commit/6cb6ba8b7b) 2022-04-06 13:33:33 +0300 - Merge 10.8 into 10.9
* Merge [Revision #7ae46ced37](https://github.com/MariaDB/server/commit/7ae46ced37) 2022-04-06 14:33:27 +1000 - Merge branch 10.8 into 10.9
* [Revision #ef930dcad5](https://github.com/MariaDB/server/commit/ef930dcad5)\
  2022-03-31 22:55:11 +0900
  * Spider: Remove unnecessary files for Autotools
* [Revision #f76da7f662](https://github.com/MariaDB/server/commit/f76da7f662)\
  2022-02-10 16:51:49 +0900
  * [MDEV-27474](https://jira.mariadb.org/browse/MDEV-27474) Spider: remove #WITH\_PARTITION\_STORAGE\_ENGINE
* [Revision #3eb1e11d8a](https://github.com/MariaDB/server/commit/3eb1e11d8a)\
  2022-01-26 03:02:45 +0530
  * [MDEV-23479](https://jira.mariadb.org/browse/MDEV-23479): Add a THD\* argument to Item\_func\_or\_sum::fix\_length\_and\_dec()
* [Revision #12abe61af4](https://github.com/MariaDB/server/commit/12abe61af4)\
  2022-03-03 14:40:55 +0530
  * [MDEV-27990](https://jira.mariadb.org/browse/MDEV-27990): Incorrect behavior of JSON\_OVERLAPS() on warning
* [Revision #a653dde279](https://github.com/MariaDB/server/commit/a653dde279)\
  2022-01-30 15:45:25 +0530
  * [MDEV-27677](https://jira.mariadb.org/browse/MDEV-27677): Implement JSON\_OVERLAPS()
* Merge [Revision #8680eedb26](https://github.com/MariaDB/server/commit/8680eedb26) 2022-03-30 09:41:14 +0300 - Merge 10.8 into 10.9
* [Revision #0c4c064f98](https://github.com/MariaDB/server/commit/0c4c064f98)\
  2022-02-09 21:21:39 +0400
  * [MDEV-27743](https://jira.mariadb.org/browse/MDEV-27743) Remove Lex::charset
* [Revision #d25b10fede](https://github.com/MariaDB/server/commit/d25b10fede)\
  2022-02-09 17:59:38 +0400
  * [MDEV-27712](https://jira.mariadb.org/browse/MDEV-27712) Reduce the size of Lex\_length\_and\_dec\_st from 16 to 8
* [Revision #ab1a792571](https://github.com/MariaDB/server/commit/ab1a792571)\
  2022-03-22 04:40:04 +0100
  * [MDEV-26971](https://jira.mariadb.org/browse/MDEV-26971) post-fix: fixes for SST scripts
* [Revision #12ce9b4f02](https://github.com/MariaDB/server/commit/12ce9b4f02)\
  2022-03-16 10:14:48 +0200
  * Fix compile error.
* [Revision #a686c10e87](https://github.com/MariaDB/server/commit/a686c10e87)\
  2022-02-17 17:19:07 +0200
  * [MDEV-26971](https://jira.mariadb.org/browse/MDEV-26971): Implement progress reporting by mariabackup SST script
* [Revision #eceb9e2478](https://github.com/MariaDB/server/commit/eceb9e2478)\
  2022-02-17 17:14:04 +0200
  * [MDEV-26971](https://jira.mariadb.org/browse/MDEV-26971): JSON file interface to wsrep node state.
* [Revision #7878eae95e](https://github.com/MariaDB/server/commit/7878eae95e)\
  2022-02-10 08:51:48 +0200
  * Small fixes Add new requirement for pv tool for debian and rpm Fix one test result difference. Set message about missing progress reporting tool pv as info.
* [Revision #73d80c8672](https://github.com/MariaDB/server/commit/73d80c8672)\
  2021-12-18 18:30:24 +0200
  * [MDEV-26971](https://jira.mariadb.org/browse/MDEV-26971): Implement progress reporting by mariabackup SST script
* [Revision #98355a0789](https://github.com/MariaDB/server/commit/98355a0789)\
  2021-12-16 13:46:37 +0200
  * [MDEV-26971](https://jira.mariadb.org/browse/MDEV-26971): Support for progress reporting from SST scripts.
* [Revision #9d7e596ba6](https://github.com/MariaDB/server/commit/9d7e596ba6)\
  2021-09-05 17:07:05 +0300
  * [MDEV-26971](https://jira.mariadb.org/browse/MDEV-26971): JSON file interface to wsrep node state.
* [Revision #d526551587](https://github.com/MariaDB/server/commit/d526551587)\
  2022-03-16 09:12:03 +0200
  * Update wsrep-lib submodule
* Merge [Revision #10d9b890b0](https://github.com/MariaDB/server/commit/10d9b890b0) 2022-03-18 11:14:48 +0100 - Merge branch '10.8' into 10.9
* Merge [Revision #df2a8d728c](https://github.com/MariaDB/server/commit/df2a8d728c) 2022-03-17 14:38:35 +0100 - Merge branch '10.8' into 10.9
* Merge [Revision #9350945023](https://github.com/MariaDB/server/commit/9350945023) 2022-03-17 09:59:37 +0200 - Merge 10.8 into 10.9
* Merge [Revision #5be92887c2](https://github.com/MariaDB/server/commit/5be92887c2) 2022-03-16 09:14:11 +0200 - Merge 10.8 into 10.9
* [Revision #00b88376e1](https://github.com/MariaDB/server/commit/00b88376e1)\
  2022-03-16 08:41:56 +0200
  * [MDEV-27812](https://jira.mariadb.org/browse/MDEV-27812) fixup: Use log\_sys.get\_block\_size()
* Merge [Revision #1ecf173741](https://github.com/MariaDB/server/commit/1ecf173741) 2022-03-15 18:26:29 +0200 - Merge 10.8 into 10.9
* Merge [Revision #66b5b9214b](https://github.com/MariaDB/server/commit/66b5b9214b) 2022-03-11 16:18:39 +0200 - Merge 10.8 into 10.9
* [Revision #b95942a2a7](https://github.com/MariaDB/server/commit/b95942a2a7)\
  2022-03-11 11:10:09 +0200
  * [MDEV-27812](https://jira.mariadb.org/browse/MDEV-27812): Fix a race condition, and pacify MemorySanitizer
* Merge [Revision #99e74478c8](https://github.com/MariaDB/server/commit/99e74478c8) 2022-03-11 11:07:49 +0200 - Merge 10.8 into 10.9
* [Revision #75db02f0f7](https://github.com/MariaDB/server/commit/75db02f0f7)\
  2022-03-10 21:02:41 +0900
  * [MDEV-27664](https://jira.mariadb.org/browse/MDEV-27664) Spider: remove #ifdef SPIDER\_SQL\_CACHE\_IS\_IN\_LEX
* [Revision #d9d3041793](https://github.com/MariaDB/server/commit/d9d3041793)\
  2022-03-10 08:39:27 +0000
  * [MDEV-27663](https://jira.mariadb.org/browse/MDEV-27663) Spider: remove #ifdef SPIDER\_USE\_CONST\_ITEM\_FOR\_STRING\_INT\_REAL\_DECIMAL\_DATE\_ITEM
* Merge [Revision #35fcae1040](https://github.com/MariaDB/server/commit/35fcae1040) 2022-03-08 10:36:22 +0200 - Merge 10.8 into 10.9
* [Revision #91803901e9](https://github.com/MariaDB/server/commit/91803901e9)\
  2022-03-04 13:19:52 +0200
  * Flag innodb\_change\_buffering as PLUGIN\_VAR\_DEPRECATED
* Merge [Revision #15ce270036](https://github.com/MariaDB/server/commit/15ce270036) 2022-03-03 13:03:17 +0200 - Merge 10.8 into 10.9
* [Revision #177345dadc](https://github.com/MariaDB/server/commit/177345dadc)\
  2022-03-02 16:53:04 +0200
  * [MDEV-27812](https://jira.mariadb.org/browse/MDEV-27812) Allow SET GLOBAL innodb\_log\_file\_size
* Merge [Revision #24a1795d5b](https://github.com/MariaDB/server/commit/24a1795d5b) 2022-03-01 12:47:18 +0200 - Merge 10.8 into 10.9
* Merge [Revision #4a2a9c02cd](https://github.com/MariaDB/server/commit/4a2a9c02cd) 2022-02-25 16:32:33 +0200 - Merge 10.8 into 10.9
* Merge [Revision #2f5e28b43c](https://github.com/MariaDB/server/commit/2f5e28b43c) 2022-02-23 17:01:11 +0200 - Merge 10.8 into 10.9
* Merge [Revision #3e92b3e9f8](https://github.com/MariaDB/server/commit/3e92b3e9f8) 2022-02-23 10:20:58 +0200 - Merge 10.8 into 10.9
* Merge [Revision #452672ab0e](https://github.com/MariaDB/server/commit/452672ab0e) 2022-02-22 19:02:15 +0200 - Merge 10.8 into 10.9
* Merge [Revision #bbe99cd4e2](https://github.com/MariaDB/server/commit/bbe99cd4e2) 2022-02-18 08:28:49 +0200 - Merge 10.8 into 10.9
* Merge [Revision #a9e00a014d](https://github.com/MariaDB/server/commit/a9e00a014d) 2022-02-15 19:28:58 +0200 - Merge 10.8 into 10.9
* Merge [Revision #f8b3c66123](https://github.com/MariaDB/server/commit/f8b3c66123) 2022-02-14 19:51:23 +0200 - Merge 10.8 into 10.9
* [Revision #b5852ffbee](https://github.com/MariaDB/server/commit/b5852ffbee)\
  2022-02-14 10:29:18 +0200
  * [MDEV-27735](https://jira.mariadb.org/browse/MDEV-27735) Deprecate the parameter innodb\_change\_buffering
* Merge [Revision #9451e90a45](https://github.com/MariaDB/server/commit/9451e90a45) 2022-02-14 09:49:05 +0200 - Merge 10.8 into 10.9
* [Revision #d644cd6bfb](https://github.com/MariaDB/server/commit/d644cd6bfb)\
  2022-02-11 17:47:33 +0900
  * [MDEV-27662](https://jira.mariadb.org/browse/MDEV-27662) Spider: remove #ifdef SPIDER\_SUPPORT\_CREATE\_OR\_REPLACE\_TABLE
* [Revision #362c5fb10f](https://github.com/MariaDB/server/commit/362c5fb10f)\
  2022-02-11 14:58:20 +0900
  * [MDEV-27660](https://jira.mariadb.org/browse/MDEV-27660) Spider: remove #ifdef SPIDER\_HANDLER\_START\_BULK\_INSERT\_HAS\_FLAGS (#2012)
* [Revision #c817fda22d](https://github.com/MariaDB/server/commit/c817fda22d)\
  2022-02-10 15:36:44 +0900
  * [MDEV-26912](https://jira.mariadb.org/browse/MDEV-26912) Spider: Remove dead code related to Oracle OCI
* [Revision #7c339a65b8](https://github.com/MariaDB/server/commit/7c339a65b8)\
  2022-02-10 14:47:55 +0900
  * [MDEV-26178](https://jira.mariadb.org/browse/MDEV-26178) fixup: Delete constants used nowhere
* [Revision #de1bc7a157](https://github.com/MariaDB/server/commit/de1bc7a157)\
  2022-01-28 16:20:29 +0900
  * [MDEV-27659](https://jira.mariadb.org/browse/MDEV-27659) Spider: remove #ifdef HANDLER\_HAS\_DIRECT\_UPDATE\_ROWS\_WITH\_HS
* [Revision #08622739b7](https://github.com/MariaDB/server/commit/08622739b7)\
  2022-01-28 16:19:06 +0900
  * [MDEV-27658](https://jira.mariadb.org/browse/MDEV-27658) Spider: remove #if defined(PARTITION\_HAS\_GET\_CHILD\_HANDLERS)
* [Revision #61df84defb](https://github.com/MariaDB/server/commit/61df84defb)\
  2022-01-28 16:14:31 +0900
  * [MDEV-27657](https://jira.mariadb.org/browse/MDEV-27657) Spider: remove #ifdef SPIDER\_HANDLER\_SUPPORT\_MULTIPLE\_KEY\_PARTS
* [Revision #284f9226fb](https://github.com/MariaDB/server/commit/284f9226fb)\
  2022-01-28 16:13:12 +0900
  * [MDEV-27656](https://jira.mariadb.org/browse/MDEV-27656) Spider: remove #ifdef SPIDER\_HAS\_DISCOVER\_TABLE\_STRUCTURE
* [Revision #e22b3fe6f6](https://github.com/MariaDB/server/commit/e22b3fe6f6)\
  2022-01-28 16:11:24 +0900
  * [MDEV-27655](https://jira.mariadb.org/browse/MDEV-27655) Spider: remove #ifdef MARIADB\_BASE\_VERSION
* [Revision #cf577bab6f](https://github.com/MariaDB/server/commit/cf577bab6f)\
  2022-01-28 16:09:48 +0900
  * [MDEV-27652](https://jira.mariadb.org/browse/MDEV-27652) Spider: remove dead code in #ifdef HA\_HAS\_CHECKSUM\_EXTENDED
* [Revision #7d4ef290f8](https://github.com/MariaDB/server/commit/7d4ef290f8)\
  2022-01-28 16:08:01 +0900
  * [MDEV-27650](https://jira.mariadb.org/browse/MDEV-27650) Spider: remove #ifdef SPIDER\_HAS\_GROUP\_BY\_HANDLER
* [Revision #4defdb0db5](https://github.com/MariaDB/server/commit/4defdb0db5)\
  2022-01-28 16:06:27 +0900
  * [MDEV-27648](https://jira.mariadb.org/browse/MDEV-27648) Spider: remove in #ifdef HASH\_UPDATE\_WITH\_HASH\_VALUE
* [Revision #0df6a95bc2](https://github.com/MariaDB/server/commit/0df6a95bc2)\
  2022-01-28 16:05:09 +0900
  * [MDEV-27647](https://jira.mariadb.org/browse/MDEV-27647) Spider: remove #ifdef HANDLER\_HAS\_DIRECT\_UPDATE\_ROWS
* [Revision #4f353dc013](https://github.com/MariaDB/server/commit/4f353dc013)\
  2022-01-28 16:03:46 +0900
  * [MDEV-27646](https://jira.mariadb.org/browse/MDEV-27646) Spider: remove #ifdef SPIDER\_HAS\_HASH\_VALUE\_TYPE
* [Revision #3beefe8f98](https://github.com/MariaDB/server/commit/3beefe8f98)\
  2022-01-28 16:02:54 +0900
  * [MDEV-27645](https://jira.mariadb.org/browse/MDEV-27645) Spider: remove #ifdef HA\_MRR\_USE\_DEFAULT\_IMPL
* [Revision #7ba4612108](https://github.com/MariaDB/server/commit/7ba4612108)\
  2022-01-28 16:01:17 +0900
  * [MDEV-27644](https://jira.mariadb.org/browse/MDEV-27644) Spider: remove #ifdef HANDLER\_HAS\_DIRECT\_AGGREGATE
* [Revision #a4da96773d](https://github.com/MariaDB/server/commit/a4da96773d)\
  2022-01-28 15:57:07 +0900
  * [MDEV-27643](https://jira.mariadb.org/browse/MDEV-27643) Spider: remove #ifdef HA\_CAN\_BULK\_ACCESS
* [Revision #00ae4272b3](https://github.com/MariaDB/server/commit/00ae4272b3)\
  2022-01-28 15:55:22 +0900
  * [MDEV-27642](https://jira.mariadb.org/browse/MDEV-27642) Spider: remove #ifdef WITHOUT\_SPIDER\_BG\_SEARCH
* [Revision #cfd145faed](https://github.com/MariaDB/server/commit/cfd145faed)\
  2022-01-28 01:03:06 +0900
  * [MDEV-27641](https://jira.mariadb.org/browse/MDEV-27641) Spider: remove #if MYSQL\_VERSION\_ID < ${VERSION}
* [Revision #06bd93c377](https://github.com/MariaDB/server/commit/06bd93c377)\
  2022-01-28 00:06:09 +0900
  * [MDEV-27637](https://jira.mariadb.org/browse/MDEV-27637) Spider: remove #if defined(MARIADB\_BASE\_VERSION) && MYSQL\_VERSION\_ID >= ${VERSION}
* Merge [Revision #802e3b616c](https://github.com/MariaDB/server/commit/802e3b616c) 2022-02-09 09:17:30 +0100 - Merge branch '10.8' into 10.9
* [Revision #b24148b146](https://github.com/MariaDB/server/commit/b24148b146)\
  2022-02-08 19:25:42 +0100
  * 10.9 branch

{% @marketo/form formid="4316" formId="4316" %}
