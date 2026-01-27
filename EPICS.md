# Studio Setup - Epics & Tickets

---

## Epic 0: The Desk (Daily Driver)
**Goal:** Tascam Mixcast Pro 4 integration for Zoom/meetings

### Ticket #15: Tascam Mixcast Pro 4 Integration
**Labels:** `phase-0`, `the-desk`, `tascam`, `critical`
**Blocked by:** #2

**Tasks:**
- [ ] Run XLR from Shure mic (desk) to Presonus channel strip (rack)
- [ ] Land Presonus line output on Vocals patchbay top row
- [ ] Land Mixcast Mic/Line 1 on bottom row, half-normalled from Presonus Out
- [ ] Set gain staging: Presonus → Mixcast
- [ ] Test with Zoom call
- [ ] Test MPC XL → Tascam via patchbay
- [ ] Test MPC XL → Tascam simple connection (headphone → ext cord)
- [ ] Document signal path for daily Zoom/meeting use

**Done when:** Daily Zoom workflow works without touching the rack

---

## Epic 1: Patchbay Foundation
**Goal:** Make MPC, outboard gear, and DAWs interchangeable without re-patching

### Ticket #1: Finalize Patchbay Signal Philosophy
**Labels:** `phase-1`, `patchbay`, `planning`

**Decisions:**
| Decision | Choice |
|----------|--------|
| Creative brain | MPC XL |
| Routing brain | Patchbays |
| Signal level | Line-level only |
| Layout | Top = outputs, Bottom = inputs |
| Normalling | Half-normal (thru for tie lines/FX) |

**Tasks:**
- [ ] Set normalling to HALF-NORMAL for all standard I/O
- [ ] Set normalling to THRU for tie lines and FX send/return
- [ ] Document signal philosophy (1 page per workstation)

**Done when:** Normalling configured, philosophy documented

---

### Ticket #2: Vocals Workstation Patchbay Layout
**Labels:** `phase-1`, `patchbay`, `hardware`, `vocals-workstation`
**Blocked by:** #1

**Top Row (Outputs):**
- [ ] Scarlett OctoPre outputs 1-8
- [ ] WA73 line out
- [ ] FET Compressor output
- [ ] Klark Teknik EQ output (if functional)
- [ ] Presonus Channel Strip output
- [ ] Cross-patch sends TO Production

**Bottom Row (Inputs):**
- [ ] Scarlett OctoPre inputs 1-8
- [ ] FET Compressor input
- [ ] Klark Teknik EQ input
- [ ] Cross-patch returns FROM Production

**Done when:** All Vocals gear patched, can access Production shared gear

---

### Ticket #2b: Production Workstation Patchbay Layout
**Labels:** `phase-1`, `patchbay`, `hardware`, `production-workstation`
**Blocked by:** #1

**Top Row (Outputs):**

*Instruments:*
- [ ] MPC XL main outs L/R
- [ ] MPC XL assignable outs 1-4
- [ ] Arturia Minifreak L/R
- [ ] Yamaha DGX 670 L/R
- [ ] MicroKorg L/R
- [ ] Numark Mixstream Pro L/R

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
- [ ] Cross-patch sends TO Vocals

**Bottom Row (Inputs):**
- [ ] All corresponding processor/FX inputs
- [ ] Scarlett/UR-RT4 inputs
- [ ] MPC sampling inputs
- [ ] Cross-patch returns FROM Vocals

**Done when:** All Production gear patched, Vocals can access Golden Age EQ and Lexicon

---

### Ticket #3: Cross-Patch Tie Lines
**Labels:** `phase-1`, `patchbay`, `hardware`
**Blocked by:** #2, #2b

**Tasks:**
- [ ] Run 8x TRS cables: Vocals "To Prod" → Production "From Vocals"
- [ ] Run 8x TRS cables: Production "To Vocals" → Vocals "From Prod"
- [ ] Test: Vocals → Golden Age EQ → Vocals (round trip)
- [ ] Test: Vocals → Lexicon MXL → Vocals (round trip)

**Done when:** Both workstations can access each other's gear via tie lines

---

### Ticket #3b: Test Klark Teknik EQ
**Labels:** `phase-1`, `hardware`, `testing`
**No dependencies**

- [ ] Power on and check signal pass-through
- [ ] Test each band
- [ ] Document status: working / partially working / dead

**Done when:** Status confirmed. If broken → decide repair/replace/remove

---

## Epic 2: MPC Creative Center
**Goal:** MPC works standalone AND feeds DAWs cleanly

### Ticket #4: MPC Internal Template
**Labels:** `phase-2`, `mpc`, `template`

**MIDI Config:**
- [ ] MIDI track for DGX 670 input
- [ ] MIDI track for Minifreak control
- [ ] Enable MIDI Clock + MMC
- [ ] Set DGX as primary MIDI input

