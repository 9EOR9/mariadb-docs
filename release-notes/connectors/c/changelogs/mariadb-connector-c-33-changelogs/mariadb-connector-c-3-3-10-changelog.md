# MariaDB Connector/C 3.3.10 Changelog

[Download](https://mariadb.com/downloads/connectors)[Release Notes](../../mariadb-connector-c-33-release-notes/mariadb-connector-c-3-3-10-release-notes.md)[Changelog](mariadb-connector-c-3-3-10-changelog.md)[About MariaDB Connector/C](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-c/README.md)

**Release date:** 21 Jun 2024

For the highlights of this release, see the[release notes](../../mariadb-connector-c-33-release-notes/mariadb-connector-c-3-3-10-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-c/) you can view more\
details of the revision and view diffs of the code modified in that revision.

* [Revision #cba62ec2](https://github.com/mariadb-corporation/mariadb-connector-c/commit/cba62ec2)\
  2024-05-10 10:26:44 +0200
  * Fix character set test.
* [Revision #923a0092](https://github.com/mariadb-corporation/mariadb-connector-c/commit/923a0092)\
  2024-05-06 14:31:49 +0200
  * Added missing support for restricted\_auth in conf files
* [Revision #4d46ae76](https://github.com/mariadb-corporation/mariadb-connector-c/commit/4d46ae76)\
  2024-05-08 11:43:18 +0200
  * Merge branch '3.1' into 3.3
* [Revision #51b2a621](https://github.com/mariadb-corporation/mariadb-connector-c/commit/51b2a621)\
  2024-03-04 04:33:30 +0000
  * Fix -Wcalloc-transposed-args
* [Revision #4c1c7f37](https://github.com/mariadb-corporation/mariadb-connector-c/commit/4c1c7f37)\
  2024-03-27 16:50:20 -0700
  * Fix SSL\_read/write return value checking in ma\_tls\_async\_check\_result
* [Revision #89d11c8b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/89d11c8b)\
  2024-04-03 21:21:35 +0100
  * Fix `sys/poll.h` -> `poll.h`
* [Revision #02151b6a](https://github.com/mariadb-corporation/mariadb-connector-c/commit/02151b6a)\
  2024-04-11 14:54:08 +0300
  * Merg 3.1 into 3.3
* [Revision #dab59732](https://github.com/mariadb-corporation/mariadb-connector-c/commit/dab59732)\
  2024-04-11 14:47:28 +0300
  * Fix GCC 14 -Wcalloc-transposed-args
* [Revision #1d3fd581](https://github.com/mariadb-corporation/mariadb-connector-c/commit/1d3fd581)\
  2022-06-29 13:27:28 +0200
  * Test fix for test\_bug4236
* [Revision #8228164f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/8228164f)\
  2024-02-24 17:09:58 +0100
  * Merge branch '3.1' into 3.3
* [Revision #558ad7d6](https://github.com/mariadb-corporation/mariadb-connector-c/commit/558ad7d6)\
  2024-02-24 17:06:03 +0100
  * [CONC-677](https://jira.mariadb.org/browse/CONC-677):
* [Revision #9155b19b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/9155b19b)\
  2024-01-26 10:40:03 +0100
  * [MDEV-26579](https://jira.mariadb.org/browse/MDEV-26579) - fix resource.rc.in
* [Revision #12f3b29c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/12f3b29c)\
  2021-09-16 13:36:51 +0200
  * [MDEV-26579](https://jira.mariadb.org/browse/MDEV-26579) - post-fix, fix standalone C/C build
* [Revision #12cc91ab](https://github.com/mariadb-corporation/mariadb-connector-c/commit/12cc91ab)\
  2021-09-10 01:45:09 +0200
  * [MDEV-26579](https://jira.mariadb.org/browse/MDEV-26579) - support minor upgrades of the server MSI
* [Revision #f1a72768](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f1a72768)\
  2023-11-23 07:11:13 +0100
  * Bump version to 3.1.23
* [Revision #98b829ca](https://github.com/mariadb-corporation/mariadb-connector-c/commit/98b829ca)\
  2024-02-22 16:24:20 +0100
  * Follow up for [CONC-505](https://jira.mariadb.org/browse/CONC-505)
* [Revision #ebe19495](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ebe19495)\
  2024-02-22 09:03:51 +0100
  * Fix for [CONC-505](https://jira.mariadb.org/browse/CONC-505):
* [Revision #06d0b9bf](https://github.com/mariadb-corporation/mariadb-connector-c/commit/06d0b9bf)\
  2024-02-22 07:39:13 +0100
  * Merge branch '3.3' of [mariadb-connector-c](https://github.com/mariadb-corporation/mariadb-connector-c) into 3.3
* [Revision #f6e99af0](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f6e99af0)\
  2024-02-19 11:09:11 +0100
  * Revert "self-signed certificate verification", it's 3.4 feature
* [Revision #d7b4881d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d7b4881d)\
  2024-02-12 15:37:08 +0100
  * Merge branch '3.3' of [mariadb-connector-c](https://github.com/mariadb-corporation/mariadb-connector-c) into 3.3
* [Revision #536d9e2b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/536d9e2b)\
  2024-02-09 01:43:34 +0100
  * [MDEV-33430](https://jira.mariadb.org/browse/MDEV-33430) Fix unexpected "SSL certificate self-signed" errors on Windows
* [Revision #8dffd569](https://github.com/mariadb-corporation/mariadb-connector-c/commit/8dffd569)\
  2023-08-30 14:39:05 +0200
  * [MDEV-31857](https://jira.mariadb.org/browse/MDEV-31857) enable MYSQL\_OPT\_SSL\_VERIFY\_SERVER\_CERT by default
* [Revision #fcef411e](https://github.com/mariadb-corporation/mariadb-connector-c/commit/fcef411e)\
  2023-08-20 23:17:06 +0200
  * [MDEV-31855](https://jira.mariadb.org/browse/MDEV-31855) hash\_password\_bin for native\_password and ed25519
* [Revision #79a746f2](https://github.com/mariadb-corporation/mariadb-connector-c/commit/79a746f2)\
  2023-08-29 21:38:29 +0200
  * unix socket and named pipes are secure
* [Revision #a99570c1](https://github.com/mariadb-corporation/mariadb-connector-c/commit/a99570c1)\
  2023-08-20 14:41:03 +0200
  * [MDEV-31855](https://jira.mariadb.org/browse/MDEV-31855) SSL cert validation protocol extension
* [Revision #50f65db2](https://github.com/mariadb-corporation/mariadb-connector-c/commit/50f65db2)\
  2023-10-22 10:03:13 +0200
  * compilation warning
* [Revision #5c9eab55](https://github.com/mariadb-corporation/mariadb-connector-c/commit/5c9eab55)\
  2023-08-19 20:51:24 +0200
  * remove a redundant duplicate of plugin\_auth.h
* [Revision #2f6b5a52](https://github.com/mariadb-corporation/mariadb-connector-c/commit/2f6b5a52)\
  2023-09-08 14:10:51 +0200
  * typo in the fp commit, cert\_fp unused
* [Revision #830d1373](https://github.com/mariadb-corporation/mariadb-connector-c/commit/830d1373)\
  2024-02-03 16:42:01 +0100
  * don't use the output printf buffer as a %s parameter
* [Revision #9aa15e72](https://github.com/mariadb-corporation/mariadb-connector-c/commit/9aa15e72)\
  2023-08-31 08:21:13 +0200
  * TLS fingerprint
* [Revision #4da7d9d4](https://github.com/mariadb-corporation/mariadb-connector-c/commit/4da7d9d4)\
  2024-02-04 11:12:25 +0100
  * Merge branch '3.3' of [mariadb-connector-c](https://github.com/mariadb-corporation/mariadb-connector-c) into 3.3
* [Revision #39564154](https://github.com/mariadb-corporation/mariadb-connector-c/commit/39564154)\
  2024-01-24 11:55:21 +0100
  * Do not use own warning-as-error logic, if standard CMake flag is in us.
* [Revision #83951fee](https://github.com/mariadb-corporation/mariadb-connector-c/commit/83951fee)\
  2024-01-24 11:09:47 +0100
  * [CONC-686](https://jira.mariadb.org/browse/CONC-686) Error 2026 TLS error messages truncated
* [Revision #6466cabd](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6466cabd)\
  2024-02-04 11:11:49 +0100
  * Bump version to 3.3.10

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
