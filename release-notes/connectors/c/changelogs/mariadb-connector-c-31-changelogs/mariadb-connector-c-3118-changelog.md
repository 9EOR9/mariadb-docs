# MariaDB Connector/C 3.1.18 Changelog

The most recent [_**Stable**_](../../../../mariadb-release-criteria.md) _**(GA)**_ release of MariaDB Connector/C is:[**MariaDB Connector/C 3.4.5**](../../mariadb-connector-c-3-4-release-notes/mariadb-connector-c-3-4-5-release-notes.md)

[Download](https://mariadb.com/downloads/#connectors)[Release Notes](https://mariadb.com/kb/en/mariadb-connector-c-3118-release-notes)[Changelog](mariadb-connector-c-3118-changelog.md)[About MariaDB Connector/C](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-c/README.md)

**Release date:** 22 Aug 2022

For the highlights of this release, see the[release notes](https://github.com/mariadb-corporation/docs-release-notes/blob/test/connectors/c/changelogs/mariadb-connector-c-31-changelogs/mariadb-connector-c-3118-release-notes/README.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-c/) you can view more\
details of the revision and view diffs of the code modified in that revision.

* [Revision #630919e](https://github.com/mariadb-corporation/mariadb-connector-c/commit/630919e)\
  2022-08-03 11:46:35 +0200
  * MSVC Build: treat warning as errors
* [Revision #7fdb3ea](https://github.com/mariadb-corporation/mariadb-connector-c/commit/7fdb3ea)\
  2022-07-29 13:35:44 +0200
  * Windows build error:
* [Revision #69e697b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/69e697b)\
  2022-07-29 11:49:39 +0200
  * Added HAVE\_WINCRYPT to plugins/auth/CMakeLists.txt
* [Revision #3bb04cd](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3bb04cd)\
  2022-07-28 15:06:25 +0200
  * Follow up of OpenSSL 3.0 backport
* [Revision #9db7314](https://github.com/mariadb-corporation/mariadb-connector-c/commit/9db7314)\
  2022-07-27 15:00:46 +0200
  * Fixed typo in ma\_errmsg.h
* [Revision #12722e3](https://github.com/mariadb-corporation/mariadb-connector-c/commit/12722e3)\
  2022-07-27 14:52:20 +0200
  * Error message fix:
* [Revision #b9811b7](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b9811b7)\
  2022-07-26 08:16:53 +0300
  * Fix clang -Wunused-but-set-variable
* [Revision #788535f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/788535f)\
  2022-07-25 15:45:36 +0300
  * Fix GCC -Og -Wmaybe-uninitialized
* [Revision #8260fe5](https://github.com/mariadb-corporation/mariadb-connector-c/commit/8260fe5)\
  2022-07-25 13:52:43 +0200
  * Backport of [CONC-503](https://jira.mariadb.org/browse/CONC-503):
* [Revision #dfe3563](https://github.com/mariadb-corporation/mariadb-connector-c/commit/dfe3563)\
  2022-07-24 17:36:49 +0200
  * Fix for [CONC-607](https://jira.mariadb.org/browse/CONC-607) (Infinite loop in pvio\_socket\_internal\_connect)
* [Revision #8e8d175](https://github.com/mariadb-corporation/mariadb-connector-c/commit/8e8d175)\
  2022-07-22 08:16:25 +0200
  * Fix gnutls error message:
* [Revision #4830ed8](https://github.com/mariadb-corporation/mariadb-connector-c/commit/4830ed8)\
  2022-07-21 12:15:16 +0200
  * Windows build fixes
* [Revision #6a67ed6](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6a67ed6)\
  2022-07-21 11:26:32 +0200
  * Don't prefix error message 2026 (SSL connection error) with TLS
* [Revision #6700ee4](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6700ee4)\
  2022-07-21 09:47:23 +0200
  * Make TLS/SSL more verbose:
* [Revision #cdb6e90](https://github.com/mariadb-corporation/mariadb-connector-c/commit/cdb6e90)\
  2022-07-21 09:11:29 +0200
  * Fix for [CONC-608](https://jira.mariadb.org/browse/CONC-608): Replace server error codes
* [Revision #9a572bc](https://github.com/mariadb-corporation/mariadb-connector-c/commit/9a572bc)\
  2022-07-18 11:41:46 +0200
  * Fix for [CONC-604](https://jira.mariadb.org/browse/CONC-604) and [CONC-605](https://jira.mariadb.org/browse/CONC-605):
* [Revision #dac298d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/dac298d)\
  2022-07-11 07:53:31 +0200
  * [CONC-605](https://jira.mariadb.org/browse/CONC-605): Disable sigpipe
* [Revision #f1b08b8](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f1b08b8)\
  2022-07-08 07:46:00 +0200
  * Partial fix for [MDEV-27405](https://jira.mariadb.org/browse/MDEV-27405):
* [Revision #d12fd88](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d12fd88)\
  2022-07-01 08:20:25 +0300
  * Fix clang -Wunused-but-set-variable
* [Revision #04be26e](https://github.com/mariadb-corporation/mariadb-connector-c/commit/04be26e)\
  2022-05-31 07:52:08 +0200
  * Merge branch '3.1' of [mariadb-connector-c](https://github.com/mariadb-corporation/mariadb-connector-c) into 3.1
* [Revision #18ae382](https://github.com/mariadb-corporation/mariadb-connector-c/commit/18ae382)\
  2022-05-25 12:06:46 -0400
  * update MARIADB\_CLIENT\_VERSION\_PATCH to next [MariaDB 10.5](../../../../mariadb-community-server-release-notes/mariadb-10-5-series/what-is-mariadb-105.md)
* [Revision #96bbb2b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/96bbb2b)\
  2022-05-25 12:02:26 -0400
  * bump the VERSION
* [Revision #02a2be0](https://github.com/mariadb-corporation/mariadb-connector-c/commit/02a2be0)\
  2022-05-31 07:50:57 +0200
  * Fix build of static plugins
