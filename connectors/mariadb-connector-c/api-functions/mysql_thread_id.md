# mysql\_thread\_id

## Syntax

```c
unsigned long mysql_thread_id(MYSQL * mysql);
```

* `mysql` - a mysql handle, which was previously allocated by [mysql\_init()](mysql_init.md) or [mysql\_real\_connect()](mysql_real_connect.md).

## Description

The mysql\_thread\_id() function returns the thread id for the current connection.

{% hint style="info" %}
The current connection can be killed with [mysql\_kill()](mysql_kill.md). If reconnect option is enabled the thread id might change if the client reconnects to the server.
{% endhint %}

{% hint style="info" %}
Note that connector will return only the first 32bits value. If your database might expect to create more than 4.3 billion connection without a restart, it's better to query 'select CONNECTION\_ID()'
{% endhint %}

## See also

* [mysql\_kill()](mysql_kill.md)
* [mysql\_options()](mysql_options.md)

{% @marketo/form formid="4316" %}
