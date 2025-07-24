# Connector/C 3.1.11 Changelog

The most recent [_**Stable**_](../../../../community-server/about/release-criteria.md) _**(GA)**_ release of MariaDB Connector/C is:[**MariaDB Connector/C 3.4.5**](../../mariadb-connector-c-3-4-release-notes/mariadb-connector-c-3-4-5-release-notes.md)

[Download](https://mariadb.com/downloads/#connectors)[Release Notes](../../mariadb-connector-c-31-release-notes/mariadb-connector-c-3111-release-notes.md)[Changelog](mariadb-connector-c-3111-changelog.md)[About MariaDB Connector/C](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-c/README.md)

**Release date:** 4 Nov 2020

For the highlights of this release, see the [release notes](../../mariadb-connector-c-31-release-notes/mariadb-connector-c-3111-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On [GitHub](https://github.com/MariaDB/mariadb-connector-c/) you can view more\
details of the revision and view diffs of the code modified in that revision.

* [Revision #6242752](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6242752)\
  2020-10-30 12:09:04 +0200
  * [CONC-513](https://jira.mariadb.org/browse/CONC-513) MSAN use-of-uninitialized-value in strstr()
* [Revision #93618b4](https://github.com/mariadb-corporation/mariadb-connector-c/commit/93618b4)\
  2020-10-30 08:18:44 +0100
  * Fix for [CONC-512](https://jira.mariadb.org/browse/CONC-512): truncation check for float values fails on i386
* [Revision #8e5be10](https://github.com/mariadb-corporation/mariadb-connector-c/commit/8e5be10)\
  2020-10-28 20:50:09 +0100
  * cleanup: use predefined CMAKE\_DL\_LIBS
* [Revision #0394882](https://github.com/mariadb-corporation/mariadb-connector-c/commit/0394882)\
  2020-10-28 10:58:05 +0100
  * Test fix:
* [Revision #0cdc165](https://github.com/mariadb-corporation/mariadb-connector-c/commit/0cdc165)\
  2020-10-24 11:07:47 +0300
  * Do not leak memory in the skipped [MDEV-23768](https://jira.mariadb.org/browse/MDEV-23768) unit test
* [Revision #7c5a40b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/7c5a40b)\
  2020-10-24 07:54:59 +0200
  * Fix for [CONC-510](https://jira.mariadb.org/browse/CONC-510): CoreDump using set env MARIADB\_PLUGIN\_DIR
* [Revision #cfc36a4](https://github.com/mariadb-corporation/mariadb-connector-c/commit/cfc36a4)\
  2020-10-23 17:03:57 +0700
  * [MDEV-23564](https://jira.mariadb.org/browse/MDEV-23564): CMAKE failing due to deprecated Apple GSS method
* [Revision #aee071d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/aee071d)\
  2020-10-23 07:57:17 +0200
  * Merge pull request #132 from grooverdan/gssapifix
* [Revision #1f13673](https://github.com/mariadb-corporation/mariadb-connector-c/commit/1f13673)\
  2020-04-04 18:54:08 +1100
  * gssapi: include path fix FreeBSD/Solaris
* [Revision #8a4fac7](https://github.com/mariadb-corporation/mariadb-connector-c/commit/8a4fac7)\
  2020-10-23 06:39:15 +0200
  * unittest fix:
* [Revision #2064d89](https://github.com/mariadb-corporation/mariadb-connector-c/commit/2064d89)\
  2020-10-23 06:14:04 +0200
  * Followup of 7b4d5e785a3ec5aab13cdf4ac4ee31ad53644e0e
* [Revision #7b4d5e7](https://github.com/mariadb-corporation/mariadb-connector-c/commit/7b4d5e7)\
  2020-10-23 05:59:41 +0200
  * Build fix:
* [Revision #aa0ba0f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/aa0ba0f)\
  2020-10-23 05:51:49 +0200
  * Removed examples directory
* [Revision #1911b9d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/1911b9d)\
  2020-10-22 12:10:53 +0200
  * Use cmake variable CMAKE\_DL\_LIBS instead of find\_package command.
* [Revision #7a7c5ad](https://github.com/mariadb-corporation/mariadb-connector-c/commit/7a7c5ad)\
  2020-10-21 12:44:41 +0200
  * [CONC-508](https://jira.mariadb.org/browse/CONC-508):
* [Revision #1fed6c3](https://github.com/mariadb-corporation/mariadb-connector-c/commit/1fed6c3)\
  2020-10-21 07:23:50 +0200
  * Build fix:
* [Revision #ca4f043](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ca4f043)\
  2020-10-20 19:32:49 +0200
  * Fix for [CONC-507](https://jira.mariadb.org/browse/CONC-507):
* [Revision #b24d337](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b24d337)\
  2020-10-20 16:17:25 +0200
  * More test fixes:
* [Revision #dec5866](https://github.com/mariadb-corporation/mariadb-connector-c/commit/dec5866)\
  2020-10-20 15:25:05 +0200
  * Test fix (appveyor):
* [Revision #569fe21](https://github.com/mariadb-corporation/mariadb-connector-c/commit/569fe21)\
  2020-10-20 15:01:24 +0200
  * Appveyor fixes:
* [Revision #b2966c0](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b2966c0)\
  2020-10-20 14:57:22 +0200
  * Revert "[MDEV-19237](https://jira.mariadb.org/browse/MDEV-19237) - do not resend prepared statement metadata unnecessarily":
* [Revision #ed4d747](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ed4d747)\
  2020-09-22 18:10:40 +0200
  * [MDEV-19237](https://jira.mariadb.org/browse/MDEV-19237) - do not resend prepared statement metadata unnecessarily
* [Revision #7799258](https://github.com/mariadb-corporation/mariadb-connector-c/commit/7799258)\
  2020-10-11 05:01:56 +0200
  * Don't define uchar if my\_global.h was previously included (server build)
* [Revision #a722cd1](https://github.com/mariadb-corporation/mariadb-connector-c/commit/a722cd1)\
  2020-10-11 04:59:42 +0200
  * Update zlib (version 1.2.11)
* [Revision #6cf8ccc](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6cf8ccc)\
  2020-10-06 15:30:05 +0200
  * Build fix for OpenSSL 1.1.0
* [Revision #55a64c1](https://github.com/mariadb-corporation/mariadb-connector-c/commit/55a64c1)\
  2020-10-02 09:47:52 +0200
  * Fix for [CONC-504](https://jira.mariadb.org/browse/CONC-504): reset stmt->result.rows when executing mysql\_stmt\_next\_result
* [Revision #c17947c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/c17947c)\
  2020-10-01 07:32:13 +0200
  * Partially revert of 9a50a7d:
* [Revision #42d32ba](https://github.com/mariadb-corporation/mariadb-connector-c/commit/42d32ba)\
  2020-09-30 16:19:31 +0200
  * Fix for mariadb\_stmt\_execute\_direct():
* [Revision #079923b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/079923b)\
  2020-09-30 08:03:42 +0200
  * revert upgrade to focal
* [Revision #c6d21c8](https://github.com/mariadb-corporation/mariadb-connector-c/commit/c6d21c8)\
  2020-09-30 06:31:58 +0200
  * Merge branch '3.1' of [mariadb-connector-c](https://github.com/mariadb-corporation/mariadb-connector-c) into 3.1
* [Revision #c0837c3](https://github.com/mariadb-corporation/mariadb-connector-c/commit/c0837c3)\
  2020-04-22 01:55:59 +0200
  * [MDEV-21612](https://jira.mariadb.org/browse/MDEV-21612) Remove COM\_MULTI.
* [Revision #2972095](https://github.com/mariadb-corporation/mariadb-connector-c/commit/2972095)\
  2020-09-30 06:29:29 +0200
  * Allow to specify the default character set in server builds with -DCONC\_DEFAULT\_CHARSET
* [Revision #aa65bd1](https://github.com/mariadb-corporation/mariadb-connector-c/commit/aa65bd1)\
  2020-09-21 18:25:10 +0200
  * Skip test\_returning, since it's not fixed on server yet ([MDEV-23768](https://jira.mariadb.org/browse/MDEV-23768))
* [Revision #8752eea](https://github.com/mariadb-corporation/mariadb-connector-c/commit/8752eea)\
  2020-09-21 15:44:05 +0200
  * Use a newer ubuntu version for travis
* [Revision #ee2216a](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ee2216a)\
  2020-09-18 09:25:08 +0200
  * Build fix for OpenSSL < 1.1
* [Revision #65cf891](https://github.com/mariadb-corporation/mariadb-connector-c/commit/65cf891)\
  2020-09-18 08:31:03 +0200
  * [CONC-501](https://jira.mariadb.org/browse/CONC-501): Support for TLSv1.3 cipher suites
* [Revision #ddc0b92](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ddc0b92)\
  2020-09-17 12:48:57 -0400
  * bump the VERSION

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
