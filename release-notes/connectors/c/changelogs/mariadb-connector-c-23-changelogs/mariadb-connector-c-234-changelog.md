# Connector/C 2.3.4 Changelog

The most recent [_**Stable**_](../../../../community-server/about/release-criteria.md) _**(GA)**_ release of MariaDB Connector/C is:[**MariaDB Connector/C 3.4.5**](../../mariadb-connector-c-3-4-release-notes/mariadb-connector-c-3-4-5-release-notes.md)

[Download](https://downloads.mariadb.org/connector-c/2.3.4)[Release Notes](../../mariadb-connector-c-23-release-notes/mariadb-connector-c-234-release-notes.md)[Changelog](mariadb-connector-c-234-changelog.md)[About MariaDB Connector/C](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/about-mariadb-connector-c/README.md)

**Release date:** 4 Dec 2017

For the highlights of this release, see the [release notes](../../mariadb-connector-c-23-release-notes/mariadb-connector-c-234-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On [GitHub](https://github.com/MariaDB/mariadb-connector-c/) you can view more details of the revision and view diffs of the code\
modified in that revision.

* [Revision #4bbcced](https://github.com/mariadb-corporation/mariadb-connector-c/commit/4bbcced)\
  2017-10-02 09:08:03 +0200
  * [CONC-282](https://jira.mariadb.org/browse/CONC-282): Connector/C now provides additional information for package version mariadb\_config --cc\_version lists the package version Beside MARIADB\_PACKAGE\_VERSION numeric representation MARIADB\_PACKAGE\_VERSION\_ID can be used now within preprocessor directives
* [Revision #b3c8de2](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b3c8de2)\
  2017-10-02 09:07:14 +0200
  * Fix test case number
* [Revision #a028307](https://github.com/mariadb-corporation/mariadb-connector-c/commit/a028307)\
  2017-09-25 13:51:01 +0200
  * Fix for [CONC-282](https://jira.mariadb.org/browse/CONC-282): mysql\_stmt\_fetch\_column doesn't work with prior call to mysql\_stmt\_store\_result - If no bind variables were bound or the function mysql\_stmt\_store\_result was not called before, the internal bind variables (stmt->bind) was not filled (lengths and null values)
* [Revision #86c4488](https://github.com/mariadb-corporation/mariadb-connector-c/commit/86c4488)\
  2017-09-22 06:49:36 +0200
  * OpenSSL fixes: - When negotiating tls protocol during handshake, use server preferences instead of client preferences. This will allow to use TLSv12 (OpenSSL server) and/or TLSv1.1 (Yassl server) - Don't check server ca unless verification flag was set. This will allow Connector/C to establish a tls/ssl connection without certificates. Bumped version number to 2.3.4

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
