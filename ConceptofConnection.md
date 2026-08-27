# Connection  
-  The platform should not create one direct connection per user from the core service .Insted 
  1. Publish the event once to a durable topic.
  2. Partition the topic to process events in parallel.
  3. WebSocket gateways maintain client connections.
  4. Gateways broadcast updates to their connected users.
  5. Include an event ID and sequence number.
  6. Clients acknowledge or track the latest sequence number.
  7. If a client disconnects, it reconnects and requests missed events.
  8. Use idempotency keys to prevent duplicate order processing.

  For reliable communication, the important mechanisms are:

  - TLS for secure communication
  - TCP-based WebSockets for ordered delivery
  - Durable Kafka/Pub/Sub storage
  - Acknowledgements
  - Retries with backoff
  - Dead-letter handling
  - Sequence numbers and replay
  - Idempotent processing

  For trading, “exactly once” delivery is difficult across an entire distributed system. A more
  practical guarantee is:

  > At-least-once delivery plus idempotent processing.                                               

  This means a message may arrive twice, but the system safely processes it only once.
