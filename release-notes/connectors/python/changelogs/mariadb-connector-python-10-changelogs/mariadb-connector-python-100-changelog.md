# Connector/Python 1.0.0 Changelog

{% include "../../../../.gitbook/includes/latest-python.md" %}

<a href="https://mariadb.com/downloads/connectors/connectors-data-access/python-connector/" class="button primary">Download</a> <a href="../../mariadb-connector-python-1-0-release-notes/mariadb-connector-python-1-0-0-release-notes.md" class="button secondary">Release Notes</a> <a href="mariadb-connector-python-100-changelog.md" class="button secondary">Changelog</a> <a href="https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/connectors-quickstart-guides/connector-python-guide" class="button secondary">Connector/Python Overview</a>

**Release date:** 24 Jun 2020

For the highlights of this release, see the [release notes](../../mariadb-connector-python-1-0-release-notes/mariadb-connector-python-1-0-0-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On [GitHub](https://github.com/MariaDB/mariadb-connector-python/) you can view more\
details of the revision and view diffs of the code modified in that revision.

* [Revision #5f2a2e1](https://github.com/mariadb-corporation/mariadb-connector-python/commit/5f2a2e1)\
  2020-06-19 14:56:55 +0200
  * Updated documentation
* [Revision #ea8354b](https://github.com/mariadb-corporation/mariadb-connector-python/commit/ea8354b)\
  2020-06-18 10:23:56 +0200
  * Added internal members for client and server capabilities to `MrdbConnection` class.
* [Revision #5fd14c9](https://github.com/mariadb-corporation/mariadb-connector-python/commit/5fd14c9)\
  2020-06-17 14:48:15 +0200
  * Fix for [CONPY-81](https://jira.mariadb.org/browse/CONPY-81): If a cursor was previously executed in text protocol,\
    the `is_text` indicator has to be set to 0 after cursor was cleared
* [Revision #1aa828d](https://github.com/mariadb-corporation/mariadb-connector-python/commit/1aa828d)\
  2020-06-17 09:11:21 +0200
  * Skip `test_reconnect` when running with MaxScale
* [Revision #5631d6e](https://github.com/mariadb-corporation/mariadb-connector-python/commit/5631d6e)\
  2020-06-17 08:59:31 +0200
  * Fixed bug in pooling tests
* [Revision #9076358](https://github.com/mariadb-corporation/mariadb-connector-python/commit/9076358)\
  2020-06-16 18:27:49 +0200
  * removed eoled versions 5.5 and 10.0
* [Revision #f28614a](https://github.com/mariadb-corporation/mariadb-connector-python/commit/f28614a)\
  2020-06-16 17:34:59 +0200
  * Skip test conpy\_61 when running against MaxScale
* [Revision #7d7add3](https://github.com/mariadb-corporation/mariadb-connector-python/commit/7d7add3)\
  2020-06-16 16:59:45 +0200
  * Fixed wrong check of return valuFixed wrong check of return valuee
* [Revision #1dba5d6](https://github.com/mariadb-corporation/mariadb-connector-python/commit/1dba5d6)\
  2020-06-16 16:58:53 +0200
  * Revert "Disable executemany() tests when running against MaxScale."
* [Revision #d24957c](https://github.com/mariadb-corporation/mariadb-connector-python/commit/d24957c)\
  2020-06-16 16:16:47 +0200
  * Disable executemany() tests when running against MaxScale.
* [Revision #b745643](https://github.com/mariadb-corporation/mariadb-connector-python/commit/b745643)\
  2020-06-16 15:35:14 +0200
  * CONPY\_76: Added the follwing aliases for connection parameter
    * username
    * passwd
    * db
* [Revision #b29b7b4](https://github.com/mariadb-corporation/mariadb-connector-python/commit/b29b7b4)\
  2020-06-16 15:08:53 +0200
  * removed copy/paste error in test\_cursor.py
* [Revision #ffa959a](https://github.com/mariadb-corporation/mariadb-connector-python/commit/ffa959a)\
  2020-06-11 19:33:28 +0200
  * \[misc] test reliability improvement \* maxscale doesn't support compression \* query "SELECT 1 WHERE 1=2" is supported only after 10.3 server. \* avoiding reuse pool name in test \* pypy: Decimal type is supported \* del cursor with pypy doesn't call tp\_dealloc, not closing cursor. test explicitly close cursor when state is not finished. \* test correction when TEST\_HOST is set
* [Revision #b491915](https://github.com/mariadb-corporation/mariadb-connector-python/commit/b491915)\
  2020-06-16 13:51:08 +0200
  * Fix for [CONPY-79](https://jira.mariadb.org/browse/CONPY-79): When emulating bulkinsert (internal function\
    execute\_many\_fallback) NULL values were not properly handled. As a solution\
    we just change the buffer type to MYSQL\_TYPE\_NULL, since it doesn't affect\
    real bulk insert, where we replace the null value by an indicator
* [Revision #ed2695b](https://github.com/mariadb-corporation/mariadb-connector-python/commit/ed2695b)\
  2020-06-15 10:13:26 +0200
  * Fix for [CONPY-78](https://jira.mariadb.org/browse/CONPY-78): Check for server capabilities instead of version
* [Revision #d0e484f](https://github.com/mariadb-corporation/mariadb-connector-python/commit/d0e484f)\
  2020-06-15 08:45:04 +0200
  * Skip compress test on travis.
* [Revision #574975b](https://github.com/mariadb-corporation/mariadb-connector-python/commit/574975b)\
  2020-06-15 08:10:14 +0200
  * Don't use default connection for xa tests
* [Revision #c4a8453](https://github.com/mariadb-corporation/mariadb-connector-python/commit/c4a8453)\
  2020-06-14 14:57:45 +0200
  * Fix/Workaround for [CONPY-75](https://jira.mariadb.org/browse/CONPY-75)
    * Set default port to 3306
    * Use LIMIT 0 to return an empty result set
* [Revision #1a5849f](https://github.com/mariadb-corporation/mariadb-connector-python/commit/1a5849f)\
  2020-06-14 13:34:38 +0200
  * Fix for [CONC-72](https://jira.mariadb.org/browse/CONC-72): When deallocating the connection pool class, we need to\
    check beside pool\_size if the array containing the connections is valid.
* [Revision #2b5695a](https://github.com/mariadb-corporation/mariadb-connector-python/commit/2b5695a)\
  2020-06-08 13:08:55 +0200
  * Added missing example for documentation
* [Revision #ba052ad](https://github.com/mariadb-corporation/mariadb-connector-python/commit/ba052ad)\
  2020-06-08 12:25:54 +0200
  * Added chapter usage (documentation)
* [Revision #9a24ee4](https://github.com/mariadb-corporation/mariadb-connector-python/commit/9a24ee4)\
  2020-06-08 11:52:35 +0200
  * Documentation fix for executemany()
* [Revision #75c4149](https://github.com/mariadb-corporation/mariadb-connector-python/commit/75c4149)\
  2020-06-06 16:01:35 +0200
  * Merge branch 'master' of [mariadb-connector-python](https://github.com/mariadb-corporation/mariadb-connector-python)
* [Revision #55fa735](https://github.com/mariadb-corporation/mariadb-connector-python/commit/55fa735)\
  2020-06-06 07:01:10 +0200
  * removed pre release segment for GA
* [Revision #47963b0](https://github.com/mariadb-corporation/mariadb-connector-python/commit/47963b0)\
  2020-06-06 16:00:57 +0200
  * Updated link for documentation
* [Revision #f6984c9](https://github.com/mariadb-corporation/mariadb-connector-python/commit/f6984c9)\
  2020-06-06 08:48:27 +0200\
  \*
  * removed debug printf - changed location for documentation
* [Revision #8f7243d](https://github.com/mariadb-corporation/mariadb-connector-python/commit/8f7243d)\
  2020-06-06 07:20:58 +0200
  * Merge branch 'master' of [mariadb-connector-python](https://github.com/mariadb-corporation/mariadb-connector-python)
* [Revision #3380bc2](https://github.com/mariadb-corporation/mariadb-connector-python/commit/3380bc2)\
  2020-06-05 18:29:45 +0200
  * Set theme jekyll-theme-minimal
* [Revision #c26a54e](https://github.com/mariadb-corporation/mariadb-connector-python/commit/c26a54e)\
  2020-06-05 18:05:27 +0200
  * Set theme jekyll-theme-minimal
* [Revision #c2ca32a](https://github.com/mariadb-corporation/mariadb-connector-python/commit/c2ca32a)\
  2020-06-06 07:20:02 +0200
  * Added missing dirs for github pages
* [Revision #10425de](https://github.com/mariadb-corporation/mariadb-connector-python/commit/10425de)\
  2020-06-05 18:03:34 +0200
  * Fixed documentation, added release notes
* [Revision #d1b1f08](https://github.com/mariadb-corporation/mariadb-connector-python/commit/d1b1f08)\
  2020-06-05 16:39:38 +0200
  * Changed "Development Status" classifier from Beta to Stable.
* [Revision #6dbcaf5](https://github.com/mariadb-corporation/mariadb-connector-python/commit/6dbcaf5)\
  2020-06-05 16:35:40 +0200
  * Calclulation of data type using \_PyLong\_NumBits was incorrect
* [Revision #190ea4e](https://github.com/mariadb-corporation/mariadb-connector-python/commit/190ea4e)\
  2020-06-05 07:41:23 +0200
  * Fixed bug when inserting negative numbers with execute() method.
* [Revision #63e0b4a](https://github.com/mariadb-corporation/mariadb-connector-python/commit/63e0b4a)\
  2020-06-03 13:34:48 +0200
  * Changed html scheme for documentation. Adjusted version number in documentation.
* [Revision #209c356](https://github.com/mariadb-corporation/mariadb-connector-python/commit/209c356)\
  2020-06-03 13:10:18 +0200
  * Added docs directory for github pages.
* [Revision #b252696](https://github.com/mariadb-corporation/mariadb-connector-python/commit/b252696)\
  2020-06-02 08:43:27 +0200
  * Fix for [CONPY-70](https://jira.mariadb.org/browse/CONPY-70): `set_config()` method needs to check the passed\
    parameter and raise an exception if the parameter type is not a dictionary.
* [Revision #64df884](https://github.com/mariadb-corporation/mariadb-connector-python/commit/64df884)\
  2020-06-01 19:02:43 +0200
  * Fix for [CONPY-69](https://jira.mariadb.org/browse/CONPY-69): We need to send the default character set already with\
    authentication packet not as an extra call after connect.
* [Revision #0ed16c9](https://github.com/mariadb-corporation/mariadb-connector-python/commit/0ed16c9)\
  2020-05-27 10:42:28 +0200
  * Bumped version number to 1.0.0
* [Revision #e58caef](https://github.com/mariadb-corporation/mariadb-connector-python/commit/e58caef)\
  2020-05-27 10:40:35 +0200
  * Fix for [CONPY-67](https://jira.mariadb.org/browse/CONPY-67): If no rows were fetched from an unbuffered cursor\
    (resultset) rowcount now returns `-1` instead of `0`
* [Revision #ea8354b](https://github.com/mariadb-corporation/mariadb-connector-python/commit/ea8354b)\
  2020-06-18 10:23:56 +0200
  * Added internal members for client and server capabilities to MrdbConnection class.
* [Revision #5fd14c9](https://github.com/mariadb-corporation/mariadb-connector-python/commit/5fd14c9)\
  2020-06-17 14:48:15 +0200
  * Fix for [CONPY-81](https://jira.mariadb.org/browse/CONPY-81): If a cursor was previously executed in text protocol, is\_text indicator\
    has to be set to 0 after cursor was cleared.
* [Revision #1aa828d](https://github.com/mariadb-corporation/mariadb-connector-python/commit/1aa828d)\
  2020-06-17 09:11:21 +0200
  * Skip test\_reconnect when running with MaxScale
* [Revision #5631d6e](https://github.com/mariadb-corporation/mariadb-connector-python/commit/5631d6e)\
  2020-06-17 08:59:31 +0200
  * Fixed bug in pooling tests
* [Revision #9076358](https://github.com/mariadb-corporation/mariadb-connector-python/commit/9076358)\
  2020-06-16 18:27:49 +0200
  * removed eoled versions 5.5 and 10.0
* [Revision #f28614a](https://github.com/mariadb-corporation/mariadb-connector-python/commit/f28614a)\
  2020-06-16 17:34:59 +0200
  * Skip test conpy\_61 when running against MaxScale
* [Revision #7d7add3](https://github.com/mariadb-corporation/mariadb-connector-python/commit/7d7add3)\
  2020-06-16 16:59:45 +0200
  * Fixed wrong check of return valuFixed wrong check of return valuee
* [Revision #1dba5d6](https://github.com/mariadb-corporation/mariadb-connector-python/commit/1dba5d6)\
  2020-06-16 16:58:53 +0200
  * Revert "Disable executemany() tests when running against MaxScale."
* [Revision #d24957c](https://github.com/mariadb-corporation/mariadb-connector-python/commit/d24957c)\
  2020-06-16 16:16:47 +0200
  * Disable executemany() tests when running against MaxScale.
* [Revision #b745643](https://github.com/mariadb-corporation/mariadb-connector-python/commit/b745643)\
  2020-06-16 15:35:14 +0200
  * CONPY\_76: Added the follwing aliases for connection parameter
    * username
    * passwd
    * db
* [Revision #b29b7b4](https://github.com/mariadb-corporation/mariadb-connector-python/commit/b29b7b4)\
  2020-06-16 15:08:53 +0200
  * removed copy/paste error in test\_cursor.py
* [Revision #ffa959a](https://github.com/mariadb-corporation/mariadb-connector-python/commit/ffa959a)\
  2020-06-11 19:33:28 +0200
  * \[misc] test reliability improvement
    * maxscale doesn't support compression
    * query "`SELECT 1 WHERE 1=2`" is supported only after 10.3 server
    * avoiding reuse pool name in test
    * pypy: Decimal type is supported
    * del cursor with pypy doesn't call tp\_dealloc, not closing cursor. test explicitly close cursor when state is not finished.
    * test correction when TEST\_HOST is set
* [Revision #b491915](https://github.com/mariadb-corporation/mariadb-connector-python/commit/b491915)\
  2020-06-16 13:51:08 +0200
  * Fix for [CONPY-79](https://jira.mariadb.org/browse/CONPY-79): When emulating bulkinsert (internal function execute\_many\_fallback) NULL values were not properly handled. As a solution we just change the buffer type to MYSQL\_TYPE\_NULL, since it doesn't affect real bulk insert, where we replace the null value by an indicator
* [Revision #ed2695b](https://github.com/mariadb-corporation/mariadb-connector-python/commit/ed2695b)\
  2020-06-15 10:13:26 +0200
  * Fix for [CONPY-78](https://jira.mariadb.org/browse/CONPY-78): Instead of checking the server version number if a specific feature is supported, we need to check the server capability or extended capability flag.
* [Revision #d0e484f](https://github.com/mariadb-corporation/mariadb-connector-python/commit/d0e484f)\
  2020-06-15 08:45:04 +0200
  * Skip compress test on travis.
* [Revision #574975b](https://github.com/mariadb-corporation/mariadb-connector-python/commit/574975b)\
  2020-06-15 08:10:14 +0200
  * Don't use default connection for xa tests
* [Revision #c4a8453](https://github.com/mariadb-corporation/mariadb-connector-python/commit/c4a8453)\
  2020-06-14 14:57:45 +0200
  * Fix/Workaround for [CONPY-75](https://jira.mariadb.org/browse/CONPY-75)
* [Revision #1a5849f](https://github.com/mariadb-corporation/mariadb-connector-python/commit/1a5849f)\
  2020-06-14 13:34:38 +0200
  * Fix for [CONC-72](https://jira.mariadb.org/browse/CONC-72): When deallocating the connection pool class, we need to check beside pool\_size if the array containing the connections is valid.
* [Revision #2b5695a](https://github.com/mariadb-corporation/mariadb-connector-python/commit/2b5695a)\
  2020-06-08 13:08:55 +0200
  * Added missing example for documentation
* [Revision #ba052ad](https://github.com/mariadb-corporation/mariadb-connector-python/commit/ba052ad)\
  2020-06-08 12:25:54 +0200
  * Added chapter usage (documentation)
* [Revision #9a24ee4](https://github.com/mariadb-corporation/mariadb-connector-python/commit/9a24ee4)\
  2020-06-08 11:52:35 +0200
  * Documentation fix for executemany()
* [Revision #75c4149](https://github.com/mariadb-corporation/mariadb-connector-python/commit/75c4149)\
  2020-06-06 16:01:35 +0200
  * Merge branch 'master' of [mariadb-connector-python](https://github.com/mariadb-corporation/mariadb-connector-python)
* [Revision #55fa735](https://github.com/mariadb-corporation/mariadb-connector-python/commit/55fa735)\
  2020-06-06 07:01:10 +0200
  * removed pre release segment for GA
* [Revision #47963b0](https://github.com/mariadb-corporation/mariadb-connector-python/commit/47963b0)\
  2020-06-06 16:00:57 +0200
  * Updated link for documentation
* [Revision #f6984c9](https://github.com/mariadb-corporation/mariadb-connector-python/commit/f6984c9)\
  2020-06-06 08:48:27 +0200
  * removed debug printf - changed location for documentation
* [Revision #8f7243d](https://github.com/mariadb-corporation/mariadb-connector-python/commit/8f7243d)\
  2020-06-06 07:20:58 +0200
  * Merge branch 'master' of [mariadb-connector-python](https://github.com/mariadb-corporation/mariadb-connector-python)
* [Revision #3380bc2](https://github.com/mariadb-corporation/mariadb-connector-python/commit/3380bc2)\
  2020-06-05 18:29:45 +0200
  * Set theme jekyll-theme-minimal
* [Revision #c26a54e](https://github.com/mariadb-corporation/mariadb-connector-python/commit/c26a54e)\
  2020-06-05 18:05:27 +0200
  * Set theme jekyll-theme-minimal
* [Revision #c2ca32a](https://github.com/mariadb-corporation/mariadb-connector-python/commit/c2ca32a)\
  2020-06-06 07:20:02 +0200
  * Added missing dirs for github pages
* [Revision #10425de](https://github.com/mariadb-corporation/mariadb-connector-python/commit/10425de)\
  2020-06-05 18:03:34 +0200
  * Fixed documentation, added release notes
* [Revision #d1b1f08](https://github.com/mariadb-corporation/mariadb-connector-python/commit/d1b1f08)\
  2020-06-05 16:39:38 +0200
  * Changed "Development Status" classifier from Beta to Stable.
* [Revision #6dbcaf5](https://github.com/mariadb-corporation/mariadb-connector-python/commit/6dbcaf5)\
  2020-06-05 16:35:40 +0200
  * Calclulation of data type using \_PyLong\_NumBits was incorrect
* [Revision #190ea4e](https://github.com/mariadb-corporation/mariadb-connector-python/commit/190ea4e)\
  2020-06-05 07:41:23 +0200
  * Fixed bug when inserting negative numbers with execute() method.
* [Revision #63e0b4a](https://github.com/mariadb-corporation/mariadb-connector-python/commit/63e0b4a)\
  2020-06-03 13:34:48 +0200
  * Changed html scheme for documentation. Adjusted version number in documentation.
* [Revision #209c356](https://github.com/mariadb-corporation/mariadb-connector-python/commit/209c356)\
  2020-06-03 13:10:18 +0200
  * Added docs directory for github pages.
* [Revision #b252696](https://github.com/mariadb-corporation/mariadb-connector-python/commit/b252696)\
  2020-06-02 08:43:27 +0200
  * Fix for [CONPY-70](https://jira.mariadb.org/browse/CONPY-70): set\_config() method needs to check the passed parameter and raise an exception if the parameter type is not a dictionary.
* [Revision #64df884](https://github.com/mariadb-corporation/mariadb-connector-python/commit/64df884)\
  2020-06-01 19:02:43 +0200
  * Fix for [CONPY-69](https://jira.mariadb.org/browse/CONPY-69): We need to send the default character set already with authentication packet not as an extra call after connect.
* [Revision #0ed16c9](https://github.com/mariadb-corporation/mariadb-connector-python/commit/0ed16c9)\
  2020-05-27 10:42:28 +0200
  * Bumped version number to 1.0.0
* [Revision #e58caef](https://github.com/mariadb-corporation/mariadb-connector-python/commit/e58caef)\
  2020-05-27 10:40:35 +0200
  * Fix for [CONPY-67](https://jira.mariadb.org/browse/CONPY-67): If no rows were fetched from an unbuffered cursor (resultset) rowcount now returns -1 instead of 0.

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
