# ADR8. REST Communication between web services and third party devices

## STATUS
Accepted

## DESCRIPTION
The system is expected to be interoperable among all the devices who have access to the internet through a web browser or the application (farmacy food) itself. 
Regarding that, due to its high level of interoperability the REST architectural style (running over HTTP) has been chosen to be responsible for exposing the public APIs for web customers.

## DECISION
Because of the need to have the system accessed and implemented in different manner (mobile applications, web, etc) the interoperability provided by REST architectural style with json/xml as published language is achieved. 
Besides that REST APIs also are scalable and flexible.

## CONSEQUENCES
You do not have the ability to maintain the state, such as sessions.