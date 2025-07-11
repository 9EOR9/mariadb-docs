# MariaDB MaxScale Configuration & Usage Scenarios

* [MariaDB MaxScale Configuration Guide](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#mariadb-maxscale-configuration-guide)
* [Introduction](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#introduction)
* [Concepts](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#concepts)
  * [Glossary](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#glossary)
  * [Objects](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#objects)
    * [Server](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#server)
    * [Protocol](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#protocol)
    * [Monitor](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#monitor)
    * [Filter](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#filter)
    * [Router](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#router)
    * [Service](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#service)
    * [Listener](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#listener)
* [Administration](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#administration)
  * [Static Configuration Parameters](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#static-configuration-parameters)
* [Configuration](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#configuration)
  * [Special Parameter Types](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#special-parameter-types)
    * [Sizes](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#sizes)
    * [Regular Expressions](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#regular-expressions)
      * [Standard regular expression settings for filters](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#standard-regular-expression-settings-for-filters)
  * [Global Settings](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#global-settings)
    * [threads](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#threads)
    * [thread\_stack\_size](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#thread_stack_size)
    * [auth\_connect\_timeout](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#auth_connect_timeout)
    * [auth\_read\_timeout](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#auth_read_timeout)
    * [auth\_write\_timeout](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#auth_write_timeout)
    * [query\_retries](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#query_retries)
    * [query\_retry\_timeout](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#query_retry_timeout)
    * [passive](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#passive)
    * [ms\_timestamp](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#ms_timestamp)
    * [skip\_permission\_checks](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#skip_permission_checks)
    * [syslog](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#syslog)
    * [maxlog](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#maxlog)
    * [log\_to\_shm](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#log_to_shm)
    * [log\_warning](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#log_warning)
    * [log\_notice](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#log_notice)
    * [log\_info](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#log_info)
    * [log\_debug](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#log_debug)
    * [log\_messages](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#log_messages)
    * [log\_trace](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#log_trace)
    * [log\_augmentation](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#log_augmentation)
    * [log\_throttling](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#log_throttling)
    * [logdir](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#logdir)
    * [datadir](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#datadir)
    * [libdir](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#libdir)
    * [cachedir](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#cachedir)
    * [piddir](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#piddir)
    * [execdir](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#execdir)
    * [connector\_plugindir](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#connector_plugindir)
    * [persistdir](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#persistdir)
    * [module\_configdir](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#module_configdir)
    * [language](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#language)
    * [query\_classifier](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#query_classifier)
    * [query\_classifier\_cache\_size](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#query_classifier_cache_size)
    * [query\_classifier\_args](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#query_classifier_args)
      * [log\_unrecognized\_statements](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#log_unrecognized_statements)
    * [substitute\_variables](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#substitute_variables)
    * [sql\_mode](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#sql_mode)
    * [local\_address](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#local_address)
    * [users\_refresh\_time](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#users_refresh_time)
    * [retain\_last\_statements](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#retain_last_statements)
    * [dump\_last\_statements](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#dump_last_statements)
    * [session\_trace](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#session_trace)
    * [writeq\_high\_water](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#writeq_high_water)
    * [writeq\_low\_water](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#writeq_low_water)
    * [load\_persisted\_configs](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#load_persisted_configs)
    * [REST API Configuration](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#rest-api-configuration)
    * [admin\_host](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#admin_host)
    * [admin\_port](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#admin_port)
    * [admin\_auth](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#admin_auth)
    * [admin\_ssl\_key](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#admin_ssl_key)
    * [admin\_ssl\_cert](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#admin_ssl_cert)
    * [admin\_ssl\_ca\_cert](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#admin_ssl_ca_cert)
    * [admin\_enabled](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#admin_enabled)
    * [admin\_log\_auth\_failures](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#admin_log_auth_failures)
  * [Events](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#events)
    * ['authentication\_failure'](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#authentication_failure)
  * [Service](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#service_1)
    * [router](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#router_1)
    * [router\_options](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#router_options)
    * [filters](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#filters)
    * [servers](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#servers)
    * [user](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#user)
    * [password](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#password)
    * [enable\_root\_user](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#enable_root_user)
    * [localhost\_match\_wildcard\_host](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#localhost_match_wildcard_host)
    * [version\_string](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#version_string)
    * [weightby](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#weightby)
    * [auth\_all\_servers](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#auth_all_servers)
    * [strip\_db\_esc](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#strip_db_esc)
    * [retry\_on\_failure](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#retry_on_failure)
    * [log\_auth\_warnings](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#log_auth_warnings)
    * [connection\_timeout](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#connection_timeout)
    * [max\_connections](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#max_connections)
    * [max\_retry\_interval](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#max_retry_interval)
    * [session\_track\_trx\_state](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#session_track_trx_state)
    * [retain\_last\_statements](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#retain_last_statements_1)
  * [Server](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#server_1)
    * [address](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#address)
    * [port](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#port)
    * [protocol](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#protocol_1)
    * [monitoruser](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#monitoruser)
    * [monitorpw](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#monitorpw)
    * [extra\_port](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#extra_port)
    * [persistpoolmax](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#persistpoolmax)
    * [persistmaxtime](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#persistmaxtime)
    * [proxy\_protocol](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#proxy_protocol)
    * [authenticator](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#authenticator)
    * [authenticator\_options](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#authenticator_options)
    * [disk\_space\_threshold](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#disk_space_threshold)
  * [Listener](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#listener_1)
    * [service](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#service_2)
    * [protocol](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#protocol_2)
    * [address](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#address_1)
    * [port](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#port_1)
    * [socket](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#socket)
    * [authenticator](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#authenticator_1)
    * [authenticator\_options](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#authenticator_options_1)
* [Available Protocols](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#available-protocols)
  * [MariaDBClient](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#mariadbclient)
  * [MariaDBBackend](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#mariadbbackend)
  * [telnetd](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#telnetd)
  * [maxscaled](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#maxscaled)
  * [HTTPD](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#httpd)
* [TLS/SSL encryption](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#tlsssl-encryption)
  * [ssl](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#ssl)
  * [ssl\_key](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#ssl_key)
  * [ssl\_cert](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#ssl_cert)
  * [ssl\_ca\_cert](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#ssl_ca_cert)
  * [ssl\_version](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#ssl_version)
  * [ssl\_cert\_verify\_depth](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#ssl_cert_verify_depth)
  * [ssl\_verify\_peer\_certificate](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#ssl_verify_peer_certificate)
    * [Example SSL enabled server configuration](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#example-ssl-enabled-server-configuration)
    * [Example SSL enabled listener configuration](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#example-ssl-enabled-listener-configuration)
* [Module Types](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#module-types)
  * [Routing Modules](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#routing-modules)
  * [Diagnostic modules](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#diagnostic-modules)
  * [Monitor Modules](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#monitor-modules)
  * [Filter Modules](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#filter-modules)
* [Encrypting Passwords](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#encrypting-passwords)
  * [Creating Encrypted Passwords](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#creating-encrypted-passwords)
* [Runtime Configuration Changes](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#runtime-configuration-changes)
  * [Backing Up Configuration Changes](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#backing-up-configuration-changes)
* [Error Reporting](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#error-reporting)
* [Limitations](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#limitations)
* [Troubleshooting](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#troubleshooting)
  * [Authentication](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#authentication)
    * [Wildcard Hosts](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#wildcard-hosts)
  * [Systemd Watchdog](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#systemd-watchdog)

## Introduction

This document describes how to configure MariaDB MaxScale and presents some\
possible usage scenarios. MariaDB MaxScale is designed with flexibility in mind,\
and consists of an event processing core with various support functions and\
plugin modules that tailor the behavior of the program.

## Concepts

### Glossary

| Word                | Description                                                                                                                                                                                                                                                                                                                                      |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Word                | Description                                                                                                                                                                                                                                                                                                                                      |
| connection routing  | Connection routing is a method of handling requests in which MariaDB MaxScale will accept connections from a client and route data on that connection to a single database using a single connection. Connection based routing will not examine individual requests on a connection and it will not move that connection once it is established. |
| statement routing   | Statement routing is a method of handling requests in which each request within a connection will be handled individually. Requests may be sent to one or more servers and connections may be dynamically added or removed from the session.                                                                                                     |
| module              | A module is a separate code entity that may be loaded dynamically into MariaDB MaxScale to increase the available functionality. Modules are implemented as run-time loadable shared objects.                                                                                                                                                    |
| connection failover | When a connection currently being used between MariaDB MaxScale and the database server fails a replacement will be automatically created to another server by MariaDB MaxScale without client intervention                                                                                                                                      |
| backend database    | A term used to refer to a database that sits behind MariaDB MaxScale and is accessed by applications via MariaDB MaxScale.                                                                                                                                                                                                                       |
| REST API            | HTTP administrative interface                                                                                                                                                                                                                                                                                                                    |

### Objects

#### Server

A server represents an individual database server to which a client can be\
connected via MariaDB MaxScale. The status of a server varies during the lifetime\
of the server and typically the status is updated by some monitor. However, it\
is also possible to update the status of a server manually.

| Status                   | Description                                                                                                                                                                                                                                                                                                               |
| ------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Status                   | Description                                                                                                                                                                                                                                                                                                               |
| Running                  | The server is running.                                                                                                                                                                                                                                                                                                    |
| Master                   | The server is the master.                                                                                                                                                                                                                                                                                                 |
| Slave                    | The server is a slave.                                                                                                                                                                                                                                                                                                    |
| Auth Error               | The monitor cannot login and query the server due to insufficient privileges.                                                                                                                                                                                                                                             |
| Maintenance              | The server is under maintenance. Typically this status bit is turned on manually using maxctrl, but it will also be turned on for a server that for some reason is blocking connections from MaxScale. When a server is in maintenace mode, no connections will be created to it and existing connections will be closed. |
| Slave of External Master | The server is a slave of a master that is not being monitored.                                                                                                                                                                                                                                                            |

#### Protocol

A protocol module is responsible for the low-level communication between\
MaxScale and either clients of MaxScale or servers exposed by MaxScale.\
The most commonly used protocol modules are `mariadbclient` and`mariadbbackend`.

Protocol modules do not have sections of their own in the MaxScale\
configuration file, but are referred to from _servers_ and _listeners_.

#### Monitor

A monitor module is capable of monitoring the state of a particular kind\
of cluster and making that state available to the routers of MaxScale.

Examples of monitor modules are `mariadbmon` that is capable of monitoring\
a regular master-slave cluster and in addition of performing both _switchover_\
and _failover_, `galeramon` that is capable of monitoring a Galera cluster,\
and `csmon` that is capable of monitoring a Columnstore cluster.

Monitor modules have sections of their own in the MaxScale configuration\
file.

#### Filter

A filter module resides in front of routers in the request processing chain\
of MaxScale. That is, a filter will see a request before it reaches the router\
and before a response is sent back to the client. This allows filters to\
reject, handle, alter or log information about a request.

Examples of filters are `dbfwfilter` that is a configurable firewall, `cache`\
that provides query caching according to rules, `regexfilter` that can rewrite\
requests according to regular expressions, and `qlafilter` that logs\
information about requests.

Filters have sections of their own in the MaxScale configuration file that are\
referred to from _services_.

#### Router

A router module is capable of routing requests to backend servers according to\
the characteristics of a request and/or the algorithm the router\
implements. Examples of routers are `readconnroute` that provides _connection_\
\&#xNAN;_routing_, that is, the server is chosen according to specified rules when the\
session is created and all requests are subsequently routed to that server,\
and `readwritesplit` that provides _statement routing_, that is, each\
individual request is routed to the most appropriate server.

Routers do not have sections of their own in the MaxScale configuration file,\
but are referred to from _services_.

#### Service

A service abstracts a set of databases and makes them appear as a single one\
to the client. Depending on what router (e.g. `readconnroute` or`readwritesplit`) the service uses, the servers are used in some particular\
way. If the service uses filters, then all requests will be pre-processed in\
some way before they reach the router.

Services have sections of their own in the MaxScale configuration file.

#### Listener

A listener defines a port MaxScale listens on. Connection requests arriving on\
that port will be forwarded to the service the listener is associated with. A\
listener may be associated with a single service, but several listeners may be\
associated with the same service.

Listeners have sections of their own in the MaxScale configuration file.

## Administration

The administation of MaxScale can be divided in two parts:

* Writing the MaxScale configuration file, which is described in the following[section](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#configuration).
* Performing runtime modifications using [MaxCtrl](../maxscale-23-reference/mariadb-maxscale-23-maxctrl.md)\
  or [MaxAdmin](../maxscale-23-reference/mariadb-maxscale-23-maxadmin-admin-interface.md).

For detailed information about _MaxAdmin_ and _MaxCtrl_ please refer to the\
specific documentation referred to above. In the following it will only be\
explained how MaxAdmin and MaxCtrl relate to each other, as far as user\
credentials go.

MaxAdmin can connect to MaxScale either using Unix (domain) sockets or\
TCP/IP sockets. In the former case, the user is identified using her\
Linux credentials and by default `root` can access.

MaxCtrl can only connect using TCP/IP sockets. When connecting with\
MaxCtrl or with MaxAdmin using TCP/IP sockets, the user and password\
must be provided and are checked against a separate user credentials\
database. By default, that database contains the user `admin` whose\
password is `mariadb`.

Note that the database is shared between MaxAdmin and MaxCtrl, that is,\
if a user is deleted via MaxAdmin, then it will also no longer be possible\
to use that user with MaxCtrl. Similarly, a user created using MaxAdmin\
or MaxCtrl can be used with either MaxAdmin or MaxCtrl.

Note that if MaxAdmin (when used over a TCP/IP socket) or MaxCtrl are\
invoked without explicitly providing a user and password then they will\
by default use `admin` and `mariadb`. That means that when the default\
user is removed, the credentials must always be provided.

### Static Configuration Parameters

The following list of global configuration parameters can **NOT** be changed at\
runtime and can only be defined in a configuration file:

* `threads`
* `thread_stack_size`
* `log_to_shm`
* `log_augmentation`
* `logdir`
* `datadir`
* `libdir`
* `cachedir`
* `piddir`
* `execdir`
* `connector_plugindir`
* `persistdir`
* `module_configdir`
* `language`
* `query_classifier`
* `query_classifier_args`
* `substitute_variables`
* `sql_mode`
* `local_address`
* `users_refresh_time`
* `load_persisted_configs`
* `admin_auth`
* `admin_ssl_key`
* `admin_ssl_cert`
* `admin_ssl_ca_cert`
* `admin_enabled`

All other parameters that relate to objects can be altered at runtime or can be\
changed by destroying and recreating the object in question.

## Configuration

The MariaDB MaxScale configuration is read from a file that MariaDB MaxScale\
will look for in the following places:

1. By default, the file `maxscale.cnf` in the directory `/etc`
2. The location given with the `--configdir=<path>` command line argument.

MariaDB MaxScale will further look for a directory with the same name as the\
configuration file, followed by `.d` (for instance `/etc/maxscale.cnf.d`) and\
recursively read all files, having a `.cnf` suffix, it finds in the directory\
hierarchy. All other files will be ignored.

There are no restrictions on how different configuration sections are arranged,\
but the strong suggestion is to place global settings into the configuration\
file MariaDB MaxScale is invoked with, and then, if deemed necessary, create\
separate configuration files for _servers_, _filters_, etc.

The configuration file itself is based on the[.ini](https://en.wikipedia.org/wiki/INI_file) file format and consists of\
various sections that are used to build the configuration; these sections define\
services, servers, listeners, monitors and global settings. Parameters, which\
expect a comma-separated list of values can be defined on multiple lines. The\
following is an example of a multi-line definition.

```
[MyService]
type=service
router=readconnroute
servers=server1,
        server2,
        server3
```

The values of the parameter that are not on the first line need to have at least\
one whitespace character before them in order for them to be recognized as a\
part of the multi-line parameter.

Comments are defined by prefixing a row with a hash (`#`). Trailing comments are\
not supported.

```
# This is a comment before a parameter
some_parameter=123
```

### Special Parameter Types

#### Sizes

Where _specifically noted_, a number denoting a size can be suffixed by a subset\
of the IEC binary prefixes or the SI prefixes. In the former case the number\
will be interpreted as a certain multiple of 1024 and in the latter case as a\
certain multiple of 1000. The supported IEC binary suffixes are `Ki`, `Mi`, `Gi`\
and `Ti` and the supported SI suffixes are `k`, `M`, `G` and `T`. In both cases,\
the matching is case insensitive.

For instance, the following entries

```
max_size=1099511628000
max_size=1073741824Ki
max_size=1048576Mi
max_size=1024Gi
max_size=1Ti
```

are equivalent, as are the following

```
max_size=1000000000000
max_size=1000000000k
max_size=1000000M
max_size=1000G
max_size=1T
```

#### Regular Expressions

Many modules have settings which accept a regular expression. In most cases, these\
settings are named either _match_ or _exclude_, and are used to filter users or queries.\
MaxScale uses the [PCRE2-library](https://www.pcre.org/current/doc/html/) for matching\
regular expressions.

When writing a regular expression (regex) type parameter to a MaxScale configuration file,\
the pattern string should be enclosed in slashes e.g. `^select` -> `match=/^select/`. This\
clarifies where the pattern begins and ends, even if it includes whitespace. Without\
slashes the configuration loader trims the pattern from the ends. The slashes are removed\
before compiling the pattern. For backwards compatibility, the slashes are not yet\
mandatory. Omitting them is, however, deprecated and will be rejected in a future release\
of MaxScale. Currently, _binlogfilter_, _ccrfilter_, _qlafilter_, _tee_ and _avrorouter_\
accept parameters in this type of regular expression form. Some other modules may not\
handle the slashes yet correctly.

PCRE2 supports a complicated regular expression[syntax](https://www.pcre.org/current/doc/html/pcre2syntax.html). MaxScale typically uses\
regular expressions simply, only checking whether the pattern and subject match at some\
point. For example, using the QLAFilter and setting `match=/SELECT/` causes the filter to\
accept any query with the text "SELECT" somewhere within. To force the pattern to only\
match at the beginning of the query, set `match=/^SELECT/`. To only match the end, set`match=/SELECT$/`.

Modules which accept regular expression parameters also often accept options which affect\
how the patterns are compiled. Typically, this setting is called _options_ and accepts\
values such as `ignorecase`, `case` and `extended`. `ignorecase` causes the regular\
expression matcher to ignore letter case, and is often on by default. `extended` ignores\
whitespace in the pattern. `case` turns on case-sensitive matching. These settings can\
also be defined in the pattern itself, so they can be used even in modules without\
pattern compilation settings. The pattern settings are `(?i)` for `ignorecase` and `(?x)`\
for `extended`. See the[PCRE2 syntax documentation](https://www.pcre.org/current/doc/html/pcre2syntax.html#SEC16)\
for more information.

**Standard regular expression settings for filters**

Many filters use the settings _match_, _exclude_ and _options_. Since these settings are\
used in a similar way across these filters, the settings are explained here. The\
documentation of the filters link here and describe any exceptions to this\
generalized explanation.

These settings typically limit the queries the filter module acts on. _match_ an&#x64;_&#x65;xclude_ define PCRE2 regular expression patterns while _options_ affects how both of the\
patterns are compiled. _options_ works as explained above, accepting the values`ignorecase`, `case` and `extended`, with `ignorecase` being the default.

The queries are matched as they arrive to the filter on their way to a routing module. I&#x66;_&#x6D;atch_ is defined, the filter only acts on queries matching that pattern. If _match_ is\
not defined, all queries are considered to match.

If _exclude_ is defined, the filter only acts on queries not matching that pattern. I&#x66;_&#x65;xclude_ is not defined, nothing is excluded.

If both are defined, the query needs to match _match_ but not match _exclude_.

Even if a filter does not act on a query, the query is not lost. The query is simply\
passed on to the next module in the processing chain as if the filter was not there.

### Global Settings

The global settings, in a section named `[MaxScale]`, allow various parameters\
that affect MariaDB MaxScale as a whole to be tuned. This section must be\
defined in the root configuration file which by default is `/etc/maxscale.cnf`.

#### `threads`

This parameter controls the number of worker threads that are handling the\
events coming from the kernel. The default is 1 thread. It is recommended that\
you start with one thread and increase the number if you require greater\
performance. Increasing the amount of worker threads beyond the number of\
processor cores does not improve the performance, rather is likely to degrade\
it, and can consume resources needlessly.

You can enable automatic configuration of this value by setting the value to`auto`. This way MariaDB MaxScale will detect the number of available processors\
and set the amount of threads to be equal to that number. This should only be\
used for systems dedicated for running MariaDB MaxScale.

```
# Valid options are:
#       threads=[<number of threads> | auto ]

[MaxScale]
threads=1
```

Additional threads will be created to execute other internal services within\
MariaDB MaxScale. This setting is used to configure the number of threads that\
will be used to manage the user connections.

#### `thread_stack_size`

Ignored and deprecated in 2.3.

If you need to explicitly set the stack size, do so using `ulimit -s` before\
starting MaxScale.

#### `auth_connect_timeout`

The connection timeout in seconds for the MySQL connections to the backend\
server when user authentication data is fetched. Increasing the value of this\
parameter will cause MariaDB MaxScale to wait longer for a response from the\
backend server before aborting the authentication process. The default is 3\
seconds.

```
auth_connect_timeout=10
```

#### `auth_read_timeout`

The read timeout in seconds for the MySQL connection to the backend database\
when user authentication data is fetched. Increasing the value of this parameter\
will cause MariaDB MaxScale to wait longer for a response from the backend\
server when user data is being actively fetched. If the authentication is\
failing and you either have a large number of database users and grants or the\
connection to the backend servers is slow, it is a good idea to increase this\
value. The default is 1 second.

```
auth_read_timeout=10
```

#### `auth_write_timeout`

The write timeout in seconds for the MySQL connection to the backend database\
when user authentication data is fetched. Currently MariaDB MaxScale does not\
write or modify the data in the backend server. The default is 2 seconds.

```
auth_write_timeout=10
```

#### `query_retries`

The number of times an interrupted internal query will be retried. The default\
is to retry the query once. This feature was added in MaxScale 2.1.10 and was\
disabled by default until MaxScale 2.3.0.

An interrupted query is any query that is interrupted by a network\
error. Connection timeouts are included in network errors and thus is it\
advisable to make sure that the value of `query_retry_timeout` is set to an\
adequate value. Internal queries are only used to retrieve authentication data\
and monitor the servers.

#### `query_retry_timeout`

The total timeout in seconds for any retried queries. The default value is 5\
seconds.

An interrupted query is retried for either the configured amount of attempts or\
until the configured timeout is reached.

#### `passive`

Controls whether MaxScale is a passive node in a cluster of multiple MaxScale\
instances. The default value is false.

This parameter is intended to be used with multiple MaxScale instances that use\
failover functionality to manipulate the cluster in some form. Passive nodes\
only observe the clusters being monitored and take no direct actions.

The following functionality is disabled when passive mode is enabled:

* Automatic failover in the `mariadbmon` module
* Automatic rejoin in the `mariadbmon` module
* Launching of monitor scripts

**NOTE:** Even if MaxScale is in passive mode, it will still accept clients and\
route any traffic sent to it. The **only** operations affected by the passive\
mode are the ones listed above.

#### `ms_timestamp`

Enable or disable the high precision timestamps in logfiles. Enabling this adds\
millisecond precision to all logfile timestamps.

```
# Valid options are:
#       ms_timestamp=<0|1>
ms_timestamp=1
```

#### `skip_permission_checks`

Skip service and monitor user permission checks. This is useful when you know\
the permissions are OK and you want to speed up the startup process. This\
parameter takes a boolean value and is disabled by default.

It is recommended to not disable the permission checks so that any missing\
privileges are detected when maxscale is starting up. If you are experiencing a\
slow startup of MaxScale due to large amounts of connection timeouts when\
permissions are checked, disabling the permission checks could speed up the\
startup process.

```
skip_permission_checks=true
```

#### `syslog`

Enable or disable the logging of messages to _syslog_.

By default logging to _syslog_ is enabled.

```
# Valid options are:
#       syslog=<0|1>
syslog=1
```

To enable logging to syslog use the value 1 and to disable use the value 0.

#### `maxlog`

Enable to disable to logging of messages to MariaDB MaxScale's log file.

By default logging to _maxlog_ is enabled.

```
# Valid options are:
#       syslog=<0|1>
maxlog=1
```

To enable logging to the MariaDB MaxScale log file use the value 1 and to\
disable use the value 0.

#### `log_to_shm`

**Note:** This parameter is deprecated and it is ignored by MaxScale versions\
2.3.0 and newer. If you want to store the log in shared memory, define the\
directory with `logdir` in `/dev/shm`.

In older MaxScale versions, the actual log file was created in `/dev/shm` and a\
symbolic link to that file was stored in place of the normal MaxScale log.

#### `log_warning`

Enable or disable the logging of messages whose syslog priority is _warning_.\
Messages of this priority are enabled by default.

```
# Valid options are:
#       log_warning=<0|1>
log_warning=0
```

To disable these messages use the value 0 and to enable them use the value 1.

#### `log_notice`

Enable or disable the logging of messages whose syslog priority is _notice_.\
Messages of this priority provide information about the functioning of MariaDB\
MaxScale and are enabled by default.

```
# Valid options are:
#       log_notice=<0|1>
log_notice=0
```

To disable these messages use the value 0 and to enable them use the value 1.

#### `log_info`

Enable or disable the logging of messages whose syslog priority is _info_. These\
messages provide detailed information about the internal workings of MariaDB\
MaxScale and should not, due to their frequency, be enabled, unless there is a\
specific reason for that. For instance, from these messages it will be evident,\
e.g., why a particular query was routed to the master instead of to a slave.\
These informational messages are disabled by default.

```
# Valid options are:
#       log_info=<0|1>
log_info=1
```

To disable these messages use the value 0 and to enable them use the value 1.

#### `log_debug`

Enable or disable the logging of messages whose syslog priority is _debug_. This\
kind of messages are intended for development purposes and are disabled by\
default. Note that if MariaDB MaxScale has been built in release mode, then\
debug messages are excluded from the build and this setting will not have any\
effect.

```
# Valid options are:
#       log_debug=<0|1>
log_debug=1
```

To disable these messages use the value 0 and to enable them use the value 1.

#### `log_messages`

**Deprecated** Use _log\_notice_ instead.

#### `log_trace`

**Deprecated** Use _log\_info_ instead.

#### `log_augmentation`

Enable or disable the augmentation of messages. If this is enabled, then each\
logged message is appended with the name of the function where the message was\
logged. This is primarily for development purposes and hence is disabled by\
default.

```
# Valid options are:
#       log_augmentation=<0|1>
log_augmentation=1
```

To disable the augmentation use the value 0 and to enable it use the value 1.

#### `log_throttling`

It is possible that a particular error (or warning) is logged over and over\
again, if the cause for the error persistently remains. To prevent the log from\
flooding, it is possible to specify how many times a particular error may be\
logged within a time period, before the logging of that error is suppressed for\
a while.

```
# A valid value looks like
#       log_throttling = X, Y, Z
#
# where each value is a positive integer and X means the number of times a
# specific error may be logged within a time period of Y milliseconds, before
# the logging of that error is suppressed for Z milliseconds.
log_throttling=8, 2000, 15000
```

In the example above, the logging of a particular error will be suppressed for\
15 seconds if the error has been logged 8 times in 2 seconds.

The default is `10, 1000, 10000`, which means that if the same error is logged\
10 times in one second, the logging of that error is suppressed for the\
following 10 seconds.

To disable log throttling, add an entry with an empty value

```
log_throttling=
```

or one where any of the integers is 0.

```
log_throttling=0, 0, 0
```

Note that _notice_, _info_ and _debug_ messages are never throttled.

#### `logdir`

Set the directory where the logfiles are stored. The folder needs to be both\
readable and writable by the user running MariaDB MaxScale.

```
logdir=/tmp/
```

#### `datadir`

Set the directory where the data files used by MariaDB MaxScale are stored.\
Modules can write to this directory and for example the binlogrouter uses this\
folder as the default location for storing binary logs.

This is also the directory where the password encryption key is read from that\
is generated by `maxkeys`.

```
datadir=/home/user/maxscale_data/
```

#### `libdir`

Set the directory where MariaDB MaxScale looks for modules. The library\
directory is the only directory that MariaDB MaxScale uses when it searches for\
modules. If you have custom modules for MariaDB MaxScale, make sure you have\
them in this folder.

```
libdir=/home/user/lib64/
```

#### `cachedir`

Configure the directory MariaDB MaxScale uses to store cached data. An example\
of cached data is the authentication data fetched from the backend servers.\
MariaDB MaxScale stores this in case a connection to the backend server is not\
possible.

```
cachedir=/tmp/maxscale_cache/
```

#### `piddir`

Configure the directory for the PID file for MariaDB MaxScale. This file\
contains the Process ID for the running MariaDB MaxScale process.

```
piddir=/tmp/maxscale_cache/
```

#### `execdir`

Configure the directory where the executable files reside. All internal\
processes which are launched will use this directory to look for executable\
files.

```
execdir=/usr/local/bin/
```

#### `connector_plugindir`

Location of the MariaDB Connector-C plugin directory. The MariaDB Connector-C\
used in MaxScale can use this directory to load authentication plugins. The\
versions of the plugins must be binary compatible with the connector version\
that MaxScale was built with.

```
connector_plugindir=/usr/lib/plugin/
```

#### `persistdir`

Configure the directory where persisted configurations are stored. When a new\
server is created via MaxAdmin, it will be stored in this directory. Do not use\
or modify the contents of this directory, use _/etc/maxscale.cnf.d/_ instead.

```
persistdir=/var/lib/maxscale/maxscale.cnf.d/
```

#### `module_configdir`

Configure the directory where module configurations are stored. Path arguments\
are resolved relative to this directory. This directory should be used to store\
module specific configurations e.g. dbfwfilter rule files.

Any configuration parameter that is not an absolute path will be interpreted as\
a relative path. The relative paths use the module configuration directory as\
the working directory.

For example, the configuration parameter `file=my_file.txt` would be interpreted\
as `/etc/maxscale.cnf.d/my_file.txt` whereas `file=/home/user/my_file.txt` would\
be interpreted as `/home/user/my_file.txt`.

```
module_configdir=/var/lib/maxscale/
```

#### `language`

Set the folder where the errmsg.sys file is located in. MariaDB MaxScale will\
look for the errmsg.sys file installed with MariaDB MaxScale from this folder.

```
language=/home/user/lang/
```

#### `query_classifier`

The module used by MariaDB MaxScale for query classification. The information\
provided by this module is used by MariaDB MaxScale when deciding where a\
particular statement should be sent. The default query classifier i&#x73;_&#x71;c\_sqlite_.

#### `query_classifier_cache_size`

Specifies the maximum size of the query classifier cache. The default limit is\
15% of total system memory starting with MaxScale 2.3.7. In older versions the\
default limit was 40% of total system memory. This feature was added in MaxScale\
2.3.0.

When the query classifier cache has been enabled, MaxScale will, after a\
statement has been parsed, store the classification result using the\
canonicalized version of the statement as the key.

If the classification result for a statement is needed, MaxScale will first\
canonicalize the statement and check whether the result can be found in the\
cache. If it can, the statement will not be parsed at all but the cached result\
is used.

The configuration parameter takes one integer that specifies the maximum size of\
the cache. The size of the cache can be specifed as explained [here](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#sizes).

```
# 1MB query classifier cache
query_classifier_cache_size=1MB
```

Note that MaxScale uses a separate cache for each worker thread. To obtain the\
amount of memory available for each thread, divide the cache size with the value\
of `threads`. If statements are evicted from the cache (visible in the\
diagnostic output), consider increasing the cache size.

Using `maxctrl show threads` it is possible to check what the actual size of\
the cache is and to see performance statistics.

| Key                | Meaning                                                                                                                 |
| ------------------ | ----------------------------------------------------------------------------------------------------------------------- |
| Key                | Meaning                                                                                                                 |
| QC cache size      | The current size of the cache (bytes).                                                                                  |
| QC cache inserts   | How many entries have been inserted into the cache.                                                                     |
| QC cache hits      | How many times the classification result has been found from the cache.                                                 |
| QC cache misses    | How many times the classification result has not been found from the cache, but the classification had to be performed. |
| QC cache evictions | How many times a cache entry has had to be removed from the cache, in order to make place for another.                  |

#### `query_classifier_args`

Arguments for the query classifier. What arguments are accepted depends on the\
particular query classifier being used. The default query classifier -_qc\_sqlite_ - supports the following arguments:

**`log_unrecognized_statements`**

An integer argument taking the following values:

* 0: Nothing is logged. This is the default.
* 1: Statements that cannot be parsed completely are logged. They may have been\
  partially parsed, or classified based on keyword matching.
* 2: Statements that cannot even be partially parsed are logged. They may have\
  been classified based on keyword matching.
* 3: Statements that cannot even be classified by keyword matching are logged.

```
query_classifier=qc_sqlite
query_classifier_args=log_unrecognized_statements=1
```

This will log all statements that cannot be parsed completely. This may be\
useful if you suspect that MariaDB MaxScale routes statements to the wrong\
server (e.g. to a slave instead of to a master).

#### `substitute_variables`

Enable or disable the substitution of environment variables in the MaxScale\
configuration file. If the substitution of variables is enabled and a\
configuration line like

```
some_parameter=$SOME_VALUE
```

is encountered, then `$SOME_VALUE` will be replaced with the actual value\
of the environment variable `SOME_VALUE`. Note:_Variable substitution will be made only if '$' is the first character_\
\&#xNAN;_of the value._ _Everything_ following '$' is interpreted as the name of the environment\
variable.

* Referring to a non-existing environment variable is a fatal error.

By default, the value of `substitute_variables` is `false`.

```
substitute_variables=true
```

The setting of `substitute_variables` will have an effect on all parameters\
in the all other sections, irrespective of where the `[maxscale]` section\
is placed in the configuration file. However, in the `[maxscale]` section,\
to ensure that substitution will take place, place the`substitute_variables=true` line first.

#### `sql_mode`

Specifies whether the query classifier parser should initially expect _MariaDB_\
or _PL/SQL_ kind of SQL.

The allowed values are:`default`: The parser expects regular _MariaDB_ SQL.`oracle` : The parser expects PL/SQL.

```
sql_mode=oracle
```

The default value is `default`.

**NOTE** If `sql_mode` is set to `oracle`, then MaxScale will also assume\
that `autocommit` initially is off.

At runtime, MariaDB MaxScale will recognize statements like

```
set sql_mode=oracle;
```

and

```
set sql_mode=default;
```

and change mode accordingly.

**NOTE** If `set sql_mode=oracle;` is encountered, then MaxScale will also\
behave as if `autocommit` had been turned off and conversely, if`set sql_mode=default;` is encountered, then MaxScale will also behave\
as if `autocommit` had been turned on.

Note that MariaDB MaxScale is **not** explicitly aware of the sql mode of\
the server, so the value of `sql_mode` should reflect the sql mode used\
when the server is started.

#### `local_address`

What specific local address/interface to use when connecting to servers.

This can be used for ensuring that MaxScale uses a particular interface\
when connecting to servers, in case the computer MaxScale is running on\
has multiple interfaces.

```
local_address=192.168.1.254
```

#### `users_refresh_time`

How often, in seconds, MaxScale at most may refresh the users from the\
backend server.

MaxScale will at startup load the users from the backend server, but if\
the authentication of a user fails, MaxScale assumes it is because a new\
user has been created and will thus refresh the users. By default, MaxScale\
will do that at most once per 30 seconds and with this configuration option\
that can be changed. A value of 0 allows infinite refreshes and a negative\
value disables the refreshing entirelly. Note that using `maxadmin` it is\
possible to explicitly cause the users of a service to be reloaded.

```
users_refresh_time=120
```

In MaxScale 2.3.9 and older versions, the minimum allowed value was 10 seconds\
but, due to a bug, the default value was 0 which allowed infinite refreshes.

#### `retain_last_statements`

How many statements MaxScale should store for each session. This is for\
debugging purposes, as in case of problems it is often of value to be able\
to find out exactly what statements were sent before a particular\
problem turned up.

**Note:** See also `dump_last_statements` using which the actual dumping\
of the statements is enabled. Unless both of the parameters are defined,\
the statement dumping mechanism doesn't work.

```
retain_last_statements=20
```

Default is `0`.

#### `dump_last_statements`

With this configuration item it is specified in what circumstances MaxScale\
should dump the last statements that a client sent. The allowed values are`never`, `on_error` and `on_close`. With `never` the statements are never\
logged, with `on_error` they are logged if the client closes the connection\
improperly, and with `on_close` they are always logged when a client session\
is closed.

```
dump_last_statements=on_error
```

Default is `never`.

Note that you need to specify with `retain_last_statements` how many statements\
MaxScale should retain for each session. Unless it has been set to another value\
than `0`, this configuration setting will not have an effect.

#### `session_trace`

How many log entries are stored in the session specific trace log. This log is\
written to disk when a session ends abnormally and can be used for debugging\
purposes. It would be good to enable this if a session is disconnected and the\
log is not detailed enough. In this case the info log might reveal the true\
cause of why the connection was closed.

```
session_trace=20
```

Default is `0`.

The session trace log is also exposed by REST API and is shown with`maxctrl show sessions`.

#### `writeq_high_water`

High water mark for network write buffer. Controls when network traffic\
throtting is started. The parameter accepts [size type values](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#sizes).

More specifically, if the client side write queue is above this value, it will\
block traffic coming from backend servers. If the backend side write queue is\
above this value, it will block traffic from client. the minimum allowed size is\
4096 bytes.

Only when both `writeq_high_water` and `writeq_low_water` are set, traffic\
throtting is enabled. By default, traffic throttling is disabled.

#### `writeq_low_water`

Low water mark for network write buffer. Once the traffic throttling is enabled,\
it will only be disabled when the write queue is below `writeq_low_water`. The\
parameter accepts [size type values](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#sizes). The minimum allowed size is 512\
bytes. `writeq_high_water` must always be greater than `writeq_low_water`.

#### `load_persisted_configs`

Load persisted runtime changes on startup. This parameter accepts boolean values\
and is enabled by default. This parameter was added in MaxScale 2.3.6.

All runtime configuration changes are persisted in generated configuration files\
located by default in `/var/lib/maxscale/maxscale.cnf.d/` and are loaded on\
startup after main configuration files have been read. To make runtime\
configurations volatile (i.e. they are lost when maxscale is restarted), use`load_persisted_configs=false`. All changes are still persisted since it stores\
the current runtime state of MaxScale. This makes problem analysis easier if an\
unexpected outage happens.

#### REST API Configuration

The MaxScale REST API is an HTTP interface that provides JSON format data\
intended to be consumed by monitoring appllications and visualization tools.

The following options must be defined under the `[maxscale]` section in the\
configuration file.

#### `admin_host`

The network interface where the REST API listens on. The default value is the\
IPv4 address `127.0.0.1` which only listens for local connections.

#### `admin_port`

The port where the REST API listens on. The default value is port 8989.

#### `admin_auth`

Enable REST API authentication using HTTP Basic Access\
authentication. This is not a secure method of authentication without HTTPS but\
it does add a small layer of security. This option is enabled by default.

The admin interface authentication uses the same user as MaxAdmin network\
interface. This means that new users can be added with both MaxAdmin and the\
REST API. The default credentials for the interface are `admin:mariadb`.

#### `admin_ssl_key`

The path to the TLS private key in PEM format for the admin interface.

If the `admin_ssl_key` and `admin_ssl_cert` options are all defined, the admin\
interface will use encrypted HTTPS instead of plain HTTP.

#### `admin_ssl_cert`

The path to the TLS public certificate in PEM format. See `admin_ssl_key`\
documentation for more details.

#### `admin_ssl_ca_cert`

The path to the TLS CA certificate in PEM format. If defined, the client\
certificate, if provided, will be validated against it. This parameter is\
optional starting with MaxScale 2.3.19.

#### `admin_enabled`

Enable or disable the admin interface. This allows the admin interface to\
be completely disabled to prevent access to it.

#### `admin_log_auth_failures`

Log authentication failures for the admin interface. This parameter expects a\
boolean value and is enabled by default.

### Events

MaxScale logs warnings and errors for various reasons and often it is self-\
evident and generally applicable whether some occurence should warrant a\
warning or an error, or perhaps just an info-level message.

However, there are events whose seriousness is not self-evident. For\
instance, in some environments an authentication failure may simply indicate\
that someone has made a typo, while in some other environment that can only\
happen in case there has been a security breech.

To handle events like these, MaxScale defines _events_ whose logging\
facility and level can be controlled by the administrator. Given an event`X`, its facility and level are controlled in the following manner:

```
event.X.facility=LOG_LOCAL0
event.X.level=LOG_ERR
```

The above means that if event _X_ occurs, then that is logged using the\
facility `LOG_LOCAL0` and the level `LOG_ERR`.

The valid values of facility`are the facility values reported by`man\
syslog`, e.g.`LOG\_AUTH`,`LOG\_LOCAL0`and`LOG\_USER`. Likewise, the valid values for`level`are the ones also reported by`man syslog`, e.g.`LOG\_WARNING`,`LOG\_ERR`and`LOG\_CRIT\`.

Note that MaxScale does not act upon the level, that is, even if the level\
of a particular event is defined to be `LOG_EMERG`, MaxScale will not shut\
down if that event occurs.

The default facility is `LOG_USER` and the default level is `LOG_WARNING`.

The available events are:

#### 'authentication\_failure'

This event occurs when there is an authentication failure.

```
event.authentication_failure.facility=LOG_AUTH
event.authentication_failure.level=LOG_CRIT
```

### Service

A service represents the database service that MariaDB MaxScale offers to the\
clients. In general a service consists of a set of backend database servers and\
a routing algorithm that determines how MariaDB MaxScale decides to send\
statements or route connections to those backend servers.

A service may be considered as a virtual database server that MariaDB MaxScale\
makes available to its clients.

Several different services may be defined using the same set of backend servers.\
For example a connection based routing service might be used by clients that\
already performed internal read/write splitting, whilst a different statement\
based router may be used by clients that are not written with this functionality\
in place. Both sets of applications could access the same data in the same\
databases.

A service is identified by a service name, which is the name of the\
configuration file section and a type parameter of service.

```
[Test-Service]
type=service
```

In order for MariaDB MaxScale to forward any requests it must have at least one\
service defined within the configuration file. The definition of a service alone\
is not enough to allow MariaDB MaxScale to forward requests however, the service\
is merely present to link together the other configuration elements.

#### `router`

The router parameter of a service defines the name of the router module that\
will be used to implement the routing algorithm between the client of MariaDB\
MaxScale and the backend databases. Additionally routers may also be passed a\
comma separated list of options that are used to control the behavior of the\
routing algorithm. The two parameters that control the routing choice are router\
and router\_options. The router options are specific to a particular router and\
are used to modify the behavior of the router. The read connection router can be\
passed options of master, slave or synced, an example of configuring a service\
to use this router and limiting the choice of servers to those in slave state\
would be as follows.

```
router=readconnroute
router_options=slave
```

To change the router to connect on to servers in the master state as well as\
slave servers, the router options can be modified to include the master state.

```
router=readconnroute
router_options=master,slave
```

A more complete description of router options and what is available for a given\
router is included with the documentation of the router itself.

#### `router_options`

Option string given to the router module. The value of this parameter should be\
a comma-separated list of key-value pairs. See router specific documentation for\
more details.

#### `filters`

The filters option allow a set of filters to be defined for a service; requests\
from the client are passed through these filters before being sent to the router\
for dispatch to the backend server. The filters parameter takes one or more\
filter names, as defined within the filter definition section of the\
configuration file. Multiple filters are separated using the | character.

```
filters=counter | QLA
```

The requests pass through the filters from left to right in the order defined in\
the configuration parameter.

#### `servers`

The servers parameter in a service definition provides a comma separated list of\
the backend servers that comprise the service. The server names are those used\
in the name section of a block with a type parameter of server (see below).

```
servers=server1,server2,server3
```

#### `user`

The user parameter, along with the password parameter are used to define the\
credentials used to connect to the backend servers to extract the list of\
database users from the backend database that is used for the client\
authentication.

```
user=maxscale
password=Mhu87p2D
```

Authentication of incoming connections is performed by MariaDB MaxScale itself\
rather than by the database server to which the client is connected. The client\
will authenticate itself with MariaDB MaxScale, using the username, hostname and\
password information that MariaDB MaxScale has extracted from the backend\
database servers. For a detailed discussion of how this impacts the\
authentication process please see the "Authentication" section below.

The host matching criteria is restricted to IPv4, IPv6 will be added in a future\
release.

Existing user configuration in the backend databases must be checked and may be\
updated before successful MariaDB MaxScale authentication:

In order for MariaDB MaxScale to obtain all the data it must be given a username\
it can use to connect to the database and retrieve that data. This is the\
parameter that gives MariaDB MaxScale the username to use for this purpose.

The account used must be able to select from the mysql.user table, the following\
is an example showing how to create this user.

```
CREATE USER 'maxscale'@'maxscalehost' IDENTIFIED BY 'maxscale-password';
```

Additionally, `SELECT` privileges on the `mysql.user`, `mysql.db` and `mysql.tables_priv`\
tables and `SHOW DATABASES` privileges are required in order to load databases\
name and grants suitable for database name authorization.

```
GRANT SELECT ON mysql.user TO 'maxscale'@'maxscalehost';
GRANT SELECT ON mysql.db TO 'maxscale'@'maxscalehost';
GRANT SELECT ON mysql.tables_priv TO 'maxscale'@'maxscalehost';
GRANT SELECT ON mysql.roles_mapping TO 'maxscale'@'maxscalehost';
GRANT SHOW DATABASES ON *.* TO 'maxscale'@'maxscalehost';

-- MariaDB from 10.2.2 to 10.2.10 requires extra grants
GRANT SELECT ON mysql.* TO 'maxscale'@'maxscalehost';
```

**Note:** MariaDB versions 10.2.10 and older require a `SELECT` grant on`mysql.*` in addition to the normal grants. This is to work around MDEV-13453\
which was fixed in MariaDB 10.2.11.

If you are using MariaDB ColumnStore, the follwing grant is requried.

```
GRANT ALL ON infinidb_vtable.* TO 'maxscale'@'maxscalehost';
```

See [MaxScale Troubleshooting](../../../../maxscale-management/maxscale-troubleshooting.md)\
for more information on how to troubleshoot authentication related problems.

#### `password`

The password parameter provides the password information for the above user and\
may be either a plain text password or it may be an encrypted password. See the\
section on encrypting passwords for use in the maxscale.cnf file. This user must\
be capable of connecting to the backend database and executing these SQL\
statements to load database names and grants from the backends:

* `SELECT user, host, password,Select_priv FROM mysql.user`.
* `SELECT user, host, db FROM mysql.db`
* `SELECT * FROM INFORMATION_SCHEMA.SCHEMATA`
* `SELECT GRANTEE,PRIVILEGE_TYPE FROM INFORMATION_SCHEMA.USER_PRIVILEGES`

**Note:** In older versions of MaxScale this parameter was called `passwd`. The\
use of `passwd` was deprecated in MaxScale 2.3.0.

#### `enable_root_user`

This parameter controls the ability of the root user to connect to MariaDB\
MaxScale and hence onwards to the backend servers via MariaDB MaxScale.

The default value is `0`, disabling the ability of the root user to connect to\
MariaDB MaxScale.

Example for enabling root user:

```
enable_root_user=1
```

Values of `on` or `true` may also be given to enable the root user and `off` or`false` may be given to disable the use of the root user.

```
enable_root_user=true
```

#### `localhost_match_wildcard_host`

This parameter enables matching of local addresses (i.e. `127.0.0.1`) against\
the wildcard host, `%`, for authentication. This parameter is enabled by\
default.

If this parameter is disabled, in order to authenticate a connection from the\
same machine as the one on which MariaDB MaxScale is running, an explicit\
user@localhost entry will be required in the MySQL user table.

#### `version_string`

This parameter sets a custom version string that is sent in the MySQL Handshake\
from MariaDB MaxScale to clients.

Example:

```
version_string=5.5.37-MariaDB-RWsplit
```

If not set, the default value is `5.5.5-10.0.0 MaxScale <MaxScale version>`\
where `<MaxScale version>` is the version of MaxScale. If the provided string\
does not start with the number 5, a 5.5.5- prefix will be added to it. This\
means that a _version\_string_ value of _MaxScale-Service_ would result in &#x61;_&#x35;.5.5-MaxScale-Service_ being sent to the client.

#### `weightby`

**Note:** This parameter has been deprecated in MaxScale 2.3.2.[A rank mechanism](https://github.com/mariadb-corporation/MaxScale/blob/develop/Documentation/Getting-Started/Configuration-Guide#rank)\
will be added in MaxScale 2.4 to allow better control over server usage.

The weightby parameter is used in conjunction with server parameters in order to\
control the load balancing applied in the router in use by the service. This\
allows varying weights to be applied to each server to create a non-uniform\
distribution of the load amongst the servers.

An example of this might be to define a parameter for each server that\
represents the amount of resource available on the server, we could call this\
serversize. Every server should then have a serversize parameter set for the\
server.

```
serversize=10
```

The service would then have the parameter `weightby=serv_weight`. If there are 4\
servers defined in the service (serverA, serverB, serverC and serverD) with the\
serversize set as shown in the table below, the connections would balanced using\
the percentages in this table.

| Server  | serversize | % connections |
| ------- | ---------- | ------------- |
| Server  | serversize | % connections |
| serverA | 10         | 18%           |
| serverB | 15         | 27%           |
| serverC | 10         | 18%           |
| serverD | 20         | 36%           |

_Note: If the value of the weighting parameter of an individual server is_\
\&#xNAN;_zero or the relative weight rounds down to zero, no queries will be routed to_\
\&#xNAN;_that server as long as a server with a positive weight is available._

Here is an excerpt from an example configuration with the `serv_weight`\
parameter used as the weighting parameter.

```
[server1]
type=server
address=127.0.0.1
port=3000
protocol=MariaDBBackend
serv_weight=3

[server2]
type=server
address=127.0.0.1
port=3001
protocol=MariaDBBackend
serv_weight=1

[Read-Service]
type=service
router=readconnroute
servers=server1,server2
weightby=serv_weight
```

With this configuration and a heavy query load, the server _server1_ will get\
most of the connections and about a third of the remaining queries are routed to\
the second server. With server weights, you can assign secondary servers that\
are only used when the primary server is under heavy load.

Without the weightby parameter, each connection counts as a single connection.\
With a weighting parameter, a single connection received its weight from the\
server's own weighting parameter divided by the sum of all weighting parameters\
in all the configured servers.

If we use the previous configuration as an example, the sum of the `serv_weight`\
parameter is 4. _Server1_ would receive a weight of `3/4=75%` and _server2_\
would get `1/4=25%`. This means that _server1_ would get 75% of the connections\
and _server2_ would get 25% of the connections.

#### `auth_all_servers`

This parameter controls whether only a single server or all of the servers are\
used when loading the users from the backend servers. This takes a boolean value\
and when enabled, creates a union of all the users and grants on all the\
servers.

#### `strip_db_esc`

The strip\_db\_esc parameter strips escape characters from database names of\
grants when loading the users from the backend server.

This parameter takes a boolean value and when enabled, will strip all backslash (`\`)\
characters from the database names. The default value for this parameter is true\
since MaxScale 2.0.1. In previous version, the default value was false.

Some visual database management tools automatically escape some characters and\
this might cause conflicts when MariaDB MaxScale tries to authenticate users.

#### `retry_on_failure`

The retry\_on\_failure parameter controls whether MariaDB MaxScale will try to\
restart failed services and accepts a boolean value. This functionality is\
enabled by default to prevent services being permanently disabled if the\
starting of the service failed due to a network outage. Disabling the restarting\
of the failed services will cause them to be permanently disabled if the\
services can't be started when MariaDB MaxScale is started.

#### `log_auth_warnings`

Enable or disable the logging of authentication failures and warnings. This\
parameter takes a boolean value.

MariaDB MaxScale normally suppresses warning messages about failed\
authentication. Enabling this option will log those messages into the message\
log with details about who tried to connect to MariaDB MaxScale and from where.

#### `connection_timeout`

The connection\_timeout parameter is used to disconnect sessions to MariaDB\
MaxScale that have been idle for too long. The session timeouts are disabled by\
default. To enable them, define the timeout in seconds in the service's\
configuration section. A value of zero is interpreted as no timeout, the same\
as if the parameter is not defined.

**Warning:** If a connection is idle for longer than the configured connection\
timeout, it will be forcefully disconnected and a warning will be logged in the\
MaxScale log file. If you are performing long-running maintenance operations\
(e.g. `ALTER TABLE`) either do them with a direct connection to the server or\
set `connection_timeout` to zero before executing them.

Example:

```
[Test-Service]
connection_timeout=300
```

#### `max_connections`

The maximum number of simultaneous connections MaxScale should permit to this\
service. If the parameter is zero or is omitted, there is no limit. Any attempt\
to make more connections after the limit is reached will result in a "Too many\
connections" error being returned.

Example:

```
[Test-Service]
max_connections=100
```

#### `max_retry_interval`

Configure the maximum interval between consecutive attempts to bind to an\
interface. The default value for this parameter is 3600 seconds. This\
parameter was introduced in MaxScale 2.2.0.

When a listener fails to bind to the interface it is assigned to, it will\
attempt to bind to the interface again after 10 seconds. If the attempt fails,\
the interval is incremented by 10 seconds and the next attempt will be in 20\
seconds. The interval is incremented until the value of `max_retry_interval` is\
reached at which point the listener attempts to bind to the interface every`max_retry_interval` seconds.

#### `session_track_trx_state`

Enable or disable session transaction state tracking by offloading it to the backend servers.\
Getting current session transaction state from server side will be more accurate for that state\
inside stored procedures or prepare statments will be handle properly, and that is also faster\
as no parsing is needed on MaxScale.

This is only supported by MariaDB versions 10.3 or newer. Default is false.\
The following Server side config is needed too.

```
session_track_state_change = ON
session_track_transaction_info = CHARACTERISTICS
```

#### `retain_last_statements`

How many statements MaxScale should store for each session of this service.\
This overrides the value of the global setting with the same name. If`retain_last_statements` has been specified in the global section of the\
MaxScale configuration file, then if it has _not_ been explicitly specified\
for the service, the global value holds, otherwise the service specific\
value rules. That is, it is possible to enable the setting globally and\
turn it off for a specific service, or just enable it for specific services.

The value of this parameter can be changed at runtime using `maxctrl` and the\
new value will take effect for sessions created thereafter.

```
maxctrl alter service MyService retain_last_statements 5
```

### Server

Server sections are used to define the backend database servers that can be\
formed into a service. A server may be a member of one or more services within\
MariaDB MaxScale. Servers are identified by a server name which is the section\
name in the configuration file. Servers have a type parameter of server, plus\
address port and protocol parameters.

```
[server1]
type=server
address=127.0.0.1
port=3000
protocol=MariaDBBackend
```

#### `address`

The IP address or hostname of the machine running the database server that is\
being defined. MariaDB MaxScale will use this address to connect to the backend\
database server.

#### `port`

The port on which the database listens for incoming connections. MariaDB\
MaxScale will use this port to connect to the database server. The default value\
is 3306.

#### `protocol`

The name for the protocol module to use to connect MariaDB MaxScale to the\
database. Currently only one backend protocol is supported, the MariaDBBackend\
module.

#### `monitoruser`

The monitor has a username and password that is used to connect to all servers\
for monitoring purposes, this may be overridden by supplying a monitoruser\
statement for each individual server.

```
monitoruser=mymonitoruser
```

#### `monitorpw`

The monitor has a username and password that is used to connect to all servers\
for monitoring purposes, this may be overridden by supplying a `monitorpw`\
for the individual servers.

```
monitorpw=mymonitorpasswd
```

The `monitorpw` parameter may be either a plain text password or it may be an\
encrypted password. See the section on encrypting passwords for use in the\
maxscale.cnf file.

#### `extra_port`

An alternative port used to monitor the server. This allows MaxScale to connect\
even when `max_connections` has been reached on the backend server. If this\
parameter is defined and a connection to the normal port fails, the alternative\
port is used.

For more information, read the[extra\_port documentation](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/buffers-caches-and-threads/thread-pool/thread-pool-system-status-variables).

#### `persistpoolmax`

The `persistpoolmax` parameter defaults to zero but can be set to an integer\
value for a back end server. If it is non zero, then when a DCB connected to a\
back end server is discarded by the system, it will be held in a pool for reuse,\
remaining connected to the back end server. If the number of DCBs in the pool\
has reached the value given by `persistpoolmax` then any further DCB that is\
discarded will not be retained, but disconnected and discarded.

#### `persistmaxtime`

The `persistmaxtime` parameter defaults to zero but can be set to an integer\
value indicating a number of seconds. A DCB placed in the persistent pool for a\
server will only be reused if the elapsed time since it joined the pool is less\
than the given value. Otherwise, the DCB will be discarded and the connection\
closed.

For more information about persistent connections, please read the[Administration Tutorial](../../mariadb-maxscale-mariadb-maxscale-22/maxscale-22-tutorials/mariadb-maxscale-22-mariadb-maxscale-administration-tutorial.md).

#### `proxy_protocol`

If `proxy_protocol` is set to `on`, MaxScale will send a[PROXY protocol](https://www.haproxy.org/download/1.8/doc/proxy-protocol.txt)\
header when connecting client sessions to the server. The header contains the\
original client IP address and port, as seen by MaxScale. The server will then\
read the header and perform authentication as if the connection originated from\
this address instead of MaxScale's IP address. With this feature, the user\
accounts on the backend server can be simplified to only contain the actual\
client hosts and not the MaxScale host.

PROXY protocol will be supported by MariaDB 10.3, which this feature has been\
tested with. To use it, enable the PROXY protocol in MaxScale for every\
compatible server and configure the MariaDB servers themselves to accept the\
protocol headers from MaxScale's IP address. On the server side, the protocol\
should be enabled only for trusted IPs, as it allows the sender to spoof the\
connection origin. If a proxy header is sent to a server not expecting it, the\
connection will fail. Usually PROXY protocol should be enabled for every\
server in a cluster, as they typically have similar grants.

Other SQL-servers may support PROXY protocol as well, but the implementation may\
be highly restricting. Strict adherence to the protocol requires that the\
backend server does not allow mixing of un-proxied and proxied connections from\
a given IP. MaxScale requires normal connections to backends for monitoring and\
authentication data queries, which would be blocked. To bypass this restriction,\
the server monitor needs to be disabled and the service listener needs to be\
configured to disregard authentication errors (`skip_authentication=true`).\
Server states also need to be set manually in MaxAdmin. These steps are _not_\
required for MariaDB 10.3, since its implementation is more flexible and allows\
both PROXY-headered and headerless connections from a proxy-enabled IP.

#### `authenticator`

The authenticator module to use. Each protocol module defines a default\
authentication module which is used if no `authenticator` parameter is found\
from the configuration.

#### `authenticator_options`

Removed feature. Only client authenticator modules have options, in the listener\
definition. Server authenticator options in the config file are ignored.

#### `disk_space_threshold`

This parameter specifies how full a disk may be, before MaxScale should start\
logging warnings or take other actions (e.g. perform a switchover). This\
functionality will only work with MariaDB server versions 10.1.32, 10.2.14 and\
10.3.6 onwards, if the `DISKS` _information schema plugin_ has been installed.

**NOTE**: In future MariaDB versions, the information will be available _only_ if\
the monitor user has the `FILE` privilege.

A limit is specified as a path followed by a colon and a percentage specifying\
how full the corresponding disk may be, before action is taken. E.g. an entry like

```
/data:80
```

specifies that the disk that has been mounted on `/data` may be used until 80%\
of the total space has been consumed. Multiple entries can be specified by\
separating them by a comma. If the path is specified using `*`, then the limit\
applies to all disks. However, the value of `*` is only applied if there is not\
an exact match.

Note that if a particular disk has been mounted on several paths, only one path\
need to be specified. If several are specified, then the one with the smallest\
percentage will be applied.

Examples:

```
disk_space_threshold=*:80
disk_space_threshold=/data:80
disk_space_threshold=/data1:80,/data2:60,*:90
```

The last line means that the disk mounted at `/data1` may be used up to\
80%, the disk mounted at `/data2` may be used up to 60% and all other disks\
mounted at any paths may be used up until 90% of maximum capacity, before\
MaxScale starts to warn to take action.

Note that the path to be used, is one of the paths returned by:

```
> use information_schema;
> select * from disks;
+-----------+----------------------+-----------+----------+-----------+
| Disk      | Path                 | Total     | Used     | Available |
+-----------+----------------------+-----------+----------+-----------+
| /dev/sda3 | /                    |  47929956 | 34332348 |  11139820 |
| /dev/sdb1 | /data                | 961301832 |    83764 | 912363644 |
...
```

There is no default value, but this parameter must be explicitly specified\
if the disk space situation should be monitored.

### Listener

The listener defines a port and protocol pair that is used to listen for\
connections to a service. A service may have multiple listeners associated with\
it, either to support multiple protocols or multiple ports. As with other\
elements of the configuration the section name is the listener name and it can\
be selected freely. A type parameter is used to identify the section as a\
listener definition. Address is optional and it allows the user to limit\
connections to certain interface only. Socket is also optional and used for Unix\
socket connections.

The network socket where the listener listens will have a backlog of\
connections. The size of this backlog is controlled by the\
net.ipv4.tcp\_max\_syn\_backlog and net.core.somaxconn kernel parameters.

Increasing the size of the backlog by modifying the kernel parameters helps with\
sudden connection spikes and rejected connections. For more information see[listen(2)](https://man7.org/linux/man-pages/man2/listen.2.html).

```
[<Listener name>]
type=listener
service=<Service name>]
protocol=[MariaDBClient|HTTPD]
address=[IP|hostname]
port=<Listen port number>
```

#### `service`

The service to which the listener is associated. This is the name of a service\
that is defined elsewhere in the configuration file.

#### `protocol`

The name of the protocol module that is used for the communication between the\
client and MariaDB MaxScale itself.

#### `address`

The address option sets the address that will be used to bind the listening\
socket. The address may be specified as an IP address in 'dot notation' or as a\
hostname. If the address option is not included in the listener definition the\
listener will bind to all network interfaces.

#### `port`

The port to use to listen for incoming connections to MariaDB MaxScale from the\
clients. If the port is omitted from the configuration a default port for the\
protocol will be used.

#### `socket`

The `socket` option may be included in a listener definition, this configures\
the listener to use Unix domain sockets to listen for incoming connections. The\
parameter value given is the name of the socket to use.

**Note:** If you want to use both network ports and UNIX domain sockets\
with a service, define two separate listeners that connect to the same\
service.

#### `authenticator`

The authenticator module to use. Each protocol module defines a default\
authentication module which is used if no `authenticator` parameter is found\
from the configuration.

#### `authenticator_options`

Option string given to the authenticator module. The value of this parameter\
should be a comma-separated list of key-value pairs. See authenticator specific\
documentation for more details.

## Available Protocols

The protocols supported by MariaDB MaxScale are implemented as external modules\
that are loaded dynamically into the MariaDB MaxScale core. They allow MariaDB\
MaxScale to communicate in various protocols both on the client side and the\
backend side. Each of the protocols can be either a client protocol or a backend\
protocol. Client protocols are used for client-MariaDB MaxScale communication\
and backend protocols are for MariaDB MaxScale-database communication.

### `MariaDBClient`

This is the implementation of the MySQL protocol that is used by clients of\
MariaDB MaxScale to connect to MariaDB MaxScale.

### `MariaDBBackend`

The MariaDBBackend protocol module is the implementation of the protocol that\
MariaDB MaxScale uses to connect to the backend MariaDB, MySQL and Percona\
Server databases. This implementation is tailored for the MariaDB MaxScale to\
MySQL Database traffic and is not a general purpose implementation of the MySQL\
protocol.

### `telnetd`

_Note:_ This module is deprecated.

The telnetd protocol module is used for connections to MariaDB MaxScale itself\
for the purposes of creating interactive user sessions with the MariaDB MaxScale\
instance itself. Currently this is used in conjunction with a special router\
implementation, the debugcli.

### `maxscaled`

_Note:_ This module is deprecated.

The protocol used used by the maxadmin client application in order to connect to\
MariaDB MaxScale and access the command line interface.

### `HTTPD`

_Note:_ This module is deprecated: use the REST API instead.

This protocol module is currently still under development, it provides a means\
to create HTTP connections to MariaDB MaxScale for use by web browsers or\
RESTful API clients.

## TLS/SSL encryption

This section describes configuration parameters for both servers and listeners\
that control the TLS/SSL encryption method and the various certificate files\
involved in it.

To enable TLS/SSL for a listener, you must set the `ssl` parameter to`true` and provide at least the `ssl_cert` and `ssl_key` parameters.

To enable TLS/SSL for a server, you must set the `ssl` parameter to`true`. If the backend database server has certificate verification\
enabled, the `ssl_cert` and `ssl_key` parameters must also be defined.

Custom CA certificates can be defined with the `ssl_ca_cert` parameter.

After this, MaxScale connections between the server and/or the client will be\
encrypted. Note that the database must also be configured to use TLS/SSL\
connections if backend connection encryption is used.

**Note:** MaxScale does not allow mixed use of TLS/SSL and normal connections on\
the same port.

If TLS encryption is enabled for a listener, any unencrypted connections to it\
will be rejected. MaxScale does this to improve security by preventing\
accidental creation of unencrypted connections.

The separation of secure and insecure connections differs from the MariaDB\
server which allows both secure and insecure connections on the same port. As\
MaxScale is the gateway through which all connections go, in order to guarantee\
a more secure system MaxScale enforces a stricter security policy than what the\
server does.

#### `ssl`

This enables SSL connections when set to true. The parameter takes a boolean\
value and is disabled by default. The parameter also accepts the special values`required` and `disabled` which were the only supported values before MaxScale\
2.3.0.

If enabled, the certificate files mentioned above must also be\
supplied. MaxScale connections to will then be encrypted with TLS/SSL.

#### `ssl_key`

A string giving a file path that identifies an existing readable file. The file\
must be the SSL client private key MaxScale should use. This is a required\
parameter for listeners but an optional parameter for servers.

#### `ssl_cert`

A string giving a file path that identifies an existing readable file. The file\
must be the SSL client certificate MaxScale should use with the server. The\
certificate must match the key defined in `ssl_key`. This is a required\
parameter for listeners but an optional parameter for servers.

#### `ssl_ca_cert`

A string giving a file path that identifies an existing readable file. The file\
must be the Certificate Authority (CA) certificate for the CA that signed the\
certificate referred to in the previous parameter. It will be used to verify\
that the certificate is valid. This is a required parameter for both listeners\
and servers. The CA certificate can consist of a certificate chain.

#### `ssl_version`

**Note:** It is highly recommended to leave this parameter to the default value\
of _MAX_. This will guarantee that the strongest available encryption is used.**Do not change this unless you know what you are doing**.

This parameter controls the level of encryption used. Accepted values are:

* TLSv10
* TLSv11
* TLSv12
* TLSv13
* MAX

The default is to use the highest level of encryption available that both the\
client and server support. MaxScale supports TLSv1.0, TLSv1.1, TLSv1.2 and\
TLSv1.3 depending on the OpenSSL library version.

The `TLSv13` value was added in MaxScale 2.3.15 ([MXS-2762](https://jira.mariadb.org/browse/MXS-2762)).

#### `ssl_cert_verify_depth`

The maximum length of the certificate authority chain that will be accepted. The\
default value is 9, same as the OpenSSL default. The configured value must be\
larger than 0.

#### `ssl_verify_peer_certificate`

Peer certificate verification. This functionality is disabled by default. In\
versions prior to 2.3.17 the feature was enabled by default.

When this feature is enabled, the peer must send a certificate. The certificate\
sent by the peer is verified against the configured Certificate Authority to\
make sure the peer is who they claim to be. For listeners, this behaves as if`REQUIRE X509` was defined for all users. For servers, this behaves like the`--ssl-verify-server-cert` command line option for the `mysql` client.

**Example SSL enabled server configuration**

```
[server1]
type=server
address=10.131.24.62
port=3306
protocol=MariaDBBackend
ssl=required
ssl_cert=/usr/local/mariadb/maxscale/ssl/crt.max-client.pem
ssl_key=/usr/local/mariadb/maxscale/ssl/key.max-client.pem
ssl_ca_cert=/usr/local/mariadb/maxscale/ssl/crt.ca.maxscale.pem
```

This example configuration requires all connections to this server to be\
encrypted with SSL. The paths to the certificate files and the Certificate\
Authority file are also provided.

**Example SSL enabled listener configuration**

```
[RW-Split-Listener]
type=listener
service=RW-Split-Router
protocol=MariaDBClient
port=3306
ssl=required
ssl_cert=/usr/local/mariadb/maxscale/ssl/crt.maxscale.pem
ssl_key=/usr/local/mariadb/maxscale/ssl/key.csr.maxscale.pem
ssl_ca_cert=/usr/local/mariadb/maxscale/ssl/crt.ca.maxscale.pem
```

This example configuration requires all connections to be encrypted with\
SSL. The paths to the certificate files and the Certificate Authority file are\
also provided.

## Module Types

### Routing Modules

The main task of MariaDB MaxScale is to accept database connections from client\
applications and route the connections or the statements sent over those\
connections to the various services supported by MariaDB MaxScale.

Currently a number of routing modules are available, these are designed for a\
range of different needs.

Connection based load balancing:

* [ReadConnRoute](../maxscale-23-routers/mariadb-maxscale-23-readconnroute.md)

Read/Write aware statement based router:

* [ReadWriteSplit](../maxscale-23-routers/mariadb-maxscale-23-readwritesplit.md)

Simple sharding on database level:

* [SchemaRouter](../maxscale-23-routers/mariadb-maxscale-23-schemarouter-router.md)

Binary log server:

* [Binlogrouter](../maxscale-23-routers/mariadb-maxscale-23-binlogrouter.md)

### Diagnostic modules

_Note:_ These modules are deprecated: use the REST API and MaxCtrl instead.

These modules are used for diagnostic purposes and can tell about the status of\
MariaDB MaxScale and the cluster it is monitoring.

* [MaxAdmin Module](../maxscale-23-routers/mariadb-maxscale-23-cli.md)
* [Telnet Module](../maxscale-23-routers/mariadb-maxscale-23-debug-cli.md)

### Monitor Modules

Monitor modules are used by MariaDB MaxScale to internally monitor the state of\
the backend databases in order to set the server flags for each of those\
servers. The router modules then use these flags to determine if the particular\
server is a suitable destination for routing connections for particular query\
classifications. The monitors are run within separate threads of MariaDB\
MaxScale and do not affect MariaDB MaxScale's routing performance.

* [MariaDB Monitor](../maxscale-23-monitors/mariadb-maxscale-23-mariadb-monitor.md)
* [Galera Monitor](../maxscale-23-monitors/mariadb-maxscale-23-galera-monitor.md)
* [NDBCluster Monitor](../maxscale-23-monitors/mariadb-maxscale-23-ndb-cluster-monitor.md)
* [Multi-Master Monitor](../maxscale-23-monitors/mariadb-maxscale-23-multi-master-monitor.md)

The use of monitors in MaxScale is not absolutely mandatory: it is possible to\
run MariaDB MaxScale without a monitor module. In this case an external\
monitoring system must the status of each server via MaxCtrl or the REST\
API. **Only do this if you know what you are doing.**

### Filter Modules

![](<../../../../.gitbook/assets/image_10.png (5).png>)

Filters provide a means to manipulate or process requests as they pass through\
MariaDB MaxScale between the client side protocol and the query router. A full\
explanation of each filter's functionality can be found in its documentation.

The [Filter Tutorial](../maxscale-tutorials/8077.md) document shows how you\
can add a filter to a service and combine multiple filters in one service.

* [Query Log All (QLA) Filter](../maxscale-23-filters/mariadb-maxscale-23-query-log-all-filter.md)
* [Regular Expression Filter](../maxscale-23-filters/mariadb-maxscale-23-regex-filter.md)
* [Tee Filter](../maxscale-23-filters/mariadb-maxscale-23-tee-filter.md)
* [Top Filter](../maxscale-23-filters/mariadb-maxscale-23-top-filter.md)
* [Database Firewall Filter](../maxscale-23-filters/mariadb-maxscale-23-database-firewall-filter.md)
* [Query Redirection Filter](../maxscale-23-filters/mariadb-maxscale-23-named-server-filter.md)
* [RabbitMQ Filter](../maxscale-23-filters/mariadb-maxscale-23-rabbitmq-filter.md)

## Encrypting Passwords

Passwords stored in the maxscale.cnf file may optionally be encrypted for added security.\
This is done by creation of an encryption key on installation of MariaDB MaxScale.\
Encryption keys may be created manually by executing the maxkeys utility with the argument\
of the filename to store the key. The default location MariaDB MaxScale stores\
the keys is `/var/lib/maxscale`. The passwords are encrypted using 256-bit AES CBC encryption.

```
# Usage: maxkeys [PATH]
maxkeys /var/lib/maxscale/
```

Changing the encryption key for MariaDB MaxScale will invalidate any currently\
encrypted keys stored in the maxscale.cnf file.

### Creating Encrypted Passwords

Encrypted passwords are created by executing the maxpasswd command with the location\
of the .secrets file and the password you require to encrypt as an argument.

```
# Usage: maxpasswd PATH PASSWORD
maxpasswd /var/lib/maxscale/ MaxScalePw001
61DD955512C39A4A8BC4BB1E5F116705
```

The output of the maxpasswd command is a hexadecimal string, this should be inserted\
into the maxscale.cnf file in place of the ordinary, plain text, password.\
MariaDB MaxScale will determine this as an encrypted password and automatically decrypt\
it before sending it the database server.

```
[Split-Service]
type=service
router=readwritesplit
servers=server1,server2,server3,server4
user=maxscale
password=61DD955512C39A4A8BC4BB1E5F116705
```

## Runtime Configuration Changes

Read the following documents for different methods of altering the MaxScale\
configuration at runtime.

* MaxCtrl
* [create](../maxscale-23-reference/mariadb-maxscale-23-maxctrl.md#create)
* [destroy](../maxscale-23-reference/mariadb-maxscale-23-maxctrl.md#destroy)
* [add](../maxscale-23-reference/mariadb-maxscale-23-maxctrl.md#add)
* [remove](../maxscale-23-reference/mariadb-maxscale-23-maxctrl.md#remove)
* [alter](../maxscale-23-reference/mariadb-maxscale-23-maxctrl.md#alter)
* [REST API](../maxscale-23-rest-api/maxscale-2-3-rest-api.md) documentation
* MaxAdmin (deprecated)
* [Runtime Configuration Changes](../maxscale-23-reference/mariadb-maxscale-23-maxadmin-admin-interface.md#runtime-configuration-changes)

All changes to the configuration are persisted as individual configuration files\
in `/var/lib/maxscale/maxscale.cnf.d/`. These files are applied after the main\
configuration file and all auxiliary configurations have been loaded. This means\
that once runtime configurations have been made, they need to be incorporated\
into the main configuration files.

### Backing Up Configuration Changes

The combination of configuration files can be done either manually\
(e.g. `rsync`) or with the `maxscale --export-config=FILE` command line\
option. See `maxscale --help` for more information about how to use the`--export-config` flag.

For example, to export the current runtime configuration, run the following\
command.

```
maxscale --export-config=/tmp/maxscale.cnf.combined
```

This will create the `/tmp/maxscale.cnf.combined` file and write the current\
configuration into the it. This allows new MaxScale instances to be easily set\
up without requiring copying of all runtime configuration files. The user\
executing the command must be able to read all MaxScale configuration files as\
well as create and write the provided filename.

## Error Reporting

MariaDB MaxScale is designed to be executed as a service, therefore all error\
reports, including configuration errors, are written to the MariaDB MaxScale\
error log file. By default, MariaDB MaxScale will log to a file in`/var/log/maxscale` and the system log.

## Limitations

The current limitations of MaxScale are listed in the [Limitations](../about-maxscale-23/mariadb-maxscale-23-limitations-and-known-issues-within-mariadb-maxscale.md) document.

## Troubleshooting

For a list of common problems and their solutions, read the[MaxScale Troubleshooting](../../../../maxscale-management/maxscale-troubleshooting.md)\
article on the MariaDB documentation.

### Authentication

MariaDB uses username, passwords and the client host in order to authenticate a\
user, so a typical user would be defined as user X at host Y and would be given\
a password to connect. MariaDB MaxScale uses exactly the same rules as MariaDB\
when users connect to the MariaDB MaxScale instance, i.e. it will check the\
address from which the client is connecting and treat this in exactly the same\
way that MariaDB would. MariaDB MaxScale will pull the authentication data from\
one of the backend servers (a master server if one is available) and use this to\
match the incoming connections. MaxScale assumes that all the backend servers\
for a particular service will share the same set of user credentials.

It is important to understand, however, that when MariaDB MaxScale itself makes\
connections to the backend servers the backend server will see all connections\
as originating from the host that runs MariaDB MaxScale and not the original\
host from which the client connected to MariaDB MaxScale. Therefore the backend\
servers should be configured to allow connections from the MariaDB MaxScale host\
for every user that can connect from any host. Since there is only a single\
password within the database server for a given host, this limits the\
configuration such that a given user name must have the same password for every\
host from which they can connect. These limitations do not apply when[proxy\_protocol](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#proxy_protocol) is in use.

To clarify, if a user _X_ is defined as using password _pass1_ from host _A_ an&#x64;_&#x70;ass2_ from host _B_ then there must be an entry in the `user` table for use&#x72;_&#x58;_ from the MariaDB MaxScale host, say _pass1_.

This would result in rows in the user table as follows

| Username | Password | Client Host |
| -------- | -------- | ----------- |
| Username | Password | Client Host |
| X        | pass1    | A           |
| X        | pass2    | B           |
| X        | pass1    | MaxScale    |

In this case the user _X_ would be able to connect to MariaDB MaxScale from host\
a giving the password of _pass1_. In addition MariaDB MaxScale would be able to\
create connections for this user to the backend servers using the username _X_\
and password _pass1_, since the MariaDB MaxScale host is also defined to have\
password _pass1_. User _X_ would not however be able to connect from host _b_\
since they would need to provide the password _pass2_ in order to connect to\
MariaDB MaxScale, but then MariaDB MaxScale would not be able to connect to the\
backends as it would also use the password _pass2_ for these connections.

#### Wildcard Hosts

Hostname mapping in MariaDB MaxScale works in exactly the same way as for MariaDB,\
if the wildcard is used for the host then any host other than the localhost\
(127.0.0.1) will match. It is important to consider that the localhost check\
will be performed at the MariaDB MaxScale level and at the MariaDB server level.

If MariaDB MaxScale and the databases are on separate hosts there are two\
important changes in behavior to consider:

1. Clients running on the same machine as the backend database now may access\
   the database using the wildcard entry. The localhost check between the client\
   and MariaDB MaxScale will allow the use of the wildcard, since the client is not\
   running on the MariaDB MaxScale host. Also the wildcard entry can be used on the\
   database host as MariaDB MaxScale is making that connection and it is not\
   running on the same host as the database.
2. Clients running on the same host as MariaDB MaxScale can not access the\
   database via MariaDB MaxScale using the wildcard entry since the connection to\
   MariaDB MaxScale will be from the localhost. These clients are able to access\
   the database directly, as they will use the wildcard entry. This behavior can be\
   configured with the[localhost\_match\_wildcard\_host](mariadb-maxscale-23-mariadb-maxscale-configuration-usage-scenarios.md#localhost_match_wildcard_host) option.

If MariaDB MaxScale is running on the same host as one or more of the database\
nodes to which it is routing statements then the wildcard host entries can be\
used to connect to MariaDB MaxScale but not to connect onwards to the database\
running on the same node.

In all these cases the issue may be solved by adding an explicit entry for the\
localhost address that has the same password as the wildcard entry. This may be\
done using a statement as below for each of the databases that are required:

```
MariaDB [mysql]> GRANT SELECT, INSERT, UPDATE, DELETE, CREATE, DROP ON employee.* 'user1'@'localhost' IDENTIFIED BY 'xxx';
Query OK, 0 rows affected (0.00 sec)
```

### Systemd Watchdog

If MaxScale is running as a systemd service, the systemd Watchdog will be\
enabled by default. To configure it, change the `WatchdogSec` option in the\
Service section of the maxscale systemd configuration file located in`/lib/systemd/system/maxscale.service`:

```
WatchdogSec=30s
```

It is not recommended to use a watchdog timeout less than 30 seconds. When\
enabled MaxScale will check that all threads are running and notify systemd\
with a "keep-alive ping".

Systemd reference: [systemd.service.html](https://www.freedesktop.org/software/systemd/man/systemd.service.html)

<sub>_This page is licensed: CC BY-SA / Gnu FDL_</sub>

{% @marketo/form formId="4316" %}
