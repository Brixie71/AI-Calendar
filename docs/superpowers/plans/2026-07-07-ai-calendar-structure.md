# AI Calendar Application Structure Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Create a Laravel backend plus React frontend workspace with FIXICS-style operating guidance, requirements capture, validation, and project-state tracking.

**Architecture:** `AI-Calendar` is the parent coordination workspace. `frontend/` owns the React application, `backend/` owns the Laravel API application, and root-level `docs/`, `governance/`, `orchestration/`, `agents/`, and `prompts/` guide future Codex sessions.

**Tech Stack:** React frontend, Laravel backend, Markdown governance/docs, future Node/npm and Composer tooling after requirements approval.

---

## File Structure

- Create `AGENTS.md`: Codex operating rules for this web app workspace.
- Create `CODEX.md`: canonical workflow and approval gates.
- Create `CONTEXT-LOAD.md`: objective-to-file map for future Codex sessions.
- Create `README.md`: short project overview and directory map.
- Create `orchestration/state.md`: current state and next decision tracking.
- Create `docs/templates/requirements-packet.md`: requirements packet template adapted for web app work.
- Create `docs/requirements/README.md`: requirement packet landing area.
- Create `docs/architecture/README.md`: architecture decision landing area.
- Create `docs/fixes/open-issues.md`: bug and follow-up issue registry.
- Create `frontend/README.md`: React frontend boundary.
- Create `backend/README.md`: Laravel backend boundary.

## Task 1: Create Root Operating Layer

**Files:**
- Create: `AGENTS.md`
- Create: `CODEX.md`
- Create: `CONTEXT-LOAD.md`
- Create: `README.md`
- Create: `orchestration/state.md`

- [ ] **Step 1: Write root Codex instructions**

Create `AGENTS.md` with:

```markdown
# AGENTS.md
# Repository Guidelines - AI Calendar

You are a delegator working under project-owner authority.
The project owner decides. You execute after approval.
Your loop is: Ask -> Suggest -> Wait -> Do.

## Project

AI Calendar is a web application workspace with a React frontend and Laravel backend.

- Frontend source: `frontend/`
- Backend source: `backend/`
- Shared project memory: `docs/`, `governance/`, `orchestration/`
- Generated output and dependency folders are never edited by hand.

## Required Workflow

1. Ask for the objective.
2. Match the objective to `CONTEXT-LOAD.md`.
3. Load only the mapped files.
4. Present a suggestion card and wait for approval.
5. Use a requirements packet for new features, architecture changes, or multi-step work.
6. Implement only after approval.
7. Run validation.
8. Update `orchestration/state.md`.

## Hard Rules

- Keep frontend and backend code separated.
- Do not introduce dependencies without approval.
- Do not edit generated output or dependency directories.
- Do not claim production readiness without validation.
```

- [ ] **Step 2: Write canonical workflow**

Create `CODEX.md` with:

```markdown
# Codex Working Guide

## Purpose

Codex collaborates with the project owner to design, build, validate, and document AI Calendar.

## Authority Order

1. `AGENTS.md`
2. `CODEX.md`
3. `governance/policies/`
4. `CONTEXT-LOAD.md`
5. Application source under `frontend/` and `backend/`

## Workflow

New application features start with a requirements packet in `docs/requirements/`.
Implementation plans live in `docs/superpowers/plans/`.
Design specs live in `docs/superpowers/specs/`.

## Validation

Frontend validation should use the project scripts once React is scaffolded.
Backend validation should use Laravel test commands once Laravel is scaffolded.
Until then, validate Markdown structure and path boundaries manually.
```

- [ ] **Step 3: Write context map**

Create `CONTEXT-LOAD.md` with:

```markdown
# CONTEXT-LOAD.md

Match one objective row. Load only those files.

| Objective | Load In Order |
|---|---|
| Requirements Packet | `docs/templates/requirements-packet.md` -> `orchestration/state.md` -> `docs/fixes/open-issues.md` |
| Frontend Feature | `frontend/README.md` -> `docs/requirements/[approved-packet].md` -> affected frontend files only |
| Backend Feature | `backend/README.md` -> `docs/requirements/[approved-packet].md` -> affected backend files only |
| Architecture Decision | `docs/architecture/README.md` -> `docs/templates/requirements-packet.md` -> `orchestration/state.md` |
| Validation / QA | `governance/audit/README.md` -> `docs/fixes/open-issues.md` |
| Bug Fix | `docs/fixes/open-issues.md` -> affected source files only |

If no row matches, ask the project owner to clarify.
```

- [ ] **Step 4: Write project README**

Create `README.md` with:

```markdown
# AI Calendar

AI Calendar is a web application workspace split into a React frontend and a Laravel backend.

## Structure

| Path | Purpose |
|---|---|
| `frontend/` | React application |
| `backend/` | Laravel API application |
| `docs/requirements/` | Approved requirements packets |
| `docs/architecture/` | Architecture notes and decisions |
| `docs/fixes/` | Open issues and fix memory |
| `orchestration/state.md` | Current project state |
| `governance/` | Policies, validation, and audit notes |
```

