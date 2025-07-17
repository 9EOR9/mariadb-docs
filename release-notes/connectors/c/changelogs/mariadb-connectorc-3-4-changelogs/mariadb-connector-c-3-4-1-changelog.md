# Connector/C 3.4.1 Changelog

The most recent [_**Stable**_](../../../../community-server/about/release-criteria.md) _**(GA)**_ release of MariaDB Connector/C is:[**MariaDB Connector/C 3.4.5**](../../mariadb-connector-c-3-4-release-notes/mariadb-connector-c-3-4-5-release-notes.md)

[Download](https://mariadb.com/downloads/connectors)[Release Notes](../../mariadb-connector-c-3-4-release-notes/mariadb-connector-c-3-4-1-release-notes.md)[Changelog](mariadb-connector-c-3-4-1-changelog.md)[About MariaDB Connector/C](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/about-mariadb-connector-c/README.md)

**Release date:** 20 Aug 2024

For the highlights of this release, see the[release notes](../../mariadb-connector-c-3-4-release-notes/mariadb-connector-c-3-4-1-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-c/) you can view more\
details of the revision and view diffs of the code modified in that revision.

* [Revision #de630591](https://github.com/mariadb-corporation/mariadb-connector-c/commit/de630591)\
  2024-08-03 16:38:02 +0200
  * Merge remote-tracking branch 'origin/3.4' into HEAD
* [Revision #4681372f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/4681372f)\
  2024-07-31 10:05:00 +0300
  * [CONC-700](https://jira.mariadb.org/browse/CONC-700): Fix gcc-14 -Wcalloc-transposed-args
* [Revision #2888c180](https://github.com/mariadb-corporation/mariadb-connector-c/commit/2888c180)\
  2024-07-24 09:53:26 +0200
  * bump version
* [Revision #dddcf400](https://github.com/mariadb-corporation/mariadb-connector-c/commit/dddcf400)\
  2024-06-26 15:10:13 +0200
  * fix [MDEV-34424](https://jira.mariadb.org/browse/MDEV-34424) for ed255129
* [Revision #05a1235d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/05a1235d)\
  2024-08-01 19:42:24 +0200
  * disable parsec by default
* [Revision #f95b7faa](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f95b7faa)\
  2024-06-21 14:26:20 +0200
  * [MDEV-34424](https://jira.mariadb.org/browse/MDEV-34424) Replica server crashes when using PARSEC plugin
* [Revision #e7316ff0](https://github.com/mariadb-corporation/mariadb-connector-c/commit/e7316ff0)\
  2024-06-13 15:48:22 +0200
  * parsec auth plugin
* [Revision #791741f3](https://github.com/mariadb-corporation/mariadb-connector-c/commit/791741f3)\
  2024-06-13 11:42:22 +0200
  * cleanup: paths
* [Revision #0f3a41ec](https://github.com/mariadb-corporation/mariadb-connector-c/commit/0f3a41ec)\
  2024-08-01 17:14:09 +0200
  * TLS post-fixes
* [Revision #32c39a9c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/32c39a9c)\
  2024-07-18 10:56:50 +0200
  * travis fix:
* [Revision #db43d638](https://github.com/mariadb-corporation/mariadb-connector-c/commit/db43d638)\
  2024-07-18 09:58:05 +0200
  * removed x509 test from connection
* [Revision #e308fae9](https://github.com/mariadb-corporation/mariadb-connector-c/commit/e308fae9)\
  2024-07-18 09:40:56 +0200
  * tls test fix:
* [Revision #109ec586](https://github.com/mariadb-corporation/mariadb-connector-c/commit/109ec586)\
  2024-07-18 08:38:17 +0200
  * tls test fixes:
* [Revision #c5d2a0eb](https://github.com/mariadb-corporation/mariadb-connector-c/commit/c5d2a0eb)\
  2024-07-18 05:44:50 +0200
  * TLS (schannel) fixes: - don't verify fingerprint twice - pci->dwVersion (certificate version) needs to be increased by 1 - use MARIADB\_TLS\_VERIFY\_UNKNOWN for unknown tls verification errors
* [Revision #efbc5624](https://github.com/mariadb-corporation/mariadb-connector-c/commit/efbc5624)\
  2024-07-17 11:56:44 +0200
  * tls test fix:
* [Revision #ea307b8d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ea307b8d)\
  2024-07-17 11:06:52 +0200
  * Travis fixes for windows
* [Revision #1287c901](https://github.com/mariadb-corporation/mariadb-connector-c/commit/1287c901)\
  2024-07-16 13:12:26 +0200
  * TLS/SSL changes (major rework)
* [Revision #5386f1a3](https://github.com/mariadb-corporation/mariadb-connector-c/commit/5386f1a3)\
  2024-06-25 11:57:27 +0200
  * Merge remote-tracking branch 'origin/3.3' into 3.4-tls
* [Revision #486ce75d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/486ce75d)\
  2024-06-11 16:00:22 +0200
  * [CONPY-704](https://jira.mariadb.org/browse/CONPY-704): parse\_connection\_string ignores empty string in last parameter
* [Revision #2daa7b28](https://github.com/mariadb-corporation/mariadb-connector-c/commit/2daa7b28)\
  2024-05-28 00:39:04 +0200
  * Windows, OpenSSL - HAVE\_OPENSSL\_APPLINK\_C is not set, when compiling with /WX
* [Revision #7498d30a](https://github.com/mariadb-corporation/mariadb-connector-c/commit/7498d30a)\
  2024-06-21 16:14:36 +0200
  * [CONC-698](https://jira.mariadb.org/browse/CONC-698): certificate info is read on every connect
* [Revision #71fa44cf](https://github.com/mariadb-corporation/mariadb-connector-c/commit/71fa44cf)\
  2024-06-20 08:34:19 +0200
  * [CONC-698](https://jira.mariadb.org/browse/CONC-698): certificate info is read on every connect
* [Revision #f97bb2e9](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f97bb2e9)\
  2024-06-10 13:19:49 +0200
  * Fix failing tests when server runs on a different machine

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
