---
layout: default
title: "Player Controller API"
parent: "C# API Reference"
nav_order: 1
---

# Player Controller API

### `PlayerMovement`
- `public float CurrentSpeed { get; }`
- `public bool IsGrounded { get; }`
- `public bool IsSprinting { get; }`
- `public float CurrentStamina { get; }`
- `public void SetMoveInput(Vector2 input)`

### `PlayerWeaponManager`
- `public Weapon ActiveWeapon { get; }`
- `public void SwitchWeapon(int slotIndex)`
- `public void EquipWeapon(WeaponData data)`
