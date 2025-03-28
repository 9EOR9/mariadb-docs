# SHOW PACKAGE BODY STATUS

#

# Syntax

```
SHOW PACKAGE BODY STATUS
 [LIKE 'pattern' | WHERE expr]
```

#

# Description

The `SHOW PACKAGE BODY STATUS` statement returns characteristics of stored package bodies (implementations), such as the database, name, type, creator, creation and modification dates, and character set information. A similar statement, [SHOW PACKAGE STATUS](show-package-status.md), displays information about stored package specifications.

The `LIKE` clause, if present, indicates which package names to match. The `WHERE` and `LIKE` clauses can be given to select rows using more general conditions, as discussed in [Extended SHOW](extended-show.md).

The [ROUTINES table](../system-tables/information-schema/information-schema-tables/information-schema-routines-table.md) in the INFORMATION_SCHEMA database contains more detailed information.

#

# Examples

```
SHOW PACKAGE BODY STATUS LIKE 'pkg1'\G
*************************** 1. row ***************************
 Db: test
 Name: pkg1
 Type: PACKAGE BODY
 Definer: root@localhost
 Modified: 2018-02-27 14:44:14
 Created: 2018-02-27 14:44:14
 Security_type: DEFINER
 Comment: This is my first package body
character_set_client: utf8
collation_connection: utf8_general_ci
 Database Collation: latin1_swedish_ci
```

#

# See Also

* [SHOW PACKAGE STATUS](show-package-status.md)
* [SHOW CREATE PACKAGE BODY](show-create-package-body.md)
* [CREATE PACKAGE BODY](../../data-definition/create/create-package-body.md)
* [DROP PACKAGE BODY](../../data-definition/drop/drop-package-body.md)
* [Oracle SQL_MODE](/en/sql_modeoracle-from-mariadb-103/)