# Phoenix Source of Truth

## Current Runtime Authority
The single canonical shipped runtime file is:

- `index.html`

## Repository Runtime Roles

### Shipped Runtime
- `index.html`

### Current Locked Rollback
- `phoenix_v9_5_beta_locked.html`

### Historical Baseline
- `phoenix_v8_baseline_locked.html`

### Active Development Sandbox
- `phoenix_v10_dev.html`

## Authority Rules
- `index.html` is the only runtime-authoritative application file.
- All regression checks, behavior reviews, bug verification, and release validation must be performed against `index.html`.
- Development, rollback, and historical files may exist in the repo, but they are not shipped authority unless explicitly promoted.
- If any non-runtime file conflicts with `index.html`, `index.html` wins.

## Development Workflow
- New features must be explored and validated in `phoenix_v10_dev.html`.
- Validated behavior is promoted into `index.html` only after function checks and manual validation pass.
- Once promoted, the shipped runtime should be locked as a rollback snapshot.
- Any promotion into `index.html` must update:
  - `docs/PROJECT_STATUS.md`
  - `docs/CHANGELOG.md`
  - `docs/RUN_MANIFEST.json`

## Regression Checks
Regression checks against `index.html` must verify:
- SIM START / PAUSE / RESET
- GRID START warmup
- GEN START / GEN STOP
- sync safety gating
- breaker OPEN / CLOSED / TRIPPED
- fault inject / clear
- live charts
- timing / waveform view
- analysis / logging
- export / replay behavior
- telemetry overlay fallback behavior

## Working Rule
- `index.html` remains the only shipped runtime authority
- `phoenix_v9_5_beta_locked.html` is the current rollback target
- `phoenix_v8_baseline_locked.html` remains the historical baseline
- `phoenix_v10_dev.html` is the active development sandbox
- Nothing is considered released until validated and promoted into `index.html`
