# MariaDB 11.6.0 Release Notes

{% include "../../../.gitbook/includes/latest-11-6.md" %}

<a href="https://downloads.mariadb.org/mariadb/11.6.0" class="button primary">Download</a> <a href="mariadb-11-6-0-release-notes.md" class="button secondary">Release Notes</a>  <a href="what-is-mariadb-116.md" class="button secondary">Overview of 11.6</a>

**Release date:** 26 June 2024

{% include "../../../.gitbook/includes/non-stable.md" %}

[MariaDB 11.6](what-is-mariadb-116.md) is a [rolling release](../../about/release-model.md). It is an evolution of [MariaDB 11.5](../release-notes-mariadb-11-5-rolling-releases/what-is-mariadb-115.md) with several entirely new features.

[MariaDB 11.6.0](mariadb-11-6-0-release-notes.md) is a single preview release. Features are to be considered preview, and none are guaranteed to make it into [MariaDB 11.6](what-is-mariadb-116.md).

The preview is available as a container **quay.io/mariadb-foundation/mariadb-devel:11.6-preview**.

Thanks, and enjoy MariaDB!

## Notable Items

### Character Sets

* The default [character set](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/data-types/string-data-types/character-sets) has been changed from `latin1` to `utf8mb4` ([MDEV-19123](https://jira.mariadb.org/browse/MDEV-19123))

### Backup and Restore

* Added the `--dir` option to [mariadb-import](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/backup-restore-and-import-clients/mariadb-import), allowing one to restore all tables from a backup directory created using [mariadb-dump --dir](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/backup-restore-and-import-clients/mariadb-dump) ([MDEV-33627](https://jira.mariadb.org/browse/MDEV-33627))
  * Added the related `--database`, `--ignore-database`, `--table` and `--ignore-table` options.
  * Refactor [mariadb-import](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/backup-restore-and-import-clients/mariadb-import) threading
* Automatic SST user account management ([MDEV-31809](https://jira.mariadb.org/browse/MDEV-31809))

### Optimizer

* Improve selectivity computations for multi-part keys ([MDEV-33697](https://jira.mariadb.org/browse/MDEV-33697))

### Syntax

* Single-table [DELETEs](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-manipulation/changing-deleting-data/delete) now support table aliases ([MDEV-33988](https://jira.mariadb.org/browse/MDEV-33988))

### Authentication

* [New authentication plugin](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/plugins/authentication-plugins/authentication-plugin-parsec) ([MDEV-32618](https://jira.mariadb.org/browse/MDEV-32618))
* Extend [Unix socket authentication](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/plugins/authentication-plugins/authentication-plugin-unix-socket) to support authentication\_string ([MDEV-33479](https://jira.mariadb.org/browse/MDEV-33479))

### Replication

* New definition for Seconds\_Behind\_Master ([MDEV-33856](https://jira.mariadb.org/browse/MDEV-33856))
  * Added three variables to [SHOW ALL REPLICAS STATUS](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/show/show-replica-status)
  * New [Information Schema SLAVE\_STATUS Table](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/system-tables/information-schema/information-schema-tables/information-schema-slave_status-table)

### General

* Set thread names for MariaDB Server threads ([MDEV-32537](https://jira.mariadb.org/browse/MDEV-32537))

### Variables

* For a list of all new variables, see [System Variables Added in MariaDB 11.6](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/system-and-status-variables-added-by-major-release/system-and-status-variables-added-by-major-unmaintained-release/system-variables-added-in-mariadb-11-6) and [Status Variables Added in MariaDB 11.6](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/system-and-status-variables-added-by-major-release/system-and-status-variables-added-by-major-unmaintained-release/status-variables-added-in-mariadb-11-5).

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
