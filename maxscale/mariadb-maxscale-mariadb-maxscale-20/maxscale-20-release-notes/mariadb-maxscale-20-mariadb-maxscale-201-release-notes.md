
# MariaDB MaxScale 2.0.1 Release Notes

# MariaDB MaxScale 2.0.1 Release Notes


Release 2.0.1 is a GA release.


This document describes the changes in release 2.0.1, when compared to
[release 2.0.0](../../mariadb-maxscale-21-06/README.md).


If you are upgrading from 1.4.3, please also read the release notes
of [2.0.0](https://mariadb.com/kb/en/node:5959).


For any problems you encounter, please consider submitting a bug
report at [Jira](https://jira.mariadb.org).


## Changed default values


### `strip_db_esc`


The service parameter [strip_db_esc](../maxscale-20-getting-started/mariadb-maxscale-20-mariadb-maxscale-configuration-usage-scenarios.md#strip_db_esc)
now defaults to true.


### `detect_stale_master`


The [stale master detection](../maxscale-20-monitors/mariadb-maxscale-20-mysql-monitor.md#detect_stale_master)
feature is now enabled by default.


## Updated Features


### Starting MariaDB MaxScale


There is now a new command line parameter `--basedir=PATH` that will
cause all directory paths and the location of the configuration file
to be defined relative to that path.


For instance, invoking MariaDB MaxScale like


```
$ maxscale --basedir=/path/maxscale
```


has the same effect as invoking MariaDB MaxScale like


```
$ maxscale --config=/path/maxscale/etc/maxscale.cnf
           --configdir=/path/maxscale/etc
           --logdir=/path/maxscale/var/log/maxscale
           --cachhedir=/path/maxscale/var/cache/maxscale
           --libdir=/path/maxscale/lib/maxscale
           --datadir=/path/maxscale/var/lib/maxscale
           --execdir=/path/maxscale/bin
           --language=/path/maxscale/var/lib/maxscale
           --piddir=/path/maxscale/var/run/maxscale
```


### Password parameter


In the configuration entry for a *service* or *monitor*, the value of
the password to be used can now be specified using `password` in addition
to `passwd`. The use of the latter will be deprecated and removed in later
releases of MaxScale.


```
[SomeService]
...
password=mypasswd
```


### Routing hint priority change


Routing hints now have the highest priority when a routing decision is made. If
there is a conflict between the original routing decision made by the
readwritesplit and the routing hint attached to the query, the routing hint
takes higher priority.


What this change means is that, if a query would normally be routed to the
master but the routing hint instructs the router to route it to the slave, it
would be routed to the slave.


**WARNING**: This change can alter the way some statements are routed and could
 possibly cause data loss, corruption or inconsisteny. Please consult the [Hint
 Syntax](https://mariadb.com/kb/Reference/Hint-Syntax) and
 [ReadWriteSplit](../maxscale-20-routers/mariadb-maxscale-20-readwritesplit.md) documentation before using
 routing hints.


### MaxAdmin Usage


In 2.0.0 (Beta), the authentication mechanism of MaxAdmin was completely
changed, so that MaxAdmin could only connect to MaxScale using a Unix domain
socket, thus *only when run on the same host*, and authorization was based
on the Unix identity. Remote access was no longer supported.


To the user this was visible so that while you in 1.4.3 had to provide
a password when starting *maxadmin* and when adding a user



```
user@host $ maxadmin -p password
MaxAdmin> add user john johns-password
```



in 2.0.0 (Beta), where only Unix domain sockets could be used, you did not
have to provide a password neither when starting *maxadmin*, nor when adding
users



```
user@host $ maxadmin
MaxAdmin> add user john
```



as the MaxScale user corresponded to a Unix user, provided the Linux user
had been added as a user of MaxScale.


In 2.0.1 (GA) this has been changed so that the 1.4.3 behaviour is intact
but *deprecated*, and the 2.0.0 (Beta) behaviour is exposed using a new set
of commands:



```
MaxAdmin> enable account alice
MaxAdmin> disable account alice
```



Note that the way you need to invoke *maxadmin* depends upon how MariaDB
MaxScale has been configued.


Please consult
[MaxAdmin documentation](../maxscale-20-reference/mariadb-maxscale-20-maxadmin.md) for more details.


## Bug fixes


[Here is a list of bugs fixed since the release of MaxScale 2.0.0.](https://jira.mariadb.org/browse/MXS-860?jql=project%20%3D%20MXS%20AND%20issuetype%20%3D%20Bug%20AND%20status%20%3D%20Closed%20AND%20fixVersion%20in%20(2.0.1)%20AND%20resolved%20%3E%3D%20-21d%20AND%20(resolution%20%3D%20Done%20OR%20resolution%20%3D%20Fixed)%20ORDER%20BY%20priority%20DESC)


* [MXS-860](https://jira.mariadb.org/browse/MXS-860): I want to access the web site if master server is down
* [MXS-870](https://jira.mariadb.org/browse/MXS-870): Assertion of Buffer Overflow
* [MXS-845](https://jira.mariadb.org/browse/MXS-845): "Server down" event is re-triggered after maintenance mode is repeated
* [MXS-836](https://jira.mariadb.org/browse/MXS-836): "Failed to start all MaxScale services" without retrying
* [MXS-835](https://jira.mariadb.org/browse/MXS-835): Please reinstate remote access to maxscaled protocol
* [MXS-773](https://jira.mariadb.org/browse/MXS-773): 100% CPU on idle MaxScale with MaxInfo
* [MXS-812](https://jira.mariadb.org/browse/MXS-812): Number of conns not matching number of operations
* [MXS-856](https://jira.mariadb.org/browse/MXS-856): If config file cannot be accessed and creation of log file fails, MaxScale crashes with SIGSEGV
* [MXS-829](https://jira.mariadb.org/browse/MXS-829): When the config file isn't readable or doesn't exist, maxscale silently ends


## Known Issues and Limitations


There are some limitations and known issues within this version of MaxScale.
For more information, please refer to the [Limitations](../about-maxscale-20/mariadb-maxscale-20-limitations-and-known-issues-within-mariadb-maxscale.md) document.


## Packaging


RPM and Debian packages are provided for the Linux distributions supported
by MariaDB Enterprise.


Packages can be downloaded [here](https://mariadb.com/resources/downloads).


## Source Code


The source code of MaxScale is tagged at GitHub with a tag, which is derived
from the version of MaxScale. For instance, the tag of version `X.Y.Z` of MaxScale
is `maxscale-X.Y.Z`.


The source code is available [here](https://github.com/mariadb-corporation/MaxScale).
