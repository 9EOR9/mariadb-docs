# MaxScale 22.08 Listener Resource

## Listener Resource

## Listener Resource

A listener resource represents a listener of a service in MaxScale. All\
listeners point to a service in MaxScale.

* [Listener Resource](mariadb-maxscale-2208-listener-resource.md#listener-resource)
  * [Resource Operations](mariadb-maxscale-2208-listener-resource.md#resource-operations)
    * [Get a listener](mariadb-maxscale-2208-listener-resource.md#get-a-listener)
      * [Response](mariadb-maxscale-2208-listener-resource.md#response)
    * [Get all listeners](mariadb-maxscale-2208-listener-resource.md#get-all-listeners)
      * [Response](mariadb-maxscale-2208-listener-resource.md#response_1)
    * [Create a new listener](mariadb-maxscale-2208-listener-resource.md#create-a-new-listener)
      * [Response](mariadb-maxscale-2208-listener-resource.md#response_2)
    * [Update a listener](mariadb-maxscale-2208-listener-resource.md#update-a-listener)
      * [Response](mariadb-maxscale-2208-listener-resource.md#response_3)
    * [Destroy a listener](mariadb-maxscale-2208-listener-resource.md#destroy-a-listener)
      * [Response](mariadb-maxscale-2208-listener-resource.md#response_4)
    * [Stop a listener](mariadb-maxscale-2208-listener-resource.md#stop-a-listener)
      * [Parameters](mariadb-maxscale-2208-listener-resource.md#parameters)
      * [Response](mariadb-maxscale-2208-listener-resource.md#response_5)
    * [Start a listener](mariadb-maxscale-2208-listener-resource.md#start-a-listener)
      * [Response](mariadb-maxscale-2208-listener-resource.md#response_6)

### Resource Operations

#### Get a listener

```
GET /v1/listeners/:name
```

Get a single listener. The _:name_ in the URI must be the name of a listener in\
MaxScale.

**Response**

`Status: 200 OK`

```
{
    "data": {
        "attributes": {
            "parameters": {
                "address": "::",
                "authenticator": null,
                "authenticator_options": null,
                "connection_init_sql_file": null,
                "port": 4006,
                "protocol": "MariaDBProtocol",
                "service": "RW-Split-Router",
                "socket": null,
                "sql_mode": "default",
                "ssl": false,
                "ssl_ca": null,
                "ssl_cert": null,
                "ssl_cert_verify_depth": 9,
                "ssl_cipher": null,
                "ssl_crl": null,
                "ssl_key": null,
                "ssl_verify_peer_certificate": false,
                "ssl_verify_peer_host": false,
                "ssl_version": "MAX",
                "type": "listener",
                "user_mapping_file": null
            },
            "source": {
                "file": "/etc/maxscale.cnf",
                "type": "static"
            },
            "state": "Running"
        },
        "id": "RW-Split-Listener",
        "relationships": {
            "services": {
                "data": [
                    {
                        "id": "RW-Split-Router",
                        "type": "services"
                    }
                ],
                "links": {
                    "related": "http://localhost:8989/v1/services/",
                    "self": "http://localhost:8989/v1/listeners/RW-Split-Listener/relationships/services/"
                }
            }
        },
        "type": "listeners"
    },
    "links": {
        "self": "http://localhost:8989/v1/listeners/RW-Split-Listener/"
    }
}
```

#### Get all listeners

```
GET /v1/listeners
```

Get all listeners.

**Response**

`Status: 200 OK`

```
{
    "data": [
        {
            "attributes": {
                "parameters": {
                    "address": "::",
                    "authenticator": null,
                    "authenticator_options": null,
                    "connection_init_sql_file": null,
                    "port": 4006,
                    "protocol": "MariaDBProtocol",
                    "service": "RW-Split-Router",
                    "socket": null,
                    "sql_mode": "default",
                    "ssl": false,
                    "ssl_ca": null,
                    "ssl_cert": null,
                    "ssl_cert_verify_depth": 9,
                    "ssl_cipher": null,
                    "ssl_crl": null,
                    "ssl_key": null,
                    "ssl_verify_peer_certificate": false,
                    "ssl_verify_peer_host": false,
                    "ssl_version": "MAX",
                    "type": "listener",
                    "user_mapping_file": null
                },
                "source": {
                    "file": "/etc/maxscale.cnf",
                    "type": "static"
                },
                "state": "Running"
            },
            "id": "RW-Split-Listener",
            "relationships": {
                "services": {
                    "data": [
                        {
                            "id": "RW-Split-Router",
                            "type": "services"
                        }
                    ],
                    "links": {
                        "related": "http://localhost:8989/v1/services/",
                        "self": "http://localhost:8989/v1/listeners/RW-Split-Listener/relationships/services/"
                    }
                }
            },
            "type": "listeners"
        },
        {
            "attributes": {
                "parameters": {
                    "address": "::",
                    "authenticator": null,
                    "authenticator_options": null,
                    "connection_init_sql_file": null,
                    "port": 4008,
                    "protocol": "MariaDBProtocol",
                    "service": "Read-Connection-Router",
                    "socket": null,
                    "sql_mode": "default",
                    "ssl": false,
                    "ssl_ca": null,
                    "ssl_cert": null,
                    "ssl_cert_verify_depth": 9,
                    "ssl_cipher": null,
                    "ssl_crl": null,
                    "ssl_key": null,
                    "ssl_verify_peer_certificate": false,
                    "ssl_verify_peer_host": false,
                    "ssl_version": "MAX",
                    "type": "listener",
                    "user_mapping_file": null
                },
                "source": {
                    "file": "/etc/maxscale.cnf",
                    "type": "static"
                },
                "state": "Running"
            },
            "id": "Read-Connection-Listener",
            "relationships": {
                "services": {
                    "data": [
                        {
                            "id": "Read-Connection-Router",
                            "type": "services"
                        }
                    ],
                    "links": {
                        "related": "http://localhost:8989/v1/services/",
                        "self": "http://localhost:8989/v1/listeners/Read-Connection-Listener/relationships/services/"
                    }
                }
            },
            "type": "listeners"
        }
    ],
    "links": {
        "self": "http://localhost:8989/v1/listeners/"
    }
}
```

#### Create a new listener

```
POST /v1/listeners
```

Creates a new listener. The request body must define the following fields.

* `data.id`
* Name of the listener
* `data.type`
* Type of the object, must be `listeners`
* `data.attributes.parameters.port` OR `data.attributes.parameters.socket`
* The TCP port or UNIX Domain Socket the listener listens on. Only one of the\
  fields can be defined.
* `data.relationships.services.data`
* The service relationships data, must define a JSON object with an `id` value\
  that defines the service to use and a `type` value set to `services`.

The following is the minimal required JSON object for defining a new listener.

```
{
    "data": {
        "id": "my-listener",
        "type": "listeners",
        "attributes": {
            "parameters": {
                "port": 3306
            }
        },
        "relationships": {
            "services": {
                "data": [
                    {"id": "RW-Split-Router", "type": "services"}
                ]
            }
        }
    }
}
```

Refer to the [Configuration Guide](../../../../../en/maxscale-2208-getting-started-mariadb-maxscale-configuration-guide/) for\
a full list of listener parameters.

**Response**

Listener is created:

`Status: 204 No Content`

#### Update a listener

```
PATCH /v1/listeners/:name
```

The request body must be a JSON object which represents a set of new definitions\
for the listener.

All parameters marked as modifiable at runtime can be modified. Currently, all\
TLS/SSL parameters and the `connection_init_sql_file` and `sql_mode` parameters\
can be modified at runtime.

Parameters that affect the network address or the port the listener listens on\
cannot be modified at runtime. To modify these parameters, recreate the\
listener.

**Response**

Listener is modified:

`Status: 204 No Content`

#### Destroy a listener

```
DELETE /v1/listeners/:name
```

The _:name_ must be a valid listener name. When a listener is destroyed, the\
network port it listens on is available for reuse.

**Response**

Listener is destroyed:

`Status: 204 No Content`

Listener cannot be deleted:

`Status: 400 Bad Request`

#### Stop a listener

```
PUT /v1/listeners/:name/stop
```

Stops a started listener. When a listener is stopped, new connections are no\
longer accepted and are queued until the listener is started again.

**Parameters**

This endpoint supports the following parameters:

* `force=yes`
* Close all existing connections that were created through this listener.

**Response**

Listener is stopped:

`Status: 204 No Content`

#### Start a listener

```
PUT /v1/listeners/:name/start
```

Starts a stopped listener.

**Response**

Listener is started:

`Status: 204 No Content`

CC BY-SA / Gnu FDL
