# Indexes

- Primary mechanism to get improved performance on a database
- Persistent data structure, stores in database
- Indexes are not accessible, they are used underneath the query execution
- Indexes can give you orders of magnitude of performance improvements by immediate locating tuples instead of scanning the full table to find them
- Build indexes on attributes that are going to be used frequently
- There are 2 main kinds of indexes structures:
    - Balance trees (for inequality conditions or equality conditions)
    - Hashtables (for equality conditions)
- Many DBMS build indexes automatically on Primary Key attributes
- Downsides of Indexes:
    - Extra space (marginal downside)
    - Index creation (medium downside) — takes a fair amount of time
    - Index maintenance — every time the table is updated, the indexes need to be maintained, and this can be costly if happens a lot. Indexes can be harmful if the table receives more updates then queries
- Benefits of an index depends on:
    - Size of the table
    - Data distributions
    - Query vs Update
- Physical Design Advisors: system that tells you which indexes to build in your database. It takes as input: database statistics and workload
    - It is based on the Query Optimizer (built-in component of most DBMSs)
- SQL to create indexes:

    ```jsx
    Create Index IndexName on T(A);
    Create Index IndexName on T(A1, A2, ..., AN);
    Create Unique Index IndexName on T(A);
    Drop Index IndexName;
    ```

    - The Unique reinforces uniqueness