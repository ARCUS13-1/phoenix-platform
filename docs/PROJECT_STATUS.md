# Phoenix Platform Progress

## 🧭 Runtime Authority

| File | Role |
|-----|------|
| `index.html` | Live public beta runtime (canonical) |
| `phoenix_v9_5_beta_locked.html` | Locked rollback snapshot |
| `phoenix_v8_baseline_locked.html` | Historical baseline |
| `phoenix_v10_dev.html` | Active development sandbox |

**Rule:**  
No feature is considered released until it is validated and promoted into `index.html`.

---

## ⚙️ Current Runtime (v9.5 Public Beta)

The live runtime (`index.html`) currently includes:

### Core Simulation
- Grid ↔ generator synchronization
- Synchroscope with sync close window
- Explicit mode / event-driven state machine
- Dwell-time sync gating
- Breaker OPEN / CLOSED / TRIPPED behavior

### Scenarios & Faults
- Scenario-based operator drills
- Fault injection and clearing
- Lower-load recovery support (overcurrent)

### Operator Feedback
- Guidance panel (state-aware)
- Trip summary panel
- Scope-status indicator (OFFLINE → PARALLEL)

### Analysis & Review
- Trend markers
- Analysis + logging (SOE-style)
- Timing Studio
- Telemetry / ghost-frequency overlay

### Controls
- Fine-trim governor / AVR controls

### Platform
- Mobile-safe single-file runtime

---

## 🧪 Development Status (v10)

`phoenix_v10_dev.html` is the active sandbox for:

- new features
- structural changes
- bug fixes prior to promotion

No changes are considered live until validated and promoted.

---

## 📍 Current Phase Progress

### Completed
- [x] State machine scaffold
- [x] Deterministic reset baseline
- [x] Command layer / next-action integration
- [x] Closed-state display truth patch
- [x] Event-driven sync transitions + guidance
- [x] Breaker label + closing-state clarity
- [x] Scenario runner scaffolding
- [x] Trip summary + chart markers
- [x] Scenario / physics truth alignment
- [x] Overcurrent drill correction
- [x] Failure semantics + blocker guidance
- [x] Manual validation (v9.5)
- [x] Public beta promotion → `index.html`

### In Progress
- [ ] GitHub issue templates enabled
- [ ] GitHub Discussions enabled
- [ ] Structured beta intake active

### Upcoming
- [ ] Post-beta defect hardening
- [ ] Stability pass for release candidate

---

## 📢 Public Beta Notes

- Public beta is active
- Feedback should be submitted via:
  - GitHub Issues (bugs, contradictions)
  - GitHub Discussions (feedback, ideas)

Direct feedback is still useful, but **tracked issues are preferred for reproducibility**.

---

## ⚠️ Current Risks

- Scenario edge cases may surface under broader testing
- Mobile usability requires real-device validation
- Guidance wording may not fully match user expectation yet
- Replay / analysis interpretation may need refinement

---

## 🔁 Development Discipline

All changes must follow:

1. Develop in `phoenix_v10_dev.html`
2. Validate behavior manually
3. Confirm no regression across:
   - controls
   - scenarios
   - sync logic
4. Update docs + manifest
5. Promote into `index.html`
6. Lock new rollback snapshot

---

## 🚧 Immediate Next Steps

1. Finalize GitHub issue templates
2. Enable GitHub Discussions
3. Begin structured beta feedback intake
4. Triage:
   - scenario logic issues
   - UI clarity issues
   - mobile issues
5. Continue development in `phoenix_v10_dev.html`
6. Promote only after validated pass
