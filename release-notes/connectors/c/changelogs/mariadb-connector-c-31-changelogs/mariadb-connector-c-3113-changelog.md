# MariaDB Connector/C 3.1.13 Changelog

The most recent [_**Stable**_](../../../../mariadb-release-criteria.md) _**(GA)**_ release of MariaDB Connector/C is:[**MariaDB Connector/C 3.4.5**](../../mariadb-connector-c-3-4-release-notes/mariadb-connector-c-3-4-5-release-notes.md)

[Download](https://mariadb.com/downloads/#connectors)[Release Notes](../../mariadb-connector-c-31-release-notes/mariadb-connector-c-3113-release-notes.md)[Changelog](mariadb-connector-c-3113-changelog.md)[About MariaDB Connector/C](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-c/README.md)

**Release date:** 11 May 2021

For the highlights of this release, see the[release notes](../../mariadb-connector-c-31-release-notes/mariadb-connector-c-3113-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-c/) you can view more\
details of the revision and view diffs of the code modified in that revision.

* [Revision #180c543](https://github.com/mariadb-corporation/mariadb-connector-c/commit/180c543)\
  2021-05-03 13:58:17 +0200
  * Fix for [CONC-548](https://jira.mariadb.org/browse/CONC-548): Symbol conflict with libsodium
* [Revision #d60bdbe](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d60bdbe)\
  2021-04-29 11:00:45 +0200
  * Merge branch '3.1' of [mariadb-connector-c](https://github.com/mariadb-corporation/mariadb-connector-c) into 3.1
* [Revision #0bd29ba](https://github.com/mariadb-corporation/mariadb-connector-c/commit/0bd29ba)\
  2021-03-23 21:00:42 +0100
  * [MDEV-25232](https://jira.mariadb.org/browse/MDEV-25232) CMake Deprecation Warning Compatibility with CMake < 2.8.12
* [Revision #9244281](https://github.com/mariadb-corporation/mariadb-connector-c/commit/9244281)\
  2021-04-29 10:59:25 +0200
  * Fix for [CONC-490](https://jira.mariadb.org/browse/CONC-490):
* [Revision #701ea94](https://github.com/mariadb-corporation/mariadb-connector-c/commit/701ea94)\
  2021-04-19 12:57:19 +0200
  * Fix for gcc-6
* [Revision #3a6e96d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3a6e96d)\
  2021-04-18 08:12:22 +0200
  * Fix for UBSAN (undefined behaviour checker) build.
* [Revision #d19c7c6](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d19c7c6)\
  2021-04-13 21:34:29 +0200
  * Fix for [CONC-543](https://jira.mariadb.org/browse/CONC-543) (hash functions conflict with GnuTLS)
* [Revision #89d0c4b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/89d0c4b)\
  2021-04-07 19:24:30 +0200
  * remove 10.6 (will require C/C 3.2) from test matrix
* [Revision #2589dd5](https://github.com/mariadb-corporation/mariadb-connector-c/commit/2589dd5)\
  2021-04-07 11:35:12 +0200
  * Travis
* [Revision #13bcf7c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/13bcf7c)\
  2021-04-01 07:15:29 +0200
  * Fix for [CONC-539](https://jira.mariadb.org/browse/CONC-539)
* [Revision #5719e9e](https://github.com/mariadb-corporation/mariadb-connector-c/commit/5719e9e)\
  2021-03-22 10:18:45 +0100
  * Merge branch '3.1' of [mariadb-connector-c](https://github.com/mariadb-corporation/mariadb-connector-c) into 3.1
* [Revision #26c66ae](https://github.com/mariadb-corporation/mariadb-connector-c/commit/26c66ae)\
  2021-03-22 09:38:30 +0100
  * Merge pull request #155 from kamipo/patch-1
* [Revision #b8eed18](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b8eed18)\
  2021-02-21 16:37:09 +0900
  * Fix typo utf8m4 -> utf8mb4
* [Revision #80d9aaa](https://github.com/mariadb-corporation/mariadb-connector-c/commit/80d9aaa)\
  2021-03-22 10:16:13 +0100
  * Fix for [CONC-537](https://jira.mariadb.org/browse/CONC-537): Only read from MYSQL\_HOME if MARIADB\_HOME is not set
* [Revision #d272377](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d272377)\
  2021-03-22 09:28:46 +0100
  * Fix for [CONC-535](https://jira.mariadb.org/browse/CONC-535): disabled checksum ignored in events
* [Revision #fca3048](https://github.com/mariadb-corporation/mariadb-connector-c/commit/fca3048)\
  2021-03-15 10:40:50 +0100
  * Update server versions for appveyor
* [Revision #c23ecca](https://github.com/mariadb-corporation/mariadb-connector-c/commit/c23ecca)\
  2021-03-15 07:18:43 +0100
  * Fix for [CONC-475](https://jira.mariadb.org/browse/CONC-475):
* [Revision #5649764](https://github.com/mariadb-corporation/mariadb-connector-c/commit/5649764)\
  2021-03-14 11:53:28 +0100
  * Disable failing tests when running against MaxScale.
* [Revision #fc431a0](https://github.com/mariadb-corporation/mariadb-connector-c/commit/fc431a0)\
  2021-03-12 00:29:16 +0100
  * Support MSVC ASAN
* [Revision #8cf925f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/8cf925f)\
  2021-03-12 00:02:08 +0100
  * Workaround a CMake bug with Ninja generator.
* [Revision #242cab8](https://github.com/mariadb-corporation/mariadb-connector-c/commit/242cab8)\
  2021-03-12 00:01:11 +0100
  * Fix syntax error in cmake 3.20
* [Revision #15471ce](https://github.com/mariadb-corporation/mariadb-connector-c/commit/15471ce)\
  2021-02-17 06:02:09 +0100
  * Bump version number (3.1.13)
