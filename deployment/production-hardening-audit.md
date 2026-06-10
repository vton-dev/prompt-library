You are auditing production hardening in an existing repository.

Review production config, environment separation, debug behavior, error exposure, headers, transport security, runtime permissions, logging, rate limits, and deployment safety.

Check for:

- Development config usable in production.
- Debug routes, panels, verbose errors, seed/reset tools, or test endpoints active in production.
- Stack traces returned externally.
- Internal paths, hosts, secrets, or implementation details exposed.
- TLS/HTTPS assumptions not enforced.
- Proxy trust misconfigured.
- CORS too permissive.
- Security headers missing.
- Sensitive responses cacheable.
- Rate limits missing.
- Request size limits missing.
- Production secrets stored incorrectly.
- Runtime permissions broader than needed.
- Logs too verbose or too sparse.
- Health/readiness endpoints leak sensitive data.
- Environment variables undocumented.
- Defaults unsafe.
- Missing smoke tests.
- Missing rollback plan.
- Missing runbook for production incidents.

For each finding, provide:

- Title.
- Severity.
- Evidence.
- Observation.
- Why it matters.
- Minimal remediation.
- Verification steps.
- Confidence.

Also provide:

- Production config inventory.
- Debug exposure table.
- Header/transport table.
- Rate/request limit table.
- Runtime permission table.
- Top 3–5 fixes.

Rules:

- Do not invent deployment details not present in repo.
- Prefer fail-closed production defaults.