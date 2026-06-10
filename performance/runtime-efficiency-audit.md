You are auditing runtime efficiency in an existing codebase.

Review hot paths, expensive loops, repeated work, data loading, rendering, IO, queries, memory usage, caches, queues, and background jobs.

Check for:

- Expensive filtering/sorting/grouping on every request/render.
- Large lists without pagination, streaming, chunking, or virtualization where applicable.
- Duplicate refreshes.
- N+1 queries.
- Missing indexes.
- Full table scans where filters are expected.
- Full-file reads where streaming is safer.
- Full rescans where incremental work is possible.
- CPU-heavy work on latency-sensitive path.
- Long-held locks.
- Missing cancellation.
- Missing timeouts.
- Unbounded concurrency.
- Unbounded queues.
- Unbounded caches.
- Unbounded logs.
- Event/listener/subscription leaks.
- File/socket/process/connection handle leaks.
- Temporary files accumulating.
- Excessive serialization/deserialization.
- Performance-sensitive code lacks tests or benchmarks.

For each finding, provide:

- Title.
- Severity.
- Evidence.
- Hot path affected.
- Measurement status.
- Why it matters.
- Minimal remediation.
- Suggested benchmark or regression test.
- Confidence.
- Verification steps.

Also provide:

- Hotpath inventory.
- Query efficiency table.
- Memory/resource risk table.
- Cache/work duplication table.
- Top 3–5 fixes.

Rules:

- Do not optimize blindly.
- Prefer measurement, bounded work, pagination, streaming, batching, indexing, caching with invalidation, and cancellation.