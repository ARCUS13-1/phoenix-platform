# Phoenix Platform Progress

## Runtime Authority
- Canonical runtime file: `index.html`
- Locked rollback baseline: `phoenix_v8_baseline_locked.html`
- Active development sandbox: `phoenix_v9_dev.html`

## Current Runtime Snapshot
`index.html` is the live single-file v8 runtime and currently includes:
- Grid ↔ generator synchronizing
- Synchroscope + sync close window
- Breaker OPEN / CLOSED / TRIPPED behavior
- Fault injection
- Analysis & logging
- Timing Studio
- Telemetry / ghost-frequency overlay
- Mobile-first single-file operation

## Current Phase
- [x] Repo live on GitHub Pages
- [x] README added
- [x] Authority docs added
- [x] Canonical runtime confirmed as `index.html`
- [x] Baseline file locked
- [ ] Step 1 - Explicit state machine
- [ ] Step 2 - Command layer / next action
- [ ] Step 3 - Quickstart scenario runner
- [ ] Step 4 - Failure scenario runner
- [ ] Step 5 - Trip summary + chart markers
- [ ] Step 6 - Post-sync semantics cleanup

## Working Rule
- `index.html` remains the shipped runtime source of truth.
- Experimental work may happen in `phoenix_v9_dev.html`.
- No behavior is considered released until it is validated and promoted into `index.html`.

## Notes
- Keep the single-file architecture until function checks pass.
- Update `CHANGELOG.md` and `RUN_MANIFEST.json` whenever runtime authority or release state changes.
