# Escalation Policy

> When and how to escalate issues beyond the current agent or person.

**Last updated:** YYYY-MM-DD

---

## Escalation Triggers

| Trigger | Action | Escalate To |
|---------|--------|-------------|
| Task requires deleting or restructuring existing files | Stop work, document proposal | Project lead / user |
| Conflict with documented decision in `decision-log.md` | Stop work, present conflict | Project lead / user |
| Test failure cannot be resolved in reasonable time | Document attempts, pause | Project lead / user |
| Architecture change needed | Document rationale, propose ADR | Project lead / user |
| Missing credentials or secrets | Stop, do not create dummy values | Project lead / user |
| Unclear which project or branch to work in | Ask before proceeding | Project lead / user |
| Data loss risk | Stop immediately | Project lead / user |
| Security vulnerability discovered | Document privately, do not expose | Project lead / user |

---

## Escalation Format

When escalating, provide:

1. **What you're trying to do** (one sentence)
2. **What's blocking you** (one sentence)
3. **What you've tried** (bullet list)
4. **What you recommend** (if you have a recommendation)

---

## When to Update This File

- When escalation triggers are revised
- When escalation targets change
- When the escalation format needs adjustment
