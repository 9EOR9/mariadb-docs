# MariaDB 10.9.8 Changelog

[Download](https://mariadb.com/downloads/)[Release Notes](../../old-releases/release-notes-mariadb-10-9-series/mariadb-10-9-8-release-notes.md)[Changelog](mariadb-10-9-8-changelog.md)[Overview of 10.9](../../old-releases/release-notes-mariadb-10-9-series/what-is-mariadb-109.md)

[_Alternate download from mariadb.org_](https://downloads.mariadb.org/mariadb/10.9.8/)

**Release date:** 14 Aug 2023

For the highlights of this release, see the[release notes](../../old-releases/release-notes-mariadb-10-9-series/mariadb-10-9-8-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/server/tree/10.9) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Includes all fixes from [MariaDB 10.8.8](../changelogs-mariadb-10-8-series/mariadb-10-8-8-changelog.md)
* Includes all fixes from [MariaDB 10.6.15](../changelogs-mariadb-106-series/mariadb-10-6-15-changelog.md)
* Merge [Revision #f692b2b6bb](https://github.com/MariaDB/server/commit/f692b2b6bb) 2023-08-09 21:21:31 +0200 - Merge branch '10.6' into 10.9
* Merge [Revision #27dc4cd1fc](https://github.com/MariaDB/server/commit/27dc4cd1fc) 2023-08-08 13:28:26 +0200 - Merge branch '10.6' into 10.9
* Merge [Revision #214654118a](https://github.com/MariaDB/server/commit/214654118a) 2023-08-07 10:33:32 +0200 - Merge branch '10.6' into 10.9
* Merge [Revision #998edc374e](https://github.com/MariaDB/server/commit/998edc374e) 2023-08-04 13:27:20 +0200 - Merge branch '10.6' into 10.9
* Merge [Revision #34a8e78581](https://github.com/MariaDB/server/commit/34a8e78581) 2023-08-04 08:01:06 +0200 - Merge branch '10.6' into 10.9
* [Revision #a89527e127](https://github.com/MariaDB/server/commit/a89527e127)\
  2023-08-02 19:28:12 +0300
  * [MDEV-31827](https://jira.mariadb.org/browse/MDEV-31827) InnoDB multi-batch recovery stops prematurely
* [Revision #8760fe11b8](https://github.com/MariaDB/server/commit/8760fe11b8)\
  2023-08-02 11:52:00 +0300
  * [MDEV-31791](https://jira.mariadb.org/browse/MDEV-31791): Recovery on memory-mapped log occasionally fails
* [Revision #941af1fa58](https://github.com/MariaDB/server/commit/941af1fa58)\
  2023-07-31 16:42:23 +0530
  * [MDEV-31803](https://jira.mariadb.org/browse/MDEV-31803) InnoDB aborts during recovery when immediate\_scrub\_data\_uncompressed is enabled
* [Revision #732d1ec3ae](https://github.com/MariaDB/server/commit/732d1ec3ae)\
  2023-07-27 19:43:45 +0300
  * [MDEV-29873](https://jira.mariadb.org/browse/MDEV-29873) MSAN uninitialized value errors in bcmp / prep\_alter\_part\_table upon re-partitioning by system time
* [Revision #b70d5476b6](https://github.com/MariaDB/server/commit/b70d5476b6)\
  2023-07-27 19:43:45 +0300
  * [MDEV-31244](https://jira.mariadb.org/browse/MDEV-31244) Assertion "not SELECT" in vers\_set\_hist\_part()
* [Revision #4700f2ac70](https://github.com/MariaDB/server/commit/4700f2ac70)\
  2023-07-26 15:52:12 +0530
  * [MDEV-30796](https://jira.mariadb.org/browse/MDEV-30796) Auto\_increment values not updated after bulk insert operation
* Merge [Revision #864bbd4d09](https://github.com/MariaDB/server/commit/864bbd4d09) 2023-07-26 13:42:23 +0300 - Merge 10.6 into 10.9
* [Revision #b9c7da4c91](https://github.com/MariaDB/server/commit/b9c7da4c91)\
  2023-07-20 07:44:05 +0400
  * [MDEV-30003](https://jira.mariadb.org/browse/MDEV-30003) Assertion failure upon 2nd execution of SP trying to set collation on non-existing database
* [Revision #42738f5f4d](https://github.com/MariaDB/server/commit/42738f5f4d)\
  2023-07-17 06:52:18 +0400
  * [MDEV-30681](https://jira.mariadb.org/browse/MDEV-30681) SIGFPE / UBSAN runtime error: division by zero in String::needs\_conversion on ALTER
* [Revision #b27167c6d6](https://github.com/MariaDB/server/commit/b27167c6d6)\
  2023-06-15 13:40:13 +0300
  * Make sure that here is MariaDB client available
* [Revision #fe5957ee92](https://github.com/MariaDB/server/commit/fe5957ee92)\
  2023-05-09 09:01:02 +0300
  * [MDEV-31118](https://jira.mariadb.org/browse/MDEV-31118): Add Lintian overrides for false positives
* [Revision #14eff727c3](https://github.com/MariaDB/server/commit/14eff727c3)\
  2023-05-08 11:09:44 +0300
  * [MDEV-31118](https://jira.mariadb.org/browse/MDEV-31118): Override lintian dh-addon for systemd
* [Revision #3dd3308152](https://github.com/MariaDB/server/commit/3dd3308152)\
  2023-05-08 11:06:52 +0300
  * [MDEV-31118](https://jira.mariadb.org/browse/MDEV-31118): Rework Salsa-CI YAML work again
* [Revision #90cd3b38f6](https://github.com/MariaDB/server/commit/90cd3b38f6)\
  2023-05-08 10:58:17 +0300
  * [MDEV-31118](https://jira.mariadb.org/browse/MDEV-31118): Remove version-substvar-for-external-package problems
* Merge [Revision #7cde5c539b](https://github.com/MariaDB/server/commit/7cde5c539b) 2023-07-10 11:22:21 +0300 - Merge 10.6 into 10.9
* [Revision #c358e216d9](https://github.com/MariaDB/server/commit/c358e216d9)\
  2023-07-10 11:14:54 +0300
  * [MDEV-31642](https://jira.mariadb.org/browse/MDEV-31642): Upgrade may crash if innodb\_log\_file\_buffering=OFF
* [Revision #0df346306a](https://github.com/MariaDB/server/commit/0df346306a)\
  2023-07-06 22:17:35 +0200
  * [MDEV-29959](https://jira.mariadb.org/browse/MDEV-29959) fix for aarch64
* [Revision #1570c6e3e0](https://github.com/MariaDB/server/commit/1570c6e3e0)\
  2023-07-05 21:51:52 +0200
  * bugfix: join a=b where cast(a as type\_of\_b) can produce NULL
* [Revision #ef84f8137b](https://github.com/MariaDB/server/commit/ef84f8137b)\
  2023-05-17 16:14:24 +0200
  * [MDEV-29959](https://jira.mariadb.org/browse/MDEV-29959) UUID Sorting
* [Revision #8bf25f3fb3](https://github.com/MariaDB/server/commit/8bf25f3fb3)\
  2023-05-06 22:11:03 +0200
  * cleanup: remove sql\_type\_uuid.cc
* [Revision #f3bacd708a](https://github.com/MariaDB/server/commit/f3bacd708a)\
  2023-07-05 14:43:46 +0200
  * cleanup: make Name and STRING\_WITH\_LEN usable in constexpr
* Merge [Revision #15a42a0a18](https://github.com/MariaDB/server/commit/15a42a0a18) 2023-07-05 16:45:10 +0300 - Merge 10.6 into 10.9
* Merge [Revision #ecd23f627d](https://github.com/MariaDB/server/commit/ecd23f627d) 2023-07-05 14:08:36 +0300 - Merge 10.6 into 10.9
* [Revision #b1317c178e](https://github.com/MariaDB/server/commit/b1317c178e)\
  2023-07-05 13:54:20 +0300
  * [MDEV-31628](https://jira.mariadb.org/browse/MDEV-31628): InnoDB reports the wrong system tablespace size on bootstrap
* [Revision #35de8326fb](https://github.com/MariaDB/server/commit/35de8326fb)\
  2023-07-03 16:50:01 +0300
  * [MDEV-31311](https://jira.mariadb.org/browse/MDEV-31311): The test innodb.log\_file\_size\_online occasionally hangs
* Merge [Revision #26fc07b162](https://github.com/MariaDB/server/commit/26fc07b162) 2023-07-03 16:49:55 +0300 - Merge 10.6 into 10.9
* Merge [Revision #d04de1aa13](https://github.com/MariaDB/server/commit/d04de1aa13) 2023-06-30 13:42:52 +0300 - Merge 10.6 into 10.9
* [Revision #8e2b20bfb0](https://github.com/MariaDB/server/commit/8e2b20bfb0)\
  2023-06-29 18:34:34 +0700
  * [MDEV-30639](https://jira.mariadb.org/browse/MDEV-30639) Upgrade to 10.8 and later does not work on Windows
* [Revision #cd39f4ab6f](https://github.com/MariaDB/server/commit/cd39f4ab6f)\
  2023-06-28 22:01:16 +0300
  * [MDEV-31573](https://jira.mariadb.org/browse/MDEV-31573): rocksdb.group\_min\_max test fails
* [Revision #73f78fb3b0](https://github.com/MariaDB/server/commit/73f78fb3b0)\
  2023-06-28 15:04:18 +0530
  * [MDEV-31537](https://jira.mariadb.org/browse/MDEV-31537) Bulk insert operation aborts the server for redundant table
* Merge [Revision #eb6b521f1b](https://github.com/MariaDB/server/commit/eb6b521f1b) 2023-06-27 13:48:46 +0300 - Merge 10.6 into 10.9
* [Revision #e1a631fecc](https://github.com/MariaDB/server/commit/e1a631fecc)\
  2023-06-12 20:11:32 +0300
  * Fixed wrong assignment in calculate\_block\_sizes() for MEM\_ROOT
* [Revision #c4cf5e17ac](https://github.com/MariaDB/server/commit/c4cf5e17ac)\
  2023-06-13 20:19:19 +0300
  * Fixed main.mysqld-help and connect.drop-open-error tests
* Merge [Revision #5b37d58306](https://github.com/MariaDB/server/commit/5b37d58306) 2023-06-08 10:46:52 +0300 - Merge mariadb-10.9.7 into 10.9
* Merge [Revision #223c2c5b9d](https://github.com/MariaDB/server/commit/223c2c5b9d) 2023-06-08 10:46:19 +0300 - Merge 10.6 into 10.9
* [Revision #7b3538051c](https://github.com/MariaDB/server/commit/7b3538051c)\
  2023-06-07 08:13:53 -0400
  * bump the VERSION
* Merge [Revision #878a86f276](https://github.com/MariaDB/server/commit/878a86f276) 2023-06-07 14:32:46 +0300 - Merge 10.6 into 10.9
* Merge [Revision #44c9008ba6](https://github.com/MariaDB/server/commit/44c9008ba6) 2023-05-25 11:35:05 +0200 - Merge branch '10.9' into bb-10.9-release
* Merge [Revision #31be25349f](https://github.com/MariaDB/server/commit/31be25349f) 2023-05-25 09:24:32 +0300 - Merge 10.6 into 10.9
* Merge [Revision #0796b7ad5e](https://github.com/MariaDB/server/commit/0796b7ad5e) 2023-05-22 09:13:51 +0300 - Merge 10.6 into 10.9
* [Revision #2f9e264781](https://github.com/MariaDB/server/commit/2f9e264781)\
  2023-05-19 15:15:38 +0300
  * [MDEV-29911](https://jira.mariadb.org/browse/MDEV-29911) InnoDB recovery and mariadb-backup --prepare fail to report detailed progress
* Merge [Revision #2ec42f793d](https://github.com/MariaDB/server/commit/2ec42f793d) 2023-05-19 15:11:06 +0300 - Merge 10.6 into 10.9
* [Revision #3b34454c9d](https://github.com/MariaDB/server/commit/3b34454c9d)\
  2023-04-03 13:34:51 +0530
  * [MDEV-23187](https://jira.mariadb.org/browse/MDEV-23187): Assorted assertion failures in json\_find\_path with certain collations
* Merge [Revision #717e3b3cfd](https://github.com/MariaDB/server/commit/717e3b3cfd) 2023-05-11 14:27:32 +0300 - Merge 10.6 into 10.9
* Merge [Revision #2763f733ee](https://github.com/MariaDB/server/commit/2763f733ee) 2023-05-11 09:24:59 +0300 - Merge 10.8 into 10.9
* Merge [Revision #1f1eaef0af](https://github.com/MariaDB/server/commit/1f1eaef0af) 2023-05-11 09:00:27 +0300 - Merge 10.6 into 10.8
* Merge [Revision #7d44e2e7ff](https://github.com/MariaDB/server/commit/7d44e2e7ff) 2023-05-11 08:59:51 +0300 - Merge mariadb-10.8.8 into 10.8
* [Revision #f288d42cdb](https://github.com/MariaDB/server/commit/f288d42cdb)\
  2023-03-31 01:18:24 +0200
  * [MDEV-29646](https://jira.mariadb.org/browse/MDEV-29646): sformat('Num \[{:20}]', 42) gives incorrect result in view
* Merge [Revision #967e9e1d47](https://github.com/MariaDB/server/commit/967e9e1d47) 2023-05-11 09:07:58 +0300 - Merge mariadb-10.9.6 into 10.9
* [Revision #56aa73a3e3](https://github.com/MariaDB/server/commit/56aa73a3e3)\
  2023-05-10 08:46:44 -0400
  * bump the VERSION
* Merge [Revision #be19f81ad5](https://github.com/MariaDB/server/commit/be19f81ad5) 2023-05-24 09:46:27 +0200 - Merge branch '10.6' into 10.9

{% @marketo/form formid="4316" formId="4316" %}
