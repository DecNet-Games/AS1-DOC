---
layout: default
title: "Quick Melee Combat"
parent: "Weapons & Ballistics"
nav_order: 8
---

# Quick Melee Combat

When enemies breach close quarters, players can execute an instantaneous knife slash via `PlayerMeleeCombat.cs` by pressing `F` (or tapping the knife icon on mobile).

---

## Spherecast Detection

Melee does not use a thin raycast, which often misses agile targets. Instead, it performs a forward `Physics.SphereCast`:
- **Cast Radius**: `0.45m`
- **Reach Distance**: `1.8m`
- **Damage**: `60 HP`
- **Stagger**: Applies immediate movement interrupt to hit zombies.
