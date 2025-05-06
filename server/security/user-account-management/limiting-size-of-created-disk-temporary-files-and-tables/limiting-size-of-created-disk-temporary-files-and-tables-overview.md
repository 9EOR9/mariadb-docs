
# Limiting Size of Created Disk Temporary Files and Tables Overview


##### MariaDB starting with [11.5](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-11-5-rolling-releases/what-is-mariadb-115)
From [MariaDB 11.5](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-11-5-rolling-releases/what-is-mariadb-115), it's possible to limit the size of created disk temporary files and tables. 
When the internal in-memory temporary table is oversize and converting to MyISAM/Aria table to store on disk, this option will limit the max space of tmp_dir. If a new disk temporary table will cause tmp_dir over the limitation, then this query will return an error.


## Temporary Space


The temporary space includes:


* All SQL level temporary files. This includes files for filesort, transaction temporary space, analyze, binlog_stmt_cache etc. It does not include engine internal temporary files used for repair, alter table, index pre sorting etc.
* All internal on disk temporary tables created as part of resolving a SELECT, multi-source update etc.


## Special Cases


* When doing a commit, the last flush of the binlog_stmt_cache will not cause an error even if the temporary space limit is exceeded. This is to avoid giving errors on commit. This means that a user can temporary go over the limit with up to [binlog_stmt_cache_size](../../../server-usage/replication-cluster-multi-master/standard-replication/replication-and-binary-log-system-variables.md#binlog_stmt_cache_size).


## System Variables


There are two system variables used for controlling this feature:


* [max_tmp_session_space_usage](max_tmp_session_space_usage-system-variable.md): Limits the the temporary space allowance per user
* [max_tmp_total_space_usage](max_tmp_total_space_usage-system-variable.md): Limits the temporary space allowance for all users.


## Status Variables


* [tmp_space_used](../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/server-status-variables.md#tmp_space_used)
* [max_tmp_space_used](../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/server-status-variables.md#max_tmp_space_used)


## Information Schema


* New field in [information_schema.process_list](../../../reference/sql-statements-and-structure/sql-statements/administrative-sql-statements/system-tables/information-schema/information-schema-tables/information-schema-processlist-table.md): TMP_SPACE_USED


## Noteworthy issue


* One has to be careful when using small values for max_tmp_space limit together with [binary logging](../../../server-management/server-monitoring-logs/binary-log/README.md) and with non transactional tables.
* If a binary log entry for the query is larger than [binlog_stmt_cache_size](../../../server-usage/replication-cluster-multi-master/standard-replication/replication-and-binary-log-system-variables.md#binlog_stmt_cache_size) and one hits the limit of max_tmp_space when flushing the entry to disk, the query will abort and the binary log will not contain the last changes to the table. This will also stop the replica!
* This is also true for all Aria tables as Aria cannot do rollback (except in case of crashes)!
* One way to avoid it is to use [@@binlog_format=statement](../../../server-usage/replication-cluster-multi-master/standard-replication/replication-and-binary-log-system-variables.md#binlog_format) for queries that update many lot of rows.


## Implementation


* All writes to temporary files or internal temporary tables, that increase the file size, are routed through temp_file_size_cb_func() which updates and checks the temp space usage.
* Most of the temporary file monitoring is done inside IO_CACHE. Temporary file monitoring is done inside the Aria engine.
* MY_TRACK and MY_TRACK_WITH_LIMIT are new flags for ini_io_cache(). MY_TRACK means that we track the file usage. TRACK_WITH_LIMIT means that we track the file usage and we give an error if the limit is breached. This is used to not give an error on commit when binlog_stmt_cache is flushed.
* global_tmp_space_used contains the total tmp space used so far. This is needed quickly check against max_total_tmp_space_usage.
* Temporary space errors are using EE_LOCAL_TMP_SPACE_FULL and handler errors are using HA_ERR_LOCAL_TMP_SPACE_FULL. This is needed until we move general errors to it's own error space so that they cannot conflict with system error numbers.
* Return value of my_chsize() and mysql_file_chsize() has changed so that -1 is returned in the case my_chsize() could not decrease the file size (very unlikely and will not happen on modern systems). All calls to _chsize() are updated to check for > 0 as the error condition.
* At the destruction of THD we check that THD::tmp_file_space == 0
* At server end we check that global_tmp_space_used == 0
* As a precaution against errors in the tmp_space_used code, one can set max_tmp_space_usage and max_total_tmp_space_usage to 0 to disable the tmp space quota errors.
* truncate_io_cache() function added.
* Aria tables using static or dynamic row length are registered in 8K increments to avoid some calls to update_tmp_file_size().


## See Also


* [MDEV-9101](https://jira.mariadb.org/browse/MDEV-9101) - Limit size of created disk temporary files and tables


CC BY-SA / Gnu FDL

