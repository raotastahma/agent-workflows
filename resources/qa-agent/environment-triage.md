# QA Environment and Browser Triage

Use only for connect/start/runtime/network/browser/token failures before setting `BLOCKED`.

## Environment

1. Run a fresh minimal probe; stale logs or prior context are not sufficient evidence.
2. Classify the failure: repository defect -> `IN_PROGRESS`; unresolved external/runtime/sandbox/credential/service dependency -> `BLOCKED`.
3. Inspect required local environment-key presence only; never print secrets, cookies, tokens, or full connection strings.
4. For a stopped or stale local Docker, Colima, Supabase, or related runtime, record its initial state, safely start/restart it when allowed, retry once, and restore the prior stopped state before reporting.
5. If the failure is sandbox-only and an approved host/rule-backed path exists, run the smallest equivalent verification there before blocking.
6. `BLOCKED` must include the exact command, error, blocker type, and smallest required user or host action.

## Local Browser QA

1. Prefer the repository browser command; otherwise use the installed Playwright Chromium project. Do not use remote CI or cloud browsers unless the task requires them.
2. Start the app on `127.0.0.1`, wait for readiness, source local environment only when required, and stop the server before reporting.
3. If the project already uses Playwright but Chromium binaries are missing, install only the Chromium browser binary; do not add a dependency.
4. A pre-page-load Chromium `bootstrap_check_in`, `MachPortRendezvousServer`, permission, sandbox, abort, or `chrome_exit=134` failure is an environment blocker, not a repository defect. Retry once with fresh temporary artifact and user-data directories, then use an approved host run when available.
5. If Playwright remains access-blocked, use the Codex in-app Browser for the smallest localhost, file, or current-tab flow that covers acceptance. Firecrawl requires both an explicit user request to use it and a public deployed URL; it cannot replace a local seeded flow.
6. Browser evidence records routes, viewports, reduced-motion state when relevant, horizontal-scroll result, critical console/page errors, and uncommitted artifact locations.
