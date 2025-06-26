# MariaDB Connector/Python 1.1.11 Changelog

The most recent [_**Stable**_](../../../../mariadb-release-criteria.md) _**(GA)**_ release of MariaDB Connector/Python is:[**MariaDB Connector/Python 1.1.12**](../../mariadb-connector-python-1-1-release-notes/mariadb-connector-python-1-1-12-release-notes.md)

[Download](https://mariadb.com/downloads/connectors/connectors-data-access/python-connector/)[Release Notes](../../mariadb-connector-python-1-1-release-notes/mariadb-connector-python-1-1-11-release-notes.md)[Changelog](mariadb-connector-python-1-1-11-changelog.md)[Connector/Python Overview](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/mariadb-connector-python/README.md)

**Release date:** 15 Nov 2024

For the highlights of this release, see the[release notes](../../mariadb-connector-python-1-1-release-notes/mariadb-connector-python-1-1-11-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-python/) you can view more\
details of the revision and view diffs of the code modified in that revision.

* [Revision #d2f4a33](https://github.com/mariadb-corporation/mariadb-connector-python/commit/d2f4a33)\
  2024-10-29 16:13:22 +0100
  * \[misc] travis test Python 3.8 removed, Python 3.13 added
* [Revision #0ce5a58](https://github.com/mariadb-corporation/mariadb-connector-python/commit/0ce5a58)\
  2024-10-14 14:28:17 +0200
  * Removed Python 3.8, added Python 3.13
* [Revision #f96cbe2](https://github.com/mariadb-corporation/mariadb-connector-python/commit/f96cbe2)\
  2024-10-01 15:55:33 +0200
  * Travis build fixes:
    * Skip MySQL batch tests
    * Fix travis on windows
* [Revision #c9c0278](https://github.com/mariadb-corporation/mariadb-connector-python/commit/c9c0278)\
  2024-09-28 08:17:49 +0200
  * Travis fixes:
    * skip extended field types for MaxScale
    * remove shadowed test
* [Revision #60562de](https://github.com/mariadb-corporation/mariadb-connector-python/commit/60562de)\
  2024-09-28 04:57:31 +0200
  * Buildfix for C/C > 3.4.1
* [Revision #aa962d0](https://github.com/mariadb-corporation/mariadb-connector-python/commit/aa962d0)\
  2024-09-27 17:55:50 +0200
  * Build fix for C/C versions < 3.4.2
* [Revision #5ae028e](https://github.com/mariadb-corporation/mariadb-connector-python/commit/5ae028e)\
  2024-09-27 17:14:25 +0200
  * [CONPY-289](https://jira.mariadb.org/browse/CONPY-289): BIGINT out of range on bulk insert
* [Revision #fee7f30](https://github.com/mariadb-corporation/mariadb-connector-python/commit/fee7f30)\
  2024-09-27 16:21:35 +0200
  * Added new connection property: tls\_peer\_cert\_info
* [Revision #3d34bb6](https://github.com/mariadb-corporation/mariadb-connector-python/commit/3d34bb6)\
  2024-09-25 13:35:16 +0200
  * [CONPY-293](https://jira.mariadb.org/browse/CONPY-293): Fix gcc warnings
* [Revision #1d03be3](https://github.com/mariadb-corporation/mariadb-connector-python/commit/1d03be3)\
  2024-09-16 10:13:38 +0200
  * TLS fixes for C/C 3.4.x
* [Revision #afb3ccd](https://github.com/mariadb-corporation/mariadb-connector-python/commit/afb3ccd)\
  2024-09-14 15:31:57 +0200
  * Check return code of db\_generate\_bulk\_request
* [Revision #e705d63](https://github.com/mariadb-corporation/mariadb-connector-python/commit/e705d63)\
  2024-03-18 10:03:57 +0100
  * Fix [CONPY-283](https://jira.mariadb.org/browse/CONPY-283): Incorrect result format after cursor.scroll()

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
