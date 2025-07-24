# Connector/C 3.0.8 Changelog

The most recent [_**Stable**_](../../../../community-server/about/release-criteria.md) _**(GA)**_ release of MariaDB Connector/C is:[**MariaDB Connector/C 3.4.5**](../../mariadb-connector-c-3-4-release-notes/mariadb-connector-c-3-4-5-release-notes.md)

[Download](https://downloads.mariadb.org/connector-c/3.0.8/)[Release Notes](../../mariadb-connector-c-30-release-notes/mariadb-connector-c-308-release-notes.md)[Changelog](mariadb-connector-c-308-changelog.md)[About MariaDB Connector/C](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-c/README.md)

**Release date:** 21 Dec 2018

For the highlights of this release, see the [release notes](../../mariadb-connector-c-30-release-notes/mariadb-connector-c-308-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On [GitHub](https://github.com/MariaDB/mariadb-connector-c/) you can view more\
details of the revision and view diffs of the code modified in that revision.

* [Revision #34f8887](https://github.com/mariadb-corporation/mariadb-connector-c/commit/34f8887)\
  2018-12-18 17:34:42 +0100
  * Fix warnings on Windows
* [Revision #9d981de](https://github.com/mariadb-corporation/mariadb-connector-c/commit/9d981de)\
  2018-12-18 15:17:42 +0100
  * gnutls (esp. when static) needs zlib
* [Revision #2a66af1](https://github.com/mariadb-corporation/mariadb-connector-c/commit/2a66af1)\
  2018-12-18 15:16:16 +0100
  * support linking with external manually specified zlib
* [Revision #5baea22](https://github.com/mariadb-corporation/mariadb-connector-c/commit/5baea22)\
  2018-12-07 17:39:34 +0100
  * Fix warnings on Windows
* [Revision #1ecc37f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/1ecc37f)\
  2018-12-07 17:21:18 +0100
  * [CONC-387](https://jira.mariadb.org/browse/CONC-387) return MYSQL\_DATA\_TRUNCATED for invalid numeric strings.
* [Revision #6e59920](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6e59920)\
  2018-12-01 13:27:22 +0100
  * Add plugin pdb's to msi
* [Revision #9eb0fa1](https://github.com/mariadb-corporation/mariadb-connector-c/commit/9eb0fa1)\
  2018-12-01 13:05:51 +0100
  * Windows build fixes:
* [Revision #e47b6aa](https://github.com/mariadb-corporation/mariadb-connector-c/commit/e47b6aa)\
  2018-12-01 11:12:26 +0100\
  \*
  * Added gcc options "-Wno-undef -Wno-unknown-pragmas" - Added LIBZ wo windows system libraries
* [Revision #3e6adb2](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3e6adb2)\
  2018-12-01 11:11:46 +0100
  * Fixed build error/warning Added missing errorcodes for mingw
* [Revision #abee401](https://github.com/mariadb-corporation/mariadb-connector-c/commit/abee401)\
  2018-12-01 10:59:50 +0100
  * Use lowercase names for windows include files
* [Revision #be25fb9](https://github.com/mariadb-corporation/mariadb-connector-c/commit/be25fb9)\
  2018-12-01 10:24:57 +0100
  * Updated server versions
* [Revision #6f5ec8c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6f5ec8c)\
  2018-12-01 09:28:58 +0100
  * Merge pull request #86 from rasmushoj/3.0
* [Revision #15d28e9](https://github.com/mariadb-corporation/mariadb-connector-c/commit/15d28e9)\
  2018-11-27 12:34:43 +0000
  * Test also with latest version of MariaDB Server 10.2
* [Revision #005195f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/005195f)\
  2018-12-01 08:56:24 +0100
  * [CONC-312](https://jira.mariadb.org/browse/CONC-312): Implementation for caching\_sha2\_password plugin
* [Revision #84ab333](https://github.com/mariadb-corporation/mariadb-connector-c/commit/84ab333)\
  2018-11-29 14:30:24 +0100
  * Skip session\_tracker\_last\_gtid test for now, it fails for unknown reasons on travis.
* [Revision #418e338](https://github.com/mariadb-corporation/mariadb-connector-c/commit/418e338)\
  2018-11-27 08:14:33 +0100
  * Fix for [CONC-375](https://jira.mariadb.org/browse/CONC-375): SSL handshake fails
* [Revision #f06bcba](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f06bcba)\
  2018-11-27 08:09:23 +0100
  * Bumped version number
* [Revision #44b21bf](https://github.com/mariadb-corporation/mariadb-connector-c/commit/44b21bf)\
  2018-11-14 08:54:47 +0100
  * install libmariadb.pc in the package-dependent location
* [Revision #06fd8c9](https://github.com/mariadb-corporation/mariadb-connector-c/commit/06fd8c9)\
  2018-11-10 23:48:27 +0100
  * [CONC-372](https://jira.mariadb.org/browse/CONC-372) Fix str\_to\_TIME() parsing wrt performance.

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
