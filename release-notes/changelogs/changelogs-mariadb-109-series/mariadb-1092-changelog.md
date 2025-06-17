# MariaDB 10.9.2 Changelog

The most recent release of [MariaDB 10.8](../../mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-8-series/what-is-mariadb-108.md) is:[**MariaDB 10.8.8**](../../mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-8-series/mariadb-10-8-8-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.8.8/)

[Download 10.9.2](https://downloads.mariadb.org/mariadb/10.9.2/)[Release Notes](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/changelogs/changelogs-mariadb-109-series/broken-reference/README.md)[Changelog](mariadb-1092-changelog.md)[Overview of 10.9](../../mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-9-series/what-is-mariadb-109.md)

**Release date:** 22 Aug 2022

For the highlights of this release, see the[release notes](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/changelogs/changelogs-mariadb-109-series/broken-reference/README.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/server/tree/10.9) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Includes all fixes from [MariaDB 10.8.4](../changelogs-mariadb-10-8-series/mariadb-1084-changelog.md)
* Merge [Revision #10ed52767d](https://github.com/MariaDB/server/commit/10ed52767d) 2022-08-10 13:57:24 +0200 - Merge branch '10.8' into 10.9
* Merge [Revision #d59674be83](https://github.com/MariaDB/server/commit/d59674be83) 2022-08-09 14:24:40 +0200 - Merge branch '10.8' into 10.9
* [Revision #15426e5b3d](https://github.com/MariaDB/server/commit/15426e5b3d)\
  2022-08-09 13:26:57 +0200
  * Version maturity fix.
* Merge [Revision #22d455612b](https://github.com/MariaDB/server/commit/22d455612b) 2022-08-09 09:57:13 +0200 - Merge branch '10.8' into 10.9
* [Revision #bfdc4ff22e](https://github.com/MariaDB/server/commit/bfdc4ff22e)\
  2022-07-29 16:17:09 +0530
  * [MDEV-28762](https://jira.mariadb.org/browse/MDEV-28762): recursive call of some json functions without stack control
* Merge [Revision #f53f64b7b9](https://github.com/MariaDB/server/commit/f53f64b7b9) 2022-07-28 10:47:33 +0300 - Merge 10.8 into 10.9
* [Revision #d8c2eeeb59](https://github.com/MariaDB/server/commit/d8c2eeeb59)\
  2022-06-21 19:10:11 +0530
  * [MDEV-28762](https://jira.mariadb.org/browse/MDEV-28762): recursive call of some json functions without stack control
* [Revision #5ad14ab272](https://github.com/MariaDB/server/commit/5ad14ab272)\
  2022-06-21 19:10:11 +0530
  * [MDEV-28762](https://jira.mariadb.org/browse/MDEV-28762): recursive call of some json functions without stack control
* [Revision #a5dc76a051](https://github.com/MariaDB/server/commit/a5dc76a051)\
  2022-02-03 01:24:14 +0100
  * [MDEV-27142](https://jira.mariadb.org/browse/MDEV-27142) - fix Connect engine reliance on textmode stdio on Windows...
* [Revision #016dd21371](https://github.com/MariaDB/server/commit/016dd21371)\
  2022-02-02 01:58:09 +0100
  * [MDEV-27142](https://jira.mariadb.org/browse/MDEV-27142) disable text mode for Windows stdio by default
* [Revision #8ee93b9cb4](https://github.com/MariaDB/server/commit/8ee93b9cb4)\
  2022-07-14 18:20:10 +0300
  * [MDEV-29060](https://jira.mariadb.org/browse/MDEV-29060) fix ps protocol
* [Revision #fe3adde250](https://github.com/MariaDB/server/commit/fe3adde250)\
  2022-07-08 19:54:46 +0300
  * [MDEV-29060](https://jira.mariadb.org/browse/MDEV-29060) main.view\_debug fix
* [Revision #2b9fb342cf](https://github.com/MariaDB/server/commit/2b9fb342cf)\
  2022-07-05 12:55:10 +0300
  * [MDEV-28978](https://jira.mariadb.org/browse/MDEV-28978) Assertion failure in THD::binlog\_query or unexpected ER\_ERROR\_ON\_WRITE with auto-partitioning
* [Revision #f88511647a](https://github.com/MariaDB/server/commit/f88511647a)\
  2022-06-29 22:53:29 +0300
  * [MDEV-28567](https://jira.mariadb.org/browse/MDEV-28567) Assertion \`0' in open\_tables upon function-related operation
* Merge [Revision #4a164364d7](https://github.com/MariaDB/server/commit/4a164364d7) 2022-06-29 16:22:22 +0300 - Merge 10.8 into 10.9
* [Revision #6e61369bb3](https://github.com/MariaDB/server/commit/6e61369bb3)\
  2022-06-28 11:27:49 +0200
  * [MDEV-28656](https://jira.mariadb.org/browse/MDEV-28656): post-merge fixes
* Merge [Revision #404d4820af](https://github.com/MariaDB/server/commit/404d4820af) 2022-06-28 10:59:01 +0300 - Merge 10.8 into 10.9
* Merge [Revision #b81460f07e](https://github.com/MariaDB/server/commit/b81460f07e) 2022-06-23 13:47:22 +0300 - Merge 10.8 into 10.9
* Merge [Revision #f421d8f50d](https://github.com/MariaDB/server/commit/f421d8f50d) 2022-06-22 15:41:24 +0300 - Merge 10.8 into 10.9
* Merge [Revision #707f2aa214](https://github.com/MariaDB/server/commit/707f2aa214) 2022-06-21 18:21:07 +0300 - Merge 10.8 into 10.9
* [Revision #3aabda7e18](https://github.com/MariaDB/server/commit/3aabda7e18)\
  2022-06-20 16:37:49 +0200
  * [MDEV-28819](https://jira.mariadb.org/browse/MDEV-28819) Statically compiled encryption plugins do not work
* Merge [Revision #70fffc7090](https://github.com/MariaDB/server/commit/70fffc7090) 2022-06-20 10:18:19 +0300 - Merge 10.8 into 10.9
* [Revision #a9fe646797](https://github.com/MariaDB/server/commit/a9fe646797)\
  2022-06-17 18:07:13 -0400
  * Fix building the Hashicorp plugin on OpenBSD / NetBSD and DragonFlyBSD
* Merge [Revision #20b8e5a07e](https://github.com/MariaDB/server/commit/20b8e5a07e) 2022-06-17 11:31:21 +0300 - Merge 10.8 into 10.9
* [Revision #152921174d](https://github.com/MariaDB/server/commit/152921174d)\
  2022-06-15 22:13:13 +0200
  * fix sporadic versioning.rpl\_row failures
* [Revision #f50c130eee](https://github.com/MariaDB/server/commit/f50c130eee)\
  2022-06-15 21:52:29 +0200
  * fixes for aarch64 deb
* [Revision #d5922c71ac](https://github.com/MariaDB/server/commit/d5922c71ac)\
  2022-06-13 23:43:58 +0200
  * deb: fix hashicorp plugin dependencies
* [Revision #a923d6f49c](https://github.com/MariaDB/server/commit/a923d6f49c)\
  2022-06-16 10:38:35 +0400
  * [MDEV-28769](https://jira.mariadb.org/browse/MDEV-28769) Assertion \`(m\_ci->state & 32) || m\_with\_collate' failed in Lex\_exact\_charset\_opt\_extended\_collate::Lex\_exact\_charset\_opt\_extended\_collate on SET NAMES
* Merge [Revision #9fe784ff7e](https://github.com/MariaDB/server/commit/9fe784ff7e) 2022-06-15 10:01:51 +0300 - Merge 10.8 into 10.9
* [Revision #f929fa45b6](https://github.com/MariaDB/server/commit/f929fa45b6)\
  2022-06-13 12:34:18 +0300
  * Make BUILD script compile hashicorp plugin dynamically
* Merge [Revision #6dea701e0f](https://github.com/MariaDB/server/commit/6dea701e0f) 2022-06-09 14:53:34 +0300 - Merge 10.8 into 10.9
* [Revision #e74858c8a8](https://github.com/MariaDB/server/commit/e74858c8a8)\
  2022-06-08 15:05:31 +0000
  * [MCOL-5114](https://jira.mariadb.org/browse/MCOL-5114) Removing ctor specialization b/c it violates c++20 syntax needed in ColumnStorew
* [Revision #8c4a2c8ad4](https://github.com/MariaDB/server/commit/8c4a2c8ad4)\
  2022-05-25 19:28:22 +0900
  * [MDEV-26282](https://jira.mariadb.org/browse/MDEV-26282) Make the version of Spider the same as the server version
* Merge [Revision #5a33a37682](https://github.com/MariaDB/server/commit/5a33a37682) 2022-06-07 09:20:07 +0300 - Merge 10.8 into 10.9
* [Revision #cd1de25912](https://github.com/MariaDB/server/commit/cd1de25912)\
  2022-06-06 17:55:01 +0400
  * [MDEV-27906](https://jira.mariadb.org/browse/MDEV-27906) CREATE TABLE/DATABASE .. CHARSET .. COLLATE is not consistent on errors
* [Revision #0e8342d47e](https://github.com/MariaDB/server/commit/0e8342d47e)\
  2022-06-03 21:53:36 +0900
  * [MDEV-27648](https://jira.mariadb.org/browse/MDEV-27648) fixup: delete unused member of st\_spider\_transaction
* [Revision #c910fdc8ce](https://github.com/MariaDB/server/commit/c910fdc8ce)\
  2022-06-03 15:21:47 +0400
  * [MDEV-28117](https://jira.mariadb.org/browse/MDEV-28117) Multiple conflicting table COLLATE clauses are not rejected
* [Revision #6ec17142dc](https://github.com/MariaDB/server/commit/6ec17142dc)\
  2022-02-27 04:28:27 +0100
  * Fix the FSF address to match the current one in: [gpl-2.0.txt](https://www.gnu.org/licenses/old-licenses/gpl-2.0.txt)
* [Revision #e9adc3959e](https://github.com/MariaDB/server/commit/e9adc3959e)\
  2022-05-25 11:07:04 +0400
  * A cleanup for [MDEV-27896](https://jira.mariadb.org/browse/MDEV-27896) Wrong result upon `COLLATE latin1_bin CHARACTER SET latin1` on the table or the database level
* Merge [Revision #1ace1075dc](https://github.com/MariaDB/server/commit/1ace1075dc) 2022-05-25 08:52:21 +0300 - Merge 10.8 into 10.9
* [Revision #208addf484](https://github.com/MariaDB/server/commit/208addf484)\
  2022-05-17 12:52:23 +0400
  * Main patch [MDEV-27896](https://jira.mariadb.org/browse/MDEV-27896) Wrong result upon `COLLATE latin1_bin CHARACTER SET latin1` on the table or the database level
* [Revision #89adedcb9f](https://github.com/MariaDB/server/commit/89adedcb9f)\
  2022-05-23 11:05:33 +0400
  * Step#3 [MDEV-27896](https://jira.mariadb.org/browse/MDEV-27896) Wrong result upon `COLLATE latin1_bin CHARACTER SET latin1` on the table or the database level
* [Revision #e7f635e2d2](https://github.com/MariaDB/server/commit/e7f635e2d2)\
  2022-05-23 08:40:26 +0400
  * Step#2 [MDEV-27896](https://jira.mariadb.org/browse/MDEV-27896) Wrong result upon `COLLATE latin1_bin CHARACTER SET latin1` on the table or the database level
* [Revision #64a5fab00e](https://github.com/MariaDB/server/commit/64a5fab00e)\
  2022-05-22 21:25:31 +0400
  * Step#1 [MDEV-27896](https://jira.mariadb.org/browse/MDEV-27896) Wrong result upon `COLLATE latin1_bin CHARACTER SET latin1` on the table or the database level
* Merge [Revision #92702430c2](https://github.com/MariaDB/server/commit/92702430c2) 2022-05-20 21:54:21 +0200 - Merge branch '10.9' into bb-10.9-release
* [Revision #e33a3868dc](https://github.com/MariaDB/server/commit/e33a3868dc)\
  2022-05-20 13:46:34 -0400
  * bump the VERSION
* [Revision #441c26da22](https://github.com/MariaDB/server/commit/441c26da22)\
  2022-05-17 16:02:48 +0300
  * [MDEV-27328](https://jira.mariadb.org/browse/MDEV-27328) MSAN failure fix

{% @marketo/form formid="4316" formId="4316" %}