**Audio Tracks (Pre-Named):**
- [ ] "DGX Sample"
- [ ] "Minifreak Sample"
- [ ] "Drums"
- [ ] "Bass"
- [ ] "Keys"
- [ ] "FX / Atmos"

**Defaults:**
- [ ] Set default BPM
- [ ] Set default swing
- [ ] Input monitoring for quick sampling

**Done when:** New project → ready to perform in <30 seconds

---

### Ticket #5: MPC Patchbay Verification
**Labels:** `phase-2`, `mpc`, `patchbay`, `testing`
**Blocked by:** #2b

**Output Tests (MPC → Processing → MPC/DAW):**
- [ ] MPC → WA Bus Compressor → MPC
- [ ] MPC → Pro VLA 2 → MPC
- [ ] MPC → Golden Age MK3 EQ → MPC
- [ ] MPC → Lexicon MXL → MPC

**Input Tests (Instruments → MPC Sampling):**
- [ ] DGX 670 audio → patchbay → MPC input
- [ ] Minifreak audio → patchbay → MPC input
- [ ] DGX 670 → processing → MPC input
- [ ] Minifreak → processing → MPC input

**MIDI Tests:**
- [ ] DGX 670 MIDI → MPC (latency check)
- [ ] MPC MIDI → Minifreak

**Done when:** Processing chains work, sampling is immediate, MIDI latency acceptable

---

## Epic 3: MPC → Ableton Integration
**Goal:** Ableton used only where it adds value

### Ticket #6: Ableton Live Setup
**Labels:** `phase-3`, `ableton`, `setup`

- [ ] Install Ableton Live Lite on Mac Studio
- [ ] Verify hardware license unlock
- [ ] Enable Ableton Link

**Done when:** Live opens, syncs, can record MPC audio/MIDI

---

### Ticket #7: MPC to Ableton Sync & Routing
**Labels:** `phase-3`, `mpc`, `ableton`, `routing`
**Blocked by:** #6

- [ ] Decide clock master (usually Ableton)
- [ ] Route MPC audio → Ableton tracks
- [ ] Route MPC MIDI → Ableton instruments (optional)
- [ ] Test transport control
- [ ] Test loop recording
- [ ] Test tempo changes

**Done when:** Can jam on MPC and capture ideas without stopping

---

### Ticket #8: iPad Control Layer
**Labels:** `phase-3`, `ableton`, `ipad`, `control`
**Blocked by:** #6

- [ ] Install Ableton Note
- [ ] Configure Sidecar for touch screen Live view
- [ ] Map controls: Play/Stop/Record, Clip launch, Track arm

**Done when:** iPad replaces mouse during creative phase

---

## Epic 4: Ableton → Pro Tools Handoff
**Goal:** Zero friction moving from ideas to records

### Ticket #9: Define Commit Strategy
**Labels:** `phase-4`, `ableton`, `pro-tools`, `planning`

- [ ] Document: When to bounce (drums as stems? MIDI vs audio?)
- [ ] Naming conventions
- [ ] Sample rate / bit depth alignment

**Deliverable:** Written rule document: "If X, commit to audio"

---

### Ticket #10: Ableton to Pro Tools Handoff Workflow
**Labels:** `phase-4`, `ableton`, `pro-tools`, `workflow`
**Blocked by:** #9

- [ ] Export from Ableton: Consolidated stems + tempo map
- [ ] Import into Pro Tools
- [ ] Verify alignment

**Done when:** Pro Tools session opens perfectly aligned on bar 1

---

### Ticket #11: Pro Tools Tracking & Mix Template
**Labels:** `phase-4`, `pro-tools`, `template`

- [ ] Create PT template: Vocal chains, instrument busses, FX returns
- [ ] Document patchbay recall for vocal chain

**Done when:** Can record vocals immediately after importing stems

---

## Epic 5: Studio Operations
**Goal:** Prevent future pain with proper systems

### Ticket #12: Backup & Versioning System
**Labels:** `phase-5`, `operations`, `backup`

- [ ] MPC projects backup strategy
- [ ] Ableton sets backup strategy
- [ ] Pro Tools sessions backup strategy
- [ ] Automate where possible

**Done when:** All project types have documented, working backup procedures

---

### Ticket #13: Gain Staging Reference
**Labels:** `phase-5`, `operations`, `documentation`

- [ ] MPC output level target
- [ ] Interface input target
- [ ] DAW headroom target

**Deliverable:** One-page reference for consistent levels across all gear

---

### Ticket #14: Standalone vs DAW Decision Checklist
**Labels:** `phase-5`, `operations`, `documentation`

**Mental Model:**
- MPC = ideas, groove, feel
- Ableton = exploration, arrangement, performance
- Pro Tools = commitment, vocals, polish

**Deliverable:** Laminated/printed reference at the desk

---

## Wire Labeling Checklist (Hand off to helper)

