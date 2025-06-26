# MariaDB 10.1.4 Release Notes

The most recent release of [MariaDB 10.1](changes-improvements-in-mariadb-10-1.md) is:[**MariaDB 10.1.48**](mariadb-10148-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.1.48/)

[Download](https://downloads.mariadb.org/mariadb/10.1.4)[Release Notes](mariadb-10-1-4-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-101-series/mariadb-10-1-4-changelog.md)[Overview of 10.1](changes-improvements-in-mariadb-10-1.md)

**Release date:** 13 Apr 2015

[MariaDB 10.1](changes-improvements-in-mariadb-10-1.md) is the current development series of MariaDB. It is an evolution\
of [MariaDB 10.0](../release-notes-mariadb-10-0-series/changes-improvements-in-mariadb-10-0.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL 5.6 and 5.7.

[MariaDB 10.1.4](mariadb-10-1-4-release-notes.md) is a [_**Beta**_](../../../mariadb-release-criteria.md) release.

**For an overview of** [**MariaDB 10.1**](changes-improvements-in-mariadb-10-1.md) **see the**[**What is MariaDB 10.1?**](changes-improvements-in-mariadb-10-1.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

* Lots of changes related to encryption. See the [updated documentation](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/securing-mariadb-encryption/encryption-data-at-rest-encryption/data-at-rest-encryption-overview). In particular:
  * The distinction between “tablespace encryption” and “page encryption” was removed, now there is only one single encryption feature. One can use both per-table encryption options and the global [innodb-encrypt-tables](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables) option at the same time.
  * Per table `PAGE_ENCRYPTION` option that could accept values of `ON` and `OFF` was renamed to `ENCRYPTED` with values `YES` and `NO`.
  * Per table `PAGE_ENCRYPTION_KEY` was renamed to `ENCRYPTION_KEY_ID`.
  * Global variable `innodb_default_page_encryption_key` become a session [innodb\_default\_encryption\_key\_id](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables).
  * The command-line option [innodb-encrypt-tables](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables) can take the value of `FORCE`. In this case XtraDB/InnoDB will refuse to create unencrypted tables (`CREATE TABLE ... ENCRYPTED=NO` will fail).
  * XtraDB/InnoDB on disk format for encrypted tablespaces and logs was changed. Tables encrypted in 10.1.3 may fail to open.
  * Key management plugins were renamed not to have “plugin” in the name, for example, “file\_key\_management\_plugin” is now “file\_key\_management”.
  * “Key management plugin” type was expanded and renamed to match the new broader set of responsibilities. It is now called [encryption plugin](https://mariadb.com/docs/release-notes/enterprise-server/mariadb-enterprise-server-differences/mariadb-enterprise-server-data-at-rest-encryption/encryption-plugins).
* Command-line option `innodb-scrub-log-interval` was renamed to [innodb-scrub-log-speed](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/storage-engines/innodb/innodb-system-variables) and now sets the log scrubbing speed in bytes per second.
* Command-line option `innodb-scrub-force-testing` was renamed to `innodb-debug-force-scrubbing`.
* Consistent support for `IF EXISTS`, `IF NOT EXISTS`, and `OR REPLACE` clauses was added to:
  * [CREATE EVENT](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-definition/create/create-event) and [DROP EVENT](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-definition/drop/drop-event) ([MDEV-7281](https://jira.mariadb.org/browse/MDEV-7281))
  * [CREATE INDEX](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-definition/create/create-index) and [DROP INDEX](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-definition/drop/drop-index) ([MDEV-7284](https://jira.mariadb.org/browse/MDEV-7284))
  * [CREATE TRIGGER](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/triggers-events/triggers/create-trigger) and [DROP TRIGGER](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-definition/drop/drop-trigger) ([MDEV-7286](https://jira.mariadb.org/browse/MDEV-7286))
* [MDEV-5214](https://jira.mariadb.org/browse/MDEV-5214) New status variables to show the number of grants on different objects (see [Status Variables Added in MariaDB 10.1](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/system-and-status-variables-added-by-major-release/system-and-status-variables-added-by-major-unmaintained-release/status-variables-added-in-mariadb-101)).
* [MDEV-6858](https://jira.mariadb.org/browse/MDEV-6858) New server variable [enforce\_storage\_engine](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#enforce_storage_engine)
* [MDEV-7728](https://jira.mariadb.org/browse/MDEV-7728) xid cache scalability was significantly improved (by using lock-free hash)
* [MDEV-7671](https://jira.mariadb.org/browse/MDEV-7671) [VIEW](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/views) definitions are now cached in memory (in the table definition cache).
* [MDEV-6981](https://jira.mariadb.org/browse/MDEV-6981) New status variables to track MASTER\_GTID\_WAIT time. This feature was contributed by Daniel Black. See [Status Variables Added in MariaDB 10.1](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/system-and-status-variables-added-by-major-release/system-and-status-variables-added-by-major-unmaintained-release/status-variables-added-in-mariadb-101).
* [MDEV-7198](https://jira.mariadb.org/browse/MDEV-7198) New status variable [Slave\_skipped\_errors](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/replication-and-binary-log-status-variables#slave_skipped_errors). This feature was contributed by Daniel Black.
* Starting with this release, commits in certain instances in parallel replication complete immediately, avoiding losing throughput when many transactions need conflicting locks. See [binlog\_commit\_wait\_count](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/replication-and-binary-log-system-variables).
* [MDEV-7061](https://jira.mariadb.org/browse/MDEV-7061) [innochecksum](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/administrative-tools/innochecksum) can now analyze leaf pages to estimate how fragmented an index is and how much benefit can be gained from defragmentation.
* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * CVE-\`-\`\`\`

Repositories exist for 10.1, but because 10.1 is still Beta, they are not visible in the [repository configuration tool](https://downloads.mariadb.org/mariadb/repositories/). To configure a 10.1 apt, yum, or zypper repository using the tool, simply select 10.0 and then when executing the instructions, manually change all occurrences of '10.0' to '10.1'.

For a complete list of changes made in [MariaDB 10.1.4](mariadb-10-1-4-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-101-series/mariadb-10-1-4-changelog.md).

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
