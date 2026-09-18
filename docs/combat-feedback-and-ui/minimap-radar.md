---
layout: default
title: "Minimap & Radar System"
parent: "Combat Feedback & UI"
nav_order: 5
---

# Minimap & Radar System

`MinimapRadarHUD.cs` provides a tactical 2D radar display in the top-right corner of the gameplay HUD.

---

## Features

- **Rotating Sweep**: Emulates a military radar sweep antenna.
- **Hostile Blips**: Tracks living zombies within radar radius (`35m`), displaying pulsing red blips.
- **Objective Tracker**: Points toward the active station or extraction bunker door.
