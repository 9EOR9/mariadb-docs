# MariaDB 5.2.9 Release Notes

The most recent release in the [MariaDB 5.2 series](changes-improvements-in-mariadb-5-2.md) is:[**MariaDB 5.2.14**](mariadb-5214-release-notes.md)

[Download](https://downloads.askmonty.org/mariadb/5.2.9) |**Release Notes** |[Changelog](../../../changelogs/changelogs-mariadb-52-series/mariadb-529-changelog.md) |[Overview of 5.2](changes-improvements-in-mariadb-5-2.md)

**Release date:** 22 Sep 2011

[MariaDB 5.2.9](mariadb-529-release-notes.md) is a [Stable release](../../../mariadb-release-criteria.md).In general this means\
there are no known serious bugs and we believe the code is ready for general\
usage. A "stable" MariaDB release is equivalent to a MySQL "GA" release.

**For a detailed description of** [**MariaDB 5.2**](changes-improvements-in-mariadb-5-2.md) **see the** [**What is MariaDB 5.2**](changes-improvements-in-mariadb-5-2.md) **page.**

Compared to [MariaDB 5.2.8](mariadb-528-release-notes.md), [MariaDB 5.2.9](mariadb-529-release-notes.md) is a\
bug-fix release.

For a list of every change made in [MariaDB 5.2.9](mariadb-529-release-notes.md), with links to detailed\
information on each push, see the[MariaDB 5.2.9 Changelog](../../../changelogs/changelogs-mariadb-52-series/mariadb-529-changelog.md).

In most respects [MariaDB](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/mariadb/README.md) will work exactly as MySQL: all commands,\
interfaces, libraries and APIs that exist in MySQL also exist in MariaDB.

Be notified of new releases automatically by adding the[releases rss feed](https://montyprogram.com/news/feed/mariadb_releases/) to\
your favorite feed reader or by [subscribing](https://mariadb.org) to the\
announce 'at' mariadb.org announcement list (this is a low traffic,\
announce-only list).

MariaDB may already be included in your favorite OS distribution. More\
information can be found on the[Distributions which Include MariaDB](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/readme-1)\
page.

#### 2 Nov 2011 Update:

We've updated the Ubuntu packages for [MariaDB 5.2.9](mariadb-529-release-notes.md). Apart from now including\
packages for Ubuntu 11.10 "Oneiric" the only other change is to remove the\
default apparmor profile.

Ubuntu 11.10 "Oneiric" introduced some significant[directory changes](https://askubuntu.com/questions/57297/why-has-var-run-been-migrated-to-run).\
Rather than try to keep our apparmor profile in sync with Ubuntu and risk a\
future breakage when they decide to change something else, we have decided to\
include an empty profile in our packages. If you have customized your`/etc/apparmor.d/usr.sbin.mysqld` file you will be given the option to keep\
or remove it during the upgrade. If you haven't customized the default profile,\
the profile will be removed.
