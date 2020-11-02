# ADR11. Stateful store for Customer -> Replayable Log -> Purchase Service

## STATUS
Accepted

## DESCRIPTION
Right after purchasing an item, the replayable log has to load Customer information to fill some data in Purchase services and identify who purchased and eventually understand better the customer actions.

## DECISION
Loading customer information in some state store provides low latency to enrich data coming from a replayable log and it increases the throughput because the latency reduces and there is no round trip to the customer service.

## CONSEQUENCES
Increases the memory footprint because customer information has to be loaded in a Stateful state store. In case it is out, it is needed to reload all the information back to the state store.