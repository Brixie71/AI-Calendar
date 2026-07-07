# Automated Web Gate

Run applicable commands from a clean project root:

```text
[INSTALL_COMMAND]
[FORMAT_COMMAND]
[LINT_COMMAND]
[TYPECHECK_COMMAND]
[TEST_COMMAND]
[BUILD_COMMAND]
```

## Procedure

1. Use the locked package-manager version.
2. Install with lockfile enforcement suitable for CI.
3. Run format, lint, types, unit/integration tests, and production build.
4. Record exit codes and test counts.
5. Confirm no generated, secret, or unrelated files changed.

## Pass

Every required command exits zero; the production build completes; no unapproved dependency or generated-output change appears.
