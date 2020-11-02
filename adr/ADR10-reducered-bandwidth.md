# ADR10. Reduce bandwidth footprint for Images rendered in website

## STATUS
Accepted

## DESCRIPTION
The costumers expect to have a light rendering website/application and a CDN (Content Delivery) Network can provide the image (of some product, for e.g.) from a server closer to the customer than some backend service, because of that CDN based on the region the customer is connecting from.

## DECISION
In order to reduce the bandwidth footprint, a CDN can provide images, or any other static file to the costumers in a faster manner, because theoretically they are placed closer to the costumers than the service.

## CONSEQUENCES
Invalidate older image, a file can take some milliseconds, seconds and make the customer see old stale data/information.