---
layout: default
title: "URP Converter"
parent: "AS1 Tool Suite"
nav_order: 7
---

# URP Converter

AS1 ships acceptance-tested in the **Built-in Render Pipeline** for maximum out-of-the-box compatibility. When integrating into a **Universal Render Pipeline (URP)** project, materials rendered in pink need to be migrated to the `Universal Render Pipeline/Lit` shader.

The **URP Converter** (`TabURPConverter.cs` / `URPConverter.cs`) automates this process with zero asset corruption.

---

## Automated Safety Backup

Before modifying any shader on disk, the URP Converter creates a timestamped zip archive in:
```text
Assets/AS1/_Backup/Materials_PreURP_[Timestamp].zip
```
If you ever switch your project back to the Built-in pipeline, you can restore original materials in one click.

---

## 1-Click Conversion Steps

1. In Unity, ensure the URP package is installed and active in `ProjectSettings > Graphics`.
2. Open `Tools > AS1 > Suite Hub` -> **[URP] URP Converter**.
3. Click **Convert All Materials to URP**.
4. The converter scans all materials inside `Assets/AS1/Materials/` and `Assets/AS1/Showcase/Materials/`, converting standard `Standard` or `Autodesk Interactive` shaders to `Universal Render Pipeline/Lit`.
5. Albedo textures, normal maps, metallic/smoothness masks, and occlusion maps are preserved intact.
