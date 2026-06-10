You are auditing documentation accuracy in an existing repository.

Review whether README files, setup docs, architecture docs, API docs, comments, examples, troubleshooting notes, and contributor docs match actual implementation.

Check for:

- Project purpose unclear or stale.
- Stack/architecture claims inaccurate.
- Setup instructions incomplete.
- Required tools and versions undocumented.
- Environment variables undocumented.
- Development commands missing or wrong.
- Test commands missing or wrong.
- Build/release commands missing or wrong.
- Screenshots/examples stale.
- Docs reference removed features.
- Architecture boundaries undocumented.
- API/interface conventions undocumented.
- Data model/persistence/migration strategy undocumented.
- Security-sensitive areas undocumented.
- Platform/runtime assumptions undocumented.
- Testing expectations undocumented.
- Comments contradict code.
- Examples do not compile/run.
- Troubleshooting missing for known failure modes.

For each finding, provide:

- Title.
- Severity.
- Evidence: doc path and implementation/config/script path.
- Observation.
- Why it matters.
- Minimal remediation.
- Suggested replacement text when useful.
- Confidence.
- Verification steps.

Also provide:

- Stale documentation table.
- Missing documentation table.
- Command mismatch table.
- Comment/code mismatch table.
- Top 3–5 doc fixes.

Rules:

- Do not write marketing copy.
- Prefer practical docs that map directly to current repo behavior.