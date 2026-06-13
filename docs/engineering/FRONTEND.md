# FRONTEND

> [AI-GENERATED if the type has UI] Detailed UI rules. Open only when DESIGN_DNA.md
> doesn't cover the specific question. Applies to: web-app, mobile-app.

## Rendering & Structure
- Component organization: _(presentational vs container; where logic lives)_
- State: _(local vs global; what tool)_
- Data fetching: _(pattern, caching)_

## Required States
Every screen/component handles: loading · empty · error · success.

## Accessibility
- Semantic markup; keyboard navigable.
- Focus rings on interactive elements.
- `aria-current="page"` on active nav.
- Respect `prefers-reduced-motion`.

## Performance
- Lazy-load heavy routes/components.
- Animate transform/opacity only; cap durations.

## Reference
Short, high-signal rules live in `docs/design/DESIGN_DNA.md` — read that first.
