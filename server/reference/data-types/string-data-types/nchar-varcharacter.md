# NCHAR VARCHARACTER

## Overview

See [NATIONAL VARCHAR](national-char.md).

## EXAMPLES

```sql
CREATE TABLE nchar_varcharacter_example (
  example NCHAR VARCHARACTER(32)
);
```

```sql
SHOW CREATE TABLE nchar_varcharacter_example\G
```

```sql
*************************** 1. row ***************************
       Table: nchar_varcharacter_example
Create Table: CREATE TABLE `nchar_varcharacter_example` (
  `example` varchar(32) CHARACTER SET utf8 DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1
```

<sub>_This page is: Copyright © 2025 MariaDB. All rights reserved._</sub>

{% @marketo/form formId="4316" %}
