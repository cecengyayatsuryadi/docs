# Documentation Map

> Full navigation guide. Every doc in the system is listed here with its purpose and usage scope.

**Last updated:** YYYY-MM-DD

---

## How to Use This File

- Scan this file to find the right document for your need
- Every entry includes **"Use this for"** and **"Do not use this for"** to prevent overlap
- If you create a new doc, add it here

---

## Core Navigation

| File | Purpose |
|------|---------|
| [README.md](README.md) | Entry point, quick-start, structure overview |
| [setup-guide.md](setup-guide.md) | First-time repo configuration checklist |
| [docs-map.md](docs-map.md) | This file — full navigation |
| [docs-governance.md](docs-governance.md) | Ownership, update cadence, quality standards, docs changelog |
| [current-state.md](current-state.md) | Living project snapshot — **handoff notes, WIP context, status** |
| [trigger-matrix.md](trigger-matrix.md) | Events → required doc updates (24 event types) |
| [prompt-skill-sync.md](prompt-skill-sync.md) | Prompt/skill update guidance |

---

## Setup

### [setup-guide.md](setup-guide.md)
- **Use this for:** First-time configuration of this docs system in a new repo
- **Do not use this for:** Ongoing docs maintenance (use `docs-governance.md`)

---

## Agreements

### [team-working-agreement.md](team-working-agreement.md)
- **Use this for:** Team-wide principles, communication norms, quality standards, Definition of Done
- **Do not use this for:** Repo-specific rules (use `repo-working-agreement.md`), agent-specific rules (use `agent-working-agreement.md`)

### [repo-working-agreement.md](repo-working-agreement.md)
- **Use this for:** Repo structure rules, naming conventions, project-specific stack constraints
- **Do not use this for:** General team principles (use `team-working-agreement.md`), git rules (use `git-management-policy.md`)

### [agent-working-agreement.md](agent-working-agreement.md)
- **Use this for:** Agent forbidden actions (F1–F10), escalation triggers (E1–E8), error handling protocol, quality checklist
- **Do not use this for:** Human team norms (use `team-working-agreement.md`), engineering standards (use `engineering/`)

---

## Session Rituals

### [session-start.md](session-start.md)
- **Use this for:** Ordered checklist to run at the start of every session — loads handoff notes and WIP context
- **Do not use this for:** Ongoing work tracking (use `board.md` or `current-state.md`)

### [session-close.md](session-close.md)
- **Use this for:** Ordered checklist for writing handoff notes, updating state, and saving context before ending
- **Do not use this for:** Sprint retrospectives (use `operations/retrospectives.md`)

---

## Engineering

### [engineering/README.md](engineering/README.md)
- **Use this for:** Index of engineering docs, finding the right engineering reference

### [engineering/architecture.md](engineering/architecture.md)
- **Use this for:** System architecture, component relationships, integration points
- **Do not use this for:** Implementation details or code patterns (use `code-standards.md`)

### [engineering/code-standards.md](engineering/code-standards.md)
- **Use this for:** Coding conventions, patterns, style rules, UI standards (if applicable)
- **Do not use this for:** Architecture decisions (use `architecture.md`), data shapes (use `data-contracts.md`)

### [engineering/data-contracts.md](engineering/data-contracts.md)
- **Use this for:** API contracts, data shapes, validation schemas, type definitions
- **Do not use this for:** Database schema (use `architecture.md`), code patterns (use `code-standards.md`)

### [engineering/testing-strategy.md](engineering/testing-strategy.md)
- **Use this for:** Testing approach, coverage targets, test tooling, test patterns
- **Do not use this for:** QA test plans for specific releases (use `operations/qa-test-plan.md`)

### [engineering/deployment-notes.md](engineering/deployment-notes.md)
- **Use this for:** Deploy process, environment configs, infrastructure notes
- **Do not use this for:** Rollback procedures (use `operations/rollback-plan.md`), incident response (use `operations/runbook.md`)

---

## Operations

### [operations/README.md](operations/README.md)
- **Use this for:** Index of operations docs, finding the right ops reference

### [operations/rca-log.md](operations/rca-log.md)
- **Use this for:** Root cause analysis of significant failures
- **Do not use this for:** Quick incident notes (use `incident-reports.md`), general lessons (use `lessons-learned.md`)

### [operations/incident-reports.md](operations/incident-reports.md)
- **Use this for:** Documenting what happened during an incident, timeline, impact
- **Do not use this for:** Deep root cause analysis (use `rca-log.md`), team process review (use `blameless-incident-reviews.md`)

