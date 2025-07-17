# MariaDB 10.2.27 Release Notes

The most recent release of [MariaDB 10.2](what-is-mariadb-102.md) is:[**MariaDB 10.2.44**](mariadb-10244-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.2.44/)

[Download](https://downloads.mariadb.org/mariadb/10.2.27/)[Release Notes](mariadb-10227-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-102-series/mariadb-10227-changelog.md)[Overview of 10.2](what-is-mariadb-102.md)

**Release date:** 11 Sep 2019

[MariaDB 10.2](what-is-mariadb-102.md) is a previous stable series of MariaDB. It is an evolution\
of [MariaDB 10.1](../release-notes-mariadb-10-1-series/changes-improvements-in-mariadb-10-1.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL 5.6 and 5.7.

[MariaDB 10.2.27](mariadb-10227-release-notes.md) is a [_**Stable (GA)**_](../../about/release-criteria.md) release.

**For an overview of** [**MariaDB 10.2**](what-is-mariadb-102.md) **see the**[**What is MariaDB 10.2?**](what-is-mariadb-102.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

* [Connect](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/connect) updated to Connect 1.06.0010
* [MDEV-15326](https://jira.mariadb.org/browse/MDEV-15326): A race condition in InnoDB transaction commit that affects record locking was fixed
* [MDEV-17187](https://jira.mariadb.org/browse/MDEV-17187): Table doesn't exist in engine after ALTER of FOREIGN KEY
* [MDEV-20301](https://jira.mariadb.org/browse/MDEV-20301): InnoDB's MVCC has `O(N^2)` behaviors
* [MDEV-18128](https://jira.mariadb.org/browse/MDEV-18128): Simplify .ibd file creation
* [MDEV-20060](https://jira.mariadb.org/browse/MDEV-20060): Failing assertion: `srv_log_file_size <= 512ULL << 30` while preparing backup
* [MDEV-20247](https://jira.mariadb.org/browse/MDEV-20247): Replication hangs with "preparing" and never starts
* [MDEV-17614](https://jira.mariadb.org/browse/MDEV-17614): Remove unnecessary locking for `INSERT...ON DUPLICATE KEY UPDATE`
* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * CVE-\`-\`\`\`

Upgrading from 10.2 versions earlier than 10.2.17 is **highly recommended**\
for all [**Galera**](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/galera/README.md) users due to bug [MDEV-12837](https://jira.mariadb.org/browse/MDEV-12837) which caused serious stability\
issues with earlier versions. See the bug issue page for more information.\
When upgrading from [MariaDB 10.2.16](mariadb-10216-release-notes.md) or earlier to [MariaDB 10.2.17](mariadb-10217-release-notes.md) or higher,\
running [mysql\_upgrade](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/legacy-clients-and-utilities/mysql_upgrade) is **required** due to changes introduced in [MDEV-14637](https://jira.mariadb.org/browse/MDEV-14637).

## Changelog

For a complete list of changes made in [MariaDB 10.2.27](mariadb-10227-release-notes.md) with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-102-series/mariadb-10227-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.2.27](mariadb-10227-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-4-8-10-3-18-and-10-2-27-now-available/).

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
