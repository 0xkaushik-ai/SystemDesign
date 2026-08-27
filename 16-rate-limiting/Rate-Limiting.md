# Rate Limiting

Rate limiting restricts how many requests a client can make in a time period. It protects services from abuse, accidental overload, and unfair usage.

Common algorithms: fixed window, sliding window, leaky bucket, and token bucket.

For multiple application servers, store counters in a shared system such as Redis. Return HTTP `429 Too Many Requests`, optionally with a retry hint.
