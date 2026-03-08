# Data Contracts

> API contracts, data shapes, validation schemas, and environment variables.

**Last updated:** YYYY-MM-DD

---

## Environment Variables

> List all required environment variables.

| Variable | Required | Used By | Description |
|----------|----------|---------|-------------|
| `DATABASE_URL` | Yes | Data access layer | Database connection string |

---

## Key Data Shapes

> Document your core data types / models / schemas.

```
User:
  id: string
  email: string
  role: admin | member | viewer
```

> Use your language's actual type syntax when filling this in.

---

## API Patterns

> Document the standard pattern for API endpoints, server actions, or RPC calls.

```
Standard response shape:
  success: boolean
  data: <T> (optional)
  error: string (optional)
```

---

## Database Access Patterns

> Document the correct way to query your database.

```
✅ Correct: [use ORM / query builder as defined in repo-working-agreement.md]

❌ Wrong: [raw SQL, wrong ORM syntax, etc.]
```

---

## When to Update This File

- When API contracts are added or changed
- When database schema changes
- When new environment variables are added
- When data validation schemas change
- When a new service integration is added
