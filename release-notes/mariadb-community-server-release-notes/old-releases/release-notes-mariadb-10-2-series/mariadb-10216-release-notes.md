# MariaDB 10.2.16 Release Notes

The most recent release of [MariaDB 10.2](what-is-mariadb-102.md) is:[**MariaDB 10.2.44**](mariadb-10244-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.2.44/)

[Download](https://downloads.mariadb.org/mariadb/10.2.16)[Release Notes](mariadb-10216-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-102-series/mariadb-10216-changelog.md)[Overview of 10.2](what-is-mariadb-102.md)

**Release date:** 26 Jun 2018

[MariaDB 10.2](what-is-mariadb-102.md) is the previous stable series of MariaDB. It is an evolution\
of [MariaDB 10.1](../release-notes-mariadb-10-1-series/changes-improvements-in-mariadb-10-1.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL 5.6 and 5.7.

[MariaDB 10.2.16](mariadb-10216-release-notes.md) is a [_**Stable (GA)**_](../../../mariadb-release-criteria.md) release.

**For an overview of** [**MariaDB 10.2**](what-is-mariadb-102.md) **see the**[**What is MariaDB 10.2?**](what-is-mariadb-102.md) **page.**

Upgrading from earlier 10.2.x versions is **highly recommended** for all **Galera** users due to bug [MDEV-12837](https://jira.mariadb.org/browse/MDEV-12837) which caused serious stability issues with earlier versions. See the bug issue page for more information.

Thanks, and enjoy MariaDB!

## Notable Changes

* [MyRocks](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/myrocks) is now [Stable (GA)](../../../mariadb-release-criteria.md)
* [MDEV-13122](https://jira.mariadb.org/browse/MDEV-13122): [mariadb-backup](broken-reference) now supports MyRocks
* [MDEV-13779](https://jira.mariadb.org/browse/MDEV-13779) - InnoDB fails to shut down purge workers, causing hang
* [MDEV-16267](https://jira.mariadb.org/browse/MDEV-16267) - Wrong INFORMATION\_SCHEMA.INNODB\_BUFFER\_PAGE.TABLE\_NAME
* [MDEV-13834](https://jira.mariadb.org/browse/MDEV-13834) - Upgrade failure from 10.1 innodb\_encrypt\_log
* [MDEV-16283](https://jira.mariadb.org/browse/MDEV-16283) - ALTER TABLE...DISCARD TABLESPACE still takes long on a large buffer pool
* [MDEV-16376](https://jira.mariadb.org/browse/MDEV-16376) - ASAN: heap-use-after-free in gcol.innodb\_virtual\_debug
* [MDEV-15824](https://jira.mariadb.org/browse/MDEV-15824) - innodb\_defragment=ON trumps innodb\_optimize\_fulltext\_only=ON in OPTIMIZE TABLE
* [MDEV-16124](https://jira.mariadb.org/browse/MDEV-16124) - fil\_rename\_tablespace() times out and crashes server during table-rebuilding ALTER TABLE
* [MDEV-16416](https://jira.mariadb.org/browse/MDEV-16416) - Crash on IMPORT TABLESPACE of a ROW\_FORMAT=COMPRESSED table
* [MDEV-16456](https://jira.mariadb.org/browse/MDEV-16456) - InnoDB error "returned OS error 71" complains about wrong path
* [MDEV-13103](https://jira.mariadb.org/browse/MDEV-13103) - Deal with page\_compressed page corruption
* [MDEV-16496](https://jira.mariadb.org/browse/MDEV-16496) - mariadb-backup: Implement --verbose option to instrument InnoDB log apply
* [MDEV-16087](https://jira.mariadb.org/browse/MDEV-16087) - Inconsistent SELECT results when query cache is enabled
* [MDEV-15114](https://jira.mariadb.org/browse/MDEV-15114) - ASAN heap-use-after-free in mem\_heap\_dup or dfield\_data\_is\_binary\_equal (fix for indexed virtual columns)
* As per the [MariaDB Deprecation Policy](../../../mariadb-platform-deprecation-policy.md), this will be\
  the last release of [MariaDB 10.2](what-is-mariadb-102.md) for Ubuntu 17.10 Artful
* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * CVE-\`-\`\`\`

## Changelog

For a complete list of changes made in [MariaDB 10.2.16](mariadb-10216-release-notes.md) with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-102-series/mariadb-10216-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.2.16](mariadb-10216-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-2-16-now-available/).

Be notified of new MariaDB Server releases automatically by [subscribing](https://lists.mariadb.org/postorius/lists/announce.lists.mariadb.org/) to the MariaDB Foundation community announce 'at' lists.mariadb.org announcement list (this is a low traffic, announce-only list). MariaDB plc customers will be notified for all new releases, security issues and critical bug fixes for all MariaDB plc products thanks to the Notification Services.

MariaDB may already be included in your favorite OS distribution. More\
information can be found on the[Distributions which Include MariaDB](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/distributions-including-mariadb)\
page.

{% @marketo/form formid="4316" formId="4316" %}
