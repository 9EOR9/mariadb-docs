# MariaDB Connector/C 3.1.5 Changelog

The most recent [_**Stable**_](../../../../mariadb-release-criteria.md) _**(GA)**_ release of MariaDB Connector/C is:[**MariaDB Connector/C 3.4.5**](../../mariadb-connector-c-3-4-release-notes/mariadb-connector-c-3-4-5-release-notes.md)

[Download](https://mariadb.com/downloads/#connectors)[Release Notes](../../mariadb-connector-c-31-release-notes/mariadb-connector-c-315-release-notes.md)[Changelog](mariadb-connector-c-315-changelog.md)[About MariaDB Connector/C](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-c/README.md)

**Release date:** 11 Nov 2019

For the highlights of this release, see the[release notes](../../mariadb-connector-c-31-release-notes/mariadb-connector-c-315-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-c/) you can view more\
details of the revision and view diffs of the code modified in that revision.

* [Revision #980f2db](https://github.com/mariadb-corporation/mariadb-connector-c/commit/980f2db)\
  2019-10-31 06:06:39 +0100
  * Typo fixed
* [Revision #9473573](https://github.com/mariadb-corporation/mariadb-connector-c/commit/9473573)\
  2019-10-22 17:36:22 +0200
  * Added test for testing maximun number of parmeters in binary protocol.
* [Revision #66d449f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/66d449f)\
  2019-10-17 18:41:58 +0200
  * Added test for [CONC-443](https://jira.mariadb.org/browse/CONC-443)
* [Revision #a0cbee9](https://github.com/mariadb-corporation/mariadb-connector-c/commit/a0cbee9)\
  2019-10-11 16:39:01 +0200
  * Schannel fix for 9ba8e32f6d0fe449114d8eb369cf29303257b460
* [Revision #0235aa6](https://github.com/mariadb-corporation/mariadb-connector-c/commit/0235aa6)\
  2019-10-08 14:18:01 +0200
  * Fixed gcc warning (missing const qualifier)
* [Revision #e37e08b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/e37e08b)\
  2019-10-08 14:13:16 +0200
  * Merge branch '3.1' of [mariadb-connector-c](https://github.com/MariaDB/mariadb-connector-c) into 3.1
* [Revision #a44b691](https://github.com/mariadb-corporation/mariadb-connector-c/commit/a44b691)\
  2019-10-08 14:11:46 +0200
  * Merge pull request #121 from grooverdan/solaris-fix
* [Revision #aacc722](https://github.com/mariadb-corporation/mariadb-connector-c/commit/aacc722)\
  2019-09-27 08:40:28 +1000
  * gssapi: fix include path for Solaris
* [Revision #44a5980](https://github.com/mariadb-corporation/mariadb-connector-c/commit/44a5980)\
  2019-10-08 14:04:42 +0200
  * Merge pull request #120 from yurriy/caching\_sha2\_password-fix
* [Revision #538da15](https://github.com/mariadb-corporation/mariadb-connector-c/commit/538da15)\
  2019-09-09 08:53:05 +0300
  * fixed caching\_sha2\_password behaviour when SSL is enabled
* [Revision #e8023f3](https://github.com/mariadb-corporation/mariadb-connector-c/commit/e8023f3)\
  2019-10-08 14:12:57 +0200
  * Added check for getpwuid() function
* [Revision #8e6812b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/8e6812b)\
  2019-10-07 13:30:49 +0200
  * Fix plugin directory: Instead of PLUGINDIR we need to set INSTALL\_PLUGINDIR (install.cmake)
* [Revision #c6403c4](https://github.com/mariadb-corporation/mariadb-connector-c/commit/c6403c4)\
  2019-10-02 11:51:04 +0200
  * Revert "Added optimization flag -O2 for GCC debug builds"
* [Revision #636d44a](https://github.com/mariadb-corporation/mariadb-connector-c/commit/636d44a)\
  2019-09-30 09:11:21 +0200
  * Fix problem with warnings of new compilers.
* [Revision #9ba8e32](https://github.com/mariadb-corporation/mariadb-connector-c/commit/9ba8e32)\
  2019-09-21 09:17:36 +0200
  * Fix for [CONC-418](https://jira.mariadb.org/browse/CONC-418):
* [Revision #ee91b2c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ee91b2c)\
  2019-09-19 14:56:53 +0200
  * [ODBC-440](https://jira.mariadb.org/browse/ODBC-440) Typo in sha256\_password cmake config
* [Revision #de04c2e](https://github.com/mariadb-corporation/mariadb-connector-c/commit/de04c2e)\
  2019-09-19 08:50:55 +0200
  * Workaround for [CONC-417](https://jira.mariadb.org/browse/CONC-417), [MDEV-13492](https://jira.mariadb.org/browse/MDEV-13492)
* [Revision #261a5c4](https://github.com/mariadb-corporation/mariadb-connector-c/commit/261a5c4)\
  2019-09-15 14:07:53 +0200
  * Fix for [CONC-437](https://jira.mariadb.org/browse/CONC-437): attempt to reassign symbol 'mysql\_get\_timeout\_value' of version 'libmysqlclient\_18' to version 'libmariadb\_3'
* [Revision #4a1f45b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/4a1f45b)\
  2019-09-11 13:45:20 -0400
  * bump the VERSION
* [Revision #662ab11](https://github.com/mariadb-corporation/mariadb-connector-c/commit/662ab11)\
  2019-09-09 10:25:46 +0300
  * Null merge
* [Revision #dc271e5](https://github.com/mariadb-corporation/mariadb-connector-c/commit/dc271e5)\
  2019-08-19 16:59:40 +0300
  * Relax the linker config for all sanitizers
* [Revision #de57d6a](https://github.com/mariadb-corporation/mariadb-connector-c/commit/de57d6a)\
  2019-09-04 11:16:15 +0300
  * Fix GCC 8 -Wstringop-truncation
* [Revision #9faaea3](https://github.com/mariadb-corporation/mariadb-connector-c/commit/9faaea3)\
  2019-09-04 09:36:20 +0200
  * Fix gcc warnings
* [Revision #f0432c9](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f0432c9)\
  2019-09-04 09:09:53 +0200
  * Added optimization flag -O2 for GCC debug builds
* [Revision #0c29493](https://github.com/mariadb-corporation/mariadb-connector-c/commit/0c29493)\
  2019-09-04 09:07:25 +0200
  * Revert "Added -O2 option for gcc debug build"
* [Revision #f7322cc](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f7322cc)\
  2019-09-04 09:04:00 +0200
  * Added -O2 option for gcc debug build

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
