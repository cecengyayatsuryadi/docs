# Testing Strategy

> Testing approach, coverage targets, and tooling.

**Last updated:** YYYY-MM-DD

---

## Philosophy

1. **Test behavior, not implementation** — tests should verify what the code does, not how
2. **Critical paths first** — prioritize tests for auth, data mutations, and core business logic
3. **Fast feedback** — unit tests should run in under 10 seconds
4. **CI-ready** — all tests must be automatable

---

## Testing Stack

> Fill in with your actual testing tools.

| Layer | Tool | What to Test |
|-------|------|-------------|
| Unit | [e.g. pytest, Vitest, Jest, go test, RSpec] | Functions, validation, business logic |
| Integration | [e.g. pytest, Supertest, httptest] | API endpoints, service interactions |
| E2E | [e.g. Playwright, Cypress, Selenium] | Critical user flows |
| Lint | [e.g. Ruff, ESLint, golangci-lint, Rubocop] | Code quality |

---

## Coverage Targets

| Area | Target |
|------|--------|
| Critical paths (auth, data mutations) | 80%+ |
| Utility / helper functions | 80%+ |
| UI components (if applicable) | Key interactions only |
| E2E flows | Happy paths + critical error paths |

---

## Test File Conventions

> Adjust to match your language's conventions.

| Convention | Rule |
|-----------|------|
| File location | [e.g. co-located `*.test.*` or separate `tests/` dir] |
| Naming | [e.g. `test_*.py`, `*.test.ts`, `*_test.go`] |
| Setup | Use setup/teardown hooks for common setup |
| Mocking | Prefer dependency injection over global mocks |

---

## CI Pipeline (When Configured)

```
lint → type-check → unit-tests → build → e2e-tests
```

All steps must pass before merge.

---

## When to Update This File

- When testing tools or frameworks change
- When coverage targets are revised
- When testing patterns or conventions change
- When CI pipeline configuration changes
