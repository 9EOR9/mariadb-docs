# MariaDB 10.6.2 Release Notes

{% include "../../.gitbook/includes/latest-10-6.md" %}

<a href="https://downloads.mariadb.org/mariadb/10.6.5/" class="button primary">Download</a> <a href="mariadb-1062-release-notes.md" class="button secondary">Release Notes</a> <a href="../changelogs/changelogs-mariadb-106-series/mariadb-1062-changelog.md" class="button secondary">Changelog</a> <a href="what-is-mariadb-106.md" class="button secondary">Overview of 10.6</a>

**Release date:** 18 Jun 2021

[MariaDB 10.6](what-is-mariadb-106.md) is the current development series of MariaDB. It is an evolution\
of [MariaDB 10.5](../old-releases/mariadb-10-5-series/what-is-mariadb-105.md) with several entirely new features.

[MariaDB 10.6.2](mariadb-1062-release-notes.md) is a [_**Release Candidate (RC)**_](../../mariadb-release-criteria.md) release.

{% include "../../.gitbook/includes/non-stable.md" %}

Thanks, and enjoy MariaDB!

## Notable Changes

### InnoDB

* When [innodb\_adaptive\_hash\_index=OFF](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables#innodb_adaptive_hash_index) (the default), the following counters (which reflect btr\_cur\_n\_non\_sea) will no longer be updated ([MDEV-25882](https://jira.mariadb.org/browse/MDEV-25882)):
  * adaptive\_hash\_index in [INFORMATION\_SCHEMA.INNODB\_METRICS](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/system-tables/information-schema/information-schema-tables/information-schema-innodb-tables/information-schema-innodb_metrics-table)
  * [Innodb\_adaptive\_hash\_non\_hash\_searches](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/innodb-status-variables#innodb_adaptive_hash_non_hash_searches) in [INFORMATION\_SCHEMA.GLOBAL\_STATUS](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/system-tables/information-schema/information-schema-tables/information-schema-global_status-and-session_status-tables)

### Replication

* [Semisync](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/semisynchronous-replication) replica recovery is introduced. [rpl-semi-sync-slave-enabled = ON](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/semisynchronous-replication#rpl_semi_sync_slave_enabled) server executes a special recovery branch to guarantee its consistency with a primary server ([MDEV-21117](https://jira.mariadb.org/browse/MDEV-21117))

### General

* Error messages now use "MariaDB" instead of "MySQL" ([MDEV-22189](https://jira.mariadb.org/browse/MDEV-22189))
* Implement `FLUSH TABLES tbl_name [, tbl_name] ... WITH READ LOCK` for views ([MDEV-15888](https://jira.mariadb.org/browse/MDEV-15888))
* All statements can be prepared, except [PREPARE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/prepared-statements/prepare-statement), [EXECUTE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/prepared-statements/execute-statement), and [DEALLOCATE / DROP PREPARE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/prepared-statements/deallocate-drop-prepare) ([MDEV-16708](https://jira.mariadb.org/browse/MDEV-16708))

## Changelog

For a complete list of changes and bugfixes made in [MariaDB 10.6.2](mariadb-1062-release-notes.md), with links to detailed\
information on each push, see the [changelog](../changelogs/changelogs-mariadb-106-series/mariadb-1062-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.6.2](mariadb-1062-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-6-2-now-available/).

**Do not use non-stable (non-GA) releases in production!**

{% include "../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