- [ ] **Step 5: Write state file**

Create `orchestration/state.md` with:

```markdown
# Project State

## Stable Facts

- Project name: AI Calendar.
- Type: Web application.
- Frontend: React, not scaffolded yet.
- Backend: Laravel, not scaffolded yet.
- Current goal: Prepare workspace structure and operating guidance.

## Last Decision

- Use one parent workspace with separated `frontend/` and `backend/` directories.
- Requirements will be drafted from a Codex CLI session opened inside this directory.

## Next Step

Draft the first application requirements packet in `docs/requirements/`.
```

- [ ] **Step 6: Verify files exist**

Run from `C:\Users\Jhon_Brix\Desktop\AI-Calendar`:

```powershell
Test-Path AGENTS.md
Test-Path CODEX.md
Test-Path CONTEXT-LOAD.md
Test-Path README.md
Test-Path orchestration\state.md
```

Expected: all commands return `True`.

## Task 2: Create Documentation and Requirement Areas

**Files:**
- Create: `docs/templates/requirements-packet.md`
- Create: `docs/requirements/README.md`
- Create: `docs/architecture/README.md`
- Create: `docs/fixes/open-issues.md`
- Create: `governance/audit/README.md`

- [ ] **Step 1: Create requirements template**

Create `docs/templates/requirements-packet.md` with:

```markdown
# Requirements Packet Template

## Objective

[Name the feature, research task, bug fix, or architecture change.]

## Current System State

- Frontend:
- Backend:
- Data model:
- Authentication:
- Known constraints:

## Files To Load

| Purpose | File |
|---|---|
| Session state | `orchestration/state.md` |
| Open issues | `docs/fixes/open-issues.md` |
| Frontend boundary | `frontend/README.md` |
| Backend boundary | `backend/README.md` |

## Questions And Answers

| Question | Answer | Decision Impact |
|---|---|---|
| [question] | [answer] | [impact] |

## Constraints

- Keep frontend and backend separated.
- Do not add dependencies without approval.
- Do not implement before requirements are approved.
- Keep validation commands explicit.

## Recommended Approach

1. Documentation/research:
2. Implementation plan:
3. Validation:
4. Owner handoff:

## Expected Output

- Files created:
- Files modified:
- Tests run:
- Manual QA focus:

## Validation Commands

```powershell
# Frontend, after scaffold exists
npm run build
npm test

# Backend, after scaffold exists
php artisan test
```
```

- [ ] **Step 2: Create docs landing files**

Create `docs/requirements/README.md` with:

```markdown
# Requirements

Store approved requirements packets here before implementation starts.
```

Create `docs/architecture/README.md` with:

```markdown
# Architecture

Store architecture decisions, API contracts, data model notes, and integration boundaries here.
```

Create `governance/audit/README.md` with:

```markdown
# Validation Audit

Record validation evidence, command outputs, and release-readiness notes here.
```

- [ ] **Step 3: Create open issues registry**

Create `docs/fixes/open-issues.md` with:

```markdown
# Open Issues

Track unresolved defects, missing decisions, and follow-up implementation notes here.

## Open Issues

No open issues recorded yet.
```

## Task 3: Create Frontend and Backend Boundaries

**Files:**
- Create: `frontend/README.md`
- Create: `backend/README.md`

- [ ] **Step 1: Create frontend boundary**

Create `frontend/README.md` with:

```markdown
# Frontend

React application boundary.

## Responsibility

- User interface
- Client-side routing
- API client calls to the Laravel backend
- Frontend tests and build scripts

## Not Responsible For

- Database schema
- Server-side authorization
- Background jobs
- Laravel API implementation
```

- [ ] **Step 2: Create backend boundary**

Create `backend/README.md` with:

```markdown
# Backend

Laravel application boundary.

## Responsibility

- API routes
- Authentication and authorization
- Database schema and migrations
- Server-side validation
- Background jobs and notifications

## Not Responsible For

- React components
- Browser routing
- Frontend-only state management
```

## Task 4: Handoff to New Codex CLI Session

**Files:**
- Read: `AGENTS.md`
- Read: `CODEX.md`
- Read: `CONTEXT-LOAD.md`
- Read: `orchestration/state.md`

- [ ] **Step 1: Open Codex CLI in workspace**

Run:

```powershell
cd C:\Users\Jhon_Brix\Desktop\AI-Calendar
codex
```

- [ ] **Step 2: Start with requirements objective**

Give Codex this objective:

```text
Draft the first Requirements Packet for the AI Calendar application. Start with product goals, user roles, calendar workflows, AI features, data model boundaries, frontend/backend responsibilities, validation commands, and approval gates. Do not scaffold React or Laravel until the packet is approved.
```

## Self-Review

- Spec coverage: The plan creates the approved parent workspace, separated frontend/backend areas, operating docs, requirements template, state tracking, and handoff path.
- Placeholder scan: Template placeholders are intentional fields for future requirements packets; implementation steps use concrete file paths and concrete content.
- Scope check: The plan does not scaffold React or Laravel. That belongs to the next Codex CLI session after application requirements are approved.
