# host\_summary\_by\_stages and x$host\_summary\_by\_stages Sys Schema Views

**MariaDB starting with** [**10.6**](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-10-6-series/what-is-mariadb-106)

These [Sys Schema](../) views were introduced in [MariaDB 10.6](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-10-6-series/what-is-mariadb-106).

## Description

The `host_summary_by_stages` and `x$host_summary_by_stages` views summarize statement stages, grouped by host. Rows are sorted by host and descending total latency by default. The `host_summary_by_stages` view is intended to be easier for human reading, while the `x$host_summary_by_stages` view provides the data in raw form, intended for tools that process the data.

They contain the following columns:

| Column         | Description                                                                                                                                           |
| -------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| Column         | Description                                                                                                                                           |
| host           | Host that the client connected from, or background for background threads (where the HOST column in the underlying Performance Schema table is NULL). |
| event\_name    | Stage event name.                                                                                                                                     |
| total          | Total number of occurrences of the file stage event for the host.                                                                                     |
| total\_latency | Total wait time of timed occurrences of the stage event for the host.                                                                                 |
| avg\_latency   | Average wait time per timed occurrence of the stage event for the host.                                                                               |

## Example

```
SELECT * FROM sys.host_summary_by_stages\G
*************************** 1. row ***************************
         host: background
   event_name: stage/innodb/buffer pool load
        total: 1
total_latency: 3.75 ms
  avg_latency: 3.75 ms

SELECT * FROM sys.x$host_summary_by_stages\G
*************************** 1. row ***************************
         host: background
   event_name: stage/innodb/buffer pool load
        total: 1
total_latency: 3747098000
  avg_latency: 3747098000
```

<sub>_This page is licensed: CC BY-SA / Gnu FDL_</sub>

{% @marketo/form formId="4316" %}
