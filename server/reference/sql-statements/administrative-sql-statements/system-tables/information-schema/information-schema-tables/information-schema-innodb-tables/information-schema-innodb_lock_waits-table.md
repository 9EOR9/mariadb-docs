# Information Schema INNODB\_LOCK\_WAITS Table

The [Information Schema](../../) `INNODB_LOCK_WAITS` table contains information about blocked InnoDB transactions. The `PROCESS` [privilege](../../../../../account-management-sql-statements/grant.md) is required to view the table.

It contains the following columns:

| Column              | Description                                                                                                                                           |
| ------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| Column              | Description                                                                                                                                           |
| REQUESTING\_TRX\_ID | Requesting transaction ID from the [INNODB\_TRX](information-schema-innodb_trx-table.md) table.                                                       |
| REQUESTED\_LOCK\_ID | Lock ID from the [INNODB.LOCKS](information-schema-innodb_locks-table.md) table for the waiting transaction.                                          |
| BLOCKING\_TRX\_ID   | Blocking transaction ID from the [INNODB\_TRX](information-schema-innodb_trx-table.md) table.                                                         |
| BLOCKING\_LOCK\_ID  | Lock ID from the [INNODB.LOCKS](information-schema-innodb_locks-table.md) table of a lock held by a transaction that is blocking another transaction. |

The table is often used in conjunction with the [INNODB\_LOCKS](information-schema-innodb_locks-table.md) and [INNODB\_TRX](information-schema-innodb_trx-table.md) tables to diagnose problematic locks and transactions.

CC BY-SA / Gnu FDL

{% @marketo/form formId="4316" %}
