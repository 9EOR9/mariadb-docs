
# Delayed Replication

The terms *master* and *slave* have historically been used in replication, and MariaDB has begun the process of adding *primary* and *replica* synonyms. The old terms will continue to be used to maintain backward compatibility - see [MDEV-18777](https://jira.mariadb.org/browse/MDEV-18777) to follow progress on this effort.


Delayed replication allows specifying that a replica should lag
behind the primary by (at least) a specified amount of time (specified in seconds). Before executing
an event, the replica will first wait, if necessary, until the given time has
passed since the event was created on the primary. The result is that the
replica will reflect the state of the primary some time back in the past.


The default is zero, or no delay, and the maximum value is 2147483647, or about 68 years.


Delayed replication is enabled using the MASTER_DELAY option to [CHANGE MASTER](../../../reference/sql-statements-and-structure/sql-statements/administrative-sql-statements/replication-statements/change-master-to.md):


```
CHANGE MASTER TO master_delay=3600;
```

A zero delay disables delayed replication. The replica must be stopped when changing the delay value.


## Fields in [SHOW SLAVE STATUS](../../../reference/sql-statements-and-structure/sql-statements/administrative-sql-statements/show/show-replica-status.md) are associated with delayed replication


1. `SQL_Delay`: This is the value specified by MASTER_DELAY in CHANGE MASTER
(or 0 if none).
1. `SQL_Remaining_Delay`: When the replica is delaying the execution of an event
due to MASTER_DELAY, this is the number of seconds of delay remaining before
the event will be applied. Otherwise, the value is NULL.
1. `Seconds_Behind_Master`:

  * If replication is not active, the value is NULL.
  * If all events has been executed and slave is now idle (waiting for new events), the value is 0.
  * If using parallel replication:

    * When starting to execute a new delayed event on an idle slave the value is `clock_time_on_slave - clock_when_started_execution_of_the_event_on_master - clock_difference_between_master_and_slave`
    * When event is committed the value is updated to: `clock_time_on_slave - clock_when_ending_execution_of_the_event_on_master - clock_difference_between_master_and_slave`
    * As Seconds_Behind_Master value depends on the timestamp of the last executed event, its value can be much bigger than SQL_Delay. For example if SQL_delay is 10 hours and the master sends a new event after not having executed anything for 20 hours, Seconds_behind_master will be 30 hours. When event starts to execute, Seconds_behind_master will still be growing until it commits. Then it will be changed to about 10 hours (more precisely to 10 hours + execution_time_on_slave - execution_time_on_master which corresponds to the above bullet). Since that the value will be growing until next event is executed and Seconds_behind_master is rebased on its completion time again.
To expand more on this check a practical example in the comments.
  * If not using parallel replication the value is updated when starting to execute an event. The value is set to: `clock_time_on_slave - clock_when_started_execution_of_the_event_on_master - clock_difference_between_master_and_slave`. Note that in this case the clock is at start of event, not at end of event like in parallel replication.
1. `Slave_SQL_Running_State`: This shows the state of the SQL driver threads,
same as in [SHOW PROCESSLIST](../../../reference/sql-statements-and-structure/sql-statements/administrative-sql-statements/show/show-processlist.md). When the replica is delaying the execution of an
event due to MASTER_DELAY, this fields displays: "Waiting until MASTER_DELAY
seconds after master executed event".


When using older versions prior to [MariaDB 10.2.3](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server/old-releases/release-notes-mariadb-10-2-series/mariadb-1023-release-notes), a 3rd party tool called [pt-slave-delay](https://www.percona.com/doc/percona-toolkit/LATEST/pt-slave-delay.html) can be used. It is part of the Percona Toolkit. Note that pt-slave-delay does not support MariaDB multi-channel replication syntax.


## clock_difference_between_master_and_slave


When setting up a master and slaves it is important that the internal clock has the same
configuration. In almost all unix systems the internal clock is in UTC by default. On Windows system it may be in local time. This should be changed to be in UTC if one uses MariaDB with replication!


In addition to being in UTC, one should ensure that the clocks are synchronized. If not
properly synchronized, there is a gap between the values of the clocks between different machines. MariaDB replication takes this into account by comparing the master and slave clocks when the slave connects to the master. The difference is `clock_difference_between_master_and_slave`.

