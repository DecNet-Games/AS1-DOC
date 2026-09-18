---
layout: default
title: "Weapon Creator Pro"
parent: "AS1 Tool Suite"
nav_order: 3
---

# Weapon Creator Pro

**Weapon Creator Pro** (`TabWeaponCreatorPro.cs`) allows technical artists and designers to author production-ready firearms in seconds. It handles procedural recoil parameters, ballistics tuning, audio binding, and visual pickup generation without touching C# code.

![Weapon Creator Pro Editor]({{ site.baseurl }}/assets/images/weapon-creator-pro.png)

---

## 1-Click Category Presets

Clicking any preset button loads mathematically tuned defaults for damage, fire rate, magazine capacity, and spring-damper recoil:

| Category Preset | Damage | Fire Rate | Mag Size | Effective Range | Recoil Vertical | Recoil Horizontal | Fire Mode |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **Assault Rifle** | 25 | 0.10s | 30 | 100m | 1.20 | 0.40 | Full Auto |
| **Tactical Pistol** | 20 | 0.25s | 12 | 50m | 1.80 | 0.20 | Semi-Auto |
| **Pump Shotgun** | 12x8 | 0.85s | 8 | 25m | 4.50 | 1.50 | Semi-Auto |
| **Sniper Rifle** | 120 | 1.20s | 5 | 300m | 6.00 | 0.10 | Bolt Action |

---

## Configuration Sections

### 1. Weapon Identity & Visuals
- **Weapon Identifier**: Unique internal string key (e.g., `AKM_AssaultRifle`).
- **3D Weapon Mesh**: The source FBX model.
- **HUD Icon Sprite**: 2D UI texture used on the gameplay weapon status widget.

### 2. Ballistics & Magazine
- **Base Damage**: Damage applied to target health on standard body impact.
- **Fire Rate**: Inter-shot delay in seconds.
- **Magazine Capacity**: Number of rounds per loaded magazine.
- **Effective Range**: Maximum raycast distance before damage falloff begins.
- **Ammo Caliber Identifier**: Matching ammo type for pickup supply packs (e.g., `7.62mm`, `9mm`).
- **Fire Mode**: `Auto`, `Burst`, or `Semi`.

### 3. Procedural Recoil & Spread
- **Vertical Kick**: Upward rotational impulse applied to the camera and weapon model.
- **Horizontal Kick**: Random left/right rotational jitter.
- **Recoil Recovery (s)**: Damping time required for the spring to return to center resting orientation.
- **Bullet Spread Angle (?)**: Base cone angle within which raycast projectiles deviate from reticle center.

### 4. Audio Sound Bank
- **Gunfire SFX**: High-priority audio clip played per shot.
- **Reload SFX**: Synchronized magazine reload audio.
- **Dry Fire SFX**: Empty chamber click when attempting to fire with 0 rounds.

---

## Generation Output

Clicking **Generate Complete Weapon Asset**:
1. Creates a `WeaponData` ScriptableObject in `Assets/AS1/Scriptables/Weapons/`.
2. Generates an equipped weapon prefab with properly attached `ProceduralRecoil` and socket markers.
3. Generates a world pickup prefab with box collider, rotation script, and `PickUpAmmo` or weapon pickup trigger.
