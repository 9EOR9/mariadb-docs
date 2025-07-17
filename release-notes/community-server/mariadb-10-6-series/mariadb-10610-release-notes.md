# MariaDB 10.6.10 Release Notes

{% include "../../.gitbook/includes/latest-10-6.md" %}

<a href="https://downloads.mariadb.org/mariadb/10.6.10/" class="button primary">Download</a> <a href="mariadb-10610-release-notes.md" class="button secondary">Release Notes</a> <a href="../changelogs/changelogs-mariadb-106-series/mariadb-10610-changelog.md" class="button secondary">Changelog</a> <a href="what-is-mariadb-106.md" class="button secondary">Overview of 10.6</a>

**Release date:** 19 Sep 2022

[MariaDB 10.6](what-is-mariadb-106.md) is the current long-term maintenance stable series of MariaDB, maintained until July 2026. It is an evolution of [MariaDB 10.5](../old-releases/mariadb-10-5-series/what-is-mariadb-105.md) with several entirely new features.

[MariaDB 10.6.10](mariadb-10610-release-notes.md) is a [_**Stable (GA)**_](../about/release-criteria.md) release.

Thanks, and enjoy MariaDB!

## Notable Items

### Issues Fixed

* Assertion mysql\_mutex\_assert\_owner(\&log\_sys.flush\_order\_mutex) failed in mtr\_t::commit() ([MDEV-29383](https://jira.mariadb.org/browse/MDEV-29383))
* Frequent "Data structure corruption" in InnoDB after OOM ([MDEV-29374](https://jira.mariadb.org/browse/MDEV-29374))
* Recovery or backup of instant ALTER TABLE is incorrect ([MDEV-29438](https://jira.mariadb.org/browse/MDEV-29438))
* InnoDB Temporary Tablespace (ibtmp1) is continuously growing ([MDEV-28240](https://jira.mariadb.org/browse/MDEV-28240))
* Full text index corruption if shutdown before changes are fully flushed ([MDEV-29342](https://jira.mariadb.org/browse/MDEV-29342))
* [JSON\_VALUE()](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/special-functions/json-functions/json_value) does not parse NULL properties properly ([MDEV-27151](https://jira.mariadb.org/browse/MDEV-27151))
* InnoDB hangs on multiple concurrent requests of a cold ROW\_FORMAT=COMPRESSED page ([MDEV-27983](https://jira.mariadb.org/browse/MDEV-27983))

## Changelog

For a complete list of changes and bugfixes made in [MariaDB 10.6.10](mariadb-10610-release-notes.md), with links to detailed\
information on each push, see the [changelog](../changelogs/changelogs-mariadb-106-series/mariadb-10610-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.6.10](mariadb-10610-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-9-3-10-8-5-10-7-6-and-10-6-10-now-available/).

{% include "../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
