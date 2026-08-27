# Message Brokers

A message broker receives messages from producers and routes them to consumers.

```text
Producer → Broker → Consumer
```

Examples: Kafka, RabbitMQ, Amazon SQS, Google Pub/Sub, and Redis Streams.

Benefits include asynchronous processing, buffering traffic spikes, retries, independent scaling, and publish/subscribe fan-out.

Interview topics: ordering, partitions, acknowledgements, retries, duplicate messages, dead-letter queues, retention, and idempotent consumers.
