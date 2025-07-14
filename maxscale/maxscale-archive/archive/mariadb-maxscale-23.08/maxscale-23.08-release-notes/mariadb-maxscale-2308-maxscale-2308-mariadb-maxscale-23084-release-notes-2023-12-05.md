# MariaDB MaxScale 23.08.4 Release Notes

## MaxScale 23.08 MariaDB MaxScale 23.08.4 Release Notes -- 2023-12-05

## MariaDB MaxScale 23.08.4 Release Notes -- 2023-12-05

Release 23.08.4 is a GA release.

This document describes the changes in release 23.08.4, when compared to the\
previous release in the same series.

If you are upgrading from an older major version of MaxScale, please read the[upgrading document](https://mariadb.com/docs/maxscale/maxscale-versions/mariadb-maxscale-24-02/maxscale-24-02upgrading/mariadb-maxscale-2402-maxscale-2402-upgrading-mariadb-maxscale-from-2302-to-2308) for\
this MaxScale version.

For any problems you encounter, please consider submitting a bug\
report on [our Jira](https://jira.mariadb.org/projects/MXS).

### New Features

* [MXS-4862](https://jira.mariadb.org/browse/MXS-4862) SSL\_VERSION should have a way to disallow deprecated versions

### Bug fixes

* [MXS-4881](https://jira.mariadb.org/browse/MXS-4881) Startup option --basedir mishandled
* [MXS-4869](https://jira.mariadb.org/browse/MXS-4869) Parameter table isn't refreshed after update in the GUI
* [MXS-4866](https://jira.mariadb.org/browse/MXS-4866) GUI doesn't show and allow to edit connection\_metadata after a listener is created
* [MXS-4858](https://jira.mariadb.org/browse/MXS-4858) maxscale 23.08.3 crash with dump\_last\_statements=on\_close set
* [MXS-4856](https://jira.mariadb.org/browse/MXS-4856) GUI failed to create a monitor in a monitored server detail page
* [MXS-4855](https://jira.mariadb.org/browse/MXS-4855) While writing query GUI response very slow
* [MXS-4851](https://jira.mariadb.org/browse/MXS-4851) No space or separator between 2 routing targets in the services dashboard
* [MXS-4818](https://jira.mariadb.org/browse/MXS-4818) Columns with the same name break sorting, filtering, and grouping features in Query Editor
* [MXS-4798](https://jira.mariadb.org/browse/MXS-4798) Broken slave promoted to master when no other servers are available
* [MXS-4789](https://jira.mariadb.org/browse/MXS-4789) GUI workspace caching doesn't work accurately
* [MXS-4728](https://jira.mariadb.org/browse/MXS-4728) Laggy issues on result data table

### Known Issues and Limitations

There are some limitations and known issues within this version of MaxScale.\
For more information, please refer to the [Limitations](../mariadb-maxscale-23-08-about/mariadb-maxscale-2308-limitations-and-known-issues-within-mariadb-maxscale.md) document.

### Packaging

RPM and Debian packages are provided for the supported Linux distributions.

Packages can be downloaded [here](https://mariadb.com/downloads/#mariadb_platform-mariadb_maxscale).

### Source Code

The source code of MaxScale is tagged at GitHub with a tag, which is identical\
with the version of MaxScale. For instance, the tag of version X.Y.Z of MaxScale\
is `maxscale-X.Y.Z`. Further, the default branch is always the latest GA version\
of MaxScale.

The source code is available [here](https://github.com/mariadb-corporation/MaxScale).

CC BY-SA / Gnu FDL
