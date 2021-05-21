# Transactions

- Motivations:
    - Concurrent db access
    - Resilience
- When multiple clients are modifying the same db at the same time working at the same attribute, unexpected results could happen.
- Concurrency Goal: execute a sequence of SQL statements so they appear to be running in isolation.
- Concurrency is wanted when possible for performance optimization
- System-Failure goal: guarantee all-or-nothing execution, regardless of failures
- Solution for both CONCURRENCY and FAILURES: TRANSACTIONS
- A transaction is a sequence of one or more SQL operations treated as a unit
    - Appear to run in isolation
    - If the system fails, each transaction's changes are reflected either entirely or not at all
- Transaction standards:
    - A transaction begins automatically on first SQL statement
    - On `commit` transaction ends and new one begins
    - Current transaction ends on session termination
    - `Autocommit` turns each statement into transaction