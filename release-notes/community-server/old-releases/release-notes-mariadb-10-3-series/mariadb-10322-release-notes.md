# MariaDB 10.3.22 Release Notes

The most recent release of [MariaDB 10.3](what-is-mariadb-103.md) is:[**MariaDB 10.3.39**](mariadb-10-3-39-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.3.39/)

Note that this version contains an issue that disabled all events created by a server with a different server\_id. See [MDEV-21758](https://jira.mariadb.org/browse/MDEV-21758) for details.

[Download](https://downloads.mariadb.org/mariadb/10.3.22/) | [Release Notes](mariadb-10322-release-notes.md) | [Changelog](../../changelogs/changelogs-mariadb-10-3-series/mariadb-10322-changelog.md) | [Overview of 10.3](what-is-mariadb-103.md)

**Release date:** 28 Jan 2020

[MariaDB 10.3](what-is-mariadb-103.md) is the previous stable series of MariaDB, and an evolution of [MariaDB 10.2](../release-notes-mariadb-10-2-series/what-is-mariadb-102.md) with several entirely new features\
not found anywhere else and with backported and reimplemented features from\
MySQL.

[MariaDB 10.3.22](mariadb-10322-release-notes.md) is a [_**Stable (GA)**_](../../about/release-criteria.md) release.

**For an overview of MariaDB Server 10.3 see the** [**What is MariaDB 10.3?**](what-is-mariadb-103.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

### General

* [MDEV-21337](https://jira.mariadb.org/browse/MDEV-21337): fix aligned\_malloc()
* [MDEV-21343](https://jira.mariadb.org/browse/MDEV-21343): Threadpool/Unix- wait\_begin() function does not wake/create threa\
  ds, when it should
* As per the [MariaDB Deprecation Policy](../../about/platform-deprecation-policy.md), this will be the last release of [MariaDB 10.3](what-is-mariadb-103.md) for Ubuntu 19.04 Disco

### mariadb-backup

* [MDEV-21255](https://jira.mariadb.org/browse/MDEV-21255): Deadlock of parallel slave and mariadb-backup (with failed log copy thread)

### InnoDB

* [MDEV-20950](https://jira.mariadb.org/browse/MDEV-20950): Reduce size of record offsets
* [MDEV-19176](https://jira.mariadb.org/browse/MDEV-19176): Reduce the memory usage during recovery
* [MDEV-21429](https://jira.mariadb.org/browse/MDEV-21429): TRUNCATE and OPTIMIZE are being refused due to "row size too large"
* [MDEV-21500](https://jira.mariadb.org/browse/MDEV-21500): Server hang when using simulated AIO
* [MDEV-21509](https://jira.mariadb.org/browse/MDEV-21509): Possible hang during purge of history, or rollback
* [MDEV-21511](https://jira.mariadb.org/browse/MDEV-21511): Wrong estimate of affected BLOB columns in update
* [MDEV-21512](https://jira.mariadb.org/browse/MDEV-21512): InnoDB may hang due to SPATIAL INDEX
* [MDEV-21513](https://jira.mariadb.org/browse/MDEV-21513): Avoid some crashes in ALTER TABLE...IMPORT TABLESPACE
* [MDEV-18865](https://jira.mariadb.org/browse/MDEV-18865): Assertion \`t->first->versioned\_by\_id()' failed in innodb\_prepare\_commit\_versioned

### Aria

* [MDEV-14183](https://jira.mariadb.org/browse/MDEV-14183): aria\_pack segfaults in compress\_maria\_file

### Optimizer

* [MDEV-21318](https://jira.mariadb.org/browse/MDEV-21318): Wrong results with window functions and implicit grouping
* [MDEV-16579](https://jira.mariadb.org/browse/MDEV-16579): Wrong result of query using DISTINCT COUNT(_) OVER (_)
* [MDEV-21383](https://jira.mariadb.org/browse/MDEV-21383): Possible range plan is not used under certain conditions

### Replication

* [MDEV-18046](https://jira.mariadb.org/browse/MDEV-18046): Crashes caused by random values to the offset option of SHOW BINLOG EVENT offset command
* [MDEV-19376](https://jira.mariadb.org/browse/MDEV-19376): Semisync Master could crash when it executed RESET MASTER and a replica reconnects using GTID protocol

### Security

* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2020-2574](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-2574)

When upgrading from [MariaDB 10.3.8](mariadb-1038-release-notes.md) or earlier to [MariaDB 10.3.9](mariadb-1039-release-notes.md) or higher,\
running [mysql\_upgrade](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/legacy-clients-and-utilities/mysql_upgrade) is **required** due to changes introduced in[MDEV-14637](https://jira.mariadb.org/browse/MDEV-14637).

## Changelog

For a complete list of changes made in [MariaDB 10.3.22](mariadb-10322-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-10-3-series/mariadb-10322-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.3.22](mariadb-10322-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-4-12-10-3-22-and-10-2-31-10-1-44-and-5-5-67-now-available/).

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
