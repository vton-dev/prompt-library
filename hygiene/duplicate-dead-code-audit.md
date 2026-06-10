You are auditing duplicate code and dead code in an existing repository.

Review repeated logic, redundant abstractions, unused files, dead exports, unreachable branches, stale compatibility layers, duplicate configuration, and unused assets.

Check for:

- Repeated business rules.
- Repeated validation logic.
- Repeated formatting/parsing/mapping logic.
- Repeated API/service wrappers.
- Repeated error handling.
- Repeated permission checks.
- Repeated configuration constants.
- Similar functions with divergent edge cases.
- Copy-pasted code with inconsistent fixes.
- Unused exports.
- Unused imports.
- Unused functions/classes/components/modules.
- Unused routes/endpoints/commands/jobs.
- Unreachable branches.
- Permanently enabled/disabled feature flags.
- Old compatibility code no longer reachable.
- Placeholder methods never called.
- Deprecated files imported nowhere.
- Generic wrappers with one caller and no real abstraction.
- Interfaces with one implementation and no realistic second use.
- Utility functions hiding simple direct calls.
- Old feature names in code.
- Duplicate config keys.
- Duplicate style tokens.
- Duplicate assets/icons/images.
- Duplicate documentation sections.

For each finding, provide:

- Title.
- Severity.
- Evidence.
- Observation.
- Why it matters.
- Minimal remediation.
- Safe deletion or consolidation notes.
- Confidence.
- Verification steps.

Also provide:

- Duplicate-code cluster table.
- Dead-code candidate table.
- Stale abstraction table.
- Duplicate config/asset table.
- Top 3–5 cleanup fixes.

Rules:

- Do not claim code is dead without reference/import/registration evidence.
- Distinguish test fixtures from production dead code.