# Checklist: Code Review

## Functionality
- [ ] Does what the PRD/FEATURES intends
- [ ] Edge cases handled (empty, error, large input)
- [ ] No obvious logic bugs

## Quality
- [ ] Consistent with CONVENTIONS.md
- [ ] Clear, descriptive names
- [ ] No duplication that should be refactored
- [ ] No magic numbers / hardcoded values that should be constants or env

## Security
- [ ] No secrets/keys in code
- [ ] User input validated & sanitized
- [ ] DB queries safe (parameterized, RLS where relevant)
- [ ] Server-only keys not imported into client

## Handoff-readiness
- [ ] Another AI could understand this without chat context
- [ ] Tricky parts commented
- [ ] Related docs updated
