# Binlog Filter

This filter was introduced in MariaDB MaxScale 2.3.0.

### Overview

The `binlogfilter` can be combined with a `binlogrouter` service to selectively\
replicate the binary log events to slave servers.

The filter uses two parameters, _match_ and _exclude_, to decide which events\
are replicated. If a binlog event does not match or is excluded, the event is\
replaced with an empty data event. The empty event is always 35 bytes which\
translates to a space reduction in most cases.

The filter works with both row based and statement based replication but we\
recommend using row based replication with the binlogfilter. This guarantees\
that there are no ambiguities in the event filtering.

### Configuration

#### `match` and `exclude`

Both the _match_ and _exclude_ parameters are optional and work mostly as other[typical regular expression parameters](../../../archive-of-2x.xx-versions/mariadb-maxscale-21-06/).\
If neither of them is defined, the filter does nothing and all events are replicated. This\
filter does not accept regular expression options as a separate parameter, such settings\
must be defined in the patterns themselves. See the[PCRE2 api documentation](https://www.pcre.org/current/doc/html/pcre2api.html#SEC20) for\
more information.

The two parameters are matched against the database and table name concatenated\
with a period. For example, the string the patterns are matched against for the\
database `test` and table `t1` is `test.t1`.

For statement based replication, the pattern is matched against all the tables\
in the statements. If any of the tables matches the _match_ pattern, the event\
is replicated. If any of the tables matches the _exclude_ pattern, the event is\
not replicated.

### Example Configuration

With the following configuration, only events belonging to database `customers`\
are replicated. In addition to this, events for the table `orders` are excluded\
and thus are not replicated.

```
[BinlogFilter]
type=filter
module=binlogfilter
match=/customers[.]/
exclude=/[.]orders/

[BinlogServer]
type=service
router=binlogrouter
server_id=33
filters=BinlogFilter

[BinlogListener]
type=listener
service=BinlogServer
protocol=MySQLClient
port=4000
```

For more information about the binlogrouter and how to use it, refer to the[binlogrouter documentation](../maxscale-23-routers/mariadb-maxscale-23-binlogrouter.md) and the[binlogrouter tutorial](../maxscale-tutorials/mariadb-maxscale-23-mariadb-maxscale-as-a-binlog-server.md).

<sub>_This page is licensed: CC BY-SA / Gnu FDL_</sub>

{% @marketo/form formId="4316" %}
