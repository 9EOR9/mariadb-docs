# MariaDB 5.5.33a Release Notes

The most recent release in the [MariaDB 5.5](changes-improvements-in-mariadb-5-5.md) series is:[**MariaDB 5.5.68**](mariadb-5568-release-notes.md) [Download Now](https://downloads.mariadb.org/mariadb/5.5.68/)

[Download](https://downloads.mariadb.org/mariadb/5.5.33a) |**Release Notes** |[Changelog](../../changelogs/changelogs-mariadb-55-series/mariadb-5533a-changelog.md) |[Overview of 5.5](changes-improvements-in-mariadb-5-5.md)

**Release date:** 20 Sep 2013

This is a [_**Stable**_](../../../mariadb-release-criteria.md) _**(GA)**_ release. In general this\
means that there are no known serious bugs, except for those marked as feature\
requests, that no bugs were fixed since last release that caused a notable code\
changes, and that we believe the code is ready for general usage (based on bug\
inflow).

**For a description of** [**MariaDB 5.5**](changes-improvements-in-mariadb-5-5.md) **see the**[**What is MariaDB 5.5?**](changes-improvements-in-mariadb-5-5.md) **page.**

For a list of changes made in this release, with links to detailed\
information on each push, see the[MariaDB 5.5.33 Changelog](../../changelogs/changelogs-mariadb-55-series/mariadb-5533-changelog.md).

In most respects [MariaDB](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/mariadb/README.md) will work exactly as MySQL: all commands,\
interfaces, libraries and APIs that exist in MySQL also exist in MariaDB.

## Bug Fixes

This is a special bug-fix release for some packaging and other errors in the\
recent [MariaDB 5.5.33](mariadb-5533-release-notes.md) release.

Specific bugs fixed in this release include:

* [MDEV-5035](https://jira.mariadb.org/browse/MDEV-5035) Debian package conflict libmariadbclient18 vs. mariadb-server-5.3
* [MDEV-5026](https://jira.mariadb.org/browse/MDEV-5026) Cannot use system jemalloc
* [MDEV-5015](https://jira.mariadb.org/browse/MDEV-5015) Wrong result with an aggregate function, index and impossible condition inside OR
* [MDEV-5029](https://jira.mariadb.org/browse/MDEV-5029) Crash in [MariaDB 5.5.33](mariadb-5533-release-notes.md) with inconsistent .frm from older MariaDB release

Full details on these and other fixes are available in the [changelog](../../changelogs/changelogs-mariadb-55-series/mariadb-5533a-changelog.md).

## Debian and Ubuntu packaging fixes

There were issues with the `.deb` packages in the 5.5.33 release. Before updating with `apt-get`, check to make sure the mirror you are using has version **5.5.33a** _(not 5.5.33)_. To check, run the following commands:

```bash
sudo apt-get update
apt-cache show mariadb-server | grep Version
```

The output will look similar to this (raring will be replaced with whatever version of Ubuntu or Debian you are using):

```bash
user@host:~$
 apt-cache show mariadb-server | grep Version

Version: 5.5.33a+maria-1~raring
```

We've created a page for those who ran into the packaging bugs present in 5.5.33. It has instructions on how to get MariaDB back into a state where it can be upgraded successfully.

* [MariaDB 5.5.33 Debian and Ubuntu Installation Issues](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/install-and-upgrade-mariadb/installing-mariadb/troubleshooting-installation-issues/installation-issues-on-debian-and-ubuntu/mariadb-5533-debian-and-ubuntu-installation-issues)

Thanks, and enjoy MariaDB!

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
