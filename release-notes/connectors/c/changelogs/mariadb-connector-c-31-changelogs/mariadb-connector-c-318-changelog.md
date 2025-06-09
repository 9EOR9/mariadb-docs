# MariaDB Connector/C 3.1.8 Changelog

The most recent [_**Stable**_](../../../../mariadb-release-criteria.md) _**(GA)**_ release of MariaDB Connector/C is:[**MariaDB Connector/C 3.4.5**](../../mariadb-connector-c-3-4-release-notes/mariadb-connector-c-3-4-5-release-notes.md)

[Download](https://mariadb.com/downloads/#connectors)[Release Notes](../../mariadb-connector-c-31-release-notes/mariadb-connector-c-318-release-notes.md)[Changelog](mariadb-connector-c-318-changelog.md)[About MariaDB Connector/C](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-c/README.md)

**Release date:** 14 May 2020

For the highlights of this release, see the[release notes](../../mariadb-connector-c-31-release-notes/mariadb-connector-c-318-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-c/) you can view more\
details of the revision and view diffs of the code modified in that revision.

* [Revision #2759b87](https://github.com/mariadb-corporation/mariadb-connector-c/commit/2759b87)\
  2020-05-07 14:57:00 +0200
  * sanity checks for client-supplied OK packet content
* [Revision #f8213af](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f8213af)\
  2020-05-07 15:06:20 +0200
  * remove debugging output
* [Revision #5883617](https://github.com/mariadb-corporation/mariadb-connector-c/commit/5883617)\
  2020-05-05 21:57:01 +0200
  * Added parameter PACKAGE\_PLATFORM\_SUFFIX for providing binaries for different Linux platforms/flavours
* [Revision #ca8f94f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ca8f94f)\
  2020-05-04 09:13:08 +0200
  * BUG#29597896 - NULL POINTER DEREFERENCE IN LIBMYSQL
* [Revision #2d81c70](https://github.com/mariadb-corporation/mariadb-connector-c/commit/2d81c70)\
  2020-04-26 03:07:59 +0200
  * Fix max\_param test:
* [Revision #86c483f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/86c483f)\
  2020-04-25 07:18:06 +0200
  * Updatei matrix of DB version numbers
* [Revision #b4ac056](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b4ac056)\
  2020-04-25 07:03:38 +0200
  *
    * Fixed archive host - Download via curl
* [Revision #8ff27a4](https://github.com/mariadb-corporation/mariadb-connector-c/commit/8ff27a4)\
  2020-04-25 06:59:33 +0200
  * Revert "Fix host for msi download"
* [Revision #79221e5](https://github.com/mariadb-corporation/mariadb-connector-c/commit/79221e5)\
  2020-04-25 06:53:58 +0200
  * Fix host for msi download
* [Revision #5390a77](https://github.com/mariadb-corporation/mariadb-connector-c/commit/5390a77)\
  2020-04-24 13:29:11 +0200
  * Fix clang-cl 32bit warning.
* [Revision #74032c5](https://github.com/mariadb-corporation/mariadb-connector-c/commit/74032c5)\
  2020-04-20 17:17:12 +0200
  * Merge pull request #133 from grooverdan/solaris\_fixes
* [Revision #dfd8f0b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/dfd8f0b)\
  2020-04-04 12:51:41 +1100
  * Solaris fix: iconv on solaris take const char
* [Revision #8de09e1](https://github.com/mariadb-corporation/mariadb-connector-c/commit/8de09e1)\
  2020-04-04 12:51:01 +1100
  * Add IF\_SOLARIS macro
* [Revision #2a10f24](https://github.com/mariadb-corporation/mariadb-connector-c/commit/2a10f24)\
  2020-04-20 17:16:07 +0200
  * Merge pull request #134 from grooverdan/mariadb\_config\_solaris\_compile\_fix
* [Revision #a4c496f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/a4c496f)\
  2020-04-04 13:40:52 +1100
  * mariadb\_config: solaris fix - types for options
* [Revision #5c1fa6b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/5c1fa6b)\
  2020-04-16 11:49:43 +0200
  * Fix Win32 error formatting.
* [Revision #e242172](https://github.com/mariadb-corporation/mariadb-connector-c/commit/e242172)\
  2020-04-14 20:31:42 +0200
  * CMake, Windows - install PDBs for client plugins
* [Revision #cbff6bc](https://github.com/mariadb-corporation/mariadb-connector-c/commit/cbff6bc)\
  2020-04-14 20:31:10 +0200
  * CMake : do not use transitive linking for shared client library
* [Revision #3f9a156](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3f9a156)\
  2020-04-14 20:28:53 +0200
  * CMake : Avoid warning with CMAKE\_INTERPROCEDURAL\_OPTIMIZATION=ON
* [Revision #6e78f12](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6e78f12)\
  2020-04-07 22:10:48 +0200
  * cmake: use MESSAGE1, not MESSAGE
* [Revision #9c84958](https://github.com/mariadb-corporation/mariadb-connector-c/commit/9c84958)\
  2020-03-11 09:54:46 +0300
  * [MDEV-21889](https://jira.mariadb.org/browse/MDEV-21889) Typo fix: ER\_KEY\_DOES\_NOT\_EXISTS
* [Revision #ac1f819](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ac1f819)\
  2020-03-28 23:23:38 +0200
  * MemorySanitizer: Avoid calling uninstrumented getservbyname()
* [Revision #7a2c052](https://github.com/mariadb-corporation/mariadb-connector-c/commit/7a2c052)\
  2020-03-28 20:12:43 +0200
  * MemorySanitizer: Avoid calling uninstrumented getservbyname()
* [Revision #21a9d12](https://github.com/mariadb-corporation/mariadb-connector-c/commit/21a9d12)\
  2020-03-28 19:17:49 +0100
  * Merge pull request #130 from ottok/feature/[CONC-456](https://jira.mariadb.org/browse/CONC-456)
* [Revision #28e1467](https://github.com/mariadb-corporation/mariadb-connector-c/commit/28e1467)\
  2020-03-27 00:22:33 +0200
  * [CONC-456](https://jira.mariadb.org/browse/CONC-456): Introduce INSTALL\_PLUGINDIR\_CLIENT
* [Revision #aa8b130](https://github.com/mariadb-corporation/mariadb-connector-c/commit/aa8b130)\
  2020-03-27 17:52:34 +0100
  * Fix "misleading indentation" warning (clang)
* [Revision #3586036](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3586036)\
  2020-03-26 19:59:19 +0100
  * As requested by Otto Käkelainen the directory for client plugins in Debian should contain also the major version number.
* [Revision #0ab6c20](https://github.com/mariadb-corporation/mariadb-connector-c/commit/0ab6c20)\
  2020-03-22 19:22:40 +0100
  * travis\_ci: remove 10.5 from allowed\_failures
* [Revision #0d8eca8](https://github.com/mariadb-corporation/mariadb-connector-c/commit/0d8eca8)\
  2020-03-22 18:32:48 +0100
  * Disable MySQL 8.0 server test due to SSL startup error. Added 10.5 branch
* [Revision #61a3798](https://github.com/mariadb-corporation/mariadb-connector-c/commit/61a3798)\
  2020-03-22 17:53:37 +0100
  * Fix server build inside travis: Instead of disabling submodules we need to checkout the actual commit.
* [Revision #1768cb6](https://github.com/mariadb-corporation/mariadb-connector-c/commit/1768cb6)\
  2020-03-16 16:24:36 +0100
  * Replaced MySQL Server 5.7 by 8.0 Added 10.5 branch
* [Revision #6552b29](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6552b29)\
  2020-03-16 14:27:11 +0100
  * Fix for previous commit
* [Revision #960dca5](https://github.com/mariadb-corporation/mariadb-connector-c/commit/960dca5)\
  2020-03-16 14:02:12 +0100
  * Travis fixes:
* [Revision #d32add1](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d32add1)\
  2020-03-16 12:36:03 +0100
  * Fix certificate generation for travis
* [Revision #08fcd79](https://github.com/mariadb-corporation/mariadb-connector-c/commit/08fcd79)\
  2020-03-16 07:05:02 +0100
  * Fixed error in naming for static remote\_io plugin.
* [Revision #fbf1db6](https://github.com/mariadb-corporation/mariadb-connector-c/commit/fbf1db6)\
  2020-03-15 16:09:37 +0100
  * Fix for [CONC-464](https://jira.mariadb.org/browse/CONC-464):
* [Revision #8c773db](https://github.com/mariadb-corporation/mariadb-connector-c/commit/8c773db)\
  2020-03-12 18:09:40 +0100
  * Fix for [CONC-441](https://jira.mariadb.org/browse/CONC-441):
* [Revision #3be5897](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3be5897)\
  2020-03-12 12:06:40 +0100
  * Fix for [MDEV-21920](https://jira.mariadb.org/browse/MDEV-21920)
* [Revision #f9a5046](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f9a5046)\
  2020-03-11 08:25:59 +0100
  * Merge pull request #129 from ottok/3.1-fix-spelling
* [Revision #c0d5d7d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/c0d5d7d)\
  2020-03-04 18:18:36 +0200
  * Fix typo in output string: inital -> initial
* [Revision #328580a](https://github.com/mariadb-corporation/mariadb-connector-c/commit/328580a)\
  2020-03-11 08:12:53 +0100
  * Because the function strncpy() will not ensure that the destination string will be terminated by the NUL character, it is best to do that externally in the caller. This code was originally introduced in commit beb9d5ea8994bb90361c4b9f3d926eee24055178. (patch by Marko)
* [Revision #ca68b11](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ca68b11)\
  2020-03-10 20:08:30 +0100
  * Fixed problem of going over 32 bit on windows.
* [Revision #b704700](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b704700)\
  2020-03-10 17:21:24 +0100
  * Fixed bug which was introduced in 1218ffac1a9adefd6428e68b6154bc54a04343aa:
* [Revision #acdd9da](https://github.com/mariadb-corporation/mariadb-connector-c/commit/acdd9da)\
  2020-03-10 14:42:46 +0100
  * Revert "Use /etc/sslcert as CERT\_PATH for travis build"
* [Revision #899e583](https://github.com/mariadb-corporation/mariadb-connector-c/commit/899e583)\
  2020-03-10 14:23:46 +0100
  * Use /etc/sslcert as CERT\_PATH for travis build
* [Revision #6632cb6](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6632cb6)\
  2020-03-10 17:02:59 +0400
  * [MDEV-17832](https://jira.mariadb.org/browse/MDEV-17832) Protocol: extensions for Pluggable types and JSON, GEOMETRY
* [Revision #d4f7548](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d4f7548)\
  2020-03-05 09:50:12 +0100
  * Fix for [CONC-458](https://jira.mariadb.org/browse/CONC-458):
* [Revision #6a0c8ff](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6a0c8ff)\
  2020-02-28 12:56:37 +0100
  * Fix for [CONC-457](https://jira.mariadb.org/browse/CONC-457):
* [Revision #5d86a33](https://github.com/mariadb-corporation/mariadb-connector-c/commit/5d86a33)\
  2020-02-14 10:01:27 +0100
  * Merge branch '3.1' of [mariadb-connector-c](https://github.com/mariadb-corporation/mariadb-connector-c) into 3.1
* [Revision #8b4305c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/8b4305c)\
  2020-02-13 09:37:08 +0100
  * Merge pull request #128 from Meuh-42/fix/charset
* [Revision #61ecc3b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/61ecc3b)\
  2020-02-12 17:03:41 +0100
  * Fix typo in charsets names
* [Revision #b787c0d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b787c0d)\
  2020-02-13 09:32:34 +0100
  * Merge pull request #127 from nismoryco/3.1
* [Revision #15856fc](https://github.com/mariadb-corporation/mariadb-connector-c/commit/15856fc)\
  2020-02-11 08:27:26 -0800
  * add @CMAKE\_SYSROOT@ to include and library paths
* [Revision #1218ffa](https://github.com/mariadb-corporation/mariadb-connector-c/commit/1218ffa)\
  2020-02-14 09:52:21 +0100
  * Fix for [CONC-452](https://jira.mariadb.org/browse/CONC-452) and [CONC-453](https://jira.mariadb.org/browse/CONC-453):
* [Revision #bc061db](https://github.com/mariadb-corporation/mariadb-connector-c/commit/bc061db)\
  2020-02-13 08:28:44 +0100
  * Fix for [CONC-455](https://jira.mariadb.org/browse/CONC-455):
* [Revision #17ba6af](https://github.com/mariadb-corporation/mariadb-connector-c/commit/17ba6af)\
  2020-02-06 10:08:32 +0100
  * Fix for mysql\_set\_character\_set:
* [Revision #6dd1ed9](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6dd1ed9)\
  2020-01-29 11:15:35 -0500
  * bump the VERSION
* [Revision #d24e742](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d24e742)\
  2020-01-29 13:22:38 +0100
  * [CONC-449](https://jira.mariadb.org/browse/CONC-449):
* [Revision #84dc415](https://github.com/mariadb-corporation/mariadb-connector-c/commit/84dc415)\
  2020-01-22 16:20:50 +0100
  * ssl unit test fixes
