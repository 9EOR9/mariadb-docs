# MaxScale 2.5 GSSAPI Client Authenticator

GSSAPI is an authentication protocol that is commonly implemented with\
Kerberos on Unix or Active Directory on Windows. This document describes\
the GSSAPI authentication in MaxScale.

### Preparing the GSSAPI system

For Unix systems, the usual GSSAPI implementation is Kerberos. This is a short\
guide on how to set up Kerberos for MaxScale.

The first step is to configure MariaDB to use GSSAPI authentication. The MariaDB\
documentation for the[GSSAPI Authentication Plugin](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/plugins/authentication-plugins/authentication-plugin-gssapi)\
is a good example on how to set it up.

The next step is to copy the keytab file from the server where MariaDB is\
installed to the server where MaxScale is located. The keytab file must be\
placed in the configured default location which almost always is`/etc/krb5.keytab`.

The location of the keytab file can be changed with the KRB5\_KTNAME environment\
variable: [keytab\_def.html](https://web.mit.edu/kerberos/krb5-latest/doc/basic/keytab_def.html)

To take GSSAPI authentication into use, add the following to the listener.

```
authenticator=GSSAPIAuth
authenticator_options=principal_name=mariadb/localhost.localdomain@EXAMPLE.COM
```

Change the principal name to the same value you configured for the MariaDB\
server.

### Authenticator options

The client side GSSAPIAuth authenticator supports one option, the service\
principal name that MaxScale sends to the client. The backend authenticator\
module has no options.

#### `principal_name`

The service principal name to send to the client. This parameter is a string\
parameter which is used by the client to request the token. The default value\
for this option is _mariadb/localhost.localdomain_.

This parameter _must_ be the same as the principal name that the backend MariaDB\
server uses.

### Implementation details

Read the [Authentication Modules](mariadb-maxscale-25-authentication-modules.md) document for more\
details on how authentication modules work in MaxScale.

#### GSSAPI authentication

The GSSAPI plugin authentication starts when the database server sends the\
service principal name in the AuthSwitchRequest packet. The principal name will\
usually be in the form `service@REALM.COM`.

The client will then request a token for this service from the GSSAPI server and\
send the token to the database server. The database server will verify the\
authenticity of the token by contacting the GSSAPI server and if the token is\
authentic, the server sends the final OK packet.

### Limitations

Client side GSSAPI authentication is only supported when the backend connections\
also use GSSAPI authentication. MaxScale will automatically use the correct\
authentication mechanism based on what the client authenticates with.

See the [Limitations](../about-maxscale-25/mariadb-maxscale-25-limitations-and-known-issues-within-mariadb-maxscale.md) document for more details.

### Building the module

The GSSAPI authenticator modules require the GSSAPI development libraries\
(krb5-devel on CentOS 7).

<sub>_This page is licensed: CC BY-SA / Gnu FDL_</sub>

{% @marketo/form formId="4316" %}
