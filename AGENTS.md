# AGENTS.md

> Primary instruction file for ALL AI agents (Claude Code, Codex, Cursor, Windsurf, Gemini, chat).
> Read this fully before any work. It is self-contained for daily work — only open `docs/` when a task needs that specific detail.

This is a **multi-stack, AI-native project template**. One template, many project types (web, ML, mobile, API). You write the PRD + references; agents build the rest. Work survives **handoff between different AIs** — when one runs out of tokens, another continues from the docs alone.

---

## 0. First Action — Always

1. Open `docs/meta/CONTINUE.md`.
   - **Has real content** → this is an ongoing project. Resume from it. Do NOT run INIT.
   - **Still the blank template** → new project. Go to `docs/meta/INIT.md` and follow it.
2. Identify the **project type** from `prd/PRD.md`: `web-app` | `ml-project` | `mobile-app` | `api-service`.
3. Load the matching preset: `stacks/<type>.md`. It tells you which engineering docs apply.
4. Load `rules/common/` always. Load type-specific rules listed in the preset.

---

## 1. Source of Truth Hierarchy

When sources conflict, the higher one wins. Never override a higher source with a lower one without flagging it to the human and recording it in `docs/engineering/DECISIONS.md`.

**Universal (every project type):**
1. **AGENTS.md** (this file) — workflow & rules
2. **prd/PRD.md** — what we're building, scope, non-goals
3. **prd/SCOPE.md** — MVP boundary
4. **docs/engineering/ARCHITECTURE.md** — structure & boundaries
5. **docs/engineering/DECISIONS.md** — locked technical choices (ADRs)
6. **docs/engineering/CONVENTIONS.md** — naming & code style
7. **docs/engineering/QUALITY.md** — definition of done
8. **rules/common/** — universal engineering rules
9. **stacks/<type>.md** — the active preset (stack + which docs apply)

**Type-specific (only when the project uses them — see the preset):**
- `prd/FEATURES.md` — feature modules tagged P0/P1/P2
- `docs/design/DESIGN_DNA.md` + `docs/engineering/FRONTEND.md` — any UI work
- `docs/engineering/API.md` — endpoint contracts
- `docs/engineering/BACKEND.md` — backend implementation rules
- `docs/engineering/DATABASE.md` — schema, RLS, migrations
- Type-specific rules under `rules/<type>/` (created by INIT when needed)

Then: existing code patterns → your own judgment.

---

## 2. When to Open Each Doc (don't read preemptively — saves tokens)

| Open this | Only when the task involves |
|-----------|------------------------------|
| `prd/PRD.md` | Scope/feature questions, "should we build X" |
| `prd/FEATURES.md` | Building or scoping a specific feature module |
| `prd/SCOPE.md` | Deciding if something is MVP or deferred |
| `prd/REFERENCES.md` | Starting design or needing direction/inspiration |
| `docs/meta/CONTINUE.md` | **Start of every session** — resume point |
| `docs/engineering/PROGRESS.md` | Building features; tracking what's done & how things connect |
| `docs/engineering/ARCHITECTURE.md` | Adding folders, modules, cross-boundary imports |
| `docs/engineering/DECISIONS.md` | Choosing a lib/DB/pattern (check if already decided) |
| `docs/engineering/CONVENTIONS.md` | Writing any code (naming, structure, style) |
| `docs/engineering/QUALITY.md` | Before marking a task done |
| `docs/design/DESIGN_DNA.md` | **Any UI work — read first.** Short anti-generic rules |
| `docs/engineering/FRONTEND.md` | Detailed UI rules beyond DESIGN_DNA |
| `docs/engineering/BACKEND.md` | Server/route/service/middleware work |
| `docs/engineering/API.md` | Any endpoint/contract work |
| `docs/engineering/DATABASE.md` | Schema, RLS, indexes, migrations, data lifecycle |
| `stacks/<type>.md` | Confirming stack, structure, or which docs apply |
| `docs/checklists/*.md` | New feature, code review, pre-launch, or handoff |

---

## 3. Handoff Protocol (CRITICAL — this template's signature)

This project is built by **multiple AIs in turns**. There are no automatic hooks — handoff is manual via `.md` files, so they jump across ANY agent. Discipline is mandatory.

**At session START:** read `docs/meta/CONTINUE.md` before touching anything.

**Before session END or when a task completes:**
1. Update `docs/meta/CONTINUE.md` — status, what you did, explicit next steps, assumptions, blockers, critical context.
2. Append to `docs/engineering/PROGRESS.md` — dated entry, files changed.
3. Record real decisions in `docs/engineering/DECISIONS.md`.
4. Leave any unfinished work marked with `// TODO(handoff):` in code AND noted in CONTINUE.md.

**Golden rule:** write CONTINUE.md as if the next AI knows NOTHING about this session. Chat history does NOT carry over — only files do. Never reference "what we did earlier" implicitly; name the file, function, and line.

Run `docs/checklists/handoff.md` before stopping.

---

## 4. Workflow

1. Confirm project type + which app/area you're touching.
2. Match existing patterns in that area before inventing new ones.
3. Follow CONVENTIONS.md and the active preset's rules.
4. Don't add dependencies outside the preset without an ADR in DECISIONS.md.
5. Building features → keep PROGRESS.md current (pointer-based: link to source docs, don't restate them).
6. Finishing → self-check against QUALITY.md Definition of Done.
7. Made an architectural choice → append to DECISIONS.md.

---

## 5. Universal Rules (inline so you don't open a doc for basics)

- **Build on what exists.** Extend the codebase; don't regenerate from scratch.
- **Respect scope.** Out-of-MVP → backlog, don't build it. Ambiguous PRD → record assumption in CONTINUE.md, don't silently guess.
- **No secrets in code.** Use env vars; never commit keys.
- **Validate at boundaries** (Zod/Pydantic). Handle error, loading, empty states for UI.
- **One responsibility per file.** No dead code, no `console.log`/`print` debug left in commits.
- **Docs are living.** Keep them synced with the code as you change things.

For the full stack table and per-type details, open `stacks/<type>.md`.
