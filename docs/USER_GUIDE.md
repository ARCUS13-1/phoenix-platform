# PHOENIX Gen — User Guide

## What this is

PHOENIX Gen is a browser-based training simulator for safely syncing a generator to the grid.

It helps you learn:

- voltage match
- frequency match
- phase timing
- breaker timing
- fault response
- event review

## Quick Start

1. Press **SIM START**
2. Press **GRID START**
3. Wait for the grid to become healthy
4. Press **GEN START**
5. Use **AUTO MATCH** or trim governor / AVR manually
6. Watch the synchroscope and sync indicators
7. Close the breaker only when the simulator shows safe sync
8. Review the debrief or trip summary

## Main Tabs

### Grid Simulator
This is the main training screen.

Use it for:
- startup
- manual trim
- auto-match
- breaker action
- drill runs
- guidance
- debrief

### Analysis & Logging
Use this for:
- event log
- trend view
- replay tools

### Timing Studio
Use this for:
- simplified timing logic review
- drill sequence review

### Grid Overlay
Use this for:
- telemetry overlay
- ghost grid reference
- context view

### Playbook / Briefing
Use this for:
- drill intent
- training reminders
- scenario framing

### Progression & Unlocks
Use this for:
- tracking training progress
- total score
- unlocked tools or views

### Rotor Visual
Two views live here:

#### Mechanical view
Shows:
- shaft / bearing / coupling stress
- rotor speed
- lock state
- machine behavior

#### Magnetic view
Shows:
- rotor field
- stator pickup zones
- slip
- phase error
- field coupling

### Instructor Mode
Reserved for training control, presets, and future overlays.

## Drills

### quickstart
Clean sync. Best place to start.

### vsag
Voltage sag drill. Recover voltage and sync safely.

### phaseerr
Phase mismatch drill. Reduce slip and close at the right time.

### overcurrent
Post-sync overload recovery. Manage current without tripping.

### stuck
Mechanical obstruction drill. Diagnose and recover.

### combined
Multi-fault drill. More than one thing is wrong at once.

## What the debrief means

The debrief is your end-of-run summary.

It should tell you:
- what the drill was
- how long it took
- whether you made unsafe attempts
- whether you tripped
- what your score was

## What the trip summary means

If protection trips, the trip summary is there to help you understand why.

It should show:
- trip cause
- conditions at trip
- active faults
- recovery guidance

## Notes

- This is a training simulator, not a protection study tool.
- Timing Studio is an instructional view, not oscillography.
- Telemetry overlay is informational only.
- Public beta feedback is expected and useful.
