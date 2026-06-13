# Checklist: New Feature

## Before starting
- [ ] Feature is in FEATURES.md / approved by human
- [ ] Checked SCOPE.md — is it MVP or deferrable?
- [ ] Read CONVENTIONS.md + relevant layer doc (FRONTEND/BACKEND/API/DATABASE)

## While coding
- [ ] Follow existing folder & naming patterns
- [ ] Validate input at the boundary
- [ ] Handle error / loading / empty states (UI)
- [ ] No new dependency without an ADR in DECISIONS.md
- [ ] Update DATABASE.md / API.md if schema or contracts change

## Before done
- [ ] Runs / tests pass; no debug logging left
- [ ] PROGRESS.md updated
- [ ] CONTINUE.md updated
- [ ] Decisions → DECISIONS.md
