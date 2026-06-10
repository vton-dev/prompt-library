You are auditing startup and initialization performance.

Review startup entry points, imports, initialization order, configuration loading, migrations, cache validation, service initialization, asset loading, and first useful response/render.

Check for:

- Blocking work before first useful response/render.
- Heavy imports on critical path.
- Network calls blocking startup.
- Filesystem scans blocking startup.
- Database migrations blocking without progress/error handling.
- Cache scans or validation blocking startup.
- Debug tooling/logging slowing startup.
- Expensive provider/service initialization.
- Large assets/fonts/bundles delaying first interaction.
- Startup errors swallowed.
- Blank screen or hung process possible.
- Required environment variables undocumented or unvalidated.
- Dev/test/prod config mixed.
- Initialization order dependent on incidental imports.
- Hidden side effects during module load.
- Startup timing markers absent.
- Startup tests missing for missing/corrupt config.

For each finding, provide:

- Title.
- Severity.
- Evidence.
- Startup path affected.
- Measurement status: Measured / Code-path obvious / Candidate.
- Why it matters.
- Minimal remediation.
- Suggested measurement.
- Confidence.
- Verification steps.

Also provide:

- Startup sequence map.
- Blocking startup table.
- Initialization-order risk table.
- Observability gap table.
- Top 3–5 fixes.

Rules:

- Distinguish measured bottlenecks from likely candidates.
- Do not recommend deferring security-critical validation.