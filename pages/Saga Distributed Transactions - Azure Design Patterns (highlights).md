title:: Saga Distributed Transactions - Azure Design Patterns (highlights)
author:: [[docs.microsoft.com]]
full-title:: "Saga Distributed Transactions - Azure Design Patterns"
category:: #articles
url:: https://docs.microsoft.com/en-us/azure/architecture/reference-architectures/saga/saga

- Highlights first synced by [[Readwise]] [[Nov 18th, 2022]]
	- A transaction is a single unit of logic or work, sometimes made up of multiple operations
	- Transactions must be atomic, consistent, isolated, and durable (ACID)
	- Compensable transactions are transactions that can potentially be reversed by processing another transaction with the opposite effect.
	  A pivot transaction is the go/no-go point in a saga. If the pivot transaction commits, the saga runs until completion. A pivot transaction can be a transaction that is neither compensable nor retryable, or it can be the last compensable transaction or the first retryable transaction in the saga.
	  Retryable transactions are transactions that follow the pivot transaction and are guaranteed to succeed.