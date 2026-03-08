# Git Management Policy

> Commit, branch, and merge rules for this repository.

**Last updated:** YYYY-MM-DD

---

## Branch Strategy

| Branch | Purpose | Merges To |
|--------|---------|-----------|
| `main` | Stable, deployable code | — |
| `feat/<name>` | New features | `main` |
| `fix/<name>` | Bug fixes | `main` |
| `docs/<name>` | Documentation changes | `main` |
| `refactor/<name>` | Code cleanup | `main` |

---

## Commit Message Format

Use [Conventional Commits](https://www.conventionalcommits.org/):

```
<type>(<scope>): <description>

[optional body]
[optional footer]
```

### Types

| Type | Use For |
|------|---------|
| `feat` | New feature |
| `fix` | Bug fix |
| `docs` | Documentation only |
| `style` | Formatting, no logic change |
| `refactor` | Code change that neither fixes nor adds |
| `test` | Adding or updating tests |
| `chore` | Build process, tooling, dependencies |
| `perf` | Performance improvements |

### Scope (optional)

Use the project name or module name as scope.

### Examples

```
feat(auth): add login with email verification
fix(api): handle null response from external service
docs: add decision log entry for database choice
chore: update dependencies to latest versions
```

---

## Commit Eligibility Checklist

Before committing, verify:

- [ ] Code compiles without errors
- [ ] All existing tests pass
- [ ] No type system bypasses introduced
- [ ] Linting passes
- [ ] Commit message follows the format above
- [ ] No secrets or credentials in the diff

---

## Merge Readiness Checklist

Before merging to `main`:

- [ ] All commit eligibility checks pass
- [ ] Feature is complete (no half-implemented state)
- [ ] Documentation updated if architecture/contracts changed
- [ ] `current-state.md` reflects the change
- [ ] `board.md` updated if a task was completed

---

## When to Update This File

- When branching strategy changes
- When commit conventions are revised
- When new checks are added to the eligibility/readiness checklists
