# SHOW CREATE DATABASE

## Syntax

```sql
SHOW CREATE {DATABASE | SCHEMA} db_name
```

## Description

Shows the [CREATE DATABASE](../../data-definition/create/create-database.md) statement that creates the given database. `SHOW CREATE SCHEMA` is a synonym for `SHOW CREATE DATABASE`. `SHOW CREATE DATABASE` quotes database names according to the value of the [sql\_quote\_show\_create](../../../../ha-and-performance/optimization-and-tuning/system-variables/server-system-variables.md#sql_quote_show_create) server system variable.

## Examples

```sql
SHOW CREATE DATABASE test;
+----------+-----------------------------------------------------------------+
| Database | Create Database                                                 |
+----------+-----------------------------------------------------------------+
| test     | CREATE DATABASE `test` /*!40100 DEFAULT CHARACTER SET latin1 */ |
+----------+-----------------------------------------------------------------+

SHOW CREATE SCHEMA test;
+----------+-----------------------------------------------------------------+
| Database | Create Database                                                 |
+----------+-----------------------------------------------------------------+
| test     | CREATE DATABASE `test` /*!40100 DEFAULT CHARACTER SET latin1 */ |
+----------+-----------------------------------------------------------------+
```

With [sql\_quote\_show\_create](../../../../ha-and-performance/optimization-and-tuning/system-variables/server-system-variables.md#sql_quote_show_create) off:

```sql
SHOW CREATE DATABASE test;
+----------+---------------------------------------------------------------+
| Database | Create Database                                               |
+----------+---------------------------------------------------------------+
| test     | CREATE DATABASE test /*!40100 DEFAULT CHARACTER SET latin1 */ |
+----------+---------------------------------------------------------------+
```

With a comment, from [MariaDB 10.5](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-10-5-series/what-is-mariadb-105):

```sql
SHOW CREATE DATABASE p;
+----------+--------------------------------------------------------------------------------------+
| Database | Create Database                                                                      |
+----------+--------------------------------------------------------------------------------------+
| p        | CREATE DATABASE `p` /*!40100 DEFAULT CHARACTER SET latin1 */ COMMENT 'presentations' |
+----------+--------------------------------------------------------------------------------------+
```

## See Also

* [CREATE DATABASE](../../data-definition/create/create-database.md)
* [ALTER DATABASE](../../data-definition/alter/alter-database.md)
* [Character Sets and Collations](../../../data-types/string-data-types/character-sets/supported-character-sets-and-collations.md)

<sub>_This page is licensed: GPLv2, originally from [fill\_help\_tables.sql](https://github.com/MariaDB/server/blob/main/scripts/fill_help_tables.sql)_</sub>

{% @marketo/form formId="4316" %}
