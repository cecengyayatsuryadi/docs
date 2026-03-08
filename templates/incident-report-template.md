# Incident Report Template

> Copy this template to create a new entry in `operations/incident-reports.md`.

---

## INC-XXX: [Title]

**Date:** YYYY-MM-DD  
**Severity:** 1 (Critical) / 2 (Major) / 3 (Minor)  
**Status:** Active / Resolved / Post-mortem Complete  
**Project:** [project name]

### Summary

One-paragraph description of the incident.

### Impact

- **Users affected:** [number/description]
- **Duration:** [start time] to [end time]
- **Data impact:** None / Partial / Full

### Timeline

| Time | Event |
|------|-------|
| HH:MM | Incident detected |
| HH:MM | Response started |
| HH:MM | Root cause identified |
| HH:MM | Mitigation applied |
| HH:MM | Service restored |

### Root Cause

Brief root cause (detailed RCA in `rca-log.md` if warranted).

### Resolution

What was done to resolve the incident.

### Follow-Up Actions

| Action | Owner | Due | Status |
|--------|-------|-----|--------|
| Action 1 | — | — | — |

> Track in `operations/action-items-tracker.md`

### Blameless Review

Link to blameless review if conducted: [blameless-incident-reviews.md]
