# Diagnostics Area

The diagnostics area contains information about the error conditions which were produced by an SQL statement, as well as some information about the statement which generated them.

## Statement Information

The statement information area contains the following data:

* NUMBER is the number of conditions which are present in the diagnostics area.
* ROW\_COUNT has the same value as the [ROW\_COUNT()](../../../sql-functions/secondary-functions/information-functions/row_count.md) function for the statement that produced the conditions.

## Condition Information

Each condition has several properties, which are explained here.

### Data Types and Sizes

The following table shows the type and size of all the properties:

| Property name       | Property type     | Notes                                                                                                                                                                                                      |
| ------------------- | ----------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Property name       | Property type     | Notes                                                                                                                                                                                                      |
| RETURNED\_SQLSTATE  | VARCHAR(5)        |                                                                                                                                                                                                            |
| MYSQL\_ERRNO        | SMALLINT UNSIGNED |                                                                                                                                                                                                            |
| MESSAGE\_TEXT       | VARCHAR(512)      | Before [MariaDB 10.3.6](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-3-series/mariadb-1036-release-notes), was VARCHAR(128) |
| CLASS\_ORIGIN       | VARCHAR(64)       |                                                                                                                                                                                                            |
| SUBCLASS\_ORIGIN    | VARCHAR(64)       |                                                                                                                                                                                                            |
| CONSTRAINT\_CATALOG | VARCHAR(64)       |                                                                                                                                                                                                            |
| CONSTRAINT\_SCHEMA  | VARCHAR(64)       |                                                                                                                                                                                                            |
| CONSTRAINT\_NAME    | VARCHAR(64)       |                                                                                                                                                                                                            |
| CATALOG\_NAME       | VARCHAR(64)       |                                                                                                                                                                                                            |
| SCHEMA\_NAME        | VARCHAR(64)       |                                                                                                                                                                                                            |
| TABLE\_NAME         | VARCHAR(64)       |                                                                                                                                                                                                            |
| COLUMN\_NAME        | VARCHAR(64)       |                                                                                                                                                                                                            |
| CURSOR\_NAME        | VARCHAR(64)       |                                                                                                                                                                                                            |

These properties can never be set to NULL. If they are empty, the empty string is used.

### Common Condition Properties

The most common ones have a value for all built-in errors, and can be read both via SQL and via the API:

RETURNED\_SQLSTATE is the SQLSTATE of the condition. It is a five characters code, composed by a class (first two characters) and a subclass (last three characters). For more information about this property, refer to the [SQLSTATE](sqlstate.md) page.

