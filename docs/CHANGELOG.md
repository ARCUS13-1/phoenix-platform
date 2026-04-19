# CHANGELOG

## [2026-04-19] - Public Beta Promotion

### Promoted
- Promoted the tested v9.5 beta build from `phoenix_v9_dev.html` into `index.html`
- Updated the public GitHub Pages runtime to the current tested beta build

### Added
- State-aware scenario engine using `armCondition`, `injectCondition`, `faultIds`, and `maxDurationSec`
- Dwell-time sync gating using `syncReadyTimer` and `syncLostTimer`
- Trip summary panel with captured trip snapshot
- Event markers on the analysis trend
- Fine-trim governor and AVR nudge controls
- State-aware breaker labels including closing-state feedback
- Scenario-specific failure messaging
- Lower-load control for overcurrent recovery
- `runFunctionChecks()` dev helper to perform internal structural checks without mutating runtime state
- Scope-status indicator near the synchroscope to show OFFLINE / TRACKING / SYNC WINDOW / PARALLEL / TRIPPED
- Enhanced overcurrent stable-window visibility in the scenario state panel

### Changed
- `loadScenario()` now uses state-aware sequencing instead of timer-driven drill flow
- `tick()` now evaluates scenario state every frame after physics updates
- `updatePhysics()` now gates sync readiness / loss with dwell timing
- Guidance panel now better reflects machine and drill context
- Scenario state panel now shows overcurrent dwell timer status
- Overcurrent drill success now requires post-injection stability under 1400 A for a continuous 3.0 s dwell window
- Failure semantics were hardened so failed drills do not present misleading successful outcomes
- Result wording now distinguishes SUCCESS, FAILED — TIMEOUT, and FAILED — TRIP
- Combined fault drill timeout was extended for clearer recovery testing

### Fixed
- Overcurrent drill no longer injects before synchronization
- Overcurrent drill no longer completes immediately on injection
- Sync-window flicker reduced by dwell gating
- Breaker close command feedback improved with closing-state clarity
- Marker indices persist correctly through history trimming
- Failure scoring no longer leaves timeout or trip failures with misleading high scores
- Guidance now includes drill-specific blocker feedback during active scenarios

### Documentation
- Updated README to reflect public beta state
- Updated `docs/PROJECT_STATUS.md` to reflect promotion into `index.html`
- Updated `docs/RUN_MANIFEST.json` to reflect current beta runtime status

### Notes
- `index.html` is now the live public beta runtime authority
- `phoenix_v9_dev.html` remains the active development sandbox
- Future changes should continue in `phoenix_v9_dev.html` and only move into `index.html` after validation
