# Changelog

## [2026-05-01] — v10 Public Beta Promotion

### Big picture
Promoted the v10 build to the live runtime.

Also shifted the public direction toward:

- **ARCUS Systems** = umbrella
- **PHOENIX Gen** = first live module

### Runtime
- `index.html` is now the live v10 runtime
- `phoenix_v10_promoted_locked.html` added as the current rollback snapshot
- `phoenix_v10_dev.html` remains the active sandbox
- `phoenix_v9_5_beta_locked.html` retained as the prior beta snapshot

### v10 Training Expansion Highlights

v10 keeps the core simulator from v9.5, but adds a much stronger training layer around it.

#### Added
- stress meter
- progression and unlocks
- playbook / briefing
- instructor mode shell
- expanded timing presets
- stronger replay and review tools
- rotor visual tab with:
  - Mechanical Rotor / Stator View
  - Magnetic Field / Sync View

#### Rotor Training Upgrade
The rotor tab now teaches two different parts of the machine on purpose.

The **mechanical view** is there to show machine behavior like shaft load, bearing stress, coupling stress, vibration, stability, and lock quality.

The **magnetic view** is there to show the field relationship like slip, phase error, stator pickup, rotor field, and flux coupling.

That split matters because mechanical stress and electrical stress are not the same thing, and the sim now teaches that better.

#### Behavior Changes
- the rotor now behaves more like a real continuously rotating machine
- after sync, it stays rotating and stabilizes at synchronous speed
- replay, markers, timing, and review tools now support the training flow better

#### Summary
v9.5 gave the project a solid sync simulator.

v10 keeps that core and adds a better training shell, better review flow, and better machine/field teaching.

### Changed
- v10 is now the live training shell
- public platform language is moving under ARCUS Systems
- PHOENIX Gen is now being treated as the first module, not the whole umbrella

### Known follow-up items
- CSS consolidation
- replay refinement
- broader device testing
- issue intake and Discussions setup
