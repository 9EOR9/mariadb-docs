# MariaDB 10.10.2 Changelog

The most recent release of [MariaDB 10.10](../../old-releases/release-notes-mariadb-10-10-series/what-is-mariadb-1010.md) is:[**MariaDB 10.10.7**](../../old-releases/release-notes-mariadb-10-10-series/mariadb-10-10-7-release-notes.md) **Stable (GA)** [Download Now](https://downloads.mariadb.org/mariadb/10.10.7)

[Download 10.10.2](https://downloads.mariadb.org/mariadb/10.10.2/)[Release Notes](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-10-series/mariadb-10-10-2-release-notes)[Changelog](mariadb-10-10-2-changelog.md)[Overview of 10.10](../../old-releases/release-notes-mariadb-10-10-series/what-is-mariadb-1010.md)

**Release date:** 17 Nov 2022

For the highlights of this release, see the[release notes](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-10-series).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/server/tree/10.10) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Includes all fixes from [MariaDB 10.9.4](../changelogs-mariadb-109-series/mariadb-10-9-4-changelog.md)
* [Revision #695f20f1b5](https://github.com/MariaDB/server/commit/695f20f1b5)\
  2022-11-14 19:09:06 +0100
  * [MDEV-30007](https://jira.mariadb.org/browse/MDEV-30007) SIGSEGV in st\_select\_lex\_unit::is\_derived\_eliminated, runtime error: member access within null pointer of type 'struct TABLE' in st\_select\_lex\_unit::is\_derived\_eliminated()
* [Revision #dc37828042](https://github.com/MariaDB/server/commit/dc37828042)\
  2022-11-12 22:52:58 +0100
  * [MDEV-29947](https://jira.mariadb.org/browse/MDEV-29947) Spider doesn't return all rows when doing a join of two tables with no usable keys
* Merge [Revision #f8997c68fe](https://github.com/MariaDB/server/commit/f8997c68fe) 2022-11-03 11:47:10 +0100 - Merge branch '10.9' into 10.10
* Merge [Revision #49a22c5897](https://github.com/MariaDB/server/commit/49a22c5897) 2022-11-01 10:42:22 +0100 - Merge branch '10.9' into 10.10
* [Revision #8e6a64194b](https://github.com/MariaDB/server/commit/8e6a64194b)\
  2022-10-06 00:45:47 +0200
  * [MDEV-29463](https://jira.mariadb.org/browse/MDEV-29463) mysqlimport occasionally fails to fail in main.mysqldump
* [Revision #648bedf0e5](https://github.com/MariaDB/server/commit/648bedf0e5)\
  2022-10-17 16:16:23 +0200
  * change to stable version
* Merge [Revision #1d7e4301cc](https://github.com/MariaDB/server/commit/1d7e4301cc) 2022-10-17 16:15:40 +0200 - Merge branch '10.9' into 10.10
* Merge [Revision #2665fe4556](https://github.com/MariaDB/server/commit/2665fe4556) 2022-10-17 16:13:46 +0200 - Merge branch 'bb-10.10-vp-[MDEV-27691](https://jira.mariadb.org/browse/MDEV-27691)' into 10.10
* [Revision #7be65b4b6b](https://github.com/MariaDB/server/commit/7be65b4b6b)\
  2022-09-28 13:53:08 +0700
  * [MDEV-27691](https://jira.mariadb.org/browse/MDEV-27691): make working view-protocol
* Merge [Revision #f9bf41632e](https://github.com/MariaDB/server/commit/f9bf41632e) 2022-09-28 09:40:17 +0700 - Merge branch 'bb-10.9-all-builders' into bb-10.10-all-builders
* [Revision #14703a4f0f](https://github.com/MariaDB/server/commit/14703a4f0f)\
  2022-10-12 14:43:53 +0400
  * [MDEV-29776](https://jira.mariadb.org/browse/MDEV-29776) collation\_connection and db\_collation are too short in mysql.proc and mysql.event
* Merge [Revision #d66f6f0cb4](https://github.com/MariaDB/server/commit/d66f6f0cb4) 2022-10-13 10:57:21 +0300 - Merge 10.9 into 10.10
* [Revision #095655365e](https://github.com/MariaDB/server/commit/095655365e)\
  2022-10-06 12:07:01 +0200
  * Speed up mysql\_upgrade test on Windows by not using SSL
* Merge [Revision #bb76dcbec7](https://github.com/MariaDB/server/commit/bb76dcbec7) 2022-10-04 13:32:38 +0200 - Merge branch '10.9' into 10.10
* [Revision #1ac8149b83](https://github.com/MariaDB/server/commit/1ac8149b83)\
  2022-09-23 14:37:58 +0200
  * [MDEV-29608](https://jira.mariadb.org/browse/MDEV-29608) Default SSL makes mysqlslap much slower, tests fail with timeout
* [Revision #530d19a320](https://github.com/MariaDB/server/commit/530d19a320)\
  2022-09-29 22:38:14 +0200
  * after merge update \*.result
* [Revision #9bf5274929](https://github.com/MariaDB/server/commit/9bf5274929)\
  2022-09-12 11:53:21 -0400
  * [MDEV-29517](https://jira.mariadb.org/browse/MDEV-29517): rpl.rpl\_change\_master\_demote sporadically fails in BB
* Merge [Revision #5e996fbad9](https://github.com/MariaDB/server/commit/5e996fbad9) 2022-09-21 10:59:56 +0300 - Merge 10.9 into 10.10
* [Revision #5deccac4aa](https://github.com/MariaDB/server/commit/5deccac4aa)\
  2022-09-13 16:59:27 +0200
  * galera tests fail with "TLS/SSL error: Success (0)"
* Merge [Revision #4f03edf4a2](https://github.com/MariaDB/server/commit/4f03edf4a2) 2022-09-13 20:59:40 +0300 - Merge 10.9 into 10.10
* Merge [Revision #c08d404f5a](https://github.com/MariaDB/server/commit/c08d404f5a) 2022-09-09 20:10:23 +0900 - Merge 10.9 into 10.10
* Merge [Revision #6978bcbf37](https://github.com/MariaDB/server/commit/6978bcbf37) 2022-09-07 10:14:06 +0300 - Merge 10.9 into 10.10
* Merge [Revision #c0a6ce61d8](https://github.com/MariaDB/server/commit/c0a6ce61d8) 2022-09-06 10:51:18 +0300 - Merge 10.9 into 10.10
* [Revision #f6118acda9](https://github.com/MariaDB/server/commit/f6118acda9)\
  2022-09-02 13:23:24 +0400
  * A follow-up patch [MDEV-27266](https://jira.mariadb.org/browse/MDEV-27266) Improve UCA collation performance for utf8mb3 and utf8mb4
* Merge [Revision #e71aca8200](https://github.com/MariaDB/server/commit/e71aca8200) 2022-08-30 13:33:02 +0300 - Merge 10.9 into 10.10
* Merge [Revision #259050f864](https://github.com/MariaDB/server/commit/259050f864) 2022-08-29 14:04:25 +0300 - Merge 10.9 into 10.10
* [Revision #87e8463e04](https://github.com/MariaDB/server/commit/87e8463e04)\
  2022-08-16 09:26:27 -0700
  * Fixed some compiler issues appeared after d7ffb7c3dd95c4c5e36f75b09662faafa0fb1ecd
* Merge [Revision #63e3fc0bb7](https://github.com/MariaDB/server/commit/63e3fc0bb7) 2022-08-15 13:48:51 +0200 - Merge branch '10.10' into bb-10.10-release
* [Revision #9542aeee7d](https://github.com/MariaDB/server/commit/9542aeee7d)\
  2022-08-15 02:50:10 -0400
  * bump the VERSION

{% include "https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/~/reusable/vX1KAy0t1XuYJaGsK28T/" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
