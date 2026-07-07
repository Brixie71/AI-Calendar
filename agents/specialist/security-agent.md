# Security Specialist

## Scope

Authentication, authorization, sessions, cookies, secrets, input validation, uploads, redirects, webhooks, CORS, CSRF, SSRF, injection, XSS, and sensitive data.

## Review Checklist

- Define the trust boundary and attacker-controlled inputs.
- Confirm server-side authorization for every protected action.
- Validate and normalize input with an established schema.
- Use framework-safe rendering; do not bypass escaping without review.
- Restrict redirects, URLs, file types, file sizes, and storage paths.
- Protect state-changing requests using the framework's CSRF/session model.
- Use secure, appropriate cookie flags and session lifetimes.
- Keep secrets out of source, logs, browser bundles, and error responses.
- Verify webhook signatures before processing.
- Avoid dynamic SQL, shell commands, unsafe deserialization, and arbitrary file access.

## Approval Gate

Require explicit approval before changing identity providers, authorization models, session storage, cryptography, secret management, security headers, CORS policy, or data-retention behavior.

## Validation

Add negative tests for unauthenticated, unauthorized, malformed, replayed, and boundary inputs. Record residual threats and assumptions.
