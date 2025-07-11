# Upgrading MaxScale from 1.3 to 1.4

This document describes upgrading MaxScale from version 1.3 to 1.4.

For more detailed information about MaxScale 1.4, please refer to:[_MaxScale 1.4.5 release notes_](../maxscale-14-release-notes/mariadb-maxscale-145-release-notes-2017-02-01.md) [MaxScale 1.4.4 release notes](../maxscale-14-release-notes/mariadb-maxscale-144-release-notes.md)[_MaxScale 1.4.3 release notes_](../maxscale-14-release-notes/mariadb-maxscale-143-release-notes.md) [MaxScale 1.4.2 release notes](../maxscale-14-release-notes/mariadb-maxscale-142-release-notes.md)[_MaxScale 1.4.1 release notes_](../maxscale-14-release-notes/mariadb-maxscale-141-release-notes.md) [MaxScale 1.4.0 release notes](../maxscale-14-release-notes/mariadb-maxscale-140-beta-release-notes.md)

### Installation

Before starting the upgrade, we **strongly** recommend you back up your current\
configuration file.

### Service user permissions

The service users now also need SELECT privileges on mysql.tables\_priv. This is\
required for the resolution of table level grants. To grant SELECT privileges\
for the service user, replace the user and hostname in the following example.

```
GRANT SELECT ON mysql.tables_priv TO 'username'@'maxscalehost';
```

### Password encryption

MaxScale 1.4 upgrades the used password encryption algorithms to more secure ones.\
This requires that the password files are recreated with the `maxkeys` tool.\
For more information about how to do this, please read the installation guide:[MariaDB MaxScale Installation Guide](../maxscale-14-getting-started/mariadb-maxscale-installation-guide.md)

### SSL

The SSL configuration parameters are now a part of the listeners. If a service\
used the old style SSL configuration parameters, the values should be moved to\
the listener which is associated with that service.

Here is an example of an old style configuration.

```
[RW Split Router]
type=service
router=readwritesplit
servers=server1,server2,server3,server4
user=jdoe
passwd=BD26E4139A15280CA882264AA1551C70
ssl=required
ssl_cert=/home/user/certs/server-cert.pem
ssl_key=/home/user/certs/server-key.pem
ssl_ca_cert=/home/user/certs/ca.pem
ssl_version=TLSv12

[RW Split Listener]
type=listener
service=RW Split Router
protocol=MySQLClient
port=3306
```

And here is the new, 1.4 compatible configuration style.

```
[RW Split Router]
type=service
router=readwritesplit
servers=server1,server2,server3,server4
user=jdoe
passwd=BD26E4139A15280CA882264AA1551C70

[RW Split Listener]
type=listener
service=RW Split Router
protocol=MySQLClient
port=3306
ssl=required
ssl_cert=/home/user/certs/server-cert.pem
ssl_key=/home/user/certs/server-key.pem
ssl_ca_cert=/home/user/certs/ca.pem
ssl_version=TLSv12
```

Please also note that the `enabled` SSL mode is no longer supported due to\
the inherent security issues with allowing SSL and non-SSL connections on\
the same port. In addition to this, SSLv3 is no longer supported due to\
vulnerabilities found in it.

<sub>_This page is licensed: CC BY-SA / Gnu FDL_</sub>

{% @marketo/form formId="4316" %}
