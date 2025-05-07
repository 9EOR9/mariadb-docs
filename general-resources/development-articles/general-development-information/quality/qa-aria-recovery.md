
# QA - Aria Recovery


## General Principles


Recovery is tested via the [RQG](https://github.com/RQG/RQG-Documentation/wiki/Category:RandomQueryGenerator), which provides a random workload against the
server, and then uses kill -9 to kill the process. After that, recovery is
attempted both by using `maria_read_log` and by restarting the `mysqld`
process. Once the server has started up, the tables are verified in various
ways, including `ALTER|OPTIMIZE|ANALYZE|REPAIR TABLE` as well `SELECT`
queries that read the table back and forth using various access methods.


A combinations `.CC` file named
`lp:randgen/conf/engines/maria/maria_recovery.cc` is used to define various
`mysql` options and RQG parameters that are relavant to recovery. Then, RQG's
`combinations.pl` script is used to run hundreds of individual test runs.
Each run uses a random permutation from the settings in the `.CC` file in
order to generate a unique workload that is then validated via the `Recovery`
RQG Reporter.


## Individual tests


The following are the individual tests or test runs that must be completed or
created in order to ensure that Aria recovery is solid.


### Standard kill -9 testing


**Done 2011-02-28** The standard `conf/engines/maria/maria_recovery.cc`
passes with no failures when run with hundreds of trials.


### Testing with small block sizes


On hold pending 2 bug fixes related to --maria-block-size=1K and
--maria-block-size=2K


### Testing with small page cache size


**Done 2011-03-04** Completed 400 rounds with


```
'--mysqld=--maria-block-size=4K --mysqld=--maria-pagecache-buffer-size=128K',
'--mysqld=--maria-block-size=16K --mysqld=--maria-pagecache-buffer-size=256K',
'--mysqld=--maria-block-size=32K --mysqld=--maria-pagecache-buffer-size=512K'
```

two pre-recovery crashes were filed, no recovery issues.


### Killing and restarting the recovery process itself


**In Progress**


The AriaDoubleRecovery reporter currently attempts doble recovery via
maria_read_log. The first invocation of maria_read_log is killed halfway
through the process and the second invocation is left to complete the recovery.


Future testing will involve doing the same with the mysqld server in place of
maria_read_log.


### Another realistic workload


The usefullness of the SMF workload, derived from the SimpleMachines forum
application means that another such workload is required in order to make sure
no residual recovery bugs remain. Hopefully something can be cooked up using
Wikipedia so that longer fields and blobs are exercised.


### Transactional consistency


A transactional grammar that simulates transactions using LOCK TABLEs is
required. The RecoveryConsistency Reporter can then be used to validate that no
partial transactions appear in the database after recovery.


## See also


* [RQG Performance Comparisons](benchmarks-and-long-running-tests/benchmarks/rqg-performance-comparisons.md)
* [RQG Extensions for MariaDB Features](rqg-extensions-for-mariadb.md)
* [Optimizer Quality](optimizer-quality.md)
* [QA Tools](qa-tools.md)
* [Worklog Quality Checklist Template](worklog-quality-checklist-template.md)


CC BY-SA / Gnu FDL

