# Preset: API SERVICE (Backend Only)

> Default for `api-service`. Pick Python or TS per project — record in DECISIONS.md.

## Docs that apply for this type
Universal + **API.md, BACKEND.md, DATABASE.md**, FEATURES.md.
NOT applicable: FRONTEND.md, DESIGN_DNA.md.
Type rules: create `rules/api/` if needed.

## Stack — Option A: Python (default for ML-adjacent / data-heavy)
| Layer | Choice |
|-------|--------|
| Framework | FastAPI |
| Server | uvicorn |
| Validation | Pydantic v2 |
| ORM | SQLAlchemy 2.0 + Alembic |
| DB | PostgreSQL (Supabase or self-hosted) |
| Auth | JWT / Supabase Auth |
| Pkg manager | uv |

## Stack — Option B: TypeScript (default for JS ecosystem)
| Layer | Choice |
|-------|--------|
| Framework | Hono (light, fast) or Express |
| Runtime | Node.js / Bun |
| Validation | Zod |
| ORM | Drizzle |
| DB | PostgreSQL |

## Structure (FastAPI)
```
src/
  api/{routes,deps}/
  models/  schemas/  services/  core/  db/
tests/
```

## Type rules
- Separate routes (HTTP) → services (logic) → models (data).
- Validate all I/O at the boundary.
- Version the API (/v1/...).
- Use auto OpenAPI docs (FastAPI) — keep API.md in sync.
- Paginate lists; never return unbounded results.

## Quick setup (FastAPI)
```bash
pip install uv && uv venv && source .venv/bin/activate
uv pip install fastapi uvicorn pydantic sqlalchemy alembic psycopg2-binary
```
