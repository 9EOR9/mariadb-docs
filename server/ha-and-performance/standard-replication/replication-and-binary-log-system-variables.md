# Replication and Binary Log System Variables

The terms _master_ and _slave_ have historically been used in replication, and MariaDB has begun the process of adding _primary_ and _replica_ synonyms. The old terms will continue to be used to maintain backward compatibility - see [MDEV-18777](https://jira.mariadb.org/browse/MDEV-18777) to follow progress on this effort.

This page lists system variables that are related to [binary logging](../../server-management/server-monitoring-logs/binary-log/) and [replication](broken-reference).

See [Server System Variables](../optimization-and-tuning/system-variables/server-system-variables.md) for a complete list of system variables and instructions on setting them, as well as [System variables for global transaction ID](gtid.md#system-variables-for-global-transaction-id).

Also see [mariadbd replication options](../../server-management/starting-and-stopping-mariadb/mariadbd-options.md#replication-and-binary-logging-options) for related options that are not system variables (such as [binlog\_do\_db](../../server-management/starting-and-stopping-mariadb/mariadbd-options.md#-binlog-do-db) and [binlog\_ignore\_db](../../server-management/starting-and-stopping-mariadb/mariadbd-options.md#-binlog-ignore-db)).

See also the [Full list of MariaDB options, system and status variables](../../server-management/variables-and-modes/full-list-of-mariadb-options-system-and-status-variables.md).

#### `auto_increment_increment`

* Description: The increment for all [AUTO\_INCREMENT](../../reference/data-types/auto_increment.md) values on the server, by default `1`. Intended for use in primary-to-primary [replication](broken-reference).
* Commandline: `--auto-increment-increment[=#]`
* Scope: Global, Session
* Dynamic: Yes
* Data Type: `numeric`
* Default Value: `1`
* Range: `1` to `65535`

#### `auto_increment_offset`

* Description: The offset for all [AUTO\_INCREMENT](../../reference/data-types/auto_increment.md) values on the server, by default `1`. Intended for use in primary-to-primary [replication](broken-reference). Should be not be larger than [auto\_increment\_increment](replication-and-binary-log-system-variables.md#auto_increment_increment). See [AUTO\_INCREMENT#Replication](../../reference/data-types/auto_increment.md#replication).
* Commandline: `--auto-increment-offset[=#]`
* Scope: Global, Session
* Dynamic: Yes
* Data Type: `numeric`
* Default Value: `1`
* Range: `1` to `65535`

#### `binlog_alter_two_phase`

* Description: When set, split ALTER at binary logging into two statements: START ALTER and COMMIT/ROLLBACK ALTER. The ON setting is recommended for long-running ALTER-table so\
  it could start on replica before its actual execution on primary.
* Commandline: `--binlog-alter-two-phase[={0|1}]`
* Scope: Global, Session
* Dynamic: Yes
* Data Type: `boolean`
* Default Value: `OFF`
* Introduced: [MariaDB 10.8.1](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-8-series/mariadb-1081-release-notes)

#### `binlog_annotate_row_events`

* Description: This option tells the primary to write [annotate\_rows\_events](../../clients-and-utilities/mariadb-binlog/annotate_rows_log_event.md) to the binary log.
* Commandline: `--binlog-annotate-row-events[={0|1}]`
* Scope: Global, Session
* Dynamic: Yes
* Data Type: boolean
* Default Value:
  * `ON` (>= [MariaDB 10.2.4](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/mariadb-1024-release-notes))
  * `OFF` (<= [MariaDB 10.2.3](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/mariadb-1023-release-notes))

#### `binlog_cache_size`

* Description: If the [binary log](../../server-management/server-monitoring-logs/binary-log/) is active, this variable determines the size in bytes, per-connection, of the cache holding a record of binary log changes during a transaction. A separate variable, [binlog\_stmt\_cache\_size](replication-and-binary-log-system-variables.md#binlog_stmt_cache_size), sets the upper limit for the statement cache. The [binlog\_cache\_disk\_use](../optimization-and-tuning/system-variables/server-status-variables.md#binlog_cache_disk_use) and [binlog\_cache\_use](../optimization-and-tuning/system-variables/server-status-variables.md#binlog_cache_use) [server status variables](../optimization-and-tuning/system-variables/server-status-variables.md) will indicate whether this variable needs to be increased (you want a low ratio of binlog\_cache\_disk\_use to binlog\_cache\_use).
* Commandline: `--binlog-cache-size=#`
* Scope: Global
* Dynamic: Yes
* Data Type: `numeric`
* Default Value: `32768`
* Range - 32 bit: `4096` to `4294967295`
* Range - 64 bit: `4096` to `18446744073709547520`

#### `binlog_checksum`

* Description: Specifies the type of BINLOG\_CHECKSUM\_ALG for log events in the [binary log](../../server-management/server-monitoring-logs/binary-log/).
* Commandline:
  * `--binlog-checksum=name`
  * `--binlog-checksum=[0|1]`
* Scope: Global
* Dynamic: Yes
* Data Type: `string`
* Default Value:
  * `CRC32` (>= [MariaDB 10.2.1](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/mariadb-1021-release-notes))
  * `NONE` (<= [MariaDB 10.2.0](broken-reference))
* Valid Values: `NONE` (`0`), `CRC32` (`1`)

#### `binlog_commit_wait_count`

* Description: Configures the behavior of [group commit for the binary log](../../server-management/server-monitoring-logs/binary-log/group-commit-for-the-binary-log.md), which can help increase transaction throughput and is used to enable [conservative mode of in-order parallel replication](parallel-replication.md#conservative-mode-of-in-order-parallel-replication).\
  With [group commit for the binary log](../../server-management/server-monitoring-logs/binary-log/group-commit-for-the-binary-log.md), the server can delay flushing a committed transaction into [binary log](../../server-management/server-monitoring-logs/binary-log/) until the given number of transactions are ready to be flushed as a group. The delay will however not be longer\
  than the value set by [binlog\_commit\_wait\_usec](replication-and-binary-log-system-variables.md#binlog_commit_wait_usec).\
  The default value of 0 means that no delay is introduced.\
  Setting this value can reduce I/O on the binary log and give an increased opportunity for parallel apply on the replica when [conservative mode of in-order parallel replication](parallel-replication.md#conservative-mode-of-in-order-parallel-replication) is enabled, but too high a value will decrease the transaction throughput. By monitoring the status variable [binlog\_group\_commit\_trigger\_count](replication-and-binary-log-status-variables.md#binlog_group_commit_trigger_count) (>=[MariaDB 10.1.5](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/mariadb-10-1-5-release-notes)) it is possible to see how often this is occurring.
* Starting with [MariaDB 10.0.18](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-0-series/mariadb-10018-release-notes) and [MariaDB 10.1.4](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/mariadb-10-1-4-release-notes):\
  If the server detects that one of the committing transactions T1 holds an[InnoDB](../../reference/storage-engines/innodb/) row lock that another transaction T2 is waiting for, then the\
  commit will complete immediately without further delay. This helps avoid\
  losing throughput when many transactions need conflicting locks. This often\
  makes it safe to use this option without losing\
  throughput on a replica with [conservative mode of in-order parallel replication](parallel-replication.md#conservative-mode-of-in-order-parallel-replication), provided the value of[slave\_parallel\_threads](replication-and-binary-log-system-variables.md#slave_parallel_threads) is sufficiently high.
* Commandline: `--binlog-commit-wait-count=#]`
* Scope: Global
* Dynamic: Yes
* Data Type: `numeric`
* Default Value: `0`
* Range: `0` to `18446744073709551615`

#### `binlog_commit_wait_usec`

* Description: Configures the behavior of [group commit for the binary log](../../server-management/server-monitoring-logs/binary-log/group-commit-for-the-binary-log.md), which can help increase transaction throughput and is used to enable [conservative mode of in-order parallel replication](parallel-replication.md#conservative-mode-of-in-order-parallel-replication).\
  With [group commit for the binary log](../../server-management/server-monitoring-logs/binary-log/group-commit-for-the-binary-log.md), the server can delay flushing a committed transaction into [binary log](../../server-management/server-monitoring-logs/binary-log/) until the transaction has waited the configured number of microseconds. By monitoring the status variable [binlog\_group\_commit\_trigger\_timeout](replication-and-binary-log-status-variables.md#binlog_group_commit_trigger_timeout) (>=[MariaDB 10.1.5](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/mariadb-10-1-5-release-notes)) it is possible to see how often group commits are made due to `binlog_commit_wait_usec`. As soon as the number of pending commits reaches [binlog\_commit\_wait\_count](replication-and-binary-log-system-variables.md#binlog_commit_wait_count), the wait will be terminated, though. Thus, this setting only takes effect if `binlog_commit_wait_count` is non-zero.
* Commandline: `--binlog-commit-wait-usec#`
* Scope: Global
* Dynamic: Yes
* Data Type: `numeric`
* Default Value: `100000`
* Range: `0` to `18446744073709551615`

#### `binlog_direct_non_transactional_updates`

* Description: [Replication](broken-reference) inconsistencies can occur due when a transaction updates both transactional and non-transactional tables and the updates to the non-transactional tables are visible before being written to the binary log. This is because, to preserve causality, the non-transactional statements are written to the transaction cache, which is only flushed on commit. Setting binlog\_direct\_non\_transactional\_updates to 1 (0 is default) will cause non-transactional tables to be written straight to the binary log, rather than the transaction cache. This setting has no effect when row-based binary logging is used, as it requires statement-based logging. See [binlog\_format](replication-and-binary-log-system-variables.md#binlog_format). Use with care, and only in situations where no dependencies exist between the non-transactional and transactional tables, for example INSERTing into a non-transactional table based upon the results of a SELECT from a transactional table.
* Commandline: `--binlog-direct-non-transactional-updates[=value]`
* Scope: Global, Session
* Dynamic: Yes
* Data Type: `boolean`
* Default Value: `OFF (0)`

#### `binlog_do_db`

* Description: This option allows you to configure a [replication primary](broken-reference) to write statements and transactions affecting databases that match a specified name into its [binary log](../../server-management/server-monitoring-logs/binary-log/). Since the filtered statements or transactions will not be present in the [binary log](../../server-management/server-monitoring-logs/binary-log/), its replicas will not be able to replicate them.
  * This option will not work with cross-database updates with [statement-based logging](../../server-management/server-monitoring-logs/binary-log/binary-log-formats.md#statement-based-logging). See the [Statement-Based Logging](replication-filters.md#statement-based-logging) section for more information.
  * Until [MariaDB 11.2.0](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-11-2-series/mariadb-11-2-0-release-notes), only available as an option, not a system variable. This option can not be set dynamically.
  * When setting it on the command-line or in a server [option group](../../server-management/install-and-upgrade-mariadb/configuring-mariadb/configuring-mariadb-with-option-files.md#option-groups) in an [option file](../../server-management/install-and-upgrade-mariadb/configuring-mariadb/configuring-mariadb-with-option-files.md), the option does not accept a comma-separated list. If you would like to specify multiple filters, then you need to specify the option multiple times.
  * See [Replication Filters](replication-filters.md) for more information.
* Commandline: `--binlog-do-db=#`
* Scope: Global
* Dynamic: No
* Data Type: `string`
* Default Value: NULL
* Introduced: [MariaDB 11.2.0](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-11-2-series/mariadb-11-2-0-release-notes) (as a system variable)

#### `binlog_expire_logs_seconds`

* Description: If non-zero, binary logs will be purged after `binlog_expire_logs_seconds` seconds. Possible purges happen at startup and at binary log rotation. From [MariaDB 10.6.1](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-10-6-series/mariadb-1061-release-notes), `binlog_expire_logs_seconds` and [expire\_logs\_days](replication-and-binary-log-system-variables.md#expire_logs_days) are forms of aliases, such that changes to one automatically reflect in the other.
* Commandline: `--binlog-expire-logs-seconds=#`
* Scope: Global
* Dynamic: Yes
* Data Type: `numeric`
* Default Value: `0`
* Range: `0` to `8553600`
* Introduced: [MariaDB 10.6.1](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-10-6-series/mariadb-1061-release-notes)

#### `binlog_file_cache_size`

* Description: Size of in-memory cache that is allocated when reading [binary log](../../server-management/server-monitoring-logs/binary-log/) and [relay log](../../server-management/server-monitoring-logs/binary-log/relay-log.md) files.
* Commandline: `--binlog-file-cache-size=#`
* Scope: Global, Session
* Dynamic: Yes
* Data Type: `numeric`
* Default Value: `16384`
* Range: `8192` to `18446744073709551615`
* Introduced: [MariaDB 10.3.3](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-3-series/mariadb-1033-release-notes)

#### `binlog_format`

* Description: Determines whether [replication](broken-reference) is row-based, statement-based or mixed. Statement-based was the default until [MariaDB 10.2.3](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/mariadb-1023-release-notes). Be careful of changing the binary log format when a replication environment is already running. See [Binary Log Formats](../../server-management/server-monitoring-logs/binary-log/binary-log-formats.md). Starting from [MariaDB 10.0.22](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-0-series/mariadb-10022-release-notes) a replica will apply any events it gets from the primary, regardless of the binary log format. `binlog_format` only applies to normal (not replicated) updates.
* Commandline: `--binlog-format=format`
* Scope: Global, Session
* Dynamic: Yes
* Data Type: `enumeration`
* Default Value:
  * `MIXED` (>= [MariaDB 10.2.4](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/mariadb-1024-release-notes))
  * `STATEMENT` (<= [MariaDB 10.2.3](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/mariadb-1023-release-notes))
* Valid Values: `ROW`, `STATEMENT` or `MIXED`

#### `binlog_gtid_index`

* Description: Enable the creation of a GTID index for every binlog file, and the use of such index for speeding up GTID lookup in the binlog. See [Binlog indexing](gtid.md#binlog-indexing).
* Commandline: `--binlog-gtid-index{=0|1}`
* Scope: Global
* Dynamic: Yes
* Data Type: `boolean`
* Default Value: `ON`
* Introduced: [MariaDB 11.4](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-11-4-series/what-is-mariadb-114)

#### `binlog_gtid_index_page_size`

* Description: Page size to use for the binlog GTID index. See [Binlog indexing](gtid.md#binlog-indexing).
* Commandline: `--binlog-gtid-index-page-size=#`
* Scope: Global
* Dynamic: Yes
* Data Type: `numeric`
* Default Value: `4096`
* Range: `64` to `16777216`
* Introduced: [MariaDB 11.4](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-11-4-series/what-is-mariadb-114)

#### `binlog_gtid_index_span_min`

* Description: Control sparseness of the binlog GTID index. If set to N, at most one index record will be added for every N bytes of binlog file written, to reduce the size of the index. Normally does not need tuning. See [Binlog indexing](gtid.md#binlog-indexing).
* Commandline: `--binlog-gtid-index-span-min=#`
* Scope: Global
* Dynamic: Yes
* Data Type: `numeric`
* Default Value: `65536`
* Range: `1` to `1073741824`
* Introduced: [MariaDB 11.4](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-11-4-series/what-is-mariadb-114)

#### `binlog_ignore_db`

* Description: This option allows you to configure a [replication primary](broken-reference) to not write statements and transactions affecting databases that match a specified name into its [binary log](../../server-management/server-monitoring-logs/binary-log/). Since the filtered statements or transactions will not be present in the [binary log](../../server-management/server-monitoring-logs/binary-log/), its replicas will not be able to replicate them.
  * This option will not work with cross-database updates with [statement-based logging](../../server-management/server-monitoring-logs/binary-log/binary-log-formats.md#statement-based-logging). See the [Statement-Based Logging](replication-filters.md#statement-based-logging) section for more information.
  * Until [MariaDB 11.2.0](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-11-2-series/mariadb-11-2-0-release-notes), only available as an option, not a system variable. This option can not be set dynamically.
  * When setting it on the command-line or in a server [option group](../../server-management/install-and-upgrade-mariadb/configuring-mariadb/configuring-mariadb-with-option-files.md#option-groups) in an [option file](../../server-management/install-and-upgrade-mariadb/configuring-mariadb/configuring-mariadb-with-option-files.md), the option does not accept a comma-separated list. If you would like to specify multiple filters, then you need to specify the option multiple times.
  * See [Replication Filters](replication-filters.md) for more information.
* Commandline: `--binlog-ignore-db=name`
* Scope: Global
* Dynamic: No
* Data Type: `string`
* Default Value: NULL
* Introduced: [MariaDB 11.2.0](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-11-2-series/mariadb-11-2-0-release-notes)

#### `binlog_large_commit_threshold`

* Description: Increases transaction concurrency for large transactions (i.e. those with sizes larger than this value) by using the large transaction's cache file as a new binary log, and rotating the active binary log to the large transaction's cache file at commit time. This avoids the default commit logic that copies the transaction cache data to the end of the active binary log file while holding a lock that prevents other transactions from binlogging.
* Commandline: `--binlog-large-commit-threshold=val`
* Scope: Global
* Dynamic: Yes
* Data Type: `bigint unsigned`
* Default Value: `134217728`
* Range: `10485760` to `18446744073709551615`
* Introduced: [MariaDB 11.7](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-11-7-rolling-releases/what-is-mariadb-117)

#### `binlog_legacy_event_pos`

* Description: Fill in the end\_log\_pos field of _all_ events in the binlog, even when doing so costs performance. Can be used in case some old application needs it for backwards compatibility. Setting this option can hurt binlog scalability.
* Commandline: `--binlog-legacy-event-pos{=0|1}`
* Scope: Global
* Dynamic: Yes
* Data Type: `boolean`
* Default Value: `OFF`
* Introduced: [MariaDB 11.4](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-11-4-series/what-is-mariadb-114)

#### `binlog_optimize_thread_scheduling`

* Description: Run fast part of group commit in a single thread, to optimize kernel thread scheduling. On by default. Disable to run each transaction in group commit in its own thread, which can be slower at very high concurrency. This option is mostly for testing one algorithm versus another, and it should not normally be necessary to change it. Deprecated in [MariaDB 11.7](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-11-7-rolling-releases/what-is-mariadb-117), as the option was initially added to provide a safe alternative for the newly added binlog group commit logic, such that when 0, it would disable a leader thread\
  from performing the binlog write for all transactions that are a part of the group commit. Problems related to the binlog group commit optimization are expected to be addressed by now, so the option has been deprecated and will be removed in future.
* Commandline: `--binlog-optimize-thread-scheduling` or `--skip-binlog-optimize-thread-scheduling`
* Scope: Global
* Dynamic: No
* Data Type: `boolean`
* Default Value: `ON`
* Deprecated: [MariaDB 11.7](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-11-7-rolling-releases/what-is-mariadb-117)

#### `binlog_row_event_max_size`

* Description: The maximum size of a row-based [binary log](../../server-management/server-monitoring-logs/binary-log/) event in bytes. Rows will be grouped into events smaller than this size if possible. The value has to be a multiple of 256. Until [MariaDB 11.2.0](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-11-2-series/mariadb-11-2-0-release-notes), only available as an option, not a system variable.
* Commandline: `--binlog-row-event-max-size=val`
* Scope: Global, Session
* Dynamic: Yes
* Data Type: `numeric`
* Default Value: `8192`
* Range: `256` to `4294967040` (in multiples of 256)
* Introduced: [MariaDB 11.2.0](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-11-2-series/mariadb-11-2-0-release-notes)

#### `binlog_row_image`

* Description: Controls the logging format in [row-based](../../server-management/server-monitoring-logs/binary-log/binary-log-formats.md#row-based) [replication](broken-reference). In row-based replication (the variable has no effect with [statement-based replication](../../server-management/server-monitoring-logs/binary-log/binary-log-formats.md#statement-based)), each row change event contains an image for matching against when choosing the row to be updated, and another image containing the changes. Before the introduction of this variable, all columns were logged for both of these images. In certain circumstances, this is not necessary, and memory, disk and network resources can be saved by partial logging. Note that to safely change this setting from the default, the table being replicated to must contain identical primary key definitions, and columns must be present, in the same order, and use the same data types as the original table. If these conditions are not met, matches may not be correctly determined and updates and deletes may diverge on the replica, with no warnings or errors returned.
  * `FULL`: All columns in the before and after image are logged. This is the default, and the only behavior in earlier versions.
  * `NOBLOB`: mariadbd avoids logging blob and text columns whenever possible (eg, blob column was not changed or is not part of primary key).
  * `MINIMAL`: A PK equivalent (PK columns or full row if there is no PK in the table) is logged in the before image, and only changed columns are logged in the after image.
  * `FULL_NODUP`: All columns are logged in the before image, but only changed columns or all columns of inserted record are logged in the after image. This is essentially the same as `FULL`, but takes less space. From [MariaDB 11.4](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-11-4-series/what-is-mariadb-114).
* Commandline: `--binlog-row-image=value`
* Scope: Global, Session
* Dynamic: Yes
* Data Type: `enum`
* Default Value: `FULL`
* Valid Values:
  * <= [MariaDB 11.3](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-11-3-rolling-releases/what-is-mariadb-113): `FULL`, `NOBLOB` or `MINIMAL`
  * > \= [MariaDB 11.4](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-11-4-series/what-is-mariadb-114): `FULL`, `NOBLOB`, `MINIMAL` or `FULL_NODUP`

#### `binlog_row_metadata`

* Description: Controls the format used for binlog metadata logging.
  * `NO_LOG`: No metadata is logged (default).
  * `MINIMAL`: Only metadata required by a replica is logged.
  * `FULL`: All metadata is logged.
* Commandline: `--binlog-row-metadata=value`
* Scope: Global
* Dynamic: Yes
* Data Type: `enum`
* Default Value: `NO_LOG`
* Valid Values: `NO_LOG`, `MINIMAL`, `FULL`
* Introduced: [MariaDB 10.5.0](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-10-5-series/mariadb-1050-release-notes)

#### `binlog_space_limit`

* Description: Alias for [max\_binlog\_total\_size](replication-and-binary-log-system-variables.md#max_binlog_total_size).
* Introduced: [MariaDB 11.4](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-11-4-series/what-is-mariadb-114)

#### `binlog_stmt_cache_size`

* Description: If the [binary log](../../server-management/server-monitoring-logs/binary-log/) is active, this variable determines the size in bytes of the cache holding a record of binary log changes outside of a transaction. The variable [binlog\_cache\_size](replication-and-binary-log-system-variables.md#binlog_cache_size), determines the cache size for binary log statements inside a transaction. The [binlog\_stmt\_cache\_disk\_use](../optimization-and-tuning/system-variables/server-status-variables.md#binlog_stmt_cache_disk_use) and [binlog\_stmt\_cache\_use](../optimization-and-tuning/system-variables/server-status-variables.md#binlog_stmt_cache_use) [server status variables](../optimization-and-tuning/system-variables/server-status-variables.md) will indicate whether this variable needs to be increased (you want a low ratio of binlog\_stmt\_cache\_disk\_use to binlog\_stmt\_cache\_use).
* Commandline: `--binlog-stmt-cache-size=#`
* Scope: Global
* Dynamic: Yes
* Data Type: `numeric`
* Default Value: `32768`
* Range - 32 bit: `4096` to `4294967295`
* Range - 64 bit: `4096` to `18446744073709547520`

#### `default_master_connection`

* Description: In [multi-source replication](multi-source-replication.md), specifies which connection will be used for commands and variables if you don't specify a connection.
* Commandline: None
* Scope: Session
* Dynamic: Yes
* Data Type: `string`
* Default Value: `''` (empty string)

#### `encrypt_binlog`

* Description: Encrypt [binary logs](../../server-management/server-monitoring-logs/binary-log/) (including [relay logs](../../server-management/server-monitoring-logs/binary-log/relay-log.md)). See [Data at Rest Encryption](../../security/securing-mariadb/securing-mariadb-encryption/encryption-data-at-rest-encryption/data-at-rest-encryption-overview.md) and [Encrypting Binary Logs](../../security/securing-mariadb/securing-mariadb-encryption/encryption-data-at-rest-encryption/encrypting-binary-logs.md).
* Commandline: `--encrypt-binlog[={0|1}]`
* Scope: Global
* Dynamic: No
* Data Type: `boolean`
* Default Value: `OFF`

#### `expire_logs_days`

* Description: Number of days after which the [binary log](../../server-management/server-monitoring-logs/binary-log/) can be automatically removed. By default 0, or no automatic removal. When using [replication](broken-reference), should always be set higher than the maximum lag by any replica. Removals take place when the server starts up, when the binary log is flushed, when the next binary log is created after the previous one reaches the maximum size, or when running [PURGE BINARY LOGS](../../reference/sql-statements/administrative-sql-statements/purge-binary-logs.md). Units are whole days (integer) until [MariaDB 10.6.0](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-10-6-series/mariadb-1060-release-notes), or 1/1000000 precision (double) from [MariaDB 10.6.1](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-10-6-series/mariadb-1061-release-notes).Starting from [MariaDB 10.6.1](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-10-6-series/mariadb-1061-release-notes), `expire_logs_days` and [binlog\_expire\_logs\_seconds](replication-and-binary-log-system-variables.md#binlog_expire_logs_seconds) are forms of aliases, such that changes to one automatically reflect in the other.
* Commandline: `--expire-logs-days=#`
* Scope: Global
* Dynamic: Yes
* Data Type: `numeric`
* Default Value: `0.000000` (>= [MariaDB 10.6.1](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-10-6-series/mariadb-1061-release-notes)), `0` (<= [MariaDB 10.6.0](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-10-6-series/mariadb-1060-release-notes))
* Range: `0` to `99`

#### `init_slave`

* Description: Similar to [init\_connect](../optimization-and-tuning/system-variables/server-system-variables.md#init_connect), but the string contains one or more SQL statements, separated by semicolons, that will be executed by a replica server each time the SQL thread starts. These statements are only executed after the acknowledgement is sent to the replica and [START SLAVE](../../reference/sql-statements/administrative-sql-statements/replication-statements/start-replica.md) completes.
* Commandline: `--init-slave=name`
* Scope: Global
* Dynamic: Yes
* Data Type: `string`
* Related variables: `[init_connect](../optimization-and-tuning/system-variables/server-system-variables.md#init_connect)`

#### `log_bin`

* Description: Whether [binary logging](../../server-management/server-monitoring-logs/binary-log/) is enabled or not. If the --log-bin [option](../../server-management/starting-and-stopping-mariadb/mariadbd-options.md) is used, log\_bin will be set to ON, otherwise it will be OFF. If no `name` option is given for `--log-bin`, `datadir/'log-basename'-bin` or `'datadir'/mysql-bin` will be used (the latter if [--log-basename](../../server-management/starting-and-stopping-mariadb/mariadbd-options.md#-log-basename) is not specified). We strongly recommend you use either `--log-basename` or specify a filename to ensure that [replication](broken-reference) doesn't stop if the real hostname of the computer changes. The name option can optionally include an absolute path. If no path is specified, the log will be written to the [data directory](../optimization-and-tuning/system-variables/server-system-variables.md#datadir). The name can optionally include the file extension; it will be stripped and only the file basename will be used.
* Commandline: `--log-bin[=name]`
* Scope: Global
* Dynamic: No
* Data Type: `boolean`
* Default Value: `OFF`
* Related variables: `[sql_log_bin](replication-and-binary-log-system-variables.md#sql_log_bin)`

#### `log_bin_basename`

* Description: The full path of the binary log file names, excluding the extension. Its value is derived from the rules specified in `log_bin` system variable. This is a read-only variable only, there is no corresponding configuration file setting or command line option by the same name, use `log_bin` to set the basename path instead.
* Commandline: `No commandline option`
* Scope: Global
* Dynamic: No
* Data Type: `string`
* Default Value: None
* Dynamic: `No`

#### `log_bin_compress`

* Description: Whether or not the binary log can be compressed. `0` (the default) means no compression. See [Compressing Events to Reduce Size of the Binary Log](../../server-management/server-monitoring-logs/binary-log/compressing-events-to-reduce-size-of-the-binary-log.md).
* Commandline: `--log-bin-compress`
* Scope: Global
* Dynamic: Yes
* Data Type: `boolean`
* Default Value: `OFF`

#### `log_bin_compress_min_len`

* Description: Minimum length of sql statement (in statement mode) or record (in row mode) that can be compressed. See [Compressing Events to Reduce Size of the Binary Log](../../server-management/server-monitoring-logs/binary-log/compressing-events-to-reduce-size-of-the-binary-log.md).
* Commandline: `--log-bin-compress-min-len`
* Scope: Global
* Dynamic: Yes
* Data Type: `numeric`
* Default Value: `256`
* Range: `10` to `1024`

#### `log_bin_index`

* Description: File that holds the names for last binlog files. If [--log-basename](../../server-management/starting-and-stopping-mariadb/mariadbd-options.md#-log-basename) is also set, `log_bin_index` should be placed after in the config files. Later settings override earlier settings, so `log-basename` will override any earlier log file name settings.
* Commandline: `--log-bin-index=name`
* Scope: Global
* Dynamic: No
* Data Type: `string`
* Default Value: None

#### `log_bin_trust_function_creators`

* Description: Functions and triggers can be dangerous when used with [replication](./). Certain types of functions and triggers may have unintended consequences when the statements are applied on a replica. For that reason, there are some restrictions on the creation of functions and triggers when the [binary log](../../server-management/server-monitoring-logs/binary-log/) is enabled by default, such as:
  * When `log_bin_trust_function_creators` is `OFF` and `[log_bin](#log_bin)` is `ON`, `[CREATE FUNCTION](../../../reference/sql-statements-and-structure/sql-statements/data-definition/create/create-function.md)` and `[ALTER FUNCTION](../../../reference/sql-statements-and-structure/sql-statements/data-definition/alter/alter-function.md)` statements will trigger an error if the function is defined with any of the `NOT DETERMINISTIC`, `CONTAINS SQL` or `MODIFIES SQL DATA` characteristics.
  * This means that when `log_bin_trust_function_creators` is `OFF` and `[log_bin](#log_bin)` is `ON`, `[CREATE FUNCTION](../../../reference/sql-statements-and-structure/sql-statements/data-definition/create/create-function.md)` and `[ALTER FUNCTION](../../../reference/sql-statements-and-structure/sql-statements/data-definition/alter/alter-function.md)` statements will only succeed if the function is defined with any of the `DETERMINISTIC`, `NO SQL`, or `READS SQL DATA` characteristics.
  * When `log_bin_trust_function_creators` is `OFF` and `[log_bin](#log_bin)` is `ON`, the `[SUPER](../../../reference/sql-statements-and-structure/sql-statements/account-management-sql-commands/grant.md#global-privileges)` privilege is also required to execute the following statements:
    * `[CREATE FUNCTION](../../../reference/sql-statements-and-structure/sql-statements/data-definition/create/create-function.md)`
    * `[CREATE TRIGGER](../../programming-customizing-mariadb/triggers-events/triggers/create-trigger.md)`
    * `[DROP TRIGGER](../../../reference/sql-statements-and-structure/sql-statements/data-definition/drop/drop-trigger.md)`
  * Setting `log_bin_trust_function_creators` to `ON` removes these requirements around functions characteristics and the `[SUPER](../../../reference/sql-statements-and-structure/sql-statements/account-management-sql-commands/grant.md#global-privileges)` privileges.
  * See [Binary Logging of Stored Routines](../../server-usage/stored-routines/binary-logging-of-stored-routines.md) for more information.
* Commandline: `--log-bin-trust-function-creators[={0|1}]`
* Scope: Global
* Dynamic: Yes
* Data Type: `boolean`
* Default Value: `OFF`

#### `log_slow_slave_statements`

* Description: Log slow statements executed by replica thread to the [slow log](../../server-management/server-monitoring-logs/slow-query-log/) if it is open. Before [MariaDB 10.1.13](broken-reference), this was only available as a mariadbd option, not a server variable.
* Commandline: `--log-slow-slave-statements`
* Scope: Global
* Dynamic: Yes
* Data Type: `boolean`
* Default Value:
  * `ON` (>= [MariaDB 10.2.4](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/mariadb-1024-release-notes))
  * `OFF` (<= [MariaDB 10.2.3](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/mariadb-1023-release-notes))

#### `log_slave_updates`

* Description: If set to `0`, the default, updates on a replica received from a primary during [replication](broken-reference) are not logged in the replica's binary log. If set to `1`, they are. The replica's binary log needs to be enabled for this to have an effect. Set to `1` if you want to daisy-chain the replicas.
* Commandline: `--log-slave-updates`
* Scope: Global
* Dynamic: No
* Data Type: `boolean`
* Default Value: `OFF`

#### `master_verify_checksum`

* Description: Verify [binlog checksums](binlog-event-checksums.md) when reading events from the binlog on the primary.
* Commandline: `--master-verify-checksum=[0|1]`
* Scope: Global
* Access Type: Can be changed dynamically
* Data Type: `bool`
* Default Value: `OFF (0)`

#### `max_binlog_cache_size`

* Description: Restricts the size in bytes used to cache a multi-transactional query. If more bytes are required, a `Multi-statement transaction required more than 'max_binlog_cache_size' bytes of storage` error is generated. If the value is changed, current sessions are unaffected, only sessions started subsequently. See [max\_binlog\_stmt\_cache\_size](replication-and-binary-log-system-variables.md#max_binlog_stmt_cache_size) and [binlog\_cache\_size](replication-and-binary-log-system-variables.md#binlog_cache_size).
* Commandline: `--max-binlog-cache-size=#`
* Scope: Global
* Dynamic: Yes
* Data Type: `numeric`
* Default Value: `18446744073709547520`
* Range: `4096` to `18446744073709547520`

#### `max_binlog_size`

* Description: If the [binary log](../../server-management/server-monitoring-logs/binary-log/) exceeds this size in bytes after a write, the server rotates it by closing it and opening a new binary log. Single transactions will always be stored in the same binary log, so the server will wait for open transactions to complete before rotating. This figure also applies to the size of [relay logs](../../server-management/server-monitoring-logs/binary-log/relay-log.md) if [max\_relay\_log\_size](replication-and-binary-log-system-variables.md#max_relay_log_size) is set to zero.
* Commandline: `--max-binlog-size=#`
* Scope: Global
* Dynamic: Yes
* Data Type: `numeric`
* Default Value: `1073741824` (1GB)
* Range: `4096` to `1073741824` (4KB to 1GB)

#### `max_binlog_stmt_cache_size`

* Description: Restricts the size used to cache non-transactional statements. See [max\_binlog\_cache\_size](replication-and-binary-log-system-variables.md#max_binlog_cache_size) and [binlog\_stmt\_cache\_size](replication-and-binary-log-system-variables.md#binlog_stmt_cache_size).
* Commandline: `--max-binlog-stmt-cache-size=#`
* Scope: Global
* Dynamic: Yes
* Data Type: `numeric`
* Default Value: `18446744073709547520` (64 bit), `4294963200` (32 bit)
* Range: `4096` to `18446744073709547520`

#### `max_binlog_total_size`

* Description: Maximum space in bytes to use for all [binary logs](../../server-management/server-monitoring-logs/binary-log/). Extra logs are deleted on server start, log rotation, FLUSH LOGS or when writing to binlog. Default is 0, which means no size restrictions. See also [slave\_connections\_needed\_for\_purge](replication-and-binary-log-system-variables.md#slave_connections_needed_for_purge).
* Commandline: `--max-binlog-size=#`
* Scope: Global
* Dynamic: Yes
* Data Type: `numeric`
* Default Value: `0`
* Range: `0` to `18446744073709551615`
* Introduced: [MariaDB 11.4](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-11-4-series/what-is-mariadb-114)

#### `max_relay_log_size`

* Description: Replica will rotate its [relay log](../../server-management/server-monitoring-logs/binary-log/relay-log.md) if it exceeds this size after a write. If set to 0, the [max\_binlog\_size](replication-and-binary-log-system-variables.md#max_binlog_size) setting is used instead. Previously global only, since the implementation of [multi-source replication](multi-source-replication.md), it can be set per session as well.
* Commandline: `--max-relay-log-size=#`
* Scope: Global, Session
* Dynamic: Yes
* Data Type: `numeric`
* Default Value: `0`
* Range: `0`, or `4096 to 1073741824` (4KB to 1GB)

#### `read_binlog_speed_limit`

* Description: Used to restrict the speed at which a [replica](broken-reference) can read the binlog from the primary. This can be used to reduce the load on a primary if many replicas need to download large amounts of old binlog files at the same time. The network traffic will be restricted to the specified number of kilobytes per second.
* Commandline: `--read-binlog-speed-limit=#`
* Scope: Global
* Dynamic: Yes
* Data Type: `numeric`
* Default Value: `0` (no limit)
* Range: `0` to `18446744073709551615`

#### `relay_log`

* Description: [Relay log](../../server-management/server-monitoring-logs/binary-log/relay-log.md) basename. If not set, the basename of the files will be `hostname-relay-bin`, or derived from [--log-basename](../../server-management/starting-and-stopping-mariadb/mariadbd-options.md#-log-basename). If [--log-basename](../../server-management/starting-and-stopping-mariadb/mariadbd-options.md#-log-basename) is also set, `relay_log` should be placed after in the config files. Later settings override earlier settings, so `log-basename` will override any earlier log file name settings.
* Commandline: `--relay-log=file_name`
* Scope: Global
* Dynamic: No
* Data Type: `filename`
* Default Value: `''` (none)

#### `relay_log_basename`

* Description: The full path of the relay log file names, excluding the extension. Its value is derived from the [relay-log](replication-and-binary-log-system-variables.md#relay_log) variable value.
* Commandline: `No commandline option`
* Scope: Global
* Dynamic: No
* Data Type: `string`
* Default Value: None
* Dynamic: `No`

#### `relay_log_index`

* Description: Name and location of the [relay log](../../server-management/server-monitoring-logs/binary-log/relay-log.md) index file, the file that keeps a list of the last relay logs. Defaults to hostname-relay-bin.index, or derived from [--log-basename](../../server-management/starting-and-stopping-mariadb/mariadbd-options.md#-log-basename). If [--log-basename](../../server-management/starting-and-stopping-mariadb/mariadbd-options.md#-log-basename) is also set, `relay_log_index` should be placed after in the config files. Later settings override earlier settings, so `log-basename` will override any earlier log file name settings.
* Commandline: `--relay-log-index=name`
* Scope: Global
* Dynamic: No
* Data Type: `string`
* Default Value: None

#### `relay_log_info_file`

* Description: Name and location of the file where the `RELAY_LOG_FILE` and `RELAY_LOG_POS` options (i.e. the [relay log](../../server-management/server-monitoring-logs/binary-log/relay-log.md) position) for the [CHANGE MASTER](../../reference/sql-statements/administrative-sql-statements/replication-statements/change-master-to.md) statement are written. The [replica's SQL thread](replication-threads.md#slave-sql-thread) keeps this [relay log](../../server-management/server-monitoring-logs/binary-log/relay-log.md) position updated as it applies events.
  * See [CHANGE MASTER TO: Option Persistence](../../reference/sql-statements/administrative-sql-statements/replication-statements/change-master-to.md#option-persistence) for more information.
* Commandline: `--relay-log-info-file=file_name`
* Scope: Global
* Dynamic: No
* Data Type: `string`
* Default Value: `relay-log.info`

#### `relay_log_purge`

* Description: If set to `1` (the default), [relay logs](../../server-management/server-monitoring-logs/binary-log/relay-log.md) will be purged as soon as they are no longer necessary.
* Commandline: `--relay-log-purge={0|1}`
* Scope: Global
* Dynamic: Yes
* Data Type: `boolean`
* Default Value: `ON`
* Note: In MySQL and in MariaDB before version 10.0.8 this variable was silently changed if you did [CHANGE MASTER](../../reference/sql-statements/administrative-sql-statements/replication-statements/change-master-to.md).

#### `relay_log_recovery`

* Description: If set to `1` (`0` is default), on startup the replica will drop all [relay logs](../../server-management/server-monitoring-logs/binary-log/relay-log.md) that haven't yet been processed, and retrieve relay logs from the primary. Can be useful after the replica has crashed to prevent the processing of corrupt relay logs. relay\_log\_recovery should always be set together with [relay\_log\_purge](replication-and-binary-log-system-variables.md#relay_log_purge). Setting `relay-log-recovery=1` with `relay-log-purge=0` can cause the relay log to be read from files that were not purged, leading to data inconsistencies.
* Commandline: `--relay-log-recovery`
* Scope: Global
* Dynamic: Yes
* Data Type: `boolean`
* Default Value: `OFF`

#### `relay_log_space_limit`

* Description: Specifies the maximum space to be used for the [relay logs](../../server-management/server-monitoring-logs/binary-log/relay-log.md). The IO thread will stop until the SQL thread has cleared the backlog. By default `0`, or no limit.
* Commandline: `--relay-log-space-limit=#`
* Scope: Global
* Dynamic: No
* Data Type: `numeric`
* Default Value: `0`
* Range - 32 bit: `0` to `4294967295`
* Range - 64 bit: `0` to `18446744073709547520`

#### `replicate_annotate_row_events`

* Description: Tells the replica to reproduce [annotate\_rows\_events](../../clients-and-utilities/mariadb-binlog/annotate_rows_log_event.md) received from the primary in its own binary log. This option is sensible only when used in tandem with the [log\_slave\_updates](replication-and-binary-log-system-variables.md#log_slave_updates) option.
* Commandline: `--replicate-annotate-row-events`
* Scope: Global
* Dynamic: No
* Data Type: `boolean`
* Default Value:
  * `ON` (>= [MariaDB 10.2.4](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/mariadb-1024-release-notes))
  * `OFF` (<= [MariaDB 10.2.3](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/mariadb-1023-release-notes))

#### `replicate_do_db`

* Description: This system variable allows you to configure a [replica](broken-reference) to apply statements and transactions affecting databases that match a specified name.
  * This system variable will not work with cross-database updates with [statement-based logging](../../server-management/server-monitoring-logs/binary-log/binary-log-formats.md#statement-based-logging). See the [Statement-Based Logging](replication-filters.md#statement-based-logging) section for more information.
  * When setting it dynamically with `[SET GLOBAL](../../../reference/sql-statements-and-structure/sql-statements/administrative-sql-statements/set-commands/set.md#global-session)`, the system variable accepts a comma-separated list of filters.
  * When setting it on the command-line or in a server [option group](../../server-management/install-and-upgrade-mariadb/configuring-mariadb/configuring-mariadb-with-option-files.md#option-groups) in an [option file](../../server-management/install-and-upgrade-mariadb/configuring-mariadb/configuring-mariadb-with-option-files.md), the system variable does not accept a comma-separated list. If you would like to specify multiple filters, then you need to specify the system variable multiple times.
  * See [Replication Filters](replication-filters.md) for more information.
* Commandline: `--replicate-do-db=name`
* Scope: Global
* Dynamic: Yes
* Data Type: `string`
* Default Value: `''` (empty)

#### `replicate_do_table`

* Description: This system variable allows you to configure a [replica](broken-reference) to apply statements and transactions that affect tables that match a specified name. The table name is specified in the format: `dbname.tablename`.
  * This system variable will not work with cross-database updates with [statement-based logging](../../server-management/server-monitoring-logs/binary-log/binary-log-formats.md#statement-based-logging). See the [Statement-Based Logging](replication-filters.md#statement-based-logging) section for more information.
  * When setting it dynamically with `[SET GLOBAL](../../../reference/sql-statements-and-structure/sql-statements/administrative-sql-statements/set-commands/set.md#global-session)`, the system variable accepts a comma-separated list of filters.
  * When setting it on the command-line or in a server [option group](../../server-management/install-and-upgrade-mariadb/configuring-mariadb/configuring-mariadb-with-option-files.md#option-groups) in an [option file](../../server-management/install-and-upgrade-mariadb/configuring-mariadb/configuring-mariadb-with-option-files.md), the system variable does not accept a comma-separated list. If you would like to specify multiple filters, then you need to specify the system variable multiple times.
  * See [Replication Filters](replication-filters.md) for more information.
* Commandline: `--replicate-do-table=name`
* Scope: Global
* Dynamic: Yes
* Data Type: `string`
* Default Value: `''` (empty)

#### `replicate_events_marked_for_skip`

* Description: Tells the replica whether to [replicate](broken-reference) events that are marked with the `@@skip_replication` flag. See [Selectively skipping replication of binlog events](selectively-skipping-replication-of-binlog-events.md) for more information.
* Commandline: `--replicate-events-marked-for-skip`
* Scope: Global
* Dynamic: Yes
* Data Type: `enumeration`
* Default Value: `replicate`
* Valid Values: `REPLICATE`, `FILTER_ON_SLAVE`, `FILTER_ON_MASTER`

#### `replicate_ignore_db`

* Description: This system variable allows you to configure a [replica](broken-reference) to ignore statements and transactions affecting databases that match a specified name.
  * This system variable will not work with cross-database updates with [statement-based logging](../../server-management/server-monitoring-logs/binary-log/binary-log-formats.md#statement-based-logging). See the [Statement-Based Logging](replication-filters.md#statement-based-logging) section for more information.
  * When setting it dynamically with `[SET GLOBAL](../../../reference/sql-statements-and-structure/sql-statements/administrative-sql-statements/set-commands/set.md#global-session)`, the system variable accepts a comma-separated list of filters.
  * When setting it on the command-line or in a server [option group](../../server-management/install-and-upgrade-mariadb/configuring-mariadb/configuring-mariadb-with-option-files.md#option-groups) in an [option file](../../server-management/install-and-upgrade-mariadb/configuring-mariadb/configuring-mariadb-with-option-files.md), the system variable does not accept a comma-separated list. If you would like to specify multiple filters, then you need to specify the system variable multiple times.
  * See [Replication Filters](replication-filters.md) for more information.
* Commandline: `--replicate-ignore-db=name`
* Scope: Global
* Dynamic: Yes
* Data Type: `string`
* Default Value: `''` (empty)

#### `replicate_ignore_table`

* Description: This system variable allows you to configure a [replica](broken-reference) to ignore statements and transactions that affect tables that match a specified name. The table name is specified in the format: `dbname.tablename`.
  * This system variable will not work with cross-database updates with [statement-based logging](../../server-management/server-monitoring-logs/binary-log/binary-log-formats.md#statement-based-logging). See the [Statement-Based Logging](replication-filters.md#statement-based-logging) section for more information.
  * When setting it dynamically with `[SET GLOBAL](../../../reference/sql-statements-and-structure/sql-statements/administrative-sql-statements/set-commands/set.md#global-session)`, the system variable accepts a comma-separated list of filters.
  * When setting it on the command-line or in a server [option group](../../server-management/install-and-upgrade-mariadb/configuring-mariadb/configuring-mariadb-with-option-files.md#option-groups) in an [option file](../../server-management/install-and-upgrade-mariadb/configuring-mariadb/configuring-mariadb-with-option-files.md), the system variable does not accept a comma-separated list. If you would like to specify multiple filters, then you need to specify the system variable multiple times.
  * See [Replication Filters](replication-filters.md) for more information.
* Commandline: `--replicate-ignore-table=name`
* Scope: Global
* Dynamic: Yes
* Data Type: `string`
* Default Value: `''` (empty)

#### `replicate_rewrite_db`

* Description: This option allows you to configure a [replica](broken-reference) to rewrite database names. It uses the format `primary_database->replica_database`. If a replica encounters a [binary log](../../server-management/server-monitoring-logs/binary-log/) event in which the default database (i.e. the one selected by the `[USE](../../../reference/sql-statements-and-structure/sql-statements/administrative-sql-statements/use-database.md)` statement) is `primary_database`, then the replica will apply the event in `replica_database` instead.
  * This option will not work with cross-database updates with [statement-based logging](../../server-management/server-monitoring-logs/binary-log/binary-log-formats.md#statement-based-logging). See the [Statement-Based Logging](replication-filters.md#statement-based-logging) section for more information.
  * This option only affects statements that involve tables. This option does not affect statements involving the database itself, such as [CREATE DATABASE](../../reference/sql-statements/data-definition/create/create-database.md), [ALTER DATABASE](../../reference/sql-statements/data-definition/alter/alter-database.md), and [DROP DATABASE](../../reference/sql-statements/data-definition/drop/drop-database.md).
  * When setting it on the command-line or in a server [option group](../../server-management/install-and-upgrade-mariadb/configuring-mariadb/configuring-mariadb-with-option-files.md#option-groups) in an [option file](../../server-management/install-and-upgrade-mariadb/configuring-mariadb/configuring-mariadb-with-option-files.md), the option does not accept a comma-separated list. If you would like to specify multiple filters, then you need to specify the option multiple times.
  * See [Replication Filters](replication-filters.md) for more information.
  * Before [MariaDB 10.11](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-10-11-series/what-is-mariadb-1011), `replicate_rewrite_db` was not available as a system variable, only as a mariadbd option, and could not be set dynamically. From [MariaDB 10.11](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-10-11-series/what-is-mariadb-1011) it is available as a dynamic system variable
* Commandline: `--replicate-rewrite-db=primary_database->replica_database`
* Scope: Global
* Dynamic: Yes
* Data Type: `string`
* Default Value: `''` (empty)
* Introduced: [MariaDB 10.11.0](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-10-11-series/mariadb-10-11-0-release-notes)

#### `replicate_wild_do_table`

* Description: This system variable allows you to configure a [replica](broken-reference) to apply statements and transactions that affect tables that match a specified wildcard pattern. The wildcard pattern uses the same semantics as the `[LIKE](../../../reference/sql-statements-and-structure/sql-statements/built-in-functions/string-functions/like.md)` operator.
  * This system variable will work with cross-database updates with [statement-based logging](../../server-management/server-monitoring-logs/binary-log/binary-log-formats.md#statement-based-logging). See the [Statement-Based Logging](replication-filters.md#statement-based-logging) section for more information.
  * When setting it dynamically with `[SET GLOBAL](../../../reference/sql-statements-and-structure/sql-statements/administrative-sql-statements/set-commands/set.md#global-session)`, the system variable accepts a comma-separated list of filters.
  * When setting it on the command-line or in a server [option group](../../server-management/install-and-upgrade-mariadb/configuring-mariadb/configuring-mariadb-with-option-files.md#option-groups) in an [option file](../../server-management/install-and-upgrade-mariadb/configuring-mariadb/configuring-mariadb-with-option-files.md), the system variable does not accept a comma-separated list. If you would like to specify multiple filters, then you need to specify the system variable multiple times.
  * See [Replication Filters](replication-filters.md) for more information.
* Commandline: `--replicate-wild-do-table=name`
* Scope: Global
* Dynamic: Yes
* Data Type: `string`
* Default Value: `''` (empty)

#### `replicate_wild_ignore_table`

* Description: This system variable allows you to configure a [replica](broken-reference) to ignore statements and transactions that affect tables that match a specified wildcard pattern. The wildcard pattern uses the same semantics as the [LIKE](../../reference/sql-functions/string-functions/like.md) operator.
  * This system variable will work with cross-database updates with [statement-based logging](../../server-management/server-monitoring-logs/binary-log/binary-log-formats.md#statement-based-logging). See the [Statement-Based Logging](replication-filters.md#statement-based-logging) section for more information.
  * When setting it dynamically with [SET GLOBAL](../../reference/sql-statements/administrative-sql-statements/set-commands/set.md#global-session), the system variable accepts a comma-separated list of filters.
  * When setting it on the command-line or in a server [option group](../../server-management/install-and-upgrade-mariadb/configuring-mariadb/configuring-mariadb-with-option-files.md#option-groups) in an [option file](../../server-management/install-and-upgrade-mariadb/configuring-mariadb/configuring-mariadb-with-option-files.md), the system variable does not accept a comma-separated list. If you would like to specify multiple filters, then you need to specify the system variable multiple times.
  * See [Replication Filters](replication-filters.md) for more information.
* Commandline: `--replicate-wild-ignore-table=name`
* Scope: Global
* Dynamic: Yes
* Data Type: `string`
* Default Value: `''` (empty)

#### `report_host`

* Description: The host name or IP address the replica reports to the primary when it registers. If left unset, the replica will not register itself. Reported by [SHOW SLAVE HOSTS](../../reference/sql-statements/administrative-sql-statements/show/show-replica-hosts.md). Note that it is not sufficient for the primary to simply read the IP of the replica from the socket once the replica connects. Due to NAT and other routing issues, that IP may not be valid for connecting to the replica from the primary or other hosts.
* Commandline: `--report-host=host_name`
* Scope: Global
* Dynamic: No
* Data Type: `string`

#### `report_password`

* Description: Replica password reported to the primary when it registers. Reported by [SHOW SLAVE HOSTS](../../reference/sql-statements/administrative-sql-statements/show/show-replica-hosts.md) if `--show-slave-auth-info` is set. This password has no connection with user privileges or with the [replication](broken-reference) user account password.
* Commandline: `--report-password=password`
* Scope: Global
* Dynamic: No
* Data Type: `string`

#### `report_port`

* Description: The commandline option sets the TCP/IP port for connecting to the replica that will be reported to the [replicating](broken-reference) primary during the replica's registration. Viewing the variable will show this value.
* Commandline: `--report-port=#`
* Scope: Global
* Dynamic: No
* Data Type: `numeric`
* Default Value: `0`
* Range: `0` to `65535`

#### `report_user`

* Description: Replica's account user name reported to the primary when it registers. Reported by [SHOW SLAVE HOSTS](../../reference/sql-statements/administrative-sql-statements/show/show-replica-hosts.md) if `--show-slave-auth-info` is set. This username has no connection with user privileges or with the [replication](broken-reference) user account.
* Commandline: `--report-user=name`
* Scope: Global
* Dynamic: No
* Data Type: `string`

#### `server_id`

* Description: This system variable is used with [MariaDB replication](broken-reference) to identify unique primary and replica servers in a topology. This system variable is also used with the [binary log](../../server-management/server-monitoring-logs/binary-log/) to determine which server a specific transaction originated on.
  * When [MariaDB replication](broken-reference) is used with standalone MariaDB Server, each server in the replication topology must have a unique `server_id` value.
  * When [MariaDB replication](broken-reference) is used with [MariaDB Galera Cluster](../../../kb/en/galera/), see [Using MariaDB Replication with MariaDB Galera Cluster: Setting server\_id on Cluster Nodes](https://app.gitbook.com/s/3VYeeVGUV4AMqrA3zwy7/high-availability/using-mariadb-replication-with-mariadb-galera-cluster/using-mariadb-replication-with-mariadb-galera-cluster-using-mariadb-replica#setting-server_id-on-cluster-nodes) for more information on how to set the `server_id` values.
  * In [MariaDB 10.2.1](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/mariadb-1021-release-notes) and below, the default `server_id` value is `0`. If a replica's `server_id` value is `0`, then all primary's will refuse its connection attempts. If a primary's `server_id` value is `0`, then it will refuse all replica connection attempts.
* Commandline: `--server-id =#`
* Scope: Global, Session
* Dynamic: Yes
* Data Type: `numeric`
* Default Value: `1`
* Range: `1` to `4294967295`

#### `skip_parallel_replication`

* Description: If set when a transaction is written to the binlog, parallel apply of that transaction will be avoided on a replica where [slave\_parallel\_mode](replication-and-binary-log-system-variables.md#slave_parallel_mode) is not `aggressive`. Can be used to avoid unnecessary rollback and retry for transactions that are likely to cause a conflict if replicated in parallel. See [parallel replication](parallel-replication.md).
* Commandline: None
* Scope: Session
* Dynamic: Yes
* Data Type: `boolean`
* Default Value: `OFF`

#### `skip_replication`

* Description: Changes are logged into the [binary log](../../server-management/server-monitoring-logs/binary-log/) with the @@skip\_replication flag set. Such events will not be [replicated](broken-reference) by replica that run with `--replicate-events-marked-for-skip` set different from its default of `REPLICATE`. See [Selectively skipping replication of binlog events](selectively-skipping-replication-of-binlog-events.md) for more information.
* Commandline: None
* Scope: Session
* Dynamic: Yes
* Data Type: `boolean`
* Default Value: `OFF`

#### `slave_abort_blocking_timeout`

* Description: Maximum time a replica DDL will wait for a blocking SELECT or other user query until that query will be aborted. The argument will be treated as a decimal value with nanosecond precision. The variable is intended to solve a problem where a long-running SELECT on a replica causes DDL to wait for that SELECT to complete, potentially causing massive replica lag.
* Commandline: `--slave-abort-blocking-timeout=num`
* Scope: Global
* Dynamic: Yes
* Data Type: `double`
* Default Value: `31536000.000000`
* Range: `0` to `31536000`
* Introduced: [MariaDB 11.7](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-11-7-rolling-releases/what-is-mariadb-117)

#### `slave_compressed_protocol`

* Description: If set to 1 (0 is the default), will use compression for the replica/primary protocol if both primary and replica support this.
* Commandline: `--slave-compressed-protocol`
* Scope: Global
* Dynamic: Yes
* Data Type: `boolean`
* Default Value: `0`

#### `slave_connections_needed_for_purge`

* Description: Minimum number of connected replicas required for automatic [binary log](../../server-management/server-monitoring-logs/binary-log/) purge with [max\_binlog\_total\_size](replication-and-binary-log-system-variables.md#max_binlog_total_size), [binlog\_expire\_logs\_seconds](replication-and-binary-log-system-variables.md#binlog_expire_logs_seconds) or [expire\_logs\_days](replication-and-binary-log-system-variables.md#expire_logs_days).\
  Change of the value triggers an attempt to purging, though without binlog rotation, with the purged set of\
  files satisfying the above two parameters and the value that is set itself.
* Commandline: `--slave-connections-needed-for-purge=#`
* Scope: Global
* Dynamic: Yes
* Data Type: `numeric`
* Default Value: `1`; `0` on Galera cluster nodes.
* Range: `0` to `18446744073709551615`
* Introduced: [MariaDB 11.4](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-11-4-series/what-is-mariadb-114)

#### `slave_ddl_exec_mode`

* Description: Modes for how [replication](broken-reference) of DDL events should be executed. Legal values are `STRICT` and `IDEMPOTENT` (default). In `IDEMPOTENT` mode, the replica will not stop for failed DDL operations that would not cause a difference between the primary and the replica. In particular [CREATE TABLE](../../reference/sql-statements/data-definition/create/create-table.md) is treated as [CREATE OR REPLACE TABLE](../../reference/sql-statements/data-definition/create/create-table.md#create-or-replace) and [DROP TABLE](../../reference/sql-statements/data-definition/drop/drop-table.md) is treated as `DROP TABLE IF EXISTS`.
* Commandline: `--slave-ddl-exec-mode=name`
* Scope: Global
* Dynamic: Yes
* Data Type: `enumeration`
* Default Value: `IDEMPOTENT`
* Valid Values: `IDEMPOTENT`, `STRICT`

#### `slave_domain_parallel_threads`

* Description: When set to a non-zero value, each [replication](broken-reference) domain in one primary connection can reserve at most that many worker threads at any one time, leaving the rest (up to the value of[slave\_parallel\_threads](replication-and-binary-log-system-variables.md#slave_parallel_threads)) free for other primary connections\
  or replication domains to use in parallel. See [Parallel Replication](parallel-replication.md#configuration-variable-slave_domain_parallel_threads) for details.
* Commandline: `--slave-domain-parallel-threads=#`
* Scope: Global
* Dynamic: Yes
* Data Type: `numeric`
* Default Value: `0`
* Valid Values: `0` to `16383`

#### `slave_exec_mode`

* Description: Determines the mode used for [replication](broken-reference) error checking and conflict resolution. STRICT mode is the default, and catches all errors and conflicts. IDEMPOTENT mode suppresses duplicate key or no key errors, which can be useful in certain replication scenarios, such as when there are multiple primaries, or circular replication.
* Scope: Global
* Dynamic: Yes
* Data Type: `enumeration`
* Default Value: `IDEMPOTENT` (NDB), `STRICT` (All)
* Valid Values: `IDEMPOTENT`, `STRICT`

#### `slave_load_tmpdir`

* Description: Directory where the replica stores temporary files for [replicating](broken-reference) [LOAD DATA INFILE](../../reference/sql-statements/data-manipulation/inserting-loading-data/load-data-into-tables-or-index/load-data-infile.md) statements. If not set, the replica will use [tmpdir](../optimization-and-tuning/system-variables/server-system-variables.md#tmpdir). Should be set to a disk-based directory that will survive restarts, or else replication may fail.
* Commandline: `--slave-load-tmpdir=path`
* Scope: Global
* Dynamic: No
* Data Type: `file name`
* Default Value: `/tmp`

#### `slave_max_allowed_packet`

* Description: Maximum packet size in bytes for replica SQL and I/O threads. This value overrides [max\_allowed\_packet](replication-and-binary-log-system-variables.md#max_allowed_packet) for [replication](broken-reference) purposes. Set in multiples of 1024 (the minimum) up to 1GB
* Commandline: `--slave-max-allowed-packet=#`
* Scope: Global
* Dynamic: Yes
* Data Type: `numeric`
* Default Value: `1073741824`
* Range: `1024` to `1073741824`

#### `slave_max_statement_time`

* Description: A query that has taken more than this in seconds to run on the replica will be aborted. The argument will be treated as a decimal value with microsecond precision. A value of 0 (default) means no timeout.
* Commandline: `--slave-max-statement-time=#`
* Scope: Global
* Dynamic: Yes
* Data Type: `numeric`
* Default Value: `0.000000`
* Range: `0` to `31536000`
* Introduced: [MariaDB 10.10](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-10-series/what-is-mariadb-1010)

#### `slave_net_timeout`

* Description: Time in seconds for the replica to wait for more data from the primary before considering the connection broken, after which it will abort the read and attempt to reconnect. The retry interval is determined by the MASTER\_CONNECT\_RETRY open for the [CHANGE MASTER](../../reference/sql-statements/administrative-sql-statements/replication-statements/change-master-to.md) statement, while the maximum number of reconnection attempts is set by the [master-retry-count](../../server-management/starting-and-stopping-mariadb/mariadbd-options.md#-master-retry-count) option. The first reconnect attempt takes place immediately.
* Commandline: `--slave-net-timeout=#`
* Scope: Global
* Dynamic: Yes
* Data Type: `numeric`
* Default Value:
  * `60 (1 minute)`
* Range: `1` to `31536000`

#### `slave_parallel_max_queued`

* Description: When [parallel\_replication](parallel-replication.md) is used, the [SQL thread](replication-threads.md#slave-sql-thread) will read ahead in the relay logs, queueing events in memory while looking for opportunities for executing events in parallel. This system variable sets a\
  limit for how much memory it will use for this.
  * The configured value of this system variable is actually allocated for each [worker thread](replication-threads.md#worker-threads), so the total allocation is actually equivalent to the following:
    * `[slave_parallel_max_queued](replication-and-binary-log-system-variables.md)` \* `[slave_parallel_threads](replication-and-binary-log-system-variables.md)`
  * This system variable is only meaningful when parallel\
    replication is configured (i.e. when `[slave_parallel_threads](replication-and-binary-log-system-variables.md)` > `0`).
  * See [Parallel Replication: Configuring the Maximum Size of the Parallel Slave Queue](parallel-replication.md#configuring-the-maximum-size-of-the-parallel-slave-queue) for more information.
* Commandline: `--slave-parallel-max-queued=#`
* Scope: Global
* Dynamic: Yes
* Data Type: `numeric`
* Default Value: `131072`
* Range: `0` to `2147483647`

#### `slave_parallel_mode`

* Description: Controls what transactions are applied in parallel when using [parallel replication](parallel-replication.md).
  * `optimistic`: tries to apply most transactional DML in parallel, and handles any conflicts with rollback and retry. See [optimistic mode](parallel-replication.md#optimistic-mode-of-in-order-parallel-replication).
  * `conservative`: limits parallelism in an effort to avoid any conflicts. See [conservative mode](parallel-replication.md#conservative-mode-of-in-order-parallel-replication).
  * `aggressive`: tries to maximize the parallelism, possibly at the cost of increased conflict rate.
  * `minimal`: only parallelizes the commit steps of transactions.
  * `none` disables parallel apply completely.
* Commandline: None
* Scope: Global
* Dynamic: Yes
* Data Type: `enum`
* Default Value: `optimistic` (>= [MariaDB 10.5.1](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-10-5-series/mariadb-1051-release-notes)), `conservative` (<= [MariaDB 10.5.0](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-10-5-series/mariadb-1050-release-notes))
* Valid Values: `conservative`, `optimistic`, `none`, `aggressive` and `minimal`

#### `slave_parallel_threads`

* Description: This system variable is used to configure [parallel replication](parallel-replication.md).
  * If this system variable is set to a value greater than `0`, then its value will determine how many replica [worker threads](replication-threads.md#worker-threads) will be created to apply [binary log](../../server-management/server-monitoring-logs/binary-log/) events in parallel.
  * If this system variable is set to `0` (which is the default value), then no replica [worker threads](replication-threads.md#worker-threads) will be created. Instead, when replication is enabled, [binary log](../../server-management/server-monitoring-logs/binary-log/) events are applied by the replica's [SQL thread](replication-threads.md#slave-sql-thread).
  * The [replica threads](replication-threads.md#threads-on-the-slave) must be [stopped](../../reference/sql-statements/administrative-sql-statements/replication-statements/stop-replica.md) in order to change this option's value dynamically.
  * Events that were logged with [GTIDs](gtid.md) with different `[gtid_domain_id](gtid.md#gtid_domain_id)` values can be applied in parallel in an [out-of-order](parallel-replication.md#out-of-order-parallel-replication) manner. Each `[gtid_domain_id](gtid.md#gtid_domain_id)` can use the number of threads configured by `[slave_domain_parallel_threads](#slave_domain_parallel_threads)`.
  * Events that were [group-committed](../../server-management/server-monitoring-logs/binary-log/group-commit-for-the-binary-log.md) on the primary can be applied in parallel in an [in-order](parallel-replication.md#what-can-be-run-in-parallel) manner, and the specific behavior can be configured by setting `[slave_parallel_mode](#slave_parallel_mode)`.
* Commandline: `--slave-parallel-threads=#`
* Scope: Global
* Dynamic: Yes
* Data Type: `numeric`
* Default Value: `0`
* Range: `0` to `16383`

#### `slave_parallel_workers`

* Description: Alias for [slave\_parallel\_threads](replication-and-binary-log-system-variables.md#slave_parallel_threads).
* Commandline: `--slave-parallel-workers=#`

#### `slave_run_triggers_for_rbr`

* Description: See [Running triggers on the slave for Row-based events](running-triggers-on-the-replica-for-row-based-events.md) for a description and use-case for this setting.
* Commandline: `--slave-run-triggers-for-rbr=value`
* Scope: Global
* Dynamic: Yes
* Data Type: `enum`
* Default Value: `NO`
* Valid Values: `NO`, `YES`, `LOGGING`, or `ENFORCE` (>= [MariaDB 10.5.2](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-10-5-series/mariadb-1052-release-notes))

#### `slave_skip_errors`

* Description: When an error occurs on the replica, [replication](broken-reference) usually halts. This option permits a list of [error codes](broken-reference) to ignore, and for which replication will continue. This option should never be needed in normal use, and careless use could lead to replica that are out of sync with primary's. Error codes are in the format of the number from the replica error log. Using `all` as an option permits the replica the keep replicating no matter what error it encounters, an option you would never normally need in production and which could rapidly lead to data inconsistencies. A count of these is kept in [slave\_skipped\_errors](replication-and-binary-log-status-variables.md#slave_skipped_errors).
* Commandline: `--slave-skip-errors=[error_code1,error_code2,...|all|ddl_exist_errors]`
* Scope: Global
* Dynamic: No
* Data Type: `string`
* Default Value: `OFF`
* Valid Values: `[list of error codes]`, `ALL`, `OFF`

#### `slave_sql_verify_checksum`

* Description: Verify [binlog checksums](binlog-event-checksums.md) when the replica SQL thread reads events from the [relay log](../../server-management/server-monitoring-logs/binary-log/relay-log.md).
* Commandline: `--slave-sql-verify-checksum=[0|1]`
* Scope: Global
* Access Type: Can be changed dynamically
* Data Type: `bool`
* Default Value: `ON (1)`

#### `slave_transaction_retries`

* Description: Number of times a [replication](broken-reference) replica retries to execute an SQL thread after it fails due to InnDB deadlock or by exceeding the transaction execution time limit. If after this number of tries the SQL thread has still failed to execute, the replica will stop with an error. See also the [innodb\_lock\_wait\_timeout](../../reference/storage-engines/innodb/innodb-system-variables.md) system variable.
* Commandline: `--slave-transaction-retries=#`
* Scope: Global
* Dynamic: Yes
* Data Type: `numeric`
* Default Value: `10`
* Range - 32 bit: `0` to `4294967295`
* Range - 64 bit: `0` to `18446744073709547520`

#### `slave_transaction_retry_errors`

* Description: When an error occurs during a transaction on the replica, [replication](broken-reference) usually halts. By default, transactions that caused a deadlock or elapsed lock wait timeout will be retried. One can add other errors to the the list of errors that should be retried by adding a comma-separated list of [error numbers](broken-reference) to this variable. This is particularly useful in some [Spider](../../reference/storage-engines/spider/) setups. Some recommended errors to retry for Spider are 1020, 1158, 1159, 1160, 1161, 1429, 2013, 12701 (these are in the default value in recent versions).
* Commandline: `--slave-transaction_retry-errors=[error_code1,error_code2,...]`
* Scope: Global
* Dynamic: No
* Data Type: `string`
* Default Value:
  * `1158,1159,1160,1161,1205,1213,1020,1429,2013,12701` (>= [MariaDB 10.6.18](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-10-6-series/mariadb-10-6-18-release-notes), [MariaDB 10.11.8](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-10-11-series/mariadb-10-11-8-release-notes), [MariaDB 11.0.6](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-11-0-series/mariadb-11-0-6-release-notes), [MariaDB 11.1.5](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-11-1-series/mariadb-11-1-5-release-notes), [MariaDB 11.2.4](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-11-2-series/mariadb-11-2-4-release-notes), [MariaDB 11.4.2](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-11-4-series/mariadb-11-4-2-release-notes))
  * `1158,1159,1160,1161,1205,1213,1429,2013,12701` (>= [MariaDB 10.4.5](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/mariadb-1045-release-notes))
* Valid Values: `comma-separated list of error codes`
* Introduced: [MariaDB 10.3.3](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-3-series/mariadb-1033-release-notes)

#### `slave_transaction_retry_interval`

* Description: Interval in seconds for the replica SQL thread to retry a failed transaction due to a deadlock, elapsed lock wait timeout or an error listed in [slave\_transaction\_retry\_errors](replication-and-binary-log-system-variables.md#slave_transaction_retry_errors). The interval is calculated as `max(slave_transaction_retry_interval, min(retry_count, 5))`.
* Commandline: `--slave-transaction-retry-interval=#`
* Scope: Global
* Dynamic: Yes
* Data Type: `numeric`
* Default Value: `0`
* Range: `0` to `3600`
* Introduced: [MariaDB 10.3.3](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-3-series/mariadb-1033-release-notes)

#### `slave_type_conversions`

* Description: Determines the type conversion mode on the replica when using [row-based](../../server-management/server-monitoring-logs/binary-log/binary-log-formats.md#row-based) [replication](broken-reference), including replications in MariaDB Galera cluster. Multiple options can be set, delimited by commas. If left empty, the default, type conversions are disallowed. The variable is dynamic and a change in its value takes effect immediately. This variable tells the server what to do if the table definition is different between the primary and replica (for example a column is 'int' on the primary and 'bigint' on the replica).
  * `ALL_NON_LOSSY` means that all safe conversions (no data loss) are allowed.
  * `ALL_LOSSY` means that all lossy conversions are allowed (for example 'bigint' to 'int'). This, however, does not imply that safe conversions (non-lossy) are allowed as well. In order to allow all conversions, one needs to allow both lossy as well as non-lossy conversions by setting this variable to ALL\_NON\_LOSSY,ALL\_LOSSY.
  * Empty (default) means that the server should give an error and replication should stop if the table definition is different between the primary and replica.
* Commandline: `--slave-type-conversions=set`
* Scope: Global
* Dynamic: Yes
* Data Type: `set`
* Default Value: `Empty variable`
* Valid Values: `ALL_LOSSY`, `ALL_NON_LOSSY`, empty

#### `sql_log_bin`

* Description: If set to 0 (1 is the default), no logging to the [binary log](../../server-management/server-monitoring-logs/binary-log/) is done for the client. Only clients with the SUPER privilege can update this variable. Does not affect the replication of events in a Galera cluster. Note that `sql_log_bin` has no effect if `[log_bin](replication-and-binary-log-system-variables.md#log_bin)` is not set.
* Scope: Session
* Dynamic: Yes
* Data Type: `boolean`
* Default Value: `1`
* Related variables: `[log_bin](replication-and-binary-log-system-variables.md#log_bin)`

#### `sql_slave_skip_counter`

* Description: Number of events that a replica skips from the primary. If this would cause the replica to begin in the middle of an event group, the replica will instead begin from the beginning of the next event group. See [SET GLOBAL sql\_slave\_skip\_counter](../../reference/sql-statements/administrative-sql-statements/replication-statements/set-global-sql_slave_skip_counter.md).
* Scope: Global
* Dynamic: Yes
* Data Type: `numeric`
* Default Value: `0`

#### `sync_binlog`

* Description: MariaDB will synchronize its binary log file to disk after this many events. The default is 0, in which case the operating system handles flushing the file to disk. 1 is the safest, but slowest, choice, since the file is flushed after each write. If autocommit is enabled, there is one write per statement, otherwise there's one write per transaction. If the disk has cache backed by battery, synchronization will be fast and a more conservative number can be chosen.
* Commandline: `--sync-binlog=#`
* Scope: Global
* Dynamic: Yes
* Data Type: `numeric`
* Default Value: `0`
* Range: `0` to `4294967295`

#### `sync_master_info`

* Description: A [replication](broken-reference) replica will synchronize its master.info file to disk after this many events. If set to 0, the operating system handles flushing the file to disk.
* Commandline: `--sync-master-info=#`
* Scope: Global
* Dynamic: Yes
* Data Type: `numeric`
* Default Value: `10000`

#### `sync_relay_log`

* Description: The MariaDB server will synchronize its [relay log](../../server-management/server-monitoring-logs/binary-log/relay-log.md) to disk after this many writes to the log. The default until [MariaDB 10.1.7](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/mariadb-10-1-7-release-notes) was 0, in which case the operating system handles flushing the file to disk. 1 is the safest, but slowest, choice, since the file is flushed after each write. If autocommit is enabled, there is one write per statement, otherwise there's one write per transaction. If the disk has cache backed by battery, synchronization will be fast and a more conservative number can be chosen.
* Commandline: `--sync-relay-log=#`
* Scope: Global
* Dynamic: Yes
* Data Type: `numeric`
* Default Value: `10000`

#### `sync_relay_log_info`

* Description: A [replication](broken-reference) replica will synchronize its relay-log.info file to disk after this many transactions. The default until [MariaDB 10.1.7](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/mariadb-10-1-7-release-notes) was 0, in which case the operating system handles flushing the file to disk. 1 is the most secure choice, because at most one event could be lost in the event of a crash, but it's also the slowest.
* Commandline: `--sync-relay-log-info=#`
* Scope: Global,
* Dynamic: Yes
* Data Type: `numeric`
* Default Value: `10000`
* Range: `0` to `4294967295`

CC BY-SA / Gnu FDL
