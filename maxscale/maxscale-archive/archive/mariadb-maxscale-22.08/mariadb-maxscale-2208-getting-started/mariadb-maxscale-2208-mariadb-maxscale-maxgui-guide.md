# MariaDB MaxScale MaxGUI Guide

## MariaDB MaxScale MaxGUI Guide

## MariaDB MaxScale MaxGUI Guide

* [MariaDB MaxScale MaxGUI Guide](mariadb-maxscale-2208-mariadb-maxscale-maxgui-guide.md#mariadb-maxscale-maxgui-guide)
* [Introduction](mariadb-maxscale-2208-mariadb-maxscale-maxgui-guide.md#introduction)
* [Enabling MaxGUI](mariadb-maxscale-2208-mariadb-maxscale-maxgui-guide.md#enabling-maxgui)
  * [Securing the GUI](mariadb-maxscale-2208-mariadb-maxscale-maxgui-guide.md#securing-the-gui)
* [Authentication](mariadb-maxscale-2208-mariadb-maxscale-maxgui-guide.md#authentication)
* [Pages](mariadb-maxscale-2208-mariadb-maxscale-maxgui-guide.md#pages)
  * [Dashboard](mariadb-maxscale-2208-mariadb-maxscale-maxgui-guide.md#dashboard)
  * [Detail](mariadb-maxscale-2208-mariadb-maxscale-maxgui-guide.md#detail)
  * [Visualization](mariadb-maxscale-2208-mariadb-maxscale-maxgui-guide.md#visualization)
  * [Settings](mariadb-maxscale-2208-mariadb-maxscale-maxgui-guide.md#settings)
  * [Logs Archive](mariadb-maxscale-2208-mariadb-maxscale-maxgui-guide.md#logs-archive)
  * [Query Editor](mariadb-maxscale-2208-mariadb-maxscale-maxgui-guide.md#query-editor)

## Introduction

_MaxGUI_ is a browser-based interface for MaxScale REST-API and query execution.

## Enabling MaxGUI

To enable MaxGUI in a testing mode, add `admin_host=0.0.0.0` and`admin_secure_gui=false` under the `[maxscale]` section of the MaxScale\
configuration file. Once enabled, MaxGUI will be available on port 8989:`http://127.0.0.1:8989/`

### Securing the GUI

To make MaxGUI secure, set `admin_secure_gui=true` and configure both the`admin_ssl_key` and `admin_ssl_cert` parameters.

See [Configuration Guide](../../../../../en/maxscale-2208-getting-started-mariadb-maxscale-configuration-guide/) and [Configuration and Hardening](../mariadb-maxscale-2208-tutorials/mariadb-maxscale-2208-rest-api-tutorial.md#configuration-and-hardening)\
for instructions on how to harden your MaxScale installation for production use.

## Authentication

MaxGUI uses the same credentials as `maxctrl`. The default username is `admin`\
with `mariadb` as the password.

Internally, MaxGUI uses [JSON Web Tokens](https://jwt.io/introduction/) as the\
authentication method for persisting the user's session. If the _Remember me_\
checkbox is ticked, the session will persist for 24 hours. Otherwise, the\
session will expire as soon as MaxGUI is closed.

To log out, simply click the username section in the top right corner of the\
page header to access the logout menu.

## Pages

### Dashboard

This page provides an overview of MaxScale configuration which includes\
Monitors, Servers, Services, Sessions, Listeners, and Filters.

By default, the refresh interval is 10 seconds.

### Detail

This page shows information on each [MaxScale object](../../../../../en/maxscale-2208-getting-started-mariadb-maxscale-configuration-guide/#objects) and allow to edit its\
parameter, relationships and perform other manipulation operations.

Access this page by clicking on the MaxScale object name on the [dashboard page](mariadb-maxscale-2208-mariadb-maxscale-maxgui-guide.md#dashboard)

### Visualization

This page visualizes MaxScale configuration and clusters.

* Configuration: Visualizing MaxScale configuration.
* Cluster: Visualizing a replication cluster into a tree graph and provides\
  manual cluster manipulation operations such as`switchover, reset-replication, release-locks, failover, rejoin` . At the\
  moment, it supports only servers monitored by Monitor using [mariadbmon](../mariadb-maxscale-2208-monitors/mariadb-maxscale-2208-mariadb-monitor.md) module.

Access this page by clicking the graph icon on the sidebar navigation.

### Settings

This page shows and allows editing of MaxScale parameters.

Access this page by clicking the gear icon on the sidebar navigation.

### Logs Archive

Realtime MaxScale logs can be accessed by clicking the logs icon on the sidebar\
navigation.

### Query Editor

Query Editor is a SQL editor tool allowing to run queries on a server, service,\
or listener. The query results can be visualized into a line, bar, or scatter\
graph and exported as CSV or JSON.

CC BY-SA / Gnu FDL
