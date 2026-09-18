---
layout: default
title: "AI & FSM API"
parent: "C# API Reference"
nav_order: 3
---

# AI & FSM API

### `BaseStateMachine`
- `public State CurrentState { get; }`
- `public AIData Data { get; }`
- `public NavMeshAgent Agent { get; }`
- `public void TransitionToState(State nextState)`

### `ZombieHitbox`
- `public float DamageMultiplier { get; set; }`
- `public bool IsHeadshot { get; }`
- `public void TakeDamage(float damage, Vector3 hitPoint, Vector3 hitDirection)`
