# Condition Pushdown into Derived Table Optimization

If a query uses a derived table (or a view), the first action that the query optimizer will attempt is to apply the [derived-table-merge-optimization](derived-table-merge-optimization.md) and merge the derived table into its parent select. However, that optimization is only applicable when the select inside the derived table has a join as the top-level operation. If it has a [GROUP-BY](../../../../reference/sql-statements/data-manipulation/selecting-data/group-by.md), [DISTINCT](../../../../reference/sql-statements/data-manipulation/selecting-data/select.md#distinct), or uses [window functions](../../../../reference/sql-functions/special-functions/window-functions/), then [derived-table-merge-optimization](derived-table-merge-optimization.md) is not applicable.

In that case, the Condition Pushdown optimization is applicable.

## Introduction to Condition Pushdown

Consider an example

```sql
create view OCT_TOTALS as
select
  customer_id,
  SUM(amount) as TOTAL_AMT
from orders
where  order_date BETWEEN '2017-10-01' and '2017-10-31'
group by customer_id;

select * from OCT_TOTALS where customer_id=1
```

The naive way to execute the above is to

1. Compute the OCT\_TOTALS contents (for all customers).
2. The, select the line with customer\_id=1

This is obviously inefficient, if there are 1000 customers, then one will be doing up to 1000 times more work than necessary.

However, the optimizer can take the condition `customer_id=1` and push it down into the OCT\_TOTALS view.

(TODO: elaborate here)

## Condition Pushdown Properties

* Condition Pushdown has been available since [MariaDB 10.2](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/what-is-mariadb-102).
* The Jira task for it was [MDEV-9197](https://jira.mariadb.org/browse/MDEV-9197).
* The optimization is enabled by default. One can disable it by setting `@@optimizer_switch` flag `condition_pushdown_for_derived` to OFF.

## See Also

* Condition Pushdown through Window Functions (since [MariaDB 10.3](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-3-series/what-is-mariadb-103))
* [Condition Pushdown into IN Subqueries](../subquery-optimizations/condition-pushdown-into-in-subqueries.md) (since [MariaDB 10.4](broken-reference))

CC BY-SA / Gnu FDL

{% @marketo/form formId="4316" %}
