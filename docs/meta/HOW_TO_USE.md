# How to Use This Template

Guide for the **human**. For AI behavior, see `AGENTS.md`.

## Philosophy
Each new project, you focus on two things: write the **PRD** and gather **references**. The AI handles stack choice, architecture, scaffolding, and progress tracking. Because all context lives in `.md` files, you can **swap AIs mid-project** — if Claude hits its limit, continue in Cursor; if that runs out, the next one picks up. Progress doesn't vanish.

## Start a new project
1. Duplicate the folder: `cp -r final-template my-project && cd my-project && git init`
2. Fill `prd/PRD.md` and set the project type.
3. Fill `prd/FEATURES.md` (tag modules P0/P1/P2) and `prd/REFERENCES.md`.
4. In your AI agent: *"Read AGENTS.md, then run docs/meta/INIT.md."*
5. The agent confirms its understanding — correct it if needed — then it generates docs + scaffolds.
6. To continue later: *"Read AGENTS.md and docs/meta/CONTINUE.md, then continue."*

## Swapping AIs (handoff)
This is the core feature. When one AI hits its limit or you want to switch:
1. Make sure the last AI updated `CONTINUE.md` + `PROGRESS.md`. (If it forgot: *"update CONTINUE.md and PROGRESS.md before stopping."*)
2. Open the new AI on the same project folder.
3. Say: *"Read AGENTS.md and docs/meta/CONTINUE.md, then continue."*
4. It picks up from the last position. Done.

## Tips
- **The PRD is living.** Update it when direction changes.
- **Trust files, not chat.** Anything important must land in a `.md` — chat history doesn't transfer between AIs.
- **Don't skip the confirmation step** at INIT — that's your chance to steer before much code is written.
- **Review DECISIONS.md** to see why the AI chose what it chose.

## How strictness adapts
Guardrails are full, but they match the project type. A `web-app` gets DESIGN_DNA + FRONTEND/BACKEND/DATABASE rules; an `ml-project` gets reproducibility + data-contract rules instead. The active `stacks/<type>.md` decides what applies — you don't carry web rules into an ML project.
