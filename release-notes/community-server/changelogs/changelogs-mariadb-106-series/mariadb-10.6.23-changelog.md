# MariaDB 10.6.23 Changelog

<a href="https://mariadb.com/downloads/community" class="button primary">Download</a> <a href="../../mariadb-10-6-series/mariadb-10.6.23-release-notes.md" class="button secondary">Release Notes</a> <a href="mariadb-10.6.23-changelog.md" class="button secondary">Changelog</a> <a href="../../mariadb-10-6-series/what-is-mariadb-106.md" class="button secondary">Overview of 10.6</a>

[<sup>_Alternate download from mariadb.org_</sup>](https://downloads.mariadb.org/mariadb/10.6.23/)

**Release date:** 6 Aug 2025

For the highlights of this release, see the [release notes](../../mariadb-10-6-series/mariadb-10.6.23-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On [GitHub](https://github.com/MariaDB/server/tree/10.6) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Includes all fixes from [MariaDB 10.5.29](../changelogs-mariadb-105-series/mariadb-10-5-29-changelog.md)
* [Revision #fe8047caf2](https://github.com/MariaDB/server/commit/fe8047caf2) <sup>_2025-07-28 15:45:51 +0200_</sup>
  * [MDEV-37320](https://jira.mariadb.org/browse/MDEV-37320) ASAN errors in Field::is\_null / Item\_param::assign\_default
* [Revision #633417308f](https://github.com/MariaDB/server/commit/633417308f) <sup>_2025-07-26 10:26:16 +0200_</sup>
  * [MDEV-37312](https://jira.mariadb.org/browse/MDEV-37312) ASAN errors or assertion failure upon attempt to UPDATE FOR PORTION violating long unique under READ COMMITTED
* [Revision #f49a5beb30](https://github.com/MariaDB/server/commit/f49a5beb30) <sup>_2025-07-25 19:15:09 +0200_</sup>
  * mariadb-backup: read --tables-file in the text mode on Windows
* [Revision #29775c03c1](https://github.com/MariaDB/server/commit/29775c03c1) <sup>_2025-05-20 06:53:03 +0200_</sup>
  * Bug#34422267 - Contribution by Tencent: comment mistake in get\_best\_ror\_intersect
* [Revision #5fa5ee3edb](https://github.com/MariaDB/server/commit/5fa5ee3edb) <sup>_2025-07-24 15:46:45 +0200_</sup>
  * Bug#37117875 test case
* [Revision #1735807448](https://github.com/MariaDB/server/commit/1735807448) <sup>_2025-02-27 08:44:14 +0530_</sup>
  * Bug#37117875 Binlog record error when delimiter is set to other symbols
* [Revision #b0a2b921cc](https://github.com/MariaDB/server/commit/b0a2b921cc) <sup>_2025-07-14 17:13:35 +0200_</sup>
  * ColumnStore 6.4.11-1
* [Revision #a0759bf017](https://github.com/MariaDB/server/commit/a0759bf017) <sup>_2025-07-16 12:50:24 +0200_</sup>
  * Connector/C 3.3.17
* [Revision #a99dfa26d3](https://github.com/MariaDB/server/commit/a99dfa26d3) <sup>_2025-07-14 17:09:11 +0200_</sup>
  * HeidiSQL 12.11
* [Revision #145afe7d79](https://github.com/MariaDB/server/commit/145afe7d79) <sup>_2025-07-14 21:58:59 +0200_</sup>
  * Workaround WolfSSL issue #9004 to fix the build on Windows.
* [Revision #a3c3db7693](https://github.com/MariaDB/server/commit/a3c3db7693) <sup>_2025-07-14 16:38:24 +0200_</sup>
  * update WolfSSL to 5.8.0-stable
* [Revision #fb2f324f85](https://github.com/MariaDB/server/commit/fb2f324f85) <sup>_2025-07-25 12:26:50 +0200_</sup>
  * [MDEV-37310](https://jira.mariadb.org/browse/MDEV-37310) Non-debug failing assertion node->pcur->rel\_pos == BTR\_PCUR\_ON upon violating long unique under READ-COMMITTED
* [Revision #18f85c8c68](https://github.com/MariaDB/server/commit/18f85c8c68) <sup>_2025-07-24 00:11:33 +0200_</sup>
  * [MDEV-37302](https://jira.mariadb.org/browse/MDEV-37302) Assertion failure in Table\_triggers\_list::add\_tables\_and\_routines\_for\_triggers upon attempt to insert DEFAULT into non-insertable view
* [Revision #5622f3f5e8](https://github.com/MariaDB/server/commit/5622f3f5e8) <sup>_2025-07-20 13:04:52 +0200_</sup>
  * [MDEV-37268](https://jira.mariadb.org/browse/MDEV-37268) HA\_ERR\_KEY\_NOT\_FOUND upon UPDATE or partitioned table with unique hash under READ-COMMITTED
* [Revision #2b11a0e991](https://github.com/MariaDB/server/commit/2b11a0e991) <sup>_2025-07-20 13:00:23 +0200_</sup>
  * [MDEV-37268](https://jira.mariadb.org/browse/MDEV-37268) assert upon UPDATE or partitioned table with unique hash under READ-COMMITTED
* [Revision #b96b5a6ccf](https://github.com/MariaDB/server/commit/b96b5a6ccf) <sup>_2025-07-20 16:08:51 +0200_</sup>
  * cleanup: ha\_partition::m\_rec0
* [Revision #774039e410](https://github.com/MariaDB/server/commit/774039e410) <sup>_2025-07-20 12:33:01 +0200_</sup>
  * [MDEV-37268](https://jira.mariadb.org/browse/MDEV-37268) ER\_DUP\_ENTRY upon REPLACE into table with unique hash under READ-COMMITTED
* [Revision #3a2e1f87a1](https://github.com/MariaDB/server/commit/3a2e1f87a1) <sup>_2025-07-20 12:06:42 +0200_</sup>
  * [MDEV-37268](https://jira.mariadb.org/browse/MDEV-37268) ER\_NOT\_KEYFILE or assertion failure upon REPLACE into table with unique hash under READ-COMMITTED
* [Revision #9412cd0e62](https://github.com/MariaDB/server/commit/9412cd0e62) <sup>_2025-07-18 18:59:25 +0530_</sup>
  * [MDEV-35330](https://jira.mariadb.org/browse/MDEV-35330): Assertion marked\_for\_read() failed in VSec9::VSec9 | Item\_func\_from\_unixtime::get\_date
* [Revision #008145b968](https://github.com/MariaDB/server/commit/008145b968) <sup>_2025-07-17 17:21:02 +0200_</sup>
  * galera: changes for transition to galera library 26.4.23
* [Revision #1681b6c330](https://github.com/MariaDB/server/commit/1681b6c330) <sup>_2025-07-17 15:42:59 +0200_</sup>
  * [MDEV-37257](https://jira.mariadb.org/browse/MDEV-37257): unstable tests temporarily added to 'disabled' list
* [Revision #bfcd2674a3](https://github.com/MariaDB/server/commit/bfcd2674a3) <sup>_2025-07-16 16:40:17 +0200_</sup>
  * [MDEV-37199](https://jira.mariadb.org/browse/MDEV-37199) disable --view-protocol
* [Revision #626d5bf832](https://github.com/MariaDB/server/commit/626d5bf832) <sup>_2025-07-16 16:25:53 +0530_</sup>
  * [MDEV-36287](https://jira.mariadb.org/browse/MDEV-36287) mariabackup ignores tables-file
* [Revision #9703c90712](https://github.com/MariaDB/server/commit/9703c90712) <sup>_2025-07-11 15:49:53 +0200_</sup>
  * [MDEV-37199](https://jira.mariadb.org/browse/MDEV-37199) UNIQUE KEY USING HASH accepting duplicate records
* [Revision #2746c19a9c](https://github.com/MariaDB/server/commit/2746c19a9c) <sup>_2025-07-11 11:23:30 +0200_</sup>
  * [MDEV-37203](https://jira.mariadb.org/browse/MDEV-37203) UBSAN: applying zero offset to null pointer in strings/ctype-uca.inl | my\_uca\_strnncollsp\_onelevel\_utf8mb4 | handler::check\_duplicate\_long\_entries\_update
* [Revision #d8c2362912](https://github.com/MariaDB/server/commit/d8c2362912) <sup>_2025-07-10 18:12:41 +0200_</sup>
  * cleanup: long unique checks
* [Revision #dc9bdb4216](https://github.com/MariaDB/server/commit/dc9bdb4216) <sup>_2025-04-16 18:22:05 +0530_</sup>
  * [MDEV-21530](https://jira.mariadb.org/browse/MDEV-21530): json\_extract STILL crashes in Item\_func\_json\_extract::read\_json
* [Revision #024c7e881f](https://github.com/MariaDB/server/commit/024c7e881f) <sup>_2025-07-16 12:01:59 +0300_</sup>
  * [MDEV-37103](https://jira.mariadb.org/browse/MDEV-37103) innodb\_immediate\_scrub\_data\_uncompressed=ON may break innodb\_undo\_log\_truncate=ON
* [Revision #e3c5565dfb](https://github.com/MariaDB/server/commit/e3c5565dfb) <sup>_2025-07-15 16:26:16 +0300_</sup>
  * [MDEV-36330](https://jira.mariadb.org/browse/MDEV-36330) fixup: Only fix innodb\_snapsho\_isolation=ON
* [Revision #3bcfc2ed0a](https://github.com/MariaDB/server/commit/3bcfc2ed0a) <sup>_2025-07-07 13:14:13 +0530_</sup>
  * [MDEV-22250](https://jira.mariadb.org/browse/MDEV-22250) InnoDB: Failing assertion: opt\_no\_lock during mariabackup --backup
* [Revision #b7b2e009b3](https://github.com/MariaDB/server/commit/b7b2e009b3) <sup>_2025-07-14 10:31:56 +0300_</sup>
  * [MDEV-37215](https://jira.mariadb.org/browse/MDEV-37215) SELECT FOR UPDATE crash in SERIALIZABLE
* [Revision #499fa24d63](https://github.com/MariaDB/server/commit/499fa24d63) <sup>_2025-07-14 10:31:48 +0300_</sup>
  * [MDEV-27058](https://jira.mariadb.org/browse/MDEV-27058) fixup: Fix a bogus assertion
* [Revision #ea962ca495](https://github.com/MariaDB/server/commit/ea962ca495) <sup>_2025-07-14 15:45:28 +1000_</sup>
  * [MDEV-30436](https://jira.mariadb.org/browse/MDEV-30436) \[fixup] Add missing check for HAVE\_PSI\_INTERFACE
* [Revision #998e765060](https://github.com/MariaDB/server/commit/998e765060) <sup>_2025-07-10 16:22:47 +1000_</sup>
  * [MDEV-32907](https://jira.mariadb.org/browse/MDEV-32907) Spider: do not create gbh if encountering Item\_aggregate\_ref
* [Revision #3e9aa07cce](https://github.com/MariaDB/server/commit/3e9aa07cce) <sup>_2025-06-05 17:38:17 +1000_</sup>
  * [MDEV-30436](https://jira.mariadb.org/browse/MDEV-30436) Spider: deduplicate some sts/crd code.
* [Revision #a3aab082ff](https://github.com/MariaDB/server/commit/a3aab082ff) <sup>_2025-06-05 17:45:54 +1000_</sup>
  * [MDEV-27474](https://jira.mariadb.org/browse/MDEV-27474) Spider: remove #WITH\_PARTITION\_STORAGE\_ENGINE
* [Revision #c78e906ed5](https://github.com/MariaDB/server/commit/c78e906ed5) <sup>_2025-06-05 16:26:10 +1000_</sup>
  * [MDEV-30264](https://jira.mariadb.org/browse/MDEV-30264) Remove unused method spider\_db\_result::fetch\_row\_from\_tmp\_table
* [Revision #4d19e55441](https://github.com/MariaDB/server/commit/4d19e55441) <sup>_2025-07-12 14:59:11 +0300_</sup>
  * [MDEV-36858](https://jira.mariadb.org/browse/MDEV-36858) MariaDB MyISAM secondary indexes silently break for tables > 10B rows
* [Revision #7fbbbc983f](https://github.com/MariaDB/server/commit/7fbbbc983f) <sup>_2025-07-11 16:07:08 +0300_</sup>
  * [MDEV-36330](https://jira.mariadb.org/browse/MDEV-36330): SERIALIZABLE read inconsistency
* [Revision #f73ffd1150](https://github.com/MariaDB/server/commit/f73ffd1150) <sup>_2025-07-11 15:20:06 +0300_</sup>
  * [MDEV-37183](https://jira.mariadb.org/browse/MDEV-37183) Scrubbing empty record breaks recovery
* [Revision #3b140fed0d](https://github.com/MariaDB/server/commit/3b140fed0d) <sup>_2025-07-11 09:52:17 +0200_</sup>
  * bump the VERSION
* [Revision #c27d78beb5](https://github.com/MariaDB/server/commit/c27d78beb5) <sup>_2025-06-30 15:44:50 +0200_</sup>
  * [MDEV-36870](https://jira.mariadb.org/browse/MDEV-36870) Spurious unrelated permission error when selecting from table with default that uses nextval(sequence)
* [Revision #1c7685f5fc](https://github.com/MariaDB/server/commit/1c7685f5fc) <sup>_2025-06-30 10:35:48 +0200_</sup>
  * bugfix: nextval() in default, and UPDATE SET x=DEFAULT
* [Revision #4c8af2007d](https://github.com/MariaDB/server/commit/4c8af2007d) <sup>_2025-06-19 11:32:40 +0200_</sup>
  * [MDEV-36934](https://jira.mariadb.org/browse/MDEV-36934): semi sync makes the master unresponsive when a replica is stopped
* [Revision #c4a2688328](https://github.com/MariaDB/server/commit/c4a2688328) <sup>_2025-05-25 23:23:29 +0300_</sup>
  * [MDEV-24726](https://jira.mariadb.org/browse/MDEV-24726) Assertion on compressed varstring as key field in optimizer temporary table
* [Revision #31aa8b6939](https://github.com/MariaDB/server/commit/31aa8b6939) <sup>_2025-07-07 09:30:34 +0300_</sup>
  * [MDEV-37170](https://jira.mariadb.org/browse/MDEV-37170) Enable AVX10.1 CRC-32 on GCC 16
* [Revision #a293dfd92a](https://github.com/MariaDB/server/commit/a293dfd92a) <sup>_2025-06-01 17:35:07 +0300_</sup>
  * Fix building with gcc 16 (evex512 removal)
* [Revision #27660ff2e9](https://github.com/MariaDB/server/commit/27660ff2e9) <sup>_2025-07-01 10:59:20 +0530_</sup>
  * [MDEV-37121](https://jira.mariadb.org/browse/MDEV-37121) Change buffer freed pages are not removed during slow shutdown
* [Revision #9059385262](https://github.com/MariaDB/server/commit/9059385262) <sup>_2025-06-20 10:41:50 +1000_</sup>
  * [MDEV-37048](https://jira.mariadb.org/browse/MDEV-37048) revert MSAN my\_vsnprintf\_ex for double workaround
* [Revision #0dd6566ee4](https://github.com/MariaDB/server/commit/0dd6566ee4) <sup>_2025-07-02 14:25:38 +0530_</sup>
  * [MDEV-37123](https://jira.mariadb.org/browse/MDEV-37123) dict\_table\_open\_on\_id() fails to release dict\_sys.latch
* [Revision #2d5dfc47a9](https://github.com/MariaDB/server/commit/2d5dfc47a9) <sup>_2025-06-30 15:48:26 +0300_</sup>
  * Define error message for HA\_ERR\_INCOMPATIBLE\_DEFINITION
* [Revision #56fbc0cdd7](https://github.com/MariaDB/server/commit/56fbc0cdd7) <sup>_2025-06-06 10:42:40 +0300_</sup>
  * [MDEV-36953](https://jira.mariadb.org/browse/MDEV-36953) : mysql-wsrep#198 test hangs
* [Revision #f495460689](https://github.com/MariaDB/server/commit/f495460689) <sup>_2025-06-09 11:00:27 +0300_</sup>
  * [MDEV-36968](https://jira.mariadb.org/browse/MDEV-36968) : galera\_3nodes.inconsistency\_shutdown test occasionally hangs
* [Revision #fd1266a980](https://github.com/MariaDB/server/commit/fd1266a980) <sup>_2025-06-11 15:57:42 +0300_</sup>
  * [MDEV-34761](https://jira.mariadb.org/browse/MDEV-34761) : Assertion client\_state\_.mode() == wsrep::client\_state::m\_local failed in int wsrep::transaction::after\_statement(wsrep::unique\_lock[wsrep::mutex](wsrep::mutex)&)
* [Revision #f41acb555d](https://github.com/MariaDB/server/commit/f41acb555d) <sup>_2025-06-23 08:56:00 +0300_</sup>
  * [MDEV-35523](https://jira.mariadb.org/browse/MDEV-35523) : Server crashes with "WSREP: Unknown writeset version: -1"
* [Revision #c3578720e6](https://github.com/MariaDB/server/commit/c3578720e6) <sup>_2025-06-28 14:32:31 +0300_</sup>
  * Removed safemalloc warnings from myisamchk --version
* [Revision #3c67d73aad](https://github.com/MariaDB/server/commit/3c67d73aad) <sup>_2025-06-26 10:05:36 +0300_</sup>
  * [MDEV-36482](https://jira.mariadb.org/browse/MDEV-36482): Make libaio work WITH\_MSAN=ON
* [Revision #e706324205](https://github.com/MariaDB/server/commit/e706324205) <sup>_2025-06-23 15:48:13 +0530_</sup>
  * [MDEV-35863](https://jira.mariadb.org/browse/MDEV-35863) innodb.doublewrite\_debug test case fails to start the server
* [Revision #cda1826201](https://github.com/MariaDB/server/commit/cda1826201) <sup>_2025-05-21 14:56:16 +0200_</sup>
  * [MDEV-36852](https://jira.mariadb.org/browse/MDEV-36852) Table definition gets corrupt after adding unique hash key
* [Revision #6ec57588bd](https://github.com/MariaDB/server/commit/6ec57588bd) <sup>_2025-06-11 20:47:43 +0530_</sup>
  * [MDEV-30363](https://jira.mariadb.org/browse/MDEV-30363) InnoDB: Failing assertion: trx->error\_state == DB\_SUCCESS in que\_run\_threads
* [Revision #888663ce12](https://github.com/MariaDB/server/commit/888663ce12) <sup>_2025-06-03 10:32:22 +0200_</sup>
  * [MDEV-36280](https://jira.mariadb.org/browse/MDEV-36280) ALTER TABLE with DEFAULT NEXTVAL(sequence) fails due to insufficient grants
* [Revision #643319a7fb](https://github.com/MariaDB/server/commit/643319a7fb) <sup>_2025-05-30 11:22:58 +0300_</sup>
  * [MDEV-36465](https://jira.mariadb.org/browse/MDEV-36465) [MDEV-33813](https://jira.mariadb.org/browse/MDEV-33813) Regression, Queries in 'Waiting for someone to free space' state will not automatically retry IO and hang forever
* [Revision #0a91bbdc41](https://github.com/MariaDB/server/commit/0a91bbdc41) <sup>_2025-05-27 10:57:16 +0300_</sup>
  * Get debug version to compile with gcc 7.5.0
* [Revision #ce4f83e6b9](https://github.com/MariaDB/server/commit/ce4f83e6b9) <sup>_2025-05-25 15:47:26 +0300_</sup>
  * [MDEV-29157](https://jira.mariadb.org/browse/MDEV-29157) SELECT using ror\_merged scan fails with s3 tables
* [Revision #5f83b219bb](https://github.com/MariaDB/server/commit/5f83b219bb) <sup>_2025-05-21 10:59:34 +0300_</sup>
  * Fixed compiler warning from clang in connect/tabxcl.cpp
* [Revision #6878c14000](https://github.com/MariaDB/server/commit/6878c14000) <sup>_2025-05-20 10:39:53 +0300_</sup>
  * Updated storage/maria/ma\_test\_big.sh to use aria\_ instead of maria\_
* [Revision #22024da64e](https://github.com/MariaDB/server/commit/22024da64e) <sup>_2025-05-08 15:08:02 +0300_</sup>
  * [MDEV-36143](https://jira.mariadb.org/browse/MDEV-36143) Row event replication with Aria does not honour BLOCK\_COMMIT
* [Revision #f533333f82](https://github.com/MariaDB/server/commit/f533333f82) <sup>_2025-05-29 11:28:15 +1000_</sup>
  * [MDEV-34388](https://jira.mariadb.org/browse/MDEV-34388): Stack overflow on Alpine Linux (postfix) - sanitizers
* [Revision #fe6a5c2200](https://github.com/MariaDB/server/commit/fe6a5c2200) <sup>_2025-05-28 11:28:17 +0300_</sup>
  * [MDEV-29155](https://jira.mariadb.org/browse/MDEV-29155) CREATE OR REPLACE with self-referencing CHECK hangs forever, cannot be killed
* [Revision #0b2434d2e9](https://github.com/MariaDB/server/commit/0b2434d2e9) <sup>_2025-05-28 11:28:16 +0300_</sup>
  * [MDEV-25158](https://jira.mariadb.org/browse/MDEV-25158) Segfault on INTERSECT ALL with UNION in Oracle mode
* [Revision #e021a61b6f](https://github.com/MariaDB/server/commit/e021a61b6f) <sup>_2025-05-02 17:13:28 +1000_</sup>
  * [MDEV-36729](https://jira.mariadb.org/browse/MDEV-36729): ha\_example::show\_func\_example is incorrectly defined
* [Revision #88d35c5c51](https://github.com/MariaDB/server/commit/88d35c5c51) <sup>_2025-05-28 17:07:50 +1000_</sup>
  * [MDEV-34388](https://jira.mariadb.org/browse/MDEV-34388): Stack overflow on Alpine Linux (postfix) mroonga+asan
* [Revision #676aea8cad](https://github.com/MariaDB/server/commit/676aea8cad) <sup>_2025-05-28 15:03:05 +1000_</sup>
  * [MDEV-36848](https://jira.mariadb.org/browse/MDEV-36848): identify tests with various MSAN suitability
* [Revision #5dbfb52d04](https://github.com/MariaDB/server/commit/5dbfb52d04) <sup>_2025-05-28 14:03:40 +1000_</sup>
  * [MDEV-36894](https://jira.mariadb.org/browse/MDEV-36894) JSNX::SetArrayOptions and BJNX::SetArrayOptions unused nm arg
* [Revision #495153feac](https://github.com/MariaDB/server/commit/495153feac) <sup>_2025-05-28 11:48:04 +1000_</sup>
  * [MDEV-36893](https://jira.mariadb.org/browse/MDEV-36893) THD::reset\_sub\_statement\_state swaps with uninitialized structure
* [Revision #8d2665e56b](https://github.com/MariaDB/server/commit/8d2665e56b) <sup>_2025-03-20 09:24:37 +1100_</sup>
  * [MDEV-34388](https://jira.mariadb.org/browse/MDEV-34388) default stack size under MSAN needs increasing
* [Revision #2811559337](https://github.com/MariaDB/server/commit/2811559337) <sup>_2025-05-24 15:55:29 +1000_</sup>
  * version string - memory sanitizer isn't the same as valgrind
* [Revision #8490901307](https://github.com/MariaDB/server/commit/8490901307) <sup>_2025-05-23 19:59:58 +1000_</sup>
  * [MDEV-34388](https://jira.mariadb.org/browse/MDEV-34388): Stack overflow on Alpine Linux (postfix - ASAN/MSAN+Debug)
* [Revision #5012402330](https://github.com/MariaDB/server/commit/5012402330) <sup>_2025-05-23 19:55:20 +1000_</sup>
  * [MDEV-34388](https://jira.mariadb.org/browse/MDEV-34388) Alpine Stack Overflow - reduce Grant\_tables::open\_and\_lock
* [Revision #df414933f1](https://github.com/MariaDB/server/commit/df414933f1) <sup>_2025-05-23 20:02:45 +1000_</sup>
  * [MDEV-36316](https://jira.mariadb.org/browse/MDEV-36316)/[MDEV-36327](https://jira.mariadb.org/browse/MDEV-36327)/[MDEV-36328](https://jira.mariadb.org/browse/MDEV-36328) Debug msan
* [Revision #507cbde68f](https://github.com/MariaDB/server/commit/507cbde68f) <sup>_2025-05-27 08:05:19 +0300_</sup>
  * [MDEV-36882](https://jira.mariadb.org/browse/MDEV-36882): Inconsistent DBUG\_ASSERT trips GCC -Og
* [Revision #aba04c562b](https://github.com/MariaDB/server/commit/aba04c562b) <sup>_2025-05-26 16:26:03 +0200_</sup>
  * Compiling - fix warnings with MSVC 17.14
* [Revision #8a4d3a044f](https://github.com/MariaDB/server/commit/8a4d3a044f) <sup>_2025-05-25 09:11:41 +0530_</sup>
  * [MDEV-36017](https://jira.mariadb.org/browse/MDEV-36017) Alter table aborts when temporary directory is full
* [Revision #4c8143b451](https://github.com/MariaDB/server/commit/4c8143b451) <sup>_2025-05-23 14:18:07 +0200_</sup>
  * Make it compiling with last gcc
* [Revision #1037f95941](https://github.com/MariaDB/server/commit/1037f95941) <sup>_2025-05-21 11:10:09 +0300_</sup>
  * [MDEV-33675](https://jira.mariadb.org/browse/MDEV-33675) Assertion(reclength < vreclength) in setup\_vcols\_for\_repair()
* [Revision #1a95c2a4b2](https://github.com/MariaDB/server/commit/1a95c2a4b2) <sup>_2025-05-21 11:10:09 +0300_</sup>
  * [MDEV-36817](https://jira.mariadb.org/browse/MDEV-36817) Server crashes in do\_mark\_index\_columns instead of ER\_DUP\_ENTRY on partitioned table
* [Revision #fbd736c872](https://github.com/MariaDB/server/commit/fbd736c872) <sup>_2025-05-21 11:10:09 +0300_</sup>
  * mysqltest: result\_format fix
* [Revision #d5247592c5](https://github.com/MariaDB/server/commit/d5247592c5) <sup>_2025-05-21 11:10:09 +0300_</sup>
  * Test sysvars\_server failure fix
* [Revision #2c4fe3557a](https://github.com/MariaDB/server/commit/2c4fe3557a) <sup>_2025-03-28 17:58:06 +1100_</sup>
  * [MDEV-36337](https://jira.mariadb.org/browse/MDEV-36337): mroonga\_\* udf correct ptr types for is\_null/error
* [Revision #b9a20752a9](https://github.com/MariaDB/server/commit/b9a20752a9) <sup>_2025-03-21 16:37:44 +1100_</sup>
  * [MDEV-36337](https://jira.mariadb.org/browse/MDEV-36337) auth\_ed25519 correct UDF pointers for is\_null/error
* [Revision #0b5a084e27](https://github.com/MariaDB/server/commit/0b5a084e27) <sup>_2025-03-20 19:21:56 +1100_</sup>
  * [MDEV-36337](https://jira.mariadb.org/browse/MDEV-36337): connect UDF pointers need unsigned char\* for is\_null/error
* [Revision #c91c2e74ff](https://github.com/MariaDB/server/commit/c91c2e74ff) <sup>_2025-03-20 18:31:25 +1100_</sup>
  * [MDEV-36337](https://jira.mariadb.org/browse/MDEV-36337): udf\_example UDF pointers need unsigned is\_null/error
* [Revision #497d6324bc](https://github.com/MariaDB/server/commit/497d6324bc) <sup>_2025-04-28 07:35:06 +0300_</sup>
  * [MDEV-36627](https://jira.mariadb.org/browse/MDEV-36627) : galera.[MDEV-29142](https://jira.mariadb.org/browse/MDEV-29142): certification position less than last commited
* [Revision #7aed06887b](https://github.com/MariaDB/server/commit/7aed06887b) <sup>_2025-04-28 10:27:19 +0300_</sup>
  * [MDEV-36512](https://jira.mariadb.org/browse/MDEV-36512) : galera\_3nodes.GCF-354: certification position less than last committed
* [Revision #7fd5957d55](https://github.com/MariaDB/server/commit/7fd5957d55) <sup>_2025-05-06 08:15:36 +0300_</sup>
  * [MDEV-36622](https://jira.mariadb.org/browse/MDEV-36622) : Hang during galera\_evs\_suspect\_timeout test
* [Revision #d38558f99b](https://github.com/MariaDB/server/commit/d38558f99b) <sup>_2025-04-29 18:31:13 +0530_</sup>
  * [MDEV-36117](https://jira.mariadb.org/browse/MDEV-36117): MDL BF-BF conflict on ALTER and UPDATE with multi-level foreign key parents
* [Revision #a96367bc67](https://github.com/MariaDB/server/commit/a96367bc67) <sup>_2025-05-08 11:58:31 +0300_</sup>
  * [MDEV-36620](https://jira.mariadb.org/browse/MDEV-36620) post-fix: galera\_toi\_ddl\_nonconflicting test failure
* [Revision #82d7419e06](https://github.com/MariaDB/server/commit/82d7419e06) <sup>_2025-05-20 17:27:05 +0300_</sup>
  * [MDEV-34388](https://jira.mariadb.org/browse/MDEV-34388): Stack overflow on Alpine Linux
* [Revision #2350295643](https://github.com/MariaDB/server/commit/2350295643) <sup>_2025-05-06 02:26:35 +0200_</sup>
  * [MDEV-36740](https://jira.mariadb.org/browse/MDEV-36740): galera.galera\_ssl\_upgrade fails due to expired certificate
* [Revision #d7457b4076](https://github.com/MariaDB/server/commit/d7457b4076) <sup>_2025-04-24 14:11:38 +0300_</sup>
  * [MDEV-36628](https://jira.mariadb.org/browse/MDEV-36628) : galera\_vote\_during\_ist test failed
* [Revision #60f046d7e6](https://github.com/MariaDB/server/commit/60f046d7e6) <sup>_2025-05-02 17:34:39 +1000_</sup>
  * [MDEV-35009](https://jira.mariadb.org/browse/MDEV-35009): Initialize affected\_rows in SQL service
* [Revision #c626715439](https://github.com/MariaDB/server/commit/c626715439) <sup>_2025-04-30 10:38:44 +1000_</sup>
  * [MDEV-35452](https://jira.mariadb.org/browse/MDEV-35452) \[fixup] fix spider/bugfix.perfschema view protocol
* <sup>_Merge_</sup> [<sup>_Revision #76e8e24b0b_</sup>](https://github.com/MariaDB/server/commit/76e8e24b0b) <sup>_2025-04-30 10:35:11 +1000 - Merge branch '10.5' into 10.6_</sup>
* [Revision #5c92b27d54](https://github.com/MariaDB/server/commit/5c92b27d54) <sup>_2025-04-17 15:35:38 +1000_</sup>
  * [MDEV-36633](https://jira.mariadb.org/browse/MDEV-36633) [MDEV-35452](https://jira.mariadb.org/browse/MDEV-35452) spider/bugfix.mdev\_33434 reports wrong error in view protocol
* [Revision #b1446080d1](https://github.com/MariaDB/server/commit/b1446080d1) <sup>_2025-04-16 17:31:39 +1000_</sup>
  * [MDEV-36476](https://jira.mariadb.org/browse/MDEV-36476) [MDEV-35452](https://jira.mariadb.org/browse/MDEV-35452) Disable view protocol for spider tests where thread metadata could prevent lock wait timeout
* [Revision #08793310fb](https://github.com/MariaDB/server/commit/08793310fb) <sup>_2025-04-16 14:45:21 +1000_</sup>
  * [MDEV-36478](https://jira.mariadb.org/browse/MDEV-36478) [MDEV-35452](https://jira.mariadb.org/browse/MDEV-35452) Remove blocks testing SELECT SQL\_CALC\_FOUND\_ROWS from spider tests
* [Revision #9089a75b7f](https://github.com/MariaDB/server/commit/9089a75b7f) <sup>_2025-04-15 14:30:35 +1000_</sup>
  * [MDEV-36477](https://jira.mariadb.org/browse/MDEV-36477) [MDEV-35452](https://jira.mariadb.org/browse/MDEV-35452) Fix Spider tests with view protocol fail with "Failed to drop view: 0: "
* [Revision #d3c5c47e0e](https://github.com/MariaDB/server/commit/d3c5c47e0e) <sup>_2025-04-02 14:20:25 +1100_</sup>
  * [MDEV-36324](https://jira.mariadb.org/browse/MDEV-36324) [MDEV-35452](https://jira.mariadb.org/browse/MDEV-35452) Missing appending FROM ... in spider\_mbase\_handler::append\_key\_select
* [Revision #55ddfe1c95](https://github.com/MariaDB/server/commit/55ddfe1c95) <sup>_2025-04-28 22:45:10 +0400_</sup>
  * [MDEV-36684](https://jira.mariadb.org/browse/MDEV-36684) - main.mdl\_sync fails under valgrind (test for Bug#42643)
* [Revision #83e0438f62](https://github.com/MariaDB/server/commit/83e0438f62) <sup>_2025-04-29 11:34:35 +0200_</sup>
  * [MDEV-36536](https://jira.mariadb.org/browse/MDEV-36536) post-review changes
* [Revision #739578915f](https://github.com/MariaDB/server/commit/739578915f) <sup>_2025-04-28 17:47:45 +0200_</sup>
  * Make the test more stable.
* [Revision #d9cd4e1f75](https://github.com/MariaDB/server/commit/d9cd4e1f75) <sup>_2025-04-22 16:54:25 +0300_</sup>
  * [MDEV-22250](https://jira.mariadb.org/browse/MDEV-22250) InnoDB: Failing assertion: opt\_no\_lock during mariabackup --backup
* [Revision #1b934a387c](https://github.com/MariaDB/server/commit/1b934a387c) <sup>_2025-04-21 19:12:58 +0300_</sup>
  * [MDEV-36536](https://jira.mariadb.org/browse/MDEV-36536) Add option to not collect statistics for long char/varchars
* [Revision #2b448e7337](https://github.com/MariaDB/server/commit/2b448e7337) <sup>_2025-04-17 10:51:48 +0300_</sup>
  * print\_ddl\_recovery\_log.pl ; Print content of the ddl\_recovery.log

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
