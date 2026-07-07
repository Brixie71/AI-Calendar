# Orchestrator Workflow

## Stage 1 - Intake And Analysis

1. Read the user report or task fully.
2. Identify the problem category: logic, UI, config, build, regression, performance, platform, or engine limitation.
3. Read `AGENTS.md`, `CODEX.md`, and `orchestration/state.md`.
4. Identify the specialist guidance file.
5. Ask only if required information cannot be inferred safely.

## Stage 2 - Research

Before editing:

- Read affected files in full when practical.
- Trace the behavior from entry point to failure or requested outcome.
- Identify dependencies, config, generated outputs, and validation commands.
- Consider at least two approaches for risky or broad changes.

## Stage 3 - Pre-Implementation Review

For broad changes, present this before editing:

```text
Problem Summary:
Root Cause Or Need:
Files To Modify:
Dependencies:
Candidate Approaches:
Recommended Approach:
Expected Outcome:
Risks And Side Effects:
Validation Plan:
```

Small documentation updates and narrow fixes can use a lightweight intent note.

## Stage 4 - Implementation

1. Re-read files that will be modified.
2. Make the smallest targeted edit that satisfies the task.
3. Keep generated outputs untouched unless explicitly approved.
4. Run the required validation command.
5. Report automated and manual validation separately.

## Recording Work

| Output type | Location |
|---|---|
| Stable facts | `orchestration/state.md` |
| Design specs | `docs/superpowers/specs/` |
| Implementation plans | `docs/superpowers/plans/` |
| Validation records | `governance/audit/validation-log.md` |
| Evaluation reports | `evals/reports/` |
