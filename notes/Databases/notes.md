
►ACID Properties:

1. Atomicity: Transactions are indivisible units; they either fully succeed or completely fail.
2. Consistency: Each transaction must maintain the database's consistency.
3. Isolation: Transactions should execute independently without affecting each other.
4. Durability: Once a transaction is finalized, it must persist even through system failures.


https://redis.io/glossary/acid-transactions/

 ACID transactions guarantee that database operations are executed correctly, and if there is any kind of failure, the database can recover to a previous state without losing any data or impacting the consistency of the data. In other words, ACID transactions provide a high level of assurance that database transactions will be processed reliably and that data will be stored accurately and consistently.

 Property	Responsibility for maintaining properties
Atomicity	Transaction Manager
Consistency	Application programmer
Isolation	Concurrency Control Manager
Durability	Recovery Manager

