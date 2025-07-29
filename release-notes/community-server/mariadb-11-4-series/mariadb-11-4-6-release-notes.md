# MariaDB 11.4.6 Release Notes

**Note:** This page describes features in the source repository for [**MariaDB 11.4**](what-is-mariadb-114.md). There are currently no official packages or binaries available for download which contain the features. If you want to try out any of the new features described here you will need to [get](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/server-client-software/download/getting-the-mariadb-source-code) and [compile](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/install-and-upgrade-mariadb/installing-mariadb/compiling-mariadb-from-source) the\
code yourself.

{% include "../../.gitbook/includes/latest-11-4.md" %}

&#x20;<a href="mariadb-11-4-5-release-notes.md" class="button secondary">Release Notes</a> <a href="../changelogs/changelogs-mariadb-11-4-series/mariadb-11-4-5-changelog.md" class="button secondary">Changelog</a> <a href="what-is-mariadb-114.md" class="button secondary">Overview of 11.4</a>

[MariaDB 11.4](what-is-mariadb-114.md) is the current long-term series of MariaDB and will be maintained until May 2029. It is an evolution of [MariaDB 11.3](../old-releases/release-notes-mariadb-11-3-rolling-releases/what-is-mariadb-113.md) with several entirely new features.

[MariaDB 11.4.6](mariadb-11-4-6-release-notes.md) is a [_**Stable (GA)**_](../about/release-criteria.md) release.

