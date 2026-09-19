---
layout: default
title: "Installation & Licensing"
parent: "Getting Started"
nav_order: 1
---

# Installation & Licensing

> [!IMPORTANT]
> **Commercial Asset Store Exclusivity**:
> **AS1 ? Advanced Shooter System (TPS + FPS)** is a commercial asset sold exclusively on the official Unity Asset Store by Decnet Games. The source code and binary assets are protected under the standard Unity Asset Store End User License Agreement (EULA).
> 
> **This GitHub repository (`DecNet-Games/AS1-DOC`) is strictly for hosting documentation, issue tracking, and community discussions. It does NOT contain the commercial asset package or downloadable binaries.**

---

## System Requirements

| Specification | Minimum Requirement | Recommended |
| :--- | :--- | :--- |
| **Unity Version** | Unity 2022.3 LTS | Unity 6000.0+ (Tested on 6000.5.4f1) |
| **Render Pipeline** | Built-in Render Pipeline | Built-in or Universal Render Pipeline (URP) |
| **Target Platforms** | Windows, macOS, Android (Vulkan / GLES3), iOS (Metal) | Desktop PC, Mobile, Consoles |
| **Required Dependencies** | TextMesh Pro, Cinemachine | TextMesh Pro, Cinemachine 2.9+ / 3.0+ |

---

## Step-by-Step Package Import

### 1. Purchase & Add to My Assets
Acquire the **AS1 ? Advanced Shooter System** from Decnet Games on the official Unity Asset Store, and ensure the purchase is bound to your Unity Organization account.

### 2. Open Package Manager in Unity
1. Open your target Unity project.
2. In the top menu bar, click `Window > Package Manager`.
3. In the top-left dropdown of Package Manager, select **Packages: My Assets**.
4. In the search box, type `AS1` or `Ultimate Shooter Pack`.
5. Click **Download**, then click **Import**.

### 3. Package Importer Window
When the Unity Package Importer modal appears:
- Ensure all items in `Assets/AS1/` are checked.
- Ensure `Assets/TextMesh Pro/` resources are included if your project does not already have them.
- Click **Import**.

---

## First Startup & The Welcome Window

Upon importing AS1 into a project, the **AS1 Getting Started** setup wizard will open automatically.

![AS1 Getting Started Welcome Window]({{ site.baseurl }}/assets/images/welcome-window.png)

If the window does not appear automatically, launch it manually from:
```text
Tools > AS1 > Welcome
```

### Key Actions on First Startup:
- **Play the Demo**: Quick links to open `MainMenu.unity`, `TestingDemo.unity` (Day), or `TestingDemo_Night.unity` (Night).
- **Open AS1 Tool Suite**: Launches the central `Suite Hub` containing Project Doctor, Weapon Creator Pro, and AI Creator Pro.
- **Refresh Project Check**: Confirms all required physics layers, gameplay tags, and input axes are registered.

---

## Verifying Setup with Project Doctor

Before pressing play, always run **Project Doctor** to verify your project's configuration:

```text
Tools > AS1 > Suite Hub -> [Project Doctor]
```

![Project Doctor Diagnostics]({{ site.baseurl }}/assets/images/project-doctor.png)

Click **Scan & Refresh Diagnostics**. If any status card indicates an unconfigured layer, tag, or input axis, click **Auto-Fix All Issues** to apply the necessary ProjectSettings configurations automatically.
