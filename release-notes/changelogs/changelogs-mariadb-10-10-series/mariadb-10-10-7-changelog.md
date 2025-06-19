# MariaDB 10.10.7 Changelog

[Download](https://mariadb.com/downloads/)[Release Notes](../../mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-10-series/mariadb-10-10-7-release-notes.md)[Changelog](mariadb-10-10-7-changelog.md)[Overview of 10.10](../../mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-10-series/what-is-mariadb-1010.md)

[_Alternate download from mariadb.org_](https://downloads.mariadb.org/mariadb/10.10.7/)

**Release date:** 13 Nov 2023

For the highlights of this release, see the[release notes](../../mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-10-series/mariadb-10-10-7-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/server/tree/10.10) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Includes all fixes from [MariaDB 10.9.8](../changelogs-mariadb-109-series/mariadb-10-9-8-changelog.md)
* Includes all fixes from [MariaDB 10.6.16](../changelogs-mariadb-106-series/mariadb-10-6-16-changelog.md)
* Merge [Revision #04d9a46c41](https://github.com/MariaDB/server/commit/04d9a46c41) 2023-11-08 16:22:42 +0100 - Merge branch '10.6' into 10.10
* [Revision #21822625aa](https://github.com/MariaDB/server/commit/21822625aa)\
  2023-11-07 11:00:49 +0100
  * [MDEV-32683](https://jira.mariadb.org/browse/MDEV-32683) Spider engine does not load with non-default alter-algorithm
* [Revision #d9752d85a3](https://github.com/MariaDB/server/commit/d9752d85a3)\
  2023-10-28 23:13:06 +0200
  * [MDEV-31926](https://jira.mariadb.org/browse/MDEV-31926) UUID v7 are compared incorrectly
* [Revision #5436b5ddd7](https://github.com/MariaDB/server/commit/5436b5ddd7)\
  2023-10-28 14:43:10 +0200
  * cleanup: UUID
* [Revision #b9e210bbf3](https://github.com/MariaDB/server/commit/b9e210bbf3)\
  2023-10-24 23:50:26 +0200
  * [MDEV-32555](https://jira.mariadb.org/browse/MDEV-32555) wrong result with an index and a partially null-rejecting condition
* [Revision #d2a867cdf0](https://github.com/MariaDB/server/commit/d2a867cdf0)\
  2023-10-23 20:24:24 +0300
  * [MDEV-32532](https://jira.mariadb.org/browse/MDEV-32532) Assertion failure in ddl\_log\_increment\_phase\_no\_lock upon ..
* [Revision #0b2fd01ed0](https://github.com/MariaDB/server/commit/0b2fd01ed0)\
  2023-10-17 15:02:12 +1100
  * [MDEV-32485](https://jira.mariadb.org/browse/MDEV-32485) Fix Spider upgrade failure caused by duplication in mysql.func
* [Revision #15a1168b36](https://github.com/MariaDB/server/commit/15a1168b36)\
  2023-10-19 12:15:39 +1100
  * [MDEV-32507](https://jira.mariadb.org/browse/MDEV-32507) Spider: Use $MTR\_SUITE\_DIR for init-file files
* Merge [Revision #5a8fca5a4f](https://github.com/MariaDB/server/commit/5a8fca5a4f) 2023-10-23 18:43:36 +0300 - Merge 10.6 into 10.10
* [Revision #057fd52876](https://github.com/MariaDB/server/commit/057fd52876)\
  2023-10-20 10:28:34 +1100
  * [MDEV-32515](https://jira.mariadb.org/browse/MDEV-32515) Use $MYSQLD\_LAST\_CMD in spider/bugfix.mdev\_30370
* Merge [Revision #c92d06748a](https://github.com/MariaDB/server/commit/c92d06748a) 2023-10-19 14:35:31 +0300 - Merge 10.6 into 10.10
* Merge [Revision #c857259ebb](https://github.com/MariaDB/server/commit/c857259ebb) 2023-10-18 16:38:09 +0300 - Merge 10.6 into 10.10
* [Revision #a49ebf71af](https://github.com/MariaDB/server/commit/a49ebf71af)\
  2023-10-16 17:14:24 +0300
  * Fixed memory leak when using histograms
* Merge [Revision #0563106b1a](https://github.com/MariaDB/server/commit/0563106b1a) 2023-10-17 13:02:57 +0300 - Merge 10.6 into 10.10
* [Revision #8f9059422e](https://github.com/MariaDB/server/commit/8f9059422e)\
  2023-10-17 15:28:16 +1100
  * \[fixup] Spider fixup after merge
* [Revision #515f8de243](https://github.com/MariaDB/server/commit/515f8de243)\
  2023-10-17 12:22:13 +1100
  * Spider: update reason for disabling spider/bugfix.mdev\_27239
* Merge [Revision #d5e15424d8](https://github.com/MariaDB/server/commit/d5e15424d8) 2023-10-13 15:14:37 +0300 - Merge 10.6 into 10.10
* [Revision #3b38c2f358](https://github.com/MariaDB/server/commit/3b38c2f358)\
  2023-09-19 11:33:51 +1000
  * [MDEV-18200](https://jira.mariadb.org/browse/MDEV-18200) mariadb-backup full backup failed with InnoDB: Failing assertion: success
* [Revision #c72ddeea4f](https://github.com/MariaDB/server/commit/c72ddeea4f)\
  2023-10-11 12:22:33 +0300
  * [MDEV-32364](https://jira.mariadb.org/browse/MDEV-32364) Server crashes when starting server with high innodb\_log\_buffer\_size
* [Revision #50784c8869](https://github.com/MariaDB/server/commit/50784c8869)\
  2023-09-25 15:46:59 +1000
  * [MDEV-32238](https://jira.mariadb.org/browse/MDEV-32238) Adding a switch to disable the spider group by handler
* [Revision #05c99435a7](https://github.com/MariaDB/server/commit/05c99435a7)\
  2023-10-05 15:24:49 +0300
  * [MDEV-31014](https://jira.mariadb.org/browse/MDEV-31014) Database privileges are insufficient for CONVERT TABLE TO PARTITION
* [Revision #ef14d6d6a4](https://github.com/MariaDB/server/commit/ef14d6d6a4)\
  2023-10-06 10:12:57 +1100
  * [MDEV-32046](https://jira.mariadb.org/browse/MDEV-32046) Adding ER\_NET\_READ\_ERROR to spider/bugfix.mdev\_27240
* [Revision #a60cf9c7ae](https://github.com/MariaDB/server/commit/a60cf9c7ae)\
  2023-10-05 16:19:10 +1100
  * [MDEV-22979](https://jira.mariadb.org/browse/MDEV-22979) [MDEV-27233](https://jira.mariadb.org/browse/MDEV-27233) [MDEV-28218](https://jira.mariadb.org/browse/MDEV-28218) Fixing spider init bugs
* [Revision #c6ba81d6bf](https://github.com/MariaDB/server/commit/c6ba81d6bf)\
  2023-04-20 13:07:43 +1000
  * [MDEV-27095](https://jira.mariadb.org/browse/MDEV-27095) clean up spd\_init\_query.h
* [Revision #fc2548c862](https://github.com/MariaDB/server/commit/fc2548c862)\
  2023-04-20 11:02:43 +1000
  * [MDEV-27095](https://jira.mariadb.org/browse/MDEV-27095) installing one spider plugin should not trigger others
* [Revision #213b916aea](https://github.com/MariaDB/server/commit/213b916aea)\
  2023-10-02 15:30:33 +0530
  * [MDEV-32291](https://jira.mariadb.org/browse/MDEV-32291) memory leak in innodb.insert\_into\_empty test
* [Revision #11c69177e9](https://github.com/MariaDB/server/commit/11c69177e9)\
  2023-09-24 19:32:04 +0200
  * fix galera.galera\_as\_slave\_gtid\_myisam for 10.10+
* [Revision #0b6de3d1ce](https://github.com/MariaDB/server/commit/0b6de3d1ce)\
  2023-08-29 11:24:16 +0200
  * avoid "'sh' is not recognized..." error in mtr on windows
* [Revision #cb384d0d04](https://github.com/MariaDB/server/commit/cb384d0d04)\
  2023-08-29 10:37:08 +0530
  * [MDEV-32008](https://jira.mariadb.org/browse/MDEV-32008) auto\_increment value on table increments by one after restart
* [Revision #cd5808eb8d](https://github.com/MariaDB/server/commit/cd5808eb8d)\
  2023-08-20 19:43:57 +0800
  * [MDEV-31963](https://jira.mariadb.org/browse/MDEV-31963) Fix libfmt usage in SFORMAT
* [Revision #f4cec369a3](https://github.com/MariaDB/server/commit/f4cec369a3)\
  2023-08-19 22:48:16 +0800
  * [MDEV-31963](https://jira.mariadb.org/browse/MDEV-31963) cmake: fix libfmt usage
* [Revision #bf3b787e02](https://github.com/MariaDB/server/commit/bf3b787e02)\
  2023-08-25 17:25:47 +0530
  * [MDEV-31835](https://jira.mariadb.org/browse/MDEV-31835) Remove unnecessary extra HA\_EXTRA\_IGNORE\_INSERT call
* [Revision #afc64eacc9](https://github.com/MariaDB/server/commit/afc64eacc9)\
  2023-08-18 07:42:06 +0400
  * [MDEV-31719](https://jira.mariadb.org/browse/MDEV-31719) Wrong result of: WHERE inet6\_column IN ('','::1')
* [Revision #8aaacb5509](https://github.com/MariaDB/server/commit/8aaacb5509)\
  2023-08-14 11:09:51 +0300
  * [MDEV-31432](https://jira.mariadb.org/browse/MDEV-31432) tmp\_table field accessed after free
* Merge [Revision #9cd2989589](https://github.com/MariaDB/server/commit/9cd2989589) 2023-08-16 15:28:42 +0300 - Merge 10.6 into 10.10
* Merge [Revision #17f5f1cba9](https://github.com/MariaDB/server/commit/17f5f1cba9) 2023-08-15 11:22:36 +0300 - Merge 10.6 into 10.10
* Merge [Revision #5bbe21182e](https://github.com/MariaDB/server/commit/5bbe21182e) 2023-08-15 11:15:03 +0300 - Merge mariadb-10.10.6 into 10.10
* [Revision #19a2456f07](https://github.com/MariaDB/server/commit/19a2456f07)\
  2023-08-14 13:48:05 -0400
  * bump the VERSION

{% @marketo/form formid="4316" formId="4316" %}
