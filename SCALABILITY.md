# Scalability and capacity plan

- Keep request handlers stateless and persist shared state in a durable service.
- Bound input size, request rate, and concurrency for expensive workflows.
- Move long-running tasks to durable, bounded workers where supported.
- Use pagination for large history or event collections.
- Apply explicit timeouts and bounded retries to external dependencies.
- Protect user-specific data with server-side authorization and avoid shared caching of private responses.
- Track p95/p99 latency, error rate, worker queue age, dependency failures, and resource saturation.

## Release gates
- [ ] Large collections and inputs are bounded.
- [ ] Retry behavior is idempotent.
- [ ] Recovery and backup/restore procedures are tested.
- [ ] CI builds and tests pass.
- [ ] Capacity claims are backed by a reproducible load test.

This document is a plan, not evidence of a benchmark or production readiness.
