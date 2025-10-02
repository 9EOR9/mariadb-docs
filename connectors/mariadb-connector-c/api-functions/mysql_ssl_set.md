# mysql\_ssl\_set

## Syntax

```c
my_bool mysql_ssl_set(MYSQL *mysql, const char *key, const char *cert,
  const char *ca, const char *capath, const char *cipher)
```

* `mysql` - a mysql handle, which was previously allocated by [mysql\_init()](mysql_init.md) or [mysql\_real\_connect()](mysql_real_connect.md).
* `key` - path to the key file.
* `cert` - path to the certificate file.
* `ca` - path to the certificate authority file.
* `capath` - path to the directory containing the trusted TLS CA certificates in PEM format.
* `cipher` list of permitted ciphers to use for TLS encryption.

## Description

Used for establishing a [secure TLS connection](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/encryption/data-in-transit-encryption). It must be called before attempting to use [mysql\_real\_connect()](mysql_real_connect.md). TLS support must be enabled in the client library in order for the function to have any effect.

NULL can be used for an unused parameter. Always returns zero.

{% hint style="info" %}
[mysql\_real\_connect()](mysql_real_connect.md) will return an error if attempting to connect and TLS is incorrectly set up.
{% endhint %}

## See also

* [mysql\_get\_ssl\_cipher()](mysql_get_ssl_cipher.md)

{% @marketo/form formId="4316" %}