MYSQL\_ERRNO is the error code. Each built-in condition has a unique numeric code. 0 indicates success, but it cannot be explicitly set or read via SQL. For a list of built-in error codes, refer to [MariaDB Error Codes](https://github.com/mariadb-corporation/docs-server/blob/test/server/server-usage/programmatic-compound-statements/programmatic-compound-statements-diagnostics/broken-reference/README.md). The API function to read it is mysql\_errno().

MESSAGE\_TEXT is a descriptive, human-readable message. For built-in errors, parsing this string is the only way to get more information about the error. For example, parsing a message like "Table 'tab1' already exists", a program can find out that the missing table is tab1. The API function to read it is mysql\_error().

For conditions generated by the user via SIGNAL, if MYSQL\_ERRNO and MESSAGE\_TEXT are not specified, their default values depend on the first two SQLSTATE characters:

* '00' means 'success'. It can not be set in any way, and can only be read via the API.
* For '01' class, default MYSQL\_ERRNO is 1642 and default MESSAGE\_TEXT is 'Unhandled user-defined warning condition'.
* For '02' class, default MYSQL\_ERRNO is 1643 and default MESSAGE\_TEXT is 'Unhandled user-defined not found condition'.
* For all other cases, including the '45000' value, default MYSQL\_ERRNO is 1644 and default MESSAGE\_TEXT is 'Unhandled user-defined exception condition'.

### Special Condition Properties

There are more condition properties, which are never set for built-in errors. They can only be set via SIGNAL and RESIGNAL statements, and can only be read via GET DIAGNOSTICS - not via the API. Such properties are:

CLASS\_ORIGIN indicates whether the SQLSTATE uses a standard class or a software-specific class. If it is defined in the SQL standards document ISO 9075-2 (section 24.1, SQLSTATE), this property's value is supposed to be 'ISO 9075', otherwise it is supposed to be 'MySQL'. However, any string is accepted.

SUBCLASS\_ORIGIN indicates whether the SQLSTATE uses a standard subclass or a software-specific class. If the SQLSTATE is defined in the SQL standards document ISO 9075-2 (section 24.1, SQLSTATE), this property's value is supposed to be 'ISO 9075', otherwise it is supposed to be 'MySQL'. However, any string is accepted.

SCHEMA\_NAME indicates in which schema (database) the error occurred.

TABLE\_NAME indicates the name of the table which was accessed by the failed statement.

COLUMN\_NAME indicates the name of the column which was accessed by the failed statement.

CONSTRAINT\_NAME indicates the name of the constraint that was violated.

CONSTRAINT\_SCHEMA indicates in which schema the violated constraint is located.

CURSOR\_NAME indicates the name of the cursor which caused the error.

The following properties can be used and are defined in the standard SQL, but have no meaning because MariaDB doesn't currently support catalogs:

CATALOG\_NAME is used by the standard SQL to indicate in which catalog the error occurred.

CONSTRAINT\_CATALOG is used by the standard SQL to indicate in which catalog the violated constraint is located.

## How the Diagnostics Area is Populated and Cleared

When a statement produces one or more error conditions (errors, warnings, notes) the conditions are inserted into the diagnostics area, and the statement information area is updated with that statement’s information. Usually, this also clears all the old conditions from the diagnostics area, but there is an exception: if the new statement is a correctly parsed RESIGNAL or GET DIAGNOSTICS, the old contents will remain in the diagnostics area. SIGNAL clears the old conditions.

When a table-based statement (like INSERT) is executed, the old data in the diagnostics area is cleared even if the statement doesn't produce any condition. However, statements which don't access any table (like SET, or a SELECT with no FROM clause) is executed and produces no warnings, the diagnostics area remains unchanged.

The maximum number of conditions that can be in the diagnostics area is [max_error_count](../../../replication-cluster-multi-master/optimization-and-tuning/system-variables/server-system-variables.md#max_error_count). If this value is 0, the diagnostics area is empty. If this variable is changed, the new value takes effect with the next statement (that is, the diagnostics area is not immediately truncated).

## How to Access the Diagnostics Area

The following statements explicitly add conditions to the diagnostics area:

* [SIGNAL](../signal.md): produces a custom error.
* [RESIGNAL](../resignal.md): after an error is produced, generates a modified version of that error.

The following statements read contents from the diagnostics area:

* [GET DIAGNOSTICS](get-diagnostics.md) is the only way to read all information
* [SHOW WARNINGS](../../administrative-sql-statements/show/show-warnings.md) shows a summary of errors, warnings and notes
* [SHOW ERRORS](../../administrative-sql-statements/show/show-errors.md) shows a summary of errors

[DECLARE HANDLER](../declare-handler.md) can be used to handle error conditions within stored programs.

[DECLARE CONDITION](../declare-condition.md) can be used to associate an SQLSTATE or an error code to a name. That name can be referenced in DECLARE HANDLER, SIGNAL and RESIGNAL statements.

All these statements can also be executed inside a stored routine. However, only SHOW WARNINGS and SHOW ERRORS can be executed as a prepared statement. After an [EXECUTE](../../prepared-statements/execute-statement.md) statement, the diagnostics area contains information about the prepared statement, if it produces error conditions.

## See Also

* [RESIGNAL](../resignal.md)
* [SIGNAL](../signal.md)
* [HANDLER](../../../sql-structure/nosql/handler/)
* [GET DIAGNOSTICS](get-diagnostics.md)
* [SHOW WARNINGS](../../administrative-sql-statements/show/show-warnings.md)
* [SHOW ERRORS](../../administrative-sql-statements/show/show-errors.md)
* [DECLARE HANDLER](../declare-handler.md)
* [MariaDB Error Codes](https://github.com/mariadb-corporation/docs-server/blob/test/server/server-usage/programmatic-compound-statements/programmatic-compound-statements-diagnostics/broken-reference/README.md)

<sub>_This page is licensed: CC BY-SA / Gnu FDL_</sub>

{% @marketo/form formId="4316" %}
