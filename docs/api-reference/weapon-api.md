---
layout: default
title: "Weapons & Ballistics API"
parent: "C# API Reference"
nav_order: 2
---

# Weapons & Ballistics API

### `Weapon`
- `public WeaponData Data { get; }`
- `public int CurrentMag { get; }`
- `public int CurrentReserve { get; }`
- `public bool CanFire { get; }`
- `public void Fire()`
- `public void StartReload()`
- `public void RefillAmmo(int amount)`

### `ProceduralRecoil`
- `public void FireRecoil()`
- `public void ResetRecoil()`
