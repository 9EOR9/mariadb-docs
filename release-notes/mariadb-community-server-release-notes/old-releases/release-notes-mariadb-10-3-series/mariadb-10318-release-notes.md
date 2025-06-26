# MariaDB 10.3.18 Release Notes

The most recent release of [MariaDB 10.3](what-is-mariadb-103.md) is:[**MariaDB 10.3.39**](mariadb-10-3-39-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.3.39/)

[Download](https://downloads.mariadb.org/mariadb/10.3.18/)[Release Notes](mariadb-10318-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-10-3-series/mariadb-10318-changelog.md)[Overview of 10.3](what-is-mariadb-103.md)

**Release date:** 11 Sep 2019

[MariaDB 10.3](what-is-mariadb-103.md) is the previous stable series of MariaDB, and an evolution of [MariaDB 10.2](../release-notes-mariadb-10-2-series/what-is-mariadb-102.md) with several entirely new features\
not found anywhere else and with backported and reimplemented features from\
MySQL.

[MariaDB 10.3.18](mariadb-10318-release-notes.md) is a [_**Stable (GA)**_](../../../mariadb-release-criteria.md) release.

**For an overview of MariaDB Server 10.3 see the** [**What is MariaDB 10.3?**](what-is-mariadb-103.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

* [Connect](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/connect) updated to Connect 1.06.0010
* [MDEV-20066](https://jira.mariadb.org/browse/MDEV-20066): This bug could cause a table to become corrupt if a column was added instantly
* [MDEV-15326](https://jira.mariadb.org/browse/MDEV-15326): A race condition in InnoDB transaction commit that affects record locking was fixed
* [MDEV-17187](https://jira.mariadb.org/browse/MDEV-17187): Table doesn't exist in engine after ALTER of FOREIGN KEY
* [MDEV-20301](https://jira.mariadb.org/browse/MDEV-20301): InnoDB's MVCC has `O(N^2)` behaviors
* [MDEV-18128](https://jira.mariadb.org/browse/MDEV-18128): Simplify .ibd file creation
* [MDEV-20060](https://jira.mariadb.org/browse/MDEV-20060): Failing assertion: `srv_log_file_size <= 512ULL << 30` while preparing backup
* [MDEV-20247](https://jira.mariadb.org/browse/MDEV-20247): Replication hangs with "preparing" and never starts
* [MDEV-17614](https://jira.mariadb.org/browse/MDEV-17614): Remove unnecessary locking for `INSERT...ON DUPLICATE KEY UPDATE`
* [MDEV-20311](https://jira.mariadb.org/browse/MDEV-20311): row\_ins\_step accesses uninitialized memory
* [MDEV-19947](https://jira.mariadb.org/browse/MDEV-19947): [Repositories](https://downloads.mariadb.org/mariadb/repositories/) for RHEL 8 ppc64le added
* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * CVE-\`-\`\`\`

When upgrading from [MariaDB 10.3.8](mariadb-1038-release-notes.md) or earlier to [MariaDB 10.3.9](mariadb-1039-release-notes.md) or higher,\
running [mysql\_upgrade](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/legacy-clients-and-utilities/mysql_upgrade) is **required** due to changes introduced in[MDEV-14637](https://jira.mariadb.org/browse/MDEV-14637).

## Changelog

For a complete list of changes made in [MariaDB 10.3.18](mariadb-10318-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-10-3-series/mariadb-10318-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.3.18](mariadb-10318-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-4-8-10-3-18-and-10-2-27-now-available/).

{% include "https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/~/reusable/vX1KAy0t1XuYJaGsK28T/" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
