# MariaDB 10.11.11 Changelog

[Download](https://mariadb.com/downloads/)[Release Notes](../../mariadb-community-server-release-notes/mariadb-10-11-series/mariadb-10-11-11-release-notes.md)[Changelog](mariadb-10-11-11-changelog.md)[Overview of 10.11](../../mariadb-community-server-release-notes/mariadb-10-11-series/what-is-mariadb-1011.md)

[_Alternate download from mariadb.org_](https://downloads.mariadb.org/mariadb/10.11.11/)

**Release date:** 4 Feb 2025

For the highlights of this release, see the[release notes](../../mariadb-community-server-release-notes/mariadb-10-11-series/mariadb-10-11-11-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/server/tree/10.11) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Includes all fixes from [MariaDB 10.6.21](../changelogs-mariadb-106-series/mariadb-10-6-21-changelog.md)
* Merge [Revision #e69f8cae1a](https://github.com/MariaDB/server/commit/e69f8cae1a) 2025-01-30 11:55:13 +0100 - Merge branch '10.6' into 10.11
* [Revision #0459517562](https://github.com/MariaDB/server/commit/0459517562)\
  2025-01-30 11:42:21 +0100
  * [MDEV-35169](https://jira.mariadb.org/browse/MDEV-35169) cleanup after the test
* [Revision #f6e00abda0](https://github.com/MariaDB/server/commit/f6e00abda0)\
  2025-01-28 11:56:35 +0530
  * [MDEV-35169](https://jira.mariadb.org/browse/MDEV-35169) ALTER TABLE...IMPORT TABLESPACE does not work with INDEX DESC
* [Revision #24c9033947](https://github.com/MariaDB/server/commit/24c9033947)\
  2025-01-22 17:14:33 +0400
  * [MDEV-35538](https://jira.mariadb.org/browse/MDEV-35538) UBSAN: nullptr-with-offset: runtime error: applying zero offset to null pointer in check\_rules and in init\_weight\_level
* [Revision #91585fff3e](https://github.com/MariaDB/server/commit/91585fff3e)\
  2024-12-16 19:56:09 -0700
  * [MDEV-35665](https://jira.mariadb.org/browse/MDEV-35665) Potential Buffer Overrun in Gtid\_log\_event::write()
* [Revision #661daf0636](https://github.com/MariaDB/server/commit/661daf0636)\
  2025-01-20 18:10:57 +0100
  * [MDEV-31298](https://jira.mariadb.org/browse/MDEV-31298) Assertion `!check_foreigns' failed in trx_mod_table_time_t* trx_t::check_bulk_buffer(dict_table_t*), Assertion` table->skip\_alter\_undo || !check\_unique\_secondary' failed in trx\_t::check\_bulk\_buffer
* [Revision #e551070ba4](https://github.com/MariaDB/server/commit/e551070ba4)\
  2024-11-29 19:04:06 +0400
  * [MDEV-35468](https://jira.mariadb.org/browse/MDEV-35468) UUID primary key filtering return incorrect results
* [Revision #3158af03bd](https://github.com/MariaDB/server/commit/3158af03bd)\
  2025-01-16 21:20:58 +0400
  * A cleanup for [MDEV-35427](https://jira.mariadb.org/browse/MDEV-35427): recording new type\_uuid\_ps.result
* [Revision #c8ef86cc8b](https://github.com/MariaDB/server/commit/c8ef86cc8b)\
  2025-01-16 21:04:39 +0400
  * A cleanup for [MDEV-35427](https://jira.mariadb.org/browse/MDEV-35427) to avoid dependency from the current date
* [Revision #2d42e9ff7d](https://github.com/MariaDB/server/commit/2d42e9ff7d)\
  2025-01-15 18:30:03 +0530
  * [MDEV-34703](https://jira.mariadb.org/browse/MDEV-34703) LOAD DATA INFILE using Innodb bulk load aborts
* [Revision #f4e999d753](https://github.com/MariaDB/server/commit/f4e999d753)\
  2025-01-15 13:18:12 +0400
  * [MDEV-35427](https://jira.mariadb.org/browse/MDEV-35427) Assertion \`is\_null() >= item->null\_value' failed in Timestamp\_or\_zero\_datetime\_native\_null::Timestamp\_or\_zero\_datetime\_native\_null on EXECUTE
* [Revision #4469540d39](https://github.com/MariaDB/server/commit/4469540d39)\
  2025-01-14 14:01:28 +0100
  * [MDEV-35810](https://jira.mariadb.org/browse/MDEV-35810) fix test results
* [Revision #b04fb9fb43](https://github.com/MariaDB/server/commit/b04fb9fb43)\
  2025-01-14 13:56:19 +0100
  * [MDEV-34062](https://jira.mariadb.org/browse/MDEV-34062) compilation failure on 32bit
* [Revision #9d80422f79](https://github.com/MariaDB/server/commit/9d80422f79)\
  2025-01-14 13:49:24 +0100
  * [MDEV-26266](https://jira.mariadb.org/browse/MDEV-26266) disable the test on 10.11 for now
* [Revision #e55fe2c2e3](https://github.com/MariaDB/server/commit/e55fe2c2e3)\
  2024-12-18 15:25:10 +1100
  * [MDEV-32686](https://jira.mariadb.org/browse/MDEV-32686) Use Red Hat package notes in compilation
* [Revision #5335681f67](https://github.com/MariaDB/server/commit/5335681f67)\
  2024-12-12 08:51:11 +1100
  * [MDEV-32686](https://jira.mariadb.org/browse/MDEV-32686): Debian: include ELF package notes
* [Revision #46aaf328ce](https://github.com/MariaDB/server/commit/46aaf328ce)\
  2025-01-13 16:57:11 +0200
  * [MDEV-35830](https://jira.mariadb.org/browse/MDEV-35830) Fix innodb\_undo\_log\_truncate in backup
* [Revision #aa35f62f1c](https://github.com/MariaDB/server/commit/aa35f62f1c)\
  2025-01-13 10:41:40 +0200
  * [MDEV-35810](https://jira.mariadb.org/browse/MDEV-35810) Missing error handling in log resizing
* [Revision #4fc3a44bab](https://github.com/MariaDB/server/commit/4fc3a44bab)\
  2025-01-13 07:28:40 +0200
  * [MDEV-33447](https://jira.mariadb.org/browse/MDEV-33447) fixup: pmem\_persist() on RISC-V and LoongArch
* [Revision #42e6058629](https://github.com/MariaDB/server/commit/42e6058629)\
  2025-01-13 07:27:17 +0200
  * [MDEV-35785](https://jira.mariadb.org/browse/MDEV-35785) innodb\_log\_file\_mmap is not defined on 32-bit systems
* [Revision #f361ad75b3](https://github.com/MariaDB/server/commit/f361ad75b3)\
  2025-01-09 17:33:47 -0700
  * [MDEV-35431](https://jira.mariadb.org/browse/MDEV-35431): fix InnoDB flags error size specifier
* Merge [Revision #221aa5e08f](https://github.com/MariaDB/server/commit/221aa5e08f) 2025-01-10 13:14:42 +0100 - Merge branch '10.6' into 10.11
* [Revision #311e88c67a](https://github.com/MariaDB/server/commit/311e88c67a)\
  2025-01-10 13:11:09 +0100
  * fix rocksdb tests for buildbot
* [Revision #542edc7743](https://github.com/MariaDB/server/commit/542edc7743)\
  2025-01-09 19:34:01 +0100
  * [MDEV-35720](https://jira.mariadb.org/browse/MDEV-35720) fix the test case
* [Revision #4704435068](https://github.com/MariaDB/server/commit/4704435068)\
  2025-01-10 08:15:09 +0200
  * [MDEV-35802](https://jira.mariadb.org/browse/MDEV-35802) Race condition in log\_t::persist()
* [Revision #81633f47c3](https://github.com/MariaDB/server/commit/81633f47c3)\
  2025-01-09 13:21:38 +0200
  * [MDEV-35796](https://jira.mariadb.org/browse/MDEV-35796) OPT\_PAGE\_CHECKSUM is ignored if innodb\_encrypt\_log=ON
* [Revision #ed13d93a25](https://github.com/MariaDB/server/commit/ed13d93a25)\
  2025-01-09 13:18:42 +0200
  * Fix mariadb-backup --backup with innodb\_undo\_log\_truncate=ON
* [Revision #ea19a6b38c](https://github.com/MariaDB/server/commit/ea19a6b38c)\
  2025-01-09 13:18:30 +0200
  * [MDEV-35699](https://jira.mariadb.org/browse/MDEV-35699) Multi-batch recovery occasionally fails
* [Revision #28b2958082](https://github.com/MariaDB/server/commit/28b2958082)\
  2024-09-20 02:59:10 +0000
  * Add MTR to verify behavior on incompatible TLS configuration
* [Revision #2294ecdf0e](https://github.com/MariaDB/server/commit/2294ecdf0e)\
  2024-09-20 01:05:52 +0000
  * Add MTR to ensure startup fails with invalid ssl-cipher
* Merge [Revision #420d9eb27f](https://github.com/MariaDB/server/commit/420d9eb27f) 2025-01-08 12:51:26 +0200 - Merge 10.6 into 10.11
* [Revision #48b724047e](https://github.com/MariaDB/server/commit/48b724047e)\
  2025-01-02 17:34:24 +0530
  * [MDEV-34119](https://jira.mariadb.org/browse/MDEV-34119) Assertion \`page\_dir\_get\_n\_heap(new\_page) == 2U' failed in dberr\_t PageBulk::init()
* Merge [Revision #3f914afd3a](https://github.com/MariaDB/server/commit/3f914afd3a) 2025-01-02 12:39:56 +0200 - Merge 10.6 into 10.11
* [Revision #95975b921e](https://github.com/MariaDB/server/commit/95975b921e)\
  2024-12-27 19:26:55 +0200
  * [MDEV-35720](https://jira.mariadb.org/browse/MDEV-35720) Add query\_time to statistics
* [Revision #ed5bba8a32](https://github.com/MariaDB/server/commit/ed5bba8a32)\
  2024-12-27 16:14:51 +0200
  * Fixed failing test case innodb.log\_file\_size\_online
* Merge [Revision #a54d151fc1](https://github.com/MariaDB/server/commit/a54d151fc1) 2024-12-19 15:38:53 +0200 - Merge 10.6 into 10.11
* [Revision #c391fb1ff1](https://github.com/MariaDB/server/commit/c391fb1ff1)\
  2024-12-16 11:50:00 +0200
  * [MDEV-35577](https://jira.mariadb.org/browse/MDEV-35577) Broken recovery after SET GLOBAL innodb\_log\_file\_size
* [Revision #b9e592a786](https://github.com/MariaDB/server/commit/b9e592a786)\
  2024-12-09 16:54:31 +0530
  * [MDEV-35475](https://jira.mariadb.org/browse/MDEV-35475) Assertion \`!rec\_offs\_nth\_extern(offsets1, n)' failed in cmp\_rec\_rec\_simple\_field
* [Revision #1a557d087c](https://github.com/MariaDB/server/commit/1a557d087c)\
  2024-12-09 12:53:38 +0200
  * [MDEV-35608](https://jira.mariadb.org/browse/MDEV-35608) Fake PMEM on /dev/shm no longer works
* [Revision #9428647be3](https://github.com/MariaDB/server/commit/9428647be3)\
  2024-12-05 14:02:09 -0500
  * [MDEV-35585](https://jira.mariadb.org/browse/MDEV-35585) unit.json\_normalize crashes on mac
* Merge [Revision #e7c6cdd842](https://github.com/MariaDB/server/commit/e7c6cdd842) 2024-12-05 10:11:58 +0100 - Merge 10.6 -> 10.11
* [Revision #aca72b326a](https://github.com/MariaDB/server/commit/aca72b326a)\
  2024-11-26 09:37:28 +1100
  * [MDEV-34815](https://jira.mariadb.org/browse/MDEV-34815) SIGILL error when executing mariadbd compiled for RISC-V with Clang
* Merge [Revision #3d23adb766](https://github.com/MariaDB/server/commit/3d23adb766) 2024-11-29 13:43:17 +0200 - Merge 10.6 into 10.11
* [Revision #27c7e73f9a](https://github.com/MariaDB/server/commit/27c7e73f9a)\
  2024-11-27 17:20:20 +1100
  * [MDEV-35513](https://jira.mariadb.org/browse/MDEV-35513) fails to compile on riscv32
* [Revision #8b057889d7](https://github.com/MariaDB/server/commit/8b057889d7)\
  2024-11-20 12:29:58 +0400
  * [MDEV-34981](https://jira.mariadb.org/browse/MDEV-34981) Functions missing from INFORMATION\_SCHEMA.SQL\_FUNCTIONS
* [Revision #c34a2feceb](https://github.com/MariaDB/server/commit/c34a2feceb)\
  2024-11-26 20:20:54 +0200
  * [MDEV-35509](https://jira.mariadb.org/browse/MDEV-35509) mariabackup.alter\_copy\_race crashes with abort in backup\_file\_op\_fail
* [Revision #e81ed928ff](https://github.com/MariaDB/server/commit/e81ed928ff)\
  2024-11-21 14:48:59 -0700
  * [MDEV-35478](https://jira.mariadb.org/browse/MDEV-35478) part 2: Redo `space_id` format fix
* [Revision #a54692a4b5](https://github.com/MariaDB/server/commit/a54692a4b5)\
  2024-11-21 17:45:26 +1100
  * main.ctype\_utf8 test fix for cursor protocol
* [Revision #db59bb62aa](https://github.com/MariaDB/server/commit/db59bb62aa)\
  2024-11-15 17:35:05 +1100
  * \[fixup] Revert an incorrect removal of some code in spider\_get\_crd in a merge
* [Revision #79cc0f9f78](https://github.com/MariaDB/server/commit/79cc0f9f78)\
  2024-11-14 19:01:07 -0700
  * [MDEV-11675](https://jira.mariadb.org/browse/MDEV-11675) fixup: Fill in the GTID TODO
* [Revision #687377633d](https://github.com/MariaDB/server/commit/687377633d)\
  2024-09-13 17:59:47 -0600
  * Extract some of #3360 fixes to 10.11.x
* [Revision #c72221e2f8](https://github.com/MariaDB/server/commit/c72221e2f8)\
  2024-11-13 12:04:05 +0200
  * [MDEV-35411](https://jira.mariadb.org/browse/MDEV-35411) innodb.log\_file\_size\_online occasionally fails
* Merge [Revision #a37f71bd10](https://github.com/MariaDB/server/commit/a37f71bd10) 2024-11-04 07:42:26 +0100 - Merge branch '10.11' into mariadb-10.11.10
* [Revision #e60fd6c204](https://github.com/MariaDB/server/commit/e60fd6c204)\
  2024-11-02 11:52:03 +0400
  * [MDEV-28767](https://jira.mariadb.org/browse/MDEV-28767) Collation "binary" is not accepted for databases, tables, columns
* [Revision #cca85eb16e](https://github.com/MariaDB/server/commit/cca85eb16e)\
  2024-11-01 11:38:20 -0400
  * bump the VERSION

{% @marketo/form formid="4316" formId="4316" %}
