---
layout: default
title: "Locomotion & Stamina"
parent: "Character Controller"
nav_order: 1
---

# Locomotion & Stamina System

Locomotion is handled by `PlayerMovement.cs` and tuned via `PlayerData.cs` ScriptableObjects.

---

## Locomotion States

| State | Speed | Stamina Drain Rate | Footstep Interval | Jump Allowed |
| :--- | :--- | :--- | :--- | :--- |
| **Walk** | 4.0 m/s | 0% (Regenerates) | 0.45s | Yes |
| **Sprint** | 7.5 m/s | 15% / sec | 0.28s | Yes |
| **Aim Down Sights (ADS)** | 2.5 m/s | 0% | 0.60s | No |
| **Airborne (Jump/Fall)** | Conserves Momentum | 10% instant cost | - | No |
| **Exhausted** | 3.0 m/s (Sprint Locked) | Regenerating to 25% threshold | 0.50s | Yes |

---

## Stamina Mechanics

Sprinting drains stamina continuously. When stamina drops to `0%`, the player enters an **Exhausted** state:
- Sprint is disabled until stamina recovers above the recovery threshold (default: `25%`).
- An exhaustion audio cue (heavy breathing) plays via the player audio source.
- Stamina begins regenerating after a short delay (`1.5s`) once sprint is released.

```csharp
// Excerpt from PlayerMovement.cs
if (isSprinting && currentStamina > 0f)
{
    currentStamina -= staminaDrainRate * Time.deltaTime;
    if (currentStamina <= 0f)
    {
        isExhausted = true;
        isSprinting = false;
    }
}
else if (!isSprinting && currentStamina < maxStamina)
{
    staminaRegenTimer += Time.deltaTime;
    if (staminaRegenTimer >= staminaRegenDelay)
    {
        currentStamina += staminaRegenRate * Time.deltaTime;
        if (currentStamina >= exhaustionThreshold)
            isExhausted = false;
    }
}
```
