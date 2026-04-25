# CHANGELOG

## [2026-04-19] — Public Beta Promotion (v9.5)

### Release Summary
Promoted the **v9.5 beta build** to the live runtime and advanced development into the v10 sandbox.

---

## Runtime Promotion

- `index.html` → now the live public beta runtime
- `phoenix_v9_5_beta_locked.html` → locked rollback snapshot
- `phoenix_v10_dev.html` → active development sandbox
- GitHub Pages updated to the promoted v9.5 build

---

## Core Systems Added

### Scenario Engine
- State-aware drill system using:
  - `armCondition`
  - `injectCondition`
  - `faultIds`
  - `maxDurationSec`

### Sync Gating
- Dwell-based sync validation using:
  - `syncReadyTimer`
  - `syncLostTimer`

### Operator Feedback
- Trip summary panel with captured snapshot
- Scenario-specific failure messaging
- Drill-aware blocker guidance
- Scope-status indicator:
  - OFFLINE / TRACKING / SYNC WINDOW / PARALLEL / TRIPPED

---

## Controls & Interaction

- Fine-trim governor and AVR nudge controls
- State-aware breaker labels with closing feedback
- Lower-load control for overcurrent recovery

---

## Analysis & Review

- Event markers on trend chart
- Marker index persistence through history trimming
- Scenario state panel enhancements:
  - overcurrent dwell window visibility
  - drill-state feedback

---

## Behavioral Changes

### Scenario Execution
- `loadScenario()` → moved to state-based sequencing
- `tick()` → now evaluates scenario state every frame
- `updatePhysics()` → now enforces dwell-based sync logic

### Drill Logic Improvements
- Overcurrent drill:
  - requires < 1400 A stability
  - requires continuous 3.0 s dwell window after injection
- Combined fault timeout extended for recovery realism

### Result Accuracy
- Clear result states:
  - SUCCESS
  - FAILED — TIMEOUT
  - FAILED — TRIP
- Failure scoring corrected to prevent misleading high scores

---

## Fixes

- Overcurrent drill:
  - no longer injects before sync
  - no longer completes immediately on injection
- Sync-window flicker reduced (dwell gating)
- Breaker close feedback improved (closing state clarity)
- Marker tracking stable across history trimming
- Guidance now reflects real drill blockers during execution

---

## Documentation Updates

- README updated for public beta
- `docs/SOURCE_OF_TRUTH.md` aligned with runtime structure
- `docs/PROJECT_STATUS.md` updated for v9.5 promotion
- `docs/RUN_MANIFEST.json` updated to current runtime state

---

## Runtime Roles (Current)

| File | Role |
|-----|------|
| `index.html` | Live public beta runtime |
| `phoenix_v9_5_beta_locked.html` | Locked rollback snapshot |
| `phoenix_v8_baseline_locked.html` | Historical baseline |
| `phoenix_v10_dev.html` | Active development sandbox |

---

## Notes

This release establishes:
- stable scenario execution
- trustworthy sync gating
- reliable failure semantics
- structured operator feedback

Foundation is now set for:
- v10 expansion
- horizon modules (relay, rotor, telemetry depth)
- improved replay and analysis tooling
### Notes
- Public beta is now live from `index.html`
- Future changes should continue in `phoenix_v10_dev.html` and only move into `index.html` after validation
- Rollback, historical baseline, and development files are not runtime-authoritative unless explicitly promoted
