# MariaDB Connector/C 2.3.0 Release notes

The most recent [_**Stable**_](../../../mariadb-release-criteria.md) _**(GA)**_ release of MariaDB Connector/C is:[**MariaDB Connector/C 3.4.5**](../mariadb-connector-c-3-4-release-notes/mariadb-connector-c-3-4-5-release-notes.md)

[Download](https://downloads.mariadb.org/connector-c/2.3.0)[Release Notes](mariadb-connector-c-230-release-notes.md)[Changelog](../changelogs/mariadb-connector-c-23-changelogs/mariadb-connector-c-230-changelog.md)[About MariaDB Connector/C](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-c/README.md)

**Release date:** 1 Jul 2016

This is a [_**Stable**_](../../../mariadb-release-criteria.md) _**(GA)**_ release of the MariaDB\
Connector/C, formerly known as MariaDB Client Library for C.

**For a description of this library see the**[**MariaDB Connector/C**](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-c) **page.**

## New features

New option `MARIADB_OPT_VERIFY_LOCAL_INFILE_CALLBACK` which allows the\
verification of filename and directory for `LOAD DATA LOCAL INFILE` calls.

The option must be set via mysql\_optionsv call:

```c
mysql_optionsv(mysql, MARIADB_OPT_VERIFY_LOCAL_INFILE_CALLBACK, my_verify_function, data);
```

The registered callback function has the following format

```c
int my_verify_function(void *data, const char *filename)
```

It returns 0 on success, non zero for error.

For a complete example check `test_local_infile_callback` in `misc.c`

## Notable Bug fixes

* In case getaddrinfo() returns an error, we return the WSA Error code instead of gai error. (For more information please read [ms738520(v=vs.85).aspx](https://msdn.microsoft.com/en-us/library/windows/desktop/ms738520\(v=vs.85\).aspx))
* Fixed numeric precision in prepared statements when converting float and double values to strings
* When connecting via TLS socket is now set to non blocking. If SSL\_get\_error returns WANT\_READ/WANT\_WRITE SSL\_connect will be called again until connect timeout seconds passed.
* Fixed behaviour of getaddrinfo: If getaddrinfo returns EAI\_AGAIN getaddrinfo will be called again until connect timeout seconds passed. If no connect timeout was specified, a default value of 30 seconds will be used.
* Removed LONGLONG\_MIN/MAX definition from config-win.h as they are also defined in my\_global
* Fix for windows build: replace SIZEOF\_CHARP with sizeof(char \*)
* [CONC-190](https://jira.mariadb.org/browse/CONC-190): Don't use verify callback in global context, since it may cause bad/unexpected behaviour in threaded issues. Instead now verification of peer certificate will be processed by the OpenSSL library itself.
* Fixed possible memory overrun in my\_strdup\_root
* [CONC-177](https://jira.mariadb.org/browse/CONC-177): fixed zerofill issues (converting numeric to string)

## Changelog

For a list of changes made in this release, with links to detailed\
information on each push, see the[changelog](../changelogs/mariadb-connector-c-23-changelogs/mariadb-connector-c-230-changelog.md).

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
