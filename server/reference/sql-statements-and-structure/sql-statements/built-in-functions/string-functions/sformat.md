
# SFORMAT


##### MariaDB starting with [10.7.0](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-7-series/mariadb-1070-release-notes)
SFORMAT was added in [MariaDB 10.7.0](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-7-series/mariadb-1070-release-notes).


## Description


The `SFORMAT` function takes an input string and a formatting specification and returns the string formatted using the rules the user passed in the specification.


It uses the [fmtlib library](https://fmt.dev/) for Python-like (as well as Rust, C++20, etc) string formatting.


Only fmtlib 7.0.0+ is supported.


There is no native support for temporal and decimal values:


* TIME_RESULT is handled as STRING_RESULT
* DECIMAL_RESULT as REAL_RESULT


## Examples


```
SELECT SFORMAT("The answer is {}.", 42);
+----------------------------------+
| SFORMAT("The answer is {}.", 42) |
+----------------------------------+
| The answer is 42.                |
+----------------------------------+

CREATE TABLE test_sformat(mdb_release char(6), mdev int, feature char(20));

INSERT INTO test_sformat VALUES('10.7.0', 25015, 'Python style sformat'), 
  ('10.7.0', 4958, 'UUID');

SELECT * FROM test_sformat;
+-------------+-------+----------------------+
| mdb_release | mdev  | feature              |
+-------------+-------+----------------------+
| 10.7.0      | 25015 | Python style sformat |
| 10.7.0      |  4958 | UUID                 |
+-------------+-------+----------------------+

SELECT SFORMAT('MariaDB Server {} has a preview for MDEV-{} which is about {}', 
  mdb_release, mdev, feature) AS 'Preview Release Examples'
  FROM test_sformat;
+----------------------------------------------------------------------------------------+
| Preview Release Examples                                                               |
+----------------------------------------------------------------------------------------+
| MariaDB Server 10.7.0 has a preview for MDEV-25015 which is about Python style sformat |
| MariaDB Server 10.7.0 has a preview for MDEV-4958 which is about UUID                  |
+----------------------------------------------------------------------------------------+
```

## See Also


* [10.7 preview feature: Python-like string formatting](https://mariadb.org/10-7-preview-feature-sformat/)

