---
hidden: true
---

# MariaDB 11.4.8 Changelog

{% include "../../../.gitbook/includes/unreleased-11-4.md" %}

<!--
<a href="https://mariadb.com/downloads/community" class="button primary">Download</a> <a href="../../mariadb-11-4-series/mariadb-11.4.8-release-notes.md" class="button secondary">Release Notes</a> <a href="mariadb-11.4.8-changelog.md" class="button secondary">Changelog</a> <a href="../../mariadb-11-4-series/what-is-mariadb-114.md" class="button secondary">Overview of 11.4</a>

[<sup>_Alternate download from mariadb.org_</sup>](https://downloads.mariadb.org/mariadb/11.4.8/)

**Release date:** ?
-->

For the highlights of this release, see the [release notes](../../mariadb-11-4-series/mariadb-11.4.8-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On [GitHub](https://github.com/MariaDB/server/tree/11.4) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Includes all fixes from [MariaDB 10.11.14](../changelogs-mariadb-10-11-series/mariadb-10.11.14-changelog.md)
* <sup>_Merge_</sup> [<sup>_Revision #c4ed889b74_</sup>](https://github.com/MariaDB/server/commit/c4ed889b74) <sup>_2025-07-28 19:40:10 +0200 - Merge branch '10.11' into 11.4_</sup>
* [Revision #ca91bf5d2a](https://github.com/MariaDB/server/commit/ca91bf5d2a) <sup>_2025-07-17 17:23:56 +0200_</sup>
  * Update ColumnStore 23.10.5-1
* [Revision #0ef4b1ab7f](https://github.com/MariaDB/server/commit/0ef4b1ab7f) <sup>_2025-07-22 23:08:29 +0200_</sup>
  * Connector/C 3.4.7
* [Revision #2b89bf7b1a](https://github.com/MariaDB/server/commit/2b89bf7b1a) <sup>_2025-07-23 17:40:10 +0200_</sup>
  * make main.desc_index_min_max more stable
* [Revision #57dd23dad8](https://github.com/MariaDB/server/commit/57dd23dad8) <sup>_2025-07-16 14:08:11 +0000_</sup>
  * New getter to read Engine Independent JSON histogram buckets directly 	This would allow Columnstore to leverage EI data in its cost-based and rewrite optimizer parts
* [Revision #3109d994eb](https://github.com/MariaDB/server/commit/3109d994eb) <sup>_2025-06-16 14:52:32 +0300_</sup>
  * MDEV-36323: Split Materialized code: last_refills is never set in 11.0+
* [Revision #6521b4112b](https://github.com/MariaDB/server/commit/6521b4112b) <sup>_2025-07-20 10:32:37 +0200_</sup>
  * MDEV-37281 incorrect isolation level in update with unique using hash or without overlap
* [Revision #a7d8c97952](https://github.com/MariaDB/server/commit/a7d8c97952) <sup>_2025-07-14 13:31:50 +1100_</sup>
  * MDEV-37230 Incorrect handling of NULL join conditions when using split-materialized
* [Revision #aa3578aa8a](https://github.com/MariaDB/server/commit/aa3578aa8a) <sup>_2025-06-23 15:05:44 +1100_</sup>
  * MDEV-37057  Wrong result with LATERAL DERIVED
* [Revision #dbeef00562](https://github.com/MariaDB/server/commit/dbeef00562) <sup>_2025-06-23 13:45:22 +1000_</sup>
  * MDEV-37052 JSON_SCHEMA_VALID stack overflow handling errors
* [Revision #29c51ee1d7](https://github.com/MariaDB/server/commit/29c51ee1d7) <sup>_2023-05-30 11:01:42 +0100_</sup>
  * MDEV-35826 Fix COLUMNSTORE in Debian CI builds
* [Revision #13e9f2d65b](https://github.com/MariaDB/server/commit/13e9f2d65b) <sup>_2025-07-03 01:01:12 +0200_</sup>
  * MDEV-37143 mariabackup fails on Windows with "SSL certificate is self-signed"
* [Revision #ef9adb569e](https://github.com/MariaDB/server/commit/ef9adb569e) <sup>_2025-07-02 17:50:24 +0700_</sup>
  * MDEV-32694: ASAN errors in Binary_string::alloced_length / reset_stmt_params
* [Revision #c742cc94ba](https://github.com/MariaDB/server/commit/c742cc94ba) <sup>_2025-06-23 15:38:49 +0200_</sup>
  * MDEV-35611 ALTER IF EXISTS assertions in sql_errno with statement timeout
* [Revision #6e9e48648a](https://github.com/MariaDB/server/commit/6e9e48648a) <sup>_2025-06-26 11:12:08 +0700_</sup>
  * MDEV-34322: ASAN heap-buffer-overflow in Field::is_null / Item_param::assign_default or bogus ER_BAD_NULL_ERROR
* [Revision #dad29f2630](https://github.com/MariaDB/server/commit/dad29f2630) <sup>_2025-06-24 15:20:25 +1000_</sup>
  * MDEV-36697: Wrong server.cnf group for version
* [Revision #e63e0e4c6f](https://github.com/MariaDB/server/commit/e63e0e4c6f) <sup>_2025-06-18 23:42:02 +0200_</sup>
  * MDEV-36904 Improve runtime DLL packaging on Windows
* <sup>_Merge_</sup> [<sup>_Revision #89c7e2b9c7_</sup>](https://github.com/MariaDB/server/commit/89c7e2b9c7) <sup>_2025-06-17 09:50:22 +0200 - Merge branch '10.11' into 11.4_</sup>
* [Revision #9bf0492b7d](https://github.com/MariaDB/server/commit/9bf0492b7d) <sup>_2025-06-10 11:53:45 +0200_</sup>
  * MDEV-36904 Improve runtime dependency packaging on Windows
* [Revision #8c6cbb3360](https://github.com/MariaDB/server/commit/8c6cbb3360) <sup>_2025-05-28 01:55:39 +0200_</sup>
  * MDEV-25870 followup : pmull support on Windows ARM64
* [Revision #fe10645eb7](https://github.com/MariaDB/server/commit/fe10645eb7) <sup>_2025-05-27 10:20:31 +0200_</sup>
  * MDEV-26713 post-fix: don't run charset_client_win_utf8mb4.test in parallel mtr
* [Revision #aaccf99fdb](https://github.com/MariaDB/server/commit/aaccf99fdb) <sup>_2025-05-23 09:19:08 +0200_</sup>
  * MDEV-36885 Windows/ARM64 - build and test on CI
* [Revision #d665810cf0](https://github.com/MariaDB/server/commit/d665810cf0) <sup>_2025-05-23 14:47:00 +0200_</sup>
  * Windows/ARM64 - fix build with clang-cl
* [Revision #be48b3ee59](https://github.com/MariaDB/server/commit/be48b3ee59) <sup>_2025-05-22 07:17:22 +0000_</sup>
  * Fix mariadb-upgrade-service crash on Windows/ARM64
* [Revision #4af231b1d1](https://github.com/MariaDB/server/commit/4af231b1d1) <sup>_2025-05-21 21:12:40 +0200_</sup>
  * Windows/ARM64 - workaround compiler bug
* [Revision #59ee33e14e](https://github.com/MariaDB/server/commit/59ee33e14e) <sup>_2025-05-21 16:32:23 +0200_</sup>
  * MDEV-32189 follow-up: Properly initialize UErrorCode for ucal_getDefaultTimeZone()
* [Revision #9e1c1d429f](https://github.com/MariaDB/server/commit/9e1c1d429f) <sup>_2025-05-23 10:34:21 +0800_</sup>
  * crc32 compatibility on Windows on ARM64
* [Revision #6c6941c9ba](https://github.com/MariaDB/server/commit/6c6941c9ba) <sup>_2025-05-22 10:25:29 -0400_</sup>
  * bump the VERSION
 
{% include "../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}
<!-- This page is licensed: CC BY-SA / Gnu FDL -->

{% @marketo/form formid="4316" formId="4316" %}
