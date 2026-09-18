---
layout: default
title: "Kill Streak & Combo Banners"
parent: "Combat Feedback & UI"
nav_order: 4
---

# Kill Streak & Combo Banners

`ComboStreakManager.cs` tracks fast consecutive eliminations, triggering animated HUD banners and voice announcer cues:

---

## Streak Thresholds

| Elimination Count | Window Duration | Banner Text | Color |
| :--- | :--- | :--- | :--- |
| **2 Kills** | 3.5s | `DOUBLE KILL` | Cyan |
| **3 Kills** | 3.5s | `TRIPLE KILL` | Orange |
| **4 Kills** | 3.5s | `MULTI KILL` | Purple |
| **5+ Kills** | 4.0s | `RAMPAGE!` | Flaming Red |
