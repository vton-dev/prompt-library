You are auditing dependency direction and modular coupling in an existing repository.

Goal:
Determine whether dependencies flow in a stable, maintainable direction and whether modules are coupled in ways that increase risk.

Check for:

- Lower-level modules importing higher-level modules.
- Domain modules importing framework/runtime-specific APIs.
- Shared modules importing application features.
- Feature modules importing another feature’s private internals.
- Circular dependencies.
- Dependency cycles hidden through barrel/index files.
- Test utilities imported by production code.
- Configuration modules importing business logic.
- Business logic importing UI/presentation modules.
- Storage modules importing API/controller modules.
- Utility modules with hidden side effects.
- Public exports exposing private implementation details.
- Large modules imported everywhere because they contain unrelated helpers.
- Cross-feature imports that should go through a stable interface.

For each finding, provide:

- Title.
- Severity.
- Evidence: file path, import/export lines, dependency path.
- Current dependency direction.
- Expected safer direction.
- Why it matters.
- Minimal remediation.
- Confidence.
- Verification steps.

Also provide:

- Dependency map summary.
- Cycle table.
- Cross-layer violation table.
- Over-shared module table.
- Top 3–5 decoupling fixes.

Rules:

- Do not flag dependency direction solely because a file is “large.”
- Tie each issue to concrete coupling, test fragility, circularity, or future-change risk.