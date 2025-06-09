# MariaDB 10.8.4 Changelog

The most recent release of [MariaDB 10.8](../../mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-8-series/what-is-mariadb-108.md) is:[**MariaDB 10.8.8**](../../mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-8-series/mariadb-10-8-8-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.8.8/)

[Download 10.8.4](https://downloads.mariadb.org/mariadb/10.8.4/)[Release Notes](broken-reference)[Changelog](mariadb-1084-changelog.md)[Overview of 10.8](../../mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-8-series/what-is-mariadb-108.md)

**Release date:** 15 Aug 2022

For the highlights of this release, see the[release notes](broken-reference).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/server/tree/10.8) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Includes all fixes from [MariaDB 10.7.5](../changelogs-mariadb-10-7-series/mariadb-1075-changelog.md)
* Merge [Revision #6ffbc0e510](https://github.com/MariaDB/server/commit/6ffbc0e510) 2022-08-10 13:36:20 +0200 - Merge branch '10.7' into 10.8
* Merge [Revision #73e086442a](https://github.com/MariaDB/server/commit/73e086442a) 2022-08-09 13:47:17 +0200 - Merge branch '10.7' into 10.8
* Merge [Revision #75d631f333](https://github.com/MariaDB/server/commit/75d631f333) 2022-08-09 09:52:15 +0200 - Merge branch '10.7' into 10.8
* Merge [Revision #9cbf8ccf29](https://github.com/MariaDB/server/commit/9cbf8ccf29) 2022-08-02 08:52:57 +0300 - Merge 10.7 into 10.8
* Merge [Revision #f79cebb4d0](https://github.com/MariaDB/server/commit/f79cebb4d0) 2022-07-28 10:33:26 +0300 - Merge 10.7 into 10.8
* [Revision #1630037959](https://github.com/MariaDB/server/commit/1630037959)\
  2022-07-28 08:18:16 +0300
  * [MDEV-27774](https://jira.mariadb.org/browse/MDEV-27774) fixup: log\_sys.mutex is log\_sys.latch
* [Revision #3fbcd68d77](https://github.com/MariaDB/server/commit/3fbcd68d77)\
  2022-06-19 22:42:22 +0300
  * [MDEV-28866](https://jira.mariadb.org/browse/MDEV-28866): mariadb-upgrade to 10.8 mysql.column\_stats hist\_type + histogram errors
* [Revision #155019b96b](https://github.com/MariaDB/server/commit/155019b96b)\
  2022-07-01 18:07:07 +0300
  * [MDEV-28994](https://jira.mariadb.org/browse/MDEV-28994) Backup of memory-mapped log is corrupted
* Merge [Revision #3c2a5ad3e8](https://github.com/MariaDB/server/commit/3c2a5ad3e8) 2022-07-01 17:53:06 +0300 - Merge 10.7 into 10.8
* [Revision #ba5b2e7b29](https://github.com/MariaDB/server/commit/ba5b2e7b29)\
  2022-06-25 22:03:08 +0800
  * json\_type should consider the charset mbmaxlen
* [Revision #5ab9265677](https://github.com/MariaDB/server/commit/5ab9265677)\
  2022-06-29 19:44:04 +0200
  * [MDEV-28982](https://jira.mariadb.org/browse/MDEV-28982)- race condition in charset\_client\_win.
* Merge [Revision #b283fd40f9](https://github.com/MariaDB/server/commit/b283fd40f9) 2022-06-29 16:18:29 +0300 - Merge 10.7 into 10.8
* Merge [Revision #9523986299](https://github.com/MariaDB/server/commit/9523986299) 2022-06-28 10:06:00 +0300 - Merge 10.7 into 10.8
* Merge [Revision #b356309840](https://github.com/MariaDB/server/commit/b356309840) 2022-06-23 13:46:23 +0300 - Merge 10.7 into 10.8
* Merge [Revision #3a66c0153a](https://github.com/MariaDB/server/commit/3a66c0153a) 2022-06-22 15:40:59 +0300 - Merge 10.7 into 10.8
* [Revision #51bce3c59a](https://github.com/MariaDB/server/commit/51bce3c59a)\
  2022-06-22 11:39:53 +0300
  * [MDEV-28882](https://jira.mariadb.org/browse/MDEV-28882): Assertion \`tmp >= 0' failed in best\_access\_path
* Merge [Revision #54ac356dea](https://github.com/MariaDB/server/commit/54ac356dea) 2022-06-21 18:19:24 +0300 - Merge 10.7 into 10.8
* [Revision #325e6aa7af](https://github.com/MariaDB/server/commit/325e6aa7af)\
  2022-06-20 10:07:33 +0300
  * [MDEV-28879](https://jira.mariadb.org/browse/MDEV-28879) Assertion \`l->lsn <= log\_sys.get\_lsn()' failed around recv\_recover\_page
* Merge [Revision #cb19e211ec](https://github.com/MariaDB/server/commit/cb19e211ec) 2022-06-16 11:15:21 +0300 - Merge 10.7 into 10.8
* [Revision #4c0cd953ab](https://github.com/MariaDB/server/commit/4c0cd953ab)\
  2022-06-14 17:46:47 +0300
  * [MDEV-28766](https://jira.mariadb.org/browse/MDEV-28766): SET GLOBAL innodb\_log\_file\_buffering
* Merge [Revision #813986a647](https://github.com/MariaDB/server/commit/813986a647) 2022-06-14 16:19:29 +0300 - Merge 10.7 into 10.8
* [Revision #62419b1733](https://github.com/MariaDB/server/commit/62419b1733)\
  2022-06-09 14:52:28 +0300
  * [MDEV-26713](https://jira.mariadb.org/browse/MDEV-26713) fixup: Correct the main.winservice\_i18n result
* Merge [Revision #0af9346079](https://github.com/MariaDB/server/commit/0af9346079) 2022-06-09 14:37:53 +0300 - Merge 10.7 into 10.8
* [Revision #d61839c71e](https://github.com/MariaDB/server/commit/d61839c71e)\
  2022-06-07 12:15:27 +0300
  * [MDEV-28708](https://jira.mariadb.org/browse/MDEV-28708) Increased congestion on buf\_pool.flush\_list\_mutex
* [Revision #cf57fa8d87](https://github.com/MariaDB/server/commit/cf57fa8d87)\
  2022-06-06 20:34:49 +0200
  * fix the test for FreeBSD
* Merge [Revision #31fc2eb4bc](https://github.com/MariaDB/server/commit/31fc2eb4bc) 2022-06-07 09:07:48 +0300 - Merge 10.7 into 10.8
* [Revision #0476f48332](https://github.com/MariaDB/server/commit/0476f48332)\
  2022-06-07 09:07:37 +0300
  * [MDEV-26713](https://jira.mariadb.org/browse/MDEV-26713) fixup: Prefer shutdown to kill
* Merge [Revision #57d4a242da](https://github.com/MariaDB/server/commit/57d4a242da) 2022-06-06 16:22:09 +0300 - Merge 10.7 into 10.8
* [Revision #e097abfa66](https://github.com/MariaDB/server/commit/e097abfa66)\
  2022-06-02 11:09:56 +0300
  * [MDEV-27926](https://jira.mariadb.org/browse/MDEV-27926) After-merge fix
* Merge [Revision #600751e769](https://github.com/MariaDB/server/commit/600751e769) 2022-06-02 08:01:17 +0300 - Merge 10.7 into 10.8
* [Revision #0e0a3580ef](https://github.com/MariaDB/server/commit/0e0a3580ef)\
  2022-05-28 09:04:28 +1000
  * [MDEV-27314](https://jira.mariadb.org/browse/MDEV-27314) Condense innodb buffer pool resize message (postfix)
* [Revision #41068a890e](https://github.com/MariaDB/server/commit/41068a890e)\
  2022-05-17 15:53:54 -0500
  * [MDEV-27314](https://jira.mariadb.org/browse/MDEV-27314) Condense innodb buffer pool resize message
* [Revision #c1752a9f8f](https://github.com/MariaDB/server/commit/c1752a9f8f)\
  2022-05-25 14:08:28 +0100
  * server.cnf: adjust major version to 10.8
* [Revision #105647df78](https://github.com/MariaDB/server/commit/105647df78)\
  2022-05-25 08:39:05 +0300
  * man: adjust major version to 10.8
* Merge [Revision #c2bae9c77f](https://github.com/MariaDB/server/commit/c2bae9c77f) 2022-05-25 08:38:17 +0300 - Merge 10.7 into 10.8
* Merge [Revision #252e7e4aa5](https://github.com/MariaDB/server/commit/252e7e4aa5) 2022-05-20 21:34:49 +0200 - Merge branch '10.8' into bb-10.8-release
* [Revision #205239cdc2](https://github.com/MariaDB/server/commit/205239cdc2)\
  2022-05-20 13:20:01 -0400
  * bump the VERSION
