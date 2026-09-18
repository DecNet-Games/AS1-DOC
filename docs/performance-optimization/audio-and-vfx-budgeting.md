---
layout: default
title: "Audio & VFX Budgeting"
parent: "Performance & Optimization"
nav_order: 2
---

# Audio & VFX Budgeting

- **Particle Lifespans**: Capped at `1.2s` for muzzle flashes and blood bursts.
- **Decal Limits**: Maximum `30` active decals in the world; oldest decals automatically recycle back to the pool.
- **Voice Concurrency**: Max `16` simultaneous audio voices to conserve mobile audio DSP cycles.
