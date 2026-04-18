## Phoenix Platform Progress

### Runtime Authority
- **Canonical runtime file:** `index.html`
- **Locked baseline:** `phoenix_v8_baseline_locked.html`
- **Development authority:** `phoenix_v9_dev.html`

### Current Runtime Snapshot
`index.html` remains the shipped v8 runtime and still serves as the authoritative public baseline.

### Current Development Snapshot
`phoenix_v9_dev.html` now includes:
- Explicit machine states via `MODE`
- Event routing via `EVENT`
- Deterministic reset helpers
- Dispatch-driven control flow
- Event-driven sync transitions
- Dwell-time gating for sync window entry/exit
- State-aware scenario engine
- Guidance + debrief panels
- Training badge and scoring path
- Fine-trim governor / AVR nudges
- Breaker button clarity improvements
- Trip summary panel
- Trend event markers
- Lower-load control for overcurrent recovery
- Scope-status indicator near the synchroscope
- `runFunctionChecks()` dev helper
- Overcurrent stable-window tracking and display in the scenario state panel

### Current Phase
- [x] Step 1 - Explicit state machine scaffold
- [x] Step 1A - Deterministic reset baseline
- [x] Step 2 - Command layer / next action integration
- [x] Step 2A - Closed-state display truth patch
- [x] Step 3 - Event-driven sync transitions + enhanced guidance
- [x] Step 4 - State-aware breaker button labels + closing-state clarity
- [x] Step 5 - Scenario runner scaffolding
- [x] Step 6 - Trip summary + chart markers
- [x] Step 6B - Scenario/physics truth alignment and overcurrent drill correction
- [ ] Step 7 - Post-sync semantics cleanup / UI polish
- [ ] Final manual validation for promotion into `index.html`

### Working Rule
- `index.html` remains shipped runtime authority.
- `phoenix_v9_dev.html` is the active development authority.
- No feature is released until validation passes and docs/manifests are updated.

### Current Blocking Risks
- Manual scenario validation is still required across all six drills: `quickstart`, `vsag`, `phaseerr`, `overcurrent`, `stuck`, `combined`.
- Mobile layout still needs live verification for the scope-status line and scenario stable-timer text.
- Overcurrent drill logic is now teachable and no longer hard-forced on injection, but it still needs live tuning validation for difficulty and operator clarity.
- Final Step 7 UI polish and promotion review remain open.
