# MariaDB 10.11.3 Changelog

The most recent release of [MariaDB 10.11](../../mariadb-community-server-release-notes/mariadb-10-11-series/what-is-mariadb-1011.md) is:[**MariaDB 10.11.11**](../../mariadb-community-server-release-notes/mariadb-10-11-series/mariadb-10-11-11-release-notes.md) Stable (GA) [Download Now](https://mariadb.com/downloads/)[_Alternate download from mariadb.org_](https://downloads.mariadb.org/mariadb/10.11.11/)

[Download 10.11.3](https://downloads.mariadb.org/mariadb/10.11.3/)[Release Notes](../../mariadb-community-server-release-notes/mariadb-10-11-series/mariadb-10-11-3-release-notes.md)[Changelog](mariadb-10-11-3-changelog.md)[Overview of 10.11](../../mariadb-community-server-release-notes/mariadb-10-11-series/what-is-mariadb-1011.md)

**Release date:** 10 May 2023

For the highlights of this release, see the[release notes](../../mariadb-community-server-release-notes/mariadb-10-11-series/mariadb-10-11-3-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/server/tree/10.11) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Includes all fixes from [MariaDB 10.10.4](../changelogs-mariadb-10-10-series/mariadb-10-10-4-changelog.md)
* Merge [Revision #0bb31039f5](https://github.com/MariaDB/server/commit/0bb31039f5) 2023-05-05 15:09:16 +0200 - Merge branch '10.10' into 10.11
* Merge [Revision #2856859fa3](https://github.com/MariaDB/server/commit/2856859fa3) 2023-05-05 11:31:53 +0200 - Merge branch '10.10' into 10.11
* Merge [Revision #71f7191c60](https://github.com/MariaDB/server/commit/71f7191c60) 2023-05-05 07:16:15 +0200 - Merge branch '10.10' into 10.11
* Merge [Revision #1c60c7ab4b](https://github.com/MariaDB/server/commit/1c60c7ab4b) 2023-05-04 11:56:52 +0200 - Merge branch '10.10' into 10.11
* Merge [Revision #06d03dcdd3](https://github.com/MariaDB/server/commit/06d03dcdd3) 2023-05-03 21:05:34 +0200 - Merge branch '10.10' into 10.11
* Merge [Revision #7b17e0d4ac](https://github.com/MariaDB/server/commit/7b17e0d4ac) 2023-04-27 14:03:24 +0300 - Merge 10.10 into 10.11
* [Revision #7020887e3e](https://github.com/MariaDB/server/commit/7020887e3e)\
  2023-02-04 20:32:26 +1100
  * [MDEV-30411](https://jira.mariadb.org/browse/MDEV-30411): main.explain\_json\_format\_partitions fails on Debian arm{el,hf}
* [Revision #55cf4194f9](https://github.com/MariaDB/server/commit/55cf4194f9)\
  2023-02-09 16:55:54 +1100
  * [MDEV-30411](https://jira.mariadb.org/browse/MDEV-30411): Fix my\_timer\_init() to match the code in as my\_timer\_cycles()
* Merge [Revision #52f6f364d9](https://github.com/MariaDB/server/commit/52f6f364d9) 2023-04-26 18:31:50 +0300 - Merge 10.10 into 10.11
* Merge [Revision #b0ecf4693d](https://github.com/MariaDB/server/commit/b0ecf4693d) 2023-04-26 13:10:57 +0400 - Merge remote-tracking branch 'origin/10.10' into 10.11
* [Revision #d6c8696724](https://github.com/MariaDB/server/commit/d6c8696724)\
  2023-04-17 16:46:52 +0300
  * Update BUILD scripts
* Merge [Revision #656c2e18b1](https://github.com/MariaDB/server/commit/656c2e18b1) 2023-04-14 13:08:28 +0300 - Merge 10.10 into 10.11
* [Revision #17caff92b5](https://github.com/MariaDB/server/commit/17caff92b5)\
  2023-04-05 10:47:32 +0400
  * [MDEV-30997](https://jira.mariadb.org/browse/MDEV-30997) SIGSEGV in strlen\_avx2 | make\_date\_time | Item\_func\_date\_format::val\_str
* Merge [Revision #d84a282629](https://github.com/MariaDB/server/commit/d84a282629) 2023-03-29 16:53:37 +0300 - Merge 10.10 into 10.11
* [Revision #50c8ef01fc](https://github.com/MariaDB/server/commit/50c8ef01fc)\
  2023-03-11 11:07:48 -0800
  * Fix trivial spelling errors
* Merge [Revision #faeca0008b](https://github.com/MariaDB/server/commit/faeca0008b) 2023-03-20 10:38:44 +0200 - Merge 10.10 into 10.11
* [Revision #7b032b01cd](https://github.com/MariaDB/server/commit/7b032b01cd)\
  2023-03-16 17:57:34 +0200
  * Fixed newly introduced bug in scripts/mysql\_install\_db
* Merge [Revision #7343a2ceb6](https://github.com/MariaDB/server/commit/7343a2ceb6) 2023-03-17 14:23:03 +0200 - Merge 10.10 into 10.11
* Merge [Revision #c50f849d64](https://github.com/MariaDB/server/commit/c50f849d64) 2023-03-17 07:00:03 +0200 - Merge 10.10 into 10.11
* [Revision #ceb0e7f944](https://github.com/MariaDB/server/commit/ceb0e7f944)\
  2023-03-09 14:53:29 +0200
  * Fixes to mysql\_install\_db
* [Revision #b600671f75](https://github.com/MariaDB/server/commit/b600671f75)\
  2023-03-08 12:27:31 +1100
  * [MDEV-30810](https://jira.mariadb.org/browse/MDEV-30810) errmsg-utf8.txt no longer uses charsets
* Merge [Revision #b4c7f5e670](https://github.com/MariaDB/server/commit/b4c7f5e670) 2023-03-09 12:16:27 +0100 - Merge branch '10.10' into 10.11
* [Revision #6b8370a90f](https://github.com/MariaDB/server/commit/6b8370a90f)\
  2023-03-06 11:04:48 +0100
  * [MDEV-30789](https://jira.mariadb.org/browse/MDEV-30789): Add Georgian error messages and locale
* [Revision #b56c613e2d](https://github.com/MariaDB/server/commit/b56c613e2d)\
  2023-03-04 05:49:36 +0100
  * [MDEV-30789](https://jira.mariadb.org/browse/MDEV-30789) Add Georgian translation (error messages)
* Merge [Revision #9267160c11](https://github.com/MariaDB/server/commit/9267160c11) 2023-03-06 13:39:12 +0200 - Merge 10.10 into 10.11
* [Revision #077425a659](https://github.com/MariaDB/server/commit/077425a659)\
  2023-03-03 11:38:43 +0200
  * [MDEV-30311](https://jira.mariadb.org/browse/MDEV-30311) system-wide max transaction id corrupted after changing the undo tablespaces
* Merge [Revision #95d51369c9](https://github.com/MariaDB/server/commit/95d51369c9) 2023-02-28 10:52:42 +0200 - Merge 10.10 into 10.11
* [Revision #8460eb25d1](https://github.com/MariaDB/server/commit/8460eb25d1)\
  2023-02-16 10:46:22 -0500
  * bump the VERSION
* Merge [Revision #1fd0099839](https://github.com/MariaDB/server/commit/1fd0099839) 2023-02-16 11:41:18 +0200 - Merge 10.10 into 10.11
* [Revision #fa5426ee46](https://github.com/MariaDB/server/commit/fa5426ee46)\
  2023-02-11 01:02:40 +0100
  * Update 10.11 HELP
* [Revision #483ddb5684](https://github.com/MariaDB/server/commit/483ddb5684)\
  2023-02-09 12:49:17 +1100
  * [MDEV-30621](https://jira.mariadb.org/browse/MDEV-30621): Türkiye is the correct current country naming
