# MariaDB 10.6.5 Changelog

The most recent release of [MariaDB 10.6](../../mariadb-community-server-release-notes/mariadb-10-6-series/what-is-mariadb-106.md) is:[**MariaDB 10.6.21**](../../mariadb-community-server-release-notes/mariadb-10-6-series/mariadb-10-6-21-release-notes.md) Stable (GA) [Download Now](https://mariadb.com/downloads/)[_Alternate download from mariadb.org_](https://downloads.mariadb.org/mariadb/10.6.21/)

[Download 10.6.5](https://mariadb.org/download/?tab=mariadb\&release=10.6.5\&product=mariadb)[Release Notes](../../mariadb-community-server-release-notes/mariadb-10-6-series/mariadb-1065-release-notes.md)[Changelog](mariadb-1065-changelog.md)[Overview of 10.6](../../mariadb-community-server-release-notes/mariadb-10-6-series/what-is-mariadb-106.md)

**Release date:** 8 Nov 2021

For the highlights of this release, see the[release notes](../../mariadb-community-server-release-notes/mariadb-10-6-series/mariadb-1065-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/server/tree/10.6) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Includes all fixes from [MariaDB 10.5.13](../changelogs-mariadb-105-series/mariadb-10513-changelog.md)
* Merge [Revision #109fc67d4d](https://github.com/MariaDB/server/commit/109fc67d4d) 2021-11-05 20:35:45 +0100 - Merge branch '10.5' into 10.6
* [Revision #9b967c4c31](https://github.com/MariaDB/server/commit/9b967c4c31)\
  2021-11-05 08:09:33 +0200
  * [MDEV-26826](https://jira.mariadb.org/browse/MDEV-26826) fixup: ROW\_FORMAT=COMPRESSED may corrupt buf\_pool.page\_hash
* Merge [Revision #20f7fc6ef2](https://github.com/MariaDB/server/commit/20f7fc6ef2) 2021-11-05 00:16:31 +0100 - Merge branch '10.5' into 10.6
* [Revision #e7199671b0](https://github.com/MariaDB/server/commit/e7199671b0)\
  2021-11-04 09:04:25 +0100
  * columnstore
* Merge [Revision #3a65a3eb93](https://github.com/MariaDB/server/commit/3a65a3eb93) 2021-11-03 14:13:50 +0100 - Merge branch '10.5' into 10.6
* Merge [Revision #415d26913d](https://github.com/MariaDB/server/commit/415d26913d) 2021-11-02 15:38:53 +0100 - Merge branch '10.5' into 10.6
* [Revision #3dc0d884ec](https://github.com/MariaDB/server/commit/3dc0d884ec)\
  2021-11-02 15:24:20 +0200
  * [MDEV-26674](https://jira.mariadb.org/browse/MDEV-26674) workaround for mariadb-backup
* Merge [Revision #c1adc4d078](https://github.com/MariaDB/server/commit/c1adc4d078) 2021-10-30 10:51:27 +0200 - Merge branch '10.5' into 10.6
* [Revision #003095e899](https://github.com/MariaDB/server/commit/003095e899)\
  2021-10-29 16:25:15 +0300
  * [MDEV-26936](https://jira.mariadb.org/browse/MDEV-26936) Recovery crash on rolling back DELETE FROM SYS\_INDEXES
* [Revision #37a4ea3f59](https://github.com/MariaDB/server/commit/37a4ea3f59)\
  2021-10-29 16:23:55 +0300
  * [MDEV-25683](https://jira.mariadb.org/browse/MDEV-25683) fixup: MSVC warning C4018: signed/unsigned mismatch
* [Revision #ad3e416e8d](https://github.com/MariaDB/server/commit/ad3e416e8d)\
  2021-10-29 13:04:10 +0200
  * columnstore-6.2.1-1
* Merge [Revision #facd9d524d](https://github.com/MariaDB/server/commit/facd9d524d) 2021-10-29 13:01:02 +0200 - Merge branch '10.5' into 10.6
* [Revision #dbd6c6dc01](https://github.com/MariaDB/server/commit/dbd6c6dc01)\
  2021-10-29 10:20:58 +0300
  * [MDEV-25683](https://jira.mariadb.org/browse/MDEV-25683) Atomic DDL: With innodb\_force\_recovery=3 InnoDB: Trying to load index but the index tree has been freed
* [Revision #ea45f0ebfb](https://github.com/MariaDB/server/commit/ea45f0ebfb)\
  2021-10-28 14:28:16 +0200
  * [MDEV-26925](https://jira.mariadb.org/browse/MDEV-26925) - upgrade fails creating trigger in sysschema, if root user does not exist
* Merge [Revision #d8c6c53a06](https://github.com/MariaDB/server/commit/d8c6c53a06) 2021-10-28 09:08:58 +0300 - Merge 10.5 into 10.6
* [Revision #1ad1d78981](https://github.com/MariaDB/server/commit/1ad1d78981)\
  2021-10-27 17:21:19 +0300
  * [MDEV-26779](https://jira.mariadb.org/browse/MDEV-26779): Enable adaptive spinning on ARMv8 for lock\_sys.wait\_mutex
* Merge [Revision #83dbf2c995](https://github.com/MariaDB/server/commit/83dbf2c995) 2021-10-27 13:47:58 +0300 - Merge 10.5 into 10.6
* Merge [Revision #d4a89b9262](https://github.com/MariaDB/server/commit/d4a89b9262) 2021-10-27 10:06:02 +0300 - Merge 10.5 into 10.6
* [Revision #58fe6b47d4](https://github.com/MariaDB/server/commit/58fe6b47d4)\
  2021-10-26 09:54:37 +0300
  * [MDEV-26903](https://jira.mariadb.org/browse/MDEV-26903): Assertion ctx->trx->state == TRX\_STATE\_ACTIVE on DROP INDEX
* [Revision #1193a793c4](https://github.com/MariaDB/server/commit/1193a793c4)\
  2021-10-25 10:55:04 +0300
  * [MDEV-26674](https://jira.mariadb.org/browse/MDEV-26674): Set innodb\_use\_native\_aio=OFF when using io\_uring on a potentially affected kernel
* [Revision #1f02280904](https://github.com/MariaDB/server/commit/1f02280904)\
  2021-10-22 12:38:45 +0300
  * [MDEV-26769](https://jira.mariadb.org/browse/MDEV-26769) InnoDB does not support hardware lock elision
* [Revision #c091a0bc8d](https://github.com/MariaDB/server/commit/c091a0bc8d)\
  2021-10-22 12:33:37 +0300
  * [MDEV-26826](https://jira.mariadb.org/browse/MDEV-26826) Duplicated computations of buf\_pool.page\_hash addresses
* [Revision #fdae71f8e3](https://github.com/MariaDB/server/commit/fdae71f8e3)\
  2021-10-22 12:32:26 +0300
  * [MDEV-26828](https://jira.mariadb.org/browse/MDEV-26828) Spinning on buf\_pool.page\_hash is wasting CPU cycles
* [Revision #5caff20216](https://github.com/MariaDB/server/commit/5caff20216)\
  2021-10-22 11:59:44 +0300
  * [MDEV-26883](https://jira.mariadb.org/browse/MDEV-26883) InnoDB hang due to table lock conflict
* [Revision #059a5f1171](https://github.com/MariaDB/server/commit/059a5f1171)\
  2021-10-21 17:19:43 +0200
  * Remove trailing space
* Merge [Revision #73f5cbd0b6](https://github.com/MariaDB/server/commit/73f5cbd0b6) 2021-10-21 16:06:34 +0300 - Merge 10.5 into 10.6
* [Revision #78dec1f199](https://github.com/MariaDB/server/commit/78dec1f199)\
  2021-10-20 10:04:31 +0300
  * [MDEV-26554](https://jira.mariadb.org/browse/MDEV-26554): Stabilize the test
* [Revision #d6a3f425ee](https://github.com/MariaDB/server/commit/d6a3f425ee)\
  2021-10-19 20:38:07 +0300
  * After-merge fix: Remove unused variable
* [Revision #6e390a62ba](https://github.com/MariaDB/server/commit/6e390a62ba)\
  2021-10-19 19:54:29 +0300
  * [MDEV-26772](https://jira.mariadb.org/browse/MDEV-26772) InnoDB DDL fails with DUPLICATE KEY error
* [Revision #f7684f0ca5](https://github.com/MariaDB/server/commit/f7684f0ca5)\
  2021-10-19 14:03:58 +0800
  * [MDEV-26855](https://jira.mariadb.org/browse/MDEV-26855): Enable spinning for log\_sys\_mutex and log\_flush\_order\_mutex
* [Revision #c3c53926c4](https://github.com/MariaDB/server/commit/c3c53926c4)\
  2021-10-18 18:03:12 +0300
  * [MDEV-26554](https://jira.mariadb.org/browse/MDEV-26554): Races between INSERT on child and DDL on parent table
* Merge [Revision #59fe6a8a01](https://github.com/MariaDB/server/commit/59fe6a8a01) 2021-10-18 17:47:31 +0300 - Merge 10.5 into 10.6
* Merge [Revision #9c5835e067](https://github.com/MariaDB/server/commit/9c5835e067) 2021-10-18 16:36:24 +0300 - Merge 10.5 into 10.6
* [Revision #78e023c274](https://github.com/MariaDB/server/commit/78e023c274)\
  2021-10-13 15:02:57 +0200
  * Workaround a assertion on shutdown.
* Merge [Revision #607de9c7ac](https://github.com/MariaDB/server/commit/607de9c7ac) 2021-10-13 15:17:20 +0300 - Merge 10.5 into 10.6
* Merge [Revision #a8379e53e8](https://github.com/MariaDB/server/commit/a8379e53e8) 2021-10-13 13:28:12 +0300 - Merge 10.5 into 10.6
* [Revision #ebd5205120](https://github.com/MariaDB/server/commit/ebd5205120)\
  2021-10-12 07:47:10 +0300
  * [MDEV-26467](https://jira.mariadb.org/browse/MDEV-26467) fixup for clang-9 and earlier
* [Revision #d8b8258a53](https://github.com/MariaDB/server/commit/d8b8258a53)\
  2021-10-08 13:18:59 +0200
  * [MDEV-26789](https://jira.mariadb.org/browse/MDEV-26789) log\_write\_up\_to needs mechanism to prevent stalls of async. waiters
* Merge [Revision #41c66ef6f7](https://github.com/MariaDB/server/commit/41c66ef6f7) 2021-10-06 10:28:07 +0300 - Merge 10.5 into 10.6
* Merge [Revision #c073c9a930](https://github.com/MariaDB/server/commit/c073c9a930) 2021-10-05 17:04:51 +0300 - Merge 10.5 into 10.6
* Merge [Revision #4ca56e8348](https://github.com/MariaDB/server/commit/4ca56e8348) 2021-10-05 09:21:34 +0300 - Merge 10.5 into 10.6
* [Revision #668a5f3d12](https://github.com/MariaDB/server/commit/668a5f3d12)\
  2021-10-03 13:49:40 +0300
  * [MDEV-26720](https://jira.mariadb.org/browse/MDEV-26720): Optimize single-bit atomic operations on IA-32 and AMD64
* [Revision #0144d1d2a6](https://github.com/MariaDB/server/commit/0144d1d2a6)\
  2021-10-02 11:29:44 +0300
  * [MDEV-26720](https://jira.mariadb.org/browse/MDEV-26720): rw\_lock: Prefer fetch\_sub() to fetch\_and()
* Merge [Revision #d301cc8edb](https://github.com/MariaDB/server/commit/d301cc8edb) 2021-10-02 11:19:55 +0300 - Merge 10.5 into 10.6
* [Revision #ec619a1def](https://github.com/MariaDB/server/commit/ec619a1def)\
  2021-10-02 09:25:40 +0300
  * [MDEV-26467](https://jira.mariadb.org/browse/MDEV-26467) fixup: Prefer fetch\_add() to fetch\_or() on IA-32 and AMD64
* Merge [Revision #a49e394399](https://github.com/MariaDB/server/commit/a49e394399) 2021-09-30 10:38:44 +0300 - Merge 10.5 into 10.6
* [Revision #260649de04](https://github.com/MariaDB/server/commit/260649de04)\
  2021-08-04 21:13:04 -0700
  * Misc improvements to the Gitlab-CI pipeline for MariaDB
* [Revision #309209c51c](https://github.com/MariaDB/server/commit/309209c51c)\
  2021-09-29 10:15:07 +0300
  * [MDEV-26467](https://jira.mariadb.org/browse/MDEV-26467): Use LOCK BTS also with the Microsoft compiler
* [Revision #27738bd774](https://github.com/MariaDB/server/commit/27738bd774)\
  2021-09-28 18:14:11 +0300
  * MTR: loops should divide milliseconds by milliseconds
* [Revision #e79fa9f542](https://github.com/MariaDB/server/commit/e79fa9f542)\
  2021-09-28 17:19:26 +0300
  * [MDEV-26467](https://jira.mariadb.org/browse/MDEV-26467): Actually use spinloop on block\_lock
* [Revision #d0d4ade918](https://github.com/MariaDB/server/commit/d0d4ade918)\
  2021-09-28 17:19:06 +0300
  * [MDEV-26467](https://jira.mariadb.org/browse/MDEV-26467): Universally implement spin loop
* [Revision #35f59bc4e1](https://github.com/MariaDB/server/commit/35f59bc4e1)\
  2021-09-28 17:17:59 +0300
  * [MDEV-26467](https://jira.mariadb.org/browse/MDEV-26467): More cache friendliness
* [Revision #0d68b0a2d6](https://github.com/MariaDB/server/commit/0d68b0a2d6)\
  2021-09-23 18:46:37 +0400
  * [MDEV-26669](https://jira.mariadb.org/browse/MDEV-26669) Add MY\_COLLATION\_HANDLER functions min\_str() and max\_str()
* [Revision #7697216371](https://github.com/MariaDB/server/commit/7697216371)\
  2021-09-21 13:29:27 +0530
  * [MDEV-26631](https://jira.mariadb.org/browse/MDEV-26631) InnoDB fails to fetch page from doublewrite buffer
* Merge [Revision #d95361107c](https://github.com/MariaDB/server/commit/d95361107c) 2021-09-24 14:38:52 +0300 - Merge 10.5 into 10.6
* [Revision #37a074f6c3](https://github.com/MariaDB/server/commit/37a074f6c3)\
  2021-09-24 09:18:07 +0300
  * [MDEV-26467](https://jira.mariadb.org/browse/MDEV-26467) fixup: Fix cmake -DWITH\_UNIT\_TESTS=ON for SUX\_LOCK\_GENERIC
* [Revision #b740b2356d](https://github.com/MariaDB/server/commit/b740b2356d)\
  2021-09-18 14:39:32 +0300
  * [MDEV-25919](https://jira.mariadb.org/browse/MDEV-25919) fixup: Acquire MDL also in defragmentation
* [Revision #56843d62f9](https://github.com/MariaDB/server/commit/56843d62f9)\
  2021-09-18 14:19:55 +0300
  * [MDEV-24258](https://jira.mariadb.org/browse/MDEV-24258) fixup: Correct a condition
* Merge [Revision #ae8c8d8874](https://github.com/MariaDB/server/commit/ae8c8d8874) 2021-09-17 20:07:38 +0300 - Merge 10.5 into 10.6
* [Revision #1e9c922fa7](https://github.com/MariaDB/server/commit/1e9c922fa7)\
  2021-09-17 09:14:20 +0300
  * [MDEV-26623](https://jira.mariadb.org/browse/MDEV-26623) Possible race condition between statistics and bulk insert
* [Revision #1a4a7dddb6](https://github.com/MariaDB/server/commit/1a4a7dddb6)\
  2021-09-16 12:50:55 +0300
  * Cleanup: Make btr\_root\_block\_get() more robust
* [Revision #48bbc44733](https://github.com/MariaDB/server/commit/48bbc44733)\
  2021-09-15 16:18:39 +0800
  * [MDEV-26609](https://jira.mariadb.org/browse/MDEV-26609) : Avoid deriving ELEMENT\_PER\_LATCH from cacheline
* [Revision #106b16a5af](https://github.com/MariaDB/server/commit/106b16a5af)\
  2021-09-17 07:01:01 +0300
  * [MDEV-26356](https://jira.mariadb.org/browse/MDEV-26356) fixup: integer type mismatch on 32-bit
* [Revision #9d8e83b676](https://github.com/MariaDB/server/commit/9d8e83b676)\
  2021-09-16 20:30:08 +0300
  * [MDEV-26356](https://jira.mariadb.org/browse/MDEV-26356) fixup: Adjust innodb\_max\_purge\_lag\_wait
* Merge [Revision #03c09837fc](https://github.com/MariaDB/server/commit/03c09837fc) 2021-09-16 20:17:12 +0300 - Merge 10.5 into 10.6
* [Revision #ea52a3eb97](https://github.com/MariaDB/server/commit/ea52a3eb97)\
  2021-09-14 19:06:05 +0300
  * [MDEV-26356](https://jira.mariadb.org/browse/MDEV-26356) Adaptive purge scheduling based on redo log fill factor
* [Revision #717a32154c](https://github.com/MariaDB/server/commit/717a32154c)\
  2021-09-14 19:05:05 +0300
  * [MDEV-26356](https://jira.mariadb.org/browse/MDEV-26356) preparation: Refactor purge\_state
* [Revision #03e4cb2484](https://github.com/MariaDB/server/commit/03e4cb2484)\
  2021-09-14 16:23:23 +0300
  * [MDEV-24512](https://jira.mariadb.org/browse/MDEV-24512) fixup: Remove after\_task\_callback
* [Revision #f6717c4af6](https://github.com/MariaDB/server/commit/f6717c4af6)\
  2021-09-13 11:55:14 +0300
  * [MDEV-24258](https://jira.mariadb.org/browse/MDEV-24258) fixup: Do not update dict\_table\_t::n\_ref\_count
* Merge [Revision #329d370f2d](https://github.com/MariaDB/server/commit/329d370f2d) 2021-09-11 19:05:25 +0200 - Merge branch '10.5' into 10.6
* Merge [Revision #15139964d5](https://github.com/MariaDB/server/commit/15139964d5) 2021-09-11 17:55:27 +0300 - Merge 10.5 into 10.6
* [Revision #54f79a0f7f](https://github.com/MariaDB/server/commit/54f79a0f7f)\
  2021-09-11 01:33:29 +0200
  * Early return from auth\_socket system checks on Windows
* [Revision #8ada144012](https://github.com/MariaDB/server/commit/8ada144012)\
  2021-09-11 00:54:08 +0200
  * [MDEV-26527](https://jira.mariadb.org/browse/MDEV-26527) : appveyor - do not clone Columnstore
* [Revision #b873651e3c](https://github.com/MariaDB/server/commit/b873651e3c)\
  2021-09-10 16:27:38 +0200
  * [MDEV-26527](https://jira.mariadb.org/browse/MDEV-26527) - disable unneeded submodules, too
* [Revision #f68c6ccd20](https://github.com/MariaDB/server/commit/f68c6ccd20)\
  2021-09-10 09:38:40 +0200
  * [MDEV-26579](https://jira.mariadb.org/browse/MDEV-26579) fixup
* [Revision #ca4bc3e3a9](https://github.com/MariaDB/server/commit/ca4bc3e3a9)\
  2021-09-10 02:20:16 +0200
  * [MDEV-26579](https://jira.mariadb.org/browse/MDEV-26579) Support minor MSI in Windows installer.
* [Revision #d089b51d66](https://github.com/MariaDB/server/commit/d089b51d66)\
  2021-09-09 03:47:56 +0600
  * TSAN: unprotected global variable
* [Revision #748539837e](https://github.com/MariaDB/server/commit/748539837e)\
  2021-09-09 02:51:52 +0600
  * TSAN: unprotected global variable
* [Revision #c8aa812369](https://github.com/MariaDB/server/commit/c8aa812369)\
  2021-09-09 02:20:53 +0600
  * TSAN: unprotected global counter
* [Revision #7f50edb215](https://github.com/MariaDB/server/commit/7f50edb215)\
  2021-09-09 01:58:02 +0600
  * TSAN: data race on a global counter
* [Revision #115fec58f1](https://github.com/MariaDB/server/commit/115fec58f1)\
  2021-09-08 22:01:45 +0200
  * Fix generation of bison output for out-of-source builds.
* [Revision #78084fa747](https://github.com/MariaDB/server/commit/78084fa747)\
  2021-09-08 16:45:11 +0600
  * TSAN: data race on vptr (ctor/dtor vs virtual call)
* [Revision #a6042123c1](https://github.com/MariaDB/server/commit/a6042123c1)\
  2021-09-06 19:21:09 +0300
  * Fixed typo in sql/log\_event\_server.cc related to ddl xid's.
* [Revision #7e31cfda64](https://github.com/MariaDB/server/commit/7e31cfda64)\
  2021-09-03 13:54:00 +0300
  * Errors from failed drop tables where ignored by atomic ddl.
* Merge [Revision #40ae9c5d10](https://github.com/MariaDB/server/commit/40ae9c5d10) 2021-09-07 10:37:36 +0300 - Merge 10.5 into 10.6
* [Revision #cacd8f5ad8](https://github.com/MariaDB/server/commit/cacd8f5ad8)\
  2021-08-31 08:48:27 +0300
  * Added galera MTR failed tests in diasbled list
* [Revision #d8943b0cc3](https://github.com/MariaDB/server/commit/d8943b0cc3)\
  2021-09-05 19:35:21 +0200
  * [MDEV-26527](https://jira.mariadb.org/browse/MDEV-26527) speedup appveyor build
* [Revision #7dd85c0ffd](https://github.com/MariaDB/server/commit/7dd85c0ffd)\
  2021-09-04 20:37:40 +0200
  * [MDEV-26527](https://jira.mariadb.org/browse/MDEV-26527) speedup appveyor build
* [Revision #999d254cf2](https://github.com/MariaDB/server/commit/999d254cf2)\
  2021-09-04 20:33:01 +0200
  * [MDEV-26527](https://jira.mariadb.org/browse/MDEV-26527) speedup appveyor build
* [Revision #16131a7e46](https://github.com/MariaDB/server/commit/16131a7e46)\
  2021-09-04 20:24:37 +0200
  * [MDEV-26527](https://jira.mariadb.org/browse/MDEV-26527) speedup appveyor build
* [Revision #2e39987fda](https://github.com/MariaDB/server/commit/2e39987fda)\
  2021-09-06 14:28:02 +0300
  * [MDEV-26467](https://jira.mariadb.org/browse/MDEV-26467): GCC 4.8.5 internal compiler error on ARMv8
* [Revision #277ba134ad](https://github.com/MariaDB/server/commit/277ba134ad)\
  2021-09-06 12:32:24 +0300
  * [MDEV-26467](https://jira.mariadb.org/browse/MDEV-26467): Avoid futile spin loops
* [Revision #0f0b7e47bc](https://github.com/MariaDB/server/commit/0f0b7e47bc)\
  2021-09-06 12:22:33 +0300
  * [MDEV-26467](https://jira.mariadb.org/browse/MDEV-26467): Avoid re-reading srv\_spin\_wait\_delay inside a loop
* [Revision #a73eedbf3f](https://github.com/MariaDB/server/commit/a73eedbf3f)\
  2021-09-06 12:16:26 +0300
  * [MDEV-26467](https://jira.mariadb.org/browse/MDEV-26467) Unnecessary compare-and-swap loop in srw\_mutex
* Merge [Revision #7730dd392b](https://github.com/MariaDB/server/commit/7730dd392b) 2021-09-06 10:31:32 +0300 - Merge 10.5 into 10.6
* [Revision #4c1ed54bfc](https://github.com/MariaDB/server/commit/4c1ed54bfc)\
  2021-09-05 13:09:02 +0200
  * fix Binary\_string::c\_ptr and c\_ptr\_safe
* [Revision #b9e2002702](https://github.com/MariaDB/server/commit/b9e2002702)\
  2021-09-05 11:53:36 +0200
  * cleanup: only do work when needed
* [Revision #12c3d1e1d7](https://github.com/MariaDB/server/commit/12c3d1e1d7)\
  2021-09-05 20:22:39 +0200
  * Fix Windows warnings and tests for -DPLUGIN\_PERFSCHEMA=NO
* [Revision #ae85835cc7](https://github.com/MariaDB/server/commit/ae85835cc7)\
  2021-09-05 19:37:13 +0200
  * Fix warnings from -DPLUGIN\_PARTITION=NO, portably.
* [Revision #4ffcfe7c2a](https://github.com/MariaDB/server/commit/4ffcfe7c2a)\
  2021-09-04 18:52:10 +0200
  * [MDEV-26538](https://jira.mariadb.org/browse/MDEV-26538) Incorrect error condition check for ReadFile (named pipes)
* [Revision #5ae5453291](https://github.com/MariaDB/server/commit/5ae5453291)\
  2021-09-04 19:08:14 +0300
  * [MDEV-25919](https://jira.mariadb.org/browse/MDEV-25919) fixup: MSAN and Valgrind errors related to statistics
* [Revision #c4ebfe22f9](https://github.com/MariaDB/server/commit/c4ebfe22f9)\
  2021-09-03 18:48:38 +0300
  * [MDEV-4750](https://jira.mariadb.org/browse/MDEV-4750) fixup: main.backup\_lock result difference
* [Revision #4690442411](https://github.com/MariaDB/server/commit/4690442411)\
  2021-09-02 17:17:18 +0300
  * [MDEV-24258](https://jira.mariadb.org/browse/MDEV-24258) fixup: Throttle purge with exclusive dict\_sys.latch
* [Revision #ee39757f3c](https://github.com/MariaDB/server/commit/ee39757f3c)\
  2021-09-01 07:44:11 +0300
  * After-merge fix e94172c2a07f21118d26e4cde0c48a2fd536cf06: unit.conc\_cursor
* [Revision #241e2ba642](https://github.com/MariaDB/server/commit/241e2ba642)\
  2021-08-31 15:38:56 +0300
  * [MDEV-25919](https://jira.mariadb.org/browse/MDEV-25919) fixup: set\_current\_thd() is not defined
* Merge [Revision #55a344ffa3](https://github.com/MariaDB/server/commit/55a344ffa3) 2021-08-31 13:56:15 +0300 - Merge 10.5 into 10.6
* [Revision #9608773f75](https://github.com/MariaDB/server/commit/9608773f75)\
  2021-08-31 13:55:02 +0300
  * [MDEV-4750](https://jira.mariadb.org/browse/MDEV-4750) follow-up: Reduce disabling innodb\_stats\_persistent
* [Revision #45a05fda27](https://github.com/MariaDB/server/commit/45a05fda27)\
  2021-08-31 13:54:55 +0300
  * [MDEV-25919](https://jira.mariadb.org/browse/MDEV-25919): Replace dict\_table\_t::stats\_bg\_flag with MDL
* [Revision #c5fd9aa562](https://github.com/MariaDB/server/commit/c5fd9aa562)\
  2021-08-31 13:54:44 +0300
  * [MDEV-25919](https://jira.mariadb.org/browse/MDEV-25919): Lock tables before acquiring dict\_sys.latch
* [Revision #094de71742](https://github.com/MariaDB/server/commit/094de71742)\
  2021-08-31 13:54:20 +0300
  * [MDEV-25919](https://jira.mariadb.org/browse/MDEV-25919) preparation: Various cleanup
* [Revision #6a2cd6f4b4](https://github.com/MariaDB/server/commit/6a2cd6f4b4)\
  2021-08-31 13:54:06 +0300
  * [MDEV-19505](https://jira.mariadb.org/browse/MDEV-19505) Do not hold mutex while calling que\_graph\_free()
* [Revision #82b7c561b7](https://github.com/MariaDB/server/commit/82b7c561b7)\
  2021-08-31 13:51:35 +0300
  * [MDEV-24258](https://jira.mariadb.org/browse/MDEV-24258) Merge dict\_sys.mutex into dict\_sys.latch
* [Revision #2e08b6d78c](https://github.com/MariaDB/server/commit/2e08b6d78c)\
  2021-08-31 13:48:10 +0300
  * [MDEV-24258](https://jira.mariadb.org/browse/MDEV-24258) preparation: Remove dict\_sys.freeze() and unfreeze()
* [Revision #4362ed1b6f](https://github.com/MariaDB/server/commit/4362ed1b6f)\
  2021-08-31 13:48:00 +0300
  * [MDEV-25691](https://jira.mariadb.org/browse/MDEV-25691) fixup: Avoid MDL acquisition in purge
* Merge [Revision #e94172c2a0](https://github.com/MariaDB/server/commit/e94172c2a0) 2021-08-31 11:00:41 +0300 - Merge 10.5 into 10.6
* [Revision #7271cf48d6](https://github.com/MariaDB/server/commit/7271cf48d6)\
  2021-08-28 10:37:37 +0200
  * bugfix: don't filter out lzma from rpm dependencies
* [Revision #77ae644f57](https://github.com/MariaDB/server/commit/77ae644f57)\
  2021-08-28 10:34:05 +0200
  * remove tokudb tests (fix bad merge)
* Merge [Revision #cc4e20e56f](https://github.com/MariaDB/server/commit/cc4e20e56f) 2021-08-26 10:20:17 +0300 - Merge 10.5 into 10.6
* Merge [Revision #ded27d2896](https://github.com/MariaDB/server/commit/ded27d2896) 2021-08-25 08:15:20 +0300 - Merge 10.5 into 10.6
* Merge [Revision #49f95c4065](https://github.com/MariaDB/server/commit/49f95c4065) 2021-08-23 11:21:33 +0300 - Merge 10.5 into 10.6
* [Revision #75c641d22b](https://github.com/MariaDB/server/commit/75c641d22b)\
  2021-08-22 10:39:42 +0200
  * need at least Bison 2.4 for `%define api.pure`
* [Revision #b0d38448a1](https://github.com/MariaDB/server/commit/b0d38448a1)\
  2021-08-19 15:56:09 +0530
  * [MDEV-25958](https://jira.mariadb.org/browse/MDEV-25958): rpl\_semi\_sync\_fail\_over.test fails in buildbot
* [Revision #d12b5e2187](https://github.com/MariaDB/server/commit/d12b5e2187)\
  2021-08-19 13:02:05 +0300
  * [MDEV-20931](https://jira.mariadb.org/browse/MDEV-20931) fixup: innodb.import\_corrtupted test cleanup
* Merge [Revision #f3fcf5f45c](https://github.com/MariaDB/server/commit/f3fcf5f45c) 2021-08-19 12:25:00 +0300 - Merge 10.5 to 10.6
* [Revision #475f69b985](https://github.com/MariaDB/server/commit/475f69b985)\
  2021-08-16 12:25:52 +0530
  * [MDEV-25958](https://jira.mariadb.org/browse/MDEV-25958): rpl\_semi\_sync\_fail\_over.test fails in buildbot
* [Revision #583516bbb9](https://github.com/MariaDB/server/commit/583516bbb9)\
  2021-08-13 14:01:26 +0530
  * [MDEV-25962](https://jira.mariadb.org/browse/MDEV-25962): binlog.binlog\_truncate\_multi\_log\_unsafe test fails in buildbot
* [Revision #9ac1ac0061](https://github.com/MariaDB/server/commit/9ac1ac0061)\
  2021-08-11 11:26:35 +0200
  * Fix clang-cl warning
* [Revision #78c7d50e4f](https://github.com/MariaDB/server/commit/78c7d50e4f)\
  2021-08-09 11:52:03 +0200
  * Fix cmake warning caused by 751ebe44fda4deb715fc2235548517c287f2a559
* Merge [Revision #1add892e6d](https://github.com/MariaDB/server/commit/1add892e6d) 2021-08-09 11:24:25 +0200 - Merge branch '10.6' of [server](https://github.com/mariadb/server) into 10.6
* [Revision #e38b372e7c](https://github.com/MariaDB/server/commit/e38b372e7c)\
  2021-08-04 20:43:56 +0700
  * [MDEV-26180](https://jira.mariadb.org/browse/MDEV-26180): follow-up patch to temporary disable the test main.func\_group in PS mode.
* [Revision #fbadc87fce](https://github.com/MariaDB/server/commit/fbadc87fce)\
  2021-08-05 10:42:39 -0400
  * bump the VERSION
* [Revision #3cc23c9973](https://github.com/MariaDB/server/commit/3cc23c9973)\
  2021-08-04 12:44:46 +0200
  * [MDEV-25602](https://jira.mariadb.org/browse/MDEV-25602) Eliminate the rest of WIN in Connect
* [Revision #7308e009c9](https://github.com/MariaDB/server/commit/7308e009c9)\
  2021-08-04 15:32:31 +0200
  * auth\_socket: Add SO\_PEERCRED definitions for NetBSD

{% @marketo/form formid="4316" formId="4316" %}
