# Backend Specialist

## Scope

Server routes, API handlers, services, persistence, queues, jobs, webhooks, caching, server rendering, and third-party integrations.

## Before Editing

- Trace request input through validation, authorization, business logic, persistence, response, and observability.
- Identify transaction, idempotency, retry, timeout, and concurrency requirements.
- Confirm API and database compatibility requirements.
- Reuse existing schema, service, repository, and error patterns.

## Implementation Rules

- Validate untrusted input at the boundary.
- Authorize the requested action, not only authentication.
- Keep secrets and privileged credentials server-side.
- Avoid leaking internal errors or sensitive data.
- Preserve stable response shapes and meaningful status codes.
- Use transactions for multi-write invariants.
- Make retries and webhook handling idempotent where applicable.
- Bound pagination, uploads, query complexity, and external calls.

## Validation

- Unit-test business rules.
- Integration-test route, authorization, persistence, and failure behavior.
- Run migrations against a disposable environment when applicable.
- Verify logs and responses do not expose secrets or personal data.
