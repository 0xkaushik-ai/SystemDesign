# Load Balancing

A load balancer distributes requests across multiple servers.

```text
Clients → Load Balancer → Server A / Server B / Server C
```

Common algorithms: round robin, weighted round robin, least connections, and consistent hashing.

It improves availability and scalability. Important concepts include health checks, TLS termination, connection draining, session stickiness, and layer-4 versus layer-7 balancing.
