# AI Project Template

Multi-stack, AI-native, handoff-ready project template. Write a PRD + references; let any AI agent build the rest. Work survives handoff between different AIs — when one runs out of tokens, another continues from the docs alone.

## What makes it different
- **Multi-stack** — one template for web, ML, mobile, API (via `stacks/`).
- **Handoff-ready** — manual `.md`-based continuity works across ANY agent (Claude Code, Cursor, Windsurf, chat). No Claude-only hooks that break on switch.
- **Strict but adaptive** — full guardrails, but strictness matches the project type.
- **Self-documenting** — Source-of-Truth Hierarchy + When-to-Open table keep AIs aligned and token-efficient.

## Start
1. Duplicate this folder, `git init`.
2. Read `START_HERE.md`.
3. Fill `prd/PRD.md` (+ type), `prd/FEATURES.md`, `prd/REFERENCES.md`.
4. Tell your agent: *"Read AGENTS.md, then run docs/meta/INIT.md."*

## Swap AIs mid-project
1. Last AI updates `CONTINUE.md` + `PROGRESS.md`.
2. Open a new AI on the same folder.
3. *"Read AGENTS.md and docs/meta/CONTINUE.md, then continue."*

## Layout
```
AGENTS.md · CLAUDE.md · .cursorrules   ← AI entry points
prd/        ← you fill: PRD, FEATURES, REFERENCES, SCOPE
docs/meta/  ← INIT, CONTINUE (handoff), HOW_TO_USE
docs/engineering/ ← AI fills: architecture, decisions, api, frontend,
                    backend, database, conventions, quality, progress
docs/design/ ← DESIGN_DNA (anti-AI-generic UI)
docs/checklists/ ← new-feature, code-review, pre-launch, handoff
rules/common/ ← universal rules
stacks/     ← presets per project type
```

## Default stacks (changeable per project)
- **Web:** Next.js 15 + TS + Tailwind + shadcn/ui + Supabase
- **ML:** Python + uv + scikit-learn/PyTorch + FastAPI
- **Mobile:** React Native + Expo + NativeWind + Supabase
- **API:** FastAPI (Python) or Hono (TS) + Postgres

## Tip
Save as a GitHub **template repository** (Settings → Template repository) so each new project is one click.
