# MariaDB 10.6.13 Changelog

The most recent release of [MariaDB 10.6](../../mariadb-community-server-release-notes/mariadb-10-6-series/what-is-mariadb-106.md) is:[**MariaDB 10.6.21**](../../mariadb-community-server-release-notes/mariadb-10-6-series/mariadb-10-6-21-release-notes.md) Stable (GA) [Download Now](https://mariadb.com/downloads/)[_Alternate download from mariadb.org_](https://downloads.mariadb.org/mariadb/10.6.21/)

[Download 10.6.13](https://downloads.mariadb.org/mariadb/10.6.13/)[Release Notes](../../mariadb-community-server-release-notes/mariadb-10-6-series/mariadb-10-6-13-release-notes.md)[Changelog](mariadb-10-6-13-changelog.md)[Overview of 10.6](../../mariadb-community-server-release-notes/mariadb-10-6-series/what-is-mariadb-106.md)

**Release date:** 10 May 2023

For the highlights of this release, see the[release notes](../../mariadb-community-server-release-notes/mariadb-10-6-series/mariadb-10-6-13-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/server/tree/10.6) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Includes all fixes from [MariaDB 10.5.20](../changelogs-mariadb-105-series/mariadb-10-5-20-changelog.md)
* [Revision #a24f2bb50b](https://github.com/MariaDB/server/commit/a24f2bb50b)\
  2023-05-05 13:55:42 +0300
  * [MDEV-31199](https://jira.mariadb.org/browse/MDEV-31199): Assertion \`field->table->stats\_is\_read' fails with hash\_join\_cardinality=on
* Merge [Revision #1c39479598](https://github.com/MariaDB/server/commit/1c39479598) 2023-05-05 11:09:46 +0200 - Merge branch '10.5' into 10.6
* Merge [Revision #db3342b325](https://github.com/MariaDB/server/commit/db3342b325) 2023-05-04 18:47:11 +0200 - Merge branch '10.5' into 10.6
* Merge [Revision #5dc0f3dafa](https://github.com/MariaDB/server/commit/5dc0f3dafa) 2023-05-04 11:26:45 +0200 - Merge branch '10.5' into 10.6
* Merge [Revision #652d54bf00](https://github.com/MariaDB/server/commit/652d54bf00) 2023-05-03 19:08:07 +0200 - Merge branch '10.5' into 10.6
* Merge [Revision #043d69bbcc](https://github.com/MariaDB/server/commit/043d69bbcc) 2023-05-03 09:51:25 +0200 - Merge branch '10.5' into 10.6
* [Revision #fe89df4268](https://github.com/MariaDB/server/commit/fe89df4268)\
  2023-05-02 00:31:57 -0700
  * [MDEV-31162](https://jira.mariadb.org/browse/MDEV-31162) Crash for query using ROWNUM over multi-table view with ORDER BY
* [Revision #5f3a4beb9d](https://github.com/MariaDB/server/commit/5f3a4beb9d)\
  2023-04-13 11:24:44 +0300
  * [MDEV-31045](https://jira.mariadb.org/browse/MDEV-31045): Update debian/rules to be in sync to MariaDB LTS 10.6
* [Revision #7e2e968997](https://github.com/MariaDB/server/commit/7e2e968997)\
  2023-04-30 11:53:21 -0700
  * [MDEV-31143](https://jira.mariadb.org/browse/MDEV-31143) Crash for query using ROWNUM() over view with ORDER BY
* [Revision #4329ec5d3b](https://github.com/MariaDB/server/commit/4329ec5d3b)\
  2023-03-09 17:04:07 +0300
  * [MDEV-30812](https://jira.mariadb.org/browse/MDEV-30812): Improve output cardinality estimates for hash join
* [Revision #2eb7bf1ec3](https://github.com/MariaDB/server/commit/2eb7bf1ec3)\
  2023-04-21 10:55:14 +0200
  * [MDEV-31073](https://jira.mariadb.org/browse/MDEV-31073) Server crash, assertion \`table != 0 && view->field\_translation != 0' failure with ROWNUM and view
* [Revision #06b443be34](https://github.com/MariaDB/server/commit/06b443be34)\
  2023-04-26 15:26:38 +0200
  * Nes CC 3.3
* [Revision #4a668c1892](https://github.com/MariaDB/server/commit/4a668c1892)\
  2023-04-27 17:11:32 +0300
  * [MDEV-29401](https://jira.mariadb.org/browse/MDEV-29401) InnoDB history list length increased in 10.6 compared to 10.5
* [Revision #f272463b02](https://github.com/MariaDB/server/commit/f272463b02)\
  2023-04-25 21:16:43 +0300
  * Cleanup of [MDEV-14974](https://jira.mariadb.org/browse/MDEV-14974): --port ignored for --host=localhost
* Merge [Revision #bb1d1dc846](https://github.com/MariaDB/server/commit/bb1d1dc846) 2023-04-27 09:48:27 +0300 - Merge 10.5 into 10.6
* [Revision #c5e50c48bb](https://github.com/MariaDB/server/commit/c5e50c48bb)\
  2023-03-24 11:42:15 +0200
  * [MDEV-30837](https://jira.mariadb.org/browse/MDEV-30837): Remove usage of AWK in autobake-debs.sh
* [Revision #f99a891858](https://github.com/MariaDB/server/commit/f99a891858)\
  2023-03-13 11:56:53 +0200
  * [MDEV-30837](https://jira.mariadb.org/browse/MDEV-30837): Remove usage of AWK from Debian init and postinst scripts
* [Revision #5740638c4c](https://github.com/MariaDB/server/commit/5740638c4c)\
  2023-04-26 12:08:59 +0300
  * [MDEV-31132](https://jira.mariadb.org/browse/MDEV-31132) Deadlock between DDL and purge of InnoDB history
* [Revision #d4265fbde5](https://github.com/MariaDB/server/commit/d4265fbde5)\
  2023-04-26 11:53:42 +0300
  * [MDEV-26055](https://jira.mariadb.org/browse/MDEV-26055): Correct the formula for adaptive flushing
* [Revision #898320b5f8](https://github.com/MariaDB/server/commit/898320b5f8)\
  2023-04-25 18:55:53 +0200
  * [MDEV-30804](https://jira.mariadb.org/browse/MDEV-30804) addendum for 10.6+ branches
* [Revision #c22ab93f8a](https://github.com/MariaDB/server/commit/c22ab93f8a)\
  2023-04-25 15:03:38 +0300
  * [MDEV-26827](https://jira.mariadb.org/browse/MDEV-26827) fixup: Prevent a hang in LRU eviction
* Merge [Revision #818d5e4814](https://github.com/MariaDB/server/commit/818d5e4814) 2023-04-25 13:10:33 +0300 - Merge 10.5 into 10.6
* [Revision #0976afec88](https://github.com/MariaDB/server/commit/0976afec88)\
  2023-04-24 09:57:58 +0300
  * [MDEV-31114](https://jira.mariadb.org/browse/MDEV-31114) Assertion !...is\_waiting() failed in os\_aio\_wait\_until\_no\_pending\_writes()
* [Revision #2c567b2fa3](https://github.com/MariaDB/server/commit/2c567b2fa3)\
  2023-04-22 16:42:52 +0530
  * [MDEV-30996](https://jira.mariadb.org/browse/MDEV-30996) insert.. select in presence of full text index freezes all other commits at commit time
* [Revision #51e62cb3b3](https://github.com/MariaDB/server/commit/51e62cb3b3)\
  2023-04-21 17:58:26 +0300
  * [MDEV-26782](https://jira.mariadb.org/browse/MDEV-26782) InnoDB temporary tablespace: reclaiming of free space does not work
* [Revision #204e7225dc](https://github.com/MariaDB/server/commit/204e7225dc)\
  2023-04-21 17:58:18 +0300
  * Cleanup: MONITOR\_EXISTING trx\_undo\_slots\_used, trx\_undo\_slots\_cached
* [Revision #86767bcc0f](https://github.com/MariaDB/server/commit/86767bcc0f)\
  2023-04-21 17:58:09 +0300
  * [MDEV-29593](https://jira.mariadb.org/browse/MDEV-29593) Purge misses a chance to free not-yet-reused undo pages
* [Revision #40eff3f868](https://github.com/MariaDB/server/commit/40eff3f868)\
  2023-04-21 17:52:47 +0300
  * [MDEV-26827](https://jira.mariadb.org/browse/MDEV-26827) fixup: hangs and !os\_aio\_pending\_writes() assertion failures
* [Revision #e55e761eae](https://github.com/MariaDB/server/commit/e55e761eae)\
  2023-04-21 16:49:59 +0300
  * [MDEV-31084](https://jira.mariadb.org/browse/MDEV-31084) assert(waiting) failed in TP\_connection\_generic::wait\_end
* Merge [Revision #abe4c7bfd6](https://github.com/MariaDB/server/commit/abe4c7bfd6) 2023-04-21 16:38:22 +0300 - Merge 10.5 into 10.6
* [Revision #7e31a8e7fa](https://github.com/MariaDB/server/commit/7e31a8e7fa)\
  2023-04-20 14:08:48 +0300
  * [MDEV-26827](https://jira.mariadb.org/browse/MDEV-26827) fixup: Fix os\_aio\_wait\_until\_no\_pending\_writes()
* [Revision #c21bc17a51](https://github.com/MariaDB/server/commit/c21bc17a51)\
  2023-04-20 10:13:12 +1000
  * [MDEV-30186](https://jira.mariadb.org/browse/MDEV-30186): mtr: Use of uninitialized value $test\_name in substitution
* [Revision #f7791cc7cb](https://github.com/MariaDB/server/commit/f7791cc7cb)\
  2023-04-20 10:10:23 +1000
  * Revert "[MDEV-30186](https://jira.mariadb.org/browse/MDEV-30186) Use of uninitialized value in substitution"
* [Revision #27ff972be2](https://github.com/MariaDB/server/commit/27ff972be2)\
  2023-04-19 18:57:18 +0300
  * [MDEV-26827](https://jira.mariadb.org/browse/MDEV-26827) fixup: Do not hog buf\_pool.mutex
* [Revision #0cda0e4e15](https://github.com/MariaDB/server/commit/0cda0e4e15)\
  2023-04-19 18:56:58 +0300
  * [MDEV-31080](https://jira.mariadb.org/browse/MDEV-31080) fil\_validate() failures during deferred tablespace recovery
* [Revision #78368e5866](https://github.com/MariaDB/server/commit/78368e5866)\
  2023-04-19 15:52:11 +0300
  * [MDEV-30863](https://jira.mariadb.org/browse/MDEV-30863) fixup: Assertion failure when using innodb\_undo\_tablespaces=0
* [Revision #1892f5d8fc](https://github.com/MariaDB/server/commit/1892f5d8fc)\
  2023-04-19 14:46:49 +0300
  * [MDEV-30863](https://jira.mariadb.org/browse/MDEV-30863) fixup: Hang in a debug build
* [Revision #485a1b1f11](https://github.com/MariaDB/server/commit/485a1b1f11)\
  2023-04-18 14:54:40 +0300
  * [MDEV-30863](https://jira.mariadb.org/browse/MDEV-30863) Server freeze, all threads in trx\_assign\_rseg\_low()
* Merge [Revision #c28d1a6fea](https://github.com/MariaDB/server/commit/c28d1a6fea) 2023-04-18 14:54:18 +0300 - Merge 10.5 into 10.6
* [Revision #1995c626a5](https://github.com/MariaDB/server/commit/1995c626a5)\
  2023-04-14 12:38:16 -0700
  * \[[MDEV-30854](https://jira.mariadb.org/browse/MDEV-30854)] Do not use " as string delimiter in mariadb-tzinfo-to-sql
* [Revision #8f87023d3f](https://github.com/MariaDB/server/commit/8f87023d3f)\
  2023-04-14 13:13:03 +0300
  * [MDEV-28777](https://jira.mariadb.org/browse/MDEV-28777) binlog.binlog\_truncate\_multi\_engine failed in bb with Lost connection
* [Revision #3b85e3dcc1](https://github.com/MariaDB/server/commit/3b85e3dcc1)\
  2023-04-15 07:52:17 +0800
  * [MDEV-30687](https://jira.mariadb.org/browse/MDEV-30687): Make small facelifting to autobake-debs.sh (fix)
* [Revision #71f16c836f](https://github.com/MariaDB/server/commit/71f16c836f)\
  2023-04-13 17:56:38 +0300
  * [MDEV-31049](https://jira.mariadb.org/browse/MDEV-31049) fil\_delete\_tablespace() returns wrong file handle if tablespace was closed by parallel thread
* [Revision #0cca8166f3](https://github.com/MariaDB/server/commit/0cca8166f3)\
  2023-04-07 00:16:16 +0300
  * [MDEV-30775](https://jira.mariadb.org/browse/MDEV-30775) Performance regression in fil\_space\_t::try\_to\_close() introduced in [MDEV-23855](https://jira.mariadb.org/browse/MDEV-23855)
* [Revision #f2fde3f667](https://github.com/MariaDB/server/commit/f2fde3f667)\
  2023-02-20 10:10:09 +0200
  * [MDEV-30687](https://jira.mariadb.org/browse/MDEV-30687): Make small facelifting to autobake-debs.sh
* [Revision #1e4eef5c17](https://github.com/MariaDB/server/commit/1e4eef5c17)\
  2023-04-13 10:42:34 +0300
  * [MDEV-31045](https://jira.mariadb.org/browse/MDEV-31045): Fix regression building on Ubuntu 18.04
* [Revision #f50abab195](https://github.com/MariaDB/server/commit/f50abab195)\
  2023-04-13 15:18:26 +0300
  * [MDEV-31048](https://jira.mariadb.org/browse/MDEV-31048) PERFORMANCE\_SCHEMA lakcs InnoDB read\_slots and write\_slots
* [Revision #c0eeb72526](https://github.com/MariaDB/server/commit/c0eeb72526)\
  2023-04-13 12:25:41 +0300
  * [MDEV-28974](https://jira.mariadb.org/browse/MDEV-28974) fixup: Fix error and warning messages
* [Revision #2ddfb83807](https://github.com/MariaDB/server/commit/2ddfb83807)\
  2023-04-05 16:55:07 +0530
  * [MDEV-29273](https://jira.mariadb.org/browse/MDEV-29273) Race condition between drop table and closing of table
* [Revision #a091d6ac4e](https://github.com/MariaDB/server/commit/a091d6ac4e)\
  2023-04-12 13:49:57 +0300
  * [MDEV-26827](https://jira.mariadb.org/browse/MDEV-26827) fixup: Do not duplicate io\_slots::pending\_io\_count()
* Merge [Revision #5bada1246d](https://github.com/MariaDB/server/commit/5bada1246d) 2023-04-11 16:15:19 +0300 - Merge 10.5 into 10.6
* [Revision #375991a531](https://github.com/MariaDB/server/commit/375991a531)\
  2023-04-11 14:42:08 +0300
  * [MDEV-26827](https://jira.mariadb.org/browse/MDEV-26827) fixup for DDL race condition
* [Revision #31536b2477](https://github.com/MariaDB/server/commit/31536b2477)\
  2023-03-31 16:16:53 +0300
  * [MDEV-30972](https://jira.mariadb.org/browse/MDEV-30972): ANALYZE FORMAT=JSON: some time is unaccounted-for in BNL-H join
* [Revision #0269d82d53](https://github.com/MariaDB/server/commit/0269d82d53)\
  2023-03-10 18:02:14 +0300
  * ANALYZE FORMAT=JSON: Backport block-nl-join.r\_unpack\_time\_ms from 11.0 +fix [MDEV-30830](https://jira.mariadb.org/browse/MDEV-30830).
* [Revision #18342cd5e1](https://github.com/MariaDB/server/commit/18342cd5e1)\
  2023-03-25 14:06:20 -0700
  * Deb: Add missing installation step to Salsa-CI job for 10.5 upgrades
* [Revision #ee68fe3272](https://github.com/MariaDB/server/commit/ee68fe3272)\
  2023-03-18 20:12:13 -0700
  * Deb: Update Salsa-CI to use Bullseye instead of Sid
* [Revision #2a5763224e](https://github.com/MariaDB/server/commit/2a5763224e)\
  2023-01-05 21:56:14 -0800
  * Deb: Sync Salsa-CI from Debian [MariaDB 10.6](../../mariadb-community-server-release-notes/mariadb-10-6-series/what-is-mariadb-106.md)
* [Revision #dc1d6213f9](https://github.com/MariaDB/server/commit/dc1d6213f9)\
  2023-03-07 19:49:57 +0300
  * [MDEV-30806](https://jira.mariadb.org/browse/MDEV-30806): ANALYZE FORMAT=JSON: better support for BNL and BNL-H joins
* [Revision #169def14f6](https://github.com/MariaDB/server/commit/169def14f6)\
  2023-03-30 13:32:44 +0200
  * [MDEV-30413](https://jira.mariadb.org/browse/MDEV-30413) : run sequence nextval got \[Note] WSREP: MDL BF-BF conflict and \[ERROR] Aborting
* Merge [Revision #0760ad3336](https://github.com/MariaDB/server/commit/0760ad3336) 2023-03-28 15:25:52 +0300 - Merge 10.5 into 10.6
* [Revision #216d99bb39](https://github.com/MariaDB/server/commit/216d99bb39)\
  2023-03-24 11:25:14 +0200
  * [MDEV-26071](https://jira.mariadb.org/browse/MDEV-26071): rpl.rpl\_perfschema\_applier\_status\_by\_worker failed in bb …
* [Revision #e06c6046d2](https://github.com/MariaDB/server/commit/e06c6046d2)\
  2023-03-24 15:20:21 +0530
  * [MDEV-29545](https://jira.mariadb.org/browse/MDEV-29545) InnoDB: Can't find record during replace stmt
* [Revision #07460c31e3](https://github.com/MariaDB/server/commit/07460c31e3)\
  2023-03-24 07:59:27 +0200
  * [MDEV-30900](https://jira.mariadb.org/browse/MDEV-30900) Crash on macOS due to zero-initialized buf\_dblwr.write\_cond
* [Revision #15ca6c5a2f](https://github.com/MariaDB/server/commit/15ca6c5a2f)\
  2023-03-24 11:18:19 +1100
  * rpl\_reporting: sprintf -> snprintf
* Merge [Revision #1efdf67e60](https://github.com/MariaDB/server/commit/1efdf67e60) 2023-03-22 15:54:45 +0200 - Merge 10.5 into 10.6
* [Revision #535a38c455](https://github.com/MariaDB/server/commit/535a38c455)\
  2023-03-20 14:28:03 +0200
  * [MDEV-30400](https://jira.mariadb.org/browse/MDEV-30400) fixup: Fix the UNIV\_ZIP\_DEBUG build
* [Revision #32a53a66df](https://github.com/MariaDB/server/commit/32a53a66df)\
  2023-03-20 10:32:35 +0200
  * [MDEV-26827](https://jira.mariadb.org/browse/MDEV-26827) fixup: Remove a bogus assertion
* [Revision #e8e0559ed2](https://github.com/MariaDB/server/commit/e8e0559ed2)\
  2023-03-17 17:17:35 +0530
  * [MDEV-30870](https://jira.mariadb.org/browse/MDEV-30870) Undo tablespace name displays wrongly for I\_S queries
* [Revision #18e4978edc](https://github.com/MariaDB/server/commit/18e4978edc)\
  2023-03-17 16:41:27 +0530
  * [MDEV-29975](https://jira.mariadb.org/browse/MDEV-29975) InnoDB fails to release savepoint during bulk insert
* [Revision #a55b951e60](https://github.com/MariaDB/server/commit/a55b951e60)\
  2023-03-16 17:19:58 +0200
  * [MDEV-26827](https://jira.mariadb.org/browse/MDEV-26827) Make page flushing even faster
* [Revision #9593cccf28](https://github.com/MariaDB/server/commit/9593cccf28)\
  2023-03-16 17:09:08 +0200
  * [MDEV-26055](https://jira.mariadb.org/browse/MDEV-26055): Improve adaptive flushing
* [Revision #4105017a58](https://github.com/MariaDB/server/commit/4105017a58)\
  2023-03-16 16:00:45 +0200
  * [MDEV-30357](https://jira.mariadb.org/browse/MDEV-30357) Performance regression in locking reads from secondary indexes
* [Revision #f2096478d5](https://github.com/MariaDB/server/commit/f2096478d5)\
  2023-03-16 15:52:42 +0200
  * [MDEV-29835](https://jira.mariadb.org/browse/MDEV-29835) InnoDB hang on B-tree split or merge
* Merge [Revision #85cbfaefee](https://github.com/MariaDB/server/commit/85cbfaefee) 2023-03-16 15:48:08 +0200 - Merge 10.5 into 10.6
* Merge [Revision #f169dfb41a](https://github.com/MariaDB/server/commit/f169dfb41a) 2023-03-10 09:35:50 +0200 - Merge 10.5 into 10.6
* Merge [Revision #25c048066a](https://github.com/MariaDB/server/commit/25c048066a) 2023-03-06 13:36:06 +0200 - Merge 10.5 into 10.6
* [Revision #49e2b50d59](https://github.com/MariaDB/server/commit/49e2b50d59)\
  2023-02-21 16:25:17 +0530
  * [MDEV-30341](https://jira.mariadb.org/browse/MDEV-30341) Reset check\_foreigns, check\_unique\_secondary variables
* Merge [Revision #085d0ac238](https://github.com/MariaDB/server/commit/085d0ac238) 2023-02-28 16:05:21 +0200 - Merge 10.5 into 10.6
* Merge [Revision #3e2ad0e918](https://github.com/MariaDB/server/commit/3e2ad0e918) 2023-02-27 13:17:35 +0200 - Merge 10.5 into 10.6
* [Revision #db245e1140](https://github.com/MariaDB/server/commit/db245e1140)\
  2023-02-22 16:57:18 +0530
  * [MDEV-25984](https://jira.mariadb.org/browse/MDEV-25984) Assertion \`max\_doc\_id > 0' failed in fts\_init\_doc\_id()
* [Revision #df9f9ba12b](https://github.com/MariaDB/server/commit/df9f9ba12b)\
  2023-02-21 10:57:52 +0530
  * [MDEV-29871](https://jira.mariadb.org/browse/MDEV-29871) innodb\_fts.fulltext\_misc unexpectedly reports a result
* [Revision #a474e3278c](https://github.com/MariaDB/server/commit/a474e3278c)\
  2023-02-09 13:51:57 +0300
  * [MDEV-27701](https://jira.mariadb.org/browse/MDEV-27701) Race on trx->lock.wait\_lock between lock\_rec\_move() and lock\_sys\_t::cancel()
* Merge [Revision #67a6ad0a4a](https://github.com/MariaDB/server/commit/67a6ad0a4a) 2023-02-16 10:17:58 +0200 - Merge 10.5 into 10.6
* [Revision #201cfc33e6](https://github.com/MariaDB/server/commit/201cfc33e6)\
  2023-02-16 08:30:20 +0200
  * [MDEV-30638](https://jira.mariadb.org/browse/MDEV-30638) Deadlock between INSERT and InnoDB non-persistent statistics update
* [Revision #54c0ac72e3](https://github.com/MariaDB/server/commit/54c0ac72e3)\
  2023-02-16 08:29:44 +0200
  * [MDEV-30134](https://jira.mariadb.org/browse/MDEV-30134) Assertion failed in buf\_page\_t::unfix() in buf\_pool\_t::watch\_unset()
* [Revision #9c15799462](https://github.com/MariaDB/server/commit/9c15799462)\
  2023-02-16 08:28:14 +0200
  * [MDEV-30397](https://jira.mariadb.org/browse/MDEV-30397): MariaDB crash due to DB\_FAIL reported for a corrupted page
* Merge [Revision #cc27e5fd0e](https://github.com/MariaDB/server/commit/cc27e5fd0e) 2023-02-16 08:17:54 +0200 - Merge 10.5 into 10.6
* [Revision #4afa3b64c4](https://github.com/MariaDB/server/commit/4afa3b64c4)\
  2023-02-15 16:20:25 +0200
  * [MDEV-30324](https://jira.mariadb.org/browse/MDEV-30324): Wrong result upon SELECT DISTINCT ... WITH TIES
* [Revision #d2b773d913](https://github.com/MariaDB/server/commit/d2b773d913)\
  2023-02-04 12:11:15 +0200
  * Whitespace fix
* [Revision #e83ae66e4a](https://github.com/MariaDB/server/commit/e83ae66e4a)\
  2023-02-04 12:10:31 +0200
  * Update comments to match new debug\_sync implementation
* Merge [Revision #96a3b11d13](https://github.com/MariaDB/server/commit/96a3b11d13) 2023-02-14 15:23:23 +0200 - Merge 10.5 into 10.6
* Merge [Revision #6aec87544c](https://github.com/MariaDB/server/commit/6aec87544c) 2023-02-10 13:03:01 +0200 - Merge 10.5 into 10.6
* Merge [Revision #70a515df43](https://github.com/MariaDB/server/commit/70a515df43) 2023-02-06 20:18:44 +0100 - Merge branch '10.6.12' into 10.6
* [Revision #80ae69c8bc](https://github.com/MariaDB/server/commit/80ae69c8bc)\
  2023-02-06 10:24:21 -0500
  * bump the VERSION
* [Revision #29b4bd4ea9](https://github.com/MariaDB/server/commit/29b4bd4ea9)\
  2023-02-06 19:16:15 +1100
  * [MDEV-30573](https://jira.mariadb.org/browse/MDEV-30573) Server doesn't build with GCOV by GCC 11+
* [Revision #9f16d15357](https://github.com/MariaDB/server/commit/9f16d15357)\
  2023-02-03 15:00:49 +0200
  * debug\_sync: Print all current active signals within the trace file during wait
* [Revision #2a08b2c15c](https://github.com/MariaDB/server/commit/2a08b2c15c)\
  2023-02-03 14:18:32 +0200
  * sql\_hset.h - include what you use uchar comes from my\_global.h
* [Revision #addcf08d0f](https://github.com/MariaDB/server/commit/addcf08d0f)\
  2023-02-03 14:13:30 +0200
  * Revert test changes from "Fixed debug\_sync timeout in deadlock\_drop\_table"
* [Revision #8ff0a7f893](https://github.com/MariaDB/server/commit/8ff0a7f893)\
  2021-09-29 14:10:56 +0300
  * Implement DEBUG\_SYNC multiple signal firing capability
* [Revision #c115559b66](https://github.com/MariaDB/server/commit/c115559b66)\
  2021-09-29 14:04:31 +0300
  * Extend Binary\_string::strstr to also take in a const char pointer
* [Revision #cd873c8688](https://github.com/MariaDB/server/commit/cd873c8688)\
  2021-09-29 11:24:05 +0300
  * debug\_sync: Implement NO\_CLEAR\_EVENT syntax
* [Revision #8885225de6](https://github.com/MariaDB/server/commit/8885225de6)\
  2021-09-28 22:17:59 +0300
  * Implement multiple-signal debug\_sync
* [Revision #cc08872c16](https://github.com/MariaDB/server/commit/cc08872c16)\
  2021-09-28 22:29:23 +0300
  * Initialize the Hash\_set during creation
* [Revision #b482e87f26](https://github.com/MariaDB/server/commit/b482e87f26)\
  2021-09-28 22:14:36 +0300
  * Silence gcc-11 warnings
* [Revision #0e737f7898](https://github.com/MariaDB/server/commit/0e737f7898)\
  2022-12-20 14:25:21 +0100
  * [MDEV-30186](https://jira.mariadb.org/browse/MDEV-30186) Use of uninitialized value in substitution
