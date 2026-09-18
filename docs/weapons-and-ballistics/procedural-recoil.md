---
layout: default
title: "Procedural Recoil"
parent: "Weapons & Ballistics"
nav_order: 3
---

# Procedural Recoil Engine

Rather than relying solely on pre-baked weapon animations, `ProceduralRecoil.cs` models physical spring-damper kickback directly on the weapon pivot and camera.

---

## Mathematical Formulation

Recoil is modeled as a damped harmonic oscillator:
- **Impulse**: When a shot is fired, an instantaneous velocity kick is added to `targetRotation` and `targetPosition`.
- **Damping**: In `Update()`, the rotation and position smoothly interpolate back to equilibrium `(Vector3.zero)` using `Mathf.Lerp` or `Vector3.Slerp`.

```csharp
// Excerpt from ProceduralRecoil.cs
public void FireRecoil()
{
    float kickV = Random.Range(minVerticalKick, maxVerticalKick);
    float kickH = Random.Range(-horizontalKick, horizontalKick);
    
    targetRotation += new Vector3(-kickV, kickH, Random.Range(-sideTilt, sideTilt));
    targetPosition += new Vector3(0f, 0f, -kickbackDepth);
}

void Update()
{
    targetRotation = Vector3.Lerp(targetRotation, Vector3.zero, returnSpeed * Time.deltaTime);
    currentRotation = Vector3.Slerp(currentRotation, targetRotation, snappiness * Time.fixedDeltaTime);
    transform.localRotation = Quaternion.Euler(currentRotation);
}
```
