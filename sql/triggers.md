# Triggers


Triggers: monitor database changes, check conditions and initiate actions. [Dynamic]

- When event occurs, check conditions; if true, do action
- Use cases:
    - Move monitoring logic from apps into DBMS
    - Enforce constraints
        - More compreensive
        - Constraint repair logic: not only reject invalid (as regular constraints do) but can also fixe and insert a valid version

## Triggers in SQL
    ```sql
    CREATE TRIGGER trigger_name BEFORE|AFTER|INSTEAD OF
    events WHEN (condition) action
    ```