# Binlog Event Checksum Interoperability

{% hint style="info" %}
The terms _master_ and _slave_ have historically been used in replication, and MariaDB has begun the process of adding _primary_ and _replica_ synonyms. The old terms will continue to be used to maintain backward compatibility - see [MDEV-18777](https://jira.mariadb.org/browse/MDEV-18777) to follow progress on this effort.
{% endhint %}

The introduction of [checksums on binlog events](binlog-event-checksums.md) changes the format that events\
are stored in [binary log](../../server-management/server-monitoring-logs/binary-log/) files and sent over the network to replicas. This raises the question on what happens when replicating between different versions of the\
server, where one server is a newer version that has the binlog checksum\
feature implemented, while the other server is an older version that does not\
know about binlog checksums.

When checksums are disabled on the primary (or the primary has the old version\
with no checksums implemented), there is no problem. In this case the binlog\
format is backwards compatible, and replication works fine.

When the primary is a newer version with checksums enabled in the binlog, but\
the replica is an old version that does not understand checksums, replication\
will fail. The primary will disconnect the replica with an error, and also log a\
warning in its own error log. This prevents sending events to the replica that it\
will be unable to interpret correctly, but means that binlog checksums can not\
be used with older replicas. (With the recommended upgrade path, where replicas are\
upgraded before primaries, this is not a problem of course).

Replicating from a new MySQL primary with checksums enabled to a new MariaDB\
which also understands checksums works, and the MariaDB replica will verify\
checksums on replicated events.

There is however a problem when a newer MySQL replica replicates against a newer\
MariaDB primary with checksums enabled. The replica server looks at the primary\
server version to know whether events include checksums or not, and MySQL has\
not yet been updated to learn that MariaDB does this already from version 5.3.0\
(as of the time of writing, MySQL 5.6.2). Thus, if MariaDB at least version\
5.3.0 but less that 5.6.1 is used as a primary with binlog checksums enabled, a\
MySQL replica will interpret the received events incorrectly as it does not\
realise the last part of the events is the checksum. So replication will fail\
with an error about corrupt events or even silent corruption of replicated data\
in unlucky cases. This requires changes to the MySQL server to fix.

Here is a summary table of the status of replication between different\
combination of primary and replica servers and checksum enabled/disabled:

* OLD: MySQL <5.6.1 or MariaDB < 5.3.0 with no checksum capabilities
* NEW-MARIA: MariaDB >= 5.3.0 with checksum capabilities
* NEW-MYSQL: MySQL >= 5.6.1 with checksum capabilities

| Primary mariadb-lbinlog | Replica / enabled? | Checksums | Status                                                                                                              |
| ----------------------- | ------------------ | --------- | ------------------------------------------------------------------------------------------------------------------- |
| Primary mariadb-lbinlog | Replica / enabled? | Checksums | Status                                                                                                              |
| OLD                     | OLD                | -         | Ok                                                                                                                  |
| OLD                     | NEW-MARIA          | -         | Ok                                                                                                                  |
| OLD                     | MYSQL              | -         | Ok                                                                                                                  |
| NEW-MARIA               | OLD                | No        | Ok                                                                                                                  |
| NEW-MARIA               | OLD                | Yes       | Primary will refuse with error                                                                                      |
| NEW-MARIA               | NEW-MARIA          | Yes/No    | Ok                                                                                                                  |
| NEW-MARIA               | NEW-MYSQL          | No        | Ok                                                                                                                  |
| NEW-MARIA               | NEW-MYSQL          | Yes       | Fail. Requires changes in MySQL, otherwise it will not realise MariaDB < 5.6.1 does checksums and will be confused. |
| NEW-MYSQL               | OLD                | No        | Ok                                                                                                                  |
| NEW-MYSQL               | OLD                | Yes       | Primary will refuse with error                                                                                      |
| NEW-MYSQL               | NEW-MARIA          | Yes/No    | Ok                                                                                                                  |
| NEW-MYSQL               | NEW-MYSQL          | Yes/No    | Ok                                                                                                                  |

## Checksums and mariadb-binlog

When using the [mariadb-binlog](../../clients-and-utilities/mariadb-binlog/) client program, there are similar issues.

A version of `mariadb-binlog` which understands checksums can read binlog files\
from either old or new servers, with or without checksums enabled.

An old version of `mariadb-binlog` can read binlog files produced by a new\
server version **if** checksums were disabled when the log was produced. Old\
versions of `mariadb-binlog` reading a new binlog file containing checksums will\
be confused, and output will be garbled, with the added checksums being\
interpreted as extra garbage at the end of query strings and similar entries. No\
error will be reported in this case, just wrong output.

A version of `mysqlbinlog` (the MySQL equivalent to mariadb-binlog and the old MariaDB name for the binary) from MySQL >= 5.6.1 will have similar problems as\
a replica until this is fixed in MySQL. When reading a binlog file with checksums\
produced by MariaDB >= 5.3.0 but < 5.6.1, it will not realise that checksums\
are included, and will produce garbled output just like an old version of`mysqlbinlog`. The MariaDB version of `mariadb-binlog` can read binlog files\
produced by either MySQL or MariaDB just fine.

## See Also

* [Binlog Event Checksums](binlog-event-checksums.md)

CC BY-SA / Gnu FDL

{% @marketo/form formId="4316" %}
