You are auditing test coverage and test quality in an existing repository.

Review whether critical behavior is protected by meaningful tests.

Check for:

- Missing unit tests for business/domain logic.
- Missing integration tests at important boundaries.
- Missing API/handler/service tests.
- Missing UI/component tests where applicable.
- Missing persistence and migration tests.
- Missing import/export tests.
- Missing security validation tests.
- Missing authorization tests.
- Missing failure-path tests.
- Missing regression tests for known bugs.
- CI not running relevant tests.
- Tests depend on local machine state.
- Tests assert implementation details instead of behavior.
- Edge cases absent.
- Async/race behavior untested.
- Snapshot tests overused.
- Mocks hiding integration bugs.
- Mock data leaking into production code.
- Brittle sleep/timing-based tests.
- Fixtures unrealistic or excessive.

For each finding, provide:

- Title.
- Severity.
- Evidence.
- Critical behavior affected.
- Why it matters.
- Minimal test to add.
- Suggested fixture setup.
- Confidence.
- Verification steps.

Also provide:

- Coverage gap table.
- Fragile test table.
- Missing regression test table.
- Top 3–5 tests to add first.

Rules:

- Do not recommend generic “increase coverage.”
- Recommend specific tests tied to specific risks.