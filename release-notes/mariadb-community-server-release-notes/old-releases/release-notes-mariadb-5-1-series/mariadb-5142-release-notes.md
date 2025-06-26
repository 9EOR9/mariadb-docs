# MariaDB 5.1.42 Release Notes

The most recent release in the [MariaDB 5.1 series](changes-improvements-in-mariadb-5-1.md) is:[**MariaDB 5.1.67**](mariadb-5167-release-notes.md)

[Download](https://askmonty.org/wiki/MariaDB:Download:MariaDB_5.1.42) | **Release Notes** | [Changelog](../../changelogs/changelogs-mariadb-51-series/mariadb-5142-changelog.md) |[Overview of 5.1](changes-improvements-in-mariadb-5-1.md)

**Release date:** 01 Feb 2010

See the [MariaDB versus MySQL](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-1-series/broken-reference/README.md) page for a high-level\
overview of the differences between MariaDB and MySQL.

See the [MariaDB 5.1.42 Changelog](../../changelogs/changelogs-mariadb-51-series/mariadb-5142-changelog.md) for a more detailed\
list of the changes in this release.

MariaDB is kept up to date with the latest MySQL release from the same branch.[MariaDB](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/mariadb/README.md) 5.1.42 is based on [MySQL](https://mysql.com) 5.1.42 and[XtraDB](https://www.percona.com/docs/wiki/percona-xtradb:start) 1.0.6-9.

In most respects MariaDB will work exactly as MySQL: all commands, interfaces,\
libraries and APIs that exist in MySQL also exist in MariaDB.

In addition to the differences noted in previous[release notes](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/release-notes/README.md) and[changelogs](../../../connectors/odbc/changelogs/), the main differences between\
MariaDB and MySQL are:

## Includes MySQL 5.1.42

For [MariaDB 5.1.42](mariadb-5142-release-notes.md) we have merged in all of the upstream changes from\
MySQL 5.1.42. The[MySQL 5.1.42 release notes](https://dev.mysql.com/doc/refman/5.1/en/news-5-1-42.html)\
have details of what changes were made upstream by MySQL since 5.1.41.

## Includes [XtraDB](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb) 1.0.6-9

We have included XtraDB 1.0.6-9 in this version of MariaDB. The[XtraDB 1.0.6-9 release notes](https://www.percona.com/docs/wiki/percona-xtradb:info:xtradb_changelog#release_1.0.6-9)\
have details of the changes made to XtraDB since version 1.0.4-8 (the version\
included with [MariaDB 5.1.41](mariadb-5141-release-notes.md) RC).

## Windows fixes

Thanks to the work of Alex Budovski we have fixed several Microsoft Windows\
test failures, compiler warnings, and compile errors. We also added page fault\
counters for SHOW PROFILE on Windows.

## Solaris fixes

We have fixed several Solaris compile issues and warnings and we are now able\
to offer Solaris binaries for download.

## Fewer warnings and bugs

Like we did with our previous releases, various additional changes were made in[MariaDB 5.1.42](mariadb-5142-release-notes.md) in our desire to fix warnings and eliminate bugs.

In [MariaDB 5.1.42](mariadb-5142-release-notes.md) these included fixing a bug where one connection didn't see\
newly committed data from another connection and a crashing bug with\
mysqlslap.exe.

These included removing or fixing invalid tests, cleaning up the codebase where\
appropriate, and so on.

## About Our Builds

We are working on setting up a [BuildBot](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/development-articles/general-info/tools/buildbot) network which will enable\
us to test and build binaries on many different platforms. We aim to produce\
binaries in .tar and package formats for all popular platforms. Right now there\
are generic Linux binaries, packages for Debian and Ubuntu, RHEL/CentOS, and a\
Windows executable.

The tarball binaries provided in this release are generic binaries, intended\
for use on most x86-based Linux systems to quickly try out MariaDB without\
having to compile the source code. For 5.1.38 they were built on Ubuntu 9.04\
systems (linked against libc 2.9), for 5.1.39 and later they were built on\
Ubuntu 8.04 systems (so older libc works). They should hopefully work on most\
x86-based Linux systems.

{% include "https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/~/reusable/vX1KAy0t1XuYJaGsK28T/" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
