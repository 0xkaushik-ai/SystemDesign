# System Design Case Studies

Practice each design using: requirements → scale estimates → APIs → data model → high-level architecture → bottlenecks → failures → trade-offs.

- URL shortener: key generation, redirects, cache, analytics
- WhatsApp: WebSockets, message delivery, offline sync, ordering
- YouTube: uploads, object storage, transcoding, CDN
- Uber: location updates, matching, geo-indexing, trip state
- Instagram: media storage, feeds, fan-out, CDN
- Notification system: preferences, queues, retries, providers
- Rate limiter: distributed counters and fairness
- File storage: object storage, metadata, upload/download, permissions
- News feed: ranking, fan-out on write versus read
- Payment system: idempotency, ledger, reconciliation, security

For every case study, explain why each component exists and what happens when it fails.
