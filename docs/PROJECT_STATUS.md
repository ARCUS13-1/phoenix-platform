# ARCUS Systems — Project Status

## Current Live Module
**PHOENIX Gen**

## Runtime Authority

| File | Role |
|---|---|
| `index.html` | live runtime |
| `phoenix_v10_promoted_locked.html` | current rollback |
| `phoenix_v9_5_beta_locked.html` | prior beta snapshot |
| `phoenix_v8_baseline_locked.html` | historical baseline |
| `phoenix_v10_dev.html` | active dev sandbox |

## What is Live Right Now

The current public build includes:

- grid ↔ generator sync training
- synchroscope and sync window logic
- breaker close / open / trip / reset
- six drill scenarios
- fault injection and clearing
- guidance panel
- debrief and trip summary
- timing studio
- analysis and event log
- telemetry overlay / ghost grid fallback
- stress meter
- rotor visual with mechanical + magnetic split
- progression / playbook / instructor shell
- mobile-friendly single-file runtime

## What is Done

- state machine flow
- deterministic reset path
- sync gating
- breaker truth
- scenario runner
- trip summary
- chart markers
- overcurrent recovery correction
- v9.5 promotion
- v10 shell expansion
- rotor training split
- public beta promotion into v10 runtime

## What is In Progress

- GitHub issue templates
- Discussions setup
- structured public beta intake
- post-promotion cleanup
- brand transition toward ARCUS Systems naming

## What is Next

- CSS cleanup / consolidation
- replay refinement
- post-beta hardening
- ARCUS Grid Lab planning
- stable release candidate prep

## Current Risks

- edge-case scenario behavior under wider public testing
- mobile readability on more devices
- wording drift between guidance and user expectation
- replay interpretation still needs polish
- some CSS sections still need consolidation

## Working Rule

Develop in `phoenix_v10_dev.html`.

Promote only after validation.

Then lock the promoted runtime.
