# CODEX.md

Web-development operating guide for `[PROJECT_NAME]`.

## Project Profile

- Product: `[PROJECT_NAME]`
- Application type: `[SPA | SSR | FULL_STACK | API | MONOREPO]`
- Framework: `[FRAMEWORK]`
- Runtime: `[RUNTIME]`
- Package manager: `[PACKAGE_MANAGER]`
- Source root: `[SOURCE_ROOT]`
- Test roots: `[TEST_ROOTS]`
- Deployment target: `[DEPLOYMENT_TARGET]`

## Authority

When guidance conflicts:

1. `AGENTS.md`
2. `CODEX.md`
3. `governance/policies/`
4. `CONTEXT-LOAD.md`
5. `agents/`
6. Actual source, framework configuration, and package scripts for implementation facts
7. Product owner and SQA for behavior and acceptance

## Session Start

Read silently:

1. `AGENTS.md`
2. `CODEX.md`
3. `orchestration/state.md`

Then ask: **"Ready. What are we working on?"**

Do not preload the repository. Route the objective through `CONTEXT-LOAD.md`.

## Task Lifecycle

1. **Intake**: identify the user, workflow, expected behavior, and acceptance criteria.
2. **Context**: load one objective row and affected source/tests.
3. **Research**: trace data flow, rendering, state, API, persistence, authorization, and failure states.
4. **Approval**: stop for behavior, architecture, dependency, public-interface, security, data, deployment, or broad design-system changes.
5. **Implementation**: use the smallest coherent change and test-first development.
6. **Verification**: run applicable static, test, build, browser, responsive, accessibility, and security checks.
7. **Handoff**: report evidence, limitations, and follow-up.

## Specialist Routing

| Topic | Guidance |
|---|---|
| UI, components, styling, browser behavior | `agents/specialist/frontend-agent.md` |
| APIs, server routes, persistence, jobs | `agents/specialist/backend-agent.md` |
| Authentication, authorization, secrets, input boundaries | `agents/specialist/security-agent.md` |
| Tests, browser verification, accessibility, regression | `agents/specialist/qa-agent.md` |
| Cross-cutting decomposition and approvals | `agents/orchestrator/workflow.md` |

## Required Verification

Configure applicable commands in `orchestration/state.md`.

Minimum source-change gate:

```text
[LINT_COMMAND]
[TYPECHECK_COMMAND]
[TEST_COMMAND]
[BUILD_COMMAND]
```

User-facing changes also require:

- Browser verification of the changed workflow.
- Desktop and mobile viewport checks.
- Loading, empty, error, and permission states where applicable.
- Keyboard and accessibility checks for interactive UI.

Never claim a browser workflow was verified unless it was actually launched and inspected.
