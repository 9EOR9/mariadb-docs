# Information Schema ENABLED\_ROLES Table

The [Information Schema](../) `ENABLED_ROLES` table shows the enabled [roles](../../../../../../security/user-account-management/roles/) for the current session.

It contains the following column:

| Column     | Description                     |
| ---------- | ------------------------------- |
| Column     | Description                     |
| ROLE\_NAME | The enabled role name, or NULL. |

This table lists all roles that are currently enabled, one role per row — the current role, roles granted to the current role, roles granted to these roles and so on. If no role is set, the row contains a `NULL` value.

The roles that the current user can enable are listed in the [APPLICABLE\_ROLES](information-schema-applicable_roles-table.md) Information Schema table.

See also [CURRENT\_ROLE()](../../../../built-in-functions/secondary-functions/information-functions/current_role.md).

## Examples

```
SELECT * FROM information_schema.ENABLED_ROLES;
+-----------+
| ROLE_NAME |
+-----------+
| NULL      |
+-----------+

SET ROLE staff;

SELECT * FROM information_schema.ENABLED_ROLES;
+-----------+
| ROLE_NAME |
+-----------+
| staff     |
+-----------+
```

CC BY-SA / Gnu FDL
