# Constraints

Constraints: aka Integrity Constraints, they constrain allowable database states. [Static]

- Restrictions on allowable data in the database, beyond those imposed by structure and types
- Example: Limit value to a range
- Use cases:
    - Data-entry errors (inserts)
    - Correctness criteria (updates)
    - Enforce consistency
    - Tell system about data
- Types of Constraints:
    - Non-null constraint
    - Key constraint (unique values)
    - Referential Integrity (aka, Foreign Key constraint)
    - Attribute-based contraint
    - Tuple-based constraint
    - General assertions
- Constraint Declaration
    - With original schema - checked after bulk load
    - Or later - checked on current DB
- Constraint Enforcement
    - Check after every (dangerous) modification
        - Dangerous modifications: those that have the potential to violate the constraint
    - Deferred constraint checking (transaction)