# Phoenix Source of Truth

## 🧭 Runtime Authority

The single canonical runtime is:

- `index.html`

This file is the **only authoritative representation of the live simulator**.

---

## 📁 Runtime Roles

| File | Role |
|-----|------|
| `index.html` | Live runtime authority |
| `phoenix_v9_5_beta_locked.html` | Locked rollback snapshot |
| `phoenix_v8_baseline_locked.html` | Historical baseline |
| `phoenix_v10_dev.html` | Active development sandbox |

---

## ⚖️ Authority Rules

- `index.html` is the only runtime-authoritative file.
- All validation, regression checks, and behavior verification must be performed against `index.html`.
- Development, rollback, and historical files are **non-authoritative** unless explicitly promoted.
- If any file conflicts with `index.html`, **`index.html` is correct by definition**.

---

## 🔁 Development Workflow

All changes must follow this flow:

1. Develop and test in `phoenix_v10_dev.html`
2. Validate behavior manually (no assumptions)
3. Confirm no regression against runtime expectations
4. Promote into `index.html`
5. Lock promoted version as a rollback snapshot
6. Update documentation:
   - `docs/PROJECT_STATUS.md`
   - `docs/CHANGELOG.md`
   - `docs/RUN_MANIFEST.json`

---

## 🧪 Regression Requirements

Every promotion must pass the following checks against `index.html`:

### Core Controls
- SIM START / PAUSE / RESET
- GRID START warmup
- GEN START / GEN STOP

### Sync + Breaker Logic
- sync safety gating
- breaker OPEN / CLOSED / TRIPPED behavior
- close eligibility correctness

### Fault Handling
- fault inject
- fault clear
- correct trip behavior

### Analysis & Review
- live charts update correctly
- timing / waveform view renders
- analysis / logging (SOE) functions
- export / replay behaves correctly

### Telemetry
- telemetry overlay functions
- fallback behavior is stable when offline

---

## 🔒 Invariants

The following must never regress without explicit, documented intent:

- single-file runtime architecture
- no external dependencies
- conservative sync safety thresholds
- deterministic state-machine behavior
- scenarios remain startable, winnable, and single-ending
- guidance reflects actual simulator behavior

---

## 🧠 Working Rule

- `index.html` is the live system
- `phoenix_v10_dev.html` is the experiment
- nothing is real until it is promoted

If there is any uncertainty:

👉 trust the runtime  
👉 not the idea  
👉 not the dev file  
👉 not the intention
