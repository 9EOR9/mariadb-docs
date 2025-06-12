# MariaDB 10.6.11 Changelog

The most recent release of [MariaDB 10.6](../../mariadb-community-server-release-notes/mariadb-10-6-series/what-is-mariadb-106.md) is:[**MariaDB 10.6.21**](../../mariadb-community-server-release-notes/mariadb-10-6-series/mariadb-10-6-21-release-notes.md) Stable (GA) [Download Now](https://mariadb.com/downloads/)[_Alternate download from mariadb.org_](https://downloads.mariadb.org/mariadb/10.6.21/)

[Download 10.6.11](https://downloads.mariadb.org/mariadb/10.6.11/)[Release Notes](../../mariadb-community-server-release-notes/mariadb-10-6-series/mariadb-10-6-11-release-notes.md)[Changelog](mariadb-10-6-11-changelog.md)[Overview of 10.6](../../mariadb-community-server-release-notes/mariadb-10-6-series/what-is-mariadb-106.md)

**Release date:** 7 Nov 2022

For the highlights of this release, see the[release notes](../../mariadb-community-server-release-notes/mariadb-10-6-series/mariadb-10-6-11-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/server/tree/10.6) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Includes all fixes from [MariaDB 10.5.18](../changelogs-mariadb-105-series/mariadb-10-5-18-changelog.md)
* [Revision #d157b250ff](https://github.com/MariaDB/server/commit/d157b250ff)\
  2022-11-02 19:01:11 +0100
  * update colunmstore
* Merge [Revision #e5aa58190f](https://github.com/MariaDB/server/commit/e5aa58190f) 2022-11-02 14:33:20 +0100 - Merge branch '10.5' into 10.6
* [Revision #6414374178](https://github.com/MariaDB/server/commit/6414374178)\
  2022-10-28 17:06:00 +0200
  * followup: fix ASAN failure of main.having\_cond\_pushdown --ps
* [Revision #a472237d42](https://github.com/MariaDB/server/commit/a472237d42)\
  2022-10-28 16:51:16 +0200
  * followup: fix ASAN failure of main.opt\_tvc --ps
* [Revision #09c4253619](https://github.com/MariaDB/server/commit/09c4253619)\
  2022-10-28 16:08:43 +0200
  * [MDEV-29895](https://jira.mariadb.org/browse/MDEV-29895) prepared view crash server (unit.conc\_view)
* [Revision #2f421688c6](https://github.com/MariaDB/server/commit/2f421688c6)\
  2022-10-27 23:35:34 +0300
  * [MDEV-28709](https://jira.mariadb.org/browse/MDEV-28709) unexpected X lock on Supremum in READ COMMITTED
* [Revision #79dc3989fd](https://github.com/MariaDB/server/commit/79dc3989fd)\
  2022-10-26 14:53:06 +0300
  * Disable perfschema.mdl\_func on Windows
* [Revision #cf96db4f35](https://github.com/MariaDB/server/commit/cf96db4f35)\
  2022-10-26 14:48:53 +0300
  * [MDEV-29886](https://jira.mariadb.org/browse/MDEV-29886) Assertion !index->table->is\_temporary() failed in CHECK TABLE
* [Revision #8b6a308e46](https://github.com/MariaDB/server/commit/8b6a308e46)\
  2022-10-26 12:52:08 +0300
  * [MDEV-29883](https://jira.mariadb.org/browse/MDEV-29883) Deadlock between InnoDB statistics update and BLOB insert
* [Revision #78a04a4c22](https://github.com/MariaDB/server/commit/78a04a4c22)\
  2022-10-26 11:58:22 +0300
  * [MDEV-29869](https://jira.mariadb.org/browse/MDEV-29869) mtr failure: innodb.deadlock\_wait\_thr\_race
* [Revision #5027cb2b74](https://github.com/MariaDB/server/commit/5027cb2b74)\
  2022-10-04 16:45:51 +0700
  * [MDEV-29662](https://jira.mariadb.org/browse/MDEV-29662) Replace same values in 'IN' list with an equality
* [Revision #b7fe6179e8](https://github.com/MariaDB/server/commit/b7fe6179e8)\
  2022-10-25 08:53:56 +0200
  * [MDEV-29843](https://jira.mariadb.org/browse/MDEV-29843) Do not use asynchronous log\_write\_upto() for system THDs
* [Revision #5dd411c79a](https://github.com/MariaDB/server/commit/5dd411c79a)\
  2022-10-25 14:51:23 +0300
  * [MDEV-29871](https://jira.mariadb.org/browse/MDEV-29871): Temporarily disable the test
* Merge [Revision #aeccbbd926](https://github.com/MariaDB/server/commit/aeccbbd926) 2022-10-25 14:25:42 +0300 - Merge 10.5 into 10.6
* [Revision #75f7c5681c](https://github.com/MariaDB/server/commit/75f7c5681c)\
  2022-10-25 13:26:49 +0300
  * [MDEV-29869](https://jira.mariadb.org/browse/MDEV-29869): Temporarily disable unstable tests
* [Revision #f70960c348](https://github.com/MariaDB/server/commit/f70960c348)\
  2022-10-25 12:12:33 +0530
  * [MDEV-28327](https://jira.mariadb.org/browse/MDEV-28327) InnoDB persistent statistics fail to update after bulk insert
* [Revision #0f93d80337](https://github.com/MariaDB/server/commit/0f93d80337)\
  2022-10-24 16:10:57 +0200
  * [MDEV-28701](https://jira.mariadb.org/browse/MDEV-28701) Update 10.6 HELP tables
* [Revision #459593dceb](https://github.com/MariaDB/server/commit/459593dceb)\
  2022-10-25 08:52:17 +1100
  * [MDEV-16708](https://jira.mariadb.org/browse/MDEV-16708): mtr ps\_missed\_cmds\_bin\_prot allow for updated HELP
* [Revision #9c04d66d11](https://github.com/MariaDB/server/commit/9c04d66d11)\
  2022-10-07 23:25:58 +0300
  * [MDEV-29622](https://jira.mariadb.org/browse/MDEV-29622) Wrong assertions in lock\_cancel\_waiting\_and\_release() for deadlock resolving caller
* [Revision #acebe35719](https://github.com/MariaDB/server/commit/acebe35719)\
  2022-10-06 16:54:00 +0300
  * [MDEV-29635](https://jira.mariadb.org/browse/MDEV-29635) race on trx->lock.wait\_lock in deadlock resolution
* [Revision #ab0190101b](https://github.com/MariaDB/server/commit/ab0190101b)\
  2022-10-21 10:02:54 +0300
  * [MDEV-24402](https://jira.mariadb.org/browse/MDEV-24402): InnoDB CHECK TABLE ... EXTENDED
* [Revision #44f2ece543](https://github.com/MariaDB/server/commit/44f2ece543)\
  2022-10-20 18:55:09 +0200
  * columnstore-6.4.6-1
* [Revision #c92c161585](https://github.com/MariaDB/server/commit/c92c161585)\
  2022-10-19 01:02:29 +0300
  * Fixed compiler warning on AIX
* [Revision #db330c87d6](https://github.com/MariaDB/server/commit/db330c87d6)\
  2022-10-16 22:02:27 +0200
  * new CC v3.3
* Merge [Revision #822694bd56](https://github.com/MariaDB/server/commit/822694bd56) 2022-10-15 23:47:33 +0200 - Merge branch '10.5' into 10.6
* Merge [Revision #ce6efb584d](https://github.com/MariaDB/server/commit/ce6efb584d) 2022-10-15 23:36:57 +0200 - Merge branch 'bb-10.6-vp-[MDEV-27691](https://jira.mariadb.org/browse/MDEV-27691)' into 10.6
* [Revision #a9962580ab](https://github.com/MariaDB/server/commit/a9962580ab)\
  2022-09-27 10:55:22 +0700
  * [MDEV-27691](https://jira.mariadb.org/browse/MDEV-27691): make working view-protocol
* Merge [Revision #f8f25b472e](https://github.com/MariaDB/server/commit/f8f25b472e) 2022-09-27 13:17:59 +0700 - Merge branch 'bb-10.5-all-builders' into bb-10.6-all-builders
* [Revision #5a9a80a213](https://github.com/MariaDB/server/commit/5a9a80a213)\
  2022-10-10 16:21:46 +0530
  * [MDEV-28480](https://jira.mariadb.org/browse/MDEV-28480): Assertion \`0' failed in Item\_row::illegal\_method\_call on SELECT FROM JSON\_TABLE
* [Revision #1feccb505f](https://github.com/MariaDB/server/commit/1feccb505f)\
  2022-10-13 09:09:03 +0300
  * [MDEV-29672](https://jira.mariadb.org/browse/MDEV-29672) test fixup for --ps-protocol
* Merge [Revision #4142a73822](https://github.com/MariaDB/server/commit/4142a73822) 2022-10-13 08:27:23 +0300 - Merge 10.5 into 10.6
* Merge [Revision #a992c615a6](https://github.com/MariaDB/server/commit/a992c615a6) 2022-10-12 12:14:13 +0300 - Merge 10.5 into 10.6
* [Revision #15edd69ddf](https://github.com/MariaDB/server/commit/15edd69ddf)\
  2022-10-11 00:07:38 +0200
  * [MDEV-27943](https://jira.mariadb.org/browse/MDEV-27943) Reduce overhead of attaching THD to OS thread, in threadpool
* [Revision #eae037c286](https://github.com/MariaDB/server/commit/eae037c286)\
  2022-10-06 16:52:16 +0200
  * galera crashes in debug builds
* [Revision #5e7bafe01c](https://github.com/MariaDB/server/commit/5e7bafe01c)\
  2022-10-06 14:10:39 +0300
  * [MDEV-29710](https://jira.mariadb.org/browse/MDEV-29710): Disable a timing-sensitive test on Valgrind
* [Revision #1b1501b0f1](https://github.com/MariaDB/server/commit/1b1501b0f1)\
  2022-10-06 13:15:12 +0300
  * Simplify purge a little
* [Revision #ea1415cbb6](https://github.com/MariaDB/server/commit/ea1415cbb6)\
  2022-10-06 13:14:51 +0300
  * [MDEV-22718](https://jira.mariadb.org/browse/MDEV-22718): purge\_sys.low\_limit\_no() is not protected
* [Revision #97b0eeed2b](https://github.com/MariaDB/server/commit/97b0eeed2b)\
  2022-10-06 13:14:40 +0300
  * Cleanup: Add missing const
* [Revision #959ad2f30f](https://github.com/MariaDB/server/commit/959ad2f30f)\
  2022-10-06 13:14:16 +0300
  * [MDEV-29612](https://jira.mariadb.org/browse/MDEV-29612) ReadViewBase::snapshot() misses an optimization
* [Revision #3e9e377bf6](https://github.com/MariaDB/server/commit/3e9e377bf6)\
  2022-10-06 13:14:07 +0300
  * [MDEV-29590](https://jira.mariadb.org/browse/MDEV-29590) Deadlock between ibuf\_insert\_to\_index\_page\_low() and DDL
* [Revision #8872d2ee71](https://github.com/MariaDB/server/commit/8872d2ee71)\
  2022-10-06 12:33:40 +0300
  * [MDEV-29710](https://jira.mariadb.org/browse/MDEV-29710): Disable a timing-sensitive test on Valgrind
* Merge [Revision #b9ac0a6235](https://github.com/MariaDB/server/commit/b9ac0a6235) 2022-10-06 12:33:21 +0300 - Merge 10.5 into 10.6
* Merge [Revision #6dc157f8a6](https://github.com/MariaDB/server/commit/6dc157f8a6) 2022-10-06 09:22:39 +0300 - Merge 10.5 into 10.6
* [Revision #286acaa796](https://github.com/MariaDB/server/commit/286acaa796)\
  2022-10-05 17:18:30 +0200
  * maintainer mode: build with -Wmissing-braces
* [Revision #51fc1ad86a](https://github.com/MariaDB/server/commit/51fc1ad86a)\
  2022-10-05 18:05:39 +0300
  * After-merge fix: clang -Wmissing-braces
* [Revision #b0c7b43074](https://github.com/MariaDB/server/commit/b0c7b43074)\
  2022-10-05 11:03:46 +0300
  * [MDEV-29440](https://jira.mariadb.org/browse/MDEV-29440) fixup: Clean up dict\_load\_foreigns()
* Merge [Revision #fe449affcf](https://github.com/MariaDB/server/commit/fe449affcf) 2022-10-03 16:20:59 +0200 - Merge branch '10.5' into 10.6
* Merge [Revision #900d7bf360](https://github.com/MariaDB/server/commit/900d7bf360) 2022-10-02 22:14:21 +0200 - Merge branch '10.5' into 10.6
* [Revision #2ab52cc0e5](https://github.com/MariaDB/server/commit/2ab52cc0e5)\
  2022-09-30 17:27:38 +0200
  * update the test after merge
* Merge [Revision #194cc36805](https://github.com/MariaDB/server/commit/194cc36805) 2022-09-30 12:29:24 +0200 - Merge branch '10.5' into 10.6
* [Revision #8833c24c61](https://github.com/MariaDB/server/commit/8833c24c61)\
  2022-09-27 10:30:49 +0300
  * Revert [MDEV-29566](https://jira.mariadb.org/browse/MDEV-29566)
* [Revision #bdc5548cad](https://github.com/MariaDB/server/commit/bdc5548cad)\
  2022-09-26 15:23:29 +0300
  * [MDEV-29566](https://jira.mariadb.org/browse/MDEV-29566) Failed to read from the .par file upon concurrent DDL/SELECT with partition pruning
* Merge [Revision #829e8111c7](https://github.com/MariaDB/server/commit/829e8111c7) 2022-09-26 14:34:43 +0300 - Merge 10.5 into 10.6
* [Revision #70701ee4b1](https://github.com/MariaDB/server/commit/70701ee4b1)\
  2022-09-20 19:34:13 +0200
  * update C/C, fix srpm build failures on fedora
* [Revision #3dd03a2334](https://github.com/MariaDB/server/commit/3dd03a2334)\
  2022-09-02 11:43:14 +0200
  * [MDEV-29347](https://jira.mariadb.org/browse/MDEV-29347) [MariaDB 10.6.8](../../mariadb-community-server-release-notes/mariadb-10-6-series/mariadb-1068-release-notes.md) fails to start when ONLY\_FULL\_GROUP\_BY gets provided
* [Revision #673243c893](https://github.com/MariaDB/server/commit/673243c893)\
  2022-09-20 11:29:08 +0530
  * [MDEV-29277](https://jira.mariadb.org/browse/MDEV-29277) On error, fts\_sync\_table() fails to release a table handle
* [Revision #ca51c9fd59](https://github.com/MariaDB/server/commit/ca51c9fd59)\
  2022-09-13 11:46:28 +0900
  * [MDEV-29352](https://jira.mariadb.org/browse/MDEV-29352) SIGSEGV's in strlen and unknown location on optimized builds at SHUTDOWN
* [Revision #789f55c947](https://github.com/MariaDB/server/commit/789f55c947)\
  2022-09-21 08:00:46 +0300
  * [MDEV-28701](https://jira.mariadb.org/browse/MDEV-28701) after-merge fix
* Merge [Revision #44fd2c4b24](https://github.com/MariaDB/server/commit/44fd2c4b24) 2022-09-20 16:53:20 +0300 - Merge 10.5 into 10.6
* [Revision #5d9d379329](https://github.com/MariaDB/server/commit/5d9d379329)\
  2022-09-20 09:14:04 +0300
  * [MDEV-15020](https://jira.mariadb.org/browse/MDEV-15020) fixup: Make trx\_t::apply\_log() truly ATTRIBUTE\_COLD
* [Revision #5ab78cf340](https://github.com/MariaDB/server/commit/5ab78cf340)\
  2022-09-12 14:45:25 +0300
  * [MDEV-29515](https://jira.mariadb.org/browse/MDEV-29515) innodb.deadlock\_victim\_race is unstable
* [Revision #a762dad4ec](https://github.com/MariaDB/server/commit/a762dad4ec)\
  2022-09-19 09:38:01 -0400
  * bump the VERSION
* [Revision #5e270ca28d](https://github.com/MariaDB/server/commit/5e270ca28d)\
  2022-09-14 08:42:33 +1000
  * [MDEV-16708](https://jira.mariadb.org/browse/MDEV-16708): ps\_missed\_cmds test - HELP deconflict

{% @marketo/form formid="4316" formId="4316" %}
