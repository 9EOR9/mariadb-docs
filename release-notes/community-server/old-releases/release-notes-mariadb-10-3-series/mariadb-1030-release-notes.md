# MariaDB 10.3.0 Release Notes

The most recent release of [MariaDB 10.3](what-is-mariadb-103.md) is:[**MariaDB 10.3.39**](mariadb-10-3-39-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.3.39/)

[Download](https://downloads.mariadb.org/mariadb/10.3.0)[Release Notes](mariadb-1030-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-10-3-series/mariadb-1030-changelog.md)[Overview of 10.3](what-is-mariadb-103.md)

**Release date:** 16 Apr 2017

[MariaDB 10.3](what-is-mariadb-103.md) is the new development series of MariaDB. It is an evolution of[MariaDB 10.2](../release-notes-mariadb-10-2-series/what-is-mariadb-102.md) with several entirely new features not found anywhere else.

[MariaDB 10.3.0](mariadb-1030-release-notes.md) is an [_**Alpha**_](../../about/release-criteria.md) release.

**Do not use&#x20;**_**alpha**_**&#x20;releases in production!**

**For an overview of** [**MariaDB 10.3**](what-is-mariadb-103.md) **see the**[**What is MariaDB 10.3?**](what-is-mariadb-103.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

This is the first [alpha](../../about/release-criteria.md) release in the [MariaDB 10.3](what-is-mariadb-103.md)\
series. Alpha releases are useful for testing and planning, but should **not**\
be used in production.

Notable additions in this release include:

### Syntax / General Features

* [CREATE SEQUENCE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-structure/sequences/create-sequence) - [MDEV-10139](https://jira.mariadb.org/browse/MDEV-10139)
* [DROP SEQUENCE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-structure/sequences/drop-sequence)
* [INTERSECT](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-manipulation/selecting-data/joins-subqueries/intersect) and [EXCEPT](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-manipulation/selecting-data/joins-subqueries/except). These are both now [reserved words](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-structure/sql-language-structure/reserved-words) and can no longer be used as an [identifier](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-structure/sql-language-structure/identifier-names) without being quoted - [MDEV-10141](https://jira.mariadb.org/browse/MDEV-10141)
* [ROW](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/data-types/string-data-types/row) data type for [stored procedure](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/stored-routines/stored-procedures) variables - [MDEV-10914](https://jira.mariadb.org/browse/MDEV-10914), [MDEV-12007](https://jira.mariadb.org/browse/MDEV-12007), [MDEV-12291](https://jira.mariadb.org/browse/MDEV-12291)
* [TYPE OF and ROW TYPE OF](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/programmatic-compound-statements/declare-variable#type-of-row-type-of) anchored data types for [stored routine](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/stored-routines/stored-procedures) variables - [MDEV-12461](https://jira.mariadb.org/browse/MDEV-12461)
* [Cursors](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/programmatic-compound-statements/programmatic-compound-statements-cursors/cursor-overview) with parameters - [MDEV-12457](https://jira.mariadb.org/browse/MDEV-12457)
* [DDL Fast Fail - WAIT/NOWAIT](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/transactions/wait-and-nowait) - [MDEV-11379](https://jira.mariadb.org/browse/MDEV-11379), [MDEV-11388](https://jira.mariadb.org/browse/MDEV-11388)

### Idle Transactions

Connections with idle transactions can be automatically killed after a specified time period by means of the [idle\_transaction\_timeout](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#idle_transaction_timeout), [idle\_readonly\_transaction\_timeout](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#idle_readonly_transaction_timeout) and [idle\_readwrite\_transaction\_timeout](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#idle_readwrite_transaction_timeout) system variables.

### Compatibility

When running with [sql\_mode=ORACLE](https://mariadb.com/docs/release-notes/compatibility-and-differences/sql_modeoracle), the server now understands a subset of Oracle's PL/SQL language instead of the traditional MariaDB syntax for stored routines. This work is in progress. See [MDEV-10142](https://jira.mariadb.org/browse/MDEV-10142) and [MDEV-10764](https://jira.mariadb.org/browse/MDEV-10764)\
for the current status and subtasks. The 10.3.0 release includes:

* Providing compatibility for basic PL/SQL constructs - [MDEV-10411](https://jira.mariadb.org/browse/MDEV-10411)
* %TYPE in variable declarations - [MDEV-10577](https://jira.mariadb.org/browse/MDEV-10577)
* cursor%ROWTYPE in variable declarations - [MDEV-12011](https://jira.mariadb.org/browse/MDEV-12011)
* table%ROWTYPE in variable declarations - [MDEV-12133](https://jira.mariadb.org/browse/MDEV-12133)
* FOR loop statement - [MDEV-10580](https://jira.mariadb.org/browse/MDEV-10580)
* Implicit cursor FOR loop - [MDEV-12098](https://jira.mariadb.org/browse/MDEV-12098)
* Explicit cursor FOR LOOP - [MDEV-10581](https://jira.mariadb.org/browse/MDEV-10581)
* Cursors with parameters - [MDEV-10597](https://jira.mariadb.org/browse/MDEV-10597)
* Implicit cursor FOR LOOP for cursors with parameters - [MDEV-12314](https://jira.mariadb.org/browse/MDEV-12314)
* Explicit cursor attributes %ISOPEN, %ROWCOUNT, %FOUND, %NOTFOUND - [MDEV-10582](https://jira.mariadb.org/browse/MDEV-10582)
* SQL%ROWCOUNT - [MDEV-10583](https://jira.mariadb.org/browse/MDEV-10583)
* Variable declarations can go after cursor declarations - [MDEV-10598](https://jira.mariadb.org/browse/MDEV-10598)
* Predefined exceptions: TOO\_MANY\_ROWS, NO\_DATA\_FOUND, DUP\_VAL\_ON\_INDEX - [MDEV-10839](https://jira.mariadb.org/browse/MDEV-10839)
* RAISE statement for predefined exceptions - [MDEV-10840](https://jira.mariadb.org/browse/MDEV-10840)
* User defined exceptions - [MDEV-10587](https://jira.mariadb.org/browse/MDEV-10587)
* SP control functions SQLCODE, SQLERRM - [MDEV-10578](https://jira.mariadb.org/browse/MDEV-10578)
* Triggers: Understand :NEW.c1 and :OLD.c1 instead of NEW.c1 and OLD.c1 - [MDEV-10579](https://jira.mariadb.org/browse/MDEV-10579)
* Dynamic SQL placeholders - [MDEV-10801](https://jira.mariadb.org/browse/MDEV-10801)
* Allow VARCHAR and VARCHAR2 without length as a data type of routine parameters and in RETURN clause - [MDEV-10596](https://jira.mariadb.org/browse/MDEV-10596)
* CAST(..AS VARCHAR(N)) - [MDEV-11275](https://jira.mariadb.org/browse/MDEV-11275)
* Anonymous blocks - [MDEV-10655](https://jira.mariadb.org/browse/MDEV-10655)
* GOTO statement - [MDEV-10697](https://jira.mariadb.org/browse/MDEV-10697)
* Allow SELECT UNIQUE as a synonym for SELECT DISTINCT - [MDEV-12086](https://jira.mariadb.org/browse/MDEV-12086)
* Do not require BEGIN..END in multi-statement exception handlers in THEN clause - [MDEV-12088](https://jira.mariadb.org/browse/MDEV-12088)
* Understand optional routine name after the END keyword - [MDEV-12089](https://jira.mariadb.org/browse/MDEV-12089)
* Inside routines the CALL keywoard is optional - [MDEV-12107](https://jira.mariadb.org/browse/MDEV-12107)
* Make the concatenation operator ignore NULL arguments - [MDEV-11880](https://jira.mariadb.org/browse/MDEV-11880)
* make the CONCAT function ignore NULL arguments - [MDEV-12143](https://jira.mariadb.org/browse/MDEV-12143)
* TRUNCATE TABLE t1 \[ {DROP|REUSE} STORAGE ] - [MDEV-10588](https://jira.mariadb.org/browse/MDEV-10588)
* Providing compatibility for basic SQL data types - [MDEV-10343](https://jira.mariadb.org/browse/MDEV-10343)

### Data Type API

10.3 continues refactoring for the data type API started in 10.2, which will\
make it possible to have user data type plugins. This work is still in progress\
(see [MDEV-4912](https://jira.mariadb.org/browse/MDEV-4912) for the current status and subtasks). Most of the task in this\
category do not change the server behavior. Some tasks implemented in 10.3.0 do\
have a good visible effect:

* An expression of the [GEOMETRY](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-structure/geometry/geometry-types) data type is not allowed any more:
  * as an argument to functions ABS(), CEILING(), FLOOR(), ROUND(), SUM(), AVG(), VARIANCE(), CAST(AS..), as well as to the unary minus operator - [MDEV-12303](https://jira.mariadb.org/browse/MDEV-12303), [MDEV-12239](https://jira.mariadb.org/browse/MDEV-12239), [MDEV-12199](https://jira.mariadb.org/browse/MDEV-12199), [MDEV-12001](https://jira.mariadb.org/browse/MDEV-12001)
  * as an argument to hybrid functions such as CASE, COALESCE, IF which have other arguments of the numeric or temporal data types - [MDEV-11478](https://jira.mariadb.org/browse/MDEV-11478)
  * as an argument to comparison operators in combination with numeric and temporal data types - [MDEV-11692](https://jira.mariadb.org/browse/MDEV-11692)
  * as an argument to operators `+`, `-`, `*`, `/`, `MOD` - [MDEV-12238](https://jira.mariadb.org/browse/MDEV-12238)
* Wrong result for INSERT INTO t1 (datetime\_field) VALUES (hybrid\_function\_of\_TIME\_data\_type) - [MDEV-11331](https://jira.mariadb.org/browse/MDEV-11331)
* Expect "Impossible where condition" for WHERE timestamp\_field>=DATE\_ADD(TIMESTAMP'9999-01-01 00:00:00',INTERVAL 1000 YEAR) - [MDEV-11333](https://jira.mariadb.org/browse/MDEV-11333)
* SP variables of temporal data types do not replicate correctly - [MDEV-11815](https://jira.mariadb.org/browse/MDEV-11815)
* Incorrect result for (time\_expr BETWEEN timestamp\_exp1 AND timestamp\_expr2) - [MDEV-11482](https://jira.mariadb.org/browse/MDEV-11482)
* Wrong result for CASE on a mixture of signed and unsigned expressions - [MDEV-11554](https://jira.mariadb.org/browse/MDEV-11554)
* Wrong result for (int\_expr IN (mixture of signed and unsigned expressions)) - [MDEV-11497](https://jira.mariadb.org/browse/MDEV-11497)
* CASE with a mixture of TIME and DATETIME returns a wrong result - [MDEV-11555](https://jira.mariadb.org/browse/MDEV-11555)
* SP variables of the SET data type erroneously allow values with comma - [MDEV-11146](https://jira.mariadb.org/browse/MDEV-11146)
* mysql\_list\_field() returns wrong default values for VIEW - [MDEV-11672](https://jira.mariadb.org/browse/MDEV-11672)

### System Variables

The following new system variables have been added:

* [idle\_readonly\_transaction\_timeout](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#idle_readonly_transaction_timeout)
* [idle\_readwrite\_transaction\_timeout](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#idle_readwrite_transaction_timeout)
* [idle\_transaction\_timeout](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#idle_transaction_timeout)

### Status Variables

The following new status variables have been added:

* [Com\_create\_sequence](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-status-variables#com_create_sequence)
* [Com\_drop\_sequence](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-status-variables#com_drop_sequence)
* [Handler\_tmp\_delete](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-status-variables#handler_tmp_delete)

See the [What is MariaDB 10.3?](what-is-mariadb-103.md) page for an overview of [MariaDB 10.3](what-is-mariadb-103.md).

**Do not use&#x20;**_**alpha**_**&#x20;releases in production!**

For a complete list of changes made in [MariaDB 10.3.0](mariadb-1030-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-10-3-series/mariadb-1030-changelog.md).

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
