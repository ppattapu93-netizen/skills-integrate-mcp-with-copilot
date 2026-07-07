# Project Issues — Mobile Integration

This file contains proposed issues to implement mobile support and related features.

## 1. Add Flutter mobile client scaffold (mobile-app)
- **Goal:** Create a minimal Flutter client that communicates with the existing FastAPI backend.
- **Scope:** Scaffold Flutter project, add screens: `Login`, `Activity List`, `Activity Detail`, `Signup`.
- **Acceptance:** App builds, lists activities from `/activities`, and can POST to `/activities/{name}/signup`.

## 2. Integrate mobile project into repository (mobile-integration)
- **Goal:** Add the mobile client to the repository as a `mobile/` directory or document how to include the external mobile repo.
- **Scope:** Add README entry, add ignore rules, and optionally add the mobile repo as a Git submodule.
- **Acceptance:** `mobile/` exists or docs reference the external app and provide clone instructions.

## 3. Add mobile CI workflow and README (mobile-ci)
- **Goal:** Create GitHub Actions that run Flutter analyze and widget tests on PRs.
- **Scope:** Add `.github/workflows/flutter.yml`, update project README with mobile build steps.
- **Acceptance:** CI runs on PR and reports status for Flutter tests.

## 4. Add persistent sync and offline support (mobile-sync)
- **Goal:** Implement a strategy for local persistence (e.g., `hive` or `sqflite`) and sync with backend.
- **Scope:** Define sync rules, data models, and implement basic caching for activity lists and signup queue.
- **Acceptance:** Mobile app shows cached activities offline and syncs queued signups when online.

## 5. Add authentication and roles to API (backend-auth)
- **Goal:** Add optional authentication (JWT or OAuth) and basic role support (student, admin) to backend endpoints.
- **Scope:** Protect signup/unregister endpoints, add login endpoint, and document token usage for mobile client.
- **Acceptance:** Mobile client can authenticate and receive a token to call protected endpoints.

## 6. Add mobile integration tests and e2e checks (mobile-tests)
- **Goal:** Implement widget and integration tests that validate signup/unregister flows against a test backend.
- **Scope:** Add example widget tests and integration test harness; optionally add Detox or Flutter driver scenarios.
- **Acceptance:** Tests run in CI and cover main flows.

---

If you'd like, I can also open these as GitHub Issues instead of adding them to `ISSUES.md` (requires GitHub Issues API permissions).