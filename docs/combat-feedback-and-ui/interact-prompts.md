---
layout: default
title: "Contextual Prompts & Menus"
parent: "Combat Feedback & UI"
nav_order: 6
---

# Contextual Prompts & Menus

UI prompts and menu management are handled by `InteractPromptUI.cs` and `GameMenuManager.cs`.

---

## World Prompts

When approaching interactive stations (Armory weapon racks, drill consoles, ammo crates):
- The prompt smoothly fades in: `[E] Pick up AK-47` or `[E] Start Zombie Drill`.
- On mobile devices, an on-screen contextual action button highlights automatically.
