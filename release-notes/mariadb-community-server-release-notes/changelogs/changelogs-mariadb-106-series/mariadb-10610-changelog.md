# MariaDB 10.6.10 Changelog

The most recent release of [MariaDB 10.6](../../mariadb-10-6-series/what-is-mariadb-106.md) is:[**MariaDB 10.6.21**](../../mariadb-10-6-series/mariadb-10-6-21-release-notes.md) Stable (GA) [Download Now](https://mariadb.com/downloads/)[_Alternate download from mariadb.org_](https://downloads.mariadb.org/mariadb/10.6.21/)

[Download 10.6.10](https://downloads.mariadb.org/mariadb/10.6.10/)[Release Notes](../../mariadb-10-6-series/mariadb-10610-release-notes.md)[Changelog](mariadb-10610-changelog.md)[Overview of 10.6](../../mariadb-10-6-series/what-is-mariadb-106.md)

**Release date:** 19 Sep 2022

For the highlights of this release, see the[release notes](../../mariadb-10-6-series/mariadb-10610-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/server/tree/10.6) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Includes all fixes from [MariaDB 10.5.17](../changelogs-mariadb-105-series/mariadb-10517-changelog.md)
* Merge [Revision #fd0bdd3180](https://github.com/MariaDB/server/commit/fd0bdd3180) 2022-09-13 08:40:05 +0300 - Merge 10.5 into 10.6
* [Revision #fb70bb44d0](https://github.com/MariaDB/server/commit/fb70bb44d0)\
  2022-09-12 12:10:10 +0200
  * [MDEV-29513](https://jira.mariadb.org/browse/MDEV-29513) avoid useless os\_thread\_sleep() during srv\_purge\_shutdown()
* Merge [Revision #0ccb95c2a9](https://github.com/MariaDB/server/commit/0ccb95c2a9) 2022-09-12 15:01:55 +0300 - Merge 10.5 into 10.6
* [Revision #bc12478a9a](https://github.com/MariaDB/server/commit/bc12478a9a)\
  2022-08-16 20:03:15 +0300
  * [MDEV-24660](https://jira.mariadb.org/browse/MDEV-24660) MYSQL\_BIN\_LOG::cleanup(): Assertion \`b->xid\_count == 0'
* [Revision #5563202089](https://github.com/MariaDB/server/commit/5563202089)\
  2022-08-30 00:26:20 +0300
  * [MDEV-29322](https://jira.mariadb.org/browse/MDEV-29322) ASAN heap-use-after-free in Query\_log\_event::do\_apply\_event
* [Revision #70021737f5](https://github.com/MariaDB/server/commit/70021737f5)\
  2022-09-08 21:02:41 +0900
  * [MDEV-27172](https://jira.mariadb.org/browse/MDEV-27172) fixup: spider/bugfix.mdev\_27172 failed with --ps-protocol
* [Revision #d2e649aec2](https://github.com/MariaDB/server/commit/d2e649aec2)\
  2022-09-08 14:57:50 +0300
  * [MDEV-29440](https://jira.mariadb.org/browse/MDEV-29440) InnoDB instant ALTER TABLE recovery must use READ UNCOMMITTED
* [Revision #0fa4dd0747](https://github.com/MariaDB/server/commit/0fa4dd0747)\
  2022-09-07 21:41:29 +0300
  * [MDEV-29433](https://jira.mariadb.org/browse/MDEV-29433) innodb.lock\_delete\_updated is unstable
* [Revision #bd7ff02a6a](https://github.com/MariaDB/server/commit/bd7ff02a6a)\
  2022-09-07 16:41:21 +0200
  * Fix CMake 3.24 warning by setting a policy
* Merge [Revision #7d63f21693](https://github.com/MariaDB/server/commit/7d63f21693) 2022-09-07 16:39:30 +0200 - Merge branch '10.5' into 10.6
* Merge [Revision #80cf7a4c43](https://github.com/MariaDB/server/commit/80cf7a4c43) 2022-09-07 15:28:58 +0200 - Merge branch '10.4' into 10.5
* [Revision #9a8faeea14](https://github.com/MariaDB/server/commit/9a8faeea14)\
  2022-09-07 13:49:49 +0200
  * [MDEV-18353](https://jira.mariadb.org/browse/MDEV-18353) - minor cleanup
* [Revision #dd092bc6eb](https://github.com/MariaDB/server/commit/dd092bc6eb)\
  2022-09-07 19:58:55 +1000
  * Deb: add kinetic to autobake (#2250)
* [Revision #bacaf2d4f4](https://github.com/MariaDB/server/commit/bacaf2d4f4)\
  2022-09-07 12:57:53 +0300
  * [MDEV-29342](https://jira.mariadb.org/browse/MDEV-29342) Assertion failure in file que0que.cc line 728
* [Revision #1872a142b5](https://github.com/MariaDB/server/commit/1872a142b5)\
  2022-09-07 11:58:04 +0300
  * [MDEV-10003](https://jira.mariadb.org/browse/MDEV-10003) main.range\_innodb retuns a wrong number of rows in EXPLAIN
* Merge [Revision #1985204044](https://github.com/MariaDB/server/commit/1985204044) 2022-09-07 08:47:20 +0300 - Merge 10.5 into 10.6
* Merge [Revision #38d36b59f9](https://github.com/MariaDB/server/commit/38d36b59f9) 2022-09-07 08:26:21 +0300 - Merge 10.4 into 10.5
* Merge [Revision #c7ba237793](https://github.com/MariaDB/server/commit/c7ba237793) 2022-09-07 08:08:59 +0300 - Merge 10.3 into 10.4
* [Revision #ac49b7a845](https://github.com/MariaDB/server/commit/ac49b7a845)\
  2022-08-29 22:54:25 +0530
  * [MDEV-29342](https://jira.mariadb.org/browse/MDEV-29342) Assertion failure in file que0que.cc line 728
* [Revision #f501f815bc](https://github.com/MariaDB/server/commit/f501f815bc)\
  2022-08-26 18:35:15 +0300
  * [MDEV-28827](https://jira.mariadb.org/browse/MDEV-28827) Minor unsafe statement warning message improvement
* [Revision #47812017c6](https://github.com/MariaDB/server/commit/47812017c6)\
  2022-05-10 14:25:35 -0600
  * [MDEV-28530](https://jira.mariadb.org/browse/MDEV-28530): Revoking privileges from a non-existing user on a master breaks replication on the slave in the presence of replication filters
* [Revision #e4cffc92c7](https://github.com/MariaDB/server/commit/e4cffc92c7)\
  2022-06-30 01:58:57 +0900
  * [MDEV-27172](https://jira.mariadb.org/browse/MDEV-27172) Prefix indices on Spider tables may lead to wrong query results
* [Revision #4f2dc716ee](https://github.com/MariaDB/server/commit/4f2dc716ee)\
  2022-08-31 15:58:52 +0300
  * [MDEV-13668](https://jira.mariadb.org/browse/MDEV-13668) fixup: Remove test work-arounds
* [Revision #c487eeed10](https://github.com/MariaDB/server/commit/c487eeed10)\
  2022-08-31 15:24:06 +1000
  * [MDEV-28592](https://jira.mariadb.org/browse/MDEV-28592) disks plugin (postfix - remove tabs)
* [Revision #38dda1f026](https://github.com/MariaDB/server/commit/38dda1f026)\
  2022-09-06 15:11:24 +0300
  * [MDEV-29475](https://jira.mariadb.org/browse/MDEV-29475) trx\_undo\_rseg\_free() does not write redo log
* Merge [Revision #4318391346](https://github.com/MariaDB/server/commit/4318391346) 2022-09-06 12:28:39 +0300 - Merge 10.5 into 10.6
* [Revision #c0470caf5a](https://github.com/MariaDB/server/commit/c0470caf5a)\
  2022-09-06 11:33:52 +0300
  * [MDEV-29471](https://jira.mariadb.org/browse/MDEV-29471) Buffer overflow in page\_cur\_insert\_rec\_low()
* [Revision #027a9963b0](https://github.com/MariaDB/server/commit/027a9963b0)\
  2022-09-06 09:52:08 +0300
  * [MDEV-13542](https://jira.mariadb.org/browse/MDEV-13542) fixup: Allow purge to run in a test
* [Revision #19de8b7013](https://github.com/MariaDB/server/commit/19de8b7013)\
  2022-09-02 22:53:08 +0530
  * [MDEV-28240](https://jira.mariadb.org/browse/MDEV-28240) InnoDB Temporary Tablespace (ibtmp1) is continously growing
* [Revision #fd8dbe0d2c](https://github.com/MariaDB/server/commit/fd8dbe0d2c)\
  2022-09-02 10:43:39 +1000
  * [MDEV-29443](https://jira.mariadb.org/browse/MDEV-29443): prevent uring access to galera sst /notify scripts
* Merge [Revision #9fefd440b5](https://github.com/MariaDB/server/commit/9fefd440b5) 2022-09-05 14:05:30 +0300 - Merge 10.5 into 10.6
* Merge [Revision #ba987a46c9](https://github.com/MariaDB/server/commit/ba987a46c9) 2022-09-05 13:28:56 +0300 - Merge 10.4 into 10.5
* [Revision #2917bd0d2c](https://github.com/MariaDB/server/commit/2917bd0d2c)\
  2022-02-15 14:36:02 +0100
  * Reduce compilation dependencies on wsrep\_mysqld.h
* Merge [Revision #3c7887a85f](https://github.com/MariaDB/server/commit/3c7887a85f) 2022-09-05 10:09:03 +0300 - Merge 10.5 into 10.6
* [Revision #244fdc435d](https://github.com/MariaDB/server/commit/244fdc435d)\
  2022-09-05 09:54:47 +0300
  * [MDEV-29438](https://jira.mariadb.org/browse/MDEV-29438) Recovery or backup of instant ALTER TABLE is incorrect
* [Revision #5cbc5dbbbe](https://github.com/MariaDB/server/commit/5cbc5dbbbe)\
  2022-08-31 13:00:16 +1000
  * [MDEV-29418](https://jira.mariadb.org/browse/MDEV-29418) linux uuid implementation returning non-hwaddr based suffix
* Merge [Revision #43037a5a48](https://github.com/MariaDB/server/commit/43037a5a48) 2022-08-31 11:06:14 +1000 - Merge branch 10.4 into 10.5
* Merge [Revision #cf1a944f5b](https://github.com/MariaDB/server/commit/cf1a944f5b) 2022-08-31 10:52:53 +1000 - Merge 10.3 into 10.4
* [Revision #129616c70a](https://github.com/MariaDB/server/commit/129616c70a)\
  2022-07-31 13:41:59 +1000
  * [MDEV-28592](https://jira.mariadb.org/browse/MDEV-28592) disks plugin - getmntinfo (BSD) & getmntent (AIX)
* [Revision #84813c396a](https://github.com/MariaDB/server/commit/84813c396a)\
  2022-09-02 05:40:33 -0400
  * Remove unused French translations in Connect engine (#2252)
* [Revision #e27c3d5230](https://github.com/MariaDB/server/commit/e27c3d5230)\
  2022-09-01 13:51:15 +0530
  * [MDEV-29425](https://jira.mariadb.org/browse/MDEV-29425) Buffer overflow in dict\_index\_t::col\_info::add()
* [Revision #40aa94df35](https://github.com/MariaDB/server/commit/40aa94df35)\
  2022-09-01 10:40:27 +0300
  * [MDEV-29435](https://jira.mariadb.org/browse/MDEV-29435) CHECK TABLE forgets to release latches after reporting failure
* [Revision #9203249987](https://github.com/MariaDB/server/commit/9203249987)\
  2022-08-31 17:52:23 +0300
  * [MDEV-27983](https://jira.mariadb.org/browse/MDEV-27983): InnoDB hangs after loading a ROW\_FORMAT=COMPRESSED page
* [Revision #bdf62ece6c](https://github.com/MariaDB/server/commit/bdf62ece6c)\
  2022-08-31 17:52:16 +0300
  * [MDEV-29374](https://jira.mariadb.org/browse/MDEV-29374) InnoDB recovery fails with "Data structure corruption"
* Merge [Revision #f410974f0f](https://github.com/MariaDB/server/commit/f410974f0f) 2022-08-30 13:01:16 +0300 - Merge 10.5 into 10.6
* Merge [Revision #29fa9bcee0](https://github.com/MariaDB/server/commit/29fa9bcee0) 2022-08-30 12:29:04 +0300 - Merge 10.4 into 10.5
* Merge [Revision #7e574eb52c](https://github.com/MariaDB/server/commit/7e574eb52c) 2022-08-30 12:17:33 +0300 - Merge 10.3 into 10.4
* [Revision #57739ae94a](https://github.com/MariaDB/server/commit/57739ae94a)\
  2022-08-30 12:03:58 +0300
  * [MDEV-13888](https://jira.mariadb.org/browse/MDEV-13888): innodb\_fts.innodb\_fts\_plugin failed
* [Revision #422f3204ef](https://github.com/MariaDB/server/commit/422f3204ef)\
  2022-08-30 12:02:56 +0300
  * [MDEV-29409](https://jira.mariadb.org/browse/MDEV-29409) Buffer overflow in my\_wc\_mb\_filename() on RENAME TABLE
* [Revision #b260903832](https://github.com/MariaDB/server/commit/b260903832)\
  2022-08-30 10:59:31 +0300
  * [MDEV-29258](https://jira.mariadb.org/browse/MDEV-29258) Failing assertion for name length on RENAME TABLE
* [Revision #0d1de5e1d1](https://github.com/MariaDB/server/commit/0d1de5e1d1)\
  2022-08-28 21:23:28 +0300
  * [MDEV-29403](https://jira.mariadb.org/browse/MDEV-29403) innodb.innodb\_sys\_semaphore\_waits fails with wrong errno 5014
* [Revision #94e3f02db7](https://github.com/MariaDB/server/commit/94e3f02db7)\
  2022-08-24 11:07:09 -0700
  * [MDEV-29350](https://jira.mariadb.org/browse/MDEV-29350) Crash when IN predicand is used in eliminated GROUP BY clause
* [Revision #827b049e1e](https://github.com/MariaDB/server/commit/827b049e1e)\
  2022-06-05 08:04:18 +0000
  * [MDEV-18873](https://jira.mariadb.org/browse/MDEV-18873) Server crashes in Compare\_identifiers::operator or in my\_strcasecmp\_utf8 upon ADD PERIOD IF NOT EXISTS with empty name
* [Revision #0324bde846](https://github.com/MariaDB/server/commit/0324bde846)\
  2022-08-26 10:20:26 +1000
  * mariadb-backup: remove MySQL wording
* [Revision #79b58f1ca8](https://github.com/MariaDB/server/commit/79b58f1ca8)\
  2022-07-30 00:11:08 +1000
  * [MDEV-23607](https://jira.mariadb.org/browse/MDEV-23607) mariadb-backup - align required GRANTS to cmd options
* [Revision #966d22b715](https://github.com/MariaDB/server/commit/966d22b715)\
  2022-08-30 04:21:40 -0400
  * Ensure that source files contain only valid UTF8 encodings (#2188)
* [Revision #0fbcb0a2b8](https://github.com/MariaDB/server/commit/0fbcb0a2b8)\
  2022-08-26 11:41:43 +0300
  * [MDEV-29383](https://jira.mariadb.org/browse/MDEV-29383) Assertion mysql\_mutex\_assert\_owner(\&log\_sys.flush\_order\_mutex) failed in mtr\_t::commit()
* Merge [Revision #76bb671e42](https://github.com/MariaDB/server/commit/76bb671e42) 2022-08-25 16:02:44 +0300 - Merge 10.5 into 10.6
* Merge [Revision #9929301ecd](https://github.com/MariaDB/server/commit/9929301ecd) 2022-08-25 15:31:19 +0300 - Merge 10.4 into 10.5
* Merge [Revision #851058a3e6](https://github.com/MariaDB/server/commit/851058a3e6) 2022-08-25 15:17:20 +0300 - Merge 10.3 into 10.4
* [Revision #d1a80c42ee](https://github.com/MariaDB/server/commit/d1a80c42ee)\
  2022-08-25 15:14:38 +0300
  * [MDEV-29384](https://jira.mariadb.org/browse/MDEV-29384) Hangs caused by innodb\_adaptive\_hash\_index=ON
* [Revision #2f6a728075](https://github.com/MariaDB/server/commit/2f6a728075)\
  2022-08-10 13:27:01 +0200
  * update a global\_suppressions() list
* [Revision #f2a53b6158](https://github.com/MariaDB/server/commit/f2a53b6158)\
  2022-08-24 15:00:47 +0300
  * btr\_search\_drop\_page\_hash\_index(): Remove a racey debug check
* [Revision #61f456e772](https://github.com/MariaDB/server/commit/61f456e772)\
  2022-08-24 12:27:15 +0530
  * [MDEV-29319](https://jira.mariadb.org/browse/MDEV-29319) Assertion failure size\_in\_header >= space.free\_limit in fsp\_get\_available\_space\_in\_free\_extents()
* [Revision #dd737d071e](https://github.com/MariaDB/server/commit/dd737d071e)\
  2022-08-17 18:09:06 +0530
  * [MDEV-29291](https://jira.mariadb.org/browse/MDEV-29291) Assertion \`!table->fts' failed in dict\_table\_can\_be\_evicted on SHUTDOWN
* [Revision #0b80573310](https://github.com/MariaDB/server/commit/0b80573310)\
  2022-08-22 18:36:30 +0530
  * [MDEV-29319](https://jira.mariadb.org/browse/MDEV-29319) Assertion failure size\_in\_header >= space.free\_limit in fsp\_get\_available\_space\_in\_free\_extents()
* [Revision #8963d64ee8](https://github.com/MariaDB/server/commit/8963d64ee8)\
  2022-04-26 19:51:42 -0600
  * [MDEV-28294](https://jira.mariadb.org/browse/MDEV-28294): set default role bypasses Replicate\_Wild\_Ignore\_Table: mysql.%
* [Revision #a3fd9e6b06](https://github.com/MariaDB/server/commit/a3fd9e6b06)\
  2022-08-24 10:09:27 +0200
  * [MDEV-29367](https://jira.mariadb.org/browse/MDEV-29367) Refactor tpool::cache
* [Revision #8ff1096999](https://github.com/MariaDB/server/commit/8ff1096999)\
  2022-08-24 17:06:57 +0300
  * [MDEV-29081](https://jira.mariadb.org/browse/MDEV-29081) trx\_t::lock.was\_chosen\_as\_deadlock\_victim race in lock\_wait\_end()
* [Revision #5b4c832c7e](https://github.com/MariaDB/server/commit/5b4c832c7e)\
  2022-08-23 19:38:24 +0530
  * [MDEV-29314](https://jira.mariadb.org/browse/MDEV-29314) Assertion \`n\_fields > n\_cols' failed in dict\_index\_t::init\_change\_cols
* Merge [Revision #03726a36b8](https://github.com/MariaDB/server/commit/03726a36b8) 2022-08-23 21:58:45 +0900 - Merge 10.5 into 10.6
* Merge [Revision #720fa05e5b](https://github.com/MariaDB/server/commit/720fa05e5b) 2022-08-23 20:59:34 +0900 - Merge 10.4 into 10.5
* [Revision #e404315258](https://github.com/MariaDB/server/commit/e404315258)\
  2022-08-23 19:53:59 +0900
  * Fix wrong diff introduced by merge commit
* [Revision #0e8544cd73](https://github.com/MariaDB/server/commit/0e8544cd73)\
  2022-08-23 13:17:35 +0400
  * [MDEV-29355](https://jira.mariadb.org/browse/MDEV-29355) Backport templatized INET6 implementation from 10.7 to 10.6
* [Revision #4feb9df105](https://github.com/MariaDB/server/commit/4feb9df105)\
  2022-08-18 16:21:31 +0530
  * [MDEV-29282](https://jira.mariadb.org/browse/MDEV-29282) atomic.rename\_trigger fails occasionally
* [Revision #01f9c81237](https://github.com/MariaDB/server/commit/01f9c81237)\
  2022-08-23 08:47:49 +0300
  * [MDEV-29336](https://jira.mariadb.org/browse/MDEV-29336): Potential deadlock in btr\_page\_alloc\_low() with the AHI
* Merge [Revision #fbb2b1f55f](https://github.com/MariaDB/server/commit/fbb2b1f55f) 2022-08-23 08:47:21 +0300 - Merge 10.5 into 10.6
* [Revision #55c648a738](https://github.com/MariaDB/server/commit/55c648a738)\
  2022-08-23 08:58:23 +0400
  * [MDEV-27099](https://jira.mariadb.org/browse/MDEV-27099) Subquery using the ALL keyword on INET6 columns produces a wrong result
* Merge [Revision #3b656ac8c1](https://github.com/MariaDB/server/commit/3b656ac8c1) 2022-08-22 19:49:56 +0300 - Merge 10.4 into 10.5
* Merge [Revision #b68ae6dc1d](https://github.com/MariaDB/server/commit/b68ae6dc1d) 2022-08-22 16:22:09 +0300 - Merge 10.3 into 10.4
* [Revision #c7f8cfc9e7](https://github.com/MariaDB/server/commit/c7f8cfc9e7)\
  2022-08-16 15:31:49 +0530
  * [MDEV-27700](https://jira.mariadb.org/browse/MDEV-27700) ASAN: Heap\_use\_after\_free in btr\_search\_drop\_page\_hash\_index()
* [Revision #316847eab7](https://github.com/MariaDB/server/commit/316847eab7)\
  2022-08-22 11:50:15 +0400
  * [MDEV-27101](https://jira.mariadb.org/browse/MDEV-27101) Subquery using the ALL keyword on TIMESTAMP columns produces a wrong result
* Merge [Revision #d65a2b7bde](https://github.com/MariaDB/server/commit/d65a2b7bde) 2022-08-22 14:02:43 +0300 - Merge 10.5 into 10.6
* Merge [Revision #1d90d6874d](https://github.com/MariaDB/server/commit/1d90d6874d) 2022-08-22 13:38:40 +0300 - Merge 10.4 into 10.5
* Merge [Revision #36d173e523](https://github.com/MariaDB/server/commit/36d173e523) 2022-08-22 12:34:42 +0300 - Merge 10.3 into 10.4
* [Revision #fd0cd4801a](https://github.com/MariaDB/server/commit/fd0cd4801a)\
  2022-08-22 12:32:47 +0300
  * [MDEV-13013](https://jira.mariadb.org/browse/MDEV-13013) fixup: Adjust a test
* [Revision #a1055ab35d](https://github.com/MariaDB/server/commit/a1055ab35d)\
  2022-08-19 09:18:24 +0300
  * [MDEV-29043](https://jira.mariadb.org/browse/MDEV-29043) mariadb-backup --compress hangs
* [Revision #32167225c7](https://github.com/MariaDB/server/commit/32167225c7)\
  2022-08-16 17:34:38 +0530
  * [MDEV-13013](https://jira.mariadb.org/browse/MDEV-13013) InnoDB unnecessarily extends data files
* [Revision #c208006080](https://github.com/MariaDB/server/commit/c208006080)\
  2022-07-28 21:24:57 +0900
  * [MDEV-29008](https://jira.mariadb.org/browse/MDEV-29008) Server crash or assertion \`field' failed in spider\_db\_open\_item\_ident / group by handler
* Merge [Revision #8c21dc52ee](https://github.com/MariaDB/server/commit/8c21dc52ee) 2022-08-15 10:11:23 +0200 - Merge branch '10.3' into bb-10.3-release
* [Revision #d48428e99a](https://github.com/MariaDB/server/commit/d48428e99a)\
  2022-08-01 19:39:09 +0530
  * [MDEV-27151](https://jira.mariadb.org/browse/MDEV-27151): JSON\_VALUE() does not parse NULL properties properly
* [Revision #d7ba72ea9b](https://github.com/MariaDB/server/commit/d7ba72ea9b)\
  2022-08-06 22:18:11 -0400
  * Remove Darwin CMake file
* [Revision #6005f3c548](https://github.com/MariaDB/server/commit/6005f3c548)\
  2022-08-22 12:33:46 +0300
  * [MDEV-25257](https://jira.mariadb.org/browse/MDEV-25257) follow-up: Fix a test
* Merge [Revision #3101751f50](https://github.com/MariaDB/server/commit/3101751f50) 2022-08-15 10:14:16 +0200 - Merge branch '10.4' into bb-10.4-release
* Merge [Revision #5fc172fd43](https://github.com/MariaDB/server/commit/5fc172fd43) 2022-08-15 10:37:33 +0200 - Merge branch '10.5' into bb-10.5-release
* [Revision #f02ca429f7](https://github.com/MariaDB/server/commit/f02ca429f7)\
  2022-08-21 00:34:41 -0400
  * Revert aligned\_alloc() addition from [MDEV-28836](https://jira.mariadb.org/browse/MDEV-28836)
* [Revision #7624bf868e](https://github.com/MariaDB/server/commit/7624bf868e)\
  2022-08-06 01:16:21 +0530
  * [MDEV-29250](https://jira.mariadb.org/browse/MDEV-29250) InnoDB: Failing assertion: table->get\_ref\_count() == 0
* [Revision #75c416d362](https://github.com/MariaDB/server/commit/75c416d362)\
  2022-08-19 09:26:13 +0300
  * [MDEV-24626](https://jira.mariadb.org/browse/MDEV-24626) fixup: mariadb-backup.compress\_qpress
* [Revision #c2df3d30c0](https://github.com/MariaDB/server/commit/c2df3d30c0)\
  2022-08-18 17:12:00 +0300
  * [MDEV-21452](https://jira.mariadb.org/browse/MDEV-21452) fixup: Avoid an unnecessary mutex operation
* [Revision #ec37906646](https://github.com/MariaDB/server/commit/ec37906646)\
  2022-08-18 16:02:13 +0300
  * [MDEV-29321](https://jira.mariadb.org/browse/MDEV-29321) Percona XtraDB 5.7 can't be upgrade to [MariaDB 10.6](../../mariadb-10-6-series/what-is-mariadb-106.md) or above
* [Revision #af552f2903](https://github.com/MariaDB/server/commit/af552f2903)\
  2022-08-16 21:33:45 +0530
  * Disabling atomic.rename\_trigger test case because of frequent failures
* Merge [Revision #39cafb666b](https://github.com/MariaDB/server/commit/39cafb666b) 2022-08-15 11:21:39 +0200 - Merge branch '10.6' into bb-10.6-release
* Merge [Revision #dacd424965](https://github.com/MariaDB/server/commit/dacd424965) 2022-08-14 23:57:56 -0400 - Merge branch 'bb-10.6-bumpversion' of github.com:MariaDB/server into bb-10.6-bumpversion
* [Revision #e78c2b846a](https://github.com/MariaDB/server/commit/e78c2b846a)\
  2022-08-14 23:38:24 -0400
  * bump the VERSION
* [Revision #58746728db](https://github.com/MariaDB/server/commit/58746728db)\
  2022-08-14 23:38:24 -0400
  * bump the VERSION
* [Revision #820175115e](https://github.com/MariaDB/server/commit/820175115e)\
  2022-08-13 12:49:48 +0800
  * [MDEV-29264](https://jira.mariadb.org/browse/MDEV-29264): JSON function overflow error based on LONGTEXT field
* [Revision #5d3bbc6da1](https://github.com/MariaDB/server/commit/5d3bbc6da1)\
  2022-08-02 14:35:48 +1000
  * [MDEV-29222](https://jira.mariadb.org/browse/MDEV-29222) - Fix mysqld\_safe script

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
