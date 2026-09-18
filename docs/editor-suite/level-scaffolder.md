---
layout: default
title: "Level Scaffolder"
parent: "AS1 Tool Suite"
nav_order: 5
---

# Level Scaffolder

The **Level Scaffolder** (`TabLevelScaffolder.cs`) generates turnkey shooter combat scenes with configured lighting environments, player spawn anchors, camera volumes, and NavMesh boundaries.

---

## Features

- **Day & Night Dual Template Generation**: Generates synchronized Day and Night scene variations with directional sun angles, ambient skyboxes, and nocturnal spotlights.
- **Drop-in Core Prefabs**: Automatically instantiates the `Managers`, `GameCanvas`, `MainCamera`, `ThirdPersonCamera`, `AimCamera`, and `Player` prefabs.
- **Bounds & Spawner Setup**: Creates perimeter boundary colliders and assigns pre-configured `ZombieSpawner` volumes.

![Night Environment Gameplay Calibration]({{ site.baseurl }}/assets/images/sector07-night-gameplay.png)

---

## How to Scaffold a New Level

1. Open `Tools > AS1 > Suite Hub` -> **[LVL] Level Builder**.
2. Enter your desired level name (e.g., `Sector_08_Outpost`).
3. Select Environment Profile: `Daytime Clear`, `Night Operations`, or `Overcast Fog`.
4. Click **Generate Starter Scene**.
5. Open the newly generated scene in `Assets/AS1/Scenes/` and bake the NavMesh (`Window > AI > Navigation`).
