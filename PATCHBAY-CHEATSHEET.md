# PATCHBAY CHEAT SHEET

## PHILOSOPHY
| Patchbay | Purpose | No cables = |
|----------|---------|-------------|
| **PB1** | Core (NORMALLED) | Synths → MPC works |
| **PB2** | Creative (THRU) | Nothing connected |

**If PB2 is unplugged, studio still works.**

---

## DEFAULT SIGNAL FLOW (No Cables Needed)
```
MiniFreak ──┐
            ├──► OctoPre Dynamic ──► MPC IN 1-4
DGX 670 ────┘       (seatbelt)

MPC OUT 3-6 ──► OctoPre Regular ──► (ready for stems)
```

---

## PB1 — CORE (Half-Normal)

| TOP (Outputs) | BOTTOM (Inputs) |
|---------------|-----------------|
| 1-2: MFREAK L/R | 1-2: OCTO-D IN 1-2 ← MFREAK |
| 3-4: DGX L/R | 3-4: OCTO-D IN 3-4 ← DGX |
| 5-8: OCTO-D OUT 1-4 | 5-8: MPC IN 1-4 ← OCTO-D |
| 9-14: MPC OUT 1-6 | 9-10: THRU |
| 15-18: OCTO OUT 3-6 | 11-14: OCTO IN 3-6 ← MPC OUT 3-6 |

---

## PB2 — CREATIVE (All THRU)

| TOP (Outputs) | BOTTOM (Inputs) |
|---------------|-----------------|
| 1-2: MPC OUT 7-8 | 1-2: — |
| 3-4: VLA OUT L/R | 3-4: VLA IN L/R |
| 5-6: VCA OUT L/R | 5-6: VCA IN L/R |
| 7: GA EQ OUT | 7: GA EQ IN |
| 8-9: ULTRA OUT L/R | 8-9: ULTRA IN L/R |
| 10-13: LEX A/B OUT | 10-13: LEX A/B IN |
| 14-15: NUMARK L/R | 14-15: NUMARK RTN L/R |
| 16-17: UR OUT 1-2 | 16-17: UR IN 1-2 |
| — | 18-19: OCTO-D IN 7-8 (returns) |

---

## COMMON PATCHES

### Add Reverb
```
MPC OUT 3-4 ──► LEX A IN ──► LEX A OUT ──► OCTO-D IN 7-8 ──► MPC
```

### Add Delay
```
MPC OUT 5-6 ──► LEX B IN ──► LEX B OUT ──► OCTO-D IN 7-8 ──► MPC
```

### Warm Up Mix (VLA)
```
MPC OUT 1-2 ──► VLA IN ──► VLA OUT ──► Headphones/Record
```

### Glue Mix (VCA)
```
MPC OUT 1-2 ──► VCA IN ──► VCA OUT ──► Headphones/Record
```

### Crush Drums (Parallel)
```
MPC OUT 7-8 ──► VLA IN ──► VLA OUT ──► MPC IN (blend)
```

### Full Lexicon (Both Engines)
```
OUT 3-4 ──► LEX A (reverb)    Returns via
OUT 5-6 ──► LEX B (delay)     OCTO-D IN 7-8
```

---

## VOCALS CHAIN (Default)
```
Mojave ──► WA73 ──► FET ──► Auto-Tune ──► Klark ──► 18i20 LINE 1
```

---

## MPC OUTPUTS

| Output | Default | Alt (patch to break) |
|--------|---------|----------------------|
| 1-2 | Main (headphones) | Master processing |
| 3-4 | Stems → OCTO | Lexicon A |
| 5-6 | Stems → OCTO | Lexicon B |
| 7-8 | FX sends | Parallel compression |

**Headphone monitoring frees ALL 8 outputs for processing.**

---

## QUICK SETTINGS

| Gear | Use For | Settings |
|------|---------|----------|
| **VLA** | Warmth, glue | Slow attack, 2-4 dB GR |
| **VCA** | Punch, control | Fast attack, 1-2 dB GR |
| **LEX A** | Reverb | Plate, 1.5-2.5s decay |
| **LEX B** | Delay | Tempo sync, 30-50% feedback |
| **OCTO-D** | Input seatbelt | 2-3 dB GR (light) |

---

## TIE LINES (4 each direction)
```
Production ←──► Vocals
TO PROD 1-4     FROM PROD 1-4
```
