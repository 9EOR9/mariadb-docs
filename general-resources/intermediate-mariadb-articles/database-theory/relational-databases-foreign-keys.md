# Relational Databases: Foreign Keys

You already know that a relationship between two tables is created by assigning a common field to the two tables (see [Relational Databases: Table Keys](relational-databases-table-keys.md)). This common field must be a primary key to one table. Consider a relationship between a _customer_ table and a _sale_ table. The relationship is not much good if instead of using the primary key, _customer\_code_, in the _sale_ table, you use another field that is not unique, such as the customer's first name. You would be unlikely to know for sure which customer made the sale in that case. So, in the table below, _customer\_code_ is called the _foreign\_key_ in the _sale_ table; in other words, it is the primary key in a foreign table.

![setting\_foreign\_keys](../../.gitbook/assets/relational-databases-foreign-keys/+image/setting_foreign_keys.png)

Foreign keys allow for something called _referential integrity_. What this means is that if a foreign key contains a value, this value refers to an existing record in the related table. For example, take a look at the tables below:

### Lecturer table

| Code | First Name | Surname |
| ---- | ---------- | ------- |
| Code | First Name | Surname |
| 1    | Anne       | Cohen   |
| 2    | Leonard    | Clark   |
| 3    | Vusi       | Cave    |

### Course table

| Course Title                | Lecturer Code |
| --------------------------- | ------------- |
| Course Title                | Lecturer Code |
| Introduction to Programming | 1             |
| Information Systems         | 2             |
| Systems Software            | 3             |

Referential integrity exists here, as all the lecturers in the _course_ table exist in the _lecturer_ table. However, let's assume Anne Cohen leaves the institution, and you remove her from the lecturer table. In a situation where referential integrity is not enforced, she would be removed from the lecturer table, but not from the course table, as shown below:

### Lecturer table

| Code | First Name | Surname |
| ---- | ---------- | ------- |
| Code | First Name | Surname |
| 2    | Leonard    | Clark   |
| 3    | Vusi       | Cave    |

### Course table

| Course Title                | Lecturer Code |
| --------------------------- | ------------- |
| Course Title                | Lecturer Code |
| Introduction to Programming | 1             |
| Information Systems         | 2             |
| Systems Software            | 3             |

Now, when you look up who lectures _Introduction to Programming_, you are sent to a non-existent record. This is called poor data intregrity.

Foreign keys also allow _cascading_ deletes and updates. For example, if Anne Cohen leaves, taking the Introduction to Programming Course with her, all trace of her can be removed from both the _lecturer_ and _course_ table using one statement. The delete _cascades_ through the relevant tables, removing all relevant records.

Foreign keys can also contain null values, indicating that no relationship exists.

CC BY-SA / Gnu FDL
