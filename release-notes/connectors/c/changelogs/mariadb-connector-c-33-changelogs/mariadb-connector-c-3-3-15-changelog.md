# MariaDB Connector/C 3.3.15 Changelog

The most recent [_**Stable**_](../../../../mariadb-release-criteria.md) _**(GA)**_ release of MariaDB Connector/C is:[**MariaDB Connector/C 3.4.5**](../../mariadb-connector-c-3-4-release-notes/mariadb-connector-c-3-4-5-release-notes.md)

[Download](https://mariadb.com/downloads/connectors)[Release Notes](../../mariadb-connector-c-33-release-notes/mariadb-connector-c-3-3-15-release-notes.md)[Changelog](mariadb-connector-c-3-3-15-changelog.md)[About MariaDB Connector/C](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-c/README.md)

**Release date:** 9 Apr 2025

For the highlights of this release, see the[release notes](../../mariadb-connector-c-33-release-notes/mariadb-connector-c-3-3-15-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-c/) you can view more\
details of the revision and view diffs of the code modified in that revision.

* [Revision #a7ad25b0](https://github.com/mariadb-corporation/mariadb-connector-c/commit/a7ad25b0)\
  2025-02-27 13:50:01 +0100
  * Fix memory leack in the test
* [Revision #0ff64ca0](https://github.com/mariadb-corporation/mariadb-connector-c/commit/0ff64ca0)\
  2025-02-27 09:35:33 +0100
  * Merge branch '3.1' into 3.3
* [Revision #f7633e9d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f7633e9d)\
  2025-02-27 09:33:35 +0100
  * Test fix: pipe name
* [Revision #4c9bc2b0](https://github.com/mariadb-corporation/mariadb-connector-c/commit/4c9bc2b0)\
  2025-02-27 07:52:35 +0100
  * Merge branch '3.1' into 3.3
* [Revision #aa240cd1](https://github.com/mariadb-corporation/mariadb-connector-c/commit/aa240cd1)\
  2025-02-27 07:48:58 +0100
  * [CONC-760](https://jira.mariadb.org/browse/CONC-760): valid named pipe connection is closed
* [Revision #bbf07912](https://github.com/mariadb-corporation/mariadb-connector-c/commit/bbf07912)\
  2025-02-18 16:32:29 +0100
  * Fix after previous revert
* [Revision #c21a246b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/c21a246b)\
  2025-02-18 16:31:09 +0100
  * Merge branch '3.1' into 3.3
* [Revision #d4eec05d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d4eec05d)\
  2025-02-18 16:19:50 +0100
  * Revert "[CONC-710](https://jira.mariadb.org/browse/CONC-710): Remove UDF declarations"
* [Revision #a8f9a57a](https://github.com/mariadb-corporation/mariadb-connector-c/commit/a8f9a57a)\
  2025-02-11 15:01:15 -0500
  * bump the VERSION
* [Revision #fe8f48c6](https://github.com/mariadb-corporation/mariadb-connector-c/commit/fe8f48c6)\
  2025-02-12 08:34:10 +0100
  * Build fix: fix warning in ps\_bugs.c
* [Revision #992c7f26](https://github.com/mariadb-corporation/mariadb-connector-c/commit/992c7f26)\
  2025-02-12 07:12:14 +0100
  * Travis fix: Skip maxscale for test\_mdev35935
* [Revision #4bbfa504](https://github.com/mariadb-corporation/mariadb-connector-c/commit/4bbfa504)\
  2025-02-11 15:03:48 -0500
  * bump the VERSION
* [Revision #1e4e4734](https://github.com/mariadb-corporation/mariadb-connector-c/commit/1e4e4734)\
  2025-02-11 19:38:55 +0100
  * test fix: use my\_ulonglong instead of ulong
* [Revision #48770939](https://github.com/mariadb-corporation/mariadb-connector-c/commit/48770939)\
  2025-02-11 11:28:56 +0100
  * Workaround for [MDEV-35935](https://jira.mariadb.org/browse/MDEV-35935)
* [Revision #28ae227e](https://github.com/mariadb-corporation/mariadb-connector-c/commit/28ae227e)\
  2025-02-11 10:50:40 +0100
  * [CONC-755](https://jira.mariadb.org/browse/CONC-755): Fix MSAN failure
* [Revision #ae507c35](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ae507c35)\
  2025-02-10 17:01:44 +0100
  * Merge pull request #270 from knielsen/knielsen\_conc\_fixes
* [Revision #2381127b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/2381127b)\
  2025-02-06 00:24:28 +0100
  * [CONC-473](https://jira.mariadb.org/browse/CONC-473): mysql\_real\_connect\_start() stack overrun with mdns hostname
* [Revision #77754f4d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/77754f4d)\
  2025-02-05 16:57:31 +0100
  * [CONC-725](https://jira.mariadb.org/browse/CONC-725): Fix compiler warning about uninitialized union member
* [Revision #fc49fa70](https://github.com/mariadb-corporation/mariadb-connector-c/commit/fc49fa70)\
  2025-02-05 16:07:25 +0100
  * [CONC-618](https://jira.mariadb.org/browse/CONC-618): Please annotate swapcontext for ASAN
* [Revision #879fcab6](https://github.com/mariadb-corporation/mariadb-connector-c/commit/879fcab6)\
  2025-02-05 13:26:43 +0100
  * Remove obsolete reference to my\_context.c which was renamed to ma\_context.c
* [Revision #003ea7e9](https://github.com/mariadb-corporation/mariadb-connector-c/commit/003ea7e9)\
  2025-02-05 11:56:35 +0100
  * [CONC-753](https://jira.mariadb.org/browse/CONC-753): Compile error on .cfi\_escape in builds with no unwind/cfi

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
