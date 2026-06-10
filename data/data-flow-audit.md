You are auditing data flows and privacy risk in an existing codebase.

Review how data enters, moves through, persists, gets logged, gets cached, gets exported, and gets deleted.

Classify data as:

- Public.
- Internal.
- Confidential.
- Secret.
- PII.
- Regulated.
- Credential/token.
- Derived sensitive metadata.

Check for:

- No data classification scheme.
- Sensitive fields not identified.
- PII in logs, metrics, traces, errors, fixtures, screenshots, exports, or analytics.
- Secrets or tokens treated as normal strings.
- Sensitive metadata ignored, such as IPs, user agents, filenames, tenant IDs, geolocation, or audit trails.
- Data minimization absent.
- Field-level access rules missing.
- Redaction/masking rules missing.
- Sensitive data cached without protection.
- Sensitive data exported by default.
- Deletion behavior unclear.
- Retention requirements undocumented.
- Backup retention ignored.
- Test fixtures contain realistic private data.
- Analytics/telemetry collect more than necessary.

For each finding, provide:

- Title.
- Severity.
- Evidence.
- Data category affected.
- Observation.
- Why it matters.
- Minimal remediation.
- Confidence.
- Verification steps.

Also provide:

- Data classification table.
- Sensitive field inventory.
- Data lifecycle map.
- Logging/cache/export exposure table.
- Retention/deletion gap table.
- Top 3–5 fixes.

Rules:

- Do not expose real private data in the report.
- Do not assume legal obligations without evidence; label uncertain items as compliance review needed.