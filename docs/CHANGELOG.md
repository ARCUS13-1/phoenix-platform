# CHANGELOG

## Unreleased
- Repository initialized for Phoenix Platform
- Live GitHub Pages deployment active
- README created
- Project authority docs added
- Current source of truth confirmed as index.html
- ### Added
- V9 explicit machine state constants (`MODE`)
- V9 event constants (`EVENT`)
- `createMachine()` machine-state factory
- `createInitialState()` cold baseline state factory
- `machineResetState(prev)` reset helper
- `deriveContext()` sync-safety context evaluation
- `dispatch(event)` state transition logging
- `applyModeDerivedState()` machine-to-runtime state synchronization
- Explicit V9 machine state and event scaffold in `phoenix_v9_dev.html`
- Deterministic reset via `createInitialState()` and `machineResetState(prev)`
- Dispatch-driven operator control routing
- Physics event emission for grid healthy, sync ready/lost, and breaker close confirmation
- Explicit `SYNC_READY` and `SYNC_LOST` event transitions in the v9 state machine. GEN_STARTING and GEN_READY now enter the sync window only via a `SYNC_READY` event and exit via `SYNC_LOST`, providing deterministic and readable flow.
- Mode‑specific operator guidance text. The guidance panel now explains the rationale for each step, including grid warm‑up, generator starting, alignment procedures, breaker closing, parallel operation, trip recovery, and pause states.
  
### Changed
- Rewired core operator controls in `phoenix_v9_dev.html` to route through dispatch/event transitions
- Reset behavior now derives from a deterministic cold baseline
- `updatePhysics(dt)` now emits machine events for grid healthy, sync ready/lost, and breaker close confirmation
- `updateUI()` now normalizes displayed generator voltage/frequency to grid values when breaker is closed
- Mobile-visible system badge now reflects machine mode rather than generic online/offline state
-  Removed direct `ctx.syncSafe` checks from generator modes in `transition()`; state changes into/out of the sync window are now driven exclusively by events.
- Simplified the sync window’s exit logic: leaving the window is triggered by `SYNC_LOST`, preventing oscillation and improving clarity.
- Expanded guidance panel copy to give operators clearer instructions in each mode and to highlight safe sync thresholds.

### Validated
- Startup sequence remains intact in V9 dev
- Sync window entry remains intact in V9 dev
- Breaker close into parallel remains intact in V9 dev
- Load raise remains intact in V9 dev
- Chaos toggle remains intact in V9 dev
- Full system reset logs correctly in V9 dev
- - Reset baseline remains deterministic
- Sync window entry remains intact
- Breaker close into parallel remains intact
- Closed-state display truth is verified on mobile screenshots
- Load raise remains intact through 9000 kW
- SOE logging/export remains intact
- All existing v9.5 features remain functional: sim start, grid warm‑up, generator start/stop, governor/AVR sliders, synchroscope, sync band and lamp, breaker controls with trip/reset, fault injection/clear, load raise, analysis logging, timing studio, telemetry overlay, scenario selector, guidance/debrief panels, training badge, and scoring path.

### Pending Validation
- Closed-state display truth patch in `updateUI()`
- State-aware breaker button labeling
- Scenario runner scaffolding
- Trip summary and chart markers
- Confirm event‑based sync transitions do not introduce race conditions under timing stress.
- Review updated guidance text for clarity and usefulness across desktop and mobile layouts.
- Ensure scenario scoring and logging logic remain correct with the new state transitions.
  
### Next
- State-aware breaker button labels
- Scenario scaffolding
- Trip summary and chart markers

### Documented
- Current v8 runtime includes simulator, analysis/logging, timing studio, and telemetry overlay
- `phoenix_v9_dev.html` remains a sandbox-only development file
- `phoenix_v8_baseline_locked.html` remains rollback reference only

### Notes
- No runtime behavior changes were made in this pass
- This was a docs/authority cleanup only
