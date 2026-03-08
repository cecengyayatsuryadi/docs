# Team Working Agreement

> Principles and norms that apply to **all** contributors — human and agent — working on this project.

**Last updated:** YYYY-MM-DD

---

## Core Principles

1. **Write it down or it doesn't exist** — decisions, context, and state must be documented before a session ends
2. **Don't repeat mistakes** — if something fails, log it and the fix; future sessions must find it
3. **Scope before you build** — understand task boundaries before writing code
4. **Ask rather than assume** — when requirements are ambiguous, clarify before implementing
5. **Leave the repo better than you found it** — every session should result in useful work or useful documentation
6. **Small, reviewable changes** — prefer multiple small commits over one large one
7. **Fail fast, recover fast** — catch errors early with types, linting, and tests; fix them immediately

---

## Quality Standards

### Code Quality

- **Type safety** — use your language's type system fully; avoid dynamic typing escape hatches
- **Lint clean** — all code must pass the project's linter before commit
- **No dead code** — remove unused imports, functions, and variables
- **No TODOs without tracking** — if you write a TODO, add it to `operations/action-items-tracker.md`
- **Naming matters** — variables and functions should describe what they do, not how

### Testing

- **Critical paths must have tests** — auth, data mutations, business logic
- **Tests must be deterministic** — no flaky tests, no reliance on external services
- **Test behavior, not implementation** — tests survive refactors

### Code Review (Self-Review for Agents)

Before considering code complete, verify:

- [ ] Does it compile/run without errors?
- [ ] Would a new developer understand this code without explanation?
- [ ] Are there edge cases not handled?
- [ ] Are error messages helpful?
- [ ] Is there any hardcoded data that should be configurable?

---

## Definition of Done

A task is **done** when:

1. ✅ Code is implemented and runs without errors
2. ✅ Tests pass (existing + new where required)
3. ✅ Linting passes
4. ✅ Documentation is updated (architecture, data contracts, etc.)
5. ✅ `current-state.md` reflects the change
6. ✅ `board.md` task status is updated
7. ✅ Code is committed with proper commit message
8. ✅ No known regressions introduced

---

## Communication Norms

- Use documentation as the primary communication channel (agents cannot use Slack/email)
- Significant decisions → `operations/decision-log.md`
- Blockers → `current-state.md` (Handoff Notes)
- Questions that can't be answered → `operations/action-items-tracker.md`
- Lessons worth sharing → `operations/lessons-learned.md`

---

## Conflict Resolution

1. Check `operations/decision-log.md` for prior decisions on the topic
2. If no prior decision exists, document the options and pick the simplest one
3. If the choice is high-impact, escalate per `operations/escalation-policy.md`
4. Log the resolution in `operations/decision-log.md`

---

## When to Update This File

- When team principles change
- When quality standards are revised
- When definition of done criteria change
- When communication or conflict resolution norms evolve
