You are auditing input validation and injection risk in an existing codebase.

Review all external and semi-trusted inputs and all dangerous sinks.

Input sources include:

- HTTP route params.
- Query strings.
- Request bodies.
- Headers.
- Cookies.
- Forms.
- Files.
- Imports.
- Webhooks.
- Messages.
- Jobs.
- CLI args.
- Environment variables.
- Third-party callbacks.
- Local/native IPC.

Dangerous sinks include:

- SQL queries.
- NoSQL queries.
- LDAP queries.
- Shell/process execution.
- Filesystem paths.
- URL fetches.
- HTML/Markdown rendering.
- Templates.
- XML parsers.
- JSON deserialization.
- Regex construction.
- Redirects.
- Logs.
- Eval-like APIs.

Check for:

- Raw SQL string concatenation.
- Unsafe ORM raw queries.
- NoSQL operator injection.
- User-controlled sort/order/group fields not allowlisted.
- Shell command interpolation.
- User-controlled filesystem paths.
- SSRF through user-controlled URLs.
- Open redirects.
- XSS through unsafe HTML/Markdown/template rendering.
- Template injection.
- XML external entity risk.
- Unsafe deserialization.
- Regex injection or catastrophic regex.
- Missing request body limits.
- Missing file size limits.
- Missing JSON depth limits.
- Parameter pollution unhandled.
- Required field validation missing.
- Type checks missing.
- Enum/status validation missing.
- Numeric range validation missing.
- Date/time validation ambiguous.
- Unicode/case/whitespace normalization missing where identity depends on it.
- Validation only in UI/client code.
- Error messages echoing unsafe input.

For each finding, provide:

- Title.
- Severity.
- CWE/OWASP reference.
- Evidence: source, sink, validation/encoding/parameterization location, line range.
- Observation.
- Why it matters.
- Safe minimal proof using dummy payloads.
- Minimal remediation.
- Defense-in-depth guidance.
- Confidence.
- Verification steps.

Also provide:

- Input source inventory.
- Sink inventory.
- Source-to-sink matrix.
- Injection risk table.
- Request limit table.
- Top 3–5 fixes.

Rules:

- Do not include destructive payloads.
- Do not rely on validation alone where parameterization or output encoding is required.
- Prefer schemas, allowlists, parameterized APIs, bounded inputs, safe parsers, and sink-specific encoding.