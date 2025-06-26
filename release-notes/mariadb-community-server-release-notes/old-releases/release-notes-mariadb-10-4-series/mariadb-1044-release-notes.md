# MariaDB 10.4.4 Release Notes

The most recent release of [MariaDB 10.4](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/broken-reference/README.md) is:[**MariaDB 10.4.34**](mariadb-10-4-34-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.4.34/)

[Download](https://downloads.mariadb.org/mariadb/10.4.4)[Release Notes](mariadb-1044-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-10-4-series/mariadb-1044-changelog.md)[Overview of 10.4](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/broken-reference/README.md)

**Release date:** 7 Apr 2019

[MariaDB 10.4](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/broken-reference/README.md) is the current _development_ series of MariaDB. It is an evolution\
of [MariaDB 10.3](../release-notes-mariadb-10-3-series/what-is-mariadb-103.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL.

[MariaDB 10.4.4](mariadb-1044-release-notes.md) is a [_**Release Candidate**_](../../../mariadb-release-criteria.md) release.

**Do not use non-stable (non-GA) releases in production!**

**For an overview of** [**MariaDB 10.4**](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/broken-reference/README.md) **see the**[**What is MariaDB 10.4?**](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/broken-reference/README.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

* Enhancements:
  * [MDEV-12026](https://jira.mariadb.org/browse/MDEV-12026)/[MDEV-18644](https://jira.mariadb.org/browse/MDEV-18644): [innodb\_checksum\_algorithm=full\_crc32](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables#innodb_checksum_algorithm) (more robust file format)
  * [MDEV-13301](https://jira.mariadb.org/browse/MDEV-13301): Optimize DROP INDEX, ADD INDEX into RENAME INDEX
  * [MDEV-17380](https://jira.mariadb.org/browse/MDEV-17380): [innodb\_flush\_neighbors=ON](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables#innodb_flush_neighbors) should be ignored on SSD
* InnoDB data corruption fixes: [MDEV-14126](https://jira.mariadb.org/browse/MDEV-14126), [MDEV-18981](https://jira.mariadb.org/browse/MDEV-18981), [MDEV-18879](https://jira.mariadb.org/browse/MDEV-18879), [MDEV-18972](https://jira.mariadb.org/browse/MDEV-18972), [MDEV-18272](https://jira.mariadb.org/browse/MDEV-18272)
* Performance fixes to purge, startup and shutdown: [MDEV-18936](https://jira.mariadb.org/browse/MDEV-18936), [MDEV-18878](https://jira.mariadb.org/browse/MDEV-18878), [MDEV-18733](https://jira.mariadb.org/browse/MDEV-18733)
* Various fixes to [ALTER TABLE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-definition/alter/alter-table)
* Replication:
  * [MDEV-18450](https://jira.mariadb.org/browse/MDEV-18450): [wait for all slaves shutdown](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/shutdown)
  * [MDEV-19116](https://jira.mariadb.org/browse/MDEV-19116), [MDEV-19117](https://jira.mariadb.org/browse/MDEV-19117): speed up rotation of binary logs, `SHOW BINARY LOGS` etc with optimizing binary log index file locking
* Includes [Connector/C 3.1.0](../../../connectors/c/mariadb-connector-c-31-release-notes/mariadb-connector-c-310-release-notes.md)
* Repositories for CentOS 7, RHEL 7 & 8, Fedora 28 & 29, and SLES 12 & 15 now\
  include a src.rpm file that you can use to build MariaDB. Instructions for\
  doing so are found on the[Building MariaDB from a Source RPM](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/install-and-upgrade-mariadb/installing-mariadb/compiling-mariadb-from-source/building-mariadb-from-a-source-rpm)\
  page
* The [Galera library](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/what-is-mariadb-galera-cluster/README.md) in the repositories has\
  been updated to version 26.4.2
* As per the [MariaDB Deprecation Policy](../../../mariadb-platform-deprecation-policy.md), this is the\
  last release of [MariaDB 10.4](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/broken-reference/README.md) for Ubuntu 14.04 Trusty
* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * CVE-\`-\`\`\`

## Changelog

For a complete list of changes made in [MariaDB 10.4.4](mariadb-1044-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-10-4-series/mariadb-1044-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.4.4](mariadb-1044-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-4-4-now-available/).

{% include "https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/~/reusable/vX1KAy0t1XuYJaGsK28T/" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