Print wraparound/heatshrink labels. ALL CAPS. Label both ends of each cable.

### Vocals Workstation Wires

- [ ] SC OUT 1
- [ ] SC OUT 2
- [ ] SC OUT 3
- [ ] SC OUT 4
- [ ] SC OUT 5
- [ ] SC OUT 6
- [ ] SC OUT 7
- [ ] SC OUT 8
- [ ] WA73 OUT
- [ ] FET OUT
- [ ] KLARK OUT
- [ ] PRESONUS OUT
- [ ] TA1VP OUT
- [ ] MIXCAST MON L
- [ ] MIXCAST MON R
- [ ] SC IN 1
- [ ] SC IN 2
- [ ] SC IN 3
- [ ] SC IN 4
- [ ] SC IN 5
- [ ] SC IN 6
- [ ] SC IN 7
- [ ] SC IN 8
- [ ] FET IN
- [ ] KLARK IN
- [ ] TA1VP IN
- [ ] MIXCAST CH1
- [ ] MIXCAST CH2
- [ ] MIXCAST LINE L
- [ ] MIXCAST LINE R

### Production PB-1 Wires (Core Gear)

- [ ] MPC MAIN L
- [ ] MPC MAIN R
- [ ] MPC SUB1
- [ ] MPC SUB2
- [ ] MPC SUB3
- [ ] MPC SUB4
- [ ] DGX L
- [ ] DGX R
- [ ] MFREAK L
- [ ] MFREAK R
- [ ] WA BUS OUT L
- [ ] WA BUS OUT R
- [ ] VLA OUT L
- [ ] VLA OUT R
- [ ] GA EQ OUT
- [ ] LEX A OUT L
- [ ] LEX A OUT R
- [ ] LEX B OUT L
- [ ] LEX B OUT R
- [ ] SC OUT 1
- [ ] SC OUT 2
- [ ] SC OUT 3
- [ ] SC OUT 4
- [ ] SC OUT 5
- [ ] WA BUS IN L
- [ ] WA BUS IN R
- [ ] VLA IN L
- [ ] VLA IN R
- [ ] GA EQ IN
- [ ] LEX A IN L
- [ ] LEX A IN R
- [ ] LEX B IN L
- [ ] LEX B IN R
- [ ] SC IN 1
- [ ] SC IN 2
- [ ] SC IN 3
- [ ] SC IN 4
- [ ] SC IN 5
- [ ] SC IN 6
- [ ] SC IN 7
- [ ] SC IN 8
- [ ] MPC IN L
- [ ] MPC IN R
- [ ] MPC→MC L
- [ ] MPC→MC R
- [ ] CUE L
- [ ] CUE R

### Production PB-2 Wires (Low-Use + Tie Lines)

- [ ] MKORG L
- [ ] MKORG R
- [ ] NUMARK L
- [ ] NUMARK R
- [ ] UR OUT 1
- [ ] UR OUT 2
- [ ] UR OUT 3
- [ ] UR OUT 4
- [ ] DBX OUT
- [ ] ULTRA OUT L
- [ ] ULTRA OUT R
- [ ] SC OUT 6
- [ ] SC OUT 7
- [ ] SC OUT 8
- [ ] FROM VOC 1
- [ ] FROM VOC 2
- [ ] FROM VOC 3
- [ ] FROM VOC 4
- [ ] FROM VOC 5
- [ ] FROM VOC 6
- [ ] FROM VOC 7
- [ ] FROM VOC 8
- [ ] UR IN 1
- [ ] UR IN 2
- [ ] UR IN 3
- [ ] UR IN 4
- [ ] DBX IN
- [ ] ULTRA IN L
- [ ] ULTRA IN R
- [ ] NUMARK RTN L
- [ ] NUMARK RTN R
- [ ] TO VOC 1
- [ ] TO VOC 2
- [ ] TO VOC 3
- [ ] TO VOC 4
- [ ] TO VOC 5
- [ ] TO VOC 6
- [ ] TO VOC 7
- [ ] TO VOC 8

### Tie-Line Cable Ends

- [ ] V→P 1
- [ ] V→P 2
- [ ] V→P 3
- [ ] V→P 4
- [ ] V→P 5
- [ ] V→P 6
- [ ] V→P 7
- [ ] V→P 8
- [ ] P→V 1
- [ ] P→V 2
- [ ] P→V 3
- [ ] P→V 4
- [ ] P→V 5
- [ ] P→V 6
- [ ] P→V 7
- [ ] P→V 8

---

## Critical Path

**Priority 1 (daily workflow):** #1 → #2 → #15 (Tascam/Zoom setup)
**Priority 2 (creative foundation):** #2b → #4 → #5 (MPC + patchbay)
**Priority 3 (DAW integration):** #6 → #7 → #9 → #10 (Ableton + Pro Tools)
