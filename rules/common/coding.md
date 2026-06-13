# Common: Coding

- One responsibility per file; functions do one thing.
- Prefer clarity over cleverness. Names describe intent.
- No dead code, no commented-out blocks in commits.
- No debug logging (`console.log`/`print`) committed.
- Validate input at boundaries (Zod / Pydantic / equivalent).
- Handle failure paths explicitly; don't swallow errors silently.
- Keep modules decoupled; respect boundaries in ARCHITECTURE.md.
