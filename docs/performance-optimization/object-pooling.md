---
layout: default
title: "Zero-Allocation Pooling"
parent: "Performance & Optimization"
nav_order: 1
---

# Zero-Allocation Object Pooling

Instantiating and destroying GameObjects during active combat causes heavy Garbage Collection (GC) pauses. `ObjectPoolManager.cs` pre-warms pools on scene load:

```csharp
// Fetch an impact decal without GC allocation
GameObject decal = ObjectPoolManager.Instance.SpawnFromPool("MetalDecal", hitPoint, Quaternion.LookRotation(hitNormal));
```
