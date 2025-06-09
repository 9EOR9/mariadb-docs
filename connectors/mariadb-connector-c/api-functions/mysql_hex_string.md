# mysql\_hex\_string

## Syntax

```c
unsigned long mysql_hex_string(char * to,
                               const char * from,
                               unsigned long len);
```

* `to` - result buffer
* `from` - the string which will be encoded
* `len` - length of the string (from)

## Description

This function is used to create a hexadecimal string which can be used in SQL statements. e.g. `INSERT INTO my_blob VALUES(X'A0E1CD')`.

Returns the length of the encoded string without the trailing null character.

{% hint style="info" %}
The size of the buffer for the encoded string must be 2 \* length + 1.

The encoded string does not contain a leading X'.
{% endhint %}

## See also

* [mysql\_real\_escape\_string()](mysql_real_escape_string.md)


{% @marketo/form formid="4316" %}
