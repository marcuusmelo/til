# Relational Model

- A database consists of a set of relations or sometimes referred to as "tables", each of which has a name.
- Typically each attribute or column has a type (integer, float, datetime, etc.)
- Schema — structural description of relations in database
- Instance — actual contents at given point in time
- NULL — special value for unknown or undefined
    - When querying a database and filtering a column with NULL value, keep in mind that this value is unknown, so if you try things like "> X", "< X" or even "> X or < X", the instances with NULL will always be out. Ordering is also weird.
- Key — attribute (column) whose value is unique in each tuple (instance or row)
    - A key can be formed by a combination of more than one attribute
- Creating relations (tables) in SQL:

```sql
CREATE TABLE table_name(attribute_1, attribute_2, attribute_3)

-- or, with attribute types

CREATE TABLE table_name(attribute_1 datetime, attribute_2 integer)
```