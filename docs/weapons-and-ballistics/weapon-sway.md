---
layout: default
title: "Weapon Sway & Bobbing"
parent: "Weapons & Ballistics"
nav_order: 4
---

# Weapon Sway & Bobbing

`WeaponSway.cs` enhances immersion by simulating the natural weight and momentum of held firearms during mouse look and player movement.

---

## Sway Dynamics

- **Look Sway**: Captures raw mouse `Mouse X` and `Mouse Y` inputs, applying an inverse rotational lag to the weapon mesh.
- **Movement Bobbing**: During locomotion, a sinusoidal displacement function (`Mathf.Sin(Time.time * frequency)`) translates the weapon slightly up, down, left, and right to mirror the operative's walking cadence.
- **ADS Suppression**: When Aiming Down Sights, sway and bobbing amplitudes are dampened by `80%` to ensure stable sight picture.
