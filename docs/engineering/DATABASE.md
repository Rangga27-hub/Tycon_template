# DATABASE / DATA MODEL

> [AI-GENERATED if the type stores data] Source of truth for data.
> For web/mobile/api: schema + RLS. For ml-project: dataset + model artifacts.

## For web / mobile / api — Schema

### Table: `<name>`
| Column | Type | Constraint | Note |
|--------|------|-----------|------|
| id | uuid | PK | |
| _(AI fills)_ | | | |

### Relations
_(one-to-many, many-to-many.)_

### Security / RLS
_(policy per table if using Postgres/Supabase RLS.)_

### Migrations
_(where migrations live; how to run.)_

---

## For ml-project — Data & Model

### Dataset
- Source / size / shape:
- Features:
- Target / label:
- Preprocessing:
- Split strategy + random seed (reproducibility):

### Model
- Architecture:
- Input/output shape:
- Eval metrics + targets:
- Artifact location (where weights/checkpoints live):
- Versioning approach:
