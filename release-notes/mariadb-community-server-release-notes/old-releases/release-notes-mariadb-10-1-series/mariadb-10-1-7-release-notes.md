# MariaDB 10.1.7 Release Notes

The most recent release of [MariaDB 10.1](changes-improvements-in-mariadb-10-1.md) is:[**MariaDB 10.1.48**](mariadb-10148-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.1.48/)

[Download](https://downloads.mariadb.org/mariadb/10.1.7)[Release Notes](mariadb-10-1-7-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-101-series/mariadb-10-1-7-changelog.md)[Overview of 10.1](changes-improvements-in-mariadb-10-1.md)

**Release date:** 9 Sep 2015

[MariaDB 10.1](changes-improvements-in-mariadb-10-1.md) is the current development series of MariaDB. It is an evolution\
of [MariaDB 10.0](../release-notes-mariadb-10-0-series/changes-improvements-in-mariadb-10-0.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL 5.6 and 5.7.

[MariaDB 10.1.7](mariadb-10-1-7-release-notes.md) is a [_**Release Candidate**_](../../../mariadb-release-criteria.md) _**(RC)**_ release.

**For an overview of** [**MariaDB 10.1**](changes-improvements-in-mariadb-10-1.md) **see the**[**What is MariaDB 10.1?**](changes-improvements-in-mariadb-10-1.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

* [XtraDB](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb) updated to XtraDB-5.6.25-73.1
* MariaDB can now also encrypt [binary logs](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/server-monitoring-logs/binary-log) (including relay\
  logs). To enable binary logs [encryption](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/securing-mariadb-encryption/encryption-data-at-rest-encryption/data-at-rest-encryption-overview) make sure\
  that an encryption plugin is loaded and add `encrypt-binlog` to\
  your `my.cnf` file.
* The [sql\_log\_bin](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/replication-and-binary-log-system-variables)\
  variable no longer affects the replication of events in a [Galera](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/galera/README.md)\
  cluster.
* SQL standards-compliant behavior when dealing with [Primary Keys with Nullable Columns](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/optimization-and-indexes/primary-keys-with-nullable-columns).
* Default values of server variables were changed as follows:

| Variable name                                                                                                                                                                 | Old value | New value                                       |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------- | ----------------------------------------------- |
| Variable name                                                                                                                                                                 | Old value | New value                                       |
| [join\_buffer\_size](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#join_buffer_size)     | 128K      | 256K                                            |
| [max\_allowed\_packet](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#max_allowed_packet) | 1M        | 4M                                              |
| [query\_cache\_size](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#query_cache_size)     | 0         | 1M                                              |
| [query\_cache\_type](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#query_cache_type)     | ON        | OFF                                             |
| [secure\_auth](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#secure_auth)                | OFF       | ON                                              |
| [sql\_mode](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#sql_mode)                      |           | NO\_ENGINE\_SUBSTITUTION,NO\_AUTO\_CREATE\_USER |
| [sync\_master\_info](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/replication-and-binary-log-system-variables)                      | 0         | 10000                                           |
| [sync\_relay\_log](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/replication-and-binary-log-system-variables)                        | 0         | 10000                                           |
| [sync\_relay\_log\_info](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/replication-and-binary-log-system-variables)                  | 0         | 10000                                           |
| [table\_open\_cache](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#table_open_cache)     | 400       | 2000                                            |

* One can now explicitly request MariaDB to select a good value for certain\
  command-line options by using the `--autoset` prefix. For example,\
  in `my.cnf`:

```
[mysqld]
autoset-back-log
```

At the moment only the [back-log](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/server-system-variables#back_log) and [host-cache-size](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/server-system-variables#host_cache_size) options support this prefix.

* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * CVE-\`-\`\`\`

For a complete list of changes made in [MariaDB 10.1.7](mariadb-10-1-7-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-101-series/mariadb-10-1-7-changelog.md).

Be notified of new MariaDB Server releases automatically by [subscribing](https://lists.mariadb.org/postorius/lists/announce.lists.mariadb.org/) to the MariaDB Foundation community announce 'at' lists.mariadb.org announcement list (this is a low traffic, announce-only list). MariaDB plc customers will be notified for all new releases, security issues and critical bug fixes for all MariaDB plc products thanks to the Notification Services.

MariaDB may already be included in your favorite OS distribution. More\
information can be found on the[Distributions which Include MariaDB](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/distributions-including-mariadb)\
page.

{% @marketo/form formid="4316" formId="4316" %}
