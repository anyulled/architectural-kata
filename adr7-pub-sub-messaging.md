# ADR7. Async Pub/Sub msg POS 2 Purchase & Inventory

## STATUS
Pending

##DESCRIPTION
POS after a purchase must forward it with kiosk, customer and purchase information (3 items of type 2, and 4 of type 13) to the Inventory, 
which must update the service by using those information or querying the SF of that kiosk, and must also forward it to the Purchase service, which must store the purchase information in case the customer is not Anonymous (i.e. purchase happened phisycally and the customer doesn't have the account).
This could be done by exposing a REST endpoint in both Purchase and Inventory, using a single topic (pub/sub) or separate queues (p2p) for each service.

## DECISION
We'll not use REST endpoints because the POS doesn't need any information back from Inventory and Purchase if not eventually an acknowledge.
To not let Purchase have to skip all the messages with Anonyous customer we could use two separate p2p queues, however assuming.

## CONSEQUENCES
...

NOTE (CONCERNES)
When a customer buys online, Purchase should act as a proxy and forward the request to POS. 
In this situation, after the POS response, Purchase should be ready to both store the purchase information and send a message to Inventory, 
or should let POS to do the job and send the event to the Purchase itself and the Inventory through the queue?
