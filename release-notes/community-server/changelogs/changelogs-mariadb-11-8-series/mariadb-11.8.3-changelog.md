# MariaDB 11.8.3 Changelog

<a href="https://mariadb.com/downloads" class="button primary">Download</a> <a href="../../mariadb-11-8-series/mariadb-11.8.3-release-notes.md" class="button secondary">Release Notes</a> <a href="mariadb-11.8.3-changelog.md" class="button secondary">Changelog</a> <a href="../../mariadb-11-8-series/what-is-mariadb-118.md" class="button secondary">Overview of 11.8</a>

[<sup>_Alternate download from mariadb.org_</sup>](https://downloads.mariadb.org/mariadb/11.8.3/)

**Release date:** 6 Aug 2025

For the highlights of this release, see the [release notes](../../mariadb-11-8-series/mariadb-11.8.3-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On [GitHub](https://github.com/MariaDB/server/tree/11.8) you can view more details of the revision and view diffs of the code modified in that revision.

* Includes all fixes from [MariaDB 11.4.8](../changelogs-mariadb-11-4-series/mariadb-11.4.8-changelog.md)
* <sup>_Merge_</sup> [<sup>_Revision #b565b3e7e0_</sup>](https://github.com/MariaDB/server/commit/b565b3e7e0) <sup>_2025-07-28 20:16:25 +0200 - Merge branch '11.4' into 11.8_</sup>
* [Revision #982535b11f](https://github.com/MariaDB/server/commit/982535b11f) <sup>_2025-07-22 15:09:55 +0200_</sup>
  * overflow/inf in vec\_distance\_euclidean
* [Revision #9d3af2c8e3](https://github.com/MariaDB/server/commit/9d3af2c8e3) <sup>_2025-07-21 20:24:34 +0200_</sup>
  * MDEV-37063 Sporadic segmentation faults possibly related to vector search
* [Revision #dfb711e9f4](https://github.com/MariaDB/server/commit/dfb711e9f4) <sup>_2025-07-09 17:16:32 +0200_</sup>
  * fix a typo in a test
* [Revision #3dc0cef218](https://github.com/MariaDB/server/commit/3dc0cef218) <sup>_2025-06-27 21:40:15 +0200_</sup>
  * MDEV-35184 Corruption errors upon creation or usage of Federated table with vector key
* [Revision #ad297c5181](https://github.com/MariaDB/server/commit/ad297c5181) <sup>_2025-06-26 21:35:37 +0200_</sup>
  * MDEV-7761 Some MTR tests fail when run on a host named 'localhost'
* [Revision #eff01f4f07](https://github.com/MariaDB/server/commit/eff01f4f07) <sup>_2025-06-26 21:28:01 +0200_</sup>
  * MDEV-37025 Incorrect error/docs for Vector column lengths (max = 65532
* [Revision #faec725599](https://github.com/MariaDB/server/commit/faec725599) <sup>_2025-06-25 22:15:15 +0200_</sup>
  * MDEV-37005 Unexpected ER\_TABLE\_EXISTS\_ERROR on primary or replica upon CREATE OR REPLACE for partitioned table
* [Revision #e05e6abf24](https://github.com/MariaDB/server/commit/e05e6abf24) <sup>_2025-06-25 10:36:42 +0200_</sup>
  * bugfix: cannot access shared MEM\_ROOT without a lock
* [Revision #9ef20acfbe](https://github.com/MariaDB/server/commit/9ef20acfbe) <sup>_2025-06-24 21:48:26 +0200_</sup>
  * MDEV-37068 Can't find record in 't1' on INSERT to Vector table
* [Revision #a158bbb1a2](https://github.com/MariaDB/server/commit/a158bbb1a2) <sup>_2025-06-22 13:27:05 +0200_</sup>
  * MDEV-36777 create vector table failed with VECTOR INDEX when innodb\_force\_primary\_key=on
* [Revision #98f1623af8](https://github.com/MariaDB/server/commit/98f1623af8) <sup>_2025-06-21 22:26:20 +0200_</sup>
  * MDEV-37022 Assertion when adding FK to MyISAM/Aria table with a vector index
* [Revision #a4f17dc64f](https://github.com/MariaDB/server/commit/a4f17dc64f) <sup>_2025-06-21 18:28:45 +0200_</sup>
  * cleanup: mhnsw - always scale>0
* [Revision #d0c6889149](https://github.com/MariaDB/server/commit/d0c6889149) <sup>_2025-06-20 15:36:13 +0200_</sup>
  * MDEV-37055 UBSAN: 32801 is outside the range of representable values of type 'short'
* [Revision #01c2f6ccf1](https://github.com/MariaDB/server/commit/01c2f6ccf1) <sup>_2025-06-18 18:31:03 +0200_</sup>
  * MDEV-36526 Enable Feedback Plugin for RPM Packages
* [Revision #5d1e485e0a](https://github.com/MariaDB/server/commit/5d1e485e0a) <sup>_2025-04-27 20:12:28 +0200_</sup>
  * MDEV-36531 Enable Feedback Plugin for DEB Packages
* [Revision #050f683c7d](https://github.com/MariaDB/server/commit/050f683c7d) <sup>_2025-06-20 17:28:51 +0200_</sup>
  * cleanup: whitespace
* [Revision #496ba6aee3](https://github.com/MariaDB/server/commit/496ba6aee3) <sup>_2025-04-27 18:04:45 +0200_</sup>
  * MDEV-36532 Enable Feedback Plugin for Windows
* [Revision #c517f0e12d](https://github.com/MariaDB/server/commit/c517f0e12d) <sup>_2025-07-18 12:50:52 +1000_</sup>
  * fix incorrect merge 15700f54c212 (part 3) galera.mariadb\_tzinfo\_to\_sql
* [Revision #63cbca3fba](https://github.com/MariaDB/server/commit/63cbca3fba) <sup>_2025-06-17 14:07:24 -0400_</sup>
  * MDEV-35913 Assertion \`m\_comparator.cmp\_type() != ROW\_RESULT' in Item\_func\_in
* [Revision #665c4fc02d](https://github.com/MariaDB/server/commit/665c4fc02d) <sup>_2025-07-09 10:55:16 +1000_</sup>
  * fix incorrect merge 15700f54c212 (part 2) rocksdb\_rpl.rpl\_xa
* [Revision #7733d63116](https://github.com/MariaDB/server/commit/7733d63116) <sup>_2025-07-03 14:24:15 +0000_</sup>
  * MDEV-36758: always release ctx in mhnsw\_delete\_all
* [Revision #9a4a30aec0](https://github.com/MariaDB/server/commit/9a4a30aec0) <sup>_2025-06-27 10:44:04 +1000_</sup>
  * MDEV-37092 galera\_new\_cluster installed under WITH\_WSREP=OFF
* [Revision #311171c176](https://github.com/MariaDB/server/commit/311171c176) <sup>_2025-06-05 16:14:38 -0500_</sup>
  * MDEV-37107 - Optimise dot\_product by loop-unrolling by a factor of 4
* [Revision #311b4445c5](https://github.com/MariaDB/server/commit/311b4445c5) <sup>_2025-06-26 11:45:33 +0300_</sup>
  * MDEV-35049: Improve test coverage
* [Revision #58b39ea650](https://github.com/MariaDB/server/commit/58b39ea650) <sup>_2025-06-24 15:15:28 +1000_</sup>
  * MDEV-36697: Wrong server.cnf group for version
* <sup>_Merge_</sup> [<sup>_Revision #a65f7dc71d_</sup>](https://github.com/MariaDB/server/commit/a65f7dc71d) <sup>_2025-06-18 07:43:24 +0200 - Merge branch '11.4' into 11.8_</sup>
* [Revision #dbd7017110](https://github.com/MariaDB/server/commit/dbd7017110) <sup>_2025-06-12 14:35:23 -0400_</sup>
  * MDEV-36997 Assertion failed in ha\_tina::delete\_row on multi delete
* [Revision #c095283ea6](https://github.com/MariaDB/server/commit/c095283ea6) <sup>_2025-06-11 09:45:32 +1000_</sup>
  * MDEV-27964: tests - enable msan tests on have\_crypt.inc
* [Revision #972dff0849](https://github.com/MariaDB/server/commit/972dff0849) <sup>_2025-06-11 09:40:32 +1000_</sup>
  * MDEV-34933 remove MSAN exclusion on test plugins.rpl\_auth
* [Revision #5203aeffb4](https://github.com/MariaDB/server/commit/5203aeffb4) <sup>_2025-06-12 11:52:17 +0200_</sup>
  * MDEV-36995: ifunc is not supported by musl
* [Revision #67e6fdee05](https://github.com/MariaDB/server/commit/67e6fdee05) <sup>_2025-06-04 09:39:02 -0400_</sup>
  * bump the VERSION
* <sup>_Merge_</sup> [<sup>_Revision #7dcdb2c876_</sup>](https://github.com/MariaDB/server/commit/7dcdb2c876) <sup>_2025-05-30 13:28:41 +0200 - Merge branch '11.8' into 11.8 release_</sup>
* [Revision #dbee7b7d7c](https://github.com/MariaDB/server/commit/dbee7b7d7c) <sup>_2025-05-28 14:34:26 +0300_</sup>
  * MDEV-36863 InnoDB: Failing assertion: !block->n\_hash\_helps after failing to shrink innodb\_buffer\_pool\_size
* [Revision #d953f2c810](https://github.com/MariaDB/server/commit/d953f2c810) <sup>_2025-05-28 13:33:06 +0300_</sup>
  * MDEV-36868: Inconsistency when shrinking innodb\_buffer\_pool\_size
* [Revision #49f351f583](https://github.com/MariaDB/server/commit/49f351f583) <sup>_2025-05-24 21:24:29 +0400_</sup>
  * MDEV-36835 - main.aborted\_clients fails after various tests
* [Revision #8868737b5a](https://github.com/MariaDB/server/commit/8868737b5a) <sup>_2025-04-09 13:53:59 +0300_</sup>
  * MDEV-36527 : Selecting mysql.wsrep\_streaming\_log incorrectly not allowed when detached
* [Revision #865b05bf4a](https://github.com/MariaDB/server/commit/865b05bf4a) <sup>_2025-02-24 20:53:39 -0700_</sup>
  * MDEV-35837: Update CODING\_STANDARDS to C++17 \[skip ci]
* [Revision #aae8c5a5aa](https://github.com/MariaDB/server/commit/aae8c5a5aa) <sup>_2025-03-05 17:12:25 +0200_</sup>
  * Update 11.8 man pages

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
