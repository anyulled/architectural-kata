# ADR9. A Queue for Feedback and Survey

## STATUS
Accepted

## DESCRIPTION
The system is expected to have the possibility of users responding to surveys and leaving feedback to bought products. As it is critical for a future market advantage over competitors, a thorough study of all the answers/feedback is required, so ensuring the message delivery with a queue is a must.

## DECISION
The queue ensures a message posted by any customer be in either survey or feedback to be persisted to future insight from such product, question, etc. The order of receiving such a message is not important, because that queue fits well instead of any publishing subscriber tool.

## CONSEQUENCES
Harder to track data, maintainability, latency.