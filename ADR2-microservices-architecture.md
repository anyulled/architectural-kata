# ADR2.Use micro services architecture

## STATUS
Accepted

## DESCRIPTION
The current systems consists of several Kiosks on Detroit, which are pairs of Smart Fridges (SFs) and Toast Point Of Sales (POSs),
being them two separate service ecosystems, however they'll expand across Michigan, Ohio, and Illinois
to hopefully dozens of Kiosks.
The basic architecture is therefore a set of service which we'll have to integrate through our solution
by means of reading SF APIs, reading and writing POS APIs:
in practice, microservices architecture is not a choice but the facts on the ground.

## DECISION
Following the initial architecture we've implemented our solution
in other microservices by main functions: Inventory, Purchase, Feedback, Survey, Recommendation.

## CONSEQUENCES
Microservices come with a set of well-known cons,
like poor performances (communication latency, message processing) or harder to test and monitor because of the complexity.
They also come with a set of well-known pros, like to be ready to the cloud, better fault tolerance, better scalability.
We'll leverage the versatility of microservices architecture applying decision to achieve quality attributes
the global solution needs (scalability, elasticity, high availability, reliability).
