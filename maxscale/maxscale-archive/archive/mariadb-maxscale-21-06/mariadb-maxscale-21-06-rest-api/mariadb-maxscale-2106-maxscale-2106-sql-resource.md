# MaxScale 21.06 SQL Resource

The SQL resource represents a database connection.

* [SQL Resource](mariadb-maxscale-2106-maxscale-2106-sql-resource.md#sql-resource)
  * [SQL Connection Interface](mariadb-maxscale-2106-maxscale-2106-sql-resource.md#sql-connection-interface)
  * [Request Parameters](mariadb-maxscale-2106-maxscale-2106-sql-resource.md#request-parameters)
    * [Get one SQL connection](mariadb-maxscale-2106-maxscale-2106-sql-resource.md#get-one-sql-connection)
      * [Response](mariadb-maxscale-2106-maxscale-2106-sql-resource.md#response)
    * [Get all SQL connections](mariadb-maxscale-2106-maxscale-2106-sql-resource.md#get-all-sql-connections)
      * [Response](mariadb-maxscale-2106-maxscale-2106-sql-resource.md#response_1)
    * [Open SQL connection to server](mariadb-maxscale-2106-maxscale-2106-sql-resource.md#open-sql-connection-to-server)
      * [Request Parameters](mariadb-maxscale-2106-maxscale-2106-sql-resource.md#request-parameters_1)
      * [Response](mariadb-maxscale-2106-maxscale-2106-sql-resource.md#response_2)
    * [Close an opened SQL connection](mariadb-maxscale-2106-maxscale-2106-sql-resource.md#close-an-opened-sql-connection)
      * [Response](mariadb-maxscale-2106-maxscale-2106-sql-resource.md#response_3)
    * [Reconnect an opened SQL connection](mariadb-maxscale-2106-maxscale-2106-sql-resource.md#reconnect-an-opened-sql-connection)
      * [Response](mariadb-maxscale-2106-maxscale-2106-sql-resource.md#response_4)
    * [Execute SQL query](mariadb-maxscale-2106-maxscale-2106-sql-resource.md#execute-sql-query)
      * [Response](mariadb-maxscale-2106-maxscale-2106-sql-resource.md#response_5)

### SQL Connection Interface

The following endpoints provide a simple REST API interface for executing\
SQL queries on servers and services in MaxScale.

This document uses the `:id` value in the URL to represent a connection ID and\
the `:query_id` to represent a query ID. These values do not need to be manually\
added as the relevant links are returned in the request body of each endpoint.

The endpoints use JSON Web Tokens to uniquely identify open SQL connections. A\
connection token can be acquired with a `POST /v1/sql` request and can be used\
with the `POST /v1/sql/:id/query`, `GET /v1/sql/:id/results/:query_id` and`DELETE /v1/sql` endpoints. All of these endpoints accept a connection token in\
the `token` parameter of the request:

```
POST /v1/sql/query?token=eyJhbGciOiJIUzI1NiJ9.eyJhdWQiOiJhZG1pbiIsImV4cCI6MTU4MzI1NDE1MSwiaWF0IjoxNTgzMjI1MzUxLCJpc3MiOiJtYXhzY2FsZSJ9.B1BqhjjKaCWKe3gVXLszpOPfeu8cLiwSb4CMIJAoyqw
```

In addition to request parameters, the token can be stored in cookies in which\
case they are automatically used by the REST API. For more information about\
token storage in cookies, see the documentation for `POST /v1/sql`.

### Request Parameters

All of the endpoints that operate on a single connection support the following\
request parameters. The `GET /v1/sql` and `GET /v1/sql/:id` endpoints are an\
exception as they ignore the current connection token.

* `token`
* The connection token to use for the request. If provided, the value is\
  unconditionally used even if a cookie with a valid token exists.

#### Get one SQL connection

```
GET /v1/sql/:id
```

**Response**

Response contains the requested resource.

`Status: 200 OK`

```
{
    "data": {
        "id": "5",
        "links": {
            "related": "http://localhost:8989/v1/sql/5/queries/",
            "self": "http://localhost:8989/v1/sql/5/"
        },
        "type": "sql"
    },
    "links": {
        "self": "http://localhost:8989/v1/sql/5/"
    },
    "meta": {
        "token": "eyJhbGciOiJIUzI1NiJ9.eyJhdWQiOiI1IiwiZXhwIjoxNjIwMjM1Mzc3LCJpYXQiOjE2MjAyMDY1NzcsImlzcyI6Im14cy1xdWVyeSJ9.2CJ8DsEPbGlvs2DrBUC6FJA64VMSU8kbX1U4FSu2-OY"
    }
}
```

#### Get all SQL connections

```
GET /v1/sql
```

**Response**

Response contains a resource collection with all the open SQL connections.

`Status: 200 OK`

```
{
    "data": [
        {
            "id": "10",
            "links": {
                "related": "http://localhost:8989/v1/sql/10/queries/",
                "self": "http://localhost:8989/v1/sql/10/"
            },
            "type": "sql"
        },
        {
            "id": "11",
            "links": {
                "related": "http://localhost:8989/v1/sql/11/queries/",
                "self": "http://localhost:8989/v1/sql/11/"
            },
            "type": "sql"
        }
    ],
    "links": {
        "self": "http://localhost:8989/v1/sql/"
    }
}
```

#### Open SQL connection to server

```
POST /v1/sql
```

The request body must be a JSON object consisting of the following fields:

* `target`
* The object in MaxScale to connect to. This is a mandatory value and the\
  given value must be the name of a valid server, service or listener in\
  MaxScale.
* `user`
* The username to use when creating the connection. This is a mandatory value.
* `password`
* The password for the user. This is a mandatory value.
* `db`
* The default database for the connection. By default the connection will have\
  no default database.
* `timeout`
* Connection timeout in seconds. The default connection timeout is 10\
  seconds. This controls how long the SQL connection creation can take before\
  an error is returned.

Here is an example request body:

```
{
    "user": "jdoe",
    "password": "my-s3cret",
    "target": "server1",
    "db": "test",
    "timeout": 15
}
```

The response will contain the new connection with the token stored at`meta.token`. If the request uses the `persist=yes` request parameter, the token\
is stored in cookies instead of the metadata object and the response body will\
not contain the token.

The location of the newly created connection will be stored at `links.self` in\
the response body as well as in the `Location` header.

The token must be given to all subsequent requests that use the connection. It\
must be either given in the `token` parameter of a request or it must be stored\
in the cookies. If both a `token` parameter and a cookie exist at the same time,\
the `token` parameter will be used instead of the cookie.

**Request Parameters**

This endpoint supports the following request parameters.

* `persist`
* Store the connection token in cookies instead of returning it as the response body.\
  This parameter expects only one value, `yes`, as its argument. When`persist=yes` is set, the token is stored in two cookies,`conn_id_body_<id>` and `conn_id_sig_<id>` where the `<id>` part is replaced\
  by the ID of the connection.\
  The `conn_id_body_<id>` cookie contains the JWT header and claims sections\
  and contains the connection ID in the `aud` value. This can be used to\
  retrieve the connection ID from the cookies if the browser session is\
  closed.
* `max-age`
* Sets the connection token maximum age in seconds. The default is`max-age=28800`. Only positive values are accepted and if a non-positive or\
  a non-integer value is found, the parameter is ignored. Once the token age\
  exceeds the configured maximum value, the token can no longer be used and a\
  new connection must be created.

**Response**

Connection was opened:

`Status: 201 Created`

```
{
    "data": {
        "id": "5",
        "links": {
                 // The "related" endpoint is the URL to the query endpoint for this connection.
            "related": "http://localhost:8989/v1/sql/5/queries/",
            "self": "http://localhost:8989/v1/sql/5/"
        },
        "type": "sql"
    },
    "links": {
        "self": "http://localhost:8989/v1/sql/5/"
    },
    "meta": {
        "token": "eyJhbGciOiJIUzI1NiJ9.eyJhdWQiOiI1IiwiZXhwIjoxNjIwMjM1Mzc3LCJpYXQiOjE2MjAyMDY1NzcsImlzcyI6Im14cy1xdWVyeSJ9.2CJ8DsEPbGlvs2DrBUC6FJA64VMSU8kbX1U4FSu2-OY"
    }
}
```

Missing or invalid payload:

`Status: 403 Forbidden`

#### Close an opened SQL connection

```
DELETE /v1/sql/:id
```

**Response**

Connection was closed:

`Status: 204 No Content`

Missing or invalid connection token:

`Status: 403 Forbidden`

#### Reconnect an opened SQL connection

```
POST /v1/sql/:id/reconnect
```

Reconnects an existing connection. This can also be used if the connection to\
the backend server was lost due to a network error.

The connection will use the same credentials that were passed to the `POST /v1/sql` endpoint. The new connection will still have the same ID in the REST\
API but will be treated as a new connection by the database. A reconnection\
re-initializes the connection and resets the session state. Reconnections cannot\
take place while a transaction is open.

**Response**

Reconnection was successful:

`Status: 204 No Content`

Reconnection failed or connection is already in use:

`Status: 503 Service Unavailable`

Missing or invalid connection token:

`Status: 403 Forbidden`

#### Execute SQL query

```
POST /v1/sql/:id/queries
```

The request body must be a JSON object with the value of the `sql` field set to\
the SQL to be executed:

```
{
    "sql": "SELECT * FROM test.t1",
    "max_rows": 1000
}
```

The request body must be a JSON object consisting of the following fields:

* `sql`
* The SQL to be executed. If the SQL contain multiple statements, multiple\
  results are returned in the response body.
* `max_rows`
* The maximum number of rows returned in the response. By default this is 1000\
  rows. Setting the value to 0 means no limit. Any extra rows in the result\
  will be discarded.

By default, the complete result is returned in the response body. If the SQL\
query returns more than one result, the `results` array will contain all the\
results.

The `results` array can have three types of objects: resultsets, errors, and OK\
responses.

* A resultset consists of the `data` field with the result data stored as a two\
  dimensional array. The names of the fields are stored in an array in the`fields` field. These types of results will be returned for any operation that\
  returns rows (i.e. `SELECT` statements)

```
{
    "data": {
        "attributes": {
            "results": [
                {
                    "data": [
                        [
                            1
                        ],
                        [
                            2
                        ],
                        [
                            3
                        ]
                    ],
                    "fields": [
                        "id"
                    ]
                }
            ],
            "sql": "select * from t1"
        },
        "id": "9-1",
        "type": "queries"
    },
    "links": {
        "self": "http://localhost:8989/v1/sql/9/queries/9-1/"
    }
}
```

* An error consists of an object with the `errno` field set to the MariaDB error\
  code, the `message` field set to the human-readable error message and the`sqlstate` field set to the current SQLSTATE of the connection.

```
{
    "data": {
        "attributes": {
            "results": [
                {
                    "errno": 1064,
                    "message": "You have an error in your SQL syntax; check the manual that corresponds to your MariaDB server version for the right syntax to use near 'table t1' at line 1",
                    "sqlstate": "42000"
                }
            ],
            "sql": "select syntax_error from table t1"
        },
        "id": "4-1",
        "type": "queries"
    },
    "links": {
        "self": "http://localhost:8989/v1/sql/4/queries/4-1/"
    }
}
```

* An OK response is returned for any result that completes successfully but not\
  return rows (e.g. an `INSERT` or `UPDATE` statement). The `affected_rows`\
  field contains the number of rows affected by the operation, the`last_insert_id` contains the auto-generated ID and the `warnings` field\
  contains the number of warnings raised by the operation.

```
{
    "data": {
        "attributes": {
            "results": [
                {
                    "affected_rows": 0,
                    "last_insert_id": 0,
                    "warnings": 0
                }
            ],
            "sql": "drop table t1"
        },
        "id": "6-1",
        "type": "queries"
    },
    "links": {
        "self": "http://localhost:8989/v1/sql/6/queries/6-1/"
    }
}
```

It is also possible for the fields of the error response to be present in the\
resultset response if the result ended with an error but still generated some\
data. Usually this happens when query execution is interrupted but a partial\
result was generated by the server.

**Response**

Query successfully executed:

`Status: 201 Created`

```
{
    "data": {
        "attributes": {
            "results": [
                {
                    "affected_rows": 0,
                    "last_insert_id": 0,
                    "warnings": 0
                }
            ],
            "sql": "drop table t1"
        },
        "id": "6-1",
        "type": "queries"
    },
    "links": {
        "self": "http://localhost:8989/v1/sql/6/queries/6-1/"
    }
}
```

Invalid payload or missing connection token:

`Status: 403 Forbidden`

Fatal connection error:

`Status: 503 Service Unavailable`

* If the API returns this response, the connection to the database server was\
  lost. The only valid action to take at this point is to close it with the`DELETE /v1/sql/:id` endpoint.

<sub>_This page is licensed: CC BY-SA / Gnu FDL_</sub>

{% @marketo/form formId="4316" %}
