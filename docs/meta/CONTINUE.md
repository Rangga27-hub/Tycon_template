# CONTINUE

> **AI agent: read this FIRST every session.** This is the handoff point between
> sessions and between different AIs. Update it before you stop.
>
> Write as if the next AI knows nothing about this session. Chat history does NOT
> carry over — only this file does. Name files, functions, lines explicitly.

---

## Status
`NOT STARTED` · `SETUP` · `IN PROGRESS` · `TESTING` · `DONE`

> **Current: NOT STARTED** ← new project; run docs/meta/INIT.md.

## Working On
> Current focus. Specific.

_(empty — fill after starting)_

## Next Steps
> Concrete, ordered actions for the next AI.

1. _(none yet)_

## Assumptions Made
> Assumptions taken because the PRD was ambiguous. Human can correct.

- _(none yet)_

## Blockers / Notes
> Anything blocking, or that the next AI MUST know.

- _(none yet)_

## Critical Context (don't lose this)
> Key decisions/info that must not be forgotten at handoff.

- _(none yet)_

---
---

## EXAMPLE (delete this whole section once the project starts)

```
## Status
IN PROGRESS

## Working On
Auth flow. Login + register done in src/app/(auth)/login/page.tsx and register/page.tsx.
Mid-way through route-protection middleware in src/middleware.ts — session check done,
admin-role redirect NOT done yet.

## Next Steps
1. Finish src/middleware.ts: admin → /dashboard, user → /home. See TODO(handoff) ~line 42.
2. Build /forgot-password (doesn't exist yet).
3. Test full auth flow end-to-end.
4. Update DATABASE.md if the users table changed.

## Assumptions Made
- Roles are only 'admin' and 'customer' (PRD didn't specify others).
- Email/password first; OAuth deferred to phase 2.

## Blockers / Notes
- Supabase RLS policy for `profiles` not created yet — queries will fail until it is.

## Critical Context
- Next.js 15 App Router (NOT Pages Router).
- Server actions live in src/actions/ — don't mix into components.
- Decision to use Supabase Auth (not NextAuth) is in DECISIONS.md ADR-003.
```
