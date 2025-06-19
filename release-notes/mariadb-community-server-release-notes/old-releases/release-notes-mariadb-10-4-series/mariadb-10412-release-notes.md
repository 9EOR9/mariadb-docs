# MariaDB 10.4.12 Release Notes

The most recent release of [MariaDB 10.4](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/broken-reference/README.md) is:[**MariaDB 10.4.34**](mariadb-10-4-34-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.4.34/)

Note that this version contains an issue that disabled all events created by a server with a different server\_id. See [MDEV-21758](https://jira.mariadb.org/browse/MDEV-21758) for details.

[Download](https://downloads.mariadb.org/mariadb/10.4.12/)[Release Notes](mariadb-10412-release-notes.md)[Changelog](../../../changelogs/changelogs-mariadb-10-4-series/mariadb-10412-changelog.md)[Overview of 10.4](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/broken-reference/README.md)

**Release date:** 28 Jan 2020

[MariaDB 10.4](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/broken-reference/README.md) is the current _stable_ series of MariaDB. It is an evolution\
of [MariaDB 10.3](../release-notes-mariadb-10-3-series/what-is-mariadb-103.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL.

[MariaDB 10.4.12](mariadb-10412-release-notes.md) will be a [_**Stable (GA)**_](../../../mariadb-release-criteria.md) release.

**For an overview of** [**MariaDB 10.4**](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/broken-reference/README.md) **see the**[**What is MariaDB 10.4?**](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/broken-reference/README.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

### General

* [MDEV-21337](https://jira.mariadb.org/browse/MDEV-21337): fix aligned\_malloc()
* [MDEV-21343](https://jira.mariadb.org/browse/MDEV-21343): Threadpool/Unix- wait\_begin() function does not wake/create threa\
  ds, when it should
* wolfssl updated to v4.3.0-stable
* As per the [MariaDB Deprecation Policy](../../../mariadb-platform-deprecation-policy.md), this will be the last release of [MariaDB 10.4](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/broken-reference/README.md) for Ubuntu 19.04 Disco

### mariadb-backup

* [MDEV-21255](https://jira.mariadb.org/browse/MDEV-21255): Deadlock of parallel slave and mariabackup (with failed log copy thread)

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
* [MDEV-21260](https://jira.mariadb.org/browse/MDEV-21260): InnoDB does not report error when trying open volumes on UNC paths on Windows

### Aria

* [MDEV-14183](https://jira.mariadb.org/browse/MDEV-14183): aria\_pack segfaults in compress\_maria\_file

### Optimizer

* [MDEV-21318](https://jira.mariadb.org/browse/MDEV-21318): Wrong results with window functions and implicit grouping
* [MDEV-16579](https://jira.mariadb.org/browse/MDEV-16579): Wrong result of query using DISTINCT COUNT(_) OVER (_)
* [MDEV-21383](https://jira.mariadb.org/browse/MDEV-21383): Possible range plan is not used under certain conditions

### Replication

* [MDEV-18046](https://jira.mariadb.org/browse/MDEV-18046): Crashes caused by random values to the offset option of SHOW BINLOG EVENT offset command
* [MDEV-19376](https://jira.mariadb.org/browse/MDEV-19376): Semisync Master could crash when it executed RESET MASTER and a replica reconnects using GTID protocol
* [MDEV-20821](https://jira.mariadb.org/browse/MDEV-20821): parallel slave server shutdown may hang when slave workers were online

### Security

* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2020-2574](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-2574)
  * [CVE-2020-7221](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-7221)

## Changelog

For a complete list of changes made in [MariaDB 10.4.12](mariadb-10412-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../../changelogs/changelogs-mariadb-10-4-series/mariadb-10412-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.4.12](mariadb-10412-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-4-12-10-3-22-and-10-2-31-10-1-44-and-5-5-67-now-available/).

Be notified of new MariaDB Server releases automatically by [subscribing](https://lists.mariadb.org/postorius/lists/announce.lists.mariadb.org/) to the MariaDB Foundation community announce 'at' lists.mariadb.org announcement list (this is a low traffic, announce-only list). MariaDB plc customers will be notified for all new releases, security issues and critical bug fixes for all MariaDB plc products thanks to the Notification Services.

MariaDB may already be included in your favorite OS distribution. More\
information can be found on the[Distributions which Include MariaDB](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/distributions-including-mariadb)\
page.

{% @marketo/form formid="4316" formId="4316" %}
