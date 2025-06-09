# MariaDB 10.0.24 Release Notes

The most recent release in the [MariaDB 10.0](changes-improvements-in-mariadb-10-0.md) series is:[**MariaDB 10.0.38**](mariadb-10038-release-notes.md) [Download Now](https://downloads.mariadb.org/mariadb/10.0.38)

[Download](https://downloads.mariadb.org/mariadb/10.0.24)[Release Notes](mariadb-10024-release-notes.md)[Changelog](../../../changelogs/changelogs-mariadb-100-series/mariadb-10024-changelog.md)[Overview of 10.0](changes-improvements-in-mariadb-10-0.md)

**Release date:** 19 Feb 2016

[MariaDB 10.0](changes-improvements-in-mariadb-10-0.md) is a previous stable series of MariaDB. It is an evolution of [MariaDB 5.5](../release-notes-mariadb-5-5-series/changes-improvements-in-mariadb-5-5.md) with several entirely new features not found anywhere else and with\
backported and reimplemented features from MySQL 5.6.

This is a [_**Stable**_](../../../mariadb-release-criteria.md) (_GA_) release.

**For an overview of** [**MariaDB 10.0**](changes-improvements-in-mariadb-10-0.md) **see the**[**What is MariaDB 10.0?**](changes-improvements-in-mariadb-10-0.md) **page.**

Thanks, and enjoy MariaDB!

## Notable changes

* [XtraDB](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/storage-engines/innodb) updated to XtraDB-5.6.28-76.1
* [Innodb](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/storage-engines/innodb) updated to InnoDB-5.6.29
* [Performance Schema](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/system-tables/performance-schema) updated to 5.6.29
* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2016-0668](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-0668)
  * [CVE-2016-0640](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-0640)
  * [CVE-2016-0644](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-0644)
  * [CVE-2016-0646](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-0646)
  * [CVE-2016-0649](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-0649)
  * [CVE-2016-0650](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-0650)
  * [CVE-2016-0641](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-0641)

### Deprecated Distributions

As per the [MariaDB Deprecation Policy](../../../mariadb-platform-deprecation-policy.md), this will be the\
last release of [MariaDB 10.0](changes-improvements-in-mariadb-10-0.md) for Ubuntu 15.04 "Vivid", and Debian 6 "Squeeze".

### Added Distributions

A repository for the newly-released Ubuntu 16.04 "xenial" has been added.\
Currently the repository is using packages built on Ubuntu 15.10 "wily", but in\
the next release they will be built on xenial builders.

* [MDEV-9781](https://jira.mariadb.org/browse/MDEV-9781) - APT 1.2.7 (and later) prefers SHA2 GPG keys and now prints warnings when a repository is signed using a SHA1 key. We have created a new SHA2 key for use with our Ubuntu 16.04 "xenial" repository.
  * The Key ID is: `C74CD1D8`
  * The full fingerprint of the new key is: `177F 4010 FE56 CA33 3630 0305 F165 6F24 C74C D1D8`
  * The key can be added using the following command:

```bash
sudo apt-key adv --recv-keys --keyserver hkp://keyserver.ubuntu.com:80 0xF1656F24C74CD1D8
```

The instructions in the[repository configuration tool](https://downloads.mariadb.org/mariadb/repositories/)\
for Ubuntu 16.04 "xenial" have been updated to refer to this new key.\
Repositories for previous versions of Ubuntu will continue to use the old key.

## Changelog

For a complete list of changes made in [MariaDB 10.0.24](mariadb-10024-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../../changelogs/changelogs-mariadb-100-series/mariadb-10024-changelog.md).

Be notified of new MariaDB Server releases automatically by [subscribing](https://lists.mariadb.org/postorius/lists/announce.lists.mariadb.org/) to the MariaDB Foundation community announce 'at' lists.mariadb.org announcement list (this is a low traffic, announce-only list). MariaDB plc customers will be notified for all new releases, security issues and critical bug fixes for all MariaDB plc products thanks to the Notification Services.

MariaDB may already be included in your favorite OS distribution. More\
information can be found on the [Distributions which Include MariaDB](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/readme-1)\
page.

{% @marketo/form formid="4316" formId="4316" %}
