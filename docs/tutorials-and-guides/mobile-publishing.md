---
layout: default
title: "Mobile Build & Publishing"
parent: "Tutorials & Guides"
nav_order: 4
---

# Mobile Build & Publishing Guide

1. Open `Build Settings` and switch platform to **Android** or **iOS**.
2. In `Player Settings > Other Settings`:
   - Set Graphics API to **Vulkan** or **Metal**.
   - Set Scripting Backend to **IL2CPP**.
   - Set Target Architectures to **ARM64**.
3. Enable `MobileControlToggle` to auto-activate the touch rig on mobile startup.
