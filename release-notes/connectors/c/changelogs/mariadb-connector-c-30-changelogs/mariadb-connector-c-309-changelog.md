# MariaDB Connector/C 3.0.9 Changelog

[Download](https://mariadb.com/downloads/?showall=1\&tab=connectors)[Release Notes](../../mariadb-connector-c-30-release-notes/mariadb-connector-c-309-release-notes.md)[Changelog](mariadb-connector-c-309-changelog.md)[About MariaDB Connector/C](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-c/README.md)

**Release date:** 11 Feb 2019

For the highlights of this release, see the [release notes](../../mariadb-connector-c-30-release-notes/mariadb-connector-c-309-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On [GitHub](https://github.com/MariaDB/mariadb-connector-c/) you can view more\
details of the revision and view diffs of the code modified in that revision.

* [Revision #2c5aebb](https://github.com/mariadb-corporation/mariadb-connector-c/commit/2c5aebb)\
  2019-02-08 16:36:35 +0100
  * auto\_local\_infile is not an user-settable option
* [Revision #7923e8d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/7923e8d)\
  2019-02-07 12:12:14 +0100
  * Fix number->string conversion in PS to follow the manual
* [Revision #70f2964](https://github.com/mariadb-corporation/mariadb-connector-c/commit/70f2964)\
  2019-02-07 04:14:55 +0100
  * Fix for [CONC-384](https://jira.mariadb.org/browse/CONC-384):
* [Revision #1e5e21c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/1e5e21c)\
  2019-02-06 18:14:57 +0100
  * compilation on Windows
* [Revision #3e8973c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3e8973c)\
  2019-02-06 16:06:30 +0100
  * it's not a truncation if the number fits into a buffer exactly
* [Revision #95b5dea](https://github.com/mariadb-corporation/mariadb-connector-c/commit/95b5dea)\
  2019-02-06 12:25:20 +0100
  * ENABLED\_LOCAL\_INFILE is always defined now
* [Revision #0ca2f2c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/0ca2f2c)\
  2019-02-06 11:00:42 +0100
  * Fixed conversion from zerofill integer to MYSQL\_TYPE\_STRING:
* [Revision #3beab84](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3beab84)\
  2019-02-06 09:02:03 +0100
  * mtr fix: mysql\_client\_test still uses the deprecated mysql\_list\_fields function, so we can set default value to zero (mysql\_client\_tedt doesn't check the value and crashes).
* [Revision #821185c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/821185c)\
  2019-02-05 14:00:49 +0100
  * Fix for [CONC-387](https://jira.mariadb.org/browse/CONC-387):
* [Revision #438b7f4](https://github.com/mariadb-corporation/mariadb-connector-c/commit/438b7f4)\
  2019-02-05 13:58:07 +0100
  * Merge branch '3.0' of [mariadb-connector-c](https://github.com/MariaDB/mariadb-connector-c) into 3.0
* [Revision #02bf903](https://github.com/mariadb-corporation/mariadb-connector-c/commit/02bf903)\
  2019-02-05 12:37:37 +0100
  * Merge pull request #102 from robertbindar/master
* [Revision #f9e626b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f9e626b)\
  2019-02-05 08:26:36 +0200
  * Support for expired passwords
* [Revision #5783a8b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/5783a8b)\
  2019-02-05 13:56:59 +0100
  * Set values for field->def and field->def\_length to zero - they are populated only from deprecated api function mysql\_list\_fields.
* [Revision #02e7d56](https://github.com/mariadb-corporation/mariadb-connector-c/commit/02e7d56)\
  2019-02-05 07:19:36 +0100
  * Crude "auto-load-data-local-infile" mode
* [Revision #2e3c152](https://github.com/mariadb-corporation/mariadb-connector-c/commit/2e3c152)\
  2019-02-03 21:27:26 +0100
  * Fixed UBSan Error
* [Revision #54afa03](https://github.com/mariadb-corporation/mariadb-connector-c/commit/54afa03)\
  2019-02-03 21:14:49 +0100
  * Fix build with deprecated OpenSSL API:
* [Revision #3ab17c0](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3ab17c0)\
  2019-02-03 17:26:24 +0100
  * Fix compiler warning (gcc-8.1)
* [Revision #017a67e](https://github.com/mariadb-corporation/mariadb-connector-c/commit/017a67e)\
  2019-02-03 17:25:59 +0100
  * Fix compiler warning (missing dl prototypes)
* [Revision #29f18ed](https://github.com/mariadb-corporation/mariadb-connector-c/commit/29f18ed)\
  2019-02-03 16:32:48 +0100
  * Merge branch '3.0' of [mariadb-connector-c](https://github.com/MariaDB/mariadb-connector-c) into 3.0
* [Revision #9f39c5c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/9f39c5c)\
  2019-02-03 09:25:50 +0100
  * Merge pull request #98 from methane/static-sha2
* [Revision #14c8a88](https://github.com/mariadb-corporation/mariadb-connector-c/commit/14c8a88)\
  2019-01-18 17:58:53 +0900
  * Support static linking auth plugins
* [Revision #4c93379](https://github.com/mariadb-corporation/mariadb-connector-c/commit/4c93379)\
  2019-02-03 09:25:09 +0100
  * Merge pull request #99 from methane/release-without-debinfo
* [Revision #5764fba](https://github.com/mariadb-corporation/mariadb-connector-c/commit/5764fba)\
  2019-01-18 20:50:13 +0900
  * Don't install pdb files for Release build
* [Revision #cb08739](https://github.com/mariadb-corporation/mariadb-connector-c/commit/cb08739)\
  2019-02-03 16:28:38 +0100\
  \*
  * Changed return code for mysql\_optionv/mysql\_get\_optionv to 1 (was -1) and added CR\_NOT\_IMPLEMENTED error message. if a options is unknown or not supported. This will fix possible error when setting connection attributes. Kudos to Coray Hickey for providing this patch!
* [Revision #4964fae](https://github.com/mariadb-corporation/mariadb-connector-c/commit/4964fae)\
  2019-01-25 08:13:57 +0100
  * Fix for [CONC-271](https://jira.mariadb.org/browse/CONC-271):
* [Revision #4e29e3b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/4e29e3b)\
  2019-01-25 08:13:29 +0100
  * bumped version number to 3.0.9
* [Revision #d803ec8](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d803ec8)\
  2019-01-19 01:20:14 +0100
  * restore pthread\_self() on Windows, used in openssl implementation
* [Revision #80bdd39](https://github.com/mariadb-corporation/mariadb-connector-c/commit/80bdd39)\
  2019-01-18 17:30:49 +0100
  * fix a 'variable maybe uninitialized' warning
* [Revision #f4ad58c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f4ad58c)\
  2019-01-18 12:26:41 +0100
  * little MySQL compatibility
* [Revision #16c780e](https://github.com/mariadb-corporation/mariadb-connector-c/commit/16c780e)\
  2019-01-17 20:03:14 +0100
  * Build fix: Do not set CMAKE\_REQUIRED\_LIBRARIES before finishing internal checks (CMAKE\_POLICY CMP0075).
* [Revision #5d5f715](https://github.com/mariadb-corporation/mariadb-connector-c/commit/5d5f715)\
  2019-01-17 19:36:30 +0100
  * fix up after eb28bf1dadc08664d7f2a95cbf565b5b7064d359
* [Revision #eb28bf1](https://github.com/mariadb-corporation/mariadb-connector-c/commit/eb28bf1)\
  2019-01-11 19:16:27 +0100
  * [CONC-385](https://jira.mariadb.org/browse/CONC-385) Remove some irrelevant cmake system checks
* [Revision #2fcebab](https://github.com/mariadb-corporation/mariadb-connector-c/commit/2fcebab)\
  2019-01-11 19:11:24 +0100
  * Fix CMake warning CMP0077

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
