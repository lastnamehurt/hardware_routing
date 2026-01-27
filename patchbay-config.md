# Patchbay Configuration

## Philosophy

| Patchbay | Purpose | Normalling |
|----------|---------|------------|
| **Patchbay 1** | Core / Default signal flow | NORMALLED |
| **Patchbay 2** | Creative / Processing / FX | ALL THRU |

> **Patchbay 1 = "things I never want to think about."**
> **Patchbay 2 = "things I want to choose."**

If Patchbay 2 is unplugged, your studio still works.

---

# PATCHBAY 1 — CORE (Production Workstation)

## Signal Flow

```
MiniFreak ──┐
            ├──► OctoPre Dynamic ──► MPC XL
DGX 670 ────┘         (seatbelt)
```

Zero patch cables to make music.

---

## Jack Layout

### Top Row (OUTPUTS)

| Jack | Label | Source |
|------|-------|--------|
| 1 | MFREAK L | Minifreak Left Out |
| 2 | MFREAK R | Minifreak Right Out |
| 3 | DGX L | Yamaha DGX 670 Left Out |
| 4 | DGX R | Yamaha DGX 670 Right Out |
| 5 | OCTO-D OUT 1 | OctoPre Dynamic Line Out 1 |
| 6 | OCTO-D OUT 2 | OctoPre Dynamic Line Out 2 |
| 7 | OCTO-D OUT 3 | OctoPre Dynamic Line Out 3 |
| 8 | OCTO-D OUT 4 | OctoPre Dynamic Line Out 4 |
| 9 | MPC OUT 1 | MPC XL Out 1 (Main L) |
| 10 | MPC OUT 2 | MPC XL Out 2 (Main R) |
| 11 | MPC OUT 3 | MPC XL Out 3 (Assignable) |
| 12 | MPC OUT 4 | MPC XL Out 4 (Assignable) |
| 13 | MPC OUT 5 | MPC XL Out 5 (Assignable) |
| 14 | MPC OUT 6 | MPC XL Out 6 (Assignable) |
| 15 | OCTO OUT 3 | OctoPre (regular) Line Out 3 |
| 16 | OCTO OUT 4 | OctoPre (regular) Line Out 4 |
| 17 | OCTO OUT 5 | OctoPre (regular) Line Out 5 |
| 18 | OCTO OUT 6 | OctoPre (regular) Line Out 6 |

### Bottom Row (INPUTS)

| Jack | Label | Destination | Normalled From |
|------|-------|-------------|----------------|
| 1 | OCTO-D IN 1 | OctoPre Dynamic Input 1 | MFREAK L |
| 2 | OCTO-D IN 2 | OctoPre Dynamic Input 2 | MFREAK R |
| 3 | OCTO-D IN 3 | OctoPre Dynamic Input 3 | DGX L |
| 4 | OCTO-D IN 4 | OctoPre Dynamic Input 4 | DGX R |
| 5 | MPC IN 1 | MPC XL Input 1 | OCTO-D OUT 1 |
| 6 | MPC IN 2 | MPC XL Input 2 | OCTO-D OUT 2 |
| 7 | MPC IN 3 | MPC XL Input 3 | OCTO-D OUT 3 |
| 8 | MPC IN 4 | MPC XL Input 4 | OCTO-D OUT 4 |
| 9 | — | (MPC OUT 1/2 = Main, not normalled) | THRU |
| 10 | — | (MPC OUT 1/2 = Main, not normalled) | THRU |
| 11 | OCTO IN 3 | OctoPre (regular) Input 3 (back) | MPC OUT 3 |
| 12 | OCTO IN 4 | OctoPre (regular) Input 4 (back) | MPC OUT 4 |
| 13 | OCTO IN 5 | OctoPre (regular) Input 5 (back) | MPC OUT 5 |
| 14 | OCTO IN 6 | OctoPre (regular) Input 6 (back) | MPC OUT 6 |
| 15 | — | (OCTO OUT not normalled) | THRU |
| 16 | — | (OCTO OUT not normalled) | THRU |
| 17 | — | (OCTO OUT not normalled) | THRU |
| 18 | — | (OCTO OUT not normalled) | THRU |

