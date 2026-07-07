# Context Loading

Load one row per objective. Do not scan unrelated source or guidance.

| Objective | Load In Order |
|---|---|
| Frontend feature or visual change | `agents/specialist/frontend-agent.md` -> `governance/policies/coding-standards.md` -> affected components/styles/tests |
| Frontend bug | `agents/specialist/frontend-agent.md` -> `agents/specialist/qa-agent.md` -> affected component and regression test |
| API or backend feature | `agents/specialist/backend-agent.md` -> `governance/policies/coding-standards.md` -> affected route/service/schema/tests |
| Authentication, authorization, secrets, or untrusted input | `agents/specialist/security-agent.md` -> `governance/policies/scope-control.md` -> affected trust boundary and tests |
| Database or migration work | `agents/specialist/backend-agent.md` -> `agents/specialist/security-agent.md` -> schema/migration/data-access tests |
| Performance issue | relevant frontend/backend specialist -> `agents/specialist/qa-agent.md` -> profiler evidence and affected source |
| Accessibility or responsive issue | `agents/specialist/frontend-agent.md` -> `agents/specialist/qa-agent.md` -> affected UI and browser tests |
| Build, dependency, CI, or deployment | `agents/orchestrator/workflow.md` -> `governance/policies/scope-control.md` -> relevant config and scripts |
| Code review | `prompts/library/code-review.md` -> affected diff and tests |
| Validation or release readiness | `agents/specialist/qa-agent.md` -> `prompts/library/validation-report.md` -> project commands |
| Architecture or broad feature | `agents/orchestrator/workflow.md` -> one approved spec -> one implementation plan |

If no row fits, ask for clarification before loading additional files.

## Mid-Task Lookups

Load additional context only to close a specific gap. State the gap before loading:

- Framework behavior: official framework documentation.
- Browser API behavior: MDN or the relevant standards source.
- Package behavior: official package documentation.
- Security behavior: framework security documentation, OWASP, or platform primary sources.
- Product behavior: approved product spec, issue, or SQA decision.

## Resume Rule

Read `orchestration/state.md`, summarize the last recorded decision in one sentence, and ask whether to resume before changing files.
