# Lessons Learned

> Reusable lessons discovered during development and operations. Not incident-specific (use `rca-log.md` for that).

**Last updated:** YYYY-MM-DD

---

## When to Add an Entry

- A pattern is discovered that saves significant time
- A mistake is made that others should avoid
- A workaround is found for a library/framework limitation
- A process improvement is identified
- An anti-pattern is discovered in the codebase or workflow

---

## Lessons

### LL-001: Agent context loss is the #1 risk

**Context:** AI agents lose all memory between sessions.  
**Lesson:** Every session must start by reading docs and end by updating them. Documentation is not optional — it's the project's memory.  
**Action:** Session start/close checklists are mandatory for all agents.

### LL-002: Check deferred features before implementing

**Context:** Projects often have explicit v2 or out-of-scope features.  
**Lesson:** Agents may eagerly implement features that are explicitly deferred. Always check the project's deferred features or out-of-scope list before building something new.  
**Action:** Verify feature is in scope before starting work.

---

## Known Anti-Patterns

> Things that have gone wrong before. If you're about to do one of these, stop.

| ID | Anti-Pattern | Why It's Bad | Do This Instead |
|----|--------------|-------------|-----------------|
| AP-001 | Using wrong library/framework syntax | Silent failures or runtime errors | Check `repo-working-agreement.md` for allowed stack |
| AP-002 | Installing dependencies without checking the allowed stack | Phantom deps, inconsistent builds | Check `repo-working-agreement.md` first |
| AP-003 | Writing "I'll document it later" | It never happens | Document during the same session |

---

## When to Update This File

- When a reusable lesson is discovered
- When a previous lesson is validated or invalidated by new experience
- When a new anti-pattern is identified from real mistakes
- Cross-reference from `rca-log.md` when an RCA produces a generalizable lesson
