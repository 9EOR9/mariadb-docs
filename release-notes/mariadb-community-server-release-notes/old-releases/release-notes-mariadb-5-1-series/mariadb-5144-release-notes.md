# MariaDB 5.1.44 Release Notes

The most recent release in the [MariaDB 5.1 series](changes-improvements-in-mariadb-5-1.md) is:[**MariaDB 5.1.67**](mariadb-5167-release-notes.md)

[Download](https://askmonty.org/wiki/MariaDB:Download:MariaDB_5.1.44) | **Release Notes** | [Changelog](../../changelogs/changelogs-mariadb-51-series/mariadb-5144-changelog.md) |[Overview of 5.1](changes-improvements-in-mariadb-5-1.md)

**Release date:** 24 Mar 2010

See the [MariaDB 5.1.44 Changelog](../../changelogs/changelogs-mariadb-51-series/mariadb-5144-changelog.md) for a more detailed\
list of the changes in this release.

In most respects MariaDB will work exactly as MySQL: all commands, interfaces,\
libraries and APIs that exist in MySQL also exist in MariaDB.

In addition to the differences noted in previous[release notes](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/release-notes/README.md) and [changelogs](../../../connectors/odbc/changelogs/), the main differences\
between MariaDB and MySQL are:

## Includes MySQL 5.1.44

For [MariaDB 5.1.44](mariadb-5144-release-notes.md) we have merged in all of the upstream changes from MySQL\
5.1.43 and 5.1.44. The MySQL[5.1.43](https://dev.mysql.com/doc/refman/5.1/en/news-5-1-43.html) and[5.1.44](https://dev.mysql.com/doc/refman/5.1/en/news-5-1-44.html) release\
notes have details of what changes were made upstream by MySQL since 5.1.42.

## Performance Improvements

While preparing for [MariaDB 5.1.44](mariadb-5144-release-notes.md) we were made aware of a performance problem\
with Maria internal temporary tables, compared to MyISAM temporary tables\
(traditionally used by MySQL). The problem arose because the Maria storage\
engine has an 8K page size, compared to MyISAM's 1K. With this difference,\
compacted keys were slower in Maria as we had to search through more data to\
find a key in each page. After fixing it to use static length keys for most\
cases, the speed is now in most cases equal or better than MyISAM. This will be\
permanently fixed for all cases when we add a key directory to Maria storage\
engine pages.

## Fewer warnings and bugs

Like we did with our previous releases, various improvements were made in[MariaDB 5.1.44](mariadb-5144-release-notes.md) in our desire to fix warnings and eliminate bugs.

In [MariaDB 5.1.44](mariadb-5144-release-notes.md) these included a fix for [Bug #534626](https://bugs.launchpad.net/bugs/534626): "MyISAM table\
created in MariaDB not readable by MySQL". With this fix, tables created\
without `CHECKSUM=1` will be readable by MySQL. We have sent a\
patch to Oracle to fix the issue and allow MySQL to read all MyISAM tables with`CHECKSUM=1`.

Another improvement we made was to not take a mutex when accessing compiled-in\
plugin code. (The fewer mutexes you take, the better off you are.)

[MariaDB 5.1.44](mariadb-5144-release-notes.md) also includes fixes for the following bugs: [MySQL Bug #44987](https://bugs.mysql.com/bug.php?id=44987),[Bug #524025](https://bugs.launchpad.net/bugs/524025), [Bug #524679](https://bugs.launchpad.net/bugs/524679), [Bug #523593](https://bugs.launchpad.net/bugs/523593), [Bug #516148](https://bugs.launchpad.net/bugs/516148), [Bug #520243](https://bugs.launchpad.net/bugs/520243), and\
others. See the [5.1.44 Changelog](../../changelogs/changelogs-mariadb-51-series/mariadb-5144-changelog.md) for a detailed list\
of the various bugs and warnings that were fixed.

## Test Suite Improvements

We have continued to improve our test suite in [MariaDB 5.1.44](mariadb-5144-release-notes.md) to cover\
additional cases and to eliminate false positives. These included things like\
adding the ability to send extra commands to the server to setup the\
environment prior to starting tests, adding new benchmark tests, and fixing\
some tests that were failing because of time zone issues.

<sub>_This page is licensed: CC BY-SA / Gnu FDL_</sub>

{% @marketo/form formid="4316" formId="4316" %}