### [operations/retrospectives.md](operations/retrospectives.md)
- **Use this for:** Sprint or milestone retrospectives — what went well, what didn't, actions
- **Do not use this for:** Incident-specific reviews (use `blameless-incident-reviews.md`), individual RCAs (use `rca-log.md`)

### [operations/blameless-incident-reviews.md](operations/blameless-incident-reviews.md)
- **Use this for:** Team-level learning from incidents without assigning blame
- **Do not use this for:** Technical root cause (use `rca-log.md`), sprint process (use `retrospectives.md`)

### [operations/decision-log.md](operations/decision-log.md)
- **Use this for:** Architecture decisions (ADRs), significant technical choices that must survive sessions
- **Do not use this for:** Sprint planning (use `board.md`), risk assessment (use `risk-register.md`)

### [operations/runbook.md](operations/runbook.md)
- **Use this for:** Step-by-step operational procedures for known scenarios
- **Do not use this for:** Strategic guidance (use `playbook.md`), deployment (use `engineering/deployment-notes.md`)

### [operations/playbook.md](operations/playbook.md)
- **Use this for:** Strategic response guides for complex situations
- **Do not use this for:** Exact step-by-step procedures (use `runbook.md`), escalation paths (use `escalation-policy.md`)

### [operations/escalation-policy.md](operations/escalation-policy.md)
- **Use this for:** When and how to escalate issues beyond the current agent/person
- **Do not use this for:** Response procedures (use `runbook.md` or `playbook.md`)

### [operations/risk-register.md](operations/risk-register.md)
- **Use this for:** Known risks, their likelihood, impact, and mitigation plans
- **Do not use this for:** Active incidents (use `incident-reports.md`), decisions (use `decision-log.md`)

### [operations/change-log.md](operations/change-log.md)
- **Use this for:** User-facing changes, releases, version history
- **Do not use this for:** Git commit history (use git log), internal refactors (use `decision-log.md`)

### [operations/qa-test-plan.md](operations/qa-test-plan.md)
- **Use this for:** Test plans for specific releases, QA checklists, acceptance criteria
- **Do not use this for:** Long-term testing strategy (use `engineering/testing-strategy.md`)

### [operations/rollback-plan.md](operations/rollback-plan.md)
- **Use this for:** How to revert a deployment or change safely
- **Do not use this for:** General deployment process (use `engineering/deployment-notes.md`)

### [operations/slo-sla-review.md](operations/slo-sla-review.md)
- **Use this for:** Service level objectives/agreements and their current status
- **Do not use this for:** Incident response (use `runbook.md`), risk tracking (use `risk-register.md`)

### [operations/action-items-tracker.md](operations/action-items-tracker.md)
- **Use this for:** Tracking action items from retrospectives, incidents, and reviews
- **Do not use this for:** Sprint task tracking (use `board.md`), long-term decisions (use `decision-log.md`)

### [operations/lessons-learned.md](operations/lessons-learned.md)
- **Use this for:** Reusable lessons discovered during development and operations
- **Do not use this for:** Incident-specific analysis (use `rca-log.md`), process retrospectives (use `retrospectives.md`)

---

## Delivery

### [board.md](board.md)
- **Use this for:** Sprint/task tracking, current delivery status, backlog
- **Do not use this for:** Architecture decisions (use `operations/decision-log.md`), project state summary (use `current-state.md`)

---

## Git

### [git-management-policy.md](git-management-policy.md)
- **Use this for:** Commit rules, branch naming, merge readiness, commit types
- **Do not use this for:** Deployment process (use `engineering/deployment-notes.md`), code standards (use `engineering/code-standards.md`)

---

## Templates

| Template | Use for |
|----------|---------|
| [templates/rca-template.md](templates/rca-template.md) | Creating new RCA entries |
| [templates/incident-report-template.md](templates/incident-report-template.md) | Creating new incident reports |
| [templates/decision-record-template.md](templates/decision-record-template.md) | Creating new ADR / decision log entries |
| [templates/sprint-plan-template.md](templates/sprint-plan-template.md) | Creating new sprint plans |
| [templates/retrospective-template.md](templates/retrospective-template.md) | Creating new retrospectives |
| [templates/task-report-template.md](templates/task-report-template.md) | Creating sprint task completion reports |

---

## When to Update This File

- When any doc file is added, renamed, or removed
- When a doc's purpose or scope changes
- When a new documentation category is created
