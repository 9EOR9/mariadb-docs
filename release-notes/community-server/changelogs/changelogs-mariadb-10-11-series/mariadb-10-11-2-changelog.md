# MariaDB 10.11.2 Changelog

<a href="https://downloads.mariadb.org/mariadb/10.11.2/" class="button primary">Download</a> <a href="../../mariadb-10-11-series/mariadb-10-11-2-release-notes.md" class="button secondary">Release Notes</a> <a href="mariadb-10-11-2-changelog.md" class="button secondary">Changelog</a> <a href="../../mariadb-10-11-series/what-is-mariadb-1011.md" class="button secondary">Overview of 10.11</a>

**Release date:** 16 Feb 2023

For the highlights of this release, see the [release notes](../../mariadb-10-11-series/mariadb-10-11-2-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On [GitHub](https://github.com/MariaDB/server/tree/10.11) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Includes all fixes from [MariaDB 10.10.3](../changelogs-mariadb-10-10-series/mariadb-10-10-3-changelog.md)
* Merge [Revision #cafba8761a](https://github.com/MariaDB/server/commit/cafba8761a) 2023-02-01 18:28:03 +0100 - Merge branch '10.10' into 10.11
* Merge [Revision #c7c415734d](https://github.com/MariaDB/server/commit/c7c415734d) 2023-01-31 11:07:08 +0100 - Merge branch '10.10' into 10.11
* Merge [Revision #10635c2833](https://github.com/MariaDB/server/commit/10635c2833) 2023-01-24 15:17:39 +0200 - Merge 10.10 into 10.11
* [Revision #f4e023ae7f](https://github.com/MariaDB/server/commit/f4e023ae7f)\
  2023-01-20 19:31:41 +0100
  * Change maturity
* Merge [Revision #66bd8cd6c3](https://github.com/MariaDB/server/commit/66bd8cd6c3) 2023-01-18 16:58:28 +0100 - Merge branch '10.10' into 10.11
* Merge [Revision #bb3a63903e](https://github.com/MariaDB/server/commit/bb3a63903e) 2023-01-13 12:22:30 +0200 - Merge 10.10 into 10.11
* [Revision #f879ee9ca0](https://github.com/MariaDB/server/commit/f879ee9ca0)\
  2023-01-11 00:25:01 +1100
  * deb: add lunar
* Merge [Revision #3a237f7666](https://github.com/MariaDB/server/commit/3a237f7666) 2023-01-11 11:13:56 +0200 - Merge 10.10 into 10.11
* [Revision #70be59913c](https://github.com/MariaDB/server/commit/70be59913c)\
  2022-11-26 18:19:35 -0800
  * Deb: Misc fixes for 10.11 series
* [Revision #cfaf47a4d4](https://github.com/MariaDB/server/commit/cfaf47a4d4)\
  2023-01-03 13:38:55 +1100
  * acl - is\_public - avoid embedded warning
* [Revision #22491e627a](https://github.com/MariaDB/server/commit/22491e627a)\
  2022-12-07 14:59:06 +0100
  * [MDEV-30154](https://jira.mariadb.org/browse/MDEV-30154): Assertion \`strcasecmp(rolename, public\_name.str) || acl\_public == role' failed in acl\_update\_role on GRANT ... TO PUBLIC
* [Revision #a5be6c91cb](https://github.com/MariaDB/server/commit/a5be6c91cb)\
  2022-10-27 09:09:39 +1100
  * [MDEV-29889](https://jira.mariadb.org/browse/MDEV-29889) mariadb-dump --tab --header is slow
* Merge [Revision #c194db34d9](https://github.com/MariaDB/server/commit/c194db34d9) 2022-12-16 11:36:10 +0200 - Merge 10.10 into 10.11
* Merge [Revision #802e26c347](https://github.com/MariaDB/server/commit/802e26c347) 2022-12-15 10:32:58 +1100 - Merge branch '10.10' into 10.11
* [Revision #c1fd082e9c](https://github.com/MariaDB/server/commit/c1fd082e9c)\
  2022-12-14 13:34:11 +0100
  * [MDEV-25341](https://jira.mariadb.org/browse/MDEV-25341) post-fix. Don't use DiscardVirtualMemory on Windows.
* Merge [Revision #0aca3012a1](https://github.com/MariaDB/server/commit/0aca3012a1) 2022-12-14 09:18:30 +0200 - Merge 10.10 into 10.11
* Merge [Revision #12786f0e77](https://github.com/MariaDB/server/commit/12786f0e77) 2022-12-12 08:10:25 +0200 - Merge 10.10 into 10.11
* Merge [Revision #64071d30bd](https://github.com/MariaDB/server/commit/64071d30bd) 2022-12-07 10:00:52 +0200 - Merge 10.10 into 10.11
* [Revision #922f7ba75c](https://github.com/MariaDB/server/commit/922f7ba75c)\
  2022-12-05 16:25:27 +0530
  * [MDEV-30158](https://jira.mariadb.org/browse/MDEV-30158) InnoDB fails to start ther server 10.11 when innodb\_undo\_tablespaces mismatch
* Merge [Revision #b81b194393](https://github.com/MariaDB/server/commit/b81b194393) 2022-11-30 12:59:57 +0200 - Merge 10.10 into 10.11
* [Revision #b18241e059](https://github.com/MariaDB/server/commit/b18241e059)\
  2022-11-29 16:23:46 +0530
  * [MDEV-30122](https://jira.mariadb.org/browse/MDEV-30122) mariadb-backup.skip\_innodb crashes when innodb\_undo\_tablespaces > 0
* Merge [Revision #936436ef43](https://github.com/MariaDB/server/commit/936436ef43) 2022-11-28 13:44:42 +0200 - Merge 10.10 into 10.11
* Merge [Revision #71dedd0ebc](https://github.com/MariaDB/server/commit/71dedd0ebc) 2022-11-24 08:40:16 +0200 - Merge 10.10 into 10.11
* Merge [Revision #7933367a27](https://github.com/MariaDB/server/commit/7933367a27) 2022-11-21 10:51:10 +0200 - Merge 10.10 into 10.11
* [Revision #8283948846](https://github.com/MariaDB/server/commit/8283948846)\
  2022-11-16 10:27:25 -0500
  * bump the VERSION

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
