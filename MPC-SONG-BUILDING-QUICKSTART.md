# MPC Song Building Quickstart

From beat idea to finished song structure. No fluff.

---

## The Big Picture

```
SAMPLES → PROGRAM → TRACKS → SEQUENCE → SONG
   ↓         ↓          ↓          ↓         ↓
 sounds   instrument  layers    "section"  arrangement
                                (verse,    (order of
                                 chorus)    sections)
```

---

## Key Concepts (30 seconds)

| Term | What It Is | Example |
|------|------------|---------|
| **Sample** | A sound file | kick.wav, snare.wav |
| **Program** | An instrument made of samples | "My Drum Kit" |
| **Track** | A layer in a sequence (uses a program) | Drums track, Bass track |
| **Sequence** | A "section" of your song (multiple tracks) | Verse, Chorus, Intro |
| **Song** | Sequences arranged in order | Intro → Verse → Chorus → Verse... |

**Key insight:** You build sequences (sections), then arrange them into a song. You don't arrange the whole song linearly like a DAW.

---

## Phase 1: Make a Beat (One Sequence)

### 1.1 Load/Create a Program

**For drums:**
1. Browser → find drum samples
2. Drag samples onto pads
3. You now have a drum program

**For synth/keys (from MiniFreak samples):**
1. Browser → find your sampled .wav
2. Create Keygroup Program (see below)
3. Assign sample, set root note to C3

---

### How to Create a Keygroup Program

A keygroup program lets you play a sample chromatically across the pads (like a piano).

**On MPC One+ hardware:**

1. **Press MENU → Program Edit** (or the four-pads icon)
2. **Press the + icon** next to Program field
3. **Select "Keygroup"** as the program type
4. **Name it** (double-tap the name field, type, press Enter)

**Assign your sample:**

5. **Load sample to project:** Browser → find your .wav → double-click (adds to sample pool)
6. **Go to Program Edit Mode** (four-pads icon)
7. **Find Sample Layers section** (scroll right in the bottom panel)
8. **Click Layer 1 dropdown** → select your sample
9. **Set Root Note:** This tells MPC what pitch the sample was recorded at
   - If you sampled at C3 (as recommended), set Root to **C3**
   - Pad 13 (Bank D) = original pitch by default

**Now your pads play the sample chromatically** — higher pads = higher pitch, lower pads = lower pitch.

**Quick visual:**
```
┌─────────────────────────────────────────┐
│ Inspector (left side)                   │
│                                         │
│ Track: Track 01                         │
│        [🥁] [🎹] [🔌] [🎵]  ← Click 🎹  │
│              ↑                          │
│         piano-keys icon = Keygroup      │
│                                         │
│ Program: [+] My Bass ▼                  │
│               ↑                         │
│          + to create new                │
└─────────────────────────────────────────┘
```

---

### 1.2 Record a Track

**Live recording (pads):**
1. Set tempo (tap tempo or type it)
2. Press **Record** → **Play**
3. Play pads to the metronome
4. Press **Stop** when done
5. Press **Overdub** to add more without erasing

**Step Sequencer (programming):**
1. Press **Menu** → **Step Sequencer** (or step-bars icon)
2. Select the pad/sound you want to program
3. Click pads to place hits on each step
4. Each pad = 1 step (16 steps = 1 bar in 4/4)

### 1.3 Add More Tracks

1. Click **+** next to Track field (or Track → Add Track)
2. Select program for new track (bass, keys, etc.)
3. Record or program that track
4. Repeat until your beat is complete

**Your first sequence is done.** This is your first "section" (e.g., Verse 1).

---

## Phase 2: Make More Sequences (Sections)

### 2.1 Create a New Sequence

1. Click **Sequence** field in Inspector
2. Select **Sequence 2 (unused)**
3. You're now on a blank sequence

### 2.2 Build It

Option A: **Start fresh**
- Record new tracks from scratch

Option B: **Copy and modify**
1. Menu → Edit → Sequence → **Copy Sequence**
2. Copy Sequence 1 → Sequence 2
3. Modify: change drums, add/remove elements

### 2.3 Suggested Sections to Build

| Sequence | Section | What's Different |
|----------|---------|------------------|
| 1 | Verse | Your main beat |
| 2 | Chorus | Add energy, new elements |
| 3 | Intro | Stripped down, builds up |
| 4 | Bridge | Different vibe, breakdown |
| 5 | Outro | Wind down, fade elements |

---

## Phase 3: Arrange into a Song

### 3.1 Enter Song Mode

1. Press **Menu** → **Song Mode** (or click Song icon in toolbar)
2. Stop playback first (Song Mode only works when stopped)

### 3.2 Understand the Layout

