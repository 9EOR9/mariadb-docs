
# host_summary_by_statement_latency and x$host_summary_by_statement_latency Sys Schema Views


##### MariaDB starting with [10.6](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/release-notes-mariadb-10-6-series/what-is-mariadb-106)
These [Sys Schema](../README.md) views were introduced in [MariaDB 10.6](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/release-notes-mariadb-10-6-series/what-is-mariadb-106).


## Description


The `host_summary_by_statement_latency` and `x$host_summary_by_statement_latency` views summarize statement statistics, grouped by host. Rows are sorted by descending total latency by default. The `host_summary_by_statement_latency` view is intended to be easier for human reading, while the `x$host_summary_by_statement_latency` view provides the data in raw form, intended for tools that process the data.


They contain the following columns:



| Column | Description |
| --- | --- |
| Column | Description |
| host | Host that the client connected from, or background for background threads (where the HOST column in the underlying Performance Schema table is NULL). |
| total | Total number of statements for the host. |
| max_latency | Maximum single wait time of timed statements for the host. |
| lock_latency | Total time spent by timed statements for the host waiting for locks. |
| total_latency | Total wait time of timed statements for the host. |
| rows_sent | Total number of rows returned by statements for the host. |
| rows_examined | Total number of rows read from storage engines by statements for the host. |
| rows_affected | Total number of rows affected by statements for the host. |
| full_scans | Total number of full table scans by statements for the host. |



## Example


```
SELECT * FROM sys.host_summary_by_statement_latency\G
*************************** 1. row ***************************
         host: localhost
        total: 1042
total_latency: 816.89 ms
  max_latency: 64.51 ms
 lock_latency: 215.64 ms
    rows_sent: 750599937895985
rows_examined: 13548
rows_affected: 6
   full_scans: 33
*************************** 2. row ***************************
         host: background
        total: 0
total_latency: 0 ps
  max_latency: 0 ps
 lock_latency: 0 ps
    rows_sent: 0
rows_examined: 0
rows_affected: 0
   full_scans: 0

SELECT * FROM sys.x$host_summary_by_statement_latency\G
*************************** 1. row ***************************
         host: localhost
        total: 1041
total_latency: 812132706000
  max_latency: 64507216000
 lock_latency: 215301000000
    rows_sent: 750599937895983
rows_examined: 13110
rows_affected: 6
   full_scans: 32
*************************** 2. row ***************************
         host: background
        total: 0
total_latency: 0
  max_latency: 0
 lock_latency: 0
    rows_sent: 0
rows_examined: 0
rows_affected: 0
   full_scans: 0
```


CC BY-SA / Gnu FDL

