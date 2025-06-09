# MariaDB 10.7.4 Changelog

The most recent release of [MariaDB 10.7](../../mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-7-series/what-is-mariadb-107.md) is:[**MariaDB 10.7.8**](../../mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-7-series/mariadb-10-7-8-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.7.8/)

[Download 10.7.4](https://mariadb.org/download/?tab=mariadb\&release=10.7.4\&product=mariadb)[Release Notes](../../mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-7-series/mariadb-1074-release-notes.md)[Changelog](mariadb-1074-changelog.md)[Overview of 10.7](../../mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-7-series/what-is-mariadb-107.md)

**Release date:** 20 May 2022

For the highlights of this release, see the[release notes](../../mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-7-series/mariadb-1074-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/server/tree/10.7) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Includes all fixes from [MariaDB 10.6.8](../changelogs-mariadb-106-series/mariadb-1068-changelog.md)
* Merge [Revision #99a433ed1c](https://github.com/MariaDB/server/commit/99a433ed1c) 2022-05-18 10:34:38 +0200 - Merge branch '10.6' into 10.7
* [Revision #0a1d9d0681](https://github.com/MariaDB/server/commit/0a1d9d0681)\
  2022-02-18 16:21:08 +0100
  * [MDEV-27415](https://jira.mariadb.org/browse/MDEV-27415) main.json\_normalize and main.json\_equals fail with UBSAN runtime error
* Merge [Revision #fd132be117](https://github.com/MariaDB/server/commit/fd132be117) 2022-05-11 11:25:33 +0200 - Merge branch '10.6' into 10.7
* [Revision #7b05fc5cdd](https://github.com/MariaDB/server/commit/7b05fc5cdd)\
  2022-04-05 19:56:33 +0200
  * sporadic mariabackup.compression\_providers\_unloaded failure
* [Revision #488e56b50c](https://github.com/MariaDB/server/commit/488e56b50c)\
  2022-05-09 21:08:33 -0700
  * [MDEV-27892](https://jira.mariadb.org/browse/MDEV-27892) Improve an error message for foreign server exists
* [Revision #56fd0d7b06](https://github.com/MariaDB/server/commit/56fd0d7b06)\
  2022-04-22 07:23:07 -0700
  * [MDEV-28344](https://jira.mariadb.org/browse/MDEV-28344):sys.ps\_setup\_save and dependent procedures fail with ER\_ILLEGAL\_HA\_CREATE\_OPTION
* Merge [Revision #638afc4acf](https://github.com/MariaDB/server/commit/638afc4acf) 2022-04-26 18:59:40 +0300 - Merge 10.6 into 10.7
* [Revision #ee5966c754](https://github.com/MariaDB/server/commit/ee5966c754)\
  2022-01-23 13:42:41 +0530
  * [MDEV-26695](https://jira.mariadb.org/browse/MDEV-26695): Number of an invalid row is not calculated for table value constructor
* [Revision #9e314fcf6e](https://github.com/MariaDB/server/commit/9e314fcf6e)\
  2022-04-18 21:45:16 +0300
  * [MDEV-27749](https://jira.mariadb.org/browse/MDEV-27749) Binary changes for --as-of and --tz-utc options
* [Revision #1866fb0537](https://github.com/MariaDB/server/commit/1866fb0537)\
  2022-04-15 03:06:35 -0700
  * [MDEV-28297](https://jira.mariadb.org/browse/MDEV-28297) Deprecate spider\_internal\_offset
* [Revision #cc13ab0ffc](https://github.com/MariaDB/server/commit/cc13ab0ffc)\
  2022-04-05 18:20:41 +0900
  * [MDEV-28010](https://jira.mariadb.org/browse/MDEV-28010) Deprecate spider\_crd\_type and spider\_crd\_weight
* [Revision #075c94fe2b](https://github.com/MariaDB/server/commit/075c94fe2b)\
  2022-04-05 17:51:38 +0900
  * [MDEV-28008](https://jira.mariadb.org/browse/MDEV-28008) Deprecate spider\_crd\_mode and spider\_sts\_mode
* [Revision #7310e93ef6](https://github.com/MariaDB/server/commit/7310e93ef6)\
  2022-04-05 16:55:42 +0900
  * [MDEV-28007](https://jira.mariadb.org/browse/MDEV-28007) Deprecate Spider plugin variables regarding statistics persistence
* [Revision #3be8f66185](https://github.com/MariaDB/server/commit/3be8f66185)\
  2022-04-05 17:37:49 +0900
  * [MDEV-28244](https://jira.mariadb.org/browse/MDEV-28244) Deprecate spider\_xa\_register\_mode
* Merge [Revision #c235295525](https://github.com/MariaDB/server/commit/c235295525) 2022-04-14 13:31:07 +0300 - Merge 10.6 into 10.7
* [Revision #e87c710dfc](https://github.com/MariaDB/server/commit/e87c710dfc)\
  2022-04-13 06:21:15 +0000
  * [MDEV-27981](https://jira.mariadb.org/browse/MDEV-27981) Deprecate spider\_internal\_limit
* Merge [Revision #aa3a9d1ef5](https://github.com/MariaDB/server/commit/aa3a9d1ef5) 2022-04-12 16:11:29 +0300 - Merge 10.6 into 10.7
* [Revision #011b332d81](https://github.com/MariaDB/server/commit/011b332d81)\
  2022-04-11 12:55:07 +0530
  * [MDEV-28037](https://jira.mariadb.org/browse/MDEV-28037) Assertion \`trx->bulk\_insert' failed in innodb\_prepare\_commit\_versioned
* [Revision #e858fc89d3](https://github.com/MariaDB/server/commit/e858fc89d3)\
  2022-01-25 14:35:43 +0200
  * [MDEV-27033](https://jira.mariadb.org/browse/MDEV-27033): Clean lintian 'duplicate-override-context' warnings
* Merge [Revision #2d8e38bc94](https://github.com/MariaDB/server/commit/2d8e38bc94) 2022-04-06 13:00:09 +0300 - Merge 10.6 into 10.7
* Merge [Revision #b249abde57](https://github.com/MariaDB/server/commit/b249abde57) 2022-04-06 14:11:58 +1000 - Merge branch '10.6' into 10.7
* [Revision #b4f3969a6c](https://github.com/MariaDB/server/commit/b4f3969a6c)\
  2022-02-16 15:22:44 +0200
  * [MDEV-28121](https://jira.mariadb.org/browse/MDEV-28121): Add new compression plugins as autopkg dependencies
* [Revision #db655e1310](https://github.com/MariaDB/server/commit/db655e1310)\
  2022-04-04 19:34:59 +0530
  * [MDEV-28237](https://jira.mariadb.org/browse/MDEV-28237) Assertion \`0' failed in row\_upd\_sec\_index\_entry on DELETE
* [Revision #b678f8811b](https://github.com/MariaDB/server/commit/b678f8811b)\
  2022-04-04 09:56:52 +0530
  * [MDEV-28138](https://jira.mariadb.org/browse/MDEV-28138) MariaDB Assertion Failed in mtr\_buf\_t::has\_space
* [Revision #cd56b40f6d](https://github.com/MariaDB/server/commit/cd56b40f6d)\
  2022-04-04 14:32:16 +0700
  * [MDEV-28129](https://jira.mariadb.org/browse/MDEV-28129): MariaDB UAF issue at lex\_end\_nops(LEX\*)
* [Revision #d48774e0e0](https://github.com/MariaDB/server/commit/d48774e0e0)\
  2022-04-01 12:32:16 +0200
  * [MDEV-27354](https://jira.mariadb.org/browse/MDEV-27354) Change maturity of plugins
* [Revision #32ab64c390](https://github.com/MariaDB/server/commit/32ab64c390)\
  2022-04-01 17:21:08 +1100
  * MDBF-348: libfmt=system, custom include path
* [Revision #2407dbbfc4](https://github.com/MariaDB/server/commit/2407dbbfc4)\
  2022-04-01 09:06:53 +0300
  * [MDEV-27600](https://jira.mariadb.org/browse/MDEV-27600) partition\_debug fails with warnings "Table is open on rename new table"
* [Revision #f78fdf087f](https://github.com/MariaDB/server/commit/f78fdf087f)\
  2022-03-07 22:02:08 +0900
  * [MDEV-28005](https://jira.mariadb.org/browse/MDEV-28005) Deprecate Spider plugin variables regarding UDFs
* Merge [Revision #a4d753758f](https://github.com/MariaDB/server/commit/a4d753758f) 2022-03-30 08:52:05 +0300 - Merge 10.6 into 10.7
* [Revision #2885fb0ee4](https://github.com/MariaDB/server/commit/2885fb0ee4)\
  2022-03-28 14:03:41 +1100
  * deb: merge fix - remove debian/mariadb-plugin-columnstore.\*
* [Revision #13b97880bd](https://github.com/MariaDB/server/commit/13b97880bd)\
  2022-03-22 09:04:37 +0200
  * [MDEV-27965](https://jira.mariadb.org/browse/MDEV-27965): MariaDB needs at least libfmt version 7.0
* Merge [Revision #8b92e346b1](https://github.com/MariaDB/server/commit/8b92e346b1) 2022-03-25 14:31:59 +1100 - Merge 10.6 into 10.7
* Merge [Revision #0444d86baf](https://github.com/MariaDB/server/commit/0444d86baf) 2022-03-24 22:01:27 +1100 - Merge 10.7
* [Revision #c3ca729ba8](https://github.com/MariaDB/server/commit/c3ca729ba8)\
  2022-03-09 17:30:21 +0530
  * [MDEV-27858](https://jira.mariadb.org/browse/MDEV-27858) Assertion \`page\_dir\_get\_n\_heap(new\_page) == 2U' failed in PageBulk::init
* Merge [Revision #e86986a157](https://github.com/MariaDB/server/commit/e86986a157) 2022-03-24 18:57:07 +1100 - Merge 10.6 into 10.7
* [Revision #9c57bbdad0](https://github.com/MariaDB/server/commit/9c57bbdad0)\
  2022-03-18 10:43:24 +0200
  * [MDEV-28120](https://jira.mariadb.org/browse/MDEV-28120) Remove false-positive Lintian linking error
* [Revision #770f62bf3e](https://github.com/MariaDB/server/commit/770f62bf3e)\
  2022-03-21 10:16:38 +0200
  * [MDEV-28135](https://jira.mariadb.org/browse/MDEV-28135): Add missing conflict and breaks for [MariaDB 10.6](../../mariadb-community-server-release-notes/mariadb-10-6-series/what-is-mariadb-106.md)
* [Revision #1960f7b224](https://github.com/MariaDB/server/commit/1960f7b224)\
  2022-01-25 14:09:22 +0200
  * [MDEV-27033](https://jira.mariadb.org/browse/MDEV-27033): Clean lintian 'extended-description-is-empty' errors
* [Revision #bf8dc0be9e](https://github.com/MariaDB/server/commit/bf8dc0be9e)\
  2022-03-17 12:13:19 +0100
  * fix columnstore compilation after 33c30da16550
* Merge [Revision #dc4b7f382b](https://github.com/MariaDB/server/commit/dc4b7f382b) 2022-03-15 15:25:31 +0200 - Merge 10.6 into 10.7
* [Revision #de4ec44b4f](https://github.com/MariaDB/server/commit/de4ec44b4f)\
  2022-03-15 12:57:39 +0200
  * Fix clang -Wtypedef-redefinition
* Merge [Revision #e67d46e4a1](https://github.com/MariaDB/server/commit/e67d46e4a1) 2022-03-14 11:30:32 +0200 - Merge 10.6 into 10.7
* [Revision #810ed88c65](https://github.com/MariaDB/server/commit/810ed88c65)\
  2022-02-21 16:02:28 +0900
  * [MDEV-27169](https://jira.mariadb.org/browse/MDEV-27169) Change default values of Spider plugin variables to default values of table variables
* [Revision #332c59a27c](https://github.com/MariaDB/server/commit/332c59a27c)\
  2022-03-02 14:14:17 +0900
  * [MDEV-27923](https://jira.mariadb.org/browse/MDEV-27923) Deprecate spider\_use\_handler
* [Revision #33c30da165](https://github.com/MariaDB/server/commit/33c30da165)\
  2022-03-11 15:33:59 +0200
  * Fix clang -Wtypedef-redefinition
* Merge [Revision #3c9f415e52](https://github.com/MariaDB/server/commit/3c9f415e52) 2022-03-11 14:52:16 +0200 - Merge 10.6 into 10.7
* Merge [Revision #79bc654ac3](https://github.com/MariaDB/server/commit/79bc654ac3) 2022-03-11 10:48:58 +0200 - Merge 10.6 into 10.7
* Merge [Revision #af87186c1d](https://github.com/MariaDB/server/commit/af87186c1d) 2022-03-08 09:51:31 +0200 - Merge 10.6 into 10.7
* Merge [Revision #64ea3eab8f](https://github.com/MariaDB/server/commit/64ea3eab8f) 2022-03-03 11:11:00 +0200 - Merge 10.6 into 10.7
* Merge [Revision #a43777cc92](https://github.com/MariaDB/server/commit/a43777cc92) 2022-03-01 09:36:28 +0200 - Merge 10.6 into 10.7
* Merge [Revision #3d88f9f34c](https://github.com/MariaDB/server/commit/3d88f9f34c) 2022-02-25 16:09:16 +0200 - Merge 10.6 into 10.7
* Merge [Revision #01bb003a3a](https://github.com/MariaDB/server/commit/01bb003a3a) 2022-02-23 16:22:34 +0200 - Merge 10.6 into 10.7
* Merge [Revision #507084517f](https://github.com/MariaDB/server/commit/507084517f) 2022-02-22 12:47:48 +0200 - Merge 10.6 into 10.7
* Merge [Revision #c76bdc57ff](https://github.com/MariaDB/server/commit/c76bdc57ff) 2022-02-17 14:57:00 +0200 - Merge 10.6 into 10.7
* Merge [Revision #38a8ac1951](https://github.com/MariaDB/server/commit/38a8ac1951) 2022-02-17 11:56:14 +0100 - Merge remote-tracking branch 'origin/10.6' into 10.7
* Merge [Revision #33fd136c61](https://github.com/MariaDB/server/commit/33fd136c61) 2022-02-14 09:26:18 +0200 - Merge 10.6 into 10.7
* Merge [Revision #5291f35f9f](https://github.com/MariaDB/server/commit/5291f35f9f) 2022-02-14 08:36:03 +0200 - Merge 10.6 into 10.7
* Merge [Revision #018519a8b2](https://github.com/MariaDB/server/commit/018519a8b2) 2022-02-14 08:35:41 +0200 - Merge mariadb-10.7.3 into 10.7
* [Revision #c62720d07f](https://github.com/MariaDB/server/commit/c62720d07f)\
  2022-02-12 13:39:28 -0500
  * bump the VERSION
