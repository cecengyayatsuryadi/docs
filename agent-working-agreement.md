# Agent Working Agreement

> Rules and rituals specific to **AI agents** operating in this repository.
> This document assumes the agent **cannot remember context across sessions**.

**Last updated:** YYYY-MM-DD

---

## Golden Rule

> **The repo docs are your memory. If you don't read them, you don't remember. If you don't write to them, the next agent forgets.**

---

## Session Entry (Mandatory)

Follow [session-start.md](session-start.md) — the full checklist is there.

**Critical reads before any work:**

1. [current-state.md](current-state.md) → Handoff Notes + WIP Context
2. [board.md](board.md) → what's the current priority
3. [repo-working-agreement.md](repo-working-agreement.md) → what are the rules

---

## Session Exit (Mandatory)

Follow [session-close.md](session-close.md) — the full checklist is there.

**Critical writes before ending:**

1. [current-state.md](current-state.md) → Handoff Notes (freeform context for next agent)
2. [current-state.md](current-state.md) → WIP Context (if interrupted mid-task)
3. [board.md](board.md) → task status changes
4. [trigger-matrix.md](trigger-matrix.md) → check if any events require additional doc updates

---

## Forbidden Actions

| # | Action | Why | Do This Instead |
|---|--------|-----|-----------------|
| F1 | Delete existing docs without reading them | Loses critical context | Read first, then improve or archive |
| F2 | Ignore lint or type errors | Build quality degrades silently | Fix before commit |
| F3 | Bypass the language's type system | Breaks type safety contract | Use the language's proper typing |
| F4 | Commit directly to main | Bypasses review, risks breakage | Use feature branches |
| F5 | Skip tests for critical paths | Regression risk compounds over time | Write tests, even minimal ones |
| F6 | Change project structure without logging | Future agents won't understand why | Log in `decision-log.md` first |
| F7 | Implement deferred/out-of-scope features | Scope creep, violates agreements | Check project's deferred list |
| F8 | Hardcode secrets or credentials | Security vulnerability | Use environment variables |
| F9 | Silence errors without logging | Hides bugs for future sessions | Log the error, then handle it |
| F10 | Install new dependencies without documenting | Phantom deps break other agents | Update `repo-working-agreement.md` |

---

## Escalation Triggers

The agent must **stop and ask the user** when:

| # | Trigger | Why |
|---|---------|-----|
| E1 | Task requires deleting or restructuring existing files | May lose work or break contracts |
| E2 | Requirements conflict with `decision-log.md` | Previous decision may still be valid |
| E3 | Test failure cannot be resolved in reasonable time | Avoid wasting tokens on rabbit holes |
| E4 | Task would change architecture in `engineering/architecture.md` | Architecture changes must be deliberate |
| E5 | Credentials or secrets needed | Agent must never create dummy secrets |
| E6 | Unsure about scope or context | Wrong context = wrong work |
| E7 | Estimated change affects >10 files | Large blast radius needs human review |
| E8 | Task involves database migration or schema change | Data loss risk |

---

## Error Handling Protocol

| Situation | Protocol |
|-----------|----------|
| Build/compile failure | Fix the error, do not skip. Log in `rca-log.md` if non-trivial |
| Test failure | Investigate root cause. Pre-existing? Note in `current-state.md` |
| Conflicting requirements | Check `decision-log.md` → still unclear? Escalate (E2) |
| Missing context | Search `docs/` → search project docs → still missing? Escalate |
| Dependency conflict | Check `repo-working-agreement.md` for allowed deps → escalate if ambiguous |
| Performance regression | Log in `rca-log.md`, note in `current-state.md`, add to `risk-register.md` |

---

## Documentation Triggers

When the agent causes or encounters these events, it must update docs per [trigger-matrix.md](trigger-matrix.md):

- Made a significant technical decision → `decision-log.md`
- Fixed a non-trivial bug → `rca-log.md`, `current-state.md`
- Changed architecture or data contracts → `architecture.md`, `data-contracts.md`
- Discovered a reusable lesson → `lessons-learned.md`
- Completed or changed a sprint task → `board.md`, `current-state.md`
- Encountered an incident or failure → `incident-reports.md`

---

## Agent Quality Checklist

Before marking any task as done, verify:

- [ ] Code runs without errors
- [ ] All existing tests still pass
- [ ] New critical code has tests (or documented reason why not)
- [ ] No type system bypasses, no lint errors
- [ ] No hardcoded secrets or credentials
- [ ] Changes are documented in appropriate docs
- [ ] `current-state.md` is updated
- [ ] Commit message follows `git-management-policy.md`

---

## When to Update This File

- When agent-specific rules change
- When new forbidden actions are identified from real mistakes
- When escalation triggers are revised based on experience
- When the error handling protocol needs new scenarios
