# Hardware Routing Epics

Use these as the source of truth for GitHub issues / project tickets.

---

## Epic 1 — PB-1 Wiring & Verification
**Goal:** Finish wiring the first production patchbay so MPC, DGX, Minifreak, and core processors are ready without tie lines.

- [ ] Mount PB-1 and set all normals (half-normal default, thru for FX sends)
- [ ] Land MPC main + sub outs, DGX, Minifreak, WA Bus, Pro VLA, Golden Age, Lexicon A/B
- [ ] Land Scarlett IN/OUT 1-5, MPC sampling inputs, Mixcast send, Ableton cue return
- [ ] Smoke-test every default path (MPC→Scarlett, DGX→MPC, Lexicon loop, etc.)
- [ ] Capture photos + final jack map for documentation

---

## Epic 2 — PB-2 Expansion & Tie Lines
**Goal:** Install the second PX3000 and bring all low-use gear plus the full 8× tie-line matrix online.

- [ ] Pre-cut and label cables for MicroKorg, Mixstream, UR-RT4, DBX 286s, Ultragraph, Scarlett outs 6-8
- [ ] Mount PB-2, set normals (half-normal for processors, thru for tie lines/FX returns)
- [ ] Wire From/To Vocals tie lines 1-8 (both bays) and run loopback tests
- [ ] Verify UR-RT4 overflow pres + DBX channel strip routing through PB-2 into MPC/Scarlett
- [ ] Update diagrams + README once PB-2 is live

---

## Epic 3 — Cable Labeling + Front-Panel Strips
**Goal:** Print/install all labels so anyone can patch without second-guessing. Share this checklist with coworkers.

- [ ] Print Vocals labels (`SC OUT 1-8`, `SC IN 1-8`, `WA73 OUT`, `Mixcast MON L/R`, etc.)
- [ ] Print PB-1 labels (`MPC MAIN L/R`, `MPC SUB1-4`, `WA BUS OUT/IN`, `LEX A/B OUT/IN`, `SC IN 1-8`, `MPC→MC L/R`, `CUE L/R`)
- [ ] Print PB-2 + tie-line labels (`MKORG L/R`, `NUMARK L/R`, `UR OUT/IN 1-4`, `DBX OUT/IN`, `ULTRA OUT/IN L/R`, `SC OUT 6-8`, `FROM/TO VOC 1-8`)
- [ ] Apply wrap labels + heatshrink on both cable ends
- [ ] Install front strip labels on both bays and take reference photos
