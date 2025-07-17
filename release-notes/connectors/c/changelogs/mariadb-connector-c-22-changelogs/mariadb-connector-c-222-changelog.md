# Connector/C 2.2.2 Changelog

The most recent [_**Stable**_](../../../../community-server/about/release-criteria.md) _**(GA)**_ release of MariaDB Connector/C is:[**MariaDB Connector/C 3.4.5**](../../mariadb-connector-c-3-4-release-notes/mariadb-connector-c-3-4-5-release-notes.md)

[Download](https://downloads.mariadb.org/connector-c/2.2.2)[Release Notes](../../mariadb-connector-c-22-release-notes/mariadb-connector-c-222-release-notes.md)[Changelog](mariadb-connector-c-222-changelog.md)[About MariaDB Connector/C](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-c/README.md)

**Release date:** 9 Dec 2015

For the highlights of this release, see the[release notes](../../mariadb-connector-c-22-release-notes/mariadb-connector-c-222-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-c/) you can view more details of the revision and view diffs of the code\
modified in that revision.

* [Revision #108e6ac](https://github.com/mariadb-corporation/mariadb-connector-c/commit/108e6ac)\
  2015-12-08 08:50:35 +0100
  * Fix for CMake >= 3.0: Allow access for non existent targets (CMake policies 26,42,45
* [Revision #d11a935](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d11a935)\
  2015-12-08 08:45:17 +0100
  * Fix for [MDEV-9212](https://jira.mariadb.org/browse/MDEV-9212): incorrect hostname check (openssl) Reimplement ssl\_verify\_server\_cert() using the logic from [Hostname\_validation](https://wiki.openssl.org/index.php/Hostname_validation) The bug was discovered by Alex Gaynor.
* [Revision #3d4b46b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3d4b46b)\
  2015-12-08 08:21:18 +0100
  * Fix for [CONC-152](https://jira.mariadb.org/browse/CONC-152): Visual Studio 2015 build fails when OpenSSL is enabled
* [Revision #f6d00bd](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f6d00bd)\
  2015-11-30 20:12:22 +0100
  * Fixed wrong #ifdef in vio\_fastsend so TCP\_NODELAY will be set on Windows platforms correctly

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
