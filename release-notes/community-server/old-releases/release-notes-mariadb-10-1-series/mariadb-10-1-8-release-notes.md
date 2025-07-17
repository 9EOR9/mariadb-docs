# MariaDB 10.1.8 Release Notes

The most recent release of [MariaDB 10.1](changes-improvements-in-mariadb-10-1.md) is:[**MariaDB 10.1.48**](mariadb-10148-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.1.48/)

[Download](https://downloads.mariadb.org/mariadb/10.1.8)[Release Notes](mariadb-10-1-8-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-101-series/mariadb-10-1-8-changelog.md)[Overview of 10.1](changes-improvements-in-mariadb-10-1.md)

**Release date:** 17 Oct 2015

[MariaDB 10.1](changes-improvements-in-mariadb-10-1.md) is the current stable series of MariaDB. It is an evolution\
of [MariaDB 10.0](../release-notes-mariadb-10-0-series/changes-improvements-in-mariadb-10-0.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL 5.6 and 5.7.

[MariaDB 10.1.8](mariadb-10-1-8-release-notes.md) is a [_**Stable (GA)**_](../../about/release-criteria.md) release.

**The release notes here only document changes from the previous version of**[**MariaDB 10.1**](changes-improvements-in-mariadb-10-1.md)**. For a complete overview of** [**MariaDB 10.1**](changes-improvements-in-mariadb-10-1.md) **see the**[**What is MariaDB 10.1?**](changes-improvements-in-mariadb-10-1.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

* [XtraDB](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb) updated to XtraDB-5.6.26-74.0
* systemd support has been added for those distributions that support it.
* For [CSV](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/csv) tables, the [IETF\_QUOTES](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-definition/create/create-table#ietf_quotes) option\
  enables IETF-compatible parsing of embedded quote and comma characters\
  ([MDEV-8682](https://jira.mariadb.org/browse/MDEV-8682)).
* [wsrep\_node\_address](https://app.gitbook.com/s/3VYeeVGUV4AMqrA3zwy7/reference/galera-cluster-system-variables#wsrep_node_address) now\
  supports IPv6 ([MDEV-8034](https://jira.mariadb.org/browse/MDEV-8034)).
* `--silent-startup` [mysqld option](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/starting-and-stopping-mariadb/mariadbd-options). If specified, mysqld does not\
  print Notes to log during startup.
* Replication from MySQL 5.6 with GTID, binlog\_rows\_query\_log\_events and\
  ignorable events now works. In this case MariaDB will remove the MySQL GTIDs\
  and other unneeded events and instead adds its own[GTIDs](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/gtid).
* New proxy server option for the [Feedback Plugin](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/plugins/other-plugins/feedback-plugin), [feedback\_http\_proxy](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/plugins/other-plugins/feedback-plugin#feedback_http_proxy), for use when http calls cannot be made, such as in a firewall environment.
* Explicit or implicit casts from MAX(string) to INT, DOUBLE or DECIMAL now produce warnings ([MDEV-8852](https://jira.mariadb.org/browse/MDEV-8852)).
* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2015-4866](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-4866)
  * [CVE-2015-4864](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-4864)
  * [CVE-2015-4816](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-4816)
  * [CVE-2015-4819](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-4819)
  * [CVE-2015-4879](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-4879)
  * [CVE-2015-4895](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-4895)
  * [CVE-2015-4802](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-4802)
  * [CVE-2015-4807](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-4807)
  * [CVE-2015-4815](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-4815)
  * [CVE-2015-4826](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-4826)
  * [CVE-2015-4830](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-4830)
  * [CVE-2015-4836](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-4836)
  * [CVE-2015-4858](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-4858)
  * [CVE-2015-4861](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-4861)
  * [CVE-2015-4870](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-4870)
  * [CVE-2015-4913](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-4913)
  * [CVE-2015-4792](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-4792)

For a complete list of changes made in [MariaDB 10.1.8](mariadb-10-1-8-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-101-series/mariadb-10-1-8-changelog.md).

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
