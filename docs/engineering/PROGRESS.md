# PROGRESS LOG

> The live build map AND chronological log. Pointer-based: link to source docs,
> don't restate them. Newest entry on top. AI updates on every significant task.

## Build Map
> Derived from FEATURES.md. Mark in-progress / done; note connections.
> Each item points back to its source doc for durable detail.

- [ ] _(e.g. Auth — login/register (FEATURES.md #1, API.md, DATABASE.md))_
- [ ] _(e.g. Menu page (FEATURES.md #2, FRONTEND.md, DESIGN_DNA.md))_

---

## Log

<!-- copy this block to the top on each update:

## [YYYY-MM-DD] — <summary>
**By:** <AI / session>
**Status:** done | partial | blocked
**Did:**
- ...
**Files changed:**
- `path` — what
**Decisions:** (ref DECISIONS.md if any)
**For next session:** (or see CONTINUE.md)

-->

## EXAMPLE (delete once project starts)

## [2026-06-12] — Setup + auth scaffold
**By:** Claude (Claude Code)
**Status:** partial
**Did:** init Next.js 15 + Tailwind + shadcn; Supabase client; login & register pages.
**Files changed:**
- `src/app/(auth)/login/page.tsx` — login form
- `src/lib/supabase/client.ts` — client init
**Decisions:** Supabase Auth over NextAuth → DECISIONS.md ADR-003.
**For next session:** middleware unfinished — see CONTINUE.md.
