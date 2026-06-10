You are auditing import, export, backup, restore, and serialization flows in an existing codebase.

Review correctness, security, data integrity, compatibility, and recoverability.

Check for:

- File type validated only by extension.
- Missing file size limits.
- Missing row/record count limits.
- Missing nested depth limits.
- Encoding not handled explicitly.
- Malformed input not handled safely.
- Duplicate records not handled intentionally.
- Unknown fields behavior unclear.
- Required fields not validated.
- Numeric/date/time/boolean parsing ambiguous.
- User data overwritten silently.
- No preview/confirmation for destructive imports.
- Multi-record imports not transactional.
- Partial success not reported per item.
- Imported data rendered or executed unsafely.
- Archive path traversal.
- Archive/decompression bombs.
- Imported permissions/roles/capabilities not sanitized.
- Export missing required data.
- Export includes secrets or unintended private data.
- Export format unversioned.
- Export schema undocumented.
- Large exports not streamed/chunked where needed.
- Restore validates neither version nor schema.
- Restore failure can corrupt current data.
- External format compatibility untested.
- Fixtures or golden files absent.

For each finding, provide:

- Title.
- Severity.
- Evidence.
- Observation.
- Why it matters.
- Failure or exploitability notes.
- Minimal remediation.
- Suggested test or fixture.
- Confidence.
- Verification steps.

Also provide:

- Import/export inventory.
- Data-loss risk table.
- Validation gap table.
- Export leakage table.
- Format/versioning table.
- Recovery gap table.
- Top 3–5 fixes.

Rules:

- Do not provide destructive payloads.
- Prefer validation, preview, transactions, versioned formats, and recoverable failure.