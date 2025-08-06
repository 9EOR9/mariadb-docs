# MariaDB 10.0.1 Release Notes

The most recent release in the [MariaDB 10.0](changes-improvements-in-mariadb-10-0.md) series is:[**MariaDB 10.0.38**](mariadb-10038-release-notes.md) [Download Now](https://downloads.mariadb.org/mariadb/10.0.38)

[Download](https://downloads.mariadb.org/mariadb/10.0.1) |**Release Notes** |[Changelog](../../changelogs/) |[Overview of 10.0](changes-improvements-in-mariadb-10-0.md)

**Release date:** 06 Feb 2013

[MariaDB 10.0](changes-improvements-in-mariadb-10-0.md) is the current development version of MariaDB. It is built on thethe [MariaDB 5.5 series](../release-notes-mariadb-5-5-series/changes-improvements-in-mariadb-5-5.md) with backported features from MySQL\
5.6 and entirely new features not found anywhere else.

[MariaDB 10.0.1](mariadb-1001-release-notes.md) is an [_**Alpha**_](../../about/release-criteria.md) release.\
This is the second 10.0-based release, and we are releasing it now to get it\
into the hands of any who might want to test it. Not all features planned for\
the [MariaDB 10.0](changes-improvements-in-mariadb-10-0.md) series are included in this release. Additional features will\
be pushed in future releases.**Do not use alpha releases on production systems.**

**For an overview of** [**MariaDB 10.0**](changes-improvements-in-mariadb-10-0.md) **see the**[**What is MariaDB 10.0?**](changes-improvements-in-mariadb-10-0.md) **page.**

For a list of changes made in [MariaDB 10.0.1](mariadb-1001-release-notes.md), with links to detailed\
information on each push, see the [Changelog](../../changelogs/) .

## Based on [MariaDB 5.5](../release-notes-mariadb-5-5-series/changes-improvements-in-mariadb-5-5.md),

The [MariaDB 10.0](changes-improvements-in-mariadb-10-0.md) series builds off of the [MariaDB 5.5](../release-notes-mariadb-5-5-series/changes-improvements-in-mariadb-5-5.md), series. It also includes features imported from MySQL 5.6, and completely new features.

In most respects [MariaDB](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/mariadb/README.md) will work exactly as MySQL: all commands,\
interfaces, libraries and APIs that exist in MySQL also exist in MariaDB.

## New Features in [MariaDB 10.0.1](mariadb-1001-release-notes.md) Alpha

### New Features

* [MDEV-4011](https://jira.mariadb.org/browse/MDEV-4011) - Per thread memory usage. — Original code from [Taobao, developed by Peng Lixun](https://mysql.taobao.org/index.php/Patch_source_code#per-thread_memory_usage_statistics).
  * [information\_schema.processlist](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/system-tables/information-schema/information-schema-tables/information-schema-processlist-table) has two new columns: `MEMORY_USAGE` and `EXAMINED_ROWS`.
  * [SHOW STATUS](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/show/show-status) has a new variable: [Memory\_used](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/variables-and-modes/server-status-variables#memory_used).
* [Cassandra storage engine](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/legacy-storage-engines/cassandra/cassandra-storage-engine-overview)
* Named [dynamic columns](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-structure/nosql/dynamic-columns) ([MDEV-377](https://jira.mariadb.org/browse/MDEV-377))
* Faster UNIQUE key generation with ALTER TABLE ([MDEV-539](https://jira.mariadb.org/browse/MDEV-539))
* Implement async commit checkpoint in InnoDB and XtraDB ([MDEV-532](https://jira.mariadb.org/browse/MDEV-532))
* [Engine independent statistics](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/query-optimizations/statistics-for-optimizing-queries/engine-independent-table-statistics) ([MDEV-3806](https://jira.mariadb.org/browse/MDEV-3806))

### New Features Re-implemented from a similar MySQL feature

* [CURRENT\_TIMESTAMP](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/date-time-functions/current_timestamp) as DEFAULT for [DATETIME](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/data-types/date-and-time-data-types/datetime) columns ([MDEV-452](https://jira.mariadb.org/browse/MDEV-452))

### New Features Backported from MySQL 5.6

* backport [--plugin-load-add](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/starting-and-stopping-mariadb/mariadbd-options) ([MDEV-3860](https://jira.mariadb.org/browse/MDEV-3860))

### Other Features

Other features are planned for inclusion in the Stable (GA) version of [MariaDB\
10.0](changes-improvements-in-mariadb-10-0.md). They are listed on the [What is MariaDB 10.0?](changes-improvements-in-mariadb-10-0.md) and Plans for 10x pages.

## Important Security Fixes

This release includes fixes for the following security vulnerabilities:

* A buffer overflow that can cause a server crash or arbitrary code execution (a variant of [CVE-2012-5611](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-5611))
* [CVE-2012-5627](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-5627)/[MDEV-3915](https://jira.mariadb.org/browse/MDEV-3915) fast password brute-forcing using the "change user" command
* [CVE-2012-5615](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-5615)/[MDEV-3909](https://jira.mariadb.org/browse/MDEV-3909) information leakage about existing user accounts via the protocol handshake
* fixes for DoS attacks - crashes and server lockups (see the [Changelog](../../changelogs/changelogs-mariadb-55-series/mariadb-5529-changelog.md))

Additionally, it includes all security fixes from MySQL 5.5.29, such as fix for [CVE-2012-5612](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-5612)/[MDEV-3908](https://jira.mariadb.org/browse/MDEV-3908) and others, such as:

* [CVE-2013-1531](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2013-1531)
* [CVE-2013-0384](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2013-0384)
* [CVE-2013-0389](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2013-0389)
* [CVE-2013-0386](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2013-0386)
* [CVE-2013-0385](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2013-0385)
* [CVE-2012-1702](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-1702)
* [CVE-2013-0383](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2013-0383)
* [CVE-2013-0368](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2013-0368)
* [CVE-2012-0572](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-0572)
* [CVE-2013-0371](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2013-0371)
* [CVE-2012-0574](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-0574)
* [CVE-2012-1705](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-1705)
* [CVE-2012-0578](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-0578)
* [CVE-2013-0367](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2013-0367)
* [CVE-2012-5096](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-5096)

## Fedora 18 and Ubuntu 12.10 Packages

This version of MariaDB includes packages for Fedora 18 "Spherical Cow" and\
Ubuntu 12.10 "Quantal". Visit the

[Repository Configurator](https://downloads.mariadb.org/mariadb/repositories/)\
to generate the necessary commands to install MariaDB on these distributions.

## Discontinued builds

The MariaDB project tries to support as many different Operating Systems and\
Linux Distributions as we can. However, when a distribution or OS stops\
receiving security and other updates it becomes difficult to freely provide\
packages for that platform. In such cases, our policy is to deprecate that\
platform and stop providing binary packages for it.

As of 1 Feb 2013, we stopped building packages for the following:

* Fedora 16 "Verne"
* Debian 5 "Lenny"
* Ubuntu 10.10 "Maverick"
* Ubuntu 11.04 "Natty"

If your chosen Linux Distribution or Operating System is deprecated, packages\
or support are not completely unavailable. Companies such as [SkySQL](https://skysql.com) and [Monty Program](https://montyprogram.com)\
(and others) provide support for all versions of MariaDB back to even very old\
MySQL versions. This includes packaged binaries. Contact them for more details.

More information on our deprecation policy can be found at:

## Archived Releases

From the beginning of the MariaDB project in 2009 we've kept all of our old\
releases online via our network of mirrors. Doing this is great for those few\
who are interested in old releases, but the disk space required to host all of\
our old releases is over 130 Gigabytes at present and grows by several\
gigabytes with each new release. This is too much for some of our mirrors to\
handle. So, starting with this release our primary mirror will only host the\
most recent three or four releases in each series (5.5, 10.0, and so on).\
Mirrors are, of course, free to keep archiving every release, but the primary\
mirror that they pull from will not.

Old releases do have value, so for those that are interested in old releases,\
we are setting up a simple, no frills, archive server which will host them.\
Once the server is up and running, links to archived releases on [downloads.mariadb.org](https://downloads.mariadb.org) will point at the archive server. During the\
transition period, links to some old releases may disappear for a short time,\
but don't worry, they haven't been deleted, they're just being moved!

Thanks, and enjoy MariaDB!

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
