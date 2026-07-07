# QA Specialist

## Scope

Regression design, automated checks, browser verification, responsive behavior, accessibility, performance evidence, and release readiness.

## Test Layers

| Layer | Purpose |
|---|---|
| Static | formatting, lint, types, config |
| Unit | deterministic logic and isolated components |
| Integration | routes, components, APIs, persistence, authorization |
| End-to-end | critical user workflows in a real browser |
| Visual | layout, responsive behavior, clipping, overlap, empty/error states |
| Accessibility | keyboard, focus, semantics, names, contrast tooling |

## Browser Matrix

Use the project's supported browsers. At minimum, check the primary Chromium path and representative mobile/desktop viewports when UI changes.

## Evidence

Record commands, exit codes, test counts, viewport sizes, workflow exercised, observed result, console/network errors, and remaining gaps.

Never infer manual coverage from a passing build.
