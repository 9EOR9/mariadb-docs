# MariaDB 11.8.1 Release Notes

{% include "../../.gitbook/includes/latest-11-8.md" %}

<a href="https://downloads.mariadb.org/mariadb/11.8.1/" class="button primary">Download</a> <a href="mariadb-11-8-1-release-notes.md" class="button secondary">Release Notes</a> <a href="../changelogs/changelogs-mariadb-11-8-series/mariadb-11-8-1-changelog.md" class="button secondary">Changelog</a> <a href="what-is-mariadb-118.md" class="button secondary">Overview of 11.8</a>

**Release date:** 13 Feb 2025

{% include "../../.gitbook/includes/non-stable.md" %}

[MariaDB 11.8](what-is-mariadb-118.md) is a current long-term development series of MariaDB. It is an evolution of [MariaDB 11.7](../old-releases/mariadb-11-7-rolling-releases/what-is-mariadb-117.md) with several entirely new features.

[MariaDB 11.8.1](mariadb-11-8-1-release-notes.md) is a [_**Release Candidate (RC)**_](../about/release-criteria.md) release.

**For an overview of** [**MariaDB 11.8**](what-is-mariadb-118.md) **see the** [**What is MariaDB 11.8?**](what-is-mariadb-118.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Items

### Storage Engines

#### [InnoDB](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb)

* Fix assertion failure on cascading foreign key update of table with vcol index in parent ([MDEV-29182](https://jira.mariadb.org/browse/MDEV-29182))

### Optimizer

* Fix possibly wrong result using a degenerated subquery (SELECT ) with window function ([MDEV-35869](https://jira.mariadb.org/browse/MDEV-35869))
* Conditions with SP local variables are now pushed into derived table. Previous behaviour caused slow performance and table scans instead of using the pushed down condition ([MDEV-35910](https://jira.mariadb.org/browse/MDEV-35910))
* Support ORDER BY and LIMIT for multi-table DELETE, index hints for single-table DELETE. ([MDEV-30469](https://jira.mariadb.org/browse/MDEV-30469))
* Optimizer can now use indexed virtual columns in WHERE/ON clauses for improved query performance. ([MDEV-35616](https://jira.mariadb.org/browse/MDEV-35616))
* Make SUBSTR(col, 1, n) = const\_str sargable ([MDEV-34911](https://jira.mariadb.org/browse/MDEV-34911))

### PL/SQL

* It is now possible to define default values (or expressions) for parameters to stored procedures, stored functions and UDFs ([MDEV-10862](https://jira.mariadb.org/browse/MDEV-10862))
* New DECLARE TYPE type\_name IS RECORD (..) with scalar members in stored routines ([MDEV-34317](https://jira.mariadb.org/browse/MDEV-34317))
* It was not possible to use a package body variable as a fetch target, instead error "Undeclared variable" was returned. ([MDEV-36047](https://jira.mariadb.org/browse/MDEV-36047))

### [Triggers](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/triggers-events/triggers)

* Fix trigger created with "[CREATE TRIGGER `table1_after_insert` AFTER INSERT](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/triggers-events/triggers/create-trigger)" which is adding rows to another table using "FOR EACH ROW insert into table2(`id`, `name`) values (NEW.`id`, NEW.`name`);" that did not work correctly when if bulk inserts are used by the application. Only the first row of the bulk insert would be added to the table ([MDEV-34958](https://jira.mariadb.org/browse/MDEV-34958))
* A Trigger definition can now include column names for specifying the columns for which a trigger should be called ([MDEV-34551](https://jira.mariadb.org/browse/MDEV-34551))
* Triggers can now use SIGNAL SQLSTATE '02TRG' to skip row operations (insert, update, delete) in BEFORE triggers, affecting data modification. ([MDEV-34724](https://jira.mariadb.org/browse/MDEV-34724))

### [Data types](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/data-types)

* Fix possible hang or crash where zero offset applied to null pointer ([MDEV-35864](https://jira.mariadb.org/browse/MDEV-35864))
* Comparison of UUID v1 and V6 could return incorrect results ([MDEV-35468](https://jira.mariadb.org/browse/MDEV-35468))

### [Character Sets](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/data-types/string-data-types/character-sets)

* Fix possible runtime error caused by XA RECOVER applying a zero offset to a null pointer ([MDEV-35549](https://jira.mariadb.org/browse/MDEV-35549))
* Fix issue where functions in default values in tables with certain character sets could break SHOW CREATE and mariadb-dump ([MDEV-29968](https://jira.mariadb.org/browse/MDEV-29968))
* OS character sets "utf8" and "utf-8" now map to MariaDB character set "utf8mb4" for full UTF-8 support. ([MDEV-22217](https://jira.mariadb.org/browse/MDEV-22217))

### [Stored routines](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/stored-routines)

* Calling a stored routine that executes a join on three or more tables and referencing not-existent column name in the USING clause could previously result in a crash on its second invocation. ([MDEV-24935](https://jira.mariadb.org/browse/MDEV-24935))

### Scripts & Clients

* When using [mariadb-import](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/backup-restore-and-import-clients/mariadb-import) with --innodb-optimize-keys, secondary index creation is delayed until after data load, potentially improving load speed. ([MDEV-34740](https://jira.mariadb.org/browse/MDEV-34740))

### Security

* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * CVE-\`-\`\`\`

## Changelog

For a complete list of changes made in [MariaDB 11.8.1](mariadb-11-8-1-release-notes.md), with links to detailed\
information on each push, see the [changelog](../changelogs/changelogs-mariadb-11-8-series/mariadb-11-8-1-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 11.8.1](mariadb-11-8-1-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-11-7-2-and-mariadb-11-8-1-now-available/).

{% include "../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
