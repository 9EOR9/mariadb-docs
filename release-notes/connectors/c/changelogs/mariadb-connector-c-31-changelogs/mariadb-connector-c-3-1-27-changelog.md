# MariaDB Connector/C 3.1.27 Changelog

The most recent [_**Stable**_](../../../../mariadb-release-criteria.md) _**(GA)**_ release of MariaDB Connector/C is:[**MariaDB Connector/C 3.4.5**](../../mariadb-connector-c-3-4-release-notes/mariadb-connector-c-3-4-5-release-notes.md)

[Download](https://mariadb.com/downloads/connectors)[Release Notes](../../mariadb-connector-c-31-release-notes/mariadb-connector-c-3-1-27-release-notes.md)[Changelog](mariadb-connector-c-3-1-27-changelog.md)[About MariaDB Connector/C](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-c/README.md)

**Release date:** 11 Feb 2025

For the highlights of this release, see the[release notes](../../mariadb-connector-c-31-release-notes/mariadb-connector-c-3-1-27-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-c/) you can view more\
details of the revision and view diffs of the code modified in that revision.

* [Revision #7d930974](https://github.com/mariadb-corporation/mariadb-connector-c/commit/7d930974)\
  2025-01-23 23:07:32 +0100
  * [CONC-751](https://jira.mariadb.org/browse/CONC-751) unit.conc\_connection fails with CYPHER missmatch on some builds
* [Revision #232b563d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/232b563d)\
  2025-01-16 20:18:10 +0100
  * [CONPY-739](https://jira.mariadb.org/browse/CONPY-739) don't use pow() to truncate an integer
* [Revision #836db563](https://github.com/mariadb-corporation/mariadb-connector-c/commit/836db563)\
  2025-01-23 19:54:44 +0100
  * memory leaks after [CONC-589](https://jira.mariadb.org/browse/CONC-589), e09e24e8
* [Revision #1a34542e](https://github.com/mariadb-corporation/mariadb-connector-c/commit/1a34542e)\
  2025-01-24 06:00:49 +0100
  * Removed ASAN options which were merged by mistake.
* [Revision #5f4b9b6e](https://github.com/mariadb-corporation/mariadb-connector-c/commit/5f4b9b6e)\
  2025-01-21 14:21:33 +0100
  * Travis fix: Skip reconnect test (MaxScale)
* [Revision #31ecf2c0](https://github.com/mariadb-corporation/mariadb-connector-c/commit/31ecf2c0)\
  2025-01-21 14:18:39 +0100
  * Merge pull request #243 from joshuahunt/johunt/fix-async-check-result
* [Revision #cb3fb01a](https://github.com/mariadb-corporation/mariadb-connector-c/commit/cb3fb01a)\
  2024-03-27 16:50:20 -0700
  * Fix SSL\_read/write return value checking in ma\_tls\_async\_check\_result
* [Revision #732a1ad1](https://github.com/mariadb-corporation/mariadb-connector-c/commit/732a1ad1)\
  2025-01-15 07:37:54 +0100
  * Merge branch '3.1-georg' into 3.1
* [Revision #e09e24e8](https://github.com/mariadb-corporation/mariadb-connector-c/commit/e09e24e8)\
  2025-01-15 07:26:18 +0100
  * [CONC-589](https://jira.mariadb.org/browse/CONC-589): First query fails after reconnect
* [Revision #d3e10fee](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d3e10fee)\
  2025-01-14 17:06:08 +0100
  * Merge pull request #264 from mariadb-corporation/3.1.26-[CONC-750](https://jira.mariadb.org/browse/CONC-750)
* [Revision #8ba53516](https://github.com/mariadb-corporation/mariadb-connector-c/commit/8ba53516)\
  2024-12-06 11:36:38 -0500
  * [CONC-750](https://jira.mariadb.org/browse/CONC-750) unit.pfs\_instr-oom fails on mac with dynamic-stack-overflow
* [Revision #12a70541](https://github.com/mariadb-corporation/mariadb-connector-c/commit/12a70541)\
  2024-12-22 11:00:12 +0100
  * Partial revert of 1a2ed3f67af698b394b2faed069b49d4f409a155
* [Revision #80a7fa5c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/80a7fa5c)\
  2024-12-20 14:35:37 +0100
  * Test fix for charsets
* [Revision #5485acd4](https://github.com/mariadb-corporation/mariadb-connector-c/commit/5485acd4)\
  2024-12-20 12:02:35 +0100
  * Test case fix:
* [Revision #6bf9557d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6bf9557d)\
  2024-12-12 10:40:30 +0100
  * [CONC-709](https://jira.mariadb.org/browse/CONC-709): Fix crash when sending NULL\_LENGTH in field description
* [Revision #294b9336](https://github.com/mariadb-corporation/mariadb-connector-c/commit/294b9336)\
  2024-12-10 08:01:37 +0100
  * [CONC-708](https://jira.mariadb.org/browse/CONC-708): buffer over-/underflow in ma\_read\_ok\_packet
* [Revision #554893c2](https://github.com/mariadb-corporation/mariadb-connector-c/commit/554893c2)\
  2024-12-09 19:28:10 +0100
  * [CONC-711](https://jira.mariadb.org/browse/CONC-711): Ubsan and ASAN fixes
* [Revision #98ae464b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/98ae464b)\
  2024-12-09 09:54:13 +0100
  * [CONC-617](https://jira.mariadb.org/browse/CONC-617): Update GnuTLS minimum required version to 3.4.2
* [Revision #af44fc5c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/af44fc5c)\
  2024-12-08 11:27:32 +0100
  * [CONC-748](https://jira.mariadb.org/browse/CONC-748): Allow to set TLSv1.3 ciphers in GnuTLS
* [Revision #232e81f0](https://github.com/mariadb-corporation/mariadb-connector-c/commit/232e81f0)\
  2024-12-04 10:13:21 +0100
  * Add test case for [CONC-176](https://jira.mariadb.org/browse/CONC-176)
* [Revision #fa987a3b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/fa987a3b)\
  2024-12-02 06:36:56 +0100
  * Added test case for [CONC-163](https://jira.mariadb.org/browse/CONC-163)
* [Revision #a13f65c4](https://github.com/mariadb-corporation/mariadb-connector-c/commit/a13f65c4)\
  2024-11-27 07:52:29 +0100
  * Fix CMake deprecation warning
* [Revision #1a2ed3f6](https://github.com/mariadb-corporation/mariadb-connector-c/commit/1a2ed3f6)\
  2024-11-20 14:42:04 +0100
  * [CONC-710](https://jira.mariadb.org/browse/CONC-710): Remove UDF declarations
* [Revision #55e3b63c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/55e3b63c)\
  2024-11-15 17:41:23 +0100
  * [CONPY-739](https://jira.mariadb.org/browse/CONPY-739): prepared statement support AUTO\_SEC\_PART\_DIGITS
* [Revision #225e1d6c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/225e1d6c)\
  2024-11-12 13:15:53 -0500
  * bump the VERSION
