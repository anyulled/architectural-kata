# ADR1.Data consistency in Purchase and Inventory

## STATUS
Accepted

## DESCRIPTION
The purchase and inventory even being separated services, they share the same data model. 
The inventory uses the followers of the write leader to show the current state of each item whereas the purchase is the one who writes to the database. 
They work such as a CQRS (Command Query Responsibility Segregation). Because purchases can be made online or in POS we need to ensure the consistency and integrity of each product in database.

## DECISION
We decided to use relational database because it provides ACID properties and it avoids us to managing concurrency in service layer (programmatically).

## CONSEQUENCES
We will need to use configuration services and cluster proxy layers who knows the database server location. 
They will increase the complexity during eventual maintanability because Relational Database does not have an already embedded configuration service, such as NOSQL system do have, for example.
