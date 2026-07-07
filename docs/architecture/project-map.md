# Web Project Map

## Runtime Boundaries

```text
Browser
  -> routes/layouts/components
  -> client state and data fetching
  -> HTTP/RPC boundary
Server
  -> request validation
  -> authentication and authorization
  -> services/domain logic
  -> persistence, queues, and external integrations
Infrastructure
  -> build, deployment, secrets, observability
```

## Project Layout

```text
[PROJECT_NAME]/
  [SOURCE_ROOTS]/
  [PUBLIC_ROOT]/
  [TEST_ROOTS]/
  [CONFIG_FILES]/
  [GENERATED_OUTPUT]/
```

## Ownership Table

| Area | Owner | Public Contract | Validation |
|---|---|---|---|
| UI routes/components | Frontend | routes, props, user workflow | component, browser, accessibility |
| API/server | Backend | request/response schema | integration, authorization |
| Persistence | Backend | schema and invariants | migration, transaction tests |
| Identity and trust boundaries | Security | permissions, sessions, input rules | negative security tests |
| Release readiness | QA | acceptance criteria | full automated and manual gate |

Document actual module dependencies and prohibited imports when installing this template.
