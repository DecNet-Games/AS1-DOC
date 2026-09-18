---
layout: default
title: "WeaponData Scriptable"
parent: "Weapons & Ballistics"
nav_order: 1
---

# WeaponData ScriptableObject

`WeaponData.cs` holds all immutable configuration data for firearms. This separation ensures that balancing weapon stats does not require modifying game scene prefabs or compiled code.

---

## Data Schema

```csharp
[CreateAssetMenu(fileName = "NewWeaponData", menuName = "AS1/Weapon Data")]
public class WeaponData : ScriptableObject
{
    [Header("Identity")]
    public string weaponName = "Assault Rifle";
    public Sprite weaponIcon;
    public FireMode fireMode = FireMode.Auto;

    [Header("Ballistics")]
    public float damage = 25f;
    public float fireRate = 0.1f;
    public float effectiveRange = 100f;
    public float bulletSpread = 0.8f;
    public int bulletsPerShot = 1; // Used for shotguns (e.g. 8 pellets)

    [Header("Ammunition")]
    public int magCapacity = 30;
    public int maxReserveAmmo = 120;
    public float reloadTime = 2.2f;
    public AmmoData ammoType;

    [Header("Procedural Recoil")]
    public float recoilVertical = 1.2f;
    public float recoilHorizontal = 0.4f;
    public float recoilRecovery = 0.15f;

    [Header("Audio")]
    public AudioClip shootSound;
    public AudioClip reloadSound;
    public AudioClip dryFireSound;
}
```
