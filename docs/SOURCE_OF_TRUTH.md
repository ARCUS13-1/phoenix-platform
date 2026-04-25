# Phoenix Source of Truth

## Runtime Authority

The live simulator is:

- `index.html`

That’s the only file that actually matters when it comes to how Phoenix behaves.

---

## Runtime Roles

- `index.html` → live runtime (this is what users are actually running)
- `phoenix_v9_5_beta_locked.html` → rollback snapshot if something breaks
- `phoenix_v8_baseline_locked.html` → older baseline kept for reference
- `phoenix_v10_dev.html` → where all new work happens

---

## Rules

- If something works in `index.html`, that’s the truth.
- If something works in a dev file but not in `index.html`, it’s not released.
- If there’s a conflict between files, trust `index.html` and ignore the rest.

---

## How changes actually get in

Everything goes through the same path:

1. Build it in `phoenix_v10_dev.html`
2. Test it like you’re trying to break it
3. Make sure nothing else got worse
4. Move it into `index.html`
5. Lock that version as the new rollback file
6. Update the docs so they match reality

No shortcuts here. If it’s not tested, it doesn’t move.

---

## What has to work before anything gets promoted

### Core controls
- SIM START / PAUSE / RESET
- GRID START
- GEN START / STOP

### Sync + breaker behavior
- sync window actually matches close eligibility
- breaker opens, closes, and trips correctly

### Faults
- faults inject when they’re supposed to
- faults clear cleanly
- trips make sense

### Analysis + review
- charts update
- timing view renders
- logs make sense
- replay doesn’t break

### Telemetry
- overlay works
- fallback works if data isn’t there

---

## Things that should not drift

These are basically guardrails:

- still a single-file simulator
- no random dependencies added
- sync safety stays conservative
- state machine stays deterministic
- drills stay winnable and not contradictory
- guidance matches what the simulator actually does

---

## Working rule

- `index.html` = real system
- `phoenix_v10_dev.html` = sandbox

Nothing is real until it’s promoted.

If something feels off:
don’t guess — go check the runtime.
