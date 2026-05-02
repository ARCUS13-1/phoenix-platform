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

v10 keeps the validated v9.5 sync simulator core, but expands the training layer around it.

#### Added
- Stress meter for faster operator awareness of unstable machine conditions
- Progression and unlocks view
- Playbook / briefing view
- Instructor mode shell
- Expanded timing presets tied more closely to drill and event flow
- Replay filtering and review improvements
- Rotor visual tab with two distinct teaching views:
  - Mechanical Rotor / Stator View
  - Magnetic Field / Sync View

#### Rotor Training Changes
The rotor visual was expanded to teach two different things on purpose:

- The **mechanical view** focuses on physical machine behavior:
  - rotor speed
  - shaft stress
  - bearing load
  - coupling stress
  - vibration / stability
  - synchronous lock quality

- The **magnetic view** focuses on the electrical relationship:
  - rotor field
  - stator pickup zones
  - slip
  - phase error
  - flux coupling
  - sync behavior

This improves training clarity by separating **mechanical stress** from **electrical stress** instead of blending them together.

#### Behavioral Improvements
- Rotor behavior now trains as a continuously rotating machine rather than a simple spinning icon
- After sync, the rotor remains in motion and stabilizes at synchronous speed instead of appearing to stop
- Review flow was expanded so logs, replay, markers, and timing views support the training story more clearly
  
#### Timing Studio Expansion
The Timing Studio was expanded beyond the original basic sync / trip / fault views.

New timing presets now cover a wider range of training and review states, including:

- quickstart
- vsag
- phaseerr
- overcurrent
- stuck
- combined
- breaker close
- unsafe close
- fault clear / recover
- sync loss
- overload recovery
- manual trim
- telemetry overlay

This makes the Timing Studio more useful as a training and review tool instead of just a small supporting utility. It now helps show drill flow, event order, recovery steps, and timing logic in a way that is easier to review after a run.

#### Summary
v9.5 established the core simulator.

v10 keeps that core intact and adds a stronger training shell, better review flow, and deeper machine/field teaching through the new rotor views.

### Changed
- v10 is now the live training shell
- public platform language is moving under ARCUS Systems
- PHOENIX Gen is now being treated as the first module, not the whole umbrella

### Known follow-up items
- CSS consolidation
- replay refinement
- broader device testing
- issue intake and Discussions setup
