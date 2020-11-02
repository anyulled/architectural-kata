# ADR13. Storage for product images and static files

## STATUS
Accepted

## DESCRIPTION
The system has to store static files somewhere.

## DECISION
Using some external driver in the cloud to store static files is cheaper than "in-house", and S3 for example is one good choice.

## CONSEQUENCES
Slower than other channels to store static files.