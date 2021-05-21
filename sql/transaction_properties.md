# Transaction Properties

## ACID Properties of Transactions
- atomicity
- consistency
- isolation
- durability

## Isolation
transactions are isolated from one another
- Serializability: operations may be interleaved, but execution must be equivalent to some sequential (serial) order of all transactions


## Durability
If the system crashes after transaction commits, all effects of the transaction remain in database. (Based on logging)


## Atomicity
an atomic transaction is an indivisible and irreducible series of database operations such that either all occurs, or nothing occurs
- Transactions are atomic (all or nothing)
- Transaction Rollback (=Abort)
    - Undoes partial effects of transaction
    - Can be initiated by the system or the client
- Transactions use a Locking mechanism, which can block other users from part of the database


## Consistency
refers to the requirement that any given database transaction must change affected data only in allowed ways