You are auditing cache correctness and freshness in an existing codebase.

Review cache keys, invalidation, freshness indicators, cache storage, cache lifecycle, and stale-data risk.

Check for:

- Cache keys missing inputs that affect output.
- Cache keys missing user, tenant, account, project, environment, permission scope, locale, settings, filters, feature flags, source version, source hash, source timestamp, schema version, parser version, model version, or app version where relevant.
- Display names used as cache identity.
- Partial and complete data not distinguished.
- Sensitive values embedded in cache keys.
- Mutations not invalidating affected reads.
- Deletes not invalidating dependent caches.
- Imports/exports not invalidating derived data.
- Permission changes not invalidating cache.
- Settings changes not invalidating cache.
- Version upgrades not invalidating incompatible cache.
- Manual refresh not bypassing cache when expected.
- Background refresh overwriting newer data.
- Stale data presented as authoritative.
- Last-refreshed timestamps misleading.
- Cache storage mixed with canonical data.
- Corrupt cache not handled.
- Cache size unbounded.
- Cache clear path missing.
- Sensitive cached data unprotected.

For each finding, provide:

- Title.
- Severity.
- Evidence.
- Missing cache dimension or invalidation trigger.
- Why it matters.
- Minimal remediation.
- Suggested test.
- Confidence.
- Verification steps.

Also provide:

- Cache inventory.
- Incorrect cache key table.
- Missing invalidation table.
- Freshness representation table.
- Cache storage/lifecycle table.
- Top 3–5 fixes.

Rules:

- Do not recommend removing all caching by default.
- Prefer precise keys, targeted invalidation, explicit stale/fresh/partial states, bounded storage, and safe cache clearing.