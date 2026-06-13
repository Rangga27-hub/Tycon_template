# Design DNA

> Read before ANY UI work. Short on purpose. Detailed rules → `docs/engineering/FRONTEND.md`.
> Product-specific direction comes from `prd/REFERENCES.md`.
>
> The goal: UI that looks **professionally designed and human-made**, never AI-generic.
> If it could be from any AI demo site, it's not done.

---

## Build on what exists
Extend the existing codebase. Don't regenerate screens from scratch. The layout
rhythm, component patterns, and token wiring are the starting point, not a reference
to glance at and ignore.

## Tokens, not raw values
- All color from design tokens / theme variables — never raw hex, never raw palette classes inline.
- One accent/brand color. Semantic colors (success, warning, error) are separate.
- Spacing on a consistent grid (e.g. 4px: 4 8 12 16 24 32 48 64). No arbitrary `10px` values.

## Background & surface weight
- **Background stays light and neutral by default** unless REFERENCES.md explicitly calls for dark.
  Don't warm it to cream/beige — that's the #1 "AI look" tell.
- **One focal point per screen.** The hero headline + primary action wins the first viewport.
  Nothing competes with it.
- **Heavy/dark/inverted surfaces are for intentional late-page moments** (closing CTA, footer),
  not the hero. A near-black panel in the hero steals the eye.

## Forbidden "AI-generic" feels (current rotation — not exhaustive)
- warm cream / beige background
- violet / indigo gradient
- warm orange + cream
- generic "forest green + cream editorial"
- muted sage everything
- dark-purple "SaaS" gradient
- teal on near-black

## Typography
- Wire a real modern font properly. Unset = browser serif fallback = instant AI tell.
- Max 3 weights: 400 (body) · 500/600 (medium) · 700 (bold). No 300, no 800/900.
- Hierarchy from size + weight, not decorative font switches.

## Composition — the most violated rule
Open sections are the default. Cards earn their place.

| Context | Use |
|---------|-----|
| Hero, marketing sections, feature grids | Open bands — no card wrapper |
| Product listings, data panels, dialogs, repeated items | Cards are appropriate |

**Hard stops:**
- Hero content not wrapped in a card.
- Not every section boxed in a bordered card ("card soup").
- Pale bordered rectangles are not a design system.

## Navigation
- Persistent nav on every route, with a visible surface (not invisible floating text).
- Active route marked with `aria-current="page"`, same on mobile and desktop.
- Routes connect: users never get trapped with no way back to home.

## Mandatory self-check before "done"
1. Could this be any AI demo site? If yes → not done.
2. Is the background warmed/cream, or a forbidden gradient? → fix.
3. Is the hero wrapped in a card or pushed below the fold? → fix.
4. Is every section a card? → open them up.
5. Is the font actually wired (not serif fallback)? → wire it.
6. Active nav state present on mobile + desktop? → add it.
7. Loading/empty/error states present? → add them.
