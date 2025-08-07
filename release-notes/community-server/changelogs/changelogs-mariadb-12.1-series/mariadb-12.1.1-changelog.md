# MariaDB 12.1.1 Changelog

{% include "../../../.gitbook/includes/latest-12-1.md" %}

<a href="https://mariadb.org/download/" class="button primary">Download</a> <a href="../../release-notes-mariadb-12.1-rolling-releases/mariadb-12.1.1-release-notes.md" class="button secondary">Release Notes</a> <a href="mariadb-12.1.1-changelog.md" class="button secondary">Changelog</a> <a href="../../release-notes-mariadb-12.1-rolling-releases/changes-and-improvements-in-mariadb-12.1.md" class="button secondary">Overview of 12.1</a>

**Release date:** 7 Aug 2025

For the highlights of this release, see the [release notes](../../release-notes-mariadb-12.0-rolling-releases/mariadb-12.0.1-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On [GitHub](https://github.com/MariaDB/server/tree/11.8) you can view more details of the revision and view diffs of the code modified in that revision.

* Changes from the MariaDB [12.1 Preview](https://mariadb.org/mariadb-12-1-preview-available/) are also included in this changelog
* Includes all fixes from [MariaDB 12.0.2](../changelogs-mariadb-12.0-series/mariadb-12.0.2-changelog.md)
* [Revision #893761b35c](https://github.com/MariaDB/server/commit/893761b35c) <sup>_2025-07-26 21:00:23 +0700_</sup>
  * MDEV-37292 Hint NO\_INDEX() disables all indexes if none of given index names is resolved
* [Revision #c329c43be7](https://github.com/MariaDB/server/commit/c329c43be7) <sup>_2025-05-01 13:38:10 +0700_</sup>
  * MDEV-35856: implement index hints
* [Revision #4453d179e4](https://github.com/MariaDB/server/commit/4453d179e4) <sup>_2025-07-04 14:39:04 +0300_</sup>
  * MDEV-36554 addendum: Assertion 'is\_wsrep() == wsrep\_on(mysql\_thd)' failed in void trx\_t::commit\_in\_memory(const mtr\_t\*)
* [Revision #603afc82d2](https://github.com/MariaDB/server/commit/603afc82d2) <sup>_2025-06-13 14:02:25 +0300_</sup>
  * MDEV-36554: Assertion 'is\_wsrep() == wsrep\_on(mysql\_thd)' failed in void trx\_t::commit\_in\_memory(const mtr\_t\*)
* [Revision #b39ea86305](https://github.com/MariaDB/server/commit/b39ea86305) <sup>_2025-03-06 11:41:49 +0200_</sup>
  * MDEV-36077: Galera feature: Retry applying writesets at slaves
* [Revision #dae5a99c73](https://github.com/MariaDB/server/commit/dae5a99c73) <sup>_2025-05-12 16:23:20 +0200_</sup>
  * MDEV-13817 add support for oracle left join syntax - the ( + )
* [Revision #58a2184f5d](https://github.com/MariaDB/server/commit/58a2184f5d) <sup>_2025-03-18 17:35:08 +0100_</sup>
  * Add Flags to Item::walk.
* <sup>_Merge_</sup> [<sup>_Revision #6e8dbb9693_</sup>](https://github.com/MariaDB/server/commit/6e8dbb9693) <sup>_2025-08-03 15:01:09 +0200 - Merge branch '12.0' into 12.1_</sup>
* [Revision #089caf901f](https://github.com/MariaDB/server/commit/089caf901f) <sup>_2025-08-03 14:54:22 +0200_</sup>
  * MDEV-34817 perfschema.lowercase\_fs\_off fails on buildbot
* [Revision #90f5e09956](https://github.com/MariaDB/server/commit/90f5e09956) <sup>_2025-07-31 13:18:31 +0200_</sup>
  * fix tests for --view
* [Revision #1563988ae6](https://github.com/MariaDB/server/commit/1563988ae6) <sup>_2025-08-02 15:18:52 +0200_</sup>
  * MDEV-37160 When >=2 clients are in use, the server\_audit\_file\_buffer\_size setting is not honored
* [Revision #a0290cfbed](https://github.com/MariaDB/server/commit/a0290cfbed) <sup>_2025-07-31 09:12:56 +0400_</sup>
  * MDEV-36850 SIGSEGV in Item\_sp\_variable::save\_in\_field | fill\_record
* [Revision #0fbdc56ee2](https://github.com/MariaDB/server/commit/0fbdc56ee2) <sup>_2025-07-28 13:11:35 +0400_</sup>
  * MDEV-36954 Improve error handling when a function-method/procedure-method is missing in stored routines
* [Revision #ef0505484e](https://github.com/MariaDB/server/commit/ef0505484e) <sup>_2025-05-19 22:36:14 +0800_</sup>
  * Cleanup#3 for MDEV-34319: DECLARE TYPE .. TABLE OF .. INDEX BY
* [Revision #5360ccf8f4](https://github.com/MariaDB/server/commit/5360ccf8f4) <sup>_2025-05-17 09:33:16 +0400_</sup>
  * Cleanup#2 for MDEV-34319: DECLARE TYPE .. TABLE OF .. INDEX BY - packed\_col\_length
* [Revision #e9d541f912](https://github.com/MariaDB/server/commit/e9d541f912) <sup>_2025-05-06 15:06:59 +0400_</sup>
  * Cleanup#1 for MDEV-34319: DECLARE TYPE .. TABLE OF .. INDEX BY
* [Revision #41014a4ecd](https://github.com/MariaDB/server/commit/41014a4ecd) <sup>_2024-10-11 13:06:20 +0800_</sup>
  * MDEV-34319: DECLARE TYPE .. TABLE OF .. INDEX BY in stored routines
* [Revision #a91b78049a](https://github.com/MariaDB/server/commit/a91b78049a) <sup>_2025-04-29 14:51:57 +0400_</sup>
  * MDEV-36705 Preparations for associative arrays (MDEV-34319)
* [Revision #ef3c843c17](https://github.com/MariaDB/server/commit/ef3c843c17) <sup>_2025-07-31 16:27:44 +0200_</sup>
  * MDEV-34680 post-fixes
* [Revision #7251cbca51](https://github.com/MariaDB/server/commit/7251cbca51) <sup>_2025-05-02 18:04:49 +0400_</sup>
  * MDEV-34680 Asynchronous and Buffered Logging for Audit Plugin.
* [Revision #26c8bc9357](https://github.com/MariaDB/server/commit/26c8bc9357) <sup>_2025-08-01 11:12:09 +0200_</sup>
  * mtr: make wait\_for\_line\_count\_in\_file.inc leave traces in the log
* [Revision #e32d98451b](https://github.com/MariaDB/server/commit/e32d98451b) <sup>_2025-07-30 20:03:03 +0200_</sup>
  * MDEV-21376 fix the test for windows, fix --help text
* [Revision #c23e20525d](https://github.com/MariaDB/server/commit/c23e20525d) <sup>_2025-05-12 14:17:40 +0400_</sup>
  * MDEV-21376 mysqldump should support wildcards.
* [Revision #6dd3decd28](https://github.com/MariaDB/server/commit/6dd3decd28) <sup>_2025-07-29 13:34:08 +0200_</sup>
  * MDEV-37339 errors about caching\_sha2\_password on server startup (WolfSSL)
* [Revision #db937cc971](https://github.com/MariaDB/server/commit/db937cc971) <sup>_2025-06-22 07:27:49 -0400_</sup>
  * MDEV-37207: dumping tables for multi delete query doesn't work always
* [Revision #67b320b413](https://github.com/MariaDB/server/commit/67b320b413) <sup>_2025-05-05 09:46:34 -0400_</sup>
  * MDEV-36483: store ddls in the optimizer trace
* [Revision #823a3a258f](https://github.com/MariaDB/server/commit/823a3a258f) <sup>_2025-07-07 19:26:48 +0200_</sup>
  * MDEV-36205 coverage test
* [Revision #c06a25e495](https://github.com/MariaDB/server/commit/c06a25e495) <sup>_2025-06-07 21:09:11 +0200_</sup>
  * MDEV-36205 autodetection of subdist applicability
* [Revision #4ca9fca4f6](https://github.com/MariaDB/server/commit/4ca9fca4f6) <sup>_2025-06-03 22:56:41 +0200_</sup>
  * MDEV-36205 subdist optimization
* [Revision #ca19a25105](https://github.com/MariaDB/server/commit/ca19a25105) <sup>_2025-05-28 17:38:32 +0200_</sup>
  * MDEV-35897 cleanup: Stats structure
* [Revision #c2bff9ff70](https://github.com/MariaDB/server/commit/c2bff9ff70) <sup>_2025-05-29 16:46:52 +0200_</sup>
  * cleanup: MHNSW\_param
* [Revision #84987d1471](https://github.com/MariaDB/server/commit/84987d1471) <sup>_2025-05-29 17:16:40 +0200_</sup>
  * cleanup
* [Revision #63583b0824](https://github.com/MariaDB/server/commit/63583b0824) <sup>_2025-05-04 19:13:43 +0200_</sup>
  * MDEV-9804 Implement a caching\_sha2\_password plugin
* [Revision #b57bf6f7b1](https://github.com/MariaDB/server/commit/b57bf6f7b1) <sup>_2025-07-24 09:39:48 -0400_</sup>
  * MDEV-37308 main.failed\_auth\_unixsocket fails
* [Revision #46d7450f75](https://github.com/MariaDB/server/commit/46d7450f75) <sup>_2025-03-21 16:00:00 +0200_</sup>
  * MDEV-35635: START SLAVE UNTIL allows CHANGE MASTER TO options
* [Revision #8cdee25952](https://github.com/MariaDB/server/commit/8cdee25952) <sup>_2025-06-04 11:43:30 +1000_</sup>
  * MDEV-36132 Substitute vcol expressions with indexed vcol fields in ORDER BY and GROUP BY
* [Revision #d308556122](https://github.com/MariaDB/server/commit/d308556122) <sup>_2025-06-03 15:46:22 +1000_</sup>
  * MDEV-36132 Initialise ordered record buffers in ha\_parititon
* [Revision #7215fe7894](https://github.com/MariaDB/server/commit/7215fe7894) <sup>_2025-07-17 15:15:36 +1000_</sup>
  * MDEV-37252 Do not check is\_key\_used in get\_index\_for\_order
* [Revision #ce7ab467db](https://github.com/MariaDB/server/commit/ce7ab467db) <sup>_2025-05-28 00:05:05 +0700_</sup>
  * MDEV-35617: DROP USER should leave no active session for that user
* [Revision #e3d9369774](https://github.com/MariaDB/server/commit/e3d9369774) <sup>_2025-06-12 08:05:32 +0200_</sup>
  * cleanup: disconnect before DROP USER
* [Revision #bead24b7f3](https://github.com/MariaDB/server/commit/bead24b7f3) <sup>_2025-06-12 00:43:26 +0200_</sup>
  * mariadb-test: wait on disconnect
* [Revision #18985d8471](https://github.com/MariaDB/server/commit/18985d8471) <sup>_2025-05-12 00:11:31 +0400_</sup>
  * MDEV-19749 - MDL scalability regression after backup locks
* [Revision #5b32446217](https://github.com/MariaDB/server/commit/5b32446217) <sup>_2025-05-07 16:04:07 +0400_</sup>
  * MDL\_lock encapsulation: removed redundant methods
* [Revision #3ca5e08f0e](https://github.com/MariaDB/server/commit/3ca5e08f0e) <sup>_2025-05-04 01:32:04 +0400_</sup>
  * MDL\_lock encapsulation: final
* [Revision #02eb8f7246](https://github.com/MariaDB/server/commit/02eb8f7246) <sup>_2025-05-04 01:59:52 +0400_</sup>
  * MDL\_lock encapsulation: MDL\_lock::get\_key()
* [Revision #36bec5697b](https://github.com/MariaDB/server/commit/36bec5697b) <sup>_2025-05-04 00:02:00 +0400_</sup>
  * MDL\_lock encapsulation: try\_acquire\_lock\_impl()
* [Revision #9d34cee80b](https://github.com/MariaDB/server/commit/9d34cee80b) <sup>_2025-05-03 02:10:01 +0400_</sup>
  * Move m\_wait.reset\_status() out of critical section
* [Revision #329bff638b](https://github.com/MariaDB/server/commit/329bff638b) <sup>_2025-05-02 16:06:25 +0400_</sup>
  * MDL\_lock encapsulation: try\_acquire\_lock()
* [Revision #a955e9dd61](https://github.com/MariaDB/server/commit/a955e9dd61) <sup>_2025-05-01 17:39:43 +0400_</sup>
  * MDL\_ticket cleanup
* [Revision #2a3b999a56](https://github.com/MariaDB/server/commit/2a3b999a56) <sup>_2025-05-01 15:29:53 +0400_</sup>
  * MDL\_lock encapsulation: MDL\_lock::remove\_ticket()
* [Revision #5aa4ccf4c4](https://github.com/MariaDB/server/commit/5aa4ccf4c4) <sup>_2025-05-01 13:40:36 +0400_</sup>
  * MDL\_lock encapsulation: notify\_conflicting\_locks()
* [Revision #0c31f85a67](https://github.com/MariaDB/server/commit/0c31f85a67) <sup>_2025-05-01 01:12:08 +0400_</sup>
  * MDL\_lock encapsulation: MDL\_lock::upgrade()
* [Revision #255a22c3a0](https://github.com/MariaDB/server/commit/255a22c3a0) <sup>_2025-05-01 00:37:01 +0400_</sup>
  * MDL\_lock encapsulation: MDL\_lock::downgrade()
* [Revision #ecd47cfa5c](https://github.com/MariaDB/server/commit/ecd47cfa5c) <sup>_2025-04-30 23:56:15 +0400_</sup>
  * MDL\_lock encapsulation: add\_cloned\_ticket()
* [Revision #fba71705df](https://github.com/MariaDB/server/commit/fba71705df) <sup>_2025-04-30 20:58:00 +0400_</sup>
  * MDL\_lock encapsulation: MDL\_lock::iterate()
* [Revision #c2881f04e8](https://github.com/MariaDB/server/commit/c2881f04e8) <sup>_2025-04-30 20:03:27 +0400_</sup>
  * MDL\_lock encapsulation: MDL\_lock::get\_lock\_owner()
* [Revision #62a1f0d990](https://github.com/MariaDB/server/commit/62a1f0d990) <sup>_2025-04-24 15:03:05 -0400_</sup>
  * MDEV-36092 New-style hint: \[NO\_]SPLIT\_MATERIALIZED
* [Revision #07d71fdcf8](https://github.com/MariaDB/server/commit/07d71fdcf8) <sup>_2024-11-21 14:31:04 +0200_</sup>
  * MDEV-20065 parallel replication for galera slave
* [Revision #6ef1303d69](https://github.com/MariaDB/server/commit/6ef1303d69) <sup>_2025-05-02 23:07:54 +0300_</sup>
  * MDEV-34954 Add JSON flag for mysqldumpslow.sh output
* [Revision #891108ed66](https://github.com/MariaDB/server/commit/891108ed66) <sup>_2025-06-05 11:30:57 +0200_</sup>
  * Got rid of the INFO\_BIN and INFO\_SRC files as specified by the comments of this pull request: https://github.com/MariaDB/server/pull/4078 Also got rid of the file\_contents.test and file\_contents.result files as they only test the existence and contents of the INFO\_BIN and INFO\_SRC, therefore they are not needed anymore.
* [Revision #cffbb17480](https://github.com/MariaDB/server/commit/cffbb17480) <sup>_2025-07-08 12:30:27 +0300_</sup>
  * MDEV-28933: Per-table unique FOREIGN KEY constraint names
* [Revision #d4d0dd00b7](https://github.com/MariaDB/server/commit/d4d0dd00b7) <sup>_2025-06-27 16:27:28 +0200_</sup>
  * MDEV-37031 Fix broken server\_audit.test on Windows
* [Revision #6efa06805d](https://github.com/MariaDB/server/commit/6efa06805d) <sup>_2025-06-02 11:01:03 +0300_</sup>
  * Fixed some compilation failures on 32bit
* [Revision #8745b6cace](https://github.com/MariaDB/server/commit/8745b6cace) <sup>_2025-05-22 12:06:14 +0300_</sup>
  * Change some Aria ULONG variables to UINT
* [Revision #0b7b5cc1b3](https://github.com/MariaDB/server/commit/0b7b5cc1b3) <sup>_2025-05-19 21:58:30 +0300_</sup>
  * MDEV-24 Segmented key cache for Aria
* [Revision #212fad1b7e](https://github.com/MariaDB/server/commit/212fad1b7e) <sup>_2025-04-21 21:26:19 +0000_</sup>
  * MDEV-36397 Record change\_user command in MTR output
* [Revision #2ee2e2d0f3](https://github.com/MariaDB/server/commit/2ee2e2d0f3) <sup>_2025-02-24 11:32:27 -0500_</sup>
  * MDEV-36106 New-style hints: \[NO\_]DERIVED\_CONDITION\_PUSHDOWN, \[NO\_]MERGE
* <sup>_Merge_</sup> [<sup>_Revision #e653666368_</sup>](https://github.com/MariaDB/server/commit/e653666368) <sup>_2025-06-18 09:27:49 +0200 - Merge branch '12.0' into 12.1_</sup>
* [Revision #247e2f8d4d](https://github.com/MariaDB/server/commit/247e2f8d4d) <sup>_2025-04-29 19:24:11 +0300_</sup>
  * MDEV-29499 Improving the 'Can't execute init\_slave query' error message with the actual failure
* [Revision #28dbfcb397](https://github.com/MariaDB/server/commit/28dbfcb397) <sup>_2025-05-03 13:09:05 -0600_</sup>
  * MDEV-35837: Update CODING\_STANDARDS to C++17
* [Revision #6a2afb42ba](https://github.com/MariaDB/server/commit/6a2afb42ba) <sup>_2025-06-06 18:42:30 +0530_</sup>
  * MDEV-36487 Fix ha\_innobase::check() for sequences
* [Revision #37274ae01f](https://github.com/MariaDB/server/commit/37274ae01f) <sup>_2025-05-28 13:58:47 +0530_</sup>
  * MDEV-36032 Check whether a table can be a sequence when ALTERed with SEQUENCE=1
* <sup>_Merge_</sup> [<sup>_Revision #a6f5555008_</sup>](https://github.com/MariaDB/server/commit/a6f5555008) <sup>_2025-06-05 12:00:59 +0200 - Merge branch '12.0' into 12.1_</sup>
* [Revision #4b79d7b8ee](https://github.com/MariaDB/server/commit/4b79d7b8ee) <sup>_2025-05-20 12:54:18 +0300_</sup>
  * MDEV-36735 rpl.rpl\_drop\_temp Result Content Mismatch Failure
* [Revision #cf644785e1](https://github.com/MariaDB/server/commit/cf644785e1) <sup>_2025-04-09 11:38:33 +0400_</sup>
  * MDEV-36503 add Pad\_attribute column to INFORMATION\_SCHEMA.COLLATIONS
* [Revision #30ed3b867a](https://github.com/MariaDB/server/commit/30ed3b867a) <sup>_2025-04-29 21:17:53 +0200_</sup>
  * skip main.mysql\_upgrade test for previews
* [Revision #72b666b837](https://github.com/MariaDB/server/commit/72b666b837) <sup>_2025-04-28 10:20:54 +0200_</sup>
  * 12.1 branch

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
