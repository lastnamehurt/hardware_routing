# Studio GitHub Issues - Draft

## Overview

17 issues across 6 phases for setting up the home studio workflow.

## Studio Layout

```
┌─────────────────────────────────────────────────────────────────────┐
│                                                                     │
│   VOCALS WORKSTATION          THE DESK           PRODUCTION         │
│   (left)                      (center)           WORKSTATION        │
│   48ch Patchbay               No patchbay        48ch Patchbay      │
│                                                                     │
└─────────────────────────────────────────────────────────────────────┘
```

## Stations

### The Desk (center)
- Tascam Mixcast Pro 4
- Shure mic (high-end)
- No patchbay — connects to Vocals workstation via Presonus channel strip

### Vocals Workstation (left)
| Gear | Type |
|------|------|
| Scarlett OctoPre | Interface (w/ compressor expansion) |
| WA73 | Mic Preamp (for Mojave mic) |
| FET Compressor/Limiter | Dynamics |
| Klark Teknik EQ | EQ (**possibly broken**) |
| Presonus Channel Strip | Preamp (Shure mic → Tascam) |
| Mac Studio | Computer (Ableton/Pro Tools) |
| 48ch Patchbay | Routing |

**Cross-station access:** Via tie lines, can access any gear on Production workstation

### Production Workstation (right)
| Gear | Type |
|------|------|
| MPC XL | Sampler/DAW |
| Yamaha DGX 670 | Keys (88 weighted) — primary MIDI controller |
| Arturia Minifreak | Synth — sound design → sample into MPC |
| MicroKorg | Vocoder/Synth (rarely used) |
| Numark Mixstream Pro | DJ Controller |
| WA Bus Compressor VCA | Dynamics |
| Pro VLA 2 | Compressor (tube/opto warmth) |
| DBX 286s | Channel Strip |
| Stereo Ultragraph Pro EQ | EQ (Behringer) |
| Golden Age MK3 EQ | EQ (mono, shared) |
| Lexicon MXL | FX (dual stereo = 2 independent stereo FX, shared) |
| Scarlett OctoPre | Interface |
| Steinberg UR-RT4 | Interface (Rupert Neve transformers) |
| 48ch Patchbay | Routing |

## Files

| File | Issues | Description |
|------|--------|-------------|
| `phase-0-the-desk.md` | #15 | Tascam integration, daily Zoom/work workflow |
| `phase-1-patchbay.md` | #1, #2, #2b, #3, #3b | Patchbay reorganization (both workstations) |
| `phase-2-mpc.md` | #4-5 | MPC as creative center |
| `phase-3-ableton.md` | #6-8 | MPC → Ableton workflow |
| `phase-4-pro-tools.md` | #9-11 | Ableton → Pro Tools handoff |
| `phase-5-operations.md` | #12-14 | Backup, gain staging, decision checklist |

## Labels to Create

**Phases:**
- `phase-0`, `phase-1`, `phase-2`, `phase-3`, `phase-4`, `phase-5`

**Stations:**
- `the-desk`, `vocals-workstation`, `production-workstation`

**Gear:**
- `patchbay`, `mpc`, `ableton`, `pro-tools`, `tascam`

**Task Types:**
- `planning`, `hardware`, `documentation`, `template`, `testing`, `workflow`, `setup`, `control`, `backup`, `operations`, `routing`, `ipad`, `critical`

## Mental Model

```
MPC (ideas, groove, feel)
    ↓
Ableton (exploration, arrangement, performance)
    ↓
Pro Tools (commitment, vocals, polish)
```

## Dependencies

```
Phase 1 (Patchbay):
#1 → #2 (Vocals) → #3
  → #2b (Production) ↗
                     ↓
                     #5 (MPC verification)
                     #15 (Tascam integration)

#3b (Klark EQ test) — no dependencies

Phase 3 (Ableton):
#6 → #7
  → #8

Phase 4 (Pro Tools):
#9 → #10
```

## Critical Path

**Priority 1 (daily workflow):** #1 → #2 → #15 (Tascam/Zoom setup)
**Priority 2 (creative foundation):** #2b → #4 → #5 (MPC + patchbay)
**Priority 3 (DAW integration):** #6 → #7 → #9 → #10 (Ableton + Pro Tools)
