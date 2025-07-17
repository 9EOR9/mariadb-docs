# MariaDB 5.3.6 Release Notes

The most recent release in the [MariaDB 5.3 series](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-3-series/broken-reference/README.md) is:[**MariaDB 5.3.12**](mariadb-5312-release-notes.md)

[Download](https://downloads.askmonty.org/mariadb/5.3.6) |**Release Notes** |[Changelog](../../changelogs/changelogs-mariadb-53-series/mariadb-536-changelog.md) |[Overview of 5.3](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-3-series/broken-reference/README.md)

**Release date:** 9 Apr 2012

[MariaDB 5.3.6](mariadb-536-release-notes.md) is a [_**Stable**_](../../about/release-criteria.md) _**(GA)**_ release. In\
general this means that there are no known serious bugs, except for those\
marked as feature requests, that no bugs were fixed since last release that\
caused notable code changes, and that we believe the code is ready for\
general usage (based on bug inflow).

**For a description of** [**MariaDB 5.3**](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-3-series/broken-reference/README.md) **see the**[**What is MariaDB 5.3**](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-3-series/broken-reference/README.md) **page.**

For a list of changes made in [MariaDB 5.3.6](mariadb-536-release-notes.md), with links to detailed\
information on each push, see the[MariaDB 5.3.6 Changelog](../../changelogs/changelogs-mariadb-53-series/mariadb-536-changelog.md).

In most respects [MariaDB](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/mariadb/README.md) will work exactly as MySQL: all commands,\
interfaces, libraries and APIs that exist in MySQL also exist in MariaDB.

## Important Security Fix for Rare Password Bug

[MariaDB 5.3.6](mariadb-536-release-notes.md) fixes a bug that under certain rare circumstances allowed a user\
to connect with an invalid password. **This is a serious security issue.** We\
recommend upgrading from older versions as soon as possible.

## Includes [MariaDB 5.2.12](../release-notes-mariadb-5-2-series/mariadb-5212-release-notes.md) and MySQL 5.1.62

This version of MariaDB includes [MariaDB 5.2.12](../release-notes-mariadb-5-2-series/mariadb-5212-release-notes.md), and, by extension, [MariaDB 5.1.62](../release-notes-mariadb-5-1-series/mariadb-5162-release-notes.md)\
and MySQL 5.1.62. See the [MariaDB 5.2.12 Release Notes](../release-notes-mariadb-5-2-series/mariadb-5212-release-notes.md)\
for the changes made in [MariaDB 5.2.12](../release-notes-mariadb-5-2-series/mariadb-5212-release-notes.md) and see[Changes in MySQL 5.1.62](https://dev.mysql.com/doc/refman/5.1/en/news-5-1-62.html)\
for what changed between this and previous MySQL versions.

## Performance Improvements

[MariaDB 5.3.6](mariadb-536-release-notes.md) includes several performance improvements, including a fix for [Bug #913030](https://bugs.launchpad.net/bugs/913030): "Optimizer chooses a suboptimal excution plan for Q18 from DBT-3".

## Other various bug fixes and enhancements

[MariaDB 5.3.6](mariadb-536-release-notes.md) also includes numerous bug fixes and enhancements, including:

* adding [Bug #956585](https://bugs.launchpad.net/bugs/956585) "Feature request - prevent truncating query in mytop" and a feature request to add 'reading of my.cnf files' to mytop (Thanks to Jean Weisbuch for the patch/suggestion.)
* a patch for [Bug #886479](https://bugs.launchpad.net/bugs/886479) "\[PATCH] plugin boolean result" (Thanks to Maarten Vanraes for the patch)
* a fix for [Bug #970528](https://bugs.launchpad.net/bugs/970528) "Server crashes in my\_strnncollsp\_simple on LEFT JOIN with CSV table, TEXT field"
* and many more...

See the [MariaDB 5.3.6 Changelog](../../changelogs/changelogs-mariadb-53-series/mariadb-536-changelog.md) for a list of every change\
made in [MariaDB 5.3.6](mariadb-536-release-notes.md), with links to detailed information on each push.

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
