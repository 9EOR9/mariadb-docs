# MariaDB Connector/C 3.2.0 Changelog

The most recent [_**Stable**_](../../../../mariadb-release-criteria.md) _**(GA)**_ release of MariaDB Connector/C is:[**MariaDB Connector/C 3.4.5**](../../mariadb-connector-c-3-4-release-notes/mariadb-connector-c-3-4-5-release-notes.md)

[Download](https://mariadb.com/downloads/#connectors)[Release Notes](../../mariadb-connector-c-32-release-notes/mariadb-connector-c-320-release-notes.md)[Changelog](mariadb-connector-c-320-changelog.md)[About MariaDB Connector/C](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/about-mariadb-connector-c/README.md)

**Release date:** 10 Jun 2021

For the highlights of this release, see the[release notes](../../mariadb-connector-c-32-release-notes/mariadb-connector-c-320-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-c/) you can view more\
details of the revision and view diffs of the code modified in that revision.

* [Revision #01ada4b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/01ada4b)\
  2021-05-03 14:01:37 +0200
  * Merge branch '3.1' into 3.2
* [Revision #03d983b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/03d983b)\
  2021-04-20 05:15:05 +0200
  * Travis fix
* [Revision #b637cda](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b637cda)\
  2021-04-19 22:01:31 +0200
  * Move SkySQL test to allowed\_failures section due to sporadic non-reproducible errors.
* [Revision #1d7b00f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/1d7b00f)\
  2021-04-19 21:06:26 +0200
  * Merge branch '3.2' of [mariadb-connector-c](https://github.com/mariadb-corporation/mariadb-connector-c) into 3.2
* [Revision #ec9ae15](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ec9ae15)\
  2021-04-19 20:56:14 +0200
  * Merge pull request #169 from rucha174/bb-3.2-[MDEV-8334](https://jira.mariadb.org/browse/MDEV-8334)-rucha
* [Revision #2f7230c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/2f7230c)\
  2021-03-26 00:55:56 +0530
  * [MDEV-8334](https://jira.mariadb.org/browse/MDEV-8334): Rename utf8 to utf8mb3
* [Revision #e9a2c9e](https://github.com/mariadb-corporation/mariadb-connector-c/commit/e9a2c9e)\
  2021-02-21 16:37:09 +0900
  * Fix typo utf8m4 -> utf8mb4
* [Revision #10784a2](https://github.com/mariadb-corporation/mariadb-connector-c/commit/10784a2)\
  2021-03-22 10:16:13 +0100
  * Fix for [CONC-537](https://jira.mariadb.org/browse/CONC-537): Only read from MYSQL\_HOME if MARIADB\_HOME is not set
* [Revision #66f8dbd](https://github.com/mariadb-corporation/mariadb-connector-c/commit/66f8dbd)\
  2021-03-22 09:28:46 +0100
  * Fix for [CONC-535](https://jira.mariadb.org/browse/CONC-535): disabled checksum ignored in events
* [Revision #c5c37e9](https://github.com/mariadb-corporation/mariadb-connector-c/commit/c5c37e9)\
  2021-03-15 10:40:50 +0100
  * Update server versions for appveyor
* [Revision #d7461f7](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d7461f7)\
  2021-04-19 21:03:19 +0200
  * [CONC-547](https://jira.mariadb.org/browse/CONC-547): Set default character set to utf8mb4
* [Revision #ac658d1](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ac658d1)\
  2021-04-19 12:59:57 +0200
  * Merge branch '3.1' into 3.2
* [Revision #4d5cdf4](https://github.com/mariadb-corporation/mariadb-connector-c/commit/4d5cdf4)\
  2021-04-18 08:14:13 +0200
  * Merge branch '3.1' into 3.2
* [Revision #132c5b5](https://github.com/mariadb-corporation/mariadb-connector-c/commit/132c5b5)\
  2021-04-15 18:19:45 +0200
  * [CONC-433](https://jira.mariadb.org/browse/CONC-433): Add CRL support for GnuTLS
* [Revision #37bb780](https://github.com/mariadb-corporation/mariadb-connector-c/commit/37bb780)\
  2021-04-13 21:42:39 +0200
  * Merge branch '3.1' into 3.2
* [Revision #b57ccee](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b57ccee)\
  2021-04-09 06:23:16 +0200
  * Travis fix:
* [Revision #0f4cfd4](https://github.com/mariadb-corporation/mariadb-connector-c/commit/0f4cfd4)\
  2021-04-07 22:05:45 +0200
  * Travis testing:
* [Revision #0f2a185](https://github.com/mariadb-corporation/mariadb-connector-c/commit/0f2a185)\
  2021-04-07 22:05:04 +0200
  * Merge branch '3.1' into 3.2
* [Revision #4e34b2d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/4e34b2d)\
  2021-04-05 21:41:55 +0200
  * Merge pull request #162 from rucha174/bb-3.2-rucha-[MDEV-22189](https://jira.mariadb.org/browse/MDEV-22189)
* [Revision #a08fd79](https://github.com/mariadb-corporation/mariadb-connector-c/commit/a08fd79)\
  2021-03-25 21:39:33 +0530
  * [MDEV-22189](https://jira.mariadb.org/browse/MDEV-22189): Change error messages inside code to have mariadb instead of mysql
* [Revision #55f71a8](https://github.com/mariadb-corporation/mariadb-connector-c/commit/55f71a8)\
  2021-02-21 16:37:09 +0900
  * Fix typo utf8m4 -> utf8mb4
* [Revision #f97c938](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f97c938)\
  2021-03-22 10:16:13 +0100
  * Fix for [CONC-537](https://jira.mariadb.org/browse/CONC-537): Only read from MYSQL\_HOME if MARIADB\_HOME is not set
* [Revision #7ac85a3](https://github.com/mariadb-corporation/mariadb-connector-c/commit/7ac85a3)\
  2021-03-22 09:28:46 +0100
  * Fix for [CONC-535](https://jira.mariadb.org/browse/CONC-535): disabled checksum ignored in events
* [Revision #ffd1ef8](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ffd1ef8)\
  2021-03-15 10:40:50 +0100
  * Update server versions for appveyor
* [Revision #ae374e0](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ae374e0)\
  2021-03-22 17:16:16 +0100
  * Merge branch '3.1' into 3.2
* [Revision #b6f8883](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b6f8883)\
  2021-03-15 20:06:31 +0100
  * [CONC-534](https://jira.mariadb.org/browse/CONC-534) memory leak in ps\_bugs.c
* [Revision #b36d896](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b36d896)\
  2021-03-15 08:25:59 +0100
  * Merge branch '3.1' into 3.2
* [Revision #b21c39c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b21c39c)\
  2021-03-14 12:03:07 +0100
  * Merge branch '3.1' into 3.2
* [Revision #4aa1734](https://github.com/mariadb-corporation/mariadb-connector-c/commit/4aa1734)\
  2021-03-12 12:40:16 +0100
  * Merge remote-tracking branch 'origin/3.1' into 3.2
* [Revision #ca1ea5c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ca1ea5c)\
  2021-02-23 07:55:35 +0100
  * Fix for [CONC-525](https://jira.mariadb.org/browse/CONC-525): Support LOAD \* LOCAL INFILE statements in binary protocol
* [Revision #375bab0](https://github.com/mariadb-corporation/mariadb-connector-c/commit/375bab0)\
  2021-02-16 18:44:15 +0200
  * Merge 3.1 into 3.2
* [Revision #3cf45a2](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3cf45a2)\
  2020-11-18 11:34:34 +0100
  * Merge branch '3.2' of [mariadb-connector-c](https://github.com/mariadb-corporation/mariadb-connector-c) into 3.2
* [Revision #b4bc6bd](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b4bc6bd)\
  2020-11-12 23:24:54 +0000
  * Merge branch '3.1' into 3.2
* [Revision #a1fb2b5](https://github.com/mariadb-corporation/mariadb-connector-c/commit/a1fb2b5)\
  2020-11-18 11:33:28 +0100
  * Removed connection plugin 'aurora'
* [Revision #b1c2d4e](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b1c2d4e)\
  2020-11-18 11:32:30 +0100
  * Merge remote-tracking branch 'origin/3.1' into 3.2
* [Revision #b11faa1](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b11faa1)\
  2020-11-08 18:00:39 +0100
  * Merge branch '3.1' into 3.2
* [Revision #02f9574](https://github.com/mariadb-corporation/mariadb-connector-c/commit/02f9574)\
  2020-11-06 07:06:23 +0100
  * Merge branch '3.1' into 3.2
* [Revision #fcd9f7b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/fcd9f7b)\
  2020-10-24 08:02:14 +0200
  * Merge branch '3.1' into 3.2
* [Revision #79b1091](https://github.com/mariadb-corporation/mariadb-connector-c/commit/79b1091)\
  2020-10-21 13:22:37 +0200
  * Merge branch '3.1' into 3.2
* [Revision #1af9e9a](https://github.com/mariadb-corporation/mariadb-connector-c/commit/1af9e9a)\
  2020-10-21 13:14:34 +0200
  * Merge branch '3.1' into 3.2
* [Revision #8cd3743](https://github.com/mariadb-corporation/mariadb-connector-c/commit/8cd3743)\
  2020-10-21 09:44:56 +0200
  * Bump version number
* [Revision #fb1b456](https://github.com/mariadb-corporation/mariadb-connector-c/commit/fb1b456)\
  2020-10-21 09:46:18 +0200
  * Bumped version to 3.2.0
* [Revision #561dcf8](https://github.com/mariadb-corporation/mariadb-connector-c/commit/561dcf8)\
  2020-10-21 07:40:53 +0200
  * Merge branch '3.1' into 3.2
* [Revision #6a763b9](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6a763b9)\
  2020-09-22 18:10:40 +0200
  * [MDEV-19237](https://jira.mariadb.org/browse/MDEV-19237) - do not resend prepared statement metadata unnecessarily

{% @marketo/form formid="4316" formId="4316" %}
