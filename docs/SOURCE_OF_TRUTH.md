# Phoenix Source of Truth

Current canonical runtime file: `index.html`

## Authority Rules
- `index.html` is the only runtime-authoritative application file.
- All regression checks, behavior reviews, bug verification, and release validation must be performed against `index.html`.
- Non-canonical files may be used for sandbox development or rollback reference, but they are not shipped authority unless explicitly promoted.
- If any legacy or development file conflicts with `index.html`, `index.html` wins.

## Development Workflow
- New features may be explored in `phoenix_v9_dev.html`.
- Validated behavior is promoted into `index.html` only after function checks pass.
- `index.html` remains the shipped runtime target at all times.
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

## Non-Canonical Files
- `phoenix_v8_baseline_locked.html` = rollback reference only
- `phoenix_v9_dev.html` = development sandbox only

These files are not authoritative. If they conflict with `index.html`, `index.html` wins.