---

## Normalling Summary (Patchbay 1)

| Connection | Type |
|------------|------|
| Minifreak → OctoPre Dynamic IN 1-2 | HALF-NORMAL |
| DGX → OctoPre Dynamic IN 3-4 | HALF-NORMAL |
| OctoPre Dynamic OUT → MPC IN 1-4 | HALF-NORMAL |
| MPC OUT 3-6 → OctoPre (regular) IN 3-6 (back) | HALF-NORMAL |
| MPC OUT 1-2 (Main) | THRU (not normalled - goes to monitors) |
| OctoPre (regular) OUT 3-6 | THRU (patch to tie lines or UR-RT4) |

## Front Panel Access (OctoPre Regular)

Inputs 1-2 are on the **front panel** - leave them free for quick mic/instrument patching.

| Input | Location | Use |
|-------|----------|-----|
| 1-2 | FRONT | Mic, quick sampling, turntable |
| 3-6 | BACK | MPC OUT 1-4 (permanent) |
| 7-8 | BACK | Spare / returns |

## MPC Output Layout

| Output | Default Use | Alt Use (patch to break normal) |
|--------|-------------|--------------------------------|
| OUT 1-2 | Main (headphones) | **Mixing/tracking** - monitors via headphone jack + splitter |
| OUT 3-6 | Stems → OctoPre Regular | **FX sends** → Lexicon, compressors, etc. |
| OUT 7-8 | FX sends | More FX / parallel processing |

### Flexibility = 8 Outputs for Anything

Since you use **headphones** (not monitors), OUT 1-2 are freed up for processing.

When you're NOT recording stems, OUT 3-6 become FX sends.

**Total available for FX/processing:** 8 outputs (all of them)

```
Headphone monitoring:
MPC headphone jack → splitter → headphones + backup speakers

All 8 outputs free for:
├── OUT 1-2 → Master bus processing (VCA, etc.)
├── OUT 3-4 → Lexicon Engine A (stereo)
├── OUT 5-6 → Lexicon Engine B (stereo)
└── OUT 7-8 → Parallel compression (VLA)
```

## MPC Stem Recording Flow

```
MPC OUT 3-6 (stems: drums, bass, keys, etc.)
    ↓ normalled
OctoPre (regular) IN 3-6 (back panel)
    ↓
OctoPre (regular) OUT 3-6
    ↓ patch cable
Tie Lines → 18i20 → DAW
    OR
UR-RT4 (for Neve color) → DAW
```

- MPC OUT 1-2 (Main) = headphones via MPC headphone jack
- OctoPre Regular front panel (IN 1-2) = free for mic/quick sampling

---

# HALF-NORMAL FLEXIBILITY

The magic of half-normal: **patch cable breaks the default, gives you full control.**

## Scenario 1: Beat Making (Default)
No patch cables needed.
```
Synths → OctoPre Dynamic → MPC (normalled)
```

## Scenario 2: Recording Stems to DAW
```
MPC OUT 3-6 → OctoPre Regular → Tie Lines → 18i20 → DAW (normalled)
```

## Scenario 3: Full Lexicon (Both Engines)
Patch to break stem chain:
```
MPC OUT 3-4 → Lexicon A IN (patch cable breaks normal)
MPC OUT 5-6 → Lexicon B IN (patch cable breaks normal)
Lexicon A/B OUT → Return (OCTO-D IN 7-8 or MPC IN)
```

## Scenario 4: Everything at Once (Max Processing)
Since you monitor via headphones:
```
MPC headphone jack → splitter → headphones

OUT 1-2 → VCA Bus (master compression)
OUT 3-4 → Lexicon A (reverb)
OUT 5-6 → Lexicon B (delay)
OUT 7-8 → VLA (parallel compression)
```

