# MariaDB 10.11.5 Changelog

<a href="https://downloads.mariadb.org/mariadb/10.11.5/" class="button primary">Download</a> <a href="../../mariadb-10-11-series/mariadb-10-11-5-release-notes.md" class="button secondary">Release Notes</a> <a href="mariadb-10-11-5-changelog.md" class="button secondary">Changelog</a> <a href="../../mariadb-10-11-series/what-is-mariadb-1011.md" class="button secondary">Overview of 10.11</a>

**Release date:** 14 Aug 2023

For the highlights of this release, see the [release notes](../../mariadb-10-11-series/mariadb-10-11-5-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On [GitHub](https://github.com/MariaDB/server/tree/10.11) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Includes all fixes from [MariaDB 10.10.6](../changelogs-mariadb-10-10-series/mariadb-10-10-6-changelog.md)
* Merge [Revision #0edb80f632](https://github.com/MariaDB/server/commit/0edb80f632) 2023-08-09 21:25:47 +0200 - Merge branch '10.10' into 10.11
* Merge [Revision #036df5f970](https://github.com/MariaDB/server/commit/036df5f970) 2023-08-08 14:57:31 +0200 - Merge branch '10.10' into 10.11
* [Revision #1ba5a0205c](https://github.com/MariaDB/server/commit/1ba5a0205c)\
  2023-08-03 14:19:10 +0200
  * [MDEV-31836](https://jira.mariadb.org/browse/MDEV-31836) mysqldump against MYSQL server 8 creates invalid dump
* Merge [Revision #bce3ee704f](https://github.com/MariaDB/server/commit/bce3ee704f) 2023-07-26 14:44:43 +0300 - Merge 10.10 into 10.11
* [Revision #23d1092f8e](https://github.com/MariaDB/server/commit/23d1092f8e)\
  2023-07-25 20:37:07 +0200
  * Update 10.11 HELP
* [Revision #6f955c262a](https://github.com/MariaDB/server/commit/6f955c262a)\
  2023-03-11 16:00:19 -0800
  * Fix syntax FB/FR -> fB/fR and bump version to 10.11 in man pages
* [Revision #2972fbc771](https://github.com/MariaDB/server/commit/2972fbc771)\
  2023-03-11 13:35:30 -0800
  * Fix syntax error in man page headers
* [Revision #e36b648077](https://github.com/MariaDB/server/commit/e36b648077)\
  2023-03-11 13:01:39 -0800
  * [MDEV-23789](https://jira.mariadb.org/browse/MDEV-23789): Fix unnecessary acute accents in man pages
* Merge [Revision #3430767e00](https://github.com/MariaDB/server/commit/3430767e00) 2023-07-04 08:19:48 +0300 - Merge 10.10 into 10.11
* Merge [Revision #71a1a28a49](https://github.com/MariaDB/server/commit/71a1a28a49) 2023-06-27 17:45:06 +0300 - Merge 10.10 into 10.11
* [Revision #774dee9abc](https://github.com/MariaDB/server/commit/774dee9abc)\
  2023-05-03 00:34:31 +0000
  * Fix compiler warnings
* [Revision #3eab2275d0](https://github.com/MariaDB/server/commit/3eab2275d0)\
  2023-06-12 14:57:21 +0300
  * Added option sql\_error\_warnings to sql\_error\_log plugin
* [Revision #582d0cf5b0](https://github.com/MariaDB/server/commit/582d0cf5b0)\
  2023-06-09 12:37:03 +0300
  * Added not\_as\_root.inc to some test scripts that fails if run as root
* [Revision #c70f35f00b](https://github.com/MariaDB/server/commit/c70f35f00b)\
  2023-06-08 17:15:16 +0300
  * Disable flush\_logs\_not\_windows.test of run as root (causes failure)
* [Revision #29ec07a5b1](https://github.com/MariaDB/server/commit/29ec07a5b1)\
  2023-06-08 15:50:50 +0300
  * Update BUILD scripts
* Merge [Revision #56bcb2b5c6](https://github.com/MariaDB/server/commit/56bcb2b5c6) 2023-06-08 11:23:45 +0300 - Merge mariadb-10.11.4 into 10.11
* Merge [Revision #5d7b957eb0](https://github.com/MariaDB/server/commit/5d7b957eb0) 2023-06-08 11:23:08 +0300 - Merge 10.10 into 10.11
* Merge [Revision #e0af03d16c](https://github.com/MariaDB/server/commit/e0af03d16c) 2023-06-07 10:46:23 -0400 - Merge branch 'bb-10.11-bumpversion' of github.com:MariaDB/server into bb-10.11-bumpversion
* [Revision #a2aaf26aaa](https://github.com/MariaDB/server/commit/a2aaf26aaa)\
  2023-06-07 08:16:38 -0400
  * bump the VERSION
* [Revision #5b0fe27783](https://github.com/MariaDB/server/commit/5b0fe27783)\
  2023-06-07 08:16:38 -0400
  * bump the VERSION
* Merge [Revision #c04284e747](https://github.com/MariaDB/server/commit/c04284e747) 2023-06-07 15:01:43 +0300 - Merge 10.10 into 10.11
* [Revision #e9fe39d566](https://github.com/MariaDB/server/commit/e9fe39d566)\
  2023-05-23 15:32:50 +0300
  * [MDEV-7389](https://jira.mariadb.org/browse/MDEV-7389) Request: log warnings into SQL\_ERROR\_LOG
* [Revision #7c9f275ee4](https://github.com/MariaDB/server/commit/7c9f275ee4)\
  2023-05-11 10:01:35 +0100
  * server.cnf: adjust major version to 10.11
* Merge [Revision #1916bf2a02](https://github.com/MariaDB/server/commit/1916bf2a02) 2023-05-11 10:00:06 +0300 - Merge 10.10 into 10.11
* [Revision #45a879f6cf](https://github.com/MariaDB/server/commit/45a879f6cf)\
  2023-05-10 20:08:33 +0300
  * Fix ./mtr --view-protocol opt\_trace
* Merge [Revision #4ee040420a](https://github.com/MariaDB/server/commit/4ee040420a) 2023-05-11 09:53:18 +0300 - Merge mariadb-10.11.3 into 10.11
* [Revision #40a857c908](https://github.com/MariaDB/server/commit/40a857c908)\
  2023-05-10 08:48:11 -0400
  * bump the VERSION
* [Revision #de8567559e](https://github.com/MariaDB/server/commit/de8567559e)\
  2023-05-02 18:09:34 +1000
  * deb: autobake - add mantic
* [Revision #41dbc32665](https://github.com/MariaDB/server/commit/41dbc32665)\
  2023-04-23 10:59:32 +0200
  * [MDEV-31140](https://jira.mariadb.org/browse/MDEV-31140): FLUSH BINARY LOGS DELETE\_DOMAIN\_ID=(D) can errorneously delete active domains

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
