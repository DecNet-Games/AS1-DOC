---
layout: default
title: "Sensory Perception Engine"
parent: "Enemy AI & Pluggable FSM"
nav_order: 3
---

# Sensory Perception Engine

Zombies in AS1 navigate their environment using dual biological senses: **Vision** and **Hearing**.

---

## Visual Field-of-View (FOV)

`EnemyDetectionDecision.cs` calculates:
1. **Distance Check**: Is the player within `sightRange` (default: `18m`)?
2. **Angle Check**: Is the angle between enemy forward and vector-to-player within `sightFOV / 2` (default: `60?`)?
3. **Obstruction Raycast**: A raycast from the enemy's eye position to the player's chest confirms unblocked line-of-sight.

---

## Auditory Perception (`NoiseManager.cs`)

When firearms are discharged, grenades detonate, or the player sprints across resonant surfaces:
- A noise event is broadcast to `NoiseManager.TriggerNoise(Vector3 origin, float radius)`.
- All registered AI agents within `radius` receive the stimulus.
- Agents not currently chasing the player transition into the **Investigate** state to inspect the disturbance.