**8 outputs = 4 stereo sends = full outboard access**

---

# PATCHBAY 2 — CREATIVE (Production Workstation)

## Purpose

All THRU. Nothing is connected by default. You patch what you want, when you want.

---

## Jack Layout

### Top Row (OUTPUTS)

| Jack | Label | Source |
|------|-------|--------|
| 1 | MPC OUT 7 | MPC XL Out 7 (FX send) |
| 2 | MPC OUT 8 | MPC XL Out 8 (FX send) |
| 3 | VLA OUT L | Pro VLA2 Output Left |
| 4 | VLA OUT R | Pro VLA2 Output Right |
| 5 | VCA OUT L | WA VCA Bus Output Left |
| 6 | VCA OUT R | WA VCA Bus Output Right |
| 7 | GA EQ OUT | Golden Age EQ Output |
| 8 | ULTRA OUT L | Ultragraph EQ Output Left |
| 9 | ULTRA OUT R | Ultragraph EQ Output Right |
| 10 | LEX A OUT L | Lexicon Engine A Output Left |
| 11 | LEX A OUT R | Lexicon Engine A Output Right |
| 12 | LEX B OUT L | Lexicon Engine B Output Left |
| 13 | LEX B OUT R | Lexicon Engine B Output Right |
| 14 | NUMARK L | Numark DJ Output Left |
| 15 | NUMARK R | Numark DJ Output Right |
| 16 | UR OUT 1 | Steinberg UR-RT4 Output 1 |
| 17 | UR OUT 2 | Steinberg UR-RT4 Output 2 |

### Bottom Row (INPUTS)

| Jack | Label | Destination |
|------|-------|-------------|
| 1 | — | (MPC OUT 7-8 are sends, no return here) |
| 2 | — | |
| 3 | VLA IN L | Pro VLA2 Input Left |
| 4 | VLA IN R | Pro VLA2 Input Right |
| 5 | VCA IN L | WA VCA Bus Input Left |
| 6 | VCA IN R | WA VCA Bus Input Right |
| 7 | GA EQ IN | Golden Age EQ Input |
| 8 | ULTRA IN L | Ultragraph EQ Input Left |
| 9 | ULTRA IN R | Ultragraph EQ Input Right |
| 10 | LEX A IN L | Lexicon Engine A Input Left |
| 11 | LEX A IN R | Lexicon Engine A Input Right |
| 12 | LEX B IN L | Lexicon Engine B Input Left |
| 13 | LEX B IN R | Lexicon Engine B Input Right |
| 14 | NUMARK RTN L | Numark DJ Return Left |
| 15 | NUMARK RTN R | Numark DJ Return Right |
| 16 | UR IN 1 | Steinberg UR-RT4 Input 1 |
| 17 | UR IN 2 | Steinberg UR-RT4 Input 2 |

### Returns (OctoPre Dynamic back panel 7-8)

| Jack | Label | Destination |
|------|-------|-------------|
| 18 | OCTO-D IN 7 | OctoPre Dynamic Input 7 (return) |
| 19 | OCTO-D IN 8 | OctoPre Dynamic Input 8 (return) |

---

## Normalling Summary (Patchbay 2)

**ALL THRU — NO NORMALS**

Nothing is connected by default.

---

# VOCALS RACK PATCHBAY

## Signal Chain

```
Mojave Mic (mic level)
    ↓
WA73 Preamp (boosts to line level + Neve tone)
    ↓
FET Compressor (dynamics control)
    ↓
Antares Auto-Tune (pitch correction - optional)
    ↓
Klark Teknik EQ (tone shaping - if working)
    ↓
18i20 LINE INPUT (A/D conversion only)
    ↓
Mac Studio
```

**Key:** WA73 → processing chain → 18i20 **line input**. Bypass 18i20's preamps.

---

## Jack Layout

