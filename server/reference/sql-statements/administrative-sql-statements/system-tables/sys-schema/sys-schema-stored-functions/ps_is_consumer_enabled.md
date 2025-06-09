# ps\_is\_consumer\_enabled

## Syntax

```
sys.ps_is_consumer_enabled(consumer)
```

## Description

`ps_is_consumer_enabled` is a [stored function](../../../../../../server-usage/stored-routines/stored-functions/) available with the [Sys Schema](../).

It returns an ENUM('YES','NO') depending on whether Performance Schema instrumentation for the given consumer is enabled, and NULL if not given a valid consumer name.

## Examples

```
SELECT sys.ps_is_consumer_enabled('global_instrumentation');
+------------------------------------------------------+
| sys.ps_is_consumer_enabled('global_instrumentation') |
+------------------------------------------------------+
| YES                                                  |
+------------------------------------------------------+

SELECT sys.ps_is_consumer_enabled('events_stages_current');
+-----------------------------------------------------+
| sys.ps_is_consumer_enabled('events_stages_current') |
+-----------------------------------------------------+
| NO                                                  |
+-----------------------------------------------------+

SELECT sys.ps_is_consumer_enabled('nonexistent_consumer');
+----------------------------------------------------+
| sys.ps_is_consumer_enabled('nonexistent_consumer') |
+----------------------------------------------------+
| NULL                                               |
+----------------------------------------------------+
```

## See Also

* [Performance Schema setup\_consumers Table](../../performance-schema/performance-schema-tables/performance-schema-setup_consumers-table.md)

CC BY-SA / Gnu FDL

{% @marketo/form formId="4316" %}
