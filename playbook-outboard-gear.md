# Outboard Gear Playbook

How to leverage your analog processing chain with the MPC XL.

---

## Your Outboard Arsenal

### Production Rack

| Gear | Type | Character |
|------|------|-----------|
| **OctoPre Dynamic** | Preamp + Compression | Input control (seatbelt) for synths |
| **OctoPre (Regular)** | Preamp | Clean gain, front panel mic access |
| **Pro VLA-2** | Tube/Opto Compressor | Warm, smooth, glue |
| **WA VCA Bus** | VCA Compressor | Punchy, tight, SSL-style |
| **Golden Age EQ** | Mono EQ | Vintage color, presence |
| **Ultragraph EQ** | Stereo Graphic EQ | Surgical or vibe |
| **Lexicon MX400XL** | Dual Stereo FX | Engine A: reverb, Engine B: delay |

### Vocals Rack

| Gear | Type | Character |
|------|------|-----------|
| **Scarlett 18i20** | Interface | A/D conversion to Mac Studio |
| **WA73** | Neve-style Preamp | Warmth, presence, color |
| **FET Compressor** | FET Compressor | Fast, punchy, 1176-style |
| **Antares Auto-Tune** | Pitch Correction | Real-time tuning, vocal effects |
| **Klark Teknik EQ** | Graphic EQ | Tone shaping (**possibly broken - may replace with passive EQ**) |

### Two Racks, Full Access

Tie lines (4 each direction) connect both racks. You can:
- Send MPC stems to Vocals rack for recording
- Access Vocals rack processing from Production
- Access Production rack processing from Vocals

---

## The Two OctoPres Explained

| OctoPre | Location | Role | Front Panel (1-2) | Back Panel (3-8) |
|---------|----------|------|-------------------|------------------|
| **Dynamic** | Production | Synths IN to MPC | Quick patching | Synths, returns |
| **Regular** | Production | MPC stems OUT | **MIC / sampling** | MPC OUT 3-6 |

### OctoPre Dynamic (Seatbelt)
- Receives synths (MiniFreak, DGX)
- Built-in compression tames hot signals before MPC
- Use 2-3 dB gain reduction (light control)
- **Think:** Input protection + slight color

### OctoPre Regular (Clean Gain)
- Receives MPC stems for recording to DAW
- Front panel inputs for quick mic/sampling
- No compression - clean pass-through
- **Think:** Utility routing + mic access

---

## Monitoring Setup

**You use headphones, not monitors.**

```
MPC Headphone Jack → Splitter → Headphones
                            → Backup speakers (when needed)
```

This frees **all 8 MPC outputs** for processing.

---

## Output Allocation by Scenario

### Scenario A: Beat Making (Default)
No patch cables. Just play.
```
Synths → OctoPre Dynamic → MPC
Monitor via headphones
```
**Outputs used:** 0

---

### Scenario B: Tracking Stems to DAW
```
MPC OUT 3-6 → OctoPre Regular → Tie Lines → 18i20 → DAW
```
**Outputs used:** 4

---

### Scenario C: Stereo Mix Processing
Single processor on master.
```
MPC OUT 1-2 → VCA Bus IN → VCA Bus OUT → Headphones (or record)
```
**Outputs used:** 2

---

### Scenario D: Parallel Compression
Crush drums while keeping original.
```
MPC OUT 7-8 → VLA IN → VLA OUT → MPC IN (blend in mixer)

MPC Routing:
├── Drums → OUT 1-2 (clean)
└── Drums → OUT 7-8 (parallel bus) → VLA → return
```
**Outputs used:** 4

---

### Scenario E: Full Lexicon (Both Engines)
Patch to break PB1 stem normals.
```
MPC OUT 3-4 → Lexicon A IN (reverb)
MPC OUT 5-6 → Lexicon B IN (delay)
Lexicon A/B OUT → OCTO-D IN 7-8 (return to MPC)
```
**Outputs used:** 4

---

### Scenario F: Max Processing Mode
Everything at once.
```
MPC OUT 1-2 → VCA Bus (master glue)
MPC OUT 3-4 → Lexicon A (reverb send)
MPC OUT 5-6 → Lexicon B (delay send)
MPC OUT 7-8 → VLA (parallel compression)

Returns:
├── VCA OUT → Record or monitor
├── Lexicon A/B OUT → OCTO-D IN 7-8
└── VLA OUT → MPC IN (blend)
```
**Outputs used:** 8

---

## Common Patches (Cheat Sheet)

### Warm Up a Beat
```
MPC OUT 1-2 → VLA IN → VLA OUT → Record/Monitor
Settings: Slow attack, medium release, 2-4 dB GR
```

### Glue the Mix
```
MPC OUT 1-2 → VCA Bus IN → VCA Bus OUT → Record/Monitor
Settings: Fast attack, auto release, 1-2 dB GR
```

### Add Space (Reverb)
```
MPC Program: Send drums/keys to OUT 3-4
OUT 3-4 → Lexicon A IN → Lexicon A OUT → OCTO-D IN 7 → MPC IN
Blend wet signal in MPC mixer
```

### Add Movement (Delay)
```
MPC Program: Send lead/vocal to OUT 5-6
OUT 5-6 → Lexicon B IN → Lexicon B OUT → OCTO-D IN 8 → MPC IN
Sync delay to tempo
```

### Crush the Drums (Parallel)
```
MPC Program: Send drums to OUT 7-8 (post-fader)
OUT 7-8 → VLA IN → VLA OUT → MPC IN
Settings: Smash it (10+ dB GR), blend to taste
```

### Add Presence (EQ)
```
MPC OUT 3 → Golden Age EQ IN → EQ OUT → MPC IN
Boost 3-5kHz for presence, cut 200-400Hz for mud
```

