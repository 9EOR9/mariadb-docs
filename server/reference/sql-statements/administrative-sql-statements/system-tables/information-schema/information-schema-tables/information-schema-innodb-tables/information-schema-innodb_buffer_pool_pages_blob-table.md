# Information Schema INNODB\_BUFFER\_POOL\_PAGES\_BLOB Table

The [Information Schema](../../) `INNODB_BUFFER_POOL_PAGES_BLOB` table is a Percona enchancement, and is only available for XtraDB, not InnoDB (see [XtraDB and InnoDB](../../../../../../storage-engines/innodb/)). It contains information about [buffer pool](../../../../../../storage-engines/innodb/innodb-buffer-pool.md) blob pages.

It has the following columns:

| Column         | Description                                                                                                      |
| -------------- | ---------------------------------------------------------------------------------------------------------------- |
| Column         | Description                                                                                                      |
| SPACE\_ID      | Tablespace ID.                                                                                                   |
| PAGE\_NO       | Page offset within tablespace.                                                                                   |
| COMPRESSED     | 1 if the blob contains compressed data, 0 if not.                                                                |
| PART\_LEN      | Page data length.                                                                                                |
| NEXT\_PAGE\_NO | Next page number.                                                                                                |
| LRU\_POSITION  | Page position in the LRU (least-recently-used) list.                                                             |
| FIX\_COUNT     | Page reference count, incremented each time the page is accessed. 0 if the page is not currently being accessed. |
| FLUSH\_TYPE    | Flush type of the most recent flush.0 (LRU), 2 (flush\_list)                                                     |

CC BY-SA / Gnu FDL

{% @marketo/form formId="4316" %}
