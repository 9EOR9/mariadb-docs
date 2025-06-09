# MariaDB 10.6.16 Changelog

The most recent release of [MariaDB 10.6](../../mariadb-community-server-release-notes/mariadb-10-6-series/what-is-mariadb-106.md) is:[**MariaDB 10.6.21**](../../mariadb-community-server-release-notes/mariadb-10-6-series/mariadb-10-6-21-release-notes.md) Stable (GA) [Download Now](https://mariadb.com/downloads/)[_Alternate download from mariadb.org_](https://downloads.mariadb.org/mariadb/10.6.21/)

[Download 10.6.16](https://downloads.mariadb.org/mariadb/10.6.16/)[Release Notes](../../mariadb-community-server-release-notes/mariadb-10-6-series/mariadb-10-6-16-release-notes.md)[Changelog](mariadb-10-6-16-changelog.md)[Overview of 10.6](../../mariadb-community-server-release-notes/mariadb-10-6-series/what-is-mariadb-106.md)

**Release date:** 13 Nov 2023

For the highlights of this release, see the[release notes](../../mariadb-community-server-release-notes/mariadb-10-6-series/mariadb-10-6-16-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/server/tree/10.6) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Includes all fixes from [MariaDB 10.5.23](../changelogs-mariadb-105-series/mariadb-10-5-23-changelog.md)
* Merge [Revision #b83c379420](https://github.com/MariaDB/server/commit/b83c379420) 2023-11-08 15:57:05 +0100 - Merge branch '10.5' into 10.6
* [Revision #2a4c573339](https://github.com/MariaDB/server/commit/2a4c573339)\
  2023-11-08 13:55:03 +0100
  * [MDEV-32728](https://jira.mariadb.org/browse/MDEV-32728): Wrong mutex usage 'LOCK\_thd\_data' and 'wait\_mutex'
* [Revision #fefd6d5559](https://github.com/MariaDB/server/commit/fefd6d5559)\
  2023-11-08 12:06:34 +0100
  * [MDEV-32656](https://jira.mariadb.org/browse/MDEV-32656): ASAN errors in base\_list\_iterator::next / setup\_table\_map upon 2nd execution of PS
* [Revision #1697747461](https://github.com/MariaDB/server/commit/1697747461)\
  2023-11-07 12:20:02 +0300
  * [MDEV-32682](https://jira.mariadb.org/browse/MDEV-32682): Assertion \`range->rows >= s->found\_records' failed in best\_access\_path
* [Revision #b52b7b4129](https://github.com/MariaDB/server/commit/b52b7b4129)\
  2023-11-06 19:16:16 +0530
  * [MDEV-31851](https://jira.mariadb.org/browse/MDEV-31851) Doublewrite recovery fixup
* [Revision #1fc2843eee](https://github.com/MariaDB/server/commit/1fc2843eee)\
  2023-11-04 16:04:21 +0200
  * [MDEV-31826](https://jira.mariadb.org/browse/MDEV-31826): File handle leak on failed IMPORT TABLESPACE
* [Revision #90e11488ac](https://github.com/MariaDB/server/commit/90e11488ac)\
  2023-11-01 11:29:12 +0100
  * update C/C - compilation failure with gcc7 on s390x-sles-12
* [Revision #0cc809f91b](https://github.com/MariaDB/server/commit/0cc809f91b)\
  2023-10-31 12:48:20 +0200
  * [MDEV-31826](https://jira.mariadb.org/browse/MDEV-31826): Memory leak on failed IMPORT TABLESPACE
* [Revision #6f091434f3](https://github.com/MariaDB/server/commit/6f091434f3)\
  2023-10-30 14:44:26 +0200
  * [MDEV-32531](https://jira.mariadb.org/browse/MDEV-32531) MSAN / Valgrind errors in Item\_func\_like::get\_mm\_leaf with temporal field
* [Revision #ab6139ddc0](https://github.com/MariaDB/server/commit/ab6139ddc0)\
  2023-10-28 06:05:25 +1200
  * [MDEV-32612](https://jira.mariadb.org/browse/MDEV-32612) Assertion \`tab->select->quick' failed in test\_if\_skip\_sort\_order
* [Revision #5b53342a6a](https://github.com/MariaDB/server/commit/5b53342a6a)\
  2023-10-26 15:10:53 +0300
  * [MDEV-32588](https://jira.mariadb.org/browse/MDEV-32588) InnoDB may hang when running out of buffer pool
* [Revision #39e3ca8bd2](https://github.com/MariaDB/server/commit/39e3ca8bd2)\
  2023-10-26 15:07:59 +0300
  * [MDEV-31826](https://jira.mariadb.org/browse/MDEV-31826) InnoDB may fail to recover after being killed in fil\_delete\_tablespace()
* [Revision #ec2574fd8f](https://github.com/MariaDB/server/commit/ec2574fd8f)\
  2023-09-15 08:44:49 +1100
  * [MDEV-31983](https://jira.mariadb.org/browse/MDEV-31983) jointable materialization subquery optimization ignoring
* [Revision #2ba9702163](https://github.com/MariaDB/server/commit/2ba9702163)\
  2023-10-25 10:21:49 +0300
  * [MDEV-32050](https://jira.mariadb.org/browse/MDEV-32050): Boost innodb\_purge\_batch\_size on slow shutdown
* [Revision #aa719b5010](https://github.com/MariaDB/server/commit/aa719b5010)\
  2023-10-25 10:19:17 +0300
  * [MDEV-32050](https://jira.mariadb.org/browse/MDEV-32050): Do not copy undo records in purge
* [Revision #88733282fb](https://github.com/MariaDB/server/commit/88733282fb)\
  2023-10-25 10:08:20 +0300
  * [MDEV-32050](https://jira.mariadb.org/browse/MDEV-32050): Look up tables in the purge coordinator
* [Revision #39bb5ebb85](https://github.com/MariaDB/server/commit/39bb5ebb85)\
  2023-10-12 16:50:37 +0400
  * [MDEV-32050](https://jira.mariadb.org/browse/MDEV-32050): Allow table to be guarded by an MDL of another thread
* [Revision #d70a98ae06](https://github.com/MariaDB/server/commit/d70a98ae06)\
  2023-10-25 09:42:38 +0300
  * [MDEV-32050](https://jira.mariadb.org/browse/MDEV-32050): Revert the throttling of [MDEV-26356](https://jira.mariadb.org/browse/MDEV-26356)
* [Revision #2027c482de](https://github.com/MariaDB/server/commit/2027c482de)\
  2023-10-25 09:38:49 +0300
  * [MDEV-32050](https://jira.mariadb.org/browse/MDEV-32050): Hold exclusive purge\_sys.rseg->latch longer
* [Revision #44689eb7d8](https://github.com/MariaDB/server/commit/44689eb7d8)\
  2023-10-25 09:38:21 +0300
  * [MDEV-32050](https://jira.mariadb.org/browse/MDEV-32050): Improve srv\_wake\_purge\_thread\_if\_not\_active()
* [Revision #14685b10df](https://github.com/MariaDB/server/commit/14685b10df)\
  2023-10-25 09:11:58 +0300
  * [MDEV-32050](https://jira.mariadb.org/browse/MDEV-32050): Deprecate\&ignore innodb\_purge\_rseg\_truncate\_frequency
* [Revision #21bec97044](https://github.com/MariaDB/server/commit/21bec97044)\
  2023-10-25 08:27:27 +0300
  * [MDEV-32050](https://jira.mariadb.org/browse/MDEV-32050): Clean up online ALTER
* [Revision #9bb5d9fe8b](https://github.com/MariaDB/server/commit/9bb5d9fe8b)\
  2023-10-25 08:27:08 +0300
  * [MDEV-32050](https://jira.mariadb.org/browse/MDEV-32050): Clean up log parsing
* [Revision #ea42c4baac](https://github.com/MariaDB/server/commit/ea42c4baac)\
  2023-10-25 08:26:34 +0300
  * [MDEV-32050](https://jira.mariadb.org/browse/MDEV-32050) preparation: Simplify ROLLBACK
* [Revision #b78b77e77d](https://github.com/MariaDB/server/commit/b78b77e77d)\
  2023-10-24 14:33:14 +0300
  * [MDEV-32530](https://jira.mariadb.org/browse/MDEV-32530) Race condition in lock\_wait\_rpl\_report()
* Merge [Revision #b21f52ee73](https://github.com/MariaDB/server/commit/b21f52ee73) 2023-10-23 16:43:48 +0300 - Merge 10.5 into 10.6
* [Revision #0a4103e6bb](https://github.com/MariaDB/server/commit/0a4103e6bb)\
  2023-10-23 08:22:18 +0200
  * new CC v3.3
* [Revision #4941ac9192](https://github.com/MariaDB/server/commit/4941ac9192)\
  2023-09-19 18:22:49 +0300
  * [MDEV-32113](https://jira.mariadb.org/browse/MDEV-32113): utf8mb3\_key\_col=utf8mb4\_value cannot be used for ref
* [Revision #6a674c3142](https://github.com/MariaDB/server/commit/6a674c3142)\
  2023-10-19 12:57:30 +0300
  * [MDEV-32476](https://jira.mariadb.org/browse/MDEV-32476) LeakSanitizer errors in get\_quick\_select or Assertion ...
* [Revision #a1b6befc78](https://github.com/MariaDB/server/commit/a1b6befc78)\
  2023-10-18 17:13:21 +0300
  * Fixed crash in is\_stat\_table() when using hash joins.
* Merge [Revision #6991b1c47c](https://github.com/MariaDB/server/commit/6991b1c47c) 2023-10-19 13:50:00 +0300 - Merge 10.5 into 10.6
* [Revision #bf7c6fc20b](https://github.com/MariaDB/server/commit/bf7c6fc20b)\
  2023-10-18 16:33:11 +0300
  * [MDEV-32511](https://jira.mariadb.org/browse/MDEV-32511) Assertion !os\_aio\_pending\_writes() failed
* [Revision #ee5cadd5c8](https://github.com/MariaDB/server/commit/ee5cadd5c8)\
  2023-10-16 20:17:09 +0530
  * [MDEV-28122](https://jira.mariadb.org/browse/MDEV-28122) Optimize table crash while applying online log
* [Revision #cca9547892](https://github.com/MariaDB/server/commit/cca9547892)\
  2023-10-16 12:55:17 +0300
  * Post fix for [MDEV-32449](https://jira.mariadb.org/browse/MDEV-32449)
* [Revision #1c554459b3](https://github.com/MariaDB/server/commit/1c554459b3)\
  2023-10-14 15:46:29 +0300
  * [MDEV-32449](https://jira.mariadb.org/browse/MDEV-32449) Server crashes in Alter\_info::add\_stat\_drop\_index upon CREATE TABLE
* [Revision #ec277a70e8](https://github.com/MariaDB/server/commit/ec277a70e8)\
  2023-10-14 13:43:26 +0300
  * Do not create histograms for single column unique key
* [Revision #18fa00a54c](https://github.com/MariaDB/server/commit/18fa00a54c)\
  2023-10-12 12:33:03 +0300
  * [MDEV-32272](https://jira.mariadb.org/browse/MDEV-32272) lock\_release\_on\_prepare\_try() does not release lock if supremum bit is set along with other bits set in lock's bitmap
* [Revision #cbad0bcd41](https://github.com/MariaDB/server/commit/cbad0bcd41)\
  2023-10-13 17:27:27 +0530
  * [MDEV-31098](https://jira.mariadb.org/browse/MDEV-31098) InnoDB Recovery doesn't display encryption message when no encryption configuration passed
* [Revision #8bf17c579b](https://github.com/MariaDB/server/commit/8bf17c579b)\
  2023-10-10 12:23:08 +0300
  * [MDEV-32388](https://jira.mariadb.org/browse/MDEV-32388) MSAN / Valgrind errors in Item\_func\_like::get\_mm\_leaf upon query from partitioned table
* [Revision #55534a2616](https://github.com/MariaDB/server/commit/55534a2616)\
  2023-10-10 12:18:49 +0300
  * Removed warning from ssl\_cipher.test
* [Revision #b159f05a63](https://github.com/MariaDB/server/commit/b159f05a63)\
  2023-10-07 17:17:15 +0300
  * [MDEV-31957](https://jira.mariadb.org/browse/MDEV-31957) Concurrent ALTER and ANALYZE collecting statistics can result in stale statistical data
* [Revision #fdcb443e62](https://github.com/MariaDB/server/commit/fdcb443e62)\
  2023-10-05 09:59:13 +0300
  * Remember first error in Dummy\_error\_handler
* [Revision #8941bdc474](https://github.com/MariaDB/server/commit/8941bdc474)\
  2023-10-07 21:27:53 -0700
  * Fix merge commit 5ea5291: No test file or result files should be executable
* Merge [Revision #625a150a86](https://github.com/MariaDB/server/commit/625a150a86) 2023-10-06 14:34:01 +0300 - Merge 10.5 into 10.6
* [Revision #10a368d35a](https://github.com/MariaDB/server/commit/10a368d35a)\
  2023-10-06 08:19:20 +0300
  * Fix GCC 13.2.0 -Wmismatched-new-delete
* [Revision #9e62ab7aaf](https://github.com/MariaDB/server/commit/9e62ab7aaf)\
  2023-04-25 14:24:39 +0200
  * [MDEV-31095](https://jira.mariadb.org/browse/MDEV-31095) tpool - do not create new worker, if thread creation is pending.
* [Revision #e33e2fa949](https://github.com/MariaDB/server/commit/e33e2fa949)\
  2023-04-25 12:00:06 +0200
  * [MDEV-31095](https://jira.mariadb.org/browse/MDEV-31095) tpool - restrict threadpool concurrency during bufferpool load
* [Revision #9ba8dc1413](https://github.com/MariaDB/server/commit/9ba8dc1413)\
  2023-09-27 17:26:24 +0300
  * [MDEV-32164](https://jira.mariadb.org/browse/MDEV-32164) Server crashes in JOIN::cleanup after erroneous query with view
* [Revision #d4347177c7](https://github.com/MariaDB/server/commit/d4347177c7)\
  2023-09-27 01:29:22 +0300
  * Change SEL\_ARG::MAX\_SEL\_ARGS to a user defined variable optimizer\_max\_sel\_args
* [Revision #4e9322e2ff](https://github.com/MariaDB/server/commit/4e9322e2ff)\
  2023-09-20 15:46:55 +0300
  * [MDEV-32203](https://jira.mariadb.org/browse/MDEV-32203) Raise notes when an index cannot be used on data type mismatch
* [Revision #4c8d2410b6](https://github.com/MariaDB/server/commit/4c8d2410b6)\
  2023-09-24 14:40:29 +0300
  * Give warnings if open\_stat\_table\_for\_ddl() fails
* [Revision #684f7f81a0](https://github.com/MariaDB/server/commit/684f7f81a0)\
  2023-09-20 03:10:45 +0300
  * Change BUILD scripts to use with-ssl=system
* [Revision #5910bc1f3d](https://github.com/MariaDB/server/commit/5910bc1f3d)\
  2023-09-19 14:13:30 +0300
  * Correction of recent PR in mroonga for 10.6 code
* [Revision #8edef482a7](https://github.com/MariaDB/server/commit/8edef482a7)\
  2023-09-09 17:13:41 +0300
  * Changed some malloc() calls to my\_malloc()
* [Revision #c4a5bd1efd](https://github.com/MariaDB/server/commit/c4a5bd1efd)\
  2023-09-07 15:18:26 +0300
  * Added Myisam, Aria and InnoDB buffer pool to @@memory\_used status variable
* [Revision #e3b36b8f1b](https://github.com/MariaDB/server/commit/e3b36b8f1b)\
  2023-08-18 18:35:02 +0300
  * [MDEV-31957](https://jira.mariadb.org/browse/MDEV-31957) Concurrent ALTER and ANALYZE collecting statistics can result in stale statistical data
* [Revision #388296a1e6](https://github.com/MariaDB/server/commit/388296a1e6)\
  2023-09-28 19:06:59 +0300
  * [MDEV-32257](https://jira.mariadb.org/browse/MDEV-32257) dangling XA-rollback in binlog from emtpy XA in pseudo\_slave\_mode
* [Revision #29e7f53bf5](https://github.com/MariaDB/server/commit/29e7f53bf5)\
  2023-09-22 21:49:01 +0200
  * [MDEV-32232](https://jira.mariadb.org/browse/MDEV-32232) mysql\_install\_db\_win.test fails on second execution
* [Revision #a2a08eda8a](https://github.com/MariaDB/server/commit/a2a08eda8a)\
  2023-09-22 13:37:07 +0200
  * [MDEV-27943](https://jira.mariadb.org/browse/MDEV-27943) - reduce calls to mysql\_socket\_set\_thread\_owner() in threadpool
* [Revision #076df87b4c](https://github.com/MariaDB/server/commit/076df87b4c)\
  2023-09-15 08:30:46 +0300
  * [MDEV-30217](https://jira.mariadb.org/browse/MDEV-30217) : Assertion \`mode\_ == m\_local || transaction\_.is\_streaming()' failed in int wsrep::client\_state::bf\_abort(wsrep::seqno)
* Merge [Revision #d13a57ae81](https://github.com/MariaDB/server/commit/d13a57ae81) 2023-09-22 15:21:15 +0300 - Merge 10.5 into 10.6.
* [Revision #ddffae0a88](https://github.com/MariaDB/server/commit/ddffae0a88)\
  2023-09-22 12:02:47 +0700
  * [MDEV-31871](https://jira.mariadb.org/browse/MDEV-31871): maria-install-db fails on MacOS
* [Revision #541433508f](https://github.com/MariaDB/server/commit/541433508f)\
  2023-09-22 12:01:52 +0700
  * [MDEV-31871](https://jira.mariadb.org/browse/MDEV-31871): maria-install-db fails on MacOS
* [Revision #52e7016248](https://github.com/MariaDB/server/commit/52e7016248)\
  2023-09-20 08:36:30 +0300
  * Remove dead code
* Merge [Revision #60b039a864](https://github.com/MariaDB/server/commit/60b039a864) 2023-09-20 08:32:04 +0300 - Merge 10.5 into 10.6
* [Revision #2fdacdcd69](https://github.com/MariaDB/server/commit/2fdacdcd69)\
  2023-09-19 17:40:21 +0530
  * [MDEV-30802](https://jira.mariadb.org/browse/MDEV-30802) Assertion \`index->is\_btree() || index->is\_ibuf()' failed in btr\_search\_guess\_on\_hash
* Merge [Revision #8096139b3a](https://github.com/MariaDB/server/commit/8096139b3a) 2023-09-19 10:47:26 +0300 - Merge 10.5 into 10.6
* [Revision #85db6df412](https://github.com/MariaDB/server/commit/85db6df412)\
  2023-09-18 18:26:07 +0530
  * [MDEV-32151](https://jira.mariadb.org/browse/MDEV-32151) InnoDB scrubbing doesn't write zero while freeing the page for temporary tablespace
* Merge [Revision #0f870914d4](https://github.com/MariaDB/server/commit/0f870914d4) 2023-09-15 15:23:37 +1000 - Merge branch '10.5' into 10.6
* Merge [Revision #b70d8fbf18](https://github.com/MariaDB/server/commit/b70d8fbf18) 2023-09-15 12:12:46 +1000 - Merge branch '10.5' into 10.6
* Merge [Revision #6a470db552](https://github.com/MariaDB/server/commit/6a470db552) 2023-09-14 15:25:53 +0300 - Merge 10.5 into 10.6
* Merge [Revision #0f9acce3f2](https://github.com/MariaDB/server/commit/0f9acce3f2) 2023-09-14 09:01:15 +0300 - Merge 10.5 into 10.6
* [Revision #cce76df5cc](https://github.com/MariaDB/server/commit/cce76df5cc)\
  2023-09-14 08:58:41 +0300
  * Fix cmake -DWITH\_INNODB\_AHI=OFF
* [Revision #736901b443](https://github.com/MariaDB/server/commit/736901b443)\
  2023-09-12 12:25:51 +0300
  * [MDEV-30100](https://jira.mariadb.org/browse/MDEV-30100) fixup: Remove a failing debug assertion
* [Revision #3c840ae746](https://github.com/MariaDB/server/commit/3c840ae746)\
  2023-09-12 12:03:35 +0300
  * [MDEV-26782](https://jira.mariadb.org/browse/MDEV-26782) fixup: Remove dead code
* [Revision #a03b8cd0a2](https://github.com/MariaDB/server/commit/a03b8cd0a2)\
  2023-09-11 17:39:58 +0530
  * [MDEV-32145](https://jira.mariadb.org/browse/MDEV-32145) Disable read-ahead for temporary tablespace
* [Revision #cdd2fa7fc5](https://github.com/MariaDB/server/commit/cdd2fa7fc5)\
  2023-09-11 14:54:50 +0300
  * [MDEV-32134](https://jira.mariadb.org/browse/MDEV-32134) InnoDB hang in buf\_flush\_wait\_LRU\_batch\_end()
* [Revision #466d9f5ff3](https://github.com/MariaDB/server/commit/466d9f5ff3)\
  2023-09-11 14:54:17 +0300
  * [MDEV-32103](https://jira.mariadb.org/browse/MDEV-32103) InnoDB ALTER TABLE is not crash-safe
* [Revision #4a8291fc5f](https://github.com/MariaDB/server/commit/4a8291fc5f)\
  2023-09-11 14:52:05 +0300
  * [MDEV-30531](https://jira.mariadb.org/browse/MDEV-30531) Corrupt index(es) on busy table when using FOREIGN KEY
* [Revision #e039720bf3](https://github.com/MariaDB/server/commit/e039720bf3)\
  2023-09-11 14:51:02 +0300
  * [MDEV-32096](https://jira.mariadb.org/browse/MDEV-32096) Parallel replication lags because innobase\_kill\_query() may fail to interrupt a lock wait
* Merge [Revision #0dd25f28f7](https://github.com/MariaDB/server/commit/0dd25f28f7) 2023-09-11 14:46:39 +0300 - Merge 10.5 into 10.6
* [Revision #961b96a5e0](https://github.com/MariaDB/server/commit/961b96a5e0)\
  2023-08-30 14:19:51 +0530
  * [MDEV-29324](https://jira.mariadb.org/browse/MDEV-29324) s390x patch srw\_lock.cc
* [Revision #f009c4da91](https://github.com/MariaDB/server/commit/f009c4da91)\
  2023-09-01 11:24:42 +0300
  * Small corrections to [MDEV-29693](https://jira.mariadb.org/browse/MDEV-29693) ANALYZE TABLE
* [Revision #182a08a8a3](https://github.com/MariaDB/server/commit/182a08a8a3)\
  2023-09-04 09:59:18 +0300
  * Removed compiler warning from connect/filamdbf.cpp
* Merge [Revision #de5dba9ebe](https://github.com/MariaDB/server/commit/de5dba9ebe) 2023-09-05 14:44:52 +0700 - Merge branch '10.5' into 10.6
* Merge [Revision #b0a43818b4](https://github.com/MariaDB/server/commit/b0a43818b4) 2023-09-04 10:15:02 +0300 - Merge 10.5 into 10.6
* Merge [Revision #2325f8f339](https://github.com/MariaDB/server/commit/2325f8f339) 2023-08-31 13:01:42 +0300 - Merge 10.5 into 10.6
* [Revision #9d1466522e](https://github.com/MariaDB/server/commit/9d1466522e)\
  2023-08-30 14:40:13 +0300
  * [MDEV-32029](https://jira.mariadb.org/browse/MDEV-32029) Assertion failures in log\_sort\_flush\_list upon crash recovery
* [Revision #31ea201ecc](https://github.com/MariaDB/server/commit/31ea201ecc)\
  2023-08-30 13:20:27 +0300
  * [MDEV-30986](https://jira.mariadb.org/browse/MDEV-30986) Slow full index scan for I/O bound case
* [Revision #9b1b4a6f69](https://github.com/MariaDB/server/commit/9b1b4a6f69)\
  2023-08-30 15:17:07 +1000
  * [MDEV-31545](https://jira.mariadb.org/browse/MDEV-31545) Revert "Fix gcc warning for wsrep\_plug"
* [Revision #c438284863](https://github.com/MariaDB/server/commit/c438284863)\
  2023-08-25 17:22:17 +0530
  * [MDEV-31835](https://jira.mariadb.org/browse/MDEV-31835) Remove unnecesary extra HA\_EXTRA\_IGNORE\_INSERT call
* [Revision #08a549c33d](https://github.com/MariaDB/server/commit/08a549c33d)\
  2023-08-25 13:44:59 +0300
  * Clean up buf\_LRU\_remove\_hashed()
* [Revision #f7780a8eb8](https://github.com/MariaDB/server/commit/f7780a8eb8)\
  2023-08-25 13:41:54 +0300
  * [MDEV-30100](https://jira.mariadb.org/browse/MDEV-30100): Assertion purge\_sys.tail.trx\_no <= purge\_sys.rseg->last\_trx\_no()
* [Revision #4ff5311dec](https://github.com/MariaDB/server/commit/4ff5311dec)\
  2023-08-25 13:23:21 +0300
  * [MDEV-30100](https://jira.mariadb.org/browse/MDEV-30100) preparation: Simplify InnoDB transaction commit further
* [Revision #f4bbea90f1](https://github.com/MariaDB/server/commit/f4bbea90f1)\
  2023-08-25 13:16:54 +0300
  * [MDEV-30100](https://jira.mariadb.org/browse/MDEV-30100) preparation: Simplify InnoDB transaction commit
* Merge [Revision #eda75cadea](https://github.com/MariaDB/server/commit/eda75cadea) 2023-08-24 10:16:24 +0300 - Merge 10.5 into 10.6
* Merge [Revision #4e7d2e73c0](https://github.com/MariaDB/server/commit/4e7d2e73c0) 2023-08-23 18:12:20 +1000 - Merge 10.5 into 10.6
* Merge [Revision #07494006dd](https://github.com/MariaDB/server/commit/07494006dd) 2023-08-22 09:36:35 +0300 - Merge 10.5 into 10.6
* [Revision #a60462d93e](https://github.com/MariaDB/server/commit/a60462d93e)\
  2023-08-21 15:51:16 +0300
  * Remove bogus references to replaced Google contributions
* [Revision #6cc88c3db1](https://github.com/MariaDB/server/commit/6cc88c3db1)\
  2023-08-21 15:51:10 +0300
  * Clean up buf0buf.inl
* Merge [Revision #448c2077fb](https://github.com/MariaDB/server/commit/448c2077fb) 2023-08-21 15:50:31 +0300 - Merge 10.5 into 10.6
* [Revision #a6bf4b5807](https://github.com/MariaDB/server/commit/a6bf4b5807)\
  2023-08-05 01:08:05 +0300
  * [MDEV-29693](https://jira.mariadb.org/browse/MDEV-29693) ANALYZE TABLE still flushes table definition cache when engine-independent statistics is used
* [Revision #88dd50b80a](https://github.com/MariaDB/server/commit/88dd50b80a)\
  2023-08-16 09:12:28 +0400
  * After-merge cleanup for [MDEV-27207](https://jira.mariadb.org/browse/MDEV-27207) + [MDEV-31719](https://jira.mariadb.org/browse/MDEV-31719)
* [Revision #ca5c122adc](https://github.com/MariaDB/server/commit/ca5c122adc)\
  2023-08-11 17:59:40 +0300
  * [MDEV-9938](https://jira.mariadb.org/browse/MDEV-9938) Prepared statement return wrong result (missing row)
* Merge [Revision #f6dd130885](https://github.com/MariaDB/server/commit/f6dd130885) 2023-08-15 18:11:35 +0200 - (Null) Merge 10.5 -> 10.6
* [Revision #805e0668c9](https://github.com/MariaDB/server/commit/805e0668c9)\
  2023-07-09 16:45:47 +0200
  * [MDEV-31482](https://jira.mariadb.org/browse/MDEV-31482): Lock wait timeout with INSERT-SELECT, autoinc, and statement-based replication
* [Revision #18acbaf416](https://github.com/MariaDB/server/commit/18acbaf416)\
  2023-08-05 22:53:44 +0200
  * [MDEV-31655](https://jira.mariadb.org/browse/MDEV-31655): Parallel replication deadlock victim preference code errorneously removed
* Merge [Revision #3fee1b4471](https://github.com/MariaDB/server/commit/3fee1b4471) 2023-08-15 11:21:34 +0300 - Merge 10.5 into 10.6
* Merge [Revision #fc78b25337](https://github.com/MariaDB/server/commit/fc78b25337) 2023-08-15 11:03:00 +0300 - Merge mariadb-10.6.15 into 10.6
* [Revision #e0398c5b8c](https://github.com/MariaDB/server/commit/e0398c5b8c)\
  2023-08-14 13:47:13 -0400
  * bump the VERSION
* [Revision #e9723c2cbb](https://github.com/MariaDB/server/commit/e9723c2cbb)\
  2023-08-14 13:36:17 +0300
  * [MDEV-31473](https://jira.mariadb.org/browse/MDEV-31473) Wrong information about innodb\_checksum\_algorithm in information\_schema.SYSTEM\_VARIABLES
* [Revision #0be4781428](https://github.com/MariaDB/server/commit/0be4781428)\
  2023-07-25 15:25:09 +0300
  * [MDEV-31737](https://jira.mariadb.org/browse/MDEV-31737) : Node never returns from Donor/Desynced to Synced when wsrep\_mode = BF\_ABORT\_MARIABACKUP

{% @marketo/form formid="4316" formId="4316" %}
