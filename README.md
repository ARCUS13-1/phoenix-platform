# ARCUS Systems

ARCUS Systems is the umbrella.

The first live module is **PHOENIX Gen**.

PHOENIX Gen is a browser-based training simulator for learning how a generator is safely matched and connected to the grid.

## Live Demo

https://arcus13-1.github.io/phoenix-platform/

## What PHOENIX Gen Does

It focuses on:

- grid ↔ generator synchronization
- synchroscope training
- breaker close / trip / reset logic
- fault drills and recovery
- scoring and debriefs
- event logging
- timing view
- telemetry overlay
- rotor / machine teaching visuals

## Current Status

Public beta.

This build is for:

- real device testing
- drill validation
- UI clarity
- debrief / guidance trust
- training realism feedback
- bug finding

## Current Structure

- **ARCUS Systems** = parent umbrella
- **PHOENIX Gen** = current live module
- **ARCUS Grid Lab** = next planned module

## Runtime Files

| File | Role |
|---|---|
| `index.html` | live public runtime |
| `phoenix_v10_dev.html` | active development sandbox |
| `phoenix_v10_promoted_locked.html` | current rollback snapshot |
| `phoenix_v9_5_beta_locked.html` | prior beta snapshot |
| `phoenix_v8_baseline_locked.html` | historical baseline |

## Quick Start

1. Press **SIM START**
2. Press **GRID START**
3. Wait for the grid to become healthy
4. Press **GEN START**
5. Use **AUTO MATCH** or trim manually
6. Watch the synchroscope and sync indicators
7. Close the breaker only when the simulator shows a safe sync condition
8. Review the debrief or trip summary

## Current Drills

- `quickstart`
- `vsag`
- `phaseerr`
- `overcurrent`
- `stuck`
- `combined`

## Docs

- [User Guide](docs/USER_GUIDE.md)
- [Source of Truth](docs/SOURCE_OF_TRUTH.md)
- [Project Status](docs/PROJECT_STATUS.md)
- [Changelog](docs/CHANGELOG.md)
- [Run Manifest](docs/RUN_MANIFEST.json)

## Feedback

Use **Issues** for bugs, contradictions, or broken behavior.

Use **Discussions** for realism feedback, workflow comments, and ideas.

## Why this exists

The goal is simple:

Make synchronization, breaker timing, fault response, and event review easier to learn through a direct browser-based simulator.
