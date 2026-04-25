# Phoenix Engineering Platform

Phoenix is a mobile-first, single-file browser simulator for power-system operator training.

It focuses on:

- Grid ↔ generator synchronization
- Synchroscope training
- Breaker close / trip / reset logic
- Fault injection and recovery drills
- Scenario scoring and debriefs
- Sequence-of-events logging
- Timing / waveform logic
- Telemetry overlay with offline fallback

## Live Demo

https://arcus13-1.github.io/phoenix-platform/

## Current Status

Phoenix is in public beta.

The live beta is intended for:

- operator workflow testing
- scenario validation
- mobile and desktop UI review
- guidance and debrief feedback
- training realism feedback
- bug reporting

## Runtime Authority

The shipped public runtime is:

- `index.html`

Active development happens in:

- `phoenix_v10_dev.html`

Rollback and historical files may exist, but they are not the live runtime unless promoted and documented.

## Runtime Files

| File | Role |
|---|---|
| `index.html` | Shipped public beta runtime |
| `phoenix_v10_dev.html` | Active development sandbox |
| `phoenix_v9_5_beta_locked.html` | Current rollback snapshot |
| `phoenix_v8_baseline_locked.html` | Historical baseline |

Nothing is considered released until it is validated and promoted into `index.html`.

## Current Live Runtime Scope

The current public beta includes:

- manual sync and auto-match
- explicit state-machine flow
- dwell-time sync gating
- breaker OPEN / CLOSED / TRIPPED behavior
- fault injection and clearing
- six scenario drills
- operator guidance
- trip summary
- mission debrief
- SOE-style logging
- analysis view
- timing studio
- telemetry / ghost-frequency overlay
- trend markers
- fine-trim governor and AVR controls
- lower-load support for overcurrent recovery
- mobile and tablet optimized layout

## Beta Drill Set

Current drills:

- `quickstart`
- `vsag`
- `phaseerr`
- `overcurrent`
- `stuck`
- `combined`

## Feedback

Use **Issues** for:

- reproducible bugs
- scenario contradictions
- incorrect trip behavior
- score or result mismatches
- mobile layout defects
- guidance that conflicts with simulator behavior

Use **Discussions** for:

- training realism feedback
- usability comments
- feature ideas
- operator workflow suggestions
- general beta discussion

## Bug Report Checklist

When reporting an issue, include:

- device
- browser
- scenario used
- expected behavior
- actual behavior
- screenshot, if available
- exported log, if available

## Project Docs

- [Source of Truth](docs/SOURCE_OF_TRUTH.md)
- [Project Status](docs/PROJECT_STATUS.md)
- [Changelog](docs/CHANGELOG.md)
- [Run Manifest](docs/RUN_MANIFEST.json)

## Development Discipline

Promotion flow:

1. Build and test in `phoenix_v10_dev.html`
2. Validate all core controls and drills
3. Update docs and manifest
4. Promote into `index.html`
5. Lock the promoted runtime as the new rollback snapshot

This keeps the public beta stable enough for useful feedback instead of becoming a glowing junk drawer with a synchroscope.

## Near-Term Beta Focus

- stabilize all six drills
- improve debrief and result trust
- tighten operator guidance
- validate mobile behavior
- improve structured issue intake
- prepare for post-beta hardening

## Purpose

Phoenix is built for real-world electrical training and system understanding.

The goal is to make synchronization, breaker behavior, fault response, and event review easier to learn through an interactive single-file simulator that runs directly in the browser.
