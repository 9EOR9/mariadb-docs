
# TIME

## Syntax


```
TIME [(<microsecond precision>)]
```


## Description


A time. The range is `<code>'-838:59:59.999999'</code>` to `<code>'838:59:59.999999'</code>`. [Microsecond precision](../../sql-statements-and-structure/sql-statements/built-in-functions/date-time-functions/microseconds-in-mariadb.md) can be from 0-6; if not specified 0 is used.


MariaDB displays `<code>TIME</code>` values in `<code>'HH:MM:SS.ssssss'</code>` format, but allows assignment of times in looser formats, including 'D HH:MM:SS', 'HH:MM:SS', 'HH:MM', 'D HH:MM', 'D HH', 'SS', or 'HHMMSS', as well as permitting dropping of any leading zeros when a delimiter is provided, for example '3:9:10'. For details, see [date and time literals](../../sql-statements-and-structure/sql-language-structure/date-and-time-literals.md).


The [--mysql56-temporal-format](../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/server-system-variables.md#mysql56_temporal_format) option, on by default, allows MariaDB to store TIMEs using the same low-level format MySQL 5.6 uses.


### Internal Format


A new temporal format was introduced from MySQL 5.6 that alters how the `<code>TIME</code>`, `<code>DATETIME</code>` and `<code>TIMESTAMP</code>` columns operate at lower levels. These changes allow these temporal data types to have fractional parts and negative values. You can disable this feature using the [mysql56_temporal_format](../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/server-system-variables.md#mysql56_temporal_format) system variable.


Tables that include `<code>TIMESTAMP</code>` values that were created on an older version of MariaDB or that were created while the [mysql56_temporal_format](../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/server-system-variables.md#mysql56_temporal_format) system variable was disabled continue to store data using the older data type format.


In order to update table columns from the older format to the newer format, execute an [ALTER TABLE... MODIFY COLUMN](../../sql-statements-and-structure/sql-statements/data-definition/alter/alter-tablespace.md#modify-column) statement that changes the column to the *same* data type. This change may be needed if you want to export the table's tablespace and import it onto a server that has `<code>mysql56_temporal_format=ON</code>` set (see [MDEV-15225](https://jira.mariadb.org/browse/MDEV-15225)).


For instance, if you have a `<code>TIME</code>` column in your table:


```
SHOW VARIABLES LIKE 'mysql56_temporal_format';

+-------------------------+-------+
| Variable_name           | Value |
+-------------------------+-------+
| mysql56_temporal_format | ON    |
+-------------------------+-------+

ALTER TABLE example_table MODIFY ts_col TIME;
```

When MariaDB executes the `<code>[ALTER TABLE](../../sql-statements-and-structure/sql-statements/data-definition/alter/alter-tablespace.md)</code>` statement, it converts the data from the older temporal format to the newer one.


In the event that you have several tables and columns using temporal data types that you want to switch over to the new format, make sure the system variable is enabled, then perform a dump and restore using `<code>mariadb-dump</code>`. The columns using relevant temporal data types are restored using the new temporal format.


Starting from [MariaDB 10.5.1](../../../../release-notes/mariadb-community-server/release-notes-mariadb-10-5-series/mariadb-1051-release-notes.md) columns with old temporal formats are marked with a `<code>/* mariadb-5.3 */</code>` comment in the output of [SHOW CREATE TABLE](../../sql-statements-and-structure/sql-statements/administrative-sql-statements/show/show-create-table.md), [SHOW COLUMNS](../../sql-statements-and-structure/sql-statements/administrative-sql-statements/show/show-columns.md), [DESCRIBE](../../sql-statements-and-structure/sql-statements/administrative-sql-statements/describe.md) statements, as well as in the `<code>COLUMN_TYPE</code>` column of the [INFORMATION_SCHEMA.COLUMNS Table](../../sql-statements-and-structure/sql-statements/administrative-sql-statements/system-tables/information-schema/information-schema-tables/information-schema-columns-table.md).


```
SHOW CREATE TABLE mariadb5312_time\G
*************************** 1. row ***************************
       Table: mariadb5312_time
Create Table: CREATE TABLE `mariadb5312_time` (
  `t0` time /* mariadb-5.3 */ DEFAULT NULL,
  `t6` time(6) /* mariadb-5.3 */ DEFAULT NULL
) ENGINE=MyISAM DEFAULT CHARSET=latin1
```

Note, columns with the current format are not marked with a comment.


## Examples


```
INSERT INTO time VALUES ('90:00:00'), ('800:00:00'), (800), (22), (151413), ('9:6:3'), ('12 09');

SELECT * FROM time;
+-----------+
| t         |
+-----------+
| 90:00:00  |
| 800:00:00 |
| 00:08:00  |
| 00:00:22  |
| 15:14:13  |
| 09:06:03  |
| 297:00:00 |
+-----------+
```

Time_Example:


```
CREATE TABLE time_example (
  description VARCHAR(30),
  example TIME(6)
);
```

```
INSERT INTO time_example VALUES
  ('HH:MM:SS', '12:34:56'),
  ('HHMMSS', '123456'),
  ('SS.microsec', '42.123456');
```

The resulting data would look like this:


```
SELECT * FROM time_example;
```

```
+-------------+-----------------+
| description | example         |
+-------------+-----------------+
| HH:MM:SS    | 12:34:56.000000 |
| HHMMSS      | 12:34:56.000000 |
| SS.microsec | 00:00:42.123456 |
+-------------+-----------------+
```

## See Also


* [Data Type Storage Requirements](../data-type-storage-requirements.md)

