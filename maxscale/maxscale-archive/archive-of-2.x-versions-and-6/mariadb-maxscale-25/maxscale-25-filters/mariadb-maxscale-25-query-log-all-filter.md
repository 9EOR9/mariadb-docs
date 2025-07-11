# Query Log All Filter

* [Query Log All Filter](mariadb-maxscale-25-query-log-all-filter.md#query-log-all-filter)
  * [Overview](mariadb-maxscale-25-query-log-all-filter.md#overview)
  * [Configuration](mariadb-maxscale-25-query-log-all-filter.md#configuration)
  * [Log Rotation](mariadb-maxscale-25-query-log-all-filter.md#log-rotation)
  * [Filter Parameters](mariadb-maxscale-25-query-log-all-filter.md#filter-parameters)
    * [filebase](mariadb-maxscale-25-query-log-all-filter.md#filebase)
    * [match, exclude and options](mariadb-maxscale-25-query-log-all-filter.md#match-exclude-and-options)
    * [user and source](mariadb-maxscale-25-query-log-all-filter.md#user-and-source)
    * [log\_type](mariadb-maxscale-25-query-log-all-filter.md#log_type)
    * [log\_data](mariadb-maxscale-25-query-log-all-filter.md#log_data)
    * [flush](mariadb-maxscale-25-query-log-all-filter.md#flush)
    * [append](mariadb-maxscale-25-query-log-all-filter.md#append)
    * [separator](mariadb-maxscale-25-query-log-all-filter.md#separator)
    * [newline\_replacement](mariadb-maxscale-25-query-log-all-filter.md#newline_replacement)
  * [Examples](mariadb-maxscale-25-query-log-all-filter.md#examples)
    * [Example 1 - Query without primary key](mariadb-maxscale-25-query-log-all-filter.md#example-1-query-without-primary-key)

### Overview

The Query Log All (QLA) filter logs query content. Logs are written to a file in\
CSV format. Log elements are configurable and include the time submitted and the\
SQL statement text, among others.

### Configuration

A minimal configuration is below.

```
[MyLogFilter]
type=filter
module=qlafilter
filebase=/tmp/SqlQueryLog

[MyService]
type=service
router=readconnroute
servers=server1
user=myuser
password=mypasswd
filters=MyLogFilter
```

### Log Rotation

The `qlafilter` logs can be rotated by executing the `maxctrl rotate logs`\
command. This will cause the log files to be reopened when the next message is\
written to the file. This applies to both unified and session type logging.

### Filter Parameters

The QLA filter has one mandatory parameter, `filebase`, and a number of optional\
parameters. These were introduced in the 1.0 release of MariaDB MaxScale.

#### `filebase`

The basename of the output file created for each session. A session index is\
added to the filename for each written session file. For unified log files,_.unified_ is appended. This is a mandatory parameter.

```
filebase=/tmp/SqlQueryLog
```

#### `match`, `exclude` and `options`

These[regular expression settings](../maxscale-25-getting-started/mariadb-maxscale-25-mariadb-maxscale-configuration-guide.md#standard-regular-expression-settings-for-filters)\
limit which queries are logged.

```
match=select.*from.*customer.*where
exclude=^insert
options=case,extended
```

#### `user` and `source`

These optional parameters limit logging on a session level. If `user` is\
defined, only the sessions with a matching client username are logged. If`source` is defined, only sessions with a matching client source address are\
logged.

```
user=john
source=127.0.0.1
```

#### `log_type`

The type of log file to use. The default value is _session_.

| Value   | Description                     |
| ------- | ------------------------------- |
| Value   | Description                     |
| session | Write to session-specific files |
| unified | Use one file for all sessions   |
| stdout  | Same as unified, but to stdout  |

```
log_type=session
```

The log types can be combined, e.g. setting `log_type=session,stdout`\
will write both session-specific files, and all sessions to stdout.

#### `log_data`

Type of data to log in the log files. The parameter value is a comma separated\
list of the following elements. By default the _date_, _user_ and _query_\
options are enabled.

| Value       | Description                                      |
| ----------- | ------------------------------------------------ |
| Value       | Description                                      |
| service     | Service name                                     |
| session     | Unique session id (ignored for session files)    |
| date        | Timestamp                                        |
| user        | User and hostname of client                      |
| reply\_time | Response time (ms until first reply from server) |
| query       | Query                                            |
| default\_db | The default (current) database                   |

```
log_data=date, user, query
```

If _reply\_time_ is enabled, the log entry is written when the first reply from\
server is received. Otherwise, the entry is written when receiving query from\
client.

#### `flush`

Flush log files after every write. The default is false.

```
flush=true
```

#### `append`

Append new entries to log files instead of overwriting them. The default is\
true.\
NOTE: the default was changed from false to true, as of the following\
versions: 2.4.18, 2.5.16 and 6.2.

```
append=true
```

#### `separator`

Default value is "," (a comma). Defines the separator string between elements of\
a log entry. The value should be enclosed in quotes.

```
separator=" | "
```

#### `newline_replacement`

Default value is " " (one space). SQL-queries may include line breaks, which, if\
printed directly to the log, may break automatic parsing. This parameter defines\
what should be written in the place of a newline sequence (\r, \n or \r\n). If\
this is set as the empty string, then newlines are not replaced and printed as\
is to the output. The value should be enclosed in quotes.

```
newline_replacement=" NL "
```

### Examples

#### Example 1 - Query without primary key

Imagine you have observed an issue with a particular table and you want to\
determine if there are queries that are accessing that table but not using the\
primary key of the table. Let's assume the table name is PRODUCTS and the\
primary key is called PRODUCT\_ID. Add a filter with the following definition:

```
[ProductsSelectLogger]
type=filter
module=qlafilter
match=SELECT.*from.*PRODUCTS .*
exclude=WHERE.*PRODUCT_ID.*
filebase=/var/logs/qla/SelectProducts

[Product-Service]
type=service
router=readconnroute
servers=server1
user=myuser
password=mypasswd
filters=ProductsSelectLogger
```

The result of using this filter with the service used by the application would\
be a log file of all select queries querying PRODUCTS without using the\
PRODUCT\_ID primary key in the predicates of the query. Executing `SELECT * FROM PRODUCTS` would log the following into `/var/logs/qla/SelectProducts`:

```
07:12:56.324 7/01/2016, SELECT * FROM PRODUCTS
```

<sub>_This page is licensed: CC BY-SA / Gnu FDL_</sub>

{% @marketo/form formId="4316" %}
