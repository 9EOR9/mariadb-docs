# MariaDB 10.1.34 Release Notes

The most recent release of [MariaDB 10.1](changes-improvements-in-mariadb-10-1.md) is:[**MariaDB 10.1.48**](mariadb-10148-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.1.48/)

[Download](https://downloads.mariadb.org/mariadb/10.1.34)[Release Notes](mariadb-10134-release-notes.md)[Changelog](../../../changelogs/changelogs-mariadb-101-series/mariadb-10134-changelog.md)[Overview of 10.1](changes-improvements-in-mariadb-10-1.md)

**Release date:** 18 Jun 2018

[MariaDB 10.1](changes-improvements-in-mariadb-10-1.md) is a previous stable series of MariaDB. It is an evolution\
of [MariaDB 10.0](../release-notes-mariadb-10-0-series/changes-improvements-in-mariadb-10-0.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL 5.6 and 5.7.

[MariaDB 10.1.34](mariadb-10134-release-notes.md) is a [_**Stable (GA)**_](../../../mariadb-release-criteria.md) release.

**For an overview of** [**MariaDB 10.1**](changes-improvements-in-mariadb-10-1.md) **see the**[**What is MariaDB 10.1?**](changes-improvements-in-mariadb-10-1.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

* [MDEV-14589](https://jira.mariadb.org/browse/MDEV-14589) InnoDB should not lock a delete-marked record
* [MDEV-16283](https://jira.mariadb.org/browse/MDEV-16283) ALTER TABLE...DISCARD TABLESPACE still takes long on a large buffer pool
* [MDEV-15824](https://jira.mariadb.org/browse/MDEV-15824) innodb\_defragment=ON trumps innodb\_optimize\_fulltext\_only=ON in OPTIMIZE TABLE
* [MDEV-16124](https://jira.mariadb.org/browse/MDEV-16124) fil\_rename\_tablespace() times out and crashes server during table-rebuilding ALTER TABLE
* [MDEV-16416](https://jira.mariadb.org/browse/MDEV-16416) Crash on IMPORT TABLESPACE of a ROW\_FORMAT=COMPRESSED table
* [MDEV-16456](https://jira.mariadb.org/browse/MDEV-16456) InnoDB error "returned OS error 71" complains about wrong path
* [MDEV-13103](https://jira.mariadb.org/browse/MDEV-13103) Deal with page\_compressed page corruption
* [MDEV-15611](https://jira.mariadb.org/browse/MDEV-15611) Due to the failure of foreign key detection, Galera slave node killed himself.
* As per the [MariaDB Deprecation Policy](../../../mariadb-platform-deprecation-policy.md), this will be\
  the last release of [MariaDB 10.1](changes-improvements-in-mariadb-10-1.md) for Ubuntu 17.10 Artful

### Security Fixes

* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * CVE-\`-\`\`\`

## Changelog

For a complete list of changes made in [MariaDB 10.1.34](mariadb-10134-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../../changelogs/changelogs-mariadb-101-series/mariadb-10134-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.1.34](mariadb-10134-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-1-34-and-latest-mariadb-connectors-now-available/).

A file format compatibility bug that was introduced in [MariaDB 10.1.0](mariadb-10-1-0-release-notes.md) was fixed in [MariaDB 10.1.21](mariadb-10121-release-notes.md).\
Using [page\_compression](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-page-compression) or non-default [innodb\_page\_size](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables) created files that were incompatible with [MariaDB 10.0](../release-notes-mariadb-10-0-series/changes-improvements-in-mariadb-10-0.md) or MySQL 5.6. [MariaDB 10.1.21](mariadb-10121-release-notes.md) and higher will convert affected files from earlier [MariaDB 10.1](changes-improvements-in-mariadb-10-1.md) releases to a compatible format.**This prevents a downgrade to earlier** [**MariaDB 10.1**](changes-improvements-in-mariadb-10-1.md) **versions.**[See the commit for details.](https://github.com/MariaDB/server/commit/ab1e6fefd869242d962cb91a006f37bb9ad534a7)

Be notified of new MariaDB Server releases automatically by [subscribing](https://lists.mariadb.org/postorius/lists/announce.lists.mariadb.org/) to the MariaDB Foundation community announce 'at' lists.mariadb.org announcement list (this is a low traffic, announce-only list). MariaDB plc customers will be notified for all new releases, security issues and critical bug fixes for all MariaDB plc products thanks to the Notification Services.

MariaDB may already be included in your favorite OS distribution. More\
information can be found on the[Distributions which Include MariaDB](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/distributions-including-mariadb)\
page.

{% @marketo/form formid="4316" formId="4316" %}
