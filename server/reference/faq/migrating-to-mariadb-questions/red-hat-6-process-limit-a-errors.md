
# Red Hat 6 Process Limit a Errors

When upgrading from MySQL 5.1 to [MariaDB 5.5](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-5-series/changes-improvements-in-mariadb-5-5) you may encounter a process limit problem with your MariaDB installation. This is not MariaDB at fault. The issue is likely triggered with high connection counts to the database and possibly exacerbated by not using [Thread pooling](../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/buffers-caches-and-threads/thread-pool/thread-pool-in-mariadb.md).


You might encounter the following error message if you are not out of available memory:


```
##SQLSTATE[HY000] [1135] Can't create a new thread (errno 11);##
```

You can consult the manual for a possible OS-dependent bug when trying to connect. There is a very good explanation and troubleshooting with a work around on the Percona [MySQL Performance Blog](https://www.mysqlperformanceblog.com/2013/02/04/cant_create_thread_errno_11/)


Review your connections and thread consumption usage prior to doing an upgrade to avoid this being a problem.

