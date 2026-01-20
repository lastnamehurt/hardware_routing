# MiniFreak Parameter Reference

Accurate parameter names from the official Arturia MiniFreak manual.

---

## Oscillator Types (OSC 1 & OSC 2 shared)

| # | Type | Parameters | Description |
|---|------|------------|-------------|
| 1 | **BasicWaves** | Morph, Sym, Sub | Saw/Square blend with sub oscillator |
| 2 | **SuperWave** | Wave, Detune, Volume | Detuned stacked waveforms (supersaw etc) |
| 3 | **Harmo** | Content, Sculpting, Chorus | Harmonic/additive synthesis |
| 4 | **KarplusStr** | Bow, Position, Decay | Physical modeling (plucked/bowed strings, drums) |
| 5 | **VAnalog** | Detune, Shape, Wave | Virtual analog pulse + sawtooth |
| 6 | **Waveshaper** | (varies) | Waveform manipulation |
| 7 | **Two Op. FM** | (varies) | 2-operator FM synthesis |
| 8 | **Formant** | (varies) | Vocal formant synthesis |
| 9 | **Chords** | (varies) | Chord engine (OSC 2 only) |
| 10 | **Speech** | (varies) | Speech synthesis |
| 11 | **Modal** | (varies) | Modal/resonator synthesis |
| 12 | **Noise** | (varies) | Noise generator |
| 13 | **Bass** | (varies) | Bass-focused engine (Noise Engineering) |
| 14 | **SawX** | (varies) | Extended saw (Noise Engineering) |
| 15 | **Harm** | (varies) | Harmonic engine (Noise Engineering) |
| 16 | **Audio In** | (varies) | External audio input (OSC 1 only) |

---

## OSC 2 Processor Types (instead of oscillator)

| Type | Description |
|------|-------------|
| **Multi Filter** | Digital multi-mode filter |
| **Surgeon Filter** | Precise surgical filter |
| **Comb Filter** | Comb filtering effect |
| **Phaser Filter** | Phase-based filter |
| **Destroy** | Bitcrusher/distortion |
| **FM/RM** | Frequency/Ring modulation of OSC 1 |

---

## Analog Filter

| Parameter | Description |
|-----------|-------------|
| **Type** | LP (Low Pass), BP (Band Pass), HP (High Pass) |
| **Cutoff** | Filter frequency (20 Hz - 20 kHz) |
| **Resonance** | Emphasis at cutoff frequency |

*Note: The analog filter is NOT multi-pole selectable (no 12dB/24dB option). It has a fixed slope.*

---

## Digital Effects (FX1 & FX2)

| # | Effect | Key Parameters |
|---|--------|----------------|
| 1 | **Chorus** | Rate, Depth, Mix |
| 2 | **Phaser** | Rate, Depth, Mix |
| 3 | **Flanger** | Rate, Depth, Mix |
| 4 | **Reverb** | Size, Decay, Mix |
| 5 | **Delay** | Time, Feedback, Mix |
| 6 | **Distortion** | Drive, Tone |
| 7 | **Bit Crusher** | Bits, Rate |
| 8 | **3 Bands EQ** | Low, Mid, High |
| 9 | **Peak EQ** | Freq, Q, Gain |
| 10 | **Multi Comp** | Threshold, Ratio |

---

## Envelopes

### Amp Envelope
- Attack, Decay, Sustain, Release (ADSR)

### Filter/Mod Envelope  
- Attack, Decay, Sustain, Release (ADSR)

### Cycling Envelope
- Can loop for LFO-like behavior

---

## LFOs

| Parameter | Description |
|-----------|-------------|
| **Shape** | Sine, Triangle, Saw, Square, S&H (Sample & Hold), Random |
| **Rate** | Speed (sync or free) |
| **Amount** | Modulation depth (set in mod matrix) |

---

## Voice Modes

| Mode | Description |
|------|-------------|
| **Poly** | Polyphonic (up to 6 voices) |
| **Mono** | Monophonic |
| **Unison** | Stacked voices |
| **Para** | Paraphonic |

---

## Key Controls

| Control | Description |
|---------|-------------|
| **Glide** | Portamento on/off |
| **Glide Time** | Portamento speed |
| **Volume** | Oscillator level |
| **Type** | Oscillator engine selector |
| **Wave/Morph/etc** | First parameter (varies by type) |
| **Timbre/Shape/etc** | Second parameter (varies by type) |
| **Shape/Sub/etc** | Third parameter (varies by type) |

---

## Corrections to Previous Patches

| Incorrect Term | Correct MiniFreak Term |
|----------------|------------------------|
| "Basic Shapes" | **BasicWaves** |
| "Analog" (osc type) | **VAnalog** |
| "Harmonic" | **Harmo** |
| "Karplus" | **KarplusStr** |
| "FM" | **Two Op. FM** |
| "Pulse" | Use **VAnalog** (Shape parameter) or **BasicWaves** (Morph=0) |
| "Saw" | Use **BasicWaves** (Morph=50) or **VAnalog** |
| "Triangle" | Use **SuperWave** (Wave parameter) or **BasicWaves** |
| "Sine" | Use **SuperWave** (Wave parameter) |
| "LP 12dB / LP 24dB" | Just **LP** (single slope) |
| "Band-Pass" | **BP** |
| "SEM" | Not available — use **LP/BP/HP** |
| "Tape Saturation" | **Distortion** (with low drive) |
| "Spring Reverb" | **Reverb** (adjust parameters for spring-like) |
