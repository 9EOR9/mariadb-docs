# MariaDB 10.6.14 Changelog

The most recent release of [MariaDB 10.6](../../mariadb-community-server-release-notes/mariadb-10-6-series/what-is-mariadb-106.md) is:[**MariaDB 10.6.21**](../../mariadb-community-server-release-notes/mariadb-10-6-series/mariadb-10-6-21-release-notes.md) Stable (GA) [Download Now](https://mariadb.com/downloads/)[_Alternate download from mariadb.org_](https://downloads.mariadb.org/mariadb/10.6.21/)

[Download 10.6.14](https://downloads.mariadb.org/mariadb/10.6.14/)[Release Notes](../../mariadb-community-server-release-notes/mariadb-10-6-series/mariadb-10-6-14-release-notes.md)[Changelog](mariadb-10-6-14-changelog.md)[Overview of 10.6](../../mariadb-community-server-release-notes/mariadb-10-6-series/what-is-mariadb-106.md)

**Release date:** 7 Jun 2023

For the highlights of this release, see the[release notes](../../mariadb-community-server-release-notes/mariadb-10-6-series/mariadb-10-6-14-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/server/tree/10.6) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Includes all fixes from [MariaDB 10.5.21](../changelogs-mariadb-105-series/mariadb-10-5-21-changelog.md)
* [Revision #c93754d45e](https://github.com/MariaDB/server/commit/c93754d45e)\
  2023-05-19 12:25:30 +0300
  * [MDEV-31234](https://jira.mariadb.org/browse/MDEV-31234) related cleanup
* Merge [Revision #a42a6fa99b](https://github.com/MariaDB/server/commit/a42a6fa99b) 2023-06-05 18:26:06 +0200 - Merge branch 'bb-10.5-release' into bb-10.6-release
* [Revision #fcfd6361cb](https://github.com/MariaDB/server/commit/fcfd6361cb)\
  2023-05-27 22:42:59 -0700
  * Deb: Fix blocksize check to use $mysql\_datadir/$datadir correctly
* [Revision #cf37e44eec](https://github.com/MariaDB/server/commit/cf37e44eec)\
  2023-05-26 16:40:07 +0300
  * [MDEV-31350](https://jira.mariadb.org/browse/MDEV-31350): Hang in innodb.recovery\_memory
* [Revision #dd298873da](https://github.com/MariaDB/server/commit/dd298873da)\
  2023-05-19 15:38:48 +0300
  * [MDEV-31309](https://jira.mariadb.org/browse/MDEV-31309) Innodb\_buffer\_pool\_read\_requests is not updated correctly
* [Revision #89eb6fa8a7](https://github.com/MariaDB/server/commit/89eb6fa8a7)\
  2023-05-19 15:29:26 +0300
  * [MDEV-31308](https://jira.mariadb.org/browse/MDEV-31308) InnoDB monitor trx\_rseg\_history\_len was accidentally disabled by default
* [Revision #883333a74e](https://github.com/MariaDB/server/commit/883333a74e)\
  2023-05-11 08:43:00 +0300
  * [MDEV-31158](https://jira.mariadb.org/browse/MDEV-31158): Potential hang with ROW\_FORMAT=COMPRESSED tables
* [Revision #459eb9a686](https://github.com/MariaDB/server/commit/459eb9a686)\
  2023-05-22 17:10:25 +0300
  * [MDEV-29593](https://jira.mariadb.org/browse/MDEV-29593) fixup: Avoid a leak if rseg.undo\_cached is corrupted
* [Revision #e89bd39c9b](https://github.com/MariaDB/server/commit/e89bd39c9b)\
  2023-05-26 16:16:10 +0300
  * [MDEV-31343](https://jira.mariadb.org/browse/MDEV-31343) Another server hang with innodb\_undo\_log\_truncate=ON
