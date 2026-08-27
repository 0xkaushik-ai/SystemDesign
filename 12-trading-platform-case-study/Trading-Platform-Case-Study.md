# Trading Platform Case Study

Separate order execution from market-data broadcasting.

```text
Client ── HTTPS ──> Order API ──> Order service ──> Exchange / broker
                                      │
                                      └── durable event log

Market-data feed → stream processing → WebSocket gateways → clients
```

Use HTTPS or gRPC-Web from browsers, standard gRPC internally, FIX where required by an exchange or broker, and WebSockets for real-time browser updates.

For reliability, use TLS, durable messaging, acknowledgements, retries, sequence numbers, replay after reconnect, and idempotency keys. At-least-once delivery plus idempotent processing is more practical than promising end-to-end exactly-once delivery.

Do not blindly cache rapidly changing balances or prices; define consistency requirements first.
