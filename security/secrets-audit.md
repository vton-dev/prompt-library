You are auditing secrets management in an existing repository.

Review secret discovery, storage, delivery, redaction, rotation, revocation, runtime exposure, build exposure, and incident readiness.

Treat the following as secrets or secret-like material:

- API keys.
- Database credentials.
- JWT/session secrets.
- Encryption keys.
- OAuth client secrets.
- Cloud credentials.
- Private keys.
- Certificates.
- Webhook secrets.
- Refresh tokens.
- Signing keys.
- Service-account credentials.

Check for:

- Hardcoded secrets.
- Secrets in config files.
- Secrets in documentation.
- Secrets in tests or fixtures.
- Secrets in examples.
- Secrets in CI/CD workflows.
- `.env` files committed.
- Example env files containing real-looking secrets.
- Secrets exposed to frontend/client/public bundles.
- Secrets printed in logs.
- Secrets returned in errors.
- Secrets passed through URLs.
- Secrets passed through command arguments.
- Secrets stored in localStorage/sessionStorage where inappropriate.
- Same secrets reused across dev/staging/prod.
- Long-lived credentials where short-lived credentials are feasible.
- No rotation procedure.
- No revocation path.
- Overbroad secret access in CI/CD.
- CI secrets exposed to untrusted pull requests.
- Secret scanning absent.
- Build artifacts containing secrets.

For each finding, provide:

- Title.
- Severity.
- CWE/OWASP reference if applicable.
- Evidence: file, variable/config key, line range.
- Observation with secrets masked.
- Why it matters.
- Immediate containment steps if a real secret is found.
- Minimal remediation.
- Rotation/revocation guidance.
- Defense-in-depth guidance.
- Confidence.
- Verification steps.

Also provide:

- Secret exposure inventory.
- Runtime secret delivery table.
- CI/CD secret risk table.
- Rotation readiness table.
- Secret scanning gap table.
- Top 3–5 fixes.

Rules:

- Never print full secret values.
- Mask secrets in evidence.
- If a real secret is found, recommend immediate revocation and rotation.
- Prefer secret managers, short-lived credentials, scoped access, redaction, and CI secret isolation.