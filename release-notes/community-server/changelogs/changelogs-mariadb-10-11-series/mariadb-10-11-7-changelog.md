# MariaDB 10.11.7 Changelog

{% include "../../../../.gitbook/includes/latest-10.11 (2).md" %}

<a href="https://downloads.mariadb.org/mariadb/10.11.7/" class="button primary">Download</a> <a href="../../mariadb-10-11-series/mariadb-10-11-7-release-notes.md" class="button secondary">Release Notes</a> <a href="mariadb-10-11-7-changelog.md" class="button secondary">Changelog</a> <a href="../../mariadb-10-11-series/what-is-mariadb-1011.md" class="button secondary">Overview of 10.11</a>

**Release date:** 7 Feb 2024

For the highlights of this release, see the [release notes](../../mariadb-10-11-series/mariadb-10-11-7-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On [GitHub](https://github.com/MariaDB/server/tree/10.11) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Includes all fixes from [MariaDB 10.6.17](../changelogs-mariadb-106-series/mariadb-10-6-17-changelog.md)
* Merge [Revision #87e13722a9](https://github.com/MariaDB/server/commit/87e13722a9) 2024-02-01 18:36:14 +0100 - Merge branch '10.6' into 10.11
* [Revision #b5c367cd88](https://github.com/MariaDB/server/commit/b5c367cd88)\
  2024-02-01 16:15:02 +0100
  * [MDEV-32815](https://jira.mariadb.org/browse/MDEV-32815) test main.func\_sformat Locale + test failures under Fedora 39 (fmt-10.0.0+)
* [Revision #dd95c58b58](https://github.com/MariaDB/server/commit/dd95c58b58)\
  2024-01-30 21:50:13 +0100
  * [MDEV-33331](https://jira.mariadb.org/browse/MDEV-33331): IO Thread Relay Log Inconsistent Statistics After [MDEV-32551](https://jira.mariadb.org/browse/MDEV-32551)
* [Revision #8c5db7a187](https://github.com/MariaDB/server/commit/8c5db7a187)\
  2024-01-12 17:34:19 +0100
  * [MDEV-29587](https://jira.mariadb.org/browse/MDEV-29587) Allowing insert into a view with columns that are not part the table
* [Revision #bc2f155019](https://github.com/MariaDB/server/commit/bc2f155019)\
  2024-01-22 11:38:26 +1100
  * Deb autobake: ready with noble (Ubuntu 24.04)
* [Revision #1acf6a0f84](https://github.com/MariaDB/server/commit/1acf6a0f84)\
  2024-01-22 12:42:37 +0200
  * [MDEV-14425](https://jira.mariadb.org/browse/MDEV-14425) fixup: mariadb-backup.huge\_lsn,strict\_crc32 rdiff
* [Revision #0335629eb3](https://github.com/MariaDB/server/commit/0335629eb3)\
  2024-01-22 11:31:22 +0200
  * [MDEV-32242](https://jira.mariadb.org/browse/MDEV-32242) fixup: innodb.doublewrite test may be skipped again
* [Revision #7f11fad85a](https://github.com/MariaDB/server/commit/7f11fad85a)\
  2024-01-22 10:04:11 +0200
  * [MDEV-32968](https://jira.mariadb.org/browse/MDEV-32968): After-merge fix
* Merge [Revision #b3ca7fa089](https://github.com/MariaDB/server/commit/b3ca7fa089) 2024-01-22 08:49:04 +0200 - Merge 10.6 into 10.11
* Merge [Revision #9d20853c74](https://github.com/MariaDB/server/commit/9d20853c74) 2024-01-18 19:22:23 +0200 - Merge 10.6 into 10.11
* [Revision #03854a84ab](https://github.com/MariaDB/server/commit/03854a84ab)\
  2024-01-17 22:26:12 +0100
  * [MDEV-32374](https://jira.mariadb.org/browse/MDEV-32374) Improve lsn\_lock. Also use futex-like on Windows
* Merge [Revision #ad13fb36bf](https://github.com/MariaDB/server/commit/ad13fb36bf) 2024-01-17 17:37:15 +0200 - Merge 10.6 into 10.11
* [Revision #78ea9ee4f2](https://github.com/MariaDB/server/commit/78ea9ee4f2)\
  2024-01-12 16:03:41 +0100
  * [MDEV-33187](https://jira.mariadb.org/browse/MDEV-33187): mariadb-hotcopy fails for sys
* [Revision #7702e481df](https://github.com/MariaDB/server/commit/7702e481df)\
  2024-01-12 16:02:02 +0100
  * [MDEV-30259](https://jira.mariadb.org/browse/MDEV-30259): mariadb-hotcopy fails for performance\_schema
* [Revision #82f27ea5a4](https://github.com/MariaDB/server/commit/82f27ea5a4)\
  2024-01-11 12:54:16 +0100
  * [MDEV-33187](https://jira.mariadb.org/browse/MDEV-33187): Make mariadb-hotcopy compatible with DBI:MariaDB
* [Revision #d0c80c211c](https://github.com/MariaDB/server/commit/d0c80c211c)\
  2024-01-08 11:58:29 -0500
  * [MDEV-32090](https://jira.mariadb.org/browse/MDEV-32090) Test for null-safe equals in join
* [Revision #338ed5c42e](https://github.com/MariaDB/server/commit/338ed5c42e)\
  2024-01-10 12:37:50 +0200
  * [MDEV-26195](https://jira.mariadb.org/browse/MDEV-26195) fixup: Remove page\_no\_t
* Merge [Revision #1eb11da3e5](https://github.com/MariaDB/server/commit/1eb11da3e5) 2024-01-10 12:37:19 +0200 - Merge 10.6 into 10.11
* Merge [Revision #bdf65893dd](https://github.com/MariaDB/server/commit/bdf65893dd) 2024-01-03 15:37:57 +0200 - Merge 10.6 into 10.11
* Merge [Revision #09049fe496](https://github.com/MariaDB/server/commit/09049fe496) 2023-12-22 14:57:05 +1100 - Merge branch '10.6' into 10.11
* Merge [Revision #2b8dc7668a](https://github.com/MariaDB/server/commit/2b8dc7668a) 2023-12-21 13:19:17 +0200 - Merge 10.6 into 10.11
* [Revision #ea0937d42a](https://github.com/MariaDB/server/commit/ea0937d42a)\
  2023-12-21 12:52:31 +0200
  * [MDEV-30172](https://jira.mariadb.org/browse/MDEV-30172): Tolerate CR\_SSL\_CONNECTION\_ERROR in Galera tests
* [Revision #138cd311b4](https://github.com/MariaDB/server/commit/138cd311b4)\
  2023-12-21 11:57:21 +0200
  * Galera after-merge fix
* [Revision #af69506de4](https://github.com/MariaDB/server/commit/af69506de4)\
  2023-12-04 11:21:58 +0200
  * Merge fixup encryption.corrupted\_during\_recovery
* [Revision #c8d52c895d](https://github.com/MariaDB/server/commit/c8d52c895d)\
  2023-12-21 09:49:40 +1100
  * [MDEV-24670](https://jira.mariadb.org/browse/MDEV-24670) memory pressure - warnings/notes
* Merge [Revision #2b99e5f7ef](https://github.com/MariaDB/server/commit/2b99e5f7ef) 2023-12-20 15:58:36 +0200 - Merge 10.6 into 10.11
* [Revision #9d2c3d388e](https://github.com/MariaDB/server/commit/9d2c3d388e)\
  2023-12-20 09:48:36 +1100
  * [MDEV-24670](https://jira.mariadb.org/browse/MDEV-24670) memory pressure - warnings/notes
* [Revision #a057a6e41f](https://github.com/MariaDB/server/commit/a057a6e41f)\
  2023-12-20 09:21:27 +1100
  * [MDEV-24670](https://jira.mariadb.org/browse/MDEV-24670) memory pressure - mariadb-backup postfix
* [Revision #25c627885a](https://github.com/MariaDB/server/commit/25c627885a)\
  2023-12-18 23:05:58 +0100
  * hashicorp plugin: any 404 from the vault means "no key found"
* [Revision #eb37a76659](https://github.com/MariaDB/server/commit/eb37a76659)\
  2023-12-18 22:13:23 +0100
  * fix test failures with ASAN
* [Revision #11ae6c9af1](https://github.com/MariaDB/server/commit/11ae6c9af1)\
  2023-12-18 17:42:50 +0100
  * InnoDB: downgrade a warning to a note
* [Revision #07a0173f1c](https://github.com/MariaDB/server/commit/07a0173f1c)\
  2023-12-18 17:37:30 +0100
  * perfschema: LOCK\_all\_status\_vars not LOCK\_status
* Merge [Revision #fd0b47f9d6](https://github.com/MariaDB/server/commit/fd0b47f9d6) 2023-12-17 16:56:38 +0100 - Merge branch '10.6' into 10.11
* [Revision #9a7deb1c36](https://github.com/MariaDB/server/commit/9a7deb1c36)\
  2023-10-31 22:09:31 +0100
  * [MDEV-32542](https://jira.mariadb.org/browse/MDEV-32542) plugins.compression - multiple buildbot failures
* [Revision #7fae2fa460](https://github.com/MariaDB/server/commit/7fae2fa460)\
  2023-10-08 00:41:48 +0300
  * [MDEV-30482](https://jira.mariadb.org/browse/MDEV-30482) libmariadb3 - debian/libmariadb3.symbols not updated
* [Revision #a016b18a58](https://github.com/MariaDB/server/commit/a016b18a58)\
  2023-12-11 14:29:04 +0100
  * [MDEV-27849](https://jira.mariadb.org/browse/MDEV-27849): rpl.rpl\_start\_alter\_XXX fail sporadically in buildbot
* [Revision #917a7386bf](https://github.com/MariaDB/server/commit/917a7386bf)\
  2023-11-16 12:46:30 +0100
  * [MDEV-32819](https://jira.mariadb.org/browse/MDEV-32819): main.show\_explain failed in buildbot
* [Revision #d018b90990](https://github.com/MariaDB/server/commit/d018b90990)\
  2023-12-06 20:57:23 +0530
  * [MDEV-32920](https://jira.mariadb.org/browse/MDEV-32920) innodb\_buffer\_pool\_read\_requests always 0
* [Revision #31ffa7441c](https://github.com/MariaDB/server/commit/31ffa7441c)\
  2023-12-04 09:38:29 +0200
  * Fix GCC -Wunused-variable
* [Revision #9d07b0520c](https://github.com/MariaDB/server/commit/9d07b0520c)\
  2023-10-06 22:36:32 +0200
  * [MDEV-31608](https://jira.mariadb.org/browse/MDEV-31608) - Connector/NET fails to connect since 10.10
* Merge [Revision #6d0bcfc4b9](https://github.com/MariaDB/server/commit/6d0bcfc4b9) 2023-11-30 13:03:59 +0200 - Merge 10.6 into 10.11
* Merge [Revision #3e90efe4c9](https://github.com/MariaDB/server/commit/3e90efe4c9) 2023-11-24 14:37:21 +0200 - Merge 10.6 into 10.11
* [Revision #a48c1b89c8](https://github.com/MariaDB/server/commit/a48c1b89c8)\
  2023-11-23 13:03:01 +1100
  * [MDEV-24670](https://jira.mariadb.org/browse/MDEV-24670) memory pressure - eventfd rather than pipe
* Merge [Revision #f2bd662f6c](https://github.com/MariaDB/server/commit/f2bd662f6c) 2023-11-22 18:14:11 +0200 - Merge 10.6 into 10.11
* [Revision #7443ad1c8a](https://github.com/MariaDB/server/commit/7443ad1c8a)\
  2023-11-21 14:38:35 +0200
  * [MDEV-32374](https://jira.mariadb.org/browse/MDEV-32374) log\_sys.lsn\_lock is a performance hog
* Merge [Revision #f87c7d1772](https://github.com/MariaDB/server/commit/f87c7d1772) 2023-11-21 12:47:51 +0200 - Merge 10.6 into 10.11
* [Revision #804b5974f5](https://github.com/MariaDB/server/commit/804b5974f5)\
  2023-11-14 19:22:56 +0530
  * [MDEV-32050](https://jira.mariadb.org/browse/MDEV-32050) Fixup
* Merge [Revision #583a745299](https://github.com/MariaDB/server/commit/583a745299) 2023-11-21 10:23:11 +0200 - Merge 10.6 into 10.11
* [Revision #45fadb64c1](https://github.com/MariaDB/server/commit/45fadb64c1)\
  2023-11-14 12:13:04 +1100
  * [MDEV-32753](https://jira.mariadb.org/browse/MDEV-32753) Make spider init queries compatible with oracle sql mode
* [Revision #3ba041f9f5](https://github.com/MariaDB/server/commit/3ba041f9f5)\
  2023-11-20 13:44:47 +0200
  * [MDEV-31953](https://jira.mariadb.org/browse/MDEV-31953) fixup: Clean up the test
* Merge [Revision #90d968dab9](https://github.com/MariaDB/server/commit/90d968dab9) 2023-11-20 10:08:19 +0200 - Merge 10.6 into 10.11
* [Revision #2323483528](https://github.com/MariaDB/server/commit/2323483528)\
  2023-10-24 09:47:46 +0300
  * [MDEV-31953](https://jira.mariadb.org/browse/MDEV-31953) madvise(..., MADV\_FREE) is causing a performance regression
* [Revision #6c34245963](https://github.com/MariaDB/server/commit/6c34245963)\
  2023-11-16 14:41:25 +0530
  * [MDEV-32811](https://jira.mariadb.org/browse/MDEV-32811) Potentially broken crash recovery if a mini-transaction frees a page, not modifying previously clean pages
* [Revision #ae0afad56f](https://github.com/MariaDB/server/commit/ae0afad56f)\
  2023-11-14 14:21:41 +0200
  * [MDEV-32746](https://jira.mariadb.org/browse/MDEV-32746) SIGSEGV on recovery when using innodb\_encrypt\_log and PMEM
* Merge [Revision #e6f56e3978](https://github.com/MariaDB/server/commit/e6f56e3978) 2023-11-14 09:18:56 +0100 - Merge branch '10.11' into mariadb-10.11.6
* [Revision #ecce948ad7](https://github.com/MariaDB/server/commit/ecce948ad7)\
  2023-11-13 14:39:41 -0500
  * bump the VERSION

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
