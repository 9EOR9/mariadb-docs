# MariaDB 5.2.1 Release Notes

The most recent release in the [MariaDB 5.2 series](changes-improvements-in-mariadb-5-2.md) is:[**MariaDB 5.2.14**](mariadb-5214-release-notes.md)

[Download](https://askmonty.org/wiki/MariaDB:Download:MariaDB_5.2.1-beta) | **Release Notes** | [Changelog](../../../changelogs/changelogs-mariadb-52-series/mariadb-521-changelog.md) |[Overview of 5.2](changes-improvements-in-mariadb-5-2.md)

**Release date:** 18 Jun 2010

### Release Notes

See the [MariaDB versus MySQL](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-2-series/broken-reference/README.md) page for a high-level overview of the differences between MariaDB and MySQL.

The [Changelog](../../../changelogs/changelogs-mariadb-52-series/mariadb-521-changelog.md) has a detailed list of the changes inluded in this release. For a description of this release see the [MariaDB 5.1 overview](../release-notes-mariadb-5-1-series/changes-improvements-in-mariadb-5-1.md).

#### OQGraph storage engine

This version of MariaDB includes the [OQGRAPH storage engine](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/oqgraph-storage-engine).

#### Extending CREATE TABLE

This version of MariaDB includes some bugfixes and small changes for [MWL#43](https://askmonty.org/worklog/?tid=43): _Extending CREATE TABLE_. See [Extending CREATE TABLE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/storage-engines-storage-engine-development/engine-defined-new-tablefieldindex-attributes) for more information on the new options this worklog gives to storage engine developers.

#### New command line option

This version of MariaDB supports a new command line option `--plugin-maturity=XXX`, where `XXX` can be one of`unknown`,`experimental`,`alpha`,`beta`,`gamma`,`stable`.

When used, MySQL will refuse to load plugins that have a maturity less than specified in this command line option.

#### Bugfixes

Several bugfixes and buildbot improvements have also been incorporated into\
this version of [MariaDB 5.2](changes-improvements-in-mariadb-5-2.md) including some that were discussed during the[2010 Storage Engine summit](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-2-series/broken-reference/README.md). See the[changelog](../../../changelogs/changelogs-mariadb-52-series/mariadb-521-changelog.md) for links to the details.

<sub>_This page is licensed: CC BY-SA / Gnu FDL_</sub>

{% @marketo/form formid="4316" formId="4316" %}
