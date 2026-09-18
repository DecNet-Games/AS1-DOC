---
layout: default
title: "Ammunition & Reloading"
parent: "Weapons & Ballistics"
nav_order: 6
---

# Ammunition & Reload Logic

AS1 manages ammunition via `AmmoManager.cs` and `PickUpAmmo.cs`.

---

## Tactical vs. Dry Reload

- **Tactical Reload**: Triggered when the magazine is depleted partially (`currentAmmo > 0`). Shorter reload duration since a round remains chambered.
- **Dry Reload**: Triggered when the magazine is empty (`currentAmmo == 0`). Slightly longer duration, requiring the operative to cycle the bolt or slide.

```csharp
public void Reload()
{
    int needed = weaponData.magCapacity - currentMag;
    int available = Mathf.Min(needed, currentReserve);
    
    currentMag += available;
    currentReserve -= available;
    UpdateHUD();
}
```
