# Hintfilter

This filter adds routing hints to a service. The filter has no parameters.

* [Hintfilter](mariadb-maxscale-25-hintfilter.md#hintfilter)
  * [Limitations](mariadb-maxscale-25-hintfilter.md#limitations)
* [Hint Syntax](mariadb-maxscale-25-hintfilter.md#hint-syntax)
  * [Comments and comment types](mariadb-maxscale-25-hintfilter.md#comments-and-comment-types)
  * [Hint body](mariadb-maxscale-25-hintfilter.md#hint-body)
    * [Routing destination hints](mariadb-maxscale-25-hintfilter.md#routing-destination-hints)
      * [Route to master](mariadb-maxscale-25-hintfilter.md#route-to-master)
      * [Route to slave](mariadb-maxscale-25-hintfilter.md#route-to-slave)
      * [Route to named server](mariadb-maxscale-25-hintfilter.md#route-to-named-server)
      * [Route to last used server](mariadb-maxscale-25-hintfilter.md#route-to-last-used-server)
      * [Name-value hints](mariadb-maxscale-25-hintfilter.md#name-value-hints)
  * [Hint stack](mariadb-maxscale-25-hintfilter.md#hint-stack)
* [Examples](mariadb-maxscale-25-hintfilter.md#examples)
  * [Routing SELECT queries to master](mariadb-maxscale-25-hintfilter.md#routing-select-queries-to-master)

### Limitations

The hintfilter does not support routing hints in prepared statements\
([MXS-2838](https://jira.mariadb.org/browse/MXS-2838)).

## Hint Syntax

**Note:** If a query has more than one comment only the first comment is\
processed. Always place any MaxScale related comments first before any other\
comments that might appear in the query.

### Comments and comment types

The client connection will need to have comments enabled. For example the`mariadb` and `mysql` command line clients have comments disabled by default and\
they need to be enabled by passing the `--comments` or `-c` option to it. Most,\
if not all, connectors keep all comments intact in executed queries.

```
# The --comments flag is needed for the command line client
mariadb --comments -u my-user -psecret -e "SELECT @@hostname -- maxscale route to server db1"
```

For comment types, use either `--` (notice the whitespace after the double\
hyphen) or `#` after the semicolon or `/* ... */` before the semicolon.

Inline comment blocks, i.e. `/* .. */`, do not require a whitespace character\
after the start tag or before the end tag but adding the whitespace is advised.

### Hint body

All hints must start with the `maxscale` tag.

```
-- maxscale <hint body>
```

The hints have two types, ones that define a server type and others that contain\
name-value pairs.

#### Routing destination hints

These hints will instruct the router to route a query to a certain type of a\
server.

```
-- maxscale route to [master | slave | server <server name>]
```

**Route to master**

```
-- maxscale route to master
```

A `master` value in a routing hint will route the query to a master server. This\
can be used to direct read queries to a master server for a up-to-date result\
with no replication lag.

**Route to slave**

```
-- maxscale route to slave
```

A `slave` value will route the query to a slave server. Please note that the\
hints will override any decisions taken by the routers which means that it is\
possible to force writes to a slave server.

**Route to named server**

```
-- maxscale route to server <server name>
```

A `server` value will route the query to a named server. The value of`<server name>` needs to be the same as the server section name in\
maxscale.cnf. If the server is not used by the service, the hint is ignored.

**Route to last used server**

```
-- maxscale route to last
```

A `last` value will route the query to the server that processed the last\
query. This hint can be used to force certain queries to be grouped to the same\
server.

**Name-value hints**

```
-- maxscale <param>=<value>
```

These control the behavior and affect the routing decisions made by the\
router. Currently the only accepted parameter is the readwritesplit parameter`max_slave_replication_lag`. This will route the query to a server with a lower\
replication lag than this parameter's value.

### Hint stack

Hints can be either single-use hints, which makes them affect only one query, or\
named hints, which can be pushed on and off a stack of active hints.

Defining named hints:

```
-- maxscale <hint name> prepare <hint content>
```

Pushing a hint onto the stack:

```
-- maxscale <hint name> begin
```

Popping the topmost hint off the stack:

```
-- maxscale end
```

You can define and activate a hint in a single command using the following:

```
-- maxscale <hint name> begin <hint content>
```

You can also push anonymous hints onto the stack which are only used as long as\
they are on the stack:

```
-- maxscale begin <hint content>
```

## Examples

### Routing `SELECT` queries to master

In this example, MariaDB MaxScale is configured with the readwritesplit router\
and the hint filter.

```
[ReadWriteService]
type=service
router=readwritesplit
servers=server1,server2
user=maxuser
password=maxpwd
filters=Hint

[Hint]
type=filter
module=hintfilter
```

Behind MariaDB MaxScale is a master server and a slave server. If there is\
replication lag between the master and the slave, read queries sent to the slave\
might return old data. To guarantee up-to-date data, we can add a routing hint\
to the query.

```
INSERT INTO table1 VALUES ("John","Doe",1);
SELECT * from table1; -- maxscale route to master
```

The first INSERT query will be routed to the master. The following SELECT query\
would normally be routed to the slave but with the added routing hint it will be\
routed to the master. This way we can do an INSERT and a SELECT right after it\
and still get up-to-date data.

<sub>_This page is licensed: CC BY-SA / Gnu FDL_</sub>

{% @marketo/form formId="4316" %}
