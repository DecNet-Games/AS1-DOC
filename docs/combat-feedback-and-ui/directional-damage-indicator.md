---
layout: default
title: "Directional Threat Indicators"
parent: "Combat Feedback & UI"
nav_order: 3
---

# Directional Threat Indicators

When the operative takes damage from an off-screen enemy, `DamageIndicatorHUD.cs` displays an arched peripheral vignette pointing toward the threat.

---

## Angle Calculation

```csharp
Vector3 attackerDir = (attackerPosition - player.position).normalized;
float angle = Vector3.SignedAngle(player.forward, attackerDir, Vector3.up);
indicatorRect.localRotation = Quaternion.Euler(0, 0, -angle);
```
The threat arc fades over `1.8s` or updates dynamically if additional damage is sustained.
