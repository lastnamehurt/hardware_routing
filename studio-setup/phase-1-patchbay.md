# Phase 1 — Patchbay Reorganization (Foundation)

**Goal:** Make MPC, outboard gear, and DAWs interchangeable without re-patching the room.

---

## Studio Layout Overview

```
┌─────────────────────────────────────────────────────────────────────┐
│                                                                     │
│   VOCALS WORKSTATION          THE DESK           PRODUCTION         │
│   (left)                      (center)           WORKSTATION        │
│                                                  (right)            │
│   ┌─────────────────┐     ┌──────────────┐    ┌─────────────────┐  │
│   │ 48ch Patchbay   │     │ Tascam       │    │ 48ch Patchbay   │  │
│   │                 │     │ Mixcast Pro 4│    │                 │  │
│   │ Scarlett Octo   │     │              │    │ MPC XL          │  │
│   │ WA73 Pre        │     │ Shure Mic    │    │ Minifreak       │  │
│   │ FET Comp        │     │ (no patchbay)│    │ Yamaha DGX 670  │  │
│   │ Klark EQ        │     │              │    │ WA Bus Comp     │  │
│   │                 │◄────┼──────────────┼───►│ Pro VLA 2       │  │
│   │ Mac Studio      │     │              │    │ Ultragraph EQ   │  │
│   │ (Ableton/PT)    │     │              │    │ Scarlett Octo   │  │
│   │                 │     │              │    │ Lexicon MXL     │  │
│   └─────────────────┘     └──────────────┘    └─────────────────┘  │
│                                                                     │
│   ◄──────────── Tie lines for cross-station access ─────────►      │
│   (Either workstation can access gear on the other)                │
│                                                                     │
└─────────────────────────────────────────────────────────────────────┘
```

---

## Vocals Workstation Gear

| Gear | Type | Notes |
|------|------|-------|
| Scarlett OctoPre | Interface/Preamp | With compressor expansion pack |
| WA73 | Mic Preamp | Dedicated to Mojave mic |
| FET Compressor/Limiter | Dynamics | Vocal chain |
| Klark Teknik EQ | EQ | **Possibly broken - needs testing** |
| Presonus Channel Strip | Preamp | For Shure mic → Tascam (desk) |
| Mac Studio | Computer | Runs Ableton + Pro Tools |
| 48ch Patchbay | Routing | — |

**Cross-Station Access:**
Via tie lines, can access any gear on Production workstation (and vice versa).

---

## Production Workstation Gear

| Gear | Type | Notes |
|------|------|-------|
| **Instruments** | | |
| MPC XL | Sampler/DAW | Creative center |
| Yamaha DGX 670 | Keys (88 weighted) | Primary MIDI controller + sound source |
| Arturia Minifreak | Synth | Sound design → sample into MPC |
| MicroKorg | Vocoder/Synth | Rarely used |
| Numark Mixstream Pro | DJ Controller | Pre-wire for quick access |
| **Dynamics** | | |
| WA Bus Compressor VCA | Compressor | Mix bus / stems |
| Pro VLA 2 | Compressor | Tube/opto warmth — smooth on vocals, bass, mix bus |
| DBX 286s | Channel Strip | Budget option, still usable |
| **EQ** | | |
| Stereo Ultragraph Pro EQ | EQ | Behringer |
| Golden Age MK3 EQ | EQ (mono) | Shared with Vocals workstation |
| **FX** | | |
| Lexicon MXL | FX | Dual stereo, shared with Vocals |
| **Interfaces** | | |
| Scarlett OctoPre | Interface | — |
| Steinberg UR-RT4 | Interface | 4-ch USB with Rupert Neve transformers |
| **Routing** | | |
| 48ch Patchbay | Routing | — |

---

## Issue #1: Finalize patchbay signal philosophy

**Labels:** `phase-1`, `patchbay`, `planning`

**Description:**
Establish the foundational signal routing philosophy for both workstations.

---

### Key Decisions

| Decision | Choice |
|----------|--------|
| Creative brain | MPC XL |
| Routing brain | Patchbays (one per workstation) |
| Capture + polish | DAWs (Ableton / Pro Tools) |
| Signal level | **Line-level only** (no mic-level through patchbay) |
| Layout | **Top row = outputs, Bottom row = inputs** |

---

### Normalling Decision: HALF-NORMAL

**Why half-normal (not full-normal or thru)?**

