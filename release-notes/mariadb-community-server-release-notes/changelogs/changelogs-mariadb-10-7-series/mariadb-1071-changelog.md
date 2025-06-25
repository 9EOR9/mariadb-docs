# MariaDB 10.7.1 Changelog

The most recent release of [MariaDB 10.7](../../old-releases/release-notes-mariadb-10-7-series/what-is-mariadb-107.md) is:[**MariaDB 10.7.8**](../../old-releases/release-notes-mariadb-10-7-series/mariadb-10-7-8-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.7.8/)

[Download 10.7.1](https://mariadb.org/download/?tab=mariadb\&release=10.7.1\&product=mariadb)[Release Notes](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-7-series)[Changelog](mariadb-1071-changelog.md)[Overview of 10.7](../../old-releases/release-notes-mariadb-10-7-series/what-is-mariadb-107.md)

**Release date:** 8 Nov 2021

For the highlights of this release, see the [Release Notes](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-7-series)

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/server/tree/10.7) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Changes from 10.7.0 are also included in this changelog
* Includes all fixes from [MariaDB 10.6.5](../changelogs-mariadb-106-series/mariadb-1065-changelog.md)
* Merge [Revision #8bd21167d2](https://github.com/MariaDB/server/commit/8bd21167d2) 2021-11-05 21:01:15 +0100 - Merge branch '10.6' into 10.7
* Merge [Revision #2b551edb4e](https://github.com/MariaDB/server/commit/2b551edb4e) 2021-11-05 08:13:35 +0200 - Merge 10.6 into 10.7
* Merge [Revision #db8248d0cd](https://github.com/MariaDB/server/commit/db8248d0cd) 2021-11-05 00:21:23 +0100 - Merge branch '10.6' into 10.7
* [Revision #37b9467a14](https://github.com/MariaDB/server/commit/37b9467a14)\
  2021-11-04 09:52:03 +0100
  * columnstore
* Merge [Revision #5051d34894](https://github.com/MariaDB/server/commit/5051d34894) 2021-11-03 14:18:50 +0100 - Merge branch '10.6' into 10.7
* Merge [Revision #167eac7d43](https://github.com/MariaDB/server/commit/167eac7d43) 2021-11-03 11:30:27 +0100 - Merge branch '10.6' into 10.7
* Merge [Revision #2b7007803e](https://github.com/MariaDB/server/commit/2b7007803e) 2021-10-31 10:34:19 +0100 - Merge branch '10.6' into 10.7
* [Revision #f5ecaf232e](https://github.com/MariaDB/server/commit/f5ecaf232e)\
  2021-10-30 11:16:22 +0200
  * [MDEV-26221](https://jira.mariadb.org/browse/MDEV-26221): DYNAMIC\_ARRAY use size\_t for sizes
* [Revision #0a17a526c1](https://github.com/MariaDB/server/commit/0a17a526c1)\
  2021-10-30 11:08:57 +0200
  * workaround for gcc bug 7302
* [Revision #960b4870a2](https://github.com/MariaDB/server/commit/960b4870a2)\
  2021-10-29 22:44:46 +0200
  * columnstore
* [Revision #da4479ef9d](https://github.com/MariaDB/server/commit/da4479ef9d)\
  2021-10-26 17:53:17 +0400
  * [MDEV-26732](https://jira.mariadb.org/browse/MDEV-26732) Assertion \`0' failed in Item::val\_native
* [Revision #6bf5a3beb3](https://github.com/MariaDB/server/commit/6bf5a3beb3)\
  2021-10-25 17:28:25 +0400
  * [MDEV-26785](https://jira.mariadb.org/browse/MDEV-26785) Hyphens inside the value of uuid datatype
* [Revision #4300f50243](https://github.com/MariaDB/server/commit/4300f50243)\
  2021-10-25 14:36:49 +0400
  * [MDEV-26742](https://jira.mariadb.org/browse/MDEV-26742) Assertion \`field->type\_handler() == this' failed in FixedBinTypeBundle\<NATIVE\_LEN, MAX\_CHAR\_LEN>::Type\_handler\_fbt::stored\_field\_cmp\_to\_item
* [Revision #b9f19f7eae](https://github.com/MariaDB/server/commit/b9f19f7eae)\
  2021-10-19 13:17:11 +0400
  * [MDEV-26664](https://jira.mariadb.org/browse/MDEV-26664) Store UUIDs in a more efficient manner
* [Revision #50bcda010f](https://github.com/MariaDB/server/commit/50bcda010f)\
  2021-10-14 13:10:09 +0400
  * Changing the FixedBinTypeBundle parameter to a "storage class" instead of sizes
* [Revision #b1fab9bf4e](https://github.com/MariaDB/server/commit/b1fab9bf4e)\
  2021-09-14 12:08:01 +0200
  * UUID() function should return UUID, not VARCHAR(36)
* [Revision #7ab11f2bda](https://github.com/MariaDB/server/commit/7ab11f2bda)\
  2019-10-28 10:52:15 +0400
  * [MDEV-4958](https://jira.mariadb.org/browse/MDEV-4958) Adding datatype UUID
* [Revision #72fb37ea89](https://github.com/MariaDB/server/commit/72fb37ea89)\
  2021-08-17 16:58:17 +0200
  * cleanup: uuid
* [Revision #bdaa7fac89](https://github.com/MariaDB/server/commit/bdaa7fac89)\
  2021-08-22 13:56:54 +0200
  * cleanup: move most of type\_inet plugin implementation into the server
* [Revision #12eb8ad7b9](https://github.com/MariaDB/server/commit/12eb8ad7b9)\
  2021-07-26 22:43:16 +0200
  * [MDEV-26242](https://jira.mariadb.org/browse/MDEV-26242): Assertion \`i >= 0' failed on setting default\_tmp\_storage\_engine to 'DEFAULT' in 10.7
* Merge [Revision #d7af7bfc2b](https://github.com/MariaDB/server/commit/d7af7bfc2b) 2021-10-28 09:14:51 +0300 - Merge 10.6 into 10.7
* [Revision #a52cd4aeda](https://github.com/MariaDB/server/commit/a52cd4aeda)\
  2021-10-26 14:37:16 +0200
  * InnoDB: send "corrupted" error to the user, not only to the log
* [Revision #db20c77782](https://github.com/MariaDB/server/commit/db20c77782)\
  2021-10-22 10:14:57 +0200
  * mariadb-backup: rename encryption\_plugin -> xb\_plugin
* [Revision #8c806c4152](https://github.com/MariaDB/server/commit/8c806c4152)\
  2021-10-11 14:53:11 +0200
  * [MDEV-26794](https://jira.mariadb.org/browse/MDEV-26794) mariadb-backup does not recognize added providers upon prepare of incremental backup
* [Revision #5a330d4cce](https://github.com/MariaDB/server/commit/5a330d4cce)\
  2021-10-11 13:45:19 +0200
  * [MDEV-26794](https://jira.mariadb.org/browse/MDEV-26794) mariadb-backup does not recognize added providers upon prepare of incremental backup
* [Revision #2be6804650](https://github.com/MariaDB/server/commit/2be6804650)\
  2021-10-09 12:59:04 +0200
  * [MDEV-26791](https://jira.mariadb.org/browse/MDEV-26791) mariadb-backup logs compression provider plugins as encryption plugin
* [Revision #b91acd405a](https://github.com/MariaDB/server/commit/b91acd405a)\
  2021-10-08 09:48:31 +0200
  * [MDEV-26773](https://jira.mariadb.org/browse/MDEV-26773) mariadb-backup backup does not work with compression providers
* [Revision #a010959a56](https://github.com/MariaDB/server/commit/a010959a56)\
  2021-10-09 11:07:47 +0200
  * [MDEV-26774](https://jira.mariadb.org/browse/MDEV-26774) Compression provider unloading at runtime has no effect but doesn't produce a warning
* [Revision #867f05ded3](https://github.com/MariaDB/server/commit/867f05ded3)\
  2021-10-09 10:53:29 +0200
  * Avoid ASAN odr error
* [Revision #3f1bf683ca](https://github.com/MariaDB/server/commit/3f1bf683ca)\
  2021-10-09 11:25:02 +0200
  * enable innodb compression tests that were disabled by mistake
* [Revision #bf8b699f64](https://github.com/MariaDB/server/commit/bf8b699f64)\
  2021-08-31 14:09:47 +0200
  * [MDEV-12933](https://jira.mariadb.org/browse/MDEV-12933) sort out the compression library chaos
* [Revision #c356714d77](https://github.com/MariaDB/server/commit/c356714d77)\
  2021-08-31 14:04:09 +0200
  * Change Find\*.cmake modules to match conventions
* [Revision #9e32f229d4](https://github.com/MariaDB/server/commit/9e32f229d4)\
  2021-08-29 13:07:28 +0200
  * plugin can signal that it cannot be unloaded by failing deinit()
* [Revision #193314f402](https://github.com/MariaDB/server/commit/193314f402)\
  2021-08-29 13:01:31 +0200
  * show "dying" state in I\_S.PLUGINS
* [Revision #06a8412b16](https://github.com/MariaDB/server/commit/06a8412b16)\
  2021-08-28 18:19:56 +0200
  * cleanup: plugin unload
* Merge [Revision #3050d5e80e](https://github.com/MariaDB/server/commit/3050d5e80e) 2021-10-27 14:08:52 +0300 - Merge 10.6 into 10.7
* Merge [Revision #da46c37bc7](https://github.com/MariaDB/server/commit/da46c37bc7) 2021-10-27 10:24:08 +0300 - Merge 10.6 into 10.7
* [Revision #c437497e14](https://github.com/MariaDB/server/commit/c437497e14)\
  2021-10-27 10:22:23 +0300
  * [MDEV-22166](https://jira.mariadb.org/browse/MDEV-22166) fixup: Undefined reference to WFRM\_WRITE\_EXTRACTED
* [Revision #91fe87c7a8](https://github.com/MariaDB/server/commit/91fe87c7a8)\
  2021-10-27 08:41:11 +0300
  * [MDEV-22166](https://jira.mariadb.org/browse/MDEV-22166): Fix cmake -DPLUGIN\_PARTITION=NO
* [Revision #92f7d008ab](https://github.com/MariaDB/server/commit/92f7d008ab)\
  2021-10-18 20:30:04 +0530
  * [MDEV-26844](https://jira.mariadb.org/browse/MDEV-26844): DELETE returns ROW\_NUMBER=1 for every row upon ER\_TRUNCATED\_WRONG\_VALUE
* [Revision #e13dc7d0d0](https://github.com/MariaDB/server/commit/e13dc7d0d0)\
  2021-10-18 13:27:36 +0530
  * [MDEV-26830](https://jira.mariadb.org/browse/MDEV-26830): Wrong ROW\_NUMBER in diagnostics upon INSERT IGNORE with CHECK violation
* [Revision #797bd73cfa](https://github.com/MariaDB/server/commit/797bd73cfa)\
  2021-10-17 16:24:31 +0530
  * [MDEV-26841](https://jira.mariadb.org/browse/MDEV-26841): ROW\_NUMBER is not set and differs from the message upon ER\_WRONG\_VALUE\_COUNT\_ON\_ROW for the 1st row
* [Revision #635be990ca](https://github.com/MariaDB/server/commit/635be990ca)\
  2021-10-17 17:58:53 +0530
  * [MDEV-26842](https://jira.mariadb.org/browse/MDEV-26842): ROW\_NUMBER is not set and differs from the message upon WARN\_DATA\_TRUNCATED produced by inplace ALTER
* [Revision #21d03cb08a](https://github.com/MariaDB/server/commit/21d03cb08a)\
  2021-10-07 12:03:34 +0200
  * [MDEV-26654](https://jira.mariadb.org/browse/MDEV-26654) ROW\_NUMBER is wrong upon INSERT into Federated table
* [Revision #5c0b63458b](https://github.com/MariaDB/server/commit/5c0b63458b)\
  2021-10-07 18:19:56 +0200
  * [MDEV-26693](https://jira.mariadb.org/browse/MDEV-26693) ROW\_NUMBER is wrong upon INSERT or UPDATE on Spider table
* [Revision #9bbd328254](https://github.com/MariaDB/server/commit/9bbd328254)\
  2021-10-08 18:44:04 +0200
  * fix RESIGNAL to save and pass the m\_row\_count too
* [Revision #b73b736506](https://github.com/MariaDB/server/commit/b73b736506)\
  2021-10-08 18:43:56 +0200
  * refactor THD::raise\_condition() family
* [Revision #a398fcbff6](https://github.com/MariaDB/server/commit/a398fcbff6)\
  2021-10-02 20:50:18 +0200
  * [MDEV-26635](https://jira.mariadb.org/browse/MDEV-26635) ROW\_NUMBER is not 0 for errors not caused because of rows
* [Revision #f845a98354](https://github.com/MariaDB/server/commit/f845a98354)\
  2021-10-02 19:44:40 +0200
  * the error should be on the second row, not the first
* [Revision #ff5de38d6c](https://github.com/MariaDB/server/commit/ff5de38d6c)\
  2021-10-15 00:40:06 +0530
  * [MDEV-26832](https://jira.mariadb.org/browse/MDEV-26832): ROW\_NUMBER in SIGNAL/RESIGNAL causes a syntax error
* [Revision #b15a5f6fff](https://github.com/MariaDB/server/commit/b15a5f6fff)\
  2021-10-11 15:28:00 +0300
  * [MDEV-26767](https://jira.mariadb.org/browse/MDEV-26767) Server crashes when rename table and alter storage engine
* [Revision #69724805bc](https://github.com/MariaDB/server/commit/69724805bc)\
  2021-09-28 12:40:06 +0300
  * [MDEV-22165](https://jira.mariadb.org/browse/MDEV-22165) CONVERT TABLE: move in partition from existing table
* [Revision #7da721be31](https://github.com/MariaDB/server/commit/7da721be31)\
  2021-09-27 15:53:52 +0300
  * Review and crash-safety fix
* [Revision #428024524c](https://github.com/MariaDB/server/commit/428024524c)\
  2021-09-12 19:06:18 +0200
  * cleanup: reduce error injection noise in partitioning
* [Revision #b7bba721ee](https://github.com/MariaDB/server/commit/b7bba721ee)\
  2021-09-09 11:58:46 +0300
  * [MDEV-22166](https://jira.mariadb.org/browse/MDEV-22166) CONVERT PARTITION: move out partition into a table
* [Revision #f6b0e34c38](https://github.com/MariaDB/server/commit/f6b0e34c38)\
  2021-09-09 11:58:46 +0300
  * [MDEV-26471](https://jira.mariadb.org/browse/MDEV-26471) Syntax extension: do not require PARTITION keyword in partition definition
* [Revision #379ddf4921](https://github.com/MariaDB/server/commit/379ddf4921)\
  2021-08-26 18:54:17 +0700
  * [MDEV-22165](https://jira.mariadb.org/browse/MDEV-22165): Prerequisite patch that adds missing data member initializers in constructors of the class Alter\_table\_ctx
* [Revision #d324c03d0c](https://github.com/MariaDB/server/commit/d324c03d0c)\
  2021-09-09 11:58:45 +0300
  * Vanilla cleanups and refactorings
* [Revision #2dc3c32070](https://github.com/MariaDB/server/commit/2dc3c32070)\
  2021-04-22 10:47:05 +0300
  * [MDEV-25292](https://jira.mariadb.org/browse/MDEV-25292) Better debug trace
* [Revision #045757af4c](https://github.com/MariaDB/server/commit/045757af4c)\
  2021-10-22 17:32:18 +0300
  * [MDEV-24621](https://jira.mariadb.org/browse/MDEV-24621) In bulk insert, pre-sort and build indexes one page at a time
* Merge [Revision #c8e309a6ac](https://github.com/MariaDB/server/commit/c8e309a6ac) 2021-10-26 15:01:22 +0300 - Merge 10.6 into 10.7
* [Revision #2897ef099c](https://github.com/MariaDB/server/commit/2897ef099c)\
  2021-10-25 21:33:16 +0200
  * libfmt fix for cmake <3.0
* [Revision #f9339759d4](https://github.com/MariaDB/server/commit/f9339759d4)\
  2021-10-25 12:40:00 +0200
  * [MDEV-26890](https://jira.mariadb.org/browse/MDEV-26890) : Crash on shutdown, with active binlog dump threads
* [Revision #30009f2999](https://github.com/MariaDB/server/commit/30009f2999)\
  2021-10-25 10:46:20 +0200
  * Fix 32bit build
* [Revision #35084c5a96](https://github.com/MariaDB/server/commit/35084c5a96)\
  2021-10-25 09:45:54 +0200
  * [MDEV-19275](https://jira.mariadb.org/browse/MDEV-19275) : Fix compiler error - calling covention mismatch (32bit Windows)
* [Revision #9624bb0fa5](https://github.com/MariaDB/server/commit/9624bb0fa5)\
  2021-10-22 14:10:45 +0300
  * Fixed mysqld--help.result if password-reuse-check is compiled in static
* [Revision #6bfaa68c62](https://github.com/MariaDB/server/commit/6bfaa68c62)\
  2021-10-22 14:42:00 +0300
  * [MDEV-26882](https://jira.mariadb.org/browse/MDEV-26882) InnoDB number of trx pools note improvement
* Merge [Revision #71d4ecf182](https://github.com/MariaDB/server/commit/71d4ecf182) 2021-10-22 14:41:47 +0300 - Merge 10.6 into 10.7
* [Revision #45a376dd2d](https://github.com/MariaDB/server/commit/45a376dd2d)\
  2021-10-20 12:02:52 +0200
  * [MDEV-26647](https://jira.mariadb.org/browse/MDEV-26647) (reuse info) Include password validation plugin information in the error message if the SQL statement is not satisfied password policy
* [Revision #3f4eb6073f](https://github.com/MariaDB/server/commit/3f4eb6073f)\
  2021-09-16 11:10:14 +0400
  * [MDEV-19275](https://jira.mariadb.org/browse/MDEV-19275) SQL service for plugins.
* [Revision #072ef0091a](https://github.com/MariaDB/server/commit/072ef0091a)\
  2021-09-16 13:54:18 +1000
  * [MDEV-9245](https://jira.mariadb.org/browse/MDEV-9245): Deb packaging include password\_reuse\_check.so
* [Revision #3e7d4a8380](https://github.com/MariaDB/server/commit/3e7d4a8380)\
  2021-09-15 19:51:22 +0200
  * don't init ddl\_log on --help
* [Revision #abbc8821dc](https://github.com/MariaDB/server/commit/abbc8821dc)\
  2021-09-15 12:53:21 +0200
  * columnstore compilation fixes
* [Revision #a1b0997d03](https://github.com/MariaDB/server/commit/a1b0997d03)\
  2021-09-15 12:49:34 +0200
  * windows
* [Revision #bc82b6c03b](https://github.com/MariaDB/server/commit/bc82b6c03b)\
  2021-08-19 13:30:45 +0200
  * [MDEV-9245](https://jira.mariadb.org/browse/MDEV-9245) password "reuse prevention" validation plugin
* [Revision #9d1a8665cb](https://github.com/MariaDB/server/commit/9d1a8665cb)\
  2021-08-20 14:03:56 +0200
  * Pre requiste [MDEV-9245](https://jira.mariadb.org/browse/MDEV-9245): add host to validate password interface
* [Revision #26c1311c39](https://github.com/MariaDB/server/commit/26c1311c39)\
  2021-09-15 08:37:29 +0200
  * compilation failures on Windows
* [Revision #585d88a237](https://github.com/MariaDB/server/commit/585d88a237)\
  2021-09-13 09:21:47 +0400
  * [MDEV-19275](https://jira.mariadb.org/browse/MDEV-19275) SQL service for plugins.
* [Revision #e1f9a80900](https://github.com/MariaDB/server/commit/e1f9a80900)\
  2021-09-10 17:15:22 +0400
  * [MDEV-19275](https://jira.mariadb.org/browse/MDEV-19275) SQL service for plugins.
* [Revision #74daa97adf](https://github.com/MariaDB/server/commit/74daa97adf)\
  2021-09-10 13:03:48 +0200
  * a plugin shouldn't need any other includes besised plugin\_xxx.h
* [Revision #a786c0208e](https://github.com/MariaDB/server/commit/a786c0208e)\
  2021-09-10 12:38:53 +0200
  * remove MYSQL\_SERVER requirement
* [Revision #0a0dfd63d9](https://github.com/MariaDB/server/commit/0a0dfd63d9)\
  2021-09-06 22:34:35 +0400
  * [MDEV-19275](https://jira.mariadb.org/browse/MDEV-19275) Provide SQL service to plugins.
* [Revision #401ff6994d](https://github.com/MariaDB/server/commit/401ff6994d)\
  2021-09-03 06:38:54 +0200
  * [MDEV-26221](https://jira.mariadb.org/browse/MDEV-26221): DYNAMIC\_ARRAY use size\_t for sizes
* [Revision #9ab0d07e10](https://github.com/MariaDB/server/commit/9ab0d07e10)\
  2021-10-15 15:52:16 +0530
  * [MDEV-26836](https://jira.mariadb.org/browse/MDEV-26836): ROW\_NUMBER differs from the number in the error message upon ER\_WARN\_DATA\_OUT\_OF\_RANGE
* [Revision #a6cf8b34a8](https://github.com/MariaDB/server/commit/a6cf8b34a8)\
  2021-10-12 10:17:52 +0200
  * [MDEV-26806](https://jira.mariadb.org/browse/MDEV-26806) Server crash in Charset::charset / Item\_func\_natural\_sort\_key::val\_str
* [Revision #bc09362eb3](https://github.com/MariaDB/server/commit/bc09362eb3)\
  2021-10-11 09:27:38 +0200
  * [MDEV-26796](https://jira.mariadb.org/browse/MDEV-26796) Natural sort does not work for utf32/utf16/ucs2
* [Revision #5b5a67b2a9](https://github.com/MariaDB/server/commit/5b5a67b2a9)\
  2021-10-07 19:52:18 +0200
  * [MDEV-26786](https://jira.mariadb.org/browse/MDEV-26786) Inserting NULL into base column breaks NATURAL\_SORT\_KEY column
* [Revision #6c5c1fd55a](https://github.com/MariaDB/server/commit/6c5c1fd55a)\
  2021-09-01 17:44:24 +0200
  * [MDEV-4742](https://jira.mariadb.org/browse/MDEV-4742) - remove leading zero handling, and cleanups.
* [Revision #167d250924](https://github.com/MariaDB/server/commit/167d250924)\
  2021-08-30 13:28:45 +0200
  * [MDEV-4742](https://jira.mariadb.org/browse/MDEV-4742) additions
* [Revision #b3cedf63a3](https://github.com/MariaDB/server/commit/b3cedf63a3)\
  2021-08-25 14:19:10 +0200
  * [MDEV-4742](https://jira.mariadb.org/browse/MDEV-4742) - address review comments.
* [Revision #5b29d407f6](https://github.com/MariaDB/server/commit/5b29d407f6)\
  2021-07-29 13:28:11 +0200
  * [MDEV-4742](https://jira.mariadb.org/browse/MDEV-4742) - provide function to sort string in "natural" order
* Merge [Revision #b4911f5a34](https://github.com/MariaDB/server/commit/b4911f5a34) 2021-10-13 16:37:12 +0300 - Merge 10.6 into 10.7
* [Revision #8c5e5e1be9](https://github.com/MariaDB/server/commit/8c5e5e1be9)\
  2021-10-13 09:05:56 +1100
  * Deb: zstd to disabled in stretch
* [Revision #6ba63f86e7](https://github.com/MariaDB/server/commit/6ba63f86e7)\
  2021-10-12 23:00:09 +0600
  * fix C++20 !!! build failure: iterator concept was not fully implemented
* [Revision #57bf8c1f35](https://github.com/MariaDB/server/commit/57bf8c1f35)\
  2021-10-09 16:00:13 +0200
  * [MDEV-26646](https://jira.mariadb.org/browse/MDEV-26646) SFORMAT Does not allow @variable use
* [Revision #6a7c10de92](https://github.com/MariaDB/server/commit/6a7c10de92)\
  2021-10-09 15:35:22 +0200
  * [MDEV-26691](https://jira.mariadb.org/browse/MDEV-26691) SFORMAT: Pass down FLOAT as FLOAT, without upcast to DOUBLE
* [Revision #284ed64336](https://github.com/MariaDB/server/commit/284ed64336)\
  2021-09-23 16:34:13 +0200
  * Fix broken build dependency, when compiling without perfschema
* [Revision #62d4e7e2df](https://github.com/MariaDB/server/commit/62d4e7e2df)\
  2021-09-23 12:26:21 +0200
  * remove auto-switch between char and string based on the string length
* [Revision #ba7287df61](https://github.com/MariaDB/server/commit/ba7287df61)\
  2021-09-18 13:53:00 +0200
  * disallow old <7.0 fmt
* [Revision #513c8b4c25](https://github.com/MariaDB/server/commit/513c8b4c25)\
  2021-09-06 09:37:33 +0200
  * cannot allocate a new String\[] in the ::val\_str() method
* [Revision #8150f52e47](https://github.com/MariaDB/server/commit/8150f52e47)\
  2021-09-05 13:09:40 +0200
  * support charsets with mbminlen > 1
* [Revision #fe65ca0176](https://github.com/MariaDB/server/commit/fe65ca0176)\
  2021-09-05 11:37:41 +0200
  * don't build bundled libfmt, we use it in header-only mode anyway
* [Revision #6777c67a39](https://github.com/MariaDB/server/commit/6777c67a39)\
  2021-09-05 11:30:08 +0200
  * support {:L} with a ',' thousand separator
* [Revision #519bb2e41c](https://github.com/MariaDB/server/commit/519bb2e41c)\
  2021-09-05 10:18:24 +0200
  * disallow {:p}
* [Revision #a363ccd681](https://github.com/MariaDB/server/commit/a363ccd681)\
  2021-09-04 23:11:54 +0200
  * misc cleanups
* [Revision #e214e60201](https://github.com/MariaDB/server/commit/e214e60201)\
  2021-06-15 22:52:51 +0200
  * [MDEV-25015](https://jira.mariadb.org/browse/MDEV-25015) Custom formatting of strings in MariaDB queries
* [Revision #cd390af982](https://github.com/MariaDB/server/commit/cd390af982)\
  2021-09-30 12:45:19 +0200
  * [MDEV-26637](https://jira.mariadb.org/browse/MDEV-26637): (hash) ASAN: main.metadata and user\_variables.basic MTR failures after [MDEV-26572](https://jira.mariadb.org/browse/MDEV-26572)
* [Revision #3c0f48a4c1](https://github.com/MariaDB/server/commit/3c0f48a4c1)\
  2021-09-30 11:45:51 +0200
  * [MDEV-26637](https://jira.mariadb.org/browse/MDEV-26637): (roles) ASAN: main.metadata and user\_variables.basic MTR failures after [MDEV-26572](https://jira.mariadb.org/browse/MDEV-26572)
* [Revision #8f7edb784f](https://github.com/MariaDB/server/commit/8f7edb784f)\
  2021-09-30 10:56:45 +0200
  * [MDEV-26637](https://jira.mariadb.org/browse/MDEV-26637): (variables) ASAN: main.metadata and user\_variables.basic MTR failures after [MDEV-26572](https://jira.mariadb.org/browse/MDEV-26572)
* [Revision #af8b2c6cec](https://github.com/MariaDB/server/commit/af8b2c6cec)\
  2021-09-30 10:14:56 +0200
  * [MDEV-26637](https://jira.mariadb.org/browse/MDEV-26637): (plugin) ASAN: main.metadata and user\_variables.basic MTR failures after [MDEV-26572](https://jira.mariadb.org/browse/MDEV-26572)
* [Revision #763bdee81b](https://github.com/MariaDB/server/commit/763bdee81b)\
  2021-09-30 10:14:28 +0200
  * [MDEV-26637](https://jira.mariadb.org/browse/MDEV-26637): (explicit length) ASAN: main.metadata and user\_variables.basic MTR failures after [MDEV-26572](https://jira.mariadb.org/browse/MDEV-26572)
* [Revision #6cf7d6a093](https://github.com/MariaDB/server/commit/6cf7d6a093)\
  2021-10-11 11:32:05 -0700
  * Deb: Sync build and runtime dependencies from downstream to upstream
* [Revision #5cc9cf9a05](https://github.com/MariaDB/server/commit/5cc9cf9a05)\
  2021-10-06 23:43:16 +0530
  * [MDEV-26681](https://jira.mariadb.org/browse/MDEV-26681): ROW\_NUMBER is not available within compound statement blocks
* [Revision #af95c991dd](https://github.com/MariaDB/server/commit/af95c991dd)\
  2021-10-06 23:36:14 +0530
  * [MDEV-26684](https://jira.mariadb.org/browse/MDEV-26684): Unexpected ROW\_NUMBER in a condition raised by a diagnostics statement
* [Revision #479e303ef3](https://github.com/MariaDB/server/commit/479e303ef3)\
  2021-09-26 01:30:36 +0530
  * [MDEV-26606](https://jira.mariadb.org/browse/MDEV-26606): ROW\_NUMBER property value isn't passed from inside a stored procedure
* Merge [Revision #25921c997e](https://github.com/MariaDB/server/commit/25921c997e) 2021-10-06 10:28:59 +0300 - Merge 10.6 into 10.7
* Merge [Revision #b7ff385d43](https://github.com/MariaDB/server/commit/b7ff385d43) 2021-10-05 19:28:18 +0300 - Merge 10.6 into 10.7
* [Revision #9791d4b4af](https://github.com/MariaDB/server/commit/9791d4b4af)\
  2021-10-05 19:28:09 +0300
  * After-merge fix: Correct s3.mysqldump result
* Merge [Revision #822066acfc](https://github.com/MariaDB/server/commit/822066acfc) 2021-10-05 13:38:53 +0300 - Merge 10.6 into 10.7
* [Revision #d5e606c605](https://github.com/MariaDB/server/commit/d5e606c605)\
  2021-09-29 14:18:40 +0530
  * [MDEV-26611](https://jira.mariadb.org/browse/MDEV-26611): ERROR\_INDEX isn't intuitively clear
* [Revision #e9d8002721](https://github.com/MariaDB/server/commit/e9d8002721)\
  2021-10-04 21:41:41 +1100
  * [MDEV-25152](https://jira.mariadb.org/browse/MDEV-25152): mysqldump - test fix for s3.mysqldump
* [Revision #4930209b12](https://github.com/MariaDB/server/commit/4930209b12)\
  2021-10-01 09:15:10 +1000
  * [MDEV-25152](https://jira.mariadb.org/browse/MDEV-25152): Insert linebreaks in mysqldump --extended-insert
* [Revision #586d6a2520](https://github.com/MariaDB/server/commit/586d6a2520)\
  2021-06-06 15:09:36 +0100
  * [MDEV-25152](https://jira.mariadb.org/browse/MDEV-25152) Insert linebreaks in mysqldump --extended-insert
* Merge [Revision #b36d6f92a8](https://github.com/MariaDB/server/commit/b36d6f92a8) 2021-09-30 11:01:07 +0300 - Merge 10.6 into 10.7
* [Revision #8dd4794c4e](https://github.com/MariaDB/server/commit/8dd4794c4e)\
  2021-09-24 17:26:01 +0200
  * bump the VERSION
* Merge [Revision #79185bd056](https://github.com/MariaDB/server/commit/79185bd056) 2021-09-24 15:32:39 +0300 - Merge 10.6 into 10.7
* [Revision #359c286499](https://github.com/MariaDB/server/commit/359c286499)\
  2021-09-14 19:01:26 +0200
  * [MDEV-26520](https://jira.mariadb.org/browse/MDEV-26520) Make innodb\_purge\_threads dynamic
* Merge [Revision #2255649939](https://github.com/MariaDB/server/commit/2255649939) 2021-09-17 20:23:17 +0300 - Merge 10.6 into 10.7
* [Revision #d552e092c9](https://github.com/MariaDB/server/commit/d552e092c9)\
  2021-09-15 15:54:49 +0200
  * [MDEV-10075](https://jira.mariadb.org/browse/MDEV-10075): Provide index of error causing error in array INSERT
* [Revision #0ff8976e12](https://github.com/MariaDB/server/commit/0ff8976e12)\
  2021-09-15 16:03:13 +0200
  * remove more tablespace tests
* [Revision #9d65d2f9d0](https://github.com/MariaDB/server/commit/9d65d2f9d0)\
  2021-09-15 11:11:00 +0200
  * fix tests after ea06c67a49c
* [Revision #ea06c67a49](https://github.com/MariaDB/server/commit/ea06c67a49)\
  2021-07-31 12:55:21 +0530
  * [MDEV-10075](https://jira.mariadb.org/browse/MDEV-10075): Provide index of error causing error in array INSERT
* [Revision #50e08f3da0](https://github.com/MariaDB/server/commit/50e08f3da0)\
  2021-09-15 08:55:21 +0200
  * remove more tablespace tests
* [Revision #8d08971c84](https://github.com/MariaDB/server/commit/8d08971c84)\
  2021-09-14 16:15:30 +0300
  * Removed CREATE/DROP TABLESPACE and related commands
* [Revision #267a07e846](https://github.com/MariaDB/server/commit/267a07e846)\
  2021-08-24 00:45:39 +0300
  * [MDEV-26307](https://jira.mariadb.org/browse/MDEV-26307) multi-source-replication support mysql syntax(for channel)
* [Revision #4ebaa80f0b](https://github.com/MariaDB/server/commit/4ebaa80f0b)\
  2021-08-24 00:38:30 +0300
  * Failed change master could leave around old relay log files
* [Revision #0629711db4](https://github.com/MariaDB/server/commit/0629711db4)\
  2021-09-08 11:42:42 +0400
  * [MDEV-26572](https://jira.mariadb.org/browse/MDEV-26572) Improve simple multibyte collation performance on the ASCII range
* Merge [Revision #4be366111b](https://github.com/MariaDB/server/commit/4be366111b) 2021-09-11 18:01:31 +0300 - Merge 10.6 into 10.7
* [Revision #7614965076](https://github.com/MariaDB/server/commit/7614965076)\
  2021-09-06 19:56:45 +0200
  * fix spider SERVER\_NAME detection
* [Revision #d0a1ea3aca](https://github.com/MariaDB/server/commit/d0a1ea3aca)\
  2021-09-06 17:03:11 +0200
  * increase the version string buffer in mariadb-upgrade
* Merge [Revision #e836673cc7](https://github.com/MariaDB/server/commit/e836673cc7) 2021-09-07 10:37:49 +0300 - Merge 10.6 into 10.7
* Merge [Revision #42ad4fa346](https://github.com/MariaDB/server/commit/42ad4fa346) 2021-09-06 16:23:49 +0300 - Merge 10.6 into 10.7
* [Revision #1bc82aaf0a](https://github.com/MariaDB/server/commit/1bc82aaf0a)\
  2021-08-20 12:54:53 +0300
  * [MDEV-26352](https://jira.mariadb.org/browse/MDEV-26352) : Add new thread states for certain WSREP scenarios
* Merge [Revision #21ce69123c](https://github.com/MariaDB/server/commit/21ce69123c) 2021-09-01 14:36:55 +0300 - Merge 10.6 into 10.7
* Merge [Revision #9a320ad1e4](https://github.com/MariaDB/server/commit/9a320ad1e4) 2021-08-31 15:39:18 +0300 - Merge 10.6 into 10.7
* Merge [Revision #2e64145921](https://github.com/MariaDB/server/commit/2e64145921) 2021-08-31 15:07:39 +0300 - Merge 10.6 into 10.7
* Merge [Revision #58aaa67064](https://github.com/MariaDB/server/commit/58aaa67064) 2021-08-31 11:01:19 +0300 - Merge 10.6 into 10.7
* [Revision #9eee9c6789](https://github.com/MariaDB/server/commit/9eee9c6789)\
  2018-07-17 15:09:18 +0300
  * [MDEV-16355](https://jira.mariadb.org/browse/MDEV-16355) Add option for mysqldump to read data as of specific timestamp from system-versioned tables
* [Revision #0860b17ef3](https://github.com/MariaDB/server/commit/0860b17ef3)\
  2021-08-23 15:54:07 +0200
  * [MDEV-26452](https://jira.mariadb.org/browse/MDEV-26452) SIGSEGV in Item::cleanup from Item::cleanup\_processor
* [Revision #0299ec29d4](https://github.com/MariaDB/server/commit/0299ec29d4)\
  2021-07-17 08:57:29 +0200
  * cleanup: MY\_BITMAP mutex
* Merge [Revision #05e29e177d](https://github.com/MariaDB/server/commit/05e29e177d) 2021-08-26 15:40:28 +0300 - Merge 10.6 into 10.7
* [Revision #6a987149a8](https://github.com/MariaDB/server/commit/6a987149a8)\
  2021-08-25 17:41:43 +1000
  * [MDEV-26474](https://jira.mariadb.org/browse/MDEV-26474): Fix mysql\_setpermission hostname logic
* Merge [Revision #64f7dffcc7](https://github.com/MariaDB/server/commit/64f7dffcc7) 2021-08-23 11:28:08 +0300 - Merge 10.6 into 10.7
* Merge [Revision #3bf42eb21b](https://github.com/MariaDB/server/commit/3bf42eb21b) 2021-08-19 13:03:48 +0300 - Merge 10.6 into 10.7
* Merge [Revision #c949772680](https://github.com/MariaDB/server/commit/c949772680) 2021-08-16 08:24:00 +0300 - Merge 10.6 into 10.7
* [Revision #52505bf20d](https://github.com/MariaDB/server/commit/52505bf20d)\
  2021-08-06 11:36:13 +0300
  * [MDEV-24947](https://jira.mariadb.org/browse/MDEV-24947) : Remove parameter wsrep\_replicate\_myisam
* [Revision #14731d7635](https://github.com/MariaDB/server/commit/14731d7635)\
  2021-08-06 10:23:53 +0300
  * [MDEV-24843](https://jira.mariadb.org/browse/MDEV-24843) : Remove parameter wsrep\_strict\_ddl
* [Revision #5982734eac](https://github.com/MariaDB/server/commit/5982734eac)\
  2021-08-06 11:27:52 +0300
  * Fix json\_normalize asan
* Merge [Revision #ddcb242b3c](https://github.com/MariaDB/server/commit/ddcb242b3c) 2021-08-04 11:52:39 +0300 - Merge 10.6 into 10.7
* [Revision #c5ae2c4971](https://github.com/MariaDB/server/commit/c5ae2c4971)\
  2021-07-30 12:38:35 +0300
  * [MDEV-26195](https://jira.mariadb.org/browse/MDEV-26195) fixup: Inconsistent types for template instantiation
* [Revision #a880ef57ef](https://github.com/MariaDB/server/commit/a880ef57ef)\
  2021-07-24 21:42:03 +0300
  * [MDEV-26195](https://jira.mariadb.org/browse/MDEV-26195) fixup: Format mismatch in mariadb-backup
* [Revision #fea8375893](https://github.com/MariaDB/server/commit/fea8375893)\
  2021-07-23 10:10:08 +0300
  * [MDEV-26195](https://jira.mariadb.org/browse/MDEV-26195) fixup: Fix format mismatch
* Merge [Revision #b857fde69a](https://github.com/MariaDB/server/commit/b857fde69a) 2021-07-22 14:36:42 +0300 - Merge 10.6 into 10.7
* [Revision #491806942e](https://github.com/MariaDB/server/commit/491806942e)\
  2021-07-22 14:36:30 +0300
  * [MDEV-26195](https://jira.mariadb.org/browse/MDEV-26195) fixup: Fix -Wconversion in innochecksum
* [Revision #ca501ffb04](https://github.com/MariaDB/server/commit/ca501ffb04)\
  2021-07-22 11:22:47 +0300
  * [MDEV-26195](https://jira.mariadb.org/browse/MDEV-26195): Use a 32-bit data type for some tablespace fields
* Merge [Revision #cee37b5d26](https://github.com/MariaDB/server/commit/cee37b5d26) 2021-07-22 11:22:09 +0300 - Merge 10.6 into 10.7
* [Revision #593885f785](https://github.com/MariaDB/server/commit/593885f785)\
  2021-07-02 08:20:37 +0200
  * [MDEV-23143](https://jira.mariadb.org/browse/MDEV-23143) Add JSON\_EQUALS function
* [Revision #fcde341764](https://github.com/MariaDB/server/commit/fcde341764)\
  2021-07-02 08:18:16 +0200
  * [MDEV-16375](https://jira.mariadb.org/browse/MDEV-16375) Function to normalize a json value
* [Revision #105e4148bf](https://github.com/MariaDB/server/commit/105e4148bf)\
  2021-07-02 07:59:56 +0200
  * Add json\_normalize function to json\_lib
* [Revision #7b587fcbe7](https://github.com/MariaDB/server/commit/7b587fcbe7)\
  2021-05-23 14:16:01 +0000
  * fix json typo s/UNINITALIZED/UNINITIALIZED/
* [Revision #71ed8c136f](https://github.com/MariaDB/server/commit/71ed8c136f)\
  2021-07-19 14:55:56 +0300
  * Test cases require debug\_sync enabled
* [Revision #fcbb2a1df1](https://github.com/MariaDB/server/commit/fcbb2a1df1)\
  2021-07-03 03:39:15 +0300
  * Make marking/testing of top level item uniform
* [Revision #f069aa1dc2](https://github.com/MariaDB/server/commit/f069aa1dc2)\
  2021-06-18 16:49:52 +0300
  * Update debian packaging for 10.7
* [Revision #b1d81974b2](https://github.com/MariaDB/server/commit/b1d81974b2)\
  2021-06-18 18:40:05 +0300
  * Added support to MEM\_ROOT for write protected memory
* [Revision #d378a466a5](https://github.com/MariaDB/server/commit/d378a466a5)\
  2021-06-18 14:36:52 +0300
  * Change Item\_true and Item\_false to pointers
* Merge [Revision #b32b1f2b19](https://github.com/MariaDB/server/commit/b32b1f2b19) 2021-07-18 19:39:45 +0300 - Merge remote-tracking branch '10.6' into 10.7
* [Revision #2c4d1fb544](https://github.com/MariaDB/server/commit/2c4d1fb544)\
  2021-01-14 14:35:45 +0100
  * Typo fix in extrabackup.cc and innobackupex.cc
* [Revision #f7216fa63d](https://github.com/MariaDB/server/commit/f7216fa63d)\
  2020-06-10 09:07:15 +0200
  * [MDEV-12914](https://jira.mariadb.org/browse/MDEV-12914): Engine for temporary tables which are implicitly created as RocksDB is substituted silently
* Merge [Revision #57f14eab20](https://github.com/MariaDB/server/commit/57f14eab20) 2021-07-07 19:23:54 +0200 - Merge branch '10.6' into 10.7
* [Revision #fe7971fab8](https://github.com/MariaDB/server/commit/fe7971fab8)\
  2021-07-06 23:48:10 +0200
  * update ColumnStore for 10.7
* [Revision #d88b443446](https://github.com/MariaDB/server/commit/d88b443446)\
  2021-07-06 16:49:58 +0200
  * debian update for 10.7
* [Revision #b836f84b31](https://github.com/MariaDB/server/commit/b836f84b31)\
  2021-07-06 16:38:16 +0200
  * update test results
* [Revision #76f4a78ba2](https://github.com/MariaDB/server/commit/76f4a78ba2)\
  2021-06-19 16:40:04 +0900
  * Spider fix for 10.7
* [Revision #3eef28a9f5](https://github.com/MariaDB/server/commit/3eef28a9f5)\
  2021-06-02 14:51:52 +0300
  * Change version to 10.7.0

{% include "https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/~/reusable/vX1KAy0t1XuYJaGsK28T/" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
