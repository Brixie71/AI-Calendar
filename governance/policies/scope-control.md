# Scope Control

## Default

Make the smallest coherent change that satisfies the approved behavior and leaves adjacent workflows valid.

## Approval Required

Stop before:

- adding, removing, or upgrading dependencies;
- changing framework, package manager, build tooling, deployment, or source layout;
- changing public routes, API contracts, exported component props, environment variables, or database schemas;
- changing authentication, authorization, sessions, cookies, CORS, CSRF, security headers, or secret handling;
- adding analytics, tracking, external services, uploads, payments, email, or personal-data processing;
- broad design-system rewrites or global CSS resets;
- destructive migrations or production data operations.

## Protected Paths

Customize this list:

- dependency directories;
- framework build/cache output;
- coverage and reports;
- generated clients and schemas;
- environment files and secrets;
- deployment credentials;
- database snapshots and production exports.

## Dependencies

Use the project's existing libraries first. A new dependency needs a concrete capability, maintenance/security assessment, bundle/runtime impact, and approval.
