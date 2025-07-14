# MariaDB 10.11.13 Release Notes

<a href="https://mariadb.com/downloads/community" class="button primary">Download</a> <a href="mariadb-10.11.13-release-notes.md" class="button secondary">Release Notes</a> <a href="../changelogs/changelogs-mariadb-10-11-series/mariadb-10.11.13-changelog.md" class="button secondary">Changelog</a> <a href="what-is-mariadb-1011.md" class="button secondary">Overview of 10.11</a>

[_Alternate download from mariadb.org_](https://downloads.mariadb.org/mariadb/11.4.7/)

**Release date:** 22 May 2025

MariaDB 10.11 is a stable long term series of MariaDB, [maintained until](https://mariadb.org/about/#maintenance-policy) February 2028. It is an evolution of MariaDB 10.10 with several entirely new features.

MariaDB 10.11.13 is a _**Stable (GA)**_ release.

**For an overview of MariaDB 10.11 see theWhat is MariaDB 10.11? page.**

Thanks, and enjoy MariaDB!

### Notable Items

#### Storage Engines

[**InnoDB**](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/storage-engines/innodb/)

* Huge performance drop after update ([MDEV-36759](https://jira.mariadb.org/browse/MDEV-36759))
* InnoDB buffer pool reserves all assigned memory even with no/minimum load ([MDEV-36780](https://jira.mariadb.org/browse/MDEV-36780))
* Possible data loss in the unlikely scenario when GET GLOBAL innodb\_buffer\_pool\_size is shrinking the size of the buffer pool while the buffer pool contains ROW\_FORMAT=COMPRESSED tables that use a non-default KEY\_BLOCK\_SIZE that is equal to innodb\_page\_size/1024 ([MDEV-36781](https://jira.mariadb.org/browse/MDEV-36781))

#### General

* As per the MariaDB Deprecation Policy, this will be the last release of MariaDB 10.11 for Ubuntu 20.04 Focal

#### Security

* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/security):
  * CVE-\`-\`\`\`

### Changelog

For a complete list of changes and bugfixes made in MariaDB 10.11.13, with links to detailed\
information on each push, see the changelog.

### Contributors

For a full list of contributors to MariaDB 10.11.13, see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-11-4-5-10-11-11-10-6-21-and-10-5-28-now-available/).

{% include "../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
