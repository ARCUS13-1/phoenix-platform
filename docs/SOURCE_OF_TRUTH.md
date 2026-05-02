# Source of Truth

## Parent Umbrella
**ARCUS Systems**

## Live Module
**PHOENIX Gen**

## File Authority

### Live runtime
- `index.html`

This is the only file that counts as live.

### Active dev file
- `phoenix_v10_dev.html`

This is where changes should happen first.

### Rollback / history
- `phoenix_v10_promoted_locked.html`
- `phoenix_v9_5_beta_locked.html`
- `phoenix_v8_baseline_locked.html`

These are reference and recovery files only.

## Rule

If files disagree:

- `index.html` wins for live runtime truth
- `phoenix_v10_dev.html` wins for current development work
- rollback files do not become live unless explicitly promoted

## Promotion Rule

Nothing is considered released until all of this happens:

1. validated
2. documented
3. promoted into `index.html`

When a promotion happens, update:

- `docs/PROJECT_STATUS.md`
- `docs/CHANGELOG.md`
- `docs/RUN_MANIFEST.json`
