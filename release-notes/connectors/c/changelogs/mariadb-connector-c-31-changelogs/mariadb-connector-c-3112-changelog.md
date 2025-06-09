# MariaDB Connector/C 3.1.12 Changelog

The most recent [_**Stable**_](../../../../mariadb-release-criteria.md) _**(GA)**_ release of MariaDB Connector/C is:[**MariaDB Connector/C 3.4.5**](../../mariadb-connector-c-3-4-release-notes/mariadb-connector-c-3-4-5-release-notes.md)

[Download](https://mariadb.com/downloads/#connectors)[Release Notes](../../mariadb-connector-c-31-release-notes/mariadb-connector-c-3112-release-notes.md)[Changelog](mariadb-connector-c-3112-changelog.md)[About MariaDB Connector/C](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-c/README.md)

**Release date:** 23 Feb 2021

For the highlights of this release, see the[release notes](../../mariadb-connector-c-31-release-notes/mariadb-connector-c-3112-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-c/) you can view more\
details of the revision and view diffs of the code modified in that revision.

* [Revision #7d304d2](https://github.com/mariadb-corporation/mariadb-connector-c/commit/7d304d2)\
  2021-02-11 19:28:56 +0100
  * [CONC-526](https://jira.mariadb.org/browse/CONC-526): Replace images for Windows installer
* [Revision #67cd96f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/67cd96f)\
  2021-02-09 20:27:52 +0100
  * Revert "[CONC-142](https://jira.mariadb.org/browse/CONC-142): Fix memory leak in connection"
* [Revision #63a207e](https://github.com/mariadb-corporation/mariadb-connector-c/commit/63a207e)\
  2021-02-09 20:25:55 +0100
  * [CONC-142](https://jira.mariadb.org/browse/CONC-142): Fix memory leak in connection
* [Revision #e62ff46](https://github.com/mariadb-corporation/mariadb-connector-c/commit/e62ff46)\
  2021-01-28 11:20:35 +0100
  * fix memory leack in the test
* [Revision #e21d21d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/e21d21d)\
  2021-01-27 20:25:13 +0100
  * Fix ASAN issues in the tests
* [Revision #b503e52](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b503e52)\
  2021-01-27 13:13:31 +0100
  * fix problems found by 10.0
* [Revision #0b46f1a](https://github.com/mariadb-corporation/mariadb-connector-c/commit/0b46f1a)\
  2021-01-21 16:56:48 +0100
  * Fix for [CONC-521](https://jira.mariadb.org/browse/CONC-521)
* [Revision #4083fd9](https://github.com/mariadb-corporation/mariadb-connector-c/commit/4083fd9)\
  2021-01-19 16:08:05 +0100
  * Merge pull request #154 from mariadb-corporation/skysql-test
* [Revision #29fc3bc](https://github.com/mariadb-corporation/mariadb-connector-c/commit/29fc3bc)\
  2021-01-19 10:23:14 +0100
  * \[misc] test improvement \* adding SkySQL HA to test suite \* test server build 10.6 \* test maxscale 2.5.3
* [Revision #0186633](https://github.com/mariadb-corporation/mariadb-connector-c/commit/0186633)\
  2021-01-19 16:05:21 +0700
  * [MDEV-24577](https://jira.mariadb.org/browse/MDEV-24577): Fix warnings generated during compilation of plugin/auth\_pam/testing/pam\_mariadb\_mtr.c on FreeBSD
* [Revision #ef3d315](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ef3d315)\
  2021-01-18 18:23:17 +0100
  * Test case fix:
* [Revision #30ee397](https://github.com/mariadb-corporation/mariadb-connector-c/commit/30ee397)\
  2020-12-21 15:11:13 +0100
  * Fix for static build
* [Revision #2ff01c1](https://github.com/mariadb-corporation/mariadb-connector-c/commit/2ff01c1)\
  2020-11-27 18:33:06 +0100
  * Fix for [CONC-518](https://jira.mariadb.org/browse/CONC-518):
* [Revision #820faff](https://github.com/mariadb-corporation/mariadb-connector-c/commit/820faff)\
  2020-11-26 09:07:17 +0100
  * codespell fixes, removed MSDOS preprocessor macros
* [Revision #79137a4](https://github.com/mariadb-corporation/mariadb-connector-c/commit/79137a4)\
  2020-11-18 09:05:54 +0100
  * Fix for [CONC-517](https://jira.mariadb.org/browse/CONC-517): C/C looks for plugins in wrong locatio on Windows
* [Revision #777460c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/777460c)\
  2020-11-12 23:24:19 +0000
  * Fix C11 conformance
* [Revision #88e9d17](https://github.com/mariadb-corporation/mariadb-connector-c/commit/88e9d17)\
  2020-11-08 14:52:42 +0100
  * Added missing test case for [CONC-512](https://jira.mariadb.org/browse/CONC-512)
* [Revision #5ac0132](https://github.com/mariadb-corporation/mariadb-connector-c/commit/5ac0132)\
  2020-11-04 18:24:10 +0100
  * Bump version number
* [Revision #e382442](https://github.com/mariadb-corporation/mariadb-connector-c/commit/e382442)\
  2020-10-30 16:22:59 +0200
  * [CONC-514](https://jira.mariadb.org/browse/CONC-514) ma\_net\_write\_buff() invokes memcpy() on null pointer
