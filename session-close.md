# Session Close Checklist

> Run this checklist **before ending** every session.
> This is how you save context for the next agent (or yourself).
> **If you skip this, the next session starts from zero.**

**Last updated:** YYYY-MM-DD

---

## Checklist

### 1. Write Handoff Notes (CRITICAL)
- [ ] Open [current-state.md](current-state.md)
- [ ] Write **Handoff Notes** — freeform, for the next human/agent:
  - What you were working on
  - Where you stopped (file, function, component)
  - What's left to do
  - Any surprises or gotchas discovered
  - What the next session should do first
- [ ] If interrupted mid-task, fill in the **WIP Context** table:
  - Active task, branch, files being modified
  - Current error/blocker
  - What was tried, what to try next
- [ ] Add a row to the **Session Log**

### 2. Update Delivery Status
- [ ] Update [board.md](board.md) if any task status changed:
  - Move tasks: ⬜ → 🔄 → ✅ / ⏸
  - Update blocked tasks with blocker description
  - Add new tasks discovered during the session

### 3. Log Decisions and Lessons
- [ ] Log any significant decisions in [operations/decision-log.md](operations/decision-log.md)
- [ ] Log any reusable lessons in [operations/lessons-learned.md](operations/lessons-learned.md)
- [ ] Log any new risks in [operations/risk-register.md](operations/risk-register.md)

### 4. Handle Events (Check Trigger Matrix)
- [ ] Scan [trigger-matrix.md](trigger-matrix.md) — did any of these events occur?
  - Failure → `rca-log.md`
  - Incident → `incident-reports.md`
  - Rollback → `rollback-plan.md`
  - Architecture change → `architecture.md`
  - Release → `change-log.md`
  - New dependency → `repo-working-agreement.md`

### 5. Git Hygiene
- [ ] All work committed with proper messages per [git-management-policy.md](git-management-policy.md)
- [ ] No uncommitted changes left (or explained in Handoff Notes)
- [ ] Branch is in a clean, buildable state

### 6. Self-Check
- [ ] Re-read your Handoff Notes — would a stranger understand them?
- [ ] Are there orphan action items? → [operations/action-items-tracker.md](operations/action-items-tracker.md)
- [ ] Did you break the build? If yes, fix it before closing.

---

## Quick Close (Emergency — Minimum 2 Minutes)

If you absolutely must close immediately:

1. **[current-state.md](current-state.md)** → Write 3 sentences in Handoff Notes answering: *What was I doing? Where did I stop? What should happen next?*
2. **[board.md](board.md)** → Update any task status that changed

Everything else can wait, but these two **cannot**.

---

## When to Update This File

- When the session exit process changes
- When new end-of-session checks are identified as necessary
- When the trigger matrix adds new session-close requirements
