# Web Development Operating Layer

## Design

The layer separates durable project guidance from application source:

- Root files define authority, workflow, and context loading.
- `agents/` assigns frontend, backend, security, QA, and orchestration responsibilities.
- `governance/` defines coding, scope, generated-file, and validation rules.
- `orchestration/` records project facts, commands, routing, and current decisions.
- `prompts/` provides repeatable implementation, review, and validation formats.
- `evals/` defines pass/fail criteria.
- `tests/` defines repeatable automated and browser procedures.
- `docs/superpowers/` stores approved designs and implementation plans.

## Layout

```text
PROJECT/
  AGENTS.md
  CODEX.md
  CONTEXT-LOAD.md
  agents/
    orchestrator/
    specialist/
      frontend-agent.md
      backend-agent.md
      security-agent.md
      qa-agent.md
  governance/
    policies/
    guardrails/
    audit/
  orchestration/
    router.md
    state.md
  prompts/library/
  evals/suites/
  tests/
    integration/
    manual/
  docs/
    architecture/
    superpowers/
      specs/
      plans/
```

## Application Compatibility

This layer does not prescribe application directories. Keep framework-native source layouts such as:

- `src/`, `app/`, `pages/`, or workspace packages;
- `public/` or framework asset directories;
- colocated or dedicated test directories;
- server, API, worker, database, and infrastructure packages.

Install the documentation around the application and replace placeholders with its actual commands and boundaries.
