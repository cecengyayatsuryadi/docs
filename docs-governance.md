# Documentation Governance

> Who owns what, when to update, and how to keep this system alive.

**Last updated:** YYYY-MM-DD

---

## Ownership Model

| Category | Owner | Review Cadence |
|----------|-------|----------------|
| Agreements (`team-`, `repo-`, `agent-`) | Project lead | On change, minimum monthly |
| Engineering docs | Any contributing agent/dev | On architecture or standards change |
| Operations docs (🟢 Core) | Session-active agent/dev | On event (see trigger matrix) |
| Operations docs (🟡 When Needed) | Session-active agent/dev | When first relevant event occurs |
| Operations docs (⚪ Enterprise) | Project lead | When team/service scale demands it |
| Delivery (`board.md`) | Session-active agent/dev | Every session close |
| Templates | Project lead | Quarterly or on process change |
| Governance (this file) | Project lead | On system structure change |
| Trigger matrix | Project lead | On new event type or process change |
| Setup guide | Project lead | On docs structure change |

---

## Update Rules

### Mandatory Updates (Trigger-Based)

These updates are driven by events, not memory. See [trigger-matrix.md](trigger-matrix.md) for the full mapping.

| Event | Must Update |
|-------|------------|
| Any session ends | `current-state.md` (Handoff Notes + Session Log) |
| Task status changes | `board.md` |
| Significant decision made | `operations/decision-log.md` |
| Incident occurs | `operations/incident-reports.md` |
| Architecture changes | `engineering/architecture.md`, `operations/decision-log.md` |
| Release deployed | `operations/change-log.md` |

### Recommended Updates (Discipline-Based)

| Cadence | Action |
|---------|--------|
| Monthly | Review `risk-register.md` for stale or resolved risks |
| After each release | Review `slo-sla-review.md` (if SLAs exist) |
| After each sprint | Run retrospective → `retrospectives.md` |
| Quarterly | Review `lessons-learned.md` for patterns |
| Quarterly | Review all docs for staleness (3-month rule) |

---

## Quality Standards

1. **Every doc must say what it's for** — "Use this for" / "Do not use this for" in `docs-map.md`
2. **Every doc must say when to update** — "When to Update" section at the bottom
3. **No stale docs** — if a doc hasn't been updated in 3 months, review or archive it
4. **No duplicate content** — if two docs describe the same thing, consolidate and cross-reference
5. **Dates matter** — every log entry and state doc must include a date
6. **Placeholders are not content** — `[Project Name]` and `YYYY-MM-DD` must be replaced before a doc is considered active
7. **Templates stay in `templates/`** — never edit a template directly; copy it to the target file

---

## Adding New Docs

1. Create the file in the appropriate directory
2. Add the file to [docs-map.md](docs-map.md) with "Use this for" / "Do not use this for"
3. If the doc type is trigger-driven, add it to [trigger-matrix.md](trigger-matrix.md)
4. If it needs a template, add one in `templates/`
5. Update [README.md](README.md) if it changes the overall structure
6. Log the addition in the Docs System Changelog below

## Archiving Docs

1. Move to `docs/archive/` (create if needed)
2. Remove from `docs-map.md`
3. Add a note to the archived file: `> **Archived on [date]. Reason: [reason]**`
4. Log the archival in the Docs System Changelog below

---

## Docs System Changelog

> Track structural changes to the documentation system itself.

| Date | Change | Reason |
|------|--------|--------|
| YYYY-MM-DD | Initial documentation system created | Agent memory unreliable — docs must serve as durable memory |

---

## When to Update This File

- When the ownership model changes
- When update rules or review cadence changes
- When quality standards are revised
- When the add/archive process changes
- When the docs system structure itself changes (log in changelog)
