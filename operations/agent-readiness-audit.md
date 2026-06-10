You are auditing whether an AI coding agent can safely modify this repository.

Review repository instructions, guardrails, tests, architecture docs, generated files, dangerous areas, mock-data policy, dependency rules, and coding conventions.

Check for:

- No coding-agent instructions.
- Architecture boundaries undocumented.
- File/folder conventions undocumented.
- Preferred patch style undocumented.
- No rule for full-file replacement versus targeted patch.
- Test/lint/typecheck/build commands missing.
- Generated files unidentified.
- Vendor files unidentified.
- Do-not-edit files unidentified.
- Sensitive files/configs unidentified.
- Dependency addition rules absent.
- Public contract change rules absent.
- Migration rules absent.
- Security-sensitive workflows undocumented.
- Mock-data policy absent.
- UI/design conventions undocumented.
- Error handling conventions undocumented.
- State/data flow conventions undocumented.
- Inconsistent patterns likely to be copied.
- Dead code likely to mislead.
- Placeholder/mock code likely to be treated as production.
- Broad type escapes allowing bad changes to pass.
- Scripts require undocumented local setup.
- No guardrail against broad rewrites.
- No guardrail against framework/library replacement.
- No guardrail against weakening validation, type checks, lint rules, tests, or security controls.
- No guardrail against modifying generated/vendor files.

For each finding, provide:

- Title.
- Severity.
- Evidence.
- Observation.
- Why it matters.
- Minimal remediation.
- Suggested instruction text.
- Confidence.
- Verification steps.

Also provide:

- Agent-readiness score from 0–10.
- Files/docs most likely to mislead an agent.
- Missing instruction table.
- Risky pattern table.
- Suggested AGENTS.md content.
- Minimal agent handoff checklist.
- Top 3–5 fixes.

Rules:

- Do not invent architecture rules that conflict with current code.
- Keep suggested guardrails concrete and enforceable.