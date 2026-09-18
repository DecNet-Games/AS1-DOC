---
layout: default
title: "Project Doctor"
parent: "AS1 Tool Suite"
nav_order: 2
---

# Project Doctor

Shooter projects fail at runtime when required physics layers, gameplay tags, or legacy input axes are missing from Unity's `ProjectSettings`. **Project Doctor** (`TabProjectDoctor.cs`) eliminates manual setup errors through automated scanning and single-click repairs.

![Project Doctor Diagnostics]({{ site.baseurl }}/assets/images/project-doctor.png)

---

## Validated Subsystems

| Diagnostic Card | Requirement Checked | Automatic Repair Action |
| :--- | :--- | :--- |
| **Required Tags** | Validates the presence of `Player`, `Enemy`, `Weapon`, `Ammo`, `Medikit`, `SafeZone`. | Appends missing tags into `ProjectSettings/TagManager.asset`. |
| **Required Layers** | Validates gameplay layers (`Player`, `Zombie`, `Bullet`, `Obstacle`) and surface audio layers (`Wood`, `Metal`, `Concrete`, `Dirt`, `Water`). | Assigns empty user layer slots and configures the 2D/3D physics collision matrix. |
| **Input Configuration** | Validates legacy input manager axes (`Horizontal`, `Vertical`, `Mouse X`, `Mouse Y`, `Fire1`, `Fire2`, `Jump`, `Reload`). | Automatically registers missing axes in `InputManager.asset` without overwriting existing mappings. |
| **Scenes in Build Settings** | Ensures `MainMenu`, `TestingDemo`, and `TestingDemo_Night` are indexed in `EditorBuildSettings`. | Adds missing scenes in the correct index order. |

---

## How to Run Diagnostics

1. Navigate to `Tools > AS1 > Suite Hub`.
2. Click the **[+] Project Doctor** tab.
3. Click **Scan & Refresh Diagnostics**.
4. If any cards show a red or yellow status warning, click **Auto-Fix All Issues**.
5. Project Doctor will write changes directly to project settings and notify you when all cards show `ONLINE / OK`.
