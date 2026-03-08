# Operations Documentation

> Operational docs for incidents, decisions, risk, runbooks, QA, and continuous improvement.
> Not all docs need to be active from day one — check the tier markers.

**Last updated:** YYYY-MM-DD

---

## Tier System

| Tier | Meaning | When to Activate |
|------|---------|-----------------|
| 🟢 **Core** | Always active. Every project needs these. | From day one |
| 🟡 **Activate When Needed** | Activate when the first relevant event occurs. | First incident, first release, first sprint end |
| ⚪ **Enterprise Scale** | For teams >3 people or production services with SLAs. | When team or service scale demands it |

---

## Index

| Document | Tier | Purpose | Trigger |
|----------|------|---------|---------|
| [decision-log.md](decision-log.md) | 🟢 Core | ADRs and technical decisions | After any significant decision |
| [risk-register.md](risk-register.md) | 🟢 Core | Known risks and mitigations | When risk identified |
| [lessons-learned.md](lessons-learned.md) | 🟢 Core | Reusable lessons discovered | When lesson discovered |
| [runbook.md](runbook.md) | 🟢 Core | Step-by-step operational procedures | When new procedure needed |
| [action-items-tracker.md](action-items-tracker.md) | 🟢 Core | Open action items from reviews | After any review |
| [change-log.md](change-log.md) | 🟡 When Needed | User-facing changes and releases | After any release |
| [rca-log.md](rca-log.md) | 🟡 When Needed | Root cause analysis of failures | After meaningful failure |
| [incident-reports.md](incident-reports.md) | 🟡 When Needed | Incident timeline and impact | After any incident |
| [qa-test-plan.md](qa-test-plan.md) | 🟡 When Needed | Release-specific test plans | Before release |
| [rollback-plan.md](rollback-plan.md) | 🟡 When Needed | How to revert safely | Before first deployment |
| [retrospectives.md](retrospectives.md) | 🟡 When Needed | Sprint/milestone process review | After sprint end |
| [playbook.md](playbook.md) | 🟡 When Needed | Strategic response guides | When new scenario identified |
| [blameless-incident-reviews.md](blameless-incident-reviews.md) | ⚪ Enterprise | Team learning from incidents | After significant incident (team >3) |
| [escalation-policy.md](escalation-policy.md) | ⚪ Enterprise | When/how to escalate | When team has escalation paths |
| [slo-sla-review.md](slo-sla-review.md) | ⚪ Enterprise | Service level tracking | When SLAs exist |

---

## Quick Decision: Which Ops Doc Do I Need?

```
Something failed?
├── Quick fix, root cause obvious → just fix it
├── Took >30 min to diagnose → rca-log.md
├── Service was down → incident-reports.md
└── Team should learn from it → blameless-incident-reviews.md

Made a choice?
├── Choosing between approaches → decision-log.md
├── Discovered a pattern → lessons-learned.md
└── Found a risk → risk-register.md

Shipping something?
├── Before release → qa-test-plan.md, rollback-plan.md
├── After release → change-log.md
└── End of sprint → retrospectives.md

Need to do something?
├── Step-by-step procedure → runbook.md
├── Judgment-based response → playbook.md
└── Can't resolve, need help → escalation-policy.md
```

---

## Relationship to Other Docs

- **Engineering questions** → [engineering/](../engineering/README.md)
- **Task/sprint tracking** → [board.md](../board.md)
- **Project state** → [current-state.md](../current-state.md)
- **Templates** → [templates/](../templates/)

---

## When to Update This Index

- When an operations doc is added or removed
- When tier assignments change
- When triggers change
