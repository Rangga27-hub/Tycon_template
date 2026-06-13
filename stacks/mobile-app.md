# Preset: MOBILE APP

> Default for `mobile-app`. Adjust per PRD — record in DECISIONS.md.

## Docs that apply for this type
Universal + **FRONTEND.md, DESIGN_DNA.md, API.md, DATABASE.md**, FEATURES.md.
Type rules: create `rules/mobile/` if needed.

## Stack
| Layer | Choice | Note |
|-------|--------|------|
| Framework | React Native + Expo | cross-platform |
| Routing | Expo Router | file-based |
| Language | TypeScript | |
| Styling | NativeWind | Tailwind for RN |
| Backend/DB | Supabase | consistent with web |
| State | Zustand / Context | lightweight |
| Validation | Zod | |
| Icons | lucide-react-native | |
| Build | EAS | build & submit to stores |

## Structure
```
app/                # Expo Router (file-based)
  (auth)/  (tabs)/
components/{ui,features}/
lib/supabase/
context/            # providers (cart, toast, auth)
hooks/  types/  constants/
```

## Type rules
- Expo Router file-based, consistent with Next.js patterns.
- Logic in hooks; keep components presentational.
- Global providers at root layout.
- Test on a real device, not just emulator.
- UI: read DESIGN_DNA.md (adapted for native surfaces).

## Quick setup
```bash
npx create-expo-app@latest . --template
npx expo install nativewind tailwindcss
npm install @supabase/supabase-js zustand zod lucide-react-native
```
