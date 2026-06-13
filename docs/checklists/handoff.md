# Checklist: Handoff (run before you stop)

> The signature of this template. Before any AI ends a session, this guarantees the
> next AI (possibly a different one) can continue with zero lost context.

## Update the handoff files
- [ ] `docs/meta/CONTINUE.md`:
  - [ ] Status set correctly
  - [ ] "Working On" describes the exact current state (file, function, how far)
  - [ ] "Next Steps" are concrete and ordered
  - [ ] "Assumptions Made" recorded (anything the PRD didn't specify)
  - [ ] "Blockers / Notes" current
  - [ ] "Critical Context" captures anything that must not be lost
- [ ] `docs/engineering/PROGRESS.md`: new dated entry + build-map items updated

## Code state
- [ ] Unfinished work marked `// TODO(handoff):` AND noted in CONTINUE.md
- [ ] No half-broken state left without explanation
- [ ] Decisions made this session appended to `DECISIONS.md`

## The real test
- [ ] Reread CONTINUE.md as if you know NOTHING about this session.
      Could a different AI continue from it alone? If not, add detail.
