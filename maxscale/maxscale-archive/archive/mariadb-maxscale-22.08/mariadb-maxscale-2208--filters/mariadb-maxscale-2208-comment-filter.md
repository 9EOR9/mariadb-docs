# MaxScale 22.08 Comment Filter

## Comment Filter

## Comment Filter

* [Comment Filter](mariadb-maxscale-2208-comment-filter.md#comment-filter)
  * [Overview](mariadb-maxscale-2208-comment-filter.md#overview)
  * [Filter Parameters](mariadb-maxscale-2208-comment-filter.md#filter-parameters)
    * [inject](mariadb-maxscale-2208-comment-filter.md#inject)
  * [Examples](mariadb-maxscale-2208-comment-filter.md#examples)
    * [Example 1 - Inject IP address of the connected client into statements](mariadb-maxscale-2208-comment-filter.md#example-1-inject-ip-address-of-the-connected-client-into-statements)

### Overview

With the _comment_ filter it is possible to define comments that are\
injected before the actual statements. These comments appear as sql\
comments when they are received by the server.

```
[MyComment]
type=filter
module=comment
inject="Comment to be injected"

[MyService]
type=service
router=readwritesplit
servers=server1
user=myuser
password=mypasswd
filters=MyComment
```

### Filter Parameters

The Comment filter requires one mandatory parameter to be defined.

#### `inject`

* Type: string
* Mandatory: Yes
* Dynamic: Yes

A parameter that contains the comment injected before the statements.\
There is also defined variable $IP that can be used to comment the\
IP address of the client in the injected comment.\
Variables must be written in all caps.

### Examples

#### Example 1 - Inject IP address of the connected client into statements

as comment.

The following configuration adds the IP address of the client to the comment.

```
[IPComment]
type=filter
module=comment
inject="IP=$IP"

[MyService]
type=service
router=readwritesplit
servers=server1
user=myuser
password=mypasswd
filters=IPComment
```

In this example when MaxScale receives statement like:

```
SELECT user FROM people;
```

It would look like

```
/* IP=::ffff:127.0.0.1 */SELECT user FROM people;
```

when received by server.

CC BY-SA / Gnu FDL
