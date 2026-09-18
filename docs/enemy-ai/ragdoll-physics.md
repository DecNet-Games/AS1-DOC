---
layout: default
title: "Dynamic Ragdoll Physics"
parent: "Enemy AI & Pluggable FSM"
nav_order: 5
---

# Dynamic Ragdoll Transition

When lethal damage is applied, `RagdollController.cs` transitions the character from Mecanim animation to full Newtonian physics.

---

## Transition Sequence

1. `NavMeshAgent.enabled = false`.
2. `Animator.enabled = false`.
3. Root `CapsuleCollider` is disabled so the corpse does not block player locomotion or bullets.
4. All child skeletal `Rigidbody.isKinematic` are set to `false`.
5. The fatal bullet's directional momentum is applied as an impulse force:
```csharp
hitRigidbody.AddForceAtPosition(hitDirection * impactForce, hitPoint, ForceMode.Impulse);
```
