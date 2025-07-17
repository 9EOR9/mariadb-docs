# MariaDB 10.0.2 Release Notes

The most recent release in the [MariaDB 10.0](changes-improvements-in-mariadb-10-0.md) series is:[**MariaDB 10.0.38**](mariadb-10038-release-notes.md) [Download Now](https://downloads.mariadb.org/mariadb/10.0.38)

[Download](https://downloads.mariadb.org/mariadb/10.0.2) |**Release Notes** |[Changelog](../../changelogs/changelogs-mariadb-100-series/mariadb-1002-changelog.md) |[Overview of 10.0](changes-improvements-in-mariadb-10-0.md)

**Release date:** 24 Apr 2013

[MariaDB 10.0](changes-improvements-in-mariadb-10-0.md) is the current development version of MariaDB. It is built on thethe [MariaDB 5.5 serie](../release-notes-mariadb-5-5-series/changes-improvements-in-mariadb-5-5.md) with backported features from MySQL\
5.6 and entirely new features not found anywhere else.

[MariaDB 10.0.2](mariadb-1002-release-notes.md) is an [_**Alpha**_](../../about/release-criteria.md) release.\
This is the third 10.0-based release, and we are releasing it now to get it\
into the hands of any who might want to test it. Not all features planned for\
the [MariaDB 10.0](changes-improvements-in-mariadb-10-0.md) series are included in this release. Additional features will\
be pushed in future releases.**Do not use alpha releases on production systems.**

**For an overview of** [**MariaDB 10.0**](changes-improvements-in-mariadb-10-0.md) **see the**[**What is MariaDB 10.0?**](changes-improvements-in-mariadb-10-0.md) **page.**

For a list of changes made in [MariaDB 10.0.2](mariadb-1002-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-100-series/mariadb-1002-changelog.md).

## Based on [MariaDB 5.5](../release-notes-mariadb-5-5-series/changes-improvements-in-mariadb-5-5.md)

The [MariaDB 10.0](changes-improvements-in-mariadb-10-0.md) series builds off of the [MariaDB 5.5](../release-notes-mariadb-5-5-series/changes-improvements-in-mariadb-5-5.md) series. It also includes\
features imported from MySQL 5.6, and completely new features.

In most respects [MariaDB](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/mariadb/README.md) will work exactly as MySQL: all commands,\
interfaces, libraries and APIs that exist in MySQL also exist in MariaDB.

## Security fixes

This release includes fixes for the following security vulnerabilities:

* [CVE-2013-1521](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2013-1521)
* [CVE-2013-2378](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2013-2378)
* [CVE-2013-1552](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2013-1552)
* [CVE-2013-1523](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2013-1523)
* [CVE-2013-1512](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2013-1512)
* [CVE-2013-1555](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2013-1555)
* [CVE-2013-1526](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2013-1526)
* [CVE-2012-5614](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-5614)
* [CVE-2013-1506](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2013-1506)

## New Features in [MariaDB 10.0.2](mariadb-1002-release-notes.md) Alpha

### New Features

* [MDEV-4146](https://jira.mariadb.org/browse/MDEV-4146) - [CONNECT](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/connect) storage engine
* [MDEV-26](https://jira.mariadb.org/browse/MDEV-26) - [Global Transaction ID](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/gtid)
* [MDEV-318](https://jira.mariadb.org/browse/MDEV-318) - IF (NOT) EXIST clauses for [ALTER TABLE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-definition/alter/alter-table).
* [MDEV-4022](https://jira.mariadb.org/browse/MDEV-4022) - [table attributes](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/storage-engines-storage-engine-development/engine-defined-new-tablefieldindex-attributes) with sysvar as a default value.
* [MDEV-3808](https://jira.mariadb.org/browse/MDEV-3808) - Better [table discovery](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/storage-engines-storage-engine-development/table-discovery). [Sequence](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/sequence-storage-engine) storage engine. Assisted discovery in [FederatedX](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/federatedx-storage-engine).
* [MDEV-3807](https://jira.mariadb.org/browse/MDEV-3807) - [show plugins soname 'xxx'](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/show/show-plugins-soname).
* [MDEV-3917](https://jira.mariadb.org/browse/MDEV-3917) - multiple use locks ([GET\_LOCK](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/secondary-functions/miscellaneous-functions/get_lock)) in one connection.
* Subquery optimizations ([MDEV-38](https://jira.mariadb.org/browse/MDEV-38) - [NOT EXISTS to IN](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/query-optimizations/subquery-optimizations/exists-to-in-optimization)), [MDEV-537](https://jira.mariadb.org/browse/MDEV-537), [MDEV-3862](https://jira.mariadb.org/browse/MDEV-3862).
* [MDEV-4145](https://jira.mariadb.org/browse/MDEV-4145) - optimizer can collect and use [histogram-based statistics](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/query-optimizations/statistics-for-optimizing-queries/histogram-based-statistics) for non-indexed columns.
* [MDEV-4338](https://jira.mariadb.org/browse/MDEV-4338) - Support for [atomic writes on FusionIO DirectFS](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/install-and-upgrade-mariadb/configuring-mariadb/mariadb-performance-advanced-configurations/atomic-write-support).

### Bug Fixes

As with all MariaDB releases, numerous bugs were fixed in this release. For\
details, see the [changelog](../../changelogs/changelogs-mariadb-100-series/mariadb-1002-changelog.md). One particular bug fix we'd like to highlight is:

* [MDEV-4172](https://jira.mariadb.org/browse/MDEV-4172) - Optimizer now can take into account the selectivity of predicates

### Other Features

Other features are planned for inclusion in the Stable (GA) version of [MariaDB\
10.0](changes-improvements-in-mariadb-10-0.md). They are listed on the [What is MariaDB 10.0?](changes-improvements-in-mariadb-10-0.md) and Plans for 10x pages.

## Discontinued builds

The MariaDB project tries to support as many different Operating Systems and\
Linux Distributions as we can. However, when a distribution or OS stops\
receiving security and other updates it becomes difficult to freely provide\
packages for that platform. In such cases, our policy is to deprecate that\
platform and stop providing binary packages for it.

Accordingly, this will be the final release of [MariaDB 10.0](changes-improvements-in-mariadb-10-0.md) for the following\
distributions:

* Ubuntu 8.04 LTS "Hardy"
* Ubuntu 11.10 "Oneiric"

Binary tar.gz files built on Ubuntu "Hardy" will also be going away. These are the ones that _do not_ require GLIBC\_2.14+. So for the next release, all binary tar.gz files for Linux will require GLIBC\_2.14+.

If your chosen Linux Distribution or Operating System is deprecated, packages\
or support are not completely unavailable. Companies such as [SkySQL](https://skysql.com), [Monty Program](https://montyprogram.com), and others provide support for all versions of\
MariaDB back to even very old MySQL versions. This includes packaged binaries.\
Contact them for more details.

More information on the deprecation policy can be found on the [Deprecation Policy](../../about/platform-deprecation-policy.md) page.

Thanks, and enjoy MariaDB!

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
