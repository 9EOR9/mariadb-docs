# MariaDB 10.6.3 Changelog

The most recent release of [MariaDB 10.6](../../mariadb-community-server-release-notes/mariadb-10-6-series/what-is-mariadb-106.md) is:[**MariaDB 10.6.21**](../../mariadb-community-server-release-notes/mariadb-10-6-series/mariadb-10-6-21-release-notes.md) Stable (GA) [Download Now](https://mariadb.com/downloads/)[_Alternate download from mariadb.org_](https://downloads.mariadb.org/mariadb/10.6.21/)

[Download 10.6.3](https://mariadb.org/download/?tab=mariadb\&release=10.6.3\&product=mariadb)[Release Notes](../../mariadb-community-server-release-notes/mariadb-10-6-series/mariadb-1063-release-notes.md)[Changelog](mariadb-1063-changelog.md)[Overview of 10.6](../../mariadb-community-server-release-notes/mariadb-10-6-series/what-is-mariadb-106.md)

**Release date:** 6 Jul 2021

For the highlights of this release, see the[release notes](../../mariadb-community-server-release-notes/mariadb-10-6-series/mariadb-1063-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/server/tree/10.6) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Includes all fixes from [MariaDB 10.5.11](../changelogs-mariadb-105-series/mariadb-10511-changelog.md)
* [Revision #1f2ccc6db8](https://github.com/MariaDB/server/commit/1f2ccc6db8)\
  2021-07-05 11:56:24 +0200
  * update C/C to 3.2.3
* [Revision #6fa72fb1f2](https://github.com/MariaDB/server/commit/6fa72fb1f2)\
  2021-07-04 12:10:54 +0200
  * mtr: report full command line of mysqld that failed to start
* [Revision #789a2a363a](https://github.com/MariaDB/server/commit/789a2a363a)\
  2021-07-03 20:35:29 +0300
  * fixup 0a67b15a9d3348d10f6df0caae6f2f973295a43a
* Merge [Revision #b797f217a3](https://github.com/MariaDB/server/commit/b797f217a3) 2021-07-03 14:54:46 +0300 - Merge 10.5 into 10.6
* [Revision #f0f47cbca1](https://github.com/MariaDB/server/commit/f0f47cbca1)\
  2021-07-03 14:52:04 +0300
  * [MDEV-26017](https://jira.mariadb.org/browse/MDEV-26017) fixup
* [Revision #bd5a6403ca](https://github.com/MariaDB/server/commit/bd5a6403ca)\
  2021-07-03 13:58:38 +0300
  * [MDEV-26033](https://jira.mariadb.org/browse/MDEV-26033): Race condition between buf\_pool.page\_hash and resize()
* [Revision #9ec3cd9af0](https://github.com/MariaDB/server/commit/9ec3cd9af0)\
  2021-07-02 23:52:55 +0200
  * gamma -> stable
* [Revision #028d611832](https://github.com/MariaDB/server/commit/028d611832)\
  2021-07-02 20:36:37 +0200
  * update test result
* [Revision #59bc063d26](https://github.com/MariaDB/server/commit/59bc063d26)\
  2021-07-02 08:26:32 +0200
  * main.lock\_kill fails in embedded
* [Revision #4145ebf99a](https://github.com/MariaDB/server/commit/4145ebf99a)\
  2021-07-02 00:26:04 +0200
  * [MDEV-25906](https://jira.mariadb.org/browse/MDEV-25906): SIGSEGV in flush\_tables\_with\_read\_lock on FTWRL or FTFE | SIGSEGV in ha\_maria::extra
* [Revision #164a64baa3](https://github.com/MariaDB/server/commit/164a64baa3)\
  2021-07-02 00:05:27 +0200
  * [MDEV-15888](https://jira.mariadb.org/browse/MDEV-15888) Implement FLUSH TABLES tbl\_name \[, tbl\_name] ... WITH READ LOCK for views.
* [Revision #b5f50e2de8](https://github.com/MariaDB/server/commit/b5f50e2de8)\
  2021-07-01 13:33:38 +0200
  * errors after altering a table has finished aren't fatal
* Merge [Revision #0ad8a825a8](https://github.com/MariaDB/server/commit/0ad8a825a8) 2021-07-02 17:00:05 +0300 - Merge 10.5 into 10.6
* [Revision #779262842e](https://github.com/MariaDB/server/commit/779262842e)\
  2021-06-30 01:03:49 +0200
  * [MDEV-23004](https://jira.mariadb.org/browse/MDEV-23004) When using GROUP BY with JSON\_ARRAYAGG with joint table, the square brackets are not included
* Merge [Revision #8c029d426a](https://github.com/MariaDB/server/commit/8c029d426a) 2021-07-02 16:19:25 +0300 - Merge 10.4 into 10.5
* [Revision #a635588b56](https://github.com/MariaDB/server/commit/a635588b56)\
  2021-07-02 16:11:01 +0300
  * [MDEV-25236](https://jira.mariadb.org/browse/MDEV-25236) Online log apply fails for ROW\_FORMAT=REDUNDANT tables
* Merge [Revision #372ea88264](https://github.com/MariaDB/server/commit/372ea88264) 2021-07-02 14:55:52 +0300 - Merge 10.3 into 10.4
* Merge [Revision #f9194d02da](https://github.com/MariaDB/server/commit/f9194d02da) 2021-07-02 14:41:41 +0300 - Merge 10.2 into 10.3
* [Revision #ffe744e77d](https://github.com/MariaDB/server/commit/ffe744e77d)\
  2021-07-02 13:07:36 +0300
  * submodules.cmake: add missing --depth=1
* [Revision #a6adefad4b](https://github.com/MariaDB/server/commit/a6adefad4b)\
  2021-07-02 14:41:32 +0300
  * Fixup 586870f9effa48831fda2590f2aee2b95b30be39
* Merge [Revision #15dcb8bd3e](https://github.com/MariaDB/server/commit/15dcb8bd3e) 2021-07-02 13:02:26 +0300 - Merge 10.4 into 10.5
* Merge [Revision #c294443b41](https://github.com/MariaDB/server/commit/c294443b41) 2021-07-02 11:48:51 +0300 - Merge 10.3 into 10.4
* Merge [Revision #05f7fd571f](https://github.com/MariaDB/server/commit/05f7fd571f) 2021-07-02 11:44:51 +0300 - Merge 10.2 into 10.3
* [Revision #2bf6f2c054](https://github.com/MariaDB/server/commit/2bf6f2c054)\
  2021-07-02 11:15:35 +0300
  * [MDEV-26077](https://jira.mariadb.org/browse/MDEV-26077) Assertion err != DB\_DUPLICATE\_KEY or unexpected ER\_TABLE\_EXISTS\_ERROR
* [Revision #5a2b625843](https://github.com/MariaDB/server/commit/5a2b625843)\
  2021-07-02 11:08:48 +0300
  * [MDEV-25129](https://jira.mariadb.org/browse/MDEV-25129) fixup: Adjust test result
* [Revision #e34877ab63](https://github.com/MariaDB/server/commit/e34877ab63)\
  2021-07-01 16:14:09 +0530
  * [MDEV-25971](https://jira.mariadb.org/browse/MDEV-25971) Instant ADD COLUMN fails to issue truncation warnings
* [Revision #fa8eb4de55](https://github.com/MariaDB/server/commit/fa8eb4de55)\
  2021-07-02 14:54:59 +1000
  * mtr: plugin.multiauth aix fix
* Merge [Revision #95e9f3c186](https://github.com/MariaDB/server/commit/95e9f3c186) 2021-07-02 17:17:33 +1000 - Merge branch 10.3 into 10.4
* [Revision #7ce5984d6d](https://github.com/MariaDB/server/commit/7ce5984d6d)\
  2021-07-02 15:50:21 +1000
  * mtr: fix tests funcs\_1.is\_tables\_is & sql\_sequence.rebuild
* Merge [Revision #a88ddb168f](https://github.com/MariaDB/server/commit/a88ddb168f) 2021-07-02 16:35:49 +1000 - Merge branch '10.2' into 10.3
* [Revision #c22f7f2323](https://github.com/MariaDB/server/commit/c22f7f2323)\
  2021-07-02 15:57:50 +1000
  * [MDEV-25129](https://jira.mariadb.org/browse/MDEV-25129) postfix for windows
* [Revision #0a9487b62b](https://github.com/MariaDB/server/commit/0a9487b62b)\
  2021-07-02 13:00:34 +1000
  * mtr: aix - no pool of threads
* [Revision #3f2c4758b0](https://github.com/MariaDB/server/commit/3f2c4758b0)\
  2021-06-11 17:13:19 +1000
  * [MDEV-25894](https://jira.mariadb.org/browse/MDEV-25894): support AIX as a platform in mtr
* [Revision #6a3a046013](https://github.com/MariaDB/server/commit/6a3a046013)\
  2021-07-02 13:00:34 +1000
  * mtr: aix - no pool of threads
* [Revision #2301093f8f](https://github.com/MariaDB/server/commit/2301093f8f)\
  2021-06-11 17:13:19 +1000
  * [MDEV-25894](https://jira.mariadb.org/browse/MDEV-25894): support AIX as a platform in mtr
* [Revision #c7443a0911](https://github.com/MariaDB/server/commit/c7443a0911)\
  2021-07-01 01:08:28 +0300
  * [MDEV-25969](https://jira.mariadb.org/browse/MDEV-25969): Condition pushdown into derived table doesn't work if select list uses SP
* Merge [Revision #eebe2090c8](https://github.com/MariaDB/server/commit/eebe2090c8) 2021-06-30 18:13:08 +0300 - Merge 10.3 -> 10.4
* [Revision #4a6e2d3437](https://github.com/MariaDB/server/commit/4a6e2d3437)\
  2021-06-30 16:43:43 +0300
  * Post-merge fix: update derived\_cond\_pushdown.result
* Merge [Revision #586870f9ef](https://github.com/MariaDB/server/commit/586870f9ef) 2021-06-30 15:06:54 +0300 - Merge 10.2->10.3
* [Revision #eb20c91b55](https://github.com/MariaDB/server/commit/eb20c91b55)\
  2021-06-29 16:31:28 +0300
  * [MDEV-25969](https://jira.mariadb.org/browse/MDEV-25969): Condition pushdown into derived table doesn't work if select list uses SP
* [Revision #768c51880a](https://github.com/MariaDB/server/commit/768c51880a)\
  2021-06-24 14:16:11 +0300
  * [MDEV-25129](https://jira.mariadb.org/browse/MDEV-25129) Add KEYWORDS view to the INFORMATION\_SCHEMA
* [Revision #58252fff15](https://github.com/MariaDB/server/commit/58252fff15)\
  2021-06-29 14:28:23 +0300
  * [MDEV-26040](https://jira.mariadb.org/browse/MDEV-26040) os\_file\_set\_size() may not work on O\_DIRECT files
* [Revision #8147d2e618](https://github.com/MariaDB/server/commit/8147d2e618)\
  2021-06-28 11:52:00 +0400
  * [MDEV-25461](https://jira.mariadb.org/browse/MDEV-25461) Assertion \`je->state == JST\_KEY' failed in Geometry::create\_from\_json.
* [Revision #4e4f742ed7](https://github.com/MariaDB/server/commit/4e4f742ed7)\
  2021-06-26 23:11:10 -0700
  * Adjusted test results after the fix for [MDEV-20411](https://jira.mariadb.org/browse/MDEV-20411) (2)
* [Revision #8b3f816cab](https://github.com/MariaDB/server/commit/8b3f816cab)\
  2021-06-26 08:51:17 -0700
  * Adjusted test results after the fix for [MDEV-20411](https://jira.mariadb.org/browse/MDEV-20411)
* [Revision #12c80df482](https://github.com/MariaDB/server/commit/12c80df482)\
  2021-06-25 18:03:29 -0700
  * [MDEV-20411](https://jira.mariadb.org/browse/MDEV-20411) Procedure containing CTE incorrectly stored in mysql.proc
* [Revision #4ad148b148](https://github.com/MariaDB/server/commit/4ad148b148)\
  2021-06-25 06:48:17 +0200
  * [MDEV-26019](https://jira.mariadb.org/browse/MDEV-26019): Upgrading MariaDB breaks TLS mariabackup SST
* [Revision #9258cfa4b4](https://github.com/MariaDB/server/commit/9258cfa4b4)\
  2021-06-22 15:44:44 +0300
  * [MDEV-25978](https://jira.mariadb.org/browse/MDEV-25978) : rsync SST does not work with custom binlog name
* [Revision #83464029ce](https://github.com/MariaDB/server/commit/83464029ce)\
  2021-06-18 10:16:38 +0300
  * Fix try for Galera test lp1376747-4
* [Revision #f67aee000d](https://github.com/MariaDB/server/commit/f67aee000d)\
  2021-06-22 22:00:23 -0400
  * bump the VERSION
* [Revision #aaaed9baa0](https://github.com/MariaDB/server/commit/aaaed9baa0)\
  2021-06-22 18:57:01 +0700
  * [MDEV-25960](https://jira.mariadb.org/browse/MDEV-25960) yum update overwrites customized logrotation config (/etc/logrotate.d/mysql)
* [Revision #29098083f7](https://github.com/MariaDB/server/commit/29098083f7)\
  2021-06-25 06:48:17 +0200
  * [MDEV-26019](https://jira.mariadb.org/browse/MDEV-26019): Upgrading MariaDB breaks TLS mariabackup SST
* [Revision #05a4996c5c](https://github.com/MariaDB/server/commit/05a4996c5c)\
  2021-06-22 15:44:44 +0300
  * [MDEV-25978](https://jira.mariadb.org/browse/MDEV-25978) : rsync SST does not work with custom binlog name
* [Revision #a1e2ca057d](https://github.com/MariaDB/server/commit/a1e2ca057d)\
  2021-06-30 10:38:44 +0300
  * [MDEV-26030](https://jira.mariadb.org/browse/MDEV-26030) : Warning: Memory not freed: 32 on setting wsrep\_sst\_auth
* [Revision #6431862022](https://github.com/MariaDB/server/commit/6431862022)\
  2021-06-29 12:44:42 +0200
  * [MDEV-25978](https://jira.mariadb.org/browse/MDEV-25978) post-merge: updated mtr result files
* [Revision #58700a426a](https://github.com/MariaDB/server/commit/58700a426a)\
  2021-06-29 12:42:14 +0200
  * [MDEV-26019](https://jira.mariadb.org/browse/MDEV-26019): Upgrading MariaDB breaks TLS mariabackup SST
* [Revision #1c03e7a667](https://github.com/MariaDB/server/commit/1c03e7a667)\
  2021-06-22 15:44:44 +0300
  * [MDEV-25978](https://jira.mariadb.org/browse/MDEV-25978) : rsync SST does not work with custom binlog name
* [Revision #315380a4d1](https://github.com/MariaDB/server/commit/315380a4d1)\
  2021-07-01 19:06:53 +0300
  * [MDEV-26052](https://jira.mariadb.org/browse/MDEV-26052) Assertion prebuilt->trx\_id < table->def\_trx\_id failed
* [Revision #ed6b230744](https://github.com/MariaDB/server/commit/ed6b230744)\
  2021-07-01 17:51:55 +0300
  * [MDEV-25919](https://jira.mariadb.org/browse/MDEV-25919) preparation: Remove trx\_t::internal
* [Revision #0a67b15a9d](https://github.com/MariaDB/server/commit/0a67b15a9d)\
  2021-07-01 16:38:24 +0300
  * Cleanup: Remove pointer indirection for trx\_t::xid
* [Revision #83234719f1](https://github.com/MariaDB/server/commit/83234719f1)\
  2021-07-01 16:37:01 +0300
  * [MDEV-24671](https://jira.mariadb.org/browse/MDEV-24671) fixup: Fix an off-by-one error
* [Revision #161e4bfafd](https://github.com/MariaDB/server/commit/161e4bfafd)\
  2021-07-01 10:35:32 +0300
  * [MDEV-25902](https://jira.mariadb.org/browse/MDEV-25902) Unexpected ER\_LOCK\_WAIT\_TIMEOUT and result
* [Revision #8c5c3a4594](https://github.com/MariaDB/server/commit/8c5c3a4594)\
  2021-07-01 10:31:08 +0300
  * [MDEV-26067](https://jira.mariadb.org/browse/MDEV-26067) innodb\_lock\_wait\_timeout values above 100,000,000 are useless
* [Revision #ce1c957ab1](https://github.com/MariaDB/server/commit/ce1c957ab1)\
  2021-07-01 10:04:47 +0300
  * Speed up the test innodb.lock\_insert\_into\_empty
* [Revision #add782a13e](https://github.com/MariaDB/server/commit/add782a13e)\
  2021-06-30 21:28:07 +0200
  * fix JSON\_ARRAYAGG not to over-quote json in joins
* [Revision #b62672af72](https://github.com/MariaDB/server/commit/b62672af72)\
  2021-06-30 21:17:57 +0200
  * [MDEV-26054](https://jira.mariadb.org/browse/MDEV-26054) Server crashes in Item\_func\_json\_arrayagg::get\_str\_from\_field
* [Revision #83684fc9a4](https://github.com/MariaDB/server/commit/83684fc9a4)\
  2021-06-30 01:03:49 +0200
  * [MDEV-23004](https://jira.mariadb.org/browse/MDEV-23004) When using GROUP BY with JSON\_ARRAYAGG with joint table, the square brackets are not included
* [Revision #8711adb786](https://github.com/MariaDB/server/commit/8711adb786)\
  2021-06-30 01:00:50 +0200
  * fix JSON\_ARRAYAGG not to over-quote json in joins
* [Revision #c8fb911e9c](https://github.com/MariaDB/server/commit/c8fb911e9c)\
  2021-06-28 22:08:52 +0200
  * fix main.lock\_kill crashes in --ps --embed
* [Revision #771f3cf995](https://github.com/MariaDB/server/commit/771f3cf995)\
  2021-06-28 12:27:00 +0200
  * make --rr work with InnoDB again
* [Revision #6fab256bc8](https://github.com/MariaDB/server/commit/6fab256bc8)\
  2021-06-29 20:12:00 +0200
  * disable spider/bugfix.wait\_timeout
* [Revision #fa5c314377](https://github.com/MariaDB/server/commit/fa5c314377)\
  2021-06-28 10:31:55 +0200
  * fix spider tests for --ps in 10.6
* [Revision #ff9150f3c5](https://github.com/MariaDB/server/commit/ff9150f3c5)\
  2021-06-30 09:00:52 +0300
  * [MDEV-25942](https://jira.mariadb.org/browse/MDEV-25942): Assertion failure in trx\_t::drop\_table()
* [Revision #c2ebe8147d](https://github.com/MariaDB/server/commit/c2ebe8147d)\
  2021-06-29 16:03:26 +0400
  * [MDEV-25837](https://jira.mariadb.org/browse/MDEV-25837) Assertion \`thd->locked\_tables\_mode == LTM\_NONE' failed in Locked\_tables\_list::init\_locked\_tables.
* [Revision #0237e9bb65](https://github.com/MariaDB/server/commit/0237e9bb65)\
  2021-06-29 13:39:42 +0300
  * [MDEV-26041](https://jira.mariadb.org/browse/MDEV-26041) Recovery failure due to delete-marked SYS\_FIELDS record
* [Revision #e04bbf73dc](https://github.com/MariaDB/server/commit/e04bbf73dc)\
  2021-06-28 17:10:09 +0300
  * [MDEV-25496](https://jira.mariadb.org/browse/MDEV-25496) Assertion 'trx->bulk\_insert' failed on INSERT
* [Revision #4b0070f642](https://github.com/MariaDB/server/commit/4b0070f642)\
  2021-06-29 15:20:16 +0300
  * [MDEV-26029](https://jira.mariadb.org/browse/MDEV-26029): Implement my\_test\_if\_thinly\_provisioned() for ScaleFlux
* [Revision #30edd5549d](https://github.com/MariaDB/server/commit/30edd5549d)\
  2021-06-28 13:42:43 +0300
  * [MDEV-26029](https://jira.mariadb.org/browse/MDEV-26029): Sparse files are inefficient on thinly provisioned storage
* Merge [Revision #b11aa0df85](https://github.com/MariaDB/server/commit/b11aa0df85) 2021-06-29 15:18:18 +0300 - Merge 10.5 into 10.6
* [Revision #617dee3488](https://github.com/MariaDB/server/commit/617dee3488)\
  2021-06-29 15:04:27 +0300
  * [MDEV-26042](https://jira.mariadb.org/browse/MDEV-26042) Atomic write capability is not detected correctly
* [Revision #3d15e3c085](https://github.com/MariaDB/server/commit/3d15e3c085)\
  2021-06-29 15:02:10 +0300
  * [MDEV-22640](https://jira.mariadb.org/browse/MDEV-22640) fixup: clang -Winconsistent-missing-override
* [Revision #98c7916f0f](https://github.com/MariaDB/server/commit/98c7916f0f)\
  2021-06-24 13:28:28 +0400
  * [MDEV-23004](https://jira.mariadb.org/browse/MDEV-23004) When using GROUP BY with JSON\_ARRAYAGG with joint table, the square brackets are not included.
* [Revision #390014781b](https://github.com/MariaDB/server/commit/390014781b)\
  2021-06-26 20:36:53 +0300
  * [MDEV-26031](https://jira.mariadb.org/browse/MDEV-26031) unnessary xid logging in one phase commit case
* [Revision #c29f45ce77](https://github.com/MariaDB/server/commit/c29f45ce77)\
  2021-06-29 00:12:03 +0300
  * [MDEV-25481](https://jira.mariadb.org/browse/MDEV-25481) Memory leak in Cached\_item\_str::Cached\_item\_str WITH TIES involving a blob
* [Revision #63e9a05440](https://github.com/MariaDB/server/commit/63e9a05440)\
  2021-06-28 15:37:29 +0300
  * [MDEV-25942](https://jira.mariadb.org/browse/MDEV-25942): Assertion !table.n\_waiting\_or\_granted\_auto\_inc\_locks
* Merge [Revision #891a927e80](https://github.com/MariaDB/server/commit/891a927e80) 2021-06-26 11:53:28 +0300 - Merge 10.5 into 10.6
* [Revision #fc2ff46469](https://github.com/MariaDB/server/commit/fc2ff46469)\
  2021-06-26 11:52:25 +0300
  * [MDEV-26017](https://jira.mariadb.org/browse/MDEV-26017): Assertion stat.flush\_list\_bytes <= curr\_pool\_size
* [Revision #aa95c42360](https://github.com/MariaDB/server/commit/aa95c42360)\
  2021-06-26 11:17:05 +0300
  * Cleanup: Remove unused mtr\_block\_dirtied
* [Revision #759deaa0a2](https://github.com/MariaDB/server/commit/759deaa0a2)\
  2021-06-26 11:16:40 +0300
  * [MDEV-26010](https://jira.mariadb.org/browse/MDEV-26010) fixup: Use acquire/release memory order
* Merge [Revision #a8350cfb5e](https://github.com/MariaDB/server/commit/a8350cfb5e) 2021-06-24 21:56:44 +0300 - Merge 10.5 into 10.6
* [Revision #5f22511e35](https://github.com/MariaDB/server/commit/5f22511e35)\
  2021-06-24 21:55:10 +0300
  * [MDEV-26010](https://jira.mariadb.org/browse/MDEV-26010): Assertion lsn > 2 failed in buf\_pool\_t::get\_oldest\_modification
* [Revision #e329dc8d86](https://github.com/MariaDB/server/commit/e329dc8d86)\
  2021-06-24 18:51:05 +0300
  * [MDEV-25948](https://jira.mariadb.org/browse/MDEV-25948) fixup: Demote a warning to a note
* [Revision #82fe83a34c](https://github.com/MariaDB/server/commit/82fe83a34c)\
  2021-06-24 16:07:27 +0300
  * [MDEV-26012](https://jira.mariadb.org/browse/MDEV-26012) InnoDB purge and shutdown hangs after failed ALTER TABLE
* [Revision #033e29b6a1](https://github.com/MariaDB/server/commit/033e29b6a1)\
  2021-06-24 15:00:34 +0300
  * [MDEV-26007](https://jira.mariadb.org/browse/MDEV-26007) Rollback unnecessarily initiates redo log write
* Merge [Revision #b4c9cd201b](https://github.com/MariaDB/server/commit/b4c9cd201b) 2021-06-24 12:39:34 +0300 - Merge 10.5 into 10.6
* [Revision #60ed479711](https://github.com/MariaDB/server/commit/60ed479711)\
  2021-06-24 11:01:18 +0300
  * [MDEV-26004](https://jira.mariadb.org/browse/MDEV-26004) Excessive wait times in buf\_LRU\_get\_free\_block()
* Merge [Revision #101da87228](https://github.com/MariaDB/server/commit/101da87228) 2021-06-23 19:36:45 +0300 - Merge 10.5 into 10.6
* [Revision #6441bc614a](https://github.com/MariaDB/server/commit/6441bc614a)\
  2021-06-23 13:13:16 +0300
  * [MDEV-25113](https://jira.mariadb.org/browse/MDEV-25113): Introduce a page cleaner mode before 'furious flush'
* [Revision #22b62edaed](https://github.com/MariaDB/server/commit/22b62edaed)\
  2021-06-23 13:13:11 +0300
  * [MDEV-25113](https://jira.mariadb.org/browse/MDEV-25113): Make page flushing faster
* [Revision #8af538979b](https://github.com/MariaDB/server/commit/8af538979b)\
  2021-06-23 12:14:26 +0300
  * [MDEV-25801](https://jira.mariadb.org/browse/MDEV-25801): buf\_flush\_dirty\_pages() is very slow
* [Revision #762bcb81b5](https://github.com/MariaDB/server/commit/762bcb81b5)\
  2021-06-23 12:01:41 +0300
  * [MDEV-25948](https://jira.mariadb.org/browse/MDEV-25948) Remove log\_flush\_task
* [Revision #6dfd44c828](https://github.com/MariaDB/server/commit/6dfd44c828)\
  2021-06-23 19:06:49 +0300
  * [MDEV-25954](https://jira.mariadb.org/browse/MDEV-25954): Trim os\_aio\_wait\_until\_no\_pending\_writes()
* [Revision #6e12ebd4a7](https://github.com/MariaDB/server/commit/6e12ebd4a7)\
  2021-06-23 13:42:11 +0300
  * [MDEV-25062](https://jira.mariadb.org/browse/MDEV-25062): Reduce trx\_rseg\_t::mutex contention
* [Revision #b3e8788009](https://github.com/MariaDB/server/commit/b3e8788009)\
  2021-06-23 13:37:11 +0300
  * [MDEV-25967](https://jira.mariadb.org/browse/MDEV-25967): Correctly extend deferred-recovery files
* [Revision #592a925c0c](https://github.com/MariaDB/server/commit/592a925c0c)\
  2021-06-23 13:36:04 +0300
  * [MDEV-25996](https://jira.mariadb.org/browse/MDEV-25996) sux\_lock::s\_lock(): Assertion !have\_s() failed on startup
* Merge [Revision #3a566de22d](https://github.com/MariaDB/server/commit/3a566de22d) 2021-06-23 09:24:32 +0300 - Merge 10.5 into 10.6
* Merge [Revision #344e59904d](https://github.com/MariaDB/server/commit/344e59904d) 2021-06-23 08:17:49 +0300 - Merge 10.4 into 10.5
* Merge [Revision #09b03ff31b](https://github.com/MariaDB/server/commit/09b03ff31b) 2021-06-23 08:05:27 +0300 - Merge 10.3 into 10.4
* [Revision #1deb630484](https://github.com/MariaDB/server/commit/1deb630484)\
  2021-06-22 22:21:24 -0400
  * bump the VERSION
* [Revision #35a9aaebe2](https://github.com/MariaDB/server/commit/35a9aaebe2)\
  2021-06-22 09:30:25 +0300
  * [MDEV-25981](https://jira.mariadb.org/browse/MDEV-25981) InnoDB upgrade fails
* Merge [Revision #e07f0a2d80](https://github.com/MariaDB/server/commit/e07f0a2d80) 2021-06-22 09:15:38 +0300 - Merge 10.2 into 10.3
* [Revision #19716ad5a8](https://github.com/MariaDB/server/commit/19716ad5a8)\
  2021-06-22 09:11:41 +0300
  * [MDEV-25982](https://jira.mariadb.org/browse/MDEV-25982) Upgrade of [MariaDB 10.1](../../mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/changes-improvements-in-mariadb-10-1.md) log crashes due to missing encryption key
* [Revision #cc0bd8431f](https://github.com/MariaDB/server/commit/cc0bd8431f)\
  2021-06-21 16:15:07 -0700
  * [MDEV-25679](https://jira.mariadb.org/browse/MDEV-25679) Wrong result selecting from simple view with LIMIT and ORDER BY
* [Revision #6e94ef4185](https://github.com/MariaDB/server/commit/6e94ef4185)\
  2021-06-21 22:25:37 -0700
  * [MDEV-25679](https://jira.mariadb.org/browse/MDEV-25679) Wrong result selecting from simple view with LIMIT and ORDER BY
* [Revision #bf2680ea09](https://github.com/MariaDB/server/commit/bf2680ea09)\
  2021-06-22 22:42:42 -0400
  * bump the VERSION
* [Revision #7f24e37fbe](https://github.com/MariaDB/server/commit/7f24e37fbe)\
  2021-06-22 12:23:13 -0700
  * [MDEV-25679](https://jira.mariadb.org/browse/MDEV-25679) Wrong result selecting from simple view with LIMIT and ORDER BY
* [Revision #55b3a3f4dd](https://github.com/MariaDB/server/commit/55b3a3f4dd)\
  2021-06-22 23:00:01 -0400
  * bump the VERSION
* [Revision #9fc67c6bf3](https://github.com/MariaDB/server/commit/9fc67c6bf3)\
  2021-06-22 17:52:54 +0300
  * [MDEV-25950](https://jira.mariadb.org/browse/MDEV-25950) Ignoring strange row from mysql.innodb\_index\_stats after DDL
* [Revision #e1c953ef23](https://github.com/MariaDB/server/commit/e1c953ef23)\
  2021-06-22 15:25:58 +0300
  * [MDEV-25989](https://jira.mariadb.org/browse/MDEV-25989) Crash (or hang) on startup after restoring backup
* Merge [Revision #367c75c099](https://github.com/MariaDB/server/commit/367c75c099) 2021-06-21 19:56:14 +0300 - Merge 10.5 into 10.6
* Merge [Revision #a1907fed60](https://github.com/MariaDB/server/commit/a1907fed60) 2021-06-21 18:49:36 +0300 - Merge 10.4 into 10.5
* Merge [Revision #ce868cd89e](https://github.com/MariaDB/server/commit/ce868cd89e) 2021-06-21 18:44:14 +0300 - Merge 10.3 into 10.4
* [Revision #9dc50ea229](https://github.com/MariaDB/server/commit/9dc50ea229)\
  2021-06-21 18:13:28 +0300
  * [MDEV-25979](https://jira.mariadb.org/browse/MDEV-25979) Invalid page number written to DB\_ROLL\_PTR
* [Revision #09249eb9bd](https://github.com/MariaDB/server/commit/09249eb9bd)\
  2021-06-21 17:51:03 +0300
  * [MDEV-14180](https://jira.mariadb.org/browse/MDEV-14180) fixup: Avoid unnecessary dirtying of pages
* Merge [Revision #4dfec8b230](https://github.com/MariaDB/server/commit/4dfec8b230) 2021-06-21 17:49:33 +0300 - Merge 10.5 into 10.6
* Merge [Revision #a42c80bd48](https://github.com/MariaDB/server/commit/a42c80bd48) 2021-06-21 14:22:22 +0300 - Merge 10.4 into 10.5
* [Revision #baf0ef9a18](https://github.com/MariaDB/server/commit/baf0ef9a18)\
  2021-06-21 14:05:43 +0300
  * After-merge fix: Remove duplicated code
* Merge [Revision #d3e4fae797](https://github.com/MariaDB/server/commit/d3e4fae797) 2021-06-21 12:38:25 +0300 - Merge 10.3 into 10.4
* [Revision #e46f76c974](https://github.com/MariaDB/server/commit/e46f76c974)\
  2021-06-21 12:34:07 +0300
  * [MDEV-15912](https://jira.mariadb.org/browse/MDEV-15912): Remove traces of insert\_undo
* [Revision #241d30d3fa](https://github.com/MariaDB/server/commit/241d30d3fa)\
  2021-06-21 12:09:00 +0300
  * After-merge fixes for [MDEV-14180](https://jira.mariadb.org/browse/MDEV-14180)
* Merge [Revision #c9a85fb1b1](https://github.com/MariaDB/server/commit/c9a85fb1b1) 2021-06-21 09:07:40 +0300 - Merge 10.2 into 10.3
* [Revision #773a07b655](https://github.com/MariaDB/server/commit/773a07b655)\
  2021-06-21 08:18:34 +0300
  * Remove Travis CI status
* [Revision #cd1a195b22](https://github.com/MariaDB/server/commit/cd1a195b22)\
  2021-06-17 16:10:11 +0530
  * [MDEV-25947](https://jira.mariadb.org/browse/MDEV-25947) innodb\_fts.misc\_debug fails in buildbot
* [Revision #35b57c37bb](https://github.com/MariaDB/server/commit/35b57c37bb)\
  2021-05-13 17:54:15 +0200
  * [MDEV-25617](https://jira.mariadb.org/browse/MDEV-25617) 10.5.10 upgrade: "scriptlet / line 6 : \[: is-active : binary operator expected"
* [Revision #c307dc6efd](https://github.com/MariaDB/server/commit/c307dc6efd)\
  2021-06-16 07:50:04 +0300
  * Remove a unused variable
* [Revision #2edb8e12e1](https://github.com/MariaDB/server/commit/2edb8e12e1)\
  2021-06-15 06:24:38 +0200
  * [MDEV-25880](https://jira.mariadb.org/browse/MDEV-25880) part 2: Improving reliability of the SST scripts
* [Revision #18d5be5b54](https://github.com/MariaDB/server/commit/18d5be5b54)\
  2021-06-09 03:41:37 +0200
  * [MDEV-25880](https://jira.mariadb.org/browse/MDEV-25880): rsync may be mistakenly killed when overlapping SST
* [Revision #1c35a3f6fd](https://github.com/MariaDB/server/commit/1c35a3f6fd)\
  2021-06-15 13:09:15 +0300
  * fix clang build
* [Revision #7d591cf850](https://github.com/MariaDB/server/commit/7d591cf850)\
  2021-06-15 13:14:39 +0530
  * [MDEV-24713](https://jira.mariadb.org/browse/MDEV-24713) Assertion \`dict\_table\_is\_comp(index->table)' failed in row\_merge\_buf\_add()
* [Revision #7229107e3e](https://github.com/MariaDB/server/commit/7229107e3e)\
  2021-06-15 13:13:01 +0530
  * [MDEV-25872](https://jira.mariadb.org/browse/MDEV-25872) InnoDB: Assertion failure in row\_merge\_read\_clustered\_index upon ALTER on table with indexed virtual columns
* [Revision #8c7d8b716c](https://github.com/MariaDB/server/commit/8c7d8b716c)\
  2021-06-15 13:12:15 +0530
  * [MDEV-14180](https://jira.mariadb.org/browse/MDEV-14180) Automatically disable key rotation checks for file\_key\_managment plugin
* [Revision #7d2c338c48](https://github.com/MariaDB/server/commit/7d2c338c48)\
  2021-06-14 19:37:06 +0530
  * [MDEV-14180](https://jira.mariadb.org/browse/MDEV-14180) preparation: Rename key\_rotation\_list
* [Revision #be243ed9e3](https://github.com/MariaDB/server/commit/be243ed9e3)\
  2021-06-15 12:40:33 +1000
  * cmake OpenBSD copyright notice correction
* [Revision #ec4df51414](https://github.com/MariaDB/server/commit/ec4df51414)\
  2021-06-15 12:34:23 +1000
  * eventscheduler mismatch of my\_{malloc,free}, delete
* [Revision #2e33f574b3](https://github.com/MariaDB/server/commit/2e33f574b3)\
  2021-06-14 23:45:31 +0200
  * update libmariadb
* [Revision #c9f9e38bb5](https://github.com/MariaDB/server/commit/c9f9e38bb5)\
  2021-06-12 12:38:45 +0200
  * fix mysqlest crash on ./mtr --sp innodb\_fts.innodb-fts-stopword
* [Revision #887f46a618](https://github.com/MariaDB/server/commit/887f46a618)\
  2021-06-12 12:23:07 +0200
  * fix mysqltest crash report output
* [Revision #4352c77c5a](https://github.com/MariaDB/server/commit/4352c77c5a)\
  2021-06-10 20:01:44 -0400
  * Link with libexecinfo on OpenBSD for stacktrace functionality.
* [Revision #152c83d49c](https://github.com/MariaDB/server/commit/152c83d49c)\
  2021-05-30 15:42:04 -0700
  * [MDEV-20392](https://jira.mariadb.org/browse/MDEV-20392): Skip ABI check if 'diff' is not found
* [Revision #396864c6b3](https://github.com/MariaDB/server/commit/396864c6b3)\
  2021-06-10 11:17:40 +0300
  * Remove orphan type name trx\_sig\_t
* [Revision #7a1eff0a9d](https://github.com/MariaDB/server/commit/7a1eff0a9d)\
  2021-06-09 15:28:35 +0300
  * [MDEV-25884](https://jira.mariadb.org/browse/MDEV-25884) Tests use environment $USER variable without quotes
* [Revision #c872125a66](https://github.com/MariaDB/server/commit/c872125a66)\
  2021-05-22 15:53:33 +0300
  * [MDEV-25630](https://jira.mariadb.org/browse/MDEV-25630): Crash with window function in left expr of IN subquery
* [Revision #068246c006](https://github.com/MariaDB/server/commit/068246c006)\
  2021-06-19 00:45:49 +0200
  * fix spider tests for --ps
* [Revision #a5f6eca50d](https://github.com/MariaDB/server/commit/a5f6eca50d)\
  2021-06-19 00:22:15 +0200
  * spider tests aren't big
* [Revision #690ae1de45](https://github.com/MariaDB/server/commit/690ae1de45)\
  2021-06-19 13:45:39 +0200
  * fix spider tests for --ps in 10.4
* [Revision #a4f485917e](https://github.com/MariaDB/server/commit/a4f485917e)\
  2021-06-19 13:45:14 +0200
  * spider tests aren't big in 10.4
* [Revision #8a2b4d531d](https://github.com/MariaDB/server/commit/8a2b4d531d)\
  2021-06-11 14:30:42 +1000
  * [MDEV-20162](https://jira.mariadb.org/browse/MDEV-20162): fix connect-abstract test case
* [Revision #e85df7feac](https://github.com/MariaDB/server/commit/e85df7feac)\
  2019-06-15 16:04:49 +0200
  * [MDEV-19702](https://jira.mariadb.org/browse/MDEV-19702) Refactor Bitmap to be based on ulonglong, not on uint32
* [Revision #0b9a59bbc4](https://github.com/MariaDB/server/commit/0b9a59bbc4)\
  2021-06-09 15:50:01 +0300
  * [MDEV-25884](https://jira.mariadb.org/browse/MDEV-25884) Tests use environment $USER variable without quotes
* [Revision #f13b80af39](https://github.com/MariaDB/server/commit/f13b80af39)\
  2021-06-09 13:17:58 +0200
  * [MDEV-23933](https://jira.mariadb.org/browse/MDEV-23933) main.failed\_auth\_unixsocket fails on arm
* [Revision #bafec28e43](https://github.com/MariaDB/server/commit/bafec28e43)\
  2021-05-06 19:47:11 +0200
  * rpm packaging: account for fedora > 31
* [Revision #7e9bc7bf4e](https://github.com/MariaDB/server/commit/7e9bc7bf4e)\
  2021-05-03 23:31:33 +0200
  * mdl\_dbug\_print\_locks(): make it useful in gdb too
* [Revision #b81803f065](https://github.com/MariaDB/server/commit/b81803f065)\
  2021-06-09 13:27:00 +0200
  * [MDEV-22221](https://jira.mariadb.org/browse/MDEV-22221): MariaDB with WolfSSL doesn't support AES-GCM cipher for SSL
* [Revision #dbe3161b6d](https://github.com/MariaDB/server/commit/dbe3161b6d)\
  2021-06-09 12:34:23 +0200
  * Remove WolfSSL workaround for old version. We're already on 4.4.6
* [Revision #bcedb4200f](https://github.com/MariaDB/server/commit/bcedb4200f)\
  2020-10-13 14:36:25 +0200
  * [MDEV-25878](https://jira.mariadb.org/browse/MDEV-25878): mytop bugs: check for mysql driver and sockets
* [Revision #59e3ac2e67](https://github.com/MariaDB/server/commit/59e3ac2e67)\
  2020-05-18 15:18:56 +0200
  * [MDEV-25878](https://jira.mariadb.org/browse/MDEV-25878): mytop bugs: check for mysql driver and sockets
* [Revision #c3a1ba0fd9](https://github.com/MariaDB/server/commit/c3a1ba0fd9)\
  2021-06-19 14:05:54 +0200
  * fix spider tests for --ps in 10.5
* [Revision #bad1440325](https://github.com/MariaDB/server/commit/bad1440325)\
  2021-06-18 13:16:51 +0300
  * Speed up of innodb\_gis.update\_root test 10x by adding BEGIN/COMMIT
* [Revision #93f5d40656](https://github.com/MariaDB/server/commit/93f5d40656)\
  2021-06-17 20:15:24 +0300
  * Fixed debug\_sync timeout in deadlock\_drop\_table
* [Revision #15e1fbc37d](https://github.com/MariaDB/server/commit/15e1fbc37d)\
  2021-06-17 19:21:35 +0300
  * Fixed flush table issue in MyISAM with CREATE ... SELECT
* [Revision #87de0e2129](https://github.com/MariaDB/server/commit/87de0e2129)\
  2021-06-17 16:06:46 +0300
  * Minor cleanups of atomic ddl code
* [Revision #83a471344f](https://github.com/MariaDB/server/commit/83a471344f)\
  2021-06-18 21:36:10 +0200
  * fix big tests for -ps
* [Revision #8bb225d10a](https://github.com/MariaDB/server/commit/8bb225d10a)\
  2021-06-18 17:52:44 +0200
  * [MDEV-16708](https://jira.mariadb.org/browse/MDEV-16708): fixed test rpl\_innodb\_bug28430, failing with --ps
* [Revision #cccc7b5f9b](https://github.com/MariaDB/server/commit/cccc7b5f9b)\
  2021-06-18 11:51:14 -0400
  * bump the VERSION
* Merge [Revision #b630f0b1b9](https://github.com/MariaDB/server/commit/b630f0b1b9) 2021-06-18 09:16:20 +0300 - Merge 10.5 into 10.6
* [Revision #b7d87bf0a9](https://github.com/MariaDB/server/commit/b7d87bf0a9)\
  2021-05-30 15:42:04 -0700
  * [MDEV-20392](https://jira.mariadb.org/browse/MDEV-20392): Skip ABI check if 'diff' is not found
