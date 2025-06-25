# Changes and Improvements in MariaDB 11.6

[MariaDB 11.6](what-is-mariadb-116.md) is an old rolling release and is no longer maintained. Please use a [more recent release](../../../latest-releases.md).

The most recent release of [MariaDB 11.6](what-is-mariadb-116.md) is:[**MariaDB 11.6.2**](mariadb-11-6-2-release-notes.md) [Download Now](https://downloads.mariadb.org/mariadb/11.6.2/)[_Alternate download from mariadb.org_](https://downloads.mariadb.org/mariadb/11.6.2)

[MariaDB 11.6](what-is-mariadb-116.md) is a [rolling release](../../../mariadb-release-model.md).

## Upgrading

* See [Upgrading Between Major MariaDB Versions](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/install-and-upgrade-mariadb/upgrading/upgrading-between-major-mariadb-versions) and [Upgrading from MariaDB 10.11 to MariaDB 11.0](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/install-and-upgrade-mariadb/upgrading/upgrading-to-unmaintained-mariadb-releases/upgrading-from-mariadb-10-11-to-mariadb-11-0).

## Notable Items

### Vectors

* [Vectors](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-structure/vectors) are a feature that allow MariaDB Server to perform as a relational vector database. In [MariaDB 10.6](../../mariadb-10-6-series/what-is-mariadb-106.md), only available in the [Vector preview release](mariadb-11-6-0-vector-release-notes.md).
* Vector Search was added to [MariaDB 11.7](../mariadb-11-7-rolling-releases/what-is-mariadb-117.md).

### Character Sets

* The default [character set](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/data-types/string-data-types/character-sets) has been changed from `latin1` to `utf8mb4` ([MDEV-19123](https://jira.mariadb.org/browse/MDEV-19123))

### Backup and Restore

* Added the `--dir` option to [mariadb-import](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/backup-restore-and-import-clients/mariadb-import), allowing one to restore all tables from a backup directory created using [mariadb-dump --dir](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/backup-restore-and-import-clients/mariadb-dump) ([MDEV-33627](https://jira.mariadb.org/browse/MDEV-33627))
  * Added the related `--database`, `--ignore-database`, `--table` and `--ignore-table` options.
  * Refactor [mariadb-import](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/backup-restore-and-import-clients/mariadb-import) threading
* Automatic SST user account management ([MDEV-31809](https://jira.mariadb.org/browse/MDEV-31809))

### Syntax

* Single-table [DELETEs](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-manipulation/changing-deleting-data/delete) now support table aliases ([MDEV-33988](https://jira.mariadb.org/browse/MDEV-33988))

### Authentication

* [New authentication plugin](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/plugins/authentication-plugins/authentication-plugin-parsec) ([MDEV-32618](https://jira.mariadb.org/browse/MDEV-32618))
* Extend [Unix socket authentication](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/plugins/authentication-plugins/authentication-plugin-unix-socket) to support authentication\_string ([MDEV-33479](https://jira.mariadb.org/browse/MDEV-33479))

### Replication

* New definition for Seconds\_Behind\_Master ([MDEV-33856](https://jira.mariadb.org/browse/MDEV-33856))
  * Added three variables to [SHOW ALL REPLICAS STATUS](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/show/show-replica-status)
  * New [Information Schema SLAVE\_STATUS Table](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/system-tables/information-schema/information-schema-tables/information-schema-slave_status-table)

### General

* Set thread names for MariaDB Server threads ([MDEV-32537](https://jira.mariadb.org/browse/MDEV-32537))

### Variables

* For a list of all new variables, see [System Variables Added in MariaDB 11.6](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/system-and-status-variables-added-by-major-release/system-variables-added-in-mariadb-11-6) and [Status Variables Added in MariaDB 11.6](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/system-and-status-variables-added-by-major-release/system-and-status-variables-added-by-major-unmaintained-release/status-variables-added-in-mariadb-11-5).

## Security Vulnerabilities Fixed in [MariaDB 11.6](what-is-mariadb-116.md)

For a complete list of security vulnerabilities (CVEs) fixed across all\
versions of MariaDB, see the [Security Vulnerabilities Fixed in MariaDB](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security)\
page.\
Add listcve macro here - removed for performance reasons

## List of All [MariaDB 11.6](what-is-mariadb-116.md) Releases

| Date        | Release                                                  | Status      | Release Notes                                           | Changelog                                                                                |
| ----------- | -------------------------------------------------------- | ----------- | ------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| Date        | Release                                                  | Status      | Release Notes                                           | Changelog                                                                                |
| 21 Nov 2024 | [MariaDB 11.6.2](mariadb-11-6-2-release-notes.md)        | Stable (GA) | [Release Notes](mariadb-11-6-2-release-notes.md)        | [Changelog](../../changelogs/changelogs-mariadb-11-6-series/mariadb-11-6-2-changelog.md) |
| 14 Aug 2024 | [MariaDB 11.6.1](mariadb-11-6-1-release-notes.md)        | RC          | [Release Notes](mariadb-11-6-1-release-notes.md)        | [Changelog](../../changelogs/changelogs-mariadb-11-6-series/mariadb-11-6-1-changelog.md) |
| 29 Jul 2024 | [MariaDB 11.6.0](mariadb-11-6-0-release-notes.md) Vector | Alpha       | [Release Notes](mariadb-11-6-0-vector-release-notes.md) |                                                                                          |
| 26 Jun 2024 | [MariaDB 11.6.0](mariadb-11-6-0-release-notes.md)        | Alpha       | [Release Notes](mariadb-11-6-0-release-notes.md)        |                                                                                          |

{% @marketo/form formid="4316" formId="4316" %}
