# MariaDB 10.8.3 Changelog

The most recent release of [MariaDB 10.8](../../old-releases/release-notes-mariadb-10-8-series/what-is-mariadb-108.md) is:[**MariaDB 10.8.8**](../../old-releases/release-notes-mariadb-10-8-series/mariadb-10-8-8-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.8.8/)

[Download 10.8.3](https://mariadb.org/download/?tab=mariadb\&release=10.8.3\&product=mariadb)[Release Notes](../../old-releases/release-notes-mariadb-10-8-series/mariadb-1083-release-notes.md)[Changelog](mariadb-1083-changelog.md)[Overview of 10.8](../../old-releases/release-notes-mariadb-10-8-series/what-is-mariadb-108.md)

**Release date:** 20 May 2022

For the highlights of this release, see the [release notes](../../old-releases/release-notes-mariadb-10-8-series/mariadb-1083-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On [GitHub](https://github.com/MariaDB/server/tree/10.8) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Includes all fixes from [MariaDB 10.7.4](../changelogs-mariadb-10-7-series/mariadb-1074-changelog.md)
* Merge [Revision #b7ffccf49b](https://github.com/MariaDB/server/commit/b7ffccf49b) 2022-05-18 13:26:48 +0200 - Merge branch '10.7' into 10.8
* [Revision #5bfd9e51b3](https://github.com/MariaDB/server/commit/5bfd9e51b3)\
  2022-05-13 16:17:56 +0200
  * Stable version
* Merge [Revision #443c2a715d](https://github.com/MariaDB/server/commit/443c2a715d) 2022-05-11 12:21:36 +0200 - Merge branch '10.7' into 10.8
* [Revision #bde0b31dc5](https://github.com/MariaDB/server/commit/bde0b31dc5)\
  2022-05-08 09:57:21 +0200
  * new CC (v3.3)
* Merge [Revision #133c2129cd](https://github.com/MariaDB/server/commit/133c2129cd) 2022-04-27 10:43:00 +0300 - Merge 10.7 into 10.8
* [Revision #6948abb94c](https://github.com/MariaDB/server/commit/6948abb94c)\
  2022-04-22 12:22:28 +0300
  * Cleanup: Remove fil\_names\_write\_bogus
* [Revision #b884410a0e](https://github.com/MariaDB/server/commit/b884410a0e)\
  2022-04-12 12:45:58 +0300
  * [MDEV-28232](https://jira.mariadb.org/browse/MDEV-28232): Add missing conflict and breaks for [MariaDB 10.7](../../old-releases/release-notes-mariadb-10-7-series/what-is-mariadb-107.md)
* [Revision #7f28cbf6b7](https://github.com/MariaDB/server/commit/7f28cbf6b7)\
  2022-04-12 12:57:19 +0300
  * [MDEV-28300](https://jira.mariadb.org/browse/MDEV-28300): Add upgrade test from MariaDB version 10.7 to 10.8
* Merge [Revision #cbf9d8a8d5](https://github.com/MariaDB/server/commit/cbf9d8a8d5) 2022-04-13 17:52:27 +0900 - Merge 10.7 into 10.8
* [Revision #c5512878fe](https://github.com/MariaDB/server/commit/c5512878fe)\
  2022-04-12 10:27:18 +0300
  * [MDEV-14425](https://jira.mariadb.org/browse/MDEV-14425) fixup: Fix a typo in mariadb-backup
* [Revision #e2e4aa29db](https://github.com/MariaDB/server/commit/e2e4aa29db)\
  2022-04-07 09:17:11 +1000
  * deb: test restrictions missed in merge
* Merge [Revision #b2baeba415](https://github.com/MariaDB/server/commit/b2baeba415) 2022-04-06 13:28:25 +0300 - Merge 10.7 into 10.8
* Merge [Revision #7b06bc9a94](https://github.com/MariaDB/server/commit/7b06bc9a94) 2022-04-06 14:23:20 +1000 - Merge branch 10.7 into 10.8
* Merge [Revision #5c69e93630](https://github.com/MariaDB/server/commit/5c69e93630) 2022-03-30 09:34:07 +0300 - Merge 10.7 into 10.8
* Merge [Revision #88ce8a3d8b](https://github.com/MariaDB/server/commit/88ce8a3d8b) 2022-03-25 15:06:56 +1100 - Merge 10.7 into 10.8
* [Revision #f6fcf827b3](https://github.com/MariaDB/server/commit/f6fcf827b3)\
  2022-03-18 15:27:57 +0200
  * [MDEV-28111](https://jira.mariadb.org/browse/MDEV-28111) fixup: Correct the start-up message
* [Revision #5c11e7eead](https://github.com/MariaDB/server/commit/5c11e7eead)\
  2022-03-18 09:47:58 +0100
  * update test results
* Merge [Revision #9aea73f74f](https://github.com/MariaDB/server/commit/9aea73f74f) 2022-03-17 12:18:40 +0100 - Merge branch '10.7' into 10.8
* [Revision #c4c8830709](https://github.com/MariaDB/server/commit/c4c8830709)\
  2022-03-17 12:00:00 +0200
  * [MDEV-28111](https://jira.mariadb.org/browse/MDEV-28111) Redo log writes are being buffered on Linux for no good reason
* [Revision #86820837cb](https://github.com/MariaDB/server/commit/86820837cb)\
  2022-03-17 09:40:46 +0200
  * [MDEV-28043](https://jira.mariadb.org/browse/MDEV-28043) fixup: GCC -m32 -Wconversion
* [Revision #f7f7a3238e](https://github.com/MariaDB/server/commit/f7f7a3238e)\
  2022-03-16 09:10:16 +0200
  * [MDEV-28051](https://jira.mariadb.org/browse/MDEV-28051) Error compiling libmariadb/plugins/compress/c\_zstd.c
* Merge [Revision #9f5a3e5689](https://github.com/MariaDB/server/commit/9f5a3e5689) 2022-03-15 18:18:07 +0200 - Merge 10.7 into 10.8
* [Revision #8575d2fb39](https://github.com/MariaDB/server/commit/8575d2fb39)\
  2022-03-15 12:35:40 +0200
  * [MDEV-28043](https://jira.mariadb.org/browse/MDEV-28043) Race condition between mtr\_t::commit() and checkpoint
* Merge [Revision #18bb95b608](https://github.com/MariaDB/server/commit/18bb95b608) 2022-03-14 11:52:11 +0200 - Merge 10.7 into 10.8
* [Revision #00021a92c4](https://github.com/MariaDB/server/commit/00021a92c4)\
  2022-02-17 00:35:43 +0900
  * [MDEV-27860](https://jira.mariadb.org/browse/MDEV-27860) SIGSEGV in spider\_parse\_connect\_info on CREATE TABLE
* Merge [Revision #89cd3da48c](https://github.com/MariaDB/server/commit/89cd3da48c) 2022-03-11 15:56:59 +0200 - Merge 10.7 into 10.8
* Merge [Revision #1596ef738c](https://github.com/MariaDB/server/commit/1596ef738c) 2022-03-11 10:49:49 +0200 - Merge 10.7 into 10.8
* Merge [Revision #e8a2a70cf8](https://github.com/MariaDB/server/commit/e8a2a70cf8) 2022-03-08 10:03:45 +0200 - Merge 10.7 into 10.8
* [Revision #c8a18589de](https://github.com/MariaDB/server/commit/c8a18589de)\
  2022-03-03 11:39:24 +0200
  * Make main.desc\_index\_range more stable
* Merge [Revision #dce8a846ae](https://github.com/MariaDB/server/commit/dce8a846ae) 2022-03-03 11:34:58 +0200 - Merge 10.7 into 10.8
* [Revision #0366fb5f54](https://github.com/MariaDB/server/commit/0366fb5f54)\
  2022-01-25 13:26:21 +0900
  * [MDEV-27605](https://jira.mariadb.org/browse/MDEV-27605) ALTER .. ADD PARTITION uses wrong partition-level option values
* [Revision #c1e88a635d](https://github.com/MariaDB/server/commit/c1e88a635d)\
  2022-03-01 11:59:54 +0200
  * [MDEV-27969](https://jira.mariadb.org/browse/MDEV-27969): mtr\_t::commit() never calls buf\_pool.page\_cleaner\_wakeup()
* Merge [Revision #0a8412b5cf](https://github.com/MariaDB/server/commit/0a8412b5cf) 2022-03-01 11:58:32 +0200 - Merge 10.7 into 10.8
* Merge [Revision #32d741b5b0](https://github.com/MariaDB/server/commit/32d741b5b0) 2022-02-25 16:24:13 +0200 - Merge 10.7 into 10.8
* [Revision #a23414dd32](https://github.com/MariaDB/server/commit/a23414dd32)\
  2022-02-25 15:50:09 +0200
  * [MDEV-27939](https://jira.mariadb.org/browse/MDEV-27939) Log buffer wrap-around errors on PMEM
* [Revision #bd946a4059](https://github.com/MariaDB/server/commit/bd946a4059)\
  2021-12-09 20:13:35 +0300
  * Code cleanup: don't call subquery\_types\_allow\_materialization() on prepare
* [Revision #f23f45413f](https://github.com/MariaDB/server/commit/f23f45413f)\
  2022-02-08 16:39:10 +0100
  * [MDEV-27778](https://jira.mariadb.org/browse/MDEV-27778) md5 in FIPS crashes with OpenSSL 3.0.0
* [Revision #687f245c8e](https://github.com/MariaDB/server/commit/687f245c8e)\
  2022-02-23 14:34:07 +0100
  * don't test for obsolete DES\_ENCRYPT/DES\_DECRYPT functions
* [Revision #7e838ec0e6](https://github.com/MariaDB/server/commit/7e838ec0e6)\
  2022-02-18 17:52:55 +0100
  * don't use my\_read() in the signal handler
* [Revision #a4f0ae7c18](https://github.com/MariaDB/server/commit/a4f0ae7c18)\
  2022-02-18 16:21:08 +0100
  * UBSAN: out of bound array read in json
* Merge [Revision #50fa94ea2b](https://github.com/MariaDB/server/commit/50fa94ea2b) 2022-02-23 16:42:59 +0200 - Merge 10.7 into 10.8
* [Revision #88d5924439](https://github.com/MariaDB/server/commit/88d5924439)\
  2022-02-23 10:20:11 +0200
  * [MDEV-14425](https://jira.mariadb.org/browse/MDEV-14425) fixup for 32-bit builds
* [Revision #3e426e0147](https://github.com/MariaDB/server/commit/3e426e0147)\
  2022-02-22 22:02:21 +0100
  * [MDEV-27866](https://jira.mariadb.org/browse/MDEV-27866) Optimize log\_sys.latch and log\_sys.lsn\_lock
* [Revision #934b2d605e](https://github.com/MariaDB/server/commit/934b2d605e)\
  2022-02-22 18:56:21 +0200
  * [MDEV-27917](https://jira.mariadb.org/browse/MDEV-27917) Some redo log diagnostics is always reported as 0
* [Revision #30b036d729](https://github.com/MariaDB/server/commit/30b036d729)\
  2022-02-22 18:45:08 +0200
  * [MDEV-27916](https://jira.mariadb.org/browse/MDEV-27916) InnoDB ignores log write errors
* Merge [Revision #a3b96d4584](https://github.com/MariaDB/server/commit/a3b96d4584) 2022-02-22 13:20:18 +0200 - Merge 10.7 into 10.8
* [Revision #66dd272572](https://github.com/MariaDB/server/commit/66dd272572)\
  2022-02-21 19:31:05 +0200
  * [MDEV-27910](https://jira.mariadb.org/browse/MDEV-27910): Internal compiler error on CentOS 7 ARMv8 GCC 4.8.5
* [Revision #1c5b099a96](https://github.com/MariaDB/server/commit/1c5b099a96)\
  2022-02-17 20:06:33 +0200
  * [MDEV-27876](https://jira.mariadb.org/browse/MDEV-27876): SUX\_LOCK\_GENERIC build fails after [MDEV-27774](https://jira.mariadb.org/browse/MDEV-27774)
* [Revision #f80deb9590](https://github.com/MariaDB/server/commit/f80deb9590)\
  2022-02-17 19:38:17 +0200
  * [MDEV-27868](https://jira.mariadb.org/browse/MDEV-27868) buf\_pool.flush\_list is in the wrong order
* Merge [Revision #080676ca51](https://github.com/MariaDB/server/commit/080676ca51) 2022-02-17 14:57:49 +0200 - Merge 10.7 into 10.8
* Merge [Revision #eb25f47423](https://github.com/MariaDB/server/commit/eb25f47423) 2022-02-17 12:43:29 +0100 - Merge branch '10.7' into 10.8
* [Revision #8251a9fb93](https://github.com/MariaDB/server/commit/8251a9fb93)\
  2022-02-15 19:28:02 +0200
  * [MDEV-27848](https://jira.mariadb.org/browse/MDEV-27848) fixup: Use os\_file\_close\_func()
* [Revision #f1beeb58e6](https://github.com/MariaDB/server/commit/f1beeb58e6)\
  2022-02-15 15:03:15 +0200
  * [MDEV-27848](https://jira.mariadb.org/browse/MDEV-27848): Remove unused wait/io/file/innodb/innodb\_log\_file
* [Revision #3b06415cb8](https://github.com/MariaDB/server/commit/3b06415cb8)\
  2022-02-14 19:49:54 +0200
  * Clean up log resizing
* [Revision #73605d1813](https://github.com/MariaDB/server/commit/73605d1813)\
  2022-02-14 18:51:52 +0200
  * Clean up some @return and @retval comments
* [Revision #972b45642a](https://github.com/MariaDB/server/commit/972b45642a)\
  2022-02-14 16:24:55 +0100
  * fixup 63b9d6e7ea77e26b666 , log\_sys.write\_buf can't run in a loop
* [Revision #63b9d6e7ea](https://github.com/MariaDB/server/commit/63b9d6e7ea)\
  2022-02-14 15:39:31 +0100
  * Restore the [MDEV-26789](https://jira.mariadb.org/browse/MDEV-26789) logic, partially lost in refactoring.
* Merge [Revision #3553cfd025](https://github.com/MariaDB/server/commit/3553cfd025) 2022-02-14 09:43:29 +0200 - Merge 10.7 into 10.8
* Merge [Revision #f613014759](https://github.com/MariaDB/server/commit/f613014759) 2022-02-14 08:37:51 +0200 - Merge 10.7 into 10.8
* Merge [Revision #6c2a7d43df](https://github.com/MariaDB/server/commit/6c2a7d43df) 2022-02-14 08:37:00 +0200 - Merge mariadb-10.8.2 into 10.8
* [Revision #8274c207df](https://github.com/MariaDB/server/commit/8274c207df)\
  2022-02-12 13:09:01 -0500
  * bump the VERSION
* [Revision #bd70ae0565](https://github.com/MariaDB/server/commit/bd70ae0565)\
  2022-02-11 11:44:40 +0200
  * [MDEV-27774](https://jira.mariadb.org/browse/MDEV-27774) fixup: Replace sspin\_lock with srw\_lock
* [Revision #a635c40648](https://github.com/MariaDB/server/commit/a635c40648)\
  2022-02-10 16:37:12 +0200
  * [MDEV-27774](https://jira.mariadb.org/browse/MDEV-27774) Reduce scalability bottlenecks in mtr\_t::commit()

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
