# ADR12. Configuration services for service discovery

## STATUS
Accepted

## DESCRIPTION
The system is expected to be highly available and thinking on that, the services need to be capable of finding each other anytime, even some being down, there will be a replica for it and has to be found.

## DECISION
Using configuration services as service discovery ensures the services/databases are found because they register themselves into the service discoveries (and a database uses a shard proxy for it).

## CONSEQUENCES
Maintainability, cost of running up more servers.