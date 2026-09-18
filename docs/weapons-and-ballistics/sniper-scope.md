---
layout: default
title: "Sniper Scope & Optics"
parent: "Weapons & Ballistics"
nav_order: 5
---

# Sniper Scope & Optical Zoom

Long-range rifles in AS1 utilize `SniperScopeOverlay.cs` to deliver realistic precision optic gameplay.

---

## Optical Sequence

1. Player holds **Right Mouse Button** while equipped with a scoped weapon.
2. The virtual camera's Field of View (FOV) zooms from `60?` down to `15?` over `0.18s`.
3. The weapon 3D mesh is momentarily culled to prevent interior clipping.
4. The full-screen 2D sniper crosshair reticle with vignetted optic housing is rendered on top of the UI.
5. Mouse sensitivity is scaled down proportionally to the FOV ratio, allowing micro-adjustments for long-distance headshots.
