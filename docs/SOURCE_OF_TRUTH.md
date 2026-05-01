# Source of Truth

## Parent Platform
**ARCUS Systems**

## Current Live Module
**PHOENIX Gen**

## Runtime Authority

The current shipped public runtime is:

- `index.html`

This is the only runtime-authoritative application file.

## Development Authority

Active development happens in:

- `phoenix_v10_dev.html`

This file is the working sandbox for future changes and is **not** considered live until explicitly promoted.

## Rollback / Historical Files

The following files are retained for rollback and historical reference:

- `phoenix_v10_promoted_locked.html` = current locked rollback snapshot
- `phoenix_v9_5_beta_locked.html` = prior beta snapshot
- `phoenix_v8_baseline_locked.html` = historical baseline

These files are not runtime-authoritative unless explicitly promoted.

## Authority Rules

- `index.html` is the only live runtime authority.
- `phoenix_v10_dev.html` is the active development authority.
- Locked rollback files are reference and recovery points only.
- If any non-runtime file disagrees with `index.html`, `index.html` wins.
- Nothing is considered released until:
  1. validated,
  2. documented,
  3. promoted into `index.html`.

## Promotion Rule

Any promotion into `index.html` must be accompanied by updates to:

- `docs/PROJECT_STATUS.md`
- `docs/CHANGELOG.md`
- `docs/RUN_MANIFEST.json`

## Platform Direction

Public platform direction is now organized as:

- **ARCUS Systems** = parent umbrella
- **PHOENIX Gen** = current live module
- **ARCUS Grid Lab** = next planned module

Legacy naming may still appear in older files or historical records, but ARCUS Systems is now the preferred public umbrella.
