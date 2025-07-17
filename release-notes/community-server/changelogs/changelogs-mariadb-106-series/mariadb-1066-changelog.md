# MariaDB 10.6.6 Changelog

{% include "../../../.gitbook/includes/latest-10-6.md" %}

&#x20;<a href="../../mariadb-10-6-series/mariadb-1066-release-notes.md" class="button secondary">Release Notes</a> <a href="mariadb-1066-changelog.md" class="button secondary">Changelog</a> <a href="../../mariadb-10-6-series/what-is-mariadb-106.md" class="button secondary">Overview of 10.6</a>

**Release date:** 9 Feb 2022

For the highlights of this release, see the [release notes](../../mariadb-10-6-series/mariadb-1066-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On [GitHub](https://github.com/MariaDB/server/tree/10.6) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Includes all fixes from [MariaDB 10.5.14](../changelogs-mariadb-105-series/mariadb-10514-changelog.md)
* [Revision #4ffffd98a5](https://github.com/MariaDB/server/commit/4ffffd98a5)\
  2022-02-05 14:50:25 +0100
  * update columnstore
* [Revision #a806c993e7](https://github.com/MariaDB/server/commit/a806c993e7)\
  2022-02-04 14:40:42 +0100
  * Fix for compiling under clang.
* Merge [Revision #d87979b48c](https://github.com/MariaDB/server/commit/d87979b48c) 2022-02-04 10:01:08 +0100 - Merge branch '10.5' into 10.6
* [Revision #82f5981e72](https://github.com/MariaDB/server/commit/82f5981e72)\
  2022-02-03 16:51:08 +0200
  * [MDEV-27058](https://jira.mariadb.org/browse/MDEV-27058) fixup: Crash in innodb.leaf\_page\_corrupted\_during\_recovery
* [Revision #05c33d6216](https://github.com/MariaDB/server/commit/05c33d6216)\
  2022-02-03 12:18:14 +0200
  * [MDEV-27736](https://jira.mariadb.org/browse/MDEV-27736) Allow seamless upgrade despite ROW\_FORMAT=COMPRESSED
* Merge [Revision #f5c5f8e41e](https://github.com/MariaDB/server/commit/f5c5f8e41e) 2022-02-03 17:01:31 +0100 - Merge branch '10.5' into 10.6
* [Revision #8d742fe4ac](https://github.com/MariaDB/server/commit/8d742fe4ac)\
  2022-01-29 18:10:25 +0530
  * [MDEV-26326](https://jira.mariadb.org/browse/MDEV-26326) mariadb-backup skip valid ibd file
* [Revision #62ba2f230a](https://github.com/MariaDB/server/commit/62ba2f230a)\
  2022-01-31 21:50:57 +0100
  * [MDEV-27535](https://jira.mariadb.org/browse/MDEV-27535) remove debug output
* [Revision #8c457dad48](https://github.com/MariaDB/server/commit/8c457dad48)\
  2022-01-31 20:09:45 +0100
  * [MDEV-27546](https://jira.mariadb.org/browse/MDEV-27546) MSI should fail if INSTALLDIR is a non-empty existing directory
* [Revision #12cea09713](https://github.com/MariaDB/server/commit/12cea09713)\
  2022-01-31 15:40:41 +0100
  * [MDEV-27535](https://jira.mariadb.org/browse/MDEV-27535) Service does not start after MSI install into restricted directory
* [Revision #2a0962f39b](https://github.com/MariaDB/server/commit/2a0962f39b)\
  2022-01-31 21:18:43 +0400
  * [MDEV-27696](https://jira.mariadb.org/browse/MDEV-27696) Json table columns accept redundant COLLATE syntax
* [Revision #2d4a0f6079](https://github.com/MariaDB/server/commit/2d4a0f6079)\
  2022-01-30 22:52:59 +0100
  * pass MYSQL\_MAINTAINER\_MODE down to srpm builds
* [Revision #77b3777bab](https://github.com/MariaDB/server/commit/77b3777bab)\
  2022-01-30 16:37:12 +0100
  * update columnstore to 6.2.3-1
* [Revision #bc10f58a58](https://github.com/MariaDB/server/commit/bc10f58a58)\
  2021-07-02 19:13:26 +0200
  * [MDEV-24909](https://jira.mariadb.org/browse/MDEV-24909) JSON functions don't respect KILL QUERY / max\_statement\_time limit
* [Revision #bae9fb5904](https://github.com/MariaDB/server/commit/bae9fb5904)\
  2021-07-02 19:11:42 +0200
  * [MDEV-24909](https://jira.mariadb.org/browse/MDEV-24909) JSON functions don't respect KILL QUERY / max\_statement\_time limit
* [Revision #3add51b769](https://github.com/MariaDB/server/commit/3add51b769)\
  2021-07-01 20:02:12 +0200
  * cleanup: move the common code into the function
* [Revision #3cc278e960](https://github.com/MariaDB/server/commit/3cc278e960)\
  2022-01-26 21:32:17 +0100
  * enable main.mysqldump-system test
* [Revision #c478a5533e](https://github.com/MariaDB/server/commit/c478a5533e)\
  2022-01-28 16:42:37 +0200
  * [MDEV-27667](https://jira.mariadb.org/browse/MDEV-27667) Fix [MDEV-26720](https://jira.mariadb.org/browse/MDEV-26720) on 64-bit Microsoft Windows
* [Revision #f0f5ce58c7](https://github.com/MariaDB/server/commit/f0f5ce58c7)\
  2022-01-28 08:31:57 +0200
  * [MDEV-27402](https://jira.mariadb.org/browse/MDEV-27402) 'asm goto' is not supported on Apple Xcode 9.4.1
* [Revision #48b974b267](https://github.com/MariaDB/server/commit/48b974b267)\
  2022-01-27 18:14:37 +0200
  * [MDEV-27026](https://jira.mariadb.org/browse/MDEV-27026) innodb\_fts.concurrent\_insert failed
* [Revision #b09a744383](https://github.com/MariaDB/server/commit/b09a744383)\
  2022-01-26 09:51:22 +0100
  * new CC 3.2
* Merge [Revision #21778b8aa8](https://github.com/MariaDB/server/commit/21778b8aa8) 2022-01-20 07:39:11 +0200 - Merge 10.5 into 10.6
* [Revision #764ca7e6e7](https://github.com/MariaDB/server/commit/764ca7e6e7)\
  2022-01-19 19:12:17 +0200
  * [MDEV-27499](https://jira.mariadb.org/browse/MDEV-27499) fixup: Add a wait to buf\_flush\_sync()
* Merge [Revision #965c0d2240](https://github.com/MariaDB/server/commit/965c0d2240) 2022-01-19 09:57:28 +0200 - [MDEV-27025](https://jira.mariadb.org/browse/MDEV-27025): Null merge 10.5 into 10.6
* [Revision #bd03c0e516](https://github.com/MariaDB/server/commit/bd03c0e516)\
  2021-12-02 16:14:27 +0300
  * [MDEV-27025](https://jira.mariadb.org/browse/MDEV-27025) insert-intention lock conflicts with waiting ORDINARY lock
* Merge [Revision #1abc476f0b](https://github.com/MariaDB/server/commit/1abc476f0b) 2022-01-18 12:59:50 +0200 - Merge 10.5 into 10.6
* [Revision #343f695c7f](https://github.com/MariaDB/server/commit/343f695c7f)\
  2022-01-17 11:19:41 +0200
  * [MDEV-27469](https://jira.mariadb.org/browse/MDEV-27469): Assertion failure in defragment due to tx\_read\_only
* Merge [Revision #16b87f9890](https://github.com/MariaDB/server/commit/16b87f9890) 2022-01-14 18:19:04 +0200 - Merge 10.5 into 10.6
* [Revision #e6a0611388](https://github.com/MariaDB/server/commit/e6a0611388)\
  2022-01-13 16:45:31 +0200
  * [MDEV-27058](https://jira.mariadb.org/browse/MDEV-27058) fixup: Bogus assertion !block->page.is\_io\_fixed()
* [Revision #ba5ef63ae1](https://github.com/MariaDB/server/commit/ba5ef63ae1)\
  2022-01-12 12:34:07 +0200
  * [MDEV-27476](https://jira.mariadb.org/browse/MDEV-27476) heap-use-after-free in buf\_pool\_t::is\_block\_field()
* Merge [Revision #0261eac57f](https://github.com/MariaDB/server/commit/0261eac57f) 2022-01-12 12:33:19 +0200 - Merge 10.5 into 10.6
* [Revision #428b057ee0](https://github.com/MariaDB/server/commit/428b057ee0)\
  2022-01-10 19:15:39 +0530
  * [MDEV-27640](https://jira.mariadb.org/browse/MDEV-27640) trx\_has\_lock\_x() gives wrong result if the table has pending table lock
* [Revision #fcbd398924](https://github.com/MariaDB/server/commit/fcbd398924)\
  2022-01-10 11:21:17 +0200
  * Cleanup: Remove unused log\_cmdq\_key
* [Revision #75d4c530c5](https://github.com/MariaDB/server/commit/75d4c530c5)\
  2022-01-09 14:09:00 +0200
  * [MDEV-26879](https://jira.mariadb.org/browse/MDEV-26879): Detach innodb\_evict\_tables\_on\_commit\_debug from SAFE\_MUTEX
* [Revision #e8d1bb0459](https://github.com/MariaDB/server/commit/e8d1bb0459)\
  2021-12-30 13:13:58 +0530
  * [MDEV-27017](https://jira.mariadb.org/browse/MDEV-27017) Assertion failure 'table->get\_ref\_count() == 0' on DDL that involves FULLTEXT INDEX
* [Revision #59e8a12657](https://github.com/MariaDB/server/commit/59e8a12657)\
  2022-01-05 12:14:01 +0200
  * [MDEV-26879](https://jira.mariadb.org/browse/MDEV-26879) innodb\_evict\_tables\_on\_commit\_debug=on makes table creation hang
* [Revision #2a6e086902](https://github.com/MariaDB/server/commit/2a6e086902)\
  2021-12-21 12:24:35 +0100
  * [MDEV-27335](https://jira.mariadb.org/browse/MDEV-27335) Windows, MSI - Bring the datadir location into the instance config UI
* [Revision #3712808ad2](https://github.com/MariaDB/server/commit/3712808ad2)\
  2021-12-18 14:51:07 +0100
  * Windows installer - fix UI of the "Uninstall" Dialog.
* [Revision #b773416888](https://github.com/MariaDB/server/commit/b773416888)\
  2022-01-05 09:58:52 +1100
  * Update errmsg-utf8.txt (spa) part 2
* [Revision #cd751f0259](https://github.com/MariaDB/server/commit/cd751f0259)\
  2022-01-04 15:53:02 +0200
  * Work around [MDEV-27421](https://jira.mariadb.org/browse/MDEV-27421) ./mtr --ps-protocol main.opt\_trace
* Merge [Revision #3f5726768f](https://github.com/MariaDB/server/commit/3f5726768f) 2022-01-04 09:26:38 +0200 - Merge 10.5 into 10.6
* [Revision #c410f7aaea](https://github.com/MariaDB/server/commit/c410f7aaea)\
  2022-01-03 17:42:13 +0200
  * [MDEV-27414](https://jira.mariadb.org/browse/MDEV-27414) Server may hang when innodb\_undo\_log\_truncate=ON
* [Revision #30b917d34a](https://github.com/MariaDB/server/commit/30b917d34a)\
  2021-12-27 12:36:51 +0200
  * [MDEV-27039](https://jira.mariadb.org/browse/MDEV-27039) Trying to lock mutex ... when the mutex was already locked
* [Revision #3e0304884b](https://github.com/MariaDB/server/commit/3e0304884b)\
  2020-12-29 11:59:01 +0000
  * Update errmsg-utf8.txt (spa)
* [Revision #dc74d23482](https://github.com/MariaDB/server/commit/dc74d23482)\
  2021-12-23 21:07:28 +0900
  * [MDEV-27184](https://jira.mariadb.org/browse/MDEV-27184) Assertion `(old_top == initial_top (av) && old_size == 0) || ((unsigned long) (old_size) >= MINSIZE && prev_inuse (old_top) && ((unsigned long) old_end & (pagesize - 1)) == 0)' failed, Assertion` str.alloced\_length() >= str.length() + data\_len' failed
* [Revision #3c1cde864e](https://github.com/MariaDB/server/commit/3c1cde864e)\
  2021-12-22 15:53:55 +0200
  * [MDEV-27181](https://jira.mariadb.org/browse/MDEV-27181) fixup: Replace symlinks
* [Revision #14521992b0](https://github.com/MariaDB/server/commit/14521992b0)\
  2021-12-21 17:33:26 +0200
  * [MDEV-27336](https://jira.mariadb.org/browse/MDEV-27336) Crash on DROP DATABASE due to out-of-bounds result from InnoDB SUBSTR()
* [Revision #8e5f09a6ed](https://github.com/MariaDB/server/commit/8e5f09a6ed)\
  2021-12-21 12:26:03 +0530
  * [MDEV-27322](https://jira.mariadb.org/browse/MDEV-27322) Test innodb.doublewrite crashes when using innodb\_flush\_method=O\_DIRECT
* [Revision #32692140e1](https://github.com/MariaDB/server/commit/32692140e1)\
  2021-12-19 17:19:02 +0300
  * [MDEV-27306](https://jira.mariadb.org/browse/MDEV-27306): SET STATEMENT optimizer\_trace=1 Doesn't save the trace
* [Revision #946dafb260](https://github.com/MariaDB/server/commit/946dafb260)\
  2021-12-16 19:16:04 +0100
  * [MDEV-26925](https://jira.mariadb.org/browse/MDEV-26925) add test that there are no triggers in sys schema.
* [Revision #30bf0bca8f](https://github.com/MariaDB/server/commit/30bf0bca8f)\
  2021-12-14 03:47:59 +0100
  * [MDEV-27181](https://jira.mariadb.org/browse/MDEV-27181): Galera SST scripts should use ssl\_capath for CA directory
* [Revision #660cfe4782](https://github.com/MariaDB/server/commit/660cfe4782)\
  2021-12-12 15:09:59 +0530
  * [MDEV-27014](https://jira.mariadb.org/browse/MDEV-27014) InnoDB fails to restore page 0 from the doublewrite buffer
* [Revision #18c335a39e](https://github.com/MariaDB/server/commit/18c335a39e)\
  2021-12-12 09:58:31 +0530
  * [MDEV-27111](https://jira.mariadb.org/browse/MDEV-27111) atomic.rename\_table test case fails
* [Revision #be5990d0c8](https://github.com/MariaDB/server/commit/be5990d0c8)\
  2021-12-07 08:19:27 +0530
  * [MDEV-27014](https://jira.mariadb.org/browse/MDEV-27014) InnoDB fails to restore page 0 from the doublewrite buffer
* [Revision #50ed0bd891](https://github.com/MariaDB/server/commit/50ed0bd891)\
  2021-12-10 11:29:06 +0200
  * [MDEV-27219](https://jira.mariadb.org/browse/MDEV-27219) Some error messages might report table names incorrectly on LLP64
* Merge [Revision #186c1fa250](https://github.com/MariaDB/server/commit/186c1fa250) 2021-12-07 22:11:30 +0100 - Merge branch '10.5' into 10.6
* [Revision #6deaff58a9](https://github.com/MariaDB/server/commit/6deaff58a9)\
  2021-12-04 12:55:26 +0200
  * [MDEV-27058](https://jira.mariadb.org/browse/MDEV-27058) fixup: GCC 11 -march=i686 -Warray-bounds
* Merge [Revision #3f7040fa97](https://github.com/MariaDB/server/commit/3f7040fa97) 2021-12-04 12:42:29 +0200 - Merge 10.5 into 10.6
* [Revision #e0e24b180d](https://github.com/MariaDB/server/commit/e0e24b180d)\
  2021-12-01 13:37:06 +0530
  * [MDEV-27014](https://jira.mariadb.org/browse/MDEV-27014) InnoDB fails to restore page 0 from the doublewrite buffer
* [Revision #cab8f4b552](https://github.com/MariaDB/server/commit/cab8f4b552)\
  2021-11-15 18:19:53 +0530
  * [MDEV-27014](https://jira.mariadb.org/browse/MDEV-27014) InnoDB fails to restore page 0 from the doublewrite buffer
* [Revision #5f22e83a29](https://github.com/MariaDB/server/commit/5f22e83a29)\
  2021-11-19 12:17:14 +0300
  * Make the Optimizer Trace of reqular query and PS EXECUTE be identical
* Merge [Revision #51c89849d1](https://github.com/MariaDB/server/commit/51c89849d1) 2021-11-29 11:39:34 +0200 - Merge 10.5 into 10.6
* [Revision #bf8735eb16](https://github.com/MariaDB/server/commit/bf8735eb16)\
  2021-11-28 11:03:02 +0100
  * Fix MSVC warning C4819 when system codepage is set to UTF-8.
* [Revision #e85089afca](https://github.com/MariaDB/server/commit/e85089afca)\
  2021-10-28 23:39:29 +0200
  * Windows : fix clang-cl build.
* [Revision #d2bbeeef6f](https://github.com/MariaDB/server/commit/d2bbeeef6f)\
  2021-11-25 15:54:19 +0200
  * galera.galera\_unicode\_pk: Avoid MDL wait timeout
* [Revision #71e10ba3bb](https://github.com/MariaDB/server/commit/71e10ba3bb)\
  2021-11-25 14:03:20 +0200
  * Make innodb.innodb-table-online more stable
* Merge [Revision #3cfbfa58de](https://github.com/MariaDB/server/commit/3cfbfa58de) 2021-11-25 08:08:42 +0200 - Merge 10.5 into 10.6
* [Revision #de7db5517d](https://github.com/MariaDB/server/commit/de7db5517d)\
  2021-11-23 14:38:05 +0200
  * [MDEV-26674](https://jira.mariadb.org/browse/MDEV-26674) follow-up: Bless Linux 5.15.3
* [Revision #fcc8f480af](https://github.com/MariaDB/server/commit/fcc8f480af)\
  2021-11-24 17:51:34 +0200
  * Fix build failure on mac due to invalid access on private member from rw\_lock
* [Revision #9436c778c3](https://github.com/MariaDB/server/commit/9436c778c3)\
  2021-11-20 13:57:23 +0200
  * [MDEV-27058](https://jira.mariadb.org/browse/MDEV-27058) fixup: Fix MemorySanitizer, and GCC 4.8.5 ICE on ARMv8
* [Revision #da3475605e](https://github.com/MariaDB/server/commit/da3475605e)\
  2021-11-19 18:54:23 +0200
  * [MDEV-27058](https://jira.mariadb.org/browse/MDEV-27058) fixup: Avoid a hang with ROW\_FORMAT=COMPRESSED
* [Revision #e0f7c89c18](https://github.com/MariaDB/server/commit/e0f7c89c18)\
  2021-11-19 09:10:40 +0200
  * [MDEV-26747](https://jira.mariadb.org/browse/MDEV-26747) after-merge fix for [MDEV-12026](https://jira.mariadb.org/browse/MDEV-12026), [MDEV-25105](https://jira.mariadb.org/browse/MDEV-25105)
* [Revision #aaef2e1d8c](https://github.com/MariaDB/server/commit/aaef2e1d8c)\
  2021-11-16 19:55:06 +0200
  * [MDEV-27058](https://jira.mariadb.org/browse/MDEV-27058): Reduce the size of buf\_block\_t and buf\_page\_t
* [Revision #db915f7387](https://github.com/MariaDB/server/commit/db915f7387)\
  2021-11-16 18:16:53 +0200
  * [MDEV-27058](https://jira.mariadb.org/browse/MDEV-27058): Move buf\_page\_t::slot to IORequest::slot
* [Revision #02e72f7b44](https://github.com/MariaDB/server/commit/02e72f7b44)\
  2021-11-16 18:16:22 +0200
  * [MDEV-26769](https://jira.mariadb.org/browse/MDEV-26769) follow-up: Remove unnecessary page locking
* [Revision #14c5178f25](https://github.com/MariaDB/server/commit/14c5178f25)\
  2021-11-18 17:39:39 +0200
  * [MDEV-27069](https://jira.mariadb.org/browse/MDEV-27069): heap-use-after-free in dict\_stats\_recalc\_pool\_del()
* [Revision #862eccd524](https://github.com/MariaDB/server/commit/862eccd524)\
  2021-11-18 17:34:19 +0200
  * [MDEV-26769](https://jira.mariadb.org/browse/MDEV-26769) fixup: Fix the SUX\_LOCK\_GENERIC build
* Merge [Revision #0a168398a0](https://github.com/MariaDB/server/commit/0a168398a0) 2021-11-17 15:03:47 +0200 - Merge 10.5 into 10.6
* Merge [Revision #6841d1afdd](https://github.com/MariaDB/server/commit/6841d1afdd) 2021-11-16 17:15:13 +0200 - Merge 10.5 into 10.6
* [Revision #89ab2538c5](https://github.com/MariaDB/server/commit/89ab2538c5)\
  2021-11-16 16:31:45 +0200
  * [MDEV-27028](https://jira.mariadb.org/browse/MDEV-27028) \[ERROR] \[FATAL] InnoDB: SYS\_VIRTUAL.TABLE\_ID mismatch
* Merge [Revision #dc8def73f7](https://github.com/MariaDB/server/commit/dc8def73f7) 2021-11-16 16:30:45 +0200 - Merge 10.5 into 10.6
* Merge [Revision #e58a312e42](https://github.com/MariaDB/server/commit/e58a312e42) 2021-11-12 00:33:48 +0100 - Merge branch '10.5' into 10.6
* [Revision #3480c3f95b](https://github.com/MariaDB/server/commit/3480c3f95b)\
  2021-11-10 11:35:19 +0530
  * [MDEV-26121](https://jira.mariadb.org/browse/MDEV-26121) \[Note] InnoDB: Resetting invalid page
* [Revision #3989d3800d](https://github.com/MariaDB/server/commit/3989d3800d)\
  2021-11-09 18:08:12 +0530
  * [MDEV-27006](https://jira.mariadb.org/browse/MDEV-27006) Assertion \`!lock\_trx\_has\_sys\_table\_locks(trx)' failed in dberr\_t row\_discard\_tablespace\_for\_mysql(dict\_table\_t\*, trx\_t\*)
* [Revision #ba4f8e317d](https://github.com/MariaDB/server/commit/ba4f8e317d)\
  2021-11-09 09:38:12 +0200
  * [MDEV-26826](https://jira.mariadb.org/browse/MDEV-26826) fixup for Valgrind and MemorySanitizer
* Merge [Revision #25ac047baf](https://github.com/MariaDB/server/commit/25ac047baf) 2021-11-09 09:11:50 +0200 - Merge 10.5 into 10.6
* Merge [Revision #96f8532606](https://github.com/MariaDB/server/commit/96f8532606) 2021-11-08 19:42:18 +0100 - Merge branch '10.6' into bb-10.6-release
* [Revision #c85caaa20b](https://github.com/MariaDB/server/commit/c85caaa20b)\
  2021-11-08 12:03:38 -0500
  * bump the VERSION
* [Revision #3ab358f0f1](https://github.com/MariaDB/server/commit/3ab358f0f1)\
  2021-11-03 18:23:16 +0100
  * appveyor - do not use buggy cygwin bison.
* [Revision #667e71399e](https://github.com/MariaDB/server/commit/667e71399e)\
  2021-11-04 09:59:06 +0200
  * [MDEV-26826](https://jira.mariadb.org/browse/MDEV-26826) fixup: clang++-13 -Wfree-nonheap-object
* [Revision #576afceadd](https://github.com/MariaDB/server/commit/576afceadd)\
  2021-11-04 09:55:35 +0200
  * [MDEV-26966](https://jira.mariadb.org/browse/MDEV-26966): Remove innodb\_force\_load\_corrupted
* [Revision #993b8edf3f](https://github.com/MariaDB/server/commit/993b8edf3f)\
  2021-11-01 13:35:47 +0200
  * [MDEV-26933](https://jira.mariadb.org/browse/MDEV-26933) InnoDB fails to detect page number mismatch
* [Revision #fdc4c3a298](https://github.com/MariaDB/server/commit/fdc4c3a298)\
  2021-10-29 16:23:55 +0300
  * [MDEV-25683](https://jira.mariadb.org/browse/MDEV-25683) fixup: MSVC warning C4018: signed/unsigned mismatch

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
