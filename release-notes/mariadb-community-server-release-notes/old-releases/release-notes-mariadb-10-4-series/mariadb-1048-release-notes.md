# MariaDB 10.4.8 Release Notes

The most recent release of [MariaDB 10.4](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series) is:[**MariaDB 10.4.34**](mariadb-10-4-34-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.4.34/)

[Download](https://downloads.mariadb.org/mariadb/10.4.8/)[Release Notes](mariadb-1048-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-10-4-series/mariadb-1048-changelog.md)[Overview of 10.4](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/what-is-mariadb-104)

**Release date:** 11 Sep 2019

[MariaDB 10.4](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series) is the current _stable_ series of MariaDB. It is an evolution\
of [MariaDB 10.3](../release-notes-mariadb-10-3-series/what-is-mariadb-103.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL.

[MariaDB 10.4.8](mariadb-1048-release-notes.md) will be a [_**Stable (GA)**_](../../../mariadb-release-criteria.md) release.

**For an overview of** [**MariaDB 10.4**](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series) **see the**[**What is MariaDB 10.4?**](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/what-is-mariadb-104) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

Notable changes of this release include:

* [Connect](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/connect) updated to Connect 1.06.0010
* [MDEV-20231](https://jira.mariadb.org/browse/MDEV-20231): Update server [HELP](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/help-command)
* [MDEV-20066](https://jira.mariadb.org/browse/MDEV-20066): This bug could cause a table to become corrupt if a column was added instantly
* [MDEV-15326](https://jira.mariadb.org/browse/MDEV-15326): A race condition in InnoDB transaction commit that affects record locking was fixed
* [MDEV-17187](https://jira.mariadb.org/browse/MDEV-17187): Table doesn't exist in engine after ALTER of FOREIGN KEY
* [MDEV-20301](https://jira.mariadb.org/browse/MDEV-20301): InnoDB's MVCC has `O(N^2)` behaviors
* [MDEV-18128](https://jira.mariadb.org/browse/MDEV-18128): Simplify .ibd file creation
* [MDEV-20060](https://jira.mariadb.org/browse/MDEV-20060): Failing assertion: `srv_log_file_size <= 512ULL << 30` while preparing backup
* [MDEV-20247](https://jira.mariadb.org/browse/MDEV-20247): Replication hangs with "preparing" and never starts
* [MDEV-17614](https://jira.mariadb.org/browse/MDEV-17614): Remove unnecessary locking for `INSERT...ON DUPLICATE KEY UPDATE`
* [MDEV-20311](https://jira.mariadb.org/browse/MDEV-20311): row\_ins\_step accesses uninitialized memory
* [MDEV-20479](https://jira.mariadb.org/browse/MDEV-20479): Assertion failure in `dict_table_get_nth_col()` after `INSTANT DROP COLUMN`
* [MDEV-20340](https://jira.mariadb.org/browse/MDEV-20340): Encrypted temporary tables cannot be read with `innodb_checksum_algorithm=full_crc32`
* [MDEV-19947](https://jira.mariadb.org/browse/MDEV-19947): [Repositories](https://downloads.mariadb.org/mariadb/repositories/) for RHEL 8 ppc64le added
* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * CVE-\`-\`\`\`

## Changelog

For a complete list of changes made in [MariaDB 10.4.8](mariadb-1048-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-10-4-series/mariadb-1048-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.4.8](mariadb-1048-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-4-8-10-3-18-and-10-2-27-now-available/).

{% include "https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/~/reusable/vX1KAy0t1XuYJaGsK28T/" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
