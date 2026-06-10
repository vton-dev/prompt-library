You are auditing file handling in an existing codebase.

Review file upload, import, download, export, archive extraction, media processing, filesystem storage, filename handling, content validation, and file lifecycle controls.

Check for:

- File type validation missing.
- Blacklist validation instead of allowlist.
- Extension-only validation.
- MIME type trusted without verification.
- Magic number/content validation absent.
- File size limits missing.
- File count limits missing.
- Archive depth/size limits missing.
- ZIP slip or archive path traversal.
- ZIP/decompression bomb risk.
- Filename sanitization missing.
- User-controlled path or filename used directly.
- Path canonicalization missing.
- Files stored in public/webroot/executable locations.
- Uploaded content can be executed.
- Image/media processing library risk not handled.
- Malware scanning hooks absent where threat model requires them.
- Temporary files not cleaned.
- Existing files overwritten without confirmation.
- Sensitive exports not access-controlled.
- Downloads not authorized per object.
- Public file URLs without expiry or access control.
- Export files include hidden or sensitive fields.
- Unsafe Content-Type or Content-Disposition headers.
- File metadata logged unnecessarily.
- No tests for malformed, oversized, wrong-type, polyglot, or malicious archive files.

For each finding, provide:

- Title.
- Severity.
- CWE/OWASP reference if applicable.
- Evidence.
- Observation.
- Why it matters.
- Safe reproduction notes.
- Minimal remediation.
- Defense-in-depth guidance.
- Confidence.
- Verification steps.

Also provide:

- File flow inventory.
- Upload validation matrix.
- Archive safety table.
- Storage/download authorization table.
- Export leakage table.
- Top 3–5 fixes.

Rules:

- Do not include malware or destructive payloads.
- Use safe dummy filenames and harmless archive examples.
- Prefer allowlists, content validation, bounded processing, safe storage, canonicalization, per-object authorization, and expiring URLs.