# Browser Smoke Test

## Start

```text
[DEV_COMMAND]
```

## Procedure

1. Open the changed workflow at `[LOCAL_URL]`.
2. Test the primary happy path.
3. Test loading, empty, validation, server error, permission, and retry states where applicable.
4. Test keyboard navigation and visible focus.
5. Test representative desktop and mobile viewports.
6. Inspect browser console and failed network requests.
7. Verify refresh, back/forward navigation, deep links, and persistence when relevant.
8. Record browser, viewport, account/role, fixture data, and observed result.

## Pass

The workflow is usable without overlap, clipping, inaccessible controls, console errors, failed required requests, or adjacent regressions.
