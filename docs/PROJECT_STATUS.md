# Phoenix Platform Progress

## Runtime Authority
 **Canonical runtime file**: `index.html`
- **Locked baseline**: `phoenix_v8_baseline_locked.html`
- **Development sandbox**: `phoenix_v9_dev.html` (this build)

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

## Current V9 Development Status
`phoenix_v9_dev.html` now includes:
- Explicit machine states via `MODE`
- Event routing via `EVENT`
- `createMachine()` and `transition(...)`
- `createInitialState()` cold-start baseline
- `machineResetState(prev)` reset helper
- `deriveContext()` sync-safety context evaluation
- `dispatch(event)` transition logging
- `applyModeDerivedState()` machine-to-runtime sync
- Rewired operator controls through dispatch/event flow
- Physics hooks that emit machine events
- Closed-state display truth patch in `updateUI()`
- phoenix_v9_dev.html` now includes:
- Event‑driven sync window transitions via `SYNC_READY` and `SYNC_LOST`.
- Enhanced guidance panel with mode‑specific explanations.
- All v9.5 features (machine state/event scaffolding, deterministic reset, dispatch‑driven controls, physics hooks) preserved.
- No promotion to runtime authority yet; further validation required.


## Current Phase
- [x] Repo live on GitHub Pages
- [x] README added
- [x] Authority docs added
- [x] Canonical runtime confirmed as `index.html`
- [x] Baseline file locked
- [x] Step 1 - Explicit state machine scaffold integrated
- [x] Step 1A - Deterministic reset baseline validated
- [x] Step 2 - Command layer / next action integration
- [x] Step 2A - Closed-state display truth patch applied, awaiting validation
- [ ] Step 3 - State-aware breaker button labels
- [ ] Step 4 - Quickstart scenario runner
- [ ] Step 5 - Failure scenario runner
- [ ] Step 6 - Trip summary + chart markers
- [ ] Step 7 - Post-sync semantics cleanup / UI polish

## Working Rule
- `index.html` remains the shipped runtime source of truth.
- Experimental work may happen in `phoenix_v9_dev.html`.
- No behavior is considered released until it is validated and promoted into `index.html`.
-  Development continues in `phoenix_v9_dev.html` until validation criteria are met.

## Notes
- Keep the single-file architecture until function checks pass.
- Update `CHANGELOG.md` and `RUN_MANIFEST.json` whenever runtime authority or release state changes.
