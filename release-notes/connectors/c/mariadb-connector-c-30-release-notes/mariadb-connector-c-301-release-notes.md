# MariaDB Connector/C 3.0.1 Release Notes

The most recent [_**Stable**_](../../../mariadb-release-criteria.md) _**(GA)**_ release of MariaDB Connector/C is:[**MariaDB Connector/C 3.4.5**](../mariadb-connector-c-3-4-release-notes/mariadb-connector-c-3-4-5-release-notes.md)

[Download](https://downloads.mariadb.org/connector-c/3.0.1)[Release Notes](mariadb-connector-c-301-release-notes.md)[Changelog](../changelogs/mariadb-connector-c-30-changelogs/mariadb-connector-c-301-changelog.md)[About MariaDB Connector/C](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-c/README.md)

**Release date:** 18 Jan 2017

This is a [_Beta_](../../../mariadb-release-criteria.md) release of MariaDB Connector/C,\
formerly known as the MariaDB Client Library for C. As with any other\
pre-production release, cautions should be taken when installing on production\
systems or systems with critical data.

**For a description of this library see the**[**MariaDB Connector/C**](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-c) **page.**

## Download

Binary packages for Windows (32 and 64-bit) and generic Linux packages as well\
as source code packages are available from the[MariaDB download page](https://downloads.mariadb.org/connector-c/3.0.1)

## New features

* [Indicator variables](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-c/api-prepared-statement-functions/connector-c-data-structures-and-definitions/mysql_bind) for prepared statements
* [MDEV-9114](https://jira.mariadb.org/browse/MDEV-9114) bulk operations (array binding) for prepared statements (insert, update, delete).
* support for extended client/server capabilities (requires [MariaDB 10.2](../../../mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/what-is-mariadb-102.md) or newer)
* The DBUG library was removed from Connector/C 3.0
* Connector/C 2.3.2 now supports client plugins from MariaDB Server and Connector/C 3.0, for example GSSAPI plugin for kerberos authentication. Older plugins from previous versions of Connector/C can't be used anymore and might crash.

### Plugins

* New [GSSAPI authentication plugin](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/plugins/authentication-plugins/authentication-plugin-gssapi).

### New API functions and enhancements

* [mariadb\_stmt\_execute\_direct()](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-c/api-prepared-statement-functions/mariadb_stmt_execute_direct) prepares and executes in one step (mainly used by MariaDB ODBC driver)
* [mariadb\_cancel()](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-c/api-functions/mariadb_cancel)aborts a connection immediately by making all subsequent read/write operations fail
* [mysql\_reset\_connection()](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-c/api-functions/mysql_reset_connection) resets the current connection and clears session state
* [mariadb\_get\_infov](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-c/api-functions/mariadb_get_infov) returns generic or connection specific information
* [mysql\_stmt\_warning\_count()](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-c/api-prepared-statement-functions/mysql_stmt_warning_count) returns warnings per statement
* Functions for obtaining session state changes:
  * [mysql\_session\_track\_get\_first()](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-c/api-functions/mysql_session_track_get_first)
  * [mysql\_session\_track\_get\_next()](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-c/api-functions/mysql_session_track_get_next)
* Added tls\_version support for schannel. tls\_version has to be specified via `mysql_options(mysql, MARIADB_OPT_TLS_VERSION, ...)`

### Notable bug fixes

* [CONC-224](https://jira.mariadb.org/browse/CONC-224): Allow to build Connector/C without TLS/SSL support
* [CONC-223](https://jira.mariadb.org/browse/CONC-223): Add client support for missing collations
* [CONC-218](https://jira.mariadb.org/browse/CONC-218): reset a previously used statement when calling mysql\_stmt\_attr\_set with option STMT\_ATTR\_PREBIND\_PARAMS
* [CONC-217](https://jira.mariadb.org/browse/CONC-217): mariadb\_stmt\_execute\_direct: Clear error message from mysql\_stmt\_execute if prepare failed
* [CONC-202](https://jira.mariadb.org/browse/CONC-202): remove definition of \_snprintf (failed with Visual Studio 15)
* [CONC-200](https://jira.mariadb.org/browse/CONC-200): support of my\_ulonglong
* [CONC-180](https://jira.mariadb.org/browse/CONC-180): return system error message in case of SEC\_E\_INTERNAL\_ERROR (Schannel)
* [CONC-177](https://jira.mariadb.org/browse/CONC-177): Fixed length calculation for zerofill conversion from float/double to string
* [CONC-170](https://jira.mariadb.org/browse/CONC-170): missing blank in mariadb\_config --libs output
* [CONC-169](https://jira.mariadb.org/browse/CONC-169): Memory corruption in mariadb\_dyncol\_unpack
* [CONC-168](https://jira.mariadb.org/browse/CONC-168): string conversion of timestamps is broken
* [CONC-161](https://jira.mariadb.org/browse/CONC-161): Increase username length to 128
* [CONC-160](https://jira.mariadb.org/browse/CONC-160): field metadata doesn't show NUM\_FLAG for NEWDECIMAL columns
* [CONC-155](https://jira.mariadb.org/browse/CONC-155): return trailing zero when fetching from binary columns into string
* [CONC-154](https://jira.mariadb.org/browse/CONC-154): set statement status to MYSQL\_STMT\_FETCH\_DONE if result set is empty or mysql\_stmt\_reset was called
* Solaris build fixes
* Build fixes for gcc 4.8
* Fixed possible overrun in authentication
* fixed crash in shared memory connection
* Fixed memory overrun in my\_strdup\_root
* binary fetch fixes for prepared statements:
  * append trailing \0 for strings
  * don't remove last byte for binary objects
* removed call of gnutls\_bye() since server is not able to detect dead socket
* Added new cipher mapping for GnuTLS
* removed global context for TLS/SSL sessions
* fixed wrong behavior when using SChannel: SEC\_I\_RENEGOTIATE is now handled as error
* Optimization for re-preparing statement: Don't send COM\_STMT\_RESET if we will send COM\_STMT\_CLOSE afterwards
* [MDEV-10894](https://jira.mariadb.org/browse/MDEV-10894): fixed conversion for big-endian platforms
* [MDEV-11008](https://jira.mariadb.org/browse/MDEV-11008): Connector/C integration does not respect INSTALL\_LIBDIR or INSTALL\_DOCDIR
* [MDEV-10357](https://jira.mariadb.org/browse/MDEV-10357): my\_context\_continue() does not store current fiber on Windows
* Added support for OpenSSL 1.1
* fixed build when using GnuTLS. Minimum required version of GnuTLS is 3.3.24
* fixed output for plugin directory in mariadb\_config
* added sigpipe handler for OpenSSL

Be notified of new MariaDB Server releases automatically by [subscribing](https://lists.mariadb.org/postorius/lists/announce.lists.mariadb.org/) to the MariaDB Foundation community announce 'at' lists.mariadb.org announcement list (this is a low traffic, announce-only list). MariaDB plc customers will be notified for all new releases, security issues and critical bug fixes for all MariaDB plc products thanks to the Notification Services.

MariaDB may already be included in your favorite OS distribution. More\
information can be found on the[Distributions which Include MariaDB](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/readme-1)\
page.
