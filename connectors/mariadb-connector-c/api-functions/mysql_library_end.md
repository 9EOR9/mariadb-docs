# mysql\_library\_end

## Syntax

```c
void mysql_library_end(void)
```

## Description

Call when finished using the library, such as after disconnecting from the server. In an embedded server application, the embedded server is shut down and cleaned up. For a client program, only cleans up by performing memory management tasks.

{% hint style="info" %}
`mysql_server_end()` is an alias.
{% endhint %}

## See also

* [mysql\_library\_init()](mysql_library_init.md)

{% @marketo/form formId="4316" %}
