---
layout: default
title: "Hitboxes & Weakpoints"
parent: "Enemy AI & Pluggable FSM"
nav_order: 4
---

# Hitboxes & Weakpoint Multipliers

Instead of a single capsule collider encompassing the entire character, AS1 equips each zombie with segmented `ZombieHitbox.cs` components across the skeletal hierarchy.

---

## Damage Multipliers

| Hitbox Segment | Collider Type | Damage Multiplier | Audio Feedback | UI Feedback |
| :--- | :--- | :--- | :--- | :--- |
| **Head** | SphereCollider | **2.5x** | Critical Headshot Chime | Red Reticle Marker + Gold Text |
| **Chest / Spine** | BoxCollider | **1.0x** (Base) | Flesh Impact Sound | Standard White Reticle Marker |
| **Arms / Hands** | CapsuleCollider | **0.7x** | Flesh Impact Sound | Standard White Reticle Marker |
| **Legs / Feet** | CapsuleCollider | **0.8x** | Flesh Impact Sound | Standard White Reticle Marker |

```csharp
// Excerpt from ZombieHitbox.cs
public void TakeDamage(float incomingDamage, Vector3 hitPoint, Vector3 hitDirection)
{
    float finalDamage = incomingDamage * damageMultiplier;
    parentHealth.ApplyDamage(finalDamage, isHeadshot, hitPoint, hitDirection);
}
```
