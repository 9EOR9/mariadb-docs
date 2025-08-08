# MariaDB 11.8.2 Changelog

{% include "../../../.gitbook/includes/latest-11-8.md" %}

<a href="https://mariadb.com/downloads" class="button primary">Download</a> <a href="../../mariadb-11-8-series/mariadb-11-8-2-release-notes.md" class="button secondary">Release Notes</a> <a href="mariadb-11.8.2-changelog.md" class="button secondary">Changelog</a> <a href="../../mariadb-11-8-series/what-is-mariadb-118.md" class="button secondary">Overview of 11.8</a>

[<sup>_Alternate download from mariadb.org_</sup>](https://downloads.mariadb.org/mariadb/11.8.2/)

**Release date:** 4 Jun 2025

For the highlights of this release, see the [release notes](../../mariadb-11-8-series/mariadb-11-8-2-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On [GitHub](https://github.com/MariaDB/server/tree/11.8) you can view more details of the revision and view diffs of the code modified in that revision.

* Includes all fixes from [MariaDB 11.4.7](../changelogs-mariadb-11-4-series/mariadb-11.4.7-changelog.md)
* <sup>_Merge_</sup> [<sup>_Revision #8d36cafe4f_</sup>](https://github.com/MariaDB/server/commit/8d36cafe4f) <sup>_2025-05-21 15:57:16 +0200 - Merge branch '11.4' into 11.8_</sup>
* <sup>_Merge_</sup> [<sup>_Revision #118cfcf821_</sup>](https://github.com/MariaDB/server/commit/118cfcf821) <sup>_2025-05-13 13:44:58 +0300 - Merge 10.11 into 11.4_</sup>
* [Revision #8fb09426b9](https://github.com/MariaDB/server/commit/8fb09426b9) 2025-05-13 12:27:50 +0300
  * [MDEV-36759](https://jira.mariadb.org/browse/MDEV-36759): Huge performance drop
* [Revision #bb48d7bc81](https://github.com/MariaDB/server/commit/bb48d7bc81) 2025-05-13 12:27:46 +0300
  * [MDEV-36781](https://jira.mariadb.org/browse/MDEV-36781): Assertion i < BUF\_BUDDY\_SIZES failed in buf\_buddy\_shrink()
* [Revision #56e0be34bc](https://github.com/MariaDB/server/commit/56e0be34bc) 2025-05-13 12:27:42 +0300
  * [MDEV-36780](https://jira.mariadb.org/browse/MDEV-36780): InnoDB buffer pool reserves all assigned memory
* [Revision #0c18e5a292](https://github.com/MariaDB/server/commit/0c18e5a292) 2025-05-08 11:18:16 +0300
  * [MDEV-36760](https://jira.mariadb.org/browse/MDEV-36760) log\_t::append\_prepare\_wait(): Bogus assertion on write\_lsn
* [Revision #a7278a3024](https://github.com/MariaDB/server/commit/a7278a3024) 2025-04-28 10:22:58 -0600
  * [MDEV-36663](https://jira.mariadb.org/browse/MDEV-36663): Testcase Fixup
* [Revision #791fcea1d7](https://github.com/MariaDB/server/commit/791fcea1d7) 2025-05-13 12:27:36 +0300
  * bump the VERSION
* [Revision #f5b5de9cf9](https://github.com/MariaDB/server/commit/f5b5de9cf9) 2025-05-13 13:43:53 +0300
  * bump the VERSION
* [Revision #da5a4d05b9](https://github.com/MariaDB/server/commit/da5a4d05b9) 2025-01-15 09:18:12 +1100
  * [MDEV-35850](https://jira.mariadb.org/browse/MDEV-35850) make HOSTNAME a cmake configure variable
* [Revision #c94133a71d](https://github.com/MariaDB/server/commit/c94133a71d) 2025-04-19 18:02:51 -0400
  * [MDEV-21510](https://jira.mariadb.org/browse/MDEV-21510): In Optimizer Trace, print index name in chosen\_access\_method
* [Revision #d1a2dc54ad](https://github.com/MariaDB/server/commit/d1a2dc54ad) 2025-05-08 19:08:29 +0200
  * Fix the test: changing charset should be dome when we can not skip the test.
* [Revision #98e02217c7](https://github.com/MariaDB/server/commit/98e02217c7) 2025-04-29 08:27:07 +0200
  * Fix version
* <sup>_Merge_</sup> [<sup>_Revision #4c6a59f120_</sup>](https://github.com/MariaDB/server/commit/4c6a59f120) <sup>_2025-04-28 19:10:10 +0200 - Merge branch '11.4' into 11.8_</sup>
* <sup>_Merge_</sup> [<sup>_Revision #237e24497b_</sup>](https://github.com/MariaDB/server/commit/237e24497b) <sup>_2025-04-27 11:33:27 +0200 - Merge remote-tracking branch 'github/bb-11.4-release' into bb-11.8-serg_</sup>
* [Revision #a0b77eb806](https://github.com/MariaDB/server/commit/a0b77eb806) 2025-04-24 14:32:14 +0300
  * [MDEV-36685](https://jira.mariadb.org/browse/MDEV-36685) CREATE-SELECT may lose in binlog side-effects of stored-routine
* [Revision #82867e07e3](https://github.com/MariaDB/server/commit/82867e07e3) 2025-04-20 10:42:53 +0200
  * [MDEV-35897](https://jira.mariadb.org/browse/MDEV-35897) vector index search allocates too much memory for large ef\_search
* [Revision #395db6f1d5](https://github.com/MariaDB/server/commit/395db6f1d5) 2025-04-07 22:43:56 +0200
  * [MDEV-36398](https://jira.mariadb.org/browse/MDEV-36398) Extend SBOM with 'license' and 'copyright'
* [Revision #805e7ca3ad](https://github.com/MariaDB/server/commit/805e7ca3ad) 2025-04-17 16:29:07 +0200
  * fix incorrect merge 15700f54c212
* [Revision #76b54a2a67](https://github.com/MariaDB/server/commit/76b54a2a67) 2025-04-15 00:36:20 +0200
  * set the function result field name for error reporting
* [Revision #b5d0e30923](https://github.com/MariaDB/server/commit/b5d0e30923) 2025-04-15 00:18:23 +0200
  * [MDEV-36596](https://jira.mariadb.org/browse/MDEV-36596) Assertion failure in TABLE\_SHARE::init\_from\_sql\_statement\_string upon returning wrong type from function
* [Revision #1691b0cfac](https://github.com/MariaDB/server/commit/1691b0cfac) 2025-04-06 11:52:34 +0200
  * cleanup: mhnsw, fix vector length when cosine
* [Revision #313b8c293a](https://github.com/MariaDB/server/commit/313b8c293a) 2024-12-23 17:25:35 +0400
  * [MDEV-35309](https://jira.mariadb.org/browse/MDEV-35309) ALTER performs vector truncation without WARN\_DATA\_TRUNCATED or similar warnings/errors
* [Revision #e5574d8b94](https://github.com/MariaDB/server/commit/e5574d8b94) 2025-04-02 18:06:29 +0200
  * [MDEV-36334](https://jira.mariadb.org/browse/MDEV-36334) test main.func\_format fails on i386 on exabyte/petabyte mismatch
* [Revision #29823f3b96](https://github.com/MariaDB/server/commit/29823f3b96) 2025-02-07 15:12:20 +0400
  * [MDEV-35152](https://jira.mariadb.org/browse/MDEV-35152) DATA/INDEX DIRECTORY options are ignored for vector index
* [Revision #1a85ae444a](https://github.com/MariaDB/server/commit/1a85ae444a) 2025-03-29 12:13:42 +0100
  * [MDEV-36050](https://jira.mariadb.org/browse/MDEV-36050) DATA/INDEX DIRECTORY handling is inconsistent
* [Revision #dc073e4c0c](https://github.com/MariaDB/server/commit/dc073e4c0c) 2025-03-28 21:57:31 +0100
  * mtr: use plugin-load-add in have\_rocksdb.opt
* [Revision #606edaa6cd](https://github.com/MariaDB/server/commit/606edaa6cd) 2025-03-28 21:56:44 +0100
  * consistent error messages, no \<angle quoting>
* [Revision #7db60533c7](https://github.com/MariaDB/server/commit/7db60533c7) 2025-03-27 20:20:32 +0100
  * [MDEV-36188](https://jira.mariadb.org/browse/MDEV-36188) assert with vector index and very long PK
* [Revision #49f330a305](https://github.com/MariaDB/server/commit/49f330a305) 2025-03-26 22:10:53 +0100
  * [MDEV-36177](https://jira.mariadb.org/browse/MDEV-36177) InnoDB: Failing assertion: prebuilt->select\_lock\_type != LOCK\_NONE || srv\_read\_only\_mode || trx->read\_view.is\_open()
* [Revision #1304181f36](https://github.com/MariaDB/server/commit/1304181f36) 2025-03-26 21:25:39 +0100
  * [MDEV-36256](https://jira.mariadb.org/browse/MDEV-36256) Crash on disconnect when dropped Aria table with vector key under lock
* [Revision #7788295022](https://github.com/MariaDB/server/commit/7788295022) 2025-03-26 16:49:40 +0100
  * [MDEV-36163](https://jira.mariadb.org/browse/MDEV-36163) InnoDB assert with vector index under LOCK TABLES
* [Revision #a3257038d1](https://github.com/MariaDB/server/commit/a3257038d1) 2025-03-25 11:11:46 +0100
  * assert in safe\_mutex\_lock that the mutex is initialized
* [Revision #cd7a454c23](https://github.com/MariaDB/server/commit/cd7a454c23) 2025-03-25 11:11:01 +0100
  * [MDEV-36351](https://jira.mariadb.org/browse/MDEV-36351) MariaDB crashes when trying to access information\_schema.users under --skip-grant-tables
* [Revision #72dc054a9e](https://github.com/MariaDB/server/commit/72dc054a9e) 2025-03-25 10:41:43 +0100
  * [MDEV-36104](https://jira.mariadb.org/browse/MDEV-36104) Server crashes when reading information\_schema.COLUMNS after creating a table with virtual columns using the GIS data type
* [Revision #3c98e8c0e3](https://github.com/MariaDB/server/commit/3c98e8c0e3) 2025-02-14 14:16:40 +0100
  * [MDEV-36067](https://jira.mariadb.org/browse/MDEV-36067) Assertion failure in TABLE\_SHARE::init\_from\_sql\_statement\_string
* [Revision #fb43b0dc3d](https://github.com/MariaDB/server/commit/fb43b0dc3d) 2025-04-18 09:41:12 +0200
  * fix for post-test check of multi\_source.master\_info\_file
* [Revision #f9125dffc6](https://github.com/MariaDB/server/commit/f9125dffc6) 2025-04-16 11:19:49 +1000
  * [MDEV-35662](https://jira.mariadb.org/browse/MDEV-35662) Optimize subqueries before sending EXPLAIN output in single table update
* [Revision #6bb92f98ce](https://github.com/MariaDB/server/commit/6bb92f98ce) 2025-02-21 12:41:50 -0500
  * [MDEV-36184](https://jira.mariadb.org/browse/MDEV-36184) - mhnsw: support powerpc64 SIMD instructions
* [Revision #db5bb6f333](https://github.com/MariaDB/server/commit/db5bb6f333) 2025-04-03 18:29:24 +1100
  * [MDEV-36469](https://jira.mariadb.org/browse/MDEV-36469) don't check is\_infoschema\_db for null db
* <sup>_Merge_</sup> [<sup>_Revision #bb1d88b6dc_</sup>](https://github.com/MariaDB/server/commit/bb1d88b6dc) <sup>_2025-04-02 14:07:01 +0300 - Merge 11.4 into 11.8_</sup>
* [Revision #6e4fa7e5a1](https://github.com/MariaDB/server/commit/6e4fa7e5a1) 2025-03-27 18:02:37 +0700
  * [MDEV-36390](https://jira.mariadb.org/browse/MDEV-36390): Minor refactoring of the method get\_expr\_query at the classes sp\_instr\_cpush/sp\_instr\_cursor\_copy\_struct
* [Revision #cc831f16c8](https://github.com/MariaDB/server/commit/cc831f16c8) 2025-03-24 12:38:46 +0700
  * [MDEV-36079](https://jira.mariadb.org/browse/MDEV-36079): Stored routine with a cursor crashes on the second execution if a DDL statement happened
* [Revision #98a75d111c](https://github.com/MariaDB/server/commit/98a75d111c) 2025-03-20 18:38:09 +0400
  * [MDEV-36322](https://jira.mariadb.org/browse/MDEV-36322) Comparison ROW(stored\_func(),1)=ROW(1,1) calls the function twice per row
* [Revision #01cf1cb84b](https://github.com/MariaDB/server/commit/01cf1cb84b) 2024-11-27 07:33:26 -0700
  * [MDEV-7850](https://jira.mariadb.org/browse/MDEV-7850): Optimize Query\_log\_event::begin\_event()
* [Revision #5217d8609b](https://github.com/MariaDB/server/commit/5217d8609b) 2025-03-06 09:36:10 +0100
  * [MDEV-9101](https://jira.mariadb.org/browse/MDEV-9101) forgotten symbolic error representation
* <sup>_Merge_</sup> [<sup>_Revision #bb9f010432_</sup>](https://github.com/MariaDB/server/commit/bb9f010432) <sup>_2025-03-05 20:39:47 +0200 - Merge 11.4 into 11.8_</sup>
* [Revision #6f1161aa34](https://github.com/MariaDB/server/commit/6f1161aa34) 2025-02-17 13:43:22 +1100
  * [MDEV-36087](https://jira.mariadb.org/browse/MDEV-36087) Check for existence of the new Options JSON field in mysql.servers
* [Revision #b453123a26](https://github.com/MariaDB/server/commit/b453123a26) 2025-02-20 13:12:23 +0100
  * [MDEV-36130](https://jira.mariadb.org/browse/MDEV-36130): main.mysqldump fails in parallel mysql-import test
* [Revision #059d06ae07](https://github.com/MariaDB/server/commit/059d06ae07) 2025-02-18 13:09:26 +0200
  * Fixed compile failure in sql\_print\_warning in sql\_acl.cc
* [Revision #59ad3225ae](https://github.com/MariaDB/server/commit/59ad3225ae) 2025-02-13 17:27:11 +0100
  * [MDEV-34979](https://jira.mariadb.org/browse/MDEV-34979) postfix
* [Revision #33e0796e7a](https://github.com/MariaDB/server/commit/33e0796e7a) 2025-02-13 13:06:50 +0200
  * [MDEV-36080](https://jira.mariadb.org/browse/MDEV-36080): Assertion on 2nd PS execution with error and Array Binding
* [Revision #1629435745](https://github.com/MariaDB/server/commit/1629435745) 2025-02-12 14:07:10 -0500
  * [MDEV-36074](https://jira.mariadb.org/browse/MDEV-36074) main.multidelete\_engine missing result file
* [Revision #d54ec1b377](https://github.com/MariaDB/server/commit/d54ec1b377) 2025-02-05 15:28:42 +0100
  * [MDEV-33965](https://jira.mariadb.org/browse/MDEV-33965) - fix non-determinism in the main.status test

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
