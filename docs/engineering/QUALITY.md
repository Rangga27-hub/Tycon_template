# QUALITY — Definition of Done

> Self-check before calling any task done. Adapt specifics per project type at INIT.

## Code Quality
- Strict typing (TS `strict`, no implicit `any`; Python type hints where it helps).
- Lint + format pass before commit.
- One responsibility per file; functions do one thing.
- No dead code, no commented-out blocks, no debug logging committed.

## Definition of Done (per task)
- [ ] Code runs / tests pass.
- [ ] Follows CONVENTIONS.md and the active preset rules.
- [ ] `PROGRESS.md` updated.
- [ ] `CONTINUE.md` updated (clear next step).
- [ ] Real decisions recorded in `DECISIONS.md`.
- [ ] No stray `TODO(handoff)` without a note in CONTINUE.md.
- [ ] (UI) passed the DESIGN_DNA self-check.
- [ ] (API/DB change) contracts/migrations + relevant docs updated.

## Docs Sync
Keep docs synchronized with code:
- Scope changes → PRD.md / FEATURES.md.
- API changes → API.md.
- Schema changes → DATABASE.md + migrations.
- UI direction → DESIGN_DNA.md.
- Architectural choices → DECISIONS.md.

## Performance Basics
- No needless re-renders; memoize only where it measurably helps.
- Lazy-load heavy routes/components.
- Paginate list endpoints; never return unbounded results.

## Security Basics
- No secrets in code or client bundles.
- Validate & sanitize all user input.
- Server-only keys never imported into client code.
- DB access guarded (parameterized queries, RLS where applicable).
