# MariaDB 10.2.43 Release Notes

The most recent release of [MariaDB 10.2](what-is-mariadb-102.md) is:[**MariaDB 10.2.44**](mariadb-10244-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.2.44/)

[Download 10.2.43](https://downloads.mariadb.org/mariadb/10.2.43/)[Release Notes](mariadb-10243-release-notes.md)[Changelog](../../../changelogs/changelogs-mariadb-102-series/mariadb-10243-changelog.md)[Overview of 10.2](what-is-mariadb-102.md)

**Release date:** 12 Feb 2022

[MariaDB 10.2](what-is-mariadb-102.md) is a previous stable series of MariaDB. It is an evolution\
of [MariaDB 10.1](../release-notes-mariadb-10-1-series/changes-improvements-in-mariadb-10-1.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL 5.6 and 5.7.

[MariaDB 10.2.43](mariadb-10243-release-notes.md) is a [_**Stable (GA)**_](../../../mariadb-release-criteria.md) release.

**For an overview of** [**MariaDB 10.2**](what-is-mariadb-102.md) **see the**[**What is MariaDB 10.2?**](what-is-mariadb-102.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Items

* This release fixes a blocking problem with the [MariaDB 10.2.42](mariadb-10242-release-notes.md) release when manually running [mariadb-upgrade](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/legacy-clients-and-utilities/mysql_upgrade). ([MDEV-27789](https://jira.mariadb.org/browse/MDEV-27789))
* See [MariaDB 10.2.42](mariadb-10242-release-notes.md) for other changes since the previous release.

### Security

* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2021-46665](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-46665)
  * [CVE-2021-46664](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-46664)
  * [CVE-2021-46661](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-46661)
  * [CVE-2021-46668](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-46668)
  * [CVE-2021-46663](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-46663)

Upgrading from 10.2 versions earlier than 10.2.17 is **highly recommended**\
for all [**Galera**](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/galera/README.md) users due to bug [MDEV-12837](https://jira.mariadb.org/browse/MDEV-12837) which caused serious stability\
issues with earlier versions. See the bug issue page for more information.\
When upgrading from [MariaDB 10.2.16](mariadb-10216-release-notes.md) or earlier to [MariaDB 10.2.17](mariadb-10217-release-notes.md) or higher,\
running [mysql\_upgrade](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/legacy-clients-and-utilities/mysql_upgrade) is **required** due to changes introduced in [MDEV-14637](https://jira.mariadb.org/browse/MDEV-14637).

## Changelog

For a complete list of changes made in [MariaDB 10.2.43](mariadb-10243-release-notes.md) with links to detailed\
information on each push, see the [changelog](../../../changelogs/changelogs-mariadb-102-series/mariadb-10243-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.2.43](mariadb-10243-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-8-2-rc-and-mariadb-10-7-3-10-6-7-10-5-15-10-4-24-10-3-34-and-10-2-43-now-available/).

Be notified of new MariaDB Server releases automatically by [subscribing](https://lists.mariadb.org/postorius/lists/announce.lists.mariadb.org/) to the MariaDB Foundation community announce 'at' lists.mariadb.org announcement list (this is a low traffic, announce-only list). MariaDB plc customers will be notified for all new releases, security issues and critical bug fixes for all MariaDB plc products thanks to the Notification Services.

MariaDB may already be included in your favorite OS distribution. More\
information can be found on the[Distributions which Include MariaDB](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/distributions-including-mariadb)\
page.

{% @marketo/form formid="4316" formId="4316" %}
