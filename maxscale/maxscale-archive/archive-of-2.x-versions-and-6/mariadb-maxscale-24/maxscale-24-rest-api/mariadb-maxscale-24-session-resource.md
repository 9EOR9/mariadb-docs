# Session Resource

A session is an abstraction of a client connection, any number of related backend\
connections, a router module session and possibly filter module sessions. Each\
session is created on a service and each service can have multiple sessions.

### Resource Operations

#### Get a session

```
GET /v1/sessions/:id
```

Get a single session. _:id_ must be a valid session ID. The session ID is the\
same that is exposed to the client as the connection ID.

This endpoint also supports the `rdns=true` parameter, which instructs MaxScale to\
perform reverse DNS on the client IP address. As this requires communicating with\
an external server, the operation may be expensive.

**Response**

`Status: 200 OK`

```
{
    "links": {
        "self": "http://localhost:8989/v1/sessions/9"
    },
    "data": {
        "id": "9", // The session ID, same as the one sent to the client
        "type": "sessions",
        "relationships": {
            "services": { // The service that the session uses
                "links": {
                    "self": "http://localhost:8989/v1/services/"
                },
                "data": [
                    {
                        "id": "RW-Split-Router",
                        "type": "services"
                    }
                ]
            }
        },
        "attributes": {
            "state": "Session ready for routing", // Session state
            "user": "maxuser", // The user that this session uses
            "remote": "::ffff:127.0.0.1", // The client address
            "connected": "Mon Jul 17 11:10:39 2017", // The time when the client connected
            "idle": 23.800000000000001 // How many seconds the session has been idle
        },
        "links": {
            "self": "http://localhost:8989/v1/sessions/9"
        }
    }
}
```

#### Get all sessions

```
GET /v1/sessions
```

Get all sessions.

**Response**

`Status: 200 OK`

```
// See `/v1/sessions/:id` for a descriptions of the fields
{
    "links": {
        "self": "http://localhost:8989/v1/sessions/"
    },
    "data": [
        {
            "id": "9",
            "type": "sessions",
            "relationships": {
                "services": {
                    "links": {
                        "self": "http://localhost:8989/v1/services/"
                    },
                    "data": [
                        {
                            "id": "RW-Split-Router",
                            "type": "services"
                        }
                    ]
                }
            },
            "attributes": {
                "state": "Session ready for routing",
                "user": "maxuser",
                "remote": "::ffff:127.0.0.1",
                "connected": "Mon Jul 17 11:10:39 2017",
                "idle": 62.899999999999999
            },
            "links": {
                "self": "http://localhost:8989/v1/sessions/9"
            }
        },
        {
            "id": "10",
            "type": "sessions",
            "relationships": {
                "services": {
                    "links": {
                        "self": "http://localhost:8989/v1/services/"
                    },
                    "data": [
                        {
                            "id": "RW-Split-Router",
                            "type": "services"
                        }
                    ]
                }
            },
            "attributes": {
                "state": "Session ready for routing",
                "user": "skysql",
                "remote": "::ffff:127.0.0.1",
                "connected": "Mon Jul 17 11:11:37 2017",
                "idle": 5.2000000000000002
            },
            "links": {
                "self": "http://localhost:8989/v1/sessions/10"
            }
        }
    ]
}
```

<sub>_This page is licensed: CC BY-SA / Gnu FDL_</sub>

{% @marketo/form formId="4316" %}
