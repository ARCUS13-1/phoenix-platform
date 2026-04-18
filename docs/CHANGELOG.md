## [Unreleased] - 2026-04-18

### Added
- State-aware scenario engine using `armCondition`, `injectCondition`, `faultIds`, and `maxDurationSec`
- Dwell-time sync gating using `syncReadyTimer` and `syncLostTimer`
- Trip summary panel with captured trip snapshot
- Event markers on the analysis trend
- Fine-trim governor and AVR nudge controls
- State-aware breaker labels including closing-state feedback
- Scenario-specific failure messaging
- Lower-load control for overcurrent recovery
- `runFunctionChecks()` dev helper to perform internal structural checks and report results without mutating state
- Scope-status indicator near the synchroscope to show OFFLINE / TRACKING / SYNC WINDOW / PARALLEL / TRIPPED derived from the state machine
- Enhanced overcurrent scenario stable-window visibility with progress and injection status in the scenario state panel

### Changed
- `loadScenario()` now uses state-aware sequencing instead of timer-driven drill flow
- `tick()` now evaluates scenario state every frame after physics updates
- `updatePhysics()` now gates sync readiness/loss with dwell timing
- `updateUI()` normalizes generator display values to grid values while closed
- Guidance panel now better reflects machine and drill context
- Updated scenario state panel to display the overcurrent dwell timer with status suffixes: `(await inj)`, `(counting)`, or `(reset)`
- Extended the element cache to include `scopeStatus`
- Overcurrent drill success now requires post-injection stability under 1400 A for a 3.0 s dwell window
- Minor indentation and comment alignment for readability

### Fixed
- Overcurrent drill no longer injects before synchronization
- Overcurrent drill no longer completes immediately on injection
- Sync-window flicker reduced by dwell gating
- Breaker close command feedback improved with `CLOSING…` state
- Marker indices persist correctly through history trimming

### Notes
- Changes apply only to `phoenix_v9_dev.html`
- Runtime authority remains `index.html`
- This pass is validation-prep only and has not yet been promoted
