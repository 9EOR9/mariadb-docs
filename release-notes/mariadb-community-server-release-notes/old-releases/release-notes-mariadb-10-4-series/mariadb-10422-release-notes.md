# MariaDB 10.4.22 Release Notes

The most recent release of [MariaDB 10.4](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series) is:[**MariaDB 10.4.34**](mariadb-10-4-34-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.4.34/)

[Download 10.4.22](https://downloads.mariadb.org/mariadb/10.4.22/)[Release Notes](mariadb-10422-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-10-4-series/mariadb-10422-changelog.md)[Overview of 10.4](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/what-is-mariadb-104)

**Release date:** 8 Nov 2021

[MariaDB 10.4](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series) is a previous _stable_ series of MariaDB. It is an evolution\
of [MariaDB 10.3](../release-notes-mariadb-10-3-series/what-is-mariadb-103.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL.

[MariaDB 10.4.22](mariadb-10422-release-notes.md) is a [_**Stable (GA)**_](../../../mariadb-release-criteria.md) release.

**For an overview of** [**MariaDB 10.4**](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series) **see the**[**What is MariaDB 10.4?**](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/what-is-mariadb-104) **page.**

Thanks, and enjoy MariaDB!

## Notable Items

### Galera

* [Galera](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/galera-cluster/README.md) updated to 26.4.11
* Fix for `WSREP: invalid state ROLLED_BACK (FATAL)` ([MDEV-25114](https://jira.mariadb.org/browse/MDEV-25114))

### InnoDB

* `ALTER TABLE…IMPORT TABLESPACE` fixes ([MDEV-18543](https://jira.mariadb.org/browse/MDEV-18543), [MDEV-20931](https://jira.mariadb.org/browse/MDEV-20931), [MDEV-26131](https://jira.mariadb.org/browse/MDEV-26131), [MDEV-26621](https://jira.mariadb.org/browse/MDEV-26621))
* `innodb_undo_log_truncate` fixes ([MDEV-26450](https://jira.mariadb.org/browse/MDEV-26450), [MDEV-26672](https://jira.mariadb.org/browse/MDEV-26672), [MDEV-26864](https://jira.mariadb.org/browse/MDEV-26864))

### Replication

* Memory hogging on slave by ROW event applier is eliminated ([MDEV-26712](https://jira.mariadb.org/browse/MDEV-26712))
* `mysql --binary-mode` now properly handles `\\0` in data ([MDEV-25444](https://jira.mariadb.org/browse/MDEV-25444))
* Fixes race condition between `SHOW BINARY LOGS` and `RESET MASTER` ([MDEV-20215](https://jira.mariadb.org/browse/MDEV-20215))
* Missed statement rollback in case transaction drops or create temporary table is corrected ([MDEV-26833](https://jira.mariadb.org/browse/MDEV-26833))

### Audit Plugin

* The `QUERY_DDL` [server\_audit\_events](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/plugins/mariadb-audit-plugin/mariadb-audit-plugin-options-and-system-variables#server_audit_events) setting now logs `CREATE/DROP [PROCEDURE / FUNCTION / USER]` statements. See [MariaDB Audit Plugin - Log Settings](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/plugins/mariadb-audit-plugin/mariadb-audit-plugin-log-settings). ([MDEV-23457](https://jira.mariadb.org/browse/MDEV-23457))

### Packaging & Misc

* Session tracking flag in OK\_PACKET ([MDEV-26868](https://jira.mariadb.org/browse/MDEV-26868))
* Some views force server (and mysqldump) to generate invalid SQL for their definitions ([MDEV-26299](https://jira.mariadb.org/browse/MDEV-26299))

### Security

* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2021-35604](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-35604)
  * [CVE-2021-46667](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-46667)
  * [CVE-2021-46662](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-46662)
  * [CVE-2022-27385](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-27385)
  * [CVE-2022-27385](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-27385)
  * [CVE-2022-31624](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-31624)

## Changelog

For a complete list of changes made in [MariaDB 10.4.22](mariadb-10422-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-10-4-series/mariadb-10422-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.4.22](mariadb-10422-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-7-1-rc-and-mariadb-10-6-5-10-5-13-10-4-22-10-3-32-and-10-2-41-now-available/).

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
