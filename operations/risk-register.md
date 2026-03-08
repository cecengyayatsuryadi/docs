# Risk Register

> Known risks, their likelihood, impact, and mitigation plans.

**Last updated:** YYYY-MM-DD

---

## When to Add an Entry

- A technical risk is identified during development
- A dependency has known vulnerabilities or instability
- A process gap could lead to failures
- An external factor could impact delivery

---

## Risk Matrix

| ID | Risk | Likelihood | Impact | Mitigation | Status | Owner |
|----|------|-----------|--------|------------|--------|-------|
| R-001 | Agent loses context across sessions | High | High | Documentation system with session rituals | Mitigated | All |
| R-002 | [Example: Beta dependency may have breaking changes] | Medium | High | Pin version, monitor releases | Active | Dev |

---

## Severity Guide

| Likelihood | Definition |
|-----------|------------|
| High | Will likely happen |
| Medium | Could happen |
| Low | Unlikely |

| Impact | Definition |
|--------|------------|
| High | Blocks delivery, data loss, or security breach |
| Medium | Slows delivery, degraded experience |
| Low | Minor inconvenience, easy workaround |

---

## When to Update This File

- When a new risk is identified
- When a risk status changes (mitigated, accepted, resolved)
- When mitigation plans are updated
- Monthly review recommended
