# MariaDB 10.2.12 Release Notes

The most recent release of [MariaDB 10.2](what-is-mariadb-102.md) is:[**MariaDB 10.2.44**](mariadb-10244-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.2.44/)

[Download](https://downloads.mariadb.org/mariadb/10.2.12)[Release Notes](mariadb-10212-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-102-series/mariadb-10212-changelog.md)[Overview of 10.2](what-is-mariadb-102.md)

**Release date:** 4 Jan 2018

[MariaDB 10.2](what-is-mariadb-102.md) is the current stable series of MariaDB. It is an evolution\
of [MariaDB 10.1](../release-notes-mariadb-10-1-series/changes-improvements-in-mariadb-10-1.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL 5.6 and 5.7.

[MariaDB 10.2.12](mariadb-10212-release-notes.md) is a [_**Stable (GA)**_](../../../mariadb-release-criteria.md) release.

**For an overview of** [**MariaDB 10.2**](what-is-mariadb-102.md) **see the**[**What is MariaDB 10.2?**](what-is-mariadb-102.md) **page.**

Upgrading from earlier 10.2.x versions is **highly recommended** for all **Galera** users due to bug [MDEV-12837](https://jira.mariadb.org/browse/MDEV-12837) which caused serious stability issues with earlier versions. See the bug issue page for more information.

Thanks, and enjoy MariaDB!

## Notable Changes

* [MDEV-12837](https://jira.mariadb.org/browse/MDEV-12837) - WSREP: BF lock wait long
* [MDEV-14799](https://jira.mariadb.org/browse/MDEV-14799) - After UPDATE of indexed columns, old values will not be purged from secondary indexes
* [MDEV-12827](https://jira.mariadb.org/browse/MDEV-12827) - Assertion failure when reporting duplicate key error in online table rebuild
* [MDEV-14008](https://jira.mariadb.org/browse/MDEV-14008) - Failure reading auto-increment values in DOUBLE column from storage engine
* [MDEV-12323](https://jira.mariadb.org/browse/MDEV-12323) - Rollback progress log messages during crash recovery are intermixed with unrelated log messages
* [MDEV-12352](https://jira.mariadb.org/browse/MDEV-12352) - InnoDB shutdown should not be blocked by a large transaction rollback
* [MDEV-13797](https://jira.mariadb.org/browse/MDEV-13797) - InnoDB may hang if shutdown is initiated soon after startup while rolling back recovered incomplete transactions
* [MDEV-14422](https://jira.mariadb.org/browse/MDEV-14422) - Assertion failure in trx\_purge\_run() on shutdown
* [MDEV-14589](https://jira.mariadb.org/browse/MDEV-14589) - InnoDB should not lock a delete-marked record
* [MDEV-14714](https://jira.mariadb.org/browse/MDEV-14714) / [MDEV-14488](https://jira.mariadb.org/browse/MDEV-14488) / [MDEV-14644](https://jira.mariadb.org/browse/MDEV-14644) - data corruption caused by error log messages ending up in database files or binary logs
* [MDEV-14511](https://jira.mariadb.org/browse/MDEV-14511) - Use fewer transactions for updating InnoDB persistent statistics
* [MDEV-13670](https://jira.mariadb.org/browse/MDEV-13670) / [MDEV-14550](https://jira.mariadb.org/browse/MDEV-14550) - Error log flood : "InnoDB: page\_cleaner: 1000ms intended loop took N ms. The settings might not be optimal."
* [mariadb-backup](broken-reference): [MDEV-14536](https://jira.mariadb.org/browse/MDEV-14536) - during backup, retry read of log blocks, if there is (possibly intermittent) checksum mismatch
* As per the [MariaDB Deprecation Policy](../../../mariadb-platform-deprecation-policy.md), this will be the last release of [MariaDB 10.2](what-is-mariadb-102.md) for Ubuntu 17.04 "Zesty".

### Updates

* The [reserved word](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-structure/sql-language-structure/reserved-words) `WINDOW` is now only disallowed for table aliases.
* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2018-3133](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-3133)

## Notes

For a complete list of changes made in [MariaDB 10.2.12](mariadb-10212-release-notes.md) with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-102-series/mariadb-10212-changelog.md).

{% include "https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/~/reusable/vX1KAy0t1XuYJaGsK28T/" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
