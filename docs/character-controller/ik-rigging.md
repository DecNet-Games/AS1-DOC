---
layout: default
title: "Inverse Kinematics (IK) Rigging"
parent: "Character Controller"
nav_order: 4
---

# Procedural Inverse Kinematics (IK)

AS1 uses `PlayerIkHelper.cs` and Unity Mecanim `OnAnimatorIK()` to ensure accurate weapon grip and sight alignment regardless of camera pitch.

---

## IK Passes

### 1. Two-Bone Left Hand Snapping
Every weapon prefab in AS1 contains a `LeftHandSocket` transform:
- During `OnAnimatorIK(int layerIndex)`, `PlayerIkHelper` queries the active weapon's socket.
- `SetIKPositionWeight` and `SetIKRotationWeight` for `AvatarIKGoal.LeftHand` are set to `1.0`.
- The operative's left hand snaps precisely to the foregrip or handguard, preventing hand floating across different weapon dimensions.

### 2. Spine & Head Pitch Look-At
When the player aims up or down:
- The spine and neck bones are rotated to align with the camera look vector.
- Rotation is clamped between `-60?` (looking down) and `+70?` (looking up) to prevent unnatural skeletal distortion.
