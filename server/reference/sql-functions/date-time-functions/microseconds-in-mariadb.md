# Microseconds in MariaDB

The [TIME](../../data-types/date-and-time-data-types/time.md), [DATETIME](../../data-types/date-and-time-data-types/datetime.md), and [TIMESTAMP](../../data-types/date-and-time-data-types/timestamp.md) types, along with\
the temporal functions, [CAST](../string-functions/cast.md) and [dynamic columns](../../sql-structure/nosql/dynamic-columns.md), support microseconds. The datetime precision of a column can be specified when creating the table with [CREATE TABLE](../../sql-statements/data-definition/create/create-table.md), for example:

```
CREATE TABLE example(
  col_microsec DATETIME(6),
  col_millisec TIME(3)
);
```

Generally, the precision can be specified for any `TIME`, `DATETIME`, or `TIMESTAMP` column, in parentheses, after the type name. The datetime precision specifies number of digits after the decimal dot and can be any integer number from 0 to 6. If no precision is specified it is assumed to be 0, for backward compatibility reasons.

A datetime precision can be specified wherever a type name is used. For example:

* when declaring arguments of stored routines.
* when specifying a return type of a stored function.
* when declaring variables.
* in a `CAST` function:

```
create function example(x datetime(5)) returns time(4)
begin
 declare y timestamp(6);
 return cast(x as time(2));
end;
```

`%f` is used as the formatting option for microseconds in the [STR\_TO\_DATE](str_to_date.md), [DATE\_FORMAT](date_format.md) and [FROM\_UNIXTIME](from_unixtime.md) functions, for example:

```
SELECT STR_TO_DATE('20200809 020917076','%Y%m%d %H%i%s%f');
+-----------------------------------------------------+
| STR_TO_DATE('20200809 020917076','%Y%m%d %H%i%s%f') |
+-----------------------------------------------------+
| 2020-08-09 02:09:17.076000                          |
+-----------------------------------------------------+
```

## Additional Information

* when comparing anything to a temporal value (`DATETIME`, `TIME`, `[DATE](../../../../data-types/date-and-time-data-types/date.md)`, or `TIMESTAMP`), both values are compared as temporal values, not as strings.
* The [INFORMATION\_SCHEMA.COLUMNS table](../../sql-statements/administrative-sql-statements/system-tables/information-schema/information-schema-tables/information-schema-columns-table.md) has a new column `DATETIME_PRECISION`
* [NOW()](now.md), [CURTIME()](curtime.md), [UTC\_TIMESTAMP()](utc_timestamp.md), [UTC\_TIME()](utc_time.md), [CURRENT\_TIME()](current_time.md), [CURRENT\_TIMESTAMP()](current_timestamp.md), [LOCALTIME()](localtime.md) and [LOCALTIMESTAMP()](localtimestamp.md) now accept datetime precision as an optional argument. For example:

```
SELECT CURTIME(4);
--> 10:11:12.3456
```

* [TIME\_TO\_SEC()](time_to_sec.md) and [UNIX\_TIMESTAMP()](unix_timestamp.md) preserve microseconds of the argument. These functions will return a [decimal](../../data-types/numeric-data-types/decimal.md) number if the result non-zero datetime precision and an [integer](../../data-types/numeric-data-types/int.md) otherwise (for backward compatibility).

```
SELECT TIME_TO_SEC('10:10:10.12345');
--> 36610.12345
```

* Current versions of this patch fix a bug in the following optimization: in\
  certain queries with `DISTINCT` MariaDB can ignore this clause if it can\
  prove that all result rows are unique anyway, for example, when a primary key\
  is compared with a constant. Sometimes this optimization was applied\
  incorrectly, though — for example, when comparing a\
  string with a date constant. This is now fixed.
* `DATE_ADD()` and `DATE_SUB()` functions can now take a `TIME`\
  expression as an argument (not just `DATETIME` as before).

```
SELECT TIME('10:10:10') + INTERVAL 100 MICROSECOND;
--> 10:10:10.000100
```

* The `event_time` field in the [mysql.general\_log](../../sql-statements/administrative-sql-statements/system-tables/the-mysql-database-tables/mysqlgeneral_log-table.md) table and the `start_time`, `query_time`, and `lock_time` fields in the [mysql.slow\_log](../../sql-statements/administrative-sql-statements/system-tables/the-mysql-database-tables/mysql-slow_log-table.md) table now store values with microsecond precision.
* This patch fixed a bug when comparing a temporal value using the `BETWEEN` operator and one of the operands is `NULL`.
* The old syntax `TIMESTAMP(N)`, where `N` is the display width, is no longer supported. It was deprecated in MySQL 4.1.0 (released on\
  2003-04-03).
* when a `DATETIME` value is compared to a `TIME` value, the latter is treated as a full datetime with a zero date part, similar to comparing `DATE` to a `DATETIME`, or to comparing `DECIMAL` numbers.\
  Earlier versions of MariaDB used to compare only the time part of both operands in such a case.
* In MariaDB, an extra column `[TIME_MS](../../administrative-sql-statements/system-tables/information-schema/time_ms-column-in-information_schemaprocesslist.md)` has been added to the `[INFORMATION_SCHEMA.PROCESSLIST](../../administrative-sql-statements/system-tables/information-schema/information-schema-tables/information-schema-processlist-table.md)` table, as well as to the output of `[SHOW FULL PROCESSLIST](../../administrative-sql-statements/show/show-processlist.md)`.

**Note:** When you convert a temporal value to a value with a smaller\
precision, it will be truncated, not rounded. This is done to guarantee that the date part is not\
changed. For example:

```
SELECT CAST('2009-12-31 23:59:59.998877' as DATETIME(3));
-> 2009-12-31 23:59:59.998
```

## MySQL 5.6 Microseconds

MySQL 5.6 introduced microseconds using a slightly different implementation to [MariaDB 5.3](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-3-series/changes-improvements-in-mariadb-5-3). Since [MariaDB 10.1](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/changes-improvements-in-mariadb-10-1), MariaDB has defaulted to the MySQL format, by means of the [--mysql56-temporal-format](../../../ha-and-performance/optimization-and-tuning/system-variables/server-system-variables.md#mysql56_temporal_format) variable. The MySQL version requires slightly [more storage](../../data-types/data-type-storage-requirements.md) but has some advantages in permitting the eventual support of negative dates, and in replication.

## See Also

* [Data Type Storage Requirements](../../data-types/data-type-storage-requirements.md)

<sub>_This page is licensed: CC BY-SA / Gnu FDL_</sub>

{% @marketo/form formId="4316" %}
