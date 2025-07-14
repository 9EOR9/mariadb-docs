# MariaDB 10.3.2 Release Notes

The most recent release of [MariaDB 10.3](what-is-mariadb-103.md) is:[**MariaDB 10.3.39**](mariadb-10-3-39-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.3.39/)

[Download](https://downloads.mariadb.org/mariadb/10.3.2)[Release Notes](mariadb-1032-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-10-3-series/mariadb-1032-changelog.md)[Overview of 10.3](what-is-mariadb-103.md)

**Release date:** 9 Oct 2017

**Do not use&#x20;**_**alpha**_**&#x20;releases in production!**

[MariaDB 10.3](what-is-mariadb-103.md) is the current development series of MariaDB. It is an evolution\
of [MariaDB 10.2](../release-notes-mariadb-10-2-series/what-is-mariadb-102.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL.

[MariaDB 10.3.2](mariadb-1032-release-notes.md) is an [_**Alpha**_](../../../mariadb-release-criteria.md) release.

**For an overview of** [**MariaDB 10.3**](what-is-mariadb-103.md) **see the**[**What is MariaDB 10.3?**](what-is-mariadb-103.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

Notable changes of this release include:

* [Instant ADD COLUMN](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-online-ddl/instant-add-column-for-innodb) ([MDEV-11369](https://jira.mariadb.org/browse/MDEV-11369)) — Tencent Game DBA Team, developed by vinchen.
* [UPDATE statements with the same source and target](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-manipulation/changing-deleting-data/update#update-statements-with-the-same-source-and-target) ([MDEV-12874](https://jira.mariadb.org/browse/MDEV-12874)) — from Jerome Brauge.
* [ORDER BY](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-manipulation/selecting-data/order-by) and [LIMIT](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-manipulation/selecting-data/limit) in multi-table update ([MDEV-13911](https://jira.mariadb.org/browse/MDEV-13911))
* [DATE\_FORMAT(date, format, locale)](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/date-time-functions/date_format) - 3 argument form of DATE\_FORMAT ([MDEV-11553](https://jira.mariadb.org/browse/MDEV-11553))

### Compression

* [Storage-engine Independent Column Compression](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/optimization-and-tuning-compression/storage-engine-independent-column-compression) ([MDEV-11371](https://jira.mariadb.org/browse/MDEV-11371)) — Tencent Game DBA Team, developed by willhan, also thanks to AliSQL.

### Encryption

* Temporary files created by merge sort and row log are encrypted if [innodb\_encrypt\_log](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables) is set to `1`, regardless of whether the table encrypted or not ([MDEV-12634](https://jira.mariadb.org/browse/MDEV-12634)).

### Variables

* [version\_source\_revision](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#version_source_revision) - permits seeing which version of the source was used for the build ([MDEV-12583](https://jira.mariadb.org/browse/MDEV-12583)).
* Renamed `idle_readwrite_transaction_timeout` to [idle\_write\_transaction\_timeout](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#idle_write_transaction_timeout).

The following deprecated variables have been removed:

* [innodb\_mtflush\_threads](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables)
* [innodb\_use\_mtflush](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables)

**Do not use&#x20;**_**alpha**_**&#x20;releases in production!**

For a complete list of changes made in [MariaDB 10.3.2](mariadb-1032-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-10-3-series/mariadb-1032-changelog.md).

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