```
HALF-NORMAL BEHAVIOR:
┌─────────────────────────────────────────────────────────────────┐
│                                                                 │
│   TOP ROW (output)     ●────────┬────────► Default destination  │
│                                 │                               │
│                                 │ (signal continues even when   │
│                                 │  you plug into bottom row)    │
│                                 │                               │
│   BOTTOM ROW (input)   ●────────┘                               │
│                        ▲                                        │
│                        │                                        │
│              Plug here to TAP/MULT the signal                   │
│              WITHOUT breaking the normal connection             │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

**Benefits:**
- Default signal paths work without any cables
- Plug into TOP row → breaks normal, sends signal elsewhere
- Plug into BOTTOM row → taps signal WITHOUT breaking the normal flow (mult)
- Best of both worlds: convenience + flexibility

**Exception — Use THRU (de-normalled) for:**
- Cross-patch tie lines (no default connection needed)
- FX send/return points (patch manually when needed)

---

### Cross-Patch (Tie Lines) — How to Access Gear on the Other Workstation

---

#### Golden Rules

```
┌────────────────────────────────────────────────────────────────────┐
│                                                                    │
│  1. TOP ROW = signal comes OUT      (it's a source)                │
│     BOTTOM ROW = signal goes IN     (it's a destination)           │
│                                                                    │
│  2. Tie lines are DUMB CABLES — just copper wire between           │
│     the two patchbays. No magic. No processing.                    │
│                                                                    │
│  3. You MUST patch at BOTH patchbays to complete the circuit.      │
│     Sitting at Vocals? Walk to Production once to set up           │
│     the gear side, then return to Vocals.                          │
│                                                                    │
│  4. Patching is always TOP → BOTTOM                                │
│     (source to destination, output to input)                       │
│                                                                    │
└────────────────────────────────────────────────────────────────────┘
```

---

#### What Are Tie Lines?

Permanent TRS cables connecting dedicated jacks on both patchbays. They just sit there waiting for you to use them.

```
VOCALS PATCHBAY                              PRODUCTION PATCHBAY
      (back)                                       (back)

  "To Prod 1"   ●═══════ TRS cable ═══════════●   "From Vocals 1"

  "From Prod 1" ●═══════ TRS cable ═══════════●   "To Vocals 1"
```

**Naming convention:**
- "To Prod" = signal leaves Vocals, goes to Production (BOTTOM row at Vocals)
- "From Prod" = signal arrives from Production (TOP row at Vocals)
- "From Vocals" = signal arrives from Vocals (TOP row at Production)
- "To Vocals" = signal leaves Production, goes to Vocals (BOTTOM row at Production)

**How many?** 8 channels each direction:
- Golden Age MK3 EQ (mono) = 1 channel
- Lexicon MXL (dual stereo) = 4 channels
- 3 spare for future use

---

#### Two Ways to Use Outboard Gear

**INSERT** — gear goes directly in your signal chain
```
Use for: EQ, compression, saturation
Signal: 100% goes through the gear

BEFORE:  Source → Destination
AFTER:   Source → [GEAR] → Destination
```

**SEND/RETURN (AUX)** — gear runs parallel, you blend it in
```
Use for: Reverb, delay, time-based FX
Signal: Copy sent to gear, mixed back in

DRY:     Track → Mix (untouched)
WET:     Track → Aux Send → [GEAR set to 100% wet] → Aux Return → Mix
BLEND:   Dry + Wet together
```

---

### Real-World Examples Using Your Gear

---

#### EXAMPLE 1: INSERT — Golden Age EQ on Vocal Chain

*You're tracking vocals at the Vocals workstation. You want to add the Golden Age MK3 EQ (which lives at Production) into your chain.*

**Your chain BEFORE:**
```
Mojave mic → WA73 → FET Comp → Scarlett → Pro Tools
```

**Your chain AFTER (with Golden Age inserted):**
```
Mojave mic → WA73 → FET Comp → [crosses to Prod] → Golden Age EQ → [crosses back] → Scarlett → Pro Tools
```

**Patching (do this once, leave it):**

```
VOCALS PATCHBAY (front):
┌─────────────────────────────────────────────────────────────┐
│                                                             │
│  FET Comp output         ──────►  "To Prod 1"               │
│      (TOP row)                       (BOTTOM row)           │
│                                                             │
│  "From Prod 1"           ──────►  Scarlett input            │
│      (TOP row)                       (BOTTOM row)           │
│                                                             │
└─────────────────────────────────────────────────────────────┘

PRODUCTION PATCHBAY (front) — walk over, patch once, walk back:
┌─────────────────────────────────────────────────────────────┐
│                                                             │
│  "From Vocals 1"         ──────►  Golden Age EQ input       │
│      (TOP row)                       (BOTTOM row)           │
│                                                             │
│  Golden Age EQ output    ──────►  "To Vocals 1"             │
│      (TOP row)                       (BOTTOM row)           │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

---

#### EXAMPLE 2: SEND/RETURN — Lexicon Reverb on Pro Tools Mix

*You're mixing in Pro Tools at the Vocals workstation. You want the Lexicon MXL reverb (which lives at Production) as an aux effect.*

**How it works:**
```
Pro Tools track (dry)  ──────────────────────────────► Mix bus
                  │
                  └──► Aux Send → Scarlett out 7/8 → [crosses to Prod]
                                                            │
                                                            ▼
                                                     Lexicon MXL
                                                     (set to 100% wet)
                                                            │
                       Aux Return ◄── Scarlett in 7/8 ◄── [crosses back]
                             │
                             └──────────────────────────────► Mix bus
                                                        (blend wet + dry)
```

**Patching:**

```
VOCALS PATCHBAY (front):
┌─────────────────────────────────────────────────────────────┐
│                                                             │
│  Scarlett output 7       ──────►  "To Prod 2L"              │
│  Scarlett output 8       ──────►  "To Prod 2R"              │
│      (TOP row)                       (BOTTOM row)           │
│                                                             │
│  "From Prod 2L"          ──────►  Scarlett input 7          │
│  "From Prod 2R"          ──────►  Scarlett input 8          │
│      (TOP row)                       (BOTTOM row)           │
│                                                             │
└─────────────────────────────────────────────────────────────┘

PRODUCTION PATCHBAY (front):
┌─────────────────────────────────────────────────────────────┐
│                                                             │
│  "From Vocals 2L"        ──────►  Lexicon input L           │
│  "From Vocals 2R"        ──────►  Lexicon input R           │
│      (TOP row)                       (BOTTOM row)           │
│                                                             │
│  Lexicon output L        ──────►  "To Vocals 2L"            │
│  Lexicon output R        ──────►  "To Vocals 2R"            │
│      (TOP row)                       (BOTTOM row)           │
│                                                             │
└─────────────────────────────────────────────────────────────┘

IMPORTANT: Set Lexicon to 100% wet. You control dry/wet blend
           with the aux return fader in Pro Tools.
```

---

#### EXAMPLE 3: LOCAL — No Tie Lines Needed

*You're at the Production workstation. The Golden Age EQ is right there. No tie lines needed.*

```
PRODUCTION PATCHBAY (front) — simple:
┌─────────────────────────────────────────────────────────────┐
│                                                             │
│  MPC output              ──────►  Golden Age EQ input       │
│      (TOP row)                       (BOTTOM row)           │
│                                                             │
│  Golden Age EQ output    ──────►  Scarlett input            │
│      (TOP row)                       (BOTTOM row)           │
│                                                             │
└─────────────────────────────────────────────────────────────┘

If the gear is at your workstation, just patch locally.
Tie lines are only for accessing gear on the OTHER side.
```

---

### Tasks

**Both Workstations:**
- [ ] Set normalling to **HALF-NORMAL** for all standard I/O points
- [ ] Set normalling to **THRU** for cross-patch tie line points
- [ ] Set normalling to **THRU** for FX send/return points
- [ ] Verify **line-level only** (preamps stay outside patchbay)
- [ ] Label: **Top row = outputs, Bottom row = inputs**

**Cross-Patch Implementation:**
- [ ] Run 8x TRS cables: Vocals "To Prod" → Production "From Vocals"
- [ ] Run 8x TRS cables: Production "To Vocals" → Vocals "From Prod"
- [ ] Label points clearly: "To Prod 1", "From Prod 1", etc.
- [ ] Test: Vocals → Golden Age EQ → Vocals (round trip)
- [ ] Test: Vocals → Lexicon MXL → Vocals (round trip)

---

**Deliverable:**
Written signal-flow doc (1 page per workstation)

**Definition of Done:**
- Normalling configured (half-normal default, thru for tie lines/FX)
- Cross-patch cables run and tested
- Signal philosophy documented

---

## Issue #2: Patchbay layout implementation — Vocals Workstation

**Labels:** `phase-1`, `patchbay`, `hardware`, `vocals-workstation`

**Description:**
Physically implement the patchbay layout for the Vocals workstation.

**Top Row (Outputs):**
- [ ] Scarlett OctoPre outputs (8 channels)
- [ ] WA73 line out
- [ ] FET Compressor output
- [ ] Klark Teknik EQ output (if functional)
- [ ] Presonus Channel Strip output
- [ ] Cross-patch sends TO Production workstation

**Bottom Row (Inputs):**
- [ ] Scarlett OctoPre inputs
- [ ] FET Compressor input
- [ ] Klark Teknik EQ input
- [ ] Cross-patch returns FROM Production workstation (Golden Age EQ, Lexicon)

**Notes:**
- WA73 stays direct to Mojave mic (not normalled)
- Presonus channel strip: Shure mic → preamp → patchbay → Tascam
- Test Klark Teknik EQ functionality before final patching

**Definition of Done:**
All Vocals workstation gear patched. Can access Production workstation shared gear via cross-patch.

**Blocked by:** #1

---

## Issue #2b: Patchbay layout implementation — Production Workstation

**Labels:** `phase-1`, `patchbay`, `hardware`, `production-workstation`

**Description:**
Physically implement the patchbay layout for the Production workstation.

**Top Row (Outputs):**

*Instruments:*
- [ ] MPC XL main outs (L/R)
- [ ] MPC XL assignable outs
- [ ] Arturia Minifreak outs
- [ ] Yamaha DGX 670 outs
- [ ] MicroKorg outs
- [ ] Numark Mixstream Pro outs (pre-wired)

*Dynamics:*
- [ ] WA Bus Compressor output
- [ ] Pro VLA 2 output
- [ ] DBX 286s output

*EQ:*
- [ ] Ultragraph EQ output
- [ ] Golden Age MK3 EQ output

*FX:*
- [ ] Lexicon MXL outputs (stereo x2)

*Interfaces:*
- [ ] Scarlett OctoPre outputs
- [ ] Steinberg UR-RT4 outputs

*Cross-patch:*
- [ ] Cross-patch sends TO Vocals workstation

**Bottom Row (Inputs):**

*Dynamics:*
- [ ] WA Bus Compressor input
- [ ] Pro VLA 2 input
- [ ] DBX 286s input

*EQ:*
- [ ] Ultragraph EQ input
- [ ] Golden Age MK3 EQ input

*FX:*
- [ ] Lexicon MXL inputs (stereo x2)

*Interfaces:*
- [ ] Scarlett OctoPre inputs
- [ ] Steinberg UR-RT4 inputs

*Cross-patch:*
- [ ] Cross-patch returns FROM Vocals workstation

**Notes:**
- MPC outs should be easily routable to any processor
- Golden Age MK3 EQ and Lexicon MXL need dedicated cross-patch points for Vocals workstation access

**Instrument Workflow:**
- **DGX 670** = primary MIDI performance controller (88 weighted keys)
  - MIDI out → MPC for capturing performances
  - Audio out → MPC for sampling DGX sounds after performing
- **Minifreak** = sound design source
  - Design patches on Minifreak → sample audio back into MPC
  - Perform Minifreak sounds via DGX MIDI if needed
- **MicroKorg** = rarely used, no dedicated patchbay priority
- **Numark Mixstream Pro** = pre-wired for quick DJ/sampling sessions

**Other:**
- Steinberg UR-RT4 provides alternative recording path with Neve transformer color
- DBX 286s available as budget channel strip option

**Definition of Done:**
All Production workstation gear patched. Vocals workstation can access Golden Age EQ and Lexicon via cross-patch.

**Blocked by:** #1

---

## Issue #3: Patchbay labeling and documentation

**Labels:** `phase-1`, `patchbay`, `documentation`

**Description:**
Create physical and digital documentation for both patchbays.

**Tasks:**

### Vocals Workstation Patchbay
- [ ] Physical labels (front + rear)
- [ ] Digital diagram (photo + notes)

### Production Workstation Patchbay
- [ ] Physical labels (front + rear)
- [ ] Digital diagram (photo + notes)

### Color Coding (Both Stations)
- Red = dynamics (compressors, limiters)
- Blue = EQ
- Green = FX (Lexicon, etc.)
- Yellow = cross-patch (between workstations)
- White = interface I/O

### Cross-Patch Documentation
- [ ] Document which points on each patchbay connect to the other
- [ ] Label cross-patch cables distinctly

**Definition of Done:**
Someone else could patch either workstation without asking questions. Cross-patch routing is clearly documented.

**Blocked by:** #2, #2b

---

## Issue #3b: Test Klark Teknik EQ

**Labels:** `phase-1`, `hardware`, `testing`

**Description:**
Determine if the Klark Teknik EQ is functional before including it in the patchbay layout.

**Tasks:**
- [ ] Power on and check for signal pass-through
- [ ] Test each band
- [ ] Document status: working / partially working / dead

**Definition of Done:**
EQ status confirmed. If broken, decide: repair, replace, or remove from layout.

**No dependencies** — can be done anytime.
