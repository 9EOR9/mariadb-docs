# MariaDB Connector/C 3.3.2 Changelog

The most recent [_**Stable**_](../../../../mariadb-release-criteria.md) _**(GA)**_ release of MariaDB Connector/C is:[**MariaDB Connector/C 3.4.5**](../../mariadb-connector-c-3-4-release-notes/mariadb-connector-c-3-4-5-release-notes.md)

[Download](https://mariadb.com/downloads/#connectors)[Release Notes](../../mariadb-connector-c-33-release-notes/mariadb-connector-c-332-release-notes.md)[Changelog](mariadb-connector-c-332-changelog.md)[About MariaDB Connector/C](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-c/README.md)

**Release date:** 22 Aug 2022

For the highlights of this release, see the[release notes](../../mariadb-connector-c-33-release-notes/mariadb-connector-c-332-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-c/) you can view more\
details of the revision and view diffs of the code modified in that revision.

* [Revision #1bd8c8b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/1bd8c8b)\
  2022-08-11 16:56:06 +0200
  * Added missing status callbacks outside of ma\_read\_ok\_packet
* [Revision #a6665e6](https://github.com/mariadb-corporation/mariadb-connector-c/commit/a6665e6)\
  2022-08-03 17:57:15 +0200
  * Clear error before reading ok packet
* [Revision #9fe6541](https://github.com/mariadb-corporation/mariadb-connector-c/commit/9fe6541)\
  2022-08-03 11:26:57 +0200
  * Windows build fix:
* [Revision #5b4c493](https://github.com/mariadb-corporation/mariadb-connector-c/commit/5b4c493)\
  2022-08-03 12:00:03 +0200
  * Merge branch '3.3' of [mariadb-connector-c](https://github.com/mariadb-corporation/mariadb-connector-c) into 3.3
* [Revision #64ebd58](https://github.com/mariadb-corporation/mariadb-connector-c/commit/64ebd58)\
  2022-08-02 15:19:39 +0200
  * Follow up for status/session\_track callback:
* [Revision #0682f22](https://github.com/mariadb-corporation/mariadb-connector-c/commit/0682f22)\
  2022-08-03 11:59:57 +0200
  * Merge branch '3.1' into 3.3
* [Revision #630919e](https://github.com/mariadb-corporation/mariadb-connector-c/commit/630919e)\
  2022-08-03 11:46:35 +0200
  * MSVC Build: treat warning as errors
* [Revision #28df8a7](https://github.com/mariadb-corporation/mariadb-connector-c/commit/28df8a7)\
  2022-08-02 10:20:19 +0200
  * Merge branch '3.3-status' into 3.3
* [Revision #a8832af](https://github.com/mariadb-corporation/mariadb-connector-c/commit/a8832af)\
  2022-08-02 10:10:50 +0200
  * status and session\_tracik callback function:
* [Revision #f124488](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f124488)\
  2022-08-01 12:28:02 +0200
  * Merge branch '3.1' into 3.3
* [Revision #7fdb3ea](https://github.com/mariadb-corporation/mariadb-connector-c/commit/7fdb3ea)\
  2022-07-29 13:35:44 +0200
  * Windows build error:
* [Revision #69e697b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/69e697b)\
  2022-07-29 11:49:39 +0200
  * Added HAVE\_WINCRYPT to plugins/auth/CMakeLists.txt
* [Revision #3bb04cd](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3bb04cd)\
  2022-07-28 15:06:25 +0200
  * Follow up of OpenSSL 3.0 backport
* [Revision #dcb14e3](https://github.com/mariadb-corporation/mariadb-connector-c/commit/dcb14e3)\
  2022-08-01 12:26:27 +0200
  * erge branch '3.1' into 3.3
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
* [Revision #df6feae](https://github.com/mariadb-corporation/mariadb-connector-c/commit/df6feae)\
  2022-02-28 16:57:52 +0400
  * Libmariadb changes for [MDEV-27009](https://jira.mariadb.org/browse/MDEV-27009) Add UCA-14.0.0 collations
* [Revision #274f2fa](https://github.com/mariadb-corporation/mariadb-connector-c/commit/274f2fa)\
  2022-07-25 09:22:04 +0200
  * Merge pull request #199 from hyung-hwan/3.3
* [Revision #6baff67](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6baff67)\
  2022-06-23 13:28:54 +0900
  * Merge branch 'mariadb-corporation:3.3' into 3.3
* [Revision #cc0a0e9](https://github.com/mariadb-corporation/mariadb-connector-c/commit/cc0a0e9)\
  2022-06-22 18:39:01 +0900
  * Merge branch 'mariadb-corporation:3.3' into 3.3
* [Revision #8af9a68](https://github.com/mariadb-corporation/mariadb-connector-c/commit/8af9a68)\
  2022-06-21 18:29:07 +0900
  * Merge branch 'mariadb-corporation:3.3' into 3.3
* [Revision #c0fea17](https://github.com/mariadb-corporation/mariadb-connector-c/commit/c0fea17)\
  2022-06-21 17:49:45 +0900
  * enhanced mysql\_close() and other related parts to prevent memory leaks when terminating an initiated but unestablished connection
* [Revision #2dd03f0](https://github.com/mariadb-corporation/mariadb-connector-c/commit/2dd03f0)\
  2022-07-25 08:44:26 +0200
  * typo fixes (was PR 203)
* [Revision #cb6d03f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/cb6d03f)\
  2022-07-24 17:41:07 +0200
  * Merge branch '3.1' into 3.3
* [Revision #dfe3563](https://github.com/mariadb-corporation/mariadb-connector-c/commit/dfe3563)\
  2022-07-24 17:36:49 +0200
  * Fix for [CONC-607](https://jira.mariadb.org/browse/CONC-607) (Infinite loop in pvio\_socket\_internal\_connect)
* [Revision #6dbd953](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6dbd953)\
  2022-07-24 10:52:52 +0200
  * Merge branch '3.1' into 3.3
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
* [Revision #e8e356e](https://github.com/mariadb-corporation/mariadb-connector-c/commit/e8e356e)\
  2022-07-18 11:48:33 +0200
  * Merge branch '3.1' into 3.3
* [Revision #9a572bc](https://github.com/mariadb-corporation/mariadb-connector-c/commit/9a572bc)\
  2022-07-18 11:41:46 +0200
  * Fix for [CONC-604](https://jira.mariadb.org/browse/CONC-604) and [CONC-605](https://jira.mariadb.org/browse/CONC-605):
* [Revision #dac298d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/dac298d)\
  2022-07-11 07:53:31 +0200
  * [CONC-605](https://jira.mariadb.org/browse/CONC-605): Disable sigpipe
* [Revision #5565de1](https://github.com/mariadb-corporation/mariadb-connector-c/commit/5565de1)\
  2022-07-08 07:49:24 +0200
  * Merge branch '3.1' into 3.3
* [Revision #f1b08b8](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f1b08b8)\
  2022-07-08 07:46:00 +0200
  * Partial fix for [MDEV-27405](https://jira.mariadb.org/browse/MDEV-27405):
* [Revision #876ba73](https://github.com/mariadb-corporation/mariadb-connector-c/commit/876ba73)\
  2022-07-03 13:47:07 +0200
  * Merge branch '3.3' of [mariadb-connector-c](https://github.com/mariadb-corporation/mariadb-connector-c) into 3.3
* [Revision #485a3ad](https://github.com/mariadb-corporation/mariadb-connector-c/commit/485a3ad)\
  2022-07-01 08:21:27 +0300
  * Merge 3.2 into 3.3
* [Revision #c3a7a38](https://github.com/mariadb-corporation/mariadb-connector-c/commit/c3a7a38)\
  2022-07-01 08:20:53 +0300
  * Merge 3.1 into 3.2
* [Revision #d12fd88](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d12fd88)\
  2022-07-01 08:20:25 +0300
  * Fix clang -Wunused-but-set-variable
* [Revision #5f1f517](https://github.com/mariadb-corporation/mariadb-connector-c/commit/5f1f517)\
  2022-07-03 13:45:37 +0200
  * Various typo fixes
* [Revision #35826cd](https://github.com/mariadb-corporation/mariadb-connector-c/commit/35826cd)\
  2022-06-29 13:27:28 +0200
  * Test fix for test\_bug4236
* [Revision #3f7719c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3f7719c)\
  2022-06-27 13:23:35 +0200
  * Typo fixes (from PR #200)
* [Revision #271ae9c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/271ae9c)\
  2022-06-23 11:41:09 +0200
  * Travis:
* [Revision #8eff2a8](https://github.com/mariadb-corporation/mariadb-connector-c/commit/8eff2a8)\
  2022-06-22 16:31:01 +0200
  * Merge branch '3.3' of [mariadb-connector-c](https://github.com/mariadb-corporation/mariadb-connector-c) into 3.3
* [Revision #92c2f89](https://github.com/mariadb-corporation/mariadb-connector-c/commit/92c2f89)\
  2022-06-22 10:55:17 +0200
  * Merge pull request #195 from Biswa96/maridb-config-mingw
* [Revision #74fb417](https://github.com/mariadb-corporation/mariadb-connector-c/commit/74fb417)\
  2022-04-13 10:34:12 +0530
  * cmake: Enable building mariadb\_config for mingw
* [Revision #abddf0b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/abddf0b)\
  2022-06-22 16:25:37 +0200
  * Fixed ROTATE\_EVENT
* [Revision #3230e75](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3230e75)\
  2022-06-21 11:17:56 +0200
  * Fix for [CONC-601](https://jira.mariadb.org/browse/CONC-601):
* [Revision #1e2f6d5](https://github.com/mariadb-corporation/mariadb-connector-c/commit/1e2f6d5)\
  2022-06-21 10:51:59 +0200
  * Fix for [CONC-600](https://jira.mariadb.org/browse/CONC-600):
* [Revision #7523c27](https://github.com/mariadb-corporation/mariadb-connector-c/commit/7523c27)\
  2022-06-15 11:42:27 +0200
  * Windows build fix
* [Revision #f804069](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f804069)\
  2022-06-04 16:35:46 +0200
  * Updated manpages
* [Revision #77a1f79](https://github.com/mariadb-corporation/mariadb-connector-c/commit/77a1f79)\
  2022-05-31 08:11:02 +0200
  * Merge branch '3.2' into 3.3
* [Revision #899f678](https://github.com/mariadb-corporation/mariadb-connector-c/commit/899f678)\
  2022-05-31 08:03:27 +0200
  * Merge branch '3.1' into 3.2
* [Revision #04be26e](https://github.com/mariadb-corporation/mariadb-connector-c/commit/04be26e)\
  2022-05-31 07:52:08 +0200
  * Merge branch '3.1' of [mariadb-connector-c](https://github.com/mariadb-corporation/mariadb-connector-c) into 3.1
* [Revision #18ae382](https://github.com/mariadb-corporation/mariadb-connector-c/commit/18ae382)\
  2022-05-25 12:06:46 -0400
  * update MARIADB\_CLIENT\_VERSION\_PATCH to next [MariaDB 10.5](../../../../mariadb-community-server-release-notes/mariadb-10-5-series/what-is-mariadb-105.md)
* [Revision #96bbb2b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/96bbb2b)\
  2022-05-25 12:02:26 -0400
  * bump the VERSION
* [Revision #4a99777](https://github.com/mariadb-corporation/mariadb-connector-c/commit/4a99777)\
  2022-05-23 16:20:21 +0300
  * Fix permissions after 79137a4ae1cf37ab46940d26879051ad1dfce512
* [Revision #02a2be0](https://github.com/mariadb-corporation/mariadb-connector-c/commit/02a2be0)\
  2022-05-31 07:50:57 +0200
  * Fix build of static plugins
* [Revision #bf8bb1c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/bf8bb1c)\
  2022-05-25 12:05:00 -0400
  * bump the VERSION
* [Revision #e0bae1b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/e0bae1b)\
  2022-05-24 06:12:20 +0200
  * Fixed version:
* [Revision #d7f8a44](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d7f8a44)\
  2022-05-25 18:30:18 +0200
  * update server error messages (mysqld\_error.h)
* [Revision #ae05dde](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ae05dde)\
  2022-05-25 18:29:55 +0200
  * Merge branch '3.3' of [mariadb-connector-c](https://github.com/mariadb-corporation/mariadb-connector-c) into 3.3
* [Revision #99598de](https://github.com/mariadb-corporation/mariadb-connector-c/commit/99598de)\
  2022-05-25 12:09:49 -0400
  * bump the VERSION
* [Revision #fcce4a8](https://github.com/mariadb-corporation/mariadb-connector-c/commit/fcce4a8)\
  2022-05-23 14:05:06 +0200
  * [CONC-592](https://jira.mariadb.org/browse/CONC-592): Register replica with host and port
