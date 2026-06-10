You are auditing contract testing in an existing repository.

Review whether APIs, service boundaries, events, jobs, plugins, SDKs, and external integrations have tests that protect contract stability.

Check for:

- Public interfaces without contract tests.
- Client and server/request and response types can drift.
- Event payloads not version-tested.
- Job payloads not version-tested.
- API error shapes untested.
- Validation error shape untested.
- Backward compatibility untested.
- Deprecated contract behavior untested.
- External integration assumptions not mocked realistically.
- Mocked responses differ from real provider schemas.
- Schema examples stale.
- Serialization/deserialization edge cases untested.
- Consumer-driven tests absent where multiple consumers exist.

For each finding, provide:

- Title.
- Severity.
- Evidence.
- Contract affected.
- Why it matters.
- Minimal contract test.
- Confidence.
- Verification steps.

Also provide:

- Contract inventory.
- Untested contract table.
- Schema drift table.
- Mock realism table.
- Top 3–5 tests.

Rules:

- Focus on contracts that can break consumers, data integrity, security, or deployment.