# Connector/Python 1.0.3 Changelog

{% include "../../../../.gitbook/includes/latest-python.md" %}

<a href="https://mariadb.com/downloads/connectors/connectors-data-access/python-connector/" class="button primary">Download</a> <a href="../../mariadb-connector-python-1-0-release-notes/mariadb-connector-python-1-0-3-release-notes.md" class="button secondary">Release Notes</a> <a href="mariadb-connector-python-103-changelog.md" class="button secondary">Changelog</a> <a href="https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/connectors-quickstart-guides/connector-python-guide" class="button secondary">Connector/Python Overview</a>

**Release date:** 7 Oct 2020

For the highlights of this release, see the [release notes](../../mariadb-connector-python-1-0-release-notes/mariadb-connector-python-1-0-3-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On [GitHub](https://github.com/MariaDB/mariadb-connector-python/) you can view more\
details of the revision and view diffs of the code modified in that revision.

* [Revision #21c9afc](https://github.com/mariadb-corporation/mariadb-connector-python/commit/21c9afc)\
  2020-10-04 12:34:41 +0200
  * Removed reference increment in cursor.description
* [Revision #8944cb8](https://github.com/mariadb-corporation/mariadb-connector-python/commit/8944cb8)\
  2020-10-04 11:35:40 +0200
  * Error handling fixes:
* [Revision #846c0d0](https://github.com/mariadb-corporation/mariadb-connector-python/commit/846c0d0)\
  2020-10-03 16:41:29 +0200
  * Fix for [CONPY-119](https://jira.mariadb.org/browse/CONPY-119): Fixed memory leak
* [Revision #cbd51de](https://github.com/mariadb-corporation/mariadb-connector-python/commit/cbd51de)\
  2020-10-02 12:54:21 +0200
  * When converting parameters also check subtype of a Python Object
* [Revision #bce98d7](https://github.com/mariadb-corporation/mariadb-connector-python/commit/bce98d7)\
  2020-10-02 12:52:09 +0200
  * Fix for [CONPY-118](https://jira.mariadb.org/browse/CONPY-118): Leak when using text protocol
* [Revision #08673bb](https://github.com/mariadb-corporation/mariadb-connector-python/commit/08673bb)\
  2020-09-29 14:14:02 +0200
  * Small "workaround" for [MDEV-23481](https://jira.mariadb.org/browse/MDEV-23481):
* [Revision #8ff0333](https://github.com/mariadb-corporation/mariadb-connector-python/commit/8ff0333)\
  2020-09-29 13:46:13 +0200
  * Fixed conversion of Integer parameters:
* [Revision #3f95456](https://github.com/mariadb-corporation/mariadb-connector-python/commit/3f95456)\
  2020-09-29 13:21:13 +0200
  * [CONPY-117](https://jira.mariadb.org/browse/CONPY-117): Added converter support
* [Revision #5d4a8d5](https://github.com/mariadb-corporation/mariadb-connector-python/commit/5d4a8d5)\
  2020-09-29 11:43:47 +0200
  * Fix for [CONPY-116](https://jira.mariadb.org/browse/CONPY-116): Wrong type reported for SQL type JSON
* [Revision #6ab09b2](https://github.com/mariadb-corporation/mariadb-connector-python/commit/6ab09b2)\
  2020-09-22 07:01:07 +0200
  * Fixed parser bug
* [Revision #23678b3](https://github.com/mariadb-corporation/mariadb-connector-python/commit/23678b3)\
  2020-09-19 15:37:54 +0200
  * removed redundant callproc method entry
* [Revision #6fcb9a5](https://github.com/mariadb-corporation/mariadb-connector-python/commit/6fcb9a5)\
  2020-09-19 15:32:50 +0200
  * more compiler warning fixes
* [Revision #709ac83](https://github.com/mariadb-corporation/mariadb-connector-python/commit/709ac83)\
  2020-09-19 14:05:53 +0200
  * Fixed compiler warnings
* [Revision #3ca93fa](https://github.com/mariadb-corporation/mariadb-connector-python/commit/3ca93fa)\
  2020-09-19 09:29:11 +0200
  * Documentation for FIELD\_TYPE constants
* [Revision #51810b7](https://github.com/mariadb-corporation/mariadb-connector-python/commit/51810b7)\
  2020-09-15 12:34:37 +0200
  * Added constants.FIELD\_TYPE
* [Revision #4989ed0](https://github.com/mariadb-corporation/mariadb-connector-python/commit/4989ed0)\
  2020-09-15 12:33:55 +0200
  * Fixed installation text
* [Revision #8d1fdaa](https://github.com/mariadb-corporation/mariadb-connector-python/commit/8d1fdaa)\
  2020-09-15 12:32:14 +0200
  * Bump version number

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
