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

## Runtime Authority
The single runtime source of truth is:

- `index.html`

Development or rollback files may exist in the repo, but they are not authoritative unless explicitly promoted in:

- `docs/SOURCE_OF_TRUTH.md`
- `docs/PROJECT_STATUS.md`
- `docs/RUN_MANIFEST.json`

## Current Runtime Scope
The current live runtime is a v8 mobile-core single-file build with:

- Manual sync + auto match
- Breaker OPEN / CLOSED / TRIPPED behavior
- Fault injection
- Sequence-of-events style logging
- Analysis view
- Timing Studio
- Telemetry / ghost-frequency overlay
- Mobile + tablet optimized UI

## Core Project Docs
- [Source of Truth](docs/SOURCE_OF_TRUTH.md)
- [Project Status](docs/PROJECT_STATUS.md)
- [Changelog](docs/CHANGELOG.md)
- [Run Manifest](docs/RUN_MANIFEST.json)

## Purpose
Built for real-world electrical testing training and system understanding.

Designed to simulate field conditions in a clean, interactive environment while preserving a single-file runtime for portability and validation discipline.

## Status
Active development.

Current shipped runtime authority: `index.html`  
Current planning track: v9 state machine architecture
