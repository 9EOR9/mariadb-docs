
# Cursor Overview


## Description


A cursor is a structure that allows you to go over records sequentially, and perform processing based on the result.


MariaDB permits cursors inside [stored programs](../../stored-routines/README.md), and MariaDB cursors are non-scrollable, read-only and asensitive.


* Non-scrollable means that the rows can only be fetched in the order specified by the SELECT statement. Rows cannot be skipped, you cannot jump to a specific row, and you cannot fetch rows in reverse order.
* Read-only means that data cannot be updated through the cursor.
* Asensitive means that the cursor points to the actual underlying data. This kind of cursor is quicker than the alternative, an insensitive cursor, as no data is copied to a temporary table. However, changes to the data being used by the cursor will affect the cursor data.


Cursors are created with a [DECLARE CURSOR](declare-cursor.md) statement and opened with an [OPEN](open.md) statement. Rows are read with a [FETCH](fetch.md) statement before the cursor is finally closed with a [CLOSE](close.md) statement.


When FETCH is issued and there are no more rows to extract, the following error is produced:


```
ERROR 1329 (02000): No data - zero rows fetched, selected, or processed
```

To avoid problems, a [DECLARE HANDLER](../declare-handler.md) statement is generally used. The HANDLER should handler the 1329 error, or the '02000' [SQLSTATE](../programmatic-compound-statements-diagnostics/sqlstate.md), or the NOT FOUND error class.


Only [SELECT](../../../../reference/sql-statements-and-structure/sql-statements/data-manipulation/selecting-data/select.md) statements are allowed for cursors, and they cannot be contained in a variable - so, they cannot be composed dynamically. However, it is possible to SELECT from a view. Since the [CREATE VIEW](../../views/create-view.md) statement can be executed as a prepared statement, it is possible to dynamically create the view that is queried by the cursor.


From [MariaDB 10.3.0](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-3-series/mariadb-1030-release-notes), cursors can have parameters. Cursor parameters can appear in any part of the [DECLARE CURSOR](declare-cursor.md) select_statement where a stored procedure variable is allowed (select list, WHERE, HAVING, LIMIT etc). See [DECLARE CURSOR](declare-cursor.md) and [OPEN](open.md) for syntax, and below for an example:


## Examples


```
CREATE TABLE c1(i INT);

CREATE TABLE c2(i INT);

CREATE TABLE c3(i INT);

DELIMITER //

CREATE PROCEDURE p1()
BEGIN
  DECLARE done INT DEFAULT FALSE;
  DECLARE x, y INT;
  DECLARE cur1 CURSOR FOR SELECT i FROM test.c1;
  DECLARE cur2 CURSOR FOR SELECT i FROM test.c2;
  DECLARE CONTINUE HANDLER FOR NOT FOUND SET done = TRUE;

  OPEN cur1;
  OPEN cur2;

  read_loop: LOOP
    FETCH cur1 INTO x;
    FETCH cur2 INTO y;
    IF done THEN
      LEAVE read_loop;
    END IF;
    IF x < y THEN
      INSERT INTO test.c3 VALUES (x);
    ELSE
      INSERT INTO test.c3 VALUES (y);
    END IF;
  END LOOP;

  CLOSE cur1;
  CLOSE cur2;
END; //

DELIMITER ;

INSERT INTO c1 VALUES(5),(50),(500);

INSERT INTO c2 VALUES(10),(20),(30);

CALL p1;

SELECT * FROM c3;
+------+
| i    |
+------+
|    5 |
|   20 |
|   30 |
+------+
```

From [MariaDB 10.3.0](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-3-series/mariadb-1030-release-notes)


```
DROP PROCEDURE IF EXISTS p1;
DROP TABLE IF EXISTS t1;
CREATE TABLE t1 (a INT, b VARCHAR(10));

INSERT INTO t1 VALUES (1,'old'),(2,'old'),(3,'old'),(4,'old'),(5,'old');

DELIMITER //

CREATE PROCEDURE p1(min INT,max INT)
BEGIN
  DECLARE done INT DEFAULT FALSE;
  DECLARE va INT;
  DECLARE cur CURSOR(pmin INT, pmax INT) FOR SELECT a FROM t1 WHERE a BETWEEN pmin AND pmax;
  DECLARE CONTINUE HANDLER FOR NOT FOUND SET done=TRUE;
  OPEN cur(min,max);
  read_loop: LOOP
    FETCH cur INTO va;
    IF done THEN
      LEAVE read_loop;
    END IF;
    INSERT INTO t1 VALUES (va,'new');
  END LOOP;
  CLOSE cur; 
END;
//

DELIMITER ;

CALL p1(2,4);

SELECT * FROM t1;
+------+------+
| a    | b    |
+------+------+
|    1 | old  |
|    2 | old  |
|    3 | old  |
|    4 | old  |
|    5 | old  |
|    2 | new  |
|    3 | new  |
|    4 | new  |
+------+------+
```

## See Also


* [DECLARE CURSOR](declare-cursor.md)
* [OPEN cursor_name](open.md)
* [FETCH cursor_name](fetch.md)
* [CLOSE cursor_name](close.md)
* [Cursors in Oracle mode](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/compatibility-and-differences/sql_modeoracle)

