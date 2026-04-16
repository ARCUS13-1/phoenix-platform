# CHANGELOG

## Unreleased
- Repository initialized for Phoenix Platform
- Live GitHub Pages deployment active
- README created
- Project authority docs added
- Current source of truth confirmed as index.html

## 2026-04-13
### Fixed
- Aligned repository baseline filename with documented baseline reference
- Reconciled source-of-truth workflow language across authority docs
- Reconfirmed `index.html` as the single runtime source of truth

### Documented
- Current v8 runtime includes simulator, analysis/logging, timing studio, and telemetry overlay
- `phoenix_v9_dev.html` remains a sandbox-only development file
- `phoenix_v8_baseline_locked.html` remains rollback reference only

### Notes
- No runtime behavior changes were made in this pass
- This was a docs/authority cleanup only
## Unreleased

### Added
- V9 explicit machine state constants (`MODE`)
- V9 event constants (`EVENT`)
- `createMachine()` machine-state factory
- `createInitialState()` cold baseline state factory
- `machineResetState(prev)` reset helper
- `deriveContext()` sync-safety context evaluation
- `dispatch(event)` state transition logging
- `applyModeDerivedState()` machine-to-runtime state synchronization

### Changed
- Rewired core operator controls in `phoenix_v9_dev.html` to route through dispatch/event transitions
- Reset behavior now derives from a deterministic cold baseline
- `updatePhysics(dt)` now emits machine events for grid healthy, sync ready/lost, and breaker close confirmation
- `updateUI()` now normalizes displayed generator voltage/frequency to grid values when breaker is closed

### Validated
- Startup sequence remains intact in V9 dev
- Sync window entry remains intact in V9 dev
- Breaker close into parallel remains intact in V9 dev
- Load raise remains intact in V9 dev
- Chaos toggle remains intact in V9 dev
- Full system reset logs correctly in V9 dev

### Pending Validation
- Closed-state display truth patch in `updateUI()`
- State-aware breaker button labeling
- Scenario runner scaffolding
- Trip summary and chart markers
