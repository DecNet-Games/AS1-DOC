---
layout: default
title: "5-Minute Quick Start"
parent: "Getting Started"
nav_order: 2
---

# 5-Minute Quick Start

This guide takes you through launching the Sector 07 proving grounds and validating the complete gameplay loop in under five minutes.

---

## Opening the Showcase Scene

In your Unity Project view, navigate to:
```text
Assets/AS1/Scenes/TestingDemo.unity
```
Double-click to open the scene, then press the **Play** button in the Unity Editor toolbar.

![Sector 07 Proving Grounds]({{ site.baseurl }}/assets/images/sector07-hero.png)

---

## Step-by-Step Gameplay Route

### 1. The Weapons Gallery (Station 01)
- You spawn in the forward staging area.
- Walk forward using `WASD` toward the counter marked **01 / ARMORY**.
- Five weapons are displayed: AK-47, M4A1, UMP-45, Tactical Pistol, and Sniper Rifle.
- Approach any weapon and press `E` to pick it up. Your secondary slot is automatically populated.

### 2. Calibrating Ballistics (Station 02)
- Turn toward the **Precision Range** featuring targets at 10m, 20m, and 35m.
- Hold **Right Mouse Button** to Aim Down Sights (ADS).
- Press `V` to toggle between **First-Person (FPS)** and **Third-Person (TPS)** modes. Notice the seamless camera blend and procedural upper-body look-at orientation.
- Fire with **Left Mouse Button**. Test single shots and sustained automatic bursts to observe physical spring-damper recoil and spread recovery.

### 3. The Zombie Arena Drill (Station 04)
- Follow the glowing amber route markers past the central operations tower toward **ZOMBIE ARENA**.
- Approach the central terminal console and interact (`E`) to initiate the drill.
- The arena spawner activates, deploying hostile NavMesh zombies.
- Aim for headshots: notice the red headshot reticle marker, specialized kill audio cue, and high-multiplier floating damage numbers.
- Fatal bullet impacts trigger real-time kinematic-to-dynamic ragdoll physics.

### 4. Bunker Extraction (Station 07)
- The objective display tracks hostile eliminations (`0/3`, `1/3`, `2/3`, `3/3`).
- When all 3 hostiles are eliminated, the hydraulic siren sounds and the **Extraction Bunker** gate behind the central tower unlocks.
- Approach the bunker entrance and enter to complete the session loop.

---

## Desktop Controls Reference

| Input Action | Primary Key / Mouse | Secondary Option |
| :--- | :--- | :--- |
| **Move** | `W`, `A`, `S`, `D` | Left Stick (Gamepad) |
| **Look / Aim Pitch & Yaw** | Mouse Movement | Right Stick (Gamepad) |
| **Sprint** | `Left Shift` (Hold) | Left Stick Click |
| **Jump** | `Space` | South Button (A / Cross) |
| **Aim Down Sights (ADS)** | `Right Mouse Button` (Hold) | Left Trigger |
| **Fire Weapon** | `Left Mouse Button` | Right Trigger |
| **Reload** | `R` | West Button (X / Square) |
| **Toggle FPS / TPS View** | `V` | D-Pad Down |
| **Quick Melee Strike** | `F` | Right Stick Click |
| **Throw Frag Grenade** | `G` | Left Bumper |
| **Weapon Slot 1 / Slot 2** | `1` / `2` | Y / Triangle (Toggle) |
| **Interact / Pickup Item** | `E` | X / Square |
| **Unlock Mouse Cursor** | `F1` | - |
| **Pause Menu** | `Esc` | Start / Options |

---

## Testing Mobile Touch Controls

You can test the mobile input layout directly inside the Unity Editor without deploying to an Android or iOS device:

1. Look at the top-right corner of the gameplay HUD.
2. Click the **TOUCH CONTROLS** checkbox.
3. The dynamic floating joystick and action buttons appear immediately.

![Mobile Controls in Armory]({{ site.baseurl }}/assets/images/gameplay-mobile-armory.png)

- **Left Screen Half**: Drag to engage the movement joystick.
- **Right Screen Half**: Drag to rotate camera pitch and yaw.
- **On-Screen Action Buttons**: Dedicated touch targets for Fire, Aim Down Sights, Jump, Sprint, Reload, Melee, and Grenade.
