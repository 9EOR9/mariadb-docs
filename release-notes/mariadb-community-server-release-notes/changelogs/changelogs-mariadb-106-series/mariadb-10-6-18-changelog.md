# MariaDB 10.6.18 Changelog

The most recent release of [MariaDB 10.6](../../mariadb-10-6-series/what-is-mariadb-106.md) is:[**MariaDB 10.6.21**](../../mariadb-10-6-series/mariadb-10-6-21-release-notes.md) Stable (GA) [Download Now](https://mariadb.com/downloads/)[_Alternate download from mariadb.org_](https://downloads.mariadb.org/mariadb/10.6.21/)

[Download 10.6.18](https://downloads.mariadb.org/mariadb/10.6.18/)[Release Notes](../../mariadb-10-6-series/mariadb-10-6-18-release-notes.md)[Changelog](mariadb-10-6-18-changelog.md)[Overview of 10.6](../../mariadb-10-6-series/what-is-mariadb-106.md)

**Release date:** 16 May 2024

For the highlights of this release, see the[release notes](../../mariadb-10-6-series/mariadb-10-6-18-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/server/tree/10.6) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Includes all fixes from [MariaDB 10.5.25](../changelogs-mariadb-105-series/mariadb-10-5-25-changelog.md)
* [Revision #887bb3f735](https://github.com/MariaDB/server/commit/887bb3f735)\
  2024-05-09 00:04:20 +0200
  * columnstore 6.4.8-2
* Merge [Revision #7b53672c63](https://github.com/MariaDB/server/commit/7b53672c63) 2024-05-08 20:06:00 +0200 - Merge branch '10.5' into 10.6
* [Revision #30d3cfad69](https://github.com/MariaDB/server/commit/30d3cfad69)\
  2024-05-08 17:20:04 +0200
  * new C/C 3.3
* [Revision #4b4db4a8e5](https://github.com/MariaDB/server/commit/4b4db4a8e5)\
  2024-05-04 11:02:41 +0200
  * [MDEV-34042](https://jira.mariadb.org/browse/MDEV-34042): Deadlock kill of XA PREPARE can break replication / rpl.rpl\_parallel\_multi\_domain\_xa sporadic failure
* [Revision #2a2019e199](https://github.com/MariaDB/server/commit/2a2019e199)\
  2024-05-05 19:01:22 +0200
  * [MDEV-33798](https://jira.mariadb.org/browse/MDEV-33798): Follow-up patch
* [Revision #596921dab8](https://github.com/MariaDB/server/commit/596921dab8)\
  2024-04-30 19:21:24 +0200
  * [MDEV-34042](https://jira.mariadb.org/browse/MDEV-34042): Deadlock kill of XA PREPARE can break replication / rpl.rpl\_parallel\_multi\_domain\_xa sporadic failure
* [Revision #e365877bae](https://github.com/MariaDB/server/commit/e365877bae)\
  2024-04-30 14:51:50 +0200
  * [MDEV-33798](https://jira.mariadb.org/browse/MDEV-33798): ROW base optimistic deadlock with concurrent writes on same table
* [Revision #90b95c6149](https://github.com/MariaDB/server/commit/90b95c6149)\
  2024-04-30 16:55:27 +0530
  * [MDEV-33543](https://jira.mariadb.org/browse/MDEV-33543) Server hang caused by InnoDB change buffer
* [Revision #156761db3b](https://github.com/MariaDB/server/commit/156761db3b)\
  2024-04-30 20:39:29 +0530
  * [MDEV-31161](https://jira.mariadb.org/browse/MDEV-31161) Assertion failures upon adding a too long key to table with COMPRESSED row
* [Revision #814dc46748](https://github.com/MariaDB/server/commit/814dc46748)\
  2024-04-27 13:35:48 +0300
  * Fixed slow bootstrap introduced in 10.6
* Merge [Revision #c1f3eff53f](https://github.com/MariaDB/server/commit/c1f3eff53f) 2024-04-29 10:08:58 +0200 - Merge branch '10.5' into 10.6
* [Revision #52f6df99ed](https://github.com/MariaDB/server/commit/52f6df99ed)\
  2024-04-24 19:53:13 +0530
  * [MDEV-33669](https://jira.mariadb.org/browse/MDEV-33669) mariadb-backup --backup hangs
* [Revision #ef7a2344af](https://github.com/MariaDB/server/commit/ef7a2344af)\
  2024-04-25 15:21:16 +0200
  * Fixup 0ccdf54b644352f42e1768bc660be7ab50c1e9d
* [Revision #0936c13809](https://github.com/MariaDB/server/commit/0936c13809)\
  2024-04-25 13:44:10 +0300
  * [MDEV-33993](https://jira.mariadb.org/browse/MDEV-33993) Possible server hang on DROP INDEX or RENAME INDEX
* [Revision #8c8b7da017](https://github.com/MariaDB/server/commit/8c8b7da017)\
  2024-04-25 10:50:34 +0530
  * [MDEV-33979](https://jira.mariadb.org/browse/MDEV-33979) Disallow bulk insert operation during partition update statement
* [Revision #0ccdf54b64](https://github.com/MariaDB/server/commit/0ccdf54b64)\
  2024-04-19 13:10:58 +0300
  * Check and remove high stack usage
* [Revision #07faba08b9](https://github.com/MariaDB/server/commit/07faba08b9)\
  2024-04-23 12:57:39 +0300
  * [MDEV-27924](https://jira.mariadb.org/browse/MDEV-27924) fixup: cmake -DWITH\_INNODB\_EXTRA\_DEBUG=ON
* [Revision #fbfb5a6f59](https://github.com/MariaDB/server/commit/fbfb5a6f59)\
  2024-04-18 15:41:30 +0300
  * [MDEV-33928](https://jira.mariadb.org/browse/MDEV-33928) : Assertion failure on wsrep\_thd\_is\_aborting
* [Revision #466bc8f7e0](https://github.com/MariaDB/server/commit/466bc8f7e0)\
  2024-04-22 17:22:11 +0200
  * fix failing large\_tests.maria\_recover\_encrypted
* [Revision #e83d92ee5e](https://github.com/MariaDB/server/commit/e83d92ee5e)\
  2024-04-21 18:28:15 +0200
  * sporadic failures of rpl.rpl\_semi\_sync\_fail\_over
* [Revision #6242783f24](https://github.com/MariaDB/server/commit/6242783f24)\
  2024-04-21 11:14:04 +0200
  * rpl.rpl\_semi\_sync\_fail\_over improve debugability
* [Revision #1437e734f7](https://github.com/MariaDB/server/commit/1437e734f7)\
  2024-04-21 10:47:20 +0200
  * adjust timeout value in main.ssl\_timeout test
* [Revision #a4b6409ff6](https://github.com/MariaDB/server/commit/a4b6409ff6)\
  2024-04-21 01:15:37 +0200
  * sporadic failures of binlog\_encryption.rpl\_parallel\_slave\_bgc\_kill
* [Revision #c7c3967181](https://github.com/MariaDB/server/commit/c7c3967181)\
  2024-04-20 18:34:03 +0200
  * use correct thd for DEBUG\_SYNC in group commit
* Merge [Revision #d8368ae289](https://github.com/MariaDB/server/commit/d8368ae289) 2024-04-20 14:47:26 +0200 - Merge '10.5' into 10.6
* Merge [Revision #15b607b552](https://github.com/MariaDB/server/commit/15b607b552) 2024-04-19 16:01:26 +0300 - Merge 10.5 into 10.6
* [Revision #ec7db2bdf8](https://github.com/MariaDB/server/commit/ec7db2bdf8)\
  2024-04-19 12:39:48 +0300
  * [MDEV-33325](https://jira.mariadb.org/browse/MDEV-33325) fixup
* [Revision #8e663f5e90](https://github.com/MariaDB/server/commit/8e663f5e90)\
  2024-04-19 11:04:51 +0300
  * [MDEV-32791](https://jira.mariadb.org/browse/MDEV-32791) MariaDB cannot be installed on Red Hat ubi9
* Merge [Revision #bb2e125d07](https://github.com/MariaDB/server/commit/bb2e125d07) 2024-04-18 07:14:56 +0300 - Merge 10.5 into 10.6
* [Revision #e459ce8336](https://github.com/MariaDB/server/commit/e459ce8336)\
  2024-04-17 16:47:41 +0300
  * [MDEV-33779](https://jira.mariadb.org/browse/MDEV-33779) InnoDB row operations could be faster
* Merge [Revision #829cb1a49c](https://github.com/MariaDB/server/commit/829cb1a49c) 2024-04-17 14:14:58 +0300 - Merge 10.5 into 10.6
* [Revision #46e9e92e22](https://github.com/MariaDB/server/commit/46e9e92e22)\
  2024-04-17 13:25:12 +0300
  * [MDEV-33855](https://jira.mariadb.org/browse/MDEV-33855) MSAN use-of-uninitialized-value in rtr\_pcur\_getnext\_from\_path()
* [Revision #a8a75ba2d0](https://github.com/MariaDB/server/commit/a8a75ba2d0)\
  2024-04-12 11:35:02 -0400
  * Factor TABLE\_LIST creation from add\_table\_to\_list
* [Revision #8dda602701](https://github.com/MariaDB/server/commit/8dda602701)\
  2024-04-11 21:00:39 +0200
  * spider should suppress errors in close\_connection
* [Revision #340d93a8cc](https://github.com/MariaDB/server/commit/340d93a8cc)\
  2024-04-11 15:06:39 +0200
  * cleanup: rpl.rpl\_semi\_sync\_shutdown\_await\_ack
* [Revision #e5c9904eba](https://github.com/MariaDB/server/commit/e5c9904eba)\
  2024-04-11 14:53:12 +0200
  * make innodb.monitor test idempotent
* Merge [Revision #41296a07c8](https://github.com/MariaDB/server/commit/41296a07c8) 2024-04-11 13:58:22 +0200 - Merge branch '10.5' into 10.6
* [Revision #263932d505](https://github.com/MariaDB/server/commit/263932d505)\
  2024-04-11 09:58:53 +0300
  * [MDEV-33325](https://jira.mariadb.org/browse/MDEV-33325) Crash in flst\_read\_addr on corrupted data
* [Revision #da47c0370d](https://github.com/MariaDB/server/commit/da47c0370d)\
  2024-04-09 21:05:14 +0300
  * Fixed calculating of last\_master\_timestamp for parallel replication.
* [Revision #3655cefc42](https://github.com/MariaDB/server/commit/3655cefc42)\
  2024-04-09 20:56:57 +0300
  * [MDEV-33813](https://jira.mariadb.org/browse/MDEV-33813) ERROR 1021 (HY000): Disk full (./org/test1.MAI); waiting for someone to free some space
* [Revision #33af5575a9](https://github.com/MariaDB/server/commit/33af5575a9)\
  2023-09-04 12:22:51 +0300
  * [MDEV-25731](https://jira.mariadb.org/browse/MDEV-25731) : Assertion \`mode\_ == m\_local' failed in void wsrep::client\_state::streaming\_params(wsrep::streaming\_context::fragment\_unit, size\_t)
* [Revision #4aa92911c7](https://github.com/MariaDB/server/commit/4aa92911c7)\
  2024-04-09 12:50:24 +0300
  * [MDEV-33802](https://jira.mariadb.org/browse/MDEV-33802) Weird read view after ROLLBACK of another transaction
* [Revision #a4cda66e2d](https://github.com/MariaDB/server/commit/a4cda66e2d)\
  2024-04-09 12:48:01 +0300
  * [MDEV-33588](https://jira.mariadb.org/browse/MDEV-33588) buf::Block\_hint is a performance hog
* [Revision #d90a2b44ad](https://github.com/MariaDB/server/commit/d90a2b44ad)\
  2024-02-27 19:08:20 +0100
  * [MDEV-33668](https://jira.mariadb.org/browse/MDEV-33668): More precise dependency tracking of XA XID in parallel replication
* [Revision #f9ecaa87ce](https://github.com/MariaDB/server/commit/f9ecaa87ce)\
  2024-02-27 12:19:18 +0100
  * [MDEV-33668](https://jira.mariadb.org/browse/MDEV-33668): Refactor parallel replication round-robin scheduling to use explicit FIFO
* [Revision #89c907bd4f](https://github.com/MariaDB/server/commit/89c907bd4f)\
  2024-03-13 14:42:28 -0600
  * [MDEV-33672](https://jira.mariadb.org/browse/MDEV-33672): Gtid\_log\_event Construction from File Should Ensure Event Length When Using Extra Flags
* [Revision #11986ec654](https://github.com/MariaDB/server/commit/11986ec654)\
  2024-04-08 14:56:31 +0400
  * [MDEV-31251](https://jira.mariadb.org/browse/MDEV-31251) [MDEV-30968](https://jira.mariadb.org/browse/MDEV-30968) breaks running mariadb-backup on older mariadb (opendir(NULL))
* [Revision #73291de74e](https://github.com/MariaDB/server/commit/73291de74e)\
  2024-04-08 11:48:46 +0300
  * [MDEV-33819](https://jira.mariadb.org/browse/MDEV-33819) The purge of committed history is mis-parsing some log
* [Revision #a202371f0b](https://github.com/MariaDB/server/commit/a202371f0b)\
  2024-04-04 16:38:26 +0300
  * [MDEV-33757](https://jira.mariadb.org/browse/MDEV-33757) Get rid of TrxUndoRsegs code
* [Revision #9a4991a089](https://github.com/MariaDB/server/commit/9a4991a089)\
  2024-04-01 09:46:50 -0600
  * [MDEV-33799](https://jira.mariadb.org/browse/MDEV-33799): mysql\_manager\_submit Segfault at Startup Still Possible During Recovery
* [Revision #722df777ca](https://github.com/MariaDB/server/commit/722df777ca)\
  2024-03-23 21:37:55 +0300
  * [MDEV-33757](https://jira.mariadb.org/browse/MDEV-33757) Get rid of TrxUndoRsegs code
* Merge [Revision #ccb7a1e9a1](https://github.com/MariaDB/server/commit/ccb7a1e9a1) 2024-03-27 15:00:56 +0200 - Merge 10.5 into 10.6
* [Revision #c5ac9836b3](https://github.com/MariaDB/server/commit/c5ac9836b3)\
  2024-01-29 15:04:57 +0200
  * [MDEV-33039](https://jira.mariadb.org/browse/MDEV-33039) Galera test failure on mysql-wsrep-features#165
* [Revision #7bf3c3124a](https://github.com/MariaDB/server/commit/7bf3c3124a)\
  2024-02-06 11:55:04 +0300
  * [MDEV-33136](https://jira.mariadb.org/browse/MDEV-33136): Properly BF-abort user transactions with explicit locks
* [Revision #318000cffc](https://github.com/MariaDB/server/commit/318000cffc)\
  2024-03-26 00:05:07 +0100
  * [MDEV-33506](https://jira.mariadb.org/browse/MDEV-33506) Show original IP in the "aborted" message.
* [Revision #b762541dd6](https://github.com/MariaDB/server/commit/b762541dd6)\
  2024-01-23 08:38:19 +0200
  * [MDEV-33278](https://jira.mariadb.org/browse/MDEV-33278) : Assertion failure in thd\_get\_thread\_id at lock\_wait\_wsrep
* [Revision #c1da568502](https://github.com/MariaDB/server/commit/c1da568502)\
  2024-03-21 14:48:06 +1100
  * [MDEV-33726](https://jira.mariadb.org/browse/MDEV-33726) Moving from [MariaDB 10.5](../../mariadb-10-5-series/what-is-mariadb-105.md) to 10.6 mysql\_upgrade
* [Revision #17e59ed3aa](https://github.com/MariaDB/server/commit/17e59ed3aa)\
  2024-03-22 14:33:48 +0200
  * [MDEV-33454](https://jira.mariadb.org/browse/MDEV-33454) release row locks for non-modified rows at XA PREPARE
* [Revision #fa8a46eb68](https://github.com/MariaDB/server/commit/fa8a46eb68)\
  2024-03-22 14:17:39 +0200
  * [MDEV-33613](https://jira.mariadb.org/browse/MDEV-33613) InnoDB may still hang when temporarily running out of buffer pool
* [Revision #75c7c6dc39](https://github.com/MariaDB/server/commit/75c7c6dc39)\
  2024-02-27 12:11:06 -0700
  * [MDEV-33551](https://jira.mariadb.org/browse/MDEV-33551): Semi-sync Wait Point AFTER\_COMMIT Slow on Workloads with Heavy Concurrency
* [Revision #b8a6719889](https://github.com/MariaDB/server/commit/b8a6719889)\
  2024-03-20 09:48:03 +0200
  * [MDEV-26642](https://jira.mariadb.org/browse/MDEV-26642)/[MDEV-26643](https://jira.mariadb.org/browse/MDEV-26643)/[MDEV-32898](https://jira.mariadb.org/browse/MDEV-32898) Implement innodb\_snapshot\_isolation
* [Revision #ca07f62992](https://github.com/MariaDB/server/commit/ca07f62992)\
  2024-03-18 14:55:05 -0600
  * [MDEV-33716](https://jira.mariadb.org/browse/MDEV-33716): rpl.rpl\_semi\_sync\_slave\_enabled\_consistent Fails with Error Condition Reached
* [Revision #c3a6248bba](https://github.com/MariaDB/server/commit/c3a6248bba)\
  2024-03-19 17:14:11 +0530
  * [MDEV-33542](https://jira.mariadb.org/browse/MDEV-33542) Inplace algorithm occupies more disk space compared to copy algorithm
* [Revision #5b4e69c059](https://github.com/MariaDB/server/commit/5b4e69c059)\
  2024-03-19 11:57:38 +0100
  * [MDEV-23224](https://jira.mariadb.org/browse/MDEV-23224) Windows threadpool - use better threadpool\_max\_threads default.
* [Revision #01d994b39a](https://github.com/MariaDB/server/commit/01d994b39a)\
  2024-03-18 23:43:56 +0100
  * Post-fix 567c0973591eb66797bb0f982f312b516f8fe82c
* Merge [Revision #50715bd2ed](https://github.com/MariaDB/server/commit/50715bd2ed) 2024-03-18 17:07:32 +0200 - Merge 10.5 into 10.6
* [Revision #51abae5e46](https://github.com/MariaDB/server/commit/51abae5e46)\
  2024-02-29 19:42:00 +0100
  * [MDEV-25923](https://jira.mariadb.org/browse/MDEV-25923): Aria parallel repair MY\_THREAD\_SPECIFIC mismatch in realloc
* [Revision #77b9b28a59](https://github.com/MariaDB/server/commit/77b9b28a59)\
  2024-03-08 22:43:26 +0100
  * [MDEV-24622](https://jira.mariadb.org/browse/MDEV-24622): Replication does not support bulk insert into empty table
* [Revision #1fb00f37ae](https://github.com/MariaDB/server/commit/1fb00f37ae)\
  2024-03-08 11:26:45 +0100
  * [MDEV-33303](https://jira.mariadb.org/browse/MDEV-33303): slave\_parallel\_mode=optimistic should not report the mode's specific temporary errors
* Merge [Revision #55cea0c2a6](https://github.com/MariaDB/server/commit/55cea0c2a6) 2024-03-14 19:52:08 +0100 - Merge branch '10.5' into 10.6
* [Revision #bb451d2cad](https://github.com/MariaDB/server/commit/bb451d2cad)\
  2024-03-14 13:38:13 +0100
  * fix galera tests after 9a132d423ab
* [Revision #dbd36bb140](https://github.com/MariaDB/server/commit/dbd36bb140)\
  2024-03-14 10:55:28 +0100
  * after merge fix
* [Revision #61f6dc5e30](https://github.com/MariaDB/server/commit/61f6dc5e30)\
  2023-12-18 17:37:30 +0100
  * perfschema: LOCK\_all\_status\_vars not LOCK\_status
* Merge [Revision #f71d7f2f0f](https://github.com/MariaDB/server/commit/f71d7f2f0f) 2024-03-13 19:49:05 +0100 - Merge branch '10.5' into 10.6
* [Revision #0e8cda6130](https://github.com/MariaDB/server/commit/0e8cda6130)\
  2024-01-25 22:39:29 +0100
  * [MDEV-33313](https://jira.mariadb.org/browse/MDEV-33313) Incorrect error message for "ALTER TABLE ... DROP CONSTRAINT ..., DROP col, DROP col"
* [Revision #6711540518](https://github.com/MariaDB/server/commit/6711540518)\
  2024-01-25 16:02:45 +0100
  * remove `exit 1` from search\_pattern\_in\_file.inc
* [Revision #bc46f1a7d9](https://github.com/MariaDB/server/commit/bc46f1a7d9)\
  2024-01-25 15:00:39 +0100
  * cleanup: remove SEARCH\_TYPE from search\_pattern\_in\_file.inc
* [Revision #424210abd2](https://github.com/MariaDB/server/commit/424210abd2)\
  2024-01-11 00:33:25 +0100
  * cleanup: reduce code duplication
* [Revision #cfa8268ef9](https://github.com/MariaDB/server/commit/cfa8268ef9)\
  2024-03-12 18:23:51 +0200
  * [MDEV-33622](https://jira.mariadb.org/browse/MDEV-33622) Server crashes when the UPDATE statement (which has duplicate key) is run after setting a low thread\_stack
* [Revision #4ac8c4c820](https://github.com/MariaDB/server/commit/4ac8c4c820)\
  2024-03-12 09:20:36 +0200
  * [MDEV-24167](https://jira.mariadb.org/browse/MDEV-24167) fixup: Stricter assertion
* Merge [Revision #c3a00dfa53](https://github.com/MariaDB/server/commit/c3a00dfa53) 2024-03-12 09:19:57 +0200 - Merge 10.5 into 10.6
* [Revision #b3d507ff13](https://github.com/MariaDB/server/commit/b3d507ff13)\
  2024-03-09 12:09:43 +0200
  * Suppressed new warning for rpl\_get\_lock on amd-freebsd and aarch64-macos
* [Revision #f838b2d799](https://github.com/MariaDB/server/commit/f838b2d799)\
  2024-03-08 15:18:21 +0200
  * [MDEV-33623](https://jira.mariadb.org/browse/MDEV-33623) Partitioning is broken on big endian architectures
* [Revision #9a132d423a](https://github.com/MariaDB/server/commit/9a132d423a)\
  2024-03-07 11:25:30 +0200
  * [MDEV-33620](https://jira.mariadb.org/browse/MDEV-33620) Improve times and states in show processlist for replication
* [Revision #0df4651c13](https://github.com/MariaDB/server/commit/0df4651c13)\
  2024-03-06 15:06:48 +0200
  * Fixed some mtr results found in Jenins after [MDEV-333582](https://jira.mariadb.org/browse/MDEV-333582) push
* [Revision #567c097359](https://github.com/MariaDB/server/commit/567c097359)\
  2024-03-01 18:16:33 +0200
  * [MDEV-33582](https://jira.mariadb.org/browse/MDEV-33582) Add more warnings to be able to better diagnose network issues
* [Revision #48f42ab2e5](https://github.com/MariaDB/server/commit/48f42ab2e5)\
  2024-02-28 12:37:20 +0300
  * Fix comment.
* [Revision #33dcf8155b](https://github.com/MariaDB/server/commit/33dcf8155b)\
  2024-02-29 16:51:17 +0200
  * Fixed memory leaks in embedded server and mysqltest
* [Revision #bd604add76](https://github.com/MariaDB/server/commit/bd604add76)\
  2024-02-26 12:11:34 -0700
  * [MDEV-33546](https://jira.mariadb.org/browse/MDEV-33546): Rpl\_semi\_sync\_slave\_status is ON When Replication Is Not Configured
* [Revision #31463f1164](https://github.com/MariaDB/server/commit/31463f1164)\
  2024-02-28 16:01:48 +0300
  * [MDEV-33502](https://jira.mariadb.org/browse/MDEV-33502): part#4: Dont make redundant extra(HA\_EXTRA\_\[NO]\_KEYREAD) calls
* [Revision #0772ac1f16](https://github.com/MariaDB/server/commit/0772ac1f16)\
  2024-02-28 12:48:38 +0200
  * [MDEV-33508](https://jira.mariadb.org/browse/MDEV-33508) Performance regression due to frequent scan of full buf\_pool.flush\_list
* [Revision #f1c615ec18](https://github.com/MariaDB/server/commit/f1c615ec18)\
  2024-02-26 14:52:38 +0200
  * Fixed failure in test connect.drop-open-error for embedded server
* [Revision #89aae15da2](https://github.com/MariaDB/server/commit/89aae15da2)\
  2024-02-26 14:51:27 +0200
  * Fixed crash in connect.misc with embedded server
* [Revision #0c079f4f76](https://github.com/MariaDB/server/commit/0c079f4f76)\
  2024-02-20 15:25:51 +0200
  * Updated test cases result for s3.parition
* [Revision #b5d65fc105](https://github.com/MariaDB/server/commit/b5d65fc105)\
  2024-02-18 17:30:01 +0200
  * Optimize performance of my\_bitmap
* [Revision #d4e1731fbc](https://github.com/MariaDB/server/commit/d4e1731fbc)\
  2024-02-18 16:05:42 +0200
  * Optimize handler\_stats\_disable() when handler\_stats are already disabled
* [Revision #a8f6b86c90](https://github.com/MariaDB/server/commit/a8f6b86c90)\
  2024-02-18 16:02:40 +0200
  * Have ha\_partition ignore HA\_EXTRA..CHILDREN extra() calls if no myisamrg
* [Revision #71834ccb6c](https://github.com/MariaDB/server/commit/71834ccb6c)\
  2024-02-27 11:14:28 +0200
  * [MDEV-24671](https://jira.mariadb.org/browse/MDEV-24671) fixup: Remove srv\_max\_n\_threads
* [Revision #2c5f3bbe78](https://github.com/MariaDB/server/commit/2c5f3bbe78)\
  2024-02-26 18:59:21 +0530
  * [MDEV-14193](https://jira.mariadb.org/browse/MDEV-14193) innodb.log\_file\_name failed in buildbot with exception
* [Revision #5b8493ba34](https://github.com/MariaDB/server/commit/5b8493ba34)\
  2024-02-23 21:29:21 +0700
  * [MDEV-15656](https://jira.mariadb.org/browse/MDEV-15656) follow-up: fix rocksdb.group\_min\_max test
* [Revision #e309e02447](https://github.com/MariaDB/server/commit/e309e02447)\
  2024-02-23 13:42:46 +0530
  * [MDEV-30655](https://jira.mariadb.org/browse/MDEV-30655) IMPORT TABLESPACE fails with column count or index count mismatch
* [Revision #e66928ab28](https://github.com/MariaDB/server/commit/e66928ab28)\
  2024-02-22 16:50:58 +0530
  * [MDEV-33462](https://jira.mariadb.org/browse/MDEV-33462) Server aborts while altering an InnoDB statistics table
* [Revision #042c3fc432](https://github.com/MariaDB/server/commit/042c3fc432)\
  2024-02-21 13:03:25 +0200
  * [MDEV-24167](https://jira.mariadb.org/browse/MDEV-24167) fixup: srw\_lock\_debug for SUX\_LOCK\_GENERIC
* [Revision #903ae30069](https://github.com/MariaDB/server/commit/903ae30069)\
  2024-02-20 19:08:13 +0530
  * [MDEV-30655](https://jira.mariadb.org/browse/MDEV-30655) IMPORT TABLESPACE fails with column count or index count mismatch
* [Revision #27b064d882](https://github.com/MariaDB/server/commit/27b064d882)\
  2024-02-19 14:30:46 +0100
  * [MDEV-33488](https://jira.mariadb.org/browse/MDEV-33488) Windows 11 misdetects mariadbd as LowQoS process, throttles CPU.
* [Revision #53c6c823dc](https://github.com/MariaDB/server/commit/53c6c823dc)\
  2024-02-15 12:34:04 +0200
  * [MDEV-33464](https://jira.mariadb.org/browse/MDEV-33464) Crash when innodb\_max\_undo\_log\_size is set to innodb\_page\_size\*4294967296
* Merge [Revision #691f923906](https://github.com/MariaDB/server/commit/691f923906) 2024-02-13 20:42:59 +0200 - Merge 10.5 into 10.6
* [Revision #c0f6c4bd40](https://github.com/MariaDB/server/commit/c0f6c4bd40)\
  2022-04-27 09:26:30 +1000
  * [MDEV-28419](https://jira.mariadb.org/browse/MDEV-28419) subsequent runs of debian/autobake-deb.sh are not idempotent
* [Revision #3907345e22](https://github.com/MariaDB/server/commit/3907345e22)\
  2024-02-09 20:27:12 +0200
  * [MDEV-33306](https://jira.mariadb.org/browse/MDEV-33306) Optimizer choosing incorrect index in 10.6, 10.5 but not in 10.4
* [Revision #4106974b9d](https://github.com/MariaDB/server/commit/4106974b9d)\
  2024-02-10 17:52:06 +0200
  * Fixed some compiler warnings
* Merge [Revision #466069b184](https://github.com/MariaDB/server/commit/466069b184) 2024-02-08 10:38:53 +0200 - Merge 10.5 into 10.6
* [Revision #b2654ba826](https://github.com/MariaDB/server/commit/b2654ba826)\
  2024-02-01 15:48:46 +0200
  * [MDEV-32899](https://jira.mariadb.org/browse/MDEV-32899) InnoDB is holding shared dict\_sys.latch while waiting for FOREIGN KEY child table lock on DDL
* [Revision #5f2dcd112b](https://github.com/MariaDB/server/commit/5f2dcd112b)\
  2024-02-01 15:47:24 +0200
  * [MDEV-24167](https://jira.mariadb.org/browse/MDEV-24167) fixup: srw\_lock\_debug instrumentation
* [Revision #8d54d173d7](https://github.com/MariaDB/server/commit/8d54d173d7)\
  2024-02-07 13:56:31 +0200
  * Cleanup: Remove ut\_format\_name()
* Merge [Revision #91a2192bf2](https://github.com/MariaDB/server/commit/91a2192bf2) 2024-02-07 13:51:03 +0200 - Merge 10.5 into 10.6
* Merge [Revision #d337700cc0](https://github.com/MariaDB/server/commit/d337700cc0) 2024-02-06 22:45:22 +0100 - Merge branch '10.6' into mariadb-10.6.17
* [Revision #5c5242a674](https://github.com/MariaDB/server/commit/5c5242a674)\
  2024-01-26 14:37:26 +0100
  * mtr - synchronize output between different threads on Windows.
* [Revision #a94d2a6888](https://github.com/MariaDB/server/commit/a94d2a6888)\
  2024-01-26 14:43:05 +0100
  * CMake remember decision to bundle WITH\_PCRE, avoid repeated system checks
* [Revision #c482e71eba](https://github.com/MariaDB/server/commit/c482e71eba)\
  2024-02-06 08:23:21 -0500
  * bump the VERSION
* [Revision #bde552aea3](https://github.com/MariaDB/server/commit/bde552aea3)\
  2024-02-05 06:14:06 -0700
  * [MDEV-32551](https://jira.mariadb.org/browse/MDEV-32551): Fix engines/funcs.rpl\_session\_var
* [Revision #1031c8848d](https://github.com/MariaDB/server/commit/1031c8848d)\
  2024-01-16 12:02:56 +1100
  * [MDEV-33242](https://jira.mariadb.org/browse/MDEV-33242) Make Spider init queries compatible with non-default old\_mode
* [Revision #12d05c8266](https://github.com/MariaDB/server/commit/12d05c8266)\
  2024-01-29 09:59:36 +1100
  * [MDEV-28640](https://jira.mariadb.org/browse/MDEV-28640): Debian typo in init script

{% include "https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/~/reusable/vX1KAy0t1XuYJaGsK28T/" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
