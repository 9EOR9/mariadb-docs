# Setting the Language for Error Messages

MariaDB server error messages are by default in English. However, MariaDB server also supports error message [localization](server-locale.md) in many different languages. Each supported language has its own version of the [error message file](../../../../../server-management/server-monitoring-logs/error-log.md#error-messages-file) called `errmsg.sys` in a dedicated directory for that language.

#

# Supported Languages for Error Messages

Error message localization is supported for the following languages:

* Bulgarian
* Chinese (from [MariaDB 10.4.25](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server/release-notes-mariadb-104-series/mariadb-10425-release-notes), [10.5.16](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server/release-notes-mariadb-105-series/mariadb-10516-release-notes), [10.6.8](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server/release-notes-mariadb-106-series/mariadb-1068-release-notes), [10.7.4](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server/release-notes-mariadb-10-7-series/mariadb-1074-release-notes), [10.8.3](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server/release-notes-mariadb-10-8-series/mariadb-1083-release-notes))
* Czech
* Danish
* Dutch
* English
* Estonian
* French
* Georgian (from [MariaDB 10.11.3](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server/release-notes-mariadb-1011-series/mariadb-10-11-3-release-notes))
* German
* Greek
* Hindi
* Hungarian
* Italian
* Japanese
* Korean
* Norwegian
* Norwegian-ny (Nynorsk)
* Polish
* Portuguese
* Romanian
* Russian
* Serbian
* Slovak
* Spanish
* Swahili (from [MariaDB 11.1.2](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server/release-notes-mariadb-11-1-series/mariadb-11-1-2-release-notes))
* Swedish
* Ukrainian

#

# Setting the `lc_messages` and `lc_messages_dir` System Variables

The [lc_messages](../../../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/server-system-variables.md#lc_messages) and [lc_messages_dir](../../../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/server-system-variables.md#lc_messages_dir) system variables can be used to set the [server locale](server-locale.md) used for error messages.

The [lc_messages](../../../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/server-system-variables.md#lc_messages) system variable can be specified as a [locale](server-locale.md) name. The language of the associated [locale](server-locale.md) will be used for error messages. See [Server Locales](server-locale.md) for a list of supported locales and their associated languages.

The [lc_messages](../../../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/server-system-variables.md#lc_messages) system variable is set to `en_US` by default, which means that error messages are in English by default.

If the `[lc_messages](../../../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/server-system-variables.md#lc_messages)` system variable is set to a valid [locale](server-locale.md) name, but the server can't find an [error message file](../../../../../server-management/server-monitoring-logs/error-log.md#error-messages-file) for the language associated with the [locale](server-locale.md), then the default language will be used instead.

This system variable can be specified as command-line arguments to [mariadbd](../../../../../server-management/getting-installing-and-upgrading-mariadb/starting-and-stopping-mariadb/mariadbd-options.md) or it can be specified in a relevant server [option group](../../../../../server-management/getting-installing-and-upgrading-mariadb/configuring-mariadb-with-option-files.md#option-groups) in an [option file](../../../../../server-management/getting-installing-and-upgrading-mariadb/configuring-mariadb-with-option-files.md). For example:

```
[mariadb]
...
lc_messages=fr_CA
```

The [lc_messages](../../../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/server-system-variables.md#lc_messages) system variable can also be changed dynamically with [SET GLOBAL](../../../../../server-usage/replication-cluster-multi-master/standard-replication/setting-up-replication.md#global-session). For example:

```
SET GLOBAL lc_messages='fr_CA';
```

If a server has the [lc_messages](../../../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/server-system-variables.md#lc_messages) system variable set to the `fr_CA` locale like the above example, then error messages would be in French. For example:

```
SELECT blah;
ERROR 1054 (42S22): Champ 'blah' inconnu dans field list
```

The [lc_messages_dir](../../../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/server-system-variables.md#lc_messages_dir) system variable can be specified either as the path to the directory storing the server's [error message files](../../../../../server-management/server-monitoring-logs/error-log.md#error-messages-file) or as the path to the directory storing the specific language's [error message file](../../../../../server-management/server-monitoring-logs/error-log.md#error-messages-file).

The server initially tries to interpret the value of the `[lc_messages_dir](../../../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/server-system-variables.md#lc_messages_dir)` system variable as a path to the directory storing the server's [error message files](../../../../../server-management/server-monitoring-logs/error-log.md#error-messages-file). Therefore, it constructs the path to the language's [error message file](../../../../../server-management/server-monitoring-logs/error-log.md#error-messages-file) by concatenating the value of the [lc_messages_dir](../../../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/server-system-variables.md#lc_messages_dir) system variable with the language name of the [locale](server-locale.md) specified by the [lc_messages](../../../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/server-system-variables.md#lc_messages) system variable .

If the server does not find the [error message file](../../../../../server-management/server-monitoring-logs/error-log.md#error-messages-file) for the language, then it tries to interpret the value of the [lc_messages_dir](../../../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/server-system-variables.md#lc_messages_dir) system variable as a direct path to the directory storing the specific language's [error message file](../../../../../server-management/server-monitoring-logs/error-log.md#error-messages-file).

This system variable can be specified as command-line arguments to [mariadbd](../../../../../server-management/getting-installing-and-upgrading-mariadb/starting-and-stopping-mariadb/mariadbd-options.md) or it can be specified in a relevant server [option group](../../../../../server-management/getting-installing-and-upgrading-mariadb/configuring-mariadb-with-option-files.md#option-groups) in an [option file](../../../../../server-management/getting-installing-and-upgrading-mariadb/configuring-mariadb-with-option-files.md).

For example, to specify the path to the directory storing the server's [error message files](../../../../../server-management/server-monitoring-logs/error-log.md#error-messages-file):

```
[mariadb]
...
lc_messages_dir=/usr/share/mysql/
```

Or to specify the path to the directory storing the specific language's [error message file](../../../../../server-management/server-monitoring-logs/error-log.md#error-messages-file):

```
[mariadb]
...
lc_messages_dir=/usr/share/mysql/french/
```

The `[lc_messages_dir](../../../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/server-system-variables.md#lc_messages_dir)` system variable can not be changed dynamically.

#

# Setting the --language Option

The [--language](../../../../../server-management/getting-installing-and-upgrading-mariadb/starting-and-stopping-mariadb/mariadbd-options.md#-language) option can also be used to set the server's language for error messages, but it is deprecated. It is recommended to set the [lc_messages](../../../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/server-system-variables.md#lc_messages) system variable instead.

The [--language](../../../../../server-management/getting-installing-and-upgrading-mariadb/starting-and-stopping-mariadb/mariadbd-options.md#-language) option can be specified either as a language name or as the path to the directory storing the language's [error message file](../../../../../server-management/server-monitoring-logs/error-log.md#error-messages-file). See [Server Locales](server-locale.md) for a list of supported locales and their associated languages.

This option can be specified as command-line arguments to [mariadbd](../../../../../server-management/getting-installing-and-upgrading-mariadb/starting-and-stopping-mariadb/mariadbd-options.md) or it can be specified in a relevant server [option group](../../../../../server-management/getting-installing-and-upgrading-mariadb/configuring-mariadb-with-option-files.md#option-groups) in an [option file](../../../../../server-management/getting-installing-and-upgrading-mariadb/configuring-mariadb-with-option-files.md).

For example, to specify a language name:

```
[mariadb]
...
language=french
```

Or to specify the path to the directory storing the language's [error message file](../../../../../server-management/server-monitoring-logs/error-log.md#error-messages-file):

```
[mariadb]
...
language=/usr/share/mysql/french/
```

#

# Character Set

The character set that the error messages are returned in is determined by the [character_set_results](../../../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/server-system-variables.md#character_set_results) variable, which defaults to UTF8.