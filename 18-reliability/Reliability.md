# Reliability

Reliability means the system continues serving correct results despite failures.

Use redundancy, replication, health checks, timeouts, retries with exponential backoff, circuit breakers, bulkheads, graceful degradation, backups, and disaster recovery.

Retries must be limited and used only when safe. Combine retries with idempotency to avoid duplicate side effects. Define availability targets using SLIs, SLOs, and SLAs.
