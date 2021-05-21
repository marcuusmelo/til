# Select

## The Form:
``` sql
SELECT attribute_1, ..., attribute_n FROM relation_1, ..., relation_n WHERE conditions
```
The result is a table (aka, relation)

## Some Features of the Select
- You can select data from multiple tables just by adding multiple tables in the FROM clause
- You can use a join condition inside the WHERE clause when you select from multiple tables
- SQL is an unordered model, you can run the same query 2 times and get the result in different order. You can use the ORDER BY clause to sort the results in a particular way.