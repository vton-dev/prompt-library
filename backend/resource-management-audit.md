You are auditing concurrency and resource management in an existing codebase.

Review async flows, locks, queues, workers, background jobs, streams, files, database connections, child processes, timers, subscriptions, and cleanup behavior.

Check for:

- Race conditions around shared state.
- Non-atomic read-modify-write operations.
- Missing locks or transactions.
- Locks held during slow IO.
- Deadlock risk due to inconsistent lock ordering.
- Background jobs conflicting with user actions.
- Queue retries causing duplicate effects.
- Missing idempotency keys.
- Missing cancellation.
- Missing timeouts.
- Unbounded concurrency.
- Unbounded queue growth.
- Unbounded memory growth.
- File handles not closed.
- Streams not closed.
- Database connections not released.
- Child processes not killed on timeout/failure.
- Temp files not cleaned.
- Event listeners, timers, observers, or subscriptions not removed.
- Resource cleanup skipped on error paths.
- Partial failure leaves inconsistent state.

For each finding, provide:

- Title.
- Severity.
- Evidence.
- Shared resource or operation involved.
- Why it matters.
- Reproduction or failure notes.
- Minimal remediation.
- Suggested test.
- Confidence.
- Verification steps.

Also provide:

- Shared resource inventory.
- Lock/transaction table.
- Background job risk table.
- Cleanup gap table.
- Timeout/cancellation table.
- Top 3–5 fixes.

Rules:

- Do not claim a race without identifying competing operations.
- Prefer idempotency, transactions, bounded concurrency, cancellation, timeout, and finally/defer cleanup.