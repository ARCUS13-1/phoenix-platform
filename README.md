# ARCUS Systems

**PHOENIX Gen** Generator to grid synchronization training simulator.

It is a browser-based training simulator for learning how a generator is safely matched and connected to the power grid.

## Live Demo

**Try it here:**  
https://arcus13-1.github.io/phoenix-platform/

## What PHOENIX Gen Teaches

PHOENIX Gen is built around the real training problem:

- matching generator voltage to the grid
- matching generator frequency to the grid
- watching phase drift and synchroscope timing
- closing the breaker at the right moment
- understanding what happens when the close is unsafe
- recovering from fault drills and reviewing the event afterward

It is meant to make synchronization, breaker timing, fault response, and machine behavior easier to understand in a direct browser-based simulator.

## What’s New in v10

v10 keeps the core sync simulator from v9.5 and adds a stronger training layer around it.

### Added / expanded
- stress meter
- progression and unlocks
- playbook / briefing
- instructor shell
- expanded timing presets
- rotor visual tab
- mechanical rotor / stator training view
- magnetic field / sync training view
- stronger replay and review flow

### Rotor training upgrade
The rotor tab now teaches two different things on purpose:

- **Mechanical view** → shaft, bearings, coupling, vibration, stability, lock quality
- **Magnetic view** → rotor field, stator pickup, slip, phase error, field coupling

That split helps separate **mechanical stress** from **electrical stress** instead of blending them together.

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

## Platform Structure

- **ARCUS Systems** = parent umbrella
- **PHOENIX Gen** = current live module
- **ARCUS Grid Lab** = next planned module

## Docs

- [User Guide](docs/USER_GUIDE.md)
- [Source of Truth](docs/SOURCE_OF_TRUTH.md)
- [Project Status](docs/PROJECT_STATUS.md)
- [Changelog](docs/CHANGELOG.md)
- [Run Manifest](docs/RUN_MANIFEST.json)

## Feedback

Use **Issues** for bugs, contradictions, or broken behavior.

Use **Discussions** for realism feedback, workflow comments, and ideas.
