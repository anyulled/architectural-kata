# ADR5. Caching (Write through) to store Inventory Information 

## STATUS
Accepted

## DESCRIPTION
As the system is accessed from the WEB through many devices(laptop, smartphone, etc), it requires a low latency in order to provide a better user experience.

## DECISION
The decision taken to reduce the latency from the web to the application and increase the throughput is by using a Cache in write-through mode.

## CONSEQUENCES
Write-through mode increases the writing time operation (two writes, database and cache), but ensures that the writing operation in both, is atomic and consistent, allowing the website customer access the real data from the device.
