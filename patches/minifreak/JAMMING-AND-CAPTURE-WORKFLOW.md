# Jamming & Capture Workflow

How to jam freely on your MiniFreak while capturing ideas for later production.

**Goal:** Play without overthinking, but never lose a good idea.

---

## The Problem

- You want to **experiment freely** without committing
- But you also want to **capture happy accidents** 
- MIDI alone doesn't capture the sound design tweaks you made
- Audio alone can't be edited/transposed later
- You need both, plus a way to find stuff later

---

## The Solution: Dual Capture + Tagging

Record **MIDI and Audio simultaneously**, then tag/keep the good stuff.

---

## Hardware Setup

```
MiniFreak MIDI OUT  →  MPC MIDI IN
MiniFreak AUDIO OUT →  MPC AUDIO IN (1/2 or 3/4)
```

**MiniFreak Settings:**
- MIDI OUT: ON
- Local: ON (so you hear yourself)
- Audio Out: Main L/R

---

## MPC Project Template

Create a template project called `JAM_SESSION_TEMPLATE` with these tracks pre-configured:

### Track 1: MIDI Track (Capture)
| Setting | Value |
|---------|-------|
| Type | MIDI |
| Output | MiniFreak (USB or DIN) |
| Input | MiniFreak |
| Monitor | OFF (you hear the synth directly) |

### Track 2: Audio Track (Capture)
| Setting | Value |
|---------|-------|
| Type | Audio |
| Input | Input 1/2 (wherever MiniFreak is plugged) |
| Monitor | ON |
| Record Arm | ON |

### Track 3: Audio Track (Colored/Processed)
| Setting | Value |
|---------|-------|
| Type | Audio |
| Input | Input 1/2 |
| Insert FX | Lo-Fi, Reverb, Delay, etc. |
| Monitor | ON |
| Record Arm | OFF (switch when you want colored version) |

---

## Jamming Workflow

### Phase 1: Free Jam (Capture Everything)

1. **Load template**
2. **Arm both MIDI and Audio tracks**
3. **Hit Record and just play**
   - Don't worry about mistakes
   - Twist knobs, change patches
   - Follow your ears
4. **Record for 5-10 minutes straight**

**What you're capturing:**
- MIDI = the notes you played
- Audio = the exact sound including knob tweaks

### Phase 2: Review & Tag

After jamming:

1. **Stop and listen back**
2. **Mark good sections:**
   - Use MPC's **Loop/Region markers**
   - Or just note the time: "2:34 - sick bass line"
3. **For keepers:**
   - Trim the audio region
   - Bounce/consolidate to a new sample
   - Name it descriptively: `JAM_01_dirty_bass_riff_Cmin`

### Phase 3: Build Sample Library

Move good captures to organized folders:

```
MiniFreak_Captures/
├── Bass_Riffs/
│   ├── JAM_01_dirty_bass_Cmin.wav
│   └── JAM_03_sub_groove_Fmin.wav
├── Lead_Phrases/
│   ├── JAM_01_crying_lead_Gmaj.wav
│   └── JAM_02_pluck_melody_Amin.wav
├── Textures/
│   └── JAM_04_atmos_pad_long.wav
└── Happy_Accidents/
    └── JAM_02_weird_filter_sweep.wav
```

---

## The "Colored" Audio Trick

Sometimes you want to hear your synth **through effects** while jamming to inspire different playing.

### How It Works

Both Track 2 and Track 3 receive the **same audio input** (MiniFreak's output). The difference is which one you hear vs. record:

| Track | Input | Insert FX | Monitor | Record Arm | Purpose |
|-------|-------|-----------|---------|------------|---------|
| Track 2 (Clean) | Input 1/2 | None | **OFF** | **ON** | Records dry signal |
| Track 3 (Colored) | Input 1/2 | Lo-Fi, Reverb, etc. | **ON** | OFF | You hear this |

### IMPORTANT: Monitoring Requirement

**This only works if you listen through the MPC, not the MiniFreak directly.**

You must:
- Turn **OFF** or unplug MiniFreak's headphone/speaker output
- Listen **only** through MPC headphones or MPC outputs

If you hear the MiniFreak directly from its own outputs, you'll hear dry regardless of MPC effects. The colored monitoring only works when the MPC is your sole audio path.

### What happens:
- You **hear** Track 3 (with effects) because Monitor is ON
- You **record** to Track 2 (dry) because Record Arm is ON
- Same source signal, different monitoring path
- Best of both worlds

### When to flip:
- If you love the colored sound and want to commit → arm Track 3 instead
- If you want flexibility later → keep recording clean

### Simpler Alternative

If this setup feels complicated, skip Track 3 entirely:

| Track | Purpose |
|-------|---------|
| Track 1 | MIDI capture |
| Track 2 | Audio capture (dry) |

Add effects later during production, not while jamming. This is totally valid.

---

## Quick Capture Mode (For Fast Ideas)

When you just need to grab something quick:

1. **Audio Track only** (skip MIDI)
2. **Hit Record**
3. **Play the idea 2-3 times**
4. **Stop**
5. **Chop and save immediately**

Don't overthink. Capture now, organize later.

---

## Naming Convention for Captures

```
{SESSION}_{NUMBER}_{DESCRIPTION}_{KEY/TEMPO}.wav
```

Examples:
- `JAM_01_dusty_rhodes_chords_Cmaj_85bpm.wav`
- `JAM_03_sub_bass_hit_F.wav`
- `JAM_07_weird_texture_atonal.wav`

The key/tempo helps when you come back later.

---

## End of Session Checklist

Before closing:

- [ ] Listened back to full jam?
- [ ] Marked/tagged good sections?
- [ ] Bounced keepers to samples?
- [ ] Named samples descriptively?
- [ ] Moved to organized folders?
- [ ] Deleted obvious garbage? (optional - disk is cheap)

---

## Weekly Sample Review

Once a week:

1. Open your `MiniFreak_Captures/` folder
2. Listen through `Happy_Accidents/` and unsorted
3. Move gems to proper categories
4. Delete the rest (or archive)

This keeps your library useful, not bloated.

---

## Pro Tips

### 1. Always Record More Than You Think
You can delete later. You can't un-miss a moment.

### 2. Don't Stop to Fix Mistakes
Keep playing. The next thing might be gold.

### 3. Name Things Immediately
"Audio_042" means nothing in 2 weeks.

### 4. Keep One "Dump" Folder
`Happy_Accidents/` or `Unsorted/` — for stuff you're not sure about yet.

### 5. MIDI is Your Safety Net
Even if the audio isn't perfect, MIDI lets you replay with a different patch later.

### 6. Commit When Inspired
If you LOVE something, bounce it to audio and move on. Don't endlessly tweak.

---

## Template Preset Idea

Save this as an MPC template:

```
JAM_SESSION_TEMPLATE.xpj
├── Track 1: MIDI → MiniFreak
├── Track 2: Audio (Clean) ← MiniFreak
├── Track 3: Audio (Colored) ← MiniFreak + FX
├── Track 4: Drums (for context/groove)
└── Tempo: 90 BPM (adjust as needed)
```

Load it, hit record, jam.

---

## Summary

| Phase | What You Do | What You Capture |
|-------|-------------|------------------|
| Jam | Play freely, twist knobs | MIDI + Clean Audio |
| Review | Listen back, mark keepers | — |
| Bounce | Trim and export good bits | Named .wav samples |
| Organize | Move to folders | Searchable library |
| Produce | Load samples into new projects | Your best ideas, ready to use |

The goal: **Never lose a good idea. Never let capture slow you down.**
