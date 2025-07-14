# MariaDB MaxScale 24.02.1 Release Notes -- 2024-04-10

Release 24.02.1 is a GA release.

This document describes the changes in release 24.02.1, when compared to the\
previous release in the same series.

If you are upgrading from an older major version of MaxScale, please read the[upgrading document](https://mariadb.com/kb/Upgrading/Upgrading-To-MaxScale-24.02) for\
this MaxScale version.

For any problems you encounter, please consider submitting a bug\
report on [our Jira](https://jira.mariadb.org/projects/MXS).

### External CVEs resolved.

* [CVE-2023-1667](https://www.cve.org/CVERecord?id=CVE-2023-1667) Fixed by [MXS-5011](https://jira.mariadb.org/browse/MXS-5011) Upgrade libssh to 0.10.6
* [CVE-2023-2283](https://www.cve.org/CVERecord?id=CVE-2023-2283) Fixed by [MXS-5011](https://jira.mariadb.org/browse/MXS-5011) Upgrade libssh to 0.10.6
* [CVE-2023-48795](https://www.cve.org/CVERecord?id=CVE-2023-48795) Fixed by [MXS-5011](https://jira.mariadb.org/browse/MXS-5011) Upgrade libssh to 0.10.6
* [CVE-2023-6004](https://www.cve.org/CVERecord?id=CVE-2023-6004) Fixed by [MXS-5011](https://jira.mariadb.org/browse/MXS-5011) Upgrade libssh to 0.10.6
* [CVE-2023-6918](https://www.cve.org/CVERecord?id=CVE-2023-6918) Fixed by [MXS-5011](https://jira.mariadb.org/browse/MXS-5011) Upgrade libssh to 0.10.6

### New Features

* [MXS-4917](https://jira.mariadb.org/browse/MXS-4917) Add disk\_space\_ok option to master\_conditions and slave\_conditions

### Bug fixes

* [MXS-5035](https://jira.mariadb.org/browse/MXS-5035) Setting a path argument to empty reads uninitialized memory
* [MXS-5034](https://jira.mariadb.org/browse/MXS-5034) REST-API TLS keys are not validated at runtime
* [MXS-5033](https://jira.mariadb.org/browse/MXS-5033) MaxScale should prevent incompatible TLS certificates from being configured
* [MXS-5031](https://jira.mariadb.org/browse/MXS-5031) enforce\_read\_only\_slaves can set master to read\_only

### Known Issues and Limitations

There are some limitations and known issues within this version of MaxScale.\
For more information, please refer to the [Limitations](../maxscale-24-02about/mariadb-maxscale-2402-maxscale-2402-limitations-and-known-issues-within-mariadb-maxscale.md) document.

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
