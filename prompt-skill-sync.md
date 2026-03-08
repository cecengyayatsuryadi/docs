# Prompt & Skill Synchronization Guide

> When and how to update prompts, skills, and agent configuration alongside documentation changes.

**Last updated:** YYYY-MM-DD

---

## Concept

The documentation system and any reusable prompts/skills must stay in sync. If the docs define new rules or change existing processes, the agent prompts and skills that reference those rules must be updated in the same task.

---

## When to Update Prompts/Skills

| Trigger | What to Update |
|---------|----------------|
| Session ritual changes (`session-start.md`, `session-close.md`) | Any prompt that references session behavior |
| New forbidden actions added to `agent-working-agreement.md` | Agent system prompts, skill constraints |
| Escalation triggers change | Agent prompts, `escalation-policy.md` |
| Stack rules change in `repo-working-agreement.md` | Project-specific skills |
| Git policy changes | Git-management skills |
| Trigger matrix changes | Any prompt that references doc update behavior |
| New documentation category added | `docs-map.md`, session-start checklist |
| Testing strategy changes | Testing-related skills |

---

## Skill Inventory

> List all reusable skills in the repo. Update this table when skills are created or modified.

| Skill | Location | Purpose | Last Updated |
|-------|----------|---------|--------------|
| — | — | No skills registered yet | — |

---

## Synchronization Checklist

When making changes that affect both docs and skills:

1. [ ] Make the documentation change first
2. [ ] Identify affected prompts/skills from the table above
3. [ ] Update affected prompts/skills
4. [ ] Add the skill update to the same commit as the docs change
5. [ ] Update the skill inventory table above

---

## When to Update This File

- When new skills are created
- When the relationship between docs and skills changes
- When new synchronization triggers are identified
