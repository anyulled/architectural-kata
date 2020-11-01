# ADR3. Replayable log when purchasing items

## STATUS
Accepted

## DESCRIPTION
As the system should store the correct ordering of the purchases, a replayable log could make the object achievable.

## DECISION
We will use replayable log in order to store the events and provide them as a source of truth (event-sourcing). 
The replayable log has enough information to generate different views, such as for example the Recommendation Service and the Purchase Service who operates over the purchased items.

## CONSEQUENCES
The trade offs are the response time of the purchasing confirmation, maintainability because of the additional tier and observability, because there is one more place to extract log from.
