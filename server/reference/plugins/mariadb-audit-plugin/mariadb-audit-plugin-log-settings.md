
# MariaDB Audit Plugin - Log Settings

Events that are logged by the MariaDB Audit Plugin are grouped generally into different types: connect, query, and table events. To log based on these types of events, set the variable, [server_audit_events](mariadb-audit-plugin-options-and-system-variables.md) to `CONNECT`, `QUERY`, or `TABLE`. To have the Audit Plugin log more than one type of event, put them in a comma-separated list like so:


```
SET GLOBAL server_audit_events = 'CONNECT,QUERY,TABLE';
```

You can put the equivalent of this in the configuration file like so:


```
[mysqld]
...
server_audit_events=connect,query
```

By default, logging is set to `OFF`. To enable it, set the [server_audit_logging](mariadb-audit-plugin-options-and-system-variables.md) variable to `ON`. Note that if the [query cache](../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/buffers-caches-and-threads/query-cache.md) is enabled, and a query is returned from the query cache, no `TABLE` records will appear in the log since the server didn't open or access any tables and instead relied on the cached results. So you may want to disable query caching.


There are actually a few types of events that may be logged, not just the three common ones mentioned above. A full list of related system variables is detailed on the [Server_Audit System Variables](mariadb-audit-plugin-options-and-system-variables.md) page, and status variables on the [Server_Audit Status Variables](mariadb-audit-plugin-status-variables.md) page of this documentation. Some of the major ones are highlighted below:



