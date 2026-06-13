# START HERE

Multi-stack, AI-native project template. Write a PRD + references; let any AI agent build the rest. Work survives handoff between different AIs.

---

## If you're a HUMAN starting a new project

1. Read `docs/meta/HOW_TO_USE.md`.
2. Fill `prd/PRD.md` (what you're building) and set the **project type**: `web-app` / `ml-project` / `mobile-app` / `api-service`.
3. Fill `prd/FEATURES.md` (modules tagged P0/P1/P2) and `prd/REFERENCES.md` (design/technical inspiration).
4. Tell your AI agent: *"Read AGENTS.md, then run docs/meta/INIT.md."*

## If you're an AI AGENT

Go to **`AGENTS.md`** and follow it. Section 0 tells you your first action.
Short version: check `docs/meta/CONTINUE.md` first — content means resume, blank means run `docs/meta/INIT.md`.

---

## Layout

```
AGENTS.md            ← AI brain: hierarchy, when-to-open, handoff protocol
CLAUDE.md            ← pointer to AGENTS.md (Claude Code auto-loads)
.cursorrules         ← pointer to AGENTS.md (Cursor auto-loads)

prd/                 ← [YOU FILL] product intent
  PRD.md · FEATURES.md · REFERENCES.md · SCOPE.md

docs/
  meta/              ← INIT, CONTINUE (handoff), HOW_TO_USE
  engineering/       ← [AI FILLS] architecture, decisions, api, frontend,
                       backend, database, conventions, quality, progress
  design/            ← DESIGN_DNA (anti-AI-generic UI rules)
  checklists/        ← new-feature, code-review, pre-launch, handoff

rules/
  common/            ← universal engineering rules (always active)

stacks/              ← presets per project type (stack + which docs apply)
  web-app · ml-project · mobile-app · api-service
```

## Why this template

- **Multi-stack** — one template handles web, ML, mobile, API via `stacks/`.
- **Handoff-ready** — manual `.md`-based continuity works across ANY agent (no Claude-only hooks).
- **Strict but adaptive** — full guardrails, but the strictness matches the project type.
- **Self-documenting** — every decision recorded, not lost in chat.
