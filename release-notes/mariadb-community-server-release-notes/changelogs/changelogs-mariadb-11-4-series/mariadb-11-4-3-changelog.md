# MariaDB 11.4.3 Changelog

{% include "../../../.gitbook/includes/latest-11-4.md" %}

<a href="https://downloads.mariadb.org/mariadb/11.4.3/" class="button primary">Download</a> <a href="../../mariadb-11-4-series/mariadb-11-4-3-release-notes.md" class="button secondary">Release Notes</a> <a href="mariadb-11-4-3-changelog.md" class="button secondary">Changelog</a> <a href="../../mariadb-11-4-series/what-is-mariadb-114.md" class="button secondary">Overview of 11.4</a>

**Release date:** 8 Aug 2024

For the highlights of this release, see the [release notes](../../mariadb-11-4-series/mariadb-11-4-3-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On [GitHub](https://github.com/MariaDB/server/tree/11.4) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Includes all fixes from [MariaDB 11.3.2](../changelogs-mariadb-11-3-series/mariadb-11-3-2-changelog.md)
* Includes all fixes from [MariaDB 11.2.5](../changelogs-mariadb-11-2-series/mariadb-11-2-5-changelog.md)
* [Revision #5ab81ffe00](https://github.com/MariaDB/server/commit/5ab81ffe00)\
  2024-08-05 10:39:50 +0200
  * fix plugins.rpl\_auth failure in bintars
* [Revision #1787164cdd](https://github.com/MariaDB/server/commit/1787164cdd)\
  2024-08-04 17:18:30 +0200
  * fix plugins.rpl\_auth failure on Debian
* [Revision #66f14ef6a1](https://github.com/MariaDB/server/commit/66f14ef6a1)\
  2024-08-01 10:04:19 +0200
  * update C/C 3.4
* [Revision #6f357feaf0](https://github.com/MariaDB/server/commit/6f357feaf0)\
  2024-08-01 09:01:46 +0200
  * suppress rocksdb warning
* Merge [Revision #1640c9b06e](https://github.com/MariaDB/server/commit/1640c9b06e) 2024-08-04 11:04:39 +0200 - Merge branch '11.2' into 11.4
* [Revision #2ee061c258](https://github.com/MariaDB/server/commit/2ee061c258)\
  2024-07-16 14:41:56 +0200
  * Add missing options to the mariadb-dump man page
* [Revision #c9284ae6d1](https://github.com/MariaDB/server/commit/c9284ae6d1)\
  2024-07-09 17:51:25 +0530
  * [MDEV-34552](https://jira.mariadb.org/browse/MDEV-34552) innodb.temp\_tablespace\_freed fails with ER\_WRONG\_ARGUMENTS
* [Revision #0437ac3ae0](https://github.com/MariaDB/server/commit/0437ac3ae0)\
  2024-07-11 13:52:14 +0300
  * Added supporession of server restart message to events.events\_restart
* [Revision #e0cff1e72b](https://github.com/MariaDB/server/commit/e0cff1e72b)\
  2024-07-11 11:12:41 +0300
  * Fixed failure in rpl.rpl\_change\_master\_demote : "IO thread should not be running..."
* [Revision #dd99780967](https://github.com/MariaDB/server/commit/dd99780967)\
  2024-07-09 10:56:06 +0300
  * [MDEV-34504](https://jira.mariadb.org/browse/MDEV-34504) PURGE BINARY LOGS not working anymore
* Merge [Revision #5fb07d942b](https://github.com/MariaDB/server/commit/5fb07d942b) 2024-07-09 17:41:26 +0400 - Merge remote-tracking branch 'origin/11.2' into 11.4
* [Revision #4ffeca643d](https://github.com/MariaDB/server/commit/4ffeca643d)\
  2024-06-03 13:56:59 +0400
  * Renaming a few mysql-test/suite/rpl/include/\*.test files into \*.inc
* [Revision #14d9801cd3](https://github.com/MariaDB/server/commit/14d9801cd3)\
  2024-06-21 15:55:38 +0200
  * fix [MDEV-34424](https://jira.mariadb.org/browse/MDEV-34424) for ed255129
* Merge [Revision #c4bf4ce948](https://github.com/MariaDB/server/commit/c4bf4ce948) 2024-06-17 14:53:54 +0400 - Merge remote-tracking branch 'origin/11.2' into 11.4
* [Revision #c9414ccd67](https://github.com/MariaDB/server/commit/c9414ccd67)\
  2024-06-13 10:51:24 +0200
  * Move debug dependent [MDEV-32441](https://jira.mariadb.org/browse/MDEV-32441) test in separate file
* [Revision #69c07f70a1](https://github.com/MariaDB/server/commit/69c07f70a1)\
  2024-06-13 10:31:28 +0200
  * Fix [MDEV-32441](https://jira.mariadb.org/browse/MDEV-32441) stability
* [Revision #1849dfef64](https://github.com/MariaDB/server/commit/1849dfef64)\
  2024-05-29 13:10:15 +0530
  * [MDEV-34256](https://jira.mariadb.org/browse/MDEV-34256) InnoDB throws out of bound write due to temporary tablespace truncation
* Merge [Revision #457948707d](https://github.com/MariaDB/server/commit/457948707d) 2024-05-29 14:07:53 -0400 - Merge branch 'bb-11.4-bumpversion' of github.com:MariaDB/server into bb-11.4-bumpversion
* Merge [Revision #708510494b](https://github.com/MariaDB/server/commit/708510494b) 2024-02-17 17:18:13 -0500 - Merge branch 'bb-11.4-bumpversion' of github.com:MariaDB/server into bb-11.4-bumpversion
* [Revision #485975ab98](https://github.com/MariaDB/server/commit/485975ab98)\
  2024-02-16 16:40:32 -0500
  * bump the VERSION
* [Revision #1173883dc5](https://github.com/MariaDB/server/commit/1173883dc5)\
  2024-05-29 14:07:14 -0400
  * bump the VERSION
* [Revision #aa04bba47b](https://github.com/MariaDB/server/commit/aa04bba47b)\
  2024-05-27 22:03:52 +0200
  * Fix appveyor build with newer OpenSSL.
* [Revision #8e980acb9e](https://github.com/MariaDB/server/commit/8e980acb9e)\
  2024-05-27 15:06:39 +0200
  * Appveyor - use latest available OpenSSL on appveyor (currently 3.2)

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
