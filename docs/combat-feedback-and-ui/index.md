---
layout: default
title: "Combat Feedback & UI"
nav_order: 7
has_children: true
permalink: /docs/combat-feedback-and-ui/
---

# Combat Feedback & UI Architecture

Tight combat feedback distinguishes satisfying shooters from sluggish ones. AS1 includes a comprehensive suite of sensory confirmation systems: reticle hit ticks, 3D floating damage numbers, directional threat arcs, streak banners, and real-time minimap radar.

---

## Feedback Loop

```mermaid
graph TD
    Impact[Bullet Hits Target] --> HitMarker[HitMarkerFeedback: Tick Audio & Reticle Flare]
    Impact --> HeadshotCheck{Is Headshot?}
    HeadshotCheck -- Yes --> RedMarker[Red Reticle & Critical Ping]
    HeadshotCheck -- No --> WhiteMarker[Standard White Reticle]
    
    Impact --> FloatingNum[FloatingDamageNumber: 3D World Billboard]
    
    ZombieAttack[Enemy Hits Player] --> ThreatArc[DamageIndicatorHUD: Peripheral Threat Arc]
    ZombieAttack --> Flash[HitFlashManager: Red Screen Vignette]
    
    Kill[Hostile Eliminated] --> Streak[ComboStreakManager: Multi-Kill Audio & HUD Banner]
    Kill --> Radar[MinimapRadarHUD: Remove Hostile Blip]
```

---

## Chapter Directory

1. [Hit Marker Feedback]({{ site.baseurl }}/docs/combat-feedback-and-ui/hit-markers/): Dynamic reticle bloom and hit sounds.
2. [Floating Damage Numbers]({{ site.baseurl }}/docs/combat-feedback-and-ui/floating-damage-numbers/): 3D billboarded floating damage indicators.
3. [Directional Damage Indicators]({{ site.baseurl }}/docs/combat-feedback-and-ui/directional-damage-indicator/): Threat arcs pointing toward attacker coordinates.
4. [Kill Streak & Combo Banners]({{ site.baseurl }}/docs/combat-feedback-and-ui/combo-streak-banner/): Multi-kill streaks and combo audio banners.
5. [Minimap & Radar System]({{ site.baseurl }}/docs/combat-feedback-and-ui/minimap-radar/): Dynamic 2D sweep tracking enemies and objectives.
6. [Contextual Prompts & Menus]({{ site.baseurl }}/docs/combat-feedback-and-ui/interact-prompts/): Interaction cues, pause menu, and game over screens.
