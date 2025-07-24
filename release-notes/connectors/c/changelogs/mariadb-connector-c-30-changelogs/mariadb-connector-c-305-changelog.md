# Connector/C 3.0.5 Changelog

The most recent [_**Stable**_](../../../../community-server/about/release-criteria.md) _**(GA)**_ release of MariaDB Connector/C is:[**MariaDB Connector/C 3.4.5**](../../mariadb-connector-c-3-4-release-notes/mariadb-connector-c-3-4-5-release-notes.md)

[Download](https://downloads.mariadb.org/connector-c/3.0.5)[Release Notes](../../mariadb-connector-c-30-release-notes/mariadb-connector-c-305-release-notes.md)[Changelog](mariadb-connector-c-305-changelog.md)[About MariaDB Connector/C](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-c/README.md)

**Release date:** 7 Jun 2018

For the highlights of this release, see the [release notes](../../mariadb-connector-c-30-release-notes/mariadb-connector-c-305-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On [GitHub](https://github.com/MariaDB/mariadb-connector-c/) you can view more\
details of the revision and view diffs of the code modified in that revision.

* [Revision #e8aea63](https://github.com/mariadb-corporation/mariadb-connector-c/commit/e8aea63)\
  2018-05-30 16:31:17 +0200
  * Windows build fix
* [Revision #22bf0be](https://github.com/mariadb-corporation/mariadb-connector-c/commit/22bf0be)\
  2018-05-30 12:37:37 +0200
  * Merge pull request #53 from FaramosCZ/patch-2
* [Revision #8848959](https://github.com/mariadb-corporation/mariadb-connector-c/commit/8848959)\
  2018-05-24 07:06:12 +0200
  * Add conversion to the types expected by the memset()
* [Revision #725e397](https://github.com/mariadb-corporation/mariadb-connector-c/commit/725e397)\
  2018-05-30 12:34:45 +0200
  * Merge pull request #50 from junaruga/hotfix/fix-cert-request-with-newer-openssl
* [Revision #b170111](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b170111)\
  2018-05-07 20:30:02 +0200
  * Fix certificate request error on OpenSSL.
* [Revision #50c21cb](https://github.com/mariadb-corporation/mariadb-connector-c/commit/50c21cb)\
  2018-05-30 09:28:49 +0200
  * Merge pull request #54 from FaramosCZ/patch-3
* [Revision #9bed6bf](https://github.com/mariadb-corporation/mariadb-connector-c/commit/9bed6bf)\
  2018-05-24 07:25:45 +0200
  * Fix: double free()
* [Revision #99c878d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/99c878d)\
  2018-05-30 07:12:34 +0200
  * Merge pull request #55 from FaramosCZ/patch-4
* [Revision #cd91dc8](https://github.com/mariadb-corporation/mariadb-connector-c/commit/cd91dc8)\
  2018-05-24 07:35:20 +0200
  * Fix: use after free()
* [Revision #8f168c4](https://github.com/mariadb-corporation/mariadb-connector-c/commit/8f168c4)\
  2018-05-30 07:04:38 +0200
  * Added test case for [CONC-336](https://jira.mariadb.org/browse/CONC-336)
* [Revision #6b16eb7](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6b16eb7)\
  2018-05-29 17:46:47 +0200
  * Fix for [CONC-336](https://jira.mariadb.org/browse/CONC-336): Allow multiple initialization of the client library (mysql\_server\_init(\
    mysql\_server\_end).
* [Revision #2a5f40f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/2a5f40f)\
  2018-05-29 15:44:46 +0300
  * Merge pull request #57 from rusher/master
* [Revision #2689375](https://github.com/mariadb-corporation/mariadb-connector-c/commit/2689375)\
  2018-05-28 16:33:49 +0200
  * \[test] removing plugins from server test build. server test build can be build with plugins according to build options. This patch permit will not install those plugins (particulary mariadb-plugin-cracklib-password-check)
* [Revision #1511314](https://github.com/mariadb-corporation/mariadb-connector-c/commit/1511314)\
  2018-05-29 11:43:47 +0200
  * Merge branch 'master' of [mariadb-connector-c](https://github.com/MariaDB/mariadb-connector-c)
* [Revision #53c40f5](https://github.com/mariadb-corporation/mariadb-connector-c/commit/53c40f5)\
  2018-05-29 09:49:35 +0200
  * Fix for [CONC-334](https://jira.mariadb.org/browse/CONC-334): Copy all members of MYSQL\_FIELD from mysql->fields to stmt->fields.
* [Revision #8455b6e](https://github.com/mariadb-corporation/mariadb-connector-c/commit/8455b6e)\
  2018-05-24 12:10:02 +0200
  * Changed default character set from utf8 (see fix for [CONC-315](https://jira.mariadb.org/browse/CONC-315)) to latin1, which is also default behavior in [MariaDB 10.1](../../../../community-server/old-releases/release-notes-mariadb-10-1-series/changes-improvements-in-mariadb-10-1.md) To use another default character set, MariaDB Connector/C has to be build with CMake parameter -DDEFAUT\_CHARSET=name.
* [Revision #407ca36](https://github.com/mariadb-corporation/mariadb-connector-c/commit/407ca36)\
  2018-05-28 15:51:58 +0200
  * Fixed string conversion to MYSQL\_TIME\_TYPE:
    * added support for negative time values
    * invalid strings (and/or conversion) and invalid values will result in MYSQL\_TIMESTAMP\_ERROR time type
    * added support for 2digit year representation:
      * values `< 69` will be converted to `20YY`
      * values `>= 69` will be converted to `19YY`
* [Revision #a12a0b8](https://github.com/mariadb-corporation/mariadb-connector-c/commit/a12a0b8)\
  2018-05-21 09:48:21 +0000
  * Merge branch '10.2-server'
* [Revision #1cc7b52](https://github.com/mariadb-corporation/mariadb-connector-c/commit/1cc7b52)\
  2018-05-17 13:02:59 +0400
  * Add GNUTLS include directory
* [Revision #27b2f3d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/27b2f3d)\
  2018-05-09 23:07:57 +0200
  * various checks for corrupted packets in the protocol
* [Revision #d70c883](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d70c883)\
  2018-05-09 23:06:28 +0200
  * minor style changes
* [Revision #d0e48e3](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d0e48e3)\
  2018-04-24 17:20:07 +0200
  * Fixed another logical-op warning if EAGAIN and EWOULDBLOCK have same values.
* [Revision #df07deb](https://github.com/mariadb-corporation/mariadb-connector-c/commit/df07deb)\
  2018-04-24 17:18:31 +0200
  * Support for -Wlogical-op flag and warning fixes (Patch provided by Monty)
* [Revision #7775af7](https://github.com/mariadb-corporation/mariadb-connector-c/commit/7775af7)\
  2018-04-24 12:17:48 +0200
  * Fix for [CONC-326](https://jira.mariadb.org/browse/CONC-326): ssl\_thread\_init() uses wrong openssl threadid callback
* [Revision #b4a138c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b4a138c)\
  2018-04-14 07:30:19 +0200
  * Windows build fixes: disable [CONC-317](https://jira.mariadb.org/browse/CONC-317) for windows platforms
* [Revision #212d405](https://github.com/mariadb-corporation/mariadb-connector-c/commit/212d405)\
  2018-03-30 06:45:19 -0400
  * Fixes misc. typos
* [Revision #061950f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/061950f)\
  2018-04-12 16:22:38 +0200
  * [CONC-322](https://jira.mariadb.org/browse/CONC-322): Correct handling of EAGAIN and EINPROGRESS in internal\_connect (socket) for non windows platforms. Kudos to Daniel Black for providing this patch.
* [Revision #5a399af](https://github.com/mariadb-corporation/mariadb-connector-c/commit/5a399af)\
  2018-04-12 08:52:21 +0200
  * Bumped version to 10.2.13 (only valid for standalone C/C build)
* [Revision #585be64](https://github.com/mariadb-corporation/mariadb-connector-c/commit/585be64)\
  2018-04-12 08:49:26 +0200
  * Fix for mariadb\_stmt\_execute: If compressed protocol is in use, mariadb\_stmt\_execute\_direct will be emulated by mysql\_stmt\_prepare and mysql\_stmt\_execute.
* [Revision #d83802a](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d83802a)\
  2018-04-12 07:00:43 +0200
  * Fix for [CONC-317](https://jira.mariadb.org/browse/CONC-317): Parsing of configuration file fails if key/value pairs contain white spaces.
* [Revision #f39db18](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f39db18)\
  2018-04-11 13:21:05 +0200
  * Fix for [CONC-315](https://jira.mariadb.org/browse/CONC-315): If no default client character set was specified, the utf8 character set will be used by default (instead of setting the client character set to server character set)
* [Revision #dae524d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/dae524d)\
  2018-04-07 07:42:59 +0200
  * [CONC-314](https://jira.mariadb.org/browse/CONC-314): Support for expired passwords (MySQL Server)
* [Revision #deeb32a](https://github.com/mariadb-corporation/mariadb-connector-c/commit/deeb32a)\
  2018-05-19 23:08:54 +0000
  * Remove LIBRARY\_OUTPUT\_DIRECTORY from target properties for plugins to fix windows build/test
* [Revision #d9fe72d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d9fe72d)\
  2018-05-19 23:03:46 +0000
  * Merge branch 'grooverdan-[MDEV-15655](https://jira.mariadb.org/browse/MDEV-15655)-abstract-socket-linux-only'
* [Revision #57742e1](https://github.com/mariadb-corporation/mariadb-connector-c/commit/57742e1)\
  2018-05-19 22:58:51 +0000
  * Merge branch '[MDEV-15655](https://jira.mariadb.org/browse/MDEV-15655)-abstract-socket-linux-only' of git:github.com/grooverdan/mariadb-connector-c into grooverdan-[MDEV-15655](https://jira.mariadb.org/browse/MDEV-15655)-abstract-socket-linux-only
* [Revision #fdbc31a](https://github.com/mariadb-corporation/mariadb-connector-c/commit/fdbc31a)\
  2018-05-10 11:14:57 +1000
  * [MDEV-15655](https://jira.mariadb.org/browse/MDEV-15655): abstract socket support - fix length(2)
* [Revision #dd3ab95](https://github.com/mariadb-corporation/mariadb-connector-c/commit/dd3ab95)\
  2018-05-19 18:50:33 +0000
  * fix plugin library building on macOS
* [Revision #252a7c3](https://github.com/mariadb-corporation/mariadb-connector-c/commit/252a7c3)\
  2018-05-17 13:02:59 +0400
  * Add GNUTLS include directory
* [Revision #cbc9a71](https://github.com/mariadb-corporation/mariadb-connector-c/commit/cbc9a71)\
  2018-05-19 15:32:39 +0200
  * attempt to fix C/C to build on older cmake
* [Revision #184a16d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/184a16d)\
  2018-05-19 12:34:07 +0000
  * Post-fix after ba9f5f4af1ed329128ae04c22952902604ba081d (adding \_server\_host attribute).
* [Revision #638f2aa](https://github.com/mariadb-corporation/mariadb-connector-c/commit/638f2aa)\
  2018-05-18 12:24:56 +0200
  * Revert "Fix for [CONC-332](https://jira.mariadb.org/browse/CONC-332):"
* [Revision #0c29fdb](https://github.com/mariadb-corporation/mariadb-connector-c/commit/0c29fdb)\
  2018-05-17 07:10:15 +0200
  * Fix for [CONC-332](https://jira.mariadb.org/browse/CONC-332):
* [Revision #bb8655d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/bb8655d)\
  2018-05-14 17:56:08 +0200
  * Merge pull request #52 from twocode/addhostname
* [Revision #fe2d323](https://github.com/mariadb-corporation/mariadb-connector-c/commit/fe2d323)\
  2018-05-11 10:09:04 +0800
  * Use \_server\_host per discussion.
* [Revision #ba9f5f4](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ba9f5f4)\
  2018-05-10 10:09:32 +0000
  * Add host name to session attributes
* [Revision #e6f0fe5](https://github.com/mariadb-corporation/mariadb-connector-c/commit/e6f0fe5)\
  2018-05-14 16:12:56 +0200
  * Merge pull request #48 from rusher/master
* [Revision #05fded6](https://github.com/mariadb-corporation/mariadb-connector-c/commit/05fded6)\
  2018-05-04 11:16:18 +0200
  * \[TODO-1299] testing connector against last server build. Those tests permit to check early regression and might failed, so tagged as "Allowed Failures" on travis
* [Revision #255c4b0](https://github.com/mariadb-corporation/mariadb-connector-c/commit/255c4b0)\
  2018-05-11 07:15:23 +0200
  * TLS/SSL test fixes: - create ssluser to prevent failing test on new db instance - skip tls\_version test when using OpenSSL 1.1.1
* [Revision #1fe8a06](https://github.com/mariadb-corporation/mariadb-connector-c/commit/1fe8a06)\
  2018-05-09 13:17:53 +0200
  * Fix for [CONC-330](https://jira.mariadb.org/browse/CONC-330): Build fails if TLS was disabled (CMake option -DWITH\_SSL=OFF)
* [Revision #ec985d9](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ec985d9)\
  2018-05-02 11:40:42 +0200
  * [CONC-327](https://jira.mariadb.org/browse/CONC-327): Add support for !include an !includedir in configuration files
* [Revision #f8ea603](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f8ea603)\
  2018-04-24 18:26:07 +0200
  * [CONC-321](https://jira.mariadb.org/browse/CONC-321): Added support for OpenSSL 1.1.1 Tested with OpenSSL 1.1.1 beta 5. For testing TLS v13 the server needs to be patched with patch attached to [MDEV-15996](https://jira.mariadb.org/browse/MDEV-15996).
* [Revision #9ba0d73](https://github.com/mariadb-corporation/mariadb-connector-c/commit/9ba0d73)\
  2018-04-24 18:02:43 +0200
  * Merge commit 'fbca960c33846147a5da301977df253e5a912527'
* [Revision #fbca960](https://github.com/mariadb-corporation/mariadb-connector-c/commit/fbca960)\
  2018-04-24 17:20:07 +0200
  * Fixed another logical-op warning if EAGAIN and EWOULDBLOCK have same values.
* [Revision #1c194bd](https://github.com/mariadb-corporation/mariadb-connector-c/commit/1c194bd)\
  2018-04-24 17:18:31 +0200
  * Support for -Wlogical-op flag and warning fixes (Patch provided by Monty)
* [Revision #443f756](https://github.com/mariadb-corporation/mariadb-connector-c/commit/443f756)\
  2018-04-24 17:17:20 +0200
  * Revert "Added -Wlogical-op warning flag and fixed two warnings"
* [Revision #2198a01](https://github.com/mariadb-corporation/mariadb-connector-c/commit/2198a01)\
  2018-04-24 17:04:59 +0200
  * Added -Wlogical-op warning flag and fixed two warnings
* [Revision #a9e2ad9](https://github.com/mariadb-corporation/mariadb-connector-c/commit/a9e2ad9)\
  2018-04-24 14:25:48 +0200
  * Bumped version number to 3.0.5
* [Revision #cb69283](https://github.com/mariadb-corporation/mariadb-connector-c/commit/cb69283)\
  2018-04-24 12:22:12 +0200
  * merge commit '966ad42cee3de834a8223ac89f15c32972e1abd3'
* [Revision #4fe6575](https://github.com/mariadb-corporation/mariadb-connector-c/commit/4fe6575)\
  2018-04-23 12:12:31 +0200
  * Build fix if Connector/C is built as submodule
* [Revision #53a1101](https://github.com/mariadb-corporation/mariadb-connector-c/commit/53a1101)\
  2018-04-23 07:27:13 +0200
  * Pushed version number to 10.3.6
* [Revision #89e27e9](https://github.com/mariadb-corporation/mariadb-connector-c/commit/89e27e9)\
  2018-04-23 03:47:07 +0200
  * Windows build fix: The msi installer package didn't contain all plugins
* [Revision #f46244c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f46244c)\
  2018-04-22 14:44:42 +0200
  * Fixed authentication plugin configuration
* [Revision #441ce64](https://github.com/mariadb-corporation/mariadb-connector-c/commit/441ce64)\
  2018-04-18 18:53:08 +1000
  * [MDEV-15655](https://jira.mariadb.org/browse/MDEV-15655): abstract socket support - limit length
* [Revision #c8464af](https://github.com/mariadb-corporation/mariadb-connector-c/commit/c8464af)\
  2018-04-22 08:49:34 +0200
  * Merge pull request #47 from MariaDB/connector\_c\_3.0-lawrin
* [Revision #9a50a7d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/9a50a7d)\
  2018-04-19 17:32:05 +0200
  * Corrections of the codepage number for some collations.
* [Revision #264cfa7](https://github.com/mariadb-corporation/mariadb-connector-c/commit/264cfa7)\
  2018-04-22 08:40:19 +0200
  * Build fix: Separate arguments if SIGN\_OPTIONS was specified via cmake variable
* [Revision #4adf242](https://github.com/mariadb-corporation/mariadb-connector-c/commit/4adf242)\
  2018-04-20 07:29:50 +0200
  * For expired password test check error codes ER\_MUST\_CHANGE\_PASSWORD (=1820) and ER\_MUST\_CHANGE\_PASSWORD\_LOGIN (=1862)
* [Revision #3f43953](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3f43953)\
  2018-04-20 07:19:40 +0200
  * Fixed test case for expired password Added test case for [ODBC-138](https://jira.mariadb.org/browse/ODBC-138)
* [Revision #60e5dee](https://github.com/mariadb-corporation/mariadb-connector-c/commit/60e5dee)\
  2018-04-18 07:13:21 +0200
  * Disable cipher mapping test - depending on used OpenSSL version (in client and/or server) several cipher suites might be disabled or removed.
* [Revision #0e2d913](https://github.com/mariadb-corporation/mariadb-connector-c/commit/0e2d913)\
  2018-04-18 06:34:50 +0200
  * Merge branch 'master' into 10.2-server
* [Revision #401f6e1](https://github.com/mariadb-corporation/mariadb-connector-c/commit/401f6e1)\
  2018-04-12 17:17:04 +0200
  * Merge pull request #44 from luzpaz/10.2-misc-typos
* [Revision #7aa3473](https://github.com/mariadb-corporation/mariadb-connector-c/commit/7aa3473)\
  2018-03-30 06:45:19 -0400
  * Fixes misc. typos
* [Revision #21df0ad](https://github.com/mariadb-corporation/mariadb-connector-c/commit/21df0ad)\
  2018-02-09 20:19:45 +0100
  * Plugin configuration fixes:
* [Revision #35d891a](https://github.com/mariadb-corporation/mariadb-connector-c/commit/35d891a)\
  2018-02-08 22:38:58 +0000
  * Fix clang on Windows warnings
* [Revision #209c4f8](https://github.com/mariadb-corporation/mariadb-connector-c/commit/209c4f8)\
  2018-02-01 11:10:06 +0100
  * Travis fixes (TLS/SSL)
* [Revision #fca3ef7](https://github.com/mariadb-corporation/mariadb-connector-c/commit/fca3ef7)\
  2018-01-28 16:48:59 +0100
  * Travis fix: Build Connector/C with OpenSSL
* [Revision #ced8e35](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ced8e35)\
  2018-01-26 15:01:12 +0100
  * Travis fixes
* [Revision #6fcec8f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6fcec8f)\
  2018-01-24 09:18:27 +0100
  * Revert "Fix for [MDEV-14977](https://jira.mariadb.org/browse/MDEV-14977):"
* [Revision #3524f5f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3524f5f)\
  2018-01-24 08:49:02 +0100
  * Fix for [MDEV-14977](https://jira.mariadb.org/browse/MDEV-14977):
* [Revision #7b46186](https://github.com/mariadb-corporation/mariadb-connector-c/commit/7b46186)\
  2018-01-22 18:39:19 +0100
  * Added support for travis
* [Revision #00903bb](https://github.com/mariadb-corporation/mariadb-connector-c/commit/00903bb)\
  2018-01-21 17:27:04 +0100
  * Fix for [CONC-294](https://jira.mariadb.org/browse/CONC-294): Since we already called plugin->close function we need to prevent that mysql\_close\_slow\_part (which sends COM\_QUIT to the server) will be handled by plugin (which might end up in crashing the application)
* [Revision #1a1499c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/1a1499c)\
  2018-01-19 07:29:51 +0100
  * Bumped version number to 3.0.4
* [Revision #c1a5ed4](https://github.com/mariadb-corporation/mariadb-connector-c/commit/c1a5ed4)\
  2018-01-17 12:43:58 +0100
  * Added installation layout for Debian (-DINSTALL\_LAYOUT=DEB)
* [Revision #d3a6061](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d3a6061)\
  2018-01-17 08:01:21 +0100
  * Changed/fixed Wix installer images
* [Revision #5c16523](https://github.com/mariadb-corporation/mariadb-connector-c/commit/5c16523)\
  2018-01-16 15:24:54 +0100
  * Fix for [MDEV-10361](https://jira.mariadb.org/browse/MDEV-10361): Don't try to reconnect twice: if mysql->options.reconnect is set, ma\_simple\_command already tries to reconnect, so there is no need to reconnect in mysql\_ping again
* [Revision #0335873](https://github.com/mariadb-corporation/mariadb-connector-c/commit/0335873)\
  2017-12-25 16:10:20 +0100
  * [CONC-299](https://jira.mariadb.org/browse/CONC-299): Add support for missing collation and character sets
* [Revision #edeffbf](https://github.com/mariadb-corporation/mariadb-connector-c/commit/edeffbf)\
  2018-01-16 11:45:49 +0100
  * If gnutls pkg-config file is missing, Cmake's module FindGNUTLS.cmake will not determine and check the version number. If GNUTLS\_VERSION\_STRING could not be determined, we try to get the version string by running gnutls\_check\_version (try\_run)
* [Revision #7fab2ec](https://github.com/mariadb-corporation/mariadb-connector-c/commit/7fab2ec)\
  2018-01-15 18:56:14 +0100
  * Merge branch 'master' of [mariadb-connector-c](https://github.com/MariaDB/mariadb-connector-c)
* [Revision #1ea0354](https://github.com/mariadb-corporation/mariadb-connector-c/commit/1ea0354)\
  2018-01-15 18:18:42 +0100
  * Merge pull request #31 from kevgs/clang\_tsan
* [Revision #7f9629a](https://github.com/mariadb-corporation/mariadb-connector-c/commit/7f9629a)\
  2017-10-06 00:38:00 +0300
  * fix TSAN build with Clang
* [Revision #c066666](https://github.com/mariadb-corporation/mariadb-connector-c/commit/c066666)\
  2018-01-15 18:55:55 +0100
  * updated README
* [Revision #ddcb21c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ddcb21c)\
  2018-01-15 17:57:29 +0100
  * Skip test for SESSION\_TRACK\_STATE\_CHANGE if the test server is a MySQL server, since MySQL 5.7 (and above) doesn't send this flag after set session session\_track\_state\_change=1
* [Revision #1af934e](https://github.com/mariadb-corporation/mariadb-connector-c/commit/1af934e)\
  2018-01-15 17:42:37 +0100
  * Merge branch 'master' of [mariadb-connector-c](https://github.com/MariaDB/mariadb-connector-c)
* [Revision #9f9a1c5](https://github.com/mariadb-corporation/mariadb-connector-c/commit/9f9a1c5)\
  2018-01-15 17:41:19 +0100
  * Merge pull request #39 from InuSasha/patch-1
* [Revision #642320e](https://github.com/mariadb-corporation/mariadb-connector-c/commit/642320e)\
  2018-01-04 22:00:40 +0100
  * fix typo in plugins.cmake
* [Revision #86dacf3](https://github.com/mariadb-corporation/mariadb-connector-c/commit/86dacf3)\
  2018-01-15 12:25:52 +0100
  * Removed determination of programname and reading configuration options from section \[programname] when parameter NULL was passed to mysql\_options(, MYSQL\_READ\_DEFAULT\_GROUP)
* [Revision #b15a7aa](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b15a7aa)\
  2018-01-11 12:10:05 +0200
  * Remove unused definitions
* [Revision #794689b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/794689b)\
  2018-01-10 16:37:15 +0000
  * Fix warnings about RETSIGTYPE/RETQSORTTYPE redefinition when using libmariadb headers together with server's
* [Revision #2e42f7a](https://github.com/mariadb-corporation/mariadb-connector-c/commit/2e42f7a)\
  2018-01-14 07:34:01 +0100
  * Test cleanup: - removed unused test for old sqlite3 module - to avoid warnings and make code more readable mysql\_stmt\_prepare and mysql\_real\_query now use the SL (string and length) macro.
* [Revision #64cf572](https://github.com/mariadb-corporation/mariadb-connector-c/commit/64cf572)\
  2018-01-04 15:43:44 +0000
  * support build with static openssl on Windows
* [Revision #75ca3c1](https://github.com/mariadb-corporation/mariadb-connector-c/commit/75ca3c1)\
  2018-01-09 18:13:54 +0100
  * TLS/SSL fixes: - don't run fingerprint and passphrase protected tests if the corresponding files (sha1 and encrypted client key) are not found in CERT\_PATH - don't overwrite SSL errors if handshake failed - Use gnutls read/write instead of pvio
* [Revision #5abcb1b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/5abcb1b)\
  2018-01-08 13:57:53 +0100
  * [CONC-302](https://jira.mariadb.org/browse/CONC-302):
* [Revision #9345d74](https://github.com/mariadb-corporation/mariadb-connector-c/commit/9345d74)\
  2018-01-08 12:39:48 +0100
  * Merge branch 'master' of [mariadb-connector-c](https://github.com/MariaDB/mariadb-connector-c)
* [Revision #74b1ba2](https://github.com/mariadb-corporation/mariadb-connector-c/commit/74b1ba2)\
  2018-01-08 12:31:33 +0100
  * removed unused function char\_val from ma\_password.c
* [Revision #72b38f5](https://github.com/mariadb-corporation/mariadb-connector-c/commit/72b38f5)\
  2018-01-08 12:31:33 +0100
  * removed unused function char\_val from ma\_password.c
* [Revision #b00cdcd](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b00cdcd)\
  2017-12-22 09:00:13 +0100
  * Merge branch 'master' of [mariadb-connector-c](https://github.com/MariaDB/mariadb-connector-c)
* [Revision #3e164b5](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3e164b5)\
  2017-12-20 10:01:32 +0100
  * Fix test failues if testing against server < 10.2
* [Revision #2314598](https://github.com/mariadb-corporation/mariadb-connector-c/commit/2314598)\
  2017-12-22 08:59:32 +0100
  * Fix for [CONC-301](https://jira.mariadb.org/browse/CONC-301) (manually merged from 2.3.5)
* [Revision #6d2fb01](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6d2fb01)\
  2017-12-15 10:48:42 +0100
  * [MDEV-14647](https://jira.mariadb.org/browse/MDEV-14647): Fixed crash when client receives extended ok packet with SESSION\_TRACK\_STATE\_CHANGE information flag.
* [Revision #434b67e](https://github.com/mariadb-corporation/mariadb-connector-c/commit/434b67e)\
  2017-12-04 19:45:07 +0100
  * Fix for [CONC-297](https://jira.mariadb.org/browse/CONC-297): MariaDB Connector/C was not compatible to libmysql when passing value for MYSQL\_OPT\_LOCAL\_INFILE. According to the documentatin local infile will be enabled if a NULL pointer was passed or a pointer to an unsigned integer which value is > 0. Connector/C expected a bool pointer, which ends up in wrong results on big endian systems.
* [Revision #87b863e](https://github.com/mariadb-corporation/mariadb-connector-c/commit/87b863e)\
  2017-11-27 19:02:37 +0100
  * Windows build fix: init\_once assignment needs to be casted (C99).
* [Revision #14fe661](https://github.com/mariadb-corporation/mariadb-connector-c/commit/14fe661)\
  2017-11-27 18:22:05 +0100
  * Fix for [MDEV-14514](https://jira.mariadb.org/browse/MDEV-14514): Wrong exit code when an invalid option was passed to mariadb\_config.
* [Revision #c849a21](https://github.com/mariadb-corporation/mariadb-connector-c/commit/c849a21)\
  2017-11-27 17:31:16 +0100
  * Fix for FreeBSD build: PTHREAD\_ONCE\_INIT is defined as a struct, so we need to cast it.
* [Revision #a81a799](https://github.com/mariadb-corporation/mariadb-connector-c/commit/a81a799)\
  2017-11-12 21:29:10 +0000
  * [MDEV-11546](https://jira.mariadb.org/browse/MDEV-11546) main.ssl\_7937 failed with timeout in buildbot on Windows
* [Revision #15e9ee4](https://github.com/mariadb-corporation/mariadb-connector-c/commit/15e9ee4)\
  2017-11-22 09:50:12 +0100
  * Fix for [CONC-277](https://jira.mariadb.org/browse/CONC-277): For backwards compatibiliry we now allow reinitialization of client library by setting init\_once to zero in mysql\_server\_end() function.
* [Revision #683e2f3](https://github.com/mariadb-corporation/mariadb-connector-c/commit/683e2f3)\
  2017-11-18 16:20:33 +0100
  * Fix for Solaris build ([MDEV-11603](https://jira.mariadb.org/browse/MDEV-11603))
* [Revision #77490eb](https://github.com/mariadb-corporation/mariadb-connector-c/commit/77490eb)\
  2017-11-08 09:12:42 +0100
  * Fix windows build: For using \_malloca (instead of deprecated alloca) we need to include malloc.h
* [Revision #b825f34](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b825f34)\
  2017-11-08 09:09:52 +0100
  * Revert "Fix windows build: Use \_malloca instead of alloca"
* [Revision #b21e60a](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b21e60a)\
  2017-11-08 08:51:36 +0100
  * Fix windows build: Use \_malloca instead of alloca
* [Revision #1e6cdb8](https://github.com/mariadb-corporation/mariadb-connector-c/commit/1e6cdb8)\
  2017-11-08 04:56:04 +0100
  * [CONC-292](https://jira.mariadb.org/browse/CONC-292): Fxed malloc result check in dynamic columns
* [Revision #c979378](https://github.com/mariadb-corporation/mariadb-connector-c/commit/c979378)\
  2017-11-07 18:45:08 +0100
  * Added additional test (invalid user)
* [Revision #771a409](https://github.com/mariadb-corporation/mariadb-connector-c/commit/771a409)\
  2017-11-07 18:36:14 +0100
  * Implementation for [MDEV-9059](https://jira.mariadb.org/browse/MDEV-9059):
* [Revision #b40058f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b40058f)\
  2017-10-28 16:46:49 +0200
  * Fix for [MDEV-14165](https://jira.mariadb.org/browse/MDEV-14165):
* [Revision #5d920a9](https://github.com/mariadb-corporation/mariadb-connector-c/commit/5d920a9)\
  2017-10-26 18:34:05 +0200
  * [CONC-290](https://jira.mariadb.org/browse/CONC-290): Return error (=1) instead of exiting.
* [Revision #12a6865](https://github.com/mariadb-corporation/mariadb-connector-c/commit/12a6865)\
  2017-10-25 19:07:17 +0200
  * Fix compiler warning
* [Revision #8ea4d2f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/8ea4d2f)\
  2017-10-23 11:04:14 +0200
  * [MDEV-14101](https://jira.mariadb.org/browse/MDEV-14101): tls-version
* [Revision #9272a18](https://github.com/mariadb-corporation/mariadb-connector-c/commit/9272a18)\
  2017-10-17 15:53:45 +0200
  * Provide details about TLS/SSL library in use
* [Revision #d67ee8b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d67ee8b)\
  2017-10-15 09:41:12 +0200
  * Revert "[MDEV-14027](https://jira.mariadb.org/browse/MDEV-14027): Determine TLS/SSL library version"
* [Revision #113418c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/113418c)\
  2017-10-15 06:01:59 +0200
  * [MDEV-14027](https://jira.mariadb.org/browse/MDEV-14027): Determine TLS/SSL library version
* [Revision #5e32110](https://github.com/mariadb-corporation/mariadb-connector-c/commit/5e32110)\
  2017-10-12 12:15:39 +0200
  * Build fix: When building as subproject inside server tree, ZLIB\_FOUND was already set by parent, so we need additionally check if WITH\_EXTERNAL\_ZLIB was specified. - New server status flags Added SERVER\_STATUS\_ANSI\_QUOTES and SERVER\_STATUS\_IN\_TRANS\_READONLY
* [Revision #6d24e0b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6d24e0b)\
  2017-10-12 09:56:50 +0200
  * Added missing dependency for zlib (WITH\_EXTERNAL\_ZLIB=ON) Added CC\_SOURCE\_REVISION definition (mariadb\_version.h)
* [Revision #cd46b30](https://github.com/mariadb-corporation/mariadb-connector-c/commit/cd46b30)\
  2017-10-10 12:20:37 +0200
  * Merge branch 'master' of [mariadb-connector-c](https://github.com/MariaDB/mariadb-connector-c)
* [Revision #0334aa4](https://github.com/mariadb-corporation/mariadb-connector-c/commit/0334aa4)\
  2017-08-14 17:23:42 +0200
  * Implementation and testcase for [CONC-275](https://jira.mariadb.org/browse/CONC-275) - skipping particular paramset in bulk operation - with help of special indicator value STMT\_INDICATOR\_IGNORE\_ROW set in any column of the row. The revision also adds some (mainly VS specific) file/dirs definitions to .gitignore to make 'gid status' usable on Windows, and the typo in bulk1 testsuite
* [Revision #6329049](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6329049)\
  2017-10-10 12:19:01 +0200
  * [CONC-286](https://jira.mariadb.org/browse/CONC-286): - Force TLS/SSL connection if finger print options were specified - Allow hex finger prints with colon separated 2 digit numbers
* [Revision #2546445](https://github.com/mariadb-corporation/mariadb-connector-c/commit/2546445)\
  2017-10-02 09:08:03 +0200
  * [CONC-282](https://jira.mariadb.org/browse/CONC-282): Connector/C now provides additional information for package version mariadb\_config --cc\_version lists the package version Beside MARIADB\_PACKAGE\_VERSION numeric representation MARIADB\_PACKAGE\_VERSION\_ID can be used now within preprocessor directives
* [Revision #2e39bb7](https://github.com/mariadb-corporation/mariadb-connector-c/commit/2e39bb7)\
  2017-10-01 05:57:58 +0200
  * Fixed test case name for [CONC-281](https://jira.mariadb.org/browse/CONC-281)
* [Revision #2083aa9](https://github.com/mariadb-corporation/mariadb-connector-c/commit/2083aa9)\
  2017-09-30 14:10:01 +0200
  * Fix for [MDEV-13959](https://jira.mariadb.org/browse/MDEV-13959): duplicated if condition in mariadb\_dyncol.c
* [Revision #5bf7813](https://github.com/mariadb-corporation/mariadb-connector-c/commit/5bf7813)\
  2017-09-29 11:12:36 +0200
  * Fix parentheses ([MDEV-13956](https://jira.mariadb.org/browse/MDEV-13956))
* [Revision #cb02751](https://github.com/mariadb-corporation/mariadb-connector-c/commit/cb02751)\
  2017-09-25 19:16:55 +0200
  * Update year in mariadb\_config output
* [Revision #7d6101d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/7d6101d)\
  2017-09-15 01:06:05 +0200
  * define MARIADB\_BASE\_VERSION in mariadb\_version.h
* [Revision #3d11d0f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3d11d0f)\
  2017-09-09 16:03:08 +0200
  * [MDEV-13588](https://jira.mariadb.org/browse/MDEV-13588) /usr/lib/x86\_64-linux-gnu/libmariadbclient.so.18: version \`libmariadbclient\_18' not found
* [Revision #17110fb](https://github.com/mariadb-corporation/mariadb-connector-c/commit/17110fb)\
  2017-09-25 13:51:01 +0200
  * Fix for [CONC-282](https://jira.mariadb.org/browse/CONC-282): mysql\_stmt\_fetch\_column doesn't work with prior call to mysql\_stmt\_store\_result - If no bind variables were bound or the function mysql\_stmt\_store\_result was not called before, the internal bind variables (stmt->bind) was not filled (lengths and null values)
* [Revision #f9a6b8e](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f9a6b8e)\
  2017-09-08 12:19:32 +0200
  * Merge branch 'master' of [mariadb-connector-c](https://github.com/MariaDB/mariadb-connector-c)
* [Revision #85d150e](https://github.com/mariadb-corporation/mariadb-connector-c/commit/85d150e)\
  2017-09-07 17:35:35 +0200
  * Export _mysql\_client\_plugin\_declaration_ from auth\_gssapi\_client.so
* [Revision #d76663a](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d76663a)\
  2017-09-08 12:18:37 +0200
  * Added missing break in mysql\_get\_infov
* [Revision #cd50748](https://github.com/mariadb-corporation/mariadb-connector-c/commit/cd50748)\
  2017-08-31 07:54:21 +0200
  * Fixed memory leak and added missing break in dynamic column conversion function
* [Revision #a2b0bcd](https://github.com/mariadb-corporation/mariadb-connector-c/commit/a2b0bcd)\
  2017-08-24 18:05:58 +0200
  * Fix for [CONC-276](https://jira.mariadb.org/browse/CONC-276): client library crashes on Windows after TLS reconnect: The connection pointer mysql is now no longer part (and doesn't need to be updated) of schannel security context, since it can be obtained directly from tls container.
* [Revision #482a0b6](https://github.com/mariadb-corporation/mariadb-connector-c/commit/482a0b6)\
  2017-07-25 09:45:16 +0200
  * Merge branch 'master' of [mariadb-connector-c](https://github.com/MariaDB/mariadb-connector-c)
* [Revision #ce01b63](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ce01b63)\
  2017-07-21 08:06:53 +0000
  * Merge branch 'master' of [mariadb-connector-c](https://github.com/MariaDB/mariadb-connector-c)
* [Revision #b481265](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b481265)\
  2017-07-19 13:50:40 +0200
  * Bumped version number to 3.0.3
* [Revision #bc2d6df](https://github.com/mariadb-corporation/mariadb-connector-c/commit/bc2d6df)\
  2017-07-21 07:53:03 +0000
  * Warning fixes for Win64 build
* [Revision #843c492](https://github.com/mariadb-corporation/mariadb-connector-c/commit/843c492)\
  2017-07-25 09:43:55 +0200
  * Fix for [CONC-271](https://jira.mariadb.org/browse/CONC-271): RPM layout now works for other 64-bit architectures than x86\_64. Thx to Michal Schorn for contributing this patch.
* [Revision #35d6fb1](https://github.com/mariadb-corporation/mariadb-connector-c/commit/35d6fb1)\
  2017-07-19 11:29:42 +0200
  * Fixed windows build: taget name for sha256 password plugin wasn't specified
* [Revision #d9bc990](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d9bc990)\
  2017-07-18 16:15:36 +0200
  * Fix for [MDEV-13317](https://jira.mariadb.org/browse/MDEV-13317): PHP5 crashes
* [Revision #e9b7f21](https://github.com/mariadb-corporation/mariadb-connector-c/commit/e9b7f21)\
  2017-07-12 06:32:35 +0200
  * added my.cnf option server-public-key-path for sha256 authentication plugin
* [Revision #ae06903](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ae06903)\
  2017-07-04 11:42:05 +0200
  * followup for e2df6d2: default directories, files, and groups
* [Revision #3f356c0](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3f356c0)\
  2017-07-07 11:18:24 +0200
  * Fix for [MDEV-13270](https://jira.mariadb.org/browse/MDEV-13270): Wrong output for mariadb\_config on OSX
* [Revision #0f11352](https://github.com/mariadb-corporation/mariadb-connector-c/commit/0f11352)\
  2017-07-04 13:56:38 +0200
  * Fixed compiler warnings
* [Revision #c596c16](https://github.com/mariadb-corporation/mariadb-connector-c/commit/c596c16)\
  2017-07-01 15:39:08 +0200
  * Fix for [CONC-252](https://jira.mariadb.org/browse/CONC-252): All functions which are supported by libmysql use now unsigned long as length parameter instead of size\_t
* [Revision #3fab8ce](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3fab8ce)\
  2017-07-01 15:36:47 +0200
  * Fix for [MDEV-12889](https://jira.mariadb.org/browse/MDEV-12889): Added version info for shared object: libmysqlclient\_18 node contains all symbols for libmysql compatibiliry libmariadb\_3 node contains all mariadb specific symbols which are not supported by libmysql
* [Revision #2d27bd7](https://github.com/mariadb-corporation/mariadb-connector-c/commit/2d27bd7)\
  2017-06-30 14:02:47 +0200
  * Merge remote-tracking branch 'origin/10.2-server'
* [Revision #90fd0cd](https://github.com/mariadb-corporation/mariadb-connector-c/commit/90fd0cd)\
  2017-06-25 14:14:55 +0200
  * Fix for [MDEV-12965](https://jira.mariadb.org/browse/MDEV-12965) and [MDEV-13100](https://jira.mariadb.org/browse/MDEV-13100): If no configuration file and no configuration group was specified, Connector/C ddoesn't read any configurationm files. By default the follwing groups will be read: - client - client-server - client-mariadb

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
