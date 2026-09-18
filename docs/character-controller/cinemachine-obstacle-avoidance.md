---
layout: default
title: "Camera Collision Avoidance"
parent: "Character Controller"
nav_order: 3
---

# Camera Obstacle Avoidance

A common issue in third-person shooters is the camera clipping through walls, interior doorframes, or low ceilings. AS1 includes `Camera obstruction target` and procedural raycast spherecasting to prevent geometric clipping.

---

## How It Works

1. A multi-ray spherecast emanates from the player's `FPS Stable Eye` target towards the third-person camera pivot.
2. If any collision with layer `Obstacle` or `Default` is detected within the camera boom distance:
   - The camera boom dynamically shortens along the line of sight.
   - Smooth exponential damping prevents jarring pops when brushing against pillars or corners.
3. Once clear of geometry, the boom smoothly expands back to its resting distance (`2.8m`).
