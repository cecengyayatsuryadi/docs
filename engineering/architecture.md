# Architecture

> High-level system architecture for this project.

**Last updated:** YYYY-MM-DD

---

## System Architecture

> Replace the diagram below with your actual architecture.
> Choose the pattern that matches your project type.

**Web application:**
```
┌──────────┐     ┌──────────┐     ┌──────────┐
│  Client  │────▶│  Server  │────▶│ Database │
└──────────┘     └──────────┘     └──────────┘
```

**API service / microservice:**
```
┌──────────┐     ┌──────────┐     ┌──────────┐
│ Consumer │────▶│   API    │────▶│  Storage │
└──────────┘     └──────────┘     └──────────┘
```

**CLI tool / library:**
```
┌──────────┐     ┌──────────┐     ┌──────────┐
│  Input   │────▶│  Core    │────▶│  Output  │
│ (args/   │     │  Logic   │     │ (stdout/ │
│  stdin)  │     │          │     │  files)  │
└──────────┘     └──────────┘     └──────────┘
```

**Data pipeline:**
```
┌──────────┐     ┌──────────┐     ┌──────────┐
│  Source  │────▶│ Process  │────▶│  Sink    │
└──────────┘     └──────────┘     └──────────┘
```

> Delete the patterns that don't apply. Keep and customize the one that fits.

---

## Key Layers

> Fill in with your project's actual layers and technologies.

| Layer | Tech | Location |
|-------|------|----------|
| Entry point | [e.g. main.py, src/app/, cmd/server/, src/main.rs] | — |
| Core logic | [e.g. services/, domain/, internal/] | — |
| Data access | [e.g. SQLAlchemy, Drizzle, GORM, Diesel] | — |
| External APIs | [e.g. REST client, gRPC, SDK wrappers] | — |
| Configuration | [e.g. .env, config.yaml, flags] | — |

---

## Data Flow

> Describe how data moves through your system.

```
Input → [Validation] → [Core Logic] → [Data Access] → Storage
                                                        ↓
                                  Response → [Output / Return]
```

---

## External Services

| Service | Purpose | Config Variable |
|---------|---------|-----------------|
| [e.g. PostgreSQL, MongoDB, SQLite] | Data storage | `DATABASE_URL` |
| [e.g. Redis, Memcached] | Cache | `CACHE_URL` |
| [e.g. S3, GCS, local filesystem] | File storage | `STORAGE_PATH` |
| [e.g. Stripe, SendGrid, Twilio] | Third-party API | `API_KEY` |

---

## When to Update This File

- When architecture changes
- When new layers or services are added or removed
- When data flow changes significantly
- When key technology decisions change (log in `decision-log.md` too)
