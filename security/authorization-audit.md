You are auditing authorization enforcement in an existing codebase.

Review all sensitive operations for broken access control, IDOR/BOLA, privilege escalation, missing object-level checks, missing function-level checks, missing tenant isolation, and field-level exposure.

Use OWASP Broken Access Control, OWASP ASVS, least privilege, deny-by-default, object-level authorization, function-level authorization, and tenant isolation.

Inventory sensitive operations:

- Read.
- List.
- Search.
- Create.
- Update.
- Delete.
- Export.
- Import.
- Share.
- Invite.
- Approve.
- Administer.
- Impersonate.
- Billing/payment.
- Role/permission change.
- API key/token management.
- Bulk actions.

Check for:

- Object IDs in route/body/query can be changed to access another user’s or tenant’s data.
- Missing ownership checks.
- Missing tenant checks.
- Tenant, owner, role, or scope accepted from client input.
- Authorization performed only in UI/client code.
- Privileged operations without server-side/system-side checks.
- Middleware or guard order incorrect.
- Nested routers, subcommands, jobs, or service methods bypass authorization.
- Bulk operations authorize only once instead of per item.
- List/search queries not scoped by tenant/owner at query time.
- Field-level authorization missing for secrets, tokens, PII, billing, admin fields, or internal status.
- Mass assignment allows role, tenantId, ownerId, isAdmin, status, emailVerified, quota, plan, or permissions changes.
- API token scopes not enforced.
- User tokens and service tokens not distinguished.
- Debug/admin/reset/seed routes exposed.
- Authorization decisions not logged for sensitive operations.

For each finding, provide:

- Title.
- Severity.
- CWE/OWASP reference.
- Evidence: file, route/handler/policy/query/serializer, line range.
- Observation.
- Why it matters.
- Safe minimal reproduction using dummy IDs.
- Minimal remediation.
- Defense-in-depth guidance.
- Confidence.
- Verification steps.

Also provide:

- Operation-to-permission matrix.
- IDOR/BOLA risk table.
- Function-level authorization table.
- Field-level exposure table.
- Bulk operation table.
- Tenant isolation table.
- Risk score from 0–10.
- Top 3–5 fixes.

Rules:

- Do not use real IDs, tokens, or tenant data.
- Prefer centralized policy checks, query-level tenant scoping, per-object authorization, field projection, and deny-by-default.