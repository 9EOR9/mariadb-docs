# Information Schema SQL\_FUNCTIONS Table

{% hint style="info" %}
This table is available as of MariaDB 10.6.3 / 10.5.12 / 10.4.21 / 10.3.31 / 10.2.40.
{% endhint %}

## Description

The [Information Schema](../) `SQL_FUNCTIONS` table contains the list of [MariaDB functions](../../../../../sql-functions/).

It contains a single column:

| Column   | Description   |
| -------- | ------------- |
| FUNCTION | Function name |

The table is not a standard Information Schema table, and is a MariaDB extension.

## Example

```sql
SELECT * FROM INFORMATION_SCHEMA.SQL_FUNCTIONS;
+---------------------------+
| FUNCTION                  |
+---------------------------+
| ADDDATE                   |
| ADD_MONTHS                |
| BIT_AND                   |
| BIT_OR                    |
| BIT_XOR                   |
| CAST                      |
| COUNT                     |
| CUME_DIST                 |
| CURDATE                   |
| CURTIME                   |
| DATE_ADD                  |
| DATE_SUB                  |
| DATE_FORMAT               |
| DECODE                    |
| DENSE_RANK                |
| EXTRACT                   |
| FIRST_VALUE               |
| GROUP_CONCAT              |
| JSON_ARRAYAGG             |
| JSON_OBJECTAGG            |
| LAG                       |
| LEAD                      |
| MAX                       |
| MEDIAN                    |
| MID                       |
| MIN                       |
| NOW                       |
| NTH_VALUE                 |
| NTILE                     |
| POSITION                  |
| PERCENT_RANK              |
| PERCENTILE_CONT           |
| PERCENTILE_DISC           |
| RANK                      |
| ROW_NUMBER                |
| SESSION_USER              |
| STD                       |
| STDDEV                    |
| STDDEV_POP                |
| STDDEV_SAMP               |
| SUBDATE                   |
| SUBSTR                    |
| SUBSTRING                 |
| SUM                       |
| SYSTEM_USER               |
| TRIM                      |
| TRIM_ORACLE               |
| VARIANCE                  |
| VAR_POP                   |
| VAR_SAMP                  |
| ABS                       |
| ACOS                      |
| ADDTIME                   |
| AES_DECRYPT               |
| AES_ENCRYPT               |
| ASIN                      |
| ATAN                      |
| ATAN2                     |
| BENCHMARK                 |
| BIN                       |
| BINLOG_GTID_POS           |
| BIT_COUNT                 |
| BIT_LENGTH                |
| CEIL                      |
| CEILING                   |
| CHARACTER_LENGTH          |
| CHAR_LENGTH               |
| CHR                       |
| COERCIBILITY              |
| COLUMN_CHECK              |
| COLUMN_EXISTS             |
| COLUMN_LIST               |
| COLUMN_JSON               |
| COMPRESS                  |
| CONCAT                    |
| CONCAT_OPERATOR_ORACLE    |
| CONCAT_WS                 |
| CONNECTION_ID             |
| CONV                      |
| CONVERT_TZ                |
| COS                       |
| COT                       |
| CRC32                     |
| DATEDIFF                  |
| DAYNAME                   |
| DAYOFMONTH                |
| DAYOFWEEK                 |
| DAYOFYEAR                 |
| DEGREES                   |
| DECODE_HISTOGRAM          |
| DECODE_ORACLE             |
| DES_DECRYPT               |
| DES_ENCRYPT               |
| ELT                       |
| ENCODE                    |
| ENCRYPT                   |
| EXP                       |
| EXPORT_SET                |
| EXTRACTVALUE              |
| FIELD                     |
| FIND_IN_SET               |
| FLOOR                     |
| FORMAT                    |
| FOUND_ROWS                |
| FROM_BASE64               |
| FROM_DAYS                 |
| FROM_UNIXTIME             |
| GET_LOCK                  |
| GREATEST                  |
| HEX                       |
| IFNULL                    |
| INSTR                     |
| ISNULL                    |
| IS_FREE_LOCK              |
| IS_USED_LOCK              |
| JSON_ARRAY                |
| JSON_ARRAY_APPEND         |
| JSON_ARRAY_INSERT         |
| JSON_COMPACT              |
| JSON_CONTAINS             |
| JSON_CONTAINS_PATH        |
| JSON_DEPTH                |
| JSON_DETAILED             |
| JSON_EXISTS               |
| JSON_EXTRACT              |
| JSON_INSERT               |
| JSON_KEYS                 |
| JSON_LENGTH               |
| JSON_LOOSE                |
| JSON_MERGE                |
| JSON_MERGE_PATCH          |
| JSON_MERGE_PRESERVE       |
| JSON_QUERY                |
| JSON_QUOTE                |
| JSON_OBJECT               |
| JSON_REMOVE               |
| JSON_REPLACE              |
| JSON_SET                  |
| JSON_SEARCH               |
| JSON_TYPE                 |
| JSON_UNQUOTE              |
| JSON_VALID                |
| JSON_VALUE                |
| LAST_DAY                  |
| LAST_INSERT_ID            |
| LCASE                     |
| LEAST                     |
| LENGTH                    |
| LENGTHB                   |
| LN                        |
| LOAD_FILE                 |
| LOCATE                    |
| LOG                       |
| LOG10                     |
| LOG2                      |
| LOWER                     |
| LPAD                      |
| LPAD_ORACLE               |
| LTRIM                     |
| LTRIM_ORACLE              |
| MAKEDATE                  |
| MAKETIME                  |
| MAKE_SET                  |
| MASTER_GTID_WAIT          |
| MASTER_POS_WAIT           |
| MD5                       |
| MONTHNAME                 |
| NAME_CONST                |
| NVL                       |
| NVL2                      |
| NULLIF                    |
| OCT                       |
| OCTET_LENGTH              |
| ORD                       |
| PERIOD_ADD                |
| PERIOD_DIFF               |
| PI                        |
| POW                       |
| POWER                     |
| QUOTE                     |
| REGEXP_INSTR              |
| REGEXP_REPLACE            |
| REGEXP_SUBSTR             |
| RADIANS                   |
| RAND                      |
| RELEASE_ALL_LOCKS         |
| RELEASE_LOCK              |
| REPLACE_ORACLE            |
| REVERSE                   |
| ROUND                     |
| RPAD                      |
| RPAD_ORACLE               |
| RTRIM                     |
| RTRIM_ORACLE              |
| SEC_TO_TIME               |
| SHA                       |
| SHA1                      |
| SHA2                      |
| SIGN                      |
| SIN                       |
| SLEEP                     |
| SOUNDEX                   |
| SPACE                     |
| SQRT                      |
| STRCMP                    |
| STR_TO_DATE               |
| SUBSTR_ORACLE             |
| SUBSTRING_INDEX           |
| SUBTIME                   |
| SYS_GUID                  |
| TAN                       |
| TIMEDIFF                  |
| TIME_FORMAT               |
| TIME_TO_SEC               |
| TO_BASE64                 |
| TO_CHAR                   |
| TO_DAYS                   |
| TO_SECONDS                |
| UCASE                     |
| UNCOMPRESS                |
| UNCOMPRESSED_LENGTH       |
| UNHEX                     |
| UNIX_TIMESTAMP            |
| UPDATEXML                 |
| UPPER                     |
| UUID                      |
| UUID_SHORT                |
| VERSION                   |
| WEEKDAY                   |
| WEEKOFYEAR                |
| WSREP_LAST_WRITTEN_GTID   |
| WSREP_LAST_SEEN_GTID      |
| WSREP_SYNC_WAIT_UPTO_GTID |
| YEARWEEK                  |
+---------------------------+
234 rows in set (0.001 sec)
```

## See Also

* [Reserved Words](../../../../../sql-structure/sql-language-structure/reserved-words.md)

<sub>_This page is licensed: CC BY-SA / Gnu FDL_</sub>

{% @marketo/form formId="4316" %}
