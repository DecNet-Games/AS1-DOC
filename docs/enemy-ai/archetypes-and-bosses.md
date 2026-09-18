---
layout: default
title: "Enemy Archetypes & Variants"
parent: "Enemy AI & Pluggable FSM"
nav_order: 7
---

# Enemy Archetypes & Variants

AS1 ships with modular archetypes ready for deployment:

---

## Specialized Archetypes

### 1. Standard Walker
Balanced baseline enemy providing horde pressure. Moderate speed (`5.5 m/s`).

### 2. Fast Runner
High agility flanking specialist (`8.5 m/s`). Low HP (`60`), requiring quick target acquisition.

### 3. Explosive Zombie (`ExplosiveZombie.cs`)
A volatile suicide bomber:
- Rushes the player with an audible countdown fuse cue.
- Detonates on close proximity or upon death, dealing high radial area-of-effect damage to the player and surrounding props.
