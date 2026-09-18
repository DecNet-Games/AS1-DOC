---
layout: default
title: "Raycast Ballistics"
parent: "Weapons & Ballistics"
nav_order: 2
---

# Raycast Ballistics & Surface Decals

AS1 uses an optimized raycasting model that calculates instantaneous projectile trajectories while applying realistic cone spread and surface-specific decals.

---

## Spread Cone Calculation

When the player fires:
1. The camera's forward vector serves as the baseline trajectory.
2. A random spherical offset proportional to `bulletSpread` is calculated:
```csharp
Vector3 spreadOffset = Random.insideUnitSphere * currentSpread;
Vector3 shotDirection = (cameraTransform.forward + spreadOffset).normalized;
```
3. When aiming down sights (ADS), `currentSpread` is multiplied by an ADS modifier (`0.35x`), creating tight groupings.

---

## Surface-Aware Decals & VFX

When the raycast collides with a collider:
- If target has tag `Enemy`: Spawns blood impact particles and audio.
- If collider is layer `Metal`: Spawns ricochet sparks and metallic impact decal.
- If collider is layer `Concrete`: Spawns dust burst and bullet hole decal.
All impact decals and particle systems are fetched from the zero-allocation `ObjectPoolManager`.
