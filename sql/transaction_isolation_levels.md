# Transaction Isolation Levels

- The isolation level is set per transaction
- Isolation Levels are specific to Reads

## How to set isolation levels:

```sql
SET TRANSACTION ISOLATION LEVEL {ISOLATION_LEVEL_NAME};
```

- Dirty Reads: The transaction can read dirty items
    - Dirty data item: written by a different uncommitted transactions (not the same transaction as the read)


## Types of Transaction Isolation Levels
### Read Uncommitted Isolation Level
- Dirty reads are allowed
- This isolation level is used when the consistency is not very important. This also leads to increased concurrency, decreased overhead and better performance overall
### Read Committed Isolation Level
- A transaction may not perform dirty reads
- Does not guarantee global serializability (independency of the order of the execution of the concurrent transactions)

### Repeatable Read Isolation Level
- A transaction may not perform dirty reads
- An item read multiple times cannot change value
- A relation can change when adding rows — aka phantom tuples. Deletion of rows cannot happen
- Does not guarantee global serializability (independency of the order of the execution of the concurrent transactions)
- Default for oracle and mysql


### Serializable Isolation Level
- No dirty reads
- No nonrepeatable reads
- No phantom tuples
- Default for postgres and some others


## Bonus: Read Only Transactions
    - Independent to Isolation Levels
    - Helps system optimize performance