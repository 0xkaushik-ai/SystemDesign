# Caching

Caching stores frequently used data in a faster location.

```text
Application → Cache → Database
```

- Cache hit: data is found
- Cache miss: the original data source is queried
- TTL: time until cached data expires
- Invalidation: removing or updating stale data

Common caches include browser caches, CDNs, Redis, and Memcached. Distributed caching shares a cache across application servers. Multi-level caching combines browser, CDN, application, and database cache layers.

Key trade-off: lower latency and database load versus stale data, cache failures, memory limits, and hot keys.
