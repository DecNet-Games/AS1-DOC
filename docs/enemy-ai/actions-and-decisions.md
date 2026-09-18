---
layout: default
title: "Actions & Decisions"
parent: "Enemy AI & Pluggable FSM"
nav_order: 2
---

# Actions & Decisions Library

AS1 includes pre-built modular actions and decision scripts:

---

## Pre-Built Actions

- **`PatrolAction.cs`**: Selects random waypoints within a radius or cycles through defined patrol anchors using `NavMeshAgent.SetDestination`.
- **`ChaseAction.cs`**: Updates pathing destination toward the player's world position at high chase velocity.
- **`AttackAction.cs`**: Triggers attack animations, faces the target, and invokes `MeleeAttack.cs` with cooldown timers.
- **`InvestigateAction.cs`**: Moves towards the last heard noise location reported by `NoiseManager`.

---

## Pre-Built Decisions

- **`EnemyDetectionDecision.cs`**: Returns `true` if the player is within sight cone FOV or within noise hearing radius.
- **`AttackDecision.cs`**: Returns `true` if the player distance is `<= attackRange` (e.g. `1.8m`).
