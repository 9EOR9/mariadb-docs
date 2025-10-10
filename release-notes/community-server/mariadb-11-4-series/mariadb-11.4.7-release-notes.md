# MariaDB 11.4.7 Release Notes

{% include "../../.gitbook/includes/latest-11-4.md" %}

<a href="https://mariadb.com/downloads/community" class="button primary">Download</a> <a href="mariadb-11.4.7-release-notes.md" class="button secondary">Release Notes</a> <a href="../changelogs/changelogs-mariadb-11-4-series/mariadb-11.4.7-changelog.md" class="button secondary">Changelog</a> <a href="what-is-mariadb-114.md" class="button secondary">Overview of 11.4</a>

[_Alternate download from mariadb.org_](https://downloads.mariadb.org/mariadb/11.4.7/)

**Release date:** 22 May 2025

MariaDB 11.4 is the current long-term series of MariaDB and will be maintained until May 2029. It is an evolution of MariaDB 11.3 with several entirely new features.

MariaDB 11.4.7 is a _**Stable (GA)**_ release.

**For an overview of MariaDB 11.4 see the** [**What is MariaDB 11.4?**](what-is-mariadb-114.md) **page.**

Thanks, and enjoy MariaDB!

### Notable Items

#### Storage Engines

[**InnoDB**](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb)

* Huge performance drop after update ([MDEV-36759](https://jira.mariadb.org/browse/MDEV-36759))
* InnoDB buffer pool reserves all assigned memory even with no/minimum load ([MDEV-36780](https://jira.mariadb.org/browse/MDEV-36780))
* Possible data loss in the unlikely scenario when GET GLOBAL innodb\_buffer\_pool\_size is shrinking the size of the buffer pool while the buffer pool contains ROW\_FORMAT=COMPRESSED tables that use a non-default KEY\_BLOCK\_SIZE that is equal to innodb\_page\_size/1024 ([MDEV-36781](https://jira.mariadb.org/browse/MDEV-36781))

#### Optimizer

* Optimizer trace should show the index name in the block chosen\_access\_method ([MDEV-21510](https://jira.mariadb.org/browse/MDEV-21510))

#### Server

* Make HOSTNAME a cmake configure variable ([MDEV-35850](https://jira.mariadb.org/browse/MDEV-35850))

#### General

* As per the [MariaDB Deprecation Policy](../about/platform-deprecation-policy.md), this will be the last release of [MariaDB 10.6](../mariadb-10-6-series/what-is-mariadb-106.md) for Ubuntu 20.04 LTS 'focal'

### Changelog

For a complete list of changes made in MariaDB 11.4.7, with links to detailed\
information on each push, see the [changelog](../changelogs/changelogs-mariadb-11-4-series/mariadb-11.4.7-changelog.md).

{% include "../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
