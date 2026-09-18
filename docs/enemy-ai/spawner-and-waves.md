---
layout: default
title: "Zombie Spawner & Safe Zones"
parent: "Enemy AI & Pluggable FSM"
nav_order: 6
---

# Zombie Spawner & Safe Zones

Wave generation and sanctuary mechanics are managed by `ZombieSpawner.cs` and `SafeZone.cs`.

---

## Safe Zones

The Armory and extraction areas are tagged with `SafeZone.cs`:
- When the player is within the trigger volume, spawned zombies are barred from entering the perimeter.
- Provides a designated hub for testing weapons, calibrating loadouts, and reviewing objectives.
