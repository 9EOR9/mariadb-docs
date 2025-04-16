
# DECLARE Variable

## Syntax


```
DECLARE var_name [, var_name] ... [[ROW] TYPE OF]] type [DEFAULT value]
```


## Description


This statement is used to declare local variables within [stored programs](../stored-routines/README.md). To
provide a default value for the variable, include a `DEFAULT` clause. The
value can be specified as an expression (even subqueries are permitted); it need not be a constant. If the
`DEFAULT` clause is missing, the initial value is `NULL`.


Local variables are treated like stored routine parameters with respect to data
type and overflow checking. See [CREATE PROCEDURE](../stored-routines/stored-procedures/create-procedure.md).


Local variables must be declared before `CONDITION`s, [CURSORs](programmatic-compound-statements-cursors/README.md) and `HANDLER`s.


Local variable names are not case sensitive.


The scope of a local variable is within the `BEGIN ... END` block where it is
declared. The variable can be referred to in blocks nested within the declaring
block, except those blocks that declare a variable with the same name.


### TYPE OF / ROW TYPE OF


Anchored data types allow a data type to be defined based on another object, such as a table row, rather than specifically set in the declaration. If the anchor object changes, so will the anchored data type. This can lead to routines being easier to maintain, so that if the data type in the table is changed, it will automatically be changed in the routine as well.


Variables declared with `ROW TYPE OF` will have the same features as implicit [ROW](../../../ref/sql-statements-and-structure/sql-statements/built-in-functions/secondary-functions/information-functions/row_count.md) variables. It is not possible to use `ROW TYPE OF` variables in a [LIMIT](../../../../general-resources/learning-and-training/training-and-tutorials/advanced-mariadb-articles/development-articles/debugging-mariadb/limitationsdifferences-with-a-mariadb-server-compiled-for-debugging.md) clause.


The real data type of `TYPE OF` and `ROW TYPE OF table_name` will become known at the very beginning of the stored routine call. [ALTER TABLE](../../../ref/sql-statements-and-structure/sql-statements/data-definition/alter/alter-tablespace.md) or [DROP TABLE](../../../ref/sql-statements-and-structure/sql-statements/data-definition/drop/drop-tablespace.md) statements performed inside the current routine on the tables that appear in anchors won't affect the data type of the anchored variables, even if the variable is declared after an [ALTER TABLE](../../../ref/sql-statements-and-structure/sql-statements/data-definition/alter/alter-tablespace.md) or [DROP TABLE](../../../ref/sql-statements-and-structure/sql-statements/data-definition/drop/drop-tablespace.md) statement.


The real data type of a `ROW TYPE OF cursor_name` variable will become known when execution enters into the block where the variable is declared. Data type instantiation will happen only once. In a cursor `ROW TYPE OF` variable that is declared inside a loop, its data type will become known on the very first iteration and won't change on further loop iterations.


The tables referenced in `TYPE OF` and `ROW TYPE OF` declarations will be checked for existence at the beginning of the stored routine call. [CREATE PROCEDURE](../stored-routines/stored-procedures/create-procedure.md) or [CREATE FUNCTION](../../../ref/sql-statements-and-structure/sql-statements/data-definition/create/create-function.md) will not check the referenced tables for existence.


## Examples


```
DECLARE name VARCHAR(5) DEFAULT 'monty';
  DECLARE x INT DEFAULT 10;
  DECLARE Y SMALLINT;
```

`TYPE OF` and `ROW TYPE OF` from [MariaDB 10.3](../../../../release-notes/mariadb-community-server/what-is-mariadb-103.md):


```
DECLARE tmp TYPE OF t1.a; -- Get the data type from the column {{a}} in the table {{t1}}

DECLARE rec1 ROW TYPE OF t1; -- Get the row data type from the table {{t1}}

DECLARE rec2 ROW TYPE OF cur1; -- Get the row data type from the cursor {{cur1}}
```

## See Also


* [User-Defined variables](../../../ref/sql-statements-and-structure/sql-language-structure/user-defined-variables.md)

