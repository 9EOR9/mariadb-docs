# Information Schema APPLICABLE\_ROLES Table

The [Information Schema](../) `APPLICABLE_ROLES` table shows the [role authorizations](../../../../../../security/user-account-management/roles/) that the current user may use.

It contains the following columns:

| Column        | Description                                        | Added                                                                                                                                                         |
| ------------- | -------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Column        | Description                                        | Added                                                                                                                                                         |
| GRANTEE       | Account that the role was granted to.              |                                                                                                                                                               |
| ROLE\_NAME    | Name of the role.                                  |                                                                                                                                                               |
| IS\_GRANTABLE | Whether the role can be granted or not.            |                                                                                                                                                               |
| IS\_DEFAULT   | Whether the role is the user's default role or not | [MariaDB 10.1.3](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/community-server/old-releases/release-notes-mariadb-10-1-series/mariadb-10-1-3-release-notes) |

The current role is in the [ENABLED\_ROLES](information-schema-enabled_roles-table.md) Information Schema table.

## Example

```
SELECT * FROM information_schema.APPLICABLE_ROLES;
+----------------+-------------+--------------+------------+
| GRANTEE        | ROLE_NAME   | IS_GRANTABLE | IS_DEFAULT |
+----------------+-------------+--------------+------------+
| root@localhost | journalist  | YES          | NO         |
| root@localhost | staff       | YES          | NO         |
| root@localhost | dd          | YES          | NO         |
| root@localhost | dog         | YES          | NO         |
+----------------+-------------+--------------+------------+
```

CC BY-SA / Gnu FDL
