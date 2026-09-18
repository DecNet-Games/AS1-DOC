---
layout: default
title: "FAQ & Troubleshooting"
nav_order: 13
permalink: /docs/faq/
---

# Frequently Asked Questions & Troubleshooting

---

### Q: Does the package include the source code?
**A:** Yes. All C# scripts are 100% full source code with zero DLL black boxes.

---

### Q: Why is this GitHub repository empty of Unity code?
**A:** **AS1 - Ultimate Shooter Pack (PRO)** is a commercial product sold exclusively on the official Unity Asset Store by DecNet Games. Under the standard Unity Asset Store EULA, raw asset binaries and source files cannot be distributed publicly on GitHub. This repository exists solely to host technical documentation, tutorials, and community issue tracking.

---

### Q: The demo scene throws missing reference or layer errors on play?
**A:** Open `Tools > AS1 > Suite Hub` and select the **[+] Project Doctor** tab. Click **Scan & Refresh Diagnostics**, then click **Auto-Fix All Issues**. Project Doctor will automatically configure missing layers, tags, and input axes in your project's settings.

---

### Q: How do I switch between PC keyboard/mouse and Mobile touch controls?
**A:** During gameplay, check or uncheck the **TOUCH CONTROLS** checkbox in the top-right corner of the HUD, or toggle `mobileControl` on the `GameManager` component.

---

### Q: Can I use my own character models with AS1?
**A:** Yes. Any standard humanoid model compatible with Unity Mecanim can be bound to the player controller or converted into an enemy using **AI Creator Pro**.

---

### Q: How do I convert materials to URP (Universal Render Pipeline)?
**A:** After installing URP in your project, open `Tools > AS1 > Suite Hub` -> **[URP] URP Converter** and click **Convert All Materials to URP**. An automated safety backup of all materials will be saved in `Assets/AS1/_Backup/`.

---

### Q: Where can I get official support or request features?
**A:** Reach out through DecNet Games official channels or our YouTube channel: [https://www.youtube.com/@decnetgames](https://www.youtube.com/@decnetgames).
