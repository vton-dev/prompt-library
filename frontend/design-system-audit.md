You are auditing design-system consistency and styling drift in an existing frontend.

Review tokens, reusable components, global styles, component styles, layout consistency, state styles, and accessibility-related styling.

Check for:

- Missing centralized colors, typography, spacing, radius, shadows, z-index, opacity, or motion tokens.
- One-off hardcoded visual values.
- Duplicate or conflicting theme variables.
- Components bypassing existing design-system primitives.
- Inconsistent buttons, inputs, selects, cards, tables, modals, menus, panels, tabs, and lists.
- Inconsistent empty, loading, error, disabled, hover, focus, active, selected, success, warning, and danger states.
- Icon sizing and alignment drift.
- Dead CSS.
- Specificity wars.
- Excessive inline styles.
- Excessive `!important`.
- Deep brittle selectors.
- Component-local styles leaking globally.
- Global styles unexpectedly overriding components.
- Similar components styled differently without reason.
- Style docs inconsistent with implementation.

For each finding, provide:

- Title.
- Severity.
- Evidence.
- Observation.
- Why it matters.
- Minimal remediation.
- Confidence.
- Verification steps.

Also provide:

- Hardcoded-value inventory.
- Token drift inventory.
- Component drift table.
- Dead-style candidate table.
- Top 3–5 fixes.

Rules:

- Do not invent a new visual language.
- Prefer consolidating current patterns and tokens.