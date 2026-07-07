# Repository Guidelines

## Operating Model

Codex works under product-owner and SQA authority.

The loop is: **Ask -> Suggest -> Wait -> Do.**

For a new objective:

1. Match it to one row in `CONTEXT-LOAD.md`.
2. Load only the listed guidance and affected source.
3. Present one concise approach with exact files and validation.
4. Wait for approval when the task changes behavior, architecture, dependencies, public APIs, data handling, authentication, deployment, or carries material regression risk.
5. Implement with focused tests.
6. Verify before claiming completion.

## Project Structure

Customize these values when installing this layer:

- `[SOURCE_ROOT]`: application source, usually `src/`, `app/`, or a workspace package.
- `[PUBLIC_ROOT]`: static public assets.
- `[TEST_ROOT]`: unit, integration, and end-to-end tests.
- `[CONFIG_FILES]`: package, framework, TypeScript, lint, test, and deployment config.
- `[GENERATED_OUTPUT]`: build, coverage, cache, generated clients, and framework output.

Preserve the framework's existing structure. Do not reorganize source merely to match this documentation.

## Required Commands

Define exact project commands:

```text
Install    : [INSTALL_COMMAND]
Development: [DEV_COMMAND]
Lint       : [LINT_COMMAND]
Types      : [TYPECHECK_COMMAND]
Unit tests : [TEST_COMMAND]
Build      : [BUILD_COMMAND]
E2E tests  : [E2E_COMMAND]
```

Run only applicable commands, but always run the full required gate before completion.

## Web Engineering Rules

- Follow the existing framework, router, data-fetching, state, styling, and component patterns.
- Keep server-only secrets and privileged logic out of browser bundles.
- Validate untrusted input at trust boundaries.
- Preserve authentication, authorization, CSRF, CORS, cookie, session, and cache semantics.
- Treat API contracts, database schemas, environment variables, routes, and exported component props as public interfaces.
- Build complete loading, empty, error, disabled, success, and permission-denied states.
- Maintain responsive behavior, keyboard access, focus visibility, semantic markup, and accessible names.
- Avoid layout shift, text overflow, incoherent overlap, and controls that resize when state changes.
- Use existing design tokens and icon libraries before adding new visual primitives.

## Testing

- Behavior changes and bug fixes use test-first development where practical.
- Unit tests cover deterministic logic.
- Integration tests cover component, route, API, persistence, and authorization boundaries.
- End-to-end tests cover critical user workflows.
- UI changes require browser verification at representative desktop and mobile widths.
- Accessibility-sensitive changes require keyboard and automated accessibility checks when tooling exists.
- Report automated and manual validation separately.

## Editing Rules

- Keep changes targeted and preserve unrelated local work.
- Do not edit generated output, dependency folders, caches, reports, logs, minified bundles, or secrets.
- Do not hand-edit lockfiles; update them only through the approved package manager.
- Do not add dependencies, alter deployment, or run migrations without approval.
- Use short, behavior-focused commits.

## Completion Report

```text
Done      : [implemented behavior]
Validated : [commands and browser scenarios]
Security  : [trust-boundary checks or not applicable]
Known gaps: [manual or environment-dependent coverage]
Next      : [recommended follow-up]
```
