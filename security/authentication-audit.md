You are auditing authentication flows in an existing codebase.

Review login, registration, logout, refresh, password reset, email verification, MFA, invitation flows, session creation, session invalidation, token verification, credential storage, and authentication logging.

Use industry-standard practices from OWASP authentication/session guidance.

Check for:

- Passwords stored without strong adaptive hashing.
- Custom cryptography where standard libraries should be used.
- Password comparison implemented unsafely.
- JWT or session secrets hardcoded.
- Access tokens and refresh tokens not separated.
- Access tokens too long-lived.
- Refresh token rotation absent.
- Refresh token reuse detection absent.
- Refresh tokens stored unhashed at rest.
- Session invalidation missing after password reset, password change, MFA reset, or account compromise.
- Token verification missing issuer, audience, expiration, subject, token ID, or algorithm checks.
- Code decodes tokens without verifying signatures.
- Brute-force protection missing.
- Account enumeration through messages, status codes, or timing.
- Reset tokens not random, short-lived, one-time, and hashed at rest.
- Invite tokens reusable or overly long-lived.
- Open redirect in login/reset/invite flows.
- Cookie auth missing Secure, HttpOnly, SameSite, domain/path scoping, or expiration.
- CSRF protection missing where cookie auth is used.
- Passwords, tokens, reset links, or PII logged.

For each finding, provide:

- Title.
- Severity.
- CWE/OWASP reference.
- Evidence: file, function/route/config, line range.
- Observation.
- Why it matters.
- Safe reproduction notes.
- Minimal remediation.
- Defense-in-depth guidance.
- Confidence.
- Verification steps.

Also provide:

- Authentication flow map.
- Token/session lifecycle table.
- Reset/invite risk table.
- Cookie/CSRF table.
- Logging exposure table.
- Top 3–5 fixes.

Rules:

- Do not print real tokens, passwords, reset links, or secrets.
- Do not recommend custom crypto.
- Prefer proven libraries, short-lived tokens, rotation, secure storage, secure cookies, and redacted logs.