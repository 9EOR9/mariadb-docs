# Connector/C 3.3.14 Changelog

The most recent [_**Stable**_](../../../../community-server/about/release-criteria.md) _**(GA)**_ release of MariaDB Connector/C is:[**MariaDB Connector/C 3.4.5**](../../mariadb-connector-c-3-4-release-notes/mariadb-connector-c-3-4-5-release-notes.md)

[Download](https://mariadb.com/downloads/connectors)[Release Notes](../../mariadb-connector-c-33-release-notes/mariadb-connector-c-3-3-14-release-notes.md)[Changelog](mariadb-connector-c-3-3-14-changelog.md)[About MariaDB Connector/C](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-c/README.md)

**Release date:** 11 Feb 2025

For the highlights of this release, see the [release notes](../../mariadb-connector-c-33-release-notes/mariadb-connector-c-3-3-14-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On [GitHub](https://github.com/MariaDB/mariadb-connector-c/) you can view more\
details of the revision and view diffs of the code modified in that revision.

* [Revision #2d56f340](https://github.com/mariadb-corporation/mariadb-connector-c/commit/2d56f340)\
  2025-01-24 14:52:35 +0100
  * Merge branch '3.1' into 3.3
* [Revision #7d930974](https://github.com/mariadb-corporation/mariadb-connector-c/commit/7d930974)\
  2025-01-23 23:07:32 +0100
  * [CONC-751](https://jira.mariadb.org/browse/CONC-751) unit.conc\_connection fails with CYPHER missmatch on some builds
* [Revision #232b563d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/232b563d)\
  2025-01-16 20:18:10 +0100
  * [CONPY-739](https://jira.mariadb.org/browse/CONPY-739) don't use pow() to truncate an integer
* [Revision #836db563](https://github.com/mariadb-corporation/mariadb-connector-c/commit/836db563)\
  2025-01-23 19:54:44 +0100
  * memory leaks after [CONC-589](https://jira.mariadb.org/browse/CONC-589), e09e24e8
* [Revision #4431d5bf](https://github.com/mariadb-corporation/mariadb-connector-c/commit/4431d5bf)\
  2025-01-24 06:02:27 +0100
  * Merge branch '3.1' into 3.3
* [Revision #1a34542e](https://github.com/mariadb-corporation/mariadb-connector-c/commit/1a34542e)\
  2025-01-24 06:00:49 +0100
  * Removed ASAN options which were merged by mistake.
* [Revision #13374492](https://github.com/mariadb-corporation/mariadb-connector-c/commit/13374492)\
  2025-01-21 14:28:52 +0100
  * Merge branch '3.1' into 3.3
* [Revision #5f4b9b6e](https://github.com/mariadb-corporation/mariadb-connector-c/commit/5f4b9b6e)\
  2025-01-21 14:21:33 +0100
  * Travis fix: Skip reconnect test (MaxScale)
* [Revision #31ecf2c0](https://github.com/mariadb-corporation/mariadb-connector-c/commit/31ecf2c0)\
  2025-01-21 14:18:39 +0100
  * Merge pull request #243 from joshuahunt/johunt/fix-async-check-result
* [Revision #cb3fb01a](https://github.com/mariadb-corporation/mariadb-connector-c/commit/cb3fb01a)\
  2024-03-27 16:50:20 -0700
  * Fix SSL\_read/write return value checking in ma\_tls\_async\_check\_result
* [Revision #53b71693](https://github.com/mariadb-corporation/mariadb-connector-c/commit/53b71693)\
  2025-01-15 10:46:29 +0100
  * Merge branch '3.1' into 3.3
* [Revision #36d1c3ac](https://github.com/mariadb-corporation/mariadb-connector-c/commit/36d1c3ac)\
  2025-01-15 10:41:32 +0100
  * Travis fix: Skip reconnect test (MaxScale)
* [Revision #57ce0ce3](https://github.com/mariadb-corporation/mariadb-connector-c/commit/57ce0ce3)\
  2025-01-15 08:00:19 +0100
  * Merge branch '3.1' into 3.3
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
* [Revision #75d381ff](https://github.com/mariadb-corporation/mariadb-connector-c/commit/75d381ff)\
  2025-01-07 16:58:39 +0100
  * Build fix: moved Item\_result back to mariadb\_com.h
* [Revision #fa9f5f66](https://github.com/mariadb-corporation/mariadb-connector-c/commit/fa9f5f66)\
  2025-01-07 16:57:53 +0100
  * Travis and test fixes:
* [Revision #486a07c8](https://github.com/mariadb-corporation/mariadb-connector-c/commit/486a07c8)\
  2024-12-21 08:33:15 +0100
  * Test fix:
* [Revision #30bd0079](https://github.com/mariadb-corporation/mariadb-connector-c/commit/30bd0079)\
  2024-12-20 06:17:01 +0100
  * Travis: Include unit test suite
* [Revision #32addee3](https://github.com/mariadb-corporation/mariadb-connector-c/commit/32addee3)\
  2024-12-20 06:14:02 +0100
  * Test case fix:
* [Revision #2fd03c82](https://github.com/mariadb-corporation/mariadb-connector-c/commit/2fd03c82)\
  2024-12-19 11:47:18 +0100
  * coverity fix: remove whitespace
* [Revision #19495f1c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/19495f1c)\
  2024-12-19 11:14:19 +0100
  * Fix logical error in parse\_connection\_string
* [Revision #13c88156](https://github.com/mariadb-corporation/mariadb-connector-c/commit/13c88156)\
  2024-12-17 19:04:08 +0100
  * Fix test [CONC-702](https://jira.mariadb.org/browse/CONC-702)
* [Revision #dc8bc987](https://github.com/mariadb-corporation/mariadb-connector-c/commit/dc8bc987)\
  2024-12-16 13:50:00 +0100
  * Test fix for character test conc223:
* [Revision #d90e911e](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d90e911e)\
  2024-12-12 10:43:07 +0100
  * Merge branch '3.1' into 3.3
* [Revision #6bf9557d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6bf9557d)\
  2024-12-12 10:40:30 +0100
  * [CONC-709](https://jira.mariadb.org/browse/CONC-709): Fix crash when sending NULL\_LENGTH in field description
* [Revision #294b9336](https://github.com/mariadb-corporation/mariadb-connector-c/commit/294b9336)\
  2024-12-10 08:01:37 +0100
  * [CONC-708](https://jira.mariadb.org/browse/CONC-708): buffer over-/underflow in ma\_read\_ok\_packet
* [Revision #16e5b88b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/16e5b88b)\
  2024-12-10 05:18:08 +0100
  * MYSQL\_OPT\_ZSTD\_COMPRESSION\_LEVEL fixes:
* [Revision #e633858c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/e633858c)\
  2024-12-09 22:22:08 +0100
  * Merge pull request #261 from markus456/3.3-zstd-compression-level
* [Revision #a2213b89](https://github.com/mariadb-corporation/mariadb-connector-c/commit/a2213b89)\
  2024-11-07 06:47:21 +0200
  * Add MYSQL\_OPT\_ZSTD\_COMPRESSION\_LEVEL
* [Revision #136d295d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/136d295d)\
  2024-12-09 19:32:13 +0100
  * Merge branch '3.1' into 3.3
* [Revision #554893c2](https://github.com/mariadb-corporation/mariadb-connector-c/commit/554893c2)\
  2024-12-09 19:28:10 +0100
  * [CONC-711](https://jira.mariadb.org/browse/CONC-711): Ubsan and ASAN fixes
* [Revision #1c8b73c1](https://github.com/mariadb-corporation/mariadb-connector-c/commit/1c8b73c1)\
  2024-12-09 10:02:52 +0100
  * Merge branch '3.1' into 3.3
* [Revision #98ae464b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/98ae464b)\
  2024-12-09 09:54:13 +0100
  * [CONC-617](https://jira.mariadb.org/browse/CONC-617): Update GnuTLS minimum required version to 3.4.2
* [Revision #6d28fe89](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6d28fe89)\
  2024-12-08 11:50:43 +0100
  * Merge branch '3.1' into 3.3
* [Revision #af44fc5c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/af44fc5c)\
  2024-12-08 11:27:32 +0100
  * [CONC-748](https://jira.mariadb.org/browse/CONC-748): Allow to set TLSv1.3 ciphers in GnuTLS
* [Revision #232e81f0](https://github.com/mariadb-corporation/mariadb-connector-c/commit/232e81f0)\
  2024-12-04 10:13:21 +0100
  * Add test case for [CONC-176](https://jira.mariadb.org/browse/CONC-176)
* [Revision #fa987a3b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/fa987a3b)\
  2024-12-02 06:36:56 +0100
  * Added test case for [CONC-163](https://jira.mariadb.org/browse/CONC-163)
* [Revision #c7a46ed6](https://github.com/mariadb-corporation/mariadb-connector-c/commit/c7a46ed6)\
  2024-12-02 13:54:33 +0100
  * Merge pull request #259 from markus456/3.3
* [Revision #721103eb](https://github.com/mariadb-corporation/mariadb-connector-c/commit/721103eb)\
  2024-10-26 07:09:21 +0300
  * Fix zstd compression level bytes
* [Revision #78e56a7f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/78e56a7f)\
  2024-11-27 16:03:45 +0100
  * Fixed replication build
* [Revision #b522ed1a](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b522ed1a)\
  2024-11-27 15:58:51 +0100
  * Merge branch '3.1' into 3.3
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
* [Revision #bdc66d6b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/bdc66d6b)\
  2024-11-27 07:48:27 +0100
  * Fix for [CONC-703](https://jira.mariadb.org/browse/CONC-703):
* [Revision #662a9660](https://github.com/mariadb-corporation/mariadb-connector-c/commit/662a9660)\
  2024-11-18 07:15:42 +0100
  * [CONC-702](https://jira.mariadb.org/browse/CONC-702): Fix statement status
* [Revision #58185578](https://github.com/mariadb-corporation/mariadb-connector-c/commit/58185578)\
  2024-11-12 13:18:19 -0500
  * bump the VERSION

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
