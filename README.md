# Phoenix Platform

Mobile-first single-file power systems simulator for:

- Grid ↔ generator synchronization
- Synchroscope visualization
- Breaker logic and protection events
- Fault injection
- Analysis and event logging
- Timing / waveform logic
- Telemetry overlay with offline fallback

## Live Demo
https://arcus13-1.github.io/phoenix-platform/

## Beta Status

Phoenix is currently in **public beta**.

The live beta runtime is intended for:
- operator workflow testing
- scenario validation
- UI and guidance review
- mobile and desktop behavior checks
- bug reporting
- training realism feedback

## Runtime Authority

The single shipped runtime source of truth is:

- `index.html`

Development, rollback, or historical files may exist in the repo, but they are not authoritative unless explicitly reflected in:

- `docs/SOURCE_OF_TRUTH.md`
- `docs/PROJECT_STATUS.md`
- `docs/RUN_MANIFEST.json`

## Repository Runtime Roles

### Shipped Runtime
- `index.html`

### Current Locked Rollback
- `phoenix_v9_5_beta_locked.html`

### Historical Baseline
- `phoenix_v8_baseline_locked.html`

### Active Development Sandbox
- `phoenix_v10_dev.html`

Working rule:
- `index.html` is the only shipped runtime authority
- `phoenix_v9_5_beta_locked.html` is the current rollback target for the promoted beta
- `phoenix_v8_baseline_locked.html` remains the historical baseline
- `phoenix_v10_dev.html` is the active development sandbox
- nothing is considered released until it is validated and promoted into `index.html`

## Current Live Runtime Scope

The current live runtime is the promoted **v9.5 public beta** single-file build with:

- Manual sync + auto match
- Explicit state machine flow
- Dwell-time sync gating
- Breaker OPEN / CLOSED / TRIPPED behavior
- Fault injection and fault clear
- Scenario-based drills
- Operator guidance panel
- Trip summary panel
- Sequence-of-events style logging
- Analysis view
- Timing Studio
- Telemetry / ghost-frequency overlay
- Trend markers
- Fine-trim governor / AVR controls
- Lower-load support for overcurrent recovery
- Mobile + tablet optimized UI

## Beta Drill Set

Current drill set:
- quickstart
- vsag
- phaseerr
- overcurrent
- stuck
- combined

## Feedback Routing

Use **Issues** for:
- reproducible bugs
- scenario contradictions
- incorrect trip behavior
- wrong debrief result wording
- score/result mismatches
- mobile layout defects
- guidance that directly conflicts with simulator behavior

Use **Discussions** for:
- simulator impressions
- training realism feedback
- usability comments
- feature ideas
- operator workflow suggestions
- general beta discussion

## What to Include in Beta Feedback

When reporting a bug or drill issue, include:

- device
- browser
- scenario or drill used
- expected behavior
- actual behavior
- screenshot if available
- exported log if available

## Core Project Docs

- [Source of Truth](docs/SOURCE_OF_TRUTH.md)
- [Project Status](docs/PROJECT_STATUS.md)
- [Changelog](docs/CHANGELOG.md)
- [Run Manifest](docs/RUN_MANIFEST.json)

## Purpose

Built for real-world electrical testing training and system understanding.

Designed to simulate field conditions in a clean, interactive environment while preserving a single-file runtime for portability, validation discipline, and fast deployment.

## Status

Active development and public beta testing.

Current shipped runtime authority: `index.html`  
Current locked rollback target: `phoenix_v9_5_beta_locked.html`  
Current active development sandbox: `phoenix_v10_dev.html`

## Promotion Discipline

Promotion flow:
1. develop and test in `phoenix_v10_dev.html`
2. validate behavior manually
3. update docs and manifest
4. promote into `index.html`
5. lock the promoted runtime as the new rollback snapshot

This keeps the public runtime stable enough for meaningful beta feedback instead of turning the repo into a landfill with buttons.

## Notes on Telemetry and Usage Monitoring

At this stage, GitHub Pages is being used as the public beta host.

Feedback collection currently depends on:
- GitHub Issues
- GitHub Discussions
- direct tester feedback
- exported simulator logs

If usage analytics or session monitoring are later added, they should be explicitly documented in both the repo and the runtime.

## Near-Term Beta Focus

- stabilize all six drills under public beta use
- tighten result / debrief trustworthiness
- refine operator guidance clarity
- review mobile behavior under real testing
- improve structured issue intake
- prepare for post-beta hardening

## Repository Structure

Key files:
- `index.html` → shipped public runtime
- `phoenix_v10_dev.html` → active development sandbox
- `phoenix_v9_5_beta_locked.html` → current locked rollback snapshot
- `phoenix_v8_baseline_locked.html` → historical baseline
- `docs/PROJECT_STATUS.md` → current project state
- `docs/CHANGELOG.md` → release and sprint history
- `docs/RUN_MANIFEST.json` → runtime / promotion manifest

## Beta Request

If you are testing Phoenix:
- run a drill
- try to break it
- report what contradicted your expectations
- include evidence when possible

That is how this gets hardened into something trustworthy.
