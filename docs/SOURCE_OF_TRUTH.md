# Phoenix Source of Truth

Current canonical application file: `index.html`

Rules:
- All edits, fixes, reviews, and feature additions must start from `index.html`
- Legacy HTML files are reference-only unless explicitly promoted
- If any legacy file conflicts with `index.html`, `index.html` wins
- Regression checks must verify:
  - SIM START / PAUSE / RESET
  - GRID START warmup
  - GEN START / GEN STOP
  - sync safety gating
  - breaker OPEN / CLOSED / TRIPPED
  - fault inject / clear
  - live charts
  - timing / waveform view
  - analysis / logging

## Non-Canonical Files

- `phoenix_v8_baseline_locked.html` = rollback reference only
- `phoenix_v9_dev.html` = temporary development sandbox only

These files are not authoritative. If they conflict with `index.html`, `index.html` wins.
