# Join

## Inner Join On condition
    - Example:

        ```sql
        SELECT x, y 
        FROM table_a 
        JOIN table_b
        ON table_a.x_id = table_b.y_id
        ```

## Natural Join
takes 2 relations that have column names in common and only keeps the values that have matching values. This removes the ambiguity of columns with same name (only one column with matching values between the relations is included in the result)
- Example:

    ```sql
    SELECT *
    FROM table_a
    NATURAL JOIN table_b
    USING (column_x)
    ```

## Inner Join Using(attrs
The USING clause is optional but it is a good practice as it makes more explicit which column(s) is (are) being used to join the tables. The value in the USING argument need to be a column present in both tables. You can't use USING and ON in the same query. Example:
- Example:

    ```sql
    SELECT *
    FROM table_a
    JOIN table_b
    USING (column_x);
    ```

## Left/Right/Full Outer Join
### Left Outer Join
Takes any tuples in the table of the left and have no values in the right table and adds them to the result with NULL values
- Example:

    ```sql
    SELECT x, y, z
    FROM table_a LEFT OUTER JOIN table_b;
    ```

### Right Outer Join
It is the same as the Left Outer Join swapping the tables

### Full Outer Join
Includes unmatched values from both left and right
- Example:

    ```sql
    SELECT x, y, z
    FROM table_a FULL OUTER JOIN table_b;
    ```

## Union
You can use the union operator to add more rows to your query