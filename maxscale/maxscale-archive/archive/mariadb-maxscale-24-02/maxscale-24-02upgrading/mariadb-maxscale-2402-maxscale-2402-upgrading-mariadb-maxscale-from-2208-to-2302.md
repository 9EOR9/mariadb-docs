# MaxScale 24.02 Upgrading MariaDB MaxScale from 22.08 to 23.02

This document describes possible issues when upgrading MariaDB MaxScale from\
version 22.08 to 23.02.

For more information about MaxScale 23.02, refer to the[ChangeLog](../mariadb-maxscale-2402-maxscale-2402-changelog.md).

Before starting the upgrade, any existing configuration files should be backed\
up.

## Removed Features

* The `csmon` and `auroramon` monitors have been removed.
* The obsolete `maxctrl drain` command has been removed.
* The `maxctrl cluster` commands have been removed.

<sub>_This page is licensed: CC BY-SA / Gnu FDL_</sub>

{% @marketo/form formId="4316" %}
