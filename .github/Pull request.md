# Phoenix PR — Change Summary

## What does this change do?

Briefly describe what was changed.

- bug fix / UI fix / logic fix / refactor / docs
- affected areas (e.g. sync logic, rotor, mobile layout, SOE, etc.)

---

## Why is this change needed?

Explain the problem this PR solves.

- what was broken, confusing, or missing
- what tester feedback or issue triggered this

---

## Scope of change

Check all that apply:

- [ ] UI / layout
- [ ] Sync / breaker logic
- [ ] Scenario behavior
- [ ] Guidance / training clarity
- [ ] SOE / replay / analysis
- [ ] Telemetry / timing
- [ ] Performance
- [ ] Docs / README
- [ ] Other:

---

## What was NOT changed

Call this out explicitly (important for Phoenix discipline):

- No changes to core simulator physics unless listed above
- No changes to thresholds unless documented
- No new external dependencies
- No multi-file refactor

---

## Validation checklist

Confirm all of these were tested before submitting:

### Core controls
- [ ] SIM START / PAUSE / RESET
- [ ] GRID START
- [ ] GEN START / STOP
- [ ] BREAKER CLOSE / OPEN / TRIP / RESET

### Sync behavior
- [ ] Sync-ready indicator matches actual close eligibility
- [ ] Close button enables only when safe
- [ ] Unsafe close still blocked or trips correctly

### Scenarios
- [ ] quickstart
- [ ] vsag
- [ ] phaseerr
- [ ] overcurrent
- [ ] stuck
- [ ] combined

### Review systems
- [ ] SOE log updates correctly
- [ ] replay works (no crashes or dead controls)
- [ ] timing studio renders
- [ ] telemetry overlay still functions

### Mobile check
- [ ] Tabs are reachable
- [ ] No overlap with sync dock
- [ ] Buttons remain thumb-safe
- [ ] No horizontal overflow issues

---

## Screenshots / Evidence (if applicable)

Add screenshots, logs, or exported data if relevant.

---

## Risk assessment

What could this break?

- list possible regressions
- list areas that need extra testing

---

## Notes

Anything reviewers should pay attention to.

- edge cases
- temporary logic
- known limitations
