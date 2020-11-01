# ADR6. UDP Protocol between monitoring system and services

## STATUS
Accepted

## DESCRIPTION
In order to have a better latency while performing the services telemetry, the UDP (User Diagram Procol) has been chosen rather than the TCP (transmission control protocol)

## DECISION
As the log metric is not that crtictical as some business event, all the telemetry generated from the services will run over UDP protocol. 
Some packet loose is acceptable in order to provide better latency during this round-trip between the monitoring system and the services.

## CONSEQUENCES
Some packet loose because there is no guarantee in the packet delivery.
