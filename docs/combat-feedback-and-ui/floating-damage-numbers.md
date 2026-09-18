---
layout: default
title: "Floating Damage Numbers"
parent: "Combat Feedback & UI"
nav_order: 2
---

# 3D Floating Damage Numbers

`FloatingDamageNumber.cs` spawns billboarded numeric damage readouts in world space at the exact bullet impact coordinate.

---

## Features

- **Billboarding**: Constantly faces the active rendering camera (`transform.rotation = camera.rotation`).
- **Critical Styling**: Standard body shots render in bold white text; headshot criticals render with increased font scale and golden amber coloration.
- **Physics Float**: Numbers drift upward with random horizontal dispersal and alpha fade-out over `0.75s`.
- **Pooled**: Managed via `ObjectPoolManager` with zero runtime memory allocations.
