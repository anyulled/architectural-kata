ADR14. Operational reuse with the sidecar pattern

## STATUS
Accepted

## DESCRIPTION
we need a mechanism for handling service-to-service communication in order to make it visible, manageable, and controlled. 

## DECISION
We apply the sidecar pattern as an implementation of service mesh to guarantee orthogonal operation on microservices on logging, monitoring, circuit breaker, fault tolerance. 
Service meshes provide visibility, resiliency, traffic, and security control of distributed application services.

## CONSEQUENCES
A general rule is defined and implemented in all microservices. Easy to maintain