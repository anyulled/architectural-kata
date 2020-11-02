# ADR4. Shared Database (Inventory and Purchase)

## STATUS
Accepted

## DESCRIPTION
The system is expected to write up to 10 thousand purchases along weekdays in 2021, so the CQRS(Command Query Responsibility Segregation) is done automatically (out of box) by the Chosen Leader Follower Relational Database, 
having the Inventory reading from the followers and the Purchasing writing to the database.

## DECISION
The idea behing a shared database is because of the writing level being too low, about 10 thousand purchases along weekdays. 
Diluted along the lunchtime and dinner time it is bearable easily by the Back End (and shared database). 
So the replica (follower) is read by the Inventory who keeps the consistency based on the ACID properties using this shared database. 

## CONSEQUENCES
Scalability is reduced in order to provide Consistency. 

## COMPLIANCE
The performance will be verified from time to time through fitness functions (tests). 
