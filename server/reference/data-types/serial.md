
# SERIAL


# Overview


This is an alias for BIGINT UNSIGNED NOT NULL AUTO_INCREMENT UNIQUE.


# EXAMPLES


```
CREATE TABLE serial_example (
  id SERIAL,
  data VARCHAR(32)
);
```

```
SHOW CREATE TABLE serial_example\G
```

```
*************************** 1. row ***************************
       Table: serial_example
Create Table: CREATE TABLE `serial_example` (
  `id` bigint(20) unsigned NOT NULL AUTO_INCREMENT,
  `data` varchar(32) DEFAULT NULL,
  UNIQUE KEY `id` (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=latin1
```

# EXTERNAL REFERENCES


Additional information is available [here](auto_increment.md).


Copyright © 2025 MariaDB

