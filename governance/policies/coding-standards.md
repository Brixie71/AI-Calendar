# Web Coding Standards

## Authority

Existing project conventions and configured formatters override generic preferences.

## Type And Data Safety

- Avoid unbounded `any`, unchecked casts, and silent parse failures.
- Validate external data at runtime even when TypeScript types exist.
- Model loading, success, empty, error, and unauthorized states explicitly.
- Keep API schemas and generated clients synchronized through approved tooling.

## Components

- Keep components focused on one coherent responsibility.
- Prefer composition over large prop matrices and speculative abstractions.
- Put reusable behavior in existing hooks/services/utilities only when reuse is real.
- Avoid state duplication and derived-state synchronization bugs.
- Keep stable keys and predictable controlled/uncontrolled input behavior.

## APIs And Server Code

- Separate transport, validation, authorization, business logic, and persistence.
- Return stable response shapes and intentional status codes.
- Do not expose stack traces, secrets, internal identifiers, or unnecessary personal data.
- Use transactions and idempotency where invariants require them.

## Styling And UX

- Use design tokens and established responsive breakpoints.
- Reserve cards for actual framed items, not every page section.
- Ensure content wraps and controls retain stable dimensions.
- Do not rely on color alone for state.
- Maintain visible focus and sufficient contrast.
- Prefer semantic controls over clickable generic containers.

## Comments

Explain non-obvious intent, browser constraints, concurrency, security boundaries, and compatibility decisions. Do not narrate obvious syntax.

## Completion Gate

- Formatting, lint, type checks, tests, and build pass.
- Browser console has no new errors.
- Changed workflows are verified at applicable desktop/mobile widths.
- Accessibility and security-sensitive behavior receive targeted checks.
