# MariaDB 10.3.8 Release Notes

The most recent release of [MariaDB 10.3](what-is-mariadb-103.md) is:[**MariaDB 10.3.39**](mariadb-10-3-39-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.3.39/)

[Download](https://downloads.mariadb.org/mariadb/10.3.8)[Release Notes](mariadb-1038-release-notes.md)[Changelog](../../../changelogs/changelogs-mariadb-10-3-series/mariadb-1038-changelog.md)[Overview of 10.3](what-is-mariadb-103.md)

**Release date:** 2 Jul 2018

[MariaDB 10.3](what-is-mariadb-103.md) is an evolution\
of [MariaDB 10.2](../release-notes-mariadb-10-2-series/what-is-mariadb-102.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL.

[MariaDB 10.3.8](mariadb-1038-release-notes.md) is a [_**Stable (GA)**_](../../../mariadb-release-criteria.md) release.

**For an overview of MariaDB Server 10.3 see the**[**What is MariaDB 10.3?**](what-is-mariadb-103.md) **page or watch the webinar recording,** [**What's new in MariaDB TX 3.0**](https://go.mariadb.com/mariadbtx3.0_webinar_registration-LP.html?utm_source=kb\&utm_campaign=mariadbtx-ondemand-webinar_kb-release-notes)**.**

Thanks, and enjoy MariaDB!

## Notable Changes

Notable changes of this release include:

* [MDEV-8743](https://jira.mariadb.org/browse/MDEV-8743) - O\_CLOEXEC on innodb/xtradb temp files
* [MDEV-16267](https://jira.mariadb.org/browse/MDEV-16267) - Wrong INFORMATION\_SCHEMA.INNODB\_BUFFER\_PAGE.TABLE\_NAME
* [MDEV-13779](https://jira.mariadb.org/browse/MDEV-13779) - InnoDB fails to shut down purge, causing hang
* [MDEV-16283](https://jira.mariadb.org/browse/MDEV-16283) - ALTER TABLE...DISCARD TABLESPACE still takes long on a large buffer pool
* [MDEV-13834](https://jira.mariadb.org/browse/MDEV-13834) - Upgrade failure from 10.1 innodb\_encrypt\_log
* [MDEV-16376](https://jira.mariadb.org/browse/MDEV-16376) - ASAN: heap-use-after-free in gcol.innodb\_virtual\_debug
* [MDEV-15824](https://jira.mariadb.org/browse/MDEV-15824) - innodb\_defragment=ON trumps innodb\_optimize\_fulltext\_only=ON in OPTIMIZE TABLE
* [MDEV-16124](https://jira.mariadb.org/browse/MDEV-16124) - fil\_rename\_tablespace() times out and crashes server during table-rebuilding ALTER TABLE
* [MDEV-16416](https://jira.mariadb.org/browse/MDEV-16416) - Crash on IMPORT TABLESPACE of a ROW\_FORMAT=COMPRESSED table
* [MDEV-16456](https://jira.mariadb.org/browse/MDEV-16456) - InnoDB error "returned OS error 71" complains about wrong path
* [MDEV-16469](https://jira.mariadb.org/browse/MDEV-16469) - SET GLOBAL innodb\_change\_buffering has no effect
* [MDEV-13103](https://jira.mariadb.org/browse/MDEV-13103) - Deal with page\_compressed page corruption
* [MDEV-15611](https://jira.mariadb.org/browse/MDEV-15611) - Due to the failure of foreign key detection, Galera slave node killed himself
* [MDEV-16496](https://jira.mariadb.org/browse/MDEV-16496) - Mariabackup: Implement --verbose option to instrument InnoDB log apply
* [MDEV-16087](https://jira.mariadb.org/browse/MDEV-16087) - Inconsistent SELECT results when query cache is enabled
* [MDEV-15114](https://jira.mariadb.org/browse/MDEV-15114) - ASAN heap-use-after-free in mem\_heap\_dup or dfield\_data\_is\_binary\_equal
* [MDEV-16330](https://jira.mariadb.org/browse/MDEV-16330) - Allow instant change of WITH SYSTEM VERSIONING column attribute
* [MDEV-16365](https://jira.mariadb.org/browse/MDEV-16365) - Setting a column NOT NULL fails to return error for NULL values when there is no DEFAULT
* [MDEV-15953](https://jira.mariadb.org/browse/MDEV-15953) - Alter InnoDB Partitioned Table Moves Files (which were originally not in the datadir) to the datadir
* [MDEV-13122](https://jira.mariadb.org/browse/MDEV-13122): [mariabackup](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/backing-up-and-restoring-databases/mariabackup) now supports [MyRocks storage engine](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/myrocks)
* As per the [MariaDB Deprecation Policy](../../../mariadb-platform-deprecation-policy.md), this will be the last release of [MariaDB 10.3](what-is-mariadb-103.md) for Ubuntu 17.10 Artful

## Changelog

For a complete list of changes made in [MariaDB 10.3.8](mariadb-1038-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../../changelogs/changelogs-mariadb-10-3-series/mariadb-1038-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.3.8](mariadb-1038-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-3-8-now-available/).

Be notified of new MariaDB Server releases automatically by [subscribing](https://lists.mariadb.org/postorius/lists/announce.lists.mariadb.org/) to the MariaDB Foundation community announce 'at' lists.mariadb.org announcement list (this is a low traffic, announce-only list). MariaDB plc customers will be notified for all new releases, security issues and critical bug fixes for all MariaDB plc products thanks to the Notification Services.

MariaDB may already be included in your favorite OS distribution. More\
information can be found on the[Distributions which Include MariaDB](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/readme-1)\
page.
