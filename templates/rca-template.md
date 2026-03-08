# RCA Template

> Copy this template to create a new entry in `operations/rca-log.md`.

---

## RCA-XXX: [Title]

**Date:** YYYY-MM-DD  
**Severity:** High / Medium / Low  
**Project:** [project name]

### What Happened

Brief description of the failure.

### Timeline

| Time | Event |
|------|-------|
| HH:MM | First symptom observed |
| HH:MM | Investigation started |
| HH:MM | Root cause identified |
| HH:MM | Fix applied |
| HH:MM | Verified resolved |

### Root Cause

What caused the failure. Be specific — not "it broke" but "the validation schema didn't handle null input, causing a runtime error when the optional field was missing."

### Contributing Factors

- Factor 1
- Factor 2

### Resolution

What was done to fix it.

### Prevention

What changes prevent recurrence:
- [ ] Code change: [description]
- [ ] Test added: [description]
- [ ] Process change: [description]

### Lessons

Add to `operations/lessons-learned.md` if the lesson is reusable.
