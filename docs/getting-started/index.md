---
layout: default
title: "Getting Started"
nav_order: 2
has_children: true
permalink: /docs/getting-started/
---

# Getting Started with AS1

Welcome to the **AS1 - Advanced Shooter System** documentation. This section covers system prerequisites, installation via the Unity Asset Store, onboarding setup, and a breakdown of the shipped package architecture.

---

## Architecture Overview

AS1 is structured around decoupled modular components communicating via standard Unity messages, events, and ScriptableObjects:

```mermaid
graph LR
    subgraph "Input Layer"
        Desktop[PC Keyboard/Mouse] --> VInput[Decnet Virtual Input]
        Mobile[Mobile Touch/Joystick] --> VInput
    end

    subgraph "Controller Layer"
        VInput --> Player[PlayerController]
        Player --> Movement[PlayerMovement]
        Player --> Aim[PlayerAim]
        Player --> WeaponMgr[PlayerWeaponManager]
    end

    subgraph "Combat & Audio"
        WeaponMgr --> Wpn[Active Weapon]
        Wpn --> Ballistics[Raycast Ballistics]
        Wpn --> Recoil[Procedural Recoil]
        Movement --> SurfaceAudio[Surface Footsteps]
    end

    subgraph "AI & World"
        Ballistics --> Zombie[ZombieHitbox / AI]
        Zombie --> FSM[Pluggable FSM]
        Zombie --> Drops[LootDropManager]
    end
```

---

## Reading Guide

1. [Installation & Licensing]({{ site.baseurl }}/docs/getting-started/installation/): Important details on obtaining the package through the official Unity Asset Store, importing assets, and pipeline considerations.
2. [5-Minute Quick Start]({{ site.baseurl }}/docs/getting-started/quick-start/): Step-by-step guidance on running Sector 07 and confirming keyboard, mouse, and touch mechanics.
3. [Project Structure]({{ site.baseurl }}/docs/getting-started/project-structure/): Folder taxonomy of `Assets/AS1/` to help you locate prefabs, scripts, animations, and scenes.
