# Connector/ODBC 3.1.2 Changelog

The most recent [_**Stable**_](../../../../community-server/about/release-criteria.md) _**(GA)**_ release of MariaDB Connector/ODBC is:[**MariaDB Connector/ODBC 3.2.5**](../../mariadb-connector-odbc-3-2-release-notes/mariadb-connector-odbc-3-2-5-release-notes.md)

[Download](https://mariadb.com/downloads/#connectors)[Release Notes](../../mariadb-connector-odbc-3-1-release-notes/mariadb-connector-odbc-3-1-2-release-notes.md)[Changelog](mariadb-connector-odbc-312-changelog.md)[About MariaDB Connector/ODBC](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-odbc/README.md)

**Release date:** 23 Jul 2019

For the highlights of this release, see the[release notes](../../mariadb-connector-odbc-3-1-release-notes/mariadb-connector-odbc-3-1-2-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-odbc) you can view more\
details of the revision and view diffs of the code modified in that revision.

* [Revision #9f043a2](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/9f043a2)\
  2019-07-15 15:54:00 +0200
  * C/C submodule -> v3.1.2. Added osx to the pkg name
* [Revision #925d222](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/925d222)\
  2019-07-11 11:49:20 +0200
  * [ODBC-255](https://jira.mariadb.org/browse/ODBC-255) MSI upgrades DSN's to new driver version
* [Revision #130a5b0](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/130a5b0)\
  2019-07-05 13:13:06 +0100
  * Fixed POSIX build error due to a type mismatch.
* [Revision #9d2f2c8](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/9d2f2c8)\
  2019-07-04 19:27:20 +0200
  * [ODBC-260](https://jira.mariadb.org/browse/ODBC-260) Removed all references to MYSQL internals
* [Revision #749d73d](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/749d73d)\
  2019-06-26 23:56:09 +0200
  * [ODBC-257](https://jira.mariadb.org/browse/ODBC-257) and [ODBC-258](https://jira.mariadb.org/browse/ODBC-258)
* [Revision #64bc771](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/64bc771)\
  2019-06-24 18:40:52 +0200
  * Updated Travis and AppVeyor configs to use 10.4
* [Revision #d8dc34c](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/d8dc34c)\
  2019-06-19 11:09:26 +0200
  * [ODBC-251](https://jira.mariadb.org/browse/ODBC-251) the testcase only + [ODBC-210](https://jira.mariadb.org/browse/ODBC-210)
* [Revision #bb8aaf1](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/bb8aaf1)\
  2019-06-13 00:18:59 +0200
  * [ODBC-254](https://jira.mariadb.org/browse/ODBC-254) INSTALL\_LIB\_SUFFIX is made CACHE, and made plugins to be installed under the same library. Also returned lib64 as libraries destination, if 64b library is built, and there is lib64 in\
    the system. But that may be yet changed back.\
    Returned plugins to the tarballs on linux. Probably was lost in a\
    merge.
* [Revision #79fb9cb](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/79fb9cb)\
  2019-06-06 21:18:02 +0200
  * [ODBC-253](https://jira.mariadb.org/browse/ODBC-253) The fix and the testcase\
    Added the check that if length of the query is shorter, than minimal\
    possible length of a SQL statement, return syntax error right away.\
    Fixed also local strndup version(for Windows) - it would not create copy\
    of an empty string.\
    Updated C/C to v3.0.10
* [Revision #5fa1597](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/5fa1597)\
  2019-06-01 18:09:35 +0200
  * [ODBC-252](https://jira.mariadb.org/browse/ODBC-252) Updated build instruction in te BUILD.md
* [Revision #b7bac9b](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/b7bac9b)\
  2019-05-17 01:35:11 +0200
  * Added to the Dbc handle new mutex to guard lists operations
* [Revision #1a7f0d6](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/1a7f0d6)\
  2019-05-15 19:37:55 +0200
  * ma\_desc test change to pass with iodbc
* [Revision #679e84c](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/679e84c)\
  2019-05-14 01:13:19 +0200
  * Fix of the testcase in the catalog2
* [Revision #0314e02](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/0314e02)\
  2019-05-10 23:23:32 +0200
  * Merge branch 'master' into develop
* [Revision #832360f](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/832360f)\
  2019-05-02 20:21:24 +0200
  * [ODBC-211](https://jira.mariadb.org/browse/ODBC-211) The fix and the testcase\
    Also fixed precision in case of unsigned decimal field and/or with 0\
    scale, octet length and display size calculation.
* [Revision #07ee7ce](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/07ee7ce)\
  2019-05-10 00:35:09 +0200
  * Version bump -> 3.1.2

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
