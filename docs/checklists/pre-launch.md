# Checklist: Pre-Launch

## Functionality
- [ ] All MVP features (SCOPE.md) done & tested
- [ ] Main user flow works end-to-end
- [ ] Errors & edge cases handled

## Quality
- [ ] No console/log errors
- [ ] Loading/empty states everywhere (UI)
- [ ] Responsive on mobile (if targeted)
- [ ] Performance meets PRD targets

## Security & Data
- [ ] Production env vars set (not dev values)
- [ ] No secrets committed
- [ ] Auth / route protection / RLS active
- [ ] DB backup/migration ready (if any)

## Deployment
- [ ] Production build succeeds
- [ ] Hosting/domain ready
- [ ] Error tracking/monitoring active (if any)

## ML-specific (if ml-project)
- [ ] Model artifact versioned & stored
- [ ] Inference endpoint tested with real input
- [ ] Metrics meet target (DATABASE.md)
- [ ] Inference latency acceptable

## Docs
- [ ] README filled (setup & run)
- [ ] PROGRESS.md & CONTINUE.md current
