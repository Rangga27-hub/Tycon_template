# INIT — Initialize a New Project

> **AI agent:** run this ONLY if `docs/meta/CONTINUE.md` is still the blank template.
> If it has real content, this project already started — resume from CONTINUE.md instead.

## Steps (in order)

### 1. Understand context
- Read `prd/PRD.md`, `prd/FEATURES.md`, `prd/SCOPE.md`, `prd/REFERENCES.md`.
- Identify the **project type** and open `stacks/<type>.md`.
- The preset tells you which engineering docs apply to this project.

### 2. Confirm with the human (before generating anything)
Summarize:
- "This is ___, type ___."
- "Stack I'll use: ___ (from the preset, with adjustments: ___)."
- "Docs that apply for this type: ___."
- "Ambiguities in the PRD: ___."

Wait for confirmation/correction. Then proceed.

### 3. Generate engineering docs (only the ones the preset lists)
Fill, don't leave as templates:
- `docs/engineering/ARCHITECTURE.md` — folders, data flow, components.
- `docs/engineering/CONVENTIONS.md` — naming & style for this stack.
- `docs/engineering/DECISIONS.md` — initial choices as ADR-001, 002, …
- `docs/engineering/QUALITY.md` — adapt the definition of done to this type.
- **If the type uses them:** `API.md`, `BACKEND.md`, `DATABASE.md`, `FRONTEND.md`, `docs/design/DESIGN_DNA.md`.
- **If type-specific rules are needed**, create `rules/<type>/` (e.g. `rules/ml/` for reproducibility).

### 4. Scaffold the real project
- Initialize per the preset's "Quick setup".
- Get it running (hello-world / empty page works).
- Initial git commit if using git.

### 5. Build the live map + handoff point
- Generate `docs/engineering/PROGRESS.md` from FEATURES.md (pointer-based: link to source docs, don't restate).
- Update `docs/meta/CONTINUE.md`: set status, fill "Working on", "Next steps", "Assumptions", "Critical context". **Delete the EXAMPLE section.**

### 6. Report
Tell the human what's set up and what's next.

## Guardrails
- Build MVP first (SCOPE.md). Don't over-engineer.
- No dependencies outside the preset without an ADR.
- PRD unclear for a part → record the assumption in CONTINUE.md, don't silently guess.
