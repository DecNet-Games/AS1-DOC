---
layout: default
title: "Dual Weapon Switching"
parent: "Weapons & Ballistics"
nav_order: 7
---

# Dual-Slot Weapon Management

`PlayerWeaponManager.cs` and `PlayerWeaponSwitch.cs` handle primary and secondary weapon inventories.

---

## Weapon Slots

- **Slot 1 (`Alpha1`)**: Primary Firearm (e.g., AK-47, M4A1, Sniper Rifle).
- **Slot 2 (`Alpha2`)**: Sidearm / Secondary (e.g., Tactical Pistol, UMP-45).

### Swap Logic:
1. Lower / holster active weapon animation plays.
2. Current weapon GameObject is disabled.
3. Target weapon GameObject is enabled.
4. Raise / draw animation plays, binding IK hand placements.
5. The HUD ammo counter and weapon silhouette smoothly update.
