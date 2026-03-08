# Repository Working Agreement

> Execution rules for this project — structure, naming, and stack constraints.

**Last updated:** YYYY-MM-DD

---

## Project Structure

> Update this diagram to match your actual project layout.

```
project/
├── docs/          ← Documentation (this system)
├── src/           ← Source code
├── tests/         ← Tests (if not co-located)
└── ...
```

---

## General Rules

1. **Docs stay in `docs/`** — project documentation lives here
2. **No secrets in code** — use environment variables, never commit credentials
3. **Dependencies are explicit** — lock files must be committed, no phantom dependencies
4. **One source of truth** — don't duplicate information across files

---

## Stack Rules

> Fill in the table below with your project's required and forbidden technologies.

| Layer | Required | Forbidden |
|-------|----------|-----------|
| Language | [e.g. Python 3.12, TypeScript, Go, Rust] | [e.g. JavaScript (untyped)] |
| Framework | [e.g. Django, Next.js, FastAPI, Rails] | [e.g. Flask, CRA] |
| Styling | [e.g. Tailwind, SCSS, Material UI] | [e.g. Bootstrap] |
| State | [e.g. Zustand, Redux, Pinia] | [e.g. MobX] |
| ORM / DB | [e.g. SQLAlchemy, Drizzle, Prisma] | [e.g. raw SQL] |
| Testing | [e.g. pytest, Vitest, Jest, Go test] | — |
| Linting | [e.g. Ruff, ESLint, golangci-lint] | — |

---

## Naming Conventions

> Adjust conventions to match your language's idioms.

| What | Convention | Example |
|------|-----------|---------|
| Files | [e.g. kebab-case, snake_case] | `user-actions.ts`, `user_actions.py` |
| Classes/Components | [e.g. PascalCase] | `UserCard`, `UserService` |
| Functions | [e.g. camelCase, snake_case] | `validateRole()`, `validate_role()` |
| Types/Interfaces | [e.g. PascalCase] | `SessionData` |
| Env vars | UPPER_SNAKE_CASE | `DATABASE_URL` |
| Docs | kebab-case | `decision-log.md` |
| Branches | type/description | `feat/user-dashboard` |

---

## When to Update This File

- When stack rules change
- When naming conventions are revised
- When project structure changes
- When a new dependency is adopted or removed
