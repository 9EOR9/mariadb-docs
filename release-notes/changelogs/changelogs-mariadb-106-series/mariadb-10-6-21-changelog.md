# MariaDB 10.6.21 Changelog

[Download](https://mariadb.com/downloads/)[Release Notes](../../mariadb-community-server-release-notes/mariadb-10-6-series/mariadb-10-6-21-release-notes.md)[Changelog](mariadb-10-6-21-changelog.md)[Overview of 10.6](../../mariadb-community-server-release-notes/mariadb-10-6-series/what-is-mariadb-106.md)

[_Alternate download from mariadb.org_](https://downloads.mariadb.org/mariadb/10.6.21/)

**Release date:** 4 Feb 2025

For the highlights of this release, see the[release notes](../../mariadb-community-server-release-notes/mariadb-10-6-series/mariadb-10-6-21-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/server/tree/10.6) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Includes all fixes from [MariaDB 10.5.28](../changelogs-mariadb-105-series/mariadb-10-5-28-changelog.md)
* Merge [Revision #066e8d6aea](https://github.com/MariaDB/server/commit/066e8d6aea) 2025-01-29 11:17:38 +0100 - Merge branch '10.5' into 10.6
* [Revision #a89e734fcb](https://github.com/MariaDB/server/commit/a89e734fcb)\
  2025-01-24 14:17:15 +0100
  * ColumnStore 6.4.10-1
* [Revision #d0c2a007ee](https://github.com/MariaDB/server/commit/d0c2a007ee)\
  2025-01-24 14:26:20 +0100
  * C/C 3.3.14
* [Revision #17e31abd8b](https://github.com/MariaDB/server/commit/17e31abd8b)\
  2025-01-24 18:05:31 +0100
  * compilation failure on CentOS 7
* [Revision #38d3b6027b](https://github.com/MariaDB/server/commit/38d3b6027b)\
  2025-01-26 21:24:53 +0100
  * [MDEV-35943](https://jira.mariadb.org/browse/MDEV-35943) ASAN errors in Query\_arena::free\_items / fill\_schema\_table\_from\_frm
* [Revision #03d2328785](https://github.com/MariaDB/server/commit/03d2328785)\
  2025-01-27 19:22:20 +0100
  * [MDEV-35944](https://jira.mariadb.org/browse/MDEV-35944) DELETE fails to notice transaction abort, violating ACID
* [Revision #d5e7bce14b](https://github.com/MariaDB/server/commit/d5e7bce14b)\
  2025-01-29 10:42:01 +0200
  * [MDEV-35966](https://jira.mariadb.org/browse/MDEV-35966) galera.galera\_as\_master crashes in debug builds
* [Revision #3cfffb4de6](https://github.com/MariaDB/server/commit/3cfffb4de6)\
  2025-01-29 09:04:50 +0200
  * [MDEV-35962](https://jira.mariadb.org/browse/MDEV-35962) CREATE INDEX fails to heal a FOREIGN KEY constraint
* [Revision #831f5bc66f](https://github.com/MariaDB/server/commit/831f5bc66f)\
  2025-01-27 12:08:30 +0200
  * [MDEV-33978](https://jira.mariadb.org/browse/MDEV-33978) P\_S.THREADS is not showing all server threads
* [Revision #d77b9a4925](https://github.com/MariaDB/server/commit/d77b9a4925)\
  2025-01-25 11:05:29 -0700
  * [MDEV-34355](https://jira.mariadb.org/browse/MDEV-34355): rpl.rpl\_semi\_sync\_no\_missed\_ack\_after\_add\_slave ‘server\_3 should have sent…’
* [Revision #72e1cc8f52](https://github.com/MariaDB/server/commit/72e1cc8f52)\
  2025-01-10 00:06:25 +0100
  * [MDEV-35806](https://jira.mariadb.org/browse/MDEV-35806): Error in read\_log\_event() corrupts relay log writer, crashes server
* [Revision #2543be6942](https://github.com/MariaDB/server/commit/2543be6942)\
  2025-01-23 14:38:35 +0200
  * [MDEV-35854](https://jira.mariadb.org/browse/MDEV-35854): Clarify row\_rename\_table\_for\_mysql()
* [Revision #d4da659b43](https://github.com/MariaDB/server/commit/d4da659b43)\
  2025-01-23 14:38:08 +0200
  * [MDEV-35854](https://jira.mariadb.org/browse/MDEV-35854): Simplify dict\_get\_referenced\_table()
* [Revision #fa74c1a40f](https://github.com/MariaDB/server/commit/fa74c1a40f)\
  2025-01-21 19:19:46 +0200
  * Non partitioned table could be marked as partitioned in ddl.log
* [Revision #c05e7c4e0e](https://github.com/MariaDB/server/commit/c05e7c4e0e)\
  2024-12-04 19:56:46 +0300
  * [MDEV-35708](https://jira.mariadb.org/browse/MDEV-35708) lock\_rec\_get\_prev() returns only the first record lock
* Merge [Revision #98dbe3bfaf](https://github.com/MariaDB/server/commit/98dbe3bfaf) 2025-01-20 09:57:37 +0200 - Merge 10.5 into 10.6
* [Revision #8d6c9ef001](https://github.com/MariaDB/server/commit/8d6c9ef001)\
  2024-12-20 14:14:28 +1100
  * [MDEV-34925](https://jira.mariadb.org/browse/MDEV-34925) Fix segv on thd in spider recovery.
* [Revision #c69fb1a627](https://github.com/MariaDB/server/commit/c69fb1a627)\
  2025-01-17 13:28:02 +0400
  * [MDEV-35864](https://jira.mariadb.org/browse/MDEV-35864) UBSAN: "applying zero offset to null pointer" when using a Field\_set with empty values
* [Revision #a6ab0e6c0b](https://github.com/MariaDB/server/commit/a6ab0e6c0b)\
  2025-01-16 18:14:26 +0530
  * [MDEV-34898](https://jira.mariadb.org/browse/MDEV-34898) Doublewrite recovery of innodb\_checksum\_algorithm=full\_crc32 encrypted pages does not work
* [Revision #0abef37ccd](https://github.com/MariaDB/server/commit/0abef37ccd)\
  2025-01-15 16:55:29 +0200
  * Minor lock\_sys cleanup
* [Revision #b82abc7163](https://github.com/MariaDB/server/commit/b82abc7163)\
  2025-01-15 16:55:01 +0200
  * [MDEV-35701](https://jira.mariadb.org/browse/MDEV-35701) trx\_t::autoinc\_locks causes unnecessary dynamic memory allocation
* [Revision #d5a417b9d5](https://github.com/MariaDB/server/commit/d5a417b9d5)\
  2025-01-13 09:14:30 +0200
  * [MDEV-35827](https://jira.mariadb.org/browse/MDEV-35827) The generic MY\_RELAX\_CPU is expensive
* [Revision #faca9500fb](https://github.com/MariaDB/server/commit/faca9500fb)\
  2025-01-11 12:09:47 -0700
  * [MDEV-35430](https://jira.mariadb.org/browse/MDEV-35430): Add cast to semi-sync wait skip msg
* [Revision #43233fe469](https://github.com/MariaDB/server/commit/43233fe469)\
  2025-01-10 10:08:24 +0200
  * Fix -DBUILD\_CONFIG=mysql\_release to keep standard cmake flags
* [Revision #ff1f611a0d](https://github.com/MariaDB/server/commit/ff1f611a0d)\
  2025-01-10 06:50:50 +0200
  * Avoid assert()
* [Revision #1b8358d943](https://github.com/MariaDB/server/commit/1b8358d943)\
  2025-01-09 14:27:13 +0200
  * Use assert() on RMW arguments
* Merge [Revision #addc828363](https://github.com/MariaDB/server/commit/addc828363) 2025-01-09 10:15:53 +0100 - Merge branch '10.5' into 10.6
* [Revision #9ddecc2164](https://github.com/MariaDB/server/commit/9ddecc2164)\
  2025-01-08 15:25:25 +0100
  * heap-buffer-overflow in mariadb-backup
* [Revision #90bd638159](https://github.com/MariaDB/server/commit/90bd638159)\
  2025-01-08 13:11:45 +0100
  * 32-bit rdiff fixes
* [Revision #9929a0a76e](https://github.com/MariaDB/server/commit/9929a0a76e)\
  2025-01-02 20:23:08 +0100
  * [MDEV-32576](https://jira.mariadb.org/browse/MDEV-32576) increase query length in the InnoDB deadlock output
* [Revision #c478b1ba08](https://github.com/MariaDB/server/commit/c478b1ba08)\
  2024-12-10 00:11:41 +0100
  * [MDEV-35598](https://jira.mariadb.org/browse/MDEV-35598) foreign key error is unnecessary truncated
* [Revision #d26b47dfd4](https://github.com/MariaDB/server/commit/d26b47dfd4)\
  2024-12-09 22:15:37 +0100
  * [MDEV-35550](https://jira.mariadb.org/browse/MDEV-35550) main.log\_slow test failure: expects count(\*) 5 got 4
* [Revision #deb20fb751](https://github.com/MariaDB/server/commit/deb20fb751)\
  2024-11-16 18:17:08 +0100
  * [MDEV-32919](https://jira.mariadb.org/browse/MDEV-32919) Cannot select particular field from IS.tables in case table needs upgrade from MySQL 5.7
* [Revision #cc99a41502](https://github.com/MariaDB/server/commit/cc99a41502)\
  2024-11-16 18:08:14 +0100
  * cleanup: extract common condition into a function
* [Revision #a0e5dd5433](https://github.com/MariaDB/server/commit/a0e5dd5433)\
  2025-01-07 21:38:11 +0100
  * mysqltest: fix --sorted\_results
* [Revision #9b941dc51f](https://github.com/MariaDB/server/commit/9b941dc51f)\
  2024-11-15 15:33:42 +0100
  * [MDEV-34494](https://jira.mariadb.org/browse/MDEV-34494) restore broken feedback plugin
* [Revision #74532f2355](https://github.com/MariaDB/server/commit/74532f2355)\
  2024-11-15 10:45:12 +0100
  * [MCOL-5819](https://jira.mariadb.org/browse/MCOL-5819) disable lto for ColumnStore
* [Revision #b79723ffe3](https://github.com/MariaDB/server/commit/b79723ffe3)\
  2024-11-14 18:56:09 +0100
  * [MDEV-35384](https://jira.mariadb.org/browse/MDEV-35384) Table performance\_schema.session\_status and other two tables are not shown in information\_schema.tables for normal users
* [Revision #0706c01b88](https://github.com/MariaDB/server/commit/0706c01b88)\
  2024-11-13 23:47:38 +0100
  * cleanup: innodb.innodb\_information\_schema
* [Revision #725b5e7794](https://github.com/MariaDB/server/commit/725b5e7794)\
  2024-11-13 20:35:03 +0100
  * [MDEV-35335](https://jira.mariadb.org/browse/MDEV-35335) implicit commit at START TRANSACTION doesn't reset characteristics
* [Revision #990b010b09](https://github.com/MariaDB/server/commit/990b010b09)\
  2025-01-09 07:43:24 +0200
  * [MDEV-35438](https://jira.mariadb.org/browse/MDEV-35438) Annotate InnoDB I/O functions with noexcept
* [Revision #39f93b6eab](https://github.com/MariaDB/server/commit/39f93b6eab)\
  2024-10-21 16:56:35 +0200
  * [MDEV-29744](https://jira.mariadb.org/browse/MDEV-29744): Fix incorrect locking order of LOCK\_log/LOCK\_commit\_ordered and LOCK\_global\_system\_variables
* [Revision #6d4841ae26](https://github.com/MariaDB/server/commit/6d4841ae26)\
  2025-01-08 13:29:16 +0200
  * [MDEV-35647](https://jira.mariadb.org/browse/MDEV-35647) Possible hang during CREATE TABLE…SELECT error handling
* Merge [Revision #b251cb6a4f](https://github.com/MariaDB/server/commit/b251cb6a4f) 2025-01-08 08:48:21 +0200 - Merge 10.5 into 10.6
* [Revision #f8cf493290](https://github.com/MariaDB/server/commit/f8cf493290)\
  2025-01-07 18:39:46 +0530
  * [MDEV-34898](https://jira.mariadb.org/browse/MDEV-34898) Doublewrite recovery of innodb\_checksum\_algorithm=full\_crc32 encrypted pages does not work
* [Revision #6abbfdef7a](https://github.com/MariaDB/server/commit/6abbfdef7a)\
  2024-05-02 22:14:19 +0200
  * sporadic failures of binlog\_encryption.rpl\_parallel\_gco\_wait\_kill
* [Revision #a2d37705ca](https://github.com/MariaDB/server/commit/a2d37705ca)\
  2025-01-02 15:15:22 +0200
  * Only print "InnoDB: Transaction was aborted..." if log\_warnings >= 4
* [Revision #130d6f9c4b](https://github.com/MariaDB/server/commit/130d6f9c4b)\
  2024-12-28 11:06:04 +0200
  * Fixed memory leak in get\_window\_functions\_required\_cursors()
* [Revision #2085f36c6c](https://github.com/MariaDB/server/commit/2085f36c6c)\
  2024-12-27 17:31:42 +0200
  * Removed not used and not visible send\_metdata\_skip variable.
* [Revision #88d9348dfc](https://github.com/MariaDB/server/commit/88d9348dfc)\
  2024-12-27 13:59:24 +0200
  * Remove dates from all rdiff files
* [Revision #87ee1e75bc](https://github.com/MariaDB/server/commit/87ee1e75bc)\
  2024-12-13 15:41:59 +0200
  * [MDEV-35643](https://jira.mariadb.org/browse/MDEV-35643) Add support for MySQL 8.0 binlog events
* [Revision #47a5eed437](https://github.com/MariaDB/server/commit/47a5eed437)\
  2024-12-04 12:03:40 +0200
  * Added status variable "Max\_memory\_used" to SHOW STATUS
* [Revision #a0bfdef5e6](https://github.com/MariaDB/server/commit/a0bfdef5e6)\
  2024-12-04 11:31:00 +0200
  * Added more information to errors reported by report\_reply\_packet()
* [Revision #996e7fd7d5](https://github.com/MariaDB/server/commit/996e7fd7d5)\
  2024-12-03 19:08:10 +0200
  * Avoid printing "rowid\_filter\_skipped" in optimizer trace if no rowid filter
* [Revision #504cfa4857](https://github.com/MariaDB/server/commit/504cfa4857)\
  2024-12-03 19:06:34 +0200
  * Updated misc\_session\_status.test to not fail if select does not fail
* [Revision #e600f9aebb](https://github.com/MariaDB/server/commit/e600f9aebb)\
  2024-11-22 14:23:57 +0200
  * [MDEV-35750](https://jira.mariadb.org/browse/MDEV-35750) Change MEM\_ROOT allocation sizes to reduse calls to malloc() and avoid memory fragmentation
* [Revision #f297623345](https://github.com/MariaDB/server/commit/f297623345)\
  2024-12-01 16:05:58 +0200
  * Update my\_default\_record\_cache\_size if global.read\_buff\_size is changed
* [Revision #52c29f3bdc](https://github.com/MariaDB/server/commit/52c29f3bdc)\
  2024-11-21 12:28:57 +0200
  * [MDEV-35469](https://jira.mariadb.org/browse/MDEV-35469) Heap tables are calling mallocs to often
* Merge [Revision #f20ee931d8](https://github.com/MariaDB/server/commit/f20ee931d8) 2025-01-03 09:10:25 +0200 - Merge 10.5 into 10.6
* [Revision #07b77e862c](https://github.com/MariaDB/server/commit/07b77e862c)\
  2024-12-17 13:34:02 +0100
  * [MDEV-35660](https://jira.mariadb.org/browse/MDEV-35660) Assertion \`trx->xid.is\_null()' failed
* [Revision #3f22f5f2fe](https://github.com/MariaDB/server/commit/3f22f5f2fe)\
  2024-12-18 14:20:30 +0530
  * [MDEV-35679](https://jira.mariadb.org/browse/MDEV-35679) Potential issue in Secondary Index with ROW\_FORMAT=COMPRESSED and Change buffering enabled
* Merge [Revision #3cd9f9d1b3](https://github.com/MariaDB/server/commit/3cd9f9d1b3) 2024-12-18 05:09:23 +0100 - Merge branch '10.5' into '10.6'
* Merge [Revision #671f80c738](https://github.com/MariaDB/server/commit/671f80c738) 2024-12-17 11:06:09 +1100 - Merge branch '10.5' into 10.6
* [Revision #c982a143fc](https://github.com/MariaDB/server/commit/c982a143fc)\
  2024-12-16 13:23:13 +0200
  * [MDEV-35494](https://jira.mariadb.org/browse/MDEV-35494) fixup: Always initialize latch
* [Revision #c7698a0b70](https://github.com/MariaDB/server/commit/c7698a0b70)\
  2024-12-11 18:36:15 +0530
  * [MDEV-35626](https://jira.mariadb.org/browse/MDEV-35626) Race condition between buf\_page\_create\_low() and read completion
* [Revision #1097164d3f](https://github.com/MariaDB/server/commit/1097164d3f)\
  2024-12-13 11:41:47 +0200
  * [MDEV-35619](https://jira.mariadb.org/browse/MDEV-35619) Assertion failure in row\_purge\_del\_mark\_error
* Merge [Revision #155203c352](https://github.com/MariaDB/server/commit/155203c352) 2024-12-13 01:45:35 +0100 - Merge branch '10.5' into '10.6'
* [Revision #ddd7d5d8e3](https://github.com/MariaDB/server/commit/ddd7d5d8e3)\
  2024-12-12 18:02:00 +0200
  * [MDEV-24035](https://jira.mariadb.org/browse/MDEV-24035) Failing assertion: UT\_LIST\_GET\_LEN(lock.trx\_locks) == 0 causing disruption and replication failure
* [Revision #9aa84cf57f](https://github.com/MariaDB/server/commit/9aa84cf57f)\
  2024-12-05 14:53:48 -0500
  * [MDEV-35587](https://jira.mariadb.org/browse/MDEV-35587) unit.innodb\_sync leaks memory on mac
* [Revision #7bcd6c610a](https://github.com/MariaDB/server/commit/7bcd6c610a)\
  2024-12-11 14:47:39 +0200
  * [MDEV-35618](https://jira.mariadb.org/browse/MDEV-35618) Bogus assertion failure 'recv\_sys.scanned\_lsn < max\_lsn + 32 \* 512U' during recovery
* Merge [Revision #69e20cab28](https://github.com/MariaDB/server/commit/69e20cab28) 2024-12-11 14:46:43 +0200 - Merge 10.5 into 10.6
* [Revision #bfe7c8ff0a](https://github.com/MariaDB/server/commit/bfe7c8ff0a)\
  2024-12-11 14:44:42 +0200
  * [MDEV-35494](https://jira.mariadb.org/browse/MDEV-35494) fil\_space\_t::fil\_space\_t() may be unsafe with GCC -flifetime-dse
* [Revision #7372ecc396](https://github.com/MariaDB/server/commit/7372ecc396)\
  2024-11-28 10:24:28 +0100
  * Restore the THD state correctly in parallel replication
* [Revision #d959acbbf8](https://github.com/MariaDB/server/commit/d959acbbf8)\
  2024-10-25 20:20:10 +0200
  * [MDEV-34049](https://jira.mariadb.org/browse/MDEV-34049): Parallel access to temptable in different domain\_id in parallel replication
* Merge [Revision #0166c89e02](https://github.com/MariaDB/server/commit/0166c89e02) 2024-12-05 09:20:36 +0100 - Merge 10.5 -> 10.6
* Merge [Revision #cefdc3e67d](https://github.com/MariaDB/server/commit/cefdc3e67d) 2024-12-03 13:08:12 +0100 - Merge branch '10.5' into '10.6'
* [Revision #1a9011d273](https://github.com/MariaDB/server/commit/1a9011d273)\
  2024-11-29 15:12:20 +0200
  * [MDEV-35525](https://jira.mariadb.org/browse/MDEV-35525): Index corruption in reverse scans
* [Revision #507323abe6](https://github.com/MariaDB/server/commit/507323abe6)\
  2024-11-29 14:16:34 +0200
  * Cleanup: Remove duplicated code
* [Revision #998a625d00](https://github.com/MariaDB/server/commit/998a625d00)\
  2024-11-29 14:16:11 +0200
  * Clean up recv\_sys.pages bookkeeping
* Merge [Revision #7d4077cc11](https://github.com/MariaDB/server/commit/7d4077cc11) 2024-11-29 12:37:46 +0200 - Merge 10.5 into 10.6
* [Revision #19acb0257e](https://github.com/MariaDB/server/commit/19acb0257e)\
  2024-11-29 10:44:38 +0200
  * [MDEV-35508](https://jira.mariadb.org/browse/MDEV-35508) Race condition between purge and secondary index INSERT or UPDATE
* [Revision #1d76fdfcb9](https://github.com/MariaDB/server/commit/1d76fdfcb9)\
  2024-10-29 16:09:56 +0100
  * Adapt galera\_sr.GCF-572 to make it work with innodb-snapshot-isolation
* [Revision #e821c9fa7c](https://github.com/MariaDB/server/commit/e821c9fa7c)\
  2024-10-29 10:47:20 +0100
  * [MDEV-35281](https://jira.mariadb.org/browse/MDEV-35281) SR transaction crashes with innodb\_snapshot\_isolation
* [Revision #f5aed74573](https://github.com/MariaDB/server/commit/f5aed74573)\
  2024-11-25 10:07:04 +0200
  * [MDEV-35486](https://jira.mariadb.org/browse/MDEV-35486) : [MDEV-33997](https://jira.mariadb.org/browse/MDEV-33997) test failed
* [Revision #9ba18d1aa0](https://github.com/MariaDB/server/commit/9ba18d1aa0)\
  2024-11-27 13:00:51 +0530
  * [MDEV-35394](https://jira.mariadb.org/browse/MDEV-35394) Innochecksum misinterprets freed pages
* [Revision #2255be0395](https://github.com/MariaDB/server/commit/2255be0395)\
  2024-11-25 10:31:57 +0200
  * [MDEV-35472](https://jira.mariadb.org/browse/MDEV-35472) Server crash in ha\_storage\_put\_memlim upon reading from INNODB\_LOCKS
* [Revision #ec58fce3da](https://github.com/MariaDB/server/commit/ec58fce3da)\
  2024-11-21 14:34:28 -0700
  * [MDEV-35478](https://jira.mariadb.org/browse/MDEV-35478) Correction for table->space\_id in dict\_load\_tablespace() was mistakenly applied on an earlier branch
* [Revision #26597b91b3](https://github.com/MariaDB/server/commit/26597b91b3)\
  2024-11-22 08:33:03 +0200
  * [MDEV-35413](https://jira.mariadb.org/browse/MDEV-35413) InnoDB: Cannot load compressed BLOB
* [Revision #a06d81ff3f](https://github.com/MariaDB/server/commit/a06d81ff3f)\
  2024-11-21 11:28:59 -0700
  * [MDEV-35477](https://jira.mariadb.org/browse/MDEV-35477): rpl\_semi\_sync\_no\_missed\_ack\_after\_add\_slave fails after [MDEV-35109](https://jira.mariadb.org/browse/MDEV-35109)
* [Revision #895cd553a3](https://github.com/MariaDB/server/commit/895cd553a3)\
  2024-11-21 11:01:30 +0200
  * [MDEV-32175](https://jira.mariadb.org/browse/MDEV-32175): Reduce page\_align(), page\_offset() calls
* [Revision #df3855a471](https://github.com/MariaDB/server/commit/df3855a471)\
  2024-11-21 08:59:31 +0200
  * [MDEV-35247](https://jira.mariadb.org/browse/MDEV-35247): ut\_hash\_ulint() is a waste
* [Revision #a9b0a1c5d0](https://github.com/MariaDB/server/commit/a9b0a1c5d0)\
  2024-11-21 08:59:17 +0200
  * [MDEV-35247](https://jira.mariadb.org/browse/MDEV-35247): ut\_fold\_ull() is a waste
* [Revision #3c312d247c](https://github.com/MariaDB/server/commit/3c312d247c)\
  2024-11-21 08:59:02 +0200
  * [MDEV-35190](https://jira.mariadb.org/browse/MDEV-35190) HASH\_SEARCH duplicates effort before HASH\_INSERT or HASH\_DELETE
* [Revision #bcbeef6772](https://github.com/MariaDB/server/commit/bcbeef6772)\
  2024-11-20 17:43:04 +0300
  * [MDEV-35457](https://jira.mariadb.org/browse/MDEV-35457) Remove btr\_cur\_t::path\_arr
* [Revision #ba69d811fa](https://github.com/MariaDB/server/commit/ba69d811fa)\
  2024-11-18 08:13:18 +0200
  * [MDEV-35409](https://jira.mariadb.org/browse/MDEV-35409) InnoDB can still hang while running out of buffer pool
* [Revision #d5f16d6305](https://github.com/MariaDB/server/commit/d5f16d6305)\
  2024-11-15 17:19:36 -0700
  * Extract some of #3360 fixes to 10.6.x
* [Revision #c4843c10a3](https://github.com/MariaDB/server/commit/c4843c10a3)\
  2024-11-14 17:05:31 +0400
  * [MDEV-35416](https://jira.mariadb.org/browse/MDEV-35416) CONV(1<<63, 10, -2) fails with --view-protocol
* [Revision #3b20045071](https://github.com/MariaDB/server/commit/3b20045071)\
  2024-11-13 16:38:45 +0400
  * [MDEV-35393](https://jira.mariadb.org/browse/MDEV-35393) ASAN unknown-crash in Field\_varstring::reset when inserting NULL value to a table with filename charset
* [Revision #8e1cf078a0](https://github.com/MariaDB/server/commit/8e1cf078a0)\
  2024-11-14 15:32:55 +0530
  * [MDEV-35363](https://jira.mariadb.org/browse/MDEV-35363) Avoid cloning of table statistics while saving the InnoDB table stats
* [Revision #b8f48d09cf](https://github.com/MariaDB/server/commit/b8f48d09cf)\
  2024-11-14 10:58:39 +0530
  * [MDEV-35363](https://jira.mariadb.org/browse/MDEV-35363) Avoid cloning of table statistics while saving the InnoDB table stats
* [Revision #25be7da202](https://github.com/MariaDB/server/commit/25be7da202)\
  2024-11-13 14:27:12 +0400
  * [MDEV-32755](https://jira.mariadb.org/browse/MDEV-32755) Stack-Buffer-Overflow at /mariadb-11.3.0/strings/int2str.c:122
* [Revision #ccb6cd8053](https://github.com/MariaDB/server/commit/ccb6cd8053)\
  2024-11-12 12:17:34 +0200
  * [MDEV-35189](https://jira.mariadb.org/browse/MDEV-35189): Updating cache for INNODB\_LOCKS et al is suboptimal
* Merge [Revision #074831ec61](https://github.com/MariaDB/server/commit/074831ec61) 2024-11-08 18:17:15 +0530 - Merge branch 10.5 into 10.6
* [Revision #ba4541ba7f](https://github.com/MariaDB/server/commit/ba4541ba7f)\
  2024-11-08 09:55:47 +0200
  * [MDEV-29015](https://jira.mariadb.org/browse/MDEV-29015)/[MDEV-29260](https://jira.mariadb.org/browse/MDEV-29260)/[MDEV-34938](https://jira.mariadb.org/browse/MDEV-34938) test fixup
* [Revision #716ed2ce22](https://github.com/MariaDB/server/commit/716ed2ce22)\
  2024-11-05 12:26:33 -0700
  * [MDEV-35350](https://jira.mariadb.org/browse/MDEV-35350): Consolidate MTR wait\_for\_pattern\_in\_file.inc and SEARCH\_WAIT in search\_pattern\_in\_file.inc
* [Revision #8c9f68cd0f](https://github.com/MariaDB/server/commit/8c9f68cd0f)\
  2024-11-05 12:22:35 -0700
  * [MDEV-35350](https://jira.mariadb.org/browse/MDEV-35350): Backport search\_pattern\_in\_file.inc for SEARCH\_WAIT functionality
* [Revision #b9f9d804f2](https://github.com/MariaDB/server/commit/b9f9d804f2)\
  2024-11-06 15:45:59 +0400
  * [MDEV-28686](https://jira.mariadb.org/browse/MDEV-28686) Assertion \`0' in Type\_handler\_string\_result::make\_sort\_key or unexpected result
* [Revision #4ded2cbe13](https://github.com/MariaDB/server/commit/4ded2cbe13)\
  2024-11-06 11:01:47 +0400
  * [MDEV-31910](https://jira.mariadb.org/browse/MDEV-31910) ASAN memcpy-param-overlap upon CONCAT in ORACLE mode
* [Revision #faf9e755ba](https://github.com/MariaDB/server/commit/faf9e755ba)\
  2024-11-05 22:38:55 +0100
  * [MDEV-35109](https://jira.mariadb.org/browse/MDEV-35109) fix test case
* [Revision #7a62b029b3](https://github.com/MariaDB/server/commit/7a62b029b3)\
  2024-11-05 17:36:28 +0100
  * post-merge cleanup - remove copy\&paste code in fil\_node\_t::find\_metadata
* [Revision #a2a0adbfc3](https://github.com/MariaDB/server/commit/a2a0adbfc3)\
  2024-11-05 18:12:05 +0100
  * [MDEV-34533](https://jira.mariadb.org/browse/MDEV-34533) post-fix
* Merge [Revision #37b7986467](https://github.com/MariaDB/server/commit/37b7986467) 2024-11-05 21:02:22 +0100 - Merge branch '10.5' into 10.6
* [Revision #7741065936](https://github.com/MariaDB/server/commit/7741065936)\
  2024-11-05 12:36:08 +0400
  * [MDEV-23895](https://jira.mariadb.org/browse/MDEV-23895) Server crash, ASAN heap-buffer-overflow or Valgrind Invalid write in Item\_func\_rpad::val\_str
* [Revision #eb41c1171e](https://github.com/MariaDB/server/commit/eb41c1171e)\
  2024-11-05 11:16:10 +0400
  * [MDEV-33942](https://jira.mariadb.org/browse/MDEV-33942) View cuts off the end of string with the utf8 character set in INSERT function
* [Revision #c2bf1d4781](https://github.com/MariaDB/server/commit/c2bf1d4781)\
  2024-11-05 09:19:05 +0400
  * [MDEV-29552](https://jira.mariadb.org/browse/MDEV-29552) LEFT and RIGHT with big value for parameter 'len' >0 return empty value in view
* [Revision #b07258a0d5](https://github.com/MariaDB/server/commit/b07258a0d5)\
  2024-10-30 12:16:32 -0600
  * [MDEV-35109](https://jira.mariadb.org/browse/MDEV-35109): Semi-sync Replication stalling Primary using wait point=AFTER\_SYNC
* [Revision #5290fa043b](https://github.com/MariaDB/server/commit/5290fa043b)\
  2024-11-01 13:13:07 -0600
  * [MDEV-35109](https://jira.mariadb.org/browse/MDEV-35109) PREP: simulate\_delay\_semisync\_slave\_reply use debug\_sync
* Merge [Revision #f2bb2ab58c](https://github.com/MariaDB/server/commit/f2bb2ab58c) 2024-11-04 07:40:45 +0100 - Merge branch '10.6' into mariadb-10.6.20
* [Revision #0e0720c862](https://github.com/MariaDB/server/commit/0e0720c862)\
  2024-11-01 11:14:23 -0400
  * bump the VERSION
* [Revision #d661bc1552](https://github.com/MariaDB/server/commit/d661bc1552)\
  2024-11-01 14:18:58 +0400
  * [MDEV-20944](https://jira.mariadb.org/browse/MDEV-20944) Wrong result of LEAST() and ASAN heap-use-after-free in my\_strnncollsp\_simple / Item::temporal\_precision on TIME()
* [Revision #dd41be2a51](https://github.com/MariaDB/server/commit/dd41be2a51)\
  2024-11-01 12:40:43 +0400
  * [MDEV-29184](https://jira.mariadb.org/browse/MDEV-29184) Assertion \`0' in Item\_row::illegal\_method\_call, Type\_handler\_row::Item\_update\_null\_value, Item::update\_null\_value
* [Revision #3734ff7c7e](https://github.com/MariaDB/server/commit/3734ff7c7e)\
  2024-10-31 12:15:46 +0300
  * [MDEV-34690](https://jira.mariadb.org/browse/MDEV-34690) lock\_rec\_unlock\_unmodified() causes deadlock
* [Revision #066f920484](https://github.com/MariaDB/server/commit/066f920484)\
  2024-10-07 18:11:26 +0300
  * [MDEV-35110](https://jira.mariadb.org/browse/MDEV-35110) Deadlock on Replica during BACKUP STAGE BLOCK\_COMMIT on XA transactions
