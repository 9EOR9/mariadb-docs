# memory\_by\_host\_by\_current\_bytes and x$memory\_by\_host\_by\_current\_bytes Views

**MariaDB starting with** [**10.6**](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/community-server/mariadb-10-6-series/what-is-mariadb-106)

These [Sys Schema](../) views were introduced in [MariaDB 10.6](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/community-server/mariadb-10-6-series/what-is-mariadb-106).

## Description

The `memory_by_host_by_current_bytes` and `x$memory_by_host_by_current_bytes` summarize memory use grouped by host. Rows by default are sorted by descending amount of memory used.

The `memory_by_host_by_current_bytes` view is intended to be easier for human reading, while the `x$memory_by_host_by_current_bytes` view provides the data in raw form, intended for tools that process the data.

They contain the following columns:

| Column               | Description                                                                                                                                                                                       |
| -------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Column               | Description                                                                                                                                                                                       |
| host                 | Host from which the client connected. If the HOST column in the underlying Performance Schema table is NULL, rows are assumed to be for background threads, and the background host name is used. |
| current\_count\_used | Current number of allocated memory blocks that have not yet been freed for the host.                                                                                                              |
| current\_allocated   | Current number of allocated bytes that have not yet been freed for the host.                                                                                                                      |
| current\_avg\_alloc  | Current number of allocated bytes per memory block for the host.                                                                                                                                  |
| current\_max\_alloc  | Largest single current memory allocation in bytes for the host.                                                                                                                                   |
| total\_allocated     | Total memory allocation in bytes for the host.                                                                                                                                                    |

CC BY-SA / Gnu FDL
