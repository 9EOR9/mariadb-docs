# MariaDB Connector/C 3.0.4 Changelog

The most recent [_**Stable**_](../../../../mariadb-release-criteria.md) _**(GA)**_ release of MariaDB Connector/C is:[**MariaDB Connector/C 3.4.5**](../../mariadb-connector-c-3-4-release-notes/mariadb-connector-c-3-4-5-release-notes.md)

[Download](https://downloads.mariadb.org/connector-c/3.0.4)[Release Notes](../../mariadb-connector-c-30-release-notes/mariadb-connector-c-304-release-notes.md)[Changelog](mariadb-connector-c-304-changelog.md)[About MariaDB Connector/C](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-c/README.md)

**Release date:** 25 Apr 2018

For the highlights of this release, see the[release notes](../../mariadb-connector-c-30-release-notes/mariadb-connector-c-304-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-c/) you can view more\
details of the revision and view diffs of the code modified in that revision.

* [Revision #cb69283](https://github.com/mariadb-corporation/mariadb-connector-c/commit/cb69283)\
  2018-04-24 12:22:12 +0200
  * merge commit '966ad42cee3de834a8223ac89f15c32972e1abd3'
* [Revision #966ad42](https://github.com/mariadb-corporation/mariadb-connector-c/commit/966ad42)\
  2018-04-24 12:17:48 +0200
  * Fix for [CONC-326](https://jira.mariadb.org/browse/CONC-326): ssl\_thread\_init() uses wrong openssl threadid callback
* [Revision #d015c17](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d015c17)\
  2018-04-23 12:12:31 +0200
  * Build fix if Connector/C is built as submodule
* [Revision #aeeab3c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/aeeab3c)\
  2018-04-23 03:47:07 +0200
  * Windows build fix: The msi installer package didn't contain all plugins
* [Revision #4982ef9](https://github.com/mariadb-corporation/mariadb-connector-c/commit/4982ef9)\
  2018-04-22 14:44:42 +0200
  * Fixed authentication plugin configuration
* [Revision #698d361](https://github.com/mariadb-corporation/mariadb-connector-c/commit/698d361)\
  2018-04-22 08:49:00 +0200
  * Merge pull request #46 from grooverdan/[MDEV-15655](https://jira.mariadb.org/browse/MDEV-15655)\_fix
* [Revision #6d92946](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6d92946)\
  2018-04-18 18:53:08 +1000
  * [MDEV-15655](https://jira.mariadb.org/browse/MDEV-15655): abstract socket support - limit length
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
* [Revision #db1028f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/db1028f)\
  2018-04-17 11:31:45 +0200
  * Merge pull request #43 from grooverdan/[MDEV-15655](https://jira.mariadb.org/browse/MDEV-15655)-abstract-sockets
* [Revision #ab59771](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ab59771)\
  2018-03-25 13:56:05 +1100
  * [MDEV-15655](https://jira.mariadb.org/browse/MDEV-15655): Add Linux abstract socket support
* [Revision #f226c3b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f226c3b)\
  2018-04-17 10:35:49 +0200
  * Fix for [CONC-320](https://jira.mariadb.org/browse/CONC-320): Non blocking/asynchronous support for OpenSSL and GnuTLS. Please note that Schannel in asynchronous mode is not supported yet.
* [Revision #1b95733](https://github.com/mariadb-corporation/mariadb-connector-c/commit/1b95733)\
  2018-04-14 07:30:19 +0200
  * Windows build fixes: disable [CONC-317](https://jira.mariadb.org/browse/CONC-317) for windows platforms
* [Revision #b2e6ed0](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b2e6ed0)\
  2018-03-30 06:45:19 -0400
  * Fixes misc. typos
* [Revision #128d152](https://github.com/mariadb-corporation/mariadb-connector-c/commit/128d152)\
  2018-04-12 16:22:38 +0200
  * [CONC-322](https://jira.mariadb.org/browse/CONC-322): Correct handling of EAGAIN and EINPROGRESS in internal\_connect (socket) for non windows platforms. Kudos to Daniel Black for providing this patch.
* [Revision #cb0952a](https://github.com/mariadb-corporation/mariadb-connector-c/commit/cb0952a)\
  2018-04-12 08:52:21 +0200
  * Bumped version to 10.2.13 (only valid for standalone C/C build)
* [Revision #748e6fb](https://github.com/mariadb-corporation/mariadb-connector-c/commit/748e6fb)\
  2018-04-12 08:49:26 +0200
  * Fix for mariadb\_stmt\_execute: If compressed protocol is in use, mariadb\_stmt\_execute\_direct will be emulated by mysql\_stmt\_prepare and mysql\_stmt\_execute.
* [Revision #679b5b5](https://github.com/mariadb-corporation/mariadb-connector-c/commit/679b5b5)\
  2018-04-12 07:00:43 +0200
  * Fix for [CONC-317](https://jira.mariadb.org/browse/CONC-317): Parsing of configuration file fails if key/value pairs contain white spaces.
* [Revision #971fae7](https://github.com/mariadb-corporation/mariadb-connector-c/commit/971fae7)\
  2018-04-11 13:21:05 +0200
  * Fix for [CONC-315](https://jira.mariadb.org/browse/CONC-315): If no default client character set was specified, the utf8 character set will be used by default (instead of setting the client character set to server character set)
* [Revision #d3644be](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d3644be)\
  2018-04-07 07:42:59 +0200
  * [CONC-314](https://jira.mariadb.org/browse/CONC-314): Support for expired passwords (MySQL Server)
* [Revision #50d48e9](https://github.com/mariadb-corporation/mariadb-connector-c/commit/50d48e9)\
  2018-02-26 19:15:55 +0100
  * Reworked plugin interface
* [Revision #6e1dd7a](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6e1dd7a)\
  2018-03-26 20:37:56 +0000
  * Windows : if plugin cannot be loaded, provide a full path of the library in the error message, to simplify troubleshooting by users.
* [Revision #668757a](https://github.com/mariadb-corporation/mariadb-connector-c/commit/668757a)\
  2018-02-17 13:12:27 +0100
  * Merge pull request #40 from 9EOR9/10.2-server
* [Revision #80b2ae2](https://github.com/mariadb-corporation/mariadb-connector-c/commit/80b2ae2)\
  2018-02-17 12:22:18 +0100
  * If COM\_PING failed, check if reconnect option was set before calling mysql\_ping again.
* [Revision #83eef02](https://github.com/mariadb-corporation/mariadb-connector-c/commit/83eef02)\
  2018-02-16 13:05:35 +0100
  * Test fixes: for api functions which require string with length parameter (e.g. mysql\_real\_connect() or mysql\_stmt\_prepare() we now use the macro SL(string) which substitutes string and string length.
* [Revision #5a30aed](https://github.com/mariadb-corporation/mariadb-connector-c/commit/5a30aed)\
  2018-02-16 12:30:19 +0100
  * Fixed README
* [Revision #9296149](https://github.com/mariadb-corporation/mariadb-connector-c/commit/9296149)\
  2018-02-16 12:14:01 +0100
  * Travis and Appveyor integration: - added travis support - fixed appveyor settings - fixed some warnings (gcc 4.8) - removed sleep commands - disabled failing tests when running against MySQL server, mostly related to stored procedures and binary protocol - reverted fix for MDEV\_10361
* [Revision #da9ed3c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/da9ed3c)\
  2018-02-16 11:45:07 +0100
  * Added test for [MDEV-15133](https://jira.mariadb.org/browse/MDEV-15133)
* [Revision #eefaadf](https://github.com/mariadb-corporation/mariadb-connector-c/commit/eefaadf)\
  2018-02-16 11:43:32 +0100
  * Removed automatic detection of program name
* [Revision #67cc343](https://github.com/mariadb-corporation/mariadb-connector-c/commit/67cc343)\
  2018-02-14 19:35:16 +0000
  * Fix unit test. Fix send() prototype
* [Revision #9b37839](https://github.com/mariadb-corporation/mariadb-connector-c/commit/9b37839)\
  2018-02-12 17:05:01 +0000
  * Merge branch '10.2-wlad' into 10.2-server
* [Revision #7698e3f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/7698e3f)\
  2018-02-12 09:29:27 +0000
  * more clang fixes
* [Revision #db1a1a1](https://github.com/mariadb-corporation/mariadb-connector-c/commit/db1a1a1)\
  2018-02-12 09:29:27 +0000
  * more clang fixes
* [Revision #aed8005](https://github.com/mariadb-corporation/mariadb-connector-c/commit/aed8005)\
  2018-02-08 22:38:58 +0000
  * Fix clang on Windows warnings
* [Revision #058fc08](https://github.com/mariadb-corporation/mariadb-connector-c/commit/058fc08)\
  2018-01-26 13:04:37 +0100
  * Fixed 2 buffer overflows in unittests
* [Revision #9ee1861](https://github.com/mariadb-corporation/mariadb-connector-c/commit/9ee1861)\
  2018-01-21 17:27:04 +0100
  * Fix for [CONC-294](https://jira.mariadb.org/browse/CONC-294): Since we already called plugin->close function we need to prevent that mysql\_close\_slow\_part (which sends COM\_QUIT to the server) will be handled by plugin (which might end up in crashing the application)
* [Revision #adf7b56](https://github.com/mariadb-corporation/mariadb-connector-c/commit/adf7b56)\
  2018-01-16 15:24:54 +0100
  * Fix for [MDEV-10361](https://jira.mariadb.org/browse/MDEV-10361): Don't try to reconnect twice: if mysql->options.reconnect is set, ma\_simple\_command already tries to reconnect, so there is no need to reconnect in mysql\_ping again

{% @marketo/form formid="4316" formId="4316" %}
