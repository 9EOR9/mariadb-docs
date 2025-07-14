# MariaDB 11.8.1 Changelog

[Download](https://mariadb.com/downloads/)[Release Notes](../../mariadb-11-8-series/mariadb-11-8-1-release-notes.md)[Changelog](mariadb-11-8-1-changelog.md)[Overview of 11.8](../../mariadb-11-8-series/what-is-mariadb-118.md)

[_Alternate download from mariadb.org_](https://downloads.mariadb.org/mariadb/11.8.1/)

**Release date:** 13 Feb 2025

For the highlights of this release, see the[release notes](../../mariadb-11-8-series/mariadb-11-8-1-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/server/tree/11.8) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Changes from [11.8.0](../../mariadb-11-8-series/mariadb-11-8-0-release-notes.md) are also included in this changelog
* Includes all fixes from [MariaDB 11.7.2](../changelogs-mariadb-11-7-series/mariadb-11-7-2-changelog.md)
* [Revision #1c4aed7c68](https://github.com/MariaDB/server/commit/1c4aed7c68)\
  2024-08-15 01:21:11 -0600
  * Update `my_snprintf`’s last loose ends to suffixes
* [Revision #5de8e2dde3](https://github.com/MariaDB/server/commit/5de8e2dde3)\
  2024-08-14 23:52:58 -0600
  * Update `errmsg-utf8.txt` re `my_snprintf` suffixes
* [Revision #202c2fb151](https://github.com/MariaDB/server/commit/202c2fb151)\
  2024-08-12 22:08:50 -0600
  * `make abi_update`
* [Revision #c8783757d6](https://github.com/MariaDB/server/commit/c8783757d6)\
  2024-10-13 19:27:37 -0600
  * Tag rest of my\_vsnprintf users w/ ATTRIBUTE\_FORMAT
* [Revision #63b0ee26f7](https://github.com/MariaDB/server/commit/63b0ee26f7)\
  2024-08-12 20:23:21 -0600
  * Tag ALL `my_error_reporter`s with `ATTRIBUTE_FORMAT`
* [Revision #1c315b3fb1](https://github.com/MariaDB/server/commit/1c315b3fb1)\
  2024-08-12 18:19:15 -0600
  * Tag `myisamdef.h` printers with `ATTRIBUTE_FORMAT`
* [Revision #302caa9549](https://github.com/MariaDB/server/commit/302caa9549)\
  2024-08-12 17:34:04 -0600
  * Tag the `logger` service with `ATTRIBUTE_FORMAT`
* [Revision #2392bd02d8](https://github.com/MariaDB/server/commit/2392bd02d8)\
  2025-01-12 22:03:23 -0700
  * Tag the `sql/log.h` family with `ATTRIBUTE_FORMAT`
* [Revision #21dfef474c](https://github.com/MariaDB/server/commit/21dfef474c)\
  2024-08-05 14:39:09 -0600
  * Reënable ATTRIBUTE\_FORMAT on DBUG\_PRINT & t/eprint
* [Revision #d5ba6f71b9](https://github.com/MariaDB/server/commit/d5ba6f71b9)\
  2025-01-12 21:55:23 -0700
  * Tag `push_warning_printf` with `ATTRIBUTE_FORMAT`
* [Revision #2047483417](https://github.com/MariaDB/server/commit/2047483417)\
  2024-07-31 22:42:56 -0600
  * Tag `my_printf_error` with `ATTRIBUTE_FORMAT`
* [Revision #618afa32ce](https://github.com/MariaDB/server/commit/618afa32ce)\
  2024-07-29 19:57:13 -0600
  * Tag `mysqltest` formatters with `ATTRIBUTE_FORMAT`
* [Revision #5100773ab9](https://github.com/MariaDB/server/commit/5100773ab9)\
  2024-06-28 20:48:51 -0600
  * Tag `my_vsnprintf.c` with `ATTRIBUTE_FORMAT`
* [Revision #f3617981ad](https://github.com/MariaDB/server/commit/f3617981ad)\
  2025-01-17 12:50:02 -0700
  * `unittest/mytap/tap.h`: Use `ATTRIBUTE_FORMAT`
* [Revision #ab50aad15d](https://github.com/MariaDB/server/commit/ab50aad15d)\
  2024-08-15 22:56:39 -0600
  * Remove ``%`s`` `%b` `%M` `%T` from `my_vsnprintf`
* [Revision #6a182553ce](https://github.com/MariaDB/server/commit/6a182553ce)\
  2024-08-11 19:58:11 -0600
  * Rename `my_snprintf`’s `%uE` to `%iE`
* [Revision #891177418e](https://github.com/MariaDB/server/commit/891177418e)\
  2024-06-22 16:11:19 -0600
  * Make service\_my\_snprintf.h doc _more professional_
* [Revision #b668a960cd](https://github.com/MariaDB/server/commit/b668a960cd)\
  2024-07-25 21:57:06 -0600
  * [MDEV-21978](https://jira.mariadb.org/browse/MDEV-21978) Add `%sQ`, `%sB`, `%uE` & `%sT` to `my_vsnprintf`
* [Revision #06851e7f77](https://github.com/MariaDB/server/commit/06851e7f77)\
  2024-06-04 19:35:46 -0600
  * Merge `vsnprintf` `%b`, `%T` & `%M` code into `%s`/`%u`
* [Revision #9799777992](https://github.com/MariaDB/server/commit/9799777992)\
  2025-02-05 17:26:32 +0100
  * [MDEV-35919](https://jira.mariadb.org/browse/MDEV-35919) Server crashes in Item\_func\_vec\_distance::fix\_length\_and\_dec upon reading from I\_S table
* [Revision #49821f21ce](https://github.com/MariaDB/server/commit/49821f21ce)\
  2024-12-04 17:51:23 +0100
  * [MDEV-9158](https://jira.mariadb.org/browse/MDEV-9158) post-merge fixes
* [Revision #4dee592450](https://github.com/MariaDB/server/commit/4dee592450)\
  2023-04-21 10:44:44 +0800
  * [MDEV-9158](https://jira.mariadb.org/browse/MDEV-9158) Read max size bytes from encryption key file and ignore remain bytes
* [Revision #e7f7789482](https://github.com/MariaDB/server/commit/e7f7789482)\
  2024-12-13 11:56:31 +0100
  * cleanup: `select ... into` tests
* Merge [Revision #9ee09a33bb](https://github.com/MariaDB/server/commit/9ee09a33bb) 2025-02-11 20:29:43 +0100 - Merge branch '11.7' into 11.8
* [Revision #c516bea30a](https://github.com/MariaDB/server/commit/c516bea30a)\
  2025-02-10 12:50:19 +0200
  * Update mariadb-import man page with --innodb-optimize-keys option
* [Revision #9e3a541d1e](https://github.com/MariaDB/server/commit/9e3a541d1e)\
  2025-02-10 13:27:59 +1100
  * [MDEV-35049](https://jira.mariadb.org/browse/MDEV-35049): Use CRC-32C and avoid allocating heap (postfix)
* [Revision #2e1ade5307](https://github.com/MariaDB/server/commit/2e1ade5307)\
  2025-02-07 16:57:05 +0200
  * Added missing DROP PROCEDURE to mtr test main.log\_state
* [Revision #74f70c3944](https://github.com/MariaDB/server/commit/74f70c3944)\
  2025-02-04 21:35:55 +0200
  * Fixed costs in JOIN\_TAB::estimate\_scan\_time() and HEAP
* [Revision #edd52b7fc7](https://github.com/MariaDB/server/commit/edd52b7fc7)\
  2025-02-05 10:41:11 -0500
  * [MDEV-30469](https://jira.mariadb.org/browse/MDEV-30469) Feature rebase
* [Revision #5e07d1abd4](https://github.com/MariaDB/server/commit/5e07d1abd4)\
  2025-01-29 15:21:03 -0500
  * [MDEV-35848](https://jira.mariadb.org/browse/MDEV-35848), [MDEV-35568](https://jira.mariadb.org/browse/MDEV-35568) Reintroduce delete\_while\_scanning for multi\_delete
* [Revision #8ec275da16](https://github.com/MariaDB/server/commit/8ec275da16)\
  2025-01-30 16:30:56 +0200
  * [MDEV-35955](https://jira.mariadb.org/browse/MDEV-35955) Wrong result for UPDATE ... ORDER BY LIMIT which uses tmp.table
* [Revision #5001300bd4](https://github.com/MariaDB/server/commit/5001300bd4)\
  2024-12-03 09:43:45 -0500
  * [MDEV-30469](https://jira.mariadb.org/browse/MDEV-30469) Support ORDER BY and LIMIT for multi-table DELETE, index hints for single-table DELETE
* [Revision #02dc8615f2](https://github.com/MariaDB/server/commit/02dc8615f2)\
  2024-12-03 09:48:17 -0500
  * [MDEV-30469](https://jira.mariadb.org/browse/MDEV-30469) (refactoring) Support ORDER BY and LIMIT for multi-table DELETE...
* [Revision #dfdbec1636](https://github.com/MariaDB/server/commit/dfdbec1636)\
  2024-11-21 14:55:51 +0800
  * [MDEV-10862](https://jira.mariadb.org/browse/MDEV-10862): Stored procedures: default values for parameters (optional parameters)
* [Revision #5a8e6230d7](https://github.com/MariaDB/server/commit/5a8e6230d7)\
  2024-12-29 12:50:04 +0400
  * [MDEV-34189](https://jira.mariadb.org/browse/MDEV-34189) Unexpected error on `WHERE inet6col`
* [Revision #d1ba623677](https://github.com/MariaDB/server/commit/d1ba623677)\
  2024-12-03 17:17:17 -0800
  * All-green GitLab CI in main branch in January 2025
* [Revision #9f5adf0ce4](https://github.com/MariaDB/server/commit/9f5adf0ce4)\
  2024-09-12 23:25:40 +0800
  * [MDEV-34317](https://jira.mariadb.org/browse/MDEV-34317): Implement RECORD type Implement `DECLARE TYPE type_name IS RECORD (..)` with scalar members in stored routines and anonymous blocks
* [Revision #4c956fa15b](https://github.com/MariaDB/server/commit/4c956fa15b)\
  2025-01-27 16:29:25 +0700
  * [MDEV-34724](https://jira.mariadb.org/browse/MDEV-34724): Skipping a row operation from a trigger
* [Revision #fcf7211136](https://github.com/MariaDB/server/commit/fcf7211136)\
  2025-01-26 13:58:03 +0200
  * [MDEV-35616](https://jira.mariadb.org/browse/MDEV-35616): Add basic optimizer support for virtual column: more tests
* [Revision #18e4b944bf](https://github.com/MariaDB/server/commit/18e4b944bf)\
  2025-01-16 10:24:34 +0200
  * [MDEV-35833](https://jira.mariadb.org/browse/MDEV-35833): Assertion \`marked\_for\_read()' failed for query with vcols
* [Revision #1c2a83179d](https://github.com/MariaDB/server/commit/1c2a83179d)\
  2024-11-26 14:50:41 +0200
  * [MDEV-35616](https://jira.mariadb.org/browse/MDEV-35616): Add basic optimizer support for virtual column
* [Revision #759df4cc5f](https://github.com/MariaDB/server/commit/759df4cc5f)\
  2025-01-24 19:22:02 +0700
  * [MDEV-34551](https://jira.mariadb.org/browse/MDEV-34551): Column list in the trigger definition
* [Revision #3bd23b76c5](https://github.com/MariaDB/server/commit/3bd23b76c5)\
  2025-01-23 15:15:03 +0100
  * [MDEV-34740](https://jira.mariadb.org/browse/MDEV-34740) mariadb-import: optimize index and constraint creation
* [Revision #9255206b86](https://github.com/MariaDB/server/commit/9255206b86)\
  2025-01-24 13:12:55 +0100
  * appveyor - run builds in "main" branch
* [Revision #b8fa8b9b3d](https://github.com/MariaDB/server/commit/b8fa8b9b3d)\
  2025-01-23 21:45:26 +0200
  * [MDEV-35921](https://jira.mariadb.org/browse/MDEV-35921): s3.mysqldump fails in buildbot
* [Revision #89f5d28191](https://github.com/MariaDB/server/commit/89f5d28191)\
  2024-10-23 15:17:32 +0400
  * [MDEV-22217](https://jira.mariadb.org/browse/MDEV-22217) Make OS character sets "utf8" and "utf-8" map to MariaDB character set "utf8mb4"
* [Revision #e11592aed3](https://github.com/MariaDB/server/commit/e11592aed3)\
  2024-12-09 17:11:08 +0100
  * [MDEV-35450](https://jira.mariadb.org/browse/MDEV-35450) VEC\_DISTANCE() function to autouse the available index type
* [Revision #528249a20a](https://github.com/MariaDB/server/commit/528249a20a)\
  2024-12-08 17:14:42 +0100
  * cleanup: one Item\_func\_vec\_distance class, not three
* [Revision #d2ec5ec9c2](https://github.com/MariaDB/server/commit/d2ec5ec9c2)\
  2024-12-09 20:40:29 +0100
  * cleanup: move test w/ character\_set\_results=utf16 into separate file
* [Revision #e36ca5b1a6](https://github.com/MariaDB/server/commit/e36ca5b1a6)\
  2024-12-09 12:24:03 +0100
  * cleanup: extraneous quotes in errmsg.txt
* [Revision #5482155df6](https://github.com/MariaDB/server/commit/5482155df6)\
  2025-01-17 11:41:32 +0100
  * [MDEV-34703](https://jira.mariadb.org/browse/MDEV-34703) followup - reenable Innodb bulk load in mariadb-import
* [Revision #11a6c1b30a](https://github.com/MariaDB/server/commit/11a6c1b30a)\
  2024-11-28 23:02:29 +0400
  * [MDEV-34699](https://jira.mariadb.org/browse/MDEV-34699) - mhnsw: support aarch64 SIMD instructions
* [Revision #cacaaebf01](https://github.com/MariaDB/server/commit/cacaaebf01)\
  2025-01-13 14:48:43 -0500
  * [MDEV-35837](https://jira.mariadb.org/browse/MDEV-35837) Move to c++17
* [Revision #2563839853](https://github.com/MariaDB/server/commit/2563839853)\
  2025-01-15 14:37:43 +0100
  * [MDEV-34979](https://jira.mariadb.org/browse/MDEV-34979) generate SBOM from server builds
* [Revision #18dbeae1b8](https://github.com/MariaDB/server/commit/18dbeae1b8)\
  2025-01-15 07:31:33 +0200
  * [MDEV-35849](https://jira.mariadb.org/browse/MDEV-35849): index records in a wrong order
* [Revision #3761a7fec8](https://github.com/MariaDB/server/commit/3761a7fec8)\
  2025-01-10 16:40:55 +0200
  * [MDEV-35312](https://jira.mariadb.org/browse/MDEV-35312) page\_cur\_search\_with\_match() could avoid rec\_get\_offsets()
* [Revision #793a2fc8ba](https://github.com/MariaDB/server/commit/793a2fc8ba)\
  2025-01-10 16:40:37 +0200
  * [MDEV-35049](https://jira.mariadb.org/browse/MDEV-35049): Always enable page\_cur\_search\_with\_match\_bytes()
* [Revision #4221ed1d7d](https://github.com/MariaDB/server/commit/4221ed1d7d)\
  2025-01-10 16:40:35 +0200
  * [MDEV-35049](https://jira.mariadb.org/browse/MDEV-35049): Avoid building AHI beyond unique field prefix
* [Revision #5f7b2a3ced](https://github.com/MariaDB/server/commit/5f7b2a3ced)\
  2025-01-10 16:40:34 +0200
  * [MDEV-35049](https://jira.mariadb.org/browse/MDEV-35049): Improve btr\_search\_drop\_page\_hash\_index()
* [Revision #c942b31340](https://github.com/MariaDB/server/commit/c942b31340)\
  2025-01-10 16:40:32 +0200
  * [MDEV-35049](https://jira.mariadb.org/browse/MDEV-35049): Fix bogus rebuild on BTR\_CUR\_HASH\_FAIL
* [Revision #6b58ee769f](https://github.com/MariaDB/server/commit/6b58ee769f)\
  2025-01-10 16:40:30 +0200
  * [MDEV-35049](https://jira.mariadb.org/browse/MDEV-35049): Fix bogus BTR\_CUR\_HASH\_FAIL on contention
* [Revision #68cac26108](https://github.com/MariaDB/server/commit/68cac26108)\
  2025-01-10 16:40:29 +0200
  * [MDEV-35049](https://jira.mariadb.org/browse/MDEV-35049): Fix bogus BTR\_CUR\_HASH\_FAIL on PAGE\_CUR\_LE
* [Revision #4dd6131711](https://github.com/MariaDB/server/commit/4dd6131711)\
  2025-01-10 16:40:22 +0200
  * [MDEV-35049](https://jira.mariadb.org/browse/MDEV-35049): Privatize ut\_fold\_ulint\_pair()
* [Revision #4dcb1b575b](https://github.com/MariaDB/server/commit/4dcb1b575b)\
  2025-01-10 16:39:44 +0200
  * [MDEV-35049](https://jira.mariadb.org/browse/MDEV-35049): Use CRC-32C and avoid allocating heap
* [Revision #9c8bdc6c15](https://github.com/MariaDB/server/commit/9c8bdc6c15)\
  2025-01-10 16:30:42 +0200
  * [MDEV-35049](https://jira.mariadb.org/browse/MDEV-35049): btr\_search\_check\_free\_space\_in\_heap() is a bottleneck
* Merge [Revision #5e8714b7b2](https://github.com/MariaDB/server/commit/5e8714b7b2) 2025-01-09 13:46:06 +0200 - Merge 11.7 into main
* [Revision #e021770667](https://github.com/MariaDB/server/commit/e021770667)\
  2024-11-26 11:28:57 +1100
  * [MDEV-34911](https://jira.mariadb.org/browse/MDEV-34911) Sargable substr(col, 1, n) = str
* [Revision #ae998c22b2](https://github.com/MariaDB/server/commit/ae998c22b2)\
  2024-12-18 13:50:03 +0100
  * [MDEV-35683](https://jira.mariadb.org/browse/MDEV-35683): add basic unit test for DYNAMIC\_ARRAY
* [Revision #7734c85c31](https://github.com/MariaDB/server/commit/7734c85c31)\
  2024-12-17 16:55:46 +0100
  * unittest output improvement for json\_normalize-t
* Merge [Revision #f5821aaf77](https://github.com/MariaDB/server/commit/f5821aaf77) 2024-12-04 10:02:00 +0200 - Merge 11.7 into main
* [Revision #b24ecd7ca6](https://github.com/MariaDB/server/commit/b24ecd7ca6)\
  2024-12-03 17:51:35 +0530
  * [MDEV-32250](https://jira.mariadb.org/browse/MDEV-32250) Enable --no-autocommit by default in mysqldump
* Merge [Revision #f0961301c8](https://github.com/MariaDB/server/commit/f0961301c8) 2024-12-02 17:55:44 +0200 - Merge 11.7 into main
* [Revision #e64857c25b](https://github.com/MariaDB/server/commit/e64857c25b)\
  2024-08-05 23:02:02 +0200
  * Provide a safe range for RocksDB errors
* [Revision #0fabe1dc18](https://github.com/MariaDB/server/commit/0fabe1dc18)\
  2024-11-16 12:23:55 -0700
  * Create FUNDING.yml
* [Revision #a35f744d78](https://github.com/MariaDB/server/commit/a35f744d78)\
  2023-04-08 06:14:14 +0200
  * [MDEV-31736](https://jira.mariadb.org/browse/MDEV-31736): format\_bytes implementation
* [Revision #f24d08df96](https://github.com/MariaDB/server/commit/f24d08df96)\
  2024-11-18 14:41:03 +0400
  * [MDEV-35437](https://jira.mariadb.org/browse/MDEV-35437) Suppress "This function has the same name" warnings in I\_S queries
* [Revision #eff9c198e3](https://github.com/MariaDB/server/commit/eff9c198e3)\
  2024-11-14 19:09:01 +0100
  * 11.8 branch

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
