# Connector/Python 1.0.5 Changelog

{% include "../../../../.gitbook/includes/latest-python.md" %}

<a href="https://mariadb.com/downloads/connectors/connectors-data-access/python-connector/" class="button primary">Download</a> <a href="../../mariadb-connector-python-1-0-release-notes/mariadb-connector-python-1-0-5-release-notes.md" class="button secondary">Release Notes</a> <a href="mariadb-connector-python-105-changelog.md" class="button secondary">Changelog</a> <a href="https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/connectors-quickstart-guides/connector-python-guide" class="button secondary">Connector/Python Overview</a>

**Release date:** 25 Nov 2020

For the highlights of this release, see the [release notes](../../mariadb-connector-python-1-0-release-notes/mariadb-connector-python-1-0-5-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On [GitHub](https://github.com/MariaDB/mariadb-connector-python/) you can view more\
details of the revision and view diffs of the code modified in that revision.

* [Revision #5718305](https://github.com/mariadb-corporation/mariadb-connector-python/commit/5718305)\
  2020-11-24 15:54:15 +0100
  * Windows build fix
* [Revision #a1c709b](https://github.com/mariadb-corporation/mariadb-connector-python/commit/a1c709b)\
  2020-11-24 14:00:56 +0100
  * Fix for [CONPY-133](https://jira.mariadb.org/browse/CONPY-133):
* [Revision #6a83209](https://github.com/mariadb-corporation/mariadb-connector-python/commit/6a83209)\
  2020-11-24 14:00:15 +0100
  * Fixed base class for exceptions
* [Revision #0f0468a](https://github.com/mariadb-corporation/mariadb-connector-python/commit/0f0468a)\
  2020-11-23 15:15:13 +0100
  * Fix for [CONC-132](https://jira.mariadb.org/browse/CONC-132): Fix leak in connection pool
* [Revision #35a1235](https://github.com/mariadb-corporation/mariadb-connector-python/commit/35a1235)\
  2020-11-23 09:31:20 +0100
  * travis: disable bench
* [Revision #1ae8afb](https://github.com/mariadb-corporation/mariadb-connector-python/commit/1ae8afb)\
  2020-11-22 21:21:39 +0100
  * MySQL test fix: use server side cursor for select only
* [Revision #fab2a6d](https://github.com/mariadb-corporation/mariadb-connector-python/commit/fab2a6d)\
  2020-11-22 20:38:26 +0100
  * Fixed bug in pooling:
* [Revision #5ef5008](https://github.com/mariadb-corporation/mariadb-connector-python/commit/5ef5008)\
  2020-11-20 15:13:45 +0100
  * Set LD\_LIBRARY\_PATH for Connector/C libraries
* [Revision #f55b734](https://github.com/mariadb-corporation/mariadb-connector-python/commit/f55b734)\
  2020-11-20 13:04:12 +0100
  * Save entry path in PROJ\_PATH environment variable
* [Revision #2d48594](https://github.com/mariadb-corporation/mariadb-connector-python/commit/2d48594)\
  2020-11-20 12:05:52 +0100
  * fixed typo in travis script
* [Revision #2a810ef](https://github.com/mariadb-corporation/mariadb-connector-python/commit/2a810ef)\
  2020-11-20 11:33:59 +0100
  * travis fix: change directory to mariadb-connector-python instead of home dir
* [Revision #6cb17e7](https://github.com/mariadb-corporation/mariadb-connector-python/commit/6cb17e7)\
  2020-11-20 09:51:02 +0100
  * Travis fix: change back to home directory after build of connector/c
* [Revision #faf23d6](https://github.com/mariadb-corporation/mariadb-connector-python/commit/faf23d6)\
  2020-11-20 09:32:55 +0100
  * fixed typo (travis test)
* [Revision #185ded7](https://github.com/mariadb-corporation/mariadb-connector-python/commit/185ded7)\
  2020-11-20 09:03:00 +0100
  * Travis fix:
* [Revision #1133b2a](https://github.com/mariadb-corporation/mariadb-connector-python/commit/1133b2a)\
  2020-11-18 21:30:58 +0100
  * Correction for MARIADB\_PLUGIN\_DIR
* [Revision #64c2026](https://github.com/mariadb-corporation/mariadb-connector-python/commit/64c2026)\
  2020-11-18 21:29:57 +0100
  * Revert "Set MARIADB\_PLUGIN\_DIR for travis environment"
* [Revision #b8af772](https://github.com/mariadb-corporation/mariadb-connector-python/commit/b8af772)\
  2020-11-18 19:41:12 +0100
  * Set MARIADB\_PLUGIN\_DIR for travis environment
* [Revision #90ce14c](https://github.com/mariadb-corporation/mariadb-connector-python/commit/90ce14c)\
  2020-11-18 18:15:26 +0100
  * Travis fixes
* [Revision #26ca934](https://github.com/mariadb-corporation/mariadb-connector-python/commit/26ca934)\
  2020-11-18 16:42:35 +0100
  * Test fixes for testing against MySQL server
* [Revision #47ae022](https://github.com/mariadb-corporation/mariadb-connector-python/commit/47ae022)\
  2020-11-18 09:55:38 +0100
  * Disable pypy build (fails due to missing PyStructureSequence\_New)
* [Revision #3ea9319](https://github.com/mariadb-corporation/mariadb-connector-python/commit/3ea9319)\
  2020-11-18 09:53:17 +0100
  * Followup form last fix: remove BLOB or JSON check
* [Revision #76f01e8](https://github.com/mariadb-corporation/mariadb-connector-python/commit/76f01e8)\
  2020-11-17 17:19:36 +0100
  * Test fix:
* [Revision #312ba15](https://github.com/mariadb-corporation/mariadb-connector-python/commit/312ba15)\
  2020-11-16 14:58:59 +0100
  * Follow up of fix for [CONC-130](https://jira.mariadb.org/browse/CONC-130):
* [Revision #acf9f91](https://github.com/mariadb-corporation/mariadb-connector-python/commit/acf9f91)\
  2020-11-16 11:15:22 +0100
  * Fix for [CONPY-127](https://jira.mariadb.org/browse/CONPY-127): Let connector accept None values
* [Revision #a47d3e5](https://github.com/mariadb-corporation/mariadb-connector-python/commit/a47d3e5)\
  2020-11-16 10:03:05 +0100
  * Implementation of [CONPY-129](https://jira.mariadb.org/browse/CONPY-129):
* [Revision #4a5d02a](https://github.com/mariadb-corporation/mariadb-connector-python/commit/4a5d02a)\
  2020-11-16 07:33:53 +0100
  * Fix for [CONPY-130](https://jira.mariadb.org/browse/CONPY-130): DeprecationWarning: builtin type Row has no _module_ attribute
* [Revision #f6be6ba](https://github.com/mariadb-corporation/mariadb-connector-python/commit/f6be6ba)\
  2020-11-16 07:07:50 +0100
  * Fix for [CONPY-131](https://jira.mariadb.org/browse/CONPY-131):
* [Revision #37864dd](https://github.com/mariadb-corporation/mariadb-connector-python/commit/37864dd)\
  2020-11-01 09:14:11 +0100
  * Fix for [CONPY-126](https://jira.mariadb.org/browse/CONPY-126)
* [Revision #ae7e442](https://github.com/mariadb-corporation/mariadb-connector-python/commit/ae7e442)\
  2020-10-20 06:25:48 +0200
  * Bumped version

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
