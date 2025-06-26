# MariaDB 10.7.7 Changelog

The most recent release of [MariaDB 10.7](../../old-releases/release-notes-mariadb-10-7-series/what-is-mariadb-107.md) is:[**MariaDB 10.7.8**](../../old-releases/release-notes-mariadb-10-7-series/mariadb-10-7-8-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.7.8/)

[Download 10.7.7](https://downloads.mariadb.org/mariadb/10.7.7/)[Release Notes](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-7-series)[Changelog](mariadb-10-7-7-changelog.md)[Overview of 10.7](../../old-releases/release-notes-mariadb-10-7-series/what-is-mariadb-107.md)

**Release date:** 7 Nov 2022

For the highlights of this release, see the [Release Notes](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-7-series).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/server/tree/10.7) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Includes all fixes from [MariaDB 10.6.11](../changelogs-mariadb-106-series/mariadb-10-6-11-changelog.md)
* Merge [Revision #5e196a7b73](https://github.com/MariaDB/server/commit/5e196a7b73) 2022-11-03 11:28:41 +0100 - Merge branch '10.6' into 10.7
* Merge [Revision #2e2173a359](https://github.com/MariaDB/server/commit/2e2173a359) 2022-11-02 19:47:23 +0100 - Merge branch '10.6' into 10.7
* [Revision #b798944a93](https://github.com/MariaDB/server/commit/b798944a93)\
  2022-11-02 19:01:11 +0100
  * update colunmstore
* [Revision #6449af6f2d](https://github.com/MariaDB/server/commit/6449af6f2d)\
  2022-10-31 17:47:22 +0100
  * fix results after merge
* [Revision #d23ad3664b](https://github.com/MariaDB/server/commit/d23ad3664b)\
  2022-10-31 16:14:26 +0900
  * Revert "[MDEV-27233](https://jira.mariadb.org/browse/MDEV-27233) Server hangs when using --init-file which loads Spider and creates a Spider table"
* Merge [Revision #1ebfa2af62](https://github.com/MariaDB/server/commit/1ebfa2af62) 2022-10-29 19:22:04 +0200 - Merge branch '10.6' into 10.7
* [Revision #dd9da61dcf](https://github.com/MariaDB/server/commit/dd9da61dcf)\
  2022-10-25 12:14:09 +0530
  * [MDEV-29761](https://jira.mariadb.org/browse/MDEV-29761) Bulk insert fails to rollback during insert..select
* [Revision #2e3d08ef51](https://github.com/MariaDB/server/commit/2e3d08ef51)\
  2022-10-24 16:16:02 +0200
  * [MDEV-28701](https://jira.mariadb.org/browse/MDEV-28701) Update 10.7 HELP tables
* Merge [Revision #e80acbbe91](https://github.com/MariaDB/server/commit/e80acbbe91) 2022-10-25 16:02:57 +1100 - Merge branch 10.6 into 10.7
* [Revision #c160a115b8](https://github.com/MariaDB/server/commit/c160a115b8)\
  2022-04-25 18:29:01 +0900
  * [MDEV-27233](https://jira.mariadb.org/browse/MDEV-27233) Server hangs when using --init-file which loads Spider and creates a Spider table
* [Revision #e967e81089](https://github.com/MariaDB/server/commit/e967e81089)\
  2022-01-18 12:14:25 +0400
  * [MDEV-27233](https://jira.mariadb.org/browse/MDEV-27233) Fixes to make SQL SERVICE working
* [Revision #3905c12b09](https://github.com/MariaDB/server/commit/3905c12b09)\
  2022-10-20 20:41:44 +0200
  * [MDEV-29031](https://jira.mariadb.org/browse/MDEV-29031) Change maturity of plugins for October 2022 Releases
* [Revision #120a4caf37](https://github.com/MariaDB/server/commit/120a4caf37)\
  2022-10-19 03:28:03 +0300
  * [MDEV-27963](https://jira.mariadb.org/browse/MDEV-27963) multisource\_for\_channel sometimes fails in bb with result content mismatch
* Merge [Revision #ec2b30e736](https://github.com/MariaDB/server/commit/ec2b30e736) 2022-10-16 21:40:33 +0200 - Merge branch '10.6' into 10.7
* Merge [Revision #8a9e17103b](https://github.com/MariaDB/server/commit/8a9e17103b) 2022-10-16 21:40:08 +0200 - Merge branch 'bb-10.7-vp-[MDEV-27691](https://jira.mariadb.org/browse/MDEV-27691)' into 10.7
* [Revision #cee61e37b9](https://github.com/MariaDB/server/commit/cee61e37b9)\
  2022-09-27 17:47:12 +0700
  * [MDEV-27691](https://jira.mariadb.org/browse/MDEV-27691): make working view-protocol
* Merge [Revision #410a07277f](https://github.com/MariaDB/server/commit/410a07277f) 2022-09-27 14:59:07 +0700 - Merge branch 'bb-10.6-all-builders' into bb-10.7-all-builders
* Merge [Revision #588efca237](https://github.com/MariaDB/server/commit/588efca237) 2022-10-13 10:05:29 +0300 - Merge 10.6 into 10.7
* Merge [Revision #b6ebadaa66](https://github.com/MariaDB/server/commit/b6ebadaa66) 2022-10-04 07:41:35 +0200 - Merge branch '10.6' into 10.7
* [Revision #7d4b2b9847](https://github.com/MariaDB/server/commit/7d4b2b9847)\
  2022-09-28 18:41:00 +0530
  * [MDEV-29570](https://jira.mariadb.org/browse/MDEV-29570) InnoDB fails to clean bulk buffer when server does rollback operation
* Merge [Revision #7c7ac6d4a4](https://github.com/MariaDB/server/commit/7c7ac6d4a4) 2022-09-21 09:33:07 +0300 - Merge 10.6 into 10.7
* [Revision #b73c70c265](https://github.com/MariaDB/server/commit/b73c70c265)\
  2022-09-19 10:02:09 -0400
  * bump the VERSION

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
