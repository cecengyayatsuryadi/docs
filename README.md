# Project Documentation System

> **Start here.** This is the durable operational memory for this project.
> Agents and humans should read this file at the beginning of every session.

**Last updated:** YYYY-MM-DD

---

## Quick Start

| Situation | Go To |
|-----------|-------|
| 🆕 **First time using this template?** | [setup-guide.md](setup-guide.md) → configure for your project |
| 🔄 **New session?** | [session-start.md](session-start.md) → load context |
| ✅ **Ending session?** | [session-close.md](session-close.md) → save context |
| 🔍 **Looking for a doc?** | [docs-map.md](docs-map.md) → full navigation |
| ⚡ **Something happened?** | [trigger-matrix.md](trigger-matrix.md) → what to update |
| 📋 **What's the current state?** | [current-state.md](current-state.md) → handoff notes + status |

---

## Documentation Structure

```
docs/
├── README.md                    ← You are here
├── setup-guide.md               ← First-time configuration
├── docs-map.md                  ← Full navigation with scope guidance
├── docs-governance.md           ← Ownership, update rules, quality standards
├── trigger-matrix.md            ← Events → required doc updates
├── current-state.md             ← Living project snapshot + handoff notes
├── board.md                     ← Sprint/task tracking with dependencies
├── session-start.md             ← Session entry checklist
├── session-close.md             ← Session exit checklist
├── team-working-agreement.md    ← Team principles + Definition of Done
├── repo-working-agreement.md    ← Project execution rules + stack constraints
├── agent-working-agreement.md   ← Agent rules + escalation triggers
├── git-management-policy.md     ← Commit + branch + merge rules
├── prompt-skill-sync.md         ← Prompt/skill update guidance
├── engineering/                 ← Architecture, standards, contracts, testing, deployment
├── operations/                  ← Decisions, incidents, risk, runbooks, QA, lessons
└── templates/                   ← Reusable templates for operational docs
```

---

## Key Documents

| Document | What It Does |
|----------|-------------|
| [current-state.md](current-state.md) | **Most critical.** Handoff notes, WIP context, project status |
| [board.md](board.md) | Sprint tasks, priorities, dependencies, blockers |
| [trigger-matrix.md](trigger-matrix.md) | 26 events → required doc updates (the enforcement mechanism) |
| [agent-working-agreement.md](agent-working-agreement.md) | Forbidden actions, escalation triggers, quality checklist |
| [operations/decision-log.md](operations/decision-log.md) | Decisions that must survive across sessions |
| [operations/lessons-learned.md](operations/lessons-learned.md) | Mistakes to never repeat |

---

## Design Principles

1. **Docs are memory** — if it's not written down, it doesn't exist next session
2. **Trigger-based updates** — update docs because an event happened, not because you remembered
3. **Scoped clearly** — every doc says what it's for and what it's not for
4. **Tiered operations** — 🟢 Core docs always active; 🟡 and ⚪ activate when needed
5. **Portable** — copy this `docs/` folder into any new repo to get started instantly
6. **Lightweight** — only maintain what's actually useful

---

## When to Update This File

- When the documentation structure changes materially
- When the quick-start workflow changes