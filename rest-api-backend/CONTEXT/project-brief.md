# Project Brief — REST API / Backend

> Fill this in before writing any routes. Cascade reads this first.

## API Identity
- **Name:** [API name]
- **Purpose:** [What does this API do? One sentence.]
- **Consumers:** [Who calls this API? Frontend app, mobile, other service?]
- **Status:** `Development` / `Staging` / `Production`

## Stack
- **Language + Framework:** [Python + FastAPI / Node + Express / other]
- **Database:** [PostgreSQL / SQLite / MongoDB]
- **ORM:** [SQLAlchemy / Prisma / Mongoose / raw SQL]
- **Auth:** [JWT / API Key / OAuth2 / None]
- **Deployment:** [Docker / Railway / Render / AWS / other]
- **API versioning:** [e.g. `/api/v1/`]

## Base URL
- **Dev:** `http://localhost:8000`
- **Staging:** [URL]
- **Prod:** [URL]

## Key Resources (Endpoints)
| Resource | Base Path | Auth Required |
|---|---|---|
| [e.g. Users] | `/api/v1/users` | Yes |

## Non-Negotiables
- [e.g. All endpoints must be authenticated]
- [e.g. Response time < 200ms for reads]
- [e.g. No raw SQL — use ORM only]

## What Cascade Should Never Do
- [e.g. Don't expose internal IDs to API responses]
- [e.g. Don't bypass the auth middleware]

## Environment Variables
| Variable | Purpose |
|---|---|
| `DATABASE_URL` | DB connection string |
| `JWT_SECRET` | Token signing key |
| `PORT` | Server port |
