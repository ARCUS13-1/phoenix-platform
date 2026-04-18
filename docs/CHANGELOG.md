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
- Introduced explicit `SYNC_READY` and `SYNC_LOST` events.  Generator modes now enter the sync window only via `SYNC_READY` and return to `GEN_READY` via `SYNC_LOST`.  This removes continuous context checks and provides deterministic behavior.
- Added detailed mode‑specific guidance to the operator guidance panel explaining the rationale for each action (grid warm‑up, generator starting, alignment, breaker closing, parallel operation, trip recovery and pause).
- Added state‑aware breaker button labels: `RESET BREAKER` when tripped, `OPEN BREAKER` when closed, `CLOSE BREAKER` when sync conditions are met, and `CLOSE BLOCKED` when not ready.
  
### Changed
- Rewired core operator controls in `phoenix_v9_dev.html` to route through dispatch/event transitions
- Reset behavior now derives from a deterministic cold baseline
- `updatePhysics(dt)` now emits machine events for grid healthy, sync ready/lost, and breaker close confirmation
- `updateUI()` now normalizes displayed generator voltage/frequency to grid values when breaker is closed
- Mobile-visible system badge now reflects machine mode rather than generic online/offline state
-  Removed direct `ctx.syncSafe` checks from generator modes in `transition()`; state changes into/out of the sync window are now driven exclusively by events.
- Simplified the sync window’s exit logic: leaving the window is triggered by `SYNC_LOST`, preventing oscillation and improving clarity.
- Expanded guidance panel copy to give operators clearer instructions in each mode and to highlight safe sync thresholds.
- Reworked `transition()` to remove direct `ctx.syncSafe` checks; sync transitions are now event‑driven.
- Updated `updatePhysics(dt)` to emit `SYNC_READY` and `SYNC_LOST` events instead of updating machine state directly.
- Updated `updateUI()` to normalize generator voltage and frequency to grid values when the breaker is closed.
- Enhanced guidance panel copy for clarity and added post‑trip instructions.

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
- Confirmed sim start, grid warm‑up, generator start/stop, sync window entry, breaker closing, load raise, fault injection/clear, log replay/export, timing studio, telemetry overlay, scenario selection, guidance/debrief panels, training badge and scoring features remain functional in the development file.

### Pending Validation
- Implement dwell time gating for `SYNC_READY`/`SYNC_LOST` events to avoid race conditions.
- Refine scenario guidance to override generic guidance when active.
- Implement scenario runner scaffolding, trip summary and chart markers.
- Validate closed‑state slip and phase display; ensure they show zero in parallel mode.
  
### Next
- Scenario scaffolding
- Trip summary and chart markers

### Documented
- Current v8 runtime includes simulator, analysis/logging, timing studio, and telemetry overlay
- `phoenix_v9_dev.html` remains a sandbox-only development file
- `phoenix_v8_baseline_locked.html` remains rollback reference only

### Notes
- No runtime behavior changes were made in this pass
- This was a docs/authority cleanup only
