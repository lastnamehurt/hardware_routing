# Patchbay Capacity Planning

## Your Patchbays

- **Vocals Workstation:** 48-point (24 top / 24 bottom)
- **Production Workstation:** Dual 48-point bays (PB-1 + PB-2 = 96 points total)

---

## VOCALS WORKSTATION — ✅ FITS

```
TOP ROW (outputs) — 24 available
┌────────────────────────────────────────────────────────────────┐
│ Scarlett OctoPre outs (8)                      ████████        │
│ WA73 line out (1)                              █               │
│ FET Compressor out (1)                         █               │
│ Klark Teknik EQ out (1)                        █               │
│ Presonus Channel Strip out (1)                 █               │
│ Tascam TA-1VP out (1)                          █               │
│ Tascam Mixcast 4 MONITOR OUT (2)               ██              │
│ "From Prod" tie lines (8)                      ████████        │
├────────────────────────────────────────────────────────────────┤
│ TOTAL: 23                                      ██████████████████████░░ │
│                                                USED         FREE(1)    │
└────────────────────────────────────────────────────────────────┘

BOTTOM ROW (inputs) — 24 available
┌────────────────────────────────────────────────────────────────┐
│ Scarlett OctoPre ins (8)                       ████████        │
│ FET Compressor in (1)                          █               │
│ Klark Teknik EQ in (1)                         █               │
│ Tascam TA-1VP in (1)                           █               │
│ Tascam Mixcast 4 Mic/Line 1 (half-normal from Presonus) █      │
│ Tascam Mixcast 4 Mic/Line 2 (set to LINE)      █               │
│ Tascam Mixcast 4 LINE IN (rear stereo pair)    ██              │
│ "To Prod" tie lines (8)                        ████████        │
├────────────────────────────────────────────────────────────────┤
│ TOTAL: 23                                      ███████████████████████░ │
│                                                USED         FREE(1)    │
└────────────────────────────────────────────────────────────────┘
```

**Tascam Mixcast 4 integration tips**
- Only one balanced stereo pair lives on the back of the Mixcast: the `MONITOR OUT L/R` jacks. Those now show up on the top row so you can route the control-room/program mix anywhere on the patchbay.
- The 1/8-inch `LINE OUT` jack stays local for cameras or handheld recorders (use the monitor outs for any patchbay routing).
- Mic/Line 1 now lands on the bottom row, half-normalled from the Presonus channel strip output. Default: Presonus → Mixcast. Patch the top/bottom to insert WA73/FET/Golden Age or reroute the vocal chain without breaking Zoom.
- Mic/Line 2 is available on the patchbay **only when you flip the front-panel switch to LINE**. Use a short TRS jumper from the patchbay into channel 2’s combo jack whenever you need to feed the Mixcast another balanced line signal.
- The rear `LINE IN R/L` pair is also exposed so you can bring DAW playback, MPC demos, or tie-line returns straight into the Mixcast auxiliary channel without crawling behind the desk.
- Headphone outs (four jacks) and the TRRS jack stay local at the desk because they’re unbalanced consumer-level feeds.
- TA-1VP Auto-Tune channel strip (1x in/out) now sits on the Vocals patchbay so you can drop it anywhere in the vocal chain with two quick patches.
- One bottom-row slot remains open if you later decide to expose Mic/Line 3-4 or the TRRS send/return.

**How the Mixcast connectors map to the patchbay**

| Mixcast jack (rear/front) | Patchbay row | Purpose |
|---------------------------|--------------|---------|
| MONITOR OUT L/R (¼″ TRS)  | Top (outputs)| Balanced mix send to Scarlett inputs, recorders, or Production tie lines |
| LINE OUT (⅛″ TRS stereo)  | —            | Local feed for DSLR/recorder; not on patchbay |
| LINE IN L/R (⅛″ TRS)      | Bottom (inputs)| Stereo return from Scarlett, MPC, or Production (use ⅛″↔¼″ cables/adapters) |
| Mic/Line 1                | Bottom (input, half-normalled)| Default: Presonus line out → Mixcast. Patch here to insert processors or send elsewhere.
| Mic/Line 2 (set to LINE)  | Bottom (input)| Optional auxiliary feed; patch a balanced line (Scarlett, MPC, tie line) into channel 2 when needed |
| Mic/Line 3-4 + TRRS + Phones | —        | Stay local, patch only if you add a second patchbay later |
| TA-1VP in/out             | Top+Bottom   | Mono insert for Auto-Tune/comp/EQ—patch anywhere in the chain |

**How to feed external mixes into the Tascam**
- **Using the rear LINE IN pair (recommended):** Patch any stereo source on the patchbay (Scarlett playback, MPC main outs via tie lines, DAW mix returns, etc.) into the Mixcast’s `LINE IN L/R` inputs. Those show up as the Mixcast stereo channel 5/6, so you can bring MPC or Production audio onto the Mixcast without touching the front panel.
- **Using Mic/Line 2 in LINE mode (optional mono):** If you need an additional mono feed (e.g., MPC click, cue mix), flip channel 2’s switch to LINE and patch its combo jack from the bay. This lets you monitor or record that signal independently from the stereo line-in.
- You can still plug something directly into Mic/Line 3-4 on the front of the Mixcast (e.g., a guest mic or phone) without consuming patch points; consider exposing them later when the second patchbay arrives.

