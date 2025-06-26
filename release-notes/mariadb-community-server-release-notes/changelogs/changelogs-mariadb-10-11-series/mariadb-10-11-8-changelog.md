# MariaDB 10.11.8 Changelog

The most recent release of [MariaDB 10.11](../../mariadb-10-11-series/what-is-mariadb-1011.md) is:[**MariaDB 10.11.11**](../../mariadb-10-11-series/mariadb-10-11-11-release-notes.md) Stable (GA) [Download Now](https://mariadb.com/downloads/)[_Alternate download from mariadb.org_](https://downloads.mariadb.org/mariadb/10.11.11/)

[Download 10.11.8](https://downloads.mariadb.org/mariadb/10.11.8/)[Release Notes](../../mariadb-10-11-series/mariadb-10-11-8-release-notes.md)[Changelog](mariadb-10-11-8-changelog.md)[Overview of 10.11](../../mariadb-10-11-series/what-is-mariadb-1011.md)

**Release date:** 16 May 2024

For the highlights of this release, see the[release notes](../../mariadb-10-11-series/mariadb-10-11-8-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/server/tree/10.11) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Includes all fixes from [MariaDB 10.6.18](../changelogs-mariadb-106-series/mariadb-10-6-18-changelog.md)
* [Revision #3a06964468](https://github.com/MariaDB/server/commit/3a06964468)\
  2024-05-09 20:37:40 +0200
  * [MDEV-33852](https://jira.mariadb.org/browse/MDEV-33852) start the server after deb installation
* Merge [Revision #a6b2f820e0](https://github.com/MariaDB/server/commit/a6b2f820e0) 2024-05-09 13:59:22 +0200 - Merge branch '10.6' into 10.11
* Merge [Revision #383ee364dc](https://github.com/MariaDB/server/commit/383ee364dc) 2024-05-07 08:45:31 +0200 - Merge 10.6 to 10.11
* [Revision #64314d3094](https://github.com/MariaDB/server/commit/64314d3094)\
  2024-05-06 12:46:31 +1000
  * [MDEV-30929](https://jira.mariadb.org/browse/MDEV-30929) spider.spider\_fixes\_part: wait and restart slave
* [Revision #3ee6f69d49](https://github.com/MariaDB/server/commit/3ee6f69d49)\
  2024-05-02 22:14:19 +0200
  * sporadic failures of binlog\_encryption.rpl\_parallel\_gco\_wait\_kill
* [Revision #9dfef3fb41](https://github.com/MariaDB/server/commit/9dfef3fb41)\
  2023-12-22 09:51:17 +0100
  * fix sporadic failures of main.lock\_sync
* [Revision #dba9d19249](https://github.com/MariaDB/server/commit/dba9d19249)\
  2024-04-30 21:59:38 +0200
  * atomic.alter\_table test is too slow for MSAN
* [Revision #b663c935a4](https://github.com/MariaDB/server/commit/b663c935a4)\
  2024-04-30 12:30:48 +0200
  * don't use normal diffs in \*.rdiff files
* Merge [Revision #0aae11ac28](https://github.com/MariaDB/server/commit/0aae11ac28) 2024-04-30 16:56:49 +0200 - Merge branch '10.6' into 10.11
* [Revision #ae03374f29](https://github.com/MariaDB/server/commit/ae03374f29)\
  2024-04-29 20:32:55 +0300
  * [MDEV-34030](https://jira.mariadb.org/browse/MDEV-34030) rpl.rpl\_using\_gtid\_default can fail in (BB) mtr
* [Revision #6a63204c36](https://github.com/MariaDB/server/commit/6a63204c36)\
  2024-04-29 20:10:21 +0300
  * [MDEV-34029](https://jira.mariadb.org/browse/MDEV-34029) rpl.rpl\_heartbeat can fail when (BB) mtr reorders tests
* [Revision #ec09c034d8](https://github.com/MariaDB/server/commit/ec09c034d8)\
  2024-04-17 12:14:14 +0300
  * [MDEV-33852](https://jira.mariadb.org/browse/MDEV-33852): Rework systemd installation on Debian
* [Revision #7ff649315e](https://github.com/MariaDB/server/commit/7ff649315e)\
  2024-04-26 14:12:47 +0200
  * sporadic failures of rpl.rpl\_parallel\_multi\_domain\_xa
* [Revision #22a69c7827](https://github.com/MariaDB/server/commit/22a69c7827)\
  2024-04-25 20:26:06 +0200
  * [MDEV-33492](https://jira.mariadb.org/browse/MDEV-33492) fix installation of rpm/deb packages
* Merge [Revision #c9b1ebee2f](https://github.com/MariaDB/server/commit/c9b1ebee2f) 2024-04-26 08:02:49 +0200 - Merge branch '10.6' into 10.11
* [Revision #9e92582024](https://github.com/MariaDB/server/commit/9e92582024)\
  2024-04-25 12:47:23 +0200
  * sporadic failures of rpl.rpl\_parallel\_sbm
* [Revision #9cf718859f](https://github.com/MariaDB/server/commit/9cf718859f)\
  2024-04-24 22:08:52 +0200
  * cleanup: use THD\_STAGE\_INFO, not thd\_proc\_info
* [Revision #8c7992165b](https://github.com/MariaDB/server/commit/8c7992165b)\
  2024-04-09 11:35:22 -0600
  * [MDEV-33672](https://jira.mariadb.org/browse/MDEV-33672): 10.11 Fix for Two Phase Alter Flags
* [Revision #720a0f6c78](https://github.com/MariaDB/server/commit/720a0f6c78)\
  2024-04-24 12:39:30 +0300
  * [MDEV-33447](https://jira.mariadb.org/browse/MDEV-33447) fixup for POWER 8
* [Revision #fb9af3f30e](https://github.com/MariaDB/server/commit/fb9af3f30e)\
  2024-04-22 04:04:33 -0400
  * fix build with WITH\_EXTRA\_CHARSETS=none in cmake
* [Revision #c3460e6904](https://github.com/MariaDB/server/commit/c3460e6904)\
  2024-04-23 16:23:14 +0530
  * [MDEV-33970](https://jira.mariadb.org/browse/MDEV-33970) Assertion \`!m.first->second.is\_bulk\_insert()' failed in trx\_undo\_report\_row\_operation()
* [Revision #455a15fd06](https://github.com/MariaDB/server/commit/455a15fd06)\
  2024-04-23 12:04:39 +0300
  * [MDEV-33972](https://jira.mariadb.org/browse/MDEV-33972): Memory corruption in innodb.insert\_into\_empty
* [Revision #f0d0ddc992](https://github.com/MariaDB/server/commit/f0d0ddc992)\
  2024-04-23 12:04:14 +0300
  * [MDEV-33447](https://jira.mariadb.org/browse/MDEV-33447) fixup for POWER
* [Revision #0271517495](https://github.com/MariaDB/server/commit/0271517495)\
  2024-02-20 17:40:43 +1100
  * [MDEV-33492](https://jira.mariadb.org/browse/MDEV-33492): mysql\_install\_db fails when baseurl is set
* [Revision #f243c73788](https://github.com/MariaDB/server/commit/f243c73788)\
  2024-04-22 21:02:11 +0200
  * sporadic failures of rpl.rpl\_rewrite\_db\_sys\_vars
* [Revision #a74846354e](https://github.com/MariaDB/server/commit/a74846354e)\
  2024-04-22 17:22:11 +0200
  * fix failing large\_tests.maria\_recover\_encrypted
* [Revision #926e38c6b9](https://github.com/MariaDB/server/commit/926e38c6b9)\
  2024-04-22 16:38:40 +0200
  * [MDEV-33447](https://jira.mariadb.org/browse/MDEV-33447) fixes for ppc64le
* [Revision #52529a528d](https://github.com/MariaDB/server/commit/52529a528d)\
  2024-04-22 15:27:14 +0200
  * [MDEV-32932](https://jira.mariadb.org/browse/MDEV-32932) fix comments to match the code
* Merge [Revision #018d537ec1](https://github.com/MariaDB/server/commit/018d537ec1) 2024-04-22 11:00:03 +0200 - Merge branch '10.6' into 10.11
* [Revision #75488a57f2](https://github.com/MariaDB/server/commit/75488a57f2)\
  2024-04-20 00:17:30 +0200
  * archive.archive and main.mysqlbinlog\_row\_compressed
* [Revision #aa4bcdbbb8](https://github.com/MariaDB/server/commit/aa4bcdbbb8)\
  2024-04-20 00:16:54 +0200
  * main.func\_sformat: fixes for fmt 10.2.1
* [Revision #f0f9dc8631](https://github.com/MariaDB/server/commit/f0f9dc8631)\
  2024-04-19 23:49:56 +0200
  * enable main.func\_sformat in --view
* [Revision #63ac87c121](https://github.com/MariaDB/server/commit/63ac87c121)\
  2024-04-19 22:32:37 +0200
  * make main.mysqlbinlog\_row\_compressed independent from the environment
* [Revision #06a884a570](https://github.com/MariaDB/server/commit/06a884a570)\
  2024-02-25 19:00:48 +0100
  * [MDEV-33429](https://jira.mariadb.org/browse/MDEV-33429) compilation of [MariaDB 10.11.7](../../mariadb-10-11-series/mariadb-10-11-7-release-notes.md) fails on arm32, sizeof(MYSQL) is wrong
* [Revision #8fd515e0d2](https://github.com/MariaDB/server/commit/8fd515e0d2)\
  2024-04-20 03:51:31 +0200
  * HASHICORP\_KEY\_MANAGEMENT: [MDEV-33420](https://jira.mariadb.org/browse/MDEV-33420) post-fix
* [Revision #3f9f5ca48e](https://github.com/MariaDB/server/commit/3f9f5ca48e)\
  2024-04-19 10:54:08 +0300
  * [MDEV-33447](https://jira.mariadb.org/browse/MDEV-33447): libpmem is not available in RHEL 8
* [Revision #8a3755cc29](https://github.com/MariaDB/server/commit/8a3755cc29)\
  2024-04-18 13:29:42 +0530
  * [MDEV-33934](https://jira.mariadb.org/browse/MDEV-33934) Assertion \`!check\_foreigns' failed in bulk\_insert\_apply\_for\_table(dict\_table\_t\*)
* [Revision #11aeef2aa2](https://github.com/MariaDB/server/commit/11aeef2aa2)\
  2024-04-12 08:55:27 +0200
  * [MDEV-33420](https://jira.mariadb.org/browse/MDEV-33420): HASHICORP\_KEY\_MANAGEMENT fails on Windows with libcurl installed
* [Revision #6815ab86d0](https://github.com/MariaDB/server/commit/6815ab86d0)\
  2024-04-18 01:42:39 +0200
  * HASHICORP\_KEY\_MANAGEMENT: code unification between MariaDB editions
* [Revision #9705d62313](https://github.com/MariaDB/server/commit/9705d62313)\
  2024-04-16 11:56:00 +0530
  * [MDEV-33809](https://jira.mariadb.org/browse/MDEV-33809) Bulk insert or DDL fails if a BLOB is too long
* [Revision #863f5996f2](https://github.com/MariaDB/server/commit/863f5996f2)\
  2024-04-10 13:52:04 +0530
  * [MDEV-33868](https://jira.mariadb.org/browse/MDEV-33868) Assertion \`trx->bulk\_insert' failed in innodb\_prepare\_commit\_versioned
* [Revision #cac0fc97cc](https://github.com/MariaDB/server/commit/cac0fc97cc)\
  2024-03-12 11:47:47 +0200
  * [MDEV-32974](https://jira.mariadb.org/browse/MDEV-32974) : Member fails to join due to old seqno in GTID
* [Revision #5faf2fdc3b](https://github.com/MariaDB/server/commit/5faf2fdc3b)\
  2024-04-10 10:37:18 +0300
  * [MDEV-33585](https://jira.mariadb.org/browse/MDEV-33585) fixup: GCC -Wsign-compare
* [Revision #d8a60dd4c9](https://github.com/MariaDB/server/commit/d8a60dd4c9)\
  2024-04-09 17:11:49 +0200
  * Fix a typo which lead to compiler error on 32 bit systems
* [Revision #42bda685db](https://github.com/MariaDB/server/commit/42bda685db)\
  2024-04-09 09:36:45 +0300
  * [MDEV-33585](https://jira.mariadb.org/browse/MDEV-33585) follow-up optimization
* [Revision #0892e6d028](https://github.com/MariaDB/server/commit/0892e6d028)\
  2024-04-09 09:32:47 +0300
  * [MDEV-33585](https://jira.mariadb.org/browse/MDEV-33585) The maximum innodb\_log\_buffer\_size is too large
* [Revision #fcd345de48](https://github.com/MariaDB/server/commit/fcd345de48)\
  2023-11-10 16:01:15 +0530
  * [MDEV-32726](https://jira.mariadb.org/browse/MDEV-32726): Fix failing test fir freebsd for json
* [Revision #188c5da72a](https://github.com/MariaDB/server/commit/188c5da72a)\
  2024-04-08 14:24:20 +0530
  * [MDEV-32453](https://jira.mariadb.org/browse/MDEV-32453) Bulk insert fails to apply when trigger does insert operation
* [Revision #5357110556](https://github.com/MariaDB/server/commit/5357110556)\
  2024-04-04 03:29:39 +0000
  * Fix error behaviour in mini-benchmark
* [Revision #2b0e0730c7](https://github.com/MariaDB/server/commit/2b0e0730c7)\
  2024-04-03 20:43:57 +0000
  * Add cpu-limit option for mini-benchmark
* [Revision #af4df93cf8](https://github.com/MariaDB/server/commit/af4df93cf8)\
  2024-04-03 16:39:36 +0300
  * Columnstore empty submodule fix 2
* [Revision #baec63e304](https://github.com/MariaDB/server/commit/baec63e304)\
  2024-04-02 09:41:49 +0200
  * [MDEV-33787](https://jira.mariadb.org/browse/MDEV-33787) : Fix Galera test failures on 10.11
* [Revision #40973d855c](https://github.com/MariaDB/server/commit/40973d855c)\
  2024-04-02 13:40:21 +0200
  * [MDEV-32926](https://jira.mariadb.org/browse/MDEV-32926) mysql\_install\_db\_win fails on buildbot
* [Revision #099ca49cc2](https://github.com/MariaDB/server/commit/099ca49cc2)\
  2024-04-02 00:14:17 +0300
  * Columnstore empty submodule fix
* [Revision #c477697422](https://github.com/MariaDB/server/commit/c477697422)\
  2024-04-02 00:11:35 +0300
  * [MDEV-29872](https://jira.mariadb.org/browse/MDEV-29872) MSAN/Valgrind uninitialised value errors in TABLE::vers\_switch\_partition
* [Revision #d966e55c0a](https://github.com/MariaDB/server/commit/d966e55c0a)\
  2024-04-02 00:11:34 +0300
  * [MDEV-31903](https://jira.mariadb.org/browse/MDEV-31903) Server crashes in \_ma\_reset\_history upon UNLOCK table with auto-create history partitions
* [Revision #a79fb66a98](https://github.com/MariaDB/server/commit/a79fb66a98)\
  2024-03-28 09:21:48 +0200
  * [MDEV-33515](https://jira.mariadb.org/browse/MDEV-33515) fixup for POWER
* Merge [Revision #788953463d](https://github.com/MariaDB/server/commit/788953463d) 2024-03-28 09:16:57 +0200 - Merge 10.6 into 10.11
* [Revision #6efa75a8cb](https://github.com/MariaDB/server/commit/6efa75a8cb)\
  2024-03-22 22:45:55 +0000
  * Enable mini-benchmark to run with perf
* [Revision #0c6cac0a6f](https://github.com/MariaDB/server/commit/0c6cac0a6f)\
  2024-03-27 09:33:37 +0200
  * [MDEV-33515](https://jira.mariadb.org/browse/MDEV-33515) fixup: Clarify mtr\_t::spin\_wait\_delay
* [Revision #bf0b82d24b](https://github.com/MariaDB/server/commit/bf0b82d24b)\
  2024-03-22 12:29:01 +0200
  * [MDEV-33515](https://jira.mariadb.org/browse/MDEV-33515) log\_sys.lsn\_lock causes excessive context switching
* [Revision #a2dd4c14a3](https://github.com/MariaDB/server/commit/a2dd4c14a3)\
  2024-03-20 16:03:15 +0100
  * post-fix 1c55b845e0fe
* [Revision #86a0b57689](https://github.com/MariaDB/server/commit/86a0b57689)\
  2024-03-08 16:26:07 +0100
  * [MDEV-32976](https://jira.mariadb.org/browse/MDEV-32976): Un-deprecate MASTER\_USE\_GTID=Current\_Pos
* [Revision #23c48474f7](https://github.com/MariaDB/server/commit/23c48474f7)\
  2024-03-08 15:23:42 +0100
  * [MDEV-33212](https://jira.mariadb.org/browse/MDEV-33212): mysqldump uses MASTER\_LOG\_POS with dump-slave
* [Revision #11c75fc396](https://github.com/MariaDB/server/commit/11c75fc396)\
  2024-03-04 16:03:42 +0200
  * Fixed sporadically failing test show\_explain\_json.test
* [Revision #611d442510](https://github.com/MariaDB/server/commit/611d442510)\
  2024-03-04 15:31:56 +0200
  * Fixed mtr random bug in lock\_sync.test
* [Revision #ee27bf749b](https://github.com/MariaDB/server/commit/ee27bf749b)\
  2024-03-01 12:44:32 +0200
  * Disable mariadb-backup.aria\_backup with msan because of timeouts
* [Revision #8d70ec59f1](https://github.com/MariaDB/server/commit/8d70ec59f1)\
  2024-03-01 10:42:44 +0200
  * Removed printing error output in bootstrap.test
* [Revision #86d542887d](https://github.com/MariaDB/server/commit/86d542887d)\
  2024-02-29 16:51:17 +0200
  * Fixed memory leaks in embedded server and mysqltest
* [Revision #3aa0bab798](https://github.com/MariaDB/server/commit/3aa0bab798)\
  2024-02-10 18:11:40 +0200
  * Fixed compiler warnings in connect
* [Revision #41b435fea9](https://github.com/MariaDB/server/commit/41b435fea9)\
  2024-02-08 16:47:00 +0200
  * [MDEV-33211](https://jira.mariadb.org/browse/MDEV-33211) : Galera SST on maria-backup causes donor node to be unresponsive
* [Revision #5d4adeabe2](https://github.com/MariaDB/server/commit/5d4adeabe2)\
  2024-02-08 16:41:04 +0200
  * [MDEV-33278](https://jira.mariadb.org/browse/MDEV-33278) Assertion failure in thd\_get\_thread\_id at lock\_wait\_wsrep
* [Revision #e5c694acd9](https://github.com/MariaDB/server/commit/e5c694acd9)\
  2023-12-03 16:12:03 +0200
  * Give warnings if one tries to use obsolete options with mariadb-backup
* [Revision #1c55b845e0](https://github.com/MariaDB/server/commit/1c55b845e0)\
  2023-12-03 14:09:43 +0200
  * [MDEV-32932](https://jira.mariadb.org/browse/MDEV-32932) Port backup features from ES
* [Revision #d7c943b363](https://github.com/MariaDB/server/commit/d7c943b363)\
  2023-12-02 17:58:26 +0200
  * Some changes to prepare for updated maria-backup
* [Revision #7246054cbb](https://github.com/MariaDB/server/commit/7246054cbb)\
  2024-02-14 12:21:59 +0400
  * [MDEV-33442](https://jira.mariadb.org/browse/MDEV-33442) REPAIR TABLE corrupts UUIDs
* [Revision #74c97a41fc](https://github.com/MariaDB/server/commit/74c97a41fc)\
  2024-02-21 13:11:32 +0200
  * [MDEV-33379](https://jira.mariadb.org/browse/MDEV-33379) fixup: undeclared identifier
* Merge [Revision #5b1406ff30](https://github.com/MariaDB/server/commit/5b1406ff30) 2024-02-21 13:08:23 +0200 - Merge 10.6 into 10.11
* [Revision #3dd7b0a80c](https://github.com/MariaDB/server/commit/3dd7b0a80c)\
  2024-02-20 11:22:52 +0200
  * Cleanup: Remove OS\_FILE\_ON\_ERROR\_NO\_EXIT
* [Revision #7f7329f092](https://github.com/MariaDB/server/commit/7f7329f092)\
  2024-02-20 11:22:45 +0200
  * [MDEV-33379](https://jira.mariadb.org/browse/MDEV-33379) innodb\_log\_file\_buffering=OFF causes corruption on bcachefs
* [Revision #4039d8605d](https://github.com/MariaDB/server/commit/4039d8605d)\
  2024-02-16 10:27:58 +0530
  * [MDEV-33363](https://jira.mariadb.org/browse/MDEV-33363) CI failure: innodb.import\_corrupted: Assertion failed: oldest\_lsn > log\_sys.last\_checkpoint\_lsn
* Merge [Revision #64cce8d5bf](https://github.com/MariaDB/server/commit/64cce8d5bf) 2024-02-14 16:12:53 +0200 - Merge 10.6 into 10.11
* [Revision #4fbd2e8573](https://github.com/MariaDB/server/commit/4fbd2e8573)\
  2023-09-15 10:47:50 -0600
  * [MDEV-31768](https://jira.mariadb.org/browse/MDEV-31768): Alias MASTER\_DEMOTE\_TO\_REPLICA for MASTER\_DEMOTE\_TO\_SLAVE
* [Revision #7bbc545f38](https://github.com/MariaDB/server/commit/7bbc545f38)\
  2023-12-18 10:10:26 +0200
  * Update my\_print\_defaults man page with mariadbd option
* [Revision #656f886772](https://github.com/MariaDB/server/commit/656f886772)\
  2024-01-04 11:30:34 +0100
  * RISC-V: use RDTIME instead of RDCYCLE
* [Revision #4ed8d98ba7](https://github.com/MariaDB/server/commit/4ed8d98ba7)\
  2024-02-07 20:10:07 +0300
  * [MDEV-33423](https://jira.mariadb.org/browse/MDEV-33423): show\_analyze sporadically fails at line 226: 'reap' succeeded...
* Merge [Revision #86c2c89743](https://github.com/MariaDB/server/commit/86c2c89743) 2024-02-08 15:04:46 +0200 - Merge 10.6 into 10.11
* [Revision #77b4399545](https://github.com/MariaDB/server/commit/77b4399545)\
  2024-02-08 14:20:42 +0200
  * [MDEV-33421](https://jira.mariadb.org/browse/MDEV-33421) innodb.corrupted\_during\_recovery fails due to error that the table is corrupted
* Merge [Revision #f30244d13c](https://github.com/MariaDB/server/commit/f30244d13c) 2024-02-07 08:18:05 +0100 - Merge branch '10.11' into mariadb-10.11.7
* [Revision #c4c167778e](https://github.com/MariaDB/server/commit/c4c167778e)\
  2024-02-07 09:05:28 +0400
  * [MDEV-33392](https://jira.mariadb.org/browse/MDEV-33392) Server crashes when using RANDOM\_BYTES function and GROUP BY clause on a column with a negative value
* [Revision #7f3839ab8c](https://github.com/MariaDB/server/commit/7f3839ab8c)\
  2024-02-06 08:25:30 -0500
  * bump the VERSION
* [Revision #c79f19a5ed](https://github.com/MariaDB/server/commit/c79f19a5ed)\
  2024-02-02 17:32:32 +0100
  * [MDEV-33374](https://jira.mariadb.org/browse/MDEV-33374) main.mysql\_connector\_net fails on new Windows 11
* [Revision #93189df44e](https://github.com/MariaDB/server/commit/93189df44e)\
  2024-02-02 10:48:10 +0200
  * [MDEV-33361](https://jira.mariadb.org/browse/MDEV-33361) Excessive delays in SET GLOBAL innodb\_log\_file\_size
* [Revision #ea9a6a1494](https://github.com/MariaDB/server/commit/ea9a6a1494)\
  2024-02-02 11:38:00 +1100
  * [MDEV-33095](https://jira.mariadb.org/browse/MDEV-33095) MariaDB-backup - no OS\_DATA\_FILE\_NO\_O\_DIRECT on some platforms
* [Revision #f5ca4077d8](https://github.com/MariaDB/server/commit/f5ca4077d8)\
  2023-03-13 15:04:54 -0400
  * [MDEV-30839](https://jira.mariadb.org/browse/MDEV-30839): Add new options to mini-benchmark and fixes

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
