# MariaDB 10.1.32 Release Notes

The most recent release of [MariaDB 10.1](changes-improvements-in-mariadb-10-1.md) is:[**MariaDB 10.1.48**](mariadb-10148-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.1.48/)

[Download](https://downloads.mariadb.org/mariadb/10.1.32)[Release Notes](mariadb-10132-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-101-series/mariadb-10132-changelog.md)[Overview of 10.1](changes-improvements-in-mariadb-10-1.md)

**Release date:** 27 Mar 2018

[MariaDB 10.1](changes-improvements-in-mariadb-10-1.md) is the previous stable series of MariaDB. It is an evolution\
of [MariaDB 10.0](../release-notes-mariadb-10-0-series/changes-improvements-in-mariadb-10-0.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL 5.6 and 5.7.

[MariaDB 10.1.32](mariadb-10132-release-notes.md) is a [_**Stable (GA)**_](../../about/release-criteria.md) release.

**For an overview of** [**MariaDB 10.1**](changes-improvements-in-mariadb-10-1.md) **see the**[**What is MariaDB 10.1?**](changes-improvements-in-mariadb-10-1.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

* [MDEV-14533](https://jira.mariadb.org/browse/MDEV-14533) - Added the [DISKS plugin](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/system-tables/information-schema/information-schema-tables/information-schema-disks-table), for monitoring disk space
* [Galera wsrep library](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/what-is-mariadb-galera-cluster/README.md) updated to 25.3.23
* [MDEV-14611](https://jira.mariadb.org/browse/MDEV-14611) - [ALTER TABLE EXCHANGE PARTITION](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-definition/alter/alter-table) does not work properly when used with DATA DIRECTORY.
* [MDEV-15333](https://jira.mariadb.org/browse/MDEV-15333) - MariaDB (still) slow start
* [MDEV-14904](https://jira.mariadb.org/browse/MDEV-14904) - Backport [innodb\_default\_row\_format](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables)
* [MDEV-12255](https://jira.mariadb.org/browse/MDEV-12255) - Wrong result with [innodb\_prefix\_index\_cluster\_optimization](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables)
* [MDEV-12396](https://jira.mariadb.org/browse/MDEV-12396) - [IMPORT TABLESPACE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-definition/alter/alter-table#import-tablespace) cleanup
* [MDEV-14648](https://jira.mariadb.org/browse/MDEV-14648) - Restore fix for MySQL BUG#39053 - [UNINSTALL PLUGIN](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/plugin-sql-statements/uninstall-plugin) does not allow the storage engine to cleanup open connections
* [MDEV-15249](https://jira.mariadb.org/browse/MDEV-15249) - IMPORT fixes
* [MDEV-14988](https://jira.mariadb.org/browse/MDEV-14988) - [innodb\_read\_only](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables) tries to modify files if transactions were recovered in COMMITTED state
* [MDEV-14773](https://jira.mariadb.org/browse/MDEV-14773) - [DROP TABLE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-definition/drop/drop-table) hangs for InnoDB table with [FULLTEXT index](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/optimization-and-indexes/full-text-indexes) (fixing a recent regression from upstream)

### Security Fixes

* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):

## Notes

For a complete list of changes made in [MariaDB 10.1.32](mariadb-10132-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-101-series/mariadb-10132-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.1.32](mariadb-10132-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-1-32-mariadb-10-1-32-and-mariadb-connector-j-2-2-3-and-1-7-3-now-available/).

A file format compatibility bug that was introduced in [MariaDB 10.1.0](mariadb-10-1-0-release-notes.md) was fixed in [MariaDB 10.1.21](mariadb-10121-release-notes.md).\
Using [page\_compression](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-page-compression) or non-default [innodb\_page\_size](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables) created files that were incompatible with [MariaDB 10.0](../release-notes-mariadb-10-0-series/changes-improvements-in-mariadb-10-0.md) or MySQL 5.6. [MariaDB 10.1.21](mariadb-10121-release-notes.md) and higher will convert affected files from earlier [MariaDB 10.1](changes-improvements-in-mariadb-10-1.md) releases to a compatible format.**This prevents a downgrade to earlier** [**MariaDB 10.1**](changes-improvements-in-mariadb-10-1.md) **versions.**[See the commit for details.](https://github.com/MariaDB/server/commit/ab1e6fefd869242d962cb91a006f37bb9ad534a7)

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
