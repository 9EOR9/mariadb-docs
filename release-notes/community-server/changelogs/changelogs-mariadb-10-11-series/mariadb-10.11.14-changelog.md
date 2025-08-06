# MariaDB 10.11.14 Changelog

<a href="https://mariadb.com/downloads/community" class="button primary">Download</a> <a href="../../mariadb-10-11-series/mariadb-10.11.14-release-notes.md" class="button secondary">Release Notes</a> <a href="mariadb-10.11.14-changelog.md" class="button secondary">Changelog</a> <a href="../../mariadb-10-11-series/what-is-mariadb-1011.md" class="button secondary">Overview of 10.11</a>

[<sup>_Alternate download from mariadb.org_</sup>](https://downloads.mariadb.org/mariadb/10.11.14/)

**Release date:** 6 Aug 2025

For the highlights of this release, see the [release notes](../../mariadb-10-11-series/mariadb-10.11.14-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On [GitHub](https://github.com/MariaDB/server/tree/10.11) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Includes all fixes from [MariaDB 10.6.23](../changelogs-mariadb-106-series/mariadb-10.6.23-changelog.md)
* <sup>_Merge_</sup> [<sup>_Revision #053f9bcb5b_</sup>](https://github.com/MariaDB/server/commit/053f9bcb5b) <sup>_2025-07-28 18:06:31 +0200 - Merge branch '10.6' into 10.11_</sup>
* [Revision #cbcb080a1f](https://github.com/MariaDB/server/commit/cbcb080a1f) <sup>_2025-07-28 16:44:59 +0200_</sup>
  * MDEV-37328 Assertion failure in make\_empty\_rec upon CONVERT PARTITION
* [Revision #03dd699ffe](https://github.com/MariaDB/server/commit/03dd699ffe) <sup>_2025-07-27 00:16:14 +0200_</sup>
  * MDEV-37315 Assertion '!xid\_state.xid\_cache\_element' failed in trans\_xa\_rollback
* [Revision #288db5fa5f](https://github.com/MariaDB/server/commit/288db5fa5f) <sup>_2025-07-18 20:32:45 +0200_</sup>
  * MDEV-24981 LOAD INDEX may cause rollback of prepared XA transaction
* [Revision #d6cb7255e9](https://github.com/MariaDB/server/commit/d6cb7255e9) <sup>_2025-07-12 19:28:23 +0300_</sup>
  * MDEV-30711: Crash in add\_keyuses\_for\_splitting() when joining with a derived table
* [Revision #5f51a3a6eb](https://github.com/MariaDB/server/commit/5f51a3a6eb) <sup>_2025-07-08 15:53:18 -0600_</sup>
  * MDEV-36906: RBR crashes upon DML after CONVERT PARTITION
* [Revision #33e845595d](https://github.com/MariaDB/server/commit/33e845595d) <sup>_2025-07-15 20:40:27 -0600_</sup>
  * MDEV-36839: Revert MDEV-7409
* [Revision #76c79d4fd8](https://github.com/MariaDB/server/commit/76c79d4fd8) <sup>_2025-07-17 19:52:27 -0600_</sup>
  * MDEV-37060: Don’t check Encrpyted Server IDs in mariadb-binlog
* [Revision #687c8be813](https://github.com/MariaDB/server/commit/687c8be813) <sup>_2025-07-21 14:44:49 +1100_</sup>
  * MDEV-19269 Pushdown into IN subquery is not made on the second execution of stmt
* [Revision #55e0c34f4f](https://github.com/MariaDB/server/commit/55e0c34f4f) <sup>_2025-07-18 10:06:33 +0300_</sup>
  * MDEV-37263 Hang or crash when shrinking innodb\_buffer\_pool\_size
* [Revision #733c58a71e](https://github.com/MariaDB/server/commit/733c58a71e) <sup>_2025-07-17 13:30:17 +0200_</sup>
  * MDEV-37232 - fix embedded build on Windows
* [Revision #cedfe8eca4](https://github.com/MariaDB/server/commit/cedfe8eca4) <sup>_2025-07-17 12:24:25 +0300_</sup>
  * MDEV-37250 buf\_pool\_t::shrink() assertion failure
* [Revision #a8eeffb0a3](https://github.com/MariaDB/server/commit/a8eeffb0a3) <sup>_2025-07-16 23:19:01 +0200_</sup>
  * MDEV-18030 waiting\_threads-t is disabled
* [Revision #aedc65fe10](https://github.com/MariaDB/server/commit/aedc65fe10) <sup>_2025-07-08 14:01:50 +0300_</sup>
  * MDEV-30364 Assertion MDL\_EXCLUSIVE on DISCARD TABLESPACE in LOCK TABLE mode
* [Revision #db3e1edac3](https://github.com/MariaDB/server/commit/db3e1edac3) <sup>_2025-07-16 13:23:16 +0200_</sup>
  * MDEV-36814 MariaDB 10.11.9 Signal 11 crash on second Stored Procedure call
* [Revision #9a51709dba](https://github.com/MariaDB/server/commit/9a51709dba) <sup>_2025-07-09 15:45:35 +0300_</sup>
  * MDEV-29001 DROP DEFAULT makes SHOW CREATE non-idempotent
* [Revision #67745e4dbf](https://github.com/MariaDB/server/commit/67745e4dbf) <sup>_2023-02-02 06:29:05 +1200_</sup>
  * MDEV-30334 Optimizer trace produces invalid JSON with WHERE subquery
* [Revision #552c477950](https://github.com/MariaDB/server/commit/552c477950) <sup>_2024-09-19 09:31:54 +0200_</sup>
  * MDEV-34926: mysql-install-db suggests a deprecated procedure
* [Revision #c05b1fe2c2](https://github.com/MariaDB/server/commit/c05b1fe2c2) <sup>_2025-07-13 09:46:40 +0200_</sup>
  * MDEV-21654 binary library file pam\_mariadb\_mtr.so installed among test data files
* [Revision #b1daecfc45](https://github.com/MariaDB/server/commit/b1daecfc45) <sup>_2025-07-13 09:36:08 +0200_</sup>
  * MDEV-30190 Password check plugin prevents changing grants for CURRENT\_USER
* [Revision #aef0468c18](https://github.com/MariaDB/server/commit/aef0468c18) <sup>_2024-12-13 11:56:31 +0100_</sup>
  * cleanup: select ... into tests
* [Revision #29277bf9d9](https://github.com/MariaDB/server/commit/29277bf9d9) <sup>_2025-07-08 22:18:10 +0200_</sup>
  * MDEV-36701 command line client doesn't check session\_track information
* [Revision #e925ddd234](https://github.com/MariaDB/server/commit/e925ddd234) <sup>_2025-07-12 23:33:25 +0200_</sup>
  * MDEV-27578 DESC attribute upon spatial index creation prevents ER\_DUP\_INDEX warning
* [Revision #dd63c6c9e3](https://github.com/MariaDB/server/commit/dd63c6c9e3) <sup>_2025-07-07 21:56:33 +0200_</sup>
  * MDEV-29186 Query cache makes virtual column function RAND() non-random
* [Revision #9fc124f8f9](https://github.com/MariaDB/server/commit/9fc124f8f9) <sup>_2025-07-05 00:21:53 +0200_</sup>
  * MDEV-25415 CASE function handles NULL inconsistently
* [Revision #1ac4aeb5d8](https://github.com/MariaDB/server/commit/1ac4aeb5d8) <sup>_2025-07-03 22:16:45 +0200_</sup>
  * MDEV-35581 On servers linked against WolfSSL SSL\_Cipher and SSL\_cipher\_list are always the same
* [Revision #0d20ed9eae](https://github.com/MariaDB/server/commit/0d20ed9eae) <sup>_2025-07-02 22:27:55 +0200_</sup>
  * MDEV-35580 Server using WolfSSL shows different name than OpenSSL for some ciphers
* [Revision #04122ed770](https://github.com/MariaDB/server/commit/04122ed770) <sup>_2025-06-21 00:15:59 +0200_</sup>
  * MDEV-36815 Fresh MariaDB 11.4 installation gives errors when configuring utf8
* [Revision #46135c625b](https://github.com/MariaDB/server/commit/46135c625b) <sup>_2025-06-17 19:08:40 +0200_</sup>
  * MDEV-36979 Same alias name with different case on same table is not working in functions
* [Revision #9253d6dad5](https://github.com/MariaDB/server/commit/9253d6dad5) <sup>_2025-05-27 10:52:32 +0200_</sup>
  * MDEV-12237 main.analyze\_stmt\_slow\_query\_log failed in buildbot
* [Revision #db2f3d230c](https://github.com/MariaDB/server/commit/db2f3d230c) <sup>_2025-05-19 18:30:37 +0200_</sup>
  * pluggable auth: server should escape '\0' too, it's OK packet
* [Revision #cb7978a12d](https://github.com/MariaDB/server/commit/cb7978a12d) <sup>_2025-05-16 11:29:56 +0200_</sup>
  * MDEV-36720 Possible memory leak on updating table with index without overlaps
* [Revision #9306353d2d](https://github.com/MariaDB/server/commit/9306353d2d) <sup>_2025-05-07 16:17:37 +0200_</sup>
  * MDEV-36753 Assertion 'str[strlen(str)-1] != '\n'' failed in my\_message\_sql upon REPAIR .. USE\_FRM with encryption enabled
* [Revision #0b16d7871c](https://github.com/MariaDB/server/commit/0b16d7871c) <sup>_2025-06-21 14:56:00 -0400_</sup>
  * MDEV-37195:
* [Revision #16190d2d77](https://github.com/MariaDB/server/commit/16190d2d77) <sup>_2025-07-15 12:01:08 -0600_</sup>
  * Sort output of binlog\_mysqlbinlog\_warn\_stop\_gtid
* [Revision #b1829ff821](https://github.com/MariaDB/server/commit/b1829ff821) <sup>_2025-07-07 12:53:46 +0530_</sup>
  * MDEV-22250 InnoDB: Failing assertion: opt\_no\_lock during mariabackup --backup
* [Revision #bd3ee3a9a2](https://github.com/MariaDB/server/commit/bd3ee3a9a2) <sup>_2025-07-14 16:22:59 -0600_</sup>
  * MDEV-34614 mysqlbinlog warn on EOF before GTID in --stop-position
* [Revision #d9bb59e7af](https://github.com/MariaDB/server/commit/d9bb59e7af) <sup>_2025-06-17 17:05:43 +1000_</sup>
  * MDEV-37018 Remove SELECT\_LEX::select\_h
* [Revision #b6385e00b6](https://github.com/MariaDB/server/commit/b6385e00b6) <sup>_2025-07-08 21:31:51 -0600_</sup>
  * MDEV-7611 mysqldump --dump-slave always starts stopped slave
* [Revision #add6a0557f](https://github.com/MariaDB/server/commit/add6a0557f) <sup>_2025-07-08 19:13:58 -0600_</sup>
  * MDEV-7611: create multi\_source.mariadb-dump\_slave
* [Revision #7d7898a47e](https://github.com/MariaDB/server/commit/7d7898a47e) <sup>_2025-07-10 18:33:24 +1000_</sup>
  * MDEV-37169: MSAN disable main.{mysqladmin,statistics\_upgrade\_not\_done}
* [Revision #6af171f3bf](https://github.com/MariaDB/server/commit/6af171f3bf) <sup>_2025-06-15 20:46:40 -0400_</sup>
  * MDEV-36410: Wrong Result with Desc Primary Key in Index
* [Revision #7f77041b0a](https://github.com/MariaDB/server/commit/7f77041b0a) <sup>_2025-07-02 19:00:17 +0530_</sup>
  * MDEV-37141 DML committed within XA transaction block after deadlock error and implicit rollback
* [Revision #56ce9e72a1](https://github.com/MariaDB/server/commit/56ce9e72a1) <sup>_2025-06-14 06:30:53 -0400_</sup>
  * MDEV-35353: write rows\_examined for union\_all queries
* [Revision #96045fb53a](https://github.com/MariaDB/server/commit/96045fb53a) <sup>_2025-07-05 10:56:59 +1000_</sup>
  * MDEV-37052: JSON\_TABLE stack overflow handling errors
* [Revision #30185c9c7c](https://github.com/MariaDB/server/commit/30185c9c7c) <sup>_2025-06-15 14:27:40 +0300_</sup>
  * MDEV-23207 Assertion 'tl-\>table == \_\_null' failed in THD::open\_temporary\_table
* [Revision #fc465596ea](https://github.com/MariaDB/server/commit/fc465596ea) <sup>_2025-07-08 14:01:50 +0300_</sup>
  * MDEV-37164 Assertion 'vers\_conditions.delete\_history' failed upon PREPARE
* [Revision #39f4908216](https://github.com/MariaDB/server/commit/39f4908216) <sup>_2025-07-08 13:16:09 +0200_</sup>
  * update ColumnStore
* [Revision #f7ba16980d](https://github.com/MariaDB/server/commit/f7ba16980d) <sup>_2025-07-07 13:01:24 -0600_</sup>
  * MDEV-36840 Seconds\_Behind\_Master Spike at Log Rotation on Parallel Replica
* [Revision #8a45128106](https://github.com/MariaDB/server/commit/8a45128106) <sup>_2025-07-07 13:33:34 -0600_</sup>
  * Add MDEV-25999 & MDEV-36840 to MDEV-16091’s test
* [Revision #7a6da5b77b](https://github.com/MariaDB/server/commit/7a6da5b77b) <sup>_2025-06-10 10:28:15 -0600_</sup>
  * Fix 'sql/slave.cc:next\_event' documentation
* [Revision #f8aec6fd52](https://github.com/MariaDB/server/commit/f8aec6fd52) <sup>_2025-07-07 13:06:41 +0200_</sup>
  * MDEV-26235 Install 64bit heidisql on 64bit Windows
* [Revision #8c817e2d8a](https://github.com/MariaDB/server/commit/8c817e2d8a) <sup>_2025-05-13 17:10:30 +0300_</sup>
  * MDEV-35570 parallel slave ALTER-SEQUENCE attempted to binlog out-of-order
* [Revision #e79aa9ca38](https://github.com/MariaDB/server/commit/e79aa9ca38) <sup>_2025-06-23 12:13:53 +1000_</sup>
  * MDEV-37052: JSON\_TABLE stack overflow handling errors
* [Revision #7c807e1075](https://github.com/MariaDB/server/commit/7c807e1075) <sup>_2025-06-30 16:41:18 -0600_</sup>
  * MDEV-37102: Fix Test by Waiting for the State
* [Revision #ef57d4d74d](https://github.com/MariaDB/server/commit/ef57d4d74d) <sup>_2025-06-30 20:32:28 +0000_</sup>
  * MDEV-36987 Add port information to server socket creation log message
* [Revision #bfbba94ead](https://github.com/MariaDB/server/commit/bfbba94ead) <sup>_2025-05-26 18:11:50 +0400_</sup>
  * MDEV-29474 - main.lock\_sync fails with timeout
* [Revision #060c0e3ff5](https://github.com/MariaDB/server/commit/060c0e3ff5) <sup>_2025-06-17 16:08:38 -0400_</sup>
  * MDEV-23699 Assertion failed in ha\_tina::delete\_row
* [Revision #3c38c37432](https://github.com/MariaDB/server/commit/3c38c37432) <sup>_2025-07-01 11:02:06 +0300_</sup>
  * MDEV-33957 UPDATE fails on replica replicating blob virtual column in NOBLOB mode when replica logging is off
* [Revision #c8cf8d3528](https://github.com/MariaDB/server/commit/c8cf8d3528) <sup>_2025-06-27 21:16:42 +0200_</sup>
  * MDEV-37104 Fix potential buffer overrun reported by the compiler.
* [Revision #2c7cea28da](https://github.com/MariaDB/server/commit/2c7cea28da) <sup>_2025-06-24 12:59:16 +0530_</sup>
  * MDEV-31721: Cursor protocol increases the counter of "Empty\_queries" for select
* [Revision #7ab205b009](https://github.com/MariaDB/server/commit/7ab205b009) <sup>_2025-06-25 14:14:50 +0300_</sup>
  * MDEV-34928 CREATE TABLE does not check valid engine for log tables
* [Revision #1dedd2a3b9](https://github.com/MariaDB/server/commit/1dedd2a3b9) <sup>_2025-06-25 14:14:50 +0300_</sup>
  * Refactoring: check\_log\_table() split
* [Revision #6a6709dbea](https://github.com/MariaDB/server/commit/6a6709dbea) <sup>_2025-06-25 14:14:50 +0300_</sup>
  * check\_if\_log\_table() cleanup
* [Revision #773d2d1960](https://github.com/MariaDB/server/commit/773d2d1960) <sup>_2025-06-25 08:10:44 +1000_</sup>
  * MDEV-36738: mariadb@.service incorrectly changing pam ownership in mariadb-install-db
* [Revision #0680e31737](https://github.com/MariaDB/server/commit/0680e31737) <sup>_2025-06-17 18:19:27 +0530_</sup>
  * MDEV-36959 Deadlock does not rollback transaction fully
* [Revision #a87bb96ecb](https://github.com/MariaDB/server/commit/a87bb96ecb) <sup>_2025-06-23 13:51:52 +0300_</sup>
  * MDEV-36234: Add innodb\_linux\_aio
* [Revision #107d1ef2c0](https://github.com/MariaDB/server/commit/107d1ef2c0) <sup>_2025-06-19 14:27:15 +1000_</sup>
  * MDEV-37033 UBSAN: row\_log\_table\_apply\_ops runtime error: applying non-zero offset 1048576 to null pointer
* [Revision #32128ab656](https://github.com/MariaDB/server/commit/32128ab656) <sup>_2025-06-23 08:38:56 +0300_</sup>
  * MDEV-37049 my\_assume\_aligned assertion in mariabackup
* [Revision #2d1e019f4f](https://github.com/MariaDB/server/commit/2d1e019f4f) <sup>_2025-06-19 18:06:03 +0530_</sup>
  * MDEV-36871 mariadb-backup incremental segfault querying mariadb\_backup\_history
* [Revision #0931617244](https://github.com/MariaDB/server/commit/0931617244) <sup>_2025-06-13 19:32:19 -0400_</sup>
  * Enable CMake CRC32 / CRYPTO tests for aarch64 with Clang
* [Revision #ec495bffe9](https://github.com/MariaDB/server/commit/ec495bffe9) <sup>_2025-06-12 20:10:22 -0400_</sup>
  * MDEV-36215: Avoid wrong result due to table elimination
* [Revision #4f7faa4bc8](https://github.com/MariaDB/server/commit/4f7faa4bc8) <sup>_2025-06-17 20:04:56 +0530_</sup>
  * MDEV-36650  Unexpected checkpoint in the test innodb.doublewrite
* [Revision #3944655357](https://github.com/MariaDB/server/commit/3944655357) <sup>_2025-06-17 17:36:08 +1000_</sup>
  * MDEV-37019 MSAN\_STAT\_WORKAROUND macro remove
* [Revision #4be442ec35](https://github.com/MariaDB/server/commit/4be442ec35) <sup>_2025-06-17 14:36:30 +0530_</sup>
  * MDEV-36962  innodb.log\_file\_overwrite fails with ASAN
* [Revision #39ef6c0dc8](https://github.com/MariaDB/server/commit/39ef6c0dc8) <sup>_2025-05-28 17:51:11 +1000_</sup>
  * MDEV-34425 mroonga files are not copied by mariabackup
* [Revision #72d2b7697d](https://github.com/MariaDB/server/commit/72d2b7697d) <sup>_2024-04-20 16:51:00 -0700_</sup>
  * MDEV-12305 FTBFS on hurd-i386 due to PATH\_MAX
* [Revision #22afd13e7a](https://github.com/MariaDB/server/commit/22afd13e7a) <sup>_2025-01-14 13:52:23 +1100_</sup>
  * Debian/Hurd doesn't support auth\_socket
* [Revision #b490240263](https://github.com/MariaDB/server/commit/b490240263) <sup>_2024-04-20 16:51:00 -0700_</sup>
  * Bug#1069094: mariadb: FTBFS on hurd-i386
* [Revision #629b8d782c](https://github.com/MariaDB/server/commit/629b8d782c) <sup>_2025-06-12 18:22:29 +0300_</sup>
  * MDEV-36662 CHECK constraint does not repeat in case of error
* [Revision #f66cd044d5](https://github.com/MariaDB/server/commit/f66cd044d5) <sup>_2025-06-13 19:34:36 -0400_</sup>
  * Enable use of elf\_aux\_info() to detect CPU features on aarch64 and powerpc64
* [Revision #729b27d390](https://github.com/MariaDB/server/commit/729b27d390) <sup>_2025-06-06 08:33:20 +1100_</sup>
  * MDEV-29300  Assertion '*ref && (*ref)-\>fixed()' failed in Item\_field::fix\_outer\_field on SELECT
* [Revision #7ba32f3ac8](https://github.com/MariaDB/server/commit/7ba32f3ac8) <sup>_2025-06-12 19:02:36 +0530_</sup>
  * MDEV-24588, 36851 followup: Fix derived, hybrid func test for --view-protocol
* [Revision #fadfd9ea28](https://github.com/MariaDB/server/commit/fadfd9ea28) <sup>_2025-05-09 18:31:25 -0400_</sup>
  * MDEV-37001 Enable building RocksDB on non-Linux aarch64 OSes
* [Revision #6d684b64d5](https://github.com/MariaDB/server/commit/6d684b64d5) <sup>_2025-05-22 20:02:04 -0400_</sup>
  * Rocksdb: Add missing getauxval() test for Linux
* [Revision #f1f9284181](https://github.com/MariaDB/server/commit/f1f9284181) <sup>_2025-06-11 16:38:10 +0300_</sup>
  * MDEV-34046 Parameterized PS converts error to warning, causes 	   replication problems
* [Revision #bff9b1e472](https://github.com/MariaDB/server/commit/bff9b1e472) <sup>_2025-05-30 17:44:55 +0530_</sup>
  * MDEV-36851: COALESCE() returns nullable column while IFNULL() does not
* [Revision #c427618462](https://github.com/MariaDB/server/commit/c427618462) <sup>_2025-06-10 15:21:04 +0700_</sup>
  * MDEV-36977: Histogram code lacks coverage for non-latin characters
* [Revision #dd2982dc33](https://github.com/MariaDB/server/commit/dd2982dc33) <sup>_2025-06-06 16:26:27 +0200_</sup>
  * MDEV-30831 Cannot compile AWS KMS Plugin
* [Revision #5729d89cd5](https://github.com/MariaDB/server/commit/5729d89cd5) <sup>_2025-06-04 09:46:06 +0200_</sup>
  * MDEV-36938 Fix MSI install failure when ADDLOCAL omits required runtime
* [Revision #5a6732983d](https://github.com/MariaDB/server/commit/5a6732983d) <sup>_2025-06-09 21:54:32 +0300_</sup>
  * MDEV-36461, followup: fix opt\_trace.test for --view-protocol
* [Revision #cce76e7225](https://github.com/MariaDB/server/commit/cce76e7225) <sup>_2025-06-09 16:40:27 +0300_</sup>
  * MDEV-36765: followup 4: Fixups to previous fixes
* [Revision #12c10712a7](https://github.com/MariaDB/server/commit/12c10712a7) <sup>_2025-06-03 13:01:06 +1000_</sup>
  * MDEV-36765: followup 3: json\_unquote/compare\_json\_str\_basic handle errors from json\_unescape
* [Revision #2b24ed87f0](https://github.com/MariaDB/server/commit/2b24ed87f0) <sup>_2025-06-03 12:56:06 +1000_</sup>
  * MDEV-36765: followup 2: st\_append\_json: handle json\_unescape error
* [Revision #0dd758e5f9](https://github.com/MariaDB/server/commit/0dd758e5f9) <sup>_2025-06-03 12:48:36 +1000_</sup>
  * MDEV-36765, followup 1: acl: handle json\_unescape errors without crashing
* [Revision #39bb34b9c5](https://github.com/MariaDB/server/commit/39bb34b9c5) <sup>_2025-06-01 11:57:21 +1000_</sup>
  * MDEV-36765: JSON Histogram cannot handle >1 byte characters
* [Revision #11d1ac7285](https://github.com/MariaDB/server/commit/11d1ac7285) <sup>_2025-06-04 15:16:54 +1000_</sup>
  * MDEV-35856 Remove error code introduced to 10.11 in MDEV-36032
* <sup>_Merge_</sup> [<sup>_Revision #28d6530571_</sup>](https://github.com/MariaDB/server/commit/28d6530571) <sup>_2025-06-04 14:09:23 +0200 - Merge branch '10.6' into 10.11_</sup>
* [Revision #e7aaf29e00](https://github.com/MariaDB/server/commit/e7aaf29e00) <sup>_2025-05-23 16:12:01 +0530_</sup>
  * MDEV-24588: Fix crash with unnamed column in derived table
* [Revision #5ff01ad7bb](https://github.com/MariaDB/server/commit/5ff01ad7bb) <sup>_2025-06-03 11:27:21 +0300_</sup>
  * MDEV-33370 Assertion !is\_set() || (m\_status == DA\_OK\_BULK && 	   is\_bulk\_op()) failed after ALTER TABLE of versioned table
* [Revision #6409e43177](https://github.com/MariaDB/server/commit/6409e43177) <sup>_2025-05-18 18:55:04 -0400_</sup>
  * Replace deprecated CMAKE\_COMPILER\_IS\_GNU(CC|CXX) with CMAKE_(C|CXX)_COMPILER_ID
* [Revision #5cd982c51b](https://github.com/MariaDB/server/commit/5cd982c51b) <sup>_2025-06-03 14:18:09 +1000_</sup>
  * MDEV-34863 RAM Usage Changed Significantly Between 10.11 Releases (postfix)
* [Revision #4d37b1c4b9](https://github.com/MariaDB/server/commit/4d37b1c4b9) <sup>_2025-05-28 14:44:43 +0300_</sup>
  * MDEV-36886 log\_t::get\_lsn\_approx() isn't lower bound
* [Revision #7b4b759f13](https://github.com/MariaDB/server/commit/7b4b759f13) <sup>_2025-05-28 13:33:06 +0300_</sup>
  * MDEV-36868: Inconsistency when shrinking innodb\_buffer\_pool\_size
* <sup>_Merge_</sup> [<sup>_Revision #bcd02c79f3_</sup>](https://github.com/MariaDB/server/commit/bcd02c79f3) <sup>_2025-05-26 16:59:32 +0200 - Merge branch '10.6' into 10.11_</sup>
* [Revision #db188083c3](https://github.com/MariaDB/server/commit/db188083c3) <sup>_2025-05-26 11:48:07 +0530_</sup>
  * MDEV-36771 Assertion bulk\_insert == TRX\_NO\_BULK failed in trx\_t::assert\_freed
* <sup>_Merge_</sup> [<sup>_Revision #3da36fa130_</sup>](https://github.com/MariaDB/server/commit/3da36fa130) <sup>_2025-05-26 08:10:47 +0300 - Merge 10.6 into 10.11_</sup>
* [Revision #d8962d138f](https://github.com/MariaDB/server/commit/d8962d138f) <sup>_2025-05-25 09:12:00 +0530_</sup>
  * MDEV-36017 Alter table aborts when temporary directory is full
* [Revision #8bc1643148](https://github.com/MariaDB/server/commit/8bc1643148) <sup>_2025-05-25 16:38:21 +0300_</sup>
  * MDEV-36860 exec\_REDO\_LOGREC\_REDO\_REPAIR\_TABLE: Assertion maria\_tmpdir failed
* [Revision #96b7671b05](https://github.com/MariaDB/server/commit/96b7671b05) <sup>_2025-05-23 14:51:38 +0300_</sup>
  * MDEV-34388 fixup: Stack usage in rename\_table\_in\_stat\_tables()
* [Revision #69af638a0c](https://github.com/MariaDB/server/commit/69af638a0c) <sup>_2025-05-22 10:23:36 -0400_</sup>
  * bump the VERSION
* <sup>_Merge_</sup> [<sup>_Revision #b8d3257243_</sup>](https://github.com/MariaDB/server/commit/b8d3257243) <sup>_2025-05-21 14:43:57 +0200 - Merge branch '10.11' into 10.11_</sup>
* <sup>_Merge_</sup> [<sup>_Revision #1c7209e828_</sup>](https://github.com/MariaDB/server/commit/1c7209e828) <sup>_2025-05-21 07:36:35 +0300 - Merge 10.6 into 10.11_</sup>
* [Revision #84dd2437c5](https://github.com/MariaDB/server/commit/84dd2437c5) <sup>_2025-05-08 11:18:16 +0300_</sup>
  * MDEV-36760 log\_t::append\_prepare\_wait(): Bogus assertion on write\_lsn
* [Revision #2263c8a1f7](https://github.com/MariaDB/server/commit/2263c8a1f7) <sup>_2025-04-20 14:06:17 -0400_</sup>
  * MDEV-36461: Optimizer trace: remove join\_execution node
* [Revision #0db5622c4f](https://github.com/MariaDB/server/commit/0db5622c4f) <sup>_2025-04-28 10:22:58 -0600_</sup>
  * MDEV-36663: Testcase Fixup
* [Revision #6f8ef26885](https://github.com/MariaDB/server/commit/6f8ef26885) <sup>_2025-04-29 16:28:01 +1000_</sup>
  * MDEV-36032 Check whether a table can be a sequence when ALTERed with SEQUENCE=1

{% include "../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}
<!-- This page is licensed: CC BY-SA / Gnu FDL -->

{% @marketo/form formid="4316" formId="4316" %}