```
┌─────────────────────────────────────────────┐
│  TIMELINE (visual blocks of sequences)      │
├─────────────────────────────────────────────┤
│  SEQUENCE LIST          │  PADS             │
│  Step 1: Intro (1x)     │  [Seq1] [Seq2]    │
│  Step 2: Verse (2x)     │  [Seq3] [Seq4]    │
│  Step 3: Chorus (1x)    │  [Seq5] [  ]      │
│  Step 4: Verse (2x)     │                   │
│  ...                    │                   │
└─────────────────────────────────────────────┘
```

- **Sequence List:** The order your song plays
- **Pads:** Each pad = one of your sequences (tap to add to list)
- **Rpts:** How many times that sequence repeats

### 3.3 Build Your Song Structure

**Method 1: Click pads**
1. Tap the pad for your Intro sequence → adds to list
2. Tap the pad for Verse → adds next
3. Tap Chorus pad
4. Keep going...

**Method 2: Use Sequence List**
1. Click **Insert Step**
2. Click Sequence dropdown → select which sequence
3. Set **Rpts** (repeats): 1 = plays once, 2 = plays twice, etc.

### 3.4 Example Song Structure

| Step | Sequence | Rpts | Bars | Section |
|------|----------|------|------|---------|
| 1 | Seq 3 | 1 | 4 | Intro |
| 2 | Seq 1 | 2 | 8 | Verse |
| 3 | Seq 2 | 1 | 8 | Chorus |
| 4 | Seq 1 | 2 | 8 | Verse |
| 5 | Seq 2 | 1 | 8 | Chorus |
| 6 | Seq 4 | 1 | 4 | Bridge |
| 7 | Seq 2 | 2 | 8 | Chorus |
| 8 | Seq 5 | 1 | 4 | Outro |

### 3.5 Play Your Song

Press **Play** in Song Mode → plays through entire arrangement.

---

## Phase 4: Export

### 4.1 Export Audio

1. Menu → File → Export → **As Audio Mixdown**
2. Set **Start bar:** 1
3. Set **End bar:** (last bar of your song)
4. Set **Audio tail:** 2 seconds (lets reverb/delay fade)
5. Choose format: WAV (quality) or MP3 (sharing)
6. Click **Export**, choose location, name it

---

## Step Sequencer Deep Dive

The step sequencer is for **programming beats precisely** without playing live.

### How It Works

```
16 PADS = 16 STEPS (one bar in 4/4)

Pad 1  2  3  4  5  6  7  8  9  10 11 12 13 14 15 16
  ↓  ↓  ↓  ↓  ↓  ↓  ↓  ↓  ↓  ↓  ↓  ↓  ↓  ↓  ↓  ↓
  1  .  .  .  2  .  .  .  3  .  .  .  4  .  .  .   ← beats
  
Lit pad = note plays on that step
```

### Basic Workflow

1. **Select sound:** Click pad name in grid (or press pad in Pad Select mode)
2. **Enter steps:** Click unlit pads to add notes
3. **Remove steps:** Click lit pads to remove notes
4. **Change bars:** Use Bar < > buttons to move between bars
5. **Adjust velocity:** Q-Links control velocity per step

### Pro Moves

| Action | How |
|--------|-----|
| Different track lengths | Set Length field per track (e.g., 1-bar drums, 4-bar bass) |
| Shift pattern timing | TC (timing correct) shifts where steps land |
| Copy pattern | Copy Track function |
| Half/double speed | Events Half Speed / Events Double Speed |

---

## Quick Reference: Modes

| Mode | What It's For | When to Use |
|------|---------------|-------------|
| **Main** | Overview, recording | Building tracks |
| **Step Sequencer** | Programming beats | Precise drum patterns |
| **Sample Edit** | Editing samples, chopping | Preparing samples |
| **Song** | Arranging sequences | Final song structure |
| **Pad Mute** | Muting individual pads | Live performance |
| **Track Mute** | Muting tracks | Live performance |
| **Next Sequence** | Triggering sequences | Live performance |

---

## Common Tasks Cheat Sheet

| I want to... | Do this... |
|--------------|------------|
| Add a track | Click + next to Track field |
| Delete a track | Right-click Track → Delete |
| Copy a sequence | Menu → Edit → Sequence → Copy Sequence |
| Change sequence length | Click Bars field, drag up/down |
| Change tempo | Click BPM field, type new value |
| Add sequence to song | Song Mode → tap sequence pad |
| Remove step from song | Song Mode → select step → Delete Step |
| Loop a section | Set Rpts value higher |
| Export stems | Export → As Audio Mixdown → select tracks |

---

## Workflow Summary

```
1. MAKE A BEAT
   Load samples → Create program → Record/program tracks → Sequence 1 done

2. MAKE VARIATIONS  
   Copy Sequence 1 → Modify for chorus, intro, etc.

3. ARRANGE
   Song Mode → Order your sequences → Set repeats

4. EXPORT
   Audio Mixdown → WAV/MP3
```

**That's it.** Everything else is refinement.
