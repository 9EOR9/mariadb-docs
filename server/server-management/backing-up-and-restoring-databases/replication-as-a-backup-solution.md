# Replication as a Backup Solution

[Replication](broken-reference) can be used to support the [backup](./) strategy.

Replication alone is _not_ sufficient for backup. It assists in protecting against hardware failure on the primary server, but does not protect against data loss. An accidental or malicious `DROP DATABASE` or `TRUNCATE TABLE` statement will be replicated onto the replica as well. Care needs to be taken to prevent data getting out of sync between the primary and the replica.

The terms _master_ and _slave_ have historically been used in replication, and MariaDB has begun the process of adding _primary_ and _replica_ synonyms. The old terms will continue to be used to maintain backward compatibility - see [MDEV-18777](https://jira.mariadb.org/browse/MDEV-18777) to follow progress on this effort.

Replication is most commonly used to support backups as follows:

* A primary server replicates to a replica
* Backups are then run off the replica without any impact on the primary.

Backups can have a significant effect on a server, and a high-availability primary may not be able to be stopped, locked or simply handle the extra load of a backup. Running the backup from a replica has the advantage of being able to shutdown or lock the replica and perform a backup without any impact on the primary server.

Note that when backing up off a replica server, it is important to ensure that the servers keep the data in sync. See for example [Replication and Foreign Keys](../../ha-and-performance/standard-replication/replication-and-foreign-keys.md) for a situation when identical statements can result in different data on a replica and a primary.

## See Also

* [Replication](broken-reference)
* [Replication Compatibility](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/comparison/mariadb-vs-mysql-compatibility#replication-compatibility)
* [Backing Up and Restoring](./)

CC BY-SA / Gnu FDL
