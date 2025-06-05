# MaxScale 24.08 Beta Admin User Resource

## Admin User Resource

Admin users represent administrative users that are able to query and change\
MaxScale's configuration.

* [Admin User Resource](mariadb-maxscale-2408-maxscale-2408-beta-admin-user-resource.md#admin-user-resource)
  * [Resource Operations](mariadb-maxscale-2408-maxscale-2408-beta-admin-user-resource.md#resource-operations)
    * [Get network user](mariadb-maxscale-2408-maxscale-2408-beta-admin-user-resource.md#get-network-user)
      * [Response](mariadb-maxscale-2408-maxscale-2408-beta-admin-user-resource.md#response)
    * [Get all network users](mariadb-maxscale-2408-maxscale-2408-beta-admin-user-resource.md#get-all-network-users)
      * [Response](mariadb-maxscale-2408-maxscale-2408-beta-admin-user-resource.md#response_1)
    * [Get enabled UNIX account](mariadb-maxscale-2408-maxscale-2408-beta-admin-user-resource.md#get-enabled-unix-account)
    * [Get all enabled UNIX accounts](mariadb-maxscale-2408-maxscale-2408-beta-admin-user-resource.md#get-all-enabled-unix-accounts)
    * [Get all users](mariadb-maxscale-2408-maxscale-2408-beta-admin-user-resource.md#get-all-users)
      * [Response](mariadb-maxscale-2408-maxscale-2408-beta-admin-user-resource.md#response_2)
    * [Create a network user](mariadb-maxscale-2408-maxscale-2408-beta-admin-user-resource.md#create-a-network-user)
      * [Response](mariadb-maxscale-2408-maxscale-2408-beta-admin-user-resource.md#response_3)
    * [Enable a UNIX account](mariadb-maxscale-2408-maxscale-2408-beta-admin-user-resource.md#enable-a-unix-account)
      * [Response](mariadb-maxscale-2408-maxscale-2408-beta-admin-user-resource.md#response_4)
    * [Delete a network user](mariadb-maxscale-2408-maxscale-2408-beta-admin-user-resource.md#delete-a-network-user)
      * [Response](mariadb-maxscale-2408-maxscale-2408-beta-admin-user-resource.md#response_5)
    * [Disable a UNIX account](mariadb-maxscale-2408-maxscale-2408-beta-admin-user-resource.md#disable-a-unix-account)
      * [Response](mariadb-maxscale-2408-maxscale-2408-beta-admin-user-resource.md#response_6)
    * [Update a network user](mariadb-maxscale-2408-maxscale-2408-beta-admin-user-resource.md#update-a-network-user)
      * [Response](mariadb-maxscale-2408-maxscale-2408-beta-admin-user-resource.md#response_7)

### Resource Operations

#### Get network user

```
GET /v1/users/inet/:name
```

Get a single network user. The _:name_ in the URI must be a valid network\
user name.

**Response**

`Status: 200 OK`

```
{
    "data": {
        "attributes": {
            "account": "admin",
            "created": "Fri, 05 Jan 2024 07:23:54 GMT",
            "last_login": "Fri, 05 Jan 2024 07:24:11 GMT",
            "last_update": null,
            "name": "admin"
        },
        "id": "admin",
        "links": {
            "self": "http://localhost:8989/v1/users/inet/admin/"
        },
        "type": "inet"
    },
    "links": {
        "self": "http://localhost:8989/v1/users/inet/admin/"
    }
}
```

#### Get all network users

```
GET /v1/users/inet
```

Get all network users.

**Response**

`Status: 200 OK`

```
{
    "data": [
        {
            "attributes": {
                "account": "admin",
                "created": "Fri, 05 Jan 2024 07:23:54 GMT",
                "last_login": "Fri, 05 Jan 2024 07:24:11 GMT",
                "last_update": null,
                "name": "admin"
            },
            "id": "admin",
            "links": {
                "self": "http://localhost:8989/v1/users/inet/admin/"
            },
            "type": "inet"
        }
    ],
    "links": {
        "self": "http://localhost:8989/v1/users/inet/"
    }
}
```

#### Get enabled UNIX account

```
GET /v1/users/unix/:name
```

**Note:** This endpoint has been deprecated and does nothing.

#### Get all enabled UNIX accounts

```
GET /v1/users/unix
```

**Note:** This endpoint has been deprecated and does nothing.

#### Get all users

```
GET /v1/users
```

Get all administrative users.

**Response**

`Status: 200 OK`

```
{
    "data": [
        {
            "attributes": {
                "account": "admin",
                "created": "Fri, 05 Jan 2024 07:23:54 GMT",
                "last_login": "Fri, 05 Jan 2024 07:24:11 GMT",
                "last_update": null,
                "name": "admin"
            },
            "id": "admin",
            "links": {
                "self": "http://localhost:8989/v1/users/inet/admin/"
            },
            "type": "inet"
        }
    ],
    "links": {
        "self": "http://localhost:8989/v1/users/inet/"
    }
}
```

#### Create a network user

```
POST /v1/users/inet
```

Create a new network user. The request body must define at least the\
following fields.

* `data.id`
* The username
* `data.type`
* Type of the object, must be `inet`
* `data.attributes.password`
* The password for this user
* `data.attributes.account`
* Set to `admin` for administrative users and `basic` to read-only users

Only admin accounts can perform POST, PUT, DELETE and PATCH requests. If a basic\
account performs one of the aforementioned request, the REST API will respond\
with a `401 Unauthorized` error.

Here is an example request body defining the network user _my-user_ with the\
password _my-password_ that is allowed to execute only read-only operations.

```
{
    "data": {
        "id": "my-user", // The user to create
        "type": "inet", // The type of the user
        "attributes": {
            "password": "my-password", // The password to use for the user
            "account": "basic" // The type of the account
        }
    }
}
```

**Response**

```
Status: 204 No Content
```

#### Enable a UNIX account

```
POST /v1/users/unix
```

This enables an existing UNIX account on the system for administrative\
operations. The request body must define at least the following fields.

* `data.id`
* The username
* `data.type`
* Type of the object, must be `unix`
* `data.attributes.account`
* Set to `admin` for administrative users and `basic` to read-only users

Here is an example request body enabling the UNIX account _jdoe_ for read-only operations.

```
{
    "data": {
        "id": "jdoe", // Account name
        "type": "unix" // Account type
        "attributes": {
            "account": "basic" // Type of the user account in MaxScale
        }
    }
}
```

**Response**

```
Status: 204 No Content
```

#### Delete a network user

```
DELETE /v1/users/inet/:name
```

The _:name_ part of the URI must be a valid user name.

**Response**

```
Status: 204 No Content
```

#### Disable a UNIX account

```
DELETE /v1/users/unix/:name
```

The _:name_ part of the URI must be a valid user name.

**Response**

```
Status: 204 No Content
```

#### Update a network user

```
PATCH /v1/users/inet/:name
```

Update network user. Currently, only the password can be updated. This\
means that the request body must define the `data.attributes.password`\
field.

Here is an example request body that updates the password.

```
{
    "data": {
        "attributes": {
            "password": "new-password"
        }
    }
}
```

**Response**

```
Status: 204 No Content
```

CC BY-SA / Gnu FDL
