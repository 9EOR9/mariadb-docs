# MariaDB 10.0.25 Release Notes

The most recent release in the [MariaDB 10.0](changes-improvements-in-mariadb-10-0.md) series is:[**MariaDB 10.0.38**](mariadb-10038-release-notes.md) [Download Now](https://downloads.mariadb.org/mariadb/10.0.38)

[Download](https://downloads.mariadb.org/mariadb/10.0.25)[Release Notes](mariadb-10025-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-100-series/mariadb-10025-changelog.md)[Overview of 10.0](changes-improvements-in-mariadb-10-0.md)

**Release date:** 30 Apr 2016

[MariaDB 10.0](changes-improvements-in-mariadb-10-0.md) is a previous stable series of MariaDB. It is an evolution of [MariaDB 5.5](../release-notes-mariadb-5-5-series/changes-improvements-in-mariadb-5-5.md) with several entirely new features not found anywhere else and with\
backported and reimplemented features from MySQL 5.6.

This is a [_**Stable**_](../../../mariadb-release-criteria.md) (_GA_) release.

**For an overview of** [**MariaDB 10.0**](changes-improvements-in-mariadb-10-0.md) **see the**[**What is MariaDB 10.0?**](changes-improvements-in-mariadb-10-0.md) **page.**

Thanks, and enjoy MariaDB!

## Notable changes

* [XtraDB](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/storage-engines/innodb) updated to XtraDB-5.6.29-76.2
* [Innodb](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/storage-engines/innodb) updated to InnoDB-5.6.30
* [Performance Schema](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/system-tables/performance-schema) updated to 5.6.30
* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2016-0655](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-0655)
  * [CVE-2016-0647](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-0647)
  * [CVE-2016-0648](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-0648)
  * [CVE-2016-0666](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-0666)
  * [CVE-2016-0643](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-0643)
  * [CVE-2016-3459](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-3459)
  * [CVE-2016-3452](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-3452)
  * [CVE-2016-5444](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-5444)

### Xenial and Sid Repositories

Our repositories for Debian "Sid" and the newly-released Ubuntu 16.04 "Xenial"\
use a new GPG signing key. As detailed in [MDEV-9781](https://jira.mariadb.org/browse/MDEV-9781), APT 1.2.7 (and later)\
prefers SHA2 GPG keys and now prints warnings when a repository is signed using\
a SHA1 key like our existing GPG key. We have created a new SHA2 key for use\
with these affected repositories.

Information about this key:

* The Key ID is: `C74CD1D8`
* The full fingerprint of the new key is: `177F 4010 FE56 CA33 3630 0305 F165 6F24 C74C D1D8`
* The key can be added using the following command:

```bash
sudo apt-key adv --recv-keys --keyserver hkp://keyserver.ubuntu.com:80 0xF1656F24C74CD1D8
```

The instructions in the[repository configuration tool](https://downloads.mariadb.org/mariadb/repositories/)\
for Ubuntu 16.04 "Xenial" and Debian "Sid" have been updated to reference this\
new key. Repositories for previous versions of Debian and Ubuntu still use the\
old key, so no changes are needed there.

### Windows

The Windows compiler used by MariaDB from this release drops Windows XP and Windows Server 2003 support.

## Changelog

For a complete list of changes made in [MariaDB 10.0.25](mariadb-10025-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-100-series/mariadb-10025-changelog.md).

{% include "https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/~/reusable/vX1KAy0t1XuYJaGsK28T/" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
