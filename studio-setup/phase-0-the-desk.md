# Phase 0 — The Desk (Tascam Integration)

---

## Issue #15: Tascam Mixcast Pro 4 integration

**Labels:** `phase-0`, `the-desk`, `tascam`, `hardware`, `critical`

**Description:**
Integrate the Tascam Mixcast Pro 4 at the desk station with the patchbay and production station. This is **critical infrastructure** for daily work — Zoom meetings, calls, etc.

### Physical Layout

```
LEFT SIDE (rack)          |  RIGHT SIDE (desk)
--------------------------|---------------------------
Presonus channel strip    |  Shure mic (high-end)
Patchbay                  |  Tascam Mixcast Pro 4
```

### Signal Flow (Daily Driver - Zoom/Meetings)

```
Shure mic (desk, right)
    ↓ XLR run across desk
Presonus channel strip preamp (rack, left)
    ↓ line-level out
Vocals patchbay TOP (Presonus out) ── half-normal ──► BOTTOM (Mixcast Mic/Line 1)
    ↓
Tascam Mixcast Pro 4 - Mic/Line 1 (desk, right)
```

**Key Point:** Mic stays **off** the patchbay. Only the **line-level** output of the Presonus lands on the bay (top row) and is half-normalled to Mixcast Mic/Line 1 (bottom row). Default path is identical to the direct cable, but now you can insert EQ/comp or reroute without touching the back of the Mixcast.

### TA-1VP Auto-Tune Insert (optional)
The Tascam TA-1VP lives on the same rack, so its I/O sits on the patchbay (top = output, bottom = input). To drop it in the vocal chain:

1. Patch `Presonus Out` (top row) → `TA-1VP In` (bottom row).
2. Patch `TA-1VP Out` (top row) → `Mixcast Line 1` (bottom row).

Unplug those two jumpers and the signal reverts to the normalled Presonus → Mixcast path instantly.

---

**Tasks:**

### Vocal Chain → Tascam (Priority)
- [ ] Run XLR from Shure mic (desk) to Presonus channel strip (rack)
- [ ] Land Presonus line output on Vocals patchbay top row (label `Presonus Out`)
- [ ] Land Mixcast Mic/Line 1 on Vocals patchbay bottom row, half-normalled from Presonus Out
- [ ] Set gain staging: Presonus output level → Mixcast input level
- [ ] Test with Zoom call to verify quality

### MPC → Tascam Integration
- [ ] Test MPC XL → Tascam connection via patchbay
- [ ] Test MPC XL → Tascam simple connection (headphone out → ext cord → Tascam input)
- [ ] Document both connection methods and use cases

### Documentation
- [ ] Document the full signal path for daily Zoom/meeting use
- [ ] Document gain staging reference for Presonus → Tascam chain
- [ ] Label cables for the desk-to-rack XLR run

---

**Definition of Done:**
- Daily Zoom/meeting workflow works without touching the rack
- Can route MPC to Tascam via either method without re-patching
- Signal path is documented so setup can be recreated

**Blocked by:** #2