| Type | Description |
| --- | --- |
| Type | Description |
| CONNECT | Connects, disconnects and failed connects—including the error code |  |
| QUERY | Queries executed and their results in plain text, including failed queries due to syntax or permission errors |  |
| TABLE | Tables affected by query execution |  |
| QUERY_DDL | Similar to QUERY, but filters only DDL-type queries (CREATE, ALTER, DROP, RENAME and TRUNCATE). There are some exceptions however. RENAME USER is not logged, while CREATE/DROP [PROCEDURE / FUNCTION / USER] are only logged from [MariaDB 10.2.38](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/mariadb-10238-release-notes), [MariaDB 10.3.29](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-3-series/mariadb-10329-release-notes), [MariaDB 10.4.22](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/mariadb-10422-release-notes), [MariaDB 10.5.13](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/release-notes-mariadb-10-5-series/mariadb-10513-release-notes) and [MariaDB 10.6.5](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/release-notes-mariadb-10-6-series/mariadb-1065-release-notes). In earlier versions they are not logged. See [MDEV-23457](https://jira.mariadb.org/browse/MDEV-23457). |
| QUERY_DML | Similar to QUERY, but filters only DML-type queries (DO, CALL, LOAD DATA/XML, DELETE, INSERT, SELECT, UPDATE, HANDLER and REPLACE statements) |
| QUERY_DML_NO_SELECT | Similar to QUERY_DML, but doesn't log SELECT queries. (since version 1.4.4) (DO, CALL, LOAD DATA/XML, DELETE, INSERT, UPDATE, HANDLER and REPLACE statements) |
| QUERY_DCL | Similar to QUERY, but filters only DCL-type queries (CREATE USER, DROP USER, RENAME USER, GRANT, REVOKE and SET PASSWORD statements) |



Since there are other types of queries besides DDL and DML, using the `QUERY_DDL` and `QUERY_DML` options together is not equivalent to using `QUERY`. Starting in version 1.3.0 of the Audit Plugin, there is the `QUERY_DCL` option for logging DCL types of queries (e.g., `GRANT` and `REVOKE` statements). In the same version, the [server_audit_query_log_limit](mariadb-audit-plugin-options-and-system-variables.md) variable was added to be able to set the length of a log record. Previously, a log entry would be truncated due to long query strings.


## Logging Connect Events


If the Audit Plugin has been configured to log connect events, it will log connects, disconnects, and failed connects. For a failed connection, the log includes the error code.


It's possible to define a list of users for which events can be excluded or included for tracing their database activities. This list will be ignored, though, for the loggings of connect events. This is because auditing standards distinguish between technical and physical users. Connects need to be logged for all types of users; access to objects need to be logged only for physical users.


## Logging Query Events


If `QUERY`, `QUERY_DDL`, `QUERY_DML`, `QUERY_DML_NO_SELECT`, and/or `QUERY_DCL` event types are enabled, then the corresponding types of queries that are executed will be logged for defined users. The queries will be logged exactly as they are executed, in plain text. This is a security vulnerability: anyone who has access to the log files will be able to read the queries. So make sure that only trusted users have access to the log files and that the files are in a protected location. An alternative is to use `TABLE` event type instead of the query-related event types.


Queries are also logged if they cannot be executed, if they're unsuccessful. For example, a query will be logged because of a syntax error or because the user doesn't have the privileges necessary to access an object. These queries can be parsed by the error code that's provided in the log.


You may find failed queries to be more interesting: They can reveal problems with applications (e.g., an SQL statement in an application that doesn't match the current schema). They can also reveal if a malicious user is guessing at the names of tables and columns to try to get access to data.


Below is an example in which a user attempts to execute an `UPDATE` statement on a table for which he does not have permission:


```
UPDATE employees 
SET salary = salary * 1.2 
WHERE emp_id = 18236;

ERROR 1142 (42000): 
UPDATE command denied to user 'bob'@'localhost' for table 'employees'
```

Looking in the Audit Plugin log (`server_audit.log`) for this entry, you can see the following entry:


```
20170817 11:07:18,ip-172-30-0-38,bob,localhost,15,46,QUERY,company,
'UPDATE employees SET salary = salary * 1.2 WHERE emp_id = 18236',1142
```

This log entry would be on one line, but it's reformatted here for better rendering. Looking at this log entry, you can see the date and time of the query, followed by the server host, the user and host for the account. Next is the connection and query identification numbers (i.e., `15` and `46`). After the log event type (i.e., `QUERY`), the database name (i.e., `company`), the query, and the error number is recorded.


Notice that the last value in the log entry is `1142`. That's the error number for the query. To find failed queries, you would look for two elements: the notation indicating that it's a `QUERY` entry, and the last value for the entry. If the query is successful, the value will be `0`.


### Queries Not Included in Subordinate Query Event Types


Note that the `QUERY` event type will log queries that are not included in any of the subordinate `QUERY_*` event types, such as:


* CREATE FUNCTION
* DROP FUNCTION
* CREATE PROCEDURE
* DROP PROCEDURE
* SET
* CHANGE MASTER TO
* FLUSH
* KILL
* CHECK
* OPTIMIZE
* LOCK
* UNLOCK
* ANALYZE
* INSTALL PLUGIN
* UNINSTALL PLUGIN
* INSTALL SONAME
* UNINSTALL SONAME
* EXPLAIN


## Logging Table Events


MariaDB has the ability to record table events in the logs—this is not a feature of MySQL. This feature is the only way to log which tables have been accessed through a view, a stored procedure, a stored function, or a trigger. Without this feature, a log entry for a query shows only the view, stored procedure or function used, not the underlying tables. Of course, you could create a custom application to parse each query executed to find the SQL statements used and the tables accessed, but that would be a drain on system resources. Table event logging is much simpler: it adds a line to the log for each table accessed, without any parsing. It includes notes as to whether it was a read or a write.


If you want to monitor user access to specific databases or tables (e.g., `mysql.user`), you can search the log for them. Then if you want to see a query which accessed a certain table, the audit log entry will include the query identificaiton number. You can use it to search the same log for the query entry. This can be useful when searching a log containing tens of thousands of entries.


Because of the `TABLE` option, you may disable query logging and still know who accessed which tables. You might want to disable `QUERY` event logging to prevent sensitive data from being logged. Since *table* event logging will log who accessed which table, you can still watch for malicious activities with the log. This is often enough to fulfill auditing requirements.


Below is an example with both `TABLE` and `QUERY` events logging. For this scenario, suppose there is a [VIEW](../../../server-usage/programming-customizing-mariadb/views/create-view.md) in which columns are selected from a few tables in a `company` database. The underlying tables are related to sensitive employee information, in particular salaries. Although we may have taken precautions to ensure that only certain user accounts have access to those tables, we will monitor the Audit Plugin logs for anyone who queries them—directly or indirectly through a view.


```
20170817 16:04:33,ip-172-30-0-38,root,localhost,29,913,READ,company,employees,
20170817 16:04:33,ip-172-30-0-38,root,localhost,29,913,READ,company,employees_salaries,
20170817 16:04:33,ip-172-30-0-38,root,localhost,29,913,READ,company,ref_job_titles,
20170817 16:04:33,ip-172-30-0-38,root,localhost,29,913,READ,company,org_departments,
20170817 16:04:33,ip-172-30-0-38,root,localhost,29,913,QUERY,company,
'SELECT * FROM employee_pay WHERE title LIKE \'%Executive%\'  OR title LIKE \'%Manager%\'',0
```

Although the user executed only one [SELECT](../../sql-statements-and-structure/sql-statements/data-manipulation/selecting-data/select.md) statement, there are multiple entries to the log: one for each table accessed and one entry for the query on the view, (i.e., `employee_pay`). We know primarily this is all for one query because they all have the same connection and query identification numbers (i.e., `29` and `913`).


## Logging User Activities


The Audit Plugin will log the database activities of all users, or only the users that you specify. A database activity is defined as a *query* event or a *table* event. *Connect* events are logged for all users.


You may specify users to include in the log with the `server_audit_incl_users` variable or exclude users with the `server_audit_excl_users` variable. This can be useful if you would like to log entries, but are not interested in entries from trusted applications and would like to exclude them from the logs.


You would typically use either the `server_audit_incl_users` variable or the `server_audit_excl_users` variable. You may, though, use both variables. If a username is inadvertently listed in both variables, database activities for that user will be logged because `server_audit_incl_users` takes priority.


Although MariaDB considers a user as the combination of the username and hostname, the Audit Plugin logs only based on the username. MariaDB uses both the username and hostname so as to grant privileges relevant to the location of the user. Privileges are not relevant though for tracing the access to database objects. The host name is still recorded in the log, but logging is not determined based on that information.


The following example shows how to add a new username to the `server_audit_incl_users` variable without removing previous usernames:


```
SET GLOBAL server_audit_incl_users = CONCAT(@@global.server_audit_incl_users, ',Maria');
```

Remember to add also any new users to be included in the logs to the same variable in MariaDB configuration file. Otherwise, when the server restarts it will discard the setting.


## Excluding or Including Users


By default events from all users are logged, but certain users can be excluded from logging by using the [server_audit_excl_users](mariadb-audit-plugin-options-and-system-variables.md) variable. For example, to exclude users *valerianus* and *rocky* from having their events logged:


```
server_audit_excl_users=valerianus,rocky
```

This option is primarily used to exclude the activities of trusted applications.


Alternatively, [server_audit_incl_users](mariadb-audit-plugin-options-and-system-variables.md) can be used to specifically include users. Both variables can be used, but if a user appears on both lists, [server_audit_incl_users](mariadb-audit-plugin-options-and-system-variables.md) has a higher priority, and their activities will be logged.


Note that `CONNECT` events are always logged for all users, regardless of these two settings. Logging is also based on username only, not the username and hostname combination that MariaDB uses to determine privileges.


CC BY-SA / Gnu FDL

