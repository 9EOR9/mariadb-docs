# MariaDB 5.1.50 Release Notes

The most recent release in the [MariaDB 5.1 series](changes-improvements-in-mariadb-5-1.md) is:[**MariaDB 5.1.67**](mariadb-5167-release-notes.md)

[Download](https://askmonty.org/wiki/MariaDB:Download:MariaDB_5.1.50) | **Release Notes** | [Changelog](../../../changelogs/changelogs-mariadb-51-series/mariadb-5150-changelog.md) |[Overview of 5.1](changes-improvements-in-mariadb-5-1.md)

**Release date:** 09 Sep 2010

For a list of every change made in this release, see the[Changelog](../../../changelogs/changelogs-mariadb-51-series/mariadb-5150-changelog.md). For a description of this release see the [MariaDB 5.1 overview](changes-improvements-in-mariadb-5-1.md).

In most respects [MariaDB](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/mariadb/README.md) will work exactly as MySQL: all commands,\
interfaces, libraries and APIs that exist in MySQL also exist in MariaDB.

In addition to the differences noted in previous[release notes](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/release-notes/README.md) and[changelogs](../../../connectors/odbc/changelogs/), the main\
differences between MariaDB and MySQL are:

## Includes MySQL 5.1.50

For [MariaDB 5.1.50](mariadb-5150-release-notes.md) we have merged in all of the upstream changes from MySQL\
5.1.49. The MySQL[5.1.50](https://dev.mysql.com/doc/refman/5.1/en/news-5-1-50.html) release\
notes have details of what changes were made upstream by MySQL since 5.1.49.

## Includes [XtraDB](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb) 5.1.49-12

We have included XtraDB from Percona Server 5.1.49-12 in this version of\
MariaDB.

## Bug Fixes

Like [previous releases](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/release-notes/README.md), [MariaDB 5.1.50](mariadb-5150-release-notes.md) includes several bug fixes and other improvements. Specific bugs fixed in [MariaDB 5.1.50](mariadb-5150-release-notes.md) include:

* [MySQL Bug #32426](https://bugs.mysql.com/bug.php?id=32426) & [Bug #571200](https://bugs.launchpad.net/bugs/571200) FederatedX corrupt ORDER BY with TEXT
* [Bug #616253](https://bugs.launchpad.net/bugs/616253) Crash in \_ma\_bitmap\_set\_full\_page\_bits on Aria recovery
* [Bug #612894](https://bugs.launchpad.net/bugs/612894) Some aggregate functions (such as MIN MAX) work incorrectly in subqueries after getting NULL value
* [Bug #605798](https://bugs.launchpad.net/bugs/605798) RQG: Table corruption after Maria engine recovery - "Wrong data in bitmap"
* [Bug #613418](https://bugs.launchpad.net/bugs/613418) (M)aria recovery failure: ma\_key\_recover.c:981: \_ma\_apply\_redo\_index: Assertion \`check\_page\_length == page\_length' failed

<sub>_This page is licensed: CC BY-SA / Gnu FDL_</sub>

{% @marketo/form formid="4316" formId="4316" %}
