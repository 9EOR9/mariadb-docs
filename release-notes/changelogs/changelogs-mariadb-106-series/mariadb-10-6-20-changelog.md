# MariaDB 10.6.20 Changelog

The most recent release of [MariaDB 10.6](../../mariadb-community-server-release-notes/mariadb-10-6-series/what-is-mariadb-106.md) is:[**MariaDB 10.6.21**](../../mariadb-community-server-release-notes/mariadb-10-6-series/mariadb-10-6-21-release-notes.md) Stable (GA) [Download Now](https://mariadb.com/downloads/)[_Alternate download from mariadb.org_](https://downloads.mariadb.org/mariadb/10.6.21/)

[Download 10.6.20](https://downloads.mariadb.org/mariadb/10.6.20/)[Release Notes](../../mariadb-community-server-release-notes/mariadb-10-6-series/mariadb-10-6-20-release-notes.md)[Changelog](mariadb-10-6-20-changelog.md)[Overview of 10.6](../../mariadb-community-server-release-notes/mariadb-10-6-series/what-is-mariadb-106.md)

**Release date:** 1 Nov 2024

For the highlights of this release, see the[release notes](../../mariadb-community-server-release-notes/mariadb-10-6-series/mariadb-10-6-20-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/server/tree/10.6) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Includes all fixes from [MariaDB 10.5.27](../changelogs-mariadb-105-series/mariadb-10-5-27-changelog.md)
* Merge [Revision #f00711bba2](https://github.com/MariaDB/server/commit/f00711bba2) 2024-10-29 14:20:03 +0100 - Merge branch '10.5' into 10.6
* [Revision #8c7786e7d5](https://github.com/MariaDB/server/commit/8c7786e7d5)\
  2024-07-26 18:31:17 +0300
  * [MDEV-34690](https://jira.mariadb.org/browse/MDEV-34690) lock\_rec\_unlock\_unmodified() causes deadlock
* [Revision #92180ad513](https://github.com/MariaDB/server/commit/92180ad513)\
  2024-06-27 12:15:37 +0300
  * [MDEV-34466](https://jira.mariadb.org/browse/MDEV-34466) XA prepare don't release unmodified records for some cases
* [Revision #1cad1dbde6](https://github.com/MariaDB/server/commit/1cad1dbde6)\
  2024-10-23 07:55:22 +0300
  * [MDEV-35235](https://jira.mariadb.org/browse/MDEV-35235) innodb\_snapshot\_isolation=ON fails to signal transaction rollback
* [Revision #b3be3c2157](https://github.com/MariaDB/server/commit/b3be3c2157)\
  2024-06-21 13:07:35 +0300
  * [MDEV-30653](https://jira.mariadb.org/browse/MDEV-30653) : With wsrep\_mode=REPLICATE\_ARIA only part of mixed-engine transactions is replicated
* [Revision #b38edd09ff](https://github.com/MariaDB/server/commit/b38edd09ff)\
  2024-10-22 11:35:33 +0300
  * [MDEV-34830](https://jira.mariadb.org/browse/MDEV-34830) fixup: Relax an assertion
* [Revision #45537939e7](https://github.com/MariaDB/server/commit/45537939e7)\
  2024-10-21 14:58:33 +0200
  * [MDEV-34859](https://jira.mariadb.org/browse/MDEV-34859): Pass thorugh -DWITH\_BOOST\_CONTEXT to libmariadb
* [Revision #1067046b7f](https://github.com/MariaDB/server/commit/1067046b7f)\
  2024-10-22 09:09:11 +0300
  * [MDEV-34830](https://jira.mariadb.org/browse/MDEV-34830) fixup: Relax an assertion
* [Revision #bea4adcb5a](https://github.com/MariaDB/server/commit/bea4adcb5a)\
  2024-10-22 09:07:57 +0300
  * [MDEV-35225](https://jira.mariadb.org/browse/MDEV-35225) Bogus debug assertion failures in innodb.innodb-32k-crash
* [Revision #1ed30e08af](https://github.com/MariaDB/server/commit/1ed30e08af)\
  2024-09-23 08:18:55 -0600
  * [MDEV-34122](https://jira.mariadb.org/browse/MDEV-34122): Assertion \`entry' failed in Active\_tranx::assert\_thd\_is\_waiter
* [Revision #e8db5c8760](https://github.com/MariaDB/server/commit/e8db5c8760)\
  2024-10-21 12:37:29 +0200
  * [MDEV-35171](https://jira.mariadb.org/browse/MDEV-35171) OS\_FILE\_NORMAL and OS\_FILE\_AIO are misleading
* [Revision #7701ccb72d](https://github.com/MariaDB/server/commit/7701ccb72d)\
  2024-10-21 10:08:58 +0300
  * [MDEV-35149](https://jira.mariadb.org/browse/MDEV-35149) Race condition around SET GLOBAL innodb\_lru\_scan\_depth
* [Revision #70d8ce63c7](https://github.com/MariaDB/server/commit/70d8ce63c7)\
  2024-10-20 17:13:20 +0200
  * update C/C
* [Revision #a68e74b5a4](https://github.com/MariaDB/server/commit/a68e74b5a4)\
  2024-10-18 15:42:05 +0300
  * [MDEV-35164](https://jira.mariadb.org/browse/MDEV-35164): optimizer\_join\_limit\_pref\_ratio: assertion when the ORDER BY table becomes constant
* [Revision #0540eac05c](https://github.com/MariaDB/server/commit/0540eac05c)\
  2024-10-16 18:35:37 +0300
  * [MDEV-35180](https://jira.mariadb.org/browse/MDEV-35180): ref\_to\_range rewrite causes poor query plan
* [Revision #3a1cf2c85b](https://github.com/MariaDB/server/commit/3a1cf2c85b)\
  2024-07-18 15:20:42 +0200
  * [MDEV-34679](https://jira.mariadb.org/browse/MDEV-34679) ER\_BAD\_FIELD uses non-localizable substrings
* [Revision #99178311ac](https://github.com/MariaDB/server/commit/99178311ac)\
  2023-11-04 10:11:51 +0100
  * don't disable lto in DEB builds
* [Revision #a20c79da13](https://github.com/MariaDB/server/commit/a20c79da13)\
  2023-11-06 17:31:09 +0100
  * [MDEV-25633](https://jira.mariadb.org/browse/MDEV-25633) MariaDB crashes when compiled with link time optimizations
* [Revision #3e3fdb25f1](https://github.com/MariaDB/server/commit/3e3fdb25f1)\
  2023-11-05 19:05:16 +0100
  * better disable lto for libmysqld\_exports.cc
* [Revision #bfa15f9b34](https://github.com/MariaDB/server/commit/bfa15f9b34)\
  2024-07-29 17:54:06 +0200
  * C/C compilation failures under -flto
* [Revision #3693fb9581](https://github.com/MariaDB/server/commit/3693fb9581)\
  2024-07-24 19:00:15 +0200
  * [MDEV-25199](https://jira.mariadb.org/browse/MDEV-25199) cluster fails to start up
* [Revision #e1e836fc76](https://github.com/MariaDB/server/commit/e1e836fc76)\
  2024-10-17 09:59:21 +0200
  * update results after the merge
* [Revision #bb47e575de](https://github.com/MariaDB/server/commit/bb47e575de)\
  2024-10-17 17:24:20 +0300
  * [MDEV-34830](https://jira.mariadb.org/browse/MDEV-34830): LSN in the future is not being treated as serious corruption
* [Revision #740519e15a](https://github.com/MariaDB/server/commit/740519e15a)\
  2024-10-17 09:10:45 +0300
  * [MDEV-35125](https://jira.mariadb.org/browse/MDEV-35125): Unnecessary buf\_pool.page\_hash lookups
* [Revision #89493a9980](https://github.com/MariaDB/server/commit/89493a9980)\
  2024-10-15 17:35:27 +0300
  * [MDEV-34993](https://jira.mariadb.org/browse/MDEV-34993): fix merge into 10.6: OPTIMIZER\_ADJ\_FIX\_CARD\_MULT should be ON by default
* [Revision #a4d2cc931d](https://github.com/MariaDB/server/commit/a4d2cc931d)\
  2024-10-16 14:37:44 +0300
  * [MDEV-35174](https://jira.mariadb.org/browse/MDEV-35174) Possible hang in trx\_undo\_prev\_version()
* [Revision #9849e3f948](https://github.com/MariaDB/server/commit/9849e3f948)\
  2024-10-09 15:32:24 +0300
  * [MDEV-35072](https://jira.mariadb.org/browse/MDEV-35072): Assertion with optimizer\_join\_limit\_pref\_ratio and 1-table select
* [Revision #5619f29384](https://github.com/MariaDB/server/commit/5619f29384)\
  2024-10-10 16:11:37 +0300
  * Replace 0.001 with symbolic name COST\_EPS
* Merge [Revision #cd5577ba4a](https://github.com/MariaDB/server/commit/cd5577ba4a) 2024-10-15 16:00:44 +1100 - Merge branch '10.5' into 10.6
* [Revision #a79c9b3812](https://github.com/MariaDB/server/commit/a79c9b3812)\
  2024-10-14 09:36:17 +0200
  * [MDEV-35135](https://jira.mariadb.org/browse/MDEV-35135) Assertion \`!is\_cond()' failed in Item\_bool\_func::val\_int / do\_select
* Merge [Revision #cd97caef84](https://github.com/MariaDB/server/commit/cd97caef84) 2024-10-09 13:13:24 +0300 - [MDEV-33106](https://jira.mariadb.org/browse/MDEV-33106): Null merge 10.5 into 10.6
* Merge [Revision #1d0e94c55f](https://github.com/MariaDB/server/commit/1d0e94c55f) 2024-10-09 08:38:48 +0200 - Merge branch '10.5' into 10.6
* [Revision #a931da82fa](https://github.com/MariaDB/server/commit/a931da82fa)\
  2024-05-14 09:19:34 +0400
  * [MDEV-34123](https://jira.mariadb.org/browse/MDEV-34123) CONCAT Function Returns Unexpected Empty Set in Query
* [Revision #6f6c1911dc](https://github.com/MariaDB/server/commit/6f6c1911dc)\
  2024-10-03 12:21:49 +0300
  * [MDEV-34251](https://jira.mariadb.org/browse/MDEV-34251) Conditional jump or move depends on uninitialised value in ha\_handler\_stats::has\_stats
* Merge [Revision #c6e4ea682c](https://github.com/MariaDB/server/commit/c6e4ea682c) 2024-10-03 10:42:58 +0300 - Merge 10.5 into 10.6
* Merge [Revision #7e0afb1c73](https://github.com/MariaDB/server/commit/7e0afb1c73) 2024-10-03 09:31:39 +0300 - Merge 10.5 into 10.6
* [Revision #cc70ca7eab](https://github.com/MariaDB/server/commit/cc70ca7eab)\
  2024-10-02 11:09:31 +0300
  * [MDEV-35059](https://jira.mariadb.org/browse/MDEV-35059) ALTER TABLE...IMPORT TABLESPACE with FULLTEXT SEARCH may corrupt the adaptive hash index
* [Revision #a298dfb84c](https://github.com/MariaDB/server/commit/a298dfb84c)\
  2024-10-01 15:03:04 +0300
  * [MDEV-35053](https://jira.mariadb.org/browse/MDEV-35053) Crash in purge\_sys\_t::iterator::free\_history\_rseg()
* [Revision #2d031f4a71](https://github.com/MariaDB/server/commit/2d031f4a71)\
  2024-10-01 13:29:59 +0300
  * [MDEV-34973](https://jira.mariadb.org/browse/MDEV-34973) fixup for POWER,s390x
* [Revision #753e7d6d7c](https://github.com/MariaDB/server/commit/753e7d6d7c)\
  2024-07-23 16:09:10 +0530
  * [MDEV-27412](https://jira.mariadb.org/browse/MDEV-27412): JSON\_TABLE doesn't properly unquote strings
* [Revision #6715e4dfe1](https://github.com/MariaDB/server/commit/6715e4dfe1)\
  2024-09-20 10:34:44 +0200
  * [MDEV-34973](https://jira.mariadb.org/browse/MDEV-34973): innobase/dict0dict: add `noexcept` to lock/unlock methods
* [Revision #813123e3e0](https://github.com/MariaDB/server/commit/813123e3e0)\
  2024-09-20 10:19:44 +0200
  * [MDEV-34973](https://jira.mariadb.org/browse/MDEV-34973): innobase/lock0lock: add `noexcept`
* [Revision #d28ac3f82d](https://github.com/MariaDB/server/commit/d28ac3f82d)\
  2024-09-30 15:27:38 +0300
  * [MDEV-34207](https://jira.mariadb.org/browse/MDEV-34207): ALTER TABLE...STATS\_PERSISTENT=0 fails to drop statistics
* [Revision #f199dffe3b](https://github.com/MariaDB/server/commit/f199dffe3b)\
  2024-09-27 06:48:55 +1000
  * [MDEV-34937](https://jira.mariadb.org/browse/MDEV-34937) s3 engine no longer functional on non-gcc builds
* [Revision #ce272f7c29](https://github.com/MariaDB/server/commit/ce272f7c29)\
  2024-07-23 14:58:24 +0300
  * Remove unused Table\_function\_json\_table::m\_text\_literal\_cs
* [Revision #d0a6a7886b](https://github.com/MariaDB/server/commit/d0a6a7886b)\
  2024-07-23 14:33:33 +0300
  * [MDEV-25822](https://jira.mariadb.org/browse/MDEV-25822) JSON\_TABLE: default values should allow non-string literals
* [Revision #231900e5bb](https://github.com/MariaDB/server/commit/231900e5bb)\
  2024-09-09 13:30:42 +0300
  * [MDEV-34836](https://jira.mariadb.org/browse/MDEV-34836): TOI on parent table must BF abort SR in progress on a child
* [Revision #638c62acac](https://github.com/MariaDB/server/commit/638c62acac)\
  2024-09-23 12:51:27 +0300
  * [MDEV-34983](https://jira.mariadb.org/browse/MDEV-34983): Remove x86 asm from InnoDB
* [Revision #71649b93cf](https://github.com/MariaDB/server/commit/71649b93cf)\
  2024-09-20 19:53:56 +0700
  * [MDEV-31933](https://jira.mariadb.org/browse/MDEV-31933): Make working view-protocol + ps-protocol (running two protocols together)
* [Revision #ac5cbaff66](https://github.com/MariaDB/server/commit/ac5cbaff66)\
  2024-09-13 13:07:47 +1000
  * Aria - correct type
* [Revision #35d477dd1d](https://github.com/MariaDB/server/commit/35d477dd1d)\
  2024-09-18 21:56:28 +0530
  * [MDEV-34453](https://jira.mariadb.org/browse/MDEV-34453) Trying to read 16384 bytes at 70368744161280 outside the bounds of the file: ./ibdata1
* Merge [Revision #80fff4c6b1](https://github.com/MariaDB/server/commit/80fff4c6b1) 2024-09-16 16:39:59 +0200 - Merge branch '10.5' into '10.6'
* [Revision #a74bea7ba9](https://github.com/MariaDB/server/commit/a74bea7ba9)\
  2024-09-12 10:52:55 +0300
  * [MDEV-34879](https://jira.mariadb.org/browse/MDEV-34879) InnoDB fails to merge the change buffer to ROW\_FORMAT=COMPRESSED tables
* [Revision #f168050e90](https://github.com/MariaDB/server/commit/f168050e90)\
  2024-09-12 10:52:12 +0300
  * [MDEV-34791](https://jira.mariadb.org/browse/MDEV-34791) fixup: Avoid an infinite loop with ROW\_FORMAT=COMPRESSED
* Merge [Revision #09b1269e4a](https://github.com/MariaDB/server/commit/09b1269e4a) 2024-09-12 10:17:51 +1000 - Merge branch '10.5' into 10.6
* [Revision #fafcd24e02](https://github.com/MariaDB/server/commit/fafcd24e02)\
  2024-09-10 19:57:51 +0300
  * Fixed compiler warning from strncpy in mysql\_plugin.c
* [Revision #3ae4ecbfc5](https://github.com/MariaDB/server/commit/3ae4ecbfc5)\
  2024-09-10 15:52:13 +0300
  * [MDEV-34867](https://jira.mariadb.org/browse/MDEV-34867) engine S3 cause 500 error for huawei buckets
* [Revision #c6eadc4087](https://github.com/MariaDB/server/commit/c6eadc4087)\
  2024-09-11 14:07:32 +0300
  * Fix main.order\_by\_join\_limit on x86-debian-12: Mask the cost numbers.
* Merge [Revision #4a09e74387](https://github.com/MariaDB/server/commit/4a09e74387) 2024-09-11 15:49:16 +1000 - Merge branch '10.5' into 10.6
* [Revision #02b30044aa](https://github.com/MariaDB/server/commit/02b30044aa)\
  2024-09-11 13:37:40 +1000
  * [MDEV-34650](https://jira.mariadb.org/browse/MDEV-34650) main.having\_cond\_pushdown test failure - crash server (s390x)
* Merge [Revision #b7b2d2bde4](https://github.com/MariaDB/server/commit/b7b2d2bde4) 2024-09-09 11:30:30 +0300 - Merge 10.5 into 10.6
* [Revision #c630e23a18](https://github.com/MariaDB/server/commit/c630e23a18)\
  2024-09-07 17:17:44 +0300
  * [MDEV-34894](https://jira.mariadb.org/browse/MDEV-34894): Poor query plan, because range estimates are not reused for ref(const)
* [Revision #c41ab95a38](https://github.com/MariaDB/server/commit/c41ab95a38)\
  2024-09-06 15:05:23 +0300
  * Remove rows and cost from optimizer trace for not usable key parts
* [Revision #886d740ad7](https://github.com/MariaDB/server/commit/886d740ad7)\
  2024-09-06 15:04:36 +0300
  * Optimized max\_part\_bit in sql\_select.cc to use my\_find\_first\_bit.
* [Revision #f0b2e76577](https://github.com/MariaDB/server/commit/f0b2e76577)\
  2024-09-06 14:58:45 +0300
  * Removed ctrl-l from the source
* Merge [Revision #60b93cdd30](https://github.com/MariaDB/server/commit/60b93cdd30) 2024-09-06 13:52:57 +1000 - Merge branch '10.5' into 10.6
* [Revision #2ed33f2fb6](https://github.com/MariaDB/server/commit/2ed33f2fb6)\
  2024-09-04 21:25:07 +0200
  * [MDEV-26114](https://jira.mariadb.org/browse/MDEV-26114): Update Sys Schema README
* [Revision #9f0b106631](https://github.com/MariaDB/server/commit/9f0b106631)\
  2024-09-03 18:22:10 +0300
  * [MDEV-34845](https://jira.mariadb.org/browse/MDEV-34845) buf\_flush\_buffer\_pool(): Assertion \`!os\_aio\_pending\_reads()' failed
* [Revision #9878238f74](https://github.com/MariaDB/server/commit/9878238f74)\
  2024-09-03 14:15:57 +0300
  * [MDEV-34791](https://jira.mariadb.org/browse/MDEV-34791): Redundant page lookups hurt performance
* [Revision #4e2c02a12c](https://github.com/MariaDB/server/commit/4e2c02a12c)\
  2024-01-15 18:25:36 +0300
  * [MDEV-33133](https://jira.mariadb.org/browse/MDEV-33133): MDL conflict handling code should skip BF-aborted trxs
* Merge [Revision #d5a669b6b6](https://github.com/MariaDB/server/commit/d5a669b6b6) 2024-09-03 07:44:51 +0200 - Merge branch '10.5' into '10.6'
* [Revision #c8d040938a](https://github.com/MariaDB/server/commit/c8d040938a)\
  2024-08-18 20:10:19 +0300
  * [MDEV-34720](https://jira.mariadb.org/browse/MDEV-34720): Poor plan choice for large JOIN with ORDER BY and small LIMIT
* [Revision #819765a47d](https://github.com/MariaDB/server/commit/819765a47d)\
  2024-08-09 11:22:14 +0300
  * Code cleanup in test\_if\_skip\_sort\_order()
* [Revision #a50a5e0f3b](https://github.com/MariaDB/server/commit/a50a5e0f3b)\
  2024-07-26 09:04:30 +0300
  * [MDEV-34647](https://jira.mariadb.org/browse/MDEV-34647) : 'INSERT...SELECT' on MyISAM table suddenly replicated by Galera
* [Revision #b1f7522170](https://github.com/MariaDB/server/commit/b1f7522170)\
  2024-08-30 08:32:10 +0300
  * [MDEV-34841](https://jira.mariadb.org/browse/MDEV-34841) : Enable working Galera tests
* [Revision #1c48950e1f](https://github.com/MariaDB/server/commit/1c48950e1f)\
  2024-06-19 14:08:13 +0300
  * [MDEV-30536](https://jira.mariadb.org/browse/MDEV-30536): Fix Galera bulk insert optimization MTR test
* Merge [Revision #bac0804d81](https://github.com/MariaDB/server/commit/bac0804d81) 2024-09-01 06:47:32 +0200 - Merge branch '10.5' into '10.6'
* Merge [Revision #a4654ecceb](https://github.com/MariaDB/server/commit/a4654ecceb) 2024-08-29 11:28:01 +0200 - Merge branch '10.5' into 10.6
* Merge [Revision #0e76c1ba94](https://github.com/MariaDB/server/commit/0e76c1ba94) 2024-08-28 15:51:36 +0300 - Merge 10.5 into 10.6
* [Revision #bda40ccb85](https://github.com/MariaDB/server/commit/bda40ccb85)\
  2024-08-28 07:18:03 +0300
  * [MDEV-34803](https://jira.mariadb.org/browse/MDEV-34803) innodb\_lru\_flush\_size is no longer used
* Merge [Revision #48becffd07](https://github.com/MariaDB/server/commit/48becffd07) 2024-08-27 08:52:10 +0300 - Merge 10.5 into 10.6
* [Revision #8cc822283e](https://github.com/MariaDB/server/commit/8cc822283e)\
  2024-08-27 08:51:45 +0300
  * [MDEV-34515](https://jira.mariadb.org/browse/MDEV-34515) fixup: innodb.innodb\_defrag\_concurrent fails
* [Revision #36ab75a498](https://github.com/MariaDB/server/commit/36ab75a498)\
  2024-08-27 07:27:24 +0300
  * [MDEV-34515](https://jira.mariadb.org/browse/MDEV-34515): Fix a bogus debug assertion
* [Revision #76f6b6d818](https://github.com/MariaDB/server/commit/76f6b6d818)\
  2024-08-26 12:23:17 +0300
  * [MDEV-34515](https://jira.mariadb.org/browse/MDEV-34515): Reduce context switching in purge
* [Revision #b7b9f3ce82](https://github.com/MariaDB/server/commit/b7b9f3ce82)\
  2024-08-26 12:23:06 +0300
  * [MDEV-34515](https://jira.mariadb.org/browse/MDEV-34515): Contention between purge and workload
* [Revision #d58734d781](https://github.com/MariaDB/server/commit/d58734d781)\
  2024-08-26 12:22:44 +0300
  * [MDEV-34520](https://jira.mariadb.org/browse/MDEV-34520) purge\_sys\_t::wait\_FTS sleeps 10ms, even if it does not have to
* [Revision #9020baf126](https://github.com/MariaDB/server/commit/9020baf126)\
  2024-08-24 19:01:06 +0300
  * Trivial fix: Make test\_if\_cheaper\_ordering() use actual\_rec\_per\_key()
* [Revision #9db2b327d4](https://github.com/MariaDB/server/commit/9db2b327d4)\
  2024-08-23 13:27:50 +0300
  * [MDEV-34759](https://jira.mariadb.org/browse/MDEV-34759): buf\_page\_get\_low() is unnecessarily acquiring exclusive latch
* [Revision #3e5e97b26f](https://github.com/MariaDB/server/commit/3e5e97b26f)\
  2024-08-22 12:59:40 -0600
  * [MDEV-34799](https://jira.mariadb.org/browse/MDEV-34799): "Could not write packet" err message args off by 1
* Merge [Revision #fc5772ce17](https://github.com/MariaDB/server/commit/fc5772ce17) 2024-08-20 09:11:34 +0200 - Merge branch '10.5' into 10.6
* Merge [Revision #267c0fce56](https://github.com/MariaDB/server/commit/267c0fce56) 2024-08-15 10:16:46 +0300 - Merge 10.5 into 10.6
* Merge [Revision #757c368139](https://github.com/MariaDB/server/commit/757c368139) 2024-08-14 10:56:11 +0300 - Merge 10.5 into 10.6
* [Revision #4f8803c036](https://github.com/MariaDB/server/commit/4f8803c036)\
  2024-08-14 07:54:15 +0300
  * [MDEV-34678](https://jira.mariadb.org/browse/MDEV-34678) pthread\_mutex\_init() without pthread\_mutex\_destroy()
* Merge [Revision #2e580dc2a8](https://github.com/MariaDB/server/commit/2e580dc2a8) 2024-08-09 08:51:21 +0200 - Merge branch '10.6' into mariadb-10.6.19
* [Revision #f15de42585](https://github.com/MariaDB/server/commit/f15de42585)\
  2024-08-08 17:58:51 -0400
  * bump the VERSION
* [Revision #fa8ce92cc0](https://github.com/MariaDB/server/commit/fa8ce92cc0)\
  2024-08-02 10:31:08 +1000
  * [MDEV-34682](https://jira.mariadb.org/browse/MDEV-34682) Return the return value of ddl recovery done in ha\_initialize\_handlerton
* [Revision #00862b688c](https://github.com/MariaDB/server/commit/00862b688c)\
  2024-08-02 14:34:31 +0700
  * [MDEV-14959](https://jira.mariadb.org/browse/MDEV-14959): Control over memory allocated for SP/PS
