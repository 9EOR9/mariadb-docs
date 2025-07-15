# MariaDB 10.11.9 Changelog

{% include "../../../../.gitbook/includes/latest-10.11 (2).md" %}

<a href="https://downloads.mariadb.org/mariadb/10.11.9/" class="button primary">Download</a> <a href="../../mariadb-10-11-series/mariadb-10-11-9-release-notes.md" class="button secondary">Release Notes</a> <a href="mariadb-10-11-9-changelog.md" class="button secondary">Changelog</a> <a href="../../mariadb-10-11-series/what-is-mariadb-1011.md" class="button secondary">Overview of 10.11</a>

**Release date:** 8 Aug 2024

For the highlights of this release, see the [release notes](../../mariadb-10-11-series/mariadb-10-11-9-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On [GitHub](https://github.com/MariaDB/server/tree/10.11) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Includes all fixes from [MariaDB 10.6.19](../changelogs-mariadb-106-series/mariadb-10-6-19-changelog.md)
* Merge [Revision #0e8fb977b0](https://github.com/MariaDB/server/commit/0e8fb977b0) 2024-08-03 09:15:40 +0200 - Merge branch '10.6' into 10.11
* [Revision #9ab37940dd](https://github.com/MariaDB/server/commit/9ab37940dd)\
  2024-08-02 12:19:27 +1000
  * [MDEV-33750](https://jira.mariadb.org/browse/MDEV-33750): postfix debian-start.inc
* [Revision #1c8af2ae53](https://github.com/MariaDB/server/commit/1c8af2ae53)\
  2024-07-30 11:58:02 +0300
  * [MDEV-34422](https://jira.mariadb.org/browse/MDEV-34422) Corrupted ib\_logfile0 due to uninitialized log\_sys.lsn\_lock
* [Revision #cc8eefb0dc](https://github.com/MariaDB/server/commit/cc8eefb0dc)\
  2024-07-30 11:59:01 +0530
  * [MDEV-33087](https://jira.mariadb.org/browse/MDEV-33087) ALTER TABLE...ALGORITHM=COPY should build indexes more efficiently
* [Revision #2844895766](https://github.com/MariaDB/server/commit/2844895766)\
  2024-07-24 11:27:05 +0200
  * disabling view protcol untill fix
* [Revision #c944cd6fec](https://github.com/MariaDB/server/commit/c944cd6fec)\
  2024-07-22 20:52:26 +0300
  * [MDEV-15393](https://jira.mariadb.org/browse/MDEV-15393) post-push: complete rpl\_mysqldump\_gtid\_slave\_pos fixes.
* Merge [Revision #0fe39d368a](https://github.com/MariaDB/server/commit/0fe39d368a) 2024-07-20 08:16:24 +0200 - Merge branch '10.6' into 10.11
* [Revision #0f6f1114d4](https://github.com/MariaDB/server/commit/0f6f1114d4)\
  2024-07-19 15:00:10 +0200
  * new libfmt 11.0.1
* [Revision #d94f34c1ed](https://github.com/MariaDB/server/commit/d94f34c1ed)\
  2024-06-14 10:11:18 +0300
  * [MDEV-33750](https://jira.mariadb.org/browse/MDEV-33750): Brand some mysql stuff to mariadb
* [Revision #c22d01c91d](https://github.com/MariaDB/server/commit/c22d01c91d)\
  2024-05-29 09:36:00 +0300
  * [MDEV-33750](https://jira.mariadb.org/browse/MDEV-33750): Conflict with Debian libmariadbd19t64
* [Revision #91336f6a18](https://github.com/MariaDB/server/commit/91336f6a18)\
  2024-05-27 13:25:26 +0300
  * [MDEV-33750](https://jira.mariadb.org/browse/MDEV-33750): Update Salsa-CI file
* [Revision #74aea60d92](https://github.com/MariaDB/server/commit/74aea60d92)\
  2024-05-10 10:23:27 +0300
  * [MDEV-33750](https://jira.mariadb.org/browse/MDEV-33750): Update few Debian Salsa-CI tests from upstream to make smoke test pass
* [Revision #89a638f4b8](https://github.com/MariaDB/server/commit/89a638f4b8)\
  2024-05-10 10:09:03 +0300
  * [MDEV-33750](https://jira.mariadb.org/browse/MDEV-33750): Sync smoke test from newer version of Debian Salsa-CI
* [Revision #4c1e4ba62e](https://github.com/MariaDB/server/commit/4c1e4ba62e)\
  2024-05-06 13:04:14 +0300
  * [MDEV-33750](https://jira.mariadb.org/browse/MDEV-33750): Remove seq in Debian init.d for-loop
* [Revision #7ae9505106](https://github.com/MariaDB/server/commit/7ae9505106)\
  2024-05-06 12:30:29 +0300
  * [MDEV-33750](https://jira.mariadb.org/browse/MDEV-33750): Rework MyISAM recovery script
* [Revision #af124c4f1c](https://github.com/MariaDB/server/commit/af124c4f1c)\
  2023-01-02 17:21:44 -0800
  * [MDEV-33750](https://jira.mariadb.org/browse/MDEV-33750): Make SysV init more verbose in case of MariaDB start failures
* [Revision #3f44efaa17](https://github.com/MariaDB/server/commit/3f44efaa17)\
  2023-10-07 20:31:39 -0700
  * [MDEV-33750](https://jira.mariadb.org/browse/MDEV-33750): Make sure that datadir always has some value and exists
* [Revision #2adaf5c261](https://github.com/MariaDB/server/commit/2adaf5c261)\
  2023-10-07 19:42:31 -0700
  * [MDEV-33750](https://jira.mariadb.org/browse/MDEV-33750): Sync maintainer scripts etc with latest downstream 10.11.5 in Debian
* [Revision #5000d1ba6e](https://github.com/MariaDB/server/commit/5000d1ba6e)\
  2023-10-07 19:28:43 -0700
  * [MDEV-33750](https://jira.mariadb.org/browse/MDEV-33750): Increase MTR verbosity and unify skip test lists usage
* [Revision #f79f3ada24](https://github.com/MariaDB/server/commit/f79f3ada24)\
  2023-05-12 10:51:10 -0700
  * [MDEV-33750](https://jira.mariadb.org/browse/MDEV-33750): Fix DPKG\_GENSYMBOLS\_CHECK\_LEVEL so it actually takes effect
* [Revision #b11892c9fb](https://github.com/MariaDB/server/commit/b11892c9fb)\
  2023-03-25 21:55:27 -0700
  * [MDEV-33750](https://jira.mariadb.org/browse/MDEV-33750): Fix Lintian warnings
* [Revision #9e9211215c](https://github.com/MariaDB/server/commit/9e9211215c)\
  2023-03-18 13:54:34 -0700
  * [MDEV-33750](https://jira.mariadb.org/browse/MDEV-33750): Enable mariadb-plugin-rocksdb for riscv64
* [Revision #bccdc72536](https://github.com/MariaDB/server/commit/bccdc72536)\
  2024-05-18 10:01:00 +0300
  * [MDEV-34191](https://jira.mariadb.org/browse/MDEV-34191): Make sure that Debian respects systemd disabled
* [Revision #70e3c144b3](https://github.com/MariaDB/server/commit/70e3c144b3)\
  2024-06-26 10:14:53 +0300
  * [MDEV-34456](https://jira.mariadb.org/browse/MDEV-34456): Move mariadb.pc to not-installed
* [Revision #b41168c6b5](https://github.com/MariaDB/server/commit/b41168c6b5)\
  2024-05-14 13:06:48 +0300
  * [MDEV-33837](https://jira.mariadb.org/browse/MDEV-33837): Suspend package-contains-documentation-outside-usr-share-doc warnings
* [Revision #56087d0d15](https://github.com/MariaDB/server/commit/56087d0d15)\
  2024-05-14 12:00:06 +0300
  * [MDEV-33837](https://jira.mariadb.org/browse/MDEV-33837): Fix spare-manual-page warnings in Debian lintian
* [Revision #3e384d830e](https://github.com/MariaDB/server/commit/3e384d830e)\
  2024-05-14 10:48:25 +0300
  * [MDEV-33837](https://jira.mariadb.org/browse/MDEV-33837): Remove unneeded lintian override in libmariadb-dev
* [Revision #cdeb30647f](https://github.com/MariaDB/server/commit/cdeb30647f)\
  2024-05-08 10:40:33 +0300
  * [MDEV-33837](https://jira.mariadb.org/browse/MDEV-33837): Suspend lintian warnings for description is synopsis
* [Revision #280035bf82](https://github.com/MariaDB/server/commit/280035bf82)\
  2024-05-14 10:29:18 +0300
  * [MDEV-33837](https://jira.mariadb.org/browse/MDEV-33837): Remove purposed spelling errors
* [Revision #659a596ca5](https://github.com/MariaDB/server/commit/659a596ca5)\
  2024-05-14 13:15:47 +0300
  * [MDEV-33837](https://jira.mariadb.org/browse/MDEV-33837): Lintian warns there are typos in manuals which are being handled
* [Revision #3607ecdfb9](https://github.com/MariaDB/server/commit/3607ecdfb9)\
  2024-04-29 11:16:16 +0300
  * [MDEV-33837](https://jira.mariadb.org/browse/MDEV-33837): Remove autogenerated files in columnstore warnings
* [Revision #8f87f9c745](https://github.com/MariaDB/server/commit/8f87f9c745)\
  2024-05-14 11:54:18 +0300
  * [MDEV-33837](https://jira.mariadb.org/browse/MDEV-33837): Remove conflicts warnings from lintian
* [Revision #517d9515f1](https://github.com/MariaDB/server/commit/517d9515f1)\
  2024-05-14 11:51:27 +0300
  * [MDEV-33837](https://jira.mariadb.org/browse/MDEV-33837): Remove false-positive Bash warnings from lintian output
* [Revision #ddefc59bc8](https://github.com/MariaDB/server/commit/ddefc59bc8)\
  2024-04-29 10:20:29 +0300
  * [MDEV-33837](https://jira.mariadb.org/browse/MDEV-33837): Fix some miscellaneous lintian warnings
* [Revision #cfec45db14](https://github.com/MariaDB/server/commit/cfec45db14)\
  2024-04-09 13:51:32 +0300
  * [MDEV-33837](https://jira.mariadb.org/browse/MDEV-33837): Fix unwanted-path-too-specific specific warning
* [Revision #263064c020](https://github.com/MariaDB/server/commit/263064c020)\
  2024-04-05 11:24:53 +0300
  * [MDEV-33837](https://jira.mariadb.org/browse/MDEV-33837): Add and fix lintian overrides
* [Revision #13ee9417c9](https://github.com/MariaDB/server/commit/13ee9417c9)\
  2024-04-05 10:09:12 +0300
  * [MDEV-33837](https://jira.mariadb.org/browse/MDEV-33837): Fix lintian warning that are against debian/control
* [Revision #632dd304c7](https://github.com/MariaDB/server/commit/632dd304c7)\
  2024-07-11 06:55:45 -0600
  * [MDEV-34554](https://jira.mariadb.org/browse/MDEV-34554): rpl\_change\_master\_demote sporadically fails on buildbot
* [Revision #fa80449725](https://github.com/MariaDB/server/commit/fa80449725)\
  2024-06-19 09:47:37 -0600
  * [MDEV-34274](https://jira.mariadb.org/browse/MDEV-34274): Test rpl.rpl\_change\_master\_demote frequently fails on buildbot with "IO thread should not be running..."
* [Revision #579450c2c1](https://github.com/MariaDB/server/commit/579450c2c1)\
  2024-07-04 20:38:00 +1000
  * [MDEV-34528](https://jira.mariadb.org/browse/MDEV-34528): bundle fmt version 11.0.0
* Merge [Revision #4d71a117a3](https://github.com/MariaDB/server/commit/4d71a117a3) 2024-07-08 21:14:55 +0400 - Merge remote-tracking branch 'origin/10.6' into 10.11
* Merge [Revision #034a175982](https://github.com/MariaDB/server/commit/034a175982) 2024-07-04 11:52:07 +0200 - Merge branch '10.6' into 10.11
* [Revision #f6989d1767](https://github.com/MariaDB/server/commit/f6989d1767)\
  2024-07-02 17:59:59 +0400
  * [MDEV-10865](https://jira.mariadb.org/browse/MDEV-10865) COLLATE keyword doesn't work in PREPARE query
* [Revision #c91ec6a5c1](https://github.com/MariaDB/server/commit/c91ec6a5c1)\
  2024-04-12 18:59:59 +0300
  * Added Lock\_time\_ms and Table\_catalog columns to metadata\_lock\_info
* [Revision #243dee7415](https://github.com/MariaDB/server/commit/243dee7415)\
  2024-06-24 09:17:26 +1000
  * [MDEV-34437](https://jira.mariadb.org/browse/MDEV-34437): handle error on getaddrinfo
* Merge [Revision #1d76794aba](https://github.com/MariaDB/server/commit/1d76794aba) 2024-06-28 16:03:28 +0300 - Merge 10.6 into 10.11
* [Revision #4ca355d863](https://github.com/MariaDB/server/commit/4ca355d863)\
  2024-06-27 16:38:08 +0300
  * [MDEV-33894](https://jira.mariadb.org/browse/MDEV-33894): Resurrect innodb\_log\_write\_ahead\_size
* Merge [Revision #27a3366663](https://github.com/MariaDB/server/commit/27a3366663) 2024-06-27 10:26:09 +0300 - Merge 10.6 into 10.11
* [Revision #77c465d5aa](https://github.com/MariaDB/server/commit/77c465d5aa)\
  2024-06-25 11:11:36 +0700
  * [MDEV-34171](https://jira.mariadb.org/browse/MDEV-34171): Memory leakage is detected on running the test versioning.partition
* Merge [Revision #34813c1aa0](https://github.com/MariaDB/server/commit/34813c1aa0) 2024-06-19 15:04:07 +0300 - Merge 10.6 into 10.11
* [Revision #387bdb2a2e](https://github.com/MariaDB/server/commit/387bdb2a2e)\
  2024-06-19 14:03:31 +0300
  * [MDEV-29934](https://jira.mariadb.org/browse/MDEV-29934) rpl.rpl\_start\_alter\_chain\_basic, rpl.rpl\_start\_alter\_restart\_slave sometimes fail in BB with result content mismatch
* [Revision #c37b2a9f04](https://github.com/MariaDB/server/commit/c37b2a9f04)\
  2024-06-17 19:06:34 +0300
  * [MDEV-30460](https://jira.mariadb.org/browse/MDEV-30460) rpl.rpl\_start\_alter\_restart\_slave sometimes fails in BB with result length mismatch
* Merge [Revision #346a0c1402](https://github.com/MariaDB/server/commit/346a0c1402) 2024-06-17 09:08:07 +0300 - Merge 10.6 into 10.11
* Merge [Revision #5b89cab44f](https://github.com/MariaDB/server/commit/5b89cab44f) 2024-06-13 08:16:49 +0300 - Merge 10.6 into 10.11
* [Revision #5b39ded713](https://github.com/MariaDB/server/commit/5b39ded713)\
  2024-06-11 12:50:26 +0530
  * [MDEV-34156](https://jira.mariadb.org/browse/MDEV-34156) InnoDB fails to apply the redo log for compressed tablespace
* Merge [Revision #b81d717387](https://github.com/MariaDB/server/commit/b81d717387) 2024-06-11 12:50:10 +0300 - Merge 10.6 into 10.11
* [Revision #1bf0950b19](https://github.com/MariaDB/server/commit/1bf0950b19)\
  2024-05-13 12:08:22 +0300
  * [MDEV-34146](https://jira.mariadb.org/browse/MDEV-34146): Remove duplicate #DEBHELPER

## from MariaDB server postrm

* [Revision #76e0dc18b6](https://github.com/MariaDB/server/commit/76e0dc18b6)\
  2024-06-04 12:00:20 +0400
  * [MDEV-34288](https://jira.mariadb.org/browse/MDEV-34288) SET NAMES DEFAULT crashes `mariadbd --collation-server=utf8mb4_unicode_ci`
* [Revision #d61947550a](https://github.com/MariaDB/server/commit/d61947550a)\
  2024-05-31 19:37:51 +0200
  * fix a typo
* Merge [Revision #22774ddb53](https://github.com/MariaDB/server/commit/22774ddb53) 2024-05-31 09:13:40 +1000 - Merge branch '10.6' into 10.11
* Merge [Revision #22ba7e4ff8](https://github.com/MariaDB/server/commit/22ba7e4ff8) 2024-05-30 16:04:00 +0300 - Merge 10.6 into 10.11
* [Revision #a960e95feb](https://github.com/MariaDB/server/commit/a960e95feb)\
  2024-05-21 08:15:28 -0400
  * don't require resolveip if it won't be used
* [Revision #82ba486e54](https://github.com/MariaDB/server/commit/82ba486e54)\
  2024-05-24 10:06:11 +0300
  * [MDEV-4742](https://jira.mariadb.org/browse/MDEV-4742) fixup: g++-14 -Wmaybe-uninitialized
* [Revision #f146ba82c4](https://github.com/MariaDB/server/commit/f146ba82c4)\
  2024-05-23 12:13:39 +1000
  * [MDEV-34206](https://jira.mariadb.org/browse/MDEV-34206) compile failure: fmt use incompatible with libfmt-10.2.\[2]+ (7.1.3 compat)
* [Revision #4375245d5d](https://github.com/MariaDB/server/commit/4375245d5d)\
  2024-05-22 17:43:17 +1000
  * [MDEV-34206](https://jira.mariadb.org/browse/MDEV-34206) compile failure: fmt use incompatible with libfmt-10.2.\[2]+
* [Revision #be0dfcdb99](https://github.com/MariaDB/server/commit/be0dfcdb99)\
  2024-05-22 13:16:10 +0530
  * [MDEV-34200](https://jira.mariadb.org/browse/MDEV-34200) InnoDB tries to write to read-only system tablespace in buf\_dblwr\_t::init\_or\_load\_pages()
* [Revision #f01e6503f4](https://github.com/MariaDB/server/commit/f01e6503f4)\
  2024-05-18 16:35:28 +0200
  * [MDEV-34194](https://jira.mariadb.org/browse/MDEV-34194): Fix spelling mistake 'depricated'
* [Revision #1bf9e1a79a](https://github.com/MariaDB/server/commit/1bf9e1a79a)\
  2024-05-15 10:54:18 -0400
  * bump the VERSION

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
