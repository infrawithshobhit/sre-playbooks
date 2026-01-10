# Kafka Consumer Lag Incident

## What Dynatrace shows
- Consumer lag increasing
- Message backlog growing
- Downstream services processing old data
- Throughput lower than expected

## What this usually means
Consumers cannot keep up with producers.
This leads to delayed processing and stale data.

## How to investigate
1. Check which consumer group has lag
2. Identify if lag is growing or stable
3. Check consumer CPU, memory, and thread usage
4. Look for message size spikes
5. Check if a deployment recently happened

## What usually fixes it
- Scale up consumer replicas
- Restart stuck consumers
- Increase partition count
- Rollback a bad deployment
- Increase consumer poll size

## How to prevent next time
- Alert on consumer lag
- Auto-scale consumers
- Add dead letter queues
- Monitor processing time per message
