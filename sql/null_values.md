# NULL Values

- SELECT DISTINCT column_x FROM table_1 shows the NULL as one of the results, but SELECT COUNT(DISTINCT column_x) FROM table_1 does not count the NULL value.
- NULL is not > nor < nor = to any number. So a query like SELECT * FROM table_1 WHERE x > 10 or X ≤ 10 will exclude the rows where X is NULL, if any