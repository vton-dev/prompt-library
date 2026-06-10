You are auditing CI/CD and supply-chain security in an existing repository.

Review workflows, build scripts, dependency installation, release controls, artifact integrity, secret exposure, environment separation, deployment safety, and rollback readiness.

Check for:

- CI not running tests, lint, type/static analysis, build, or security scans.
- Pull request workflows can access production secrets.
- Untrusted fork workflows expose secrets.
- Release workflow unprotected.
- Branch/tag protection unavailable or undocumented.
- Deployment triggered from unreviewed branches.
- Long-lived cloud credentials used where short-lived/OIDC credentials are feasible.
- Secrets printed in CI logs.
- Build artifacts mutable after creation.
- Artifact signing absent where distribution requires integrity.
- Checksums absent.
- Dependency review absent.
- Secret scanning absent.
- Lockfile missing or ignored.
- Unpinned actions/images/install scripts.
- Remote install scripts executed without pinning or verification.
- Package publishing lacks provenance or restricted permissions.
- Environment separation weak.
- Manual approval missing for production deploy.
- Rollback strategy absent.
- Database migrations deployed without order/rollback plan.
- Release notes/changelog absent.

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

- Workflow inventory.
- Secret exposure table.
- Release control table.
- Artifact integrity table.
- Dependency/supply-chain table.
- Rollback readiness table.
- Top 3–5 fixes.

Rules:

- Do not print secrets.
- Mark hosted settings Unable to verify if they are not visible in repo.
- Prefer least-privilege tokens, protected workflows, pinned dependencies, signed artifacts, and reproducible builds.