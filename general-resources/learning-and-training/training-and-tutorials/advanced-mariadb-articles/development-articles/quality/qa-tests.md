
# QA Tests


## Optimizer and the Random Query Generator


The RQG is used to test various Optimizer features. See the [Optimizer Quality](optimizer-quality.md) article for more information.


## Aria Engine Recovery


The [QA - Aria Recovery](qa-aria-recovery.md) page contains a plan on how to test it.


## Upgrade and Installer Testing


* Upgrades using .deb and RPM packages are tested using very simple tests in
 BuildBot by the various `bld_kvm*` builders.


### TODO:


* More complex tests around .deb, RPM and tarballs;
* Decide on specific upgrade/downgrade paths (e.g. MySQL 5.5 to [MariaDB 2.2](https://mariadb.com/kb/en/what-is-mariadb-22/)?)
 and methods (mysqldump, mysql_upgrade) that we support and test each
 individually;
* Test the Windows installer and service NSIS allows for scripted unattended
 installs by providing an `/SD` argument to functions such
 as `MessageBox`.
* Test the contents of the Windows package, e.g. if HELP, .test, etc. files are
 properly placed and runnable;


## Linking Testing


The purpose of those tests is to check that various applications that use
`libmysql` can be compiled, linked and run with MariaDB. They are run by the
`compile-connectors` builder in BuildBot


* Perl DBD::mysql

  * We configure and compile the Perl DBI MySQL driver. Then we run the test suite provided with it.
* PHP

  * We configure and compile both the `mysql` and `mysqli` PHP drivers
 without mysql-nd. For each, we run those tests from the PHP test suite
 that are known to be good (other tests fail for both MySQL and MariaDB).


### TODO:


* Perl and PHP with the embedded library


## Connectors Testing


The purpose of those tests is to check that the libraries that implement the
MySQL protocol can work with MariaDB.


* The `libmysql` library/connector is tested both by the MTR test suite
 (since `mysqltest` links with it)


### TODO:


* PHP with the mysql-nd driver
* Connector C++
* JDBC


## Replication Testing


Individual applications:


* group commit:
```
perl runall.pl \
 --engine=InnoDB \
 --grammar=conf/replication/rpl_transactions.yy \
 --gendata=conf/replication/rpl_transactions.zz \
 --mysqld=--sync_binlog=1 \
 --mysqld=--innodb-flush_log_at_trx_commit=1 \
 --mysqld=--binlog-dbug_fsync_sleep=100000 \
 --mysqld=--default-storage-engine=InnoDB \
 --threads=15 \
 --queries=1M \
 --duration=600 \
 --validator=None
```

