# Phase 2 — MPC as the Creative Center

**Goal:** MPC works standalone *and* feeds DAWs cleanly.

---

## Creative Workflow

```
┌─────────────────────────────────────────────────────────────────┐
│                                                                 │
│   DGX 670 (88 weighted keys)                                    │
│       │                                                         │
│       ├── MIDI out ──────────► MPC XL (capture performance)     │
│       │                                                         │
│       └── Audio out ─────────► MPC XL (sample DGX sounds)       │
│                                                                 │
│   Minifreak                                                     │
│       │                                                         │
│       └── Audio out ─────────► MPC XL (sample after patch design)│
│                                                                 │
│   (Optional: DGX MIDI → Minifreak for performing Minifreak      │
│    sounds on weighted keys)                                     │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

---

## Issue #4: Create MPC internal template

**Labels:** `phase-2`, `mpc`, `template`

**Description:**
Build a default MPC project template for rapid creative starts, optimized for the DGX + Minifreak workflow.

**Tasks:**

### MIDI Configuration
- [ ] MIDI track for DGX 670 input (capture performances)
- [ ] MIDI track for Minifreak control (optional: play Minifreak via DGX)
- [ ] Enable MIDI Clock + MMC receive/send
- [ ] Set DGX as primary MIDI input device

### Audio Tracks (Pre-Named)
- [ ] "DGX Sample" — for sampling DGX 670 sounds
- [ ] "Minifreak Sample" — for sampling Minifreak patches
- [ ] "Drums" — drum program
- [ ] "Bass"
- [ ] "Keys"
- [ ] "FX / Atmos"

### Defaults
- [ ] Set default BPM (your preference)
- [ ] Set default swing preferences
- [ ] Input monitoring setup for quick sampling

**Definition of Done:**
New project opens → ready to perform on DGX and capture MIDI/audio in <30 seconds.

---

## Issue #5: MPC to patchbay verification

**Labels:** `phase-2`, `mpc`, `patchbay`, `testing`

**Description:**
Verify MPC integrates properly with patchbay routing for both output processing and input sampling.

**Output Tests (MPC → Processing → MPC or DAW):**
- [ ] MPC → WA Bus Compressor → MPC (working)
- [ ] MPC → Pro VLA 2 → MPC (working)
- [ ] MPC → Golden Age MK3 EQ → MPC (working)
- [ ] MPC → Lexicon MXL → MPC (working)
- [ ] Parallel processing via patchbay (working)

**Input Tests (Instruments → MPC Sampling):**
- [ ] DGX 670 audio → patchbay → MPC input (clean signal)
- [ ] Minifreak audio → patchbay → MPC input (clean signal)
- [ ] DGX 670 → processing → MPC input (colored signal)
- [ ] Minifreak → processing → MPC input (colored signal)

**MIDI Tests:**
- [ ] DGX 670 MIDI → MPC (latency acceptable)
- [ ] MPC MIDI → Minifreak (if controlling externally)

**Definition of Done:**
- Processing chains work with no gain-staging surprises
- Sampling workflow is immediate (DGX/Minifreak → MPC)
- MIDI performance capture has acceptable latency

**Blocked by:** #2b
