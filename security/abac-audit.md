You are auditing attribute-based access control in an existing codebase.

Determine whether ABAC is designed and enforced correctly. If the codebase does not implement ABAC, state that clearly and describe the current model instead, such as RBAC, ACL, ownership checks, tenant checks, or ad hoc authorization.

Use NIST SP 800-162 concepts:

- Subject attributes.
- Object/resource attributes.
- Action/operation attributes.
- Environment/context attributes.
- Policy Enforcement Point.
- Policy Decision Point.
- Policy Information Point.
- Policy Administration Point.

Inventory:

- Policy definitions.
- Policy evaluators.
- Guards/middleware.
- Route/handler authorization.
- Service-level authorization.
- Query-level filters.
- Serializers/field projection.
- User/session/tenant/resource models.
- Attribute sources.
- Attribute caches.
- Policy tests.
- Audit logs.

Check for:

- ABAC claimed but implemented as scattered role checks.
- No explicit policy model.
- Subject, object, action, or environment attributes missing from decisions.
- Attribute source of truth unclear.
- Client-provided attributes trusted.
- JWT/session claims trusted without freshness checks for sensitive decisions.
- Object/resource attributes not loaded before authorization.
- Tenant or ownership not represented as object attributes.
- Policy rules embedded directly in controllers or UI.
- Policy evaluation duplicated across modules.
- No deny-by-default behavior.
- Missing or stale attributes fail open.
- Attribute lookup errors fail open.
- No policy combining rule for multiple applicable policies.
- PEP and PDP responsibilities blurred.
- PIP strategy missing for authoritative attributes.
- Policy administration/change control missing.
- Policy versioning missing.
- No audit logging of subject, object, action, decision, policy version, and reason.
- Bulk operations not evaluated per object.
- Field-level ABAC missing.
- List/search queries not filtered at query time.
- Attribute cache has no TTL, invalidation, version, or provenance.
- No negative tests for missing, stale, conflicting, or forged attributes.

For each finding, provide:

- Title.
- Severity.
- Standard reference: NIST SP 800-162 / OWASP Broken Access Control / CWE.
- Evidence: file, policy/function/guard/model/test, line range.
- Observation.
- Why it matters.
- Minimal remediation.
- Suggested policy contract or test.
- Confidence.
- Verification steps.

Also provide:

- ABAC applicability statement.
- Current authorization model summary.
- Subject/object/action/environment attribute inventory.
- PEP/PDP/PIP/PAP map.
- Enforcement coverage matrix.
- Attribute provenance table.
- Fail-open risk table.
- Attribute freshness/cache risk table.
- Top 3–5 fixes.

Rules:

- Do not invent business policy.
- Do not force ABAC if RBAC/ACL is sufficient for the product risk.
- Prefer authoritative attributes, centralized policy decisions, query-level scoping, field projection, deny-by-default, and audit logging.