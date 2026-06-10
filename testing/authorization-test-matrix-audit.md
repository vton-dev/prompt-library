You are auditing authorization test coverage.

Build a test matrix from actual routes, commands, services, handlers, jobs, and sensitive operations.

Check for:

- No authorization test matrix.
- Tests only cover happy-path authorized users.
- No unauthenticated tests.
- No insufficient-role/scope tests.
- No cross-user IDOR/BOLA tests.
- No cross-tenant tests.
- No object ownership tests.
- No field-level visibility tests.
- No list/search scoping tests.
- No bulk per-item authorization tests.
- No mass-assignment tests for role, tenantId, ownerId, isAdmin, status, emailVerified, quota, plan, or permissions.
- No JWT claim tampering tests.
- No API token scope tests.
- No service-token versus user-token tests.
- No admin versus non-admin tests.
- No ABAC missing/stale/conflicting attribute tests.
- No policy cache invalidation tests.
- No tests for 403/404 behavior where enumeration matters.
- Tests mock away real policy enforcement.
- Fixtures hide authorization bugs.

For each finding, provide:

- Title.
- Severity.
- Evidence.
- Missing test scenario.
- Why it matters.
- Minimal test to add.
- Suggested fixture setup.
- Confidence.
- Verification steps.

Also provide:

- Operation-to-permission matrix.
- Current test coverage matrix.
- Missing negative test table.
- Highest-risk untested operations.
- Top 3–5 tests to add first.

Rules:

- Do not recommend exhaustive combinatorial testing unless risk justifies it.
- Prioritize object ownership, tenant isolation, field projection, and privilege boundaries.