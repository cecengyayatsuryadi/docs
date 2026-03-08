# Rollback Plan

> How to revert a deployment or change safely. Not for general deployment process (see `engineering/deployment-notes.md`).

**Last updated:** YYYY-MM-DD

---

## When to Use

- A deployment causes user-facing errors
- A new feature breaks existing functionality
- Data corruption is detected after a migration
- Performance degrades significantly after a change

---

## General Rollback Procedure

### Code Rollback

```bash
# 1. Identify the last known good commit
git log --oneline -10

# 2. Revert to last good commit
git revert HEAD

# 3. Push the revert
git push origin main

# 4. Redeploy
# Follow deployment process in engineering/deployment-notes.md
```

### Database Rollback

1. **First:** Check if the migration is reversible
2. **If reversible:** Apply the reverse migration
3. **If not reversible:** Restore from backup
4. **Always:** Document what happened in `incident-reports.md` and `rca-log.md`

### Environment Variable Rollback

1. Revert environment variables to previous values
2. Restart the application
3. Verify functionality

---

## Project-Specific Notes

> Add project-specific rollback notes as needed, e.g.:
> - Database backup/restore procedures
> - Cache invalidation steps
> - Session/token handling after rollback

---

## Post-Rollback Checklist

- [ ] Service is restored and verified
- [ ] `incident-reports.md` updated
- [ ] `rca-log.md` updated if root cause is known
- [ ] `current-state.md` updated
- [ ] Team/user notified

---

## When to Update This File

- When rollback procedures change
- When new infrastructure is added
- After a rollback reveals missing steps
