# Setup Guide — First-Time Configuration

> Follow this guide after copying the `docs/` folder into your new project repo.
> Complete all steps before the first working session.

---

## Prerequisites

- A Git repository initialized
- Your project code (or scaffold) already exists
- A person or agent designated as initial docs owner

---

## Setup Checklist

### Step 1: Fill in Project Rules (15 min)

- [ ] **`repo-working-agreement.md`** — Fill in:
  - Project structure diagram
  - Stack Rules table (required/forbidden technologies)
  - Review naming conventions — adjust if needed
- [ ] **`team-working-agreement.md`** — Review and adjust:
  - Core principles — match your team culture
  - Definition of Done — adjust criteria for your project
- [ ] **`agent-working-agreement.md`** — Review:
  - Forbidden actions — add any project-specific ones
  - Escalation triggers — adjust for your context

### Step 2: Fill in Engineering Docs (30 min)

- [ ] **`engineering/architecture.md`** — Add:
  - Architecture diagram for your project
  - Key layers table
  - External services
- [ ] **`engineering/code-standards.md`** — Add:
  - Project stack table
  - Code patterns (✅ correct / ❌ wrong)
  - Import rules
  - UI standards (if your project has a frontend)
- [ ] **`engineering/data-contracts.md`** — Add:
  - Environment variables table
  - Key data shapes / types
  - API or server action patterns
- [ ] **`engineering/testing-strategy.md`** — Add:
  - Testing tool stack
  - Coverage targets
- [ ] **`engineering/deployment-notes.md`** — Add:
  - Environments table
  - Required services
  - Local development commands

### Step 3: Initialize State (10 min)

- [ ] **`current-state.md`** — Fill in:
  - Project Status section
  - First session log entry with today's date
- [ ] **`board.md`** — Fill in:
  - Current sprint name and period
  - Initial task list with priorities

### Step 4: Activate Core Operations Docs (10 min)

- [ ] **`operations/decision-log.md`** — Add initial ADRs:
  - ADR for each major technology choice already made
- [ ] **`operations/risk-register.md`** — Add initial risks:
  - Known technical risks, dependency risks
- [ ] **`operations/runbook.md`** — Add initial procedures:
  - How to start the dev server
  - How to run tests
  - How to run migrations (if applicable)

### Step 5: Configure Git Policy (5 min)

- [ ] **`git-management-policy.md`** — Review and adjust:
  - Branch strategy
  - Commit types and scope values

### Step 6: Replace All Placeholders (5 min)

```bash
# Find remaining placeholders
grep -rn "YYYY-MM-DD\|\[e.g." docs/ --include="*.md" | grep -v templates/
```

Replace all `YYYY-MM-DD` with today's date. Replace all example text with real values.

### Step 7: First Commit

```bash
git add docs/
git commit -m "docs: initialize documentation system"
```

---

## Post-Setup Verification

- [ ] `current-state.md` has Project Status filled in
- [ ] `board.md` has at least one task
- [ ] `decision-log.md` has at least one ADR
- [ ] `risk-register.md` has at least one risk
- [ ] `runbook.md` has at least one procedure
- [ ] No `YYYY-MM-DD` placeholders remain outside `templates/`:
  ```bash
  grep -rn "YYYY-MM-DD" docs/ --include="*.md" | grep -v templates/
  ```

---

## When to Update This File

- When the setup process changes
- When the docs structure changes enough to affect initial setup