**For an overview of** [**MariaDB 11.4**](what-is-mariadb-114.md) **see the**[**What is MariaDB 11.4?**](what-is-mariadb-114.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Items

### Storage Engines

#### InnoDB

* Incorrect undo logging for indexes on virtual columns whose index ID does not fit in 32 bits ([MDEV-36613](https://jira.mariadb.org/browse/MDEV-36613))
* Race conditions between ALTER TABLE or OPTIMIZE TABLE and the purge of transaction history were fixed. ([MDEV-36122](https://jira.mariadb.org/browse/MDEV-36122))
* ASAN errors in dict\_sys\_t::load\_table / get\_foreign\_key\_info after failing to load a table ([MDEV-33167](https://jira.mariadb.org/browse/MDEV-33167))
* CREATE INDEX fails to heal a FOREIGN KEY constraint ([MDEV-35962](https://jira.mariadb.org/browse/MDEV-35962))
* Doublewrite recovery of innodb\_checksum\_algorithm=full\_crc32 page\_compressed pages does not work ([MDEV-36180](https://jira.mariadb.org/browse/MDEV-36180))
* innodb\_snapshot\_isolation=1 gives error for not committed row changes ([MDEV-36639](https://jira.mariadb.org/browse/MDEV-36639))
* The deprecated parameter innodb\_purge\_rseg\_truncate\_frequency is not being recognized ([MDEV-36378](https://jira.mariadb.org/browse/MDEV-36378))
* dict\_stats\_fetch\_from\_ps() unnecessarily holds exclusive dict\_sys.latch ([MDEV-35436](https://jira.mariadb.org/browse/MDEV-35436))
* Stall and crash when page cleaner fails to generate free pages during Async flush ([MDEV-36226](https://jira.mariadb.org/browse/MDEV-36226))
* Performance regression in INSERT…SELECT due to unnecessarily making InnoDB log durable. ([MDEV-35813](https://jira.mariadb.org/browse/MDEV-35813))
* decreasing innodb\_buffer\_pool\_size at runtime does not release memory ([MDEV-32339](https://jira.mariadb.org/browse/MDEV-32339))
* LSN allocation is a bottleneck ([MDEV-21923](https://jira.mariadb.org/browse/MDEV-21923))
* reorganise innodb buffer pool (and remove buffer pool chunks) ([MDEV-29445](https://jira.mariadb.org/browse/MDEV-29445))
* FLUSH TABLES will no longer cause InnoDB persistent statistics to be reloaded. RENAME TABLE will. This change of logic improves the performance in general, and avoids a case where statistics for relatively rarely modified tables are never updated. ([MDEV-35000](https://jira.mariadb.org/browse/MDEV-35000))
* The Linux memory pressure interface, which could previously not be disabled and could cause performance anomalies, was rewritten and is disabled by default. ([MDEV-34863](https://jira.mariadb.org/browse/MDEV-34863))
* Race condition between log\_t::resize\_start() and log\_t::resize\_abort() ([MDEV-36082](https://jira.mariadb.org/browse/MDEV-36082))
* Memory leak after failed CREATE TABLE…SELECT; crash on CREATE TABLE…SELECT that reads from multiple tables ([MDEV-36504](https://jira.mariadb.org/browse/MDEV-36504))
* Server crashes when resizing default innodb buffer pool after setting innodb-buffer-pool-chunk-size to 1M ([MDEV-34677](https://jira.mariadb.org/browse/MDEV-34677))

#### Spider

* The untested ha\_spider::index\_first\_internal constructs broken queries ([MDEV-36324](https://jira.mariadb.org/browse/MDEV-36324))
* Unexpected error 1264 'Out of Range Value for Column' when inserting into ... select ... from a spider table ([MDEV-35874](https://jira.mariadb.org/browse/MDEV-35874))
* Tests calling the udf spider\_copy\_tables fail with --view-protocol ([MDEV-36335](https://jira.mariadb.org/browse/MDEV-36335))

### Optimizer

* group by handler missing constant fields when selecting from a view ([MDEV-36307](https://jira.mariadb.org/browse/MDEV-36307))
* A multi-table UPDATE ... ORDER BY ... LIMIT statement could update the wrong rows when the ORDER BY clause was resolved by using temporary and filesort. ([MDEV-35955](https://jira.mariadb.org/browse/MDEV-35955))
* A query using a subquery in form:

```sql
WHERE col IN (SELECT ... LEFT JOIN tbl ON tbl.column=reference_outside_subquery)
```

could cause a crash in the optimizer. The essential part is that ON expression has only two kinds of references: 1.to inner side of the outer join and 2. to outside the subquery. ([MDEV-32084](https://jira.mariadb.org/browse/MDEV-32084))

* find\_order\_in\_list mismatch when order item needs fixing() ([MDEV-36607](https://jira.mariadb.org/browse/MDEV-36607))
* If the join\_condition is specified via USING (column\_list), the query plan depends on the sequence of tables in the query ([MDEV-36592](https://jira.mariadb.org/browse/MDEV-36592))
* Large N-way OR causes a lot of index\_merge variants to be created and discarded ([MDEV-34620](https://jira.mariadb.org/browse/MDEV-34620))
* Wrong result in loose index scan ([MDEV-36118](https://jira.mariadb.org/browse/MDEV-36118))

### Data Definition - Alter Table

* Incorrect error handling on DDL with FULLTEXT INDEX ([MDEV-36061](https://jira.mariadb.org/browse/MDEV-36061))
* ALTER TABLE…SEQUENCE does not work correctly with InnoDB ([MDEV-36038](https://jira.mariadb.org/browse/MDEV-36038))
* The server could crash when an UPDATE is about to commit concurrently with a CREATE INDEX that includes VIRTUAL columns ([MDEV-36281](https://jira.mariadb.org/browse/MDEV-36281))
* ALTER TABLE…DROP COLUMN after a failed ALTER TABLE…DROP COLUMN could lead to a server crash ([MDEV-36236](https://jira.mariadb.org/browse/MDEV-36236))

### Backup

* mariadb-backup --backup crash during innodb\_undo\_log\_truncate=ON, innodb\_encrypt\_log=ON ([MDEV-36152](https://jira.mariadb.org/browse/MDEV-36152))
* MariaDB Backup returns with an error like "Error on file ./test/t1#P#p513.MYD open during `test`.`t1` table copy for partitioned MyISAM tables when running out of file handles ([MDEV-36437](https://jira.mariadb.org/browse/MDEV-36437))
* make mariadb-backup to force an innodb checkpoint ([MDEV-30000](https://jira.mariadb.org/browse/MDEV-30000))

### GIS

* Server aborts while deleting the record in spatial index ([MDEV-35420](https://jira.mariadb.org/browse/MDEV-35420))

### Upgrades

* Upgrades fail on Windows ([MDEV-36128](https://jira.mariadb.org/browse/MDEV-36128))

### OTHER

* Field pointer may be uninitialized in fill\_record ([MDEV-36181](https://jira.mariadb.org/browse/MDEV-36181))
* Wrong results from tables with a single record and an aggregate ([MDEV-35238](https://jira.mariadb.org/browse/MDEV-35238))

### Galera

* [Galera](https://app.gitbook.com/o/diTpXxF5WsbHqTReoBsS/s/3VYeeVGUV4AMqrA3zwy7/) updated to 26.4.22
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
* A Galera node may hang due to improper mutex handling: a thread held lock\_sys.wait\_mutex while triggering a streaming replication rollback, which also tried to acquire THD::LOCK\_thd\_kill, leading to incorrect mutex usage. In debug versions, this leads to diagnostics like "safe\_mutex: Found wrong usage of mutex 'wait\_mutex' and 'LOCK\_thd\_data'", but in both debug and release versions, there is some probability that the node may hang. ([MDEV-36509](https://jira.mariadb.org/browse/MDEV-36509))
* A Galera node might hang if foreign key (FK) and unique key (UK) checks are disabled on multiple appliers executing INSERTs into the same table, because InnoDB might treat these operations as bulk inserts, leading one applier to acquire a table-level lock. If another applier with a lower sequence number then waits for this lock, a deadlock can occur within Galera. Specifically, the lock holder waits for the earlier applier to commit, while the earlier applier is blocked by the lock. ([MDEV-36360](https://jira.mariadb.org/browse/MDEV-36360))

### Partitioning

* corruption when query cache cannot allocate block ([MDEV-34075](https://jira.mariadb.org/browse/MDEV-34075))

### Data Manipulation - Update

* Stack looping and SIGSEGV in Item\_args::walk\_args on UPDATE ([MDEV-31647](https://jira.mariadb.org/browse/MDEV-31647))

### Server

* Server crash in find\_field\_in\_tables, Assertion \`name' failed in find\_field\_in\_table\_ref ([MDEV-25012](https://jira.mariadb.org/browse/MDEV-25012))
* Server crash when inserting from derived table containing insert target table ([MDEV-32086](https://jira.mariadb.org/browse/MDEV-32086))
* MariaDB effectively running as root CAP\_DAC\_OVERRIDE ([MDEV-36229](https://jira.mariadb.org/browse/MDEV-36229))
* Build fails with cmake 4.0 ([MDEV-36506](https://jira.mariadb.org/browse/MDEV-36506))
* mysqldump does not preserve case of table names in generated sql ([MDEV-14432](https://jira.mariadb.org/browse/MDEV-14432))
* Incorrect result for BETWEEN over unique blob prefix ([MDEV-36235](https://jira.mariadb.org/browse/MDEV-36235))
* Incorrect query result for comparisons of binary\_column NOT LIKE binary\_column ([MDEV-36211](https://jira.mariadb.org/browse/MDEV-36211))

### Replication

* Semi-sync Replica Can't Kill Dump Thread When Using SSL ([MDEV-36663](https://jira.mariadb.org/browse/MDEV-36663))
* Mysqlbinlog --stop-position does not warn if EOF not reached with --read-from-remote-server ([MDEV-35694](https://jira.mariadb.org/browse/MDEV-35694))

### Plugin - Audit

* Long server\_audit\_file\_path causes buffer overflow ([MDEV-36245](https://jira.mariadb.org/browse/MDEV-36245))

### Configuration

* Bad value for the variable "Buffer pool size" ([MDEV-21203](https://jira.mariadb.org/browse/MDEV-21203))

### Packaging

* Error while installing MariaDB on Windows Server 2022 due to antivirus interference. ([MDEV-35983](https://jira.mariadb.org/browse/MDEV-35983))
* RHEL 8 (and compatible) + Ubuntu 20.04 cannot start systemd servce (EXIT\_CAPABILTIES/218) ([MDEV-36591](https://jira.mariadb.org/browse/MDEV-36591))

### JSON

* JSON\_UNQUOTE doesn't work with emojis ([MDEV-35614](https://jira.mariadb.org/browse/MDEV-35614))

### Security

* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2025-30722](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2025-30722)
  * [CVE-2025-30693](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2025-30693)
  * [CVE-2023-52970](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2023-52970)
  * [CVE-2023-52969](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2023-52969)
  * [CVE-2023-52971](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2023-52971)

## Changelog

For a complete list of changes made in [MariaDB 11.4.6](mariadb-11-4-6-release-notes.md), with links to detailed\
information on each push, see the [changelog](../changelogs/changelogs-mariadb-11-4-series/mariadb-11-4-6-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 11.4.6](mariadb-11-4-6-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-7-1-rc-and-mariadb-10-6-5-10-5-13-10-4-22-10-3-32-and-10-2-41-now-available/).

{% include "../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
