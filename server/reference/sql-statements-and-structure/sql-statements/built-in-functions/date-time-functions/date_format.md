
# DATE_FORMAT

## Syntax


```
DATE_FORMAT(date, format[, locale])
```


## Description


Formats the date value according to the format string.


The language used for the names is controlled by the value of the [lc_time_names](../../../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/server-system-variables.md#lc_time_names) system variable. See [server locale](../../../../data-types/string-data-types/character-sets/internationalization-and-localization/server-locale.md) for more on the supported locales.


The options that can be used by DATE_FORMAT(), as well as its inverse [STR_TO_DATE](str_to_date.md)() and the [FROM_UNIXTIME()](from_unixtime.md) function, are:



| Option | Description |
| --- | --- |
| Option | Description |
| %a | Short weekday name in current locale (Variable [lc_time_names](../../../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/server-system-variables.md#lc_time_names)). |
| %b | Short form month name in current locale. For locale en_US this is one of: Jan,Feb,Mar,Apr,May,Jun,Jul,Aug,Sep,Oct,Nov or Dec. |
| %c | Month with 1 or 2 digits. |
| %D | Day with English suffix 'th', 'nd', 'st' or 'rd''. (1st, 2nd, 3rd...). |
| %d | Day with 2 digits. |
| %e | Day with 1 or 2 digits. |
| %f | [Microseconds](microseconds-in-mariadb.md) 6 digits. |
| %H | Hour with 2 digits between 00-23. |
| %h | Hour with 2 digits between 01-12. |
| %I | Hour with 2 digits between 01-12. |
| %i | Minute with 2 digits. |
| %j | Day of the year (001-366) |
| %k | Hour with 1 digits between 0-23. |
| %l | Hour with 1 digits between 1-12. |
| %M | Full month name in current locale (Variable [lc_time_names](../../../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/server-system-variables.md#lc_time_names)). |
| %m | Month with 2 digits. |
| %p | AM/PM according to current locale (Variable [lc_time_names](../../../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/server-system-variables.md#lc_time_names)). |
| %r | Time in 12 hour format, followed by AM/PM. Short for '%I:%i:%S %p'. |
| %S | Seconds with 2 digits. |
| %s | Seconds with 2 digits. |
| %T | Time in 24 hour format. Short for '%H:%i:%S'. |
| %U | Week number (00-53), when first day of the week is Sunday. |
| %u | Week number (00-53), when first day of the week is Monday. |
| %V | Week number (01-53), when first day of the week is Sunday. Used with %X. |
| %v | Week number (01-53), when first day of the week is Monday. Used with %x. |
| %W | Full weekday name in current locale (Variable [lc_time_names](../../../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/server-system-variables.md#lc_time_names)). |
| %w | Day of the week. 0 = Sunday, 6 = Saturday. |
| %X | Year with 4 digits when first day of the week is Sunday. Used with %V. |
| %x | Year with 4 digits when first day of the week is Monday. Used with %v. |
| %Y | Year with 4 digits. |
| %y | Year with 2 digits. |
| %Z | Timezone abbreviation. From [MariaDB 11.3.0](../../../../../../release-notes/mariadb-community-server/release-notes-mariadb-11-3-rolling-releases/mariadb-11-3-0-release-notes.md). |
| %z | Numeric timezone +hhmm or -hhmm presenting the hour and minute offset from UTC. From [MariaDB 11.3.0](../../../../../../release-notes/mariadb-community-server/release-notes-mariadb-11-3-rolling-releases/mariadb-11-3-0-release-notes.md). |
| %# | For [str_to_date](str_to_date.md)(), skip all numbers. |
| %. | For [str_to_date](str_to_date.md)(), skip all punctation characters. |
| %@ | For [str_to_date](str_to_date.md)(), skip all alpha characters. |
| %% | A literal % character. |



To get a date in one of the standard formats, `<code>[GET_FORMAT()](get_format.md)</code>` can be used.


## Examples


```
SELECT DATE_FORMAT('2009-10-04 22:23:00', '%W %M %Y');
+------------------------------------------------+
| DATE_FORMAT('2009-10-04 22:23:00', '%W %M %Y') |
+------------------------------------------------+
| Sunday October 2009                            |
+------------------------------------------------+

SELECT DATE_FORMAT('2007-10-04 22:23:00', '%H:%i:%s');
+------------------------------------------------+
| DATE_FORMAT('2007-10-04 22:23:00', '%H:%i:%s') |
+------------------------------------------------+
| 22:23:00                                       |
+------------------------------------------------+

SELECT DATE_FORMAT('1900-10-04 22:23:00', '%D %y %a %d %m %b %j');
+------------------------------------------------------------+
| DATE_FORMAT('1900-10-04 22:23:00', '%D %y %a %d %m %b %j') |
+------------------------------------------------------------+
| 4th 00 Thu 04 10 Oct 277                                   |
+------------------------------------------------------------+

SELECT DATE_FORMAT('1997-10-04 22:23:00', '%H %k %I %r %T %S %w');
+------------------------------------------------------------+
| DATE_FORMAT('1997-10-04 22:23:00', '%H %k %I %r %T %S %w') |
+------------------------------------------------------------+
| 22 22 10 10:23:00 PM 22:23:00 00 6                         |
+------------------------------------------------------------+

SELECT DATE_FORMAT('1999-01-01', '%X %V');
+------------------------------------+
| DATE_FORMAT('1999-01-01', '%X %V') |
+------------------------------------+
| 1998 52                            |
+------------------------------------+

SELECT DATE_FORMAT('2006-06-00', '%d');
+---------------------------------+
| DATE_FORMAT('2006-06-00', '%d') |
+---------------------------------+
| 00                              |
+---------------------------------+
```

Optionally, the locale can be explicitly specified as the third DATE_FORMAT() argument. Doing so makes the function independent from the session settings, and the three argument version of DATE_FORMAT() can be used in virtual indexed and persistent [generated-columns](../../data-definition/create/generated-columns.md):


```
SELECT DATE_FORMAT('2006-01-01', '%W', 'el_GR');
+------------------------------------------+
| DATE_FORMAT('2006-01-01', '%W', 'el_GR') |
+------------------------------------------+
| Κυριακή                                  |
+------------------------------------------+
```

From [MariaDB 11.3](../../../../../../release-notes/mariadb-community-server/what-is-mariadb-113.md), the timezone information:


```
SELECT DATE_FORMAT(NOW(), '%W %d %M %Y %H:%i:%s %Z %z');
+--------------------------------------------------+
| DATE_FORMAT(NOW(), '%W %d %M %Y %H:%i:%s %Z %z') |
+--------------------------------------------------+
| Wednesday 20 September 2023 15:00:23 SAST +0200  |
+--------------------------------------------------+
```

## See Also


* [STR_TO_DATE()](str_to_date.md)
* [FROM_UNIXTIME()](from_unixtime.md)

