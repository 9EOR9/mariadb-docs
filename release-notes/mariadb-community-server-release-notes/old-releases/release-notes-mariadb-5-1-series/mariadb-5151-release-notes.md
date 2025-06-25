# MariaDB 5.1.51 Release Notes

The most recent release in the [MariaDB 5.1 series](changes-improvements-in-mariadb-5-1.md) is:[**MariaDB 5.1.67**](mariadb-5167-release-notes.md)

[Download](https://askmonty.org/wiki/MariaDB:Download:MariaDB_5.1.51) | **Release Notes** | [Changelog](../../changelogs/changelogs-mariadb-51-series/mariadb-5151-changelog.md) |[Overview of 5.1](changes-improvements-in-mariadb-5-1.md)

**Release date:** 19 Nov 2010

For a list of every change made in this release, see the[Changelog](../../changelogs/changelogs-mariadb-51-series/mariadb-5151-changelog.md). For a description of this release see the [MariaDB 5.1 overview](changes-improvements-in-mariadb-5-1.md).

In most respects [MariaDB](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/mariadb/README.md) will work exactly as MySQL: all commands,\
interfaces, libraries and APIs that exist in MySQL also exist in MariaDB.

In addition to the differences noted in previous[release notes](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/release-notes/README.md) and[changelogs](../../../connectors/odbc/changelogs/), the main\
differences between MariaDB and MySQL are:

## Includes MySQL 5.1.51

For [MariaDB 5.1.51](mariadb-5151-release-notes.md) we have merged in all of the upstream changes from MySQL\
5.1.51. The MySQL[5.1.51](https://dev.mysql.com/doc/refman/5.1/en/news-5-1-51.html) release\
notes have details of what changes were made upstream by MySQL since 5.1.50.

## Includes [XtraDB](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb) 5.1.51-12

We have included XtraDB from Percona-server-5.1.51-12 in this version of MariaDB.

## Shared Library - libmysqld.so

In addition to the static library, libmysqld.a, this version of MariaDB also includes a corresponding shared library, libmysqld.so. This is needed by applications such as Amarok, which use the embedded server from within dynamically loaded plugins or libraries. Details of this are found in [MWL#74](https://askmonty.org/worklog/?tid=74), and this patch fixes [MySQL Bug #39288](https://bugs.mysql.com/bug.php?id=39288).

## Bug Fixes

Like [previous releases](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/release-notes/README.md), [MariaDB 5.1.51](mariadb-5151-release-notes.md) includes several bug fixes and other improvements. Specific bugs fixed in [MariaDB 5.1.51](mariadb-5151-release-notes.md) include:

* [MySQL Bug #57491](https://bugs.mysql.com/bug.php?id=57491) thd->main\_da.is\_ok() assert in embedded
* [MySQL Bug #26447](https://bugs.mysql.com/bug.php?id=26447) "ALTER TABLE .. ORDER" does not work with InnoDB and auto\_increment keys
* [MySQL Bug #35850](https://bugs.mysql.com/bug.php?id=35850) Performance regression in 5.1.23/5.1.24
* [MySQL Bug #39653](https://bugs.mysql.com/bug.php?id=39653) find\_shortest\_key in sql\_select.cc does not consider clustered primary keys
* [MySQL Bug #55656](https://bugs.mysql.com/bug.php?id=55656) mysqldump can be slower after [MySQL Bug #39653](https://bugs.mysql.com/bug.php?id=39653) fix
* [MySQL Bug #43152](https://bugs.mysql.com/bug.php?id=43152) Assertion \`bitmap\_is\_set\_all(\&table->s->all\_set)' failed in handler::ha\_reset
* [MySQL Bug #44797](https://bugs.mysql.com/bug.php?id=44797) plugins w/o command-line options have no disabling option in --help
* [MySQL Bug #53161](https://bugs.mysql.com/bug.php?id=53161) Left join optimized into join leads to incorrect results
* [MySQL Bug #56862](https://bugs.mysql.com/bug.php?id=56862) Execution of a query that uses index merge returns a wrong result
* [MySQL Bug #49600](https://bugs.mysql.com/bug.php?id=49600) Server incorrectly processing RIGHT JOIN with constant WHERE clause and no index
* [MySQL Bug #49322](https://bugs.mysql.com/bug.php?id=49322) Server is adding extra NULL row on processing a WHERE clause
* [MySQL Bug #57024](https://bugs.mysql.com/bug.php?id=57024) Serious performance issue with an outer join
* [Bug #618608](https://bugs.launchpad.net/bugs/618608) FederatedX is not the default on Windows
* [Bug #608369](https://bugs.launchpad.net/bugs/608369) (M)Aria engine recovery failure: "Page: 1 Found wrong page type 0' on CHECK TABLE EXTENDED
* [Bug #640419](https://bugs.launchpad.net/bugs/640419) Wrong result with sort\_union/index\_merge in maria-5.1 and a large table
* [Bug #634943](https://bugs.launchpad.net/bugs/634943) "marked as crashed", "zerofilling" and "wrong data in bitmap" when recovering Aria tables
* [Bug #605798](https://bugs.launchpad.net/bugs/605798) RQG: Table corruption after Maria engine recovery - "Wrong data in bitmap"
* [Bug #618558](https://bugs.launchpad.net/bugs/618558) Assertion data\_length < ((block\_size) \*3 / 4) in write\_block\_record() at ma\_blockrec.c:3483 with --maria-block-size=1K
* [Bug #634955](https://bugs.launchpad.net/bugs/634955) ma\_blockrec.c:3932: \_ma\_update\_at\_original\_place: Assertion \`blocks->count > 1 || ((new\_row->total\_length) > (share->base.min\_block\_length) ? (new\_row->total\_length) : (share->base.min\_block\_length)) <= length\_on\_head\_page' on Aria recovery
* [Bug #643463](https://bugs.launchpad.net/bugs/643463) slow XtraDB shutdown due to 10 second sleep in purge thread

<sub>_This page is licensed: CC BY-SA / Gnu FDL_</sub>

{% @marketo/form formid="4316" formId="4316" %}
