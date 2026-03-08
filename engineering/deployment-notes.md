# Deployment Notes

> Deploy process, environment configurations, and infrastructure notes.

**Last updated:** YYYY-MM-DD

---

## Environments

| Environment | Purpose | URL |
|-------------|---------|-----|
| Development | Local development | `http://localhost:XXXX` |
| Staging | Pre-production testing | TBD |
| Production | Live application | TBD |

---

## Required Services

| Service | Purpose | Config Variable |
|---------|---------|-----------------|
| [e.g. PostgreSQL, MySQL, MongoDB] | Primary database | `DATABASE_URL` |
| [e.g. Redis, Memcached] | Cache / Sessions | `CACHE_URL` |

---

## Deploy Process

1. Ensure all tests pass
2. Ensure build succeeds
3. Set environment variables (see [data-contracts.md](data-contracts.md))
4. Run database migrations (if applicable)
5. Deploy to hosting platform

---

## Local Development

> Fill in with your project's actual setup commands.

```bash
git clone <repo-url>
cd <project-name>

# Install dependencies (choose your language's approach)
# npm install          ← Node.js
# pip install -r requirements.txt  ← Python
# go mod download      ← Go
# bundle install       ← Ruby

# Configure environment
cp .env.example .env.local  # Fill in values

# Start development server
# npm run dev           ← Node.js
# python manage.py runserver  ← Django
# go run cmd/server/main.go  ← Go
# rails server          ← Ruby
```

---

## Rollback

See [operations/rollback-plan.md](../operations/rollback-plan.md) for rollback procedures.

---

## When to Update This File

- When hosting or infrastructure changes
- When new environment variables are required
- When deploy process steps change
- When new services are added