### Widen Stereo (EQ)
```
MPC OUT 1-2 → Ultragraph IN → Ultragraph OUT → Record
Subtle smile curve: boost lows + highs, cut mids slightly
```

---

## Signal Chain Recipes

### Lo-Fi Drums
```
Drums → VLA (crush) → Golden Age EQ (cut highs) → MPC
```

### Thick Bass
```
Bass → VCA Bus (control peaks) → MPC
```

### Dreamy Keys
```
Keys → Lexicon A (plate reverb, long tail) → MPC
```

### Dub Delay
```
Any element → Lexicon B (tempo sync, feedback 60%) → MPC
```

### Full Mix Polish
```
MPC Master → VCA Bus (1-2 dB glue) → VLA (warmth) → Record
```

---

## Return Routing Options

| Return To | Use Case |
|-----------|----------|
| MPC IN 1-4 | Blend processed signal in MPC mixer |
| OCTO-D IN 7-8 | Record processed signal via OctoPre |
| Tie Lines → 18i20 | Record to DAW |
| Headphones direct | Monitor only, don't record |

---

## Pro Tips

1. **Gain staging:** Hit outboard at -18 to -12 dBFS. Too hot = distortion.

2. **Commit early:** Print the processed sound to MPC. Don't save everything for later.

3. **A/B test:** Bypass the processor to make sure it's actually helping.

4. **Less is more:** 1-2 dB of compression often beats 10 dB.

5. **Serial vs parallel:**
   - Serial (in-line): 100% processed
   - Parallel (blend): Keep punch, add character

6. **Lexicon tip:** Use A for space (reverb), B for time (delay). Don't use both for the same thing.

7. **VLA vs VCA:**
   - VLA = smooth, invisible, warming
   - VCA = punchy, controlled, aggressive

---

---

## Vocals Rack Processing

### Vocal Recording Chain

```
Mojave Mic
    ↓
WA73 (preamp + Neve color)
    ↓
FET Compressor (control dynamics)
    ↓
Antares Auto-Tune (pitch correction if needed)
    ↓
18i20 LINE IN (A/D conversion)
    ↓
Mac Studio (Pro Tools / Ableton)
```

### WA73 Settings (Vocals)
```
Gain: Set for healthy level (-18 to -12 dBFS)
Tone control: To taste (adds presence/air)
```
**Character:** Neve warmth, slight saturation when pushed

### FET Compressor Settings (Vocals)

**Controlled Performance:**
```
Ratio: 4:1
Attack: Medium-fast (catch transients)
Release: Medium
GR: 3-6 dB
```

**Aggressive/Effect:**
```
Ratio: 8:1 or higher
Attack: Fast
Release: Fast
GR: 8-12 dB (intentional squash)
```

### Antares Auto-Tune Usage

**Natural Correction:**
```
Retune Speed: 20-50ms (subtle)
Key: Match your track
Humanize: 20-30
```

**Effect (T-Pain style):**
```
Retune Speed: 0ms (hard tune)
Key: Match your track
Humanize: 0
```

**Bypass:** When you want raw, untuned vocals

### Klark Teknik EQ (if working)

**Vocal Settings:**
```
Cut 200-300Hz: Reduce mud
Boost 3-5kHz: Presence/clarity
Cut 6-8kHz: If sibilant
Boost 10kHz+: Air (if needed)
```

**If broken:** Replace with passive EQ (Pultec-style recommended)

---

## Cross-Rack Workflows

### MPC Stems to Pro Tools

```
MPC OUT 3-6 → OctoPre Regular → Tie Lines → 18i20 → Pro Tools

Production Rack          Vocals Rack
─────────────           ───────────
MPC OUT 3-6      →      FROM PROD 1-4
     ↓                       ↓
OctoPre Regular         18i20 LINE IN
     ↓                       ↓
TO PROD 1-4             Mac Studio
```

### Vocals Through Production Processing

Want to run vocals through the Lexicon or VLA?

```
Vocals Rack              Production Rack
───────────             ─────────────
WA73 OUT         →      FROM VOC
     ↓                       ↓
TO PROD                  Lexicon / VLA / etc.
                             ↓
                         TO VOC
     ↓
FROM PROD        ←
     ↓
18i20 LINE IN
```

### MPC as Vocal Processor

Record vocals, process through MPC effects, return to DAW:

```
18i20 OUT → Tie Lines → MPC IN
MPC processing (effects, sampling)
MPC OUT → Tie Lines → 18i20 IN → DAW
```

---

## Quick Reference: What Goes Where

### Production Rack

| I want to... | Route |
|--------------|-------|
| Warm up the mix | MPC OUT 1-2 → VLA |
| Glue the mix | MPC OUT 1-2 → VCA Bus |
| Add reverb | MPC OUT 3-4 → Lexicon A |
| Add delay | MPC OUT 5-6 → Lexicon B |
| Crush drums | MPC OUT 7-8 → VLA (parallel) |
| Add presence | Any OUT → Golden Age EQ |
| Shape tone | Any OUT → Ultragraph EQ |
| Control synth input | Synths → OctoPre Dynamic |
| Record stems | MPC OUT 3-6 → OctoPre Regular → Tie Lines |
| Quick mic recording | Mic → OctoPre Regular front panel (IN 1-2) |

### Vocals Rack

| I want to... | Route |
|--------------|-------|
| Record vocals | Mojave → WA73 → FET → 18i20 |
| Pitch correct | Insert Auto-Tune after FET |
| Shape vocal tone | Insert Klark Teknik EQ |
| Add outboard FX to vocals | WA73 → Tie Lines → Production processing → Tie Lines → 18i20 |
| Send DAW audio to MPC | 18i20 OUT → Tie Lines → MPC IN |
