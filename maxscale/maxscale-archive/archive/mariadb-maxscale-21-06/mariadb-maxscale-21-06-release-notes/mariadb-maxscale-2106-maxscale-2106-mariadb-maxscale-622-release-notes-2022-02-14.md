# MariaDB MaxScale 6.2.2 Release Notes -- 2022-02-14

Release 6.2.2 is a GA release.

This document describes the changes in release 6.2.2, when compared to the\
previous release in the same series.

If you are upgrading from an older major version of MaxScale, please read the[upgrading document](https://mariadb.com/kb/Upgrading/Upgrading-To-MaxScale-6) for\
this MaxScale version.

For any problems you encounter, please consider submitting a bug\
report on [our Jira](https://jira.mariadb.org/projects/MXS).

### Bug fixes

* [MXS-3989](https://jira.mariadb.org/browse/MXS-3989) Rebalancing may cause MaxScale to crash
* [MXS-3978](https://jira.mariadb.org/browse/MXS-3978) Binlog router appends -BinlogRouter to master version string again and again ...
* [MXS-3973](https://jira.mariadb.org/browse/MXS-3973) Session capabilities are not frozen on session startup
* [MXS-3966](https://jira.mariadb.org/browse/MXS-3966) MariaDBMonitor does not log connection error on startup
* [MXS-3959](https://jira.mariadb.org/browse/MXS-3959) Transaction replay doesn't reset transaction on implicit commit
* [MXS-3958](https://jira.mariadb.org/browse/MXS-3958) MaxScale stalls and crashes occasionally
* [MXS-3955](https://jira.mariadb.org/browse/MXS-3955) Crash after unexpected result
* [MXS-3953](https://jira.mariadb.org/browse/MXS-3953) Transaction start written to binlog prematurely
* [MXS-3949](https://jira.mariadb.org/browse/MXS-3949) "transaction" is always parsed as a reserved word
* [MXS-3948](https://jira.mariadb.org/browse/MXS-3948) Toggle query result columns isn't working as expected
* [MXS-3932](https://jira.mariadb.org/browse/MXS-3932) Xpand monitor doesn't show full configuration in diagnostic output
* [MXS-3886](https://jira.mariadb.org/browse/MXS-3886) Hang in RoutingWorker::execute\_concurrently semaphore.hh:146
* [MXS-3865](https://jira.mariadb.org/browse/MXS-3865) Shutdown bug

### Known Issues and Limitations

There are some limitations and known issues within this version of MaxScale.\
For more information, please refer to the [Limitations](../mariadb-maxscale-21-06-about/mariadb-maxscale-2106-maxscale-2106-limitations-and-known-issues-within-mariadb-maxscale.md) document.

### Packaging

RPM and Debian packages are provided for the supported Linux distributions.

Packages can be downloaded [here](https://mariadb.com/downloads/#mariadb_platform-mariadb_maxscale).

### Source Code

The source code of MaxScale is tagged at GitHub with a tag, which is identical\
with the version of MaxScale. For instance, the tag of version X.Y.Z of MaxScale\
is `maxscale-X.Y.Z`. Further, the default branch is always the latest GA version\
of MaxScale.

The source code is available [here](https://github.com/mariadb-corporation/MaxScale).

<sub>_This page is licensed: CC BY-SA / Gnu FDL_</sub>

{% @marketo/form formId="4316" %}
