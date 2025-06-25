# MariaDB 10.6.12 Release Notes

[Download](https://downloads.mariadb.org/mariadb/10.6.12)[Release Notes](mariadb-10-6-12-release-notes.md)[Changelog](../changelogs/changelogs-mariadb-106-series/mariadb-10-6-12-changelog.md)[Overview of 10.6](what-is-mariadb-106.md)

**Release date:** 6 Feb 2023

[MariaDB 10.6](what-is-mariadb-106.md) is the current long-term series of MariaDB, [maintained until](https://mariadb.org/about/#maintenance-policy) July 2026. It is an evolution of [MariaDB 10.5](../mariadb-10-5-series/what-is-mariadb-105.md) with several entirely new features.

[MariaDB 10.6.12](mariadb-10-6-12-release-notes.md) is a [_**Stable (GA)**_](../../mariadb-release-criteria.md) release.

**For an overview of** [**MariaDB 10.6**](what-is-mariadb-106.md) **see the**[**What is MariaDB 10.6?**](what-is-mariadb-106.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Items

* As mentioned in the [10.6.11 release notes](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/mariadb-10-6-series/broken-reference/README.md), our Yum/DNF/Zypper repositories for Red Hat Enterprise Linux, CentOS, Fedora, openSUSE, and SUSE are changing with this release to being signed with a new GPG key with SHA2 digest algorithms instead of SHA1. See [this blog post](https://mariadb.org/new-gpg-release-key-rpms/) and the [GPG](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/install-and-upgrade-mariadb/installing-mariadb/binary-packages/gpg) page for more details.

### InnoDB

* [Full-text index](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/optimization-and-indexes/full-text-indexes) corruption with [system versioning](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-structure/temporal-tables/system-versioned-tables) ([MDEV-25004](https://jira.mariadb.org/browse/MDEV-25004))
* [innodb\_undo\_log\_truncate=ON](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables#innodb_undo_log_truncate) recovery and backup fixes ([MDEV-29999](https://jira.mariadb.org/browse/MDEV-29999), [MDEV-30179](https://jira.mariadb.org/browse/MDEV-30179), [MDEV-30438](https://jira.mariadb.org/browse/MDEV-30438))
* Upgrade after a crash is not supported ([MDEV-24412](https://jira.mariadb.org/browse/MDEV-24412))
* Remove [InnoDB buffer pool](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-buffer-pool) load throttling ([MDEV-25417](https://jira.mariadb.org/browse/MDEV-25417))
* InnoDB shutdown hangs when the change buffer is corrupted ([MDEV-30009](https://jira.mariadb.org/browse/MDEV-30009))
* `innodb_fast_shutdown=0` fails to report change buffer merge progress ([MDEV-29984](https://jira.mariadb.org/browse/MDEV-29984))
* `mariadb-backup --backup --incremental --throttle=...` hangs ([MDEV-29896](https://jira.mariadb.org/browse/MDEV-29896))
* Crash after recovery, with InnoDB: Tried to read ([MDEV-30132](https://jira.mariadb.org/browse/MDEV-30132))
* Trying to write ... bytes at ... outside the bounds ([MDEV-30069](https://jira.mariadb.org/browse/MDEV-30069))
* TRUNCATE breaks FOREIGN KEY locking ([MDEV-29504](https://jira.mariadb.org/browse/MDEV-29504), [MDEV-29849](https://jira.mariadb.org/browse/MDEV-29849))
* `INFORMATION_SCHEMA.INNODB_TABLESPACES_ENCRYPTION.NAME` is NULL for undo tablespaces ([MDEV-30119](https://jira.mariadb.org/browse/MDEV-30119))
* Fixed hangs and error handling in B-tree operations ([MDEV-29603](https://jira.mariadb.org/browse/MDEV-29603), [MDEV-30400](https://jira.mariadb.org/browse/MDEV-30400))

### Galera

* [Galera](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/galera-cluster/README.md) updated to 26.4.14
* Fixes for cluster wide write conflict resolving ([MDEV-29684](https://jira.mariadb.org/browse/MDEV-29684))

### Replication

* Parallel slave applying in binlog order is corrected for admin class of commands including ANALYZE ([MDEV-30323](https://jira.mariadb.org/browse/MDEV-30323))
* [Seconds\_Behind\_Master](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/show/show-replica-status) is now shown now more precisely at the slave applier start, including in the delayed mode ([MDEV-29639](https://jira.mariadb.org/browse/MDEV-29639))
* `mysqlbinlog --verbose` is made to show the type of compressed columns ([MDEV-25277](https://jira.mariadb.org/browse/MDEV-25277))
* Deadlock is resolved on replica involving `BACKUP STAGE BLOCK_COMMIT` and a committing user XA ([MDEV-30423](https://jira.mariadb.org/browse/MDEV-30423))

### JSON

* [JSON\_PRETTY](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/special-functions/json-functions/json_pretty) added as an alias for [JSON\_DETAILED](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/special-functions/json-functions/json_detailed) ([MDEV-19160](https://jira.mariadb.org/browse/MDEV-19160))

### General

* Infinite sequence of recursive calls when processing embedded CTE ([MDEV-30248](https://jira.mariadb.org/browse/MDEV-30248))
* Crash with a query containing nested WINDOW clauses ([MDEV-30052](https://jira.mariadb.org/browse/MDEV-30052))
* Major performance regression with 10.6.11 ([MDEV-29988](https://jira.mariadb.org/browse/MDEV-29988))
* As per the [MariaDB Deprecation Policy](../../mariadb-platform-deprecation-policy.md), this will be the last release of [MariaDB 10.6](what-is-mariadb-106.md) for Fedora 35.
* In this release repositories for Fedora 37 and Ubuntu 22.10 Kinetic have been added.

### Security

* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * CVE-\`-\`\`\`

## Changelog

For a complete list of changes and bugfixes made in [MariaDB 10.6.12](mariadb-10-6-12-release-notes.md), with links to detailed\
information on each push, see the [changelog](../changelogs/changelogs-mariadb-106-series/mariadb-10-6-12-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.6.12](mariadb-10-6-12-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-10-3-10-9-5-10-8-7-10-7-8-10-6-12-10-5-19-10-4-28-and-10-3-38-now-available/).

{% include "https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/~/reusable/vX1KAy0t1XuYJaGsK28T/" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
