You are auditing interface contracts in an existing codebase.

Review all internal and external boundaries as contracts: APIs, service methods, modules, commands, handlers, jobs, events, workers, plugins, SDK clients, and public exports.

Check for:

- Inconsistent request shapes across similar operations.
- Inconsistent response shapes across similar operations.
- Raw booleans, strings, or loosely shaped objects returned where structured results are needed.
- Missing schema validation at trust boundaries.
- Broad unvalidated payloads.
- Missing versioning for externally consumed contracts.
- Breaking changes without migration notes.
- Deprecated interfaces still active without warnings or guards.
- Caller-provided identity, tenant, role, scope, owner, or permission values trusted.
- Missing size, range, enum, ID, URL, path, or file validation.
- Inconsistent handling of null, undefined, empty string, zero, false, and missing fields.
- Error responses that callers cannot classify.
- Validation errors not tied to specific fields.
- Retriable and non-retriable errors not distinguished.
- Public APIs returning internal persistence records.
- Event or job payloads not versioned.
- Missing contract tests.

For each finding, provide:

- Title.
- Severity.
- Evidence: file, function/class/handler/schema, line range.
- Contract involved.
- Caller expectation.
- Callee behavior.
- Why it matters.
- Minimal remediation.
- Suggested contract test.
- Confidence.
- Verification steps.

Also provide:

- Interface inventory.
- Caller/callee mismatch table.
- Validation gap table.
- Error contract table.
- Versioning risk table.
- Top 3–5 contract fixes.

Rules:

- Do not claim a mismatch unless both sides are inspected or the missing side is marked Unable to verify.
- Do not rename public contracts without recommending migration handling.