**Vocals: 23 top, 23 bottom — FITS with room to spare ✅**

---

## PRODUCTION WORKSTATION — Dual Patchbay Layout

Second PX3000 is on the way, so Production becomes a 96-point system. The plan below keeps **Patchbay 1 (PB-1)** lean so you can wire it today (no tie lines, no rarely used gear). **Patchbay 2 (PB-2)** will hold the lower-priority gear plus all tie lines once it arrives. Everything is half-normalled unless noted.

#### PB-1 (install today) — Core instruments + MPC I/O

```
TOP ROW (outputs) — 24/24 used
│ MPC XL main L/R (2)                               │
│ MPC XL assignable outs 1-4 (4)                    │
│ Yamaha DGX 670 (2)                                │
│ Arturia Minifreak (2)                             │
│ WA Bus Compressor out (2)                         │
│ Pro VLA 2 out (2)                                 │
│ Golden Age MK3 EQ out (1)                         │
│ Lexicon MXL Engine A/B outs (4)                   │
│ Scarlett OctoPre line outs 1-5 (5)                │
```

```
BOTTOM ROW (inputs) — 24/24 used
│ WA Bus Compressor in (2)                          │
│ Pro VLA 2 in (2)                                  │
│ Golden Age MK3 EQ in (1)                          │
│ Lexicon MXL Engine A/B ins (4)                    │
│ Scarlett OctoPre line ins 1-8 (8)                 │
│ MPC sampling inputs L/R (2)                       │
│ MPC mix sends to Mixcast (2)                      │
│ Ableton cue return L/R (2)                        │
│ Pedal/DI capture inputs 1-3 (3)                   │
```

PB-1 now uses every jack with the always-on sources: MPC main + assignable outs, DGX, Minifreak, and all core processors stay here. Scarlett sends 1-5 cover the DAW playback/cue feeds; anything else (Scarlett outs 6-8, tie lines, lower-priority gear) lives on PB-2.

**Overflow pre plan**
- Scarlett OctoPre (all 8 pres) handle DGX, Minifreak, and utility feeds that half-normal into the MPC sampling inputs.
- If those channels are full, power the Steinberg UR-RT4 and patch its line outputs 1-2 (on PB-2 top row) into MPC or Scarlett/Mixcast inputs.
- If you still need another channel, patch the DBX 286s (PB-2) output into the MPC or Scarlett input.
#### PB-2 (after it arrives) — Tie lines + low-priority gear

```
TOP ROW (outputs) — 24/24 used
│ MicroKorg (2)                                     │
│ Numark Mixstream (2)                              │
│ Steinberg UR-RT4 outs 1-4 (4)                     │
│ DBX 286s out (1)                                  │
│ Ultragraph EQ out (2)                             │
│ Scarlett OctoPre line outs 6-8 (3)                │
│ Tie lines "From Vocals" 1-8 (8)                   │
│ Spare stereo pair (2)                             │

BOTTOM ROW (inputs) — 24/24 used
│ Steinberg UR-RT4 ins 1-4 (4)                      │
│ DBX 286s in (1)                                   │
│ Ultragraph EQ in (2)                              │
│ Numark return (2)                                 │
│ Tie lines "To Vocals" 1-8 (8)                     │
│ Reamp/pedal inserts 1-7 (7)                       │
```

PB-2 carries every tie line plus the rarely used gear (MicroKorg, Numark, Steinberg, DBX 286s, Ultragraph). Once it is wired you can patch from PB-1 into PB-2 when you actually need those pieces.

**Signal flow tips**
- Instruments → PB-1 top → half-normal to Scarlett inputs or MPC. Jack in on PB-1 to insert compressors/EQs before they hit the interfaces.
- DAW playback → UR-RT4 outs (PB-2 top) → processors or tie lines → PB-1 bottom (Scarlett ins) → Vocals or external recorders.
- Lexicon engines and tie-line points stay thru-normal so you patch send/returns manually.
- UR-RT4 doubles as an overflow preamp: its outs on PB-2 feed MPC/Scarlett/Mixcast when the OctoPre is full; DBX 286s on PB-2 is the final backup channel strip.

#### Implementation checklist (turn into GitHub issues)

1. **Wire PB-1 (core routing)** — land every jack listed above, set normals, confirm MPC/DGX → Scarlett paths and processor inserts.
2. **Label + photo PB-1** — print strip labels, capture pictures for the repo, update diagrams.
3. **Prepare PB-2 harness** — pre-cut cables and label for MicroKorg/Numark/Steinberg/DBX/Ultragraph/tie lines so installation is plug-and-play when the bay arrives.
4. **Install PB-2 + tie lines** — mount the second PX3000, wire all tie lines + low-use gear, verify round trips to Vocals.
5. **Final documentation + testing** — update `phase-1` doc, patchbay diagrams, and run end-to-end tests (MPC → PB-2 processor → PB-1 → DAW, Vocals ↔ Production tie line loopback).

---

## RECOMMENDATION

The second patchbay is already in flight, so move forward with the PB-A/PB-B layout above. Treat the checklist as five GitHub issues under a single “Production Dual Patchbays” epic so you can track mounting, wiring, tie lines, and documentation separately.
