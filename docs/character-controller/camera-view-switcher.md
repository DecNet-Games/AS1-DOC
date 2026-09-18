---
layout: default
title: "FPS / TPS Hybrid Camera"
parent: "Character Controller"
nav_order: 2
---

# Seamless FPS / TPS Hybrid Camera

AS1 allows players to toggle instantly between **First-Person (FPS)** and **Third-Person (TPS)** views via `ViewSwitcher.cs` by pressing `V` (or tapping the HUD toggle on mobile).

---

## Priority Blending Architecture

The camera system uses Unity Cinemachine virtual cameras:
- `ThirdPersonCamera` (Priority: `10` default)
- `CM_FPSCam` (Priority: `5` default)
- `AimCamera` (Dynamic ADS zoom camera, Priority: `15` when aiming)

When toggling to FPS:
1. `CM_FPSCam` priority elevates to `20`.
2. Cinemachine smoothly interpolates the position and field of view.
3. Player mesh cull mask is toggled: in FPS, the player's head and body mesh are hidden from the primary eye camera while shadow casters remain active.
4. Weapon models switch to first-person viewport offsets for optimal screen real-estate.

```csharp
// Excerpt from ViewSwitcher.cs
public void ToggleView()
{
    isFirstPerson = !isFirstPerson;
    if (isFirstPerson)
    {
        fpsVirtualCamera.Priority = 20;
        tpsVirtualCamera.Priority = 5;
        SetFirstPersonMeshVisibility(false);
    }
    else
    {
        fpsVirtualCamera.Priority = 5;
        tpsVirtualCamera.Priority = 20;
        SetFirstPersonMeshVisibility(true);
    }
}
```
