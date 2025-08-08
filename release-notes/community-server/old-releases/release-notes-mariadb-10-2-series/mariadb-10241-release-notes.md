# MariaDB 10.2.41 Release Notes

The most recent release of [MariaDB 10.2](what-is-mariadb-102.md) is:[**MariaDB 10.2.44**](mariadb-10244-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.2.44/)

[Download 10.2.41](https://downloads.mariadb.org/mariadb/10.2.41/) | [Release Notes](mariadb-10241-release-notes.md) | [Changelog](../../changelogs/changelogs-mariadb-102-series/mariadb-10241-changelog.md) | [Overview of 10.2](what-is-mariadb-102.md)

**Release date:** 8 Nov 2021

[MariaDB 10.2](what-is-mariadb-102.md) is a previous stable series of MariaDB. It is an evolution\
of [MariaDB 10.1](../release-notes-mariadb-10-1-series/changes-improvements-in-mariadb-10-1.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL 5.6 and 5.7.

[MariaDB 10.2.41](mariadb-10241-release-notes.md) is a [_**Stable (GA)**_](../../about/release-criteria.md) release.

**For an overview of** [**MariaDB 10.2**](what-is-mariadb-102.md) **see the**[**What is MariaDB 10.2?**](what-is-mariadb-102.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Items

### Galera

* Fix for `WSREP: invalid state ROLLED_BACK (FATAL)` ([MDEV-25114](https://jira.mariadb.org/browse/MDEV-25114))

### InnoDB

* `ALTER TABLE…IMPORT TABLESPACE` fixes ([MDEV-20931](https://jira.mariadb.org/browse/MDEV-20931), [MDEV-26131](https://jira.mariadb.org/browse/MDEV-26131))
* `innodb_undo_log_truncate` fixes ([MDEV-26450](https://jira.mariadb.org/browse/MDEV-26450), [MDEV-26864](https://jira.mariadb.org/browse/MDEV-26864))

### Replication

* Memory hogging on slave by ROW event applier is eliminated ([MDEV-26712](https://jira.mariadb.org/browse/MDEV-26712))
* `mysql --binary-mode` now properly handles `\\0` in data ([MDEV-25444](https://jira.mariadb.org/browse/MDEV-25444))
* Missed statement rollback in case transaction drops or create temporary table is corrected ([MDEV-26833](https://jira.mariadb.org/browse/MDEV-26833))

### Packaging & Misc

* Session tracking flag in OK\_PACKET ([MDEV-26868](https://jira.mariadb.org/browse/MDEV-26868))
* Some views force server (and mysqldump) to generate invalid SQL for their definitions ([MDEV-26299](https://jira.mariadb.org/browse/MDEV-26299))

### Security

* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2021-35604](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-35604)
  * [CVE-2021-46667](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-46667)
  * [CVE-2022-31624](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-31624)

Upgrading from 10.2 versions earlier than 10.2.17 is **highly recommended**\
for all [**Galera**](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/galera/README.md) users due to bug [MDEV-12837](https://jira.mariadb.org/browse/MDEV-12837) which caused serious stability\
issues with earlier versions. See the bug issue page for more information.\
When upgrading from [MariaDB 10.2.16](mariadb-10216-release-notes.md) or earlier to [MariaDB 10.2.17](mariadb-10217-release-notes.md) or higher,\
running [mysql\_upgrade](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/legacy-clients-and-utilities/mysql_upgrade) is **required** due to changes introduced in [MDEV-14637](https://jira.mariadb.org/browse/MDEV-14637).

## Changelog

For a complete list of changes made in [MariaDB 10.2.41](mariadb-10241-release-notes.md) with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-102-series/mariadb-10241-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.2.41](mariadb-10241-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-7-1-rc-and-mariadb-10-6-5-10-5-13-10-4-22-10-3-32-and-10-2-41-now-available/).

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
