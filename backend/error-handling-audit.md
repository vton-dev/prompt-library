You are auditing error handling and failure modes in an existing codebase.

Review whether errors are classified, propagated, logged, displayed, retried, recovered from, and tested correctly.

Check for:

- Errors represented only as raw strings.
- Validation, permission, not found, conflict, timeout, dependency, corrupt-data, cancellation, and internal errors not distinguished.
- Retriable and non-retriable errors not distinguished.
- User-actionable and developer-actionable errors not distinguished.
- Exceptions/errors swallowed.
- Broad catch blocks hiding root cause.
- Error wrapping losing context.
- Error wrapping exposing secrets or internals.
- Callers ignoring returned errors.
- Cleanup not run after failure.
- Transaction rollback missing.
- Stack traces shown externally.
- Internal paths, hosts, secrets, tokens, or implementation details shown externally.
- Generic messages where user needs an action.
- Loading indicators stuck after failure.
- Forms losing user input after validation failure.
- Retries unbounded.
- Retry of non-idempotent actions unsafe.
- Partial success not represented.
- Batch failures not reported per item.
- External dependency failure not isolated.
- Corrupt or missing config/storage not recoverable.
- Startup failure path unclear.

For each finding, provide:

- Title.
- Severity.
- Evidence.
- Observation.
- Why it matters.
- Failure/reproduction notes.
- Minimal remediation.
- Suggested test.
- Confidence.
- Verification steps.

Also provide:

- Error taxonomy assessment.
- Failure-mode table.
- User-facing error table.
- Retry/timeout table.
- Logging/diagnostic gap table.
- Top 3–5 fixes.

Rules:

- Do not recommend swallowing errors.
- Preserve internal diagnostics while preventing external leakage.
- Prefer classified errors, cleanup guarantees, rollback, bounded retries, and testable recovery.