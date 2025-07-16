# MariaDB 10.5.29 Release Notes

{% hint style="info" %}
The most recent release of [MariaDB 10.5](what-is-mariadb-105.md) is: [**MariaDB 10.5.29**](mariadb-10-5-29-release-notes.md) Stable (GA) <a href="https://downloads.mariadb.org/mariadb/10.5.29/" class="button primary">Download Now</a>\

{% endhint %}

<a href="https://downloads.mariadb.org/mariadb/10.5.29/" class="button primary">Download</a> <a href="mariadb-10-5-29-release-notes.md" class="button secondary">Release Notes</a> <a href="../../changelogs/changelogs-mariadb-105-series/mariadb-10-5-28-changelog.md" class="button secondary">Changelog</a> <a href="what-is-mariadb-105.md" class="button secondary">Overview of 10.5</a>

**Release date:** 8 May 2025

[MariaDB 10.5](what-is-mariadb-105.md) is a previous _stable_ series of MariaDB, [maintained until](https://mariadb.org/about/#maintenance-policy) June 2025. It is an evolution of [MariaDB 10.4](../../../../mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/) with several entirely new features not found anywhere else and with backported and reimplemented features from MySQL.

[MariaDB 10.5.29](mariadb-10-5-29-release-notes.md) is a [_**Stable (GA)**_](../../../mariadb-release-criteria.md) release.

Thanks, and enjoy MariaDB!

## Notable Items

### Storage Engines

#### InnoDB

* Incorrect undo logging for indexes on virtual columns whose index ID does not fit in 32 bits ([MDEV-36613](https://jira.mariadb.org/browse/MDEV-36613))

#### Spider

* The untested ha\_spider::index\_first\_internal constructs broken queries ([MDEV-36324](https://jira.mariadb.org/browse/MDEV-36324))
* Unexpected error 1264 'Out of Range Value for Column' when inserting into ... select ... from a spider table ([MDEV-35874](https://jira.mariadb.org/browse/MDEV-35874))
* Tests calling the udf spider\_copy\_tables fail with --view-protocol ([MDEV-36335](https://jira.mariadb.org/browse/MDEV-36335))

### Data Definition - Alter Table

* ALTER TABLE…SEQUENCE does not work correctly with InnoDB ([MDEV-36038](https://jira.mariadb.org/browse/MDEV-36038))

### GIS

* Server aborts while deleting the record in spatial index ([MDEV-35420](https://jira.mariadb.org/browse/MDEV-35420))

### Upgrades

* Upgrades fail on Windows ([MDEV-36128](https://jira.mariadb.org/browse/MDEV-36128))

### OTHER

* Field pointer may be uninitialized in fill\_record ([MDEV-36181](https://jira.mariadb.org/browse/MDEV-36181))
* Wrong results from tables with a single record and an aggregate ([MDEV-35238](https://jira.mariadb.org/browse/MDEV-35238))

### Galera

* With wsrep\_ignore\_apply\_errors = 0, the node crashes due to assertion thd->is\_error() failed in Sql\_cmd\_dml::prepare(), shown in the logs ([MDEV-35946](https://jira.mariadb.org/browse/MDEV-35946))
* In some cases, if there are MDL locks (for example, when LOCK TABLE is executed), a node could get stuck in the system thread due to incorrect handling of metadata locks (MDL) in server code when a transaction was BF aborted. ([MDEV-35941](https://jira.mariadb.org/browse/MDEV-35941))
* Regression after the fix for [MDEV-31413](https://jira.mariadb.org/browse/MDEV-31413) - sometimes the server crashes with an assertion in wsrep::transaction::before\_rollback(), for example when using OPTIMIZE TABLE on an ARIA table with wsrep\_osu\_method=RSU. ([MDEV-32631](https://jira.mariadb.org/browse/MDEV-32631))
* In Galera, creating sequence with a small cache leads to signal 6 error: \[ERROR] WSREP: FSM: no such a transition REPLICATING -> COMMITTED. ([MDEV-33850](https://jira.mariadb.org/browse/MDEV-33850))
* Assertion \`commit\_trx' failed in innobase\_commit() (ha\_innodb.cc). An INSERT with sql\_log\_bin=0 is still replicated in Galera (per [MDEV-7205](https://jira.mariadb.org/browse/MDEV-7205)), despite binary logging being disabled. This results in a partial binlog bypass, requiring a two-phase commit (2PC). During 2PC, the INSERT is first prepared (entering the PREPARED state in InnoDB), and on commit, the new assertion from [MDEV-24035](https://jira.mariadb.org/browse/MDEV-24035) fails, causing a crash with "Assertion 'commit\_trx' failed" in logs. ([MDEV-35658](https://jira.mariadb.org/browse/MDEV-35658))
* When a sequence is used and inserts run in parallel on multiple Galera nodes, a transaction may be aborted after passing certification. If it then attempts to roll back, the binlog statement cache—which includes reserved sequence values—may be written prematurely. This causes a crash with the diagnostic "WSREP: FSM: no such a transition REPLICATING -> COMMITTED" in the logs, as the transaction is supposed to replay and only write to the binlog during the final commit. ([MDEV-33589](https://jira.mariadb.org/browse/MDEV-33589))
* After a corrupted table on one node triggers the cluster to vote to evict a node that failed a transaction, the current master can't commit any more and hangs. To avoid this crash in the future, the user should also update the galera library to version 26.4.21+. ([MDEV-34998](https://jira.mariadb.org/browse/MDEV-34998))
* Creating partitioned tables is disallowed when wsrep\_osu\_method=TOI and wsrep\_strict\_ddl=ON, preventing alteration or deletion of partitioned tables. ([MDEV-27861](https://jira.mariadb.org/browse/MDEV-27861))
* Attempting to create a CONNECT engine table results in "non-InnoDB sequences in Galera cluster" error message in logs due to an incorrect engine check. ([MDEV-35748](https://jira.mariadb.org/browse/MDEV-35748))
* Build fails with cmake 4.0.0 due to wsrep ([MDEV-36422](https://jira.mariadb.org/browse/MDEV-36422))

### Partitioning

* corruption when query cache cannot allocate block ([MDEV-34075](https://jira.mariadb.org/browse/MDEV-34075))

### Data Manipulation - Update

* Stack looping and SIGSEGV in Item\_args::walk\_args on UPDATE ([MDEV-31647](https://jira.mariadb.org/browse/MDEV-31647))

### Server

* Server crash in find\_field\_in\_tables, Assertion \`name' failed in find\_field\_in\_table\_ref ([MDEV-25012](https://jira.mariadb.org/browse/MDEV-25012))
* Server crash when inserting from derived table containing insert target table ([MDEV-32086](https://jira.mariadb.org/browse/MDEV-32086))
* MariaDB effectively running as root CAP\_DAC\_OVERRIDE ([MDEV-36229](https://jira.mariadb.org/browse/MDEV-36229))
* Build fails with cmake 4.0 ([MDEV-36506](https://jira.mariadb.org/browse/MDEV-36506))

### Plugin - Audit

* Long server\_audit\_file\_path causes buffer overflow ([MDEV-36245](https://jira.mariadb.org/browse/MDEV-36245))

### Optimizer

* group by handler missing constant fields when selecting from a view ([MDEV-36307](https://jira.mariadb.org/browse/MDEV-36307))

### Security

* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2025-30722](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2025-30722)
  * [CVE-2025-30693](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2025-30693)
  * [CVE-2023-52970](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2023-52970)
  * [CVE-2023-52969](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2023-52969)

## Changelog

For a complete list of changes made in MariaDB 10.5.29, with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-105-series/mariadb-10-5-29-changelog.md).

## Contributors

For a full list of contributors to MariaDB 10.5.29, see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-11-0-3-10-11-5-10-10-6-10-9-8-10-6-15-10-5-22-10-4-31-now-available/).

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
