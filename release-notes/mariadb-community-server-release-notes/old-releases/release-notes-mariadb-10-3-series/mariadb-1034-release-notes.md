# MariaDB 10.3.4 Release Notes

The most recent release of [MariaDB 10.3](what-is-mariadb-103.md) is:[**MariaDB 10.3.39**](mariadb-10-3-39-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.3.39/)

[Download](https://downloads.mariadb.org/mariadb/10.3.4)[Release Notes](mariadb-1034-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-10-3-series/mariadb-1034-changelog.md)[Overview of 10.3](what-is-mariadb-103.md)

**Release date:** 18 Jan 2018

[MariaDB 10.3](what-is-mariadb-103.md) is the current development series of MariaDB. It is an evolution\
of [MariaDB 10.2](../release-notes-mariadb-10-2-series/what-is-mariadb-102.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL.

[MariaDB 10.3.4](mariadb-1034-release-notes.md) is a [_**Beta**_](../../../mariadb-release-criteria.md) release.

**Do not use&#x20;**_**Beta**_**&#x20;releases on production systems!**

**For an overview of** [**MariaDB 10.3**](what-is-mariadb-103.md) **see the** [**What is MariaDB 10.3?**](what-is-mariadb-103.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

This is the second beta release in the [MariaDB 10.3](what-is-mariadb-103.md) series.

Notable changes of this release include:

* [System-versioned tables](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-structure/temporal-tables/system-versioned-tables) ([MDEV-12894](https://jira.mariadb.org/browse/MDEV-12894))
* The [MyRocks](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/myrocks) storage engine is now Beta.
* [MDEV-14837](https://jira.mariadb.org/browse/MDEV-14837) - Duplicate primary keys are allowed after ADD COLUMN / UPDATE
* [MDEV-14848](https://jira.mariadb.org/browse/MDEV-14848) - [MariaDB 10.3](what-is-mariadb-103.md) refuses InnoDB crash-upgrade from [MariaDB 10.2](../release-notes-mariadb-10-2-series/what-is-mariadb-102.md)
* [MDEV-14717](https://jira.mariadb.org/browse/MDEV-14717) - RENAME TABLE in InnoDB is not crash-safe
* [MDEV-14952](https://jira.mariadb.org/browse/MDEV-14952) - Avoid repeated calls to btr\_get\_search\_latch()
* [MDEV-14638](https://jira.mariadb.org/browse/MDEV-14638) - Replace trx\_sys\_t::rw\_trx\_set with LF\_HASH
* Added the `tail-lines` option to [mysql-test-run](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/testing-tools/mariadb-test/mariadb-test-run-pl-options)
* As per the [MariaDB Deprecation Policy](../../../mariadb-platform-deprecation-policy.md), this will be the last release of [MariaDB 10.3](what-is-mariadb-103.md) for Ubuntu 17.04 "zesty"

**Do not use&#x20;**_**Beta**_**&#x20;releases on production systems!**

For a complete list of changes made in [MariaDB 10.3.4](mariadb-1034-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-10-3-series/mariadb-1034-changelog.md).

{% include "https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/~/reusable/vX1KAy0t1XuYJaGsK28T/" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
