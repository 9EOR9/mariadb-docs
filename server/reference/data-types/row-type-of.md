# ROW TYPE OF

## Overview

This is special declaration only available inside a stored procedure.

## EXAMPLES

```sql
CREATE TABLE rowtypeof_table(
  descr VARCHAR(20),
  val INT
);
```

```sql
INSERT INTO rowtypeof_table VALUES ('Life', 42);
```

```sql
DELIMITER $$
CREATE PROCEDURE rowtypeof_proc()
BEGIN
  DECLARE rec1 ROW TYPE OF rowtypeof_table;
  SELECT * INTO rec1 FROM rowtypeof_table;
  SELECT rec1.descr, rec1.val;
END;
$$
DELIMITER ;
```

```sql
CALL rowtypeof_proc();

+------------+----------+
| rec1.descr | rec1.val |
+------------+----------+
| Life       |       42 |
+------------+----------+
```

<sub>_This page is: Copyright © 2025 MariaDB. All rights reserved._</sub>

{% @marketo/form formId="4316" %}
