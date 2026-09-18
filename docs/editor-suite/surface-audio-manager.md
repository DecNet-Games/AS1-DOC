---
layout: default
title: "Surface Audio Manager"
parent: "AS1 Tool Suite"
nav_order: 6
---

# Surface Audio Manager

Shooter immersion demands that footstep sounds correspond to the material underfoot. The **Surface Audio Manager** (`TabSurfaceAudio.cs`) binds physics LayerMasks to randomized sound clip banks.

---

## Surface Layer Matrix

| Surface | Layer | Detection Mechanism | Included Audio Samples |
| :--- | :--- | :--- | :--- |
| **Concrete** | Layer 10 (`Concrete`) | Downward raycast from player ground checker | Crisp pavement footsteps, scuffs |
| **Metal** | Layer 11 (`Metal`) | Downward raycast | Hollow industrial grating, metallic clangs |
| **Dirt / Sand** | Layer 12 (`Dirt`) | Downward raycast | Soft gravel shuffle, loose earth |
| **Wood** | Layer 13 (`Wood`) | Downward raycast | Resonant plank creaks, floorboards |
| **Water** | Layer 14 (`Water`) | Downward raycast | Wet splash, slosh effects |

---

## Tuning Pitch and Volume Randomization

To prevent repetitive footstep fatigue:
- Set **Volume Range**: `0.85` to `1.0`.
- Set **Pitch Jitter**: `0.92` to `1.08`.
Each footstep step randomly perturbs the playback frequency, producing authentic organic locomotion audio.
