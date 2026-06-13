# DECISIONS — Architecture Decision Records

> Why each non-trivial choice was made. Critical for handoff: the next AI sees the
> reasoning without re-litigating it. Newest at the bottom (numbers go up).
> Never delete an ADR — supersede it with a new one if reversed.

## ADR Template
```
## ADR-NNN: <title>
- Date: YYYY-MM-DD
- Status: Accepted | Rejected | Superseded by ADR-XXX
- Context: the situation forcing a decision
- Decision: what was decided
- Rationale: why, vs alternatives
- Alternatives: other options + why not
- Consequences: + and − impacts
```

## EXAMPLE (delete once real ADRs exist)

## ADR-001: Use Next.js App Router (not Pages Router)
- Date: 2026-06-12
- Status: Accepted
- Context: Need a fullstack React framework with modern routing & SSR.
- Decision: Next.js 15 with App Router.
- Rationale: Official direction; Server Components + server actions cut boilerplate.
- Alternatives: Pages Router (legacy); Remix (smaller ecosystem).
- Consequences: (+) less API code. (−) some libs lag on Server Components.
