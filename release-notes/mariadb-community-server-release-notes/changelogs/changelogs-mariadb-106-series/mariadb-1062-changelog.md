# MariaDB 10.6.2 Changelog

The most recent release of [MariaDB 10.6](../../mariadb-10-6-series/what-is-mariadb-106.md) is:[**MariaDB 10.6.21**](../../mariadb-10-6-series/mariadb-10-6-21-release-notes.md) Stable (GA) [Download Now](https://mariadb.com/downloads/)[_Alternate download from mariadb.org_](https://downloads.mariadb.org/mariadb/10.6.21/)

[Download 10.6.2](https://downloads.mariadb.org/mariadb/10.6.2/)[Release Notes](../../mariadb-10-6-series/mariadb-1062-release-notes.md)[Changelog](mariadb-1062-changelog.md)[Overview of 10.6](../../mariadb-10-6-series/what-is-mariadb-106.md)

**Release date:** 18 Jun 2021

**Do not use non-stable (non-GA) releases in production!**

For the highlights of this release, see the[release notes](../../mariadb-10-6-series/mariadb-1062-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/server/tree/10.6) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Includes all fixes from [MariaDB 10.6.1](mariadb-1061-changelog.md)
* Includes all fixes from [MariaDB 10.5.10](../changelogs-mariadb-105-series/mariadb-10510-changelog.md)
* [Revision #59cf1a8a8a](https://github.com/MariaDB/server/commit/59cf1a8a8a)\
  2021-06-17 12:12:42 +0200
  * update C/C
* [Revision #44db6ffc19](https://github.com/MariaDB/server/commit/44db6ffc19)\
  2021-06-17 14:53:22 +0700
  * [MDEV-16708](https://jira.mariadb.org/browse/MDEV-16708): fixed failure of the test sys\_vars.sql\_select\_limit\_func
* [Revision #3d752f0a3a](https://github.com/MariaDB/server/commit/3d752f0a3a)\
  2021-06-16 20:40:40 +0200
  * [MDEV-16708](https://jira.mariadb.org/browse/MDEV-16708): correct server side cursor detection in embedded
* [Revision #12bcbfc978](https://github.com/MariaDB/server/commit/12bcbfc978)\
  2021-06-16 16:18:15 +0200
  * [MDEV-16708](https://jira.mariadb.org/browse/MDEV-16708): extract nonembedded part of the test into a separate file
* [Revision #aedf314333](https://github.com/MariaDB/server/commit/aedf314333)\
  2021-06-16 14:49:19 +0200
  * [MDEV-16708](https://jira.mariadb.org/browse/MDEV-16708): spurious ER\_NEED\_REPREPARE for gtid\_slave\_pos and event\_scheduler
* [Revision #510662e81b](https://github.com/MariaDB/server/commit/510662e81b)\
  2021-06-16 13:18:29 +0200
  * [MDEV-16708](https://jira.mariadb.org/browse/MDEV-16708): more fixes to test cases
* [Revision #97e8d27bed](https://github.com/MariaDB/server/commit/97e8d27bed)\
  2021-06-10 11:12:27 +0700
  * [MDEV-16708](https://jira.mariadb.org/browse/MDEV-16708): fix in test failures(added --enable\_prepared\_warnings/--disable\_prepared\_warnings)
* [Revision #fe78495053](https://github.com/MariaDB/server/commit/fe78495053)\
  2021-06-11 11:25:56 +0700
  * [MDEV-16708](https://jira.mariadb.org/browse/MDEV-16708): fixed assert firing in the method THD::reset\_for\_the\_next\_command
* [Revision #994e3f40b5](https://github.com/MariaDB/server/commit/994e3f40b5)\
  2021-06-10 01:00:31 +0700
  * [MDEV-16708](https://jira.mariadb.org/browse/MDEV-16708): fixed incorrect issuing the error
* [Revision #ccb0504fb0](https://github.com/MariaDB/server/commit/ccb0504fb0)\
  2021-06-09 23:03:34 +0700
  * [MDEV-16708](https://jira.mariadb.org/browse/MDEV-16708): fix in test failures caused by missing warnings received in prepare response packet
* [Revision #b126c3f3fa](https://github.com/MariaDB/server/commit/b126c3f3fa)\
  2021-06-07 00:39:15 +0700
  * [MDEV-16708](https://jira.mariadb.org/browse/MDEV-16708): fixed issue with handling of the directive --enable-prepared-warnings in mysqltest
* [Revision #fc71746a6a](https://github.com/MariaDB/server/commit/fc71746a6a)\
  2021-06-04 12:59:24 +0700
  * [MDEV-16708](https://jira.mariadb.org/browse/MDEV-16708): Fixed ths issue with handling of ERR packet received by mysqltest on response to COM\_STMT\_EXECUTE
* [Revision #a72098421c](https://github.com/MariaDB/server/commit/a72098421c)\
  2021-05-30 21:49:34 +0700
  * [MDEV-16708](https://jira.mariadb.org/browse/MDEV-16708): Unsupported commands for prepared statements
* [Revision #a3a80420ea](https://github.com/MariaDB/server/commit/a3a80420ea)\
  2021-05-19 12:30:06 +0700
  * [MDEV-16708](https://jira.mariadb.org/browse/MDEV-16708): disabled the test main.sp to be executed with ps-protocol
* [Revision #a00b51f639](https://github.com/MariaDB/server/commit/a00b51f639)\
  2021-05-19 11:28:58 +0700
  * [MDEV-16708](https://jira.mariadb.org/browse/MDEV-16708): Fixed the failed test main.set\_statement
* [Revision #b33111ba93](https://github.com/MariaDB/server/commit/b33111ba93)\
  2021-05-18 08:50:57 +0700
  * [MDEV-16708](https://jira.mariadb.org/browse/MDEV-16708): Fixed the failed test main.join\_cache
* [Revision #129098b70c](https://github.com/MariaDB/server/commit/129098b70c)\
  2021-05-11 15:16:55 +0700
  * [MDEV-16708](https://jira.mariadb.org/browse/MDEV-16708): Unsupported commands for prepared statements
* [Revision #4decc03b28](https://github.com/MariaDB/server/commit/4decc03b28)\
  2021-05-06 13:55:57 +0700
  * [MDEV-16708](https://jira.mariadb.org/browse/MDEV-16708): Unsupported commands for prepared statements
* [Revision #5478ca779a](https://github.com/MariaDB/server/commit/5478ca779a)\
  2021-05-05 17:56:12 +0700
  * [MDEV-25576](https://jira.mariadb.org/browse/MDEV-25576): The statement EXPLAIN running as regular statement and as prepared statement produces different results for UPDATE with subquery
* [Revision #f536974b73](https://github.com/MariaDB/server/commit/f536974b73)\
  2021-04-29 17:16:56 +0700
  * [MDEV-16708](https://jira.mariadb.org/browse/MDEV-16708): Unsupported commands for prepared statements
* [Revision #8754fce8b0](https://github.com/MariaDB/server/commit/8754fce8b0)\
  2021-04-28 12:44:46 +0700
  * [MDEV-16708](https://jira.mariadb.org/browse/MDEV-16708): Unsupported commands for prepared statements
* [Revision #aeca826c5f](https://github.com/MariaDB/server/commit/aeca826c5f)\
  2021-04-27 16:49:17 +0700
  * [MDEV-16708](https://jira.mariadb.org/browse/MDEV-16708): Unsupported commands for prepared statements
* [Revision #7586eead5d](https://github.com/MariaDB/server/commit/7586eead5d)\
  2021-04-26 10:47:10 +0700
  * [MDEV-16708](https://jira.mariadb.org/browse/MDEV-16708): Unsupported commands for prepared statements
* [Revision #327402291a](https://github.com/MariaDB/server/commit/327402291a)\
  2021-04-22 23:57:49 +0700
  * [MDEV-16708](https://jira.mariadb.org/browse/MDEV-16708): Unsupported commands for prepared statements
* [Revision #d5836a6277](https://github.com/MariaDB/server/commit/d5836a6277)\
  2021-04-22 23:21:54 +0700
  * [MDEV-16708](https://jira.mariadb.org/browse/MDEV-16708): Unsupported commands for prepared statements
* [Revision #9370c6e83c](https://github.com/MariaDB/server/commit/9370c6e83c)\
  2021-04-22 14:52:19 +0700
  * [MDEV-16708](https://jira.mariadb.org/browse/MDEV-16708): Unsupported commands for prepared statements
* [Revision #f778a5d5e2](https://github.com/MariaDB/server/commit/f778a5d5e2)\
  2021-06-17 13:46:16 +0300
  * [MDEV-25854](https://jira.mariadb.org/browse/MDEV-25854): Remove garbage tables after restoring a backup
* [Revision #e95f78f475](https://github.com/MariaDB/server/commit/e95f78f475)\
  2021-06-16 17:10:11 +0300
  * [MDEV-21117](https://jira.mariadb.org/browse/MDEV-21117) post-push to cover a "custom" xid format
* [Revision #da65cb4d97](https://github.com/MariaDB/server/commit/da65cb4d97)\
  2021-06-16 12:23:41 +0300
  * [MDEV-25936](https://jira.mariadb.org/browse/MDEV-25936) Crash during DDL that involves FULLTEXT INDEX
* [Revision #71964c76fe](https://github.com/MariaDB/server/commit/71964c76fe)\
  2021-06-16 09:03:02 +0300
  * [MDEV-25910](https://jira.mariadb.org/browse/MDEV-25910): Aim to make all InnoDB DDL durable
* [Revision #e5b9dc1536](https://github.com/MariaDB/server/commit/e5b9dc1536)\
  2021-06-15 22:14:51 +0300
  * [MDEV-25910](https://jira.mariadb.org/browse/MDEV-25910): Make ALTER TABLE...ALGORITHM=COPY durable again
* [Revision #e0647dc733](https://github.com/MariaDB/server/commit/e0647dc733)\
  2021-06-14 19:53:23 +0200
  * update C/C to 3.2.2-rc
* [Revision #79a2dbc879](https://github.com/MariaDB/server/commit/79a2dbc879)\
  2021-06-14 19:22:29 +0300
  * [MDEV-21117](https://jira.mariadb.org/browse/MDEV-21117) post-push fixes
* [Revision #e41522d6bf](https://github.com/MariaDB/server/commit/e41522d6bf)\
  2021-06-15 01:34:14 +0300
  * Updated libmarias3
* [Revision #278ab53849](https://github.com/MariaDB/server/commit/278ab53849)\
  2021-06-14 21:33:42 +0300
  * Updated libmarias3 to latest version
* [Revision #6653206467](https://github.com/MariaDB/server/commit/6653206467)\
  2021-06-13 19:46:16 +0300
  * Fixed compiler warnings
* [Revision #6e282e7efc](https://github.com/MariaDB/server/commit/6e282e7efc)\
  2021-06-14 18:40:06 +0300
  * [MDEV-20787](https://jira.mariadb.org/browse/MDEV-20787) Script dgcov.pl does not work
* [Revision #7f0024a54f](https://github.com/MariaDB/server/commit/7f0024a54f)\
  2021-06-14 19:51:37 +0300
  * Fixed BUILD scripts to remove all .gcov and .gcno files from submodules
* [Revision #c2c10094a8](https://github.com/MariaDB/server/commit/c2c10094a8)\
  2021-06-13 19:38:16 +0300
  * Made main.flush more resilient for parallel threads
* [Revision #af33202af7](https://github.com/MariaDB/server/commit/af33202af7)\
  2021-06-11 15:34:23 +0300
  * Added DDL\_options\_st \*thd\_ddl\_options(const MYSQL\_THD thd)
* [Revision #4ea1c48abe](https://github.com/MariaDB/server/commit/4ea1c48abe)\
  2021-06-09 14:49:58 +0300
  * Added a function comment to Field\_varstring::mark\_unused\_memory\_as\_defined()
* [Revision #8d37ef2999](https://github.com/MariaDB/server/commit/8d37ef2999)\
  2021-06-09 14:48:28 +0300
  * Aria now marks not used varchar space with MEM\_UNDEFINED on read.
* [Revision #15d2a6cfa3](https://github.com/MariaDB/server/commit/15d2a6cfa3)\
  2021-06-11 14:26:50 +0300
  * Fixed mysql-test-run "Waiting ... seconds for pidfile" output
* [Revision #6f15a8e4f7](https://github.com/MariaDB/server/commit/6f15a8e4f7)\
  2021-06-11 14:24:03 +0300
  * Don't run test "forever" with mysql-test-run --valgrind
* [Revision #9d261eeca8](https://github.com/MariaDB/server/commit/9d261eeca8)\
  2021-06-09 14:46:33 +0300
  * Marked some very slow mtr tests with not\_valgrind
* [Revision #9c778285ea](https://github.com/MariaDB/server/commit/9c778285ea)\
  2021-06-09 14:44:13 +0300
  * Added comments to some BUILD scripts
* [Revision #193bfdd831](https://github.com/MariaDB/server/commit/193bfdd831)\
  2021-02-08 14:52:04 +0530
  * [MDEV-22010](https://jira.mariadb.org/browse/MDEV-22010): use executables MariaDB named in scripts
* [Revision #cb0cad8156](https://github.com/MariaDB/server/commit/cb0cad8156)\
  2021-06-14 10:06:27 +0300
  * [MDEV-25907](https://jira.mariadb.org/browse/MDEV-25907): Assertion failed in dict\_table\_schema\_check()
* [Revision #6ba938af62](https://github.com/MariaDB/server/commit/6ba938af62)\
  2021-06-14 09:15:20 +0300
  * [MDEV-25905](https://jira.mariadb.org/browse/MDEV-25905): Assertion table2==NULL in dict\_sys\_t::add()
* [Revision #28e362eaca](https://github.com/MariaDB/server/commit/28e362eaca)\
  2021-06-14 08:57:04 +0300
  * [MDEV-25760](https://jira.mariadb.org/browse/MDEV-25760): Resubmit IO job on -EAGAIN from io\_uring
* [Revision #74a0a9877b](https://github.com/MariaDB/server/commit/74a0a9877b)\
  2021-06-14 12:09:12 +0300
  * [MDEV-24731](https://jira.mariadb.org/browse/MDEV-24731) fixup: Another bogus assertion
* [Revision #4a184f52b0](https://github.com/MariaDB/server/commit/4a184f52b0)\
  2021-06-14 12:33:23 +0300
  * [MDEV-21117](https://jira.mariadb.org/browse/MDEV-21117) fixup: Fix the test parts.backup\_log\_rocksdb
* [Revision #6c39eaeb12](https://github.com/MariaDB/server/commit/6c39eaeb12)\
  2020-04-09 20:45:45 +0530
  * [MDEV-21117](https://jira.mariadb.org/browse/MDEV-21117): refine the server binlog-based recovery for semisync
* [Revision #82c07b178a](https://github.com/MariaDB/server/commit/82c07b178a)\
  2021-06-11 15:58:50 +0300
  * [MDEV-25288](https://jira.mariadb.org/browse/MDEV-25288) follow-up: Remove traces of unstable-tests
* [Revision #f4943b4ace](https://github.com/MariaDB/server/commit/f4943b4ace)\
  2021-06-10 13:43:52 +0200
  * cleanup perfschema.short\_options\_1 test
* [Revision #773ee80fab](https://github.com/MariaDB/server/commit/773ee80fab)\
  2020-10-13 13:29:05 +0200
  * federatedx: ha\_federatedx::get\_txn -> static
* [Revision #4d0b33958d](https://github.com/MariaDB/server/commit/4d0b33958d)\
  2020-10-13 14:24:29 +0200
  * don't show DBUG\_ASSERT to plugins
* [Revision #abc3889f1c](https://github.com/MariaDB/server/commit/abc3889f1c)\
  2020-09-28 10:51:18 +0200
  * cleanup: rename Protocol::store() to Protocol::store\_datetime()
* [Revision #59b51e6aa7](https://github.com/MariaDB/server/commit/59b51e6aa7)\
  2020-10-02 00:03:20 +0200
  * cleanup: Field\_set::empty\_set\_string
* [Revision #3648b333c7](https://github.com/MariaDB/server/commit/3648b333c7)\
  2021-06-09 18:31:23 +0200
  * cleanup: formatting
* [Revision #89342a3bd5](https://github.com/MariaDB/server/commit/89342a3bd5)\
  2021-06-09 18:32:09 +0200
  * change maturity to gamma
* [Revision #ff3fd02249](https://github.com/MariaDB/server/commit/ff3fd02249)\
  2021-06-11 13:06:05 +0300
  * [MDEV-25288](https://jira.mariadb.org/browse/MDEV-25288) follow-up: Remove mysql-test/unstable-tests
* [Revision #102ff4208d](https://github.com/MariaDB/server/commit/102ff4208d)\
  2021-06-09 13:13:06 +0800
  * [MDEV-25882](https://jira.mariadb.org/browse/MDEV-25882): Statistics used to track b-tree (non-adaptive) searches should be updated only when adaptive hashing is turned-on
* [Revision #6fbf978eec](https://github.com/MariaDB/server/commit/6fbf978eec)\
  2021-06-09 22:06:11 +0300
  * [MDEV-25750](https://jira.mariadb.org/browse/MDEV-25750): Assertion wait\_lock->is\_waiting() in lock\_wait\_rpl\_report
* [Revision #1bd681c8b3](https://github.com/MariaDB/server/commit/1bd681c8b3)\
  2021-06-09 17:02:55 +0300
  * [MDEV-25506](https://jira.mariadb.org/browse/MDEV-25506) (3 of 3): Do not delete .ibd files before commit
* [Revision #3f78fbc582](https://github.com/MariaDB/server/commit/3f78fbc582)\
  2021-06-09 16:58:52 +0300
  * [MDEV-25180](https://jira.mariadb.org/browse/MDEV-25180) fixup: Assertion table->def\_trx\_id == trx->id... failed in row\_merge\_drop\_indexes()
* [Revision #6a4e5bf1f5](https://github.com/MariaDB/server/commit/6a4e5bf1f5)\
  2021-06-09 12:31:02 +0300
  * [MDEV-25852](https://jira.mariadb.org/browse/MDEV-25852): Orphan #sql\*.ibd files are left behind
* Merge [Revision #65f1a42788](https://github.com/MariaDB/server/commit/65f1a42788) 2021-06-09 16:50:58 +0300 - Merge 10.5 into 10.6
* Merge [Revision #b25d2a4578](https://github.com/MariaDB/server/commit/b25d2a4578) 2021-06-09 14:29:58 +0300 - Merge 10.4 into 10.5
* Merge [Revision #c7ee039d36](https://github.com/MariaDB/server/commit/c7ee039d36) 2021-06-09 14:28:57 +0300 - Merge 10.3 to 10.4
* [Revision #75a65d3201](https://github.com/MariaDB/server/commit/75a65d3201)\
  2021-06-09 14:23:20 +0300
  * [MDEV-25886](https://jira.mariadb.org/browse/MDEV-25886) CHECK TABLE crash with DB\_MISSING\_HISTORY if innodb\_read\_only
* Merge [Revision #f4425d3a3d](https://github.com/MariaDB/server/commit/f4425d3a3d) 2021-06-08 16:03:53 +0300 - Merge 10.4 into 10.5
* [Revision #b8d38c5e39](https://github.com/MariaDB/server/commit/b8d38c5e39)\
  2021-06-08 15:03:50 +0300
  * dict\_index\_build\_internal\_clust(): Catch [MDEV-20131](https://jira.mariadb.org/browse/MDEV-20131) on CREATE TABLE
* Merge [Revision #72b2489621](https://github.com/MariaDB/server/commit/72b2489621) 2021-06-08 15:02:40 +0300 - Merge 10.3 into 10.4
* Merge [Revision #6e9642beb2](https://github.com/MariaDB/server/commit/6e9642beb2) 2021-06-08 14:33:07 +0300 - Merge 10.2 into 10.3
* [Revision #dfa2d0bc13](https://github.com/MariaDB/server/commit/dfa2d0bc13)\
  2021-06-07 17:46:59 +0300
  * [MDEV-25869](https://jira.mariadb.org/browse/MDEV-25869) Change buffer entries are lost on InnoDB restart
* [Revision #3c922d6def](https://github.com/MariaDB/server/commit/3c922d6def)\
  2021-05-28 22:04:17 -0700
  * Revert "CONNECT: move jar files to /usr/share and include them in DEBs"
* [Revision #9f9a925c39](https://github.com/MariaDB/server/commit/9f9a925c39)\
  2021-06-06 08:46:59 +0200
  * [MDEV-23815](https://jira.mariadb.org/browse/MDEV-23815) Windows : mysql\_upgrade\_wizard fails, if service name has spaces
* [Revision #cebc435592](https://github.com/MariaDB/server/commit/cebc435592)\
  2021-06-05 16:57:10 +0200
  * [MDEV-25859](https://jira.mariadb.org/browse/MDEV-25859) - HeidiSQL 11.3
* [Revision #7eed97ed9f](https://github.com/MariaDB/server/commit/7eed97ed9f)\
  2021-05-26 14:15:26 +0200
  * [MDEV-25777](https://jira.mariadb.org/browse/MDEV-25777): JAVA\_INCLUDE\_PATH and JAVA\_INCLUDE\_PATH2 not found with out of source configuration and Ninja generator
* [Revision #5c896472b6](https://github.com/MariaDB/server/commit/5c896472b6)\
  2021-06-02 23:10:21 +0200
  * [MDEV-25672](https://jira.mariadb.org/browse/MDEV-25672) table alias from previous statement interferes later commands
* [Revision #2e78910806](https://github.com/MariaDB/server/commit/2e78910806)\
  2021-06-02 08:40:30 -0700
  * [MDEV-25635](https://jira.mariadb.org/browse/MDEV-25635) Assertion failure when pushing from HAVING into WHERE of view
* [Revision #8149e4d0a1](https://github.com/MariaDB/server/commit/8149e4d0a1)\
  2021-06-07 15:08:18 -0700
  * [MDEV-25682](https://jira.mariadb.org/browse/MDEV-25682) Explain shows an execution plan different from actually executed
* [Revision #b1b4d67bcd](https://github.com/MariaDB/server/commit/b1b4d67bcd)\
  2021-06-04 15:00:34 +0200
  * [MDEV-21373](https://jira.mariadb.org/browse/MDEV-21373) DBUG compilation - bad synchronization in ha\_heap::external\_lock()
* [Revision #bb28bffc3e](https://github.com/MariaDB/server/commit/bb28bffc3e)\
  2021-06-07 19:51:57 -0700
  * Ported the test case for [MDEV-25682](https://jira.mariadb.org/browse/MDEV-25682) from 10.2
* [Revision #ddddfc33c7](https://github.com/MariaDB/server/commit/ddddfc33c7)\
  2021-06-04 14:57:11 +0200
  * Fix mtr tests with file\_key\_managment extension for Windows
* [Revision #bf5c050fd2](https://github.com/MariaDB/server/commit/bf5c050fd2)\
  2021-06-07 17:40:30 +0300
  * [MDEV-25866](https://jira.mariadb.org/browse/MDEV-25866) Upgrade from pre-10.5.10 to 10.5.10 causes CHECK errors on encrypted Aria tables
* [Revision #eed419b487](https://github.com/MariaDB/server/commit/eed419b487)\
  2021-06-07 15:38:38 +0300
  * Fixed a DBUG\_ASSERT when running zerofill() on aria tables
* [Revision #310dff5d84](https://github.com/MariaDB/server/commit/310dff5d84)\
  2021-06-07 19:07:45 +0300
  * [MDEV-25783](https://jira.mariadb.org/browse/MDEV-25783): Change buffer records are lost under heavy load
* [Revision #f456e716fe](https://github.com/MariaDB/server/commit/f456e716fe)\
  2021-06-02 18:29:30 +0300
  * Make maria.repair more resiliant for different failures
* [Revision #d4a6e3a698](https://github.com/MariaDB/server/commit/d4a6e3a698)\
  2021-05-06 12:08:38 -0700
  * Deb: Misc cleanup and autobake-deb.sh and Salsa-CI fixes
* Merge [Revision #3c97097f11](https://github.com/MariaDB/server/commit/3c97097f11) 2021-06-04 10:07:29 +0300 - Merge 10.4 into 10.5
* Merge [Revision #bab4348c6c](https://github.com/MariaDB/server/commit/bab4348c6c) 2021-06-04 09:42:18 +0300 - Merge 10.3 into 10.4
* [Revision #2d38c5e64e](https://github.com/MariaDB/server/commit/2d38c5e64e)\
  2021-06-04 09:35:18 +0300
  * [MDEV-17749](https://jira.mariadb.org/browse/MDEV-17749) fixup: ./mtr --embedded main.lock\_kill (again)
* [Revision #663bc849b5](https://github.com/MariaDB/server/commit/663bc849b5)\
  2021-05-26 23:41:59 -0700
  * [MDEV-25714](https://jira.mariadb.org/browse/MDEV-25714) Join using derived with aggregation returns incorrect results
* [Revision #385f4316c3](https://github.com/MariaDB/server/commit/385f4316c3)\
  2021-06-03 20:43:04 -0700
  * Corrected the test case of [MDEV-25714](https://jira.mariadb.org/browse/MDEV-25714) in order to have the same EXPLAIN output as in 10.3
* [Revision #0b797130c6](https://github.com/MariaDB/server/commit/0b797130c6)\
  2021-05-26 23:41:59 -0700
  * [MDEV-25714](https://jira.mariadb.org/browse/MDEV-25714) Join using derived with aggregation returns incorrect results
* [Revision #fa0bbff032](https://github.com/MariaDB/server/commit/fa0bbff032)\
  2021-06-02 14:05:12 +0300
  * Fixed that compile-pentium64-valgrind-max works
* [Revision #29e8c15417](https://github.com/MariaDB/server/commit/29e8c15417)\
  2021-05-03 09:43:43 +0200
  * [MDEV-25857](https://jira.mariadb.org/browse/MDEV-25857): MTR should report at least last test that was executed in case of shutdown and not-completed
* [Revision #8b02e02b27](https://github.com/MariaDB/server/commit/8b02e02b27)\
  2021-06-04 09:40:46 +0200
  * [MDEV-25698](https://jira.mariadb.org/browse/MDEV-25698) SIGSEGV in wsrep\_should\_replicate\_ddl
* [Revision #4927bf2534](https://github.com/MariaDB/server/commit/4927bf2534)\
  2021-06-07 16:50:55 +0200
  * [MDEV-25870](https://jira.mariadb.org/browse/MDEV-25870) Windows - MSI generation cleanup, fix ARM64
* [Revision #5ba4c4200c](https://github.com/MariaDB/server/commit/5ba4c4200c)\
  2021-06-06 22:22:03 +0200
  * [MDEV-25870](https://jira.mariadb.org/browse/MDEV-25870) Windows - fix ARM64 cross-compilation
* [Revision #233590a48d](https://github.com/MariaDB/server/commit/233590a48d)\
  2021-06-07 18:28:27 +0300
  * [MDEV-25754](https://jira.mariadb.org/browse/MDEV-25754) ASAN: stack-buffer-overflow in Field\_newdate::val\_str()
* [Revision #b1009ddfc9](https://github.com/MariaDB/server/commit/b1009ddfc9)\
  2021-06-07 18:15:39 +0300
  * [MDEV-25778](https://jira.mariadb.org/browse/MDEV-25778) Overrun buffer in to\_string\_native()
* [Revision #be84f9cea7](https://github.com/MariaDB/server/commit/be84f9cea7)\
  2021-06-07 13:48:56 +0300
  * Record in test suite that temporary tables only uses write locks
* [Revision #3d6eb7afcf](https://github.com/MariaDB/server/commit/3d6eb7afcf)\
  2021-06-06 13:21:03 +0200
  * [MDEV-25602](https://jira.mariadb.org/browse/MDEV-25602) get rid of WIN in favor of standard \_WIN32
* Merge [Revision #06dd151bb8](https://github.com/MariaDB/server/commit/06dd151bb8) 2021-06-02 11:31:01 +0300 - Merge 10.5 into 10.6
* [Revision #8426c7411b](https://github.com/MariaDB/server/commit/8426c7411b)\
  2021-06-02 08:48:09 +0300
  * [MDEV-23399](https://jira.mariadb.org/browse/MDEV-23399) fixup for [MDEV-10814](https://jira.mariadb.org/browse/MDEV-10814)
* Merge [Revision #49ab50f882](https://github.com/MariaDB/server/commit/49ab50f882) 2021-06-02 08:30:33 +0300 - Merge 10.4 into 10.5
* Merge [Revision #d3d2c96567](https://github.com/MariaDB/server/commit/d3d2c96567) 2021-06-02 08:29:47 +0300 - Merge 10.3 into 10.4
* Merge [Revision #aa70690e9a](https://github.com/MariaDB/server/commit/aa70690e9a) 2021-06-02 08:29:01 +0300 - Merge 10.2 into 10.3
* [Revision #a8434c6c59](https://github.com/MariaDB/server/commit/a8434c6c59)\
  2021-06-02 08:25:12 +0300
  * [MDEV-25730](https://jira.mariadb.org/browse/MDEV-25730) fixup: GCC -Og -Wmaybe-uninitialized
* [Revision #4847a2e730](https://github.com/MariaDB/server/commit/4847a2e730)\
  2021-06-02 08:28:48 +0300
  * [MDEV-17749](https://jira.mariadb.org/browse/MDEV-17749) fixup: ./mtr --embedded main.lock\_kill
* [Revision #6d21b6acb8](https://github.com/MariaDB/server/commit/6d21b6acb8)\
  2021-05-27 13:11:17 +0300
  * Updated main.trigger-trans.test to make it more resiliant
* [Revision #3dd91241cb](https://github.com/MariaDB/server/commit/3dd91241cb)\
  2021-06-01 10:25:27 +0200
  * [MDEV-24985](https://jira.mariadb.org/browse/MDEV-24985) Shutdown fails to abort current InnoDB lock waits
* [Revision #4555fb1722](https://github.com/MariaDB/server/commit/4555fb1722)\
  2021-06-01 15:46:52 +0300
  * After-merge fix: ./mtr --embedded main.lock\_kill
* Merge [Revision #a722ee88f3](https://github.com/MariaDB/server/commit/a722ee88f3) 2021-06-01 11:39:38 +0300 - Merge 10.5 into 10.6
* Merge [Revision #9c7a456a92](https://github.com/MariaDB/server/commit/9c7a456a92) 2021-06-01 10:38:09 +0300 - Merge 10.4 into 10.5
* Merge [Revision #77d8da57d7](https://github.com/MariaDB/server/commit/77d8da57d7) 2021-06-01 09:14:59 +0300 - Merge 10.3 into 10.4
* Merge [Revision #950a220060](https://github.com/MariaDB/server/commit/950a220060) 2021-06-01 08:40:59 +0300 - Merge 10.2 into 10.3
* [Revision #2fb4407827](https://github.com/MariaDB/server/commit/2fb4407827)\
  2021-05-29 19:54:25 +0200
  * [MDEV-25818](https://jira.mariadb.org/browse/MDEV-25818): RSYNC SST failed due to busy port
* [Revision #d3c77e08ae](https://github.com/MariaDB/server/commit/d3c77e08ae)\
  2021-05-31 12:27:47 +0200
  * [MDEV-20556](https://jira.mariadb.org/browse/MDEV-20556) Remove references to "xtrabackup" and "innobackupex" in mariadb-backup --help
* [Revision #91bde0fb67](https://github.com/MariaDB/server/commit/91bde0fb67)\
  2021-05-30 17:31:55 +0700
  * [MDEV-25576](https://jira.mariadb.org/browse/MDEV-25576): The statement EXPLAIN running as regular statement and as prepared statement produces different results for UPDATE with subquery
* [Revision #d06205ba37](https://github.com/MariaDB/server/commit/d06205ba37)\
  2021-05-27 14:00:58 +0200
  * CONNECT: use my\_snprintf
* [Revision #1638241e31](https://github.com/MariaDB/server/commit/1638241e31)\
  2021-05-27 12:06:21 +0200
  * mtr: fix the debug printout
* [Revision #ef0d883903](https://github.com/MariaDB/server/commit/ef0d883903)\
  2021-05-26 15:27:07 +0300
  * Revert "Add Pull Request template file to the MariaDB/server repository"
* [Revision #c11c5f36d8](https://github.com/MariaDB/server/commit/c11c5f36d8)\
  2021-05-24 19:40:47 +0530
  * [MDEV-25758](https://jira.mariadb.org/browse/MDEV-25758) InnoDB spatial indexes miss large geometry fields after [MDEV-25459](https://jira.mariadb.org/browse/MDEV-25459)
* [Revision #ab87fc6c7a](https://github.com/MariaDB/server/commit/ab87fc6c7a)\
  2021-05-27 09:31:19 +0300
  * Cleanup: Remove handler::update\_table\_comment()
* [Revision #17106c984b](https://github.com/MariaDB/server/commit/17106c984b)\
  2021-03-11 18:17:06 +0200
  * Add Pull Request template file to the MariaDB/server repository
* [Revision #d8fa71a089](https://github.com/MariaDB/server/commit/d8fa71a089)\
  2021-05-19 22:26:02 +0200
  * [MDEV-25730](https://jira.mariadb.org/browse/MDEV-25730): maria.repair test fails with valgrind
* [Revision #fe7e44d8ad](https://github.com/MariaDB/server/commit/fe7e44d8ad)\
  2021-05-25 05:08:25 +0200
  * [MDEV-21192](https://jira.mariadb.org/browse/MDEV-21192): SST failing when enabling IPV6
* [Revision #81f94c26a4](https://github.com/MariaDB/server/commit/81f94c26a4)\
  2021-05-24 16:48:27 +0200
  * [MDEV-15730](https://jira.mariadb.org/browse/MDEV-15730): rename --stream=xbstream to --stream=mbstream
* [Revision #1e5ebf3762](https://github.com/MariaDB/server/commit/1e5ebf3762)\
  2021-05-26 14:53:26 +0300
  * Fixed results for main.delete\_use\_source to make it repeatable
* [Revision #aa284e0237](https://github.com/MariaDB/server/commit/aa284e0237)\
  2021-05-26 14:35:23 +0300
  * [MDEV-17749](https://jira.mariadb.org/browse/MDEV-17749) Kill during LOCK TABLE ; ALTER TABLE causes assert
* [Revision #26f9ff0a60](https://github.com/MariaDB/server/commit/26f9ff0a60)\
  2021-05-26 11:11:27 +0300
  * Remove unnecessary test case
* [Revision #88ce7cf744](https://github.com/MariaDB/server/commit/88ce7cf744)\
  2021-05-26 09:06:32 +0300
  * [MDEV-25769](https://jira.mariadb.org/browse/MDEV-25769) : Galera test failure on galera\_sr.GCF-627
* [Revision #e212415690](https://github.com/MariaDB/server/commit/e212415690)\
  2021-05-24 18:58:57 +0300
  * [MDEV-25551](https://jira.mariadb.org/browse/MDEV-25551) applying crash with tables without PK
* [Revision #2a4f72b7d2](https://github.com/MariaDB/server/commit/2a4f72b7d2)\
  2021-06-01 09:09:56 +1000
  * [MDEV-25807](https://jira.mariadb.org/browse/MDEV-25807): ARM build failure due to missing ISB instruction on ARMv6
* [Revision #0d44792a83](https://github.com/MariaDB/server/commit/0d44792a83)\
  2021-05-26 10:23:43 +1000
  * perfschema: native type for my\_thread\_os\_id\_t
* [Revision #90adf2aa59](https://github.com/MariaDB/server/commit/90adf2aa59)\
  2021-05-26 09:52:00 +1000
  * perfschema: use glibc gettid if available
* [Revision #68eac8a3ad](https://github.com/MariaDB/server/commit/68eac8a3ad)\
  2021-05-24 15:28:20 +0200
  * my\_thread: Use unsigned long long for storing pthread IDs
* [Revision #139333a6cc](https://github.com/MariaDB/server/commit/139333a6cc)\
  2021-05-31 15:44:11 +0300
  * [MDEV-25745](https://jira.mariadb.org/browse/MDEV-25745): Not applying INSERT\_REUSE\_REDUNDANT
* [Revision #6ca065468f](https://github.com/MariaDB/server/commit/6ca065468f)\
  2021-05-27 16:46:11 +0300
  * [MDEV-19514](https://jira.mariadb.org/browse/MDEV-19514) fixup: Optimize ibuf\_merge\_or\_delete\_for\_page() calls
* [Revision #601eb41183](https://github.com/MariaDB/server/commit/601eb41183)\
  2021-05-27 16:17:43 +0300
  * Cleanup: deduplicate code
* [Revision #5bd517259f](https://github.com/MariaDB/server/commit/5bd517259f)\
  2021-05-29 06:19:46 +0200
  * [MDEV-25815](https://jira.mariadb.org/browse/MDEV-25815) mariadb-backup crash or debug assert with --backup --databases-exclude
* [Revision #a70a5537e7](https://github.com/MariaDB/server/commit/a70a5537e7)\
  2021-05-23 21:23:18 -0700
  * Deb: Innotop: Add support for [MariaDB 10.5](../../old-releases/mariadb-10-5-series/what-is-mariadb-105.md)+
* [Revision #08bc7ee068](https://github.com/MariaDB/server/commit/08bc7ee068)\
  2021-05-27 00:37:51 +0200
  * [MDEV-25792](https://jira.mariadb.org/browse/MDEV-25792) server hangs on early shutdown if InnoDB needs to purge indexed virtual columns
* [Revision #4777097fee](https://github.com/MariaDB/server/commit/4777097fee)\
  2021-05-23 18:38:46 +0200
  * followup: rename generated files to have distinct names
* [Revision #dfbeddaa11](https://github.com/MariaDB/server/commit/dfbeddaa11)\
  2021-05-22 17:47:42 +0200
  * [MDEV-25726](https://jira.mariadb.org/browse/MDEV-25726) get rid of cmake comment hack in sql\_yacc.yy
* [Revision #288b801696](https://github.com/MariaDB/server/commit/288b801696)\
  2021-05-26 11:54:29 +0300
  * Fix [MDEV-25562](https://jira.mariadb.org/browse/MDEV-25562) test case.
* [Revision #5727d56260](https://github.com/MariaDB/server/commit/5727d56260)\
  2021-05-20 14:15:43 +1000
  * Change connection\_count back to static
* [Revision #b118f92be6](https://github.com/MariaDB/server/commit/b118f92be6)\
  2021-02-09 00:59:55 +0400
  * [MDEV-15888](https://jira.mariadb.org/browse/MDEV-15888) Implement FLUSH TABLES tbl\_name \[, tbl\_name] ... WITH READ LOCK for views.
* [Revision #be8e51c459](https://github.com/MariaDB/server/commit/be8e51c459)\
  2021-05-31 08:29:37 +0200
  * [MDEV-25511](https://jira.mariadb.org/browse/MDEV-25511): Command line tools don't support CRL parameters
* [Revision #904edfd24b](https://github.com/MariaDB/server/commit/904edfd24b)\
  2021-05-26 14:15:26 +0200
  * [MDEV-25777](https://jira.mariadb.org/browse/MDEV-25777): JAVA\_INCLUDE\_PATH and JAVA\_INCLUDE\_PATH2 not found with out of source configuration and Ninja generator
* [Revision #2274c4f5fc](https://github.com/MariaDB/server/commit/2274c4f5fc)\
  2021-03-11 18:17:06 +0200
  * Add Pull Request template file to the MariaDB/server repository
* [Revision #f078788e29](https://github.com/MariaDB/server/commit/f078788e29)\
  2021-05-27 13:25:27 +0300
  * [MDEV-25312](https://jira.mariadb.org/browse/MDEV-25312) fixup: Fix .isl file parsing
* [Revision #a7d68e7a0f](https://github.com/MariaDB/server/commit/a7d68e7a0f)\
  2021-05-27 10:13:14 +0300
  * [MDEV-25791](https://jira.mariadb.org/browse/MDEV-25791): Remove UNIV\_INTERN
* [Revision #9ec2129f71](https://github.com/MariaDB/server/commit/9ec2129f71)\
  2021-05-26 22:07:20 +0300
  * Fixed bug in mtr that caused restart to fail if mysqld died to fast
* [Revision #552bb1af7b](https://github.com/MariaDB/server/commit/552bb1af7b)\
  2021-05-25 17:35:34 +0300
  * Removed test for [MDEV-23842](https://jira.mariadb.org/browse/MDEV-23842) as the results are not stable
* [Revision #e8a54a376a](https://github.com/MariaDB/server/commit/e8a54a376a)\
  2021-05-25 15:58:46 +0300
  * Replace item->marker=

## with Item->marker= DEFINE

* Merge [Revision #860e754349](https://github.com/MariaDB/server/commit/860e754349) 2021-05-26 11:22:40 +0300 - Merge 10.5 into 10.6
* Merge [Revision #365cd08345](https://github.com/MariaDB/server/commit/365cd08345) 2021-05-26 09:47:28 +0300 - Merge 10.4 into 10.5
* Merge [Revision #1dea7f7977](https://github.com/MariaDB/server/commit/1dea7f7977) 2021-05-25 15:38:57 +0300 - Merge 10.3 into 10.4
* Merge [Revision #1864a8ea93](https://github.com/MariaDB/server/commit/1864a8ea93) 2021-05-24 09:38:49 +0300 - Merge 10.2 into 10.3
* [Revision #5c75ba9cad](https://github.com/MariaDB/server/commit/5c75ba9cad)\
  2021-05-24 11:33:01 +0530
  * [MDEV-25663](https://jira.mariadb.org/browse/MDEV-25663) Double free of transaction during truncate operation
* [Revision #349d77ecdd](https://github.com/MariaDB/server/commit/349d77ecdd)\
  2021-05-20 15:47:21 +0530
  * [MDEV-25721](https://jira.mariadb.org/browse/MDEV-25721) Double free of table when inplace alter FTS add index fails
* [Revision #98f7b2cb09](https://github.com/MariaDB/server/commit/98f7b2cb09)\
  2021-05-14 14:13:59 +0530
  * [MDEV-25663](https://jira.mariadb.org/browse/MDEV-25663) Double free of transaction during truncate operation
* [Revision #c88e9342f3](https://github.com/MariaDB/server/commit/c88e9342f3)\
  2021-05-23 01:11:19 +0200
  * [MDEV-25759](https://jira.mariadb.org/browse/MDEV-25759): is\_local\_ip function can come to incorrect conclusion
* [Revision #f70b11c8c9](https://github.com/MariaDB/server/commit/f70b11c8c9)\
  2021-05-21 10:52:12 +0200
  * cmake: fewer Build-Depends in SRPM
* [Revision #d7321893d8](https://github.com/MariaDB/server/commit/d7321893d8)\
  2021-05-14 21:25:46 +0200
  * CONNECT: move jar files to /usr/share and include them in DEBs
* [Revision #9d0fde3ba1](https://github.com/MariaDB/server/commit/9d0fde3ba1)\
  2021-05-22 12:21:05 +0200
  * cmake: silence repeated git searches too
* [Revision #f9f8cae9fe](https://github.com/MariaDB/server/commit/f9f8cae9fe)\
  2021-05-14 19:55:53 +0200
  * cmake: fix FindJava/FindJNI wrappers for cmake re-runs
* [Revision #6bf866cc79](https://github.com/MariaDB/server/commit/6bf866cc79)\
  2021-05-14 14:45:53 +0200
  * [MDEV-25641](https://jira.mariadb.org/browse/MDEV-25641) max\_password\_errors not working with ed25519 auth plugin
* [Revision #681918a849](https://github.com/MariaDB/server/commit/681918a849)\
  2021-05-13 18:35:02 +0200
  * [MDEV-24996](https://jira.mariadb.org/browse/MDEV-24996) file conflict in rpm packages
* [Revision #43c9fcefc0](https://github.com/MariaDB/server/commit/43c9fcefc0)\
  2021-05-12 19:32:29 -0700
  * [MDEV-23886](https://jira.mariadb.org/browse/MDEV-23886) Reusing CTE inside a function fails with table doesn't exist
* [Revision #9739cf1859](https://github.com/MariaDB/server/commit/9739cf1859)\
  2021-05-21 18:50:30 +0300
  * [MDEV-25664](https://jira.mariadb.org/browse/MDEV-25664) Potential hang in purge for virtual columns
* [Revision #2087d47aae](https://github.com/MariaDB/server/commit/2087d47aae)\
  2021-05-21 17:46:48 +0300
  * [MDEV-22462](https://jira.mariadb.org/browse/MDEV-22462): Item\_in\_subselect::create\_single\_in\_to\_exists\_cond(JOIN \*, Item , Item ): Assertion \`false' failed.
* [Revision #8c8a6ed3b8](https://github.com/MariaDB/server/commit/8c8a6ed3b8)\
  2021-05-21 03:11:48 +0200
  * [MDEV-25719](https://jira.mariadb.org/browse/MDEV-25719): stunnel uses "verifyChain" without subject checks
* [Revision #629449172a](https://github.com/MariaDB/server/commit/629449172a)\
  2021-04-30 23:14:57 +0530
  * [MDEV-25462](https://jira.mariadb.org/browse/MDEV-25462): Assertion \`m\_status == DA\_ERROR || m\_status == DA\_OK || m\_status == DA\_OK\_BULK' failed in Diagnostics\_area::message from get\_schema\_tables\_record
* [Revision #406ce57232](https://github.com/MariaDB/server/commit/406ce57232)\
  2021-05-19 18:09:49 +1000
  * [MDEV-25728](https://jira.mariadb.org/browse/MDEV-25728): mysqld --help --verbose creates a log-bin-index file
* [Revision #e570f740cd](https://github.com/MariaDB/server/commit/e570f740cd)\
  2021-05-14 20:43:21 +0300
  * [MDEV-25629](https://jira.mariadb.org/browse/MDEV-25629): Crash in get\_sort\_by\_table() in subquery with order by having outer ref
* [Revision #af8d4a97e2](https://github.com/MariaDB/server/commit/af8d4a97e2)\
  2021-05-18 15:45:43 +0530
  * [MDEV-22530](https://jira.mariadb.org/browse/MDEV-22530): Aborting OPTIMIZE TABLE still logs in binary log and replicates to the Slave server.
* [Revision #acede480c5](https://github.com/MariaDB/server/commit/acede480c5)\
  2021-05-13 15:31:58 +0300
  * Updated galera\_3nodes disabled.def file
* [Revision #b01a9fd817](https://github.com/MariaDB/server/commit/b01a9fd817)\
  2021-05-21 03:13:37 +0200
  * [MDEV-25719](https://jira.mariadb.org/browse/MDEV-25719): stunnel uses "verifyChain" without subject checks
* [Revision #04de651725](https://github.com/MariaDB/server/commit/04de651725)\
  2021-05-25 00:43:03 -0700
  * [MDEV-23886](https://jira.mariadb.org/browse/MDEV-23886) Reusing CTE inside a function fails with table doesn't exist
* [Revision #67083ca4f3](https://github.com/MariaDB/server/commit/67083ca4f3)\
  2021-05-22 01:17:46 +0200
  * [MDEV-25719](https://jira.mariadb.org/browse/MDEV-25719) post-merge correction: wsrep\_debug=ON -> wsrep\_debug=1
* [Revision #8e280f3007](https://github.com/MariaDB/server/commit/8e280f3007)\
  2021-05-21 03:38:04 +0200
  * [MDEV-25719](https://jira.mariadb.org/browse/MDEV-25719): stunnel uses "verifyChain" without subject checks
* [Revision #5667baad5d](https://github.com/MariaDB/server/commit/5667baad5d)\
  2021-05-20 09:56:53 +0200
  * [MDEV-25562](https://jira.mariadb.org/browse/MDEV-25562) Assertion \`pause\_seqno\_.is\_undefined() == false' failed in void wsrep::server\_state::resume()
* [Revision #675716e1cb](https://github.com/MariaDB/server/commit/675716e1cb)\
  2021-05-25 17:13:17 -0700
  * [MDEV-23886](https://jira.mariadb.org/browse/MDEV-23886) Reusing CTE inside a function fails with table doesn't exist
* [Revision #4926498a67](https://github.com/MariaDB/server/commit/4926498a67)\
  2021-05-07 01:33:27 -0400
  * CRC32 on OpenBSD/powerpc64.
* [Revision #6d549aecf5](https://github.com/MariaDB/server/commit/6d549aecf5)\
  2021-05-25 13:34:52 +0200
  * threadpool\_generic: support future NetBSD kqueue versions
* [Revision #2eb357496c](https://github.com/MariaDB/server/commit/2eb357496c)\
  2021-05-24 15:35:06 +0200
  * my\_largepage: Fix build with MAP\_ALIGNED by no MAP\_ALIGNED\_SUPER
* [Revision #c80cecb5e3](https://github.com/MariaDB/server/commit/c80cecb5e3)\
  2021-05-23 19:53:38 +0300
  * Updated BUILD scripts to update modules wsrep-lib and columnstore
* [Revision #30c9089095](https://github.com/MariaDB/server/commit/30c9089095)\
  2021-05-23 19:31:06 +0300
  * Fixed compiler warnings from CONNECT
* [Revision #5a20b30fb3](https://github.com/MariaDB/server/commit/5a20b30fb3)\
  2021-05-23 19:41:17 +0300
  * [MDEV-25738](https://jira.mariadb.org/browse/MDEV-25738) Assertion \`ticket->m\_duration == MDL\_EXPLICIT' failed
* [Revision #15214a4f11](https://github.com/MariaDB/server/commit/15214a4f11)\
  2021-05-23 19:30:05 +0300
  * [MDEV-25708](https://jira.mariadb.org/browse/MDEV-25708) THD::cleanup(): Assertion \`!mdl\_context.has\_locks()' failed
* [Revision #2c90dc091c](https://github.com/MariaDB/server/commit/2c90dc091c)\
  2021-05-22 02:16:38 +0200
  * [MDEV-25719](https://jira.mariadb.org/browse/MDEV-25719) post-merge correction: wsrep\_debug=ON -> wsrep\_debug=1
* [Revision #b2556b256b](https://github.com/MariaDB/server/commit/b2556b256b)\
  2021-05-21 03:39:58 +0200
  * [MDEV-25719](https://jira.mariadb.org/browse/MDEV-25719): stunnel uses "verifyChain" without subject checks
* [Revision #9bbedcdd59](https://github.com/MariaDB/server/commit/9bbedcdd59)\
  2021-05-19 16:10:13 +0200
  * don't require jemalloc for 10.5 official packages
* [Revision #9ecf9a644c](https://github.com/MariaDB/server/commit/9ecf9a644c)\
  2021-05-13 17:54:15 +0200
  * [MDEV-25617](https://jira.mariadb.org/browse/MDEV-25617) 10.5.10 upgrade: "scriptlet / line 6 : \[: is-active : binary operator expected"
* [Revision #71e1ddda22](https://github.com/MariaDB/server/commit/71e1ddda22)\
  2021-05-25 21:20:08 +0300
  * Race condition occurs upon server restart inside test cases
* [Revision #cf9e4c8b16](https://github.com/MariaDB/server/commit/cf9e4c8b16)\
  2021-05-21 13:06:38 +0300
  * Fixed result set change in spider/bugfix/r/slave\_trx\_isolation.result
* [Revision #e5b6db0179](https://github.com/MariaDB/server/commit/e5b6db0179)\
  2021-05-21 13:06:00 +0300
  * Speed up atomic test suite by improving wait\_until\_connected\_again.inc and remove usage of RESET MASTER in loops.
* [Revision #3b8d4180d5](https://github.com/MariaDB/server/commit/3b8d4180d5)\
  2021-05-20 15:46:06 +0300
  * Flush gcov files for DBUG\_ASSERT and DBUG\_SUICIDE
* [Revision #e0a6cfb38b](https://github.com/MariaDB/server/commit/e0a6cfb38b)\
  2021-05-14 15:42:05 +0300
  * [MDEV-25078](https://jira.mariadb.org/browse/MDEV-25078): ALTER INDEX is inconsistent with ADD/DROP/RENAME index
* [Revision #4e19539c14](https://github.com/MariaDB/server/commit/4e19539c14)\
  2021-03-18 13:17:30 +0530
  * [MDEV-22189](https://jira.mariadb.org/browse/MDEV-22189): Change error messages inside code to have mariadb instead of mysql
* [Revision #16502e8cf3](https://github.com/MariaDB/server/commit/16502e8cf3)\
  2021-05-22 02:17:16 +0200
  * [MDEV-25719](https://jira.mariadb.org/browse/MDEV-25719) post-merge correction: wsrep\_debug=ON -> wsrep\_debug=1
* [Revision #66165ae221](https://github.com/MariaDB/server/commit/66165ae221)\
  2021-05-21 16:34:26 -0400
  * bump the VERSION
* [Revision #49e2c8f0a6](https://github.com/MariaDB/server/commit/49e2c8f0a6)\
  2021-05-20 14:58:25 +0300
  * [MDEV-25743](https://jira.mariadb.org/browse/MDEV-25743): Unnecessary copying of table names in InnoDB dictionary
* [Revision #525bf04910](https://github.com/MariaDB/server/commit/525bf04910)\
  2021-05-20 10:18:33 +0300
  * Cleanup: Remove the compile-innodb script
* [Revision #7bdb8d125e](https://github.com/MariaDB/server/commit/7bdb8d125e)\
  2021-05-20 09:43:25 +0300
  * Cleanup: Remove the error code DB\_MUST\_GET\_MORE\_FILE\_SPACE
* [Revision #9eb4ad57de](https://github.com/MariaDB/server/commit/9eb4ad57de)\
  2021-05-20 09:26:23 +0300
  * Cleanup: Access lower\_case\_table\_names, tdc\_size directly
* [Revision #383f77cd84](https://github.com/MariaDB/server/commit/383f77cd84)\
  2021-05-19 18:51:19 +0300
  * Cleanup: Simplify dict\_table\_schema\_check()
* [Revision #7ff9e5831e](https://github.com/MariaDB/server/commit/7ff9e5831e)\
  2021-05-21 09:35:00 +0300
  * [MDEV-25748](https://jira.mariadb.org/browse/MDEV-25748) DROP DATABASE drops unrelated FOREIGN KEY constraints
* [Revision #3246e729ff](https://github.com/MariaDB/server/commit/3246e729ff)\
  2021-05-21 03:39:58 +0200
  * [MDEV-25719](https://jira.mariadb.org/browse/MDEV-25719): stunnel uses "verifyChain" without subject checks

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
