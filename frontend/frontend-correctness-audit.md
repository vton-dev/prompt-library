You are auditing frontend correctness in an existing codebase.

Review rendering, lifecycle behavior, async state, user interactions, forms, routing, service calls, and UI failure modes.

Check for:

- Missing cleanup for listeners, timers, subscriptions, observers, or events.
- Derived state stored unnecessarily.
- Effects/lifecycle hooks causing duplicate requests.
- Infinite render/update loops.
- Stale closures.
- Unstable dependencies causing unnecessary work.
- Components remounting unexpectedly due to unstable keys.
- Conditional rendering destroying user input.
- Loading states that can get stuck.
- Error states swallowed or overwritten.
- Results applied after component unmount.
- Older async response overwriting newer response.
- Missing cancellation or stale-request guards.
- Duplicate submit/click handling.
- Missing pending/disabled states during mutation.
- Optimistic updates without rollback.
- Presentational components importing service/runtime logic directly.
- Controlled/uncontrolled input problems.
- Blank, zero, false, null, undefined, and missing values mishandled.
- Numeric inputs unable to represent invalid intermediate input.
- UI allows values that backend/system rejects.
- File or record selectors not handling cancellation.
- Unsaved changes lost during navigation.
- Route/page state reset unexpectedly.

For each finding, provide:

- Title.
- Severity.
- Evidence.
- Observation.
- Why it matters.
- Reproduction steps.
- Minimal remediation.
- Suggested test.
- Confidence.
- Verification steps.

Also provide:

- Critical UI flow map.
- Component/hook findings table.
- Async race table.
- Form/input issue table.
- Top 3–5 fixes.

Rules:

- Do not redesign visual style.
- Prefer targeted component, hook, state, and service-call fixes.