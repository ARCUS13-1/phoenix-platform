## Unreleased

### Added
- State-aware scenario engine using `armCondition`, `injectCondition`, `faultIds`, and `maxDurationSec`
- Dwell-time sync gating using `syncReadyTimer` and `syncLostTimer`
- Trip summary panel with captured trip snapshot
- Event markers on the analysis trend
- Fine-trim governor and AVR nudge controls
- State-aware breaker labels including closing-state feedback
- Scenario-specific failure messaging

### Changed
- `loadScenario()` now uses state-aware sequencing instead of timer-driven drill flow
- `tick()` now evaluates scenario state every frame after physics updates
- `updatePhysics()` now gates sync readiness/loss with dwell timing
- `updateUI()` normalizes generator display values to grid values while closed
- Guidance panel now better reflects machine and drill context

### Fixed
- Overcurrent drill no longer injects before synchronization
- Sync-window flicker reduced by dwell gating
- Breaker close command feedback improved with `CLOSING…` state
- Marker indices persist correctly through history trimming

### Known Remaining Issue
- OVERCURRENT drill is still not fully recoverable because fault current is hard-forced to a trip level after closure and needs to be converted into a controllable overload model.
