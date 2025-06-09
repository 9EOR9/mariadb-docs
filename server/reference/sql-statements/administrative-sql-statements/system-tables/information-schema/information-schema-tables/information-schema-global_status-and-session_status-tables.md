# Information Schema GLOBAL\_STATUS and SESSION\_STATUS Tables

The [Information Schema](../) `GLOBAL_STATUS` and `SESSION_STATUS` tables store a record of all [status variables](../../../../../../ha-and-performance/optimization-and-tuning/system-variables/server-status-variables.md) and their global and session values respectively. This is the same information as displayed by the `[SHOW STATUS](../../../show/show-status.md)` commands `SHOW GLOBAL STATUS` and `SHOW SESSION STATUS`.

They contain the following columns:

| Column          | Description              |
| --------------- | ------------------------ |
| Column          | Description              |
| VARIABLE\_NAME  | Status variable name.    |
| VARIABLE\_VALUE | Global or session value. |

## Example

```
SELECT * FROM information_schema.GLOBAL_STATUS;
+-----------------------------------------------+--------------------+
| VARIABLE_NAME                                 | VARIABLE_VALUE     |
+-----------------------------------------------+--------------------+
...
| BINLOG_SNAPSHOT_FILE                          | mariadb-bin.000208 |
| BINLOG_SNAPSHOT_POSITION                      | 369                |
...
| THREADS_CONNECTED                             | 1                  |
| THREADS_CREATED                               | 1                  |
| THREADS_RUNNING                               | 1                  |
| UPTIME                                        | 57358              |
| UPTIME_SINCE_FLUSH_STATUS                     | 57358              |
+-----------------------------------------------+--------------------+
```

CC BY-SA / Gnu FDL

{% @marketo/form formId="4316" %}
