You are auditing placeholder logic, mock data, stubs, no-ops, fake success states, and unwired features in an existing repository.

Search for:

- mock
- fake
- sample
- demo
- placeholder
- stub
- todo
- fixme
- noop
- temporary
- hardcoded
- localhost
- sandbox

Check for:

- Hardcoded sample records in production paths.
- Fake users, accounts, projects, files, events, metrics, dates, IDs, or statuses.
- Mock responses outside test/dev fixtures.
- Demo data mixed with real data flows.
- Placeholder values persisted.
- Fallback mock data hiding failed real requests.
- Buttons with no handler.
- Forms that do not submit.
- UI claims success without real mutation.
- Pages displaying placeholders while real backend/system logic exists.
- Search/filter/sort/export/import controls not connected.
- Services/functions/handlers/jobs never called.
- API endpoints/routes/commands defined but unreachable.
- Validation functions defined but bypassed.
- Permission checks defined but not used.
- Empty catch blocks.
- Empty handlers.
- Return success without doing work.
- Stub implementations returning defaults.
- Logging instead of actual mutation.
- Dev-only code active in production.
- Test fixtures bundled into production.
- Debug panels/routes enabled.
- Localhost or sandbox endpoints hardcoded.
- Sample credentials or tokens present.

For each finding, provide:

- Title.
- Severity.
- Evidence.
- Observation.
- Why it matters.
- Trace/reproduction notes.
- Minimal remediation.
- Confidence.
- Verification steps.

Also provide:

- Placeholder/mock inventory.
- Unwired UI/action table.
- Unreachable backend/system table.
- Fake success/no-op table.
- Dev/test leakage table.
- Top 3–5 fixes.

Rules:

- Do not remove legitimate test fixtures.
- Prefer gating, removal from production paths, honest disabled states, or real wiring.