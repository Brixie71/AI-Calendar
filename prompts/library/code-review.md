# Web Code Review Prompt

Lead with findings, ordered by severity.

## Review Areas

1. Runtime errors, broken routes, invalid imports, hydration failures, and missing registrations.
2. Authentication, authorization, injection, XSS, CSRF, SSRF, secret, upload, and privacy risks.
3. Data loss, race conditions, stale state, transaction, cache, retry, and idempotency defects.
4. API/schema compatibility and error/status behavior.
5. Loading, empty, error, permission, disabled, and success state regressions.
6. Keyboard, semantic, focus, accessible-name, contrast, responsive, overflow, and overlap defects.
7. Performance regressions supported by evidence.
8. Missing regression tests and unverified manual workflows.

Use precise file/line references. If no findings exist, state that clearly and list residual test gaps.
