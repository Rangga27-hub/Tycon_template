# Preset: WEB APP (Fullstack)

> Default for `web-app`. Adjust per PRD/REFERENCES — record changes in DECISIONS.md.

## Docs that apply for this type
Universal + **FRONTEND.md, BACKEND.md, API.md, DATABASE.md, DESIGN_DNA.md**, FEATURES.md.
Type rules: create `rules/web/` if extra UI/security rules are needed.

## Stack
| Layer | Choice | Note |
|-------|--------|------|
| Framework | Next.js 15 (App Router) | server actions |
| Language | TypeScript | strict |
| Styling | Tailwind CSS | utility-first |
| UI | shadcn/ui | copy-paste, not heavy dep |
| DB | Supabase (Postgres) | + Auth + Storage |
| Auth | Supabase Auth | integrates with RLS |
| Validation | Zod | at boundaries |
| Data fetching | TanStack Query | client caching |
| Forms | React Hook Form + Zod | |
| Icons | lucide-react | |
| Deploy | Vercel | |

## Structure
```
src/
  app/            # App Router
    (auth)/
    (dashboard)/
    api/
  components/{ui,features}/
  lib/{supabase,utils}/
  actions/        # server actions
  types/  hooks/
```

## Type rules
- Server actions in `src/actions/`, not in components.
- Server-only Supabase service-role key never imported into client.
- Security via RLS — don't rely on client-side checks alone.
- UI: read DESIGN_DNA.md first; obey its self-check before "done".

## Quick setup
```bash
npx create-next-app@latest . --typescript --tailwind --app --src-dir
npx shadcn@latest init
npm install @supabase/supabase-js @supabase/ssr zod @tanstack/react-query react-hook-form lucide-react
```
