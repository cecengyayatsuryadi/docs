# Trigger Matrix

> Maps real events to required documentation updates. This is the core mechanism that makes docs update behavior **trigger-based** rather than memory-based.

**Last updated:** YYYY-MM-DD

---

## How to Use

When an event occurs during your work, find it in the table below and update all listed docs **before the session ends**.

---

## Event → Documentation Update Map

| Event | Required Updates | Optional Updates |
|-------|-----------------|------------------|
| **Meaningful failure** (build, test, deploy) | `operations/rca-log.md`, `current-state.md` | `operations/lessons-learned.md` |
| **Incident** (service down, data issue) | `operations/incident-reports.md`, `current-state.md` | `operations/rca-log.md`, `operations/blameless-incident-reviews.md` |
| **Rollback** | `operations/rollback-plan.md`, `operations/incident-reports.md`, `current-state.md` | `operations/rca-log.md` |
| **Significant decision** | `operations/decision-log.md` | `engineering/architecture.md` |
| **Architecture change** | `engineering/architecture.md`, `operations/decision-log.md` | `engineering/data-contracts.md` |
| **Testing expectation change** | `engineering/testing-strategy.md` | `operations/qa-test-plan.md` |
| **Sprint/task plan change** | `board.md` | `current-state.md` |
| **Task completed** | `board.md`, `current-state.md` | `operations/change-log.md` |
| **Release / deployment** | `operations/change-log.md`, `current-state.md` | `operations/qa-test-plan.md`, `operations/slo-sla-review.md` |
| **New risk identified** | `operations/risk-register.md` | — |
| **Data contract change** | `engineering/data-contracts.md` | `engineering/architecture.md` |
| **Code standard change** | `engineering/code-standards.md` | — |
| **Git rule change** | `git-management-policy.md` | — |
| **Team rule change** | `team-working-agreement.md` | `agent-working-agreement.md` |
| **Repo structure change** | `repo-working-agreement.md` | `docs-map.md`, `README.md` |
| **Reusable lesson discovered** | `operations/lessons-learned.md` | — |
| **Sprint end** | `operations/retrospectives.md`, `board.md` | `operations/action-items-tracker.md` |
| **New doc created** | `docs-map.md` | `README.md` |
| **Session end** (every time) | `current-state.md` | `board.md`, `operations/action-items-tracker.md` |
| **Prompt/skill change** | `prompt-skill-sync.md` | Relevant skill files |
| **Docs system change** | `docs-governance.md`, `docs-map.md` | `prompt-skill-sync.md` |
| **Dependency added/removed** | `repo-working-agreement.md` | `engineering/deployment-notes.md` |
| **Environment variable change** | `engineering/data-contracts.md` | `engineering/deployment-notes.md` |
| **Escalation needed** | Follow `operations/escalation-policy.md` | `current-state.md` |
| **Work interrupted mid-task** | `current-state.md` (WIP Context table) | `board.md` (mark ⏸ Blocked) |
| **Definition of Done not met** | Do not mark task ✅ in `board.md` | `current-state.md` (explain gap) |

---

## Minimum Session-Close Updates

Regardless of what happened, every session must update:

1. **`current-state.md`** — what changed, what's next
2. **`board.md`** — if any task status changed

---

## When to Update This File

- When new event types are identified
- When the required update list for an event changes
- When new docs are added to the system that should be trigger-driven
