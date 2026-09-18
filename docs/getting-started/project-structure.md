---
layout: default
title: "Project Structure"
parent: "Getting Started"
nav_order: 3
---

# Project Structure

Understanding the organization of `Assets/AS1/` ensures frictionless integration into existing codebases.

---

## Directory Hierarchy

```text
Assets/AS1/
??? Animations/
?   ??? Enemy/               # Mecanim controllers, walk, run, attack, death clips
?   ??? Player/              # FPS & TPS locomotion, aim blends, reload, jump
?   ??? Weapons/             # Bolt action, slide reciprocation, mag drop anims
??? Audio/
?   ??? Guns/                # Muzzle blasts, silenced variants, mechanical reloads
?   ??? Player/              # Exertion sounds, breathing, surface-aware footsteps
?   ??? UI/                  # Hit markers, objective dings, click interactions
?   ??? Zombie/              # Groans, aggro roars, swipe impacts, flesh hits
??? Documentation/           # Local manuals, license notices, quick reference
??? Fonts/                   # TextMesh Pro font assets and materials
??? Materials/               # Standard PBR materials, decnet master shaders
??? Models/
?   ??? Characters/          # Humanoid operative meshes and zombie archetypes
?   ??? Environment/         # Sector 07 architectural modules, barriers, crates
?   ??? Weapons/             # High-fidelity firearms and melee weapon meshes
??? Prefabs/
?   ??? Drag & Drop/         # Pre-wired drop-in cameras, UI canvas, managers
?   ??? Enemies/             # Ready-to-spawn NavMesh zombie variants
?   ??? Weapons/             # Visual weapon pickups and equipped socket prefabs
?   ??? VFX/                 # Muzzle flashes, bullet trails, spark decals, blood
??? Scenes/
?   ??? MainMenu.unity       # Operational start menu with scene selector
?   ??? TestingDemo.unity    # Daytime Sector 07 proving grounds
?   ??? TestingDemo_Night.unity # Atmospheric night variant with dynamic spotlights
??? Scripts/                 # Core modular C# engine architecture
??? Textures/                # PBR texture maps (Albedo, Normal, MetallicSmoothness)
??? UI/                      # Crosshairs, minimap frames, damage indicator arcs
??? VFX/                     # Shuriken particle systems for ballistics & explosions
```

---

## Core Script Subsystems (`Assets/AS1/Scripts/`)

| Folder | Core Scripts | Architectural Role |
| :--- | :--- | :--- |
| **`Player/`** | `PlayerController`, `PlayerMovement`, `PlayerAim`, `PlayerWeaponManager`, `PlayerWeaponSwitch`, `DamageIndicatorHUD`, `MinimapRadarHUD` | Player locomotion, upper-body IK orientation, dual weapon inventory, and tactical HUD. |
| **`Weapon/`** | `Weapon`, `WeaponData`, `ProceduralRecoil`, `WeaponSway`, `SniperScopeOverlay`, `MeleeWeapon`, `FragGrenade` | Data-driven ballistics, physical recoil spring-damper, inertial sway, optics zoom. |
| **`Zombie/`** | `BaseStateMachine`, `BaseState`, `AttackAction`, `ChaseAction`, `EnemyDetectionDecision`, `NoiseManager`, `ZombieHitbox` | Pluggable Finite State Machine AI, sensory hearing and vision, weakpoint hitboxes. |
| **`Input/`** | `DecnetInputManager`, `DecnetVirtualInput`, `DecnetJoystick`, `DecnetMobileControlRig`, `DecnetButtonHandler` | Abstracted cross-platform input engine supporting keyboard/mouse, gamepads, and touch. |
| **`Editor/`** | `DecnetSuiteHub`, `TabProjectDoctor`, `TabWeaponCreatorPro`, `TabAICreatorPro`, `TabLevelScaffolder`, `DecnetWelcomeWindow` | Next-gen editor tooling engine for rapid content creation and project validation. |
| **`Utilities/`** | `ObjectPoolManager`, `ExplosiveBarrel`, `DestructibleCrate`, `FloatingDamageNumber`, `ComboStreakManager`, `RagdollController` | Zero-allocation pooling, physics destructibles, billboarded damage numbers. |
| **`Advance/`** | `GameManager`, `GameMenuManager`, `InstructionManager`, `BunkerUnlockSystem`, `ZombieSpawner`, `ViewSwitcher` | Scene progression, objective state management, wave spawning, and camera blending. |
