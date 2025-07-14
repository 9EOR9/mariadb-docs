# MariaDB Connector/C 2.3.6 Changelog

The most recent [_**Stable**_](../../../../mariadb-release-criteria.md) _**(GA)**_ release of MariaDB Connector/C is:[**MariaDB Connector/C 3.4.5**](../../mariadb-connector-c-3-4-release-notes/mariadb-connector-c-3-4-5-release-notes.md)

[Download](https://downloads.mariadb.org/connector-c/2.3.6)[Release Notes](../../mariadb-connector-c-23-release-notes/mariadb-connector-c-236-release-notes.md)[Changelog](mariadb-connector-c-236-changelog.md)[About MariaDB Connector/C](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-c/README.md)

**Release date:** 7 Jun 2018

For the highlights of this release, see the[release notes](../../mariadb-connector-c-23-release-notes/mariadb-connector-c-236-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-c/) you can view more details of the revision and view diffs of the code\
modified in that revision.

* [Revision #783d7ad](https://github.com/mariadb-corporation/mariadb-connector-c/commit/783d7ad)\
  2018-06-05 08:21:46 +0200
  * Set default charset to latin1
* [Revision #9311595](https://github.com/mariadb-corporation/mariadb-connector-c/commit/9311595)\
  2018-06-05 08:20:53 +0200
  * Revert "bumped version number"
* [Revision #2a83c0b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/2a83c0b)\
  2018-05-30 13:45:00 +0200
  * bumped version number
* [Revision #d2154fa](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d2154fa)\
  2018-05-29 13:34:11 +0200
  * Fixed compiler bug caused by merge from master branch
* [Revision #e245f2d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/e245f2d)\
  2018-05-29 09:49:35 +0200
  * Fix for [CONC-334](https://jira.mariadb.org/browse/CONC-334): Copy all members of MYSQL\_FIELD from mysql->fields to stmt->fields.
* [Revision #589760a](https://github.com/mariadb-corporation/mariadb-connector-c/commit/589760a)\
  2018-05-28 15:57:25 +0200
  * Merge branch 'connector\_c\_2.3' of [mariadb-connector-c](https://github.com/MariaDB/mariadb-connector-c) into connector\_c\_2.3
* [Revision #0781cb9](https://github.com/mariadb-corporation/mariadb-connector-c/commit/0781cb9)\
  2018-05-28 15:47:04 +0200
  * Changed setting version-script file in cmake script
* [Revision #fb100c8](https://github.com/mariadb-corporation/mariadb-connector-c/commit/fb100c8)\
  2018-05-28 15:51:58 +0200
  * Fixed string conversion to MYSQL\_TIME\_TYPE:
    * added support for negative time values
    * invalid strings (and/or conversion) and invalid values will result in MYSQL\_TIMESTAMP\_ERROR time type
    * added support for 2digit year representation:
      * `values < 69` will be converted to `20YY`
      * `values >= 69` will be converted to `19YY`
* [Revision #33fbafa](https://github.com/mariadb-corporation/mariadb-connector-c/commit/33fbafa)\
  2018-05-28 15:46:05 +0200
  * Connection attributes fix: Throw an error if key or val has zero length
* [Revision #01f78eb](https://github.com/mariadb-corporation/mariadb-connector-c/commit/01f78eb)\
  2018-05-25 10:37:51 +0200
  * Set default sign options if not specified
* [Revision #fba1e54](https://github.com/mariadb-corporation/mariadb-connector-c/commit/fba1e54)\
  2018-05-25 10:24:59 +0200
  * Fix msi build (code signing)
* [Revision #d25dbac](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d25dbac)\
  2018-05-24 17:16:56 +0200
  * Add status definitions for server\_status: - SERVER\_STATUS\_IN\_TRANS\_READONLY - SERVER\_STATUS\_ANSI\_QUOTES
* [Revision #351860f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/351860f)\
  2018-05-23 18:59:53 +0200
  * Changes enabling build C/C v2.3 as a sub-project
* [Revision #7d0d7f2](https://github.com/mariadb-corporation/mariadb-connector-c/commit/7d0d7f2)\
  2018-05-22 15:02:20 +0200
  * Add support for length encoded datetime strings: In some cases server doesn't send date values with field type MYSQL\_TYPE\_STRING, but as length encoded string with type MYSQL\_TYPE\_VAR\_STRING.
* [Revision #2861c15](https://github.com/mariadb-corporation/mariadb-connector-c/commit/2861c15)\
  2018-05-17 05:20:55 +0200
  * [MDEV-15450](https://jira.mariadb.org/browse/MDEV-15450): Add Host Name Field to MariaDB Client Handshake Protocol
* [Revision #f71b4f8](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f71b4f8)\
  2018-04-09 15:59:16 +0200
  * Fix for [CONC-315](https://jira.mariadb.org/browse/CONC-315): If no default client character set was specified, the utf8 character set will be used by default (instead of setting the client character set to server character set).
* [Revision #2bd29c2](https://github.com/mariadb-corporation/mariadb-connector-c/commit/2bd29c2)\
  2018-02-20 18:58:17 +0100
  * Fix for [CONC-133](https://jira.mariadb.org/browse/CONC-133): Allow to build connector/c with older (outdated) gcc compilers. This was fixed in C/C 3.0.x already
* [Revision #f99dcfb](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f99dcfb)\
  2018-01-19 07:30:46 +0100
  * Bumped version number to 2.3.6

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
