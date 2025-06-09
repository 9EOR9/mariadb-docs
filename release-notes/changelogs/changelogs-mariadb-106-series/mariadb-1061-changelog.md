# MariaDB 10.6.1 Changelog

The most recent release of [MariaDB 10.6](../../mariadb-community-server-release-notes/mariadb-10-6-series/what-is-mariadb-106.md) is:[**MariaDB 10.6.21**](../../mariadb-community-server-release-notes/mariadb-10-6-series/mariadb-10-6-21-release-notes.md) Stable (GA) [Download Now](https://mariadb.com/downloads/)[_Alternate download from mariadb.org_](https://downloads.mariadb.org/mariadb/10.6.21/)

[Download 10.6.1](https://downloads.mariadb.org/mariadb/10.6.1/)[Release Notes](../../mariadb-community-server-release-notes/mariadb-10-6-series/mariadb-1061-release-notes.md)[Changelog](mariadb-1061-changelog.md)[Overview of 10.6](../../mariadb-community-server-release-notes/mariadb-10-6-series/what-is-mariadb-106.md)

**Release date:** 21 May 2021

**Do not use&#x20;**_**beta**_**&#x20;releases in production!**

For the highlights of this release, see the[release notes](../../mariadb-community-server-release-notes/mariadb-10-6-series/mariadb-1061-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/server/tree/10.6) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Includes all fixes from [MariaDB 10.5.10](../changelogs-mariadb-105-series/mariadb-10510-changelog.md)
* [Revision #00a8357bd3](https://github.com/MariaDB/server/commit/00a8357bd3)\
  2021-05-21 01:00:32 +0200
  * update test result
* [Revision #57094b4fe2](https://github.com/MariaDB/server/commit/57094b4fe2)\
  2021-05-20 23:47:00 +0200
  * 10.6.1 is beta
* [Revision #fd713f26f3](https://github.com/MariaDB/server/commit/fd713f26f3)\
  2021-05-20 18:33:07 +0200
  * mariadb-conv --character-sets-dir
* [Revision #4e946cb1f1](https://github.com/MariaDB/server/commit/4e946cb1f1)\
  2021-05-20 11:42:00 +0200
  * fix of [MDEV-24312](https://jira.mariadb.org/browse/MDEV-24312)
* [Revision #852d1f8eb9](https://github.com/MariaDB/server/commit/852d1f8eb9)\
  2021-05-20 16:05:52 +0200
  * compilation error with -Werror -Og
* [Revision #d8127ff76e](https://github.com/MariaDB/server/commit/d8127ff76e)\
  2021-05-20 16:05:24 +0200
  * fix main.strings test to clean up after itself
* [Revision #55ebf7f41f](https://github.com/MariaDB/server/commit/55ebf7f41f)\
  2021-05-20 10:00:49 +0200
  * another compilation fix for partition-less debug build
* [Revision #d67663a758](https://github.com/MariaDB/server/commit/d67663a758)\
  2021-05-20 09:44:16 +0200
  * fix main.sp test failures
* [Revision #1fff2398ef](https://github.com/MariaDB/server/commit/1fff2398ef)\
  2021-05-19 22:26:02 +0200
  * [MDEV-22530](https://jira.mariadb.org/browse/MDEV-22530) Aborting OPTIMIZE TABLE still logs in binary log and replicates to the Slave server
* [Revision #16d8763b87](https://github.com/MariaDB/server/commit/16d8763b87)\
  2021-05-19 16:18:47 +0200
  * fix a race condition in the main.rownum test
* [Revision #c3b5003851](https://github.com/MariaDB/server/commit/c3b5003851)\
  2021-05-19 14:55:10 +0200
  * fixes for win32
* [Revision #ecd6588454](https://github.com/MariaDB/server/commit/ecd6588454)\
  2021-05-19 14:26:26 +0200
  * show pmem detection in cmake
* [Revision #b2340cdd07](https://github.com/MariaDB/server/commit/b2340cdd07)\
  2021-05-19 14:21:32 +0200
  * fix compilation w/o partitioning
* [Revision #f44c5e5eb9](https://github.com/MariaDB/server/commit/f44c5e5eb9)\
  2021-05-17 21:24:20 +0200
  * switch columnstore from pre-alpha 6.1.1 back to 5.5.2-3 suppress columnstore boost warning
* [Revision #7700626fe6](https://github.com/MariaDB/server/commit/7700626fe6)\
  2021-05-15 13:15:41 +0200
  * remove thread\_pool\_priv.h
* [Revision #0c7b018944](https://github.com/MariaDB/server/commit/0c7b018944)\
  2021-05-11 14:09:45 +0300
  * Remove not used IPC\_COND\_USED\_INDEX
* [Revision #acf282c36b](https://github.com/MariaDB/server/commit/acf282c36b)\
  2021-05-10 18:36:13 +0300
  * [MDEV-25606](https://jira.mariadb.org/browse/MDEV-25606): Concurrent CREATE TRIGGER statements mix up in binlog and break replication
* [Revision #79d9a725f9](https://github.com/MariaDB/server/commit/79d9a725f9)\
  2021-04-30 17:08:11 +0300
  * Added checking to protect against simultaneous double free in safemalloc
* [Revision #744a53806e](https://github.com/MariaDB/server/commit/744a53806e)\
  2021-04-29 21:08:32 +0300
  * Fixed hang in concurrent DROP TABLE and BACKUP LOCK BLOCK\_DDL
* [Revision #0b59320d3d](https://github.com/MariaDB/server/commit/0b59320d3d)\
  2021-04-29 17:40:32 +0300
  * [MDEV-19198](https://jira.mariadb.org/browse/MDEV-19198) - DBUG assert in CREATE IF NOT EXIST under LOCK TABLES WRITE
* [Revision #0bc3a0801c](https://github.com/MariaDB/server/commit/0bc3a0801c)\
  2021-04-22 18:25:53 +0300
  * Added ER\_... labels to mtr fatal error messages
* [Revision #cc125bebfe](https://github.com/MariaDB/server/commit/cc125bebfe)\
  2021-04-14 13:40:36 +0300
  * Fix all warnings given by UBSAN
* [Revision #b332ffc1af](https://github.com/MariaDB/server/commit/b332ffc1af)\
  2021-04-12 19:42:55 +0300
  * Fixed assert in WSREP if one started with --wsrep\_provider=..
* [Revision #85f3ed5f8b](https://github.com/MariaDB/server/commit/85f3ed5f8b)\
  2021-04-08 12:12:24 +0300
  * Added malloc\_calls to SHOW GLOBAL STATUS for DEBUG server
* [Revision #0fceb752c5](https://github.com/MariaDB/server/commit/0fceb752c5)\
  2021-04-01 13:50:03 +0300
  * Fixes for mtr --valgrind
* [Revision #aa1626d15e](https://github.com/MariaDB/server/commit/aa1626d15e)\
  2021-03-31 13:06:12 +0300
  * Made --mariadbd a synonym for --mysqld in mysql-test-run
* [Revision #83e529eced](https://github.com/MariaDB/server/commit/83e529eced)\
  2021-03-30 17:06:55 +0300
  * [MDEV-18465](https://jira.mariadb.org/browse/MDEV-18465) Logging of DDL statements during backup
* [Revision #496a14e187](https://github.com/MariaDB/server/commit/496a14e187)\
  2021-05-14 15:27:24 +0300
  * Move debug\_crash\_here to it's own source files
* [Revision #ad02d53a71](https://github.com/MariaDB/server/commit/ad02d53a71)\
  2021-05-16 13:45:54 +0300
  * Create a backup file of ddl\_recovery.log before starting recovery
* [Revision #7762ee5dbe](https://github.com/MariaDB/server/commit/7762ee5dbe)\
  2021-03-18 12:41:08 +0200
  * [MDEV-25180](https://jira.mariadb.org/browse/MDEV-25180) Atomic ALTER TABLE [MDEV-25604](https://jira.mariadb.org/browse/MDEV-25604) Atomic DDL: Binlog event written upon recovery does not have default database
* [Revision #3c578b0a96](https://github.com/MariaDB/server/commit/3c578b0a96)\
  2021-03-22 16:05:08 +0200
  * Check if we can rename triggers before doing an ALTER TABLE ... RENAME
* [Revision #c844a76b0a](https://github.com/MariaDB/server/commit/c844a76b0a)\
  2021-03-21 17:47:56 +0200
  * Ensure that one can drop a trigger with an orphan .TRN file
* [Revision #ffe7f19fa6](https://github.com/MariaDB/server/commit/ffe7f19fa6)\
  2021-01-31 18:43:50 +0200
  * [MDEV-24746](https://jira.mariadb.org/browse/MDEV-24746) Atomic CREATE TRIGGER
* [Revision #d494abd175](https://github.com/MariaDB/server/commit/d494abd175)\
  2021-01-17 16:34:01 +0200
  * [MDEV-24607](https://jira.mariadb.org/browse/MDEV-24607) Atomic CREATE VIEW
* [Revision #6aa9a552c2](https://github.com/MariaDB/server/commit/6aa9a552c2)\
  2021-01-17 16:06:43 +0200
  * [MDEV-24576](https://jira.mariadb.org/browse/MDEV-24576) Atomic CREATE TABLE
* [Revision #7a588c30b1](https://github.com/MariaDB/server/commit/7a588c30b1)\
  2020-12-20 17:44:11 +0200
  * [MDEV-24408](https://jira.mariadb.org/browse/MDEV-24408) Crash-safe DROP DATABASE
* [Revision #407e9b78cf](https://github.com/MariaDB/server/commit/407e9b78cf)\
  2020-12-14 15:57:04 +0200
  * [MDEV-24395](https://jira.mariadb.org/browse/MDEV-24395) Atomic DROP TRIGGER
* [Revision #e3cfb7c803](https://github.com/MariaDB/server/commit/e3cfb7c803)\
  2020-12-04 18:23:40 +0200
  * [MDEV-23844](https://jira.mariadb.org/browse/MDEV-23844) Atomic DROP TABLE (single table)
* [Revision #47010ccffa](https://github.com/MariaDB/server/commit/47010ccffa)\
  2020-10-15 02:25:57 +0300
  * [MDEV-23842](https://jira.mariadb.org/browse/MDEV-23842) Atomic RENAME TABLE
* [Revision #55c771b4f3](https://github.com/MariaDB/server/commit/55c771b4f3)\
  2021-03-24 12:27:11 +0200
  * Make rename atomic/repeatable in MyISAM and Aria
* [Revision #5e7b1bad2f](https://github.com/MariaDB/server/commit/5e7b1bad2f)\
  2021-05-12 18:36:43 +0300
  * Do not display not moved tables as moved in aria\_chk
* [Revision #58f26ab9d5](https://github.com/MariaDB/server/commit/58f26ab9d5)\
  2021-03-30 17:49:48 +0300
  * Renamed comment\_length -> get\_comment
* [Revision #e45b54b75d](https://github.com/MariaDB/server/commit/e45b54b75d)\
  2021-03-28 18:50:40 +0300
  * Removed Static\_binary\_string
* [Revision #85d6278fed](https://github.com/MariaDB/server/commit/85d6278fed)\
  2021-01-26 02:20:05 +0200
  * Change replication to use uchar for all buffers instead of char
* [Revision #db9398ba5e](https://github.com/MariaDB/server/commit/db9398ba5e)\
  2021-03-15 14:53:55 +0200
  * Improved code comment and removed nop test
* [Revision #08bc062e3c](https://github.com/MariaDB/server/commit/08bc062e3c)\
  2021-01-30 14:03:23 +0200
  * Remove some usage of Check\_level\_instant\_set and Sql\_mode\_save
* [Revision #d754d3d951](https://github.com/MariaDB/server/commit/d754d3d951)\
  2021-03-15 15:45:47 +0200
  * Less noise in the error log
* [Revision #249263525f](https://github.com/MariaDB/server/commit/249263525f)\
  2021-03-18 12:48:20 +0200
  * Avoid creating the .frm file twice in some cases
* [Revision #4832e54915](https://github.com/MariaDB/server/commit/4832e54915)\
  2021-02-05 17:10:43 +0200
  * [MDEV-20025](https://jira.mariadb.org/browse/MDEV-20025): ADD\_MONTHS() Oracle function
* [Revision #eb73245e30](https://github.com/MariaDB/server/commit/eb73245e30)\
  2021-02-16 15:22:22 +0200
  * Ensure that we do not allocate strings bigger than 4G in String objects.
* [Revision #81d9bed3a4](https://github.com/MariaDB/server/commit/81d9bed3a4)\
  2021-01-24 23:56:43 +0200
  * [MDEV-20017](https://jira.mariadb.org/browse/MDEV-20017) Implement TO\_CHAR() Oracle compatible function
* [Revision #cf93209c70](https://github.com/MariaDB/server/commit/cf93209c70)\
  2021-01-05 20:46:23 +0200
  * [MDEV-20021](https://jira.mariadb.org/browse/MDEV-20021) sql\_mode="oracle" does not support MINUS set operator
* [Revision #b8c3159594](https://github.com/MariaDB/server/commit/b8c3159594)\
  2021-01-04 17:27:26 +0200
  * [MDEV-24285](https://jira.mariadb.org/browse/MDEV-24285) support oracle build-in function: sys\_guid
* [Revision #be093c81a7](https://github.com/MariaDB/server/commit/be093c81a7)\
  2021-01-04 17:03:16 +0200
  * [MDEV-24089](https://jira.mariadb.org/browse/MDEV-24089) support oracle syntax: rownum
* [Revision #f16b8590bf](https://github.com/MariaDB/server/commit/f16b8590bf)\
  2020-11-17 16:59:38 +0200
  * [MDEV-19682](https://jira.mariadb.org/browse/MDEV-19682) sql\_mode="oracle" does not support sysdate
* [Revision #7b134ffa3d](https://github.com/MariaDB/server/commit/7b134ffa3d)\
  2020-11-13 12:55:40 +0200
  * Make LEX::can\_not\_use\_merged more general
* [Revision #f2e3f0db6d](https://github.com/MariaDB/server/commit/f2e3f0db6d)\
  2020-11-04 19:39:27 +0200
  * Added comment to create\_inital\_db.cmake of how to run it
* [Revision #5ac05a6172](https://github.com/MariaDB/server/commit/5ac05a6172)\
  2020-10-18 16:36:22 +0300
  * Give a readable error in mtr if resolve\_at\_variable fails
* [Revision #188b0b99cf](https://github.com/MariaDB/server/commit/188b0b99cf)\
  2020-10-12 11:21:05 +0300
  * Rename all external ddl\_log function to start with ddl\_log\_ prefix
* [Revision #02b6cef45e](https://github.com/MariaDB/server/commit/02b6cef45e)\
  2020-10-02 15:59:06 +0300
  * Move all ddl log code to ddl\_log.cc and ddl\_log.h
* [Revision #a28ea028af](https://github.com/MariaDB/server/commit/a28ea028af)\
  2020-10-15 02:26:44 +0300
  * Indentation cleanups (break long lines)
* [Revision #f671a9dee7](https://github.com/MariaDB/server/commit/f671a9dee7)\
  2020-09-29 19:02:05 +0300
  * Replace find\_temporary\_table() with is\_temporary\_table()
* [Revision #949d10bea2](https://github.com/MariaDB/server/commit/949d10bea2)\
  2020-09-03 20:27:12 +0300
  * Don't reset StringBuffers in loops when not needed
* [Revision #a206658b98](https://github.com/MariaDB/server/commit/a206658b98)\
  2020-08-22 02:08:59 +0300
  * Change CHARSET\_INFO character set and collaction names to LEX\_CSTRING
* [Revision #b0910dddf5](https://github.com/MariaDB/server/commit/b0910dddf5)\
  2020-08-22 02:09:34 +0300
  * Fix test of characterset used with fulltext index in InnoDB
* [Revision #6de84e6f4e](https://github.com/MariaDB/server/commit/6de84e6f4e)\
  2021-05-17 00:59:51 +0200
  * cleanup: Item::can\_eval\_in\_optimize()
* [Revision #30f0a246a0](https://github.com/MariaDB/server/commit/30f0a246a0)\
  2020-08-19 02:53:22 +0300
  * Added override to all releveant methods in Item (and a few other classes)
* [Revision #53b43f3078](https://github.com/MariaDB/server/commit/53b43f3078)\
  2020-08-14 21:11:30 +0300
  * Added full\_name\_cstring()
* [Revision #b6ff139aa3](https://github.com/MariaDB/server/commit/b6ff139aa3)\
  2020-08-12 20:29:55 +0300
  * Reduce usage of strlen()
* [Revision #b3bc02f923](https://github.com/MariaDB/server/commit/b3bc02f923)\
  2020-08-14 20:22:43 +0300
  * Added ErrConvString.lex\_cstring() to simplify code
* [Revision #5c7d243b29](https://github.com/MariaDB/server/commit/5c7d243b29)\
  2020-08-13 20:17:00 +0300
  * Add support for minimum field width for strings to my\_vsnprintf()
* [Revision #8dd6ad573c](https://github.com/MariaDB/server/commit/8dd6ad573c)\
  2020-09-02 20:56:47 +0300
  * Replaced base\_flags\_t::IS\_AUTOGENERATED\_NAME with IS\_EXPLICT\_NAME
* [Revision #6079b46d8d](https://github.com/MariaDB/server/commit/6079b46d8d)\
  2020-09-02 03:13:32 +0300
  * Split item->flags into base\_flags and with\_flags
* [Revision #7ca4e381f7](https://github.com/MariaDB/server/commit/7ca4e381f7)\
  2020-08-14 19:51:10 +0300
  * Removed Item::is\_fixed() and Item::has\_subquery()
* [Revision #9448548481](https://github.com/MariaDB/server/commit/9448548481)\
  2020-08-03 13:13:39 +0300
  * Remove calls to current\_thd() in Item functions
* [Revision #3105c9e7a5](https://github.com/MariaDB/server/commit/3105c9e7a5)\
  2020-08-02 12:31:14 +0300
  * Change bitfields in Item to an uint16
* [Revision #451c4ae548](https://github.com/MariaDB/server/commit/451c4ae548)\
  2020-07-31 16:11:35 +0300
  * Renamed 'flags' variables in Item\_class
* [Revision #189d03dac5](https://github.com/MariaDB/server/commit/189d03dac5)\
  2020-07-29 13:51:47 +0300
  * Revert [MDEV-14517](https://jira.mariadb.org/browse/MDEV-14517) Cleanup for Item::with\_subselect
* [Revision #ae39f4f6d6](https://github.com/MariaDB/server/commit/ae39f4f6d6)\
  2020-07-28 19:41:05 +0300
  * Revert [MDEV-16592](https://jira.mariadb.org/browse/MDEV-16592) "Change Item::with\_sum\_func to a virtual method"
* [Revision #963e5e406d](https://github.com/MariaDB/server/commit/963e5e406d)\
  2020-08-14 11:28:39 +0300
  * Changed field\_index to use field\_index\_t instead of uint16
* [Revision #00d13069dd](https://github.com/MariaDB/server/commit/00d13069dd)\
  2020-07-28 18:18:43 +0300
  * Removed Item::common\_flags and replaced it with bit fields
* [Revision #cd1782d26a](https://github.com/MariaDB/server/commit/cd1782d26a)\
  2020-08-18 23:24:09 +0300
  * Renamed Type\_all\_attributes::set\_maybe\_null() to set\_type\_maybe\_null()
* [Revision #c6bf04ab2e](https://github.com/MariaDB/server/commit/c6bf04ab2e)\
  2020-08-14 21:13:52 +0300
  * Removed not used object Geometry::bad\_geometry\_data()
* [Revision #61822a9b5f](https://github.com/MariaDB/server/commit/61822a9b5f)\
  2020-09-02 20:51:39 +0300
  * Removed not used Item\_type\_holder() function
* [Revision #60335ba16c](https://github.com/MariaDB/server/commit/60335ba16c)\
  2020-08-17 18:42:58 +0300
  * Enable BUILD scripts to work with clang
* [Revision #163be5fd8c](https://github.com/MariaDB/server/commit/163be5fd8c)\
  2020-08-22 02:12:07 +0300
  * Remove compiler warnings regarding signed/unsigned compare in mroonga
* [Revision #e42130e9cd](https://github.com/MariaDB/server/commit/e42130e9cd)\
  2020-08-17 18:56:47 +0300
  * Fixes that enables my\_new.cc (new wrapper using my\_malloc)
* [Revision #a93c514595](https://github.com/MariaDB/server/commit/a93c514595)\
  2020-08-17 19:01:43 +0300
  * Fixed my\_addr\_resolve
* [Revision #942a5a89a9](https://github.com/MariaDB/server/commit/942a5a89a9)\
  2020-08-17 19:05:10 +0300
  * Report memory leaks from mariadbd if -T or --debug is used
* [Revision #36cdd5c3cd](https://github.com/MariaDB/server/commit/36cdd5c3cd)\
  2020-09-16 11:23:50 +0300
  * Optimize usage of c\_ptr(), c\_ptr\_quick() and String::alloc()
* [Revision #da85ad7987](https://github.com/MariaDB/server/commit/da85ad7987)\
  2020-08-14 18:56:56 +0300
  * Optimize Sql\_alloc
* [Revision #c76eabfb5e](https://github.com/MariaDB/server/commit/c76eabfb5e)\
  2020-08-27 13:09:49 +0300
  * Improved storage size for Item, Field and some other classes
* [Revision #8e8bda7fd3](https://github.com/MariaDB/server/commit/8e8bda7fd3)\
  2020-08-28 17:11:55 +0300
  * Optimize size of lex structures
* [Revision #fa7d4abf16](https://github.com/MariaDB/server/commit/fa7d4abf16)\
  2020-08-27 12:24:32 +0300
  * Added typedef decimal\_digits\_t (uint16) for number of digits in most aspects of decimals and integers
* [Revision #aee84453ab](https://github.com/MariaDB/server/commit/aee84453ab)\
  2020-07-14 18:36:05 +0300
  * [MDEV-23001](https://jira.mariadb.org/browse/MDEV-23001) Precreate static Item\_bool() to simplify code
* [Revision #78a0fe792a](https://github.com/MariaDB/server/commit/78a0fe792a)\
  2021-05-18 09:52:13 -0600
  * [MDEV-25222](https://jira.mariadb.org/browse/MDEV-25222): mysqlbinlog --base64-output wrong option default drops BINLOG from output
* [Revision #2714158150](https://github.com/MariaDB/server/commit/2714158150)\
  2021-05-19 14:27:12 +0300
  * [MDEV-25691](https://jira.mariadb.org/browse/MDEV-25691) fixup: Correctly drop orphan foreign keys
* Merge [Revision #5d495fc44b](https://github.com/MariaDB/server/commit/5d495fc44b) 2021-05-19 09:15:54 +0300 - Merge 10.5 into 10.6
* Merge [Revision #db8fb40824](https://github.com/MariaDB/server/commit/db8fb40824) 2021-05-19 08:39:39 +0300 - Merge 10.4 into 10.5
* [Revision #08b6fd9395](https://github.com/MariaDB/server/commit/08b6fd9395)\
  2021-05-18 12:13:18 +0300
  * [MDEV-25710](https://jira.mariadb.org/browse/MDEV-25710): Dead code os\_file\_opendir() in the server
* [Revision #895c126a23](https://github.com/MariaDB/server/commit/895c126a23)\
  2021-05-18 16:04:56 +0300
  * [MDEV-15528](https://jira.mariadb.org/browse/MDEV-15528) fixup: Remove references to background scrubbing
* [Revision #e3adb4345d](https://github.com/MariaDB/server/commit/e3adb4345d)\
  2021-05-19 09:15:28 +0300
  * [MDEV-8334](https://jira.mariadb.org/browse/MDEV-8334): Adjust test results
* [Revision #2fdb556e04](https://github.com/MariaDB/server/commit/2fdb556e04)\
  2021-02-15 01:39:37 +0530
  * [MDEV-8334](https://jira.mariadb.org/browse/MDEV-8334): Rename utf8 to utf8mb3
* [Revision #c366845a0b](https://github.com/MariaDB/server/commit/c366845a0b)\
  2021-05-18 12:53:40 +0300
  * [MDEV-25691](https://jira.mariadb.org/browse/MDEV-25691): Simplify handlerton::drop\_database for InnoDB
* Merge [Revision #f09d33f521](https://github.com/MariaDB/server/commit/f09d33f521) 2021-05-18 11:13:45 +0300 - Merge 10.5 into 10.6
* [Revision #7b51d11cca](https://github.com/MariaDB/server/commit/7b51d11cca)\
  2021-05-18 09:27:59 +0300
  * [MDEV-25594](https://jira.mariadb.org/browse/MDEV-25594): Improve debug checks
* Merge [Revision #cc2651b74c](https://github.com/MariaDB/server/commit/cc2651b74c) 2021-05-18 09:21:59 +0300 - Merge 10.4 into 10.5
* Merge [Revision #4240704abc](https://github.com/MariaDB/server/commit/4240704abc) 2021-05-18 08:59:12 +0300 - Merge 10.3 into 10.4
* Merge [Revision #ca3f497564](https://github.com/MariaDB/server/commit/ca3f497564) 2021-05-18 08:40:19 +0300 - Merge 10.2 into 10.3, except [MDEV-25682](https://jira.mariadb.org/browse/MDEV-25682)
* [Revision #b9a2e4609f](https://github.com/MariaDB/server/commit/b9a2e4609f)\
  2021-05-18 08:37:24 +0300
  * [MDEV-25594](https://jira.mariadb.org/browse/MDEV-25594): Assertion failure in DeadlockChecker::check\_and\_resolve()
* [Revision #23cad4d8c5](https://github.com/MariaDB/server/commit/23cad4d8c5)\
  2021-05-17 18:59:26 +0200
  * wsrep\_sst\_common.sh: file mode changed back to 664
* [Revision #88c7a58ecf](https://github.com/MariaDB/server/commit/88c7a58ecf)\
  2021-05-12 18:03:45 +0530
  * [MDEV-22530](https://jira.mariadb.org/browse/MDEV-22530): Aborting OPTIMIZE TABLE still logs in binary log and replicates to the Slave server.
* [Revision #410e3c1a9a](https://github.com/MariaDB/server/commit/410e3c1a9a)\
  2021-05-12 18:00:06 +0530
  * [MDEV-17515](https://jira.mariadb.org/browse/MDEV-17515): GTID Replication in optimistic mode deadlock
* [Revision #80ae3677e1](https://github.com/MariaDB/server/commit/80ae3677e1)\
  2021-05-17 09:39:19 +1000
  * [MDEV-25681](https://jira.mariadb.org/browse/MDEV-25681): --relay-log{,-index} missing warning
* [Revision #6811ed3e10](https://github.com/MariaDB/server/commit/6811ed3e10)\
  2021-05-14 12:51:36 +0200
  * [MDEV-25669](https://jira.mariadb.org/browse/MDEV-25669): SST scripts should check all server groups in config files
* [Revision #4675febb7a](https://github.com/MariaDB/server/commit/4675febb7a)\
  2021-05-13 12:23:11 +0200
  * Added missing connection lines to some tests
* [Revision #677f1ef6f0](https://github.com/MariaDB/server/commit/677f1ef6f0)\
  2021-05-14 16:43:36 -0700
  * [MDEV-25682](https://jira.mariadb.org/browse/MDEV-25682) Explain shows an execution plan different from actually executed
* [Revision #e607f3398c](https://github.com/MariaDB/server/commit/e607f3398c)\
  2021-04-14 10:56:12 +0100
  * [MDEV-25336](https://jira.mariadb.org/browse/MDEV-25336) Parallel replication causes failed assert while restarting
* [Revision #355dc74b76](https://github.com/MariaDB/server/commit/355dc74b76)\
  2021-04-14 11:23:38 +0100
  * [MDEV-22370](https://jira.mariadb.org/browse/MDEV-22370) safe\_mutex: Trying to lock uninitialized mutex at /data/src/10.4-bug/sql/rpl\_parallel.cc, line 470 upon shutdown during FTWRL
* [Revision #3616640a31](https://github.com/MariaDB/server/commit/3616640a31)\
  2020-01-17 20:26:14 +0200
  * [MDEV-20821](https://jira.mariadb.org/browse/MDEV-20821) parallel slave server shutdown hang
* [Revision #ec348f555b](https://github.com/MariaDB/server/commit/ec348f555b)\
  2021-05-11 20:08:40 +0200
  * mtr: --gdb mode, also quote ";", not only " "
* [Revision #3cf57aae9f](https://github.com/MariaDB/server/commit/3cf57aae9f)\
  2021-05-11 10:04:52 +0200
  * [MDEV-23580](https://jira.mariadb.org/browse/MDEV-23580) addendum: normal operation in configurations where stunnel is not available
* [Revision #089d82a74b](https://github.com/MariaDB/server/commit/089d82a74b)\
  2021-05-10 09:50:56 -0400
  * bump the VERSION
* [Revision #8fef2b8667](https://github.com/MariaDB/server/commit/8fef2b8667)\
  2021-05-10 04:27:16 +0200
  * [MDEV-23580](https://jira.mariadb.org/browse/MDEV-23580): WSREP\_SST: \[ERROR] rsync daemon port has been taken
* [Revision #9f03a394ff](https://github.com/MariaDB/server/commit/9f03a394ff)\
  2021-05-17 18:59:26 +0200
  * wsrep\_sst\_common.sh: file mode changed back to 664
* [Revision #f92cd0c56b](https://github.com/MariaDB/server/commit/f92cd0c56b)\
  2021-05-14 12:51:36 +0200
  * [MDEV-25669](https://jira.mariadb.org/browse/MDEV-25669): SST scripts should check all server groups in config files
* [Revision #16437e5e25](https://github.com/MariaDB/server/commit/16437e5e25)\
  2021-05-13 12:23:11 +0200
  * Added missing connection lines to some tests
* [Revision #1447b39475](https://github.com/MariaDB/server/commit/1447b39475)\
  2021-05-07 14:04:24 +0300
  * Updated galera\_3nodes disabled.def file
* [Revision #2d47bad3ac](https://github.com/MariaDB/server/commit/2d47bad3ac)\
  2021-05-11 10:04:52 +0200
  * [MDEV-23580](https://jira.mariadb.org/browse/MDEV-23580) addendum: normal operation in configurations where stunnel is not available
* [Revision #7e8a89387b](https://github.com/MariaDB/server/commit/7e8a89387b)\
  2021-05-10 04:27:16 +0200
  * [MDEV-23580](https://jira.mariadb.org/browse/MDEV-23580): WSREP\_SST: \[ERROR] rsync daemon port has been taken
* [Revision #bc4d995cfa](https://github.com/MariaDB/server/commit/bc4d995cfa)\
  2021-05-10 10:49:19 -0400
  * bump the VERSION
* [Revision #e861e057ad](https://github.com/MariaDB/server/commit/e861e057ad)\
  2021-05-17 19:51:49 +0200
  * [MDEV-25693](https://jira.mariadb.org/browse/MDEV-25693): SST failed due to incorrect connection address
* [Revision #cf4dd3cc81](https://github.com/MariaDB/server/commit/cf4dd3cc81)\
  2021-05-17 18:59:26 +0200
  * wsrep\_sst\_common.sh: file mode changed back to 664
* [Revision #f9f8e33f29](https://github.com/MariaDB/server/commit/f9f8e33f29)\
  2021-05-14 12:51:36 +0200
  * [MDEV-25669](https://jira.mariadb.org/browse/MDEV-25669): SST scripts should check all server groups in config files
* [Revision #16898e7f11](https://github.com/MariaDB/server/commit/16898e7f11)\
  2021-05-13 12:23:11 +0200
  * Added missing connection lines to some tests
* [Revision #9aac079a84](https://github.com/MariaDB/server/commit/9aac079a84)\
  2021-05-11 10:04:52 +0200
  * [MDEV-23580](https://jira.mariadb.org/browse/MDEV-23580) addendum: normal operation in configurations where stunnel is not available
* [Revision #27ae7f2a26](https://github.com/MariaDB/server/commit/27ae7f2a26)\
  2021-05-10 04:27:16 +0200
  * [MDEV-23580](https://jira.mariadb.org/browse/MDEV-23580): WSREP\_SST: \[ERROR] rsync daemon port has been taken
* [Revision #b2bb747f8c](https://github.com/MariaDB/server/commit/b2bb747f8c)\
  2021-05-10 11:11:21 -0400
  * bump the VERSION
* [Revision #81402c1318](https://github.com/MariaDB/server/commit/81402c1318)\
  2021-05-12 11:46:58 -0600
  * [MDEV-25222](https://jira.mariadb.org/browse/MDEV-25222): mysqlbinlog --base64-output wrong option default drops BINLOG from output
* [Revision #740917620a](https://github.com/MariaDB/server/commit/740917620a)\
  2021-05-17 19:51:49 +0200
  * [MDEV-25693](https://jira.mariadb.org/browse/MDEV-25693): SST failed due to incorrect connection address
* [Revision #2947cf6499](https://github.com/MariaDB/server/commit/2947cf6499)\
  2021-05-17 18:59:26 +0200
  * wsrep\_sst\_common.sh: file mode changed back to 664
* [Revision #527675d53a](https://github.com/MariaDB/server/commit/527675d53a)\
  2021-05-14 12:51:36 +0200
  * [MDEV-25669](https://jira.mariadb.org/browse/MDEV-25669): SST scripts should check all server groups in config files
* [Revision #7bc458dd79](https://github.com/MariaDB/server/commit/7bc458dd79)\
  2021-05-11 10:04:52 +0200
  * [MDEV-23580](https://jira.mariadb.org/browse/MDEV-23580) addendum: normal operation in configurations where stunnel is not available
* [Revision #d57e60d782](https://github.com/MariaDB/server/commit/d57e60d782)\
  2021-05-10 04:27:16 +0200
  * [MDEV-23580](https://jira.mariadb.org/browse/MDEV-23580): WSREP\_SST: \[ERROR] rsync daemon port has been taken
* [Revision #c22d567e1a](https://github.com/MariaDB/server/commit/c22d567e1a)\
  2021-05-14 15:59:09 +0400
  * [MDEV-25690](https://jira.mariadb.org/browse/MDEV-25690) Plugins can't execute sql statements with the Galera enabled.
* [Revision #34340fb501](https://github.com/MariaDB/server/commit/34340fb501)\
  2021-05-17 19:51:49 +0200
  * [MDEV-25693](https://jira.mariadb.org/browse/MDEV-25693): SST failed due to incorrect connection address
* [Revision #d45f61c3ad](https://github.com/MariaDB/server/commit/d45f61c3ad)\
  2021-05-17 18:59:26 +0200
  * wsrep\_sst\_common.sh: file mode changed back to 664
* [Revision #9e8e82cc11](https://github.com/MariaDB/server/commit/9e8e82cc11)\
  2021-05-14 12:51:36 +0200
  * [MDEV-25669](https://jira.mariadb.org/browse/MDEV-25669): SST scripts should check all server groups in config files
* [Revision #69feb040bf](https://github.com/MariaDB/server/commit/69feb040bf)\
  2021-05-11 10:04:52 +0200
  * [MDEV-23580](https://jira.mariadb.org/browse/MDEV-23580) addendum: normal operation in configurations where stunnel is not available
* [Revision #bcd6af931f](https://github.com/MariaDB/server/commit/bcd6af931f)\
  2021-05-10 04:27:16 +0200
  * [MDEV-23580](https://jira.mariadb.org/browse/MDEV-23580): WSREP\_SST: \[ERROR] rsync daemon port has been taken
* [Revision #86dc7b4d4c](https://github.com/MariaDB/server/commit/86dc7b4d4c)\
  2021-05-17 18:12:33 +0300
  * [MDEV-24626](https://jira.mariadb.org/browse/MDEV-24626) Remove synchronous write of page0 file during file creation
* [Revision #c290c0d7e0](https://github.com/MariaDB/server/commit/c290c0d7e0)\
  2021-05-17 15:54:33 +0300
  * Simplify a preprocessor condition
* [Revision #7e1ec1550c](https://github.com/MariaDB/server/commit/7e1ec1550c)\
  2021-05-11 20:10:54 +0530
  * [MDEV-19371](https://jira.mariadb.org/browse/MDEV-19371): Implement binlog\_expire\_logs\_seconds for purging of binary logs
* [Revision #1b1882c627](https://github.com/MariaDB/server/commit/1b1882c627)\
  2021-05-17 09:56:04 +0300
  * [MDEV-25689](https://jira.mariadb.org/browse/MDEV-25689): Remove MONITOR\_TABLE\_REFERENCE, MONITOR\_TABLE\_CLOSE
* [Revision #adb0fdb268](https://github.com/MariaDB/server/commit/adb0fdb268)\
  2021-05-17 09:03:06 +0300
  * Cleanup: Remove unused DB\_TABLE\_IS\_BEING\_USED
* [Revision #a6cff02a2f](https://github.com/MariaDB/server/commit/a6cff02a2f)\
  2021-05-17 08:37:59 +0300
  * [MDEV-25687](https://jira.mariadb.org/browse/MDEV-25687): Remove trx\_active\_transactions
* [Revision #cdbd04dde5](https://github.com/MariaDB/server/commit/cdbd04dde5)\
  2021-05-17 07:44:40 +0300
  * [MDEV-18518](https://jira.mariadb.org/browse/MDEV-18518) fixup: Remove row\_drop\_table\_after\_create\_fail()
* [Revision #bee1bb056d](https://github.com/MariaDB/server/commit/bee1bb056d)\
  2021-05-14 13:25:03 +0300
  * [MDEV-9609](https://jira.mariadb.org/browse/MDEV-9609) : wsrep\_debug only logs DDL information on originating node
* [Revision #1c5ae99194](https://github.com/MariaDB/server/commit/1c5ae99194)\
  2021-05-14 08:36:14 +0300
  * [MDEV-25666](https://jira.mariadb.org/browse/MDEV-25666): After backup, "Could not find a valid tablespace file"
* [Revision #7750cda148](https://github.com/MariaDB/server/commit/7750cda148)\
  2021-05-14 08:27:16 +0300
  * Cleanup: Remove innodb\_flush\_method (use srv\_file\_flush\_method)
* [Revision #3a427c568b](https://github.com/MariaDB/server/commit/3a427c568b)\
  2021-05-14 08:26:51 +0300
  * Cleanup: Remove useless message "If you are installing InnoDB"
* [Revision #a0b133f431](https://github.com/MariaDB/server/commit/a0b133f431)\
  2021-05-14 08:24:43 +0300
  * [MDEV-25312](https://jira.mariadb.org/browse/MDEV-25312) fixup: Invoke fil\_space\_t::rename() correctly
* [Revision #4547c6f283](https://github.com/MariaDB/server/commit/4547c6f283)\
  2021-05-13 12:25:01 +0300
  * [MDEV-25154](https://jira.mariadb.org/browse/MDEV-25154): JSON\_TABLE: Queries involving ordinality columns are unsafe ...
* [Revision #916c28c9e5](https://github.com/MariaDB/server/commit/916c28c9e5)\
  2021-05-13 13:19:57 +0300
  * fixup e3b3384282b080e2d331507513afdf2b612f630b: wsrep test results
* [Revision #fe9450676f](https://github.com/MariaDB/server/commit/fe9450676f)\
  2021-05-12 13:46:51 +0530
  * [MDEV-25502](https://jira.mariadb.org/browse/MDEV-25502): rpl.rpl\_perfschema\_applier\_status\_by\_worker failed in bb with: Test assertion failed
* [Revision #e3b3384282](https://github.com/MariaDB/server/commit/e3b3384282)\
  2021-05-11 16:27:37 +0300
  * tztime\_to\_sql: quote `Offset` field
* [Revision #982290fe9b](https://github.com/MariaDB/server/commit/982290fe9b)\
  2021-05-13 01:51:19 +0900
  * Fix the following valgrind error on Spider
* Merge [Revision #370b310b1d](https://github.com/MariaDB/server/commit/370b310b1d) 2021-05-12 07:47:51 +0300 - Merge 10.5 into 10.6
* [Revision #4d53a7585c](https://github.com/MariaDB/server/commit/4d53a7585c)\
  2021-05-11 21:25:08 +0300
  * Updated tests in decimal.c that match current API and usage
* [Revision #0df51e610b](https://github.com/MariaDB/server/commit/0df51e610b)\
  2021-05-11 21:05:51 +0300
  * [MDEV-25651](https://jira.mariadb.org/browse/MDEV-25651) Server crash or assertion failure in THD::update\_stats upon concurrent DROP TRIGGER
* [Revision #621501f38b](https://github.com/MariaDB/server/commit/621501f38b)\
  2021-05-10 20:36:38 +0300
  * [MDEV-25606](https://jira.mariadb.org/browse/MDEV-25606): Concurrent CREATE TRIGGER statements mix up in binlog and break replication
* [Revision #5d8684863c](https://github.com/MariaDB/server/commit/5d8684863c)\
  2021-05-10 11:33:29 -0400
  * bump the VERSION
* [Revision #b6cfb2961e](https://github.com/MariaDB/server/commit/b6cfb2961e)\
  2021-05-10 11:10:53 -0600
  * [MDEV-14974](https://jira.mariadb.org/browse/MDEV-14974): --port ignored for --host=localhost
* [Revision #02380cd384](https://github.com/MariaDB/server/commit/02380cd384)\
  2021-05-11 09:58:23 +0300
  * [MDEV-21452](https://jira.mariadb.org/browse/MDEV-21452) fixup: recursive recv\_sys.mutex lock
* Merge [Revision #f8665314d4](https://github.com/MariaDB/server/commit/f8665314d4) 2021-05-10 11:42:04 +0300 - Merge 10.5 into 10.6
* Merge [Revision #0e1437e147](https://github.com/MariaDB/server/commit/0e1437e147) 2021-05-10 10:01:15 +0300 - Merge 10.4 into 10.5
* Merge [Revision #8c73fab7f7](https://github.com/MariaDB/server/commit/8c73fab7f7) 2021-05-10 09:52:01 +0300 - Merge 10.3 into 10.4
* Merge [Revision #98e6159892](https://github.com/MariaDB/server/commit/98e6159892) 2021-05-10 09:09:50 +0300 - Merge 10.2 into 10.3
* [Revision #d0785f7731](https://github.com/MariaDB/server/commit/d0785f7731)\
  2021-05-09 10:32:49 +0200
  * [MDEV-25232](https://jira.mariadb.org/browse/MDEV-25232) Ninja MSVC build sets default CMAKE\_BUILD\_TYPE to Debug
* [Revision #e1bf1aea5c](https://github.com/MariaDB/server/commit/e1bf1aea5c)\
  2021-05-06 22:58:28 +0200
  * force jemalloc to be used in release rpm/deb builds
* [Revision #66acec99d5](https://github.com/MariaDB/server/commit/66acec99d5)\
  2021-05-03 18:10:13 +0200
  * XA PREPARE and SHOW STATUS
* [Revision #18fbe566bd](https://github.com/MariaDB/server/commit/18fbe566bd)\
  2021-05-03 18:01:30 +0200
  * mtr --gdb='commands' and restarts
* [Revision #af781f1ac4](https://github.com/MariaDB/server/commit/af781f1ac4)\
  2021-05-03 18:00:09 +0200
  * fix mtr --client-gdb to work
* [Revision #ad4b51948f](https://github.com/MariaDB/server/commit/ad4b51948f)\
  2021-05-03 17:53:17 +0200
  * Revert "Connect: remove Mongo dependencies"
* [Revision #afb8e87391](https://github.com/MariaDB/server/commit/afb8e87391)\
  2021-05-07 21:42:42 +0200
  * Skip auth\_named\_pipe test, if plugin was not built
* [Revision #76c2b5106e](https://github.com/MariaDB/server/commit/76c2b5106e)\
  2021-05-07 14:52:46 +0300
  * Fix clang++-11 -Wsometimes-uninitialized
* Merge [Revision #c225eee219](https://github.com/MariaDB/server/commit/c225eee219) 2021-05-07 11:18:55 +0200 - Merge branch 'bb-10.2-release' into 10.2
* [Revision #54d7ba9609](https://github.com/MariaDB/server/commit/54d7ba9609)\
  2021-05-06 04:03:07 +0200
  * [MDEV-25418](https://jira.mariadb.org/browse/MDEV-25418): Improve mariabackup SST script compliance with native MariaDB SSL practices and configuration.
* [Revision #cf67ca48d6](https://github.com/MariaDB/server/commit/cf67ca48d6)\
  2021-04-25 18:06:53 +0300
  * [MDEV-25418](https://jira.mariadb.org/browse/MDEV-25418) rsync SST does not work with stunnel encryption
* [Revision #ee1e877470](https://github.com/MariaDB/server/commit/ee1e877470)\
  2021-05-06 01:16:52 +0200
  * [MDEV-24962](https://jira.mariadb.org/browse/MDEV-24962) addendum: improved handling of paths with spaces
* [Revision #6895c9eaa0](https://github.com/MariaDB/server/commit/6895c9eaa0)\
  2021-05-05 03:17:51 +0200
  * [MDEV-24962](https://jira.mariadb.org/browse/MDEV-24962) addendum: mariabackup does not understand --log-bin-index and --log-basename options
* [Revision #5ad7f52558](https://github.com/MariaDB/server/commit/5ad7f52558)\
  2021-05-03 23:26:30 +0200
  * [MDEV-21603](https://jira.mariadb.org/browse/MDEV-21603) Crashing SHOW TABLES with derived table in WHERE condition
* [Revision #1ae7673aae](https://github.com/MariaDB/server/commit/1ae7673aae)\
  2021-04-28 01:39:31 +0200
  * [MDEV-24962](https://jira.mariadb.org/browse/MDEV-24962): Galera SST innobackupex-move ignores Environment settings
* [Revision #e0324bf300](https://github.com/MariaDB/server/commit/e0324bf300)\
  2021-04-15 13:53:28 +0200
  * wsrep sst scripts: removing extra blank lines and spaces
* Merge [Revision #72753d2b65](https://github.com/MariaDB/server/commit/72753d2b65) 2021-05-07 11:51:22 +0200 - Merge branch 'bb-10.3-release' into 10.3
* [Revision #625e44a80d](https://github.com/MariaDB/server/commit/625e44a80d)\
  2021-05-05 15:46:22 +0530
  * [MDEV-25597](https://jira.mariadb.org/browse/MDEV-25597): Disable rpl\_semi\_sync\_slave\_compressed\_protocol.test
* Merge [Revision #583b72ad0d](https://github.com/MariaDB/server/commit/583b72ad0d) 2021-05-07 11:50:24 +0200 - Merge branch 'bb-10.4-release' into 10.4
* [Revision #1ef3207cb8](https://github.com/MariaDB/server/commit/1ef3207cb8)\
  2021-05-10 09:36:22 +0530
  * [MDEV-19371](https://jira.mariadb.org/browse/MDEV-19371): Implement binlog\_expire\_logs\_seconds for purging of binary logs
* [Revision #49ff2cbff4](https://github.com/MariaDB/server/commit/49ff2cbff4)\
  2021-05-07 12:57:20 +0530
  * [MDEV-19371](https://jira.mariadb.org/browse/MDEV-19371): Implement binlog\_expire\_logs\_seconds for purging of binary logs
* [Revision #4205078b41](https://github.com/MariaDB/server/commit/4205078b41)\
  2021-05-09 23:50:11 +0200
  * Fix clang-cl warning
* [Revision #f3c1e3f40f](https://github.com/MariaDB/server/commit/f3c1e3f40f)\
  2021-05-09 23:49:19 +0200
  * Remove incorrect comment.
* [Revision #bc64a03c3a](https://github.com/MariaDB/server/commit/bc64a03c3a)\
  2021-05-09 23:45:24 +0200
  * Windows - Fix CMAKE\_INTERPROCEDURAL\_OPTIMIZATION build with MSVC
* [Revision #f33e8e4a95](https://github.com/MariaDB/server/commit/f33e8e4a95)\
  2021-05-09 13:26:03 +0200
  * Windows : fix warning about potential division by 0
* [Revision #fbad1b1150](https://github.com/MariaDB/server/commit/fbad1b1150)\
  2021-05-09 13:23:22 +0200
  * [MDEV-19237](https://jira.mariadb.org/browse/MDEV-19237) - small performance tweak
* Merge [Revision #916b237b3f](https://github.com/MariaDB/server/commit/916b237b3f) 2021-05-07 15:00:27 +0300 - Merge 10.5 into 10.6
* Merge [Revision #35977e81f9](https://github.com/MariaDB/server/commit/35977e81f9) 2021-05-07 12:13:17 +0200 - Merge branch 'bb-10.5-release' into 10.5
* [Revision #a5b3982585](https://github.com/MariaDB/server/commit/a5b3982585)\
  2021-05-07 08:13:28 +0200
  * [MDEV-25613](https://jira.mariadb.org/browse/MDEV-25613) assertion (file\_system.n\_open > 0) failed
* [Revision #a04202673f](https://github.com/MariaDB/server/commit/a04202673f)\
  2021-05-07 14:18:36 +0300
  * [MDEV-18518](https://jira.mariadb.org/browse/MDEV-18518) fixup: Remove unused variables
* [Revision #c74f059abc](https://github.com/MariaDB/server/commit/c74f059abc)\
  2021-05-07 09:45:56 +0300
  * Update Galera disabled.def files on 10.6
* [Revision #2ceadb3903](https://github.com/MariaDB/server/commit/2ceadb3903)\
  2021-05-06 16:34:10 +0300
  * [MDEV-25506](https://jira.mariadb.org/browse/MDEV-25506) (2 of 3): Kill during DDL leaves orphan .ibd file
* [Revision #cc2ddde4d8](https://github.com/MariaDB/server/commit/cc2ddde4d8)\
  2021-05-06 16:04:29 +0300
  * [MDEV-18518](https://jira.mariadb.org/browse/MDEV-18518) follow-up fixes
* Merge [Revision #b2e0a45d7a](https://github.com/MariaDB/server/commit/b2e0a45d7a) 2021-05-05 13:15:06 +0300 - Merge 10.5 into 10.6
* [Revision #d44a10f4dd](https://github.com/MariaDB/server/commit/d44a10f4dd)\
  2021-05-05 12:51:44 +0300
  * [MDEV-23855](https://jira.mariadb.org/browse/MDEV-23855) follow-up: Make innodb.doublewrite more stable
* [Revision #f673277491](https://github.com/MariaDB/server/commit/f673277491)\
  2021-05-05 07:29:10 +0300
  * [MDEV-25586](https://jira.mariadb.org/browse/MDEV-25586) : SIGSEGV in my\_strcasecmp\_utf8mb3
* [Revision #803fa4b3fc](https://github.com/MariaDB/server/commit/803fa4b3fc)\
  2021-04-11 08:22:28 -0700
  * [MCOL-4535](https://jira.mariadb.org/browse/MCOL-4535): Clean up libreadline as ColumnStore no longer needs it
* Merge [Revision #e0d61cb41c](https://github.com/MariaDB/server/commit/e0d61cb41c) 2021-05-04 12:12:15 +0300 - Merge remote-tracking branch 10.4 into 10.5
* [Revision #473e85e931](https://github.com/MariaDB/server/commit/473e85e931)\
  2021-05-04 08:44:56 +0300
  * [MDEV-25591](https://jira.mariadb.org/browse/MDEV-25591) : Test case cleanups
* [Revision #0238e68464](https://github.com/MariaDB/server/commit/0238e68464)\
  2021-05-04 08:44:56 +0300
  * [MDEV-25591](https://jira.mariadb.org/browse/MDEV-25591) : Test case cleanups
* [Revision #4ff4df3232](https://github.com/MariaDB/server/commit/4ff4df3232)\
  2021-05-04 20:01:59 +0300
  * [MDEV-25491](https://jira.mariadb.org/browse/MDEV-25491) fixup: Optimize fil\_space\_t::check\_pending\_operations()
* [Revision #11597e02f3](https://github.com/MariaDB/server/commit/11597e02f3)\
  2021-05-04 15:40:05 +0530
  * [MDEV-25502](https://jira.mariadb.org/browse/MDEV-25502): rpl.rpl\_perfschema\_applier\_status\_by\_worker failed in bb with: Test assertion failed
* [Revision #025eed061b](https://github.com/MariaDB/server/commit/025eed061b)\
  2021-05-04 11:51:35 +0300
  * Cleanup: Remove unnecessary InnoDB log writes
* [Revision #0ff90b3b94](https://github.com/MariaDB/server/commit/0ff90b3b94)\
  2021-05-04 11:29:55 +0300
  * [MDEV-25506](https://jira.mariadb.org/browse/MDEV-25506): Kill during DDL leaves orphan .ibd file
* [Revision #52aac131e3](https://github.com/MariaDB/server/commit/52aac131e3)\
  2021-05-03 18:53:01 +0300
  * [MDEV-18518](https://jira.mariadb.org/browse/MDEV-18518) Multi-table CREATE and DROP transactions for InnoDB
* Merge [Revision #1e1073b810](https://github.com/MariaDB/server/commit/1e1073b810) 2021-05-04 07:37:38 +0300 - Merge 10.5 into 10.6
* [Revision #9fe681c9e4](https://github.com/MariaDB/server/commit/9fe681c9e4)\
  2021-04-30 16:39:06 +0530
  * [MDEV-25509](https://jira.mariadb.org/browse/MDEV-25509) Atomic DDL: Assertion \`err != DB\_DUPLICATE\_KEY' fails after previous error upon multi-RENAME
* [Revision #fd8c68c7fe](https://github.com/MariaDB/server/commit/fd8c68c7fe)\
  2021-04-30 10:31:37 +0300
  * [MDEV-25491](https://jira.mariadb.org/browse/MDEV-25491) fixup: Race between DROP TABLE and purge of DROP INDEX
* [Revision #f21e159bb5](https://github.com/MariaDB/server/commit/f21e159bb5)\
  2021-04-30 08:55:16 +0200
  * [MDEV-25506](https://jira.mariadb.org/browse/MDEV-25506) fixup for Windows
* [Revision #db0782243c](https://github.com/MariaDB/server/commit/db0782243c)\
  2021-04-29 22:17:37 +0300
  * [MDEV-25524](https://jira.mariadb.org/browse/MDEV-25524) fixup for Windows
* [Revision #54e2e70194](https://github.com/MariaDB/server/commit/54e2e70194)\
  2021-04-29 15:25:57 +0300
  * [MDEV-25524](https://jira.mariadb.org/browse/MDEV-25524) heap-use-after-free in fil\_space\_t::rename()
* Merge [Revision #55e0ce1401](https://github.com/MariaDB/server/commit/55e0ce1401) 2021-04-29 16:35:26 +0300 - Merge 10.5 into 10.6
* [Revision #aed8605dd1](https://github.com/MariaDB/server/commit/aed8605dd1)\
  2021-04-29 12:03:48 +0300
  * Update wsrep-lib
* [Revision #c409dd42ef](https://github.com/MariaDB/server/commit/c409dd42ef)\
  2021-04-28 10:58:05 +0200
  * [MDEV-22131](https://jira.mariadb.org/browse/MDEV-22131) allow transition from unencrypted to TLS cluster communication without cluster downtime
* [Revision #98e3034eea](https://github.com/MariaDB/server/commit/98e3034eea)\
  2021-04-28 17:11:48 +0300
  * [MDEV-25534](https://jira.mariadb.org/browse/MDEV-25534) Assertion lock\_table\_has...LOCK\_IX
* [Revision #a29618f3bd](https://github.com/MariaDB/server/commit/a29618f3bd)\
  2021-04-27 18:21:38 +0300
  * [MDEV-25522](https://jira.mariadb.org/browse/MDEV-25522): Purge of aborted ADD INDEX leaves orphan locks behind
* [Revision #5abb505af9](https://github.com/MariaDB/server/commit/5abb505af9)\
  2021-04-27 18:05:36 +0300
  * dict\_drop\_index\_tree(): More robust corruption handling
* [Revision #f619d79bda](https://github.com/MariaDB/server/commit/f619d79bda)\
  2021-04-26 13:52:52 +0300
  * [MDEV-25491](https://jira.mariadb.org/browse/MDEV-25491): Race condition between DROP TABLE and purge of SYS\_INDEXES record
* [Revision #a81aec1505](https://github.com/MariaDB/server/commit/a81aec1505)\
  2021-04-23 16:58:25 +0300
  * [MDEV-25491](https://jira.mariadb.org/browse/MDEV-25491) preparation: Clean up tablespace destruction
* [Revision #b3d963fee4](https://github.com/MariaDB/server/commit/b3d963fee4)\
  2021-04-19 22:54:45 +0900
  * [MDEV-22265](https://jira.mariadb.org/browse/MDEV-22265) Connect string character limit too small for full 64 character InnoDB table-name limit when using ad-hoc Spider server definitions.
* [Revision #9db14e93ac](https://github.com/MariaDB/server/commit/9db14e93ac)\
  2021-04-26 09:51:38 -0400
  * bump the VERSION
* Merge [Revision #ed4b2b3f95](https://github.com/MariaDB/server/commit/ed4b2b3f95) 2021-04-26 08:40:36 +0300 - Merge 10.5 into 10.6
* [Revision #b81382887c](https://github.com/MariaDB/server/commit/b81382887c)\
  2021-04-25 12:58:16 +0300
  * [MDEV-25512](https://jira.mariadb.org/browse/MDEV-25512) Deadlock between sux\_lock::u\_x\_upgrade() and sux\_lock::u\_lock()
