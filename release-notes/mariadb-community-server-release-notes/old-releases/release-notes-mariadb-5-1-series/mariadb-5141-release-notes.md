# MariaDB 5.1.41 Release Notes

The most recent release in the [MariaDB 5.1 series](changes-improvements-in-mariadb-5-1.md) is:[**MariaDB 5.1.67**](mariadb-5167-release-notes.md)

[Download](https://askmonty.org/wiki/MariaDB:Download:MariaDB_5.1.41) | **Release Notes** | [Changelog](../../changelogs/changelogs-mariadb-51-series/mariadb-5141-changelog.md) |[Overview of 5.1](changes-improvements-in-mariadb-5-1.md)

**Release date:** 13 Jan 2010

See the [MariaDB versus MySQL](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-1-series/broken-reference/README.md) page for a high-level\
overview of the differences between MariaDB and MySQL.

See the [MariaDB 5.1.41 Changelog](../../changelogs/changelogs-mariadb-51-series/mariadb-5141-changelog.md) for a more detail\
list of the changes in this release.

This release is a 'release candidate'. This means that we think it's almost\
ready for a final release but we don't want to call it a final release until\
more people have had a chance to test it. This release should be followed by a\
final release in a few weeks.

[MariaDB](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/mariadb/README.md) 5.1.41 RC is based on [MySQL](https://mysql.com) 5.1.41 and[XtraDB](https://www.percona.com/docs/wiki/percona-xtradb:start) 1.0.4-8.

MariaDB is kept up to date with the latest MySQL release from the same branch.

In most respects MariaDB will work exactly as MySQL; all commands, interfaces,\
libraries and APIs that exist in MySQL also exist in MariaDB.

In addition to the differences noted in the MariaDB[5.1.38](mariadb-5138-release-notes.md) and [5.1.39](mariadb-5139-release-notes.md)\
release notes, the main differences between MariaDB and MySQL are:

## Includes MySQL 5.1.41

For [MariaDB 5.1.41](mariadb-5141-release-notes.md) we have merged in all of the upstream changes from MySQL\
5.1.41. The[MySQL 5.1.41 release notes](https://dev.mysql.com/doc/refman/5.1/en/news-5-1-41.html)\
have details of what changes were made upstream by MySQL since 5.1.39

## Includes [XtraDB](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb) 1.0.4-8

We have included XtraDB 1.0.4-8 in this version of MariaDB. The[XtraDB 1.0.4-8 release notes](https://www.percona.com/docs/wiki/percona-xtradb:info:xtradb_changelog#release_1.0.4-8)\
have details of the changes made to XtraDB since version 1.0.3-6 (the version\
included with [MariaDB 5.1.38](mariadb-5138-release-notes.md) Beta).

## Includes [PBXT](https://github.com/mariadb-corporation/docs-release-notes/blob/test/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-1-series/pbxt-storage-engine/README.md) 1.0.09f RC3

We have included PBXT 1.0.09f RC3 in this version of MariaDB.

This is the 3rd RC release of PBXT. It includes a number of bug fixes (some specifically for MariaDB), and 2 features:

* XA/2-Phase commit support
* Online backup native driver for PBXT

The backup uses the MySQL backup API (MySQL 6.0/5.4), and is not yet available in MariaDB.

Release notes since the RC2 version in [MariaDB 5.1.39](mariadb-5139-release-notes.md) Beta are as follows:

```
------- 1.0.09f RC3 - 2009-11-30

RN291: Fixed bug #489088: On shutdown MySQL reports: [Warning] Plugin 'PBXT' will be forced to shutdown.

RN290: Fixed bug #345524: pbxt does not compile on 64 bit windows. Currently atomic operations are not supported on this platform.

RN286: Fixed a bug introduced in RN281, which could cause an index scan to hang. The original change was to prevent a warning in Valgrind.

RN285: Merged changes required to compile with Drizzle.

RN284: Fixed bug that cause the error "[ERROR] Invalid (old?) table or database name 'mysqld.1'", when running temp_table.test under MariaDB (thanks to Monty for his initial bug fix). Added a fix for partition table names as well.

RN283: Added win_inttypes.h to the distribution. This file is only required for the Windows build.

RN282: Fixed bug #451101: jump or move depends on uninitialised value in myxt_get_key_length

RN281: Fixed bug #451080: Uninitialised memory write in XTDatabaseLog::xlog_append

RN280: Fixed bug #451085: jump or move depends on uninitialised value in my_type_to_string

RN279: Fixed bug #441000: xtstat crashes with segmentation fault on startup if max_pbxt_threads exceeded.

------- 1.0.09e RC3 - 2009-11-20

RN278: Fixed compile error with MySQL 5.1.41.

------- 1.0.09d RC3 - 2009-09-30

RN277: Added r/o flag to pbxt_max_threads server variable (this fix is related to bug #430637)

RN276: Added test case for replication on tables w/o PKs (see bug #430716)

RN275: Fixed bug #430600: 'Failed to read auto-increment value from storage engine' error.

RN274: Fixed bug #431240: This report is public edit xtstat fails if no PBXT table has been created. xtstat now accepts --database=information_schema or --database=pbxt. Depending on this setting PBXT will either use the information_schema.pbxt_statistics or the pbxt.statistics table. If information_schema is used, then the statistics are displayed even when no PBXT table exists. Recovery activity is also displayed, unless pbxt_support_xa=1, in which case MySQL will wait for PBXT recovery to complete before allowing connections. 

RN273: Fixed bug #430633: XA_RBDEADLOCK is not returned on XA END after the transacting ended with a deadlock.

RN272: Fixed bug #430596: Backup/restore does not work well even on a basic PBXT table with auto-increment.

------- 1.0.09c RC3 - 2009-09-16

RN271: Windows build update: now you can simply put the pbxt directory under <mysql-root>/storage and build the PBXT engine as a part of the source tree. The engine will be linked statically. Be sure to specify the WITH_PBXT_STORAGE_ENGINE option when running win\configure.js

RN270: Correctly disabled PBMS so that this version now compiles under Windows. If PBMS_ENABLED is defined, PBXT will not compile under Windows becaause of a getpid() call in pbms.h.

------- 1.0.09 RC3 - 2009-09-09

RN269: Implemented online backup. A native online backup driver now performs BACKUP and RESTORE DATABASE operations for PBXT. NOTE: This feature is only supported by MySQL 6.0.9 or later.

RN268: Implemented XA support. PBXT now supports all XA related MySQL statements. The variable pbxt_support_xa determines if XA support is enabled. Note: due to MySQL bug #47134, enabling XA support could lead to a crash.
```

## Includes [FederatedX](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/federatedx-storage-engine)

The FederatedX storage engine replaces the old, not maintained, Federated storage engine.

See also: [FederatedX storage engine](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/federatedx-storage-engine)

## Fewer warnings and bugs

Like we did with the 5.1.39 Beta, various changes were made in [MariaDB 5.1.41](mariadb-5141-release-notes.md) RC in our desire to fix warnings and eliminate bugs. These included removing or fixing invalid tests, cleaning up the codebase where appropriate, and so on.

## About Our Builds

We are working on setting up a [BuildBot](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/development-articles/general-info/tools/buildbot) network which will enable\
us to test and build binaries on many different platforms. We aim to produce\
binaries in .tar and package formats for all popular platforms. Right now there\
are generic Linux binaries, packages for Debian and Ubuntu, RHEL/CentOS, and a\
Windows executable.

The tarball binaries provided in this release are generic binaries, intended\
for use on most x86-based Linux systems to quickly try out MariaDB without\
having to compile the source code. For 5.1.38 they were built on Ubuntu 9.04\
systems (linked against libc 2.9), for 5.1.39 and 5.1.41 they were built on\
Ubuntu 8.04 systems (so older libc works). They should hopefully work on most\
x86-based Linux systems.

{% include "https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/~/reusable/vX1KAy0t1XuYJaGsK28T/" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
