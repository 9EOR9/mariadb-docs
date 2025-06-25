# MariaDB 10.6.4 Changelog

The most recent release of [MariaDB 10.6](../../mariadb-10-6-series/what-is-mariadb-106.md) is:[**MariaDB 10.6.21**](../../mariadb-10-6-series/mariadb-10-6-21-release-notes.md) Stable (GA) [Download Now](https://mariadb.com/downloads/)[_Alternate download from mariadb.org_](https://downloads.mariadb.org/mariadb/10.6.21/)

[Download 10.6.4](https://mariadb.org/download/?tab=mariadb\&release=10.6.4\&product=mariadb)[Release Notes](../../mariadb-10-6-series/mariadb-1064-release-notes.md)[Changelog](mariadb-1064-changelog.md)[Overview of 10.6](../../mariadb-10-6-series/what-is-mariadb-106.md)

**Release date:** 6 Aug 2021

For the highlights of this release, see the[release notes](../../mariadb-10-6-series/mariadb-1064-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/server/tree/10.6) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Includes all fixes from [MariaDB 10.5.12](../changelogs-mariadb-105-series/mariadb-10512-changelog.md)
* [Revision #2db692f5b4](https://github.com/MariaDB/server/commit/2db692f5b4)\
  2021-08-03 11:38:55 +0200
  * [MDEV-26180](https://jira.mariadb.org/browse/MDEV-26180): Enable test main.sp-row after the 10.5 merge
* Merge [Revision #7ae6ef5236](https://github.com/MariaDB/server/commit/7ae6ef5236) 2021-08-03 11:21:22 +0200 - Merge branch '10.5' into 10.6
* [Revision #a4482cdbed](https://github.com/MariaDB/server/commit/a4482cdbed)\
  2021-08-02 10:18:35 +0200
  * new columnstore
* Merge [Revision #6efb5e9f5e](https://github.com/MariaDB/server/commit/6efb5e9f5e) 2021-08-02 10:11:41 +0200 - Merge branch '10.5' into 10.6
* [Revision #07674e6a74](https://github.com/MariaDB/server/commit/07674e6a74)\
  2021-07-29 12:55:31 +0200
  * [MDEV-26165](https://jira.mariadb.org/browse/MDEV-26165) Failed to upgrade from 10.4 to 10.6
* [Revision #c314fd8c1a](https://github.com/MariaDB/server/commit/c314fd8c1a)\
  2021-07-17 21:17:41 +0200
  * compilation failure on clang 11.1.0
* [Revision #3b052f8187](https://github.com/MariaDB/server/commit/3b052f8187)\
  2021-07-15 09:39:44 +0200
  * don't use \*.in for test data
* [Revision #3e4fa50571](https://github.com/MariaDB/server/commit/3e4fa50571)\
  2021-07-14 20:52:36 +0200
  * die verbosely in main.mysql\_install\_db\_win
* [Revision #ac56a6c1c4](https://github.com/MariaDB/server/commit/ac56a6c1c4)\
  2021-07-30 08:05:28 +0300
  * fixup e305493b1c0cd4e158c19bab3047a738fcd4e5c5 -DWITH\_DBUG\_TRACE=ON
* [Revision #0aa2bc7a94](https://github.com/MariaDB/server/commit/0aa2bc7a94)\
  2021-07-29 16:41:58 +0300
  * [MDEV-19445](https://jira.mariadb.org/browse/MDEV-19445)/[MDEV-16678](https://jira.mariadb.org/browse/MDEV-16678) fixup: Acquire proper MDL on innodb\_ft\_aux\_table
* [Revision #e305493b1c](https://github.com/MariaDB/server/commit/e305493b1c)\
  2021-07-29 16:38:24 +0300
  * [MDEV-21175](https://jira.mariadb.org/browse/MDEV-21175) follow-up: Remove redundant locking; rely on MDL
* [Revision #86a1428934](https://github.com/MariaDB/server/commit/86a1428934)\
  2021-07-29 16:35:19 +0300
  * [MDEV-23484](https://jira.mariadb.org/browse/MDEV-23484) Rollback unnecessarily acquires dict\_sys.latch
* [Revision #15363a4f1b](https://github.com/MariaDB/server/commit/15363a4f1b)\
  2021-07-29 15:37:35 +0300
  * Cleanup: Remove pars\_stored\_procedure\_call()
* [Revision #92046ba244](https://github.com/MariaDB/server/commit/92046ba244)\
  2021-07-29 15:28:05 +0300
  * [MDEV-25506](https://jira.mariadb.org/browse/MDEV-25506) fixup: Correct a bogus comment
* [Revision #72764b2f29](https://github.com/MariaDB/server/commit/72764b2f29)\
  2021-07-29 15:27:47 +0300
  * Cleanup: Remove a workaround
* [Revision #e8ba64262b](https://github.com/MariaDB/server/commit/e8ba64262b)\
  2021-07-29 15:00:38 +0300
  * [MDEV-26274](https://jira.mariadb.org/browse/MDEV-26274) fts\_lock\_table() attempts to release unreserved dict\_sys.mutex
* [Revision #beb401b25f](https://github.com/MariaDB/server/commit/beb401b25f)\
  2021-06-24 16:42:57 +0530
  * This commit is a fixup for [MDEV-22189](https://jira.mariadb.org/browse/MDEV-22189).
* [Revision #bdae5508b8](https://github.com/MariaDB/server/commit/bdae5508b8)\
  2021-07-26 14:51:19 +0300
  * Cleanup: Remove a test hack
* [Revision #42b9daaea7](https://github.com/MariaDB/server/commit/42b9daaea7)\
  2021-07-23 17:29:51 +0300
  * [MDEV-26138](https://jira.mariadb.org/browse/MDEV-26138) innodb\_flush\_log\_at\_trx\_commit=3 doesn't flush
* [Revision #c35ac54891](https://github.com/MariaDB/server/commit/c35ac54891)\
  2021-07-22 14:30:57 +0300
  * Update libmariadb
* Merge [Revision #7783161f30](https://github.com/MariaDB/server/commit/7783161f30) 2021-07-22 13:02:26 +0300 - Merge 10.5 into 10.6
* [Revision #5f4314f0e6](https://github.com/MariaDB/server/commit/5f4314f0e6)\
  2021-07-22 11:17:44 +0300
  * [MDEV-26210](https://jira.mariadb.org/browse/MDEV-26210): Disable mariabackup.log\_page\_corruption
* [Revision #a4dc926579](https://github.com/MariaDB/server/commit/a4dc926579)\
  2021-07-21 15:44:32 +0300
  * [MDEV-26193](https://jira.mariadb.org/browse/MDEV-26193): Wake up purge less often
* Merge [Revision #641f09398f](https://github.com/MariaDB/server/commit/641f09398f) 2021-07-22 10:11:08 +0300 - Merge 10.5 into 10.6
* [Revision #f43370baf3](https://github.com/MariaDB/server/commit/f43370baf3)\
  2021-07-21 19:31:17 +0700
  * [MDEV-26150](https://jira.mariadb.org/browse/MDEV-26150): follow-up patch to add missing fill opt\_trace,ps.rdiff
* [Revision #61fcbed920](https://github.com/MariaDB/server/commit/61fcbed920)\
  2021-07-20 17:36:46 +0300
  * [MDEV-26192](https://jira.mariadb.org/browse/MDEV-26192): Sparse files are being created on thinly provisioned storage
* [Revision #ed0a7b1b3f](https://github.com/MariaDB/server/commit/ed0a7b1b3f)\
  2021-07-20 17:35:03 +0300
  * [MDEV-24626](https://jira.mariadb.org/browse/MDEV-24626) fixup: Remove useless code
* [Revision #68694c8ed9](https://github.com/MariaDB/server/commit/68694c8ed9)\
  2021-07-20 12:36:35 +0300
  * Update libmariadb
* [Revision #ae62f115be](https://github.com/MariaDB/server/commit/ae62f115be)\
  2021-07-20 10:55:03 +0300
  * [MDEV-26166](https://jira.mariadb.org/browse/MDEV-26166): non-functional changes
* Merge [Revision #eb9a28478f](https://github.com/MariaDB/server/commit/eb9a28478f) 2021-07-20 10:54:17 +0300 - Merge 10.5 into 10.6
* [Revision #832e473d5e](https://github.com/MariaDB/server/commit/832e473d5e)\
  2021-07-19 23:13:18 +0700
  * [MDEV-26181](https://jira.mariadb.org/browse/MDEV-26181): The test compat/oracle.sp-row fails in case it is run in PS mode.
* [Revision #fa45400d77](https://github.com/MariaDB/server/commit/fa45400d77)\
  2021-07-19 17:16:54 +0700
  * [MDEV-26149](https://jira.mariadb.org/browse/MDEV-26149): The test main.fetch\_first fails in case it is run in PS mode
* [Revision #74f5aa164e](https://github.com/MariaDB/server/commit/74f5aa164e)\
  2021-07-16 23:20:36 +0200
  * [MDEV-19237](https://jira.mariadb.org/browse/MDEV-19237) - Fix assertion in should\_send\_column\_info
* Merge [Revision #e7f4daf88c](https://github.com/MariaDB/server/commit/e7f4daf88c) 2021-07-16 22:12:09 +0200 - merge 10.5 to 10.6
* [Revision #461cac8901](https://github.com/MariaDB/server/commit/461cac8901)\
  2021-07-16 09:30:36 +0700
  * [MDEV-26150](https://jira.mariadb.org/browse/MDEV-26150): The test main.opt\_trace fails in case it is run in PS mode
* [Revision #429382c29f](https://github.com/MariaDB/server/commit/429382c29f)\
  2021-07-15 16:27:31 +0700
  * [MDEV-26142](https://jira.mariadb.org/browse/MDEV-26142): Fix failures of the tests main.features and sys\_vars.stored\_program\_cache\_func when they are run in PS mode
* [Revision #ff0d3bb8dd](https://github.com/MariaDB/server/commit/ff0d3bb8dd)\
  2021-07-14 22:23:36 +0700
  * [MDEV-26146](https://jira.mariadb.org/browse/MDEV-26146): The test main.limit\_rows\_examined fails in case it is run in PS mode.
* [Revision #04369f9cee](https://github.com/MariaDB/server/commit/04369f9cee)\
  2021-05-29 21:58:51 -0700
  * Implement simple Gitlab-CI pipeline for MariaDB with RPM builds
* [Revision #edcab6366f](https://github.com/MariaDB/server/commit/edcab6366f)\
  2021-07-13 16:10:02 +0200
  * simplify myskel.m4 and make it work when a path contains '@'
* [Revision #a8410693dc](https://github.com/MariaDB/server/commit/a8410693dc)\
  2021-07-06 09:50:41 -0400
  * bump the VERSION
* [Revision #94c508dd4f](https://github.com/MariaDB/server/commit/94c508dd4f)\
  2021-07-06 00:06:20 +0200
  * [MDEV-22709](https://jira.mariadb.org/browse/MDEV-22709) Assertion \`store.length() <= (256&#x4C;_&#x32;56&#x4C;_&#x32;56L-1)' failed in net\_send\_ok

{% @marketo/form formid="4316" formId="4316" %}
