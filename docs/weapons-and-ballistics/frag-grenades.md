---
layout: default
title: "Frag Grenades"
parent: "Weapons & Ballistics"
nav_order: 9
---

# Explosive Frag Grenades

`PlayerGrenadeThrower.cs` and `FragGrenade.cs` provide a physics-based explosive ordnance system.

---

## Mechanics

1. **Throw Impulse**: Pressing `G` instantiates a physics `FragGrenade` prefab with forward force (`18 m/s`) and upward loft (`4 m/s`).
2. **Bouncing & Surface Friction**: Utilizes a bouncy physic material, rolling across terrain and ricocheting off walls.
3. **Fuse Timer**: Explodes automatically after `3.0s`.
4. **Radial Blast**:
   - `Physics.OverlapSphere` evaluates all objects within `7.5m`.
   - Linear falloff: Maximum damage (`250 HP`) at epicenter, scaling to `0 HP` at boundary.
   - Triggers camera trauma shake on the Cinemachine camera.
