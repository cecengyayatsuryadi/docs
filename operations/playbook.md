# Playbook

> Strategic response guides for complex situations. Unlike runbooks (exact steps), playbooks provide decision frameworks.

**Last updated:** YYYY-MM-DD

---

## When to Add an Entry

- A situation requires judgment, not just steps
- Multiple response paths are possible depending on context
- Team needs a shared mental model for complex scenarios

---

## Playbooks

### PLAY-001: Agent Encounters Unknown Architecture

**Situation:** Agent is asked to modify code in an area not covered by existing docs.

**Response framework:**
1. Search `engineering/architecture.md` and `operations/decision-log.md` for related context
2. Read surrounding code to understand patterns before modifying
3. If the modification would change data flow or component boundaries, **stop and escalate**
4. If modification is local (within one component), proceed with caution and log the decision
5. Update `engineering/architecture.md` if you discover undocumented architecture

### PLAY-002: Conflicting Requirements

**Situation:** User request conflicts with documented decisions or constraints.

**Response framework:**
1. Check `operations/decision-log.md` for the conflicting decision
2. If the decision is still valid, explain the conflict to the user
3. If circumstances have changed, propose updating the decision (create new ADR)
4. Never silently override a documented decision

### PLAY-003: Build Failure on Fresh Checkout

**Situation:** Project doesn't build after cloning or starting a new session.

**Response framework:**
1. Check `current-state.md` — is there a known issue?
2. Install dependencies (check `engineering/deployment-notes.md` for commands)
3. Check environment variables are set
4. Check external services are accessible (database, cache, etc.)
5. If build still fails, log in `operations/rca-log.md` and update `current-state.md`

---

## When to Update This File

- When a new complex scenario pattern is identified
- When an existing playbook's response framework needs revision
