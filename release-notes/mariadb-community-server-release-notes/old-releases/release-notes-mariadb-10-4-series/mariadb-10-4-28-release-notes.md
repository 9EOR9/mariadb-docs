# MariaDB 10.4.28 Release Notes

[Download](https://downloads.mariadb.org/mariadb/10.4.28/)[Release Notes](mariadb-10-4-28-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-10-4-series/mariadb-10-4-28-changelog.md)[Overview of 10.4](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/what-is-mariadb-104)

**Release date:** 6 Feb 2023

[MariaDB 10.4](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/what-is-mariadb-104) is a previous _stable_ series of MariaDB, maintained until June 2024. It is an evolution\
of [MariaDB 10.3](../release-notes-mariadb-10-3-series/what-is-mariadb-103.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL.

[MariaDB 10.4.28](mariadb-10-4-28-release-notes.md) is a [_**Stable (GA)**_](../../../mariadb-release-criteria.md) release.

**For an overview of** [**MariaDB 10.4**](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/what-is-mariadb-104) **see the**[**What is MariaDB 10.4?**](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/what-is-mariadb-104) **page.**

Thanks, and enjoy MariaDB!

## Notable Items

* As mentioned in the [10.4.27 release notes](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/mariadb-10-4-27-release-notes), our Yum/DNF/Zypper repositories for Red Hat Enterprise Linux, CentOS, openSUSE, and SUSE are changing with this release to being signed with a new GPG key with SHA2 digest algorithms instead of SHA1. See [this blog post](https://mariadb.org/new-gpg-release-key-rpms/) and the [GPG](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/install-and-upgrade-mariadb/installing-mariadb/binary-packages/gpg) page for more details.

### InnoDB

* [Full-text index](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/optimization-and-indexes/full-text-indexes) corruption with [system versioning](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-structure/temporal-tables/system-versioned-tables) ([MDEV-25004](https://jira.mariadb.org/browse/MDEV-25004))

### Galera

* [Galera](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/galera-cluster/README.md) updated to 26.4.14
* Fixes for cluster wide write conflict resolving ([MDEV-29684](https://jira.mariadb.org/browse/MDEV-29684))

### Replication

* Parallel slave applying in binlog order is corrected for admin class of commands including ANALYZE ([MDEV-30323](https://jira.mariadb.org/browse/MDEV-30323))
* [Seconds\_Behind\_Master](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/show/show-replica-status) is now shown now more precisely at the slave applier start, including in the delayed mode ([MDEV-29639](https://jira.mariadb.org/browse/MDEV-29639))
* `mysqlbinlog --verbose` is made to show the type of compressed columns ([MDEV-25277](https://jira.mariadb.org/browse/MDEV-25277))

### JSON

* [JSON\_PRETTY](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/special-functions/json-functions/json_pretty) added as an alias for [JSON\_DETAILED](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/special-functions/json-functions/json_detailed) ([MDEV-19160](https://jira.mariadb.org/browse/MDEV-19160))

### General

* Infinite sequence of recursive calls when processing embedded CTE ([MDEV-30248](https://jira.mariadb.org/browse/MDEV-30248))
* Crash with a query containing nested WINDOW clauses ([MDEV-30052](https://jira.mariadb.org/browse/MDEV-30052))
* Major performance regression with 10.6.11 ([MDEV-29988](https://jira.mariadb.org/browse/MDEV-29988))

### Security

* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * CVE-\`-\`\`\`

## Changelog

For a complete list of changes made in [MariaDB 10.4.28](mariadb-10-4-28-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-10-4-series/mariadb-10-4-28-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.4.28](mariadb-10-4-28-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-10-3-10-9-5-10-8-7-10-7-8-10-6-12-10-5-19-10-4-28-and-10-3-38-now-available/).

{% include "https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/~/reusable/vX1KAy0t1XuYJaGsK28T/" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
