# Phoenix Platform Progress

## Runtime Authority
- **Canonical runtime file:** `index.html`
- **Current locked rollback:** `phoenix_v9_5_beta_locked.html`
- **Historical baseline:** `phoenix_v8_baseline_locked.html`
- **Active development sandbox:** `phoenix_v10_dev.html`

## Current Runtime Snapshot
`index.html` is the live single-file public beta runtime and currently includes:

- Grid ↔ generator synchronizing
- Synchroscope + sync close window
- Explicit mode / event state machine behavior
- Dwell-time sync gating
- Breaker OPEN / CLOSED / TRIPPED behavior
- Fault injection and fault clear
- Scenario-based operator drills
- Operator guidance panel
- Trip summary panel
- Trend markers
- Analysis & logging
- Timing Studio
- Telemetry / ghost-frequency overlay
- Fine-trim governor / AVR controls
- Lower-load recovery support
- Scope-status indicator
- Mobile-safe single-file operation

## Current Development Snapshot
`phoenix_v10_dev.html` is the active development sandbox for future non-shipped changes and promotion candidates.

## Current Phase
- [x] Step 1 - Explicit state machine scaffold
- [x] Step 1A - Deterministic reset baseline
- [x] Step 2 - Command layer / next action integration
- [x] Step 2A - Closed-state display truth patch
- [x] Step 3 - Event-driven sync transitions + enhanced guidance
- [x] Step 4 - State-aware breaker button labels + closing-state clarity
- [x] Step 5 - Scenario runner scaffolding
- [x] Step 6 - Trip summary + chart markers
- [x] Step 6B - Scenario / physics truth alignment and overcurrent drill correction
- [x] Step 7 - Failure semantics, blocker guidance, and beta promotion preparation
- [x] Manual validation completed for current promotion build
- [x] Promoted tested v9.5 beta build into `index.html`
- [ ] GitHub issue templates enabled
- [ ] GitHub Discussions enabled
- [ ] Structured public beta intake cycle active
- [ ] Post-beta defect hardening pass
- [ ] Stable release candidate review

## Working Rule
- `index.html` remains the shipped runtime authority.
- `phoenix_v9_5_beta_locked.html` is the current rollback target for the promoted beta.
- `phoenix_v8_baseline_locked.html` remains the historical baseline.
- `phoenix_v10_dev.html` is the active development sandbox.
- No feature is released until validation passes and docs / manifests are updated.

## Public Beta Notes
- Public beta is active.
- Feedback should be routed through GitHub Issues and GitHub Discussions.
- Direct tester feedback is still useful, but repo-tracked feedback is preferred for reproducibility.
- Analytics are not currently authoritative because no official beta telemetry layer has been documented yet.

## Current Risks
- Public beta feedback may surface scenario edge cases not caught in manual validation.
- Mobile readability should continue to be checked under real-world device testing.
- Guidance wording may still need refinement as broader testers interact with the drills.
- Future fixes should continue in `phoenix_v10_dev.html` and only be promoted after validation.

## Immediate Next Steps
1. Enable GitHub issue templates
2. Enable GitHub Discussions
3. Begin structured beta feedback collection
4. Triage scenario logic, UI clarity, and mobile issues
5. Continue development in `phoenix_v10_dev.html`
6. Promote only after the next validated pass