### Top Row (OUTPUTS)

| Jack | Label | Source |
|------|-------|--------|
| 1 | WA73 OUT | WA73 Preamp Output |
| 2 | FET OUT | FET Compressor Output |
| 3 | AUTOTUNE OUT | Antares Auto-Tune Output |
| 4 | KLARK OUT | Klark Teknik EQ Output (if working) |
| 5 | PRESONUS OUT | Presonus Channel Strip Output |
| 6 | 18i20 OUT 1 | DAW Send 1 |
| 7 | 18i20 OUT 2 | DAW Send 2 |
| 8 | 18i20 OUT 3 | DAW Send 3 |
| 9 | 18i20 OUT 4 | DAW Send 4 |
| 10 | TO PROD 1 | Tie Line to Production |
| 11 | TO PROD 2 | Tie Line to Production |
| 12 | TO PROD 3 | Tie Line to Production |
| 13 | TO PROD 4 | Tie Line to Production |

### Bottom Row (INPUTS)

| Jack | Label | Destination | Normalled From |
|------|-------|-------------|----------------|
| 1 | FET IN | FET Compressor Input | WA73 OUT |
| 2 | AUTOTUNE IN | Antares Auto-Tune Input | FET OUT |
| 3 | KLARK IN | Klark Teknik EQ Input | AUTOTUNE OUT |
| 4 | 18i20 LINE 1 | 18i20 Line Input 1 | KLARK OUT (or AUTOTUNE OUT if Klark broken) |
| 5 | 18i20 LINE 2 | 18i20 Line Input 2 | — |
| 6 | 18i20 LINE 3 | 18i20 Line Input 3 | — |
| 7 | 18i20 LINE 4 | 18i20 Line Input 4 | — |
| 8 | FROM PROD 1 | Tie Line from Production | THRU |
| 9 | FROM PROD 2 | Tie Line from Production | THRU |
| 10 | FROM PROD 3 | Tie Line from Production | THRU |
| 11 | FROM PROD 4 | Tie Line from Production | THRU |

---

## Normalling Summary (Vocals Patchbay)

| Connection | Type |
|------------|------|
| WA73 OUT → FET IN | HALF-NORMAL |
| FET OUT → AUTOTUNE IN | HALF-NORMAL |
| AUTOTUNE OUT → KLARK IN | HALF-NORMAL |
| KLARK OUT → 18i20 LINE 1 | HALF-NORMAL |
| All tie lines | THRU |

**Default chain:** WA73 → FET → Auto-Tune → Klark → 18i20

**Bypass any processor:** Patch around it (half-normal lets signal through until you patch)

---

# TIE LINES (Between Workstations)

4 lines each direction = 8 cables total.

| Label | Direction |
|-------|-----------|
| V→P 1 | Vocals → Production |
| V→P 2 | Vocals → Production |
| V→P 3 | Vocals → Production |
| V→P 4 | Vocals → Production |
| P→V 1 | Production → Vocals |
| P→V 2 | Production → Vocals |
| P→V 3 | Production → Vocals |
| P→V 4 | Production → Vocals |

---

# COMMON PATCHES (Cheat Sheet)

## Beat Making (no cables)
Just use Patchbay 1. Synths → OctoPre Dynamic → MPC.

## Add Character Compression
```
MPC OUT 3 ──► VLA IN L/R ──► VLA OUT L/R ──► OCTO IN 5-6 ──► MPC
```

## Add Reverb
```
MPC OUT 4 ──► LEX A IN L/R ──► LEX A OUT L/R ──► OCTO IN 7-8 ──► MPC
```

## Master Bus Compression (experiment only)
```
MPC MAIN L/R ──► VCA IN L/R ──► VCA OUT L/R ──► Monitor
```
Unpatch when done.

## Print Through Lexicon
```
MPC OUT 3 ──► LEX A IN ──► LEX A OUT ──► UR IN 1-2 ──► Record in DAW
```
