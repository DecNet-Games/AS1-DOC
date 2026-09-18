---
layout: default
title: "Managers API"
parent: "C# API Reference"
nav_order: 4
---

# Managers & Game Systems API

### `ObjectPoolManager`
- `public GameObject SpawnFromPool(string tag, Vector3 position, Quaternion rotation)`
- `public void ReturnToPool(string tag, GameObject objectToReturn)`

### `BunkerUnlockSystem`
- `public int RequiredKills { get; set; }`
- `public int CurrentKills { get; }`
- `public void RegisterKill()`
- `public event Action OnBunkerUnlocked`
