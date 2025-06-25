# MariaDB 10.8.8 Changelog

[Download](https://mariadb.com/downloads/)[Release Notes](../../old-releases/release-notes-mariadb-10-8-series/mariadb-10-8-8-release-notes.md)[Changelog](mariadb-10-8-8-changelog.md)[Overview of 10.8](../../old-releases/release-notes-mariadb-10-8-series/what-is-mariadb-108.md)

[_Alternate download from mariadb.org_](https://downloads.mariadb.org/mariadb/10.8.8/)

**Release date:** 10 May 2023

For the highlights of this release, see the[release notes](../../old-releases/release-notes-mariadb-10-8-series/mariadb-10-8-8-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/server/tree/10.8) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Includes all fixes from [MariaDB 10.7.8](../changelogs-mariadb-10-7-series/mariadb-10-7-8-changelog.md)
* Includes all fixes from [MariaDB 10.6.13](../changelogs-mariadb-106-series/mariadb-10-6-13-changelog.md)
* Merge [Revision #2668d596d1](https://github.com/MariaDB/server/commit/2668d596d1) 2023-05-05 13:35:13 +0200 - Merge branch '10.6' into 10.8
* Merge [Revision #5f5f743d56](https://github.com/MariaDB/server/commit/5f5f743d56) 2023-05-05 11:14:33 +0200 - Merge branch '10.6' into 10.8
* Merge [Revision #4ccc310d0e](https://github.com/MariaDB/server/commit/4ccc310d0e) 2023-05-04 19:13:56 +0200 - Merge branch '10.6' into 10.8
* Merge [Revision #85997115c2](https://github.com/MariaDB/server/commit/85997115c2) 2023-05-04 11:34:11 +0200 - Merge branch '10.6' into 10.8
* Merge [Revision #f0f1f2de0e](https://github.com/MariaDB/server/commit/f0f1f2de0e) 2023-05-03 11:33:57 +0200 - Merge branch '10.6' into 10.8
* [Revision #7d967423fe](https://github.com/MariaDB/server/commit/7d967423fe)\
  2023-04-28 12:15:45 +0300
  * [MDEV-31147](https://jira.mariadb.org/browse/MDEV-31147) json\_normalize does not work correctly with MSAN build
* Merge [Revision #5028b7c7c8](https://github.com/MariaDB/server/commit/5028b7c7c8) 2023-04-27 17:14:36 +0300 - Merge 10.6 into 10.8
* Merge [Revision #bbd261bb2e](https://github.com/MariaDB/server/commit/bbd261bb2e) 2023-04-27 09:53:56 +0300 - Merge 10.6 into 10.8
* Merge [Revision #c15c8ef3e3](https://github.com/MariaDB/server/commit/c15c8ef3e3) 2023-04-26 13:58:40 +0300 - Merge 10.6 into 10.8
* Merge [Revision #3c25077899](https://github.com/MariaDB/server/commit/3c25077899) 2023-04-24 15:59:23 +0300 - Merge 10.6 into 10.8
* Merge [Revision #10147af9e5](https://github.com/MariaDB/server/commit/10147af9e5) 2023-04-14 09:48:22 +0300 - Merge 10.6 into 10.8
* Merge [Revision #e552747cfd](https://github.com/MariaDB/server/commit/e552747cfd) 2023-04-13 15:52:46 +0300 - Merge 10.6 into 10.8
* Merge [Revision #8bd5cf01f9](https://github.com/MariaDB/server/commit/8bd5cf01f9) 2023-04-13 09:59:41 +0300 - Merge 10.6 into 10.8
* Merge [Revision #1d1e0ab2cc](https://github.com/MariaDB/server/commit/1d1e0ab2cc) 2023-04-12 15:50:08 +0300 - Merge 10.6 into 10.8
* [Revision #a1ba06f2a7](https://github.com/MariaDB/server/commit/a1ba06f2a7)\
  2023-04-12 13:05:48 +0300
  * [MDEV-27774](https://jira.mariadb.org/browse/MDEV-27774) fixup: Remove an unused function
* Merge [Revision #dd2fe81122](https://github.com/MariaDB/server/commit/dd2fe81122) 2023-03-29 15:16:42 +0300 - Merge 10.6 into 10.8
* Merge [Revision #e4b83f0feb](https://github.com/MariaDB/server/commit/e4b83f0feb) 2023-03-20 10:33:04 +0200 - Merge 10.6 into 10.8
* Merge [Revision #fa56adff75](https://github.com/MariaDB/server/commit/fa56adff75) 2023-03-17 14:19:17 +0200 - Merge 10.6 into 10.8
* Merge [Revision #acf46b7b36](https://github.com/MariaDB/server/commit/acf46b7b36) 2023-03-16 18:11:37 +0200 - Merge 10.6 into 10.8
* [Revision #e97560eac0](https://github.com/MariaDB/server/commit/e97560eac0)\
  2023-01-30 19:42:27 -0800
  * [MDEV-28958](https://jira.mariadb.org/browse/MDEV-28958) Crash when checking whether condition can be pushed into view
* [Revision #20d2c9038a](https://github.com/MariaDB/server/commit/20d2c9038a)\
  2023-02-08 19:49:47 +0000
  * Fix mini-benchmark
* [Revision #2458badf9b](https://github.com/MariaDB/server/commit/2458badf9b)\
  2023-03-07 13:00:59 +0530
  * [MDEV-30798](https://jira.mariadb.org/browse/MDEV-30798) deadlock between CHECK TABLE and bulk insert
* [Revision #062ba0bd4a](https://github.com/MariaDB/server/commit/062ba0bd4a)\
  2023-03-03 19:05:44 +0530
  * [MDEV-30183](https://jira.mariadb.org/browse/MDEV-30183) Assertion \`!memcmp(rec\_trx\_id, old\_pk\_trx\_id->data, 6 + 7)' failed in row\_log\_table\_apply\_update
* Merge [Revision #669a0c6efb](https://github.com/MariaDB/server/commit/669a0c6efb) 2023-03-06 13:37:12 +0200 - Merge 10.6 into 10.8
* [Revision #550b8d76b3](https://github.com/MariaDB/server/commit/550b8d76b3)\
  2023-02-28 20:19:06 +0530
  * [MDEV-30752](https://jira.mariadb.org/browse/MDEV-30752) Assertion \`!index->is\_ibuf()' failed around cmp\_dtuple\_rec\_with\_match\_bytes
* Merge [Revision #6ac44ac3ab](https://github.com/MariaDB/server/commit/6ac44ac3ab) 2023-02-28 10:36:17 +0200 - Merge 10.6 into 10.8
* [Revision #b62123e0d5](https://github.com/MariaDB/server/commit/b62123e0d5)\
  2023-02-23 22:19:26 +0400
  * [MDEV-30716](https://jira.mariadb.org/browse/MDEV-30716) Wrong casefolding in xxx\_unicode\_520\_ci for U+0700..U+07FF
* Merge [Revision #b12cd88ce1](https://github.com/MariaDB/server/commit/b12cd88ce1) 2023-02-16 10:24:23 +0200 - Merge 10.6 into 10.8
* [Revision #34f0433c09](https://github.com/MariaDB/server/commit/34f0433c09)\
  2023-02-16 09:17:40 +0200
  * [MDEV-27774](https://jira.mariadb.org/browse/MDEV-27774) fixup: Correct a comment
* Merge [Revision #5abbe092e6](https://github.com/MariaDB/server/commit/5abbe092e6) 2023-02-16 09:17:06 +0200 - Merge 10.6 into 10.8
* [Revision #951d81d92e](https://github.com/MariaDB/server/commit/951d81d92e)\
  2023-02-14 15:43:33 +0530
  * [MDEV-30426](https://jira.mariadb.org/browse/MDEV-30426) Assertion !rec\_offs\_nth\_extern(offsets2, n) during bulk insert
* [Revision #c7fba948e1](https://github.com/MariaDB/server/commit/c7fba948e1)\
  2023-02-10 14:44:45 +0200
  * Fix RPL tests post DEBUG\_SYNC change
* Merge [Revision #dbab3e8d90](https://github.com/MariaDB/server/commit/dbab3e8d90) 2023-02-10 13:43:53 +0200 - Merge 10.6 into 10.8
* Merge [Revision #29cd17e8d9](https://github.com/MariaDB/server/commit/29cd17e8d9) 2023-02-06 20:46:33 +0100 - Merge branch '10.8.7' into 10.8
* [Revision #d3b84ef458](https://github.com/MariaDB/server/commit/d3b84ef458)\
  2023-02-06 10:49:10 -0500
  * bump the VERSION

{% include "https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/~/reusable/vX1KAy0t1XuYJaGsK28T/" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
