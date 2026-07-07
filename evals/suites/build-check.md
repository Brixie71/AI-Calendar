# Automated Web Gate Evaluation

## Pass Criteria

- Lockfile-enforced install succeeds.
- Format, lint, and type checks pass.
- Unit and integration tests pass.
- Production build succeeds.
- No unapproved dependency, generated artifact, secret, or unrelated file is introduced.

## Fail Criteria

- Any required command exits nonzero.
- Tests are skipped to obtain a pass.
- Build requires hand-editing generated output.
- New warnings indicate runtime, type, accessibility, or bundle regressions.
