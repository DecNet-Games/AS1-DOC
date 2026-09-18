---
layout: default
title: "Welcome Wizard"
parent: "AS1 Tool Suite"
nav_order: 1
---

# AS1 Getting Started Wizard

The **AS1 Getting Started** window (`DecnetWelcomeWindow.cs`) provides immediate onboarding when the package is imported or when opened via `Tools > AS1 > Welcome`.

![AS1 Getting Started Welcome Window]({{ site.baseurl }}/assets/images/welcome-window.png)

---

## Key Capabilities

### 1. Play The Demo Shortcuts
- **Open Main Menu**: Loads `Assets/AS1/Scenes/MainMenu.unity` with interactive scene selector.
- **Day Proving Grounds**: Loads `Assets/AS1/Scenes/TestingDemo.unity` directly into the editor.
- **Night Proving Grounds**: Loads `Assets/AS1/Scenes/TestingDemo_Night.unity` with active nocturnal lighting.

### 2. Authoring Quick-Access
- **Open AS1 Tool Suite**: Immediately opens the docked `Suite Hub` window.

### 3. Project Diagnostics Check
- Displays the real-time health of tags, layers, input axes, and registered scenes.
- **Refresh Project Check**: Re-evaluates configuration status on demand.
- **Open Demo Guide**: Opens the packaged technical documentation PDF.

> [!TIP]
> Check the **"Do not show this window on project startup"** box in the lower-left corner if you do not want the wizard to pop up whenever you open Unity. You can reopen it at any time from `Tools > AS1 > Welcome`.